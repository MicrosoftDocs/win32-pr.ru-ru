---
description: Запросы к доступным связанным коллекциям
ms.assetid: 9c7d2a01-5dc3-4d35-b938-f1d0525a8286
title: Запросы к доступным связанным коллекциям
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0203df5bb7b5bf89396d5687dc28b19e9b183d56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342322"
---
# <a name="querying-for-available-related-collections"></a><span data-ttu-id="a8eea-103">Запросы к доступным связанным коллекциям</span><span class="sxs-lookup"><span data-stu-id="a8eea-103">Querying for Available Related Collections</span></span>

<span data-ttu-id="a8eea-104">При написании средства администрирования общего назначения, скорее всего, потребуется написать подпрограммы для навигации по всей иерархии коллекции.</span><span class="sxs-lookup"><span data-stu-id="a8eea-104">If you are writing a general-purpose administration tool, it is likely that you will need to write routines for navigating the entire collection hierarchy.</span></span> <span data-ttu-id="a8eea-105">Для этого в COM+ есть средство, которое позволяет динамически запрашивать связанные коллекции, доступные из любой заданной коллекции.</span><span class="sxs-lookup"><span data-stu-id="a8eea-105">To support this, COM+ has a facility that enables you to dynamically query for the related collections that are available from any given collection.</span></span>

<span data-ttu-id="a8eea-106">Коллекция [**релатедколлектионинфо**](relatedcollectioninfo.md) доступна из любой коллекции, которая может храниться, и содержит элемент для каждой доступной связанной коллекции.</span><span class="sxs-lookup"><span data-stu-id="a8eea-106">The [**RelatedCollectionInfo**](relatedcollectioninfo.md) collection is available from any collection that you might be holding and contains an item for each available related collection.</span></span> <span data-ttu-id="a8eea-107">Можно перечислить эти элементы, чтобы определить, доступна ли данная коллекция.</span><span class="sxs-lookup"><span data-stu-id="a8eea-107">You can enumerate through these items to determine whether a given collection is available.</span></span>

<span data-ttu-id="a8eea-108">Коллекцию [**релатедколлектионинфо**](relatedcollectioninfo.md) можно получить из любой коллекции, которую вы удерживаете, с помощью метода [**IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) . Второй параметр остается пустым, где обычно указывается свойство ключа родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="a8eea-108">You can get the [**RelatedCollectionInfo**](relatedcollectioninfo.md) collection from any collection you are holding by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8eea-109">См. также</span><span class="sxs-lookup"><span data-stu-id="a8eea-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8eea-110">Навигация по иерархии коллекции COM+</span><span class="sxs-lookup"><span data-stu-id="a8eea-110">Navigating the COM+ Collection Hierarchy</span></span>](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="a8eea-111">Заполнение коллекций COM+</span><span class="sxs-lookup"><span data-stu-id="a8eea-111">Populating COM+ Collections</span></span>](populating-com--collections.md)
</dt> <dt>

[<span data-ttu-id="a8eea-112">Получение коллекций в каталоге COM+</span><span class="sxs-lookup"><span data-stu-id="a8eea-112">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



