---
title: Недавние элементы
description: Список Недавние элементы — это панель в меню приложение, в которой отображаются последние использовавшиеся элементы для приложения.
ms.assetid: fdead358-d303-46de-9f8e-6fc2832d8e94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f78c01fc4d6cc830eba644f7dcf22b6fb03e82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104570005"
---
# <a name="recent-items"></a><span data-ttu-id="fab0a-103">Недавние элементы</span><span class="sxs-lookup"><span data-stu-id="fab0a-103">Recent Items</span></span>

<span data-ttu-id="fab0a-104">Список Недавние элементы — это панель в [меню приложение](windowsribbon-controls-applicationmenu.md) , в которой отображаются последние использовавшиеся элементы для приложения.</span><span class="sxs-lookup"><span data-stu-id="fab0a-104">The Recent Items list is a pane in the [Application Menu](windowsribbon-controls-applicationmenu.md) that displays the most recently used (MRU) items for an application.</span></span>

-   [<span data-ttu-id="fab0a-105">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="fab0a-105">Details</span></span>](#details)
-   [<span data-ttu-id="fab0a-106">Свойства недавних элементов</span><span class="sxs-lookup"><span data-stu-id="fab0a-106">Recent Items Properties</span></span>](#recent-items-properties)
-   [<span data-ttu-id="fab0a-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="fab0a-107">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="fab0a-108">См. также</span><span class="sxs-lookup"><span data-stu-id="fab0a-108">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="fab0a-109">Сведения</span><span class="sxs-lookup"><span data-stu-id="fab0a-109">Details</span></span>

<span data-ttu-id="fab0a-110">На следующем снимке экрана показан список последних элементов из WordPad для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fab0a-110">The following screen shot illustrates a Recent Items list from WordPad for Windows 7).</span></span>

![снимок экрана: список последних элементов на ленте Microsoft Paint.](images/controls/recentitems.png)

<span data-ttu-id="fab0a-112">[Меню приложения](windowsribbon-controls-applicationmenu.md) может иметь не более одного списка [**аппликатионмену. рецентитемс**](windowsribbon-element-applicationmenu-recentitems.md) , представленного элементом **аппликатионмену. рецентитемс** для отображения последних документов, изображений, фильмов и других проектов, над которыми пользователь работал.</span><span class="sxs-lookup"><span data-stu-id="fab0a-112">The [Application Menu](windowsribbon-controls-applicationmenu.md) can have at most one [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) list, represented by an **ApplicationMenu.RecentItems** element, for displaying recent documents, pictures, movies, and other projects a user has been working on.</span></span> <span data-ttu-id="fab0a-113">Число элементов в списке в диапазоне от нуля до максимального числа, указанного в разметке, со значением по умолчанию, равным 10.</span><span class="sxs-lookup"><span data-stu-id="fab0a-113">The number of listed items ranges from zero to the maximum number specified in markup, with a default value of ten.</span></span> <span data-ttu-id="fab0a-114">Последние элементы отображаются в виде нумерованного списка строк, указывающих имена файлов.</span><span class="sxs-lookup"><span data-stu-id="fab0a-114">The recent items are displayed as a numbered list of strings indicating file names.</span></span> <span data-ttu-id="fab0a-115">Рекомендуется использовать свойство [**Command. лабелдескриптион**](windowsribbon-element-command-labeldescription.md) для предоставления полного пути к расположению файла, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="fab0a-115">It is recommended that the [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md) property be used to give the full path for the file location, as shown in the following screen shot .</span></span>

![снимок экрана: список последних элементов в меню приложения.](images/overviews/applicationmenu-menurecentitems.png)

<span data-ttu-id="fab0a-117">Элемент [**рецентитемс**](windowsribbon-element-recentitems.md) имеет атрибут *енаблепиннинг* , который, если задано значение `true` , отображает значок ПИН-кода справа от каждого элемента в списке, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="fab0a-117">The [**RecentItems**](windowsribbon-element-recentitems.md) element has an *EnablePinning* attribute that, if set to `true`, displays a pin icon to the right of each item in the list, as shown in the following screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="fab0a-118">Закрепление включено по умолчанию, если не указан атрибут *енаблепиннинг* .</span><span class="sxs-lookup"><span data-stu-id="fab0a-118">Pinning is enabled by default if the *EnablePinning* attribute is not specified.</span></span>

 

![снимок экрана с закреплением последних элементов в меню приложения.](images/overviews/applicationmenu-menurecentitemspinned.png)

<span data-ttu-id="fab0a-120">Алгоритм закрепления предназначен для того, чтобы элементы не выпадают из списка **последних элементов** .</span><span class="sxs-lookup"><span data-stu-id="fab0a-120">The pinning algorithm is intended to keep items from falling off the **Recent items** list.</span></span> <span data-ttu-id="fab0a-121">Алгоритм создает следующее поведение:</span><span class="sxs-lookup"><span data-stu-id="fab0a-121">The algorithm produces the following behavior:</span></span>

-   <span data-ttu-id="fab0a-122">Новый элемент всегда добавляется в верхнюю часть списка **последних элементов** .</span><span class="sxs-lookup"><span data-stu-id="fab0a-122">A new item is always added at the top of the **Recent items** list.</span></span>
-   <span data-ttu-id="fab0a-123">Элементы будут перемещены вниз в списке с течением времени.</span><span class="sxs-lookup"><span data-stu-id="fab0a-123">Items will move down in the list over time.</span></span> <span data-ttu-id="fab0a-124">После заполнения списка (достигает максимального количества элементов, указанных в разметке) более старые элементы переходят в нижнюю часть списка, так как новые элементы добавляются в начало списка.</span><span class="sxs-lookup"><span data-stu-id="fab0a-124">Once the list is full (reaches the maximum number of items specified in markup), older items fall off the bottom of the list as new items are added to the top of the list.</span></span>
-   <span data-ttu-id="fab0a-125">Если элемент уже присутствует где-либо в списке, но снова доступен, он переместится в начало списка.</span><span class="sxs-lookup"><span data-stu-id="fab0a-125">If an item already appears somewhere in the list but is accessed again, it moves back to the top of the list.</span></span>
-   <span data-ttu-id="fab0a-126">Если элемент закреплен, он по-прежнему будет переноситься вниз по списку, но не будет выпадать в нижнюю часть.</span><span class="sxs-lookup"><span data-stu-id="fab0a-126">If an item is pinned, it will still travel down the list, but it will not fall off the bottom.</span></span> <span data-ttu-id="fab0a-127">Вместо этого после заполнения списка первый незакрепленный элемент, расположенный выше закрепленного элемента, будет отключен при добавлении нового элемента в список.</span><span class="sxs-lookup"><span data-stu-id="fab0a-127">Instead, once the list is full, the first unpinned item above the pinned item will fall off when a new item is added to the list.</span></span>
-   <span data-ttu-id="fab0a-128">Если количество закрепленных элементов достигает максимального числа элементов, новые элементы не добавляются в список до тех пор, пока элемент не будет откреплен.</span><span class="sxs-lookup"><span data-stu-id="fab0a-128">If the number of pinned items ever reaches the maximum number of items, then no new items will get added to the list until an item is unpinned.</span></span>

## <a name="recent-items-properties"></a><span data-ttu-id="fab0a-129">Свойства недавних элементов</span><span class="sxs-lookup"><span data-stu-id="fab0a-129">Recent Items Properties</span></span>

<span data-ttu-id="fab0a-130">Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления "Недавние элементы".</span><span class="sxs-lookup"><span data-stu-id="fab0a-130">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Recent Items control.</span></span>

<span data-ttu-id="fab0a-131">Как правило, свойство недавние элементы обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="fab0a-131">Typically, a Recent Items property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="fab0a-132">Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="fab0a-132">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="fab0a-133">Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы.</span><span class="sxs-lookup"><span data-stu-id="fab0a-133">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="fab0a-134">Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.</span><span class="sxs-lookup"><span data-stu-id="fab0a-134">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="fab0a-135">В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="fab0a-135">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="fab0a-136">В следующей таблице перечислены ключи свойств, связанные с элементом управления "Недавние элементы".</span><span class="sxs-lookup"><span data-stu-id="fab0a-136">The following table lists the property keys that are associated with the Recent Items control.</span></span>



| <span data-ttu-id="fab0a-137">Ключ свойства</span><span class="sxs-lookup"><span data-stu-id="fab0a-137">Property Key</span></span>                                                                       | <span data-ttu-id="fab0a-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="fab0a-138">Notes</span></span>                                     |
|------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="fab0a-139">UI \_ PKEY \_ keytip</span><span class="sxs-lookup"><span data-stu-id="fab0a-139">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)           | <span data-ttu-id="fab0a-140">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="fab0a-140">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="fab0a-141">UI \_ PKEY \_ рецентитемс</span><span class="sxs-lookup"><span data-stu-id="fab0a-141">UI\_PKEY\_RecentItems</span></span>](windowsribbon-reference-properties-uipkey-recentitems.md) | <span data-ttu-id="fab0a-142">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="fab0a-142">Can only be updated through invalidation.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fab0a-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fab0a-143">Remarks</span></span>

<span data-ttu-id="fab0a-144">Метод [иаппликатиондокументлистс::/List](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) можно использовать для получения списка MRU оболочки Windows для приложения ленты.</span><span class="sxs-lookup"><span data-stu-id="fab0a-144">The [IApplicationDocumentLists::GetList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) method can be used to retrieve the Windows Shell MRU list for the Ribbon application.</span></span> <span data-ttu-id="fab0a-145">Объект, полученный этим методом, затем может использоваться приложением для создания данных, необходимых платформе Ribbon для заполнения списка **последних элементов** [меню приложения](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="fab0a-145">The object retrieved by this method can then be used by the application to create the data required by the Ribbon framework to populate the **Recent items** list of the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

> [!Note]  
> <span data-ttu-id="fab0a-146">При использовании этого метода *листтипе* должен иметь значение `ADLT_RECENT` .</span><span class="sxs-lookup"><span data-stu-id="fab0a-146">When using this method, *listtype* should have the value `ADLT_RECENT`.</span></span>

 

<span data-ttu-id="fab0a-147">Пример реализации списка MRU-элементов в приложении платформы Ribbon см. в примере [хтмледитриббон](windowsribbon-htmleditribbonsample.md).</span><span class="sxs-lookup"><span data-stu-id="fab0a-147">For an example of how to implement an MRU items list in a Ribbon framework application, see the [HTMLEditRibbon Sample](windowsribbon-htmleditribbonsample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fab0a-148">См. также</span><span class="sxs-lookup"><span data-stu-id="fab0a-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fab0a-149">Библиотека элементов управления платформы Windows ленты</span><span class="sxs-lookup"><span data-stu-id="fab0a-149">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="fab0a-150">**Элемент разметки недавних элементов**</span><span class="sxs-lookup"><span data-stu-id="fab0a-150">**Recent items markup element**</span></span>](windowsribbon-element-recentitems.md)
</dt> </dl>

 

 