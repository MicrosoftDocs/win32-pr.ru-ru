---
title: Устаревшие функции шаблона элемента управления
description: Устаревшие функции шаблона элемента управления
ms.assetid: 06434b07-7592-4909-8c4e-064382bdbf98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f646f9a9e3139d487785e344b9d3fc242b1a40e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410693"
---
# <a name="deprecated-control-pattern-functions"></a><span data-ttu-id="85528-103">Устаревшие функции шаблона элемента управления</span><span class="sxs-lookup"><span data-stu-id="85528-103">Deprecated Control Pattern Functions</span></span>

> [!Note]  
> <span data-ttu-id="85528-104">Функции шаблона элемента управления, описанные в этом разделе, являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="85528-104">The control pattern functions described in this section are deprecated.</span></span> <span data-ttu-id="85528-105">Клиентские приложения должны использовать интерфейсы модели COM, описанные в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="85528-105">Client applications should use the Component Object Model (COM) interfaces described in the following sections:</span></span>
>
> -   [<span data-ttu-id="85528-106">Интерфейсы элементов модели автоматизации пользовательского интерфейса для клиентов</span><span class="sxs-lookup"><span data-stu-id="85528-106">UI Automation Element Interfaces for Clients</span></span>](uiauto-entry-uiautoclientinterfaces.md)
> -   [<span data-ttu-id="85528-107">Интерфейс условий свойств для клиентов</span><span class="sxs-lookup"><span data-stu-id="85528-107">Property Condition Interface for Clients</span></span>](uiauto-client-propconditioninterfaces.md)
> -   [<span data-ttu-id="85528-108">Интерфейсы шаблонов элементов управления для клиентов</span><span class="sxs-lookup"><span data-stu-id="85528-108">Control Pattern Interfaces for Clients</span></span>](uiauto-client-controlpatterninterfaces.md)
> -   [<span data-ttu-id="85528-109">Интерфейсы обработки событий для клиентов</span><span class="sxs-lookup"><span data-stu-id="85528-109">Event Handling Interfaces for Clients</span></span>](uiauto-client-eventhandlinginterfaces.md)
> -   [<span data-ttu-id="85528-110">Интерфейсы фабрики прокси-серверов для клиентов</span><span class="sxs-lookup"><span data-stu-id="85528-110">Proxy Factory Interfaces for Clients</span></span>](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a><span data-ttu-id="85528-111">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="85528-111">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85528-112">Функция</span><span class="sxs-lookup"><span data-stu-id="85528-112">Function</span></span></th>
<th><span data-ttu-id="85528-113">Описание</span><span class="sxs-lookup"><span data-stu-id="85528-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="85528-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-dockpattern_setdockposition"><strong>DockPattern_SetDockPosition</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-dockpattern_setdockposition"><strong>DockPattern_SetDockPosition</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-115">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-115">This function is deprecated.</span></span> <span data-ttu-id="85528-116">Вместо этого клиентские приложения должны использовать COM-интерфейсы модели автоматизации пользовательского интерфейса Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="85528-116">Client applications should use the Microsoft UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-117">Закрепляет элемент модели автоматизации пользовательского интерфейса в запрошенном <em>dockPosition</em> в контейнере закрепления.</span><span class="sxs-lookup"><span data-stu-id="85528-117">Docks the UI Automation element at the requested <em>dockPosition</em> within a docking container.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_collapse"><strong>ExpandCollapsePattern_Collapse</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_collapse"><strong>ExpandCollapsePattern_Collapse</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-119">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-119">This function is deprecated.</span></span> <span data-ttu-id="85528-120">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-120">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-121">Скрывает все узлы-потомки, элементы управления или содержимое элемента модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-121">Hides all descendant nodes, controls, or content of the UI Automation element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_expand"><strong>ExpandCollapsePattern_Expand</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_expand"><strong>ExpandCollapsePattern_Expand</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-123">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-123">This function is deprecated.</span></span> <span data-ttu-id="85528-124">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-124">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-125">Развертывает элемент управления на экране, чтобы показать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="85528-125">Expands a control on the screen so that it shows more information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-gridpattern_getitem"><strong>GridPattern_GetItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-gridpattern_getitem"><strong>GridPattern_GetItem</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-127">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-127">This function is deprecated.</span></span> <span data-ttu-id="85528-128">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-128">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-129">Возвращает узел для элемента в сетке.</span><span class="sxs-lookup"><span data-stu-id="85528-129">Gets the node for an item in a grid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-invokepattern_invoke"><strong>InvokePattern_Invoke</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-invokepattern_invoke"><strong>InvokePattern_Invoke</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-131">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-131">This function is deprecated.</span></span> <span data-ttu-id="85528-132">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-132">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-133">Направляет запрос на активацию элемента управления и инициирует его единственное, однозначное действие.</span><span class="sxs-lookup"><span data-stu-id="85528-133">Sends a request to activate a control and initiate its single, unambiguous action.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-itemcontainerpattern_finditembyproperty"><strong>ItemContainerPattern_FindItemByProperty</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-itemcontainerpattern_finditembyproperty"><strong>ItemContainerPattern_FindItemByProperty</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-135">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-135">This function is deprecated.</span></span> <span data-ttu-id="85528-136">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-136">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-137">Извлекает узел внутри содержащего узла на основе указанного значения свойства.</span><span class="sxs-lookup"><span data-stu-id="85528-137">Retrieves a node within a containing node, based on a specified property value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-138"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_dodefaultaction"><strong>LegacyIAccessiblePattern_DoDefaultAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-138"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_dodefaultaction"><strong>LegacyIAccessiblePattern_DoDefaultAction</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-139">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-139">This function is deprecated.</span></span> <span data-ttu-id="85528-140">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-140">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-141">Выполняет действие Microsoft Active Accessibility по умолчанию для элемента.</span><span class="sxs-lookup"><span data-stu-id="85528-141">Performs the Microsoft Active Accessibility default action for the element.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-142"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_getiaccessible"><strong>LegacyIAccessiblePattern_GetIAccessible</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-142"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_getiaccessible"><strong>LegacyIAccessiblePattern_GetIAccessible</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-143">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-143">This function is deprecated.</span></span> <span data-ttu-id="85528-144">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-144">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-145">Извлекает объект <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible"><strong>IAccessible</strong></a> , соответствующий элементу модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-145">Retrieves an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible"><strong>IAccessible</strong></a> object that corresponds to the UI Automation element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-146"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_select"><strong>LegacyIAccessiblePattern_Select</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-146"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_select"><strong>LegacyIAccessiblePattern_Select</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-147">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-147">This function is deprecated.</span></span> <span data-ttu-id="85528-148">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-148">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-149">Выполняет выбор Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="85528-149">Performs a Microsoft Active Accessibility selection.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-150"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_setvalue"><strong>LegacyIAccessiblePattern_SetValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-150"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_setvalue"><strong>LegacyIAccessiblePattern_SetValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-151">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-151">This function is deprecated.</span></span> <span data-ttu-id="85528-152">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-152">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-153">Задает свойство Microsoft Active Accessibility Value для узла.</span><span class="sxs-lookup"><span data-stu-id="85528-153">Sets the Microsoft Active Accessibility value property for the node.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-154"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_getviewname"><strong>MultipleViewPattern_GetViewName</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-154"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_getviewname"><strong>MultipleViewPattern_GetViewName</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-155">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-155">This function is deprecated.</span></span> <span data-ttu-id="85528-156">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-156">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-157">Извлекает имя представления для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="85528-157">Retrieves the name of a control-specific view.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-158"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_setcurrentview"><strong>MultipleViewPattern_SetCurrentView</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-158"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_setcurrentview"><strong>MultipleViewPattern_SetCurrentView</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-159">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-159">This function is deprecated.</span></span> <span data-ttu-id="85528-160">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-160">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-161">Задает другой макет элемента управления.</span><span class="sxs-lookup"><span data-stu-id="85528-161">Sets a control to a different layout.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-162"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-rangevaluepattern_setvalue"><strong>RangeValuePattern_SetValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-162"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-rangevaluepattern_setvalue"><strong>RangeValuePattern_SetValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-163">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-163">This function is deprecated.</span></span> <span data-ttu-id="85528-164">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-164">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-165">Задает значение элемента управления с числовым диапазоном.</span><span class="sxs-lookup"><span data-stu-id="85528-165">Sets the value of a control that has a numerical range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-166"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollitempattern_scrollintoview"><strong>ScrollItemPattern_ScrollIntoView</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-166"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollitempattern_scrollintoview"><strong>ScrollItemPattern_ScrollIntoView</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-167">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-167">This function is deprecated.</span></span> <span data-ttu-id="85528-168">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-168">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-169">Прокручивает область содержимого объекта контейнера, чтобы отобразить элемент модели автоматизации пользовательского интерфейса в видимой области (окне просмотра) контейнера.</span><span class="sxs-lookup"><span data-stu-id="85528-169">Scrolls the content area of a container object in order to display the UI Automation element within the visible region (viewport) of the container.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-170"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_scroll"><strong>ScrollPattern_Scroll</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-170"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_scroll"><strong>ScrollPattern_Scroll</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-171">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-171">This function is deprecated.</span></span> <span data-ttu-id="85528-172">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-172">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-173">Прокручивает видимую в данный момент область содержимого на заданный <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount"><strong>скролламаунт</strong></a>, по горизонтали, по вертикали или в обе части.</span><span class="sxs-lookup"><span data-stu-id="85528-173">Scrolls the currently visible region of the content area the specified <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount"><strong>ScrollAmount</strong></a>, horizontally, vertically, or both.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-174"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_setscrollpercent"><strong>ScrollPattern_SetScrollPercent</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-174"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_setscrollpercent"><strong>ScrollPattern_SetScrollPercent</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-175">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-175">This function is deprecated.</span></span> <span data-ttu-id="85528-176">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-176">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-177">Прокручивает контейнер до определенной позицией по горизонтали, вертикали или обоим.</span><span class="sxs-lookup"><span data-stu-id="85528-177">Scrolls a container to a specific position horizontally, vertically, or both.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-178"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_addtoselection"><strong>SelectionItemPattern_AddToSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-178"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_addtoselection"><strong>SelectionItemPattern_AddToSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-179">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-179">This function is deprecated.</span></span> <span data-ttu-id="85528-180">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-180">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-181">Добавляет невыбранный элемент к выделенному элементу в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="85528-181">Adds an unselected element to a selection in a control.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-182"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_removefromselection"><strong>SelectionItemPattern_RemoveFromSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-182"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_removefromselection"><strong>SelectionItemPattern_RemoveFromSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-183">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-183">This function is deprecated.</span></span> <span data-ttu-id="85528-184">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-184">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-185">Удаляет элемент из выделения в контейнере выбора.</span><span class="sxs-lookup"><span data-stu-id="85528-185">Removes an element from the selection in a selection container.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-186"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_select"><strong>SelectionItemPattern_Select</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-186"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_select"><strong>SelectionItemPattern_Select</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-187">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-187">This function is deprecated.</span></span> <span data-ttu-id="85528-188">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-188">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-189">Выбирает элемент в контейнере выбора.</span><span class="sxs-lookup"><span data-stu-id="85528-189">Selects an element in a selection container.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-190"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_cancel"><strong>SynchronizedInputPattern_Cancel</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-190"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_cancel"><strong>SynchronizedInputPattern_Cancel</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-191">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-191">This function is deprecated.</span></span> <span data-ttu-id="85528-192">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-192">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-193">Заставляет поставщик автоматизации пользовательского интерфейса прекращать прослушивание ввода мыши или клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="85528-193">Causes the UI Automation provider to stop listening for mouse or keyboard input.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-194"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_startlistening"><strong>SynchronizedInputPattern_StartListening</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-194"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_startlistening"><strong>SynchronizedInputPattern_StartListening</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-195">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-195">This function is deprecated.</span></span> <span data-ttu-id="85528-196">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-196">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-197">Заставляет поставщик автоматизации пользовательского интерфейса начать прослушивание ввода с клавиатуры или мыши.</span><span class="sxs-lookup"><span data-stu-id="85528-197">Causes the UI Automation provider to start listening for mouse or keyboard input.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-198"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_documentrange"><strong>TextPattern_get_DocumentRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-198"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_documentrange"><strong>TextPattern_get_DocumentRange</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-199">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-199">This function is deprecated.</span></span> <span data-ttu-id="85528-200">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-200">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-201">Возвращает текстовый диапазон для всего документа.</span><span class="sxs-lookup"><span data-stu-id="85528-201">Gets the text range for the entire document.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-202"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_supportedtextselection"><strong>TextPattern_get_SupportedTextSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-202"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_supportedtextselection"><strong>TextPattern_get_SupportedTextSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-203">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-203">This function is deprecated.</span></span> <span data-ttu-id="85528-204">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-204">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-205">Определяет, можно ли выбрать содержимое текстового контейнера и отменить его выбор.</span><span class="sxs-lookup"><span data-stu-id="85528-205">Ascertains whether the text container's contents can be selected and deselected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-206"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getselection"><strong>TextPattern_GetSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-206"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getselection"><strong>TextPattern_GetSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-207">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-207">This function is deprecated.</span></span> <span data-ttu-id="85528-208">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-208">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-209">Возвращает текущий диапазон выбранного текста из текстового контейнера, поддерживающего текстовый шаблон.</span><span class="sxs-lookup"><span data-stu-id="85528-209">Gets the current range of selected text from a text container supporting the text pattern.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-210"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getvisibleranges"><strong>TextPattern_GetVisibleRanges</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-210"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getvisibleranges"><strong>TextPattern_GetVisibleRanges</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-211">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-211">This function is deprecated.</span></span> <span data-ttu-id="85528-212">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-212">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-213">Возвращает массив раздельных текстовых диапазонов из текстового контейнера, где каждый диапазон начинается с первой частично видимой строки и оканчивается последней частично видимой строкой.</span><span class="sxs-lookup"><span data-stu-id="85528-213">Retrieves an array of disjoint text ranges from a text container where each text range begins with the first partially visible line through to the end of the last partially visible line.</span></span> <span data-ttu-id="85528-214">Например, макет с несколькими столбцами, в котором столбцы частично прокручивается из видимой области окна просмотра, и содержимое перемещается от нижнего края одного столбца к другому.</span><span class="sxs-lookup"><span data-stu-id="85528-214">For example, a multi-column layout where the columns are partially scrolled out of the visible area of the viewport and the content flows from the bottom of one column to the top of the next.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefromchild"><strong>TextPattern_RangeFromChild</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefromchild"><strong>TextPattern_RangeFromChild</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-216">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-216">This function is deprecated.</span></span> <span data-ttu-id="85528-217">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-217">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-218">Возвращает текстовый диапазон, охватываемый данным узлом.</span><span class="sxs-lookup"><span data-stu-id="85528-218">Gets the text range that a given node spans.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefrompoint"><strong>TextPattern_RangeFromPoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefrompoint"><strong>TextPattern_RangeFromPoint</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-220">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-220">This function is deprecated.</span></span> <span data-ttu-id="85528-221">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-221">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-222">Извлекает вырожденный (пустой) текстовый диапазон, ближайший к указанным экранным координатам.</span><span class="sxs-lookup"><span data-stu-id="85528-222">Retrieves the degenerate (empty) text range nearest to the specified screen coordinates.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_addtoselection"><strong>TextRange_AddToSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_addtoselection"><strong>TextRange_AddToSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-224">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-224">This function is deprecated.</span></span> <span data-ttu-id="85528-225">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-225">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-226">Добавляет к существующей коллекции выделенного текста в текстовом контейнере, который поддерживает несколько несвязных выделений, выделяя дополнительный текст, соответствующий <em>начальным</em> и <em>конечным</em> конечным точкам текстового диапазона.</span><span class="sxs-lookup"><span data-stu-id="85528-226">Adds to the existing collection of highlighted text in a text container that supports multiple, disjoint selections by highlighting supplementary text corresponding to the calling text range <em>Start</em> and <em>End</em> endpoints.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_clone"><strong>TextRange_Clone</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_clone"><strong>TextRange_Clone</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-228">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-228">This function is deprecated.</span></span> <span data-ttu-id="85528-229">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-229">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-230">Копирует текстовый диапазон.</span><span class="sxs-lookup"><span data-stu-id="85528-230">Copies a text range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-231"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compare"><strong>TextRange_Compare</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-231"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compare"><strong>TextRange_Compare</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-232">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-232">This function is deprecated.</span></span> <span data-ttu-id="85528-233">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-233">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-234">Сравнивает два текстовых диапазона.</span><span class="sxs-lookup"><span data-stu-id="85528-234">Compares two text ranges.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-235"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compareendpoints"><strong>TextRange_CompareEndpoints</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-235"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compareendpoints"><strong>TextRange_CompareEndpoints</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-236">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-236">This function is deprecated.</span></span> <span data-ttu-id="85528-237">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-237">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-238">Возвращает значение, указывающее, имеют ли два текстовых диапазона одинаковые конечные точки.</span><span class="sxs-lookup"><span data-stu-id="85528-238">Returns a value indicating whether two text ranges have identical endpoints.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-239"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_expandtoenclosingunit"><strong>TextRange_ExpandToEnclosingUnit</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-239"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_expandtoenclosingunit"><strong>TextRange_ExpandToEnclosingUnit</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-240">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-240">This function is deprecated.</span></span> <span data-ttu-id="85528-241">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-241">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-242">Расширяет текстовый диапазон до более крупной или меньшей единицы, такой как символ, слово, строка или страница.</span><span class="sxs-lookup"><span data-stu-id="85528-242">Expands the text range to a larger or smaller unit such as Character, Word, Line, or Page.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-243"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findattribute"><strong>TextRange_FindAttribute</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-243"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findattribute"><strong>TextRange_FindAttribute</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-244">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-244">This function is deprecated.</span></span> <span data-ttu-id="85528-245">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-245">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-246">Выполняет поиск первого фрагмента текста, поддерживающего указанный текстовый атрибут, в указанном направлении.</span><span class="sxs-lookup"><span data-stu-id="85528-246">Searches in a specified direction for the first piece of text supporting a specified text attribute.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-247"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findtext"><strong>TextRange_FindText</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-247"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findtext"><strong>TextRange_FindText</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-248">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-248">This function is deprecated.</span></span> <span data-ttu-id="85528-249">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-249">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-250">Возвращает первый текстовый диапазон в указанном направлении, который содержит текст, который ищет клиент.</span><span class="sxs-lookup"><span data-stu-id="85528-250">Returns the first text range in the specified direction that contains the text the client is searching for.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-251"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getattributevalue"><strong>TextRange_GetAttributeValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-251"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getattributevalue"><strong>TextRange_GetAttributeValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-252">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-252">This function is deprecated.</span></span> <span data-ttu-id="85528-253">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-253">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-254">Возвращает значение текстового атрибута для текстового диапазона.</span><span class="sxs-lookup"><span data-stu-id="85528-254">Gets the value of an text attribute for a text range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-255"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getboundingrectangles"><strong>TextRange_GetBoundingRectangles</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-255"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getboundingrectangles"><strong>TextRange_GetBoundingRectangles</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-256">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-256">This function is deprecated.</span></span> <span data-ttu-id="85528-257">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-257">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-258">Возвращает минимальное число ограничивающих прямоугольников, которые могут заключаться в диапазон, по одному прямоугольнику на строку.</span><span class="sxs-lookup"><span data-stu-id="85528-258">Retrieves the minimum number of bounding rectangles that can enclose the range, one rectangle per line.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-259"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getchildren"><strong>TextRange_GetChildren</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-259"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getchildren"><strong>TextRange_GetChildren</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-260">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-260">This function is deprecated.</span></span> <span data-ttu-id="85528-261">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-261">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-262">Возвращает все элементы модели автоматизации пользовательского интерфейса, содержащиеся в указанном текстовом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="85528-262">Returns all UI Automation elements contained within the specified text range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-263"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getenclosingelement"><strong>TextRange_GetEnclosingElement</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-263"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getenclosingelement"><strong>TextRange_GetEnclosingElement</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-264">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-264">This function is deprecated.</span></span> <span data-ttu-id="85528-265">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-265">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-266">Возвращает узел для следующего наименьшего поставщика, охватывающего диапазон.</span><span class="sxs-lookup"><span data-stu-id="85528-266">Returns the node for the next smallest provider that covers the range.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-267"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_gettext"><strong>TextRange_GetText</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-267"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_gettext"><strong>TextRange_GetText</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-268">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-268">This function is deprecated.</span></span> <span data-ttu-id="85528-269">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-269">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-270">Возвращает текст в текстовом диапазоне до указанного числа символов.</span><span class="sxs-lookup"><span data-stu-id="85528-270">Returns the text in a text range, up to a specified number of characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-271"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_move"><strong>TextRange_Move</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-271"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_move"><strong>TextRange_Move</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-272">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-272">This function is deprecated.</span></span> <span data-ttu-id="85528-273">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-273">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-274">Перемещает текстовый диапазон на указанное число единиц, запрошенное клиентом.</span><span class="sxs-lookup"><span data-stu-id="85528-274">Moves the text range the specified number of units requested by the client.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-275"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyrange"><strong>TextRange_MoveEndpointByRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-275"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyrange"><strong>TextRange_MoveEndpointByRange</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-276">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-276">This function is deprecated.</span></span> <span data-ttu-id="85528-277">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-277">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-278">Перемещает конечную точку одного диапазона в конечную точку другого диапазона.</span><span class="sxs-lookup"><span data-stu-id="85528-278">Moves an endpoint of one range to the endpoint of another range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-279"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyunit"><strong>TextRange_MoveEndpointByUnit</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-279"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyunit"><strong>TextRange_MoveEndpointByUnit</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-280">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-280">This function is deprecated.</span></span> <span data-ttu-id="85528-281">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-281">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-282">Перемещает конечную точку в диапазоне на указанное число единиц.</span><span class="sxs-lookup"><span data-stu-id="85528-282">Moves an endpoint of the range the specified number of units.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-283"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_removefromselection"><strong>TextRange_RemoveFromSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-283"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_removefromselection"><strong>TextRange_RemoveFromSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-284">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-284">This function is deprecated.</span></span> <span data-ttu-id="85528-285">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-285">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-286">Удаляет выделенный текст, соответствующий вызывающему текстовому диапазону <em>TextPatternRangeEndpoint_Start</em> и <em>TextPatternRangeEndpoint_End</em> конечные точки из существующей коллекции выделенного текста в текстовом контейнере, поддерживающем несколько несвязных выделений.</span><span class="sxs-lookup"><span data-stu-id="85528-286">Removes the selected text, corresponding to the calling text range <em>TextPatternRangeEndpoint_Start</em> and <em>TextPatternRangeEndpoint_End</em> endpoints, from an existing collection of selected text in a text container that supports multiple, disjoint selections.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-287"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_scrollintoview"><strong>TextRange_ScrollIntoView</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-287"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_scrollintoview"><strong>TextRange_ScrollIntoView</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-288">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-288">This function is deprecated.</span></span> <span data-ttu-id="85528-289">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-289">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-290">Прокручивает текст таким образом, чтобы указанный диапазон был виден в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="85528-290">Scrolls the text so the specified range is visible in the viewport.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-291"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_select"><strong>TextRange_Select</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-291"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_select"><strong>TextRange_Select</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-292">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-292">This function is deprecated.</span></span> <span data-ttu-id="85528-293">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-293">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-294">Выбирает текстовый диапазон.</span><span class="sxs-lookup"><span data-stu-id="85528-294">Selects a text range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-295"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-togglepattern_toggle"><strong>TogglePattern_Toggle</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-295"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-togglepattern_toggle"><strong>TogglePattern_Toggle</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-296">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-296">This function is deprecated.</span></span> <span data-ttu-id="85528-297">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-297">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-298">Переключает элемент управления в следующее поддерживаемое состояние.</span><span class="sxs-lookup"><span data-stu-id="85528-298">Toggles a control to its next supported state.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-299"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_move"><strong>TransformPattern_Move</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-299"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_move"><strong>TransformPattern_Move</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-300">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-300">This function is deprecated.</span></span> <span data-ttu-id="85528-301">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-301">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-302">Перемещает элемент в указанное место на экране.</span><span class="sxs-lookup"><span data-stu-id="85528-302">Moves an element to a specified location on the screen.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-303"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_resize"><strong>TransformPattern_Resize</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-303"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_resize"><strong>TransformPattern_Resize</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-304">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-304">This function is deprecated.</span></span> <span data-ttu-id="85528-305">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-305">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-306">Изменяет размер элемента на экране.</span><span class="sxs-lookup"><span data-stu-id="85528-306">Resizes an element on the screen.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-307"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_rotate"><strong>TransformPattern_Rotate</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-307"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_rotate"><strong>TransformPattern_Rotate</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-308">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-308">This function is deprecated.</span></span> <span data-ttu-id="85528-309">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-309">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-310">Поворачивает элемент на экране.</span><span class="sxs-lookup"><span data-stu-id="85528-310">Rotates an element on the screen.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-311"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-valuepattern_setvalue"><strong>ValuePattern_SetValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-311"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-valuepattern_setvalue"><strong>ValuePattern_SetValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-312">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-312">This function is deprecated.</span></span> <span data-ttu-id="85528-313">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-313">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-314">Задает текстовое значение элемента.</span><span class="sxs-lookup"><span data-stu-id="85528-314">Sets the text value of an element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-315"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-virtualizeditempattern_realize"><strong>VirtualizedItemPattern_Realize</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-315"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-virtualizeditempattern_realize"><strong>VirtualizedItemPattern_Realize</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-316">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-316">This function is deprecated.</span></span> <span data-ttu-id="85528-317">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-317">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-318">Делает виртуальный элемент полностью доступным как элемент модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-318">Makes the virtual item fully accessible as a UI Automation element.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-319"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_close"><strong>WindowPattern_Close</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-319"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_close"><strong>WindowPattern_Close</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-320">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-320">This function is deprecated.</span></span> <span data-ttu-id="85528-321">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-321">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-322">Закрывает открытое окно.</span><span class="sxs-lookup"><span data-stu-id="85528-322">Closes an open window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85528-323"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_setwindowvisualstate"><strong>WindowPattern_SetWindowVisualState</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-323"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_setwindowvisualstate"><strong>WindowPattern_SetWindowVisualState</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-324">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-324">This function is deprecated.</span></span> <span data-ttu-id="85528-325">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-325">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-326">Задает визуальное состояние окна; Например, чтобы развернуть окно.</span><span class="sxs-lookup"><span data-stu-id="85528-326">Sets the visual state of a window; for example, to maximize a window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85528-327"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_waitforinputidle"><strong>WindowPattern_WaitForInputIdle</strong></a></span><span class="sxs-lookup"><span data-stu-id="85528-327"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_waitforinputidle"><strong>WindowPattern_WaitForInputIdle</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="85528-328">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="85528-328">This function is deprecated.</span></span> <span data-ttu-id="85528-329">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85528-329">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="85528-330">Блокирует вызывающий код в течение заданного промежутка времени или до того момента, как связанный процесс перейдет в состояние бездействия, в зависимости от того, что произойдет раньше.</span><span class="sxs-lookup"><span data-stu-id="85528-330">Causes the calling code to block for the specified time or until the associated process enters an idle state, whichever completes first.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="85528-331">См. также</span><span class="sxs-lookup"><span data-stu-id="85528-331">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85528-332">Клиенты автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="85528-332">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





