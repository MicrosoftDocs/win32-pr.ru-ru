---
title: Поиск объектов по классу
description: Типичные поисковые запросы для конкретного класса объектов.
ms.assetid: 1805f98a-7e6b-4b4a-b173-dfb5d17e539a
ms.tgt_platform: multiple
keywords:
- Поиск объектов по классу AD
- Active Directory, использование, поиск по классу
- объект Active Directory, поиск по классу
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172c8b150090fae83aee1cf3e0f6a63a0e21dec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654187"
---
# <a name="finding-objects-by-class"></a><span data-ttu-id="06ef0-106">Поиск объектов по классу</span><span class="sxs-lookup"><span data-stu-id="06ef0-106">Finding Objects by Class</span></span>

<span data-ttu-id="06ef0-107">Типичные поисковые запросы для конкретного класса объектов.</span><span class="sxs-lookup"><span data-stu-id="06ef0-107">A typical search queries for a specific object class.</span></span> <span data-ttu-id="06ef0-108">В следующем примере кода выполняется поиск компьютеров с расположением в сборке 7N.</span><span class="sxs-lookup"><span data-stu-id="06ef0-108">The following code example searches for computers with location in Building 7N.</span></span>


```C++
(&(objectCategory=computer)(location=Building 7N))
```



<span data-ttu-id="06ef0-109">Рассмотрим, почему не используется **objectClass** .</span><span class="sxs-lookup"><span data-stu-id="06ef0-109">Consider why **objectClass** is not used.</span></span> <span data-ttu-id="06ef0-110">Не используйте **objectClass** без другого сравнения, содержащего индексированный атрибут.</span><span class="sxs-lookup"><span data-stu-id="06ef0-110">Do not use **objectClass** without another comparison that contains an indexed attribute.</span></span> <span data-ttu-id="06ef0-111">Атрибуты индекса могут повысить эффективность запроса.</span><span class="sxs-lookup"><span data-stu-id="06ef0-111">Index attributes can increase the efficiency of a query.</span></span> <span data-ttu-id="06ef0-112">Атрибут **objectClass** имеет несколько значений и не индексируется.</span><span class="sxs-lookup"><span data-stu-id="06ef0-112">The **objectClass** attribute is multi-valued and not indexed.</span></span> <span data-ttu-id="06ef0-113">Чтобы указать тип или класс объекта, используйте **objectCategory**.</span><span class="sxs-lookup"><span data-stu-id="06ef0-113">To specify the type or class of an object, use **objectCategory**.</span></span>

<span data-ttu-id="06ef0-114">Менее эффективно:</span><span class="sxs-lookup"><span data-stu-id="06ef0-114">Less efficient:</span></span>


```C++
(objectClass=computer)
```



<span data-ttu-id="06ef0-115">Более эффективно:</span><span class="sxs-lookup"><span data-stu-id="06ef0-115">More Efficient:</span></span>


```C++
(objectCategory=computer)
```



<span data-ttu-id="06ef0-116">Имейте в виду, что в некоторых случаях необходимо использовать сочетание **objectClass** и **objectCategory** .</span><span class="sxs-lookup"><span data-stu-id="06ef0-116">Be aware that there are some cases where a combination of **objectClass** and **objectCategory** must be used.</span></span> <span data-ttu-id="06ef0-117">Класс пользователя и класс Contact должны быть указаны следующим образом.</span><span class="sxs-lookup"><span data-stu-id="06ef0-117">The user class and contact class should be specified as follows.</span></span>


```C++
(&(objectClass=user)(objectCategory=person))
 
(&(objectClass=contact)(objectCategory=person))
```



<span data-ttu-id="06ef0-118">Имейте в виду, что можно искать как пользователей, так и контакты в следующих случаях.</span><span class="sxs-lookup"><span data-stu-id="06ef0-118">Be aware that you could search for both users and contacts with the following.</span></span>


```C++
(objectCategory=person)
```



 

 




