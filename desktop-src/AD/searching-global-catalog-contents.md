---
title: Поиск в глобальном каталоге
description: Домен Active Directory Services также имеют глобальный каталог (GC), который содержит частичную реплику всех объектов в каталоге.
ms.assetid: 83970563-1a56-4671-b264-56e29939e369
ms.tgt_platform: multiple
keywords:
- Поиск Active Directory в глобальном каталоге
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a057330309c12df6d18a209fc3d2adaf42b03005
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773094"
---
# <a name="searching-the-global-catalog"></a><span data-ttu-id="d2631-104">Поиск в глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d2631-104">Searching the Global Catalog</span></span>

<span data-ttu-id="d2631-105">Домен Active Directory Services также имеют глобальный каталог (GC), который содержит частичную реплику всех объектов в каталоге.</span><span class="sxs-lookup"><span data-stu-id="d2631-105">Active Directory Domain Services also have a global catalog (GC), which contains a partial replica of all objects in the directory.</span></span> <span data-ttu-id="d2631-106">Он также содержит частичные реплики для контейнеров схемы и конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d2631-106">It also contains partial replicas of the schema and configuration containers.</span></span> <span data-ttu-id="d2631-107">Один или несколько контроллеров домена в домене могут содержать копию глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="d2631-107">One or more domain controllers in a domain can hold a copy of the global catalog.</span></span> <span data-ttu-id="d2631-108">Дополнительные сведения о привязке к глобальному каталогу см. в разделе [Привязка к глобальному каталогу](binding-to-the-global-catalog.md).</span><span class="sxs-lookup"><span data-stu-id="d2631-108">For more information about binding to a global catalog, see [Binding to the Global Catalog](binding-to-the-global-catalog.md).</span></span>

<span data-ttu-id="d2631-109">Глобальный каталог содержит реплику каждого объекта в службах домен Active Directory Services, но с небольшим количеством их атрибутов.</span><span class="sxs-lookup"><span data-stu-id="d2631-109">The global catalog holds a replica of every object in Active Directory Domain Services, but with only a small number of their attributes.</span></span> <span data-ttu-id="d2631-110">Атрибуты в глобальном каталоге чаще всего используются в операциях поиска, таких как имена и фамилии пользователей, имена входа и т. д.</span><span class="sxs-lookup"><span data-stu-id="d2631-110">The attributes in the global catalog are those most frequently used in search operations, such as a user's first and last names, login names, and so on.</span></span> <span data-ttu-id="d2631-111">Атрибуты глобального каталога также включают в себя те, которые необходимы для нахождение полной реплики объекта.</span><span class="sxs-lookup"><span data-stu-id="d2631-111">The global catalog attributes also include those required to locate a full replica of the object.</span></span> <span data-ttu-id="d2631-112">Глобальный каталог позволяет пользователям быстро находить нужные объекты, не зная о том, в каком домене они хранятся, и не требуя наличия непрерывного расширенного пространства имен на предприятии. Это значит, что можно выполнять поиск по всему лесу.</span><span class="sxs-lookup"><span data-stu-id="d2631-112">The global catalog allows users to quickly find objects of interest without knowing what domain holds them and without requiring a contiguous extended namespace in the enterprise; that is, you can search the entire forest.</span></span>

<span data-ttu-id="d2631-113">Таким образом, при привязке к объекту в глобальном каталоге будет осуществляться поиск этого объекта и всей иерархии под ним — без необходимости перехода на другой сервер.</span><span class="sxs-lookup"><span data-stu-id="d2631-113">So, if you bind to an object in the global catalog, you will search that object and the entire hierarchy below it — without having to go to any other server.</span></span> <span data-ttu-id="d2631-114">Однако поиск может использовать только фильтр запросов, содержащий свойства в глобальном каталоге, и может извлекать только свойства из глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="d2631-114">However, the search can only use a query filter containing properties in the global catalog and can retrieve only properties in the global catalog.</span></span>

<span data-ttu-id="d2631-115">Поиск в глобальном каталоге имеет следующие преимущества.</span><span class="sxs-lookup"><span data-stu-id="d2631-115">Searching the global catalog has the following benefits:</span></span>

-   <span data-ttu-id="d2631-116">Глобальный каталог позволяет выполнять поиск по всему лесу или любой части леса, а также к контейнерам схемы и конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d2631-116">Global catalog enables you to search the entire forest or any part of the forest as well as the schema and configuration containers.</span></span>
-   <span data-ttu-id="d2631-117">Глобальный каталог позволяет выполнить полный поиск на одном сервере.</span><span class="sxs-lookup"><span data-stu-id="d2631-117">Global catalog enables you to perform a complete search on a single server.</span></span> <span data-ttu-id="d2631-118">Ссылки или отслеживание ссылок не требуются.</span><span class="sxs-lookup"><span data-stu-id="d2631-118">No referrals or referral chasing is required.</span></span>

<span data-ttu-id="d2631-119">Поиск в глобальном каталоге имеет следующие недостатки.</span><span class="sxs-lookup"><span data-stu-id="d2631-119">Searching the global catalog has the following disadvantages:</span></span>

-   <span data-ttu-id="d2631-120">Глобальный каталог содержит небольшое подмножество свойств для каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="d2631-120">Global catalog contains a small subset of the properties on each object.</span></span> <span data-ttu-id="d2631-121">Если фильтр запроса содержит свойства, которых нет в глобальном каталоге, запрос вычислит выражения, содержащие эти свойства, как false.</span><span class="sxs-lookup"><span data-stu-id="d2631-121">If your query filter includes properties that are not in the global catalog, the query will evaluate the expressions containing those properties as false.</span></span> <span data-ttu-id="d2631-122">При указании свойств неглобального каталога в списке возвращаемых свойств эти свойства не извлекаются.</span><span class="sxs-lookup"><span data-stu-id="d2631-122">If you specify non-global catalog properties in the list of properties to return, those properties are not retrieved.</span></span>
-   <span data-ttu-id="d2631-123">Для поиска в глобальном каталоге должен быть доступен контроллер домена, содержащий глобальный каталог.</span><span class="sxs-lookup"><span data-stu-id="d2631-123">To search the global catalog, a domain controller that contains a global catalog must be available.</span></span> <span data-ttu-id="d2631-124">Если он недоступен, выполнять поиск по глобальному каталогу нельзя.</span><span class="sxs-lookup"><span data-stu-id="d2631-124">If one is not available, you cannot perform a global catalog search.</span></span>
-   <span data-ttu-id="d2631-125">Глобальный каталог доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d2631-125">The global catalog is read-only.</span></span> <span data-ttu-id="d2631-126">Это означает, что вы не можете выполнить привязку к объекту в глобальном каталоге для создания, изменения или удаления объектов.</span><span class="sxs-lookup"><span data-stu-id="d2631-126">This means you cannot bind to an object in the global catalog to create, modify, or delete objects.</span></span>

 

 




