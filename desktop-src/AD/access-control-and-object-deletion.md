---
title: Управление доступом и удаление объектов
description: Active Directory позволяет удалить объект, если у вас есть доступ на удаление объекта или ADS \_ справа \_ DS \_ Удаление \_ дочернего объекта к типу объектов в родительском контейнере.
ms.assetid: 87027c25-e3c9-4bad-8df3-cb6205e40ef6
ms.tgt_platform: multiple
keywords:
- Управление доступом и удаление объектов AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bddcd2b563e144743689f2a26c17bd417db14ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789432"
---
# <a name="access-control-and-object-deletion"></a><span data-ttu-id="37d2c-104">Управление доступом и удаление объектов</span><span class="sxs-lookup"><span data-stu-id="37d2c-104">Access Control and Object Deletion</span></span>

<span data-ttu-id="37d2c-105">Домен Active Directory службы позволяют удалить объект, если у вас есть одно из следующих прав доступа:</span><span class="sxs-lookup"><span data-stu-id="37d2c-105">Active Directory Domain Services enable you to delete an object if you have one of the following access rights:</span></span>

-   <span data-ttu-id="37d2c-106">Удаление доступа к самому объекту</span><span class="sxs-lookup"><span data-stu-id="37d2c-106">DELETE access to the object itself</span></span>
-   <span data-ttu-id="37d2c-107">Реклама \_ справа \_ DS \_ Удаление \_ дочернего объекта для этого типа объектов в родительском контейнере</span><span class="sxs-lookup"><span data-stu-id="37d2c-107">ADS\_RIGHT\_DS\_DELETE\_CHILD access for that object type on the parent container</span></span>

<span data-ttu-id="37d2c-108">Имейте в виду, что система проверяет дескриптор безопасности как для объекта, так и для его родителя перед запретом на удаление.</span><span class="sxs-lookup"><span data-stu-id="37d2c-108">Be aware that the system verifies the security descriptor for both the object and its parent before denying the deletion.</span></span> <span data-ttu-id="37d2c-109">Это означает, что элемент управления доступом, который явно запрещает доступ DELETE к пользователю, не оказывает никакого влияния, если пользователь УДАЛЯЕТ \_ дочерний доступ к родительскому объекту.</span><span class="sxs-lookup"><span data-stu-id="37d2c-109">This means that an ACE that explicitly denies DELETE access to a user has no effect if the user has DELETE\_CHILD access on the parent.</span></span> <span data-ttu-id="37d2c-110">Аналогично, элемент управления доступом, который запрещает удаление \_ дочернего объекта в родительском объекте, может быть переопределен, если разрешен доступ на удаление к самому объекту.</span><span class="sxs-lookup"><span data-stu-id="37d2c-110">Similarly, an ACE that denies DELETE\_CHILD access on the parent can be overridden if DELETE access is allowed on the object itself.</span></span>

<span data-ttu-id="37d2c-111">Чтобы выполнить операцию удаления дерева, например с помощью метода [**иадсделетеопс::D елетеобжект**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) , необходимо иметь AD \_ \_ DS right Directory \_ DELETE \_ доступ к объекту.</span><span class="sxs-lookup"><span data-stu-id="37d2c-111">To perform a tree-delete operation, for example using the [**IADsDeleteOps::DeleteObject**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) method, you must have ADS\_RIGHT\_DS\_DELETE\_TREE access to the object.</span></span> <span data-ttu-id="37d2c-112">При наличии этого права доступа можно удалить объект и все дочерние объекты независимо от защиты дочерних объектов.</span><span class="sxs-lookup"><span data-stu-id="37d2c-112">If you have this access right, you can delete the object and any child objects regardless of the protections on the child objects.</span></span> <span data-ttu-id="37d2c-113">Чтобы удалить дерево, если у вас нет ADS с \_ \_ доступом к дереву доменных служб Active Directory \_ \_ , необходимо выполнить рекурсивный обход дерева, удалив каждый объект по отдельности.</span><span class="sxs-lookup"><span data-stu-id="37d2c-113">To delete a tree if you do not have ADS\_RIGHT\_DS\_DELETE\_TREE access, you must recursively traverse the tree, deleting each object individually.</span></span> <span data-ttu-id="37d2c-114">В этом случае необходимо иметь доступ на удаление или удаление \_ дочернего элемента для каждого объекта в дереве.</span><span class="sxs-lookup"><span data-stu-id="37d2c-114">In this case, you must have the necessary DELETE or DELETE\_CHILD access for each object in the tree.</span></span>

> [!WARNING]
> <span data-ttu-id="37d2c-115">Если у пользователей есть \_ права \_ доступа к дереву доменных служб Active Directory \_ \_ для объекта, это дает возможность удалить все поддерево, включая все дочерние объекты.</span><span class="sxs-lookup"><span data-stu-id="37d2c-115">If users have ADS\_RIGHT\_DS\_DELETE\_TREE access for an object, this gives them the ability to delete a whole subtree, including all child objects.</span></span> <span data-ttu-id="37d2c-116">По этой причине вы можете отменить разрешение на доступ "удаление поддерева" для всех пользователей в родительском контейнере.</span><span class="sxs-lookup"><span data-stu-id="37d2c-116">For this reason, you may consider revoking "Delete Subtree" access permission for all users on a parent container.</span></span>

 

 

 