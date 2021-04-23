---
title: Кнопка Drop-Down
description: Кнопка Drop-Down состоит из кнопки, при нажатии на которой отображается раскрывающийся список взаимоисключающих элементов.
ms.assetid: 41c5da07-43f7-4544-83be-248941cb8633
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87e6a776dd705fe503e5e93ec601baf6cc2b3cf
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104339468"
---
# <a name="drop-down-button"></a><span data-ttu-id="a8139-103">Кнопка Drop-Down</span><span class="sxs-lookup"><span data-stu-id="a8139-103">Drop-Down Button</span></span>

<span data-ttu-id="a8139-104">Кнопка Drop-Down состоит из кнопки, при нажатии на которой отображается раскрывающийся список взаимоисключающих элементов.</span><span class="sxs-lookup"><span data-stu-id="a8139-104">The Drop-Down Button consists of a button that when clicked displays a drop-down list of mutually exclusive items.</span></span>

-   [<span data-ttu-id="a8139-105">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="a8139-105">Details</span></span>](#details)
-   [<span data-ttu-id="a8139-106">Свойства кнопки раскрывающегося списка</span><span class="sxs-lookup"><span data-stu-id="a8139-106">Drop-Down Button Properties</span></span>](#drop-down-button-properties)
-   [<span data-ttu-id="a8139-107">См. также</span><span class="sxs-lookup"><span data-stu-id="a8139-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="a8139-108">Сведения</span><span class="sxs-lookup"><span data-stu-id="a8139-108">Details</span></span>

<span data-ttu-id="a8139-109">Этот элемент управления полезен для предоставления тесно связанных элементов в случаях, когда очевидное значение по умолчанию недоступно и когда отдельные элементы могут быть представлены изображением, текстом или обоими.</span><span class="sxs-lookup"><span data-stu-id="a8139-109">This control is useful for exposing closely related items in cases where no obvious default is available and where the individual items can be represented by an image, text, or both.</span></span>

<span data-ttu-id="a8139-110">На следующем снимке экрана показана кнопка Drop-Down ленты в образце ленты.</span><span class="sxs-lookup"><span data-stu-id="a8139-110">The following screen shot illustrates the Ribbon Drop-Down Button in a sample Ribbon.</span></span>

![снимок экрана элемента управления DropDownButton в образце ленты.](images/controls/dropdownbutton.png)

## <a name="drop-down-button-properties"></a><span data-ttu-id="a8139-112">Свойства кнопки Drop-Down</span><span class="sxs-lookup"><span data-stu-id="a8139-112">Drop-Down Button Properties</span></span>

<span data-ttu-id="a8139-113">Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления "кнопка" Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="a8139-113">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Drop-Down Button control.</span></span>

<span data-ttu-id="a8139-114">Как правило, свойство кнопки Drop-Down обновляется в пользовательском интерфейсе Ribbon путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="a8139-114">Typically, a Drop-Down Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="a8139-115">Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="a8139-115">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="a8139-116">Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы.</span><span class="sxs-lookup"><span data-stu-id="a8139-116">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="a8139-117">Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.</span><span class="sxs-lookup"><span data-stu-id="a8139-117">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="a8139-118">В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="a8139-118">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="a8139-119">В следующей таблице перечислены ключи свойств, связанные с элементом управления "кнопка Drop-Down".</span><span class="sxs-lookup"><span data-stu-id="a8139-119">The following table lists the property keys that are associated with the Drop-Down Button control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a8139-120">Ключ свойства</span><span class="sxs-lookup"><span data-stu-id="a8139-120">Property Key</span></span></th>
<th><span data-ttu-id="a8139-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="a8139-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a8139-122"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span><span class="sxs-lookup"><span data-stu-id="a8139-122"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span></span></td>
<td><span data-ttu-id="a8139-123">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a8139-123">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8139-124"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="a8139-124"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="a8139-125">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a8139-125">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span><br/> <span data-ttu-id="a8139-126">Если все дочерние элементы отключены, платформа устанавливает для <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> значение false (0).</span><span class="sxs-lookup"><span data-stu-id="a8139-126">If all child items are disabled, the framework sets <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> to false (0).</span></span> <span data-ttu-id="a8139-127">В противном случае, если один или несколько дочерних элементов включены, UI_PKEY_Enabled имеет значение true (-1).</span><span class="sxs-lookup"><span data-stu-id="a8139-127">Otherwise, if one or more child items are enabled, UI_PKEY_Enabled is set to true (-1).</span></span>
<blockquote>
[!Important]<br />
<span data-ttu-id="a8139-128">Свойство <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> элемента управления "кнопка Drop-Down" должно быть недействительным после включения или отключения одного или нескольких дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="a8139-128">The <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> property for the Drop-Down Button control should be invalidated after one or more child items are enabled or disabled.</span></span> <span data-ttu-id="a8139-129">Это гарантирует, что платформа запрашивает обновленное значение свойства и обновляет состояние элемента управления кнопки Drop-Down в пользовательском интерфейсе ленты.</span><span class="sxs-lookup"><span data-stu-id="a8139-129">This ensures that the framework queries the updated property value and refreshes the state of the Drop-Down Button control in the ribbon UI.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a8139-130"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span><span class="sxs-lookup"><span data-stu-id="a8139-130"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span></span></td>
<td><span data-ttu-id="a8139-131">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a8139-131">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8139-132"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="a8139-132"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="a8139-133">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="a8139-133">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a8139-134"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="a8139-134"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="a8139-135">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="a8139-135">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8139-136"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="a8139-136"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="a8139-137">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="a8139-137">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a8139-138"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="a8139-138"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="a8139-139">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="a8139-139">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8139-140"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a></span><span class="sxs-lookup"><span data-stu-id="a8139-140"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a></span></span></td>
<td><span data-ttu-id="a8139-141">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a8139-141">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="a8139-142">Если команда, связанная с элементом управления, становится недействительной при вызове <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>иуифрамеворк:: инвалидатеуикомманд</strong></a>, платформа запрашивает это свойство, когда в <code>UI_INVALIDATIONS_VALUE</code> качестве значения <em>флагов</em>передается.</span><span class="sxs-lookup"><span data-stu-id="a8139-142">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a8139-143"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="a8139-143"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="a8139-144">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="a8139-144">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8139-145"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="a8139-145"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="a8139-146">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="a8139-146">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a8139-147"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="a8139-147"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="a8139-148">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="a8139-148">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8139-149"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="a8139-149"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="a8139-150">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="a8139-150">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="a8139-151">См. также</span><span class="sxs-lookup"><span data-stu-id="a8139-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8139-152">Библиотека элементов управления платформы Windows ленты</span><span class="sxs-lookup"><span data-stu-id="a8139-152">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="a8139-153">**DropDownButton, элемент разметки**</span><span class="sxs-lookup"><span data-stu-id="a8139-153">**DropDownButton markup element**</span></span>](windowsribbon-element-dropdownbutton.md)
</dt> </dl>