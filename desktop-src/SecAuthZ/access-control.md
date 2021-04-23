---
description: Управление доступом относится к функциям безопасности, которые контролируют доступ к ресурсам в операционной системе. Приложения вызывают функции управления доступом, чтобы задать, кто может получать доступ к конкретным ресурсам или управлять доступом к ресурсам, предоставляемым приложением.
ms.assetid: d9ce4ec5-5c09-4b33-93a1-39638a925986
title: Управление доступом (авторизация)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31c0198f0ce0de77750e0587d9b54c1e20cee756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080666"
---
# <a name="access-control-authorization"></a><span data-ttu-id="19266-104">Управление доступом (авторизация)</span><span class="sxs-lookup"><span data-stu-id="19266-104">Access Control (Authorization)</span></span>

<span data-ttu-id="19266-105">Управление доступом относится к функциям безопасности, которые контролируют доступ к ресурсам в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="19266-105">Access control refers to security features that control who can access resources in the operating system.</span></span> <span data-ttu-id="19266-106">Приложения вызывают функции управления доступом, чтобы задать, кто может получать доступ к конкретным ресурсам или управлять доступом к ресурсам, предоставляемым приложением.</span><span class="sxs-lookup"><span data-stu-id="19266-106">Applications call access control functions to set who can access specific resources or control access to resources provided by the application.</span></span>

<span data-ttu-id="19266-107">В этом обзоре описывается модель безопасности для управления доступом к объектам Windows, таким как файлы, а также для управления доступом к административным функциям, таким как Настройка системного времени или аудит действий пользователя.</span><span class="sxs-lookup"><span data-stu-id="19266-107">This overview describes the security model for controlling access to Windows objects, such as files, and for controlling access to administrative functions, such as setting the system time or auditing user actions.</span></span> <span data-ttu-id="19266-108">В разделе [модель контроля доступа](access-control-model.md) содержится обобщенное описание частей управления доступом и их взаимодействия друг с другом.</span><span class="sxs-lookup"><span data-stu-id="19266-108">The [Access Control Model](access-control-model.md) topic provides a high-level description of the parts of access control and how they interact with each other.</span></span>

<span data-ttu-id="19266-109">В следующих разделах описывается управление доступом:</span><span class="sxs-lookup"><span data-stu-id="19266-109">The following topics describe access control:</span></span>

-   [<span data-ttu-id="19266-110">Безопасность на уровне C2</span><span class="sxs-lookup"><span data-stu-id="19266-110">C2-level Security</span></span>](c2-level-security.md)
-   [<span data-ttu-id="19266-111">Модель контроля доступа</span><span class="sxs-lookup"><span data-stu-id="19266-111">Access Control Model</span></span>](access-control-model.md)
-   [<span data-ttu-id="19266-112">Язык определения дескрипторов безопасности</span><span class="sxs-lookup"><span data-stu-id="19266-112">Security Descriptor Definition Language</span></span>](security-descriptor-definition-language.md)
-   [<span data-ttu-id="19266-113">Права</span><span class="sxs-lookup"><span data-stu-id="19266-113">Privileges</span></span>](privileges.md)
-   [<span data-ttu-id="19266-114">Создание записей аудита</span><span class="sxs-lookup"><span data-stu-id="19266-114">Audit Generation</span></span>](audit-generation.md)
-   [<span data-ttu-id="19266-115">Защищаемые объекты</span><span class="sxs-lookup"><span data-stu-id="19266-115">Securable Objects</span></span>](securable-objects.md)
-   [<span data-ttu-id="19266-116">Управление доступом низкого уровня</span><span class="sxs-lookup"><span data-stu-id="19266-116">Low-level Access Control</span></span>](low-level-access-control.md)

<span data-ttu-id="19266-117">Ниже перечислены стандартные задачи управления доступом.</span><span class="sxs-lookup"><span data-stu-id="19266-117">The following are common access control tasks:</span></span>

-   [<span data-ttu-id="19266-118">Управление доступом к объекту с помощью списков DACL</span><span class="sxs-lookup"><span data-stu-id="19266-118">How DACLs Control Access to an Object</span></span>](how-dacls-control-access-to-an-object.md)
-   [<span data-ttu-id="19266-119">Управление созданием дочерних объектов в C++</span><span class="sxs-lookup"><span data-stu-id="19266-119">Controlling Child Object Creation in C++</span></span>](controlling-child-object-creation-in-c--.md)
-   [<span data-ttu-id="19266-120">ACE для управления доступом к свойствам объекта</span><span class="sxs-lookup"><span data-stu-id="19266-120">ACEs to Control Access to an Object's Properties</span></span>](aces-to-control-access-to-an-object-s-properties.md)
-   [<span data-ttu-id="19266-121">Запрос прав доступа к объекту</span><span class="sxs-lookup"><span data-stu-id="19266-121">Requesting Access Rights to an Object</span></span>](requesting-access-rights-to-an-object.md)

<span data-ttu-id="19266-122">В следующих разделах приводятся примеры кода для задач управления доступом.</span><span class="sxs-lookup"><span data-stu-id="19266-122">The following topics provide example code for access control tasks:</span></span>

-   [<span data-ttu-id="19266-123">Изменение списков управления доступом объекта в C++</span><span class="sxs-lookup"><span data-stu-id="19266-123">Modifying the ACLs of an Object in C++</span></span>](modifying-the-acls-of-an-object-in-c--.md)
-   [<span data-ttu-id="19266-124">Создание дескриптора безопасности для нового объекта в C++</span><span class="sxs-lookup"><span data-stu-id="19266-124">Creating a Security Descriptor for a New Object in C++</span></span>](creating-a-security-descriptor-for-a-new-object-in-c--.md)
-   [<span data-ttu-id="19266-125">Управление созданием дочерних объектов в C++</span><span class="sxs-lookup"><span data-stu-id="19266-125">Controlling Child Object Creation in C++</span></span>](controlling-child-object-creation-in-c--.md)
-   [<span data-ttu-id="19266-126">Включение и отключение привилегий в C++</span><span class="sxs-lookup"><span data-stu-id="19266-126">Enabling and Disabling Privileges in C++</span></span>](enabling-and-disabling-privileges-in-c--.md)
-   [<span data-ttu-id="19266-127">Поиск идентификатора безопасности в маркере доступа в C++</span><span class="sxs-lookup"><span data-stu-id="19266-127">Searching for a SID in an Access Token in C++</span></span>](searching-for-a-sid-in-an-access-token-in-c--.md)
-   [<span data-ttu-id="19266-128">Поиск владельца объекта файла в C++</span><span class="sxs-lookup"><span data-stu-id="19266-128">Finding the Owner of a File Object in C++</span></span>](finding-the-owner-of-a-file-object-in-c--.md)
-   [<span data-ttu-id="19266-129">Получение владения объектом в C++</span><span class="sxs-lookup"><span data-stu-id="19266-129">Taking Object Ownership in C++</span></span>](taking-object-ownership-in-c--.md)
-   [<span data-ttu-id="19266-130">Создание списка DACL</span><span class="sxs-lookup"><span data-stu-id="19266-130">Creating a DACL</span></span>](/windows/desktop/SecBP/creating-a-dacl)

 

 
