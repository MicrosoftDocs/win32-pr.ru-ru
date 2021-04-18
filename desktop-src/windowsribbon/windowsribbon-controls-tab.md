---
title: Tab (платформа Windows Ribbon)
description: Вкладка содержит группы связанных элементов управления.
ms.assetid: 7315ca96-73c8-4ea1-bce0-172ebc4dd43a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b760bfc0c588c71ee9dbffa32b6cebc12a39fea7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340250"
---
# <a name="tab-windows-ribbon-framework"></a><span data-ttu-id="023cf-103">Tab (платформа Windows Ribbon)</span><span class="sxs-lookup"><span data-stu-id="023cf-103">Tab (Windows Ribbon Framework)</span></span>

<span data-ttu-id="023cf-104">Вкладка содержит [группы](windowsribbon-controls-group.md) связанных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="023cf-104">A Tab contains [groups](windowsribbon-controls-group.md) of related controls.</span></span>

-   [<span data-ttu-id="023cf-105">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="023cf-105">Details</span></span>](#details)
-   [<span data-ttu-id="023cf-106">Свойства вкладки</span><span class="sxs-lookup"><span data-stu-id="023cf-106">Tab Properties</span></span>](#tab-properties)
-   [<span data-ttu-id="023cf-107">См. также</span><span class="sxs-lookup"><span data-stu-id="023cf-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="023cf-108">Сведения</span><span class="sxs-lookup"><span data-stu-id="023cf-108">Details</span></span>

<span data-ttu-id="023cf-109">В платформе ленты есть три типа вкладок.</span><span class="sxs-lookup"><span data-stu-id="023cf-109">There are three types of Tab in the Ribbon framework.</span></span>



| <span data-ttu-id="023cf-110">Тип</span><span class="sxs-lookup"><span data-stu-id="023cf-110">Type</span></span>               | <span data-ttu-id="023cf-111">Описание</span><span class="sxs-lookup"><span data-stu-id="023cf-111">Description</span></span>                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="023cf-112">**Вкладка "ядро"**</span><span class="sxs-lookup"><span data-stu-id="023cf-112">**Core tab**</span></span>       | <span data-ttu-id="023cf-113">Основные вкладки, которые упорядочивают функции по умолчанию приложения.</span><span class="sxs-lookup"><span data-stu-id="023cf-113">Core tabs that organize the default functions of the application.</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="023cf-114">**Контекстная вкладка**</span><span class="sxs-lookup"><span data-stu-id="023cf-114">**Contextual tab**</span></span> | <span data-ttu-id="023cf-115">Вкладки, отображаемые во время конкретных состояний документа или рабочей области.</span><span class="sxs-lookup"><span data-stu-id="023cf-115">Tabs that are displayed during specific document or workspace states.</span></span> <span data-ttu-id="023cf-116">Например, если пользователь выбирает определенный тип объекта, например изображение, содержащееся в заголовке таблицы, то могут отображаться различные контекстные вкладки, предоставляющие функциональные возможности работы с таблицами и изображениями.</span><span class="sxs-lookup"><span data-stu-id="023cf-116">For example, if a user selects a particular object type, such as an image contained in the header of a table, then various contextual tabs might be displayed that expose both table and image functionality.</span></span> |
| <span data-ttu-id="023cf-117">**Модальная вкладка**</span><span class="sxs-lookup"><span data-stu-id="023cf-117">**Modal tab**</span></span>      | <span data-ttu-id="023cf-118">Основные вкладки, отображаемые во время конкретного документа или рабочей области [приложения](ribbon-applicationmodes.md), например предварительный просмотр.</span><span class="sxs-lookup"><span data-stu-id="023cf-118">Core tabs that are displayed during a specific document or workspace [application mode](ribbon-applicationmodes.md), such as print preview.</span></span>                                                                                                                                        |



 

<span data-ttu-id="023cf-119">На следующем снимке экрана показана основная вкладка из Windows 7 Paint.</span><span class="sxs-lookup"><span data-stu-id="023cf-119">The following screen shot shows a core Tab from Windows 7 Paint.</span></span>

![снимок экрана, на котором показан основной элемент управления "Вкладка".](images/controls/coretab.png)

## <a name="tab-properties"></a><span data-ttu-id="023cf-121">Свойства вкладки</span><span class="sxs-lookup"><span data-stu-id="023cf-121">Tab Properties</span></span>

<span data-ttu-id="023cf-122">Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="023cf-122">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Tab control.</span></span>

<span data-ttu-id="023cf-123">Как правило, свойство вкладки обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="023cf-123">Typically, a Tab property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="023cf-124">Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="023cf-124">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="023cf-125">Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы.</span><span class="sxs-lookup"><span data-stu-id="023cf-125">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="023cf-126">Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.</span><span class="sxs-lookup"><span data-stu-id="023cf-126">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="023cf-127">В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="023cf-127">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="023cf-128">В следующей таблице перечислены ключи свойств, связанные с элементом управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="023cf-128">The following table lists the property keys that are associated with the Tab control.</span></span>



| <span data-ttu-id="023cf-129">Ключ свойства</span><span class="sxs-lookup"><span data-stu-id="023cf-129">Property Key</span></span>                                                                                     | <span data-ttu-id="023cf-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="023cf-130">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="023cf-131">\_Метка PKEY пользовательского интерфейса \_</span><span class="sxs-lookup"><span data-stu-id="023cf-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="023cf-132">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="023cf-132">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="023cf-133">UI \_ PKEY \_ keytip</span><span class="sxs-lookup"><span data-stu-id="023cf-133">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="023cf-134">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="023cf-134">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="023cf-135">UI \_ PKEY \_ тултипдескриптион</span><span class="sxs-lookup"><span data-stu-id="023cf-135">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="023cf-136">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="023cf-136">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="023cf-137">UI \_ PKEY \_ тултиптитле</span><span class="sxs-lookup"><span data-stu-id="023cf-137">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="023cf-138">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="023cf-138">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="023cf-139">См. также</span><span class="sxs-lookup"><span data-stu-id="023cf-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="023cf-140">Библиотека элементов управления платформы Windows ленты</span><span class="sxs-lookup"><span data-stu-id="023cf-140">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="023cf-141">**Элемент разметки вкладки**</span><span class="sxs-lookup"><span data-stu-id="023cf-141">**Tab markup element**</span></span>](windowsribbon-element-tab.md)
</dt> </dl>

 

 
