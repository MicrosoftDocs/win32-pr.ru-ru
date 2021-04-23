---
title: Поиск сервера узла раздела каталога приложений
description: В этом разделе описывается, как разместить сервер узла раздела каталога приложений.
ms.assetid: 636e8bc2-136c-42be-aa64-1b059dedf775
ms.tgt_platform: multiple
keywords:
- Поиск сервера узла раздела каталога приложений AD
- Разделы каталога приложений Active Directory, поиск сервера узла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c9e8f80ccf4b1549af9a76e7b588685d38c297
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773142"
---
# <a name="locating-an-application-directory-partition-host-server"></a><span data-ttu-id="f58d2-105">Поиск сервера узла раздела каталога приложений</span><span class="sxs-lookup"><span data-stu-id="f58d2-105">Locating an Application Directory Partition Host Server</span></span>

<span data-ttu-id="f58d2-106">Служба NetLogon регистрирует следующий список записей SRV для раздела каталога приложений:</span><span class="sxs-lookup"><span data-stu-id="f58d2-106">The NetLogon service registers the following list of SRV records for an application directory partition:</span></span>

-   <span data-ttu-id="f58d2-107">\_Протокол LDAP. \_ входящий.<partition name></span><span class="sxs-lookup"><span data-stu-id="f58d2-107">\_ldap.\_tcp.<partition name></span></span>
-   <span data-ttu-id="f58d2-108">\_Протокол LDAP. \_ TCP. <site name> . \_ черн.<partition name></span><span class="sxs-lookup"><span data-stu-id="f58d2-108">\_ldap.\_tcp.<site name>.\_sites.<partition name></span></span>

<span data-ttu-id="f58d2-109">Чтобы определить контроллер домена, на котором размещена реплика указанного раздела каталога приложений, вызовите функцию [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) с параметром *имя_домена* , заданным как DNS-имя раздела каталога приложений, и установленный в параметре *flags* флаг **\_ \_ LDAP \_ только DS** .</span><span class="sxs-lookup"><span data-stu-id="f58d2-109">To locate a domain controller that hosts a replica of a specified application directory partition, call the [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) function with the *DomainName* parameter set to the DNS name of the application directory partition and the **DS\_ONLY\_LDAP\_NEEDED** flag set in the *Flags* parameter.</span></span> <span data-ttu-id="f58d2-110">Дополнительные сведения и пример кода, демонстрирующий использование функции **DsGetDcName** , как найти контроллер домена, на котором размещена реплика раздела каталога приложений, см. в разделе [пример кода для поиска сервера узла раздела каталога приложений](example-code-for-locating-an-application-directory-partition-host-server.md).</span><span class="sxs-lookup"><span data-stu-id="f58d2-110">For more information and a code example that shows, using the **DsGetDcName** function, how to locate a domain controller that hosts a replica of an application directory partition, see [Example Code for Locating an Application Directory Partition Host Server](example-code-for-locating-an-application-directory-partition-host-server.md).</span></span>

 

 




