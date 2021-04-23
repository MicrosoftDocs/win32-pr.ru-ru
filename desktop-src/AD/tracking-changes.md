---
title: Отслеживание изменений
description: Некоторые приложения должны поддерживать согласованность между конкретными данными, хранящимися в Active Directory службе каталогов и другими данными.
ms.assetid: f4539482-1170-4c0c-b817-b39e58049d39
ms.tgt_platform: multiple
keywords:
- Active Directory, использование, отслеживание изменений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dc772f883b97eb4e7305b39f0a582448a8bc021
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103987304"
---
# <a name="tracking-changes"></a><span data-ttu-id="f2a17-104">Отслеживание изменений</span><span class="sxs-lookup"><span data-stu-id="f2a17-104">Tracking Changes</span></span>

<span data-ttu-id="f2a17-105">Некоторые приложения должны поддерживать согласованность между конкретными данными, хранящимися в Active Directory службе каталогов и другими данными.</span><span class="sxs-lookup"><span data-stu-id="f2a17-105">Some applications must maintain consistency between specific data stored in the Active Directory directory service and other data.</span></span> <span data-ttu-id="f2a17-106">Другие данные могут храниться в каталоге, в SQL Server таблице, в файле или в реестре.</span><span class="sxs-lookup"><span data-stu-id="f2a17-106">The other data might be stored in the directory, in a SQL Server table, in a file, or in the registry.</span></span> <span data-ttu-id="f2a17-107">При изменении данных, хранящихся в каталоге, может потребоваться изменить другие данные, чтобы они оставались постоянными.</span><span class="sxs-lookup"><span data-stu-id="f2a17-107">When data stored in the directory changes, the other data may be required to change in order to remain consistent.</span></span> <span data-ttu-id="f2a17-108">В число приложений, которые входят в это требование:</span><span class="sxs-lookup"><span data-stu-id="f2a17-108">Applications that have this requirement include:</span></span>

<span data-ttu-id="f2a17-109">В этом разделе не рассматриваются механизмы, используемые приложениями мониторинга.</span><span class="sxs-lookup"><span data-stu-id="f2a17-109">This section does not cover mechanisms used by monitoring applications.</span></span> <span data-ttu-id="f2a17-110">Это приложения, отслеживающие изменения каталога, не предназначенные для поддержания согласованных данных между отдельными хранилищами, но в качестве средства управления системой.</span><span class="sxs-lookup"><span data-stu-id="f2a17-110">These are applications that monitor directory changes not for the purpose of maintaining consistent data between separate stores, but as a system management tool.</span></span> <span data-ttu-id="f2a17-111">Хотя мониторинг приложений может использовать те же механизмы, которые поддерживают приложения отслеживания изменений, следующие механизмы предназначены специально для мониторинга приложений:</span><span class="sxs-lookup"><span data-stu-id="f2a17-111">Although monitoring applications can use the same mechanisms that support change-tracking applications, the following mechanisms are specifically designed for monitoring applications:</span></span>

-   <span data-ttu-id="f2a17-112">Аудит безопасности.</span><span class="sxs-lookup"><span data-stu-id="f2a17-112">Security auditing.</span></span> <span data-ttu-id="f2a17-113">Изменяя часть списка управления доступом к системе (SACL) дескриптора безопасности объекта, вы можете вызвать доступ к объекту на данном контроллере домена для создания записей аудита в журнале событий безопасности на этом DC.</span><span class="sxs-lookup"><span data-stu-id="f2a17-113">By modifying the system access-control list (SACL) portion of an object security descriptor, you can cause accesses to the object on a given domain controller to generate audit records in the security event log on that DC.</span></span> <span data-ttu-id="f2a17-114">Можно выполнять аудит операций чтения, записи или и того, и другого. можно выполнить аудит всего объекта или отдельных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="f2a17-114">You can audit reads, writes, or both; you can audit the entire object or specific attributes.</span></span> <span data-ttu-id="f2a17-115">Дополнительные сведения см. в разделе [Получение списка SACL объекта](retrieving-an-objectampaposs-sacl.md) и [Создание аудита](/windows/desktop/SecAuthZ/audit-generation).</span><span class="sxs-lookup"><span data-stu-id="f2a17-115">For more information, see [Retrieving an Object's SACL](retrieving-an-objectampaposs-sacl.md) and [Audit Generation](/windows/desktop/SecAuthZ/audit-generation).</span></span>
-   <span data-ttu-id="f2a17-116">ведение журнала событий;</span><span class="sxs-lookup"><span data-stu-id="f2a17-116">Event logging.</span></span> <span data-ttu-id="f2a17-117">Изменяя параметры реестра на заданном контроллере домена, можно изменять типы событий, регистрируемых в журнале событий службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="f2a17-117">By modifying registry settings on a given domain controller, you can change the kinds of events logged to the directory service event log.</span></span> <span data-ttu-id="f2a17-118">В частности, чтобы внести в журнал все изменения, установите значение **8 для доступа к каталогу** в следующем разделе реестра равным 4.</span><span class="sxs-lookup"><span data-stu-id="f2a17-118">Specifically, to log all modifications, set the **8 Directory Access** value under the following registry key to 4.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                NTDS
                   Diagnostics
    ```

    <span data-ttu-id="f2a17-119">Дополнительные сведения см. в разделе [ведение журнала событий](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="f2a17-119">For more information, see [Event Logging](/windows/desktop/EventLog/event-logging).</span></span>

-   <span data-ttu-id="f2a17-120">Трассировка событий.</span><span class="sxs-lookup"><span data-stu-id="f2a17-120">Event tracing.</span></span> <span data-ttu-id="f2a17-121">В Windows 2000 появился API трассировки событий для трассировки и ведения журнала интересных событий программного или аппаратного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="f2a17-121">Windows 2000 introduced an Event Tracing API for tracing and logging interesting events in software or hardware.</span></span> <span data-ttu-id="f2a17-122">Операционная система Windows и домен Active Directory служб в частности поддерживают использование трассировки событий для планирования емкости и подробного анализа производительности.</span><span class="sxs-lookup"><span data-stu-id="f2a17-122">The Windows operating system, and Active Directory Domain Services in particular, support the use of event tracing for capacity planning and detailed performance analysis.</span></span> <span data-ttu-id="f2a17-123">Дополнительные сведения см. в разделе [Трассировка событий](/windows/desktop/ETW/event-tracing-portal) и [Трассировка событий в ADSI](/windows/desktop/ADSI/adsi-and-etw).</span><span class="sxs-lookup"><span data-stu-id="f2a17-123">For more information, see [Event Tracing](/windows/desktop/ETW/event-tracing-portal) and [Event Tracing in ADSI](/windows/desktop/ADSI/adsi-and-etw).</span></span>

<span data-ttu-id="f2a17-124">Этот раздел содержит следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="f2a17-124">This section includes the following topics:</span></span>

-   [<span data-ttu-id="f2a17-125">Общие сведения о методах Отслеживание изменений</span><span class="sxs-lookup"><span data-stu-id="f2a17-125">Overview of Change Tracking Techniques</span></span>](overview-of-change-tracking-techniques.md)
-   [<span data-ttu-id="f2a17-126">Уведомления об изменениях в службах домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="f2a17-126">Change Notifications in Active Directory Domain Services</span></span>](change-notifications-in-active-directory-domain-services.md)
-   [<span data-ttu-id="f2a17-127">Опрос изменений с помощью элемента управления DirSync</span><span class="sxs-lookup"><span data-stu-id="f2a17-127">Polling for Changes Using the DirSync Control</span></span>](polling-for-changes-using-the-dirsync-control.md)
-   [<span data-ttu-id="f2a17-128">Опрос изменений с помощью USNChanged</span><span class="sxs-lookup"><span data-stu-id="f2a17-128">Polling for Changes Using USNChanged</span></span>](polling-for-changes-using-usnchanged.md)

 

 