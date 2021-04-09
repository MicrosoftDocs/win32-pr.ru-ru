---
title: Доменные службы Active Directory
description: Службы Microsoft домен Active Directory Services являются основой для распределенных сетей, построенных на базе Windows 2000 Server, Windows Server 2003 и Microsoft Windows Server 2008, которые используют контроллеры домена.
ms.assetid: 9fc78c72-c59c-4c4d-ace5-00a431645c4b
ms.tgt_platform: multiple
keywords:
- Службы домен Active Directory Active Directory
- Active Directory Active Directory, начальная страница
- Active Directory домен Active Directory Services, начальная страница
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0270f331a68d23ad89a8e5a999f8cabd95487020
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104070824"
---
# <a name="active-directory-domain-services"></a><span data-ttu-id="b0282-106">Доменные службы Active Directory</span><span class="sxs-lookup"><span data-stu-id="b0282-106">Active Directory Domain Services</span></span>

## <a name="purpose"></a><span data-ttu-id="b0282-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="b0282-107">Purpose</span></span>

<span data-ttu-id="b0282-108">Службы Microsoft домен Active Directory Services являются основой для распределенных сетей, построенных на базе Windows 2000 Server, Windows Server 2003 и Microsoft Windows Server 2008, которые используют контроллеры домена.</span><span class="sxs-lookup"><span data-stu-id="b0282-108">Microsoft Active Directory Domain Services are the foundation for distributed networks built on Windows 2000 Server, Windows Server 2003 and Microsoft Windows Server 2008 operating systems that use domain controllers.</span></span> <span data-ttu-id="b0282-109">Домен Active Directory Services предоставляют безопасное, структурированное, иерархическое хранилище данных для объектов в сети, таких как пользователи, компьютеры, принтеры и службы.</span><span class="sxs-lookup"><span data-stu-id="b0282-109">Active Directory Domain Services provide secure, structured, hierarchical data storage for objects in a network such as users, computers, printers, and services.</span></span> <span data-ttu-id="b0282-110">Службы домен Active Directory предоставляют поддержку для поиска этих объектов и работы с ними.</span><span class="sxs-lookup"><span data-stu-id="b0282-110">Active Directory Domain Services provide support for locating and working with these objects.</span></span>

<span data-ttu-id="b0282-111">В этом разделе представлен обзор служб домен Active Directory и примеры кода для основных задач, таких как поиск объектов и чтение свойств, в более сложные задачи, такие как публикация службы.</span><span class="sxs-lookup"><span data-stu-id="b0282-111">This guide provides an overview of Active Directory Domain Services and sample code for basic tasks, such as searching for objects and reading properties, to more advanced tasks such as service publication.</span></span>

<span data-ttu-id="b0282-112">Windows 2000 Server и более поздние операционные системы предоставляют пользователям пользовательский интерфейс для работы с объектами и данными в службах домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="b0282-112">Windows 2000 Server and later operating systems provide a user interface for users and administrators to work with the objects and data in Active Directory Domain Services.</span></span> <span data-ttu-id="b0282-113">В этом руководство описывается, как расширить и настроить этот пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="b0282-113">This guide describes how to extend and customize that user interface.</span></span> <span data-ttu-id="b0282-114">В нем также описывается расширение служб домен Active Directory путем определения новых классов и атрибутов объектов.</span><span class="sxs-lookup"><span data-stu-id="b0282-114">It also describes how to extend Active Directory Domain Services by defining new object classes and attributes.</span></span>

> [!Note]  
> <span data-ttu-id="b0282-115">Следующая документация предназначена для компьютерных программистов.</span><span class="sxs-lookup"><span data-stu-id="b0282-115">The following documentation is for computer programmers.</span></span> <span data-ttu-id="b0282-116">Если вы являетесь конечным пользователем, пытающимся выполнить отладку ошибки печати или проблемы с домашней сетью, см. [форумы сообщества Майкрософт](https://answers.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="b0282-116">If you are an end-user trying to debug a printing error or home network issue, see the [Microsoft community forums](https://answers.microsoft.com).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="b0282-117">Где применимо</span><span class="sxs-lookup"><span data-stu-id="b0282-117">Where applicable</span></span>

<span data-ttu-id="b0282-118">Сетевые администраторы пишут сценарии и приложения, обращающиеся к службам домен Active Directory для автоматизации общих административных задач, таких как добавление пользователей и групп, Управление принтерами и настройка разрешений для сетевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b0282-118">Network administrators write scripts and applications that access Active Directory Domain Services to automate common administrative tasks, such as adding users and groups, managing printers, and setting permissions for network resources.</span></span>

<span data-ttu-id="b0282-119">Независимые поставщики программного обеспечения и разработчики конечных пользователей могут использовать программирование служб домен Active Directory Services для включения в каталог своих продуктов и приложений.</span><span class="sxs-lookup"><span data-stu-id="b0282-119">Independent software vendors and end-user developers can use Active Directory Domain Services programming to directory-enable their products and applications.</span></span> <span data-ttu-id="b0282-120">Службы могут публиковать себя в домен Active Directory Services; Клиенты могут использовать службы домен Active Directory для поиска служб, и они могут использовать службы домен Active Directory для поиска и работы с другими объектами в сети.</span><span class="sxs-lookup"><span data-stu-id="b0282-120">Services can publish themselves in Active Directory Domain Services; clients can use Active Directory Domain Services to find services, and both can use Active Directory Domain Services to locate and work with other objects on a network.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="b0282-121">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="b0282-121">Developer audience</span></span>

<span data-ttu-id="b0282-122">Приложения, обращающиеся к данным в службах домен Active Directory Services, могут быть написаны с помощью API [интерфейсов служб Active Directory](../adsi/active-directory-service-interfaces-adsi.md) , API [протокола упрощенного доступа к каталогам](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) или пространства имен [System. DirectoryServices](/dotnet/api/system.directoryservices) .</span><span class="sxs-lookup"><span data-stu-id="b0282-122">Applications that access data in Active Directory Domain Services can be written using the [Active Directory Service Interfaces](../adsi/active-directory-service-interfaces-adsi.md) API, [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) API, or the [System.DirectoryServices](/dotnet/api/system.directoryservices) namespace.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b0282-123">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="b0282-123">Run-time requirements</span></span>

<span data-ttu-id="b0282-124">Службы домен Active Directory работают на контроллерах домена Windows 2000 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="b0282-124">Active Directory Domain Services run on Windows 2000 and later domain controllers.</span></span> <span data-ttu-id="b0282-125">Однако клиентские приложения могут быть написаны для и запускаться в Windows Vista, Windows Server 2003, Windows XP, Windows 2000, Windows NT 4,0, Windows 98 и Windows 95.</span><span class="sxs-lookup"><span data-stu-id="b0282-125">However, client applications can be written for and run on Windows Vista, Windows Server 2003, Windows XP, Windows 2000, Windows NT 4.0, Windows 98, and Windows 95.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b0282-126">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="b0282-126">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="b0282-127">Сведения о службах домен Active Directory</span><span class="sxs-lookup"><span data-stu-id="b0282-127">About Active Directory Domain Services</span></span>](about-active-directory-domain-services.md)
</dt> <dd>

<span data-ttu-id="b0282-128">Общие сведения о службах домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b0282-128">General information about Active Directory Domain Services.</span></span>

</dd> <dt>

[<span data-ttu-id="b0282-129">Использование доменных служб Active Directory</span><span class="sxs-lookup"><span data-stu-id="b0282-129">Using Active Directory Domain Services</span></span>](using-active-directory-domain-services.md)
</dt> <dd>

<span data-ttu-id="b0282-130">Руководством по программированию служб домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="b0282-130">Active Directory Domain Services programming guide.</span></span>

</dd> <dt>

[<span data-ttu-id="b0282-131">Справочник по службам домен Active Directory</span><span class="sxs-lookup"><span data-stu-id="b0282-131">Active Directory Domain Services Reference</span></span>](active-directory-domain-services-reference.md)
</dt> <dd>

<span data-ttu-id="b0282-132">Справочник по программированию домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="b0282-132">Active Directory Domain Services programming reference.</span></span>

</dd> </dl>

 

 