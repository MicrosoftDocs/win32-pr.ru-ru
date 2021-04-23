---
title: Отображение подсказок для кнопок
description: При указании \_ стиля подсказок тбстиле панель инструментов создает элемент управления ToolTip и управляет им. Элемент управления ToolTip скрыт и появляется, только если пользователь наводит указатель мыши на кнопку панели инструментов и оставляет его примерно на одну секунду.
ms.assetid: 0383DB63-A10E-4235-A974-AB21551E086B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb37de7c21c904673a1f656533497130d50bd8f7
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "103890339"
---
# <a name="how-to-display-tooltips-for-buttons"></a><span data-ttu-id="fe5ff-104">Отображение подсказок для кнопок</span><span class="sxs-lookup"><span data-stu-id="fe5ff-104">How to Display Tooltips for Buttons</span></span>

<span data-ttu-id="fe5ff-105">При указании стиля [**\_ подсказок тбстиле**](toolbar-control-and-button-styles.md) панель инструментов создает элемент управления ToolTip и управляет им.</span><span class="sxs-lookup"><span data-stu-id="fe5ff-105">When you specify the [**TBSTYLE\_TOOLTIPS**](toolbar-control-and-button-styles.md) style, the toolbar creates and manages a tooltip control.</span></span> <span data-ttu-id="fe5ff-106">Элемент управления ToolTip скрыт и появляется, только если пользователь наводит указатель мыши на кнопку панели инструментов и оставляет его примерно на одну секунду.</span><span class="sxs-lookup"><span data-stu-id="fe5ff-106">The tooltip control is hidden and appears only when users move the pointer over a toolbar button and leave it there for approximately one second.</span></span>

<span data-ttu-id="fe5ff-107">Приложение может передать текст в элемент управления ToolTip одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="fe5ff-107">Your application can supply text to the tooltip control in any one of the following ways:</span></span>

-   <span data-ttu-id="fe5ff-108">Установите текст подсказки в качестве элемента **истринг** структуры [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) для каждой кнопки.</span><span class="sxs-lookup"><span data-stu-id="fe5ff-108">Set the tooltip text as the **iString** member of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure for each button.</span></span> <span data-ttu-id="fe5ff-109">Кроме того, необходимо отправить [**сообщение \_ Сетмакстекстровс в ТБ**](tb-setmaxtextrows.md) и установить максимальное число строк в 0, чтобы текст не отображался как метка кнопки, а не как всплывающая подсказка.</span><span class="sxs-lookup"><span data-stu-id="fe5ff-109">You must also send a [**TB\_SETMAXTEXTROWS**](tb-setmaxtextrows.md) message and set the maximum text rows to 0, so that the text does not appear as the button label rather than as a tooltip.</span></span>
-   <span data-ttu-id="fe5ff-110">Создайте панель инструментов со стилем [**\_ списка тбстиле**](toolbar-control-and-button-styles.md) , а затем задайте расширенный стиль [**тбстиле \_ ex \_ микседбуттонс**](toolbar-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fe5ff-110">Create the toolbar with the [**TBSTYLE\_LIST**](toolbar-control-and-button-styles.md) style and then set the [**TBSTYLE\_EX\_MIXEDBUTTONS**](toolbar-extended-styles.md) extended style.</span></span> <span data-ttu-id="fe5ff-111">Метки отображаются только для кнопок, имеющих стиль [**бтнс \_ SHOWTEXT**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fe5ff-111">Labels are shown only for buttons that have the [**BTNS\_SHOWTEXT**](toolbar-control-and-button-styles.md) style.</span></span> <span data-ttu-id="fe5ff-112">Для кнопок, у которых нет этого стиля, отображается подсказка, содержащая текст кнопки.</span><span class="sxs-lookup"><span data-stu-id="fe5ff-112">For buttons that do not have this style, a tooltip is shown that contains the button text.</span></span>
-   <span data-ttu-id="fe5ff-113">Ответьте на код уведомления [ТТН \_ жетдиспинфо](ttn-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="fe5ff-113">Respond to the [TTN\_GETDISPINFO](ttn-getdispinfo.md) notification code.</span></span>
-   <span data-ttu-id="fe5ff-114">Ответьте на код уведомления [ТБН \_ жетинфотип](tbn-getinfotip.md) .</span><span class="sxs-lookup"><span data-stu-id="fe5ff-114">Respond to the [TBN\_GETINFOTIP](tbn-getinfotip.md) notification code.</span></span>

<span data-ttu-id="fe5ff-115">Приложение, которому требуется отправить сообщения непосредственно в элемент управления ToolTip, может получить этот маркер в элементе управления с помощью сообщения [**TB \_**](tb-gettooltips.md) .</span><span class="sxs-lookup"><span data-stu-id="fe5ff-115">An application that needs to send messages directly to the tooltip control can retrieve the handle to the control by using the [**TB\_GETTOOLTIPS**](tb-gettooltips.md) message.</span></span> <span data-ttu-id="fe5ff-116">Приложение может заменить элемент управления ToolTip панели инструментов другим элементом управления ToolTip с помощью сообщения [**\_ сеттултипс ТБ**](tb-settooltips.md) .</span><span class="sxs-lookup"><span data-stu-id="fe5ff-116">An application can replace the tooltip control of a toolbar with another tooltip control by using the [**TB\_SETTOOLTIPS**](tb-settooltips.md) message.</span></span>

<span data-ttu-id="fe5ff-117">Самый гибкий способ предоставления текста подсказки — ответ на код уведомления [ТТН \_ Жетдиспинфо](ttn-getdispinfo.md) или [ТБН \_ жетинфотип](tbn-getinfotip.md) , отправленный элементом управления ToolBar на родительский элемент в форме сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fe5ff-117">The most flexible way of supplying tooltip text is to respond to the [TTN\_GETDISPINFO](ttn-getdispinfo.md) or [TBN\_GETINFOTIP](tbn-getinfotip.md) notification code sent by the toolbar control to its parent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="fe5ff-118">Для [ТТН \_ Жетдиспинфо](ttn-getdispinfo.md)параметр *lParam* включает указатель на структуру [**Нмттдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) (также определенную как **лптултиптекст**), которая указывает идентификатор команды для кнопки, для которой требуется текст справки.</span><span class="sxs-lookup"><span data-stu-id="fe5ff-118">For [TTN\_GETDISPINFO](ttn-getdispinfo.md), the *lParam* parameter includes a pointer to an [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure (also defined as **LPTOOLTIPTEXT**) that specifies the command identifier of the button for which Help text is needed.</span></span> <span data-ttu-id="fe5ff-119">Этот идентификатор находится в элементе **нмттдиспинфо. HDR. идфром** .</span><span class="sxs-lookup"><span data-stu-id="fe5ff-119">This identifier is in the **NMTTDISPINFO.hdr.idFrom** member.</span></span> <span data-ttu-id="fe5ff-120">Приложение может скопировать текст справки в структуру, указать адрес строки, содержащей текст справки, или указать идентификатор ресурса строкового ресурса.</span><span class="sxs-lookup"><span data-stu-id="fe5ff-120">An application can copy the Help text to the structure, specify the address of a string containing the Help text, or specify the instance handle and resource identifier of a string resource.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="fe5ff-121">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="fe5ff-121">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="fe5ff-122">Технологии</span><span class="sxs-lookup"><span data-stu-id="fe5ff-122">Technologies</span></span>

-   [<span data-ttu-id="fe5ff-123">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="fe5ff-123">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="fe5ff-124">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="fe5ff-124">Prerequisites</span></span>

-   <span data-ttu-id="fe5ff-125">C/C++</span><span class="sxs-lookup"><span data-stu-id="fe5ff-125">C/C++</span></span>
-   <span data-ttu-id="fe5ff-126">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="fe5ff-126">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="fe5ff-127">Инструкции</span><span class="sxs-lookup"><span data-stu-id="fe5ff-127">Instructions</span></span>

### <a name="display-a-tooltip-for-a-button"></a><span data-ttu-id="fe5ff-128">Отображение всплывающей подсказки для кнопки</span><span class="sxs-lookup"><span data-stu-id="fe5ff-128">Display a Tooltip for a Button</span></span>

<span data-ttu-id="fe5ff-129">Следующий пример кода обрабатывает код уведомления подсказки [ТТН \_ жетдиспинфо](ttn-getdispinfo.md) , предоставляя текст из идентификаторов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe5ff-129">The following example code handles the [TTN\_GETDISPINFO](ttn-getdispinfo.md) tooltip notification code by providing text from resource identifiers.</span></span>


```C++
case WM_NOTIFY: 
            
    switch (((LPNMHDR) lParam)->code) 
    {
    
    case TTN_GETDISPINFO: 
        { 
            LPTOOLTIPTEXT lpttt = (LPTOOLTIPTEXT)lParam; 
            
            // Set the instance of the module that contains the resource.
            lpttt->hinst = g_hInst; 
            
            UINT_PTR idButton = lpttt->hdr.idFrom;
            
            switch (idButton) 
            { 
            case IDM_NEW: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_NEW); 
                break; 
                
            case IDM_OPEN: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_OPEN); 
                break; 
                
            case IDM_SAVE: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_SAVE); 
                break; 
            } 
            
            break; 
        } 
    }
    return TRUE;
```



## <a name="related-topics"></a><span data-ttu-id="fe5ff-130">См. также</span><span class="sxs-lookup"><span data-stu-id="fe5ff-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe5ff-131">Использование элементов управления ToolBar</span><span class="sxs-lookup"><span data-stu-id="fe5ff-131">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="fe5ff-132">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="fe5ff-132">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




