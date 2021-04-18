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
# <a name="using-common-dialog-boxes"></a><span data-ttu-id="0a159-105">Использование общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="0a159-105">Using Common Dialog Boxes</span></span>

<span data-ttu-id="0a159-106">В этом разделе рассматриваются задачи, вызывающие общие диалоговые окна:</span><span class="sxs-lookup"><span data-stu-id="0a159-106">This section covers tasks that invoke common dialog boxes:</span></span>

-   [<span data-ttu-id="0a159-107">Выбор цвета</span><span class="sxs-lookup"><span data-stu-id="0a159-107">Choosing a Color</span></span>](#choosing-a-color)
-   [<span data-ttu-id="0a159-108">Выбор шрифта</span><span class="sxs-lookup"><span data-stu-id="0a159-108">Choosing a Font</span></span>](#choosing-a-font)
-   [<span data-ttu-id="0a159-109">Открытие файла</span><span class="sxs-lookup"><span data-stu-id="0a159-109">Opening a File</span></span>](#opening-a-file)
-   [<span data-ttu-id="0a159-110">Отображение диалогового окна «Печать»</span><span class="sxs-lookup"><span data-stu-id="0a159-110">Displaying the Print Dialog Box</span></span>](#displaying-the-print-dialog-box)
-   [<span data-ttu-id="0a159-111">Использование страницы свойств печати</span><span class="sxs-lookup"><span data-stu-id="0a159-111">Using the Print Property Sheet</span></span>](#using-the-print-property-sheet)
-   [<span data-ttu-id="0a159-112">Настройка печатной страницы</span><span class="sxs-lookup"><span data-stu-id="0a159-112">Setting Up the Printed Page</span></span>](#setting-up-the-printed-page)
-   [<span data-ttu-id="0a159-113">Поиск текста</span><span class="sxs-lookup"><span data-stu-id="0a159-113">Finding Text</span></span>](#finding-text)

## <a name="choosing-a-color"></a><span data-ttu-id="0a159-114">Выбор цвета</span><span class="sxs-lookup"><span data-stu-id="0a159-114">Choosing a Color</span></span>

<span data-ttu-id="0a159-115">В этом разделе описывается пример кода, в котором отображается диалоговое окно **цвета** , в котором пользователь может выбрать цвет.</span><span class="sxs-lookup"><span data-stu-id="0a159-115">This topic describes sample code that displays a **Color** dialog box so that a user can select a color.</span></span> <span data-ttu-id="0a159-116">В примере кода сначала инициализируется структура [**чусеколор**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) , а затем вызывается функция [**чусеколор**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) для вывода диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0a159-116">The sample code first initializes a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure, and then calls the [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) function to display the dialog box.</span></span> <span data-ttu-id="0a159-117">Если функция возвращает **значение true**, указывающее, что пользователь выбрал цвет, в образце кода для создания новой сплошной кисти используется выбранный цвет.</span><span class="sxs-lookup"><span data-stu-id="0a159-117">If the function returns **TRUE**, indicating that the user selected a color, the sample code uses the selected color to create a new solid brush.</span></span>

<span data-ttu-id="0a159-118">В этом примере используется структура [**чусеколор**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) для инициализации диалогового окна следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0a159-118">This example uses the [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure to initialize the dialog box as follows:</span></span>

-   <span data-ttu-id="0a159-119">Инициализирует элемент **лпкустколорс** указателем на статический массив значений.</span><span class="sxs-lookup"><span data-stu-id="0a159-119">Initializes the **lpCustColors** member with a pointer to a static array of values.</span></span> <span data-ttu-id="0a159-120">Цвета в массиве изначально являются черными, но статический массив сохраняет пользовательские цвета, созданные пользователем для последующих вызовов [**чусеколор**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0a159-120">The colors in the array are initially black, but the static array preserves custom colors created by the user for subsequent [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) calls.</span></span>
-   <span data-ttu-id="0a159-121">Устанавливает флаг **CC \_ ргбинит** и инициализирует элемент **ргбресулт** , чтобы указать цвет, изначально выбранный при открытии этого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0a159-121">Sets the **CC\_RGBINIT** flag and initializes the **rgbResult** member to specify the color that is initially selected when the dialog box opens.</span></span> <span data-ttu-id="0a159-122">Если не указано, первоначальный выбор будет черным.</span><span class="sxs-lookup"><span data-stu-id="0a159-122">If not specified, the initial selection is black.</span></span> <span data-ttu-id="0a159-123">В примере используется статическая переменная *ргбкуррент* для сохранения выбранного значения между вызовами [**чусеколор**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0a159-123">The example uses the *rgbCurrent* static variable to preserve the selected value between calls to [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)).</span></span>
-   <span data-ttu-id="0a159-124">Устанавливает флаг **CC \_ фуллопен** , чтобы расширение пользовательских цветов диалогового окна всегда отображалось.</span><span class="sxs-lookup"><span data-stu-id="0a159-124">Sets the **CC\_FULLOPEN** flag so the custom colors extension of the dialog box is always displayed.</span></span>


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



## <a name="choosing-a-font"></a><span data-ttu-id="0a159-125">Выбор шрифта</span><span class="sxs-lookup"><span data-stu-id="0a159-125">Choosing a Font</span></span>

<span data-ttu-id="0a159-126">В этом разделе описывается пример кода, в котором отображается диалоговое окно **Шрифт** , в котором пользователь может выбрать атрибуты шрифта.</span><span class="sxs-lookup"><span data-stu-id="0a159-126">This topic describes sample code that displays a **Font** dialog box so that a user can choose the attributes of a font.</span></span> <span data-ttu-id="0a159-127">В примере кода сначала инициализируется структура [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) , а затем вызывается функция [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) для вывода диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0a159-127">The sample code first initializes a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure, and then calls the [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function to display the dialog box.</span></span>

<span data-ttu-id="0a159-128">В этом примере устанавливается флаг **CF \_ скринфонтс** , чтобы указать, что в диалоговом окне должны отображаться только экранные шрифты.</span><span class="sxs-lookup"><span data-stu-id="0a159-128">This example sets the **CF\_SCREENFONTS** flag to specify that the dialog box should display only screen fonts.</span></span> <span data-ttu-id="0a159-129">Он устанавливает флаг **« \_ эффекты CF** », чтобы отображать элементы управления, позволяющие пользователю выбрать параметры зачеркивания, подчеркивание и цвет.</span><span class="sxs-lookup"><span data-stu-id="0a159-129">It sets the **CF\_EFFECTS** flag to display controls that allow the user to select strikeout, underline, and color options.</span></span>

<span data-ttu-id="0a159-130">Если [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) возвращает **значение true**, указывающее, что пользователь щелкнул кнопку **ОК** , структура [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) содержит сведения, описывающие атрибуты шрифта и шрифта, выбранные пользователем, включая элементы структуры [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , на которые указывает элемент **лплогфонт** .</span><span class="sxs-lookup"><span data-stu-id="0a159-130">If [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) returns **TRUE**, indicating that the user clicked the **OK** button, the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure contains information that describes the font and font attributes selected by the user, including the members of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure pointed to by the **lpLogFont** member.</span></span> <span data-ttu-id="0a159-131">Элемент **ргбколорс** содержит выбранный цвет текста.</span><span class="sxs-lookup"><span data-stu-id="0a159-131">The **rgbColors** member contains the selected text color.</span></span> <span data-ttu-id="0a159-132">В примере кода эти сведения используются для задания цвета шрифта и текста для контекста устройства, связанного с окном владельца.</span><span class="sxs-lookup"><span data-stu-id="0a159-132">The sample code uses this information to set the font and text color for the device context associated with the owner window.</span></span>


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



## <a name="opening-a-file"></a><span data-ttu-id="0a159-133">Открытие файла</span><span class="sxs-lookup"><span data-stu-id="0a159-133">Opening a File</span></span>

> [!Note]  
> <span data-ttu-id="0a159-134">Начиная с Windows Vista, общее диалоговое окно файла заменено диалоговым окном общих элементов при использовании для открытия файла.</span><span class="sxs-lookup"><span data-stu-id="0a159-134">Starting with Windows Vista, the Common File Dialog has been superseded by the Common Item Dialog when used to open a file.</span></span> <span data-ttu-id="0a159-135">Вместо общепринятого API-интерфейса диалогового окна рекомендуется использовать интерфейс API общего элемента.</span><span class="sxs-lookup"><span data-stu-id="0a159-135">We recommend that you use the Common Item Dialog API instead of the Common File Dialog API.</span></span> <span data-ttu-id="0a159-136">Дополнительные сведения см. в разделе [диалоговое окно общих элементов](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0a159-136">For more information, see [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span>

 

<span data-ttu-id="0a159-137">В этом разделе описывается пример кода, в котором отображается **открытое** диалоговое окно, в котором пользователь может указать диск, каталог и имя открываемого файла.</span><span class="sxs-lookup"><span data-stu-id="0a159-137">This topic describes sample code that displays an **Open** dialog box so that a user can specify the drive, directory, and name of a file to open.</span></span> <span data-ttu-id="0a159-138">В примере кода сначала инициализируется структура [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) , а затем вызывается функция [**GetOpenFilename**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) для вывода диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0a159-138">The sample code first initializes an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure, and then calls the [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) function to display the dialog box.</span></span>

<span data-ttu-id="0a159-139">В этом примере элемент **лпстрфилтер** является указателем на буфер, указывающий два фильтра имен файлов, которые пользователь может выбрать для ограничения отображаемых имен файлов.</span><span class="sxs-lookup"><span data-stu-id="0a159-139">In this example, the **lpstrFilter** member is a pointer to a buffer that specifies two file name filters that the user can select to limit the file names that are displayed.</span></span> <span data-ttu-id="0a159-140">Буфер содержит массив строк, заканчивающийся двойным нулем, в котором каждая пара строк задает фильтр.</span><span class="sxs-lookup"><span data-stu-id="0a159-140">The buffer contains a double-null terminated array of strings in which each pair of strings specifies a filter.</span></span> <span data-ttu-id="0a159-141">Элемент **нфилтериндекс** указывает, что первый шаблон используется при создании диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0a159-141">The **nFilterIndex** member specifies that the first pattern is used when the dialog box is created.</span></span>

<span data-ttu-id="0a159-142">В этом примере задаются флаги **ОФН \_ Пасмустексист** и **ОФН \_ выполнить операцию filemustexist** в элементе **flags** .</span><span class="sxs-lookup"><span data-stu-id="0a159-142">This example sets the **OFN\_PATHMUSTEXIST** and **OFN\_FILEMUSTEXIST** flags in the **Flags** member.</span></span> <span data-ttu-id="0a159-143">Эти флаги приводят к тому, что перед возвратом диалоговое окно проверяет, что путь и имя файла, указанные пользователем, действительно существуют.</span><span class="sxs-lookup"><span data-stu-id="0a159-143">These flags cause the dialog box to verify, before returning, that the path and file name specified by the user actually exist.</span></span>

<span data-ttu-id="0a159-144">Функция [**GetOpenFilename**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) возвращает **значение true** , если пользователь нажимает кнопку **ОК** , а указанный путь и имя файла существуют.</span><span class="sxs-lookup"><span data-stu-id="0a159-144">The [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) function returns **TRUE** if the user clicks the **OK** button and the specified path and file name exist.</span></span> <span data-ttu-id="0a159-145">В этом случае буфер, на который указывает член **указанный** , содержит путь и имя файла.</span><span class="sxs-lookup"><span data-stu-id="0a159-145">In this case, the buffer pointed to by the **lpstrFile** member contains the path and file name.</span></span> <span data-ttu-id="0a159-146">В примере кода эти сведения используются в вызове функции для открытия файла.</span><span class="sxs-lookup"><span data-stu-id="0a159-146">The sample code uses this information in a call to the function to open the file.</span></span>

<span data-ttu-id="0a159-147">Несмотря на то, что этот пример не устанавливает флаг **\_ обозревателя ОФН** , он по-прежнему отображает диалоговое окно « **Открыть** в стиле обозревателя по умолчанию».</span><span class="sxs-lookup"><span data-stu-id="0a159-147">Although this example does not set the **OFN\_EXPLORER** flag, it still displays the default Explorer-style **Open** dialog box.</span></span> <span data-ttu-id="0a159-148">Однако если вы хотите предоставить процедуру-обработчик или пользовательский шаблон, и вы хотите использовать пользовательский интерфейс обозревателя, необходимо установить флаг **\_ обозревателя ОФН** .</span><span class="sxs-lookup"><span data-stu-id="0a159-148">However, if you want to provide a hook procedure or a custom template and you want the Explorer user interface, you must set the **OFN\_EXPLORER** flag.</span></span>

> [!Note]  
> <span data-ttu-id="0a159-149">В языке программирования C строка, заключенная в кавычки, завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="0a159-149">In the C programming language, a string enclosed in quotation marks is null-terminated.</span></span>

 


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



## <a name="displaying-the-print-dialog-box"></a><span data-ttu-id="0a159-150">Отображение диалогового окна «Печать»</span><span class="sxs-lookup"><span data-stu-id="0a159-150">Displaying the Print Dialog Box</span></span>

<span data-ttu-id="0a159-151">В этом разделе описывается пример кода, в котором отображается диалоговое окно **Печать** , в котором пользователь может выбрать параметры печати документа.</span><span class="sxs-lookup"><span data-stu-id="0a159-151">This topic describes sample code that displays a **Print** dialog box so that a user can select options for printing a document.</span></span> <span data-ttu-id="0a159-152">В примере кода сначала инициализируется структура [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) , а затем вызывается функция [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) для вывода диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0a159-152">The sample code first initializes a [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure, and then calls the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function to display the dialog box.</span></span>

<span data-ttu-id="0a159-153">В этом примере задается флаг **PD \_ ретурндк** в элементе **flags** структуры [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="0a159-153">This example sets the **PD\_RETURNDC** flag in the **Flags** member of the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="0a159-154">Это приводит к тому, что [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) возвращает маркер контекста устройства выбранному принтеру в члене **HDC** .</span><span class="sxs-lookup"><span data-stu-id="0a159-154">This causes [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) to return a device context handle to the selected printer in the **hDC** member.</span></span> <span data-ttu-id="0a159-155">Вы можете использовать этот маркер для отрисовки выходных данных на принтере.</span><span class="sxs-lookup"><span data-stu-id="0a159-155">You can use the handle to render output on the printer.</span></span>

<span data-ttu-id="0a159-156">На входе в примере кода в качестве элементов **хдевмоде** и **Хдевнамес** присваивается **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0a159-156">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="0a159-157">Если функция возвращает **значение true**, эти элементы возвращают дескрипторы в структуры [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) , которые содержат введенные пользователем данные и сведения о принтере.</span><span class="sxs-lookup"><span data-stu-id="0a159-157">If the function returns **TRUE**, these members return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures that contain the user input and information about the printer.</span></span> <span data-ttu-id="0a159-158">Эти сведения можно использовать для подготовки выходных данных к отправке на выбранный принтер.</span><span class="sxs-lookup"><span data-stu-id="0a159-158">You can use this information to prepare the output to be sent to the selected printer.</span></span>


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



## <a name="using-the-print-property-sheet"></a><span data-ttu-id="0a159-159">Использование страницы свойств печати</span><span class="sxs-lookup"><span data-stu-id="0a159-159">Using the Print Property Sheet</span></span>

<span data-ttu-id="0a159-160">В этом разделе описывается пример кода, отображающий страницу свойств **печати** , чтобы пользователь мог выбрать параметры печати документа.</span><span class="sxs-lookup"><span data-stu-id="0a159-160">This topic describes sample code that displays a **Print** property sheet so that a user can select options for printing a document.</span></span> <span data-ttu-id="0a159-161">В примере кода сначала инициализируется структура [**принтдлжекс**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) , а затем вызывается функция [**принтдлжекс**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) для вывода страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="0a159-161">The sample code first initializes a [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) structure, then calls the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to display the property sheet.</span></span>

<span data-ttu-id="0a159-162">В примере кода устанавливается флаг **PD \_ ретурндк** в элементе **flags** структуры [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="0a159-162">The sample code sets the **PD\_RETURNDC** flag in the **Flags** member of the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="0a159-163">Это приводит к тому, что функция [**принтдлжекс**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) возвращает маркер контекста устройства выбранному принтеру в члене **HDC** .</span><span class="sxs-lookup"><span data-stu-id="0a159-163">This causes the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to return a device context handle to the selected printer in the **hDC** member.</span></span>

<span data-ttu-id="0a159-164">На входе в примере кода в качестве элементов **хдевмоде** и **Хдевнамес** присваивается **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0a159-164">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="0a159-165">Если функция возвращает значение **S \_ ОК**, эти элементы возвращают дескрипторы в структуры [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) , содержащие ввод пользователя и сведения о принтере.</span><span class="sxs-lookup"><span data-stu-id="0a159-165">If the function returns **S\_OK**, these members return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures containing the user input and information about the printer.</span></span> <span data-ttu-id="0a159-166">Эти сведения можно использовать для подготовки выходных данных к отправке на выбранный принтер.</span><span class="sxs-lookup"><span data-stu-id="0a159-166">You can use this information to prepare the output to be sent to the selected printer.</span></span>

<span data-ttu-id="0a159-167">После завершения операции печати пример кода освобождает буферы [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames)и [**принтпажеранже**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) и вызывает функцию [**делетедк**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) для удаления контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="0a159-167">After the printing operation has been completed, the sample code frees the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames), and [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) buffers and calls the [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) function to delete the device context.</span></span>


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



## <a name="setting-up-the-printed-page"></a><span data-ttu-id="0a159-168">Настройка печатной страницы</span><span class="sxs-lookup"><span data-stu-id="0a159-168">Setting Up the Printed Page</span></span>

<span data-ttu-id="0a159-169">В этом разделе описывается пример кода, отображающий диалоговое окно « **Параметры страницы** », в котором пользователь может выбрать атрибуты печатной страницы, такие как тип бумаги, источник бумаги, ориентация страницы и поля страницы.</span><span class="sxs-lookup"><span data-stu-id="0a159-169">This topic describes sample code that displays a **Page Setup** dialog box so that a user can select the attributes of the printed page, such as the paper type, paper source, page orientation, and page margins.</span></span> <span data-ttu-id="0a159-170">В примере кода сначала инициализируется структура [**пажесетупдлг**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) , а затем вызывается функция [**пажесетупдлг**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) для вывода диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0a159-170">The sample code first initializes a [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure, and then calls the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function to display the dialog box.</span></span>

<span data-ttu-id="0a159-171">В этом примере задаются флаги **\_ полей PSD** в элементе **flags** и используется элемент **ртмаргин** для указания начальных значений полей.</span><span class="sxs-lookup"><span data-stu-id="0a159-171">This example sets the **PSD\_MARGINS** flag in the **Flags** member and uses the **rtMargin** member to specify the initial margin values.</span></span> <span data-ttu-id="0a159-172">Он устанавливает флаг **PSD \_ инсаусандссофинчес** , чтобы гарантировать, что диалоговое окно выражает размеры полей в тысячах дюйма.</span><span class="sxs-lookup"><span data-stu-id="0a159-172">It sets the **PSD\_INTHOUSANDTHSOFINCHES** flag to ensure that the dialog box expresses margin dimensions in thousandths of an inch.</span></span>

<span data-ttu-id="0a159-173">На входе в примере кода в качестве элементов **хдевмоде** и **Хдевнамес** присваивается **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0a159-173">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="0a159-174">Если функция возвращает **значение true**, функция использует эти элементы для возврата дескрипторов в структуры [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) , содержащие входные данные пользователя и сведения о принтере.</span><span class="sxs-lookup"><span data-stu-id="0a159-174">If the function returns **TRUE**, the function uses these members to return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures containing the user input and information about the printer.</span></span> <span data-ttu-id="0a159-175">Эти сведения можно использовать для подготовки выходных данных к отправке на выбранный принтер.</span><span class="sxs-lookup"><span data-stu-id="0a159-175">You can use this information to prepare the output to be sent to the selected printer.</span></span>

<span data-ttu-id="0a159-176">В следующем примере также активируется процедура-обработчик [**пажепаинсук**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) для настройки рисования содержимого образца страницы.</span><span class="sxs-lookup"><span data-stu-id="0a159-176">The following example also enables a [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize drawing the contents of the sample page.</span></span>


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



<span data-ttu-id="0a159-177">В следующем примере показан пример процедуры-обработчика [**пажепаинсук**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) , которая рисует прямоугольник поля в области страницы выборки:</span><span class="sxs-lookup"><span data-stu-id="0a159-177">The following example shows a sample [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure that draws the margin rectangle in the sample page area:</span></span>


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



## <a name="finding-text"></a><span data-ttu-id="0a159-178">Поиск текста</span><span class="sxs-lookup"><span data-stu-id="0a159-178">Finding Text</span></span>

<span data-ttu-id="0a159-179">В этом разделе описывается пример кода, который отображает диалоговое окно **поиска** и управляет им, чтобы пользователь мог указать параметры операции поиска.</span><span class="sxs-lookup"><span data-stu-id="0a159-179">This topic describes sample code that displays and manages a **Find** dialog box so that the user can specify the parameters of a search operation.</span></span> <span data-ttu-id="0a159-180">Диалоговое окно отправляет сообщения в процедуру окна, чтобы можно было выполнить операцию поиска.</span><span class="sxs-lookup"><span data-stu-id="0a159-180">The dialog box sends messages to the window procedure so you can perform the search operation.</span></span>

<span data-ttu-id="0a159-181">Код для отображения диалогового окна **замены** и управления им аналогичен, за исключением того, что он использует функцию [**реплацетекст**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) для отображения диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0a159-181">The code for displaying and managing a **Replace** dialog box is similar, except that it uses the [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) function to display the dialog box.</span></span> <span data-ttu-id="0a159-182">Диалоговое окно **заменить** также отправляет сообщения в ответ на нажатие пользователем кнопки **заменить** и **заменить все** .</span><span class="sxs-lookup"><span data-stu-id="0a159-182">The **Replace** dialog box also sends messages in response to user clicks on the **Replace** and **Replace All** buttons.</span></span>

<span data-ttu-id="0a159-183">Чтобы использовать диалоговое окно **найти** или **заменить** , необходимо выполнить три отдельные задачи:</span><span class="sxs-lookup"><span data-stu-id="0a159-183">To use the **Find** or **Replace** dialog box, you must perform three separate tasks:</span></span>

1.  <span data-ttu-id="0a159-184">Получение идентификатора сообщения для зарегистрированного сообщения [**финдмсгстринг**](findmsgstring.md) .</span><span class="sxs-lookup"><span data-stu-id="0a159-184">Get a message identifier for the [**FINDMSGSTRING**](findmsgstring.md) registered message.</span></span>
2.  <span data-ttu-id="0a159-185">Отображение диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0a159-185">Display the dialog box.</span></span>
3.  <span data-ttu-id="0a159-186">Обрабатывать сообщения [**финдмсгстринг**](findmsgstring.md) , когда открыто диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="0a159-186">Process [**FINDMSGSTRING**](findmsgstring.md) messages when the dialog box is open.</span></span>

<span data-ttu-id="0a159-187">При инициализации приложения вызовите функцию [**регистервиндовмессаже**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) , чтобы получить идентификатор сообщения для зарегистрированного сообщения [**финдмсгстринг**](findmsgstring.md) .</span><span class="sxs-lookup"><span data-stu-id="0a159-187">When you initialize your application, call the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get a message identifier for the [**FINDMSGSTRING**](findmsgstring.md) registered message.</span></span>


```
UINT uFindReplaceMsg;  // message identifier for FINDMSGSTRING 

uFindReplaceMsg = RegisterWindowMessage(FINDMSGSTRING);
```



<span data-ttu-id="0a159-188">Чтобы открыть диалоговое окно **Поиск** , сначала инициализируйте структуру [**финдреплаце**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) , а затем вызовите функцию [**строки FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) .</span><span class="sxs-lookup"><span data-stu-id="0a159-188">To display a **Find** dialog box, first initialize a [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure and then call the [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) function.</span></span> <span data-ttu-id="0a159-189">Обратите внимание, что структура **финдреплаце** и буфер для строки поиска должны быть глобальной или статической переменной, чтобы она не выйдет из области, прежде чем диалоговое окно закроется.</span><span class="sxs-lookup"><span data-stu-id="0a159-189">Note that the **FINDREPLACE** structure and the buffer for the search string should be a global or static variable so that it does not go out of scope before the dialog box closes.</span></span> <span data-ttu-id="0a159-190">Необходимо задать элемент **хвндовнер** , чтобы указать окно, которое получает зарегистрированные сообщения.</span><span class="sxs-lookup"><span data-stu-id="0a159-190">You must set the **hwndOwner** member to specify the window that receives the registered messages.</span></span> <span data-ttu-id="0a159-191">После создания диалогового окна его можно перемещать или манипулировать с помощью возвращенного маркера.</span><span class="sxs-lookup"><span data-stu-id="0a159-191">After you create the dialog box, you can move or manipulate it by using the returned handle.</span></span>


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



<span data-ttu-id="0a159-192">Когда диалоговое окно открыто, основной цикл обработки сообщений должен включать вызов функции [**исдиалогмессаже**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) .</span><span class="sxs-lookup"><span data-stu-id="0a159-192">When the dialog box is open, your main message loop must include a call to the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function.</span></span> <span data-ttu-id="0a159-193">Передайте обработчик в диалоговое окно в качестве параметра в вызове **исдиалогмессаже** .</span><span class="sxs-lookup"><span data-stu-id="0a159-193">Pass a handle to the dialog box as a parameter in the **IsDialogMessage** call.</span></span> <span data-ttu-id="0a159-194">Это гарантирует правильную обработку сообщений клавиатуры в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="0a159-194">This ensures that the dialog box correctly processes keyboard messages.</span></span>

<span data-ttu-id="0a159-195">Для наблюдения за сообщениями, отправленными из диалогового окна, процедура окна должна проверить зарегистрированное сообщение [**финдмсгстринг**](findmsgstring.md) и обработать значения, переданные в структуре [**финдреплаце**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="0a159-195">To monitor messages sent from the dialog box, your window procedure must check for the [**FINDMSGSTRING**](findmsgstring.md) registered message and process the values passed in the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure as in the following example.</span></span>


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



 

 
