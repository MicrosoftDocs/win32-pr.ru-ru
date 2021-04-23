---
description: Диспетчер управления службами (SCM) управляет службой, отправляя события управления службами в подпрограммы обработчика управления службами.
ms.assetid: 86e04b43-5f6f-409e-ac18-d7efada4d3d3
title: Многопоточные службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5795a170f912050d115537407fcb491305a35ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664200"
---
# <a name="multithreaded-services"></a><span data-ttu-id="4d555-103">Многопоточные службы</span><span class="sxs-lookup"><span data-stu-id="4d555-103">Multithreaded Services</span></span>

<span data-ttu-id="4d555-104">Диспетчер управления службами (SCM) управляет службой, отправляя события управления службами в подпрограммы обработчика управления службы.</span><span class="sxs-lookup"><span data-stu-id="4d555-104">The service control manager (SCM) controls a service by sending service control events to the service's control handler routine.</span></span> <span data-ttu-id="4d555-105">Служба должна своевременно реагировать на события управления, чтобы диспетчер SCM мог контролировать состояние службы.</span><span class="sxs-lookup"><span data-stu-id="4d555-105">The service must respond to control events in a timely manner so that the SCM can keep track of the state of the service.</span></span> <span data-ttu-id="4d555-106">Кроме того, состояние службы должно соответствовать описанию состояния, которое получает диспетчер SCM.</span><span class="sxs-lookup"><span data-stu-id="4d555-106">Also, the state of the service must match the description of its state that the SCM receives.</span></span>

<span data-ttu-id="4d555-107">Из-за этого механизма связи между службой и SCM необходимо соблюдать осторожность при использовании нескольких потоков в службе.</span><span class="sxs-lookup"><span data-stu-id="4d555-107">Due to this communication mechanism between a service and the SCM, you must be careful when using multiple threads in a service.</span></span> <span data-ttu-id="4d555-108">Когда служба передается службе SCM, она должна ждать завершения всех потоков, прежде чем сообщить службе SCM о том, что служба остановлена.</span><span class="sxs-lookup"><span data-stu-id="4d555-108">When a service is instructed to stop by the SCM, it must wait for all the threads to exit before reporting to the SCM that the service is stopped.</span></span> <span data-ttu-id="4d555-109">В противном случае SCM может стать запутанным о состоянии службы и может не завершить работу правильно.</span><span class="sxs-lookup"><span data-stu-id="4d555-109">Otherwise, the SCM can become confused about the state of the service and might fail to shut down correctly.</span></span>

<span data-ttu-id="4d555-110">SCM должен получать уведомления о том, что служба отвечает на событие остановки управления и выполняется в процессе остановки службы.</span><span class="sxs-lookup"><span data-stu-id="4d555-110">The SCM needs to be notified that the service is responding to the stop control event and that progress is being made in stopping the service.</span></span> <span data-ttu-id="4d555-111">SCM считает, что служба выполняется, если служба отвечает (через [**сбой SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)) в течение времени (Подсказка ожидания), указанной в предыдущем вызове **сбой SetServiceStatus**, а контрольная точка обновляется так, чтобы она превышала контрольную точку, указанную в предыдущем вызове **сбой SetServiceStatus**.</span><span class="sxs-lookup"><span data-stu-id="4d555-111">The SCM will assume the service is making progress if the service responds (through [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)) within the time (wait hint) specified in the previous call to **SetServiceStatus**, and the check point is updated to be greater than the checkpoint specified in the previous call to **SetServiceStatus**.</span></span>

<span data-ttu-id="4d555-112">Если служба сообщает SCM о том, что служба остановлена до того, как все потоки завершились, возможно, SCM будет интерпретировать это как противоречие.</span><span class="sxs-lookup"><span data-stu-id="4d555-112">If the service reports to the SCM that the service has stopped before all threads have exited, it is possible that the SCM will interpret this as a contradiction.</span></span> <span data-ttu-id="4d555-113">Это может привести к состоянию, в котором служба не может быть остановлена или перезапущена.</span><span class="sxs-lookup"><span data-stu-id="4d555-113">This might result in a state where the service cannot be stopped or restarted.</span></span>

 

 



