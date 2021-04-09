---
title: Использование диалоговых окон
description: Используйте диалоговые окна для вывода сведений и запроса ввода от пользователя.
ms.assetid: 8a5b6bdd-4429-4f48-b846-6bd617a87abf
keywords:
- Пользовательский интерфейс Windows, окна
- Пользовательский интерфейс Windows, диалоговые окна
- окна, диалоговые окна
- диалоговые окна, сведения
- диалоговые окна, отображение
- модальные диалоговые окна
- безрежимные диалоговые окна
- диалоговые окна, модальные
- диалоговые окна, немодальные
- диалоговые окна, инициализация
- шаблоны диалоговых окон
- диалоговые окна, шаблоны
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21da47d7d59f4cadc21314566bce41a9ef3456a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070433"
---
# <a name="using-dialog-boxes"></a>Использование диалоговых окон

Используйте диалоговые окна для вывода сведений и запроса ввода от пользователя. Приложение загружает и Инициализирует диалоговое окно, обрабатывает входные данные пользователя и уничтожает диалоговое окно, когда пользователь завершает задачу. Процесс обработки диалоговых окон зависит от того, является ли диалоговое окно модальным или немодальным. Модальное диалоговое окно требует, чтобы пользователь закрыл диалоговое окно перед активацией другого окна в приложении. Однако пользователь может активировать Windows в разных приложениях. Немодальное диалоговое окно не требует немедленного ответа от пользователя. Он аналогичен главному окну, содержащему элементы управления.

В следующих разделах описывается использование обоих типов диалоговых окон.

-   [Отображение окна сообщения](#displaying-a-message-box)
-   [Создание модального диалогового окна](#creating-a-modal-dialog-box)
-   [Создание немодального диалогового окна](#creating-a-modeless-dialog-box)
-   [Инициализация диалогового окна](#initializing-a-dialog-box)
-   [Создание шаблона в памяти](#creating-a-template-in-memory)

## <a name="displaying-a-message-box"></a>Отображение окна сообщения

Простейшей формой модального диалогового окна является окно сообщения. Большинство приложений используют окна сообщений для предупреждения пользователя об ошибках и для запроса инструкций о том, как продолжать работу после возникновения ошибки. Создайте окно сообщения с помощью функции [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) или [**мессажебоксекс**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) , указав сообщение и число и тип отображаемых кнопок. Система создает модальное диалоговое окно, предоставляя собственный шаблон и процедуру диалогового окна. После того, как пользователь закроет окно сообщения, **MessageBox** или **мессажебоксекс** возвращает значение, идентифицирующее кнопку, выбранную пользователем, чтобы закрыть окно сообщения.

В следующем примере приложение отображает окно сообщения, предлагающее пользователю ввести действие после возникновения ошибки. В окне сообщения отобразится сообщение с описанием условия ошибки и способами ее устранения. **\_ Данет** в стиле "МБ" направляет [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) для предоставления двух кнопок, с помощью которых пользователь может выбрать способ продолжения:


```
int DisplayConfirmSaveAsMessageBox()
{
    int msgboxID = MessageBox(
        NULL,
        L"temp.txt already exists.\nDo you want to replace it?",
        L"Confirm Save As",
        MB_ICONEXCLAMATION | MB_YESNO
    );

    if (msgboxID == IDYES)
    {
        // TODO: add code
    }

    return msgboxID;    
}
```



На следующем рисунке показаны выходные данные предыдущего примера кода:

![окно сообщения](images/messagebox-01.png)

## <a name="creating-a-modal-dialog-box"></a>Создание модального диалогового окна

Модальное диалоговое окно создается с помощью функции [**диалогбокс**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) . Необходимо указать идентификатор или имя ресурса шаблона диалогового окна и указатель на процедуру диалогового окна. Функция **диалогбокс** загружает шаблон, отображает диалоговое окно и обрабатывает все входные данные пользователя до тех пор, пока пользователь не закроет диалоговое окно.

В следующем примере приложение отображает модальное диалоговое окно, когда пользователь нажимает кнопку " **удалить элемент** " из меню приложения. Диалоговое окно содержит элемент управления "поле ввода" (в котором пользователь вводит имя элемента) и кнопки  "ОК **" и "Отмена"** . Идентификаторы элементов управления для этих элементов управления имеют ИДЕНТИФИКАТОРы \_ ITEMNAME, идок и идканцел соответственно.

Первая часть примера состоит из инструкций, которые создают модальное диалоговое окно. Эти инструкции в процедуре окна для главного окна приложения создают диалоговое окно, когда система получает сообщение [**\_ команды WM**](/windows/desktop/menurc/wm-command) с \_ идентификатором меню IDM DELETEITEM. Во второй части примера показана процедура диалогового окна, которая извлекает содержимое элемента управления "поле ввода" и закрывает диалоговое окно при получении **\_ командного сообщения WM** .

Следующие инструкции создают модальное диалоговое окно. Шаблон диалогового окна — это ресурс в исполняемом файле приложения с идентификатором ресурса DLG \_ DELETEITEM.


```
case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_DELETEITEM: 
            if (DialogBox(hinst, 
                          MAKEINTRESOURCE(DLG_DELETEITEM), 
                          hwnd, 
                          (DLGPROC)DeleteItemProc)==IDOK) 
            {
                // Complete the command; szItemName contains the 
                // name of the item to delete. 
            }

            else 
            {
                // Cancel the command. 
            } 
            break; 
    } 
    return 0L; 
```



В этом примере приложение указывает его главное окно в качестве окна "владелец" для диалогового окна. Когда система первоначально отображает диалоговое окно, его расположение задается относительно верхнего левого угла клиентской области окна-владельца. Приложение использует возвращаемое значение из [**диалогбокс**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) , чтобы определить, следует ли продолжить операцию или отменить ее. В следующих инструкциях определяется процедура диалогового окна.


```
char szItemName[80]; // receives name of item to delete. 
 
BOOL CALLBACK DeleteItemProc(HWND hwndDlg, 
                             UINT message, 
                             WPARAM wParam, 
                             LPARAM lParam) 
{ 
    switch (message) 
    { 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    if (!GetDlgItemText(hwndDlg, ID_ITEMNAME, szItemName, 80)) 
                         *szItemName=0; 
 
                    // Fall through. 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, wParam); 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



В этом примере процедура использует [**жетдлгитемтекст**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) для получения текущего текста из элемента управления Edit, идентифицируемого по идентификатору \_ ITEMNAME. Затем процедура вызывает функцию [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) для задания возвращаемого значения диалогового окна как ИДОК или идканцел, в зависимости от полученного сообщения и для начала процесса закрытия диалогового окна. Идентификаторы ИДОК и ИДКАНЦЕЛ соответствуют кнопкам **ОК** и **Отмена** . После вызова метода **EndDialog** система отправляет дополнительные сообщения в процедуру для уничтожения диалогового окна и возвращает обратное значение диалогового окна функции, создавшей диалоговое окно.

## <a name="creating-a-modeless-dialog-box"></a>Создание немодального диалогового окна

Можно создать немодальное диалоговое окно с помощью функции [**креатедиалог**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) , указав идентификатор или имя ресурса шаблона диалогового окна, а также указатель на процедуру диалогового окна. **Креатедиалог** загружает шаблон, создает диалоговое окно и при необходимости отображает его. Приложение отвечает за получение и отправку сообщений о вводе пользователем в процедуру диалогового окна.

В следующем примере приложение отображает немодальное диалоговое окно (если оно еще не отображается), когда пользователь щелкает **"переход к** " из меню приложения. Диалоговое окно содержит элемент управления "поле ввода", флажок, а также кнопки " **ОК** " и **"Отмена"** . Шаблон диалогового окна — это ресурс в исполняемом файле приложения с идентификатором ресурса DLG \_ goto. Пользователь вводит номер строки в элементе управления "поле ввода" и устанавливает флажок, чтобы указать, что номер строки относится к текущей строке. Идентификаторы элементов управления: \_ line ID, ID \_ АБСРЕЛ, ИДОК и идканцел.

Инструкции в первой части примера создают немодальное диалоговое окно. Эти инструкции в процедуре окна для главного окна приложения создают диалоговое окно, когда процедура окна получает сообщение [**\_ команды WM**](/windows/desktop/menurc/wm-command) с \_ идентификатором меню IDM, но только в том случае, если глобальная переменная еще не содержит допустимый обработчик. Вторая часть примера — основной цикл обработки сообщений приложения. Цикл включает функцию [**исдиалогмессаже**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) , чтобы убедиться, что пользователь может использовать интерфейс клавиатуры диалогового окна в этом немодальном диалоговом окне. В третьей части примера приведена процедура диалогового окна. Процедура извлекает содержимое элемента управления "поле ввода" и флажка, когда пользователь нажимает кнопку " **ОК** ". Процедура уничтожает диалоговое окно, когда пользователь нажимает кнопку **Отмена** .


```
HWND hwndGoto = NULL;  // Window handle of dialog box 
                
...

case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_GOTO: 
            if (!IsWindow(hwndGoto)) 
            { 
                hwndGoto = CreateDialog(hinst, 
                                        MAKEINTRESOURCE(DLG_GOTO), 
                                        hwnd, 
                                        (DLGPROC)GoToProc); 
                ShowWindow(hwndGoto, SW_SHOW); 
            } 
            break; 
    } 
    return 0L; 
```



В приведенных выше инструкциях [**креатедиалог**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) вызывается, только если не `hwndGoto` содержит допустимый обработчик окна. Это гарантирует, что приложение не будет одновременно отображать два диалоговых окна. Для поддержки этого метода процедура диалогового окна должна иметь значение **null** при уничтожении диалогового окна.

Цикл обработки сообщений для приложения состоит из следующих инструкций.


```
BOOL bRet;

while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0) 
{ 
    if (bRet == -1)
    {
        // Handle the error and possibly exit
    }
    else if (!IsWindow(hwndGoto) || !IsDialogMessage(hwndGoto, &msg)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
} 
```



Цикл проверяет допустимость диалогового окна в диалоговом окне и вызывает функцию [**исдиалогмессаже**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) только в том случае, если этот маркер является допустимым. **Исдиалогмессаже** обрабатывает сообщение только в том случае, если оно принадлежит диалоговому окну. В противном случае возвращается **значение false** , и цикл отправляет сообщение в соответствующее окно.

В следующих инструкциях определяется процедура диалогового окна.


```
int iLine;             // Receives line number.
BOOL fRelative;        // Receives check box status. 
 
BOOL CALLBACK GoToProc(HWND hwndDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    BOOL fError; 
 
    switch (message) 
    { 
        case WM_INITDIALOG: 
            CheckDlgButton(hwndDlg, ID_ABSREL, fRelative); 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    fRelative = IsDlgButtonChecked(hwndDlg, ID_ABSREL); 
                    iLine = GetDlgItemInt(hwndDlg, ID_LINE, &fError, fRelative); 
                    if (fError) 
                    { 
                        MessageBox(hwndDlg, SZINVALIDNUMBER, SZGOTOERR, MB_OK); 
                        SendDlgItemMessage(hwndDlg, ID_LINE, EM_SETSEL, 0, -1L); 
                    } 
                    else 

                    // Notify the owner window to carry out the task. 
 
                    return TRUE; 
 
                case IDCANCEL: 
                    DestroyWindow(hwndDlg); 
                    hwndGoto = NULL; 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



В приведенных выше инструкциях процедура обрабатывает сообщения [**\_ командной строки**](/windows/desktop/menurc/wm-command) [**WM \_ инитдиалог**](wm-initdialog.md) и WM. Во время обработки **\_ Инитдиалог в WM** процедура Инициализирует этот флажок, передавая текущее значение глобальной переменной в [**чеккдлгбуттон**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx). Затем процедура возвращает **значение true** , чтобы система настроила фокус ввода по умолчанию.

Во время обработки [**\_ команд WM**](/windows/desktop/menurc/wm-command) это диалоговое окно закрывается только в том случае, если пользователь нажмет кнопку **Отмена** , то есть кнопку с идентификатором идканцел. Процедура должна вызвать [**дестройвиндов**](/windows/desktop/api/winuser/nf-winuser-destroywindow) , чтобы закрыть немодальное диалоговое окно. Обратите внимание, что процедура также задает для переменной **значение NULL** , чтобы убедиться, что другие инструкции, зависящие от этой переменной, работают правильно.

Если пользователь нажмет кнопку **ОК** , процедура получает текущее состояние флажка и назначает его переменной **фрелативе** . Затем она использует переменную для получения номера строки из элемента управления Edit. [**Жетдлгитеминт**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) преобразует текст в элементе управления "поле ввода" в целое число. Значение **фрелативе** определяет, интерпретирует ли функция число как значение со знаком или без знака. Если текст элемента управления "поле ввода" не является допустимым числом, **жетдлгитеминт** устанавливает значение переменной **fError** равным нулю. Процедура проверяет это значение, чтобы определить, следует ли отображать сообщение об ошибке или выполнить задачу. В случае ошибки процедура диалогового окна отправляет сообщение в элемент управления редактированием, направляя его для выбора текста в элементе управления, чтобы пользователь мог легко его заменить. Если **жетдлгитеминт** не возвращает ошибку, процедура может либо выполнить запрошенную задачу, либо отправить сообщение в окно владельца, направляя его для выполнения операции.

## <a name="initializing-a-dialog-box"></a>Инициализация диалогового окна

Вы Инициализирует диалоговое окно и его содержимое при обработке сообщения [**WM \_ инитдиалог**](wm-initdialog.md) . Наиболее распространенной задачей является инициализация элементов управления для отражения текущих настроек диалогового окна. Другой распространенной задачей является центрирование диалогового окна на экране или в окне его владельца. Полезной задачей для некоторых диалоговых окон является установка фокуса ввода на указанный элемент управления вместо принятия фокуса ввода по умолчанию.

В следующем примере диалоговое окно обрабатывает диалоговое окно и устанавливает фокус ввода при обработке сообщения [**WM \_ инитдиалог**](wm-initdialog.md) . Для центрирования диалогового окна процедура извлекает прямоугольники окна для диалогового окна и окна владелец и вычисляет новую точку для диалогового окна. Чтобы установить фокус ввода, процедура проверяет параметр *wParam* , чтобы определить идентификатор фокуса ввода по умолчанию.


```
HWND hwndOwner; 
RECT rc, rcDlg, rcOwner; 

....
 
case WM_INITDIALOG: 

    // Get the owner window and dialog box rectangles. 

    if ((hwndOwner = GetParent(hwndDlg)) == NULL) 
    {
        hwndOwner = GetDesktopWindow(); 
    }

    GetWindowRect(hwndOwner, &rcOwner); 
    GetWindowRect(hwndDlg, &rcDlg); 
    CopyRect(&rc, &rcOwner); 

    // Offset the owner and dialog box rectangles so that right and bottom 
    // values represent the width and height, and then offset the owner again 
    // to discard space taken up by the dialog box. 

    OffsetRect(&rcDlg, -rcDlg.left, -rcDlg.top); 
    OffsetRect(&rc, -rc.left, -rc.top); 
    OffsetRect(&rc, -rcDlg.right, -rcDlg.bottom); 

    // The new position is the sum of half the remaining space and the owner's 
    // original position. 

    SetWindowPos(hwndDlg, 
                 HWND_TOP, 
                 rcOwner.left + (rc.right / 2), 
                 rcOwner.top + (rc.bottom / 2), 
                 0, 0,          // Ignores size arguments. 
                 SWP_NOSIZE); 

    if (GetDlgCtrlID((HWND) wParam) != ID_ITEMNAME) 
    { 
        SetFocus(GetDlgItem(hwndDlg, ID_ITEMNAME)); 
        return FALSE; 
    } 
    return TRUE; 
```



В приведенных выше инструкциях процедура [**использует функцию getHandler**](/windows/desktop/api/winuser/nf-winuser-getparent) для получения маркера окна-владельца для диалогового окна. Функция возвращает обработчик окна владельца в диалоговые окна, а родительский окно — в дочерние окна. Поскольку приложение может создать диалоговое окно, не имеющее владельца, процедура проверяет возвращенный обработчик и использует функцию [**жетдесктопвиндов**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) для получения маркера окна рабочего стола при необходимости. После вычисления новой должности процедура использует функцию [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) для перемещения диалогового окна, указывая \_ верхнее значение HWND, чтобы убедиться, что диалоговое окно остается в верхней части окна владельца.

Перед установкой фокуса ввода процедура проверяет идентификатор элемента управления фокуса ввода по умолчанию. Система передает маркер окна фокуса ввода по умолчанию в параметре *wParam* . Функция [**жетдлгктрлид**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) возвращает идентификатор элемента управления, идентифицируемого маркером окна. Если идентификатор не соответствует правильному идентификатору, процедура использует функцию [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) для установки фокуса ввода. Функция [**жетдлгитем**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) необходима для получения маркера окна требуемого элемента управления.

## <a name="creating-a-template-in-memory"></a>Создание шаблона в памяти

Приложения иногда адаптируют или изменяют содержимое диалоговых окон в зависимости от текущего состояния обрабатываемых данных. В таких случаях нецелесообразно предоставлять все возможные шаблоны диалоговых окон в качестве ресурсов исполняемого файла приложения. Но создание шаблонов в памяти обеспечивает большую гибкость при адаптации к любым обстоятельствам.

В следующем примере приложение создает шаблон в памяти для модального диалогового окна, содержащего сообщение и кнопки « **ОК** » и « **Справка** ».

В шаблоне диалогового окна все символьные строки, например диалоговые окна и заголовки кнопок, должны быть строками в Юникоде. В этом примере используется функция [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) для создания этих строк Юникода.

Структуры [**длгитемтемплате**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) в шаблоне диалогового окна должны быть согласованы по границам **DWORD** . Чтобы выстроить эти структуры, в этом примере используется вспомогательная подпрограммы, которая принимает входной указатель и возвращает ближайший указатель, выравниваемая по границе **DWORD** .


```
#define ID_HELP   150
#define ID_TEXT   200

LPWORD lpwAlign(LPWORD lpIn)
{
    ULONG ul;

    ul = (ULONG)lpIn;
    ul ++;
    ul >>=1;
    ul <<=1;
    return (LPWORD)ul;
}

LRESULT DisplayMyMessage(HINSTANCE hinst, HWND hwndOwner, LPSTR lpszMessage)
{
    HGLOBAL hgbl;
    LPDLGTEMPLATE lpdt;
    LPDLGITEMTEMPLATE lpdit;
    LPWORD lpw;
    LPWSTR lpwsz;
    LRESULT ret;
    int nchar;

    hgbl = GlobalAlloc(GMEM_ZEROINIT, 1024);
    if (!hgbl)
        return -1;
 
    lpdt = (LPDLGTEMPLATE)GlobalLock(hgbl);
 
    // Define a dialog box.
 
    lpdt->style = WS_POPUP | WS_BORDER | WS_SYSMENU | DS_MODALFRAME | WS_CAPTION;
    lpdt->cdit = 3;         // Number of controls
    lpdt->x  = 10;  lpdt->y  = 10;
    lpdt->cx = 100; lpdt->cy = 100;

    lpw = (LPWORD)(lpdt + 1);
    *lpw++ = 0;             // No menu
    *lpw++ = 0;             // Predefined dialog box class (by default)

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "My Dialog", -1, lpwsz, 50);
    lpw += nchar;

    //-----------------------
    // Define an OK button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 70;
    lpdit->cx = 80; lpdit->cy = 20;
    lpdit->id = IDOK;       // OK button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_DEFPUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "OK", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a Help button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 55; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_HELP;    // Help button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_PUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class atom

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "Help", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a static text control.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_TEXT;    // Text identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | SS_LEFT;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0082;        // Static class

    for (lpwsz = (LPWSTR)lpw; *lpwsz++ = (WCHAR)*lpszMessage++;);
    lpw = (LPWORD)lpwsz;
    *lpw++ = 0;             // No creation data

    GlobalUnlock(hgbl); 
    ret = DialogBoxIndirect(hinst, 
                           (LPDLGTEMPLATE)hgbl, 
                           hwndOwner, 
                           (DLGPROC)DialogProc); 
    GlobalFree(hgbl); 
    return ret; 
}
```



 

 