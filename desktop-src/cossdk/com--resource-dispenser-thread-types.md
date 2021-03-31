---
description: Типы потоков распределителя ресурсов COM+
ms.assetid: 3ab67adb-311f-404c-a3ca-d274af53f91c
title: Типы потоков распределителя ресурсов COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761d85edc3105785ded904fd2dc6083a9aea30cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423277"
---
# <a name="com-resource-dispenser-thread-types"></a><span data-ttu-id="20e83-103">Типы потоков распределителя ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="20e83-103">COM+ Resource Dispenser Thread Types</span></span>

<span data-ttu-id="20e83-104">Вызовы распределителя ресурсов COM+ могут исходить в одном из следующих типов потоков:</span><span class="sxs-lookup"><span data-stu-id="20e83-104">Calls into a COM+ resource dispenser may originate in one of the following thread types:</span></span>

-   <span data-ttu-id="20e83-105">Апартаментный поток (STA)</span><span class="sxs-lookup"><span data-stu-id="20e83-105">Apartment thread (STA)</span></span>
-   <span data-ttu-id="20e83-106">Свободный поток (MTA)</span><span class="sxs-lookup"><span data-stu-id="20e83-106">Free thread (MTA)</span></span>
-   <span data-ttu-id="20e83-107">Поток, не связанный с COM (приложение или поток сборщика мусора диспетчера программ- [распределителя](com--dispenser-manager.md) )</span><span class="sxs-lookup"><span data-stu-id="20e83-107">Non-COM thread (application or the [dispenser manager](com--dispenser-manager.md) garbage-collector thread)</span></span>

<span data-ttu-id="20e83-108">Если распределитель ресурсов не является COM-объектом, он должен иметь возможность обрабатывать вызовы, поступающие из любого потока в любое время.</span><span class="sxs-lookup"><span data-stu-id="20e83-108">If a resource dispenser is not a COM object, it must be able to handle calls arriving from any thread at any time.</span></span> <span data-ttu-id="20e83-109">Если распределитель ресурсов является COM-объектом, COM-объект должен быть зарегистрирован в потоковой модели **обоих типов**.</span><span class="sxs-lookup"><span data-stu-id="20e83-109">If a resource dispenser is a COM object, the COM object should be registered with a threading model of **Both**.</span></span> <span data-ttu-id="20e83-110">Это позволяет потокам STA или MTA создавать и использовать распределитель ресурсов без переключения потока.</span><span class="sxs-lookup"><span data-stu-id="20e83-110">This allows STA or MTA threads to create and use the resource dispenser without a thread switch.</span></span>

<span data-ttu-id="20e83-111">Если распределитель ресурсов создает и использует другой COM-объект (например, диспетчер ресурсов вне процесса), ему может потребоваться поддерживать несколько учетных записей-посредников для этого другого объекта COM и гарантировать, что вызовы объекта выполняются с помощью соответствующего прокси-сервера для вызывающего потока.</span><span class="sxs-lookup"><span data-stu-id="20e83-111">If a resource dispenser creates and uses another COM object (for example, an out-of-process resource manager), the resource dispenser might need to maintain multiple proxies to this other COM object and ensure that calls to the object are made using the appropriate proxy for the calling thread.</span></span> <span data-ttu-id="20e83-112">Когда распределитель ресурсов создает этот объект, он маршалирует и сохраняет ссылку.</span><span class="sxs-lookup"><span data-stu-id="20e83-112">When the resource dispenser creates this object, it marshals and saves the reference.</span></span> <span data-ttu-id="20e83-113">Перед повторным вызовом объекта его необходимо распаковать, чтобы создать прокси-сервер для вызывающего потока.</span><span class="sxs-lookup"><span data-stu-id="20e83-113">Before calling the object again, it must unmarshal to create a proxy for the calling thread.</span></span>

<span data-ttu-id="20e83-114">Возможно, более эффективно кэшировать эти прокси для каждого потока, сохранив карту из идентификатора потока в указатель прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="20e83-114">It might be more efficient to cache these per-thread proxies by keeping a map from the thread ID to a proxy pointer.</span></span> <span data-ttu-id="20e83-115">Эта схема расширяется по мере использования новых потоков в процессе.</span><span class="sxs-lookup"><span data-stu-id="20e83-115">This map expands as new threads are used in the process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20e83-116">См. также</span><span class="sxs-lookup"><span data-stu-id="20e83-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20e83-117">Основные понятия распределителя ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="20e83-117">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



