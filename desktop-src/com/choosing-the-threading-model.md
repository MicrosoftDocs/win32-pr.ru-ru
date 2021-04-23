---
title: Выбор потоковой модели
description: Выбор потоковой модели
ms.assetid: e8a0286d-1831-454f-8549-1957fd794809
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f0fdcd327bf05c0019a03ad171d41c1f1d95a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411349"
---
# <a name="choosing-the-threading-model"></a><span data-ttu-id="f0800-103">Выбор потоковой модели</span><span class="sxs-lookup"><span data-stu-id="f0800-103">Choosing the Threading Model</span></span>

<span data-ttu-id="f0800-104">Выбор модели потоков для объекта зависит от функции объекта.</span><span class="sxs-lookup"><span data-stu-id="f0800-104">Choosing the threading model for an object depends on the object's function.</span></span> <span data-ttu-id="f0800-105">Объект, который выполняет широкие возможности ввода-вывода, может поддерживать бесплатную поддержку потоков, чтобы обеспечить максимальное реагирование на клиентов, разрешая вызовы интерфейса во время задержки ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="f0800-105">An object that does extensive I/O might support free-threading to provide maximum response to clients by allowing interface calls during I/O latency.</span></span> <span data-ttu-id="f0800-106">С другой стороны, объект, взаимодействующий с пользователем, может поддерживать потоковое разделение для синхронизации входящих вызовов COM с операциями окна.</span><span class="sxs-lookup"><span data-stu-id="f0800-106">On the other hand, an object that interacts with the user might support apartment threading to synchronize incoming COM calls with its window operations.</span></span>

<span data-ttu-id="f0800-107">Проще поддерживать потоковое подразделение в однопотоковых апартаментах, так как COM обеспечивает синхронизацию на основе каждого вызова.</span><span class="sxs-lookup"><span data-stu-id="f0800-107">It is easier to support apartment threading in single-threaded apartments because COM provides synchronization on a per-call basis.</span></span> <span data-ttu-id="f0800-108">Поддержка свободной потоковой реализации сложнее, поскольку объект должен реализовывать синхронизацию. Однако отклики на клиенты могут быть лучше, так как синхронизация может быть реализована для небольших разделов кода.</span><span class="sxs-lookup"><span data-stu-id="f0800-108">Supporting free-threading is more difficult because the object must implement synchronization; however, response to clients may be better because synchronization can be implemented for smaller sections of code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0800-109">См. также</span><span class="sxs-lookup"><span data-stu-id="f0800-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0800-110">Доступ к интерфейсам в разных апартаментах</span><span class="sxs-lookup"><span data-stu-id="f0800-110">Accessing Interfaces Across Apartments</span></span>](accessing-interfaces-across-apartments.md)
</dt> <dt>

[<span data-ttu-id="f0800-111">Многопоточные подразделения</span><span class="sxs-lookup"><span data-stu-id="f0800-111">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="f0800-112">Проблемы потоковой обработки в процессе сервера</span><span class="sxs-lookup"><span data-stu-id="f0800-112">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="f0800-113">Процессы, потоки и подразделения</span><span class="sxs-lookup"><span data-stu-id="f0800-113">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="f0800-114">Однопотоковое и многопоточное взаимодействие</span><span class="sxs-lookup"><span data-stu-id="f0800-114">Single-Threaded and Multithreaded Communication</span></span>](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[<span data-ttu-id="f0800-115">Подразделения с одним потоком</span><span class="sxs-lookup"><span data-stu-id="f0800-115">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




