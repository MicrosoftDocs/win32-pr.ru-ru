---
title: Группа (платформа Windows для ленты)
description: Группа организует связанные команды и элементы управления на вкладке.
ms.assetid: 5d098d3f-a4ee-4f76-8c81-832d0c49cb80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903bd422d11fea81ed03a48bf8e9437f9caab699
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414632"
---
# <a name="group-windows-ribbon-framework"></a><span data-ttu-id="0278d-103">Группа (платформа Windows для ленты)</span><span class="sxs-lookup"><span data-stu-id="0278d-103">Group (Windows Ribbon Framework)</span></span>

<span data-ttu-id="0278d-104">Группа организует связанные команды и элементы управления на [вкладке](windowsribbon-controls-tab.md).</span><span class="sxs-lookup"><span data-stu-id="0278d-104">The Group organizes related Commands and controls within a [Tab](windowsribbon-controls-tab.md).</span></span>

-   [<span data-ttu-id="0278d-105">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="0278d-105">Details</span></span>](#details)
-   [<span data-ttu-id="0278d-106">Свойства группы</span><span class="sxs-lookup"><span data-stu-id="0278d-106">Group Properties</span></span>](#group-properties)
-   [<span data-ttu-id="0278d-107">См. также</span><span class="sxs-lookup"><span data-stu-id="0278d-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="0278d-108">Сведения</span><span class="sxs-lookup"><span data-stu-id="0278d-108">Details</span></span>

<span data-ttu-id="0278d-109">На следующем снимке экрана показан элемент управления "группа ленты".</span><span class="sxs-lookup"><span data-stu-id="0278d-109">The following screen shot illustrates the Ribbon Group control.</span></span>

![снимок экрана с выносками, отображающими группу.](images/controls/group.png)

## <a name="group-properties"></a><span data-ttu-id="0278d-111">Свойства группы</span><span class="sxs-lookup"><span data-stu-id="0278d-111">Group Properties</span></span>

<span data-ttu-id="0278d-112">Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления группы.</span><span class="sxs-lookup"><span data-stu-id="0278d-112">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Group control.</span></span>

<span data-ttu-id="0278d-113">Как правило, свойство группы обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="0278d-113">Typically, a Group property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="0278d-114">Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="0278d-114">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="0278d-115">Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы.</span><span class="sxs-lookup"><span data-stu-id="0278d-115">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="0278d-116">Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.</span><span class="sxs-lookup"><span data-stu-id="0278d-116">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="0278d-117">В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="0278d-117">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="0278d-118">В следующей таблице перечислены ключи свойств, связанные с элементом управления группы.</span><span class="sxs-lookup"><span data-stu-id="0278d-118">The following table lists the property keys that are associated with the Group control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0278d-119">Ключ свойства</span><span class="sxs-lookup"><span data-stu-id="0278d-119">Property Key</span></span></th>
<th><span data-ttu-id="0278d-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="0278d-120">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0278d-121"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="0278d-121"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="0278d-122">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="0278d-122">Can only be updated through invalidation.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="0278d-123">Платформа требует, чтобы значение <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> для элемента управления группы начиналось с буквы верхнего регистра Z. Если значение, предоставленное приложением в методе обратного вызова <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty"><strong>иуикоммандхандлер:: упдатепроперти</strong></a> , не начинается с буквы Z, это значение игнорируется, и вместо этого создается значение платформы.</span><span class="sxs-lookup"><span data-stu-id="0278d-123">The framework requires that the value of <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> for a Group control begins with the upper-case letter Z. If the value supplied by the application in the <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty"><strong>IUICommandHandler::UpdateProperty</strong></a> callback method does not begin with the letter Z, this value is ignored and a value is generated by the framework instead.</span></span> <span data-ttu-id="0278d-124">Значением платформы является буква Z, за которой следует числовое значение, начинающееся с 1 и последовательно увеличивающееся при необходимости для последующих элементов управления группы (Z1, Z2,..., ЗКС).</span><span class="sxs-lookup"><span data-stu-id="0278d-124">The framework value is the letter Z followed by a numeric value starting at 1 and increasing sequentially, as required, for subsequent Group controls (Z1, Z2, ..., Zx).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0278d-125"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="0278d-125"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="0278d-126">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="0278d-126">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0278d-127"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="0278d-127"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="0278d-128">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="0278d-128">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0278d-129"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="0278d-129"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="0278d-130">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="0278d-130">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0278d-131"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="0278d-131"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="0278d-132">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="0278d-132">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0278d-133"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="0278d-133"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="0278d-134">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="0278d-134">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0278d-135"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="0278d-135"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="0278d-136">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="0278d-136">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0278d-137"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="0278d-137"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="0278d-138">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="0278d-138">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="0278d-139">См. также</span><span class="sxs-lookup"><span data-stu-id="0278d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0278d-140">Библиотека элементов управления платформы Windows ленты</span><span class="sxs-lookup"><span data-stu-id="0278d-140">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="0278d-141">**Group, элемент**</span><span class="sxs-lookup"><span data-stu-id="0278d-141">**Group element**</span></span>](windowsribbon-element-group.md)
</dt> </dl>

