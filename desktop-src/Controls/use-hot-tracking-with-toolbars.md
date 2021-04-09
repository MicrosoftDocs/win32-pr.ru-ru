---
title: Использование Hot-Tracking с панелями инструментов
description: Когда указатель мыши наводится на элемент, он начинает быть активным. Если включено отслеживание, горячий элемент выделяется. Панель инструментов, созданная с помощью ТБСТИЛЕ \_ плоского стиля или использующего стили оформления, поддерживает по умолчанию функцию оперативного отслеживания.
ms.assetid: E77B15D7-F0C9-41F7-8BE9-30260FA4BB0C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a486407b8dafade1e3bba083c5a56f3a9be2adcf
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "104069722"
---
# <a name="how-to-use-hot-tracking-with-toolbars"></a><span data-ttu-id="005c8-105">Использование Hot-Tracking с панелями инструментов</span><span class="sxs-lookup"><span data-stu-id="005c8-105">How to Use Hot-Tracking with Toolbars</span></span>

<span data-ttu-id="005c8-106">Когда указатель мыши наводится на элемент, он начинает быть активным.</span><span class="sxs-lookup"><span data-stu-id="005c8-106">When a mouse pointer hovers over an item, the item becomes hot.</span></span> <span data-ttu-id="005c8-107">Если включено отслеживание, горячий элемент выделяется.</span><span class="sxs-lookup"><span data-stu-id="005c8-107">If hot-tracking is enabled, the hot item is highlighted.</span></span> <span data-ttu-id="005c8-108">Панель инструментов, созданная с помощью [**тбстиле \_ плоского**](toolbar-control-and-button-styles.md) стиля или использующего [стили оформления](themes-overview.md), поддерживает по умолчанию функцию оперативного отслеживания.</span><span class="sxs-lookup"><span data-stu-id="005c8-108">A toolbar that is created with the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style, or one that uses [Visual Styles](themes-overview.md), supports hot-tracking by default.</span></span>

<span data-ttu-id="005c8-109">Для оперативного отслеживания необходимо создавать списки изображений. Таким образом, нельзя использовать сообщение [**\_ аддбитмап ТБ**](tb-addbitmap.md) или функцию [**креатетулбарекс**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) для создания панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="005c8-109">Hot-tracking requires that you create image lists; therefore, you cannot use the [**TB\_ADDBITMAP**](tb-addbitmap.md) message or the [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) function to create your toolbar.</span></span>

<span data-ttu-id="005c8-110">При наведении указателя мыши на кнопку на панели инструментов отображается кнопка, выделенная для выделения.</span><span class="sxs-lookup"><span data-stu-id="005c8-110">When the mouse hovers over a toolbar button, the button is outlined to highlight it.</span></span> <span data-ttu-id="005c8-111">На следующем рисунке показана панель инструментов с включенной функцией оперативного отслеживания. указатель мыши наводится на кнопку Save (сохранить), когда был сделан снимок экрана.</span><span class="sxs-lookup"><span data-stu-id="005c8-111">The following illustration shows a toolbar with hot-tracking enabled; the mouse pointer was hovering on the Save button when the screen shot was taken.</span></span>

![снимок экрана: диалоговое окно с тремя элементами панели инструментов; Выбранный значок отображается в контуре](images/tb-withstyles.png)

<span data-ttu-id="005c8-113">Если необходимо изменить изображение кнопки панели инструментов при изменении состояния элемента управления, сохраните другие изображения в [списках изображений](image-lists.md).</span><span class="sxs-lookup"><span data-stu-id="005c8-113">If you want a toolbar button bitmap to change when the state of the control changes, store the different images in [image lists](image-lists.md).</span></span> <span data-ttu-id="005c8-114">Например, некоторые приложения имеют черные и белые кнопки панели инструментов, которые становятся цветными, когда они выбраны.</span><span class="sxs-lookup"><span data-stu-id="005c8-114">For example, some applications have black and white toolbar buttons that become colored when they are selected.</span></span> <span data-ttu-id="005c8-115">Два разных образа хранятся в списках изображений.</span><span class="sxs-lookup"><span data-stu-id="005c8-115">The two different images are stored in image lists.</span></span> <span data-ttu-id="005c8-116">Панели инструментов поддерживают использование до трех списков изображений.</span><span class="sxs-lookup"><span data-stu-id="005c8-116">Toolbars support using up to three image lists.</span></span> <span data-ttu-id="005c8-117">Как правило, в приложении используется список образов по умолчанию, отключен и горячая отслеживание.</span><span class="sxs-lookup"><span data-stu-id="005c8-117">Typically an application has a default, disabled, and hot-tracking list of images.</span></span> <span data-ttu-id="005c8-118">Чтобы задать и получить списки изображений для кнопок активной панели инструментов, используйте сообщения [**\_ Жесотимажелист**](tb-gethotimagelist.md) в [**ТБ \_ сесотимажелист**](tb-sethotimagelist.md) и ТБ.</span><span class="sxs-lookup"><span data-stu-id="005c8-118">To set and retrieve image lists for hot toolbar buttons, use the [**TB\_SETHOTIMAGELIST**](tb-sethotimagelist.md) and [**TB\_GETHOTIMAGELIST**](tb-gethotimagelist.md) messages.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="005c8-119">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="005c8-119">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="005c8-120">Технологии</span><span class="sxs-lookup"><span data-stu-id="005c8-120">Technologies</span></span>

-   [<span data-ttu-id="005c8-121">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="005c8-121">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="005c8-122">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="005c8-122">Prerequisites</span></span>

-   <span data-ttu-id="005c8-123">C/C++</span><span class="sxs-lookup"><span data-stu-id="005c8-123">C/C++</span></span>
-   <span data-ttu-id="005c8-124">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="005c8-124">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="005c8-125">Инструкции</span><span class="sxs-lookup"><span data-stu-id="005c8-125">Instructions</span></span>

### <a name="use-hot-tracking-with-a-toolbar"></a><span data-ttu-id="005c8-126">Использование Hot-Tracking с панелью инструментов</span><span class="sxs-lookup"><span data-stu-id="005c8-126">Use Hot-Tracking with a Toolbar</span></span>

<span data-ttu-id="005c8-127">В следующем примере кода создается, заполняется и назначается список изображений для горячих кнопок.</span><span class="sxs-lookup"><span data-stu-id="005c8-127">The following code example creates, fills, and assigns an image list for hot buttons.</span></span>


```C++
// Create the image list, himlHot.
g_himlHot = ImageList_Create(MYICON_CX,MYICON_CY,ILC_COLOR8,0,4);

// Load a bitmap from a resource file, and add the images to the image list.
// Note that the bitmap contains four images.

hBitmapHot = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_HOT));

ImageList_Add(g_himlHot, hBitmapHot, NULL);
   
// Set the image list. 
SendMessage(hwndTB, TB_SETHOTIMAGELIST, 0, (LPARAM)g_himlHot);
   
// Loop to fill the array of TBBUTTON structures.  
for(i=0;i<MAX_BUTTONS;i++)
{
    tbArray[i].iBitmap   = i;                   // Bitmap from image list.
    tbArray[i].idCommand = IDM_BUTTONSTART + i;
    tbArray[i].fsState   = TBSTATE_ENABLED;
    tbArray[i].fsStyle   = BTNS_DROPDOWN;
    tbArray[i].dwData    = 0;
    tbArray[i].iString   = i;
}

DeleteObject(hBitmapHot);    // Delete the loaded bitmap.
```



## <a name="related-topics"></a><span data-ttu-id="005c8-128">См. также</span><span class="sxs-lookup"><span data-stu-id="005c8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="005c8-129">Использование элементов управления ToolBar</span><span class="sxs-lookup"><span data-stu-id="005c8-129">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="005c8-130">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="005c8-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




