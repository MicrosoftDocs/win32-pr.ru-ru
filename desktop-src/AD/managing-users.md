---
title: Управление пользователями
description: Сведения об управлении пользователями. Учетные записи пользователей создаются и сохраняются в виде объектов в домен Active Directory Services.
ms.assetid: 57c83e4d-2d9f-4f22-97e2-27e2d277f014
ms.tgt_platform: multiple
keywords:
- Active Directory, использование, Управление пользователями
- Пользователи AD
- Пользователи AD, Управление пользователями
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8154dc9d062b86d10b0df6418b5b4cbb79b44d2
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395319"
---
# <a name="managing-users"></a><span data-ttu-id="5d27f-107">Управление пользователями</span><span class="sxs-lookup"><span data-stu-id="5d27f-107">Managing Users</span></span>

<span data-ttu-id="5d27f-108">Учетные записи пользователей создаются и сохраняются в виде объектов в домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="5d27f-108">User accounts are created and stored as objects in Active Directory Domain Services.</span></span> <span data-ttu-id="5d27f-109">Эти пользовательские объекты представляют пользователей и компьютеры.</span><span class="sxs-lookup"><span data-stu-id="5d27f-109">These user objects represent users and computers.</span></span> <span data-ttu-id="5d27f-110">В этом разделе определяется, какие пользователи и как они используются, а также объясняется, как программным образом управлять пользователями в службах домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5d27f-110">This section defines what users are and how they are used, and explains how to programmatically manage users in Active Directory Domain Services.</span></span> <span data-ttu-id="5d27f-111">В этом разделе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="5d27f-111">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="5d27f-112">Пользователи в службах домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="5d27f-112">Users in Active Directory Domain Services</span></span>](users-in-active-directory-domain-services.md)
-   [<span data-ttu-id="5d27f-113">Субъекты безопасности</span><span class="sxs-lookup"><span data-stu-id="5d27f-113">Security Principals</span></span>](security-principals.md)
-   [<span data-ttu-id="5d27f-114">Что такое пользователь?</span><span class="sxs-lookup"><span data-stu-id="5d27f-114">What is a User?</span></span>](what-is-a-user.md)
-   [<span data-ttu-id="5d27f-115">Пример кода для привязки к контейнеру Users</span><span class="sxs-lookup"><span data-stu-id="5d27f-115">Example Code for Binding to the Users Container</span></span>](example-code-for-binding-to-the-users-container.md)
-   [<span data-ttu-id="5d27f-116">Атрибуты объекта «пользователь»</span><span class="sxs-lookup"><span data-stu-id="5d27f-116">User Object Attributes</span></span>](user-object-attributes.md)
-   [<span data-ttu-id="5d27f-117">Создание пользователя</span><span class="sxs-lookup"><span data-stu-id="5d27f-117">Creating a User</span></span>](creating-a-user.md)
-   <span data-ttu-id="5d27f-118">Удаление пользователя.</span><span class="sxs-lookup"><span data-stu-id="5d27f-118">Deleting a user.</span></span> <span data-ttu-id="5d27f-119">Пользователь удаляется в том же самом, что и любой другой объект в службах домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="5d27f-119">A user is deleted in the same was as any other object in Active Directory Domain Services.</span></span> <span data-ttu-id="5d27f-120">Дополнительные сведения об удалении объектов см. [в разделе Создание и удаление объектов в домен Active Directory Services](creating-and-deleting-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="5d27f-120">For more information about deleting objects, see [Creating and Deleting Objects in Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md).</span></span>
-   [<span data-ttu-id="5d27f-121">Перечисление пользователей</span><span class="sxs-lookup"><span data-stu-id="5d27f-121">Enumerating Users</span></span>](enumerating-users.md)
-   [<span data-ttu-id="5d27f-122">Запросы пользователей</span><span class="sxs-lookup"><span data-stu-id="5d27f-122">Querying for Users</span></span>](querying-for-users.md)
-   <span data-ttu-id="5d27f-123">Перемещение пользователей.</span><span class="sxs-lookup"><span data-stu-id="5d27f-123">Moving users.</span></span> <span data-ttu-id="5d27f-124">Пользователь перемещается в том же виде, что и любой другой объект Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5d27f-124">A user is moved in the same was as any other Active Directory object.</span></span> <span data-ttu-id="5d27f-125">Дополнительные сведения о перемещении объектов Active Directory см. в разделе [Перемещение объектов](moving-objects.md).</span><span class="sxs-lookup"><span data-stu-id="5d27f-125">For more information about moving Active Directory objects, see [Moving Objects](moving-objects.md).</span></span>
-   [<span data-ttu-id="5d27f-126">Управление пользователями на рядовых серверах и Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5d27f-126">Managing Users on Member Servers and Windows 2000 Professional</span></span>](managing-users-on-member-servers-and-windows-2000-professional.md)

 

 




