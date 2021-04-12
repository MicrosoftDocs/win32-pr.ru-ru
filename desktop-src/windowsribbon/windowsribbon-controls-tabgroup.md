---
title: Группа вкладок
description: Группа вкладок — это контекстный элемент управления, который скрывается или отображается во время выполнения в зависимости от состояния документа или рабочей области. Группа вкладок содержит набор элементов управления вкладки, связанных с контекстом.
ms.assetid: 5b74ff46-2543-43f3-ab42-dab1bc67a75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253c803a07c0d27692442ddb7a291930a261a2ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338641"
---
# <a name="tab-group"></a><span data-ttu-id="de696-104">Группа вкладок</span><span class="sxs-lookup"><span data-stu-id="de696-104">Tab Group</span></span>

<span data-ttu-id="de696-105">Группа вкладок — это контекстный элемент управления, который скрывается или отображается во время выполнения в зависимости от состояния документа или рабочей области.</span><span class="sxs-lookup"><span data-stu-id="de696-105">A Tab Group is a contextual control that is hidden or displayed at run time, based on a document or workspace state.</span></span> <span data-ttu-id="de696-106">Группа вкладок содержит набор элементов управления [вкладки](windowsribbon-controls-tab.md) , связанных с контекстом.</span><span class="sxs-lookup"><span data-stu-id="de696-106">The Tab Group contains a set of context-related [Tab](windowsribbon-controls-tab.md) controls.</span></span>

-   [<span data-ttu-id="de696-107">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="de696-107">Details</span></span>](#details)
-   [<span data-ttu-id="de696-108">Свойства группы вкладок</span><span class="sxs-lookup"><span data-stu-id="de696-108">Tab Group Properties</span></span>](#tab-group-properties)
-   [<span data-ttu-id="de696-109">См. также</span><span class="sxs-lookup"><span data-stu-id="de696-109">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="de696-110">Сведения</span><span class="sxs-lookup"><span data-stu-id="de696-110">Details</span></span>

<span data-ttu-id="de696-111">Как правило, группа вкладок отображается во время определенных состояний документа или рабочей области, например, когда пользователь выбирает определенный тип объекта.</span><span class="sxs-lookup"><span data-stu-id="de696-111">Typically, a Tab Group is displayed during specific document or workspace states, such as when a user selects a particular object type.</span></span> <span data-ttu-id="de696-112">Например, для выбора изображения, содержащегося в заголовке таблицы, может потребоваться отображение различных контекстных вкладок, предоставляющих функции для работы с таблицами и изображениями.</span><span class="sxs-lookup"><span data-stu-id="de696-112">For example, the selection of an image contained in the header of a table might require various contextual tabs to be displayed that expose both table and image functionality.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de696-113">Группа вкладок не поддерживает [режимы приложений](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="de696-113">A Tab Group does not support [application modes](ribbon-applicationmodes.md).</span></span> <span data-ttu-id="de696-114">Однако отдельные элементы управления [вкладки](windowsribbon-controls-tab.md) в группе вкладок могут.</span><span class="sxs-lookup"><span data-stu-id="de696-114">However, the individual [Tab](windowsribbon-controls-tab.md) controls within a Tab Group may.</span></span>

 

<span data-ttu-id="de696-115">На следующем снимке экрана показана контекстная [вкладка](windowsribbon-controls-tab.md) из Windows 7 Paint.</span><span class="sxs-lookup"><span data-stu-id="de696-115">The following screen shot shows a contextual [Tab](windowsribbon-controls-tab.md) from Windows 7 Paint.</span></span>

![снимок экрана, на котором показан контекстный элемент управления вкладки.](images/controls/contextualtab.png)

## <a name="tab-group-properties"></a><span data-ttu-id="de696-117">Свойства группы вкладок</span><span class="sxs-lookup"><span data-stu-id="de696-117">Tab Group Properties</span></span>

<span data-ttu-id="de696-118">Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления группы вкладок.</span><span class="sxs-lookup"><span data-stu-id="de696-118">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Tab Group control.</span></span>

<span data-ttu-id="de696-119">Как правило, свойство группы вкладок обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="de696-119">Typically, a Tab Group property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="de696-120">Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="de696-120">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="de696-121">Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы.</span><span class="sxs-lookup"><span data-stu-id="de696-121">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="de696-122">Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.</span><span class="sxs-lookup"><span data-stu-id="de696-122">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="de696-123">В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="de696-123">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="de696-124">В следующей таблице перечислены ключи свойств, связанные с элементом управления группы вкладок.</span><span class="sxs-lookup"><span data-stu-id="de696-124">The following table lists the property keys that are associated with the Tab Group control.</span></span>



| <span data-ttu-id="de696-125">Ключ свойства</span><span class="sxs-lookup"><span data-stu-id="de696-125">Property Key</span></span>                                                                                     | <span data-ttu-id="de696-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="de696-126">Notes</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de696-127">UI \_ PKEY \_ контекставаилабле</span><span class="sxs-lookup"><span data-stu-id="de696-127">UI\_PKEY\_ContextAvailable</span></span>](windowsribbon-reference-properties-uipkey-contextavailable.md)     | <span data-ttu-id="de696-128">Поддерживает [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="de696-128">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="de696-129">UI \_ PKEY \_ keytip</span><span class="sxs-lookup"><span data-stu-id="de696-129">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="de696-130">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="de696-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="de696-131">\_Метка PKEY пользовательского интерфейса \_</span><span class="sxs-lookup"><span data-stu-id="de696-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="de696-132">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="de696-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="de696-133">UI \_ PKEY \_ тултипдескриптион</span><span class="sxs-lookup"><span data-stu-id="de696-133">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="de696-134">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="de696-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="de696-135">UI \_ PKEY \_ тултиптитле</span><span class="sxs-lookup"><span data-stu-id="de696-135">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="de696-136">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="de696-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="de696-137">См. также</span><span class="sxs-lookup"><span data-stu-id="de696-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de696-138">Библиотека элементов управления платформы Windows ленты</span><span class="sxs-lookup"><span data-stu-id="de696-138">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="de696-139">**Табграуп, элемент разметки**</span><span class="sxs-lookup"><span data-stu-id="de696-139">**TabGroup markup element**</span></span>](windowsribbon-element-tabgroup.md)
</dt> </dl>

 

 