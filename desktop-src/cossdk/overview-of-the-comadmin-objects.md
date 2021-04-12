---
description: Объекты Комадмин предлагают простую объектную модель, которая предоставляет доступ к каталогу COM+.
ms.assetid: 84cee7a7-f7a6-41a0-afd5-fae56365612e
title: Общие сведения об объектах Комадмин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22837cbe0548b623463234d1a03d17288eba2149
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142961"
---
# <a name="overview-of-the-comadmin-objects"></a><span data-ttu-id="83fbd-103">Общие сведения об объектах Комадмин</span><span class="sxs-lookup"><span data-stu-id="83fbd-103">Overview of the COMAdmin Objects</span></span>

<span data-ttu-id="83fbd-104">Объекты Комадмин предлагают простую объектную модель, которая предоставляет доступ к каталогу COM+.</span><span class="sxs-lookup"><span data-stu-id="83fbd-104">The COMAdmin objects offer a simple object model that provides you with access to the COM+ catalog.</span></span> <span data-ttu-id="83fbd-105">При этом они служат для моделирования всех функциональных возможностей, предоставляемых средством администрирования служб компонентов.</span><span class="sxs-lookup"><span data-stu-id="83fbd-105">In doing so, they serve to model all the functionality provided by the Component Services administrative tool.</span></span> <span data-ttu-id="83fbd-106">Всякий раз, когда вы выполняете администрирование COM+, вы взаимодействуете с каталогом COM+.</span><span class="sxs-lookup"><span data-stu-id="83fbd-106">Whenever you do any kind of COM+ administration, you are interacting with the COM+ catalog.</span></span> <span data-ttu-id="83fbd-107">Описание каталога см. в разделе [доступ к каталогу com+](accessing-the-com--catalog.md).</span><span class="sxs-lookup"><span data-stu-id="83fbd-107">For a description of the catalog, see [Accessing the COM+ Catalog](accessing-the-com--catalog.md).</span></span>

<span data-ttu-id="83fbd-108">Сведения, полученные из средства администрирования служб компонентов или с помощью объектов Комадмин, имеют одинаковую структуру, а действия, выполняемые в обоих контекстах, являются аналогичными.</span><span class="sxs-lookup"><span data-stu-id="83fbd-108">The information you obtain either from the Component Services administrative tool or by using the COMAdmin objects is structured similarly, and the actions you perform in either context are analogous.</span></span> <span data-ttu-id="83fbd-109">Базовой корреляцией между использованием оснастки "службы компонентов" и программного администрирования является то, что папки в дереве консоли оснастки соответствуют коллекциям в каталоге COM+.</span><span class="sxs-lookup"><span data-stu-id="83fbd-109">The basic correlation between using the Component Services snap-in and programmatic administration is that folders in the console tree of the snap-in correspond to collections in the COM+ catalog.</span></span> <span data-ttu-id="83fbd-110">То есть, так как каждая папка в оснастке содержит элементы всех видов; Например, **приложения COM+** содержат установленные приложения COM+ — каждая коллекция в каталоге COM+ содержит элементы единообразного вида.</span><span class="sxs-lookup"><span data-stu-id="83fbd-110">That is, just as each folder in the snap-in contains items all of a kind; for example, **COM+ Applications** holds installed COM+ applications—each collection in the COM+ catalog holds items of a uniform kind.</span></span> <span data-ttu-id="83fbd-111">Кроме того, так как каждый элемент в папке имеет свойства, которые можно установить на странице свойств, каждый элемент в коллекции предоставляет свойства, которые можно задать.</span><span class="sxs-lookup"><span data-stu-id="83fbd-111">Further, just as each item in a folder has properties that you can set on a property sheet, each item in a collection exposes properties that you can set.</span></span>

<span data-ttu-id="83fbd-112">Чтобы обеспечить возможность настройки объектов в этой структуре, объекты Комадмин предоставляют следующие средства:</span><span class="sxs-lookup"><span data-stu-id="83fbd-112">To enable you to configure objects within this structure, the COMAdmin objects provide you with the means to do the following:</span></span>

-   <span data-ttu-id="83fbd-113">Доступ к каталогу COM+</span><span class="sxs-lookup"><span data-stu-id="83fbd-113">Access the COM+ catalog</span></span>
-   <span data-ttu-id="83fbd-114">Доступ к коллекциям в каталоге</span><span class="sxs-lookup"><span data-stu-id="83fbd-114">Access collections in the catalog</span></span>
-   <span data-ttu-id="83fbd-115">Доступ к элементам в коллекциях</span><span class="sxs-lookup"><span data-stu-id="83fbd-115">Access items in collections</span></span>
-   <span data-ttu-id="83fbd-116">Доступ к свойствам элементов в коллекциях</span><span class="sxs-lookup"><span data-stu-id="83fbd-116">Access properties on the items in the collections</span></span>

<span data-ttu-id="83fbd-117">Для поддержки этих действий библиотека Комадмин предоставляет следующие три класса:</span><span class="sxs-lookup"><span data-stu-id="83fbd-117">To support these actions, the COMAdmin Library provides the following three classes:</span></span>

-   <span data-ttu-id="83fbd-118">[**Комадминкаталог**](comadmincatalog.md), который представляет каталог.</span><span class="sxs-lookup"><span data-stu-id="83fbd-118">[**COMAdminCatalog**](comadmincatalog.md), which represents the catalog itself.</span></span>
-   <span data-ttu-id="83fbd-119">[**Комадминкаталогколлектион**](comadmincatalogcollection.md), представляющий любую коллекцию.</span><span class="sxs-lookup"><span data-stu-id="83fbd-119">[**COMAdminCatalogCollection**](comadmincatalogcollection.md), which represents any collection.</span></span>
-   <span data-ttu-id="83fbd-120">[**Комадминкаталогобжект**](comadmincatalogobject.md), представляющий любой элемент в коллекции.</span><span class="sxs-lookup"><span data-stu-id="83fbd-120">[**COMAdminCatalogObject**](comadmincatalogobject.md), which represents any item in a collection.</span></span>

<span data-ttu-id="83fbd-121">Более полное описание этих классов см. в разделе [сводное описание классов комадмин](summary-description-of-the-comadmin-classes.md) этого раздела.</span><span class="sxs-lookup"><span data-stu-id="83fbd-121">For fuller descriptions of these classes, see [Summary Description of the COMAdmin Classes](summary-description-of-the-comadmin-classes.md) in this section.</span></span>

<span data-ttu-id="83fbd-122">Чтобы быстро получить представление о типичных действиях, выполняемых в программном администрировании, см. [вводный пример с использованием каталога администрирования com+](introductory-example-using-the-com--administration-catalog.md).</span><span class="sxs-lookup"><span data-stu-id="83fbd-122">To get a quick idea of typical actions you perform in programmatic administration, see [Introductory Example Using the COM+ Administration Catalog](introductory-example-using-the-com--administration-catalog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="83fbd-123">См. также</span><span class="sxs-lookup"><span data-stu-id="83fbd-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83fbd-124">Операции администрирования COM+ в транзакциях</span><span class="sxs-lookup"><span data-stu-id="83fbd-124">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="83fbd-125">Обработка ошибок администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="83fbd-125">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="83fbd-126">Вводный пример с использованием каталога администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="83fbd-126">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="83fbd-127">Получение коллекций в каталоге COM+</span><span class="sxs-lookup"><span data-stu-id="83fbd-127">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="83fbd-128">Установка свойств и сохранение изменений в каталоге COM+</span><span class="sxs-lookup"><span data-stu-id="83fbd-128">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



