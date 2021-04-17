---
description: В этом разделе описывается, как получить контекст печатающего устройства.
ms.assetid: b3eb9c48-f4c4-42f1-b189-1fa42670008e
title: Как получить контекст печатающего устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39fde55450273e42f3429f173150296fdd67a1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693296"
---
# <a name="how-to-retrieve-a-printer-device-context"></a><span data-ttu-id="66ca3-103">Как получить контекст печатающего устройства</span><span class="sxs-lookup"><span data-stu-id="66ca3-103">How To: Retrieve a Printer Device Context</span></span>

<span data-ttu-id="66ca3-104">В этом разделе описывается, как получить контекст печатающего устройства.</span><span class="sxs-lookup"><span data-stu-id="66ca3-104">This topic describes how to retrieve a printer device context.</span></span> <span data-ttu-id="66ca3-105">Контекст печатающего устройства можно получить, вызвав функцию [**креатедк**](/windows/desktop/api/wingdi/nf-wingdi-createdca) напрямую или выполнив общее диалоговое окно **Печать** .</span><span class="sxs-lookup"><span data-stu-id="66ca3-105">You can retrieve a printer device context by calling the [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) function directly, or it can be returned by a **Print** common dialog box.</span></span>

<span data-ttu-id="66ca3-106">При отображении общего диалогового окна « **Печать** » пользователь сможет выбрать принтер, страницы документа и число копий документов, которые нужно напечатать.</span><span class="sxs-lookup"><span data-stu-id="66ca3-106">When you display a **Print** common dialog box a user will be able to select the printer, the pages of the document, and the number of document copies they want to print.</span></span> <span data-ttu-id="66ca3-107">Диалоговое окно « **Печать** общего» возвращает эти варианты в структуре данных.</span><span class="sxs-lookup"><span data-stu-id="66ca3-107">The **Print** common dialog box returns these selections in a data structure.</span></span>

<span data-ttu-id="66ca3-108">В этом разделе описывается, как получить контекст печатающего устройства с помощью следующих методов.</span><span class="sxs-lookup"><span data-stu-id="66ca3-108">This topic describes how to obtain a printer device context by using the following methods.</span></span>

-   [<span data-ttu-id="66ca3-109">Вызов Креатедк</span><span class="sxs-lookup"><span data-stu-id="66ca3-109">Call CreateDC</span></span>](#call-createdc)
-   [<span data-ttu-id="66ca3-110">Отображение общего диалогового окна «Печать»</span><span class="sxs-lookup"><span data-stu-id="66ca3-110">Display a Print Common Dialog Box</span></span>](#display-a-print-common-dialog-box)
    -   [<span data-ttu-id="66ca3-111">Использование функции Принтдлжекс</span><span class="sxs-lookup"><span data-stu-id="66ca3-111">Using the PrintDlgEx Function</span></span>](#using-the-printdlgex-function)
    -   [<span data-ttu-id="66ca3-112">Использование функции Принтдлг</span><span class="sxs-lookup"><span data-stu-id="66ca3-112">Using the PrintDlg Function</span></span>](#using-the-printdlg-function)

## <a name="call-createdc"></a><span data-ttu-id="66ca3-113">Вызов Креатедк</span><span class="sxs-lookup"><span data-stu-id="66ca3-113">Call CreateDC</span></span>

<span data-ttu-id="66ca3-114">Если известно устройство, на которое нужно выполнить печать, можно вызвать [**креатедк**](/windows/desktop/api/wingdi/nf-wingdi-createdca) и передать эту информацию непосредственно в функцию.</span><span class="sxs-lookup"><span data-stu-id="66ca3-114">If you know the device to which you want to print, you can call [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) and pass that information directly to the function.</span></span> <span data-ttu-id="66ca3-115">**Креатедк** Возвращает контекст устройства, в котором можно визуализировать содержимое для печати.</span><span class="sxs-lookup"><span data-stu-id="66ca3-115">**CreateDC** returns a device context into which you can render the content to print.</span></span>

<span data-ttu-id="66ca3-116">Самый простой вызов для получения контекста устройства показан в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="66ca3-116">The simplest call to retrieve a device context is shown in the code example that follows.</span></span> <span data-ttu-id="66ca3-117">Код в этом примере извлекает контекст устройства для устройства вывода по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="66ca3-117">The code in this example retrieves a device context to the default display device.</span></span>


```C++
    hDC = CreateDC(TEXT("DISPLAY"),NULL,NULL,NULL);
```



<span data-ttu-id="66ca3-118">Чтобы подготовиться к просмотру на определенном принтере, необходимо указать "ВИНСПУЛ" в качестве устройства и передать правильное имя принтера в [**креатедк**](/windows/desktop/api/wingdi/nf-wingdi-createdca).</span><span class="sxs-lookup"><span data-stu-id="66ca3-118">To render to a specific printer, you must specify "WINSPOOL" as the device and pass the correct name of the printer to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca).</span></span> <span data-ttu-id="66ca3-119">Можно также передать структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) в вызове **креатедк** , если вы хотите предоставить данные инициализации для драйвера устройства при создании контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="66ca3-119">You can also pass a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure in the call to **CreateDC** if you want to provide device-specific initialization data for the device driver when you create the device context.</span></span>

<span data-ttu-id="66ca3-120">В следующем примере показан вызов [**креатедк**](/windows/desktop/api/wingdi/nf-wingdi-createdca) , в котором выбран драйвер "винспул", а имя принтера указано по имени.</span><span class="sxs-lookup"><span data-stu-id="66ca3-120">The following example shows a call to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) in which the "WINSPOOL" driver is selected and the printer name is specified by name.</span></span>


```C++
    printerDC = CreateDC( L"WINSPOOL", printerName, NULL, NULL);
```



<span data-ttu-id="66ca3-121">Вы можете получить точную строку имени принтера для передачи в [**креатедк**](/windows/desktop/api/wingdi/nf-wingdi-createdca) , вызвав функцию [**енумпринтерс**](enumprinters.md) .</span><span class="sxs-lookup"><span data-stu-id="66ca3-121">You can obtain the exact printer name string to pass to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) by calling the [**EnumPrinters**](enumprinters.md) function.</span></span> <span data-ttu-id="66ca3-122">В следующем примере кода показано, как вызвать **енумпринтерс** и получить имена локальных и локально подключенных принтеров.</span><span class="sxs-lookup"><span data-stu-id="66ca3-122">The following code example shows how to call **EnumPrinters** and get the names of the local and locally connected printers.</span></span> <span data-ttu-id="66ca3-123">Так как размер требуемого буфера не может быть заранее известен, **енумпринтерс** вызывается два раза.</span><span class="sxs-lookup"><span data-stu-id="66ca3-123">Because the size of the required buffer cannot be known in advance, the **EnumPrinters** is called two times.</span></span> <span data-ttu-id="66ca3-124">Первый вызов возвращает размер требуемого буфера.</span><span class="sxs-lookup"><span data-stu-id="66ca3-124">The first call returns the size of the required buffer.</span></span> <span data-ttu-id="66ca3-125">Эта информация используется для выделения буфера требуемого размера, а второй вызов **енумпринтерс** возвращает необходимые данные.</span><span class="sxs-lookup"><span data-stu-id="66ca3-125">That information is used to allocate a buffer of the required size, and the second call to **EnumPrinters** returns the data that you want.</span></span>


```C++
    fnReturn = EnumPrinters(
                PRINTER_ENUM_LOCAL | PRINTER_ENUM_CONNECTIONS,
                NULL,
                1L,                // printer info level
                (LPBYTE)NULL,
                0L,
                &dwNeeded,
                &dwReturned);
    
    if (dwNeeded > 0)
    {
        pInfo = (PRINTER_INFO_1 *)HeapAlloc(
                    GetProcessHeap(), 0L, dwNeeded);
    }

    if (NULL != pInfo)
    {
        dwReturned = 0;
        fnReturn = EnumPrinters(
                PRINTER_ENUM_LOCAL | PRINTER_ENUM_CONNECTIONS,
                NULL,
                1L,                // printer info level
                (LPBYTE)pInfo,
                dwNeeded,
                &dwNeeded,
                &dwReturned);
    }

    if (fnReturn)
    {
        // Review the information from all the printers
        //  returned by EnumPrinters.
        for (i=0; i < dwReturned; i++)
        {
            // pThisInfo[i]->pName contains the printer
            //  name to use in the CreateDC function call.
            //
            // When this desired printer is found in the list of
            //  returned printer, set the printerName value to 
            //  use in the call to CreateDC.

            // printerName = pThisInfo[i]->pName
        }
    }
```



## <a name="display-a-print-common-dialog-box"></a><span data-ttu-id="66ca3-126">Отображение общего диалогового окна «Печать»</span><span class="sxs-lookup"><span data-stu-id="66ca3-126">Display a Print Common Dialog Box</span></span>

<span data-ttu-id="66ca3-127">Можно выбрать один из двух общих диалоговых окон **печати** для отображения пользователю. новое диалоговое окно, которое можно отобразить, вызвав функцию [**принтдлжекс**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) и диалоговое окно старого стиля, которое можно отобразить, вызвав функцию [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="66ca3-127">You can choose from two **Print** common dialog boxes to display to a user; the newer dialog box, which you can display by calling the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function, and the older style dialog box, which you can display by calling the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function.</span></span> <span data-ttu-id="66ca3-128">В следующих разделах описывается вызов каждого диалогового окна из приложения.</span><span class="sxs-lookup"><span data-stu-id="66ca3-128">The following sections describe how to call each dialog box from an application.</span></span>

### <a name="using-the-printdlgex-function"></a><span data-ttu-id="66ca3-129">Использование функции Принтдлжекс</span><span class="sxs-lookup"><span data-stu-id="66ca3-129">Using the PrintDlgEx Function</span></span>

<span data-ttu-id="66ca3-130">Вызовите функцию [**принтдлжекс**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) для отображения страницы свойств **Печать** .</span><span class="sxs-lookup"><span data-stu-id="66ca3-130">Call the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to display the **Print** property sheet.</span></span> <span data-ttu-id="66ca3-131">С помощью страницы свойств пользователь может указать сведения о задании печати.</span><span class="sxs-lookup"><span data-stu-id="66ca3-131">By using the property sheet, the user can specify information about the print job.</span></span> <span data-ttu-id="66ca3-132">Например, пользователь может выбрать диапазон страниц для печати, число копий и т. д.</span><span class="sxs-lookup"><span data-stu-id="66ca3-132">For example, the user can select a range of pages to print, the number of copies, and so on.</span></span> <span data-ttu-id="66ca3-133">**Принтдлжекс** также может получить маркер для контекста устройства для выбранного принтера.</span><span class="sxs-lookup"><span data-stu-id="66ca3-133">The **PrintDlgEx** can also retrieve a handle to a device context for the selected printer.</span></span> <span data-ttu-id="66ca3-134">Вы можете использовать этот маркер для отрисовки выходных данных на принтере.</span><span class="sxs-lookup"><span data-stu-id="66ca3-134">You can use the handle to render output on the printer.</span></span>

<span data-ttu-id="66ca3-135">Пример кода, иллюстрирующий использование [**принтдлжекс**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) для получения контекста печатающего устройства, см. в разделе «Использование страницы свойств печати» раздела « [использование общих диалоговых](../dlgbox/using-common-dialog-boxes.md)окон».</span><span class="sxs-lookup"><span data-stu-id="66ca3-135">For sample code that illustrates the use of [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) to retrieve a printer device context, see "Using the Print Property Sheet" in [Using Common Dialog Boxes](../dlgbox/using-common-dialog-boxes.md).</span></span>

### <a name="using-the-printdlg-function"></a><span data-ttu-id="66ca3-136">Использование функции Принтдлг</span><span class="sxs-lookup"><span data-stu-id="66ca3-136">Using the PrintDlg Function</span></span>

<span data-ttu-id="66ca3-137">Если приложение должно выполняться в системе, которая не поддерживает функцию [**принтдлжекс**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) , например в системе, где используется версия Windows, предшествующая Windows 2000, или не требуются дополнительные функции, предоставляемые функцией **принтдлжекс** , используйте функцию [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="66ca3-137">If your application must run on a system that does not support the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function, such as on a system that is running a version of Windows earlier than Windows 2000, or does not need the extra functionality that the **PrintDlgEx** function provides, use the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function.</span></span> <span data-ttu-id="66ca3-138">В следующих шагах описывается, как отобразить диалоговое окно "Общие" для **печати** старого стиля.</span><span class="sxs-lookup"><span data-stu-id="66ca3-138">The following steps describe how to display the older style **Print** common dialog box.</span></span>

1.  <span data-ttu-id="66ca3-139">Инициализируйте структуру данных [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="66ca3-139">Initialize the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) data structure.</span></span>
2.  <span data-ttu-id="66ca3-140">Вызовите [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) , чтобы отобразить для пользователя общее диалоговое окно **печати** .</span><span class="sxs-lookup"><span data-stu-id="66ca3-140">Call [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) to display the **Print** common dialog box to the user.</span></span>
3.  <span data-ttu-id="66ca3-141">Если вызов [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) возвращает **значение true**, блокирует возвращенную память структуры [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .</span><span class="sxs-lookup"><span data-stu-id="66ca3-141">If the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) call returns **TRUE**, lock the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure memory.</span></span> <span data-ttu-id="66ca3-142">Если вызов **принтдлг** возвращает **значение false**, пользователь нажал кнопку **Отмена** в диалоговом окне **Печать** общего, чтобы больше не обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="66ca3-142">If the **PrintDlg** call returns **FALSE**, the user pressed the **Cancel** button in the **Print** common dialog box so there is nothing more to process.</span></span>
4.  <span data-ttu-id="66ca3-143">Выделите буфер локальной памяти, достаточно большой для хранения копии структуры [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .</span><span class="sxs-lookup"><span data-stu-id="66ca3-143">Allocate a local memory buffer that is large enough to contain a copy of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>
5.  <span data-ttu-id="66ca3-144">Скопируйте возвращенную структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) в локально выделенный.</span><span class="sxs-lookup"><span data-stu-id="66ca3-144">Copy the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure to the locally allocated one.</span></span>
6.  <span data-ttu-id="66ca3-145">Сохраните другие сведения, возвращаемые в структуре [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) , и необходимо обработать задание печати.</span><span class="sxs-lookup"><span data-stu-id="66ca3-145">Save other information that is returned in the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure and that you will need to process the print job.</span></span>
7.  <span data-ttu-id="66ca3-146">Освободите [**принтдлг**](/windows/win32/api/commdlg/ns-commdlg-printdlga) и буферы памяти, на которые он ссылается.</span><span class="sxs-lookup"><span data-stu-id="66ca3-146">Free the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) and the memory buffers it references.</span></span>

<span data-ttu-id="66ca3-147">В следующем примере кода показано, как использовать функцию [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) для получения контекста устройства и имени выбранного принтера.</span><span class="sxs-lookup"><span data-stu-id="66ca3-147">The following example code illustrates how to use the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function to get the device context and the name of selected printer.</span></span>


```C++
// Display the printer dialog box so the user can select the 
//  printer and the number of copies to print.
BOOL            printDlgReturn = FALSE;
HDC                printerDC = NULL;
PRINTDLG        printDlgInfo = {0};
LPWSTR            localPrinterName = NULL;
PDEVMODE        returnedDevmode = NULL;
PDEVMODE        localDevmode = NULL;
int                localNumberOfCopies = 0;

// Initialize the print dialog box's data structure.
printDlgInfo.lStructSize = sizeof( printDlgInfo );
printDlgInfo.Flags = 
    // Return a printer device context.
    PD_RETURNDC 
    // Don't allow separate print to file.
    // Remove these flags if you want to support this feature.
    | PD_HIDEPRINTTOFILE        
    | PD_DISABLEPRINTTOFILE 
    // Don't allow selecting individual document pages to print.
    // Remove this flag if you want to support this feature.
    | PD_NOSELECTION;

// Display the printer dialog and retrieve the printer DC.
printDlgReturn = PrintDlg(&printDlgInfo);

// Check the return value.
if (TRUE == printDlgReturn)
{
    // The user clicked OK so the printer dialog box data 
    //  structure was returned with the user's selections.
    //  Copy the relevant data from the data structure and 
    //  save them to a local data structure.

    //
    // Get the HDC of the selected printer
    printerDC = printDlgInfo.hDC;
    
    // In this example, the DEVMODE structure returned by 
    //    the printer dialog box is copied to a local memory
    //    block and a pointer to the printer name that is 
    //    stored in the copied DEVMODE structure is saved.

    //
    //  Lock the handle to get a pointer to the DEVMODE structure.
    returnedDevmode = (PDEVMODE)GlobalLock(printDlgInfo.hDevMode);

    localDevmode = (LPDEVMODE)HeapAlloc(
                        GetProcessHeap(), 
                        HEAP_ZERO_MEMORY | HEAP_GENERATE_EXCEPTIONS, 
                        returnedDevmode->dmSize);

    if (NULL != localDevmode) 
    {
        memcpy(
            (LPVOID)localDevmode,
            (LPVOID)returnedDevmode, 
            returnedDevmode->dmSize);

        // Save the printer name from the DEVMODE structure.
        //  This is done here just to illustrate how to access
        //  the name field. The printer name can also be accessed
        //  by referring to the dmDeviceName in the local 
        //  copy of the DEVMODE structure.
        localPrinterName = localDevmode->dmDeviceName;

        // Save the number of copies as entered by the user
        localNumberOfCopies = printDlgInfo.nCopies;    
    }
    else
    {
        // Unable to allocate a new structure so leave
        //  the pointer as NULL to indicate that it's empty.
    }

    // Free the DEVMODE structure returned by the print 
    //  dialog box.
    if (NULL != printDlgInfo.hDevMode) 
    {
        GlobalFree(printDlgInfo.hDevMode);
    }
}
else
{
    // The user cancelled out of the print dialog box.
}
```



<span data-ttu-id="66ca3-148">Дополнительные сведения о функции [**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) см. в разделе "Отображение диалогового окна печати" раздела [использование общих диалоговых](../dlgbox/using-common-dialog-boxes.md)окон.</span><span class="sxs-lookup"><span data-stu-id="66ca3-148">For more information about the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function, see "Displaying the Print Dialog Box" in [Using Common Dialog Boxes](../dlgbox/using-common-dialog-boxes.md).</span></span>

 

 
