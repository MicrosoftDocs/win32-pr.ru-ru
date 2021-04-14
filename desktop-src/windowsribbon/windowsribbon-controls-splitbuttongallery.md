---
title: Коллекция разделенных кнопок
description: Коллекция разворачивающихся кнопок — это составной элемент управления, который содержит основную кнопку, предоставляющую один элемент или команду по умолчанию, и вспомогательную кнопку, которая при нажатии отображает остальную часть элемента или коллекции команд в взаимно исключающем раскрывающемся списке.
ms.assetid: c0fcfe72-d2e9-465d-941a-b3832b36b8c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1865949c1b6f3e274b01d0b4e454dc42e619c2c0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104413928"
---
# <a name="split-button-gallery"></a><span data-ttu-id="c0f00-103">Коллекция разделенных кнопок</span><span class="sxs-lookup"><span data-stu-id="c0f00-103">Split Button Gallery</span></span>

<span data-ttu-id="c0f00-104">Коллекция разворачивающихся кнопок — это составной элемент управления, который содержит основную кнопку, предоставляющую один элемент или команду по умолчанию, и вспомогательную кнопку, которая при нажатии отображает остальную часть элемента или коллекции команд в взаимно исключающем раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="c0f00-104">The Split Button Gallery is a composite control that contains a primary button which exposes a single default item or Command, and a secondary button which when clicked displays the rest of the item or Command collection in a mutually exclusive drop-down list.</span></span>

-   [<span data-ttu-id="c0f00-105">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="c0f00-105">Details</span></span>](#details)
-   [<span data-ttu-id="c0f00-106">Свойства коллекции разделенных кнопок</span><span class="sxs-lookup"><span data-stu-id="c0f00-106">Split Button Gallery Properties</span></span>](#split-button-gallery-properties)
-   [<span data-ttu-id="c0f00-107">См. также</span><span class="sxs-lookup"><span data-stu-id="c0f00-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="c0f00-108">Сведения</span><span class="sxs-lookup"><span data-stu-id="c0f00-108">Details</span></span>

<span data-ttu-id="c0f00-109">Этот элемент управления полезен для предоставления тесно связанных элементов в случаях, когда доступно очевидное по умолчанию, а отдельные элементы могут быть представлены изображением, текстом или обоими.</span><span class="sxs-lookup"><span data-stu-id="c0f00-109">This control is useful for exposing closely related items in cases where an obvious default is available and where the individual items can be represented by an image, text, or both.</span></span>

<span data-ttu-id="c0f00-110">На следующем снимке экрана показана коллекция кнопок разделения ленты в Microsoft Paint.</span><span class="sxs-lookup"><span data-stu-id="c0f00-110">The following screen shot illustrates the Ribbon Split Button Gallery in Microsoft Paint.</span></span>

![снимок экрана элемента управления сплитбуттонгаллери на ленте Microsoft Paint.](images/controls/splitbuttongallery.png)

## <a name="split-button-gallery-properties"></a><span data-ttu-id="c0f00-112">Свойства коллекции разделенных кнопок</span><span class="sxs-lookup"><span data-stu-id="c0f00-112">Split Button Gallery Properties</span></span>

<span data-ttu-id="c0f00-113">Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления коллекции разворачивающихся кнопок.</span><span class="sxs-lookup"><span data-stu-id="c0f00-113">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Split Button Gallery control.</span></span>

<span data-ttu-id="c0f00-114">Как правило, свойство коллекции разделенных кнопок обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="c0f00-114">Typically, a Split Button Gallery property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="c0f00-115">Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="c0f00-115">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="c0f00-116">Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы.</span><span class="sxs-lookup"><span data-stu-id="c0f00-116">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="c0f00-117">Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.</span><span class="sxs-lookup"><span data-stu-id="c0f00-117">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="c0f00-118">В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="c0f00-118">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="c0f00-119">В следующей таблице перечислены ключи свойств, связанные с элементом управления коллекции "разворачивающаяся кнопка".</span><span class="sxs-lookup"><span data-stu-id="c0f00-119">The following table lists the property keys that are associated with the Split Button Gallery control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0f00-120">Ключ свойства</span><span class="sxs-lookup"><span data-stu-id="c0f00-120">Property Key</span></span></th>
<th><span data-ttu-id="c0f00-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="c0f00-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0f00-122"><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></span><span class="sxs-lookup"><span data-stu-id="c0f00-122"><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></span></span></td>
<td><span data-ttu-id="c0f00-123">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c0f00-123">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0f00-124"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span><span class="sxs-lookup"><span data-stu-id="c0f00-124"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span></span></td>
<td><span data-ttu-id="c0f00-125">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c0f00-125">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0f00-126"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="c0f00-126"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="c0f00-127">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c0f00-127">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0f00-128"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span><span class="sxs-lookup"><span data-stu-id="c0f00-128"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span></span></td>
<td><span data-ttu-id="c0f00-129">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c0f00-129">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0f00-130"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="c0f00-130"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="c0f00-131">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="c0f00-131">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0f00-132"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="c0f00-132"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="c0f00-133">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="c0f00-133">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0f00-134"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="c0f00-134"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="c0f00-135">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="c0f00-135">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0f00-136"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="c0f00-136"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="c0f00-137">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="c0f00-137">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0f00-138"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(допустимо только для коллекции элементов)</span><span class="sxs-lookup"><span data-stu-id="c0f00-138"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(only valid for an item gallery)</span></span><br/></td>
<td><span data-ttu-id="c0f00-139">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c0f00-139">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c0f00-140">Если команда, связанная с элементом управления, становится недействительной при вызове <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>иуифрамеворк:: инвалидатеуикомманд</strong></a>, платформа запрашивает это свойство, когда в <code>UI_INVALIDATIONS_VALUE</code> качестве значения <em>флагов</em>передается.</span><span class="sxs-lookup"><span data-stu-id="c0f00-140">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0f00-141"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="c0f00-141"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="c0f00-142">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="c0f00-142">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0f00-143"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="c0f00-143"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="c0f00-144">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="c0f00-144">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0f00-145"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="c0f00-145"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="c0f00-146">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="c0f00-146">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0f00-147"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="c0f00-147"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="c0f00-148">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="c0f00-148">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="c0f00-149">См. также</span><span class="sxs-lookup"><span data-stu-id="c0f00-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0f00-150">**Сплитбуттонгаллери, элемент разметки**</span><span class="sxs-lookup"><span data-stu-id="c0f00-150">**SplitButtonGallery markup element**</span></span>](windowsribbon-element-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="c0f00-151">Работа с коллекциями</span><span class="sxs-lookup"><span data-stu-id="c0f00-151">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="c0f00-152">Пример коллекции</span><span class="sxs-lookup"><span data-stu-id="c0f00-152">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

