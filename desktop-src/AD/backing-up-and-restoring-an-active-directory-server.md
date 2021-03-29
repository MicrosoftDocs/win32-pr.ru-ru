---
title: Резервное копирование и восстановление сервера Active Directory
description: Домен Active Directory Services предоставляют функции для резервного копирования и восстановления данных в базе данных каталогов.
ms.assetid: d9b9db51-ed1b-4db4-a4de-b8798c9647ac
ms.tgt_platform: multiple
keywords:
- Домен Active Directory служб, использование, резервное копирование и восстановление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92d57c2ddf572db8806aca71282e6b4fd8799ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789637"
---
# <a name="backing-up-and-restoring-an-active-directory-server"></a><span data-ttu-id="dc792-104">Резервное копирование и восстановление сервера Active Directory</span><span class="sxs-lookup"><span data-stu-id="dc792-104">Backing Up and Restoring an Active Directory Server</span></span>

<span data-ttu-id="dc792-105">Домен Active Directory Services предоставляют функции для резервного копирования и восстановления данных в базе данных каталогов.</span><span class="sxs-lookup"><span data-stu-id="dc792-105">Active Directory Domain Services provide functions for backing up and restoring data in the directory database.</span></span> <span data-ttu-id="dc792-106">В этом разделе описано, как выполнить [резервное копирование](backing-up-an-active-directory-server.md) и [Восстановление](restoring-an-active-directory-server.md) сервера Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dc792-106">This section describes how to [back up](backing-up-an-active-directory-server.md) and [restore](restoring-an-active-directory-server.md) an Active Directory server.</span></span> <span data-ttu-id="dc792-107">Дополнительные сведения о резервном копировании сервера Active Directory с помощью служебных программ, предоставляемых в операционных системах Windows 2000 и Windows Server 2003, см. в соответствующем наборе ресурсов, доступном на веб-сайте Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="dc792-107">For more information about backing up an Active Directory server using the utilities provided in Windows 2000 and Windows Server 2003 operating systems, see the applicable Resource Kit, available on the Microsoft TechNet website.</span></span>

<span data-ttu-id="dc792-108">Резервная копия сервера Active Directory должна быть выполнена в режиме в сети и должна быть выполнена при установке служб домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dc792-108">Backup of an Active Directory server must be performed online and must be performed when the Active Directory Domain Services are installed.</span></span> <span data-ttu-id="dc792-109">Домен Active Directory службы основаны на специальной базе данных и экспорте набора функций резервного копирования, предоставляющих интерфейс программной архивации.</span><span class="sxs-lookup"><span data-stu-id="dc792-109">Active Directory Domain Services are built on a special database and export a set of backup functions that provide the programmatic backup interface.</span></span> <span data-ttu-id="dc792-110">Резервная копия не поддерживает добавочное резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="dc792-110">The backup does not support incremental backups.</span></span> <span data-ttu-id="dc792-111">Приложение резервного копирования привязывается к локальной библиотеке DLL на стороне клиента с точками входа, определенными в Нтдсбкли. h.</span><span class="sxs-lookup"><span data-stu-id="dc792-111">A backup application binds to a local client-side DLL with entry points defined in Ntdsbcli.h.</span></span>

<span data-ttu-id="dc792-112">Восстановление сервера Active Directory всегда выполняется в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="dc792-112">Restoration of an Active Directory server is always performed offline.</span></span>

<span data-ttu-id="dc792-113">Хотя в подразделах этого раздела описывается только процесс резервного копирования и восстановления сервера Active Directory, имейте в виду, что Windows 2000 и операционные системы Windows Server 2003 имеют несколько компонентов "состояние системы", которые необходимо архивировать и восстанавливать вместе.</span><span class="sxs-lookup"><span data-stu-id="dc792-113">Although the topics in this section describe only how to back up and restore an Active Directory server, be aware that Windows 2000 and the Windows Server 2003 operating systems have several "system state" components that must be backed up and restored together.</span></span> <span data-ttu-id="dc792-114">Эти компоненты состояния системы состоят из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="dc792-114">These system state components consist of:</span></span>

-   <span data-ttu-id="dc792-115">Загрузочные файлы, такие как NTLDR, нтдетект, все файлы, защищенные SFP, и конфигурация счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="dc792-115">Boot files such as ntldr, ntdetect, all files protected by SFP, and performance counter configuration</span></span>
-   <span data-ttu-id="dc792-116">Контроллер домен Active Directory</span><span class="sxs-lookup"><span data-stu-id="dc792-116">The Active Directory Domain Controller</span></span>
-   <span data-ttu-id="dc792-117">SysVol (только контроллер домена)</span><span class="sxs-lookup"><span data-stu-id="dc792-117">SysVol (domain controller only)</span></span>
-   <span data-ttu-id="dc792-118">Сервер сертификатов (только ЦС)</span><span class="sxs-lookup"><span data-stu-id="dc792-118">Certificate Server (CA only)</span></span>
-   <span data-ttu-id="dc792-119">База данных кластера (только для узла кластера)</span><span class="sxs-lookup"><span data-stu-id="dc792-119">Cluster database (cluster node only)</span></span>
-   <span data-ttu-id="dc792-120">Реестр</span><span class="sxs-lookup"><span data-stu-id="dc792-120">Registry</span></span>
-   <span data-ttu-id="dc792-121">База данных регистрации классов COM+</span><span class="sxs-lookup"><span data-stu-id="dc792-121">COM+ class registration database</span></span>

<span data-ttu-id="dc792-122">Состояние системы можно архивировать в любом порядке, но восстановление состояния системы должно выполняться в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="dc792-122">The system state can be backed up in any order, but restoration of the system state must occur in the following order:</span></span>

1.  <span data-ttu-id="dc792-123">Восстановите файлы загрузки.</span><span class="sxs-lookup"><span data-stu-id="dc792-123">Restore the boot files.</span></span>
2.  <span data-ttu-id="dc792-124">Восстановите SysVol, сервер сертификатов, базу данных кластера и базу данных регистрации классов COM+, как применимо.</span><span class="sxs-lookup"><span data-stu-id="dc792-124">Restore SysVol, Certificate Server, Cluster database and COM+ class registration database, as applicable.</span></span>
3.  <span data-ttu-id="dc792-125">Восстановите сервер Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dc792-125">Restore the Active Directory server.</span></span>
4.  <span data-ttu-id="dc792-126">Восстановите реестр.</span><span class="sxs-lookup"><span data-stu-id="dc792-126">Restore the registry.</span></span>

<span data-ttu-id="dc792-127">Дополнительные сведения о резервном копировании и восстановлении служб сертификатов см. [в разделе Использование функций резервного копирования и восстановления служб сертификатов](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions).</span><span class="sxs-lookup"><span data-stu-id="dc792-127">For more information about backing up and restoring Certificate Services, see [Using the Certificate Services Backup and Restore Functions](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions).</span></span>

<span data-ttu-id="dc792-128">Дополнительные сведения о резервном копировании и восстановлении домен Active Directory служб см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="dc792-128">For more information about backing up and restoring Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="dc792-129">Рекомендации по резервному копированию домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="dc792-129">Considerations for Active Directory Domain Services Backup</span></span>](considerations-for-active-directory-domain-services-backup.md)
-   [<span data-ttu-id="dc792-130">Резервное копирование сервера Active Directory</span><span class="sxs-lookup"><span data-stu-id="dc792-130">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
-   [<span data-ttu-id="dc792-131">Восстановление сервера Active Directory</span><span class="sxs-lookup"><span data-stu-id="dc792-131">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
-   [<span data-ttu-id="dc792-132">Функции резервного копирования каталога</span><span class="sxs-lookup"><span data-stu-id="dc792-132">Directory Backup Functions</span></span>](directory-backup-functions.md)

 

 