---
title: Single-Threaded и многопоточное взаимодействие
description: Single-Threaded и многопоточное взаимодействие
ms.assetid: 8d3a855c-b52d-48bb-9fdf-efbf8005c374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6470ac398e6ae1c8a645fb076fbbf509d58b579
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329304"
---
# <a name="single-threaded-and-multithreaded-communication"></a><span data-ttu-id="cc09e-103">Single-Threaded и многопоточное взаимодействие</span><span class="sxs-lookup"><span data-stu-id="cc09e-103">Single-Threaded and Multithreaded Communication</span></span>

<span data-ttu-id="cc09e-104">Клиент или сервер, поддерживающий как однопотоковые, так и многопоточные подразделения, будут иметь один многопоточный апартамент, содержащий все потоки, инициализированные в качестве свободных потоков, и один или несколько однопотоковых апартаментов.</span><span class="sxs-lookup"><span data-stu-id="cc09e-104">A client or server that supports both single-threaded and multithreaded apartments will have one multithreaded apartment, containing all threads initialized as free-threaded, and one or more single-threaded apartments.</span></span> <span data-ttu-id="cc09e-105">Указатели интерфейса должны быть упакованы между апартаментами, но их можно использовать без маршалирования в апартамент.</span><span class="sxs-lookup"><span data-stu-id="cc09e-105">Interface pointers must be marshaled between apartments but can be used without marshaling within an apartment.</span></span> <span data-ttu-id="cc09e-106">Вызовы объектов в однопотоковом апартаменте будут синхронизированы COM.</span><span class="sxs-lookup"><span data-stu-id="cc09e-106">Calls to objects in a single-threaded apartment will be synchronized by COM.</span></span> <span data-ttu-id="cc09e-107">Вызовы объектов в многопоточном апартаменте не будут синхронизированы COM.</span><span class="sxs-lookup"><span data-stu-id="cc09e-107">Calls to objects in the multithreaded apartment will not be synchronized by COM.</span></span>

<span data-ttu-id="cc09e-108">Вся информация о однопотоковых апартаментах применяется к потокам, помеченным как модель подразделения, и вся информация о многопоточных подразделениях применяется ко всем потокам, помеченным как свободные потоки.</span><span class="sxs-lookup"><span data-stu-id="cc09e-108">All of the information on single-threaded apartments applies to the threads marked as apartment model, and all of the information on multithreaded apartments applies to all of the threads marked as free-threaded.</span></span> <span data-ttu-id="cc09e-109">Правила потоков подразделений применяются к взаимодействию между апартаментами. при этом указатели интерфейса должны быть упакованы между апартаментами с вызовами [**комаршалинтерсреадинтерфацеинстреам**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) и [**кожетинтерфацеандрелеасестреам**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream), как описано в [однопотоковых апартаментах](single-threaded-apartments.md).</span><span class="sxs-lookup"><span data-stu-id="cc09e-109">Apartment threading rules apply to inter-apartment communication, requiring that interface pointers be marshaled between apartments with calls to [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) and [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream), as described in [Single-Threaded Apartments](single-threaded-apartments.md).</span></span>

> [!Note]  
> <span data-ttu-id="cc09e-110">При работе с внутрипроцессного серверами применяются некоторые особенности.</span><span class="sxs-lookup"><span data-stu-id="cc09e-110">Some special considerations apply when dealing with in-process servers.</span></span> <span data-ttu-id="cc09e-111">Дополнительные сведения см. [в разделе проблемы потоковой обработки на сервере](in-process-server-threading-issues.md).</span><span class="sxs-lookup"><span data-stu-id="cc09e-111">For more information, see [In-Process Server Threading Issues](in-process-server-threading-issues.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cc09e-112">См. также</span><span class="sxs-lookup"><span data-stu-id="cc09e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc09e-113">Доступ к интерфейсам в разных апартаментах</span><span class="sxs-lookup"><span data-stu-id="cc09e-113">Accessing Interfaces Across Apartments</span></span>](accessing-interfaces-across-apartments.md)
</dt> <dt>

[<span data-ttu-id="cc09e-114">Выбор потоковой модели</span><span class="sxs-lookup"><span data-stu-id="cc09e-114">Choosing the Threading Model</span></span>](choosing-the-threading-model.md)
</dt> <dt>

[<span data-ttu-id="cc09e-115">Многопоточные подразделения</span><span class="sxs-lookup"><span data-stu-id="cc09e-115">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="cc09e-116">Проблемы потоковой обработки в процессе сервера</span><span class="sxs-lookup"><span data-stu-id="cc09e-116">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="cc09e-117">Процессы, потоки и подразделения</span><span class="sxs-lookup"><span data-stu-id="cc09e-117">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="cc09e-118">Подразделения с одним потоком</span><span class="sxs-lookup"><span data-stu-id="cc09e-118">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




