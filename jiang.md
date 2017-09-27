

// Cmfc4App message handlers

void GetText(CWnd* cwnd , char* buff, int nBuff) {
	cwnd->GetWindowTextW((LPTSTR)buff, nBuff);
	
}
void SetText(CWnd* cwnd , char* buff) {
	SetWindowTextW(cwnd->m_hWnd, (LPCWSTR) buff);
}

#define IDD_INPUTFILEDIALOG         701
#define IDC_FILENAME                702
#define IDCONVERT                   703
#define ID_TASKS_2					710
#define ID_TASKS_3					711


IDD_INPUTFILEDIALOG DIALOGEX 0, 0, 375, 65
STYLE DS_SETFONT | DS_MODALFRAME | DS_FIXEDSYS | WS_POPUP | WS_CAPTION | WS_SYSMENU
CAPTION "Task 2"
FONT 8, "MS Shell Dlg", 400, 0, 0x1
BEGIN
    PUSHBUTTON      "Cancel",IDCANCEL,318,44,50,14
    CONTROL         "Please input case Number\n(Place csv file as c:\\abc.csv), output file will be found in executable/project directory)",IDC_STATIC,
                    "Static",SS_SIMPLE | WS_GROUP,7,7,361,32
    EDITTEXT        IDC_FILENAME,15,44,246,14,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "Convert",IDCONVERT,265,44,50,14
END
