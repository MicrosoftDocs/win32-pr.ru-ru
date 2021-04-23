---
title: Системный агент каталога
description: Агент системы каталогов (DSA) — это набор служб и процессов, которые выполняются на каждом контроллере домена и предоставляют доступ к хранилищу данных.
ms.assetid: a921a822-6b2e-4a84-8112-0ae516443667
ms.tgt_platform: multiple
keywords:
- Active Directory системного агента каталога
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df39d1670f6668f933c20bcd2b9a8771ce83ec56
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103890443"
---
# <a name="directory-system-agent"></a><span data-ttu-id="6f180-104">Системный агент каталога</span><span class="sxs-lookup"><span data-stu-id="6f180-104">Directory System Agent</span></span>

<span data-ttu-id="6f180-105">[*Агент системы каталогов*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) (DSA) — это набор служб и процессов, которые выполняются на каждом контроллере домена и предоставляют доступ к хранилищу данных.</span><span class="sxs-lookup"><span data-stu-id="6f180-105">The [*directory system agent*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) (DSA) is a collection of services and processes that run on each domain controller and provides access to the data store.</span></span> <span data-ttu-id="6f180-106">Хранилище данных — это физическое хранилище данных каталога, расположенное на жестком диске.</span><span class="sxs-lookup"><span data-stu-id="6f180-106">The data store is the physical store of directory data located on a hard disk.</span></span> <span data-ttu-id="6f180-107">В домен Active Directory Services DSA является частью подсистемы локального системного администратора (LSA).</span><span class="sxs-lookup"><span data-stu-id="6f180-107">In Active Directory Domain Services, the DSA is part of the local system authority (LSA) subsystem.</span></span> <span data-ttu-id="6f180-108">Клиенты получают доступ к каталогу с помощью одного из следующих механизмов, поддерживаемых DSA:</span><span class="sxs-lookup"><span data-stu-id="6f180-108">Clients access the directory using one of the following mechanisms supported by the DSA:</span></span>

-   <span data-ttu-id="6f180-109">Клиенты LDAP подключаются к DSA с помощью протокола LDAP.</span><span class="sxs-lookup"><span data-stu-id="6f180-109">LDAP clients connect to the DSA using the Lightweight Directory Access Protocol (LDAP).</span></span> <span data-ttu-id="6f180-110">Службы домен Active Directory Services поддерживают LDAP 3,0, определенный стандартом RFC 3377 и LDAP 2,0, который определяется RFC 1777.</span><span class="sxs-lookup"><span data-stu-id="6f180-110">Active Directory Domain Services support LDAP 3.0, defined by RFC 3377, and LDAP 2.0, defined by RFC 1777.</span></span> <span data-ttu-id="6f180-111">Клиенты Windows используют LDAP 3,0 для подключения к DSA.</span><span class="sxs-lookup"><span data-stu-id="6f180-111">Windows clients use LDAP 3.0 to connect to the DSA.</span></span>
-   <span data-ttu-id="6f180-112">Клиенты MAPI, такие как Microsoft Exchange Server, подключаются к DSA с помощью интерфейса удаленного вызова процедуры MAPI.</span><span class="sxs-lookup"><span data-stu-id="6f180-112">MAPI clients such as Microsoft Exchange Server connect to the DSA using the MAPI remote procedure call interface.</span></span>
-   <span data-ttu-id="6f180-113">DSA в домен Active Directory Services подключаются друг к другу для выполнения репликации с помощью собственного интерфейса удаленного вызова процедур.</span><span class="sxs-lookup"><span data-stu-id="6f180-113">The DSAs in Active Directory Domain Services connect to each other to perform replication using a proprietary remote procedure call interface.</span></span>

 

 