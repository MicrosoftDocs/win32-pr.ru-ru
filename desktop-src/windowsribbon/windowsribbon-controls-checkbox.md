---
title: Флажок
description: Флажок — это элемент управления, который пользователь может щелкнуть, чтобы предоставить входные данные приложению. Элемент управления предоставляет состояние переключения, которое представлено визуально.
ms.assetid: fe07aa5c-1818-41e2-b48d-5fefe50d733f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e283facf81e8c3d2adad670329fcf0cf168d09
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "103795720"
---
# <a name="check-box"></a><span data-ttu-id="39905-104">Флажок</span><span class="sxs-lookup"><span data-stu-id="39905-104">Check Box</span></span>

<span data-ttu-id="39905-105">Флажок — это элемент управления, который пользователь может щелкнуть, чтобы предоставить входные данные приложению.</span><span class="sxs-lookup"><span data-stu-id="39905-105">The Check Box is a control the user can click to provide input to an application.</span></span> <span data-ttu-id="39905-106">Элемент управления предоставляет состояние переключения, которое представлено визуально.</span><span class="sxs-lookup"><span data-stu-id="39905-106">The control provides a toggle state that is represented visually.</span></span>

-   [<span data-ttu-id="39905-107">Сведения</span><span class="sxs-lookup"><span data-stu-id="39905-107">Details</span></span>](#details)
-   [<span data-ttu-id="39905-108">Свойства флажка</span><span class="sxs-lookup"><span data-stu-id="39905-108">Check Box Properties</span></span>](#check-box-properties)
-   [<span data-ttu-id="39905-109">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="39905-109">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="39905-110">Сведения</span><span class="sxs-lookup"><span data-stu-id="39905-110">Details</span></span>

<span data-ttu-id="39905-111">Флажок не поддерживает третичное, или неопределенное состояние.</span><span class="sxs-lookup"><span data-stu-id="39905-111">The Check Box does not support a tertiary, or indeterminate, state.</span></span>

<span data-ttu-id="39905-112">На следующем снимке экрана показан элемент флажка ленты.</span><span class="sxs-lookup"><span data-stu-id="39905-112">The following screen shot illustrates the Ribbon Check Box element.</span></span>

![снимок экрана элемента управления CheckBox на ленте Microsoft Paint.](images/controls/checkbox.png)

## <a name="check-box-properties"></a><span data-ttu-id="39905-114">Свойства флажка</span><span class="sxs-lookup"><span data-stu-id="39905-114">Check Box Properties</span></span>

<span data-ttu-id="39905-115">Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления "флажок".</span><span class="sxs-lookup"><span data-stu-id="39905-115">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Check Box control.</span></span>

<span data-ttu-id="39905-116">Как правило, свойство флажка обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="39905-116">Typically, a Check Box property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="39905-117">Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="39905-117">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="39905-118">Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы.</span><span class="sxs-lookup"><span data-stu-id="39905-118">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="39905-119">Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.</span><span class="sxs-lookup"><span data-stu-id="39905-119">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="39905-120">В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="39905-120">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="39905-121">В следующей таблице перечислены ключи свойств, связанные с элементом управления "флажок".</span><span class="sxs-lookup"><span data-stu-id="39905-121">The following table lists the property keys that are associated with the Check Box control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39905-122">Ключ свойства</span><span class="sxs-lookup"><span data-stu-id="39905-122">Property Key</span></span></th>
<th><span data-ttu-id="39905-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="39905-123">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="39905-124"><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></span><span class="sxs-lookup"><span data-stu-id="39905-124"><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></span></span></td>
<td><span data-ttu-id="39905-125">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="39905-125">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="39905-126">Если команда, связанная с элементом управления, становится недействительной при вызове <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>иуифрамеворк:: инвалидатеуикомманд</strong></a>, платформа запрашивает это свойство, когда в <code>UI_INVALIDATIONS_VALUE</code> качестве значения <em>флагов</em>передается.</span><span class="sxs-lookup"><span data-stu-id="39905-126">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39905-127"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="39905-127"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="39905-128">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="39905-128">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39905-129"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="39905-129"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="39905-130">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="39905-130">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39905-131"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="39905-131"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="39905-132">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="39905-132">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39905-133"><a href="windowsribbon-reference-properties-uipkey-labeldescription.md">UI_PKEY_LabelDescription</a></span><span class="sxs-lookup"><span data-stu-id="39905-133"><a href="windowsribbon-reference-properties-uipkey-labeldescription.md">UI_PKEY_LabelDescription</a></span></span></td>
<td><span data-ttu-id="39905-134">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="39905-134">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39905-135"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="39905-135"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="39905-136">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="39905-136">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39905-137"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="39905-137"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="39905-138">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="39905-138">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39905-139"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="39905-139"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="39905-140">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="39905-140">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39905-141"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="39905-141"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="39905-142">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="39905-142">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39905-143"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="39905-143"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="39905-144">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="39905-144">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39905-145"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="39905-145"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="39905-146">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="39905-146">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="39905-147">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="39905-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39905-148">Библиотека элементов управления платформы Windows ленты</span><span class="sxs-lookup"><span data-stu-id="39905-148">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="39905-149">**Элемент разметки CheckBox**</span><span class="sxs-lookup"><span data-stu-id="39905-149">**CheckBox markup element**</span></span>](windowsribbon-element-checkbox.md)
</dt> </dl>

