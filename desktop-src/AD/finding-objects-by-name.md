---
title: Поиск объектов по имени
description: Большинство объектов в службах домен Active Directory используют свойство CN в качестве атрибута именования.
ms.assetid: c5df7403-23bc-440e-8cd6-215ab8037aed
ms.tgt_platform: multiple
keywords:
- Active Directory, использование, поиск по имени
- объект Active Directory, поиск по имени
- Поиск объектов по имени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914faa443402a1d20698aabaf0bf4a112279a322
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773154"
---
# <a name="finding-objects-by-name"></a><span data-ttu-id="f848b-106">Поиск объектов по имени</span><span class="sxs-lookup"><span data-stu-id="f848b-106">Finding Objects by Name</span></span>

<span data-ttu-id="f848b-107">Большинство объектов в службах домен Active Directory используют свойство **CN** в качестве атрибута именования.</span><span class="sxs-lookup"><span data-stu-id="f848b-107">Most objects in Active Directory Domain Services use the **cn** property as their naming attribute.</span></span> <span data-ttu-id="f848b-108">Однако некоторые объекты используют атрибут именования, отличный от **CN**.</span><span class="sxs-lookup"><span data-stu-id="f848b-108">Some objects, however, use a naming attribute other than **cn**.</span></span> <span data-ttu-id="f848b-109">Например, контроллер домена использует свойство **домаинднс** для атрибута именования, а подразделение использует свойство **OrganizationalUnit** для атрибута именования.</span><span class="sxs-lookup"><span data-stu-id="f848b-109">For example, a domain controller uses the **domainDNS** property for the naming attribute and an organizational unit uses the **organizationalUnit** property for the naming attribute.</span></span> <span data-ttu-id="f848b-110">Чтобы не использовать другой атрибут именования для различных типов объектов, для поиска объектов по имени следует использовать свойство **Name** , которое содержит относительное различающееся имя объекта.</span><span class="sxs-lookup"><span data-stu-id="f848b-110">To avoid having to use a different naming attribute for different object types, the **name** property, which contains the relative distinguished name of the object, should be used to search for objects by name.</span></span>

## <a name="examples"></a><span data-ttu-id="f848b-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="f848b-111">Examples</span></span>

<span data-ttu-id="f848b-112">В следующем примере кода показаны различные строки запроса, которые можно использовать для поиска объектов по имени.</span><span class="sxs-lookup"><span data-stu-id="f848b-112">The following code examples show different query strings that can be used to find objects by name.</span></span>

<span data-ttu-id="f848b-113">Следующая строка запроса находит все объекты с именем, которое начинается с «Джеффа».</span><span class="sxs-lookup"><span data-stu-id="f848b-113">The following query string finds all objects with a name that begins with "Jeff".</span></span>


```C++
(name=Jeff*)
```



<span data-ttu-id="f848b-114">Следующая строка запроса находит все объекты-компьютеры с именем, которое начинается с "арендовано" или "Corp".</span><span class="sxs-lookup"><span data-stu-id="f848b-114">The following query string finds all computer objects with a name that begins with "leased" or "corp".</span></span>


```C++
(&(objectCategory=computer)(|(name=leased*)(name=corp*)))
```



<span data-ttu-id="f848b-115">Следующая строка запроса находит всех пользователей и с именем, которое начинается с "Карен" или "Джефф".</span><span class="sxs-lookup"><span data-stu-id="f848b-115">The following query string finds all users and with a name that begins with "Karen" or "Jeff".</span></span>


```C++
(&(&(objectClass=user)(objectCategory=person))(|(name=Karen*)(name=Jeff*)))
```



 

 




