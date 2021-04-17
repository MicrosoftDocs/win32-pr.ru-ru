---
description: Диспетчер управления службами (SCM) запускается при загрузке системы. Это сервер удаленного вызова процедур (RPC), который позволяет программам настройки служб и управления службами управлять службами на удаленных компьютерах.
ms.assetid: 56ad011d-17c4-4410-b598-6ef47fb3638f
title: Диспетчер служб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8a35fd34bd2714d22d40ccf618c89a8b66a6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662353"
---
# <a name="service-control-manager"></a><span data-ttu-id="9be79-104">Диспетчер служб</span><span class="sxs-lookup"><span data-stu-id="9be79-104">Service Control Manager</span></span>

<span data-ttu-id="9be79-105">Диспетчер управления службами (SCM) запускается при загрузке системы.</span><span class="sxs-lookup"><span data-stu-id="9be79-105">The service control manager (SCM) is started at system boot.</span></span> <span data-ttu-id="9be79-106">Это сервер удаленного вызова процедур (RPC), который позволяет программам настройки служб и управления службами управлять службами на удаленных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="9be79-106">It is a remote procedure call (RPC) server, so that service configuration and service control programs can manipulate services on remote machines.</span></span>

<span data-ttu-id="9be79-107">Функции службы предоставляют интерфейс для следующих задач, выполняемых SCM:</span><span class="sxs-lookup"><span data-stu-id="9be79-107">The service functions provide an interface for the following tasks performed by the SCM:</span></span>

-   <span data-ttu-id="9be79-108">Обслуживание базы данных установленных служб.</span><span class="sxs-lookup"><span data-stu-id="9be79-108">Maintaining the database of installed services.</span></span>
-   <span data-ttu-id="9be79-109">Запуск служб и служб драйверов при запуске системы или по требованию.</span><span class="sxs-lookup"><span data-stu-id="9be79-109">Starting services and driver services either upon system startup or upon demand.</span></span>
-   <span data-ttu-id="9be79-110">Перечисление установленных служб и служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="9be79-110">Enumerating installed services and driver services.</span></span>
-   <span data-ttu-id="9be79-111">Поддержание сведений о состоянии выполняющихся служб и служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="9be79-111">Maintaining status information for running services and driver services.</span></span>
-   <span data-ttu-id="9be79-112">Передача управляющих запросов на выполнение служб.</span><span class="sxs-lookup"><span data-stu-id="9be79-112">Transmitting control requests to running services.</span></span>
-   <span data-ttu-id="9be79-113">Блокировка и разблокировка базы данных службы.</span><span class="sxs-lookup"><span data-stu-id="9be79-113">Locking and unlocking the service database.</span></span>

<span data-ttu-id="9be79-114">В следующих разделах более подробно описывается Диспетчер служб:</span><span class="sxs-lookup"><span data-stu-id="9be79-114">The following sections describe the SCM in more detail:</span></span>

-   [<span data-ttu-id="9be79-115">База данных установленных служб</span><span class="sxs-lookup"><span data-stu-id="9be79-115">Database of Installed Services</span></span>](database-of-installed-services.md)
-   [<span data-ttu-id="9be79-116">Автоматический запуск служб</span><span class="sxs-lookup"><span data-stu-id="9be79-116">Automatically Starting Services</span></span>](automatically-starting-services.md)
-   [<span data-ttu-id="9be79-117">Запуск служб по требованию</span><span class="sxs-lookup"><span data-stu-id="9be79-117">Starting Services on Demand</span></span>](starting-services-on-demand.md)
-   [<span data-ttu-id="9be79-118">Список записей службы</span><span class="sxs-lookup"><span data-stu-id="9be79-118">Service Record List</span></span>](service-record-list.md)
-   [<span data-ttu-id="9be79-119">Дескрипторы SCM</span><span class="sxs-lookup"><span data-stu-id="9be79-119">SCM Handles</span></span>](scm-handles.md)

 

 



