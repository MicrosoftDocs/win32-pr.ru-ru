---
title: Управление доступом к объектам в службах домен Active Directory Services
description: Каждый объект службы каталогов Active Directory защищен системой безопасности Windows 2000.
ms.assetid: 0821069d-76bd-49cb-a617-8446d26e61d9
ms.tgt_platform: multiple
keywords:
- Службы домен Active Directory Services, использование, безопасность
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cac744ef63fa95c45d5af535f5155378d479fdb
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/04/2019
ms.locfileid: "104069420"
---
# <a name="controlling-object-access-in-active-directory-domain-services"></a><span data-ttu-id="e1a11-104">Управление доступом к объектам в службах домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="e1a11-104">Controlling object access in Active Directory Domain Services</span></span>

<span data-ttu-id="e1a11-105">Каждый объект службы каталогов Active Directory защищен системой безопасности Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e1a11-105">Each Active Directory directory service object is protected by Windows 2000 security.</span></span> <span data-ttu-id="e1a11-106">Эта защита безопасности управляет операциями, которые каждый субъект безопасности может выполнять в каталоге.</span><span class="sxs-lookup"><span data-stu-id="e1a11-106">This security protection controls the operations that each security principal can perform in the directory.</span></span> <span data-ttu-id="e1a11-107">В следующих разделах описывается, как приложение с поддержкой каталогов может использовать функции контроля доступа в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e1a11-107">The following sections describe how a directory-enabled application can use the access control features in Active Directory.</span></span>

-   [<span data-ttu-id="e1a11-108">Как работает управление доступом в службах домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="e1a11-108">How Access Control Works in Active Directory Domain Services</span></span>](how-access-control-works-in-active-directory-domain-services.md)
-   [<span data-ttu-id="e1a11-109">Как управление доступом влияет на операции чтения, операции записи, создание и удаление объектов.</span><span class="sxs-lookup"><span data-stu-id="e1a11-109">How access control affects read operations, write operation, object creation and deletion.</span></span>](how-security-affects-operations-in-active-directory-domain-services.md)
-   [<span data-ttu-id="e1a11-110">Использование интерфейсов IADs и Идиректорйобжект для работы с дескриптором безопасности объекта</span><span class="sxs-lookup"><span data-stu-id="e1a11-110">Using the IADs and IDirectoryObject interfaces to work with an object's security descriptor</span></span>](apis-for-working-with-security-descriptors.md)
-   [<span data-ttu-id="e1a11-111">Изменение разрешений на доступ к объекту</span><span class="sxs-lookup"><span data-stu-id="e1a11-111">Modifying the access permissions on an object</span></span>](setting-access-rights-on-an-object.md)
-   [<span data-ttu-id="e1a11-112">Как устанавливаются дескрипторы безопасности для новых объектов каталога</span><span class="sxs-lookup"><span data-stu-id="e1a11-112">How security descriptors are set on new directory objects</span></span>](how-security-descriptors-are-set-on-new-directory-objects.md)
-   [<span data-ttu-id="e1a11-113">Создание дескриптора безопасности для нового объекта каталога</span><span class="sxs-lookup"><span data-stu-id="e1a11-113">Creating a Security Descriptor for a New Directory Object</span></span>](creating-a-security-descriptor-for-a-new-directory-object.md)
-   [<span data-ttu-id="e1a11-114">Использование наследования разрешений на доступ для разрешения административного доступа ко всему поддереву каталога</span><span class="sxs-lookup"><span data-stu-id="e1a11-114">Using inheritance of access permissions to enable administrative access to an entire subtree of the directory</span></span>](inheritance-and-delegation-of-administration.md)
-   [<span data-ttu-id="e1a11-115">Создание, изменение и чтение дескриптора безопасности по умолчанию для класса объекта</span><span class="sxs-lookup"><span data-stu-id="e1a11-115">Creating, modifying, and reading the default security descriptor for an object class</span></span>](default-security-descriptor.md)
-   [<span data-ttu-id="e1a11-116">Создание, установка и проверка прав доступа для операций, которые выходят за рамки стандартных прав</span><span class="sxs-lookup"><span data-stu-id="e1a11-116">Creating, setting, and checking control access rights for operations that go beyond those covered by the predefined rights</span></span>](control-access-rights.md)
-   [<span data-ttu-id="e1a11-117">Использование Дсаддсидхистори</span><span class="sxs-lookup"><span data-stu-id="e1a11-117">Using DsAddSidHistory</span></span>](using-dsaddsidhistory.md)
-   [<span data-ttu-id="e1a11-118">Управление видимостью объекта</span><span class="sxs-lookup"><span data-stu-id="e1a11-118">Controlling Object Visibility</span></span>](controlling-object-visibility.md)
-   [<span data-ttu-id="e1a11-119">Списки DACL NULL и пустые списки DACL</span><span class="sxs-lookup"><span data-stu-id="e1a11-119">Null DACLs and Empty DACLs</span></span>](null-dacls-and-empty-dacls.md)

 

 




