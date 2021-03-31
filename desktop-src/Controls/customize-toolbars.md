---
title: Настройка панелей инструментов
description: Большинство приложений на основе Windows используют элементы управления Toolbar для предоставления пользователям удобного доступа к функциональным возможностям программы.
ms.assetid: 0CE2988E-D887-433B-BFB2-5F3442E8E1B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091451a139cf846b1106916f28c165d6640699eb
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "104069720"
---
# <a name="how-to-customize-toolbars"></a><span data-ttu-id="1b588-103">Настройка панелей инструментов</span><span class="sxs-lookup"><span data-stu-id="1b588-103">How to Customize Toolbars</span></span>

<span data-ttu-id="1b588-104">Большинство приложений на основе Windows используют элементы управления Toolbar для предоставления пользователям удобного доступа к функциональным возможностям программы.</span><span class="sxs-lookup"><span data-stu-id="1b588-104">Most Windows-based applications use toolbar controls to provide users with convenient access to the program functionality.</span></span> <span data-ttu-id="1b588-105">Однако у статических панелей инструментов есть некоторые недостатки, например слишком мало места для эффективного вывода всех доступных инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-105">However, static toolbars have some shortcomings—such as too little space to effectively display all the available tools.</span></span> <span data-ttu-id="1b588-106">Решение этой проблемы заключается в том, чтобы сделать пользовательские панели инструментов приложения настраиваемыми.</span><span class="sxs-lookup"><span data-stu-id="1b588-106">The solution to this problem is to make your application's toolbars user-customizable.</span></span> <span data-ttu-id="1b588-107">Затем пользователи могут отображать только необходимые вам средства, и они могут упорядочивать их в соответствии с личными образа жизниами.</span><span class="sxs-lookup"><span data-stu-id="1b588-107">Then, users can choose to display only the tools they need, and they can organize them in a way that suits their personal workstyle.</span></span>

> [!Note]  
> <span data-ttu-id="1b588-108">Панели инструментов в диалоговых окнах не могут быть настроены.</span><span class="sxs-lookup"><span data-stu-id="1b588-108">Toolbars in dialog boxes cannot be customized.</span></span>

 

<span data-ttu-id="1b588-109">Чтобы включить настройку, включите флаг стиля [**CCS \_ регулируемых**](common-control-styles.md) стандартных элементов управления при создании элемента управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="1b588-109">To enable customization, include the [**CCS\_ADJUSTABLE**](common-control-styles.md) common controls style flag when you create the toolbar control.</span></span> <span data-ttu-id="1b588-110">Существует два основных подхода к настройке.</span><span class="sxs-lookup"><span data-stu-id="1b588-110">There are two basic approaches to customization:</span></span>

-   <span data-ttu-id="1b588-111">Диалоговое окно "Настройка".</span><span class="sxs-lookup"><span data-stu-id="1b588-111">The customization dialog box.</span></span> <span data-ttu-id="1b588-112">Данное системное диалоговое окно является самым простым способом.</span><span class="sxs-lookup"><span data-stu-id="1b588-112">This system-provided dialog box is the simplest approach.</span></span> <span data-ttu-id="1b588-113">Он предоставляет пользователям графический пользовательский интерфейс, позволяющий добавлять, удалять и перемещать значки.</span><span class="sxs-lookup"><span data-stu-id="1b588-113">It gives users a graphical user interface that allows them to add, delete, or move icons.</span></span>
-   <span data-ttu-id="1b588-114">Перетаскивание инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-114">Dragging and dropping tools.</span></span> <span data-ttu-id="1b588-115">Реализация функции перетаскивания позволяет пользователям перемещать средства в другое место на панели инструментов или удалять их, перетаскивая их за пределы панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-115">Implementing drag-and-drop functionality allows users to move tools to another location on the toolbar or delete them by dragging them off the toolbar.</span></span> <span data-ttu-id="1b588-116">Она предоставляет пользователям быстрый и простой способ организации панели инструментов, но не позволяет им добавлять средства.</span><span class="sxs-lookup"><span data-stu-id="1b588-116">It provides users a quick and easy way to organize their toolbar, but does not allow them to add tools.</span></span>

<span data-ttu-id="1b588-117">В зависимости от потребностей приложения можно реализовать любой из этих подходов или оба.</span><span class="sxs-lookup"><span data-stu-id="1b588-117">You can implement either approach or both, depending on the needs of the application.</span></span> <span data-ttu-id="1b588-118">Ни один из этих двух подходов к настройке не предоставляет встроенного механизма, такого как кнопка отмены или отмены, для возвращения панели инструментов в прежнее состояние.</span><span class="sxs-lookup"><span data-stu-id="1b588-118">Neither of these two approaches to customization provides a built-in mechanism, such as a Cancel or Undo button, to return the toolbar to its former state.</span></span> <span data-ttu-id="1b588-119">Необходимо явно использовать API элемента управления Toolbar для хранения состояния преднастройки панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-119">You must explicitly use the toolbar control API to store the toolbar's precustomization state.</span></span> <span data-ttu-id="1b588-120">При необходимости можно использовать эти сохраненные сведения для восстановления исходного состояния панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-120">If necessary, you can later use this stored information to restore the toolbar to its original state.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="1b588-121">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="1b588-121">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1b588-122">Технологии</span><span class="sxs-lookup"><span data-stu-id="1b588-122">Technologies</span></span>

-   [<span data-ttu-id="1b588-123">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="1b588-123">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="1b588-124">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="1b588-124">Prerequisites</span></span>

-   <span data-ttu-id="1b588-125">C/C++</span><span class="sxs-lookup"><span data-stu-id="1b588-125">C/C++</span></span>
-   <span data-ttu-id="1b588-126">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="1b588-126">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="1b588-127">Инструкции</span><span class="sxs-lookup"><span data-stu-id="1b588-127">Instructions</span></span>

### <a name="customization-dialog-box"></a><span data-ttu-id="1b588-128">Диалоговое окно «Настройка»</span><span class="sxs-lookup"><span data-stu-id="1b588-128">Customization Dialog Box</span></span>

<span data-ttu-id="1b588-129">Диалоговое окно Настройка предоставляется элементом управления Toolbar для предоставления пользователям простого способа добавления, перемещения или удаления инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-129">The customization dialog box is provided by the toolbar control to give users a simple way to add, move, or delete tools.</span></span> <span data-ttu-id="1b588-130">Пользователи могут запустить его, дважды щелкнув панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-130">Users can launch it by double-clicking the toolbar.</span></span> <span data-ttu-id="1b588-131">Приложения могут запускать диалоговое окно настройки программным путем, отправляя элемент управления панели инструментов в [**ТБ \_ настраиваемого**](tb-customize.md) сообщения.</span><span class="sxs-lookup"><span data-stu-id="1b588-131">Applications can launch the customization dialog box programmatically by sending the toolbar control a [**TB\_CUSTOMIZE**](tb-customize.md) message.</span></span>

<span data-ttu-id="1b588-132">На следующем рисунке показан пример диалогового окна Настройка панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-132">The following illustration shows an example of the toolbar customization dialog box.</span></span>

![снимок экрана окна с панелью инструментов из трех элементов и диалоговым окном со списками доступных и текущих кнопок панели инструментов](images/tb-customdlg.png)

<span data-ttu-id="1b588-134">В списке справа находятся инструменты, находящиеся на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-134">The tools in the list box on the right are those currently on the toolbar.</span></span> <span data-ttu-id="1b588-135">Изначально в этом списке будут содержаться средства, которые вы указали при создании панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-135">Initially, this list will contain the tools that you specify when you create the toolbar.</span></span> <span data-ttu-id="1b588-136">В списке слева содержатся средства, доступные для добавления на панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-136">The list box in the left contains the tools that are available to add to the toolbar.</span></span> <span data-ttu-id="1b588-137">Приложение несет ответственность за заполнение этого списка (за исключением разделителя, который отображается автоматически).</span><span class="sxs-lookup"><span data-stu-id="1b588-137">Your application is responsible for populating that list (other than with the Separator, which appears automatically).</span></span>

<span data-ttu-id="1b588-138">Элемент управления "панель инструментов" уведомляет ваше приложение, что оно запускает диалоговое окно настройки, отправив его родительское окно код уведомления [ТБН \_ бегинаджуст](tbn-beginadjust.md) , за которым следует код уведомления [ТБН \_ иниткустомизе](tbn-initcustomize.md) .</span><span class="sxs-lookup"><span data-stu-id="1b588-138">The toolbar control notifies your application that it is launching a customization dialog box by sending its parent window a [TBN\_BEGINADJUST](tbn-beginadjust.md) notification code followed by a [TBN\_INITCUSTOMIZE](tbn-initcustomize.md) notification code.</span></span> <span data-ttu-id="1b588-139">В большинстве случаев приложению не нужно отвечать на эти коды уведомлений.</span><span class="sxs-lookup"><span data-stu-id="1b588-139">In most cases, the application does not need to respond to these notification codes.</span></span> <span data-ttu-id="1b588-140">Однако, если не нужно, чтобы диалоговое окно Настройка панели инструментов отображало кнопку справки, обработайте ТБН \_ иниткустомизе, возвращая тбнрф \_ хидехелп.</span><span class="sxs-lookup"><span data-stu-id="1b588-140">However, if you do not want the Customize Toolbar dialog box to display a Help button, handle TBN\_INITCUSTOMIZE by returning TBNRF\_HIDEHELP.</span></span>

<span data-ttu-id="1b588-141">Затем элемент управления ToolBar собирает сведения, необходимые для инициализации диалогового окна, отправляя три последовательности кодов уведомления в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="1b588-141">The toolbar control then collects the information it needs to initialize the dialog box by sending three series of notification codes, in the following order:</span></span>

-   <span data-ttu-id="1b588-142">Код уведомления [ТБН \_ куеринсерт](tbn-queryinsert.md) для каждой кнопки на панели инструментов, чтобы определить, где можно вставить кнопки.</span><span class="sxs-lookup"><span data-stu-id="1b588-142">A [TBN\_QUERYINSERT](tbn-queryinsert.md) notification code for each button on the toolbar to determine where buttons can be inserted.</span></span> <span data-ttu-id="1b588-143">Возвращает **значение false** , чтобы запретить вставку кнопки слева от кнопки, указанной в сообщении уведомления.</span><span class="sxs-lookup"><span data-stu-id="1b588-143">Return **FALSE** to prevent a button from being inserted to the left of the button specified in the notification message.</span></span> <span data-ttu-id="1b588-144">Если вы возвращаете **значение false** для всех \_ кодов уведомлений ТБН куеринсерт, диалоговое окно не будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="1b588-144">If you return **FALSE** to all TBN\_QUERYINSERT notification codes, the dialog box will not be displayed.</span></span>
-   <span data-ttu-id="1b588-145">Код уведомления [ТБН \_ куериделете](tbn-querydelete.md) для каждого инструмента, который в данный момент находится на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-145">A [TBN\_QUERYDELETE](tbn-querydelete.md) notification code for each tool that is currently on the toolbar.</span></span> <span data-ttu-id="1b588-146">Возвращает **значение true** , если средство можно удалить, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1b588-146">Return **TRUE** if a tool can be deleted, or **FALSE** if not.</span></span>
-   <span data-ttu-id="1b588-147">Ряд кодов уведомлений [ТБН \_ жетбуттонинфо](tbn-getbuttoninfo.md) для заполнения списка доступных кнопок.</span><span class="sxs-lookup"><span data-stu-id="1b588-147">A series of [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) notification codes to populate the list of available buttons.</span></span> <span data-ttu-id="1b588-148">Чтобы добавить кнопку в список, заполните структуру [**нмтулбар**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) , которая передается вместе с кодом уведомления, и возвратит **значение true**.</span><span class="sxs-lookup"><span data-stu-id="1b588-148">To add a button to the list, fill in the [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that is passed with the notification code and return **TRUE**.</span></span> <span data-ttu-id="1b588-149">Если больше нет средств для добавления, возвратите **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1b588-149">When you have no more tools to add, return **FALSE**.</span></span> <span data-ttu-id="1b588-150">Обратите внимание, что можно получить сведения о кнопках, которые уже находятся на панели инструментов. Эти кнопки не будут добавлены в список.</span><span class="sxs-lookup"><span data-stu-id="1b588-150">Note that you can return information for buttons that are already on the toolbar; these buttons will not be added to the list.</span></span>

<span data-ttu-id="1b588-151">Затем отображается диалоговое окно, и пользователь может начать настройку панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-151">The dialog box is then displayed, and the user can begin to customize the toolbar.</span></span>

<span data-ttu-id="1b588-152">Когда диалоговое окно открыто, приложение может получить различные коды уведомлений в зависимости от действий пользователя:</span><span class="sxs-lookup"><span data-stu-id="1b588-152">When the dialog box is open, your application can receive a variety of notification codes, depending on the user's actions:</span></span>

-   <span data-ttu-id="1b588-153">[ТБН \_ КУЕРИНСЕРТ](tbn-queryinsert.md).</span><span class="sxs-lookup"><span data-stu-id="1b588-153">[TBN\_QUERYINSERT](tbn-queryinsert.md).</span></span> <span data-ttu-id="1b588-154">Пользователь изменил расположение инструмента на панели инструментов или добавил средство.</span><span class="sxs-lookup"><span data-stu-id="1b588-154">The user has changed the location of a tool on the toolbar or added a tool.</span></span> <span data-ttu-id="1b588-155">Возвращает **значение false** , чтобы предотвратить вставку средства в это место.</span><span class="sxs-lookup"><span data-stu-id="1b588-155">Return **FALSE** to prevent the tool from being inserted at that location.</span></span>
-   <span data-ttu-id="1b588-156">[ТБН \_ ДЕЛЕТИНГБУТТОН](tbn-deletingbutton.md).</span><span class="sxs-lookup"><span data-stu-id="1b588-156">[TBN\_DELETINGBUTTON](tbn-deletingbutton.md).</span></span> <span data-ttu-id="1b588-157">Пользователь собирается удалить средство с панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-157">The user is about to remove a tool from the toolbar.</span></span>
-   <span data-ttu-id="1b588-158">[ТБН \_ КУССЕЛП](tbn-custhelp.md).</span><span class="sxs-lookup"><span data-stu-id="1b588-158">[TBN\_CUSTHELP](tbn-custhelp.md).</span></span> <span data-ttu-id="1b588-159">Пользователь щелкнул кнопку Справка.</span><span class="sxs-lookup"><span data-stu-id="1b588-159">The user has clicked the Help button.</span></span>
-   <span data-ttu-id="1b588-160">[ТБН \_ ТУЛБАРЧАНЖЕ](tbn-toolbarchange.md).</span><span class="sxs-lookup"><span data-stu-id="1b588-160">[TBN\_TOOLBARCHANGE](tbn-toolbarchange.md).</span></span> <span data-ttu-id="1b588-161">Пользователь добавил, переместил или удалил инструмент.</span><span class="sxs-lookup"><span data-stu-id="1b588-161">The user has added, moved, or deleted a tool.</span></span>
-   <span data-ttu-id="1b588-162">[ТБН \_ Сброс](tbn-reset.md).</span><span class="sxs-lookup"><span data-stu-id="1b588-162">[TBN\_RESET](tbn-reset.md).</span></span> <span data-ttu-id="1b588-163">Пользователь щелкнул кнопку Reset (Сброс).</span><span class="sxs-lookup"><span data-stu-id="1b588-163">The user has clicked the Reset button.</span></span>

<span data-ttu-id="1b588-164">После уничтожения диалогового окна приложение получит код уведомления [ТБН \_ ендаджуст](tbn-endadjust.md) .</span><span class="sxs-lookup"><span data-stu-id="1b588-164">After the dialog box is destroyed, your application will receive a [TBN\_ENDADJUST](tbn-endadjust.md) notification code.</span></span>

<span data-ttu-id="1b588-165">В следующем примере кода показан один из способов реализации настройки панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-165">The following code example shows one way to implement toolbar customization.</span></span>


```C++
// The buttons are stored in an array of TBBUTTON structures. 
//
// Constants such as STD_FILENEW are identifiers for the 
// built-in bitmaps that have already been assigned as the toolbar's 
// image list.
//
// Constants such as IDM_NEW are application-defined command identifiers.

TBBUTTON allButtons[] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"New" },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Open"},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Save"},
        { MAKELONG(STD_CUT,      ImageListID), IDM_CUT,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Cut" },
        { MAKELONG(STD_COPY,     ImageListID), IDM_COPY,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Copy"},
        { MAKELONG(STD_PASTE,    ImageListID), IDM_PASTE, TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Paste"}
    };

// The following appears in the window's message handler.

case WM_NOTIFY: 
    {
        switch (((LPNMHDR)lParam)->code) 
        {
        
        case TBN_GETBUTTONINFO:  
            {
                LPTBNOTIFY lpTbNotify = (LPTBNOTIFY)lParam;

                // Pass the next button from the array. There is no need to filter out buttons
                // that are already used—they will be ignored.
                
                int buttonCount = sizeof(allButtons) / sizeof(TBBUTTON);
                
                if (lpTbNotify->iItem < buttonCount)
                {
                    lpTbNotify->tbButton = allButtons[lpTbNotify->iItem];
                    return TRUE;
                }
                
                else
                
                {
                    return FALSE;  // No more buttons.
                }
            }
            
            break;

            case TBN_QUERYINSERT:
            
            case TBN_QUERYDELETE:
                return TRUE; 
        }
    }
```



### <a name="dragging-and-dropping-tools"></a><span data-ttu-id="1b588-166">Перетаскивание инструментов</span><span class="sxs-lookup"><span data-stu-id="1b588-166">Dragging and Dropping Tools</span></span>

<span data-ttu-id="1b588-167">Пользователи также могут изменить порядок кнопок на панели инструментов, нажав клавишу SHIFT и перетащив кнопку в другое место.</span><span class="sxs-lookup"><span data-stu-id="1b588-167">Users can also rearrange the buttons on a toolbar by pressing the SHIFT key and dragging the button to another location.</span></span> <span data-ttu-id="1b588-168">Процесс перетаскивания автоматически обрабатывается элементом управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="1b588-168">The drag-and-drop process is handled automatically by the toolbar control.</span></span> <span data-ttu-id="1b588-169">Он отображает несинхронизированное изображение кнопки при перетаскивании и перемещает панель инструментов после ее удаления.</span><span class="sxs-lookup"><span data-stu-id="1b588-169">It displays a ghost image of the button as it is dragged, and rearranges the toolbar after it is dropped.</span></span> <span data-ttu-id="1b588-170">Пользователи не могут добавлять кнопки таким образом, но могут удалить кнопку, удалив ее с панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-170">Users cannot add buttons in this way, but they can delete a button by dropping it off the toolbar.</span></span>

<span data-ttu-id="1b588-171">Хотя элемент управления панели инструментов обычно выполняет эту операцию автоматически, он также отправляет два кода уведомления: [ТБН \_ Куериделете](tbn-querydelete.md) и [ТБН \_ куеринсерт](tbn-queryinsert.md).</span><span class="sxs-lookup"><span data-stu-id="1b588-171">Although the toolbar control normally does this operation automatically, it also sends your application two notification codes: [TBN\_QUERYDELETE](tbn-querydelete.md) and [TBN\_QUERYINSERT](tbn-queryinsert.md).</span></span> <span data-ttu-id="1b588-172">Чтобы управлять процессом перетаскивания, обрабатывайте эти коды уведомлений следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1b588-172">To control the drag-and-drop process, handle these notification codes as follows:</span></span>

-   <span data-ttu-id="1b588-173">Код уведомления [ТБН \_ куериделете](tbn-querydelete.md) отправляется сразу после того, как пользователь попытается переместить кнопку, перед отображением кнопки фантомной копии.</span><span class="sxs-lookup"><span data-stu-id="1b588-173">The [TBN\_QUERYDELETE](tbn-querydelete.md) notification code is sent as soon as the user attempts to move the button, before the ghost button is displayed.</span></span> <span data-ttu-id="1b588-174">Возвращает **значение false** , чтобы предотвратить перемещение кнопки.</span><span class="sxs-lookup"><span data-stu-id="1b588-174">Return **FALSE** to prevent the button from being moved.</span></span> <span data-ttu-id="1b588-175">Если вы возвращаете **значение true**, пользователь сможет либо переместить средство, либо удалить его, удалив его с панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-175">If you return **TRUE**, the user will be able to either move the tool or delete it by dropping it off the toolbar.</span></span> <span data-ttu-id="1b588-176">Если средство можно переместить, его можно удалить.</span><span class="sxs-lookup"><span data-stu-id="1b588-176">If a tool can be moved, it can be deleted.</span></span> <span data-ttu-id="1b588-177">Тем не менее, если пользователь удаляет средство, элемент управления ToolBar отправляет приложению код уведомления [ТБН \_ делетингбуттон](tbn-deletingbutton.md) , после чего вы можете выбрать повторную вставку кнопки в ее исходном расположении, тем самым отменяя удаление.</span><span class="sxs-lookup"><span data-stu-id="1b588-177">However, if the user deletes a tool, the toolbar control will send your application a [TBN\_DELETINGBUTTON](tbn-deletingbutton.md) notification code, at which point you can choose to reinsert the button at its original location, thereby canceling the deletion.</span></span>
-   <span data-ttu-id="1b588-178">Код уведомления [ТБН \_ куеринсерт](tbn-queryinsert.md) отправляется, когда пользователь пытается удалить кнопку на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-178">The [TBN\_QUERYINSERT](tbn-queryinsert.md) notification code is sent when the user attempts to drop the button on the toolbar.</span></span> <span data-ttu-id="1b588-179">Чтобы предотвратить удаление перемещаемой кнопки слева от кнопки, указанной в уведомлении, возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1b588-179">To prevent the button that is being moved from being dropped to the left of the button specified in the notification, return **FALSE**.</span></span> <span data-ttu-id="1b588-180">Этот код уведомления не отправляется, если пользователь удаляет средство с панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-180">This notification code is not sent if the user drops the tool off the toolbar.</span></span>

<span data-ttu-id="1b588-181">Если пользователь пытается перетащить кнопку, не нажимая клавишу SHIFT, элемент управления ToolBar не будет управлять операцией перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="1b588-181">If the user attempts to drag a button without also pressing the SHIFT key, the toolbar control will not handle the drag-and-drop operation.</span></span> <span data-ttu-id="1b588-182">Однако он отправит приложению код уведомления [ТБН \_ бегиндраг](tbn-begindrag.md) , чтобы указать начало операции перетаскивания, и код уведомления [ТБН \_ енддраг](tbn-enddrag.md) для указания конца.</span><span class="sxs-lookup"><span data-stu-id="1b588-182">However, it will send your application a [TBN\_BEGINDRAG](tbn-begindrag.md) notification code to indicate the start of a drag operation, and a [TBN\_ENDDRAG](tbn-enddrag.md) notification code to indicate the end.</span></span> <span data-ttu-id="1b588-183">Если вы хотите включить эту форму перетаскивания, приложение должно поддерживать эти коды уведомлений, предоставлять необходимый пользовательский интерфейс и изменять панель инструментов в соответствии с любыми изменениями.</span><span class="sxs-lookup"><span data-stu-id="1b588-183">If you want to enable this form of drag-and-drop, your application must handle these notification codes, provide the necessary user interface, and modify the toolbar to reflect any changes.</span></span>

### <a name="saving-and-restoring-toolbars"></a><span data-ttu-id="1b588-184">Сохранение и восстановление панелей инструментов</span><span class="sxs-lookup"><span data-stu-id="1b588-184">Saving and Restoring Toolbars</span></span>

<span data-ttu-id="1b588-185">В процессе настройки панели инструментов приложению может потребоваться сохранить информацию, чтобы можно было восстановить ее исходное состояние.</span><span class="sxs-lookup"><span data-stu-id="1b588-185">In the process of customizing a toolbar, your application might need to save information so that you can restore the toolbar to its original state.</span></span> <span data-ttu-id="1b588-186">Чтобы начать сохранение или восстановление состояния панели инструментов, отправляйте панель инструментов с сообщением [**\_ савересторе ТБ**](tb-saverestore.md) с параметром *lParam* , имеющим значение **true**.</span><span class="sxs-lookup"><span data-stu-id="1b588-186">To initiate saving or restoring a toolbar state, send the toolbar control a [**TB\_SAVERESTORE**](tb-saverestore.md) message with the *lParam* set to **TRUE**.</span></span> <span data-ttu-id="1b588-187">Значение *lParam* этого сообщения указывает, запрашивается ли операция сохранения или восстановления.</span><span class="sxs-lookup"><span data-stu-id="1b588-187">The *lParam* value of this message specifies whether you are requesting a save or a restore operation.</span></span> <span data-ttu-id="1b588-188">После отправки сообщения существует два способа работы с операцией сохранения и восстановления:</span><span class="sxs-lookup"><span data-stu-id="1b588-188">After the message is sent, there are two ways to handle the save/restore operation:</span></span>

-   <span data-ttu-id="1b588-189">С помощью стандартных элементов управления [версии 4,72](common-control-versions.md) и более ранних версий необходимо реализовать обработчик [ \_ жетбуттонинфо ТБН](tbn-getbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="1b588-189">With common controls [version 4.72](common-control-versions.md) and earlier, you must implement a [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) handler.</span></span> <span data-ttu-id="1b588-190">Элемент управления ToolBar отправляет этот код уведомления для запроса сведений о каждой кнопке при ее восстановлении.</span><span class="sxs-lookup"><span data-stu-id="1b588-190">The toolbar control sends this notification code to request information about each button as it is restored.</span></span>
-   <span data-ttu-id="1b588-191">Версия 5,80 включает параметр «сохранить/восстановить».</span><span class="sxs-lookup"><span data-stu-id="1b588-191">Version 5.80 includes a save/restore option.</span></span> <span data-ttu-id="1b588-192">В начале процесса и при сохранении или восстановлении каждой кнопки приложение получит код уведомления [ТБН \_ Save](tbn-save.md) или [ТБН \_ RESTORE](tbn-restore.md) .</span><span class="sxs-lookup"><span data-stu-id="1b588-192">At the beginning of the process, and as each button is saved or restored, your application will receive a [TBN\_SAVE](tbn-save.md) or [TBN\_RESTORE](tbn-restore.md) notification code.</span></span> <span data-ttu-id="1b588-193">Чтобы использовать этот параметр, необходимо реализовать обработчики уведомлений, чтобы предоставить сведения о битовой карте и состоянии, необходимые для успешного сохранения или восстановления состояния панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-193">To use this option, you must implement notification handlers to provide the bitmap and state information that is needed to successfully save or restore the toolbar state.</span></span>

<span data-ttu-id="1b588-194">Состояния панелей инструментов сохраняются в потоке данных, который состоит из блоков данных, определяемых оболочкой, которые изменяются блоками данных, определяемых приложением.</span><span class="sxs-lookup"><span data-stu-id="1b588-194">Toolbar states are saved in a data stream that consists of blocks of Shell-defined data alternating with blocks of application-defined data.</span></span> <span data-ttu-id="1b588-195">Для каждой кнопки хранится один блок данных каждого типа, а также необязательный блок глобальных данных, которые приложения могут размещать в начале потока.</span><span class="sxs-lookup"><span data-stu-id="1b588-195">One data block of each type is stored for each button, along with an optional block of global data that applications can place at the beginning of the stream.</span></span> <span data-ttu-id="1b588-196">Во время процесса сохранения обработчик [ \_ сохранения ТБН](tbn-save.md) добавляет определенные приложением блоки в поток данных.</span><span class="sxs-lookup"><span data-stu-id="1b588-196">During the save process, your [TBN\_SAVE](tbn-save.md) handler adds the application-defined blocks to the data stream.</span></span> <span data-ttu-id="1b588-197">Во время процесса восстановления обработчик [ \_ восстановления ТБН](tbn-restore.md) считывает каждый блок и предоставляет оболочке сведения, необходимые для восстановления панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-197">During the restore process, the [TBN\_RESTORE](tbn-restore.md) handler reads each block and gives the Shell the information it needs to reconstruct the toolbar.</span></span>

### <a name="how-to-handle-a-tbn_save-notification"></a><span data-ttu-id="1b588-198">Как выполнить обработку \_ уведомления о СОХРАНЕНИИ ТБН</span><span class="sxs-lookup"><span data-stu-id="1b588-198">How to Handle a TBN\_SAVE Notification</span></span>

<span data-ttu-id="1b588-199">Первый [тбнный \_ ](tbn-save.md) код уведомления о сохранении отправляется в начале процесса сохранения.</span><span class="sxs-lookup"><span data-stu-id="1b588-199">The first [TBN\_SAVE](tbn-save.md) notification code is sent at the beginning of the save process.</span></span> <span data-ttu-id="1b588-200">Перед сохранением каких бы то ни было кнопок, элементы структуры [**нмтбсаве**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) задаются, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1b588-200">Before any buttons are saved, the members of the [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) structure are set as shown in the following table.</span></span>



| <span data-ttu-id="1b588-201">Член</span><span class="sxs-lookup"><span data-stu-id="1b588-201">Member</span></span>       | <span data-ttu-id="1b588-202">Параметр</span><span class="sxs-lookup"><span data-stu-id="1b588-202">Setting</span></span>                                                                                                                                                                                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b588-203">**iItem**</span><span class="sxs-lookup"><span data-stu-id="1b588-203">**iItem**</span></span>    | <span data-ttu-id="1b588-204">–1</span><span class="sxs-lookup"><span data-stu-id="1b588-204">–1</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="1b588-205">**cbData**</span><span class="sxs-lookup"><span data-stu-id="1b588-205">**cbData**</span></span>   | <span data-ttu-id="1b588-206">Объем памяти, необходимый для данных, определяемых оболочкой.</span><span class="sxs-lookup"><span data-stu-id="1b588-206">The amount of memory needed for Shell-defined data.</span></span>                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="1b588-207">**кбуттонс**</span><span class="sxs-lookup"><span data-stu-id="1b588-207">**cButtons**</span></span> | <span data-ttu-id="1b588-208">Число кнопок.</span><span class="sxs-lookup"><span data-stu-id="1b588-208">The number of buttons.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="1b588-209">**pData**</span><span class="sxs-lookup"><span data-stu-id="1b588-209">**pData**</span></span>    | <span data-ttu-id="1b588-210">Вычисленный объем памяти, необходимый для определяемых приложением данных.</span><span class="sxs-lookup"><span data-stu-id="1b588-210">The calculated amount of memory needed for application-defined data.</span></span> <span data-ttu-id="1b588-211">Обычно включаются некоторые глобальные данные, а также данные для каждой кнопки.</span><span class="sxs-lookup"><span data-stu-id="1b588-211">Typically, you include some global data, plus data for each button.</span></span> <span data-ttu-id="1b588-212">Добавьте это значение в **cbData** и выделите достаточно памяти для **pData** , чтобы вместить все данные.</span><span class="sxs-lookup"><span data-stu-id="1b588-212">Add that value to **cbData** and allocate enough memory to **pData** to hold it all.</span></span>                                                                                                                      |
| <span data-ttu-id="1b588-213">**пкуррент**</span><span class="sxs-lookup"><span data-stu-id="1b588-213">**pCurrent**</span></span> | <span data-ttu-id="1b588-214">Первый неиспользуемый байт в потоке данных.</span><span class="sxs-lookup"><span data-stu-id="1b588-214">The first unused byte in the data stream.</span></span> <span data-ttu-id="1b588-215">Если не требуются глобальные сведения о панели инструментов, установите **пкуррент**  =  **pData** так, чтобы он указывал на начало потока данных.</span><span class="sxs-lookup"><span data-stu-id="1b588-215">If you do not require global toolbar information, set **pCurrent** = **pData** so that it points to the start of the data stream.</span></span> <span data-ttu-id="1b588-216">Если вам требуются глобальные сведения о панели инструментов, сохраните их в **pData**, а затем установите **пкуррент** в начале неиспользуемой части потока данных перед возвратом.</span><span class="sxs-lookup"><span data-stu-id="1b588-216">If you do require global toolbar information, store it at **pData**, then set **pCurrent** to the beginning of the unused portion of the data stream before returning.</span></span> |



 

<span data-ttu-id="1b588-217">Если необходимо добавить некоторые глобальные сведения о панели инструментов, поставьте ее в начало потока данных.</span><span class="sxs-lookup"><span data-stu-id="1b588-217">If you want to add some global toolbar information, put it at the start of the data stream.</span></span> <span data-ttu-id="1b588-218">**Пкуррент** до конца глобальных данных, чтобы они указывали на начало неиспользуемой части потока данных и возвращали.</span><span class="sxs-lookup"><span data-stu-id="1b588-218">Advance **pCurrent** to the end of the global data so that it points to the beginning of the unused portion of the data stream, and return.</span></span>

<span data-ttu-id="1b588-219">После возврата оболочка запускает сохранение сведений о кнопке.</span><span class="sxs-lookup"><span data-stu-id="1b588-219">After you return, the Shell starts saving button information.</span></span> <span data-ttu-id="1b588-220">Он добавляет определяемые оболочкой данные для первой кнопки по адресу **пкуррент** , а затем перемещает **пкуррент** в начало неиспользуемой части.</span><span class="sxs-lookup"><span data-stu-id="1b588-220">It adds the Shell-defined data for the first button at **pCurrent** and then advances **pCurrent** to the start of the unused portion.</span></span>

<span data-ttu-id="1b588-221">После сохранения каждой кнопки отправляется код уведомления [ТБН \_ Save](tbn-save.md) , а [**нмтбсаве**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) возвращается с этими членами следующим образом.</span><span class="sxs-lookup"><span data-stu-id="1b588-221">After each button is saved, a [TBN\_SAVE](tbn-save.md) notification code is sent and [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) is returned with these members set as follows.</span></span>



| <span data-ttu-id="1b588-222">Член</span><span class="sxs-lookup"><span data-stu-id="1b588-222">Member</span></span>                       | <span data-ttu-id="1b588-223">Параметр</span><span class="sxs-lookup"><span data-stu-id="1b588-223">Setting</span></span>                                                                                                                                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b588-224">**iItem**</span><span class="sxs-lookup"><span data-stu-id="1b588-224">**iItem**</span></span>                    | <span data-ttu-id="1b588-225">Отсчитываемый от нуля индекс номера кнопки.</span><span class="sxs-lookup"><span data-stu-id="1b588-225">The zero-based index of the button number.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="1b588-226">**пкуррент**</span><span class="sxs-lookup"><span data-stu-id="1b588-226">**pCurrent**</span></span>                 | <span data-ttu-id="1b588-227">Указатель на первый неиспользуемый байт в потоке данных.</span><span class="sxs-lookup"><span data-stu-id="1b588-227">A pointer to the first unused byte in the data stream.</span></span> <span data-ttu-id="1b588-228">Если вы хотите сохранить дополнительные сведения о кнопке, сохраните ее в расположении, на которое указывает **пкуррент** , и обновите **пкуррент** , чтобы указать на первую неиспользуемую часть потока данных после этого.</span><span class="sxs-lookup"><span data-stu-id="1b588-228">If you want to store additional information about the button, store it at the location pointed to by **pCurrent** and update **pCurrent** to point to the first unused portion of the data stream after that.</span></span> |
| [<span data-ttu-id="1b588-229">**тббуттон**</span><span class="sxs-lookup"><span data-stu-id="1b588-229">**TBBUTTON**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) | <span data-ttu-id="1b588-230">Структура [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) , описывающая сохраняемую кнопку.</span><span class="sxs-lookup"><span data-stu-id="1b588-230">A [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure that describes the button that is being saved.</span></span>                                                                                                                                                                              |



 

<span data-ttu-id="1b588-231">При получении кода уведомления необходимо извлечь все сведения, необходимые для каждой кнопки, из [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton).</span><span class="sxs-lookup"><span data-stu-id="1b588-231">When you receive the notification code, you should extract any button-specific information you need from [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton).</span></span> <span data-ttu-id="1b588-232">Помните, что при добавлении кнопки можно использовать элемент **двдата** из **тббуттон** для хранения данных, зависящих от приложения.</span><span class="sxs-lookup"><span data-stu-id="1b588-232">Remember that when you add a button, you can use the **dwData** member of **TBBUTTON** to hold application-specific data.</span></span> <span data-ttu-id="1b588-233">Загрузите данные в поток данных по адресу **пкуррент**.</span><span class="sxs-lookup"><span data-stu-id="1b588-233">Load your data into the data stream at **pCurrent**.</span></span> <span data-ttu-id="1b588-234">Передайте **пкуррент** к концу данных, снова наведите указатель на начало неиспользуемой части потока и возвратите.</span><span class="sxs-lookup"><span data-stu-id="1b588-234">Advance **pCurrent** to the end of your data, again pointing to the beginning of the unused portion of the stream, and return.</span></span>

<span data-ttu-id="1b588-235">Затем оболочка переходит к следующей кнопке, добавляет ее сведения в **pData**, увеличивает **пкуррент**, загружает [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)и отправляет еще один код уведомления о [ \_ тбне](tbn-save.md) .</span><span class="sxs-lookup"><span data-stu-id="1b588-235">The Shell then goes to the next button, adds its information to **pData**, advances **pCurrent**, loads [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton), and sends another [TBN\_SAVE](tbn-save.md) notification code.</span></span> <span data-ttu-id="1b588-236">Этот процесс будет продолжен до тех пор, пока не будут сохранены все кнопки.</span><span class="sxs-lookup"><span data-stu-id="1b588-236">This process continues until all buttons are saved.</span></span>

### <a name="restoring-saved-toolbars"></a><span data-ttu-id="1b588-237">Восстановление сохраненных панелей инструментов</span><span class="sxs-lookup"><span data-stu-id="1b588-237">Restoring Saved Toolbars</span></span>

<span data-ttu-id="1b588-238">Процесс восстановления, в основном, обращается к процессу сохранения.</span><span class="sxs-lookup"><span data-stu-id="1b588-238">The restore process basically reverses the save process.</span></span> <span data-ttu-id="1b588-239">В начале приложение получит код уведомления о [ \_ восстановлении ТБН](tbn-restore.md) с элементом **Член iItem** структуры [**нмтбресторе**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) со значением – 1.</span><span class="sxs-lookup"><span data-stu-id="1b588-239">At the beginning, your application will receive a [TBN\_RESTORE](tbn-restore.md) notification code with the **iItem** member of the [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) structure set to –1.</span></span> <span data-ttu-id="1b588-240">Для элемента **cbData** задается размер **PData**, а **кбуттонс** — количество кнопок.</span><span class="sxs-lookup"><span data-stu-id="1b588-240">The **cbData** member is set to the size of **pData**, and **cButtons** is set to the number of buttons.</span></span>

<span data-ttu-id="1b588-241">Обработчик уведомлений должен извлекать глобальные сведения, которые были помещены в начало элемента **pData** во время сохранения, а также **пкуррент** до начала первого блока данных, определяемых оболочкой.</span><span class="sxs-lookup"><span data-stu-id="1b588-241">Your notification handler should extract the global information that was placed at the beginning of **pData** during the save, and advance **pCurrent** to the start of the first block of Shell-defined data.</span></span> <span data-ttu-id="1b588-242">Задайте **кбитесперрекорд** в качестве размера блоков данных, которые использовались для сохранения данных кнопки.</span><span class="sxs-lookup"><span data-stu-id="1b588-242">Set **cBytesPerRecord** to the size of the data blocks you used to save the button data.</span></span> <span data-ttu-id="1b588-243">Задайте для **кбуттонс** число кнопок и возвратите.</span><span class="sxs-lookup"><span data-stu-id="1b588-243">Set **cButtons** to the number of buttons, and return.</span></span>

<span data-ttu-id="1b588-244">Следующий [**нмтбресторе**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) — для первой кнопки.</span><span class="sxs-lookup"><span data-stu-id="1b588-244">The next [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) is for the first button.</span></span> <span data-ttu-id="1b588-245">Элемент **пкуррент** указывает на начало первого блока данных кнопки, а **Член iItem** — на индекс кнопки.</span><span class="sxs-lookup"><span data-stu-id="1b588-245">The **pCurrent** member points to the start of your first block of button data, and **iItem** is set to the button index.</span></span> <span data-ttu-id="1b588-246">Извлеките эти данные и предварительные **пкуррент**.</span><span class="sxs-lookup"><span data-stu-id="1b588-246">Extract that data and advance **pCurrent**.</span></span> <span data-ttu-id="1b588-247">Загрузите данные в [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)и возвратите.</span><span class="sxs-lookup"><span data-stu-id="1b588-247">Load the data into [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton), and return.</span></span> <span data-ttu-id="1b588-248">Чтобы опустить кнопку в восстановленной панели инструментов, установите для элемента **идкомманд** в **тббуттон** значение 0.</span><span class="sxs-lookup"><span data-stu-id="1b588-248">To omit a button from the restored toolbar, set the **idCommand** member of **TBBUTTON** to zero.</span></span> <span data-ttu-id="1b588-249">Оболочка будет повторять процесс для оставшихся кнопок.</span><span class="sxs-lookup"><span data-stu-id="1b588-249">The Shell will repeat the process for the remaining buttons.</span></span> <span data-ttu-id="1b588-250">Помимо сообщений [**нмтбсаве**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) и **нмтбресторе** , можно также использовать такие сообщения, как [ТБН \_ Reset](tbn-reset.md) , чтобы сохранить и восстановить панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="1b588-250">In addition to the [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) and **NMTBRESTORE** messages, you can also use messages such as [TBN\_RESET](tbn-reset.md) to save and restore a toolbar.</span></span>

<span data-ttu-id="1b588-251">Следующий пример кода сохраняет панель инструментов до ее настройки и восстанавливает ее, если приложение получает сообщение о [ \_ сбросе ТБН](tbn-reset.md) .</span><span class="sxs-lookup"><span data-stu-id="1b588-251">The following code example saves a toolbar before it is customized, and restores it if the application receives a [TBN\_RESET](tbn-reset.md) message.</span></span>


```C++
int               i;
LPNMHDR           lpnmhdr;
static int        nResetCount;
static LPTBBUTTON lpSaveButtons;
LPARAM            lParam;

switch( lpnmhdr->code)
{
    case TBN_BEGINADJUST: // Begin customizing the toolbar.
    {
        LPTBNOTIFY  lpTB = (LPTBNOTIFY)lparam;
       
        // Allocate memory for the button information.
        
        nResetCount   = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        lpSaveButtons = (LPTBBUTTON)GlobalAlloc(GPTR, sizeof(TBBUTTON) * nResetCount);
      
        // In case the user presses reset, save the current configuration 
        // so the original toolbar can be restored.
        
        for(i = 0; i < nResetCount; i++)
        {
            SendMessage(lpTB->hdr.hwndFrom, 
                        TB_GETBUTTON, i, 
                        (LPARAM)(lpSaveButtons + i));
        }
    }
    
    return TRUE;
   
    case TBN_RESET:
    {
        LPTBNOTIFY lpTB = (LPTBNOTIFY)lparam;
        
        int nCount, i;
    
        // Remove all of the existing buttons, starting with the last one.
        
        nCount = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        
        for(i = nCount - 1; i >= 0; i--)
        {
            SendMessage(lpTB->hdr.hwndFrom, TB_DELETEBUTTON, i, 0);
        }
      
        SendMessage(lpTB->hdr.hwndFrom,      // Restore the saved buttons.
                    TB_ADDBUTTONS, 
                    (WPARAM)nResetCount, 
                    (LPARAM)lpSaveButtons);
    }
    
    return TRUE;
   
    case TBN_ENDADJUST:                // Free up the memory you allocated.
        GlobalFree((HGLOBAL)lpSaveButtons);
        
        return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="1b588-252">См. также</span><span class="sxs-lookup"><span data-stu-id="1b588-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b588-253">Использование элементов управления ToolBar</span><span class="sxs-lookup"><span data-stu-id="1b588-253">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

[<span data-ttu-id="1b588-254">**Значения индекса изображения стандартной кнопки панели инструментов**</span><span class="sxs-lookup"><span data-stu-id="1b588-254">**Toolbar Standard Button Image Index Values**</span></span>](toolbar-standard-button-image-index-values.md)
</dt> <dt>

<span data-ttu-id="1b588-255">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="1b588-255">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




