
```C++
//确定头文件的包含逻辑，不要包含不需要的MFC内容
#define WIN32_LEAN_AND_MEAN

//所有的Windows头文件
#include <windows.h>
//包含许多重要的宏和常量的头文件
#include <windowsx.h>

//Windows应用程序的主要入口
/*
	WINAPI声明符等同于Pascal函数声明符，强制参数从左到右传递
	hinstance：Windows为应用程序生成的实例句柄，实例是用来跟踪资源的指针或数
	hprevinstance：该参数已经不在使用，在Windows的旧版本中跟踪应用程序以前的实例，就是产生当前实例的应用程序实例
	lpcmdline：空值终止字符串
	ncmdshow：启动过程中被传递给应用程序，带有如何打开主应用程序窗口的信息
*/
int WINAPI WinMain(HINSTANCE hinstance, HINSTANCE hprevinstance, LPSTR lpcmdline, int ncmdshow)
{
	//Win32 API函数：在屏幕上显示一个窗口
	/*
		int MessageBox(
		  [in, optional] HWND    hWnd,		//要创建的消息框的所有者窗口的句柄
		  [in, optional] LPCTSTR lpText,	//要显示的消息
		  [in, optional] LPCTSTR lpCaption,	//对话框标题
		  [in]           UINT    uType		//对话框的内容和行为
		);

		MB_OK:					消息框包含一个按钮： 确定。 这是默认值
		MB_ICONEXCLAMATION:		消息框中会显示一个感叹号图标。

	*/
	MessageBox(NULL, (LPCWSTR)L"There can be only one", (LPCWSTR)L"My first window program", MB_OK | MB_ICONEXCLAMATION);
	return 0;
}
```