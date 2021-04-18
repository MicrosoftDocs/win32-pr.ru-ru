---
title: Разворачивающаяся кнопка
description: Разворачивающаяся кнопка — это составной элемент управления, с помощью которого пользователь может выбрать значение по умолчанию, привязанное к основной кнопке, или выбрать из списка взаимоисключающих значений, отображаемых в раскрывающемся списке, привязанном к дополнительной кнопке.
ms.assetid: 0939b3be-fa88-4864-8096-a664ab2e97b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b78aa261eebb24404eeaf8b3fdad7f630331f58
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "105691688"
---
# <a name="split-button"></a><span data-ttu-id="4cd19-103">Разворачивающаяся кнопка</span><span class="sxs-lookup"><span data-stu-id="4cd19-103">Split Button</span></span>

<span data-ttu-id="4cd19-104">Разворачивающаяся кнопка — это составной элемент управления, с помощью которого пользователь может выбрать значение по умолчанию, привязанное к основной кнопке, или выбрать из списка взаимоисключающих значений, отображаемых в раскрывающемся списке, привязанном к дополнительной кнопке.</span><span class="sxs-lookup"><span data-stu-id="4cd19-104">The Split Button is a composite control with which the user can select a default value bound to a primary button, or select from a list of mutually exclusive values displayed in a drop-down list bound to a secondary button.</span></span>

-   [<span data-ttu-id="4cd19-105">Введение</span><span class="sxs-lookup"><span data-stu-id="4cd19-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="4cd19-106">Свойства разворачивающейся кнопки</span><span class="sxs-lookup"><span data-stu-id="4cd19-106">Split Button Properties</span></span>](#split-button-properties)
-   [<span data-ttu-id="4cd19-107">См. также</span><span class="sxs-lookup"><span data-stu-id="4cd19-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="4cd19-108">Введение</span><span class="sxs-lookup"><span data-stu-id="4cd19-108">Introduction</span></span>

<span data-ttu-id="4cd19-109">Этот элемент управления полезен для предоставления тесно связанных элементов в случаях, когда доступно очевидное по умолчанию, а отдельные элементы могут быть представлены изображением, текстом или обоими.</span><span class="sxs-lookup"><span data-stu-id="4cd19-109">This control is useful for exposing closely related items in cases where an obvious default is available and where the individual items can be represented by an image, text, or both.</span></span>

<span data-ttu-id="4cd19-110">На следующем снимке экрана показана кнопка разделения ленты.</span><span class="sxs-lookup"><span data-stu-id="4cd19-110">The following screen shot illustrates the Ribbon Split Button.</span></span>

![снимок экрана элемента управления SplitButton в образце ленты.](images/controls/splitbutton.png)

## <a name="split-button-properties"></a><span data-ttu-id="4cd19-112">Свойства разворачивающейся кнопки</span><span class="sxs-lookup"><span data-stu-id="4cd19-112">Split Button Properties</span></span>

<span data-ttu-id="4cd19-113">Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления "кнопка разворачивающейся кнопки".</span><span class="sxs-lookup"><span data-stu-id="4cd19-113">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Split Button control.</span></span>

<span data-ttu-id="4cd19-114">Как правило, свойство разворачивающейся кнопки обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="4cd19-114">Typically, a Split Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="4cd19-115">Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="4cd19-115">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="4cd19-116">Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы.</span><span class="sxs-lookup"><span data-stu-id="4cd19-116">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="4cd19-117">Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.</span><span class="sxs-lookup"><span data-stu-id="4cd19-117">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="4cd19-118">В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="4cd19-118">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="4cd19-119">В следующей таблице перечислены ключи свойств, связанные с элементом управления "кнопка разворачивающейся кнопки".</span><span class="sxs-lookup"><span data-stu-id="4cd19-119">The following table lists the property keys that are associated with the Split Button control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4cd19-120">Ключ свойства</span><span class="sxs-lookup"><span data-stu-id="4cd19-120">Property Key</span></span></th>
<th><span data-ttu-id="4cd19-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="4cd19-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4cd19-122"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="4cd19-122"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="4cd19-123">Поддерживает <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>иуифрамеворк:: жетуикоммандпроперти</strong></a> и <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>Иуифрамеворк:: сетуикоммандпроперти</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4cd19-123">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span><br/> <span data-ttu-id="4cd19-124">Если все дочерние элементы отключены, платформа устанавливает для <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> значение false (0).</span><span class="sxs-lookup"><span data-stu-id="4cd19-124">If all child items are disabled, the framework sets <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> to false (0).</span></span> <span data-ttu-id="4cd19-125">В противном случае, если один или несколько дочерних элементов включены, UI_PKEY_Enabled имеет значение true (-1).</span><span class="sxs-lookup"><span data-stu-id="4cd19-125">Otherwise, if one or more child items are enabled, UI_PKEY_Enabled is set to true (-1).</span></span>
<blockquote>
[!Important]<br />
<span data-ttu-id="4cd19-126">Свойство <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> элемента управления "разворачивающаяся кнопка" должно быть недействительным после включения или отключения одного или нескольких дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="4cd19-126">The <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> property for the Split Button control should be invalidated after one or more child items are enabled or disabled.</span></span> <span data-ttu-id="4cd19-127">Это гарантирует, что платформа запрашивает обновленное значение свойства и обновляет состояние элемента управления "разворачивающаяся кнопка" в пользовательском интерфейсе ленты.</span><span class="sxs-lookup"><span data-stu-id="4cd19-127">This ensures that the framework queries the updated property value and refreshes the state of the Split Button control in the ribbon UI.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4cd19-128"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="4cd19-128"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="4cd19-129">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="4cd19-129">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4cd19-130"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="4cd19-130"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="4cd19-131">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="4cd19-131">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4cd19-132"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="4cd19-132"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="4cd19-133">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="4cd19-133">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="4cd19-134">См. также</span><span class="sxs-lookup"><span data-stu-id="4cd19-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cd19-135">Библиотека элементов управления платформы Windows ленты</span><span class="sxs-lookup"><span data-stu-id="4cd19-135">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="4cd19-136">**Элемент разметки SplitButton**</span><span class="sxs-lookup"><span data-stu-id="4cd19-136">**SplitButton markup element**</span></span>](windowsribbon-element-splitbutton.md)
</dt> </dl>