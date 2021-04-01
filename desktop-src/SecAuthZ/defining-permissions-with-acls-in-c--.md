---
description: Определите, какие клиенты имеют доступ к каким ресурсам, создав и изменив списки ACL, связанные с этими ресурсами, а также включив и отключая права клиента.
ms.assetid: dc1c510d-f0d4-4d04-ba79-3aac1aaaf5d4
title: Определение разрешений с помощью списков ACL в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d9129e448f62998eb685c6607bc2e6ed29c035
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999089"
---
# <a name="defining-permissions-with-acls-in-c"></a><span data-ttu-id="cbdc9-103">Определение разрешений с помощью списков ACL в C++</span><span class="sxs-lookup"><span data-stu-id="cbdc9-103">Defining Permissions with ACLs in C++</span></span>

<span data-ttu-id="cbdc9-104">Списки ACL можно использовать для управления доступом к защищенным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="cbdc9-104">You can use ACLs to control access to protected resources.</span></span> <span data-ttu-id="cbdc9-105">Определите, какие клиенты имеют доступ к каким ресурсам, создав и изменив списки ACL, связанные с этими ресурсами, а также включив и отключая права клиента.</span><span class="sxs-lookup"><span data-stu-id="cbdc9-105">Define which clients have access to which resources by creating and modifying the ACLs associated with those resources and by enabling and disabling client privileges.</span></span>



| <span data-ttu-id="cbdc9-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="cbdc9-106">Topic</span></span>                                                                                                                | <span data-ttu-id="cbdc9-107">Описание</span><span class="sxs-lookup"><span data-stu-id="cbdc9-107">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbdc9-108">Изменение списков управления доступом объекта в C++</span><span class="sxs-lookup"><span data-stu-id="cbdc9-108">Modifying the ACLs of an Object in C++</span></span>](modifying-the-acls-of-an-object-in-c--.md)                                 | <span data-ttu-id="cbdc9-109">Добавление или удаление [*записи контроля доступа*](/windows/desktop/SecGloss/a-gly) (ACE) в [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) объекта.</span><span class="sxs-lookup"><span data-stu-id="cbdc9-109">Add or remove an [*access control entry*](/windows/desktop/SecGloss/a-gly) (ACE) to the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of an object.</span></span> |
| [<span data-ttu-id="cbdc9-110">Создание дескриптора безопасности для нового объекта в C++</span><span class="sxs-lookup"><span data-stu-id="cbdc9-110">Creating a Security Descriptor for a New Object in C++</span></span>](creating-a-security-descriptor-for-a-new-object-in-c--.md) | <span data-ttu-id="cbdc9-111">Создайте дескриптор безопасности для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="cbdc9-111">Create a security descriptor for a new object.</span></span>                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="cbdc9-112">Управление созданием дочерних объектов в C++</span><span class="sxs-lookup"><span data-stu-id="cbdc9-112">Controlling Child Object Creation in C++</span></span>](controlling-child-object-creation-in-c--.md)                             | <span data-ttu-id="cbdc9-113">Используйте список DACL объекта-контейнера для управления тем, кому разрешено создавать дочерние объекты в контейнере.</span><span class="sxs-lookup"><span data-stu-id="cbdc9-113">Use the DACL of a container object to control who is allowed to create child objects within the container.</span></span>                                                                                                                                                                                                              |
| [<span data-ttu-id="cbdc9-114">Включение и отключение привилегий в C++</span><span class="sxs-lookup"><span data-stu-id="cbdc9-114">Enabling and Disabling Privileges in C++</span></span>](enabling-and-disabling-privileges-in-c--.md)                             | <span data-ttu-id="cbdc9-115">Разрешает или запрещает процессу выполнять действия на уровне системы.</span><span class="sxs-lookup"><span data-stu-id="cbdc9-115">Allow or disallow a process to perform system-level actions.</span></span>                                                                                                                                                                                                                                                            |



 

 

 
