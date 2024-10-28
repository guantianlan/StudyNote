[> 前提要求，window 端需要安装 x11

连接 docker 容器后输入下行指令安装 wxWidgets

```bash
apt install libwxgtk3.2-gtk3-dev
```

创建 helloworld. cpp

编写 helloworld. cpp，输入官方 hello world 示例示例

```c++
// Start of wxWidgets "Hello World" Program
#include <wx/wx.h>
 
class MyApp : public wxApp
{
public:
    bool OnInit() override;
};
 
wxIMPLEMENT_APP(MyApp);
 
class MyFrame : public wxFrame
{
public:
    MyFrame();
 
private:
    void OnHello(wxCommandEvent& event);
    void OnExit(wxCommandEvent& event);
    void OnAbout(wxCommandEvent& event);
};
 
enum
{
    ID_Hello = 1
};
 
bool MyApp::OnInit()
{
    MyFrame *frame = new MyFrame();
    frame->Show(true);
    return true;
}
 
MyFrame::MyFrame()
    : wxFrame(nullptr, wxID_ANY, "Hello World")
{
    wxMenu *menuFile = new wxMenu;
    menuFile->Append(ID_Hello, "&Hello...\tCtrl-H",
                     "Help string shown in status bar for this menu item");
    menuFile->AppendSeparator();
    menuFile->Append(wxID_EXIT);
 
    wxMenu *menuHelp = new wxMenu;
    menuHelp->Append(wxID_ABOUT);
 
    wxMenuBar *menuBar = new wxMenuBar;
    menuBar->Append(menuFile, "&File");
    menuBar->Append(menuHelp, "&Help");
 
    SetMenuBar( menuBar );
 
    CreateStatusBar();
    SetStatusText("Welcome to wxWidgets!");
 
    Bind(wxEVT_MENU, &MyFrame::OnHello, this, ID_Hello);
    Bind(wxEVT_MENU, &MyFrame::OnAbout, this, wxID_ABOUT);
    Bind(wxEVT_MENU, &MyFrame::OnExit, this, wxID_EXIT);
}
 
void MyFrame::OnExit(wxCommandEvent& event)
{
    Close(true);
}
 
void MyFrame::OnAbout(wxCommandEvent& event)
{
    wxMessageBox("This is a wxWidgets Hello World example",
                 "About Hello World", wxOK | wxICON_INFORMATION);
}
 
void MyFrame::OnHello(wxCommandEvent& event)
{
    wxLogMessage("Hello world from wxWidgets!");
}
```

编写完成后输入下行指令进行编译
```bash
g++ hello_world.cpp `wx-config --cxxflags --libs` -o hello_world
```

运行编译后的文件

```bash
./hello_world
```

# 拓展：

```c++
#include <wx/wx.h>

#include <wx/filedlg.h>

#include <fstream>

#include <sstream>

#include <vector>

#include <string>

// 进程数据结构体

struct ProcessData {

    std::string processName;

    double computationTime;

    double ioTime;

};

// 读取 CSV 文件的函数

std::vector<ProcessData> readCSV(const std::string& filename) {

    std::vector<ProcessData> data;

    std::ifstream file(filename);

    if (!file.is_open()) {

        wxLogError("Could not open the file!");

        return data;

    }

    std::string line;

    while (std::getline(file, line)) {

        std::stringstream ss(line);

        ProcessData processData;

        std::getline(ss, processData.processName, ',');

        ss >> processData.computationTime;

        ss.ignore(1); // 忽略逗号

        ss >> processData.ioTime;

        data.push_back(processData);

    }

    file.close();

    return data;

}

// 面板类，用于绘图

class MyPanel : public wxPanel {

public:

    MyPanel(wxWindow* parent)

        : wxPanel(parent, wxID_ANY), processData() {}

    void setProcessData(const std::vector<ProcessData>& data) {

        processData = data;

        Refresh();  // 重新绘制

    }

private:

    std::vector<ProcessData> processData;

    void OnPaint(wxPaintEvent& evt) {

        wxPaintDC dc(this);

        dc.Clear();  // 清除之前的绘图

        dc.SetBrush(*wxGREEN_BRUSH);

        dc.SetPen(wxPen(wxColor(0, 0, 0), 1));

        int x = 50;

        int y = 50;

        for (const auto& process : processData) {

            // 绘制计算阶段

            dc.DrawRectangle(x, y, process.computationTime * 10, 50);

            x += process.computationTime * 10;

            // 绘制 I/O 阶段

            dc.DrawRectangle(x, y, process.ioTime * 10, 50);

            x += process.ioTime * 10;

            y += 70;  // 下一个进程的位置

            x = 50;

        }

    }

    DECLARE_EVENT_TABLE()

};

BEGIN_EVENT_TABLE(MyPanel, wxPanel)

    EVT_PAINT(MyPanel::OnPaint)

END_EVENT_TABLE()

// 主窗口类

class MyFrame : public wxFrame {

public:

    MyFrame() : wxFrame(NULL, wxID_ANY, "Process Execution Diagram") {

        panel = new MyPanel(this);

        wxBoxSizer* sizer = new wxBoxSizer(wxVERTICAL);

        wxButton* openButton = new wxButton(this, wxID_OPEN, "Open CSV File");

        sizer->Add(openButton, 0, wxALL | wxCENTER, 10);

        sizer->Add(panel, 1, wxEXPAND | wxALL, 10);

        SetSizer(sizer);

        SetSize(wxSize(600, 400));

        Bind(wxEVT_BUTTON, &MyFrame::OnOpenFile, this, wxID_OPEN);

    }

private:

    MyPanel* panel;

    void OnOpenFile(wxCommandEvent& event) {

        wxFileDialog openFileDialog(

            this, _("Open CSV file"), "", "",

            "CSV files (*.csv)|*.csv", wxFD_OPEN | wxFD_FILE_MUST_EXIST);

        if (openFileDialog.ShowModal() == wxID_CANCEL)

            return; // 用户取消了选择

        std::string filename = openFileDialog.GetPath().ToStdString();

        auto data = readCSV(filename);

        panel->setProcessData(data);

    }

};

// 应用类

class MyApp : public wxApp {

public:

    virtual bool OnInit() {

        MyFrame* frame = new MyFrame();

        frame->Show(true);

        return true;

    }

};

wxIMPLEMENT_APP(MyApp);
```

创建 csv 文件

```bash
vim test.csv
```

```bash
Process1,10.5,3.2

Process2,7.8,2.5

Process3,12.3,4.1

Process4,9.6,3.8

Process5,6.9,2.0
```

