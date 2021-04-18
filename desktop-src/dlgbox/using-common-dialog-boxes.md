---
title: Использование общих диалоговых окон
description: В этом разделе рассматриваются задачи, вызывающие общие диалоговые окна.
ms.assetid: ba038bc1-fb5c-4576-be80-7eae7339ba05
keywords:
- Библиотека общих диалоговых окон, задачи
- Общие диалоговые окна, использование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a973fee7c8f7cd88abad3097edfc0349cc9118c1
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/19/2020
ms.locfileid: "105691716"
---
# <a name="using-common-dialog-boxes"></a>Использование общих диалоговых окон

В этом разделе рассматриваются задачи, вызывающие общие диалоговые окна:

-   [Выбор цвета](#choosing-a-color)
-   [Выбор шрифта](#choosing-a-font)
-   [Открытие файла](#opening-a-file)
-   [Отображение диалогового окна «Печать»](#displaying-the-print-dialog-box)
-   [Использование страницы свойств печати](#using-the-print-property-sheet)
-   [Настройка печатной страницы](#setting-up-the-printed-page)
-   [Поиск текста](#finding-text)

## <a name="choosing-a-color"></a>Выбор цвета

В этом разделе описывается пример кода, в котором отображается диалоговое окно **цвета** , в котором пользователь может выбрать цвет. В примере кода сначала инициализируется структура [**чусеколор**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) , а затем вызывается функция [**чусеколор**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) для вывода диалогового окна. Если функция возвращает **значение true**, указывающее, что пользователь выбрал цвет, в образце кода для создания новой сплошной кисти используется выбранный цвет.

В этом примере используется структура [**чусеколор**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) для инициализации диалогового окна следующим образом:

-   Инициализирует элемент **лпкустколорс** указателем на статический массив значений. Цвета в массиве изначально являются черными, но статический массив сохраняет пользовательские цвета, созданные пользователем для последующих вызовов [**чусеколор**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) .
-   Устанавливает флаг **CC \_ ргбинит** и инициализирует элемент **ргбресулт** , чтобы указать цвет, изначально выбранный при открытии этого диалогового окна. Если не указано, первоначальный выбор будет черным. В примере используется статическая переменная *ргбкуррент* для сохранения выбранного значения между вызовами [**чусеколор**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)).
-   Устанавливает флаг **CC \_ фуллопен** , чтобы расширение пользовательских цветов диалогового окна всегда отображалось.


```
CHOOSECOLOR cc;                 // common dialog box structure 
static COLORREF acrCustClr[16]; // array of custom colors 
HWND hwnd;                      // owner window
HBRUSH hbrush;                  // brush handle
static DWORD rgbCurrent;        // initial color selection

// Initialize CHOOSECOLOR 
ZeroMemory(&cc, sizeof(cc));
cc.lStructSize = sizeof(cc);
cc.hwndOwner = hwnd;
cc.lpCustColors = (LPDWORD) acrCustClr;
cc.rgbResult = rgbCurrent;
cc.Flags = CC_FULLOPEN | CC_RGBINIT;
 
if (ChooseColor(&cc)==TRUE) 
{
    hbrush = CreateSolidBrush(cc.rgbResult);
    rgbCurrent = cc.rgbResult; 
}
```



## <a name="choosing-a-font"></a>Выбор шрифта

В этом разделе описывается пример кода, в котором отображается диалоговое окно **Шрифт** , в котором пользователь может выбрать атрибуты шрифта. В примере кода сначала инициализируется структура [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) , а затем вызывается функция [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) для вывода диалогового окна.

В этом примере устанавливается флаг **CF \_ скринфонтс** , чтобы указать, что в диалоговом окне должны отображаться только экранные шрифты. Он устанавливает флаг **« \_ эффекты CF** », чтобы отображать элементы управления, позволяющие пользователю выбрать параметры зачеркивания, подчеркивание и цвет.

Если [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) возвращает **значение true**, указывающее, что пользователь щелкнул кнопку **ОК** , структура [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) содержит сведения, описывающие атрибуты шрифта и шрифта, выбранные пользователем, включая элементы структуры [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , на которые указывает элемент **лплогфонт** . Элемент **ргбколорс** содержит выбранный цвет текста. В примере кода эти сведения используются для задания цвета шрифта и текста для контекста устройства, связанного с окном владельца.


```
HWND hwnd;                // owner window
HDC hdc;                  // display device context of owner window

CHOOSEFONT cf;            // common dialog box structure
static LOGFONT lf;        // logical font structure
static DWORD rgbCurrent;  // current text color
HFONT hfont, hfontPrev;
DWORD rgbPrev;

// Initialize CHOOSEFONT
ZeroMemory(&cf, sizeof(cf));
cf.lStructSize = sizeof (cf);
cf.hwndOwner = hwnd;
cf.lpLogFont = &lf;
cf.rgbColors = rgbCurrent;
cf.Flags = CF_SCREENFONTS | CF_EFFECTS;

if (ChooseFont(&cf)==TRUE)
{
    hfont = CreateFontIndirect(cf.lpLogFont);
    hfontPrev = SelectObject(hdc, hfont);
    rgbCurrent= cf.rgbColors;
    rgbPrev = SetTextColor(hdc, rgbCurrent);
 .
 .
 .
}
```



## <a name="opening-a-file"></a>Открытие файла

> [!Note]  
> Начиная с Windows Vista, общее диалоговое окно файла заменено диалоговым окном общих элементов при использовании для открытия файла. Вместо общепринятого API-интерфейса диалогового окна рекомендуется использовать интерфейс API общего элемента. Дополнительные сведения см. в разделе [диалоговое окно общих элементов](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).

 

В этом разделе описывается пример кода, в котором отображается **открытое** диалоговое окно, в котором пользователь может указать диск, каталог и имя открываемого файла. В примере кода сначала инициализируется структура [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) , а затем вызывается функция [**GetOpenFilename**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) для вывода диалогового окна.

В этом примере элемент **лпстрфилтер** является указателем на буфер, указывающий два фильтра имен файлов, которые пользователь может выбрать для ограничения отображаемых имен файлов. Буфер содержит массив строк, заканчивающийся двойным нулем, в котором каждая пара строк задает фильтр. Элемент **нфилтериндекс** указывает, что первый шаблон используется при создании диалогового окна.

В этом примере задаются флаги **ОФН \_ Пасмустексист** и **ОФН \_ выполнить операцию filemustexist** в элементе **flags** . Эти флаги приводят к тому, что перед возвратом диалоговое окно проверяет, что путь и имя файла, указанные пользователем, действительно существуют.

Функция [**GetOpenFilename**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) возвращает **значение true** , если пользователь нажимает кнопку **ОК** , а указанный путь и имя файла существуют. В этом случае буфер, на который указывает член **указанный** , содержит путь и имя файла. В примере кода эти сведения используются в вызове функции для открытия файла.

Несмотря на то, что этот пример не устанавливает флаг **\_ обозревателя ОФН** , он по-прежнему отображает диалоговое окно « **Открыть** в стиле обозревателя по умолчанию». Однако если вы хотите предоставить процедуру-обработчик или пользовательский шаблон, и вы хотите использовать пользовательский интерфейс обозревателя, необходимо установить флаг **\_ обозревателя ОФН** .

> [!Note]  
> В языке программирования C строка, заключенная в кавычки, завершается нулем.

 


```
OPENFILENAME ofn;       // common dialog box structure
char szFile[260];       // buffer for file name
HWND hwnd;              // owner window
HANDLE hf;              // file handle

// Initialize OPENFILENAME
ZeroMemory(&ofn, sizeof(ofn));
ofn.lStructSize = sizeof(ofn);
ofn.hwndOwner = hwnd;
ofn.lpstrFile = szFile;
// Set lpstrFile[0] to '\0' so that GetOpenFileName does not 
// use the contents of szFile to initialize itself.
ofn.lpstrFile[0] = '\0';
ofn.nMaxFile = sizeof(szFile);
ofn.lpstrFilter = "All\0*.*\0Text\0*.TXT\0";
ofn.nFilterIndex = 1;
ofn.lpstrFileTitle = NULL;
ofn.nMaxFileTitle = 0;
ofn.lpstrInitialDir = NULL;
ofn.Flags = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;

// Display the Open dialog box. 

if (GetOpenFileName(&ofn)==TRUE) 
    hf = CreateFile(ofn.lpstrFile, 
                    GENERIC_READ,
                    0,
                    (LPSECURITY_ATTRIBUTES) NULL,
                    OPEN_EXISTING,
                    FILE_ATTRIBUTE_NORMAL,
                    (HANDLE) NULL);
```



## <a name="displaying-the-print-dialog-box"></a>Отображение диалогового окна «Печать»

В этом разделе описывается пример кода, в котором отображается диалоговое окно **Печать** , в котором пользователь может выбрать параметры печати документа. В примере кода сначала инициализируется структура [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) , а затем вызывается функция [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) для вывода диалогового окна.

В этом примере задается флаг **PD \_ ретурндк** в элементе **flags** структуры [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . Это приводит к тому, что [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) возвращает маркер контекста устройства выбранному принтеру в члене **HDC** . Вы можете использовать этот маркер для отрисовки выходных данных на принтере.

На входе в примере кода в качестве элементов **хдевмоде** и **Хдевнамес** присваивается **значение NULL**. Если функция возвращает **значение true**, эти элементы возвращают дескрипторы в структуры [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) , которые содержат введенные пользователем данные и сведения о принтере. Эти сведения можно использовать для подготовки выходных данных к отправке на выбранный принтер.


```
PRINTDLG pd;
HWND hwnd;

// Initialize PRINTDLG
ZeroMemory(&pd, sizeof(pd));
pd.lStructSize = sizeof(pd);
pd.hwndOwner   = hwnd;
pd.hDevMode    = NULL;     // Don't forget to free or store hDevMode.
pd.hDevNames   = NULL;     // Don't forget to free or store hDevNames.
pd.Flags       = PD_USEDEVMODECOPIESANDCOLLATE | PD_RETURNDC; 
pd.nCopies     = 1;
pd.nFromPage   = 0xFFFF; 
pd.nToPage     = 0xFFFF; 
pd.nMinPage    = 1; 
pd.nMaxPage    = 0xFFFF; 

if (PrintDlg(&pd)==TRUE) 
{
    // GDI calls to render output. 

    // Delete DC when done.
    DeleteDC(pd.hDC);
}
```



## <a name="using-the-print-property-sheet"></a>Использование страницы свойств печати

В этом разделе описывается пример кода, отображающий страницу свойств **печати** , чтобы пользователь мог выбрать параметры печати документа. В примере кода сначала инициализируется структура [**принтдлжекс**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) , а затем вызывается функция [**принтдлжекс**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) для вывода страницы свойств.

В примере кода устанавливается флаг **PD \_ ретурндк** в элементе **flags** структуры [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . Это приводит к тому, что функция [**принтдлжекс**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) возвращает маркер контекста устройства выбранному принтеру в члене **HDC** .

На входе в примере кода в качестве элементов **хдевмоде** и **Хдевнамес** присваивается **значение NULL**. Если функция возвращает значение **S \_ ОК**, эти элементы возвращают дескрипторы в структуры [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) , содержащие ввод пользователя и сведения о принтере. Эти сведения можно использовать для подготовки выходных данных к отправке на выбранный принтер.

После завершения операции печати пример кода освобождает буферы [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames)и [**принтпажеранже**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) и вызывает функцию [**делетедк**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) для удаления контекста устройства.


```
// hWnd is the window that owns the property sheet.
HRESULT DisplayPrintPropertySheet(HWND hWnd)
{
    HRESULT hResult;
    PRINTDLGEX pdx = {0};
    LPPRINTPAGERANGE pPageRanges = NULL;

    // Allocate an array of PRINTPAGERANGE structures.
    pPageRanges = (LPPRINTPAGERANGE) GlobalAlloc(GPTR, 10 * sizeof(PRINTPAGERANGE));
    if (!pPageRanges)
        return E_OUTOFMEMORY;

    //  Initialize the PRINTDLGEX structure.
    pdx.lStructSize = sizeof(PRINTDLGEX);
    pdx.hwndOwner = hWnd;
    pdx.hDevMode = NULL;
    pdx.hDevNames = NULL;
    pdx.hDC = NULL;
    pdx.Flags = PD_RETURNDC | PD_COLLATE;
    pdx.Flags2 = 0;
    pdx.ExclusionFlags = 0;
    pdx.nPageRanges = 0;
    pdx.nMaxPageRanges = 10;
    pdx.lpPageRanges = pPageRanges;
    pdx.nMinPage = 1;
    pdx.nMaxPage = 1000;
    pdx.nCopies = 1;
    pdx.hInstance = 0;
    pdx.lpPrintTemplateName = NULL;
    pdx.lpCallback = NULL;
    pdx.nPropertyPages = 0;
    pdx.lphPropertyPages = NULL;
    pdx.nStartPage = START_PAGE_GENERAL;
    pdx.dwResultAction = 0;
    
    //  Invoke the Print property sheet.
    
    hResult = PrintDlgEx(&pdx);

    if ((hResult == S_OK) && pdx.dwResultAction == PD_RESULT_PRINT) 
    {
        // User clicked the Print button, so use the DC and other information returned in the 
        // PRINTDLGEX structure to print the document.
    }

    if (pdx.hDevMode != NULL) 
        GlobalFree(pdx.hDevMode); 
    if (pdx.hDevNames != NULL) 
        GlobalFree(pdx.hDevNames); 
    if (pdx.lpPageRanges != NULL)
        GlobalFree(pPageRanges);

    if (pdx.hDC != NULL) 
        DeleteDC(pdx.hDC);

    return hResult;
}
```



## <a name="setting-up-the-printed-page"></a>Настройка печатной страницы

В этом разделе описывается пример кода, отображающий диалоговое окно « **Параметры страницы** », в котором пользователь может выбрать атрибуты печатной страницы, такие как тип бумаги, источник бумаги, ориентация страницы и поля страницы. В примере кода сначала инициализируется структура [**пажесетупдлг**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) , а затем вызывается функция [**пажесетупдлг**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) для вывода диалогового окна.

В этом примере задаются флаги **\_ полей PSD** в элементе **flags** и используется элемент **ртмаргин** для указания начальных значений полей. Он устанавливает флаг **PSD \_ инсаусандссофинчес** , чтобы гарантировать, что диалоговое окно выражает размеры полей в тысячах дюйма.

На входе в примере кода в качестве элементов **хдевмоде** и **Хдевнамес** присваивается **значение NULL**. Если функция возвращает **значение true**, функция использует эти элементы для возврата дескрипторов в структуры [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) , содержащие входные данные пользователя и сведения о принтере. Эти сведения можно использовать для подготовки выходных данных к отправке на выбранный принтер.

В следующем примере также активируется процедура-обработчик [**пажепаинсук**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) для настройки рисования содержимого образца страницы.


```
PAGESETUPDLG psd;    // common dialog box structure
HWND hwnd;           // owner window

// Initialize PAGESETUPDLG
ZeroMemory(&psd, sizeof(psd));
psd.lStructSize = sizeof(psd);
psd.hwndOwner   = hwnd;
psd.hDevMode    = NULL; // Don't forget to free or store hDevMode.
psd.hDevNames   = NULL; // Don't forget to free or store hDevNames.
psd.Flags       = PSD_INTHOUSANDTHSOFINCHES | PSD_MARGINS | 
                  PSD_ENABLEPAGEPAINTHOOK; 
psd.rtMargin.top = 1000;
psd.rtMargin.left = 1250;
psd.rtMargin.right = 1250;
psd.rtMargin.bottom = 1000;
psd.lpfnPagePaintHook = PaintHook;

if (PageSetupDlg(&psd)==TRUE)
{
    // check paper size and margin values here.
}
```



В следующем примере показан пример процедуры-обработчика [**пажепаинсук**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) , которая рисует прямоугольник поля в области страницы выборки:


```
BOOL CALLBACK PaintHook(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    LPRECT lprc; 
    COLORREF crMargRect; 
    HDC hdc, hdcOld; 
 
    switch (uMsg) 
    { 
        // Draw the margin rectangle. 
        case WM_PSD_MARGINRECT: 
            hdc = (HDC) wParam; 
            lprc = (LPRECT) lParam; 
 
            // Get the system highlight color. 
            crMargRect = GetSysColor(COLOR_HIGHLIGHT); 
 
            // Create a dash-dot pen of the system highlight color and 
            // select it into the DC of the sample page. 
            hdcOld = SelectObject(hdc, CreatePen(PS_DASHDOT, .5, crMargRect)); 
 
            // Draw the margin rectangle. 
            Rectangle(hdc, lprc->left, lprc->top, lprc->right, lprc->bottom); 
 
            // Restore the previous pen to the DC. 
            SelectObject(hdc, hdcOld); 
            return TRUE; 
 
        default: 
            return FALSE; 
    } 
    return TRUE; 
}
```



## <a name="finding-text"></a>Поиск текста

В этом разделе описывается пример кода, который отображает диалоговое окно **поиска** и управляет им, чтобы пользователь мог указать параметры операции поиска. Диалоговое окно отправляет сообщения в процедуру окна, чтобы можно было выполнить операцию поиска.

Код для отображения диалогового окна **замены** и управления им аналогичен, за исключением того, что он использует функцию [**реплацетекст**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) для отображения диалогового окна. Диалоговое окно **заменить** также отправляет сообщения в ответ на нажатие пользователем кнопки **заменить** и **заменить все** .

Чтобы использовать диалоговое окно **найти** или **заменить** , необходимо выполнить три отдельные задачи:

1.  Получение идентификатора сообщения для зарегистрированного сообщения [**финдмсгстринг**](findmsgstring.md) .
2.  Отображение диалогового окна.
3.  Обрабатывать сообщения [**финдмсгстринг**](findmsgstring.md) , когда открыто диалоговое окно.

При инициализации приложения вызовите функцию [**регистервиндовмессаже**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) , чтобы получить идентификатор сообщения для зарегистрированного сообщения [**финдмсгстринг**](findmsgstring.md) .


```
UINT uFindReplaceMsg;  // message identifier for FINDMSGSTRING 

uFindReplaceMsg = RegisterWindowMessage(FINDMSGSTRING);
```



Чтобы открыть диалоговое окно **Поиск** , сначала инициализируйте структуру [**финдреплаце**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) , а затем вызовите функцию [**строки FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) . Обратите внимание, что структура **финдреплаце** и буфер для строки поиска должны быть глобальной или статической переменной, чтобы она не выйдет из области, прежде чем диалоговое окно закроется. Необходимо задать элемент **хвндовнер** , чтобы указать окно, которое получает зарегистрированные сообщения. После создания диалогового окна его можно перемещать или манипулировать с помощью возвращенного маркера.


```
FINDREPLACE fr;       // common dialog box structure
HWND hwnd;            // owner window
CHAR szFindWhat[80];  // buffer receiving string
HWND hdlg = NULL;     // handle to Find dialog box

// Initialize FINDREPLACE
ZeroMemory(&fr, sizeof(fr));
fr.lStructSize = sizeof(fr);
fr.hwndOwner = hwnd;
fr.lpstrFindWhat = szFindWhat;
fr.wFindWhatLen = 80;
fr.Flags = 0;

hdlg = FindText(&fr);
```



Когда диалоговое окно открыто, основной цикл обработки сообщений должен включать вызов функции [**исдиалогмессаже**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) . Передайте обработчик в диалоговое окно в качестве параметра в вызове **исдиалогмессаже** . Это гарантирует правильную обработку сообщений клавиатуры в диалоговом окне.

Для наблюдения за сообщениями, отправленными из диалогового окна, процедура окна должна проверить зарегистрированное сообщение [**финдмсгстринг**](findmsgstring.md) и обработать значения, переданные в структуре [**финдреплаце**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) , как показано в следующем примере.


```
LPFINDREPLACE lpfr;

if (message == uFindReplaceMsg)
{ 
    // Get pointer to FINDREPLACE structure from lParam.
    lpfr = (LPFINDREPLACE)lParam;

    // If the FR_DIALOGTERM flag is set, 
    // invalidate the handle that identifies the dialog box. 
    if (lpfr->Flags & FR_DIALOGTERM)
    { 
        hdlg = NULL; 
        return 0; 
    } 

    // If the FR_FINDNEXT flag is set, 
    // call the application-defined search routine
    // to search for the requested string. 
    if (lpfr->Flags & FR_FINDNEXT) 
    {
        SearchFile(lpfr->lpstrFindWhat,
                   (BOOL) (lpfr->Flags & FR_DOWN), 
                   (BOOL) (lpfr->Flags & FR_MATCHCASE)); 
    }

    return 0; 
}
```



 

 
