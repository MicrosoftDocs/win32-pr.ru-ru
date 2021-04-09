---
title: Запрос групп в домене
description: Группы могут размещаться в любом контейнере или подразделении в домене, а также в корне домена.
ms.assetid: 338a93dd-445d-4f74-a6d6-e5c8ba2e765e
ms.tgt_platform: multiple
keywords:
- Запрос групп в доменных службах Active Directory
- Группы AD, запросы групп в домене
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3abd4ec393fbeca1308ed59e08131b9b73e6b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103890384"
---
# <a name="querying-for-groups-in-a-domain"></a><span data-ttu-id="19872-105">Запрос групп в домене</span><span class="sxs-lookup"><span data-stu-id="19872-105">Querying for Groups in a Domain</span></span>

<span data-ttu-id="19872-106">Группы могут размещаться в любом контейнере или подразделении в домене, а также в корне домена.</span><span class="sxs-lookup"><span data-stu-id="19872-106">Groups can be placed in any container or organizational unit in a domain as well as the root of the domain.</span></span> <span data-ttu-id="19872-107">Группы могут не всегда находиться в одном контейнере.</span><span class="sxs-lookup"><span data-stu-id="19872-107">Groups may not always be in one container.</span></span> <span data-ttu-id="19872-108">Таким образом, для поиска всех групп в домене необходимо выполнить поиск по всему домену.</span><span class="sxs-lookup"><span data-stu-id="19872-108">Therefore, it is necessary to search the entire domain to find all groups in the domain.</span></span>

<span data-ttu-id="19872-109">Чтобы найти все группы в домене, установите начальную точку поиска в корень домена, задайте для области поиска поддерево и найдите все объекты, имеющие значение [**objectClass**](/windows/desktop/ADSchema/a-objectclass) "Group".</span><span class="sxs-lookup"><span data-stu-id="19872-109">To search for all groups in a domain, set the search start point to the root of the domain, set the search scope to subtree and search for all objects that have an [**objectClass**](/windows/desktop/ADSchema/a-objectclass) value of "group".</span></span>

<span data-ttu-id="19872-110">Если необходимо найти группы, содержащие конкретные значения [**\_ \_ \_ перечисления типов групп баннеров**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) , то для поиска групп с определенными битами, заданными в атрибуте [**groupType**](/windows/desktop/ADSchema/a-grouptype) , можно использовать **\_ \_ бит правила сопоставления LDAP \_ \_ и** оператор правила сопоставления.</span><span class="sxs-lookup"><span data-stu-id="19872-110">If groups that contain particular [**ADS\_GROUP\_TYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) values must be found, the **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule operator can be used to search for groups that have particular bits set in the [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute.</span></span> <span data-ttu-id="19872-111">Дополнительные сведения об использовании правил сопоставления см. в разделе [синтаксис фильтра поиска](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="19872-111">For more information about using matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="19872-112">Дополнительные сведения и пример кода, демонстрирующий Поиск групп в домене, см. в разделе [пример кода для поиска групп в домене](example-code-for-performing-a-query-in-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="19872-112">For more information and a code example that shows how to search for groups in a domain, see [Example Code for Searching for Groups in a Domain](example-code-for-performing-a-query-in-a-domain.md).</span></span>

 

 