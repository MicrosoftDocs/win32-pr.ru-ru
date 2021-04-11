---
description: Заполнение коллекций COM+
ms.assetid: df86cbab-dcb8-46ac-aebf-8516276b6e81
title: Заполнение коллекций COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521d85521eb7e3750d06920a570ddeaf4d7e9b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342252"
---
# <a name="populating-com-collections"></a><span data-ttu-id="31ce2-103">Заполнение коллекций COM+</span><span class="sxs-lookup"><span data-stu-id="31ce2-103">Populating COM+ Collections</span></span>

<span data-ttu-id="31ce2-104">После получения коллекции и перед непосредственной работой с элементами, которые она содержит, необходимо заполнить коллекцию с помощью метода [**заполнения**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) .</span><span class="sxs-lookup"><span data-stu-id="31ce2-104">After you have retrieved a collection and before you can work directly with the items it contains, you must populate the collection by using the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method.</span></span> <span data-ttu-id="31ce2-105">Это приведет к получению данных для содержимого коллекции из каталога COM+.</span><span class="sxs-lookup"><span data-stu-id="31ce2-105">This fetches data for the collection's contents from the COM+ catalog.</span></span>

<span data-ttu-id="31ce2-106">Важно понимать, что при использовании объектов Комадмин для управления элементами или данными в коллекциях вы фактически работаете с временными кэшированными данными. Вы не работаете непосредственно с сохраненным каталогом.</span><span class="sxs-lookup"><span data-stu-id="31ce2-106">It is important to understand that whenever you use the COMAdmin objects to manipulate items or data in collections, you are really working on transiently cached data; you are not working directly with the persisted catalog.</span></span> <span data-ttu-id="31ce2-107">Действия, выполняемые с коллекцией или любыми ее элементами, отражаются в каталоге до тех пор, пока не будет вызван метод [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="31ce2-107">Nothing that you do with a collection or any of its items is reflected on the catalog until you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on the collection.</span></span> <span data-ttu-id="31ce2-108">Дополнительные сведения см. в разделе [Сохранение или удаление изменений](saving-or-discarding-changes.md).</span><span class="sxs-lookup"><span data-stu-id="31ce2-108">For more detail, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="31ce2-109">Все последующие вызовы, которые необходимо [**заполнить**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate)до вызова команды [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), влияют на отмену ожидающих изменений для всех элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="31ce2-109">Any subsequent calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate), prior to calling [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), has the effect of discarding pending changes to all items in the collection.</span></span> <span data-ttu-id="31ce2-110">**Заполнение** всегда заполняет кэш, с которым вы работаете, независимо от того, какие данные сохраняются в базовом хранилище данных каталога.</span><span class="sxs-lookup"><span data-stu-id="31ce2-110">**Populate** always populates the cache you're working in with whatever data is persisted on the underlying catalog data store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31ce2-111">См. также</span><span class="sxs-lookup"><span data-stu-id="31ce2-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31ce2-112">Навигация по иерархии коллекции COM+</span><span class="sxs-lookup"><span data-stu-id="31ce2-112">Navigating the COM+ Collection Hierarchy</span></span>](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="31ce2-113">Запросы к доступным связанным коллекциям</span><span class="sxs-lookup"><span data-stu-id="31ce2-113">Querying for Available Related Collections</span></span>](querying-for-available-related-collections.md)
</dt> <dt>

[<span data-ttu-id="31ce2-114">Получение коллекций в каталоге COM+</span><span class="sxs-lookup"><span data-stu-id="31ce2-114">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



