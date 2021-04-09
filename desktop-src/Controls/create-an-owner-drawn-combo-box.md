---
title: Создание Owner-Drawn поля со списком
description: В этом разделе показано, как использовать поле со списком, рисуемое владельцем.
ms.assetid: D866DE82-9734-4E8A-A366-5870C25B7C7B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5355dd33fe0067165308e9e6e5885b76edbe7ceb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070655"
---
# <a name="how-to-create-an-owner-drawn-combo-box"></a><span data-ttu-id="cb67a-103">Создание Owner-Drawn поля со списком</span><span class="sxs-lookup"><span data-stu-id="cb67a-103">How to Create an Owner-Drawn Combo Box</span></span>

<span data-ttu-id="cb67a-104">В этом разделе показано, как использовать поле со списком, рисуемое владельцем.</span><span class="sxs-lookup"><span data-stu-id="cb67a-104">This topic demonstrates how to use an owner-drawn combo box.</span></span> <span data-ttu-id="cb67a-105">В примере кода C++ используется раскрывающийся список, рисуемый владельцем, для отображения четырех групп продуктов, каждый из которых представлен точечным рисунком и именем.</span><span class="sxs-lookup"><span data-stu-id="cb67a-105">The C++ code example uses an owner-drawn drop-down list box to display the four food groups, each represented by a bitmap and a name.</span></span> <span data-ttu-id="cb67a-106">Выбор группы продуктов питания приводит к тому, что продуктов в этой группе появятся в списке.</span><span class="sxs-lookup"><span data-stu-id="cb67a-106">Selecting a food group causes the foods in that group to appear in a list.</span></span>

![снимок экрана с диалоговым окном со списком и развернутым раскрывающимся списком, отображающим значок и метку для каждого элемента](images/cscbx-01.png)

<span data-ttu-id="cb67a-108">Диалоговое окно также содержит список (IDLIST) и две кнопки: **ОК** (идок) и **Отмена** (идканцел).</span><span class="sxs-lookup"><span data-stu-id="cb67a-108">The dialog box also contains a list box (IDLIST) and two buttons: **OK** (IDOK) and **Cancel** (IDCANCEL).</span></span> <span data-ttu-id="cb67a-109">Константы ИДОК и ИДКАНЦЕЛ определяются файлами заголовков пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="cb67a-109">The IDOK and IDCANCEL constants are defined by the SDK header files.</span></span> <span data-ttu-id="cb67a-110">Константа IDLIST определяется в файле заголовка приложения, как и идентификатор элемента управления ИДКОМБО.</span><span class="sxs-lookup"><span data-stu-id="cb67a-110">The constant IDLIST is defined in the application's header file, as is the control identifier, IDCOMBO.</span></span> <span data-ttu-id="cb67a-111">Дополнительные сведения о диалоговых окнах см. в разделе [диалоговые окна](/windows/desktop/dlgbox/dialog-boxes).</span><span class="sxs-lookup"><span data-stu-id="cb67a-111">For more information about dialog boxes, see [Dialog Boxes](/windows/desktop/dlgbox/dialog-boxes).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="cb67a-112">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="cb67a-112">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="cb67a-113">Технологии</span><span class="sxs-lookup"><span data-stu-id="cb67a-113">Technologies</span></span>

-   [<span data-ttu-id="cb67a-114">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="cb67a-114">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="cb67a-115">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="cb67a-115">Prerequisites</span></span>

-   <span data-ttu-id="cb67a-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="cb67a-116">C/C++</span></span>
-   <span data-ttu-id="cb67a-117">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="cb67a-117">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="cb67a-118">Инструкции</span><span class="sxs-lookup"><span data-stu-id="cb67a-118">Instructions</span></span>

### <a name="step-1-create-the-owner-drawn-dialog-box"></a><span data-ttu-id="cb67a-119">Шаг 1. Создание диалогового окна «Owner-Drawn»</span><span class="sxs-lookup"><span data-stu-id="cb67a-119">Step 1: Create the Owner-Drawn Dialog Box</span></span>

<span data-ttu-id="cb67a-120">В примере кода используется функция [**диалогбокс**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) для создания модального диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="cb67a-120">The code example uses the [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) function to create a modal dialog box.</span></span> <span data-ttu-id="cb67a-121">Шаблон диалогового окна Идд \_ скмеал определяет стили окна, кнопки и идентификаторы элементов управления для поля со списком.</span><span class="sxs-lookup"><span data-stu-id="cb67a-121">The dialog box template, IDD\_SQMEAL, defines the window styles, buttons, and control identifiers for the combo box.</span></span> <span data-ttu-id="cb67a-122">В поле со списком в этом примере используются [**Стили \_ CBS**](combo-box-styles.md), [**CBS \_ овнердравфиксед**](combo-box-styles.md), [**CBS \_ Sort**](combo-box-styles.md), [**CBS \_ хасстрингс**](combo-box-styles.md), [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)и [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="cb67a-122">The combo box in this example uses the [**CBS\_DROPDOWNLIST**](combo-box-styles.md), [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md), [**CBS\_SORT**](combo-box-styles.md), [**CBS\_HASSTRINGS**](combo-box-styles.md), [**WS\_VSCROLL**](/windows/desktop/winmsg/window-styles), and [**WS\_TABSTOP**](/windows/desktop/winmsg/window-styles) styles.</span></span>


```C++
DialogBox(hInst, MAKEINTRESOURCE(IDD_SQMEAL), 
    hWnd, FoodDlgProc);
```



### <a name="step-2-process-the-wm_initdialog-and-wm_destroy-messages-in-a-dialog-box"></a><span data-ttu-id="cb67a-123">Шаг 2. Обработка сообщений WM \_ инитдиалог и WM \_ destroy в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="cb67a-123">Step 2: Process the WM\_INITDIALOG and WM\_DESTROY messages in a dialog box.</span></span>

<span data-ttu-id="cb67a-124">При использовании поля со списком в диалоговом окне, как правило, вы отвечаете на сообщение [**WM \_ инитдиалог**](/windows/desktop/dlgbox/wm-initdialog) , инициализируя поле со списком.</span><span class="sxs-lookup"><span data-stu-id="cb67a-124">When you use a combo box in a dialog box, you usually respond to a [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message by initializing the combo box.</span></span> <span data-ttu-id="cb67a-125">Приложение загружает точечные рисунки, используемые для рисуемого владельцем поля со списком, а затем вызывает определяемую приложением `InitGroupList` функцию для инициализации поля со списком.</span><span class="sxs-lookup"><span data-stu-id="cb67a-125">The application loads the bitmaps used for the owner-drawn combo box and then calls the application-defined `InitGroupList` function to initialize the combo box.</span></span> <span data-ttu-id="cb67a-126">Он также выбирает первый элемент списка в поле со списком, а затем вызывает определяемую приложением `InitFoodList` функцию для инициализации списка.</span><span class="sxs-lookup"><span data-stu-id="cb67a-126">It also selects the first list item in the combo box and then calls the application-defined `InitFoodList` function to initialize the list box.</span></span>

<span data-ttu-id="cb67a-127">В этом примере поле со списком, рисуемым владельцем, представляет собой раскрывающийся список, содержащий имена всех четырех групп продуктов.</span><span class="sxs-lookup"><span data-stu-id="cb67a-127">In the example, the owner-drawn combo box is a drop-down list box that contains the names of each of the four food groups.</span></span> <span data-ttu-id="cb67a-128">`InitGroupList` Добавляет имя каждой группы продуктов и использует сообщение [**\_ сетитемдата CB**](cb-setitemdata.md) для связывания маркера точечного рисунка с каждым элементом списка, идентифицирующим группу продуктов.</span><span class="sxs-lookup"><span data-stu-id="cb67a-128">`InitGroupList` adds the name of each food group , and uses the [**CB\_SETITEMDATA**](cb-setitemdata.md) message to associate a bitmap handle with each list item that identifies a food group.</span></span>

<span data-ttu-id="cb67a-129">Список в примере содержит имена продуктов в выбранной группе продуктов.</span><span class="sxs-lookup"><span data-stu-id="cb67a-129">The list box in the example contains the names of foods in the selected food group.</span></span> <span data-ttu-id="cb67a-130">**Инитфудлист** сбрасывает содержимое списка, а затем добавляет имена текущего выбора продуктов в раскрывающийся список текущая группа продуктов.</span><span class="sxs-lookup"><span data-stu-id="cb67a-130">**InitFoodList** resets the contents of the list box, then adds the names of the current food selection in the current food group drop-down list box.</span></span>


```C++
case WM_INITDIALOG:

    // Call an application-defined function to load bitmap resources.
    if (!LoadIconBitmaps())
    {
        EndDialog(hDlg, -1);
        break;
    }

    // Initialize the food groups combo box and select the first item.
    InitGroupList(hDlg);
    SendDlgItemMessage(hDlg, IDCOMBO, CB_SETCURSEL, 0, 0); 

    // Initialize the food list box and select the first item.
    InitFoodList(hDlg);
    SendDlgItemMessage(hDlg, IDLIST, LB_SETCURSEL, 0, 0); 

     return (INT_PTR)TRUE;
```



<span data-ttu-id="cb67a-131">При получении сообщения [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) приложение удаляет точечные рисунки в поле со списком, рисуемом владельцем.</span><span class="sxs-lookup"><span data-stu-id="cb67a-131">When it receives the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, the application deletes the bitmaps in the owner-drawn combo box.</span></span>


```C++
case WM_DESTROY:

    // Call the application-defined function to free the bitmap resources.
    DeleteIconBitmaps();
    break;
```



### <a name="step-3-process-the-wm_measureitem-message"></a><span data-ttu-id="cb67a-132">Шаг 3. обработка сообщения WM \_ меасуреитем.</span><span class="sxs-lookup"><span data-stu-id="cb67a-132">Step 3: Process the WM\_MEASUREITEM message.</span></span>

<span data-ttu-id="cb67a-133">Поле со списком, рисуемое владельцем, отправляет сообщение [**WM \_ меасуреитем**](wm-measureitem.md) в свое родительское окно или процедуру диалогового окна, чтобы приложение может задать размеры каждого элемента списка.</span><span class="sxs-lookup"><span data-stu-id="cb67a-133">An owner-drawn combo box sends the [**WM\_MEASUREITEM**](wm-measureitem.md) message to its parent window or dialog box procedure so that the application can set the dimensions of each list item.</span></span> <span data-ttu-id="cb67a-134">Так как поле со списком "пример" имеет стиль [**CBS \_ овнердравфиксед**](combo-box-styles.md) , система отправляет сообщение **WM \_ меасуреитем** только один раз.</span><span class="sxs-lookup"><span data-stu-id="cb67a-134">Because the example combo box has the [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md) style, the system sends the **WM\_MEASUREITEM** message only once.</span></span> <span data-ttu-id="cb67a-135">Поля со списком в стиле [**CBS \_ овнердраввариабле**](combo-box-styles.md) отправляют сообщение **WM \_ меасуреитем** для каждого элемента списка.</span><span class="sxs-lookup"><span data-stu-id="cb67a-135">Combo boxes with the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style send a **WM\_MEASUREITEM** message for each list item.</span></span>

<span data-ttu-id="cb67a-136">Параметр *lParam* является указателем на структуру [**меасуреитемструкт**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) , определяющую элемент управления и элемент списка.</span><span class="sxs-lookup"><span data-stu-id="cb67a-136">The *lParam* parameter is a pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that identifies the control and list item.</span></span> <span data-ttu-id="cb67a-137">Он также содержит измерения по умолчанию для элемента списка.</span><span class="sxs-lookup"><span data-stu-id="cb67a-137">It also contains the default dimensions of the list item.</span></span> <span data-ttu-id="cb67a-138">В примере изменяется элемент структуры **итемхеигхт** , чтобы гарантировать, что элементы списка достаточно высоки для размещения растровых изображений группы продуктов.</span><span class="sxs-lookup"><span data-stu-id="cb67a-138">The example modifies the **itemHeight** structure member to ensure that the list items are high enough to accommodate the food-group bitmaps.</span></span>


```C++
case WM_MEASUREITEM:
    {
    // Set the height of the items in the food groups combo box.
    LPMEASUREITEMSTRUCT lpmis = (LPMEASUREITEMSTRUCT) lParam;

    if (lpmis->itemHeight < CY_BITMAP + 2)
        lpmis->itemHeight = CY_BITMAP + 2;

    break;
    }
```



### <a name="step-4-process-the-wm_drawitem-message"></a><span data-ttu-id="cb67a-139">Шаг 4. обработка сообщения WM \_ DRAWITEM.</span><span class="sxs-lookup"><span data-stu-id="cb67a-139">Step 4: Process the WM\_DRAWITEM message.</span></span>

<span data-ttu-id="cb67a-140">Поле со списком, рисуемое владельцем, отправляет сообщение [**WM \_ DRAWITEM**](wm-drawitem.md) в свое родительское окно или процедуру диалогового окна каждый раз, когда приложение должно перерисовывать элемент списка.</span><span class="sxs-lookup"><span data-stu-id="cb67a-140">An owner-drawn combo box sends the [**WM\_DRAWITEM**](wm-drawitem.md) message to its parent window or dialog box procedure each time the application must repaint a list item.</span></span> <span data-ttu-id="cb67a-141">Параметр *lParam* является указателем на структуру [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) , определяющую элемент управления и элемент списка.</span><span class="sxs-lookup"><span data-stu-id="cb67a-141">The *lParam* parameter is a pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure that identifies the control and list item.</span></span> <span data-ttu-id="cb67a-142">Он также содержит сведения, необходимые для рисования элемента.</span><span class="sxs-lookup"><span data-stu-id="cb67a-142">It also contains information needed to paint the item.</span></span>

<span data-ttu-id="cb67a-143">В примере приложения отображается текст элемента списка и точечный рисунок, связанный с группой пищи.</span><span class="sxs-lookup"><span data-stu-id="cb67a-143">The example application displays the list-item text and the bitmap associated with the food group.</span></span> <span data-ttu-id="cb67a-144">Если элемент имеет фокус, он также рисует прямоугольник фокуса.</span><span class="sxs-lookup"><span data-stu-id="cb67a-144">If the item has the focus, it also draws a focus rectangle.</span></span> <span data-ttu-id="cb67a-145">Перед отображением текста в примере задаются цвета переднего плана и фона на основе выбранного элемента.</span><span class="sxs-lookup"><span data-stu-id="cb67a-145">Before displaying the text, the example sets the foreground and background colors, based on the item selected.</span></span> <span data-ttu-id="cb67a-146">Так как поле со списком имеет стиль [**CBS \_ хасстрингс**](combo-box-styles.md) , поле со списком поддерживает текст для каждого элемента списка, который можно получить с помощью сообщения [**\_ жетлбтекст CB**](cb-getlbtext.md) .</span><span class="sxs-lookup"><span data-stu-id="cb67a-146">Because the combo box has the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the combo box maintains the text for each list item that can be retrieved using the [**CB\_GETLBTEXT**](cb-getlbtext.md) message.</span></span>

<span data-ttu-id="cb67a-147">Точечные рисунки, используемые для элемента списка, зависят от группы продуктов.</span><span class="sxs-lookup"><span data-stu-id="cb67a-147">The bitmaps used for the list item depend on the food group.</span></span> <span data-ttu-id="cb67a-148">`InitGroupList` использует сообщение [**\_ сетитемдата CB**](cb-setitemdata.md) для связывания маркера точечного рисунка с каждым элементом списка.</span><span class="sxs-lookup"><span data-stu-id="cb67a-148">`InitGroupList` uses the [**CB\_SETITEMDATA**](cb-setitemdata.md) message to associate a bitmap handle with each list item.</span></span> <span data-ttu-id="cb67a-149">Процедура окна Извлекает маркер растрового изображения из элемента **итемдата** структуры [**дравитемструкт**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) .</span><span class="sxs-lookup"><span data-stu-id="cb67a-149">The window procedure retrieves the bitmap handle from the **itemData** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span> <span data-ttu-id="cb67a-150">Система использует два точечных рисунка для каждого символа группы пищи: монохромное растровое изображение с растровой операцией СРКАНД для стирания неправильного региона за изображением и цветовой точечный рисунок с растровой операцией СРКПАИНТ для рисования изображения.</span><span class="sxs-lookup"><span data-stu-id="cb67a-150">The system uses two bitmaps for each food group symbol: a monochrome bitmap with the SRCAND raster operation to erase the irregular region behind the image, and a color bitmap with the SRCPAINT raster operation to paint the image.</span></span>


```C++
case WM_DRAWITEM:
    {
    COLORREF clrBackground;
    COLORREF clrForeground;
    TEXTMETRIC tm;
    int x;
    int y;
    HRESULT hr;
    size_t cch;

    LPDRAWITEMSTRUCT lpdis = (LPDRAWITEMSTRUCT) lParam;
       
    if (lpdis->itemID == -1) // Empty item)
        break;

    // Get the food icon from the item data.
    hbmIcon = (HBITMAP) lpdis->itemData;

    // The colors depend on whether the item is selected.
    clrForeground = SetTextColor(lpdis->hDC, 
        GetSysColor(lpdis->itemState & ODS_SELECTED ?
        COLOR_HIGHLIGHTTEXT : COLOR_WINDOWTEXT));

    clrBackground = SetBkColor(lpdis->hDC, 
        GetSysColor(lpdis->itemState & ODS_SELECTED ?
        COLOR_HIGHLIGHT : COLOR_WINDOW));

    // Calculate the vertical and horizontal position.
    GetTextMetrics(lpdis->hDC, &tm);
    y = (lpdis->rcItem.bottom + lpdis->rcItem.top - tm.tmHeight) / 2;
    x = LOWORD(GetDialogBaseUnits()) / 4;

    // Get and display the text for the list item.
    SendMessage(lpdis->hwndItem, CB_GETLBTEXT,
        lpdis->itemID, (LPARAM) achTemp);

    hr = StringCchLength(achTemp, 256, &cch);
    if (FAILED(hr))
    {
        // TODO: Write error handler.
    }

    ExtTextOut(lpdis->hDC, CX_BITMAP + 2 * x, y,
        ETO_CLIPPED | ETO_OPAQUE, &lpdis->rcItem,
        achTemp, (UINT)cch, NULL);

    // Restore the previous colors.
    SetTextColor(lpdis->hDC, clrForeground);
    SetBkColor(lpdis->hDC, clrBackground);
    
    //  Draw the food icon for the item. 
    HDC hdc = CreateCompatibleDC(lpdis->hDC); 
    if (hdc == NULL) 
        break; 
 
    SelectObject(hdc, hbmMask); 
    BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
        CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCAND); 
 
    SelectObject(hdc, hbmIcon); 
    BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
        CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCPAINT); 
 
    DeleteDC(hdc); 
  
    // If the item has the focus, draw the focus rectangle.
    if (lpdis->itemState & ODS_FOCUS)
        DrawFocusRect(lpdis->hDC, &lpdis->rcItem);

    break;
    }
```



### <a name="step-5-process-the-wm_command-message"></a><span data-ttu-id="cb67a-151">Шаг 5. Обработка \_ командного сообщения WM.</span><span class="sxs-lookup"><span data-stu-id="cb67a-151">Step 5: Process the WM\_COMMAND message.</span></span>

<span data-ttu-id="cb67a-152">При возникновении события в элементе управления диалогового окна элемент управления уведомляет процедуру диалогового окна с помощью [**\_ командного сообщения WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="cb67a-152">When an event occurs in a dialog box control, the control notifies the dialog box procedure by means of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="cb67a-153">Пример обрабатывает сообщения уведомления из поля со списком, списка и кнопки **ОК** .</span><span class="sxs-lookup"><span data-stu-id="cb67a-153">The example processes notification messages from the combo box, the list box, and the **OK** button.</span></span> <span data-ttu-id="cb67a-154">Идентификатор элемента управления находится в младшем слове *wParam*, а код уведомления — в слове *wParam* с высоким порядком.</span><span class="sxs-lookup"><span data-stu-id="cb67a-154">The control identifier is in the low-order word of *wParam*, and the notification code is in the high-order word of *wParam*.</span></span>

<span data-ttu-id="cb67a-155">Если идентификатор элемента управления — ИДКОМБО, в поле со списком возникло событие.</span><span class="sxs-lookup"><span data-stu-id="cb67a-155">If the control identifier is IDCOMBO, an event has occurred in the combo box.</span></span> <span data-ttu-id="cb67a-156">В ответ процедура диалогового окна игнорирует все другие события поля со списком, кроме [**КБН \_ селендок**](cbn-selendok.md), что означает, что был сделан выбор, раскрывающийся список был закрыт и внесенные изменения должны быть приняты.</span><span class="sxs-lookup"><span data-stu-id="cb67a-156">In response, the dialog box procedure ignores all other combo box events except [**CBN\_SELENDOK**](cbn-selendok.md), which indicates that a selection was made, the drop down list box was closed, and the changes made should be accepted.</span></span> <span data-ttu-id="cb67a-157">В диалоговом окне вызывается процедура `InitFoodList` для сброса содержимого списка и добавления имен текущего выбора в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="cb67a-157">The dialog box procedure calls `InitFoodList` to reset the contents of the list box and to add the names of the current selections in the drop-down list box.</span></span>

<span data-ttu-id="cb67a-158">Если идентификатор элемента управления — IDLIST, в списке произошло событие.</span><span class="sxs-lookup"><span data-stu-id="cb67a-158">If the control identifier is IDLIST, an event has occurred in the list box.</span></span> <span data-ttu-id="cb67a-159">Это приводит к тому, что процедура диалогового окна пропускает все события списка, кроме [**ЛБН \_ дблклк**](lbn-dblclk.md), что означает, что пользователь дважды щелкнул элемент списка.</span><span class="sxs-lookup"><span data-stu-id="cb67a-159">This causes the dialog box procedure to ignore all list box events except [**LBN\_DBLCLK**](lbn-dblclk.md), which indicates that the user has double-clicked a list item.</span></span> <span data-ttu-id="cb67a-160">Это событие обрабатывается так же, как если бы была выбрана кнопка **ОК** .</span><span class="sxs-lookup"><span data-stu-id="cb67a-160">This event is processed in the same way as if an **OK** button had been chosen.</span></span>

<span data-ttu-id="cb67a-161">Если идентификатор элемента управления — ИДОК, пользователь выбрал кнопку **ОК** .</span><span class="sxs-lookup"><span data-stu-id="cb67a-161">If the control identifier is IDOK, the user has chosen the **OK** button.</span></span> <span data-ttu-id="cb67a-162">В ответ процедура диалогового окна вставляет имя выбранного пищи в многострочный элемент управления "поле ввода", а затем вызывает функцию [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) для закрытия этого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="cb67a-162">In response, the dialog box procedure inserts the name of the selected food into the application's multi-line edit control, then calls the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function to close the dialog box.</span></span>

<span data-ttu-id="cb67a-163">Если идентификатор элемента управления — ИДКАНЦЕЛ, пользователь нажмет кнопку **Отмена** .</span><span class="sxs-lookup"><span data-stu-id="cb67a-163">If the control identifier is IDCANCEL, the user has clicked the **Cancel** button.</span></span> <span data-ttu-id="cb67a-164">В ответ процедура диалогового окна вызывает метод [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) , чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cb67a-164">In response, the dialog box procedure calls [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) to close the dialog box.</span></span>


```C++
case WM_COMMAND:
        switch (LOWORD(wParam)) 
        { 
            case IDCOMBO: 
                if (HIWORD(wParam) == CBN_SELENDOK) 
                { 
                    InitFoodList(hDlg); 
                    SendDlgItemMessage(hDlg, IDLIST, 
                        LB_SETCURSEL, 0, 0); 
                } 
                break; 
 
            case IDLIST: 
                if (HIWORD(wParam) != LBN_DBLCLK) 
                    break; 
 
            // For a double-click, process the OK case. 
            case IDOK: 
 
                // Get the text for the selected list item. 
                hwnd = GetDlgItem(hDlg, IDLIST); 

                // Here it is assumed the text can fit into achTemp.
                // If there is doubt, call LB_GETTEXTLENGTH first.
                SendMessage(hwnd, LB_GETTEXT, 
                    SendMessage(hwnd, LB_GETCURSEL, 0, 0), 
                    (LPARAM) achTemp); 
 
                // TODO: Do something with the selected text.
 
                EndDialog(hDlg, 0); 
                break; 
 
            case IDCANCEL: 
                hwnd = GetDlgItem(hDlg, IDCOMBO); 
                if (SendMessage(hwnd, CB_GETDROPPEDSTATE, 0, 0)) 
                    SendMessage(hwnd, CB_SHOWDROPDOWN, FALSE, 0); 
                else EndDialog(hDlg, 0); 
        } 
        break; 
```



## <a name="complete-example"></a><span data-ttu-id="cb67a-165">Полный пример</span><span class="sxs-lookup"><span data-stu-id="cb67a-165">Complete example</span></span>

<span data-ttu-id="cb67a-166">Ниже приведена процедура диалогового окна и вспомогательные функции для диалогового окна « **квадратный еды** ».</span><span class="sxs-lookup"><span data-stu-id="cb67a-166">Following is the dialog box procedure and the supporting functions for the **Square Meal** dialog box.</span></span>


```C++
#define ID_BREAD 0
#define ID_DAIRY 1
#define ID_FRUIT 2
#define ID_MEAT  3

#define CX_BITMAP 24
#define CY_BITMAP 24

HBITMAP hbmBread;
HBITMAP hbmDairy;
HBITMAP hbmMeat;
HBITMAP hbmFruit;
HBITMAP hbmMask;

HBITMAP hbmIcon;
```

```C++
// Message handler for Square Meal dialog box.
INT_PTR CALLBACK FoodDlgProc(HWND hDlg, UINT message, WPARAM wParam, 
    LPARAM lParam)
{
    UNREFERENCED_PARAMETER(lParam);
    TCHAR achTemp[256];
    HWND hwnd;

    switch (message)
    {
    case WM_INITDIALOG:

        // Call an application-defined function to load bitmap resources.
        if (!LoadIconBitmaps())
        {
            EndDialog(hDlg, -1);
            break;
        }

        // Initialize the food groups combo box and select the first item.
        InitGroupList(hDlg);
        SendDlgItemMessage(hDlg, IDCOMBO, CB_SETCURSEL, 0, 0); 

        // Initialize the food list box and select the first item.
        InitFoodList(hDlg);
        SendDlgItemMessage(hDlg, IDLIST, LB_SETCURSEL, 0, 0); 

         return (INT_PTR)TRUE;
   
    case WM_MEASUREITEM:
        {
        // Set the height of the items in the food groups combo box.
        LPMEASUREITEMSTRUCT lpmis = (LPMEASUREITEMSTRUCT) lParam;

        if (lpmis->itemHeight < CY_BITMAP + 2)
            lpmis->itemHeight = CY_BITMAP + 2;

        break;
        }

    case WM_DRAWITEM:
        {
        COLORREF clrBackground;
        COLORREF clrForeground;
        TEXTMETRIC tm;
        int x;
        int y;
        HRESULT hr;
        size_t cch;

        LPDRAWITEMSTRUCT lpdis = (LPDRAWITEMSTRUCT) lParam;
           
        if (lpdis->itemID == -1) // Empty item)
            break;

        // Get the food icon from the item data.
        hbmIcon = (HBITMAP) lpdis->itemData;

        // The colors depend on whether the item is selected.
        clrForeground = SetTextColor(lpdis->hDC, 
            GetSysColor(lpdis->itemState & ODS_SELECTED ?
            COLOR_HIGHLIGHTTEXT : COLOR_WINDOWTEXT));

        clrBackground = SetBkColor(lpdis->hDC, 
            GetSysColor(lpdis->itemState & ODS_SELECTED ?
            COLOR_HIGHLIGHT : COLOR_WINDOW));

        // Calculate the vertical and horizontal position.
        GetTextMetrics(lpdis->hDC, &tm);
        y = (lpdis->rcItem.bottom + lpdis->rcItem.top - tm.tmHeight) / 2;
        x = LOWORD(GetDialogBaseUnits()) / 4;

        // Get and display the text for the list item.
        SendMessage(lpdis->hwndItem, CB_GETLBTEXT,
            lpdis->itemID, (LPARAM) achTemp);

        hr = StringCchLength(achTemp, 256, &cch);
        if (FAILED(hr))
        {
            // TODO: Write error handler.
        }

        ExtTextOut(lpdis->hDC, CX_BITMAP + 2 * x, y,
            ETO_CLIPPED | ETO_OPAQUE, &lpdis->rcItem,
            achTemp, (UINT)cch, NULL);

        // Restore the previous colors.
        SetTextColor(lpdis->hDC, clrForeground);
        SetBkColor(lpdis->hDC, clrBackground);
        
        //  Draw the food icon for the item. 
        HDC hdc = CreateCompatibleDC(lpdis->hDC); 
        if (hdc == NULL) 
            break; 
 
        SelectObject(hdc, hbmMask); 
        BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
            CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCAND); 
 
        SelectObject(hdc, hbmIcon); 
        BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
            CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCPAINT); 
 
        DeleteDC(hdc); 
      
        // If the item has the focus, draw the focus rectangle.
        if (lpdis->itemState & ODS_FOCUS)
            DrawFocusRect(lpdis->hDC, &lpdis->rcItem);

        break;
        }

    case WM_COMMAND:
            switch (LOWORD(wParam)) 
            { 
                case IDCOMBO: 
                    if (HIWORD(wParam) == CBN_SELENDOK) 
                    { 
                        InitFoodList(hDlg); 
                        SendDlgItemMessage(hDlg, IDLIST, 
                            LB_SETCURSEL, 0, 0); 
                    } 
                    break; 
 
                case IDLIST: 
                    if (HIWORD(wParam) != LBN_DBLCLK) 
                        break; 
 
                // For a double-click, process the OK case. 
                case IDOK: 
 
                    // Get the text for the selected list item. 
                    hwnd = GetDlgItem(hDlg, IDLIST); 

                    // Here it is assumed the text can fit into achTemp.
                    // If there is doubt, call LB_GETTEXTLENGTH first.
                    SendMessage(hwnd, LB_GETTEXT, 
                        SendMessage(hwnd, LB_GETCURSEL, 0, 0), 
                        (LPARAM) achTemp); 
 
                    // TODO: Do something with the selected text.
 
                    EndDialog(hDlg, 0); 
                    break; 
 
                case IDCANCEL: 
                    hwnd = GetDlgItem(hDlg, IDCOMBO); 
                    if (SendMessage(hwnd, CB_GETDROPPEDSTATE, 0, 0)) 
                        SendMessage(hwnd, CB_SHOWDROPDOWN, FALSE, 0); 
                    else EndDialog(hDlg, 0); 
            } 
            break; 

    case WM_DESTROY:

        // Call the application-defined function to free the bitmap resources.
        DeleteIconBitmaps();
        break;
    }
    return (INT_PTR)FALSE;
}

// Loads string resources and adds them as items to the drop-down list of
//   the food groups combo box. The bitmap handle of each item&#39;s icon is
//   stored as item data for easy access when the item needs to be drawn.
// 
void InitGroupList(HWND hDlg)
{
    TCHAR achTemp[256];
    DWORD dwIndex;

    // Get the handle of the food groups combo box.
    HWND hwndGroupsBox = GetDlgItem(hDlg, IDCOMBO);

    LoadString(hInst, IDS_BREAD, achTemp, sizeof(achTemp)/sizeof(TCHAR));
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmBread);
    
    LoadString(hInst, IDS_DAIRY, achTemp, sizeof(achTemp)/sizeof(TCHAR)); 
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmDairy);

    LoadString(hInst, IDS_FRUIT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmFruit); 

    LoadString(hInst, IDS_MEAT, achTemp, sizeof(achTemp)/sizeof(TCHAR)); 
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmMeat);

    return;
}

// Fills the food list based on the selected item in the food groups
//   combo box.
void InitFoodList(HWND hDlg)
{
    TCHAR achTemp[256];

    HWND hwndGroupsBox = GetDlgItem(hDlg, IDCOMBO);
    HWND hwndFoodList = GetDlgItem(hDlg, IDLIST);

    // Clear the list contents.
    SendMessage(hwndFoodList, LB_RESETCONTENT, 0, 0);

    // Find out which food group is selected.
    int idFoodGroup = SendMessage(hwndGroupsBox, CB_GETCURSEL, 0, 0);

    switch (idFoodGroup)
    {
    case ID_BREAD:
        LoadString(hInst, IDS_OAT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_WHEAT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_RYE, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);
        break;

    case ID_DAIRY:
        LoadString(hInst, IDS_CHEDDAR, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_MILK, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_PROCESSED, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_SWISS, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);
        
        break;

    case ID_FRUIT:
        LoadString(hInst, IDS_APPLES, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_BANANAS, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_ORANGES, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        break;

    case ID_MEAT:
        LoadString(hInst, IDS_BEEF, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_CHICKEN, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_PORK, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        break;

    default:
        break;
    }

    return;
}

// Loads the food icon bitmaps from the application resources.
//
BOOL LoadIconBitmaps(void)
{
    hbmBread = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_BREAD));

    if (hbmBread != NULL)
         hbmDairy = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_DAIRY));

    if (hbmDairy != NULL)
         hbmMeat = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_MEAT));

    if (hbmMeat != NULL)
        hbmFruit = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_FRUIT));
    
    if (hbmFruit != NULL)
        hbmMask = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_MASK));

    if (hbmMask != NULL)
        return TRUE;
        
    return FALSE;
}

// Frees the icon bitmps.
//
void DeleteIconBitmaps(void)
{
    FreeResource(reinterpret_cast<HGLOBAL>(hbmBread));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmDairy));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmMeat));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmFruit));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmMask));
}
```


## <a name="related-topics"></a><span data-ttu-id="cb67a-167">См. также</span><span class="sxs-lookup"><span data-stu-id="cb67a-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb67a-168">Использование полей со списком</span><span class="sxs-lookup"><span data-stu-id="cb67a-168">Using Combo Boxes</span></span>](using-combo-boxes.md)
</dt> </dl>

 

 