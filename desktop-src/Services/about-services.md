---
description: Диспетчер управления службами (SCM) поддерживает базу данных установленных служб и служб драйверов, а также предоставляет унифицированные и безопасные средства управления ими.
ms.assetid: a3af8340-d367-417b-9759-7282edf1d694
title: О службах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87aeec6dfcdc4e2dc0cc0ab3ef084b7927b2c3bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998877"
---
# <a name="about-services"></a><span data-ttu-id="aa13c-103">О службах</span><span class="sxs-lookup"><span data-stu-id="aa13c-103">About Services</span></span>

<span data-ttu-id="aa13c-104">[Диспетчер управления службами](service-control-manager.md) (SCM) поддерживает базу данных установленных служб и служб драйверов, а также предоставляет унифицированные и безопасные средства управления ими.</span><span class="sxs-lookup"><span data-stu-id="aa13c-104">The [service control manager](service-control-manager.md) (SCM) maintains a database of installed services and driver services, and provides a unified and secure means of controlling them.</span></span> <span data-ttu-id="aa13c-105">База данных содержит сведения о том, как должны запускаться службы или служба драйвера.</span><span class="sxs-lookup"><span data-stu-id="aa13c-105">The database includes information on how each service or driver service should be started.</span></span> <span data-ttu-id="aa13c-106">Он также позволяет системным администраторам настраивать требования безопасности для каждой службы и таким образом управлять доступом к службе.</span><span class="sxs-lookup"><span data-stu-id="aa13c-106">It also enables system administrators to customize security requirements for each service and thereby control access to the service.</span></span>

<span data-ttu-id="aa13c-107">Следующие типы программ используют функции, предоставляемые SCM.</span><span class="sxs-lookup"><span data-stu-id="aa13c-107">The following types of programs use the functions provided by the SCM.</span></span>



| <span data-ttu-id="aa13c-108">Тип</span><span class="sxs-lookup"><span data-stu-id="aa13c-108">Type</span></span>                          | <span data-ttu-id="aa13c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="aa13c-109">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa13c-110">Служебная программа</span><span class="sxs-lookup"><span data-stu-id="aa13c-110">Service program</span></span>               | <span data-ttu-id="aa13c-111">Программа, предоставляющая исполняемый код для одной или нескольких служб.</span><span class="sxs-lookup"><span data-stu-id="aa13c-111">A program that provides executable code for one or more services.</span></span> <span data-ttu-id="aa13c-112">Программы службы используют функции, которые подключаются к SCM и отправляют сведения о состоянии SCM.</span><span class="sxs-lookup"><span data-stu-id="aa13c-112">Service programs use functions that connect to the SCM and send status information to the SCM.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="aa13c-113">Программа настройки службы</span><span class="sxs-lookup"><span data-stu-id="aa13c-113">Service configuration program</span></span> | <span data-ttu-id="aa13c-114">Программа, которая запрашивает или изменяет базу данных служб.</span><span class="sxs-lookup"><span data-stu-id="aa13c-114">A program that queries or modifies the services database.</span></span> <span data-ttu-id="aa13c-115">Программы настройки служб используют функции, которые открывают базу данных, устанавливают или удаляют службы в базе данных, запрашивают или изменяют параметры конфигурации и безопасности для установленных служб.</span><span class="sxs-lookup"><span data-stu-id="aa13c-115">Service configuration programs use functions that open the database, install or delete services in the database, and query or modify the configuration and security parameters for installed services.</span></span> <span data-ttu-id="aa13c-116">Программы настройки служб управляют службами и службами драйверов.</span><span class="sxs-lookup"><span data-stu-id="aa13c-116">Service configuration programs manage both services and driver services.</span></span> |
| <span data-ttu-id="aa13c-117">Программа управления службами</span><span class="sxs-lookup"><span data-stu-id="aa13c-117">Service control program</span></span>       | <span data-ttu-id="aa13c-118">Программа, запускающая и управляющая службами и службами драйверов.</span><span class="sxs-lookup"><span data-stu-id="aa13c-118">A program that starts and controls services and driver services.</span></span> <span data-ttu-id="aa13c-119">Программы управления службами используют функции, которые отправляют запросы к SCM, который выполняет запрос.</span><span class="sxs-lookup"><span data-stu-id="aa13c-119">Service control programs use functions that send requests to the SCM, which carries out the request.</span></span>                                                                                                                                                                     |



 

<span data-ttu-id="aa13c-120">В этом обзоре рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="aa13c-120">This overview discusses the following topics:</span></span>

-   [<span data-ttu-id="aa13c-121">Диспетчер служб</span><span class="sxs-lookup"><span data-stu-id="aa13c-121">Service Control Manager</span></span>](service-control-manager.md)
-   [<span data-ttu-id="aa13c-122">Служебные программы</span><span class="sxs-lookup"><span data-stu-id="aa13c-122">Service Programs</span></span>](service-programs.md)
-   [<span data-ttu-id="aa13c-123">Программы настройки служб</span><span class="sxs-lookup"><span data-stu-id="aa13c-123">Service Configuration Programs</span></span>](service-configuration-programs.md)
-   [<span data-ttu-id="aa13c-124">Программы управления службами</span><span class="sxs-lookup"><span data-stu-id="aa13c-124">Service Control Programs</span></span>](service-control-programs.md)
-   [<span data-ttu-id="aa13c-125">Учетные записи пользователей службы</span><span class="sxs-lookup"><span data-stu-id="aa13c-125">Service User Accounts</span></span>](service-user-accounts.md)
-   [<span data-ttu-id="aa13c-126">Интерактивные службы</span><span class="sxs-lookup"><span data-stu-id="aa13c-126">Interactive Services</span></span>](interactive-services.md)
-   [<span data-ttu-id="aa13c-127">Права доступа и безопасности службы</span><span class="sxs-lookup"><span data-stu-id="aa13c-127">Service Security and Access Rights</span></span>](service-security-and-access-rights.md)
-   [<span data-ttu-id="aa13c-128">Отладка службы</span><span class="sxs-lookup"><span data-stu-id="aa13c-128">Debugging a Service</span></span>](debugging-a-service.md)
-   [<span data-ttu-id="aa13c-129">События триггера службы</span><span class="sxs-lookup"><span data-stu-id="aa13c-129">Service Trigger Events</span></span>](service-trigger-events.md)

 

 



