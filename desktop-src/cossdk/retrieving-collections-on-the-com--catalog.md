---
description: Получение коллекций в каталоге COM+
ms.assetid: 7cd5c491-6c85-410f-845b-c2f7b4f2a560
title: Получение коллекций в каталоге COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cbf81bfedd4ba37b74b36e5ad9a8ad320e9c39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807174"
---
# <a name="retrieving-collections-on-the-com-catalog"></a><span data-ttu-id="2b631-103">Получение коллекций в каталоге COM+</span><span class="sxs-lookup"><span data-stu-id="2b631-103">Retrieving Collections on the COM+ Catalog</span></span>

<span data-ttu-id="2b631-104">Данные в каталоге COM+ хранятся в иерархии коллекций.</span><span class="sxs-lookup"><span data-stu-id="2b631-104">Data on the COM+ catalog is stored within a hierarchy of collections.</span></span> <span data-ttu-id="2b631-105">В средстве администрирования служб компонентов многие из этих коллекций отображаются в виде папок в дереве консоли.</span><span class="sxs-lookup"><span data-stu-id="2b631-105">In the Component Services administrative tool, many of these collections appear as folders in the console tree.</span></span> <span data-ttu-id="2b631-106">Коллекции, которые не отображаются как папки, доступны только программно.</span><span class="sxs-lookup"><span data-stu-id="2b631-106">Collections that don't appear as folders can be accessed only programmatically.</span></span> <span data-ttu-id="2b631-107">Коллекции служат контейнерами для элементов.</span><span class="sxs-lookup"><span data-stu-id="2b631-107">Collections serve as containers for items.</span></span> <span data-ttu-id="2b631-108">Все элементы в данной коллекции имеют одинаковый тип; то есть все они представляют один и тот же тип элемента, и в коллекции может быть произвольное число элементов.</span><span class="sxs-lookup"><span data-stu-id="2b631-108">The items in a given collection are all of a consistent type; that is, they all represent the same kind of element, and there can be an arbitrary number of items in a collection.</span></span> <span data-ttu-id="2b631-109">Например, коллекция [**приложений**](applications.md) содержит элемент для каждого приложения COM+, установленного на компьютере.</span><span class="sxs-lookup"><span data-stu-id="2b631-109">For example, the [**Applications**](applications.md) collection contains an item for each COM+ application that is installed on the machine.</span></span> <span data-ttu-id="2b631-110">Эта коллекция отображается в средстве администрирования в виде папки **приложения COM+** .</span><span class="sxs-lookup"><span data-stu-id="2b631-110">This collection appears in the administrative tool as the **COM+ Applications** folder.</span></span>

<span data-ttu-id="2b631-111">Коллекции выполняются в иерархической структуре, поскольку элементы, которые они содержат, следуют присущей последовательности включения.</span><span class="sxs-lookup"><span data-stu-id="2b631-111">The collections occur in a hierarchical structure because the elements they contain follow an innate order of inclusion.</span></span> <span data-ttu-id="2b631-112">Например, поскольку компоненты устанавливаются в приложение COM+, коллекция [**Components**](components.md) логически относящиеся в коллекции [**приложений**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="2b631-112">For example, because components are installed into a COM+ application, the [**Components**](components.md) collection is logically subsumed under the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="2b631-113">В частности, для хранения компонентов, установленных в этом конкретном приложении, существует отдельная коллекция **компонентов** для каждого элемента в коллекции **приложений** .</span><span class="sxs-lookup"><span data-stu-id="2b631-113">More particularly, to hold the components installed into that particular application, there is a distinct **Components** collection for each item in the **Applications** collection.</span></span>

<span data-ttu-id="2b631-114">Если требуется получить элемент и задать его свойства, необходимо получить коллекцию в каталоге.</span><span class="sxs-lookup"><span data-stu-id="2b631-114">You must get a collection on the catalog whenever you want to retrieve an item and set properties on it.</span></span> <span data-ttu-id="2b631-115">В общем случае необходимо выполнить шаг с заходом в несколько коллекций, чтобы перейти к нужному элементу.</span><span class="sxs-lookup"><span data-stu-id="2b631-115">In the general case, you need to step through several collections to get to the element you want.</span></span> <span data-ttu-id="2b631-116">Инструкции по выполнению этой процедуры см. [в разделе Навигация по иерархии коллекции com+](navigating-the-com--collection-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="2b631-116">For the procedure for doing this, see [Navigating the COM+ Collection Hierarchy](navigating-the-com--collection-hierarchy.md).</span></span>

<span data-ttu-id="2b631-117">После получения коллекции и перед тем, как работать непосредственно с элементами, которые она содержит, необходимо заполнить коллекцию, которая извлекает данные для содержимого коллекции из каталога COM+.</span><span class="sxs-lookup"><span data-stu-id="2b631-117">After you have retrieved a collection and before you can work directly with the items it contains, you must populate the collection, which fetches data for the collection's contents from the COM+ catalog.</span></span> <span data-ttu-id="2b631-118">Дополнительные сведения см. в разделе [Заполнение коллекций com+](populating-com--collections.md).</span><span class="sxs-lookup"><span data-stu-id="2b631-118">For details, see [Populating COM+ Collections](populating-com--collections.md).</span></span>

<span data-ttu-id="2b631-119">Кроме того, существует средство, которое позволяет динамически отправлять запросы, чтобы узнать, какие связанные коллекции доступны из данной коллекции.</span><span class="sxs-lookup"><span data-stu-id="2b631-119">Additionally, there is a facility you can use that enables you to dynamically query to see what related collections are available from a given collection you are holding.</span></span> <span data-ttu-id="2b631-120">Дополнительные сведения см. в разделе [запросы к доступным связанным коллекциям](querying-for-available-related-collections.md).</span><span class="sxs-lookup"><span data-stu-id="2b631-120">For details, see [Querying for Available Related Collections](querying-for-available-related-collections.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b631-121">См. также</span><span class="sxs-lookup"><span data-stu-id="2b631-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b631-122">Операции администрирования COM+ в транзакциях</span><span class="sxs-lookup"><span data-stu-id="2b631-122">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="2b631-123">Обработка ошибок администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="2b631-123">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="2b631-124">Вводный пример с использованием каталога администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="2b631-124">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="2b631-125">Общие сведения об объектах Комадмин</span><span class="sxs-lookup"><span data-stu-id="2b631-125">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="2b631-126">Установка свойств и сохранение изменений в каталоге COM+</span><span class="sxs-lookup"><span data-stu-id="2b631-126">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



