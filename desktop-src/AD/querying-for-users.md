---
title: Запросы пользователей
description: Для запроса пользователя запрос должен содержать выражение поиска \ 0034;( (пользователь objectClass) (objectCategory Person)) \ 0034;.
ms.assetid: a9f12de4-e1e2-41bb-b2cc-ff9c9fa1c39a
ms.tgt_platform: multiple
keywords:
- Пользователи AD, запросы пользователей
- Active Directory, использование, пользователи, запросы для пользователей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39037ff805dab753aae066d1f6611432b28ea73c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789493"
---
# <a name="querying-for-users"></a><span data-ttu-id="a681c-105">Запросы пользователей</span><span class="sxs-lookup"><span data-stu-id="a681c-105">Querying for Users</span></span>

<span data-ttu-id="a681c-106">Для запроса пользователя запрос должен содержать выражение поиска "(& (objectClass = пользователь) (objectCategory = Person))".</span><span class="sxs-lookup"><span data-stu-id="a681c-106">To query for a user, the query must contain the search expression "(&(objectClass=user)(objectCategory=person))".</span></span>

<span data-ttu-id="a681c-107">Поскольку класс Computer является подклассом пользователя, запрос, содержащий только (objectClass = User), возвращает объекты пользователя и объекты-компьютеры.</span><span class="sxs-lookup"><span data-stu-id="a681c-107">Because the computer class is a subclass of user, a query containing only (objectClass=user) would return user objects and computer objects.</span></span> <span data-ttu-id="a681c-108">Кроме того, категория объектов пользователя имеет значение Person (не пользователь); Таким образом, выражение (objectCategory = User) не возвращает пользователей.</span><span class="sxs-lookup"><span data-stu-id="a681c-108">Also, the object category of the user object is person (not user); therefore, the expression (objectCategory=user) does not return any users.</span></span> <span data-ttu-id="a681c-109">При использовании выражения (objectCategory = Person) запрос возвращает объекты пользователей и объекты-контакты.</span><span class="sxs-lookup"><span data-stu-id="a681c-109">If you use the expression (objectCategory=person), the query returns user objects and contact objects.</span></span>

<span data-ttu-id="a681c-110">Пользователи могут размещаться в любом контейнере или подразделении в домене, а также в корне домена.</span><span class="sxs-lookup"><span data-stu-id="a681c-110">Users can be placed in any container or organizational unit in a domain as well as the root of the domain.</span></span> <span data-ttu-id="a681c-111">Это означает, что пользователи могут находиться в нескольких местах иерархии каталогов.</span><span class="sxs-lookup"><span data-stu-id="a681c-111">This means that users can be in numerous locations in the directory hierarchy.</span></span> <span data-ttu-id="a681c-112">Можно выполнить глубокий поиск "(objectCategory = User)", чтобы найти всех пользователей в контейнере, подразделении, домене, доменном дереве или лесу, в зависимости от объекта, с которым связан указатель [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="a681c-112">You can perform a deep search for "(objectCategory=user)" to find all users in a container, organizational unit, domain, domain tree, or forest—depending on the object that the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer you are using is bound to.</span></span>

 

 