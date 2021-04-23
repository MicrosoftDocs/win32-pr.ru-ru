---
description: Media Foundation API платформы
ms.assetid: 1eb20c44-58cb-4e34-a108-1b3c27d54ff1
title: Media Foundation API платформы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed1e8d8aa0dcd5d7b1184a406e09910a98892f4f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105720021"
---
# <a name="media-foundation-platform-apis"></a><span data-ttu-id="e2374-103">Media Foundation API платформы</span><span class="sxs-lookup"><span data-stu-id="e2374-103">Media Foundation Platform APIs</span></span>

<span data-ttu-id="e2374-104">Уровень платформы Media Foundation содержит примитивы и вспомогательные объекты, используемые другими слоями.</span><span class="sxs-lookup"><span data-stu-id="e2374-104">The platform layer of Media Foundation contains primitives and helper objects used by the other layers.</span></span>

<span data-ttu-id="e2374-105">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="e2374-105">This section contains the following topics:</span></span>



| <span data-ttu-id="e2374-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="e2374-106">Topic</span></span>                                                                           | <span data-ttu-id="e2374-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e2374-107">Description</span></span>                                                                                                                                                       |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2374-108">Инициализация платформы Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2374-108">Initializing the Media Foundation Platform</span></span>](initializing-media-foundation.md) | <span data-ttu-id="e2374-109">Инициализация платформы Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e2374-109">How to initialize the Media Foundation platform.</span></span>                                                                                                                  |
| [<span data-ttu-id="e2374-110">Media Foundation и COM</span><span class="sxs-lookup"><span data-stu-id="e2374-110">Media Foundation and COM</span></span>](media-foundation-and-com.md)                        | <span data-ttu-id="e2374-111">Описывает взаимодействие между COM и Microsoft Media Foundation и определяет некоторые рекомендации для использования при разработке компонентов подключаемых модулей Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e2374-111">Describes the interaction between COM and Microsoft Media Foundation, and defines some best practices to use when developing Media Foundation plug-in components.</span></span> |
| [<span data-ttu-id="e2374-112">Асинхронные методы обратного вызова</span><span class="sxs-lookup"><span data-stu-id="e2374-112">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)              | <span data-ttu-id="e2374-113">Как вызывать асинхронные методы и реализовывать асинхронные операции в Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e2374-113">How to call asynchronous methods and how to implement asynchronous operations in Media Foundation.</span></span>                                                                |
| [<span data-ttu-id="e2374-114">Рабочие очереди</span><span class="sxs-lookup"><span data-stu-id="e2374-114">Work Queues</span></span>](work-queues.md)                                                  | <span data-ttu-id="e2374-115">Рабочая очередь — это эффективный способ выполнения асинхронных операций в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="e2374-115">A work queue is an efficient way to perform asynchronous operations on another thread.</span></span>                                                                            |
| [<span data-ttu-id="e2374-116">Генераторы событий мультимедиа</span><span class="sxs-lookup"><span data-stu-id="e2374-116">Media Event Generators</span></span>](media-event-generators.md)                            | <span data-ttu-id="e2374-117">Как получить асинхронные события и как вызывать события в Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e2374-117">How to receive asynchronous events and how to raise events in Media Foundation.</span></span>                                                                                   |
| [<span data-ttu-id="e2374-118">Интерфейсы службы</span><span class="sxs-lookup"><span data-stu-id="e2374-118">Service Interfaces</span></span>](service-interfaces.md)                                    | <span data-ttu-id="e2374-119">Интерфейс службы — это COM-интерфейс, предоставляемый одним объектом, но предоставляемый приложению через другой объект.</span><span class="sxs-lookup"><span data-stu-id="e2374-119">A service interface is a COM interface provided by one object, but exposed to the application through another object.</span></span>                                             |
| [<span data-ttu-id="e2374-120">Объекты активации</span><span class="sxs-lookup"><span data-stu-id="e2374-120">Activation Objects</span></span>](activation-objects.md)                                    | <span data-ttu-id="e2374-121">Объект активации — это объект, который создает другой объект.</span><span class="sxs-lookup"><span data-stu-id="e2374-121">An activation object is an object that creates another object.</span></span>                                                                                                    |
| [<span data-ttu-id="e2374-122">Часы представления</span><span class="sxs-lookup"><span data-stu-id="e2374-122">Presentation Clock</span></span>](presentation-clock.md)                                    | <span data-ttu-id="e2374-123">Часы презентации формируют время, которое используется для управления воспроизведением, а также синхронными потоками аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="e2374-123">The presentation clock generates the clock time that is used to control playback, and also to synchronous audio and video streams.</span></span>                                |



 

## <a name="related-topics"></a><span data-ttu-id="e2374-124">См. также</span><span class="sxs-lookup"><span data-stu-id="e2374-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2374-125">Архитектура Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2374-125">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="e2374-126">Media Foundationое программное руководством</span><span class="sxs-lookup"><span data-stu-id="e2374-126">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 



