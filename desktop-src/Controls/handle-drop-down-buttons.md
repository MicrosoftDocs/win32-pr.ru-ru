---
title: Как управлять кнопками с раскрывающимся списком
description: Кнопка раскрывающегося списка может представлять пользователям список параметров.
ms.assetid: 2D908D4B-AA8B-4DEF-B656-C37B673ABB4D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d6f59bfa888d346e196e13ce030d1473a07f0f
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "103789354"
---
# <a name="how-to-handle-drop-down-buttons"></a><span data-ttu-id="f6eb1-103">Как управлять кнопками с раскрывающимся списком</span><span class="sxs-lookup"><span data-stu-id="f6eb1-103">How to Handle Drop-down Buttons</span></span>

<span data-ttu-id="f6eb1-104">Кнопка раскрывающегося списка может представлять пользователям список параметров.</span><span class="sxs-lookup"><span data-stu-id="f6eb1-104">A drop-down button can present users with a list of options.</span></span> <span data-ttu-id="f6eb1-105">Чтобы создать этот стиль кнопки, укажите стиль [**\_ раскрывающегося списка бтнс**](toolbar-control-and-button-styles.md) (также именуемый [**\_ раскрывающимся списком тбстиле**](toolbar-control-and-button-styles.md) для совместимости с предыдущими версиями стандартных элементов управления).</span><span class="sxs-lookup"><span data-stu-id="f6eb1-105">To create this style of button, specify the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style (also called [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md) for compatibility with previous versions of the common controls).</span></span> <span data-ttu-id="f6eb1-106">Чтобы отобразить кнопку с раскрывающимся списком, необходимо также задать стиль панели инструментов [**тбстиле \_ ex \_ дравддарровс**](toolbar-extended-styles.md) , отправив сообщение сетекстендедстиле в [**ТБ \_**](tb-setextendedstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="f6eb1-106">To show a drop-down button with an arrow, you must also set the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) toolbar style by sending a [**TB\_SETEXTENDEDSTYLE**](tb-setextendedstyle.md) message.</span></span>

<span data-ttu-id="f6eb1-107">На следующем рисунке показана раскрывающийся список "Открыть" с открытым контекстным меню и отображением списка файлов.</span><span class="sxs-lookup"><span data-stu-id="f6eb1-107">The following illustration shows a drop-down "Open" button with the context menu open and showing a list of files.</span></span> <span data-ttu-id="f6eb1-108">В этом примере панель инструментов имеет стиль [**тбстиле \_ ex \_ дравддарровс**](toolbar-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f6eb1-108">In this example, the toolbar has the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style.</span></span>

![снимок экрана: диалоговое окно с тремя элементами панели инструментов, представленными значками; у одной из них Развернутая стрелка раскрывающегося списка и контекстное меню из трех элементов](images/tb-dropdown.png)

<span data-ttu-id="f6eb1-110">На следующем рисунке показана та же панель инструментов, но без стиля [**тбстиле \_ ex \_ дравддарровс**](toolbar-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f6eb1-110">The following illustration shows the same toolbar, this time without the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style.</span></span>

![снимок экрана предыдущего диалогового окна, но значок с контекстным меню не содержит стрелку раскрывающегося списка](images/tb-dropdown2.png)

<span data-ttu-id="f6eb1-112">Когда пользователь наводит кнопку на панель инструментов, использующую стиль [**\_ раскрывающегося списка бтнс**](toolbar-control-and-button-styles.md) , элемент управления ToolBar отправляет родительскому окну код уведомления [ТБН \_ DROPDOWN](tbn-dropdown.md) .</span><span class="sxs-lookup"><span data-stu-id="f6eb1-112">When users click a toolbar button that uses the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style, the toolbar control sends its parent window a [TBN\_DROPDOWN](tbn-dropdown.md) notification code.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f6eb1-113">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="f6eb1-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f6eb1-114">Технологии</span><span class="sxs-lookup"><span data-stu-id="f6eb1-114">Technologies</span></span>

-   [<span data-ttu-id="f6eb1-115">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="f6eb1-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f6eb1-116">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="f6eb1-116">Prerequisites</span></span>

-   <span data-ttu-id="f6eb1-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="f6eb1-117">C/C++</span></span>
-   <span data-ttu-id="f6eb1-118">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="f6eb1-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f6eb1-119">Инструкции</span><span class="sxs-lookup"><span data-stu-id="f6eb1-119">Instructions</span></span>

### <a name="handle-a-drop-down-button"></a><span data-ttu-id="f6eb1-120">Обработайте кнопку раскрывающегося списка</span><span class="sxs-lookup"><span data-stu-id="f6eb1-120">Handle a Drop-down Button</span></span>

<span data-ttu-id="f6eb1-121">В следующем примере кода показано, как приложение может поддерживать кнопку раскрывающегося списка в элементе управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="f6eb1-121">The following code example demonstrates how an application can support a drop-down button in a toolbar control.</span></span>


```C++
BOOL DoNotify(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{

    #define lpnm   ((LPNMHDR)lParam)
    #define lpnmTB ((LPNMTOOLBAR)lParam)

    switch(lpnm->code)
    {
        case TBN_DROPDOWN:
        {
            // Get the coordinates of the button.
            RECT rc;
            SendMessage(lpnmTB->hdr.hwndFrom, TB_GETRECT, (WPARAM)lpnmTB->iItem, (LPARAM)&rc);

            // Convert to screen coordinates.            
            MapWindowPoints(lpnmTB->hdr.hwndFrom, HWND_DESKTOP, (LPPOINT)&rc, 2);                         
        
            // Get the menu.
            HMENU hMenuLoaded = LoadMenu(g_hinst, MAKEINTRESOURCE(IDR_POPUP)); 
         
            // Get the submenu for the first menu item.
            HMENU hPopupMenu = GetSubMenu(hMenuLoaded, 0);

            // Set up the pop-up menu.
            // In case the toolbar is too close to the bottom of the screen, 
            // set rcExclude equal to the button rectangle and the menu will appear above 
            // the button, and not below it.
         
            TPMPARAMS tpm;
         
            tpm.cbSize    = sizeof(TPMPARAMS);
            tpm.rcExclude = rc;
         
            // Show the menu and wait for input. 
            // If the user selects an item, its WM_COMMAND is sent.
         
            TrackPopupMenuEx(hPopupMenu, 
                             TPM_LEFTALIGN | TPM_LEFTBUTTON | TPM_VERTICAL, 
                             rc.left, rc.bottom, g_hwndMain, &tpm);

            DestroyMenu(hMenuLoaded);
         
        return (FALSE);
      
        }
    }
   
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="f6eb1-122">См. также</span><span class="sxs-lookup"><span data-stu-id="f6eb1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6eb1-123">Использование элементов управления ToolBar</span><span class="sxs-lookup"><span data-stu-id="f6eb1-123">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="f6eb1-124">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="f6eb1-124">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




