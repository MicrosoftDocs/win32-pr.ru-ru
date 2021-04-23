---
title: Выключатель
description: Выключатель при нажатии предоставляет входные данные для приложения. Элемент управления представляет взаимоисключающее состояние переключателя.
ms.assetid: 290052b7-0528-41c5-b6f4-958cc42d502b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d72c06f8382e7210f1041960b92de5f6054548d1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104550238"
---
# <a name="toggle-button"></a><span data-ttu-id="4c85a-104">Выключатель</span><span class="sxs-lookup"><span data-stu-id="4c85a-104">Toggle Button</span></span>

<span data-ttu-id="4c85a-105">Выключатель при нажатии предоставляет входные данные для приложения.</span><span class="sxs-lookup"><span data-stu-id="4c85a-105">The Toggle Button when clicked provides input to an application.</span></span> <span data-ttu-id="4c85a-106">Элемент управления представляет взаимоисключающее состояние переключателя.</span><span class="sxs-lookup"><span data-stu-id="4c85a-106">The control represents a mutually exclusive toggle state.</span></span>

-   [<span data-ttu-id="4c85a-107">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="4c85a-107">Details</span></span>](#details)
-   [<span data-ttu-id="4c85a-108">Свойства выключателя</span><span class="sxs-lookup"><span data-stu-id="4c85a-108">Toggle Button Properties</span></span>](#toggle-button-properties)
-   [<span data-ttu-id="4c85a-109">См. также</span><span class="sxs-lookup"><span data-stu-id="4c85a-109">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="4c85a-110">Сведения</span><span class="sxs-lookup"><span data-stu-id="4c85a-110">Details</span></span>

<span data-ttu-id="4c85a-111">На следующем снимке экрана показана выключатель ленты.</span><span class="sxs-lookup"><span data-stu-id="4c85a-111">The following screen shot illustrates the Ribbon Toggle Button.</span></span>

![снимок экрана: элемент управления ToggleButton на ленте Microsoft Paint.](images/controls/togglebutton.png)

## <a name="toggle-button-properties"></a><span data-ttu-id="4c85a-113">Свойства выключателя</span><span class="sxs-lookup"><span data-stu-id="4c85a-113">Toggle Button Properties</span></span>

<span data-ttu-id="4c85a-114">Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления "выключатель".</span><span class="sxs-lookup"><span data-stu-id="4c85a-114">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Toggle Button control.</span></span>

<span data-ttu-id="4c85a-115">Как правило, свойство выключателя обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="4c85a-115">Typically, a Toggle Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="4c85a-116">Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="4c85a-116">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="4c85a-117">Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы.</span><span class="sxs-lookup"><span data-stu-id="4c85a-117">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="4c85a-118">Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.</span><span class="sxs-lookup"><span data-stu-id="4c85a-118">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="4c85a-119">В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="4c85a-119">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="4c85a-120">В следующей таблице перечислены ключи свойств, связанные с элементом управления "выключатель".</span><span class="sxs-lookup"><span data-stu-id="4c85a-120">The following table lists the property keys that are associated with the Toggle Button control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4c85a-121">Ключ свойства</span><span class="sxs-lookup"><span data-stu-id="4c85a-121">Property Key</span></span></th>
<th><span data-ttu-id="4c85a-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="4c85a-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c85a-123"><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></span><span class="sxs-lookup"><span data-stu-id="4c85a-123"><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></span></span></td>
<td><span data-ttu-id="4c85a-124">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4c85a-124">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="4c85a-125">Если команда, связанная с элементом управления, становится недействительной при вызове <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>иуифрамеворк:: инвалидатеуикомманд</strong></a>, платформа запрашивает это свойство, когда в <code>UI_INVALIDATIONS_VALUE</code> качестве значения <em>флагов</em>передается.</span><span class="sxs-lookup"><span data-stu-id="4c85a-125">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c85a-126"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="4c85a-126"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="4c85a-127">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4c85a-127">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c85a-128"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="4c85a-128"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="4c85a-129">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="4c85a-129">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c85a-130"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="4c85a-130"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="4c85a-131">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="4c85a-131">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c85a-132"><a href="windowsribbon-reference-properties-uipkey-labeldescription.md">UI_PKEY_LabelDescription</a></span><span class="sxs-lookup"><span data-stu-id="4c85a-132"><a href="windowsribbon-reference-properties-uipkey-labeldescription.md">UI_PKEY_LabelDescription</a></span></span></td>
<td><span data-ttu-id="4c85a-133">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="4c85a-133">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c85a-134"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="4c85a-134"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="4c85a-135">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="4c85a-135">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c85a-136"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="4c85a-136"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="4c85a-137">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="4c85a-137">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c85a-138"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="4c85a-138"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="4c85a-139">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="4c85a-139">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c85a-140"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="4c85a-140"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="4c85a-141">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="4c85a-141">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c85a-142"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="4c85a-142"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="4c85a-143">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="4c85a-143">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c85a-144"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="4c85a-144"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="4c85a-145">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="4c85a-145">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="4c85a-146">См. также</span><span class="sxs-lookup"><span data-stu-id="4c85a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c85a-147">Библиотека элементов управления платформы Windows ленты</span><span class="sxs-lookup"><span data-stu-id="4c85a-147">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="4c85a-148">**Элемент разметки ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="4c85a-148">**ToggleButton markup element**</span></span>](windowsribbon-element-togglebutton.md)
</dt> </dl>

