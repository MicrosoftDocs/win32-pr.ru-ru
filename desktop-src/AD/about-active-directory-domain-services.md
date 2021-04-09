---
title: Сведения о службах домен Active Directory
description: В этом справочном материале содержится основная информация по интеграции Active Directory Майкрософт в распределенные приложения, предназначенные для операционных систем, поддерживающих Active Directory.
ms.assetid: cc6c63dd-ae22-40a7-8312-0a4648bb92bd
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, сведения
- Active Directory домен Active Directory Services, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d8dafb89533d796f0651ad08b913eacda1d0fe9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070048"
---
# <a name="about-active-directory-domain-services"></a><span data-ttu-id="8a820-105">Сведения о службах домен Active Directory</span><span class="sxs-lookup"><span data-stu-id="8a820-105">About Active Directory Domain Services</span></span>

## <a name="writing-powerful-applications-that-use-active-directory-domain-services"></a><span data-ttu-id="8a820-106">Написание мощных приложений, использующих службы домен Active Directory</span><span class="sxs-lookup"><span data-stu-id="8a820-106">Writing Powerful Applications that Use Active Directory Domain Services</span></span>

<span data-ttu-id="8a820-107">Это руководство содержит подробную информацию по интеграции домен Active Directory служб в распределенные приложения, предназначенные для операционных систем, которые поддерживают службы домен Active Directory, в том числе:</span><span class="sxs-lookup"><span data-stu-id="8a820-107">This guide provides essential information for integrating Active Directory Domain Services in distributed applications designed for operating systems that support Active Directory Domain Services, including:</span></span>

-   <span data-ttu-id="8a820-108">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a820-108">Windows Server 2008</span></span>
-   <span data-ttu-id="8a820-109">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8a820-109">Windows Server 2008 R2</span></span>
-   <span data-ttu-id="8a820-110">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8a820-110">Windows Server 2012</span></span>
-   <span data-ttu-id="8a820-111">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8a820-111">Windows Server 2012 R2</span></span>
-   <span data-ttu-id="8a820-112">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8a820-112">Windows Server 2016</span></span>

> [!Note]  
> <span data-ttu-id="8a820-113">Эти разделы предназначены для разработчиков программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="8a820-113">These topics are for software developers.</span></span> <span data-ttu-id="8a820-114">Сведения о проблемах поддержки см. в разделе [Служба поддержки Майкрософт](https://windows.microsoft.com/windows/support#1tc).</span><span class="sxs-lookup"><span data-stu-id="8a820-114">For support issues, see [Microsoft Support](https://windows.microsoft.com/windows/support#1tc).</span></span> <span data-ttu-id="8a820-115">Сведения об администрировании Active Directory см. в разделе [домен Active Directory Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) на сайте TechNet.</span><span class="sxs-lookup"><span data-stu-id="8a820-115">For information about administering Active Directory, see [Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) at TechNet.</span></span>

 

## <a name="fundamental-directory-features"></a><span data-ttu-id="8a820-116">Основные возможности каталога</span><span class="sxs-lookup"><span data-stu-id="8a820-116">Fundamental Directory Features</span></span>

<span data-ttu-id="8a820-117">Служба каталогов — это фундаментальная служба для распределенных приложений.</span><span class="sxs-lookup"><span data-stu-id="8a820-117">A directory service is a fundamental service for distributed applications.</span></span> <span data-ttu-id="8a820-118">Служба каталогов должна предоставлять функции, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8a820-118">A directory service must provide the features listed in the following table.</span></span>



| <span data-ttu-id="8a820-119">Функция</span><span class="sxs-lookup"><span data-stu-id="8a820-119">Feature</span></span>               | <span data-ttu-id="8a820-120">Описание</span><span class="sxs-lookup"><span data-stu-id="8a820-120">Description</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a820-121">Прозрачность расположения</span><span class="sxs-lookup"><span data-stu-id="8a820-121">Location transparency</span></span> | <span data-ttu-id="8a820-122">Возможность поиска пользователей, групп, сетевых служб или ресурсов, данных без адреса объекта</span><span class="sxs-lookup"><span data-stu-id="8a820-122">Able to find user, group, networked service, or resource, data without the object address</span></span>           |
| <span data-ttu-id="8a820-123">Хранилище данных объектов</span><span class="sxs-lookup"><span data-stu-id="8a820-123">Object data</span></span>           | <span data-ttu-id="8a820-124">Возможность хранения данных пользователя, группы, Организации и службы в иерархическом дереве</span><span class="sxs-lookup"><span data-stu-id="8a820-124">Able to store user, group, organization, and service data in a hierarchical tree</span></span>                    |
| <span data-ttu-id="8a820-125">Расширенный запрос</span><span class="sxs-lookup"><span data-stu-id="8a820-125">Rich query</span></span>            | <span data-ttu-id="8a820-126">Возможность поиска объекта путем запроса свойств объекта</span><span class="sxs-lookup"><span data-stu-id="8a820-126">Able to locate an object by querying for object properties</span></span>                                          |
| <span data-ttu-id="8a820-127">Высокий уровень доступности</span><span class="sxs-lookup"><span data-stu-id="8a820-127">High availability</span></span>     | <span data-ttu-id="8a820-128">Возможность поиска реплики каталога в расположении, которое эффективно для операций чтения и записи</span><span class="sxs-lookup"><span data-stu-id="8a820-128">Able to locate a replica of the directory at a location that is efficient for read/write operations</span></span> |



 

## <a name="advanced-features-of-active-directory-domain-services"></a><span data-ttu-id="8a820-129">Дополнительные возможности служб домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="8a820-129">Advanced Features of Active Directory Domain Services</span></span>

<span data-ttu-id="8a820-130">Службы домен Active Directory Services предоставляют функции, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8a820-130">Active Directory Domain Services provides the features listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8a820-131">Функция</span><span class="sxs-lookup"><span data-stu-id="8a820-131">Feature</span></span></th>
<th><span data-ttu-id="8a820-132">Описание</span><span class="sxs-lookup"><span data-stu-id="8a820-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8a820-133">Поддержка стандартов Интернета</span><span class="sxs-lookup"><span data-stu-id="8a820-133">Support for Internet standards</span></span></td>
<td><span data-ttu-id="8a820-134">Службы домен Active Directory Services реализуют свои функции в соответствии с опубликованными интернет-стандартами, такими как LDAP и DNS.</span><span class="sxs-lookup"><span data-stu-id="8a820-134">Active Directory Domain Services implements its features in accordance with published Internet standards such as LDAP and DNS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a820-135">Тесно интегрированная и гибкая безопасность</span><span class="sxs-lookup"><span data-stu-id="8a820-135">Tightly integrated and flexible security</span></span></td>
<td><span data-ttu-id="8a820-136">Преимущества (список неполон):</span><span class="sxs-lookup"><span data-stu-id="8a820-136">Advantages include:</span></span><br/>
<ul>
<li><span data-ttu-id="8a820-137">Выбранные пакеты проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="8a820-137">Choice of authentication packages.</span></span> <span data-ttu-id="8a820-138">Kerberos, SSL (SSL) или сочетание; Например, установите канал SSL для шифрования, а затем используйте Kerberos для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="8a820-138">Kerberos, Secure Sockets Layer (SSL), or a combination; for example, establish an SSL channel for encryption and then use Kerberos for authentication.</span></span></li>
<li><span data-ttu-id="8a820-139">Централизованное управление доступом к службам и ресурсам с помощью пользователей и групп в службах домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="8a820-139">Central management of service and resource access by using the users and groups in Active Directory Domain Services.</span></span></li>
<li><span data-ttu-id="8a820-140">Делегирование администрирования, чтобы администраторы центрального администратора могли делегировать административные задачи, такие как изменение пароля или создание и удаление конкретного объекта.</span><span class="sxs-lookup"><span data-stu-id="8a820-140">Delegation of administration so that central administrators can delegate administrative tasks such as password changing or specific object creation and deletion.</span></span></li>
<li><span data-ttu-id="8a820-141">Сервер Active Directory использует те же механизмы контроля доступа, которые используются в файловых системах операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="8a820-141">The Active Directory server uses the same access control mechanisms used on file systems in the Windows operating systems.</span></span> <span data-ttu-id="8a820-142">Таким же средствами, которые управляют доступом к файловой системе, работают с домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="8a820-142">Thus, the same tools that manage access control on a file system work for Active Directory Domain Services.</span></span></li>
<li><span data-ttu-id="8a820-143">Комплексная инфраструктура открытых ключей.</span><span class="sxs-lookup"><span data-stu-id="8a820-143">Comprehensive Public Key infrastructure.</span></span> <span data-ttu-id="8a820-144">Сервер сертификатов (Майкрософт) и поддержка смарт-карт интегрированы со службами домен Active Directory Services для обеспечения входа и управления сертификатами с помощью смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="8a820-144">The Microsoft Certificate Server and Smart Card support are integrated with Active Directory Domain Services to provide Smart Card logon and Certificate management.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a820-145">Легко программировать</span><span class="sxs-lookup"><span data-stu-id="8a820-145">Easily programmable</span></span></td>
<td><span data-ttu-id="8a820-146">К серверу Active Directory можно обращаться и администрировать программно с помощью API <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">интерфейсов служб Active Directory</a> , API <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">протокола Lightweight Directory Access</a> или пространства имен <a href="/dotnet/api/system.directoryservices">System. DirectoryServices</a> .</span><span class="sxs-lookup"><span data-stu-id="8a820-146">The Active Directory server can be programmatically accessed and administered using the <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">Active Directory Service Interfaces</a> API, <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol</a> API, or the <a href="/dotnet/api/system.directoryservices">System.DirectoryServices</a> namespace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a820-147">Системные службы с поддержкой каталога</span><span class="sxs-lookup"><span data-stu-id="8a820-147">Directory enabled system services</span></span></td>
<td><span data-ttu-id="8a820-148">Клиентское приложение можно легко развернуть на распределенных настольных компьютерах, создав пакет установщик Windows и используя функцию развертывания приложений, доступную в операционных системах Windows.</span><span class="sxs-lookup"><span data-stu-id="8a820-148">Your client application can be easily deployed to distributed desktops by creating a Windows Installer package and using the application deployment feature available in the Windows operating systems.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a820-149">Интеграция ключевых приложений</span><span class="sxs-lookup"><span data-stu-id="8a820-149">Key application integration</span></span></td>
<td><span data-ttu-id="8a820-150">Ключевые распределенные приложения, такие как Exchange, интегрируются со службами домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8a820-150">Key distributed applications, such as Exchange, are integrated with Active Directory Domain Services.</span></span> <span data-ttu-id="8a820-151">Таким же компаниям можно сократить количество управляемых служб каталогов.</span><span class="sxs-lookup"><span data-stu-id="8a820-151">Thus, companies can reduce the number of directory services to be managed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a820-152">Расширенная и расширяемая схема</span><span class="sxs-lookup"><span data-stu-id="8a820-152">Rich and extensible schema</span></span></td>
<td><span data-ttu-id="8a820-153">Схема определяет, какие объекты и свойства могут быть записаны и прочитаны из службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="8a820-153">The schema defines what objects and properties can be written and read from a directory service.</span></span> <span data-ttu-id="8a820-154">Схема Active Directory является богатой.</span><span class="sxs-lookup"><span data-stu-id="8a820-154">The Active Directory Schema is rich.</span></span> <span data-ttu-id="8a820-155">Большая часть объектов и свойств, необходимых службе, доступна.</span><span class="sxs-lookup"><span data-stu-id="8a820-155">Most of the objects and properties a service requires are available.</span></span> <span data-ttu-id="8a820-156">В противном случае распределенное приложение может расширить схему для поддержки требований приложения.</span><span class="sxs-lookup"><span data-stu-id="8a820-156">If not, a distributed application can extend the schema to support the application requirements.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8a820-157">Дополнительные сведения о службах домен Active Directory см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="8a820-157">For more information about Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="8a820-158">Основные понятия домен Active Directory служб</span><span class="sxs-lookup"><span data-stu-id="8a820-158">Core Concepts of Active Directory Domain Services</span></span>](core-concepts-of-active-directory-domain-services.md)
-   [<span data-ttu-id="8a820-159">Архитектура Active Directory</span><span class="sxs-lookup"><span data-stu-id="8a820-159">Active Directory Architecture</span></span>](active-directory-domain-services-architecture.md)
-   [<span data-ttu-id="8a820-160">Схема Active Directory</span><span class="sxs-lookup"><span data-stu-id="8a820-160">Active Directory Schema</span></span>](active-directory-schema.md)

