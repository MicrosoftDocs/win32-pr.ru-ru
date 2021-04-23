---
title: Обработайте уведомления BCN_DROPDOWN из Сплитбуттонс
description: В этом разделе описывается один из возможных способов реагирования на \_ уведомление в раскрывающемся списке BCN в процедуре диалогового окна.
ms.assetid: 847DD645-AE29-4F62-BC32-F235BA409E1E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a368dd28c5347f438feff75fbddb129a420caae7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104134678"
---
# <a name="how-to-handle-the-bcn_dropdown-notification-from-a-split-button"></a><span data-ttu-id="4ea0f-103">Как управлять \_ уведомлением из раскрывающегося списка BCN с помощью разворачивающейся кнопки</span><span class="sxs-lookup"><span data-stu-id="4ea0f-103">How to Handle the BCN\_DROPDOWN Notification from a Split Button</span></span>

<span data-ttu-id="4ea0f-104">В этом разделе описывается один из возможных способов реагирования на уведомление в [ \_ раскрывающемся списке BCN](bcn-dropdown.md) в процедуре диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-104">This topic describes one possible way of responding to the [BCN\_DROPDOWN](bcn-dropdown.md) notification in a dialog procedure.</span></span>

<span data-ttu-id="4ea0f-105">Приложение C++ получает клиентские координаты кнопки из заголовка уведомления и преобразует их в экранные координаты.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-105">The C++ application retrieves the client coordinates of the button from the notification header and converts them to screen coordinates.</span></span> <span data-ttu-id="4ea0f-106">Затем он создает всплывающее меню и отображает его в нижней части кнопки.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-106">It then creates a popup menu and displays it at the bottom of the button.</span></span> <span data-ttu-id="4ea0f-107">Для упрощения примера сочетания клавиш не реализуются в меню.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-107">To keep the example simple, keyboard shortcuts are not implemented for the menu.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="4ea0f-108">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="4ea0f-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="4ea0f-109">Технологии</span><span class="sxs-lookup"><span data-stu-id="4ea0f-109">Technologies</span></span>

-   [<span data-ttu-id="4ea0f-110">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="4ea0f-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="4ea0f-111">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="4ea0f-111">Prerequisites</span></span>

-   <span data-ttu-id="4ea0f-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="4ea0f-112">C/C++</span></span>
-   <span data-ttu-id="4ea0f-113">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="4ea0f-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="4ea0f-114">Инструкции</span><span class="sxs-lookup"><span data-stu-id="4ea0f-114">Instructions</span></span>

### <a name="step-1-wait-for-the-bcn_dropdown-notification"></a><span data-ttu-id="4ea0f-115">Шаг 1. Дождитесь уведомления в *\_ раскрывающемся списке BCN* .</span><span class="sxs-lookup"><span data-stu-id="4ea0f-115">Step 1: Wait for the *BCN\_DROPDOWN* notification.</span></span>


```C++
case BCN_DROPDOWN:
{
    NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
    if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
    {
```



### <a name="step-2-get-the-screen-coordinates-of-the-button"></a><span data-ttu-id="4ea0f-116">Шаг 2. получение экранных координат кнопки.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-116">Step 2: Get the screen coordinates of the button.</span></span>

<span data-ttu-id="4ea0f-117">Используйте функцию [**клиенттоскрин**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) для преобразования координат окна нижнего левого края кнопки в экранные координаты.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-117">Use the [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) function to convert the window coordinates of the button's lower left edge to screen coordinates.</span></span>


```C++
POINT pt;
pt.x = pDropDown->rcButton.left;
pt.y = pDropDown->rcButton.bottom;
ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
```



### <a name="step-3-create-a-menu-and-add-items"></a><span data-ttu-id="4ea0f-118">Шаг 3. Создание меню и добавление элементов.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-118">Step 3: Create a menu and add items.</span></span>

<span data-ttu-id="4ea0f-119">Для создания меню используйте функцию [**креатепопупмену**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) .</span><span class="sxs-lookup"><span data-stu-id="4ea0f-119">Use the [**CreatePopupMenu**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) function to create a menu.</span></span> <span data-ttu-id="4ea0f-120">Используйте функцию [**аппендмену**](/windows/desktop/menurc/u) для добавления элементов в меню.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-120">Use the [**AppendMenu**](/windows/desktop/menurc/u) function to add items to the menu.</span></span> <span data-ttu-id="4ea0f-121">IDC \_ MENUCOMMAND1 и IDC \_ MENUCOMMAND2 — это определяемые приложением константы для команд меню.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-121">IDC\_MENUCOMMAND1 and IDC\_MENUCOMMAND2 are application-defined constants for menu commands.</span></span>


```C++
HMENU hSplitMenu = CreatePopupMenu();
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
```



### <a name="step-4-display-the-menu"></a><span data-ttu-id="4ea0f-122">Шаг 4. Отображение меню.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-122">Step 4: Display the menu.</span></span>

<span data-ttu-id="4ea0f-123">Функция [**метод TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) отображает контекстное меню в указанном расположении и отслеживает выбор элементов в меню.</span><span class="sxs-lookup"><span data-stu-id="4ea0f-123">The [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) function displays a shortcut menu at the specified location and tracks the selection of items on the menu.</span></span>


```C++
TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
```



## <a name="complete-example"></a><span data-ttu-id="4ea0f-124">Полный пример</span><span class="sxs-lookup"><span data-stu-id="4ea0f-124">Complete example</span></span>


```C++
case WM_NOTIFY:
    switch (((LPNMHDR)lParam)->code)
    {
        case BCN_DROPDOWN:
        {
            NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
            if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
            {

                // Get screen coordinates of the button.
                POINT pt;
                pt.x = pDropDown->rcButton.left;
                pt.y = pDropDown->rcButton.bottom;
                ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
        
                // Create a menu and add items.
                HMENU hSplitMenu = CreatePopupMenu();
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
        
                // Display the menu.
                TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
                return TRUE;
            }
            break;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="4ea0f-125">См. также</span><span class="sxs-lookup"><span data-stu-id="4ea0f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ea0f-126">\_Код уведомления для раскрывающегося списка BCN</span><span class="sxs-lookup"><span data-stu-id="4ea0f-126">BCN\_DROPDOWN Notification Code</span></span>](bcn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="4ea0f-127">О кнопках</span><span class="sxs-lookup"><span data-stu-id="4ea0f-127">About Buttons</span></span>](about-buttons.md)
</dt> <dt>

[<span data-ttu-id="4ea0f-128">Справочник по элементу управления Button</span><span class="sxs-lookup"><span data-stu-id="4ea0f-128">Button Control Reference</span></span>](bumper-button-button-control-reference.md)
</dt> <dt>

[<span data-ttu-id="4ea0f-129">Использование кнопок</span><span class="sxs-lookup"><span data-stu-id="4ea0f-129">Using Buttons</span></span>](using-buttons.md)
</dt> <dt>

[<span data-ttu-id="4ea0f-130">Кнопка</span><span class="sxs-lookup"><span data-stu-id="4ea0f-130">Button</span></span>](buttons.md)
</dt> </dl>

 

 