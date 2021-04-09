---
title: (Платформа Windows лента)
description: Кнопка — это элемент управления, который пользователь может щелкнуть, чтобы предоставить входные данные приложению.
ms.assetid: 6d4aa571-dbea-4139-a6b7-45a85595dd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1514a1ae66e383d18f81d1ca0ee1a5a8e453335d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134879"
---
# <a name="button-windows-ribbon-framework"></a><span data-ttu-id="89b69-103">(Платформа Windows лента)</span><span class="sxs-lookup"><span data-stu-id="89b69-103">Button (Windows Ribbon Framework)</span></span>

<span data-ttu-id="89b69-104">Кнопка — это элемент управления, который пользователь может щелкнуть, чтобы предоставить входные данные приложению.</span><span class="sxs-lookup"><span data-stu-id="89b69-104">The Button is a control the user can click to provide input to an application.</span></span>

-   [<span data-ttu-id="89b69-105">Введение</span><span class="sxs-lookup"><span data-stu-id="89b69-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="89b69-106">Свойства кнопки</span><span class="sxs-lookup"><span data-stu-id="89b69-106">Button Properties</span></span>](#button-properties)
-   [<span data-ttu-id="89b69-107">См. также</span><span class="sxs-lookup"><span data-stu-id="89b69-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="89b69-108">Введение</span><span class="sxs-lookup"><span data-stu-id="89b69-108">Introduction</span></span>

<span data-ttu-id="89b69-109">На следующем снимке экрана представлены три примера элемента кнопки на ленте.</span><span class="sxs-lookup"><span data-stu-id="89b69-109">The following screen shot contains three examples of the Ribbon Button element.</span></span>

![снимок экрана элементов управления "Кнопка" на ленте Microsoft WordPad.](images/controls/button.png)

## <a name="button-properties"></a><span data-ttu-id="89b69-111">Свойства кнопки</span><span class="sxs-lookup"><span data-stu-id="89b69-111">Button Properties</span></span>

<span data-ttu-id="89b69-112">Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="89b69-112">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Button control.</span></span>

<span data-ttu-id="89b69-113">Как правило, свойство Button обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="89b69-113">Typically, a Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="89b69-114">Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="89b69-114">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="89b69-115">Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы.</span><span class="sxs-lookup"><span data-stu-id="89b69-115">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="89b69-116">Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.</span><span class="sxs-lookup"><span data-stu-id="89b69-116">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="89b69-117">В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="89b69-117">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="89b69-118">В следующей таблице перечислены ключи свойств, связанные с элементом управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="89b69-118">The following table lists the property keys that are associated with the Button control.</span></span>



| <span data-ttu-id="89b69-119">Ключ свойства</span><span class="sxs-lookup"><span data-stu-id="89b69-119">Property Key</span></span>                                                                                             | <span data-ttu-id="89b69-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="89b69-120">Notes</span></span>                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="89b69-121">Пользовательский интерфейс \_ PKEY \_ включен</span><span class="sxs-lookup"><span data-stu-id="89b69-121">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                               | <span data-ttu-id="89b69-122">Поддерживает [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="89b69-122">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="89b69-123">UI \_ PKEY \_ keytip</span><span class="sxs-lookup"><span data-stu-id="89b69-123">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                                 | <span data-ttu-id="89b69-124">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="89b69-124">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="89b69-125">\_Метка PKEY пользовательского интерфейса \_</span><span class="sxs-lookup"><span data-stu-id="89b69-125">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                                   | <span data-ttu-id="89b69-126">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="89b69-126">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="89b69-127">UI \_ PKEY \_ лабелдескриптион</span><span class="sxs-lookup"><span data-stu-id="89b69-127">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)             | <span data-ttu-id="89b69-128">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="89b69-128">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="89b69-129">UI \_ PKEY \_ ларжехигхконтрастимаже</span><span class="sxs-lookup"><span data-stu-id="89b69-129">UI\_PKEY\_LargeHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md) | <span data-ttu-id="89b69-130">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="89b69-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="89b69-131">UI \_ PKEY \_ ларжеимаже</span><span class="sxs-lookup"><span data-stu-id="89b69-131">UI\_PKEY\_LargeImage</span></span>](windowsribbon-reference-properties-uipkey-largeimage.md)                         | <span data-ttu-id="89b69-132">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="89b69-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="89b69-133">UI \_ PKEY \_ смаллхигхконтрастимаже</span><span class="sxs-lookup"><span data-stu-id="89b69-133">UI\_PKEY\_SmallHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md) | <span data-ttu-id="89b69-134">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="89b69-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="89b69-135">UI \_ PKEY \_ смаллимаже</span><span class="sxs-lookup"><span data-stu-id="89b69-135">UI\_PKEY\_SmallImage</span></span>](windowsribbon-reference-properties-uipkey-smallimage.md)                         | <span data-ttu-id="89b69-136">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="89b69-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="89b69-137">UI \_ PKEY \_ тултипдескриптион</span><span class="sxs-lookup"><span data-stu-id="89b69-137">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md)         | <span data-ttu-id="89b69-138">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="89b69-138">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="89b69-139">UI \_ PKEY \_ тултиптитле</span><span class="sxs-lookup"><span data-stu-id="89b69-139">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)                     | <span data-ttu-id="89b69-140">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="89b69-140">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="89b69-141">См. также</span><span class="sxs-lookup"><span data-stu-id="89b69-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89b69-142">Библиотека элементов управления платформы Windows ленты</span><span class="sxs-lookup"><span data-stu-id="89b69-142">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="89b69-143">**Элемент разметки кнопки**</span><span class="sxs-lookup"><span data-stu-id="89b69-143">**Button markup element**</span></span>](windowsribbon-element-button.md)
</dt> </dl>

 

 
