---
title: Использование доменных служб Active Directory
description: В этом разделе приводятся рекомендации по написанию приложений, использующих или публикующих данные в службе Active Directory Directory.
ms.assetid: 2ae20169-08a5-4e15-8430-ea99a917725f
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory с помощью
- Службы домен Active Directory Services Active Directory, использование
- Active Directory примеры Active Directory
- Примеры домен Active Directory Services Active Directory
- Примеры Active Directory
- Active Directory Active Directory, примеры см. в статье примеры домен Active Directory служб.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540b9004311db320decbd15c4f0a29e52ec1302a
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797059"
---
# <a name="using-active-directory-domain-services"></a><span data-ttu-id="3d394-109">Использование доменных служб Active Directory</span><span class="sxs-lookup"><span data-stu-id="3d394-109">Using Active Directory Domain Services</span></span>

<span data-ttu-id="3d394-110">В этом разделе приводятся рекомендации по написанию приложений, использующих или публикующих данные в службе Active Directory Directory.</span><span class="sxs-lookup"><span data-stu-id="3d394-110">This section provides guidelines for writing applications that use or publish data in an Active Directory directory service.</span></span>

> [!Note]  
> <span data-ttu-id="3d394-111">Следующая документация предназначена для компьютерных программистов.</span><span class="sxs-lookup"><span data-stu-id="3d394-111">The following documentation is for computer programmers.</span></span> <span data-ttu-id="3d394-112">Если вы пытаетесь устранить ошибку Active Directory домашней печати, см. [следующие предложения](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) на страницах сообщества Майкрософт. Если это не поможет, воспользуйтесь приведенными ниже рекомендациями на [сайте TechNet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint).</span><span class="sxs-lookup"><span data-stu-id="3d394-112">If you are trying to resolve an Active Directory home printing error, see the [following suggestion](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) from the Microsoft community pages; if that doesn't help, try these recommendations from [TechNet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint).</span></span>

 

<span data-ttu-id="3d394-113">Службы домен Active Directory Services совместимы с протоколом упрощенного доступа к каталогу 3,0, который определяется RFC 2251 и другими RFC.</span><span class="sxs-lookup"><span data-stu-id="3d394-113">Active Directory Domain Services are compliant with Lightweight Directory Access Protocol 3.0, which is defined by RFC 2251 and other RFCs.</span></span> <span data-ttu-id="3d394-114">Для доступа к домен Active Directory службам можно использовать любой из следующих наборов API.</span><span class="sxs-lookup"><span data-stu-id="3d394-114">Any of the following API sets can be used to access Active Directory Domain Services.</span></span> <span data-ttu-id="3d394-115">Каждый набор API имеет свои преимущества и недостатки, которые зависят от языка программирования, среды программирования и предполагаемого метода выполнения.</span><span class="sxs-lookup"><span data-stu-id="3d394-115">Each API set has advantages and disadvantages that depend on the programming language, programming environment, and intended method of execution.</span></span> <span data-ttu-id="3d394-116">Большинство примеров в этом пошаговом руководству используют интерфейсы ADSI, которые поддерживаются такими языками, как C и C++, а также поддерживающими автоматизацией языками, такими как Microsoft Visual Basic и Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="3d394-116">The majority of the examples in this guide use ADSI, which is supported by languages such as C and C++, as well as automation-compliant languages such as Microsoft Visual Basic and Visual Basic Scripting Edition.</span></span>

<span data-ttu-id="3d394-117">Дополнительные сведения о конкретных технологиях домен Active Directory Services см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="3d394-117">For more information about specific Active Directory Domain Services technologies, see:</span></span>

-   [<span data-ttu-id="3d394-118">протокол LDAP</span><span class="sxs-lookup"><span data-stu-id="3d394-118">Lightweight Directory Access Protocol</span></span>](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api)
-   [<span data-ttu-id="3d394-119">Интерфейсы служб Active Directory</span><span class="sxs-lookup"><span data-stu-id="3d394-119">Active Directory Service Interfaces</span></span>](../adsi/active-directory-service-interfaces-adsi.md)
-   [<span data-ttu-id="3d394-120">System.DirectoryServices</span><span class="sxs-lookup"><span data-stu-id="3d394-120">System.DirectoryServices</span></span>](/dotnet/api/system.directoryservices)

<span data-ttu-id="3d394-121">В этом разделе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="3d394-121">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="3d394-122">Привязка к службам домен Active Directory</span><span class="sxs-lookup"><span data-stu-id="3d394-122">Binding to Active Directory Domain Services</span></span>](binding-to-active-directory-domain-services.md)
-   [<span data-ttu-id="3d394-123">Поиск в домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="3d394-123">Searching in Active Directory Domain Services</span></span>](searching-in-active-directory-domain-services.md)
-   [<span data-ttu-id="3d394-124">Создание и удаление объектов в службах домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="3d394-124">Creating and Deleting Objects in Active Directory Domain Services</span></span>](creating-and-deleting-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="3d394-125">Перемещение объектов</span><span class="sxs-lookup"><span data-stu-id="3d394-125">Moving Objects</span></span>](moving-objects.md)
-   [<span data-ttu-id="3d394-126">Чтение и запись атрибутов объектов в службах домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="3d394-126">Reading and Writing Attributes of Objects in Active Directory Domain Services</span></span>](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="3d394-127">Управление доступом к объектам в службах домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="3d394-127">Controlling Access to Objects in Active Directory Domain Services</span></span>](controlling-access-to-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="3d394-128">Расширение схемы</span><span class="sxs-lookup"><span data-stu-id="3d394-128">Extending the Schema</span></span>](extending-the-schema.md)
-   [<span data-ttu-id="3d394-129">Расширение пользовательского интерфейса для объектов каталога</span><span class="sxs-lookup"><span data-stu-id="3d394-129">Extending the User Interface for Directory Objects</span></span>](extending-the-user-interface-for-directory-objects.md)
-   [<span data-ttu-id="3d394-130">Управление пользователями</span><span class="sxs-lookup"><span data-stu-id="3d394-130">Managing Users</span></span>](managing-users.md)
-   [<span data-ttu-id="3d394-131">Управление группами</span><span class="sxs-lookup"><span data-stu-id="3d394-131">Managing Groups</span></span>](managing-groups.md)
-   [<span data-ttu-id="3d394-132">Отслеживание изменений</span><span class="sxs-lookup"><span data-stu-id="3d394-132">Tracking Changes</span></span>](tracking-changes.md)
-   [<span data-ttu-id="3d394-133">Публикация службы</span><span class="sxs-lookup"><span data-stu-id="3d394-133">Service Publication</span></span>](service-publication.md)
-   [<span data-ttu-id="3d394-134">Учетные записи входа в службу</span><span class="sxs-lookup"><span data-stu-id="3d394-134">Service Logon Accounts</span></span>](service-logon-accounts.md)
-   [<span data-ttu-id="3d394-135">Взаимная проверка подлинности с помощью Kerberos</span><span class="sxs-lookup"><span data-stu-id="3d394-135">Mutual Authentication Using Kerberos</span></span>](mutual-authentication-using-kerberos.md)
-   [<span data-ttu-id="3d394-136">Резервное копирование и восстановление Active Directory</span><span class="sxs-lookup"><span data-stu-id="3d394-136">Backing Up and Restoring Active Directory</span></span>](backing-up-and-restoring-an-active-directory-server.md)
-   [<span data-ttu-id="3d394-137">Сохранение платформа динамических данных</span><span class="sxs-lookup"><span data-stu-id="3d394-137">Storing Dynamic Data</span></span>](storing-dynamic-data.md)
-   [<span data-ttu-id="3d394-138">Разделы каталога приложений</span><span class="sxs-lookup"><span data-stu-id="3d394-138">Application Directory Partitions</span></span>](application-directory-partitions.md)
-   [<span data-ttu-id="3d394-139">Обнаружение режима работы домена</span><span class="sxs-lookup"><span data-stu-id="3d394-139">Detecting the Operation Mode of a Domain</span></span>](detecting-the-operation-mode-of-a-domain.md)

 

 