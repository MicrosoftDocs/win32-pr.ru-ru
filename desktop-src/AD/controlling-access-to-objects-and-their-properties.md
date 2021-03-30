---
title: Управление доступом к объектам и их свойствам
description: Для управления доступом к объектам приложения следует работать с дескриптором безопасности объекта, а именно со списком управления доступом (DACL) и списком записей управления доступом (ACE).
ms.assetid: cfcb0998-4400-45cd-bbee-415d43b96a99
ms.tgt_platform: multiple
keywords:
- объект Active Directory, управление доступом к
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4534f383fa3747e0a53b402098f5a8338812c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252727"
---
# <a name="controlling-access-to-objects-and-their-properties"></a><span data-ttu-id="ad2c9-104">Управление доступом к объектам и их свойствам</span><span class="sxs-lookup"><span data-stu-id="ad2c9-104">Controlling Access to Objects and Their Properties</span></span>

<span data-ttu-id="ad2c9-105">Для управления доступом к объектам приложения следует работать с дескриптором безопасности объекта, а именно со списком управления доступом (DACL) и списком записей управления доступом (ACE).</span><span class="sxs-lookup"><span data-stu-id="ad2c9-105">To control access to application objects, work with the object security descriptor, and specifically, with the discretionary access-control list (DACL) and its list of access-control entries (ACEs).</span></span>

<span data-ttu-id="ad2c9-106">При создании объекта он получает дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-106">When an object is created, it receives a security descriptor.</span></span> <span data-ttu-id="ad2c9-107">Дополнительные сведения и описание правил, которые система использует для создания списка DACL для нового объекта, см. [в разделе как устанавливаются дескрипторы безопасности для новых объектов каталога](how-security-descriptors-are-set-on-new-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ad2c9-107">For more information, and a description of the rules that the system uses to create the DACL for a new object, see [How Security Descriptors are Set on New Directory Objects](how-security-descriptors-are-set-on-new-directory-objects.md).</span></span> <span data-ttu-id="ad2c9-108">Эти правила показывают, что вы можете:</span><span class="sxs-lookup"><span data-stu-id="ad2c9-108">These rules reveal that you can:</span></span>

-   <span data-ttu-id="ad2c9-109">Создайте новый дескриптор безопасности и присоедините его к объекту во время создания.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-109">Create a new security descriptor and attach it to the object at creation time.</span></span> <span data-ttu-id="ad2c9-110">Дополнительные сведения см. в разделе [Создание дескриптора безопасности для нового объекта каталога](creating-a-security-descriptor-for-a-new-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="ad2c9-110">For more information, see [Creating a Security Descriptor for a New Directory Object](creating-a-security-descriptor-for-a-new-directory-object.md).</span></span>
-   <span data-ttu-id="ad2c9-111">Примените наследуемую запись ACE в любой точке иерархии каталогов, чтобы объекты ACE наследовались объектами вниз по дереву.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-111">Apply an inheritable ACE, at any point in the directory hierarchy, such that an ACE is inherited by objects down the tree.</span></span> <span data-ttu-id="ad2c9-112">Объект может наследовать ACE от родительского контейнера.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-112">An object can inherit an ACE from its parent container.</span></span> <span data-ttu-id="ad2c9-113">Дополнительные сведения см. в разделе [наследование и делегирование администрирования](inheritance-and-delegation-of-administration.md).</span><span class="sxs-lookup"><span data-stu-id="ad2c9-113">For more information, see [Inheritance and Delegation of Administration](inheritance-and-delegation-of-administration.md).</span></span>
-   <span data-ttu-id="ad2c9-114">Если у вас есть необходимые права доступа, укажите элемент ACE в списке DACL по умолчанию в схеме.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-114">Specify an ACE in the default DACL in the schema, if you have the necessary access rights.</span></span> <span data-ttu-id="ad2c9-115">Каждое определение класса объектов в схеме содержит дескриптор безопасности по умолчанию, который может иметь DACL по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-115">Every object class definition in the schema includes a default security descriptor that can have a default DACL.</span></span> <span data-ttu-id="ad2c9-116">Дополнительные сведения см. в разделе [дескриптор безопасности по умолчанию](default-security-descriptor.md).</span><span class="sxs-lookup"><span data-stu-id="ad2c9-116">For more information, see [Default Security Descriptor](default-security-descriptor.md).</span></span>

<span data-ttu-id="ad2c9-117">Кроме того, можно изменить список DACL существующего объекта.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-117">In addition the DACL of an existing object can be modified.</span></span> <span data-ttu-id="ad2c9-118">Вы можете:</span><span class="sxs-lookup"><span data-stu-id="ad2c9-118">You can:</span></span>

-   <span data-ttu-id="ad2c9-119">Замените список DACL новым.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-119">Replace the DACL with a new one.</span></span>
-   <span data-ttu-id="ad2c9-120">Прочтите существующий список DACL, измените его и примените измененный список DACL.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-120">Read the existing DACL, modify it, and apply the modified DACL.</span></span> <span data-ttu-id="ad2c9-121">Дополнительные сведения см. [в разделе Установка прав доступа для объекта](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="ad2c9-121">For more information, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="ad2c9-122">В следующем списке приводится наиболее важная функция ACE в домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-122">The following list describes the most important function of an ACE in Active Directory Domain Services.</span></span> <span data-ttu-id="ad2c9-123">С помощью элемента управления доступом можно выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ad2c9-123">With an ACE, you can:</span></span>

-   <span data-ttu-id="ad2c9-124">Управление доступом к объекту для выполнения конкретных операций.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-124">Control who can perform specific operations on an object.</span></span>
-   <span data-ttu-id="ad2c9-125">Управление доступом к определенному свойству или набору свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-125">Control who has access to a specific property, or set of properties, of an object.</span></span>
-   <span data-ttu-id="ad2c9-126">Управление тем, кто может создавать дочерние объекты в контейнере, в том числе о том, кто может создавать дочерний объект определенного типа.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-126">Control who can create child objects in a container, including who can create a specific type of child object.</span></span>
-   <span data-ttu-id="ad2c9-127">Определение закрытого элемента управления — права доступа для типа объекта и контроль над тем, кто может выполнять операции, защищенные закрытыми правами.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-127">Define private control-access rights for an object type and control who can perform the operations protected by the private rights.</span></span>
-   <span data-ttu-id="ad2c9-128">Примените ACE к объекту-контейнеру в корне поддерева каталога, чтобы защита была автоматически унаследована всеми дочерними объектами в дереве.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-128">Apply an ACE to a container object at the root of a directory subtree, such that the protections can be inherited automatically by all child objects down the tree.</span></span>
-   <span data-ttu-id="ad2c9-129">Примените ACE, который наследуется автоматически конкретным типом дочернего объекта в поддереве.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-129">Apply an ACE that is inherited automatically by a specific type of child object in a subtree.</span></span>
-   <span data-ttu-id="ad2c9-130">Создайте запись ACE, которая предоставляет права группе безопасности, а не одному пользователю.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-130">Create an ACE that grants rights to a security group, rather than to a single user.</span></span>
-   <span data-ttu-id="ad2c9-131">Примените ACE к групповая политика объектам, чтобы управлять учетными записями и компьютерами, затронутыми политикой.</span><span class="sxs-lookup"><span data-stu-id="ad2c9-131">Apply an ACE to Group Policy Objects to control the accounts and computers affected by the policy.</span></span>

 

 




