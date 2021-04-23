---
title: Поле со списком (платформа Windows для ленты)
description: Поле со списком состоит из списка с одним столбцом, в котором содержится коллекция взаимоисключающих элементов или команд, Объединенных с помощью элемента управления static или Edit и раскрывающейся стрелкой.
ms.assetid: 6b7de2ec-dcb7-44cb-b01f-db1ba0643499
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c61c19963811d12557beafe3c5cff314c927ae7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488742"
---
# <a name="combo-box-windows-ribbon-framework"></a><span data-ttu-id="d7919-103">Поле со списком (платформа Windows для ленты)</span><span class="sxs-lookup"><span data-stu-id="d7919-103">Combo Box (Windows Ribbon Framework)</span></span>

<span data-ttu-id="d7919-104">Поле со списком состоит из списка с одним столбцом, в котором содержится коллекция взаимоисключающих элементов или команд, Объединенных с помощью элемента управления static или Edit и раскрывающейся стрелкой.</span><span class="sxs-lookup"><span data-stu-id="d7919-104">The Combo Box consists of a single-column list box that contains a collection of mutually exclusive items or Commands combined with a static or edit control and a drop-down arrow.</span></span> <span data-ttu-id="d7919-105">Часть элемента управления отображается в списке, когда пользователь щелкает стрелку раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="d7919-105">The list box portion of the control is displayed when the user clicks the drop-down arrow.</span></span>

-   [<span data-ttu-id="d7919-106">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="d7919-106">Details</span></span>](#details)
-   [<span data-ttu-id="d7919-107">Свойства поля со списком</span><span class="sxs-lookup"><span data-stu-id="d7919-107">Combo Box Properties</span></span>](#combo-box-properties)
-   [<span data-ttu-id="d7919-108">См. также</span><span class="sxs-lookup"><span data-stu-id="d7919-108">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="d7919-109">Сведения</span><span class="sxs-lookup"><span data-stu-id="d7919-109">Details</span></span>

<span data-ttu-id="d7919-110">Выбранный в данный момент элемент или команда (если есть) в списке отображается в статическом или в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="d7919-110">The currently selected item or Command (if any) in the list box is displayed in the static or edit control.</span></span> <span data-ttu-id="d7919-111">Если в элементе управления "поле ввода" введены начальные символы существующего элемента или команды, в списке будет выделен первый элемент с этими начальными символами и Автозаполнение записи в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="d7919-111">With an edit control, if the user types the initial characters of an existing item or Command, the list box will highlight the first item with those initial characters and autocomplete the entry in the edit control.</span></span>

<span data-ttu-id="d7919-112">Поддерживает вертикальную полосу захвата или только маркер изменения размера.</span><span class="sxs-lookup"><span data-stu-id="d7919-112">Supports a vertical gripper bar, or resizing handle, only.</span></span>

<span data-ttu-id="d7919-113">Этот элемент управления полезен для предоставления простых тесно связанных текстовых элементов.</span><span class="sxs-lookup"><span data-stu-id="d7919-113">This control is useful for exposing simple, closely related text items.</span></span>

<span data-ttu-id="d7919-114">На следующем снимке экрана показано поле со списком ленты в Live Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="d7919-114">The following screen shot illustrates the Ribbon Combo Box in Live Movie Maker.</span></span>

![снимок экрана элемента управления ComboBox на ленте Microsoft Paint.](images/controls/combobox.png)

## <a name="combo-box-properties"></a><span data-ttu-id="d7919-116">Свойства поля со списком</span><span class="sxs-lookup"><span data-stu-id="d7919-116">Combo Box Properties</span></span>

<span data-ttu-id="d7919-117">Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления "поле со списком".</span><span class="sxs-lookup"><span data-stu-id="d7919-117">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Combo Box control.</span></span>

<span data-ttu-id="d7919-118">Как правило, свойство поля со списком обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="d7919-118">Typically, a Combo Box property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="d7919-119">Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="d7919-119">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="d7919-120">Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы.</span><span class="sxs-lookup"><span data-stu-id="d7919-120">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="d7919-121">Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.</span><span class="sxs-lookup"><span data-stu-id="d7919-121">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="d7919-122">В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="d7919-122">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="d7919-123">В следующей таблице перечислены ключи свойств, связанные с элементом управления "поле со списком".</span><span class="sxs-lookup"><span data-stu-id="d7919-123">The following table lists the property keys that are associated with the Combo Box control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7919-124">Ключ свойства</span><span class="sxs-lookup"><span data-stu-id="d7919-124">Property Key</span></span></th>
<th><span data-ttu-id="d7919-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="d7919-125">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d7919-126"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span><span class="sxs-lookup"><span data-stu-id="d7919-126"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span></span></td>
<td><span data-ttu-id="d7919-127">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d7919-127">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7919-128"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="d7919-128"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="d7919-129">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d7919-129">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7919-130"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span><span class="sxs-lookup"><span data-stu-id="d7919-130"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span></span></td>
<td><span data-ttu-id="d7919-131">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d7919-131">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7919-132"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="d7919-132"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="d7919-133">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="d7919-133">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7919-134"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="d7919-134"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="d7919-135">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="d7919-135">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7919-136"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="d7919-136"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="d7919-137">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="d7919-137">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7919-138"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="d7919-138"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="d7919-139">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="d7919-139">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7919-140"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a></span><span class="sxs-lookup"><span data-stu-id="d7919-140"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a></span></span></td>
<td><span data-ttu-id="d7919-141">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d7919-141">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7919-142"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="d7919-142"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="d7919-143">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="d7919-143">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7919-144"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="d7919-144"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="d7919-145">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="d7919-145">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7919-146"><a href="windowsribbon-reference-properties-uipkey-stringvalue.md">UI_PKEY_StringValue</a></span><span class="sxs-lookup"><span data-stu-id="d7919-146"><a href="windowsribbon-reference-properties-uipkey-stringvalue.md">UI_PKEY_StringValue</a></span></span></td>
<td><span data-ttu-id="d7919-147">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d7919-147">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="d7919-148">Если команда, связанная с элементом управления, становится недействительной при вызове <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>иуифрамеворк:: инвалидатеуикомманд</strong></a>, платформа запрашивает это свойство, когда в <code>UI_INVALIDATIONS_VALUE</code> качестве значения <em>флагов</em>передается.</span><span class="sxs-lookup"><span data-stu-id="d7919-148">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7919-149"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="d7919-149"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="d7919-150">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="d7919-150">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7919-151"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="d7919-151"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="d7919-152">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="d7919-152">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="d7919-153">См. также</span><span class="sxs-lookup"><span data-stu-id="d7919-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7919-154">Библиотека элементов управления платформы Windows ленты</span><span class="sxs-lookup"><span data-stu-id="d7919-154">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="d7919-155">**Элемент разметки ComboBox**</span><span class="sxs-lookup"><span data-stu-id="d7919-155">**ComboBox markup element**</span></span>](windowsribbon-element-combobox.md)
</dt> <dt>

[<span data-ttu-id="d7919-156">Работа с коллекциями</span><span class="sxs-lookup"><span data-stu-id="d7919-156">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="d7919-157">Пример коллекции</span><span class="sxs-lookup"><span data-stu-id="d7919-157">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

