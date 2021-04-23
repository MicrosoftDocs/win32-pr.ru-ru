---
title: Кнопка "Справка"
description: Кнопка Справка — это элемент управления, который пользователь может щелкнуть для вывода справочной системы приложения.
ms.assetid: 5f08a8b2-bc83-4256-bcc4-aecfbd07ea51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc44c9f9a03561f1627067849272509838d7a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987528"
---
# <a name="help-button"></a><span data-ttu-id="48e7c-103">Кнопка "Справка"</span><span class="sxs-lookup"><span data-stu-id="48e7c-103">Help Button</span></span>

<span data-ttu-id="48e7c-104">Кнопка Справка — это элемент управления, который пользователь может щелкнуть для вывода справочной системы приложения.</span><span class="sxs-lookup"><span data-stu-id="48e7c-104">The Help Button is a control that the user can click to display the application help system.</span></span>

-   [<span data-ttu-id="48e7c-105">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="48e7c-105">Details</span></span>](#details)
-   [<span data-ttu-id="48e7c-106">Свойства кнопки "Справка"</span><span class="sxs-lookup"><span data-stu-id="48e7c-106">Help Button Properties</span></span>](#help-button-properties)
-   [<span data-ttu-id="48e7c-107">См. также</span><span class="sxs-lookup"><span data-stu-id="48e7c-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="48e7c-108">Сведения</span><span class="sxs-lookup"><span data-stu-id="48e7c-108">Details</span></span>

<span data-ttu-id="48e7c-109">На следующем снимке экрана показана кнопка Справка на ленте.</span><span class="sxs-lookup"><span data-stu-id="48e7c-109">The following screen shot illustrates the Ribbon Help Button.</span></span>

![снимок экрана с кнопкой "Справка".](images/controls/helpbutton.png)

## <a name="help-button-properties"></a><span data-ttu-id="48e7c-111">Свойства кнопки "Справка"</span><span class="sxs-lookup"><span data-stu-id="48e7c-111">Help Button Properties</span></span>

<span data-ttu-id="48e7c-112">Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления кнопки "Справка".</span><span class="sxs-lookup"><span data-stu-id="48e7c-112">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Help Button control.</span></span>

<span data-ttu-id="48e7c-113">Как правило, свойство кнопки справки обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="48e7c-113">Typically, a Help Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="48e7c-114">Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="48e7c-114">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="48e7c-115">Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы.</span><span class="sxs-lookup"><span data-stu-id="48e7c-115">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="48e7c-116">Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.</span><span class="sxs-lookup"><span data-stu-id="48e7c-116">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="48e7c-117">В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="48e7c-117">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="48e7c-118">В следующей таблице перечислены ключи свойств, связанные с элементом управления кнопки "Справка".</span><span class="sxs-lookup"><span data-stu-id="48e7c-118">The following table lists the property keys that are associated with the Help Button control.</span></span>



| <span data-ttu-id="48e7c-119">Ключ свойства</span><span class="sxs-lookup"><span data-stu-id="48e7c-119">Property Key</span></span>                                                                                     | <span data-ttu-id="48e7c-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="48e7c-120">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="48e7c-121">UI \_ PKEY \_ keytip</span><span class="sxs-lookup"><span data-stu-id="48e7c-121">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="48e7c-122">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="48e7c-122">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="48e7c-123">\_Метка PKEY пользовательского интерфейса \_</span><span class="sxs-lookup"><span data-stu-id="48e7c-123">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="48e7c-124">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="48e7c-124">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="48e7c-125">UI \_ PKEY \_ тултипдескриптион</span><span class="sxs-lookup"><span data-stu-id="48e7c-125">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="48e7c-126">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="48e7c-126">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="48e7c-127">UI \_ PKEY \_ тултиптитле</span><span class="sxs-lookup"><span data-stu-id="48e7c-127">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="48e7c-128">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="48e7c-128">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="48e7c-129">См. также</span><span class="sxs-lookup"><span data-stu-id="48e7c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48e7c-130">Библиотека элементов управления платформы Windows ленты</span><span class="sxs-lookup"><span data-stu-id="48e7c-130">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="48e7c-131">**Хелпбуттон, элемент**</span><span class="sxs-lookup"><span data-stu-id="48e7c-131">**HelpButton element**</span></span>](windowsribbon-element-helpbutton.md)
</dt> </dl>

 

 