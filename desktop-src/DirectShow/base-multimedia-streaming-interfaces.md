---
description: Базовые интерфейсы потоковой передачи мультимедиа
ms.assetid: a94dbb64-dfca-4c24-8c11-761835faf8a8
title: Базовые интерфейсы потоковой передачи мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b715a68bd65a2fa3a3923edf10f0e2d1f6c22edb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999982"
---
# <a name="base-multimedia-streaming-interfaces"></a><span data-ttu-id="dea99-103">Базовые интерфейсы потоковой передачи мультимедиа</span><span class="sxs-lookup"><span data-stu-id="dea99-103">Base Multimedia Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="dea99-104">Эти API-интерфейсы являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="dea99-104">These APIs are deprecated.</span></span> <span data-ttu-id="dea99-105">Приложения должны использовать [**образец фильтра захвата**](sample-grabber-filter.md) или реализовать настраиваемый фильтр для получения данных из графа фильтра DirectShow.</span><span class="sxs-lookup"><span data-stu-id="dea99-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="dea99-106">Базовые интерфейсы потоковой передачи мультимедиа предоставляют программный способ доступа к потокам мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="dea99-106">The base multimedia streaming interfaces provide a programmatic way to access multimedia streams.</span></span> <span data-ttu-id="dea99-107">Однако использование базового интерфейса для доступа к данным определенного типа может ограничить объем контроля над данными, поэтому разработчики мультимедиа должны создавать производные версии этих интерфейсов, обеспечивающие более эффективный контроль над уникальными возможностями типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="dea99-107">However, using a base interface to access a specific type of data can limit the amount of control you have over the data, so media developers should create derived versions of these interfaces that provide more powerful control over the unique capabilities of their media type.</span></span>



| <span data-ttu-id="dea99-108">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="dea99-108">Interface</span></span>                                      | <span data-ttu-id="dea99-109">Описание</span><span class="sxs-lookup"><span data-stu-id="dea99-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dea99-110">**имултимедиастреам**</span><span class="sxs-lookup"><span data-stu-id="dea99-110">**IMultiMediaStream**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) | <span data-ttu-id="dea99-111">Определяет способ доступа к объекту мультимедийного потока самого высокого уровня. Этот объект содержит и предоставляет доступ к другим объектам потока.</span><span class="sxs-lookup"><span data-stu-id="dea99-111">Defines how to access the highest-level multimedia stream object; this object contains and provides access to other stream objects.</span></span> <span data-ttu-id="dea99-112">[**Имултимедиастреам**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) содержит методы, которые перечисляют или извлекают определенные потоки, а также проверяют общую длительность времени потока и ищут их в потоке.</span><span class="sxs-lookup"><span data-stu-id="dea99-112">[**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) has methods that enumerate or retrieve specific streams, as well as checking the stream's total time duration and seeking within the stream.</span></span>                                                                                                       |
| [<span data-ttu-id="dea99-113">**имедиастреам**</span><span class="sxs-lookup"><span data-stu-id="dea99-113">**IMediaStream**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)           | <span data-ttu-id="dea99-114">Определяет универсальный объект потока.</span><span class="sxs-lookup"><span data-stu-id="dea99-114">Defines a generic stream object.</span></span> <span data-ttu-id="dea99-115">Используйте его методы для получения указателя на поток, получения сведений о потоке и создания примеров из потоковых данных.</span><span class="sxs-lookup"><span data-stu-id="dea99-115">Use its methods to retrieve a pointer to the stream, get information about the stream, and create samples from the stream data.</span></span> <span data-ttu-id="dea99-116">Можно также создавать образцы общего потока, к которым можно получить доступ из нескольких потоков без дублирования данных выборки.</span><span class="sxs-lookup"><span data-stu-id="dea99-116">You can also create shared stream samples, which multiple streams can access without duplicating the sample's data.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="dea99-117">**истреамсампле**</span><span class="sxs-lookup"><span data-stu-id="dea99-117">**IStreamSample**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)         | <span data-ttu-id="dea99-118">Управляет поведением конкретного примера потока.</span><span class="sxs-lookup"><span data-stu-id="dea99-118">Controls the behavior of a specific stream sample.</span></span> <span data-ttu-id="dea99-119">Вы можете получить поток, который создал образец, проверить время начала и окончания выборки и состояние завершения, а также выполнить определяемую пользователем функцию в образце (с помощью метода [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) ).</span><span class="sxs-lookup"><span data-stu-id="dea99-119">You can retrieve the stream that created the sample, check the sample's start and end times and completion status, and perform a user-defined function on the sample itself (through the [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) method).</span></span> <span data-ttu-id="dea99-120">Как правило, метод Update обрабатывает демонстрационные данные соответствующим образом, например отрисовку видеоданных или воспроизведение звуковых данных.</span><span class="sxs-lookup"><span data-stu-id="dea99-120">Typically, the Update method processes the sample data in an appropriate manner, such as rendering video data or playing back audio data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="dea99-121">См. также</span><span class="sxs-lookup"><span data-stu-id="dea99-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dea99-122">Список интерфейсов потоковой передачи мультимедиа</span><span class="sxs-lookup"><span data-stu-id="dea99-122">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



