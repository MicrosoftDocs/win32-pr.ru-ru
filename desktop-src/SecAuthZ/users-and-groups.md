---
description: Описание определения пользователей и групп в API диспетчера авторизации.
ms.assetid: 783be0b2-7894-4780-900d-98918f824a04
title: Пользователи и группы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c40ee9234fa8d6259282855011cfc3fc008d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651182"
---
# <a name="users-and-groups"></a><span data-ttu-id="9dcf0-103">Пользователи и группы</span><span class="sxs-lookup"><span data-stu-id="9dcf0-103">Users and Groups</span></span>

<span data-ttu-id="9dcf0-104">В диспетчере авторизации получатели политики авторизации представлены следующими группами:</span><span class="sxs-lookup"><span data-stu-id="9dcf0-104">In Authorization Manager, recipients of authorization policy are represented by the following groups:</span></span>

-   <span data-ttu-id="9dcf0-105">Пользователи и группы Windows</span><span class="sxs-lookup"><span data-stu-id="9dcf0-105">Windows Users and Groups</span></span>

    <span data-ttu-id="9dcf0-106">К этим группам относятся пользователи, компьютеры и встроенные группы для субъектов безопасности.</span><span class="sxs-lookup"><span data-stu-id="9dcf0-106">These groups include users, computers, and built-in groups for security principals.</span></span>

-   <span data-ttu-id="9dcf0-107">Группы запросов LDAP</span><span class="sxs-lookup"><span data-stu-id="9dcf0-107">LDAP Query Groups</span></span>

    <span data-ttu-id="9dcf0-108">Членство в этих группах динамически вычисляется по мере необходимости из запросов LDAP.</span><span class="sxs-lookup"><span data-stu-id="9dcf0-108">Membership in these groups is dynamically calculated as needed from Lightweight Directory Access Protocol (LDAP) queries.</span></span> <span data-ttu-id="9dcf0-109">Группа запросов LDAP — это тип группы приложений.</span><span class="sxs-lookup"><span data-stu-id="9dcf0-109">An LDAP query group is a type of application group.</span></span>

-   <span data-ttu-id="9dcf0-110">Основные группы приложений</span><span class="sxs-lookup"><span data-stu-id="9dcf0-110">Basic Application Groups</span></span>

    <span data-ttu-id="9dcf0-111">Эти группы состоят из групп запросов LDAP, пользователей и групп Windows и других основных групп приложений.</span><span class="sxs-lookup"><span data-stu-id="9dcf0-111">These groups consist of LDAP query groups, Windows users and groups, and other basic application groups.</span></span>

## <a name="windows-users-and-groups"></a><span data-ttu-id="9dcf0-112">Пользователи и группы Windows</span><span class="sxs-lookup"><span data-stu-id="9dcf0-112">Windows Users and Groups</span></span>

<span data-ttu-id="9dcf0-113">Они совпадают с пользователями и группами, используемыми во всей операционной системе Windows.</span><span class="sxs-lookup"><span data-stu-id="9dcf0-113">These are the same as the users and groups used throughout the Windows operating system.</span></span>

## <a name="ldap-query-groups"></a><span data-ttu-id="9dcf0-114">Группы запросов LDAP</span><span class="sxs-lookup"><span data-stu-id="9dcf0-114">LDAP Query Groups</span></span>

<span data-ttu-id="9dcf0-115">В диспетчере авторизации можно использовать запросы LDAP для сопоставления атрибутов пользователя с объектами пользователя в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9dcf0-115">In Authorization Manager, you can use LDAP queries to match the user's attributes with those of the user's object in Active Directory.</span></span>

<span data-ttu-id="9dcf0-116">Например, следующий запрос находит всех, кроме Энди.</span><span class="sxs-lookup"><span data-stu-id="9dcf0-116">For example, the following query finds everyone except Andy.</span></span>


```C++
(&(objectCategory=person)(objectClass=user)(!cn=andy))
```



<span data-ttu-id="9dcf0-117">Следующий запрос находит всех членов псевдонима лица по адресу www.fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="9dcf0-117">The following query finds all members of the someone alias at www.fabrikam.com.</span></span>


```C++
(memberOf=CN=someone,OU=litwareinc,DC=Fabrikam,DC=com)
```



## <a name="basic-application-groups"></a><span data-ttu-id="9dcf0-118">Основные группы приложений</span><span class="sxs-lookup"><span data-stu-id="9dcf0-118">Basic Application Groups</span></span>

<span data-ttu-id="9dcf0-119">В API диспетчера авторизации группа приложений представляется объектом [**иазаппликатионграуп**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .</span><span class="sxs-lookup"><span data-stu-id="9dcf0-119">In the Authorization Manager API, an application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span> <span data-ttu-id="9dcf0-120">Основная группа приложений — это тип группы приложений.</span><span class="sxs-lookup"><span data-stu-id="9dcf0-120">A basic application group is a type of application group.</span></span>

<span data-ttu-id="9dcf0-121">Чтобы определить основное членство в группе приложений, определите, кто является членом, и определите, кто не является членом.</span><span class="sxs-lookup"><span data-stu-id="9dcf0-121">To define basic application group membership, define who is a member and define who is not a member.</span></span> <span data-ttu-id="9dcf0-122">Оба эти действия выполняются аналогичным образом.</span><span class="sxs-lookup"><span data-stu-id="9dcf0-122">Both of these steps are carried out in the same way.</span></span> <span data-ttu-id="9dcf0-123">Укажите ноль или несколько пользователей и групп Windows, ранее определенных основных групп приложений или групп запросов LDAP.</span><span class="sxs-lookup"><span data-stu-id="9dcf0-123">Specify zero or more Windows users and groups, previously defined basic application groups, or LDAP query groups.</span></span> <span data-ttu-id="9dcf0-124">Членство базовой группы приложений вычисляется путем удаления всех нечленов группы.</span><span class="sxs-lookup"><span data-stu-id="9dcf0-124">The membership of the basic application group is calculated by removing any nonmembers from the group.</span></span> <span data-ttu-id="9dcf0-125">Диспетчер авторизации выполняет это автоматически во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="9dcf0-125">Authorization Manager does this automatically at run time.</span></span>

<span data-ttu-id="9dcf0-126">Нечленство в базовой группе приложений имеет более высокий приоритет, чем принадлежность.</span><span class="sxs-lookup"><span data-stu-id="9dcf0-126">Nonmembership in a basic application group takes precedence over membership.</span></span>

<span data-ttu-id="9dcf0-127">Циклическое определение членства не разрешено; в результате появляется следующее сообщение об ошибке: "не удается добавить GroupName.</span><span class="sxs-lookup"><span data-stu-id="9dcf0-127">Circular membership definitions are not allowed; they result in the following error message: "Cannot add GroupName.</span></span> <span data-ttu-id="9dcf0-128">Произошла следующая проблема: обнаружен цикл.</span><span class="sxs-lookup"><span data-stu-id="9dcf0-128">The following problem occurred: A loop has been detected."</span></span>

## <a name="related-topics"></a><span data-ttu-id="9dcf0-129">См. также</span><span class="sxs-lookup"><span data-stu-id="9dcf0-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dcf0-130">Определение групп пользователей в C++</span><span class="sxs-lookup"><span data-stu-id="9dcf0-130">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)
</dt> </dl>

 

 



