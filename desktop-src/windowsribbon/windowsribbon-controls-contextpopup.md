---
title: Контекстное всплывающее окно
description: Всплывающее контекстное меню — это основной элемент управления в Контекстпопуп представлении платформы Windows Ribbon.
ms.assetid: c41b888a-15aa-4c47-ad73-5dc30b5fa6f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c77441cc3cdcc9212d27d2230d76d2618f1831ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672329"
---
# <a name="context-popup"></a><span data-ttu-id="342ce-103">Контекстное всплывающее окно</span><span class="sxs-lookup"><span data-stu-id="342ce-103">Context Popup</span></span>

<span data-ttu-id="342ce-104">Всплывающее контекстное меню — это основной элемент управления в [**Контекстпопуп представлении**](windowsribbon-element-contextpopup.md) платформы Windows Ribbon.</span><span class="sxs-lookup"><span data-stu-id="342ce-104">A Context Popup is the principal control in the [**ContextPopup View**](windowsribbon-element-contextpopup.md) of the Windows Ribbon framework.</span></span> <span data-ttu-id="342ce-105">Это обширная система контекстного меню, доступная только для платформы в качестве расширения для реализации ленты — платформа не предоставляет всплывающее окно контекста как независимый элемент управления.</span><span class="sxs-lookup"><span data-stu-id="342ce-105">It is a rich context menu system that is only exposed by the framework as an extension to a Ribbon implementation—the framework does not expose the Context Popup as an independent control.</span></span>

-   [<span data-ttu-id="342ce-106">Компоненты всплывающего контекстного меню</span><span class="sxs-lookup"><span data-stu-id="342ce-106">Components of the Context Popup</span></span>](#context-popup)
-   [<span data-ttu-id="342ce-107">Реализация всплывающего контекстного меню</span><span class="sxs-lookup"><span data-stu-id="342ce-107">Implement the Context Popup</span></span>](#implement-the-context-popup)
    -   [<span data-ttu-id="342ce-108">разметку</span><span class="sxs-lookup"><span data-stu-id="342ce-108">Markup</span></span>](#markup)
    -   [<span data-ttu-id="342ce-109">Код</span><span class="sxs-lookup"><span data-stu-id="342ce-109">Code</span></span>](#code)
-   [<span data-ttu-id="342ce-110">Свойства всплывающего контекстного меню</span><span class="sxs-lookup"><span data-stu-id="342ce-110">Context Popup Properties</span></span>](#context-popup-properties)
-   [<span data-ttu-id="342ce-111">См. также</span><span class="sxs-lookup"><span data-stu-id="342ce-111">Related topics</span></span>](#related-topics)

## <a name="components-of-the-context-popup"></a><span data-ttu-id="342ce-112">Компоненты всплывающего контекстного меню</span><span class="sxs-lookup"><span data-stu-id="342ce-112">Components of the Context Popup</span></span>

<span data-ttu-id="342ce-113">Всплывающее контекстное меню — это логический контейнер для контекстного дерева, а Mini-Toolbar вложенные элементы управления, доступные через элементы разметки [**ContextMenu**](windowsribbon-element-contextmenu.md) и [**минитулбар**](windowsribbon-element-minitoolbar.md) соответственно:</span><span class="sxs-lookup"><span data-stu-id="342ce-113">The Context Popup is a logical container for the Context Menu and Mini-Toolbar sub-controls that are exposed through the [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) markup elements, respectively:</span></span>

-   <span data-ttu-id="342ce-114">[**ContextMenu**](windowsribbon-element-contextmenu.md) предоставляет меню команд и коллекций.</span><span class="sxs-lookup"><span data-stu-id="342ce-114">The [**ContextMenu**](windowsribbon-element-contextmenu.md) exposes a menu of Commands and galleries.</span></span>
-   <span data-ttu-id="342ce-115">[**Минитулбар**](windowsribbon-element-minitoolbar.md) предоставляет плавающую панель инструментов различных команд, коллекций и сложных элементов управления, таких как [элемент управления шрифта](windowsribbon-controls-fontcontrol.md) и [поле со списком](windowsribbon-controls-combobox.md).</span><span class="sxs-lookup"><span data-stu-id="342ce-115">The [**MiniToolbar**](windowsribbon-element-minitoolbar.md) exposes a floating toolbar of various Commands, galleries, and complex controls such as the [Font Control](windowsribbon-controls-fontcontrol.md) and the [Combo Box](windowsribbon-controls-combobox.md).</span></span>

<span data-ttu-id="342ce-116">Каждый подэлемент управления может отображаться в контекстном меню не более одного раза.</span><span class="sxs-lookup"><span data-stu-id="342ce-116">Each sub-control can appear at most once in a Context Popup.</span></span>

<span data-ttu-id="342ce-117">На следующем снимке экрана показан контекст всплывающего окна и его вложенные элементы управления.</span><span class="sxs-lookup"><span data-stu-id="342ce-117">The following screen shot illustrates the Context Popup and its constituent sub-controls.</span></span>

![снимок экрана с выносками, в которых отображаются контекстные компоненты пользовательского интерфейса ленты.](images/controls/contextpopup.png)

<span data-ttu-id="342ce-119">Всплывающее контекстное меню является исключительно концептуальным и не предоставляет никаких функциональных возможностей пользовательского интерфейса, таких как позиционирование или изменение размера.</span><span class="sxs-lookup"><span data-stu-id="342ce-119">The Context Popup is purely conceptual and does not expose any UI functionality itself, such as positioning or sizing.</span></span>

> [!Note]  
> <span data-ttu-id="342ce-120">Всплывающее контекстное меню обычно выводится щелчком правой кнопкой мыши (или нажатием клавиши SHIFT + F10) на интересующем объекте.</span><span class="sxs-lookup"><span data-stu-id="342ce-120">The Context Popup is typically displayed by right-clicking the mouse (or through the keyboard shortcut SHIFT+F10) on an object of interest.</span></span> <span data-ttu-id="342ce-121">Однако действия, необходимые для вывода контекстного всплывающего окна, определяются приложением.</span><span class="sxs-lookup"><span data-stu-id="342ce-121">However, the steps required to display the Context Popup are defined by the application.</span></span>

 

## <a name="implement-the-context-popup"></a><span data-ttu-id="342ce-122">Реализация всплывающего контекстного меню</span><span class="sxs-lookup"><span data-stu-id="342ce-122">Implement the Context Popup</span></span>

<span data-ttu-id="342ce-123">Аналогично тому, как и другие элементы управления платформы Windows Ribbon, всплывающее контекстное меню реализуется с помощью компонента разметки, который указывает сведения о презентации и компонент кода, управляющий его функциональностью.</span><span class="sxs-lookup"><span data-stu-id="342ce-123">In similar fashion to other Windows Ribbon framework controls, the Context Popup is implemented through a markup component that specifies its presentation details and a code component that governs its functionality.</span></span>

<span data-ttu-id="342ce-124">В следующей таблице перечислены элементы управления, поддерживаемые каждым всплывающим контекстным элементом управления.</span><span class="sxs-lookup"><span data-stu-id="342ce-124">The following table lists the controls that are supported by each Context Popup sub-control.</span></span>



| <span data-ttu-id="342ce-125">Control</span><span class="sxs-lookup"><span data-stu-id="342ce-125">Control</span></span>                                                                  | <span data-ttu-id="342ce-126">Mini-Toolbar</span><span class="sxs-lookup"><span data-stu-id="342ce-126">Mini-Toolbar</span></span> | <span data-ttu-id="342ce-127">Контекстное меню</span><span class="sxs-lookup"><span data-stu-id="342ce-127">Context Menu</span></span> |
|--------------------------------------------------------------------------|--------------|--------------|
| [<span data-ttu-id="342ce-128">Кнопка</span><span class="sxs-lookup"><span data-stu-id="342ce-128">Button</span></span>](windowsribbon-controls-button.md)                              | <span data-ttu-id="342ce-129">x</span><span class="sxs-lookup"><span data-stu-id="342ce-129">x</span></span>            | <span data-ttu-id="342ce-130">x</span><span class="sxs-lookup"><span data-stu-id="342ce-130">x</span></span>            |
| [<span data-ttu-id="342ce-131">Флажок</span><span class="sxs-lookup"><span data-stu-id="342ce-131">Check Box</span></span>](windowsribbon-controls-checkbox.md)                         | <span data-ttu-id="342ce-132">x</span><span class="sxs-lookup"><span data-stu-id="342ce-132">x</span></span>            | <span data-ttu-id="342ce-133">x</span><span class="sxs-lookup"><span data-stu-id="342ce-133">x</span></span>            |
| [<span data-ttu-id="342ce-134">Поле со списком</span><span class="sxs-lookup"><span data-stu-id="342ce-134">Combo Box</span></span>](windowsribbon-controls-combobox.md)                         | <span data-ttu-id="342ce-135">x</span><span class="sxs-lookup"><span data-stu-id="342ce-135">x</span></span>            |              |
| [<span data-ttu-id="342ce-136">Кнопка раскрывающегося списка</span><span class="sxs-lookup"><span data-stu-id="342ce-136">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)            | <span data-ttu-id="342ce-137">x</span><span class="sxs-lookup"><span data-stu-id="342ce-137">x</span></span>            | <span data-ttu-id="342ce-138">x</span><span class="sxs-lookup"><span data-stu-id="342ce-138">x</span></span>            |
| [<span data-ttu-id="342ce-139">Выбор цвета для раскрывающегося списка</span><span class="sxs-lookup"><span data-stu-id="342ce-139">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md) | <span data-ttu-id="342ce-140">x</span><span class="sxs-lookup"><span data-stu-id="342ce-140">x</span></span>            | <span data-ttu-id="342ce-141">x</span><span class="sxs-lookup"><span data-stu-id="342ce-141">x</span></span>            |
| [<span data-ttu-id="342ce-142">Раскрывающийся список</span><span class="sxs-lookup"><span data-stu-id="342ce-142">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)          | <span data-ttu-id="342ce-143">x</span><span class="sxs-lookup"><span data-stu-id="342ce-143">x</span></span>            | <span data-ttu-id="342ce-144">x</span><span class="sxs-lookup"><span data-stu-id="342ce-144">x</span></span>            |
| [<span data-ttu-id="342ce-145">Элемент управления шрифтами</span><span class="sxs-lookup"><span data-stu-id="342ce-145">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)                   | <span data-ttu-id="342ce-146">x</span><span class="sxs-lookup"><span data-stu-id="342ce-146">x</span></span>            |              |
| [<span data-ttu-id="342ce-147">Кнопка "Справка"</span><span class="sxs-lookup"><span data-stu-id="342ce-147">Help Button</span></span>](windowsribbon-controls-helpbutton.md)                     |              |              |
| [<span data-ttu-id="342ce-148">Коллекция на ленте</span><span class="sxs-lookup"><span data-stu-id="342ce-148">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)          |              |              |
| [<span data-ttu-id="342ce-149">Spinner</span><span class="sxs-lookup"><span data-stu-id="342ce-149">Spinner</span></span>](windowsribbon-controls-spinner.md)                            |              |              |
| [<span data-ttu-id="342ce-150">Разворачивающаяся кнопка</span><span class="sxs-lookup"><span data-stu-id="342ce-150">Split Button</span></span>](windowsribbon-controls-splitbutton.md)                   | <span data-ttu-id="342ce-151">x</span><span class="sxs-lookup"><span data-stu-id="342ce-151">x</span></span>            | <span data-ttu-id="342ce-152">x</span><span class="sxs-lookup"><span data-stu-id="342ce-152">x</span></span>            |
| [<span data-ttu-id="342ce-153">Коллекция разделенных кнопок</span><span class="sxs-lookup"><span data-stu-id="342ce-153">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)    | <span data-ttu-id="342ce-154">x</span><span class="sxs-lookup"><span data-stu-id="342ce-154">x</span></span>            | <span data-ttu-id="342ce-155">x</span><span class="sxs-lookup"><span data-stu-id="342ce-155">x</span></span>            |
| [<span data-ttu-id="342ce-156">Выключатель</span><span class="sxs-lookup"><span data-stu-id="342ce-156">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md)                 | <span data-ttu-id="342ce-157">x</span><span class="sxs-lookup"><span data-stu-id="342ce-157">x</span></span>            | <span data-ttu-id="342ce-158">x</span><span class="sxs-lookup"><span data-stu-id="342ce-158">x</span></span>            |



 

### <a name="markup"></a><span data-ttu-id="342ce-159">разметку</span><span class="sxs-lookup"><span data-stu-id="342ce-159">Markup</span></span>

<span data-ttu-id="342ce-160">Каждый всплывающий элемент контекстного меню должен быть объявлен отдельно в разметке.</span><span class="sxs-lookup"><span data-stu-id="342ce-160">Each Context Popup sub-control must be declared individually in markup.</span></span>

### <a name="mini-toolbar"></a><span data-ttu-id="342ce-161">Mini-Toolbar</span><span class="sxs-lookup"><span data-stu-id="342ce-161">Mini-Toolbar</span></span>

<span data-ttu-id="342ce-162">При добавлении элементов управления в контекстное меню мини-панели инструментов следует учитывать следующие две рекомендации.</span><span class="sxs-lookup"><span data-stu-id="342ce-162">When adding controls to a Context Popup Mini-Toolbar, the following two recommendations should be considered:</span></span>

-   <span data-ttu-id="342ce-163">Элементы управления должны быть хорошо распознаваемыми и предоставляют очевидные функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="342ce-163">Controls should be highly recognizable and provide obvious functionality.</span></span> <span data-ttu-id="342ce-164">Знание является ключом, так как метки и подсказки не доступны для элементов управления Mini-Toolbar.</span><span class="sxs-lookup"><span data-stu-id="342ce-164">Familiarity is key, as labels and tooltips are not exposed for Mini-Toolbar controls.</span></span>
-   <span data-ttu-id="342ce-165">Каждая команда, предоставляемая элементом управления, должна быть представлена в любом расположении в пользовательском интерфейсе ленты.</span><span class="sxs-lookup"><span data-stu-id="342ce-165">Each Command exposed by a control should be presented elsewhere in the ribbon UI.</span></span> <span data-ttu-id="342ce-166">Mini-Toolbar не поддерживает навигацию по клавишам.</span><span class="sxs-lookup"><span data-stu-id="342ce-166">The Mini-Toolbar does not support keyboard navigation.</span></span>

<span data-ttu-id="342ce-167">В следующем примере показана базовая разметка для элемента [**минитулбар**](windowsribbon-element-minitoolbar.md) , который содержит три элемента управления ["Кнопка"](windowsribbon-controls-button.md) .</span><span class="sxs-lookup"><span data-stu-id="342ce-167">The following example demonstrates the basic markup for a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element that contains three [Button](windowsribbon-controls-button.md) controls.</span></span>

> [!Note]  
> <span data-ttu-id="342ce-168">Для каждой строки элементов управления на мини-панели инструментов указан один элемент [**менуграуп**](windowsribbon-element-menugroup.md) .</span><span class="sxs-lookup"><span data-stu-id="342ce-168">One [**MenuGroup**](windowsribbon-element-menugroup.md) element is specified for each row of controls in the Mini-Toolbar.</span></span>

 


```C++
<MiniToolbar Name="MiniToolbar">
  <MenuGroup>
    <Button CommandName="cmdButton1" />
    <Button CommandName="cmdButton2" />
    <Button CommandName="cmdButton3" />
  </MenuGroup>
</MiniToolbar>
```



### <a name="context-menu"></a><span data-ttu-id="342ce-169">Контекстное меню</span><span class="sxs-lookup"><span data-stu-id="342ce-169">Context Menu</span></span>

<span data-ttu-id="342ce-170">В следующем примере показана базовая разметка для элемента [**ContextMenu**](windowsribbon-element-contextmenu.md) , содержащего три элемента управления ["Кнопка"](windowsribbon-controls-button.md) .</span><span class="sxs-lookup"><span data-stu-id="342ce-170">The following example demonstrates the basic markup for a [**ContextMenu**](windowsribbon-element-contextmenu.md) element that contains three [Button](windowsribbon-controls-button.md) controls.</span></span>

> [!Note]  
> <span data-ttu-id="342ce-171">Каждый набор элементов управления в элементе [**менуграуп**](windowsribbon-element-menugroup.md) отделяется горизонтальной чертой в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="342ce-171">Each set of controls in the [**MenuGroup**](windowsribbon-element-menugroup.md) element is separated by a horizontal bar in the Context Menu.</span></span>

 


```C++
<ContextMenu Name="ContextMenu">
  <MenuGroup>
    <Button CommandName="cmdCut" />
    <Button CommandName="cmdCopy" />
    <Button CommandName="cmdPaste" />
  </MenuGroup>
</ContextMenu>
```



<span data-ttu-id="342ce-172">Хотя всплывающее контекстное меню может содержать не более одного из дочерних элементов управления, в разметке ленты можно использовать несколько объявлений элементов [**ContextMenu**](windowsribbon-element-contextmenu.md) и [**минитулбар**](windowsribbon-element-minitoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="342ce-172">Although a Context Popup can contain at most one of each sub-control, multiple [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element declarations in the Ribbon markup are valid.</span></span> <span data-ttu-id="342ce-173">Это позволяет приложению поддерживать различные сочетания контекстного меню и Mini-Toolbar элементов управления на основе критериев, определенных приложением, например контекста рабочей области.</span><span class="sxs-lookup"><span data-stu-id="342ce-173">This allows an application to support various combinations of Context Menu and Mini-Toolbar controls, based on criteria defined by the application, such as workspace context.</span></span>

<span data-ttu-id="342ce-174">Дополнительные сведения см. в описании элемента [**контекстмап**](windowsribbon-element-contextmap.md) .</span><span class="sxs-lookup"><span data-stu-id="342ce-174">For more information, see the [**ContextMap**](windowsribbon-element-contextmap.md) element.</span></span>

<span data-ttu-id="342ce-175">В следующем примере показана базовая разметка для элемента [**контекстпопуп**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="342ce-175">The following example demonstrates the basic markup for the [**ContextPopup**](windowsribbon-element-contextpopup.md) element.</span></span>


```C++
<ContextPopup>
  <ContextPopup.MiniToolbars>
    <MiniToolbar Name="MiniToolbar">
      <MenuGroup>
        <Button CommandName="cmdButton1" />
        <Button CommandName="cmdButton2" />
        <Button CommandName="cmdButton3" />
      </MenuGroup>
    </MiniToolbar>
  </ContextPopup.MiniToolbars>
  <ContextPopup.ContextMenus>
    <ContextMenu Name="ContextMenu">
      <MenuGroup>
        <Button CommandName="cmdCut" />
        <Button CommandName="cmdCopy" />
        <Button CommandName="cmdPaste" />
      </MenuGroup>
    </ContextMenu>
  </ContextPopup.ContextMenus>
  <ContextPopup.ContextMaps>
    <ContextMap CommandName="cmdContextMap" ContextMenu="ContextMenu" MiniToolbar="MiniToolbar"/>
  </ContextPopup.ContextMaps>
</ContextPopup>
```



### <a name="code"></a><span data-ttu-id="342ce-176">Код</span><span class="sxs-lookup"><span data-stu-id="342ce-176">Code</span></span>

<span data-ttu-id="342ce-177">Чтобы вызвать всплывающее контекстное меню, метод [**иуиконтекстуалуи:: шоватлокатион**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) вызывается, когда окно верхнего уровня приложения на ленте получает \_ уведомление WM CONTEXTMENU.</span><span class="sxs-lookup"><span data-stu-id="342ce-177">To invoke a Context Popup, the [**IUIContextualUI::ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) method is called when the top-level window of the Ribbon application receives a WM\_CONTEXTMENU notification.</span></span>

<span data-ttu-id="342ce-178">В этом примере показано, как управлять \_ уведомлением WM CONTEXTMENU в методе WndProc () приложения Ribbon.</span><span class="sxs-lookup"><span data-stu-id="342ce-178">This example demonstrates how to handle the WM\_CONTEXTMENU notification in the WndProc() method of the Ribbon application.</span></span>


```C++
case WM_CONTEXTMENU:
  POINT pt;
  POINTSTOPOINT(pt, lParam);

  // ShowContextualUI method defined by the application.
  ShowContextualUI (pt, hWnd);
  break;
```



<span data-ttu-id="342ce-179">В следующем примере показано, как приложение ленты может отображать контекстное всплывающее окно в определенном месте на экране с помощью метода [**иуиконтекстуалуи:: шоватлокатион**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) .</span><span class="sxs-lookup"><span data-stu-id="342ce-179">The following example demonstrates how a Ribbon application can show the Context Popup at a specific screen location using the [**IUIContextualUI::ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) method.</span></span>

<span data-ttu-id="342ce-180">Жеткуррентконтекст () имеет значение `cmdContextMap` , определенное в предыдущем примере разметки.</span><span class="sxs-lookup"><span data-stu-id="342ce-180">GetCurrentContext() has a value of `cmdContextMap` as defined in the preceding markup example.</span></span>

<span data-ttu-id="342ce-181">g \_ паппликатион — это ссылка на интерфейс [**иуифрамеворк**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) .</span><span class="sxs-lookup"><span data-stu-id="342ce-181">g\_pApplication is a reference to the [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) interface.</span></span>


```C++
HRESULT ShowContextualUI(POINT& ptLocation, HWND hWnd)
{
  GetDisplayLocation(ptLocation, hWnd);

  HRESULT hr = E_FAIL;

  IUIContextualUI* pContextualUI = NULL;
 
  if (SUCCEEDED(g_pFramework->GetView(
                                g_pApplication->GetCurrentContext(), 
                                IID_PPV_ARGS(&pContextualUI))))
  {
    hr = pContextualUI->ShowAtLocation(ptLocation.x, ptLocation.y);
    pContextualUI->Release();
  }

  return hr;
}
```



<span data-ttu-id="342ce-182">Ссылку на [**иуиконтекстуалуи**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) можно освободить до закрытия всплывающего окна контекста, как показано в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="342ce-182">The reference to [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) can be released before the Context Popup is dismissed, as shown in the preceding example.</span></span> <span data-ttu-id="342ce-183">Однако ссылка должна быть освобождена в некоторый момент, чтобы избежать утечек памяти.</span><span class="sxs-lookup"><span data-stu-id="342ce-183">However, the reference must be released at some point to avoid memory leaks.</span></span>

> [!Caution]  
> <span data-ttu-id="342ce-184">Mini-Toolbar имеет встроенный эффект исчезания, основанный на указателе мыши.</span><span class="sxs-lookup"><span data-stu-id="342ce-184">The Mini-Toolbar has a built-in fade effect that is based on the proximity of the mouse pointer.</span></span> <span data-ttu-id="342ce-185">По этой причине рекомендуется, чтобы Mini-Toolbar отображались как можно ближе к указателю мыши.</span><span class="sxs-lookup"><span data-stu-id="342ce-185">For this reason, it is recommended that the Mini-Toolbar be displayed as close to the mouse pointer as possible.</span></span> <span data-ttu-id="342ce-186">В противном случае, в связи с конфликтующими механизмами отображения, Mini-Toolbar может отображаться не так, как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="342ce-186">Otherwise, due to the conflicting display mechanisms, the Mini-Toolbar may not render as expected.</span></span>

 

## <a name="context-popup-properties"></a><span data-ttu-id="342ce-187">Свойства всплывающего контекстного меню</span><span class="sxs-lookup"><span data-stu-id="342ce-187">Context Popup Properties</span></span>

<span data-ttu-id="342ce-188">Нет ключей свойств, связанных с всплывающим элементом управления контекстом.</span><span class="sxs-lookup"><span data-stu-id="342ce-188">There are no property keys associated with the Context Popup control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="342ce-189">См. также</span><span class="sxs-lookup"><span data-stu-id="342ce-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="342ce-190">Библиотека элементов управления платформы Windows ленты</span><span class="sxs-lookup"><span data-stu-id="342ce-190">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="342ce-191">Пример Контекстпопуп</span><span class="sxs-lookup"><span data-stu-id="342ce-191">ContextPopup Sample</span></span>](windowsribbon-contextpopupsample.md)
</dt> </dl>

 

 