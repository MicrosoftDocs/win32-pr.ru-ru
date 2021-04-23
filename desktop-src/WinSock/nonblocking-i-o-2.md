---
description: Если сокет находится в неблокирующем режиме, любая операция ввода-вывода должна либо завершиться немедленно, либо вернуть код ошибки ВСАЕВАУЛДБЛОКК, указывающий, что операция не может быть завершена сразу.
ms.assetid: badd279b-ec71-4761-9066-d501aa2485c2
title: Неблокируемые входные и выходные данные
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9f6fec896c8daf1998e71a20a23a296b7b5a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541530"
---
# <a name="nonblocking-inputoutput"></a><span data-ttu-id="f3c8a-103">Неблокируемые входные и выходные данные</span><span class="sxs-lookup"><span data-stu-id="f3c8a-103">Nonblocking Input/Output</span></span>

<span data-ttu-id="f3c8a-104">Если сокет находится в неблокирующем режиме, любая операция ввода-вывода должна либо завершиться немедленно, либо вернуть код ошибки ВСАЕВАУЛДБЛОКК, указывающий, что операция не может быть завершена сразу.</span><span class="sxs-lookup"><span data-stu-id="f3c8a-104">If a socket is in nonblocking mode, any I/O operation must either complete immediately or return the error code WSAEWOULDBLOCK indicating that the operation cannot be finished right away.</span></span> <span data-ttu-id="f3c8a-105">В последнем случае необходимо использовать механизм, чтобы определить, когда может потребоваться повторить операцию с ожиданием, что операция будет выполнена.</span><span class="sxs-lookup"><span data-stu-id="f3c8a-105">In the latter case, a mechanism is needed to discover when it is appropriate to try the operation again with the expectation that the operation will succeed.</span></span> <span data-ttu-id="f3c8a-106">Для этой цели определен набор сетевых событий.</span><span class="sxs-lookup"><span data-stu-id="f3c8a-106">A set of network events has been defined for this purpose.</span></span> <span data-ttu-id="f3c8a-107">Эти события можно опрашивать или ожидать с помощью [**вспселект**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))или можно зарегистрировать для асинхронной доставки, вызвав [**вспасинкселект**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) или [**вспевентселект**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3c8a-107">These events can be polled or waited on by using [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)), or they can be registered for asynchronous delivery by calling [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) or [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span></span> <span data-ttu-id="f3c8a-108">Дополнительные сведения см. в разделе [уведомление о сетевых событиях](notification-of-network-events-2.md) .</span><span class="sxs-lookup"><span data-stu-id="f3c8a-108">See [Notification of Network Events](notification-of-network-events-2.md) for more information.</span></span>

 

 
