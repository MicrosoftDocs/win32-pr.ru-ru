---
description: Каждый элемент в коллекции предоставляет свойства.
ms.assetid: d9af57ea-c5b3-4017-bdc2-e43b86b3ddcd
title: Изменение свойств в каталоге COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed2bade8886fe08bb7ed1ece179b35677569f1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807355"
---
# <a name="editing-properties-in-the-com-catalog"></a><span data-ttu-id="e6053-103">Изменение свойств в каталоге COM+</span><span class="sxs-lookup"><span data-stu-id="e6053-103">Editing Properties in the COM+ Catalog</span></span>

<span data-ttu-id="e6053-104">Каждый элемент в коллекции предоставляет свойства.</span><span class="sxs-lookup"><span data-stu-id="e6053-104">Each item in a collection exposes properties.</span></span> <span data-ttu-id="e6053-105">Эти свойства служат для хранения данных конфигурации для любого элемента, представляемого элементом.</span><span class="sxs-lookup"><span data-stu-id="e6053-105">These properties serve to hold configuration data for whatever element the item represents.</span></span> <span data-ttu-id="e6053-106">В средстве администрирования "службы компонентов" эти свойства отображаются на странице свойств, к которой можно получить доступ, щелкнув правой кнопкой мыши элемент в папке.</span><span class="sxs-lookup"><span data-stu-id="e6053-106">In the Component Services administrative tool, these properties appear on a property page that you access by right-clicking an item in a folder.</span></span>

<span data-ttu-id="e6053-107">Поскольку элементы в заданной коллекции представляют один и тот же тип предмета, эти элементы предоставляют набор свойств, которые согласованы по коллекции.</span><span class="sxs-lookup"><span data-stu-id="e6053-107">Because the items in a given collection all represent the same kind of thing, those items expose a set of properties that is consistent across the collection.</span></span> <span data-ttu-id="e6053-108">Например, коллекция [**Applications**](applications.md) предоставляет свойство Name, свойство AppID и т. д.</span><span class="sxs-lookup"><span data-stu-id="e6053-108">For example, the [**Applications**](applications.md) collection exposes a Name property, an AppID property, and so forth.</span></span> <span data-ttu-id="e6053-109">Это аналогично использованию для каждого приложения в средстве администрирования "службы компонентов" единообразно структурированной страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="e6053-109">This is analogous to how each application in the Component Services administrative tool has a consistently structured property page available for it.</span></span> <span data-ttu-id="e6053-110">Список свойств, доступных коллекции **приложений** , см. в разделе **приложения**.</span><span class="sxs-lookup"><span data-stu-id="e6053-110">For a list of properties available to the **Applications** collection, see **Applications**.</span></span> <span data-ttu-id="e6053-111">Список свойств, доступных для коллекции [**Components**](components.md) , см. в разделе **Components**.</span><span class="sxs-lookup"><span data-stu-id="e6053-111">For a list of properties available to the [**Components**](components.md) collection, see **Components**.</span></span>

<span data-ttu-id="e6053-112">Полный список свойств, предоставляемых элементами в каждой коллекции, см. в разделе [com+ Administration Collections](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="e6053-112">For a complete list of properties exposed by items in each collection, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="e6053-113">Элемент в коллекции представляется с помощью объекта, созданного из класса [**комадминкаталогобжект**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="e6053-113">You represent an item in a collection by using an object created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span> <span data-ttu-id="e6053-114">Этот объект позволяет задавать и получать любые свойства, предоставляемые элементом.</span><span class="sxs-lookup"><span data-stu-id="e6053-114">This object enables you to set and get any of the properties exposed by the item.</span></span> <span data-ttu-id="e6053-115">При задании свойств также возможно, что возможно попытаться использовать другой модуль записи в каталог COM+.</span><span class="sxs-lookup"><span data-stu-id="e6053-115">When setting properties, it is also possible that you might be contending with another writer to the COM+ catalog.</span></span> <span data-ttu-id="e6053-116">Дополнительные сведения см. в разделе [Получение и задание свойств](getting-and-setting-properties.md).</span><span class="sxs-lookup"><span data-stu-id="e6053-116">For more information, see [Getting and Setting Properties](getting-and-setting-properties.md).</span></span>

<span data-ttu-id="e6053-117">После задания свойств никакие изменения на самом деле не фиксируются до тех пор, пока не будут явно сохранены изменения.</span><span class="sxs-lookup"><span data-stu-id="e6053-117">After you have set properties, no changes are actually committed until you explicitly save changes.</span></span> <span data-ttu-id="e6053-118">Дополнительные сведения см. в разделе [Сохранение или удаление изменений](saving-or-discarding-changes.md).</span><span class="sxs-lookup"><span data-stu-id="e6053-118">For more information, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="e6053-119">При сохранении изменений каталог COM+ применяет некоторую логику конфигурации, чтобы не задавать параметры для несовместимых конфигураций.</span><span class="sxs-lookup"><span data-stu-id="e6053-119">When you save changes, the COM+ catalog enforces some configuration logic to ensure that you don't set things to incompatible configurations.</span></span> <span data-ttu-id="e6053-120">Он также изменяет некоторые свойства при явном изменении некоторых других свойств.</span><span class="sxs-lookup"><span data-stu-id="e6053-120">It also changes some properties for you when you explicitly change certain other properties.</span></span> <span data-ttu-id="e6053-121">Дополнительные сведения см. в разделе [взаимозависимости между свойствами](interdependencies-between-properties.md).</span><span class="sxs-lookup"><span data-stu-id="e6053-121">For more information, see [Interdependencies Between Properties](interdependencies-between-properties.md).</span></span>

<span data-ttu-id="e6053-122">Кроме того, в COM+ есть средство, которое позволяет динамически создавать запросы, чтобы узнать, какие свойства доступны для элементов в данной коллекции.</span><span class="sxs-lookup"><span data-stu-id="e6053-122">Additionally, COM+ has a facility that enables you to dynamically query to see what properties are available for the items in a given collection.</span></span> <span data-ttu-id="e6053-123">Дополнительные сведения см. в разделе [запрос доступных свойств](querying-for-available-properties.md).</span><span class="sxs-lookup"><span data-stu-id="e6053-123">For details, see [Querying for Available Properties](querying-for-available-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6053-124">См. также</span><span class="sxs-lookup"><span data-stu-id="e6053-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6053-125">Операции администрирования COM+ в транзакциях</span><span class="sxs-lookup"><span data-stu-id="e6053-125">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="e6053-126">Обработка ошибок администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="e6053-126">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="e6053-127">Вводный пример с использованием каталога администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="e6053-127">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="e6053-128">Общие сведения об объектах Комадмин</span><span class="sxs-lookup"><span data-stu-id="e6053-128">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="e6053-129">Получение коллекций в каталоге COM+</span><span class="sxs-lookup"><span data-stu-id="e6053-129">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



