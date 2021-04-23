---
title: Чтение и запись атрибутов объектов в службах домен Active Directory Services
description: Объекты в домен Active Directory Services имеют атрибуты, содержащие данные об определенном объекте.
ms.assetid: d11b32c5-5bda-45af-846d-f35b839cf10d
ms.tgt_platform: multiple
keywords:
- Active Directory домен Active Directory Services с помощью чтения и записи атрибутов Active Directoryных объектов
- объекты Active Directory, чтение и запись атрибутов объектов Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da4e0c2b6da52458178fc50f4ce4e96d887b17d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487416"
---
# <a name="reading-and-writing-attributes-of-objects-in-active-directory-domain-services"></a><span data-ttu-id="1b6f9-105">Чтение и запись атрибутов объектов в службах домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="1b6f9-105">Reading and Writing Attributes of Objects in Active Directory Domain Services</span></span>

<span data-ttu-id="1b6f9-106">Объекты в домен Active Directory Services имеют атрибуты, содержащие данные об определенном объекте.</span><span class="sxs-lookup"><span data-stu-id="1b6f9-106">Objects in Active Directory Domain Services have attributes that contain data about the specific object.</span></span> <span data-ttu-id="1b6f9-107">Доступ к атрибутам и их изменение зависит от используемой технологии программирования.</span><span class="sxs-lookup"><span data-stu-id="1b6f9-107">How the attributes are accessed and modified depends upon the programming technology being used.</span></span> <span data-ttu-id="1b6f9-108">Дополнительные сведения о чтении и изменении атрибутов в домен Active Directory Services с помощью определенной технологии программирования см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="1b6f9-108">For more information about reading and modifying attributes in Active Directory Domain Services with a specific programming technology, see the following listed topics.</span></span>



| <span data-ttu-id="1b6f9-109">Технология программирования</span><span class="sxs-lookup"><span data-stu-id="1b6f9-109">Programming technology</span></span>                                                                       | <span data-ttu-id="1b6f9-110">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="1b6f9-110">For more information</span></span>                                                                        |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b6f9-111">Интерфейсы служб Active Directory</span><span class="sxs-lookup"><span data-stu-id="1b6f9-111">Active Directory Service Interfaces</span></span>](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [<span data-ttu-id="1b6f9-112">Доступ к данным и управление ими с помощью ADSI</span><span class="sxs-lookup"><span data-stu-id="1b6f9-112">Accessing and Manipulating Data with ADSI</span></span>](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi) |
| [<span data-ttu-id="1b6f9-113">протокол LDAP</span><span class="sxs-lookup"><span data-stu-id="1b6f9-113">Lightweight Directory Access Protocol</span></span>](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [<span data-ttu-id="1b6f9-114">Изменение записи каталога</span><span class="sxs-lookup"><span data-stu-id="1b6f9-114">Modifying a Directory Entry</span></span>](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry)                             |
| [<span data-ttu-id="1b6f9-115">System.DirectoryServices</span><span class="sxs-lookup"><span data-stu-id="1b6f9-115">System.DirectoryServices</span></span>](/dotnet/api/system.directoryservices) | <span data-ttu-id="1b6f9-116">[Свойства объекта каталога](https://msdn.microsoft.com/library/ms180858(v=VS.80).aspx)</span><span class="sxs-lookup"><span data-stu-id="1b6f9-116">[Directory Object Properties](https://msdn.microsoft.com/library/ms180858(v=VS.80).aspx)</span></span>                         |



 

<span data-ttu-id="1b6f9-117">Дополнительные сведения об атрибутах см. [в разделе Определение типа атрибута](determining-an-attribute-type.md).</span><span class="sxs-lookup"><span data-stu-id="1b6f9-117">For more information about attributes, see [Determining an Attribute Type](determining-an-attribute-type.md).</span></span>

 

 