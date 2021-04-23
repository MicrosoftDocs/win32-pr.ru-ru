---
title: Печать содержимого элементов управления Rich Edit
description: В этом разделе содержатся сведения о печати содержимого элементов управления Rich Edit.
ms.assetid: d61e2e11-d848-43fc-9622-b3b2032bda48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a304e5c09b5f8ea934c90873c3d915179295964e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105654383"
---
# <a name="how-to-print-the-contents-of-rich-edit-controls"></a><span data-ttu-id="27b8f-103">Печать содержимого элементов управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="27b8f-103">How to Print the Contents of Rich Edit Controls</span></span>

<span data-ttu-id="27b8f-104">В этом разделе содержатся сведения о печати содержимого элементов управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="27b8f-104">This section contains information about how to print the contents of rich edit controls.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="27b8f-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="27b8f-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="27b8f-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="27b8f-106">Technologies</span></span>

-   [<span data-ttu-id="27b8f-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="27b8f-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="27b8f-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="27b8f-108">Prerequisites</span></span>

-   <span data-ttu-id="27b8f-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="27b8f-109">C/C++</span></span>
-   <span data-ttu-id="27b8f-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="27b8f-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="27b8f-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="27b8f-111">Instructions</span></span>

### <a name="use-print-preview"></a><span data-ttu-id="27b8f-112">Использовать предварительный просмотр</span><span class="sxs-lookup"><span data-stu-id="27b8f-112">Use Print Preview</span></span>

<span data-ttu-id="27b8f-113">Чтобы отформатировать текст в элементе управления Rich Edit, который будет отображаться на целевом устройстве (обычно на печатной странице), отправьте сообщение [**\_ сеттаржетдевице EM**](em-settargetdevice.md) , передав маркер в контекст устройства (HDC) целевого устройства и желаемую ширину линии.</span><span class="sxs-lookup"><span data-stu-id="27b8f-113">To format text in a rich edit control as it will appear on a target device (usually the printed page), send the [**EM\_SETTARGETDEVICE**](em-settargetdevice.md) message, passing in the handle to a device context (HDC) of the target device and the desired line width.</span></span> <span data-ttu-id="27b8f-114">Обычно вы получаете толщину линии, вызывая [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) для целевого HDC.</span><span class="sxs-lookup"><span data-stu-id="27b8f-114">Usually you will obtain the line width by calling [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) for the target HDC.</span></span>

### <a name="format-print-for-a-specific-device"></a><span data-ttu-id="27b8f-115">Форматирование печати для определенного устройства</span><span class="sxs-lookup"><span data-stu-id="27b8f-115">Format Print for a Specific Device</span></span>

<span data-ttu-id="27b8f-116">Чтобы форматировать часть содержимого элемента управления Rich Edit для конкретного устройства, отправьте сообщение [**EM \_ форматранже**](em-formatrange.md) .</span><span class="sxs-lookup"><span data-stu-id="27b8f-116">To format part of a rich edit control's contents for a specific device, send the [**EM\_FORMATRANGE**](em-formatrange.md) message.</span></span> <span data-ttu-id="27b8f-117">Структура [**форматранже**](/windows/desktop/api/Richedit/ns-richedit-formatrange) , используемая с этим сообщением, определяет диапазон текста для форматирования, а также параметр hdc для целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="27b8f-117">The [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) structure that is used with this message specifies the range of text to format as well as the HDC for the target device.</span></span> <span data-ttu-id="27b8f-118">При необходимости это сообщение также отправляет текст на принтер.</span><span class="sxs-lookup"><span data-stu-id="27b8f-118">Optionally, this message also sends the text to the printer.</span></span>

### <a name="use-banding"></a><span data-ttu-id="27b8f-119">Использовать чередование</span><span class="sxs-lookup"><span data-stu-id="27b8f-119">Use Banding</span></span>

<span data-ttu-id="27b8f-120">Чередование — это процесс, с помощью которого одна страница выходных данных создается с использованием одного или нескольких отдельных прямоугольников или делений.</span><span class="sxs-lookup"><span data-stu-id="27b8f-120">Banding is the process by which a single page of output is generated using one or more separate rectangles, or bands.</span></span> <span data-ttu-id="27b8f-121">Когда на странице помещаются все полосы, происходит полное изображение.</span><span class="sxs-lookup"><span data-stu-id="27b8f-121">When all bands are placed on the page, a complete image results.</span></span> <span data-ttu-id="27b8f-122">Этот подход часто используется для растровых принтеров, которые не имеют достаточного объема памяти или могут одновременно создавать изображения на полной странице.</span><span class="sxs-lookup"><span data-stu-id="27b8f-122">This approach is often used by raster printers that do not have sufficient memory or ability to image a full page at one time.</span></span>

<span data-ttu-id="27b8f-123">Чтобы реализовать чередование, используйте сообщение [**EM \_ дисплайбанд**](em-displayband.md) для отправки последовательных частей содержимого элемента управления Rich Edit на устройство.</span><span class="sxs-lookup"><span data-stu-id="27b8f-123">To implement banding, use the [**EM\_DISPLAYBAND**](em-displayband.md) message to send successive portions of the rich edit control's content to the device.</span></span> <span data-ttu-id="27b8f-124">Это сообщение выводится на устройство, указанное в предыдущем вызове [**EM \_ форматранже**](em-formatrange.md).</span><span class="sxs-lookup"><span data-stu-id="27b8f-124">This message prints to the device that was specified in a previous call to [**EM\_FORMATRANGE**](em-formatrange.md).</span></span> <span data-ttu-id="27b8f-125">Конечно, параметр *wParam* сообщения **EM \_ форматранже** должен быть равен нулю, поэтому печать не инициируется этим сообщением.</span><span class="sxs-lookup"><span data-stu-id="27b8f-125">Of course, the *wParam* parameter of the **EM\_FORMATRANGE** message should be zero, so that printing is not initiated by that message.</span></span>

## <a name="printrtf-code-example"></a><span data-ttu-id="27b8f-126">Пример кода Принтртф</span><span class="sxs-lookup"><span data-stu-id="27b8f-126">PrintRTF Code Example</span></span>

<span data-ttu-id="27b8f-127">Следующий пример кода выводит содержимое элемента управления Rich Edit на указанный принтер.</span><span class="sxs-lookup"><span data-stu-id="27b8f-127">The following example code prints the contents of a rich edit control to the specified printer.</span></span>


```C++
// hwnd is the HWND of the rich edit control.
// hdc is the HDC of the printer. This value can be obtained for the 
// default printer as follows:
//
//     PRINTDLG pd = { sizeof(pd) };
//     pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
//
//     if (PrintDlg(&pd))
//     {
//        HDC hdc = pd.hDC;
//        ...
//     }

BOOL PrintRTF(HWND hwnd, HDC hdc)
{
    DOCINFO di = { sizeof(di) };
    
    if (!StartDoc(hdc, &di))
    {
        return FALSE;
    }

    int cxPhysOffset = GetDeviceCaps(hdc, PHYSICALOFFSETX);
    int cyPhysOffset = GetDeviceCaps(hdc, PHYSICALOFFSETY);
    
    int cxPhys = GetDeviceCaps(hdc, PHYSICALWIDTH);
    int cyPhys = GetDeviceCaps(hdc, PHYSICALHEIGHT);

    // Create "print preview". 
    SendMessage(hwnd, EM_SETTARGETDEVICE, (WPARAM)hdc, cxPhys/2);

    FORMATRANGE fr;

    fr.hdc       = hdc;
    fr.hdcTarget = hdc;

    // Set page rect to physical page size in twips.
    fr.rcPage.top    = 0;  
    fr.rcPage.left   = 0;  
    fr.rcPage.right  = MulDiv(cxPhys, 1440, GetDeviceCaps(hDC, LOGPIXELSX));  
    fr.rcPage.bottom = MulDiv(cyPhys, 1440, GetDeviceCaps(hDC, LOGPIXELSY)); 

    // Set the rendering rectangle to the pintable area of the page.
    fr.rc.left   = cxPhysOffset;
    fr.rc.right  = cxPhysOffset + cxPhys;
    fr.rc.top    = cyPhysOffset;
    fr.rc.bottom = cyPhysOffset + cyPhys;

    SendMessage(hwnd, EM_SETSEL, 0, (LPARAM)-1);          // Select the entire contents.
    SendMessage(hwnd, EM_EXGETSEL, 0, (LPARAM)&fr.chrg);  // Get the selection into a CHARRANGE.

    BOOL fSuccess = TRUE;

    // Use GDI to print successive pages.
    while (fr.chrg.cpMin < fr.chrg.cpMax && fSuccess) 
    {
        fSuccess = StartPage(hdc) > 0;
        
        if (!fSuccess) break;
        
        int cpMin = SendMessage(hwnd, EM_FORMATRANGE, TRUE, (LPARAM)&fr);
        
        if (cpMin <= fr.chrg.cpMin) 
        {
            fSuccess = FALSE;
            break;
        }
        
        fr.chrg.cpMin = cpMin;
        fSuccess = EndPage(hdc) > 0;
    }
    
    SendMessage(hwnd, EM_FORMATRANGE, FALSE, 0);
    
    if (fSuccess)
    {
        EndDoc(hdc);
    } 
    
    else 
    
    {
        AbortDoc(hdc);
    }
    
    return fSuccess;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="27b8f-128">См. также</span><span class="sxs-lookup"><span data-stu-id="27b8f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27b8f-129">Использование элементов управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="27b8f-129">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="27b8f-130">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="27b8f-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 