---
description: Несколько процессов могут иметь дескрипторы одного и того же события, мьютекса, семафора или объекта таймера, поэтому эти объекты можно использовать для выполнения синхронизации между процессами.
ms.assetid: 1738e586-580f-4b74-95dc-ede300b6ac9a
title: Синхронизация между процессами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c18fb26d6a64fdc2d785d16c7bccb8b007c3f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663882"
---
# <a name="interprocess-synchronization"></a><span data-ttu-id="bd313-103">Синхронизация между процессами</span><span class="sxs-lookup"><span data-stu-id="bd313-103">Interprocess Synchronization</span></span>

<span data-ttu-id="bd313-104">Несколько процессов могут иметь дескрипторы одного и того же события, мьютекса, семафора или объекта таймера, поэтому эти объекты можно использовать для выполнения синхронизации между процессами.</span><span class="sxs-lookup"><span data-stu-id="bd313-104">Multiple processes can have handles to the same event, mutex, semaphore, or timer object, so these objects can be used to accomplish interprocess synchronization.</span></span> <span data-ttu-id="bd313-105">Процесс, создающий объект, может использовать маркер, возвращенный функцией создания ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**createsemaphore-**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)или [**сбой createwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)).</span><span class="sxs-lookup"><span data-stu-id="bd313-105">The process that creates an object can use the handle returned by the creation function ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea), or [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)).</span></span> <span data-ttu-id="bd313-106">Другие процессы могут открыть обработчик для объекта, используя его имя или наследование или дублирование.</span><span class="sxs-lookup"><span data-stu-id="bd313-106">Other processes can open a handle to the object by using its name, or through inheritance or duplication.</span></span> <span data-ttu-id="bd313-107">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="bd313-107">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="bd313-108">Имена объектов</span><span class="sxs-lookup"><span data-stu-id="bd313-108">Object Names</span></span>](object-names.md)
-   [<span data-ttu-id="bd313-109">Наследование объектов</span><span class="sxs-lookup"><span data-stu-id="bd313-109">Object Inheritance</span></span>](object-inheritance.md)
-   [<span data-ttu-id="bd313-110">Дублирование объектов</span><span class="sxs-lookup"><span data-stu-id="bd313-110">Object Duplication</span></span>](object-duplication.md)

 

 
