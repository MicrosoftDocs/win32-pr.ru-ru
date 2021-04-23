---
description: Запускается программа управления службами, которая управляет службами.
ms.assetid: e7ba295f-2937-44ad-89e8-40200c5e58b6
title: Программы управления службами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78b34232f5f87d84bdf30acd51f57afbf79a8385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897150"
---
# <a name="service-control-programs"></a><span data-ttu-id="716eb-103">Программы управления службами</span><span class="sxs-lookup"><span data-stu-id="716eb-103">Service Control Programs</span></span>

<span data-ttu-id="716eb-104">Запускается программа управления службами, которая управляет службами.</span><span class="sxs-lookup"><span data-stu-id="716eb-104">A service control program starts and controls services.</span></span> <span data-ttu-id="716eb-105">Он выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="716eb-105">It performs the following actions:</span></span>

-   <span data-ttu-id="716eb-106">Запускает службу или драйвер, если тип запуска — \_ Запуск по запросу службы \_ .</span><span class="sxs-lookup"><span data-stu-id="716eb-106">Starts a service or driver service, if the start type is SERVICE\_DEMAND\_START.</span></span>
-   <span data-ttu-id="716eb-107">Отправляет управляющие запросы в работающую службу.</span><span class="sxs-lookup"><span data-stu-id="716eb-107">Sends control requests to a running service.</span></span>
-   <span data-ttu-id="716eb-108">Запрашивает текущее состояние выполняющейся службы.</span><span class="sxs-lookup"><span data-stu-id="716eb-108">Queries the current status of a running service.</span></span>

<span data-ttu-id="716eb-109">Для этих действий требуется открытый обработчик для объекта службы.</span><span class="sxs-lookup"><span data-stu-id="716eb-109">These actions require an open handle to the service object.</span></span> <span data-ttu-id="716eb-110">Для получения этого маркера программа управления службой должна:</span><span class="sxs-lookup"><span data-stu-id="716eb-110">To obtain the handle, the service control program must:</span></span>

1.  <span data-ttu-id="716eb-111">Используйте функцию [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) для получения маркера базы данных SCM на указанном компьютере.</span><span class="sxs-lookup"><span data-stu-id="716eb-111">Use the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to obtain a handle to the SCM database on a specified machine.</span></span>
2.  <span data-ttu-id="716eb-112">Используйте функцию [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) или [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) для получения маркера объекта службы.</span><span class="sxs-lookup"><span data-stu-id="716eb-112">Use the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) or [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to obtain a handle to the service object.</span></span>

<span data-ttu-id="716eb-113">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="716eb-113">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="716eb-114">Запуск службы</span><span class="sxs-lookup"><span data-stu-id="716eb-114">Service Startup</span></span>](service-startup.md)
-   [<span data-ttu-id="716eb-115">Запросы управления службами</span><span class="sxs-lookup"><span data-stu-id="716eb-115">Service Control Requests</span></span>](service-control-requests.md)
-   [<span data-ttu-id="716eb-116">Управление службой с помощью SC</span><span class="sxs-lookup"><span data-stu-id="716eb-116">Controlling a Service Using SC</span></span>](controlling-a-service-using-sc.md)

 

 



