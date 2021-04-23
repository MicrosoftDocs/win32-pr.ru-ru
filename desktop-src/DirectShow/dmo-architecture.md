---
description: Архитектура DMO
ms.assetid: f74b2d0f-b40c-4598-97a4-9c1dc71bbb1a
title: Архитектура DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93fcf7f4ef4528cd4d7949d804b149588075d5ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105650416"
---
# <a name="dmo-architecture"></a><span data-ttu-id="36f44-103">Архитектура DMO</span><span class="sxs-lookup"><span data-stu-id="36f44-103">DMO Architecture</span></span>

<span data-ttu-id="36f44-104">В этом разделе описывается общая архитектура DMO.</span><span class="sxs-lookup"><span data-stu-id="36f44-104">This section describes the overall architecture of a DMO.</span></span>

<span data-ttu-id="36f44-105">**Потоки**</span><span class="sxs-lookup"><span data-stu-id="36f44-105">**Streams**</span></span>

<span data-ttu-id="36f44-106">DMO — это объект, принимающий входные данные *m* и создающий *n* выходов.</span><span class="sxs-lookup"><span data-stu-id="36f44-106">A DMO is an object that takes *m* inputs and produces *n* outputs.</span></span> <span data-ttu-id="36f44-107">Входные и выходные данные называются *потоками*.</span><span class="sxs-lookup"><span data-stu-id="36f44-107">The inputs and outputs are called *streams*.</span></span> <span data-ttu-id="36f44-108">Каждый DMO имеет по крайней мере один поток.</span><span class="sxs-lookup"><span data-stu-id="36f44-108">Every DMO has at least one stream.</span></span> <span data-ttu-id="36f44-109">Потоки не являются объектами; они просто ссылаются на DMO по номеру индекса.</span><span class="sxs-lookup"><span data-stu-id="36f44-109">Streams are not objects; they are simply referenced on the DMO by index number.</span></span> <span data-ttu-id="36f44-110">Количество потоков фиксируется во время разработки.</span><span class="sxs-lookup"><span data-stu-id="36f44-110">The number of streams is fixed at design time.</span></span>

<span data-ttu-id="36f44-111">**Типы носителей**</span><span class="sxs-lookup"><span data-stu-id="36f44-111">**Media Types**</span></span>

<span data-ttu-id="36f44-112">Все данные вводятся с помощью *типа мультимедиа*, который определяет способ интерпретации содержимого данных.</span><span class="sxs-lookup"><span data-stu-id="36f44-112">All data is typed using a *media type*, which defines how to interpret the contents of the data.</span></span> <span data-ttu-id="36f44-113">Например, 320 x 240 24-разрядное видео RGB имеет один тип; 44,1-килохертз (кГц) 16-разрядный стереофонический звук PCM является еще одним типом.</span><span class="sxs-lookup"><span data-stu-id="36f44-113">For example, 320 x 240 24-bit RGB video is one type; 44.1-kilohertz (kHz) 16-bit stereo PCM audio is another type.</span></span> <span data-ttu-id="36f44-114">Типы носителей описываются с помощью структуры [**\_ \_ типа мультимедиа DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) .</span><span class="sxs-lookup"><span data-stu-id="36f44-114">Media types are described using the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span> <span data-ttu-id="36f44-115">Прежде чем клиент сможет обработать какие бы то ни было данные, он должен задать тип носителя для каждого потока в DMO.</span><span class="sxs-lookup"><span data-stu-id="36f44-115">Before the client can process any data, it must set the media type for each stream on the DMO.</span></span>

<span data-ttu-id="36f44-116">Как правило, поток может принимать целый ряд типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="36f44-116">Typically, a stream can accept a range of media types.</span></span> <span data-ttu-id="36f44-117">Некоторые дмос поддерживают более широкий диапазон типов, чем другие.</span><span class="sxs-lookup"><span data-stu-id="36f44-117">Some DMOs support a wider range of types than others.</span></span> <span data-ttu-id="36f44-118">Интерфейсы DMO определяют методы клиента для обнаружения поддерживаемых типов.</span><span class="sxs-lookup"><span data-stu-id="36f44-118">The DMO interfaces define methods for the client to discover the supported types.</span></span> <span data-ttu-id="36f44-119">Например, один DMO может поддерживать видео RGB с любой глубиной, а другой может поддерживать только 24-разрядный RGB.</span><span class="sxs-lookup"><span data-stu-id="36f44-119">For example, one DMO might support RGB video at any bit depth, while another might support only 24-bit RGB.</span></span> <span data-ttu-id="36f44-120">Кроме того, DMO может быть ограничен определенным сочетанием входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="36f44-120">Also, a DMO might be limited to certain combinations of inputs and outputs.</span></span> <span data-ttu-id="36f44-121">Например, если тип входных данных — 16-разрядное видео, для потока вывода может потребоваться одна и та же битовая глубина.</span><span class="sxs-lookup"><span data-stu-id="36f44-121">For example, if the input type is 16-bit video, the output stream might require the same bit depth.</span></span> <span data-ttu-id="36f44-122">Клиент может перечислить предпочтительные типы каждого потока и затем проверить определенные сочетания.</span><span class="sxs-lookup"><span data-stu-id="36f44-122">The client can enumerate each stream's preferred types and then test specific combinations.</span></span>

<span data-ttu-id="36f44-123">**Buffers**</span><span class="sxs-lookup"><span data-stu-id="36f44-123">**Buffers**</span></span>

<span data-ttu-id="36f44-124">В модели DMO по умолчанию клиент выделяет отдельные Входные буферы и выходные буферы.</span><span class="sxs-lookup"><span data-stu-id="36f44-124">In the default DMO model, the client allocates separate input buffers and output buffers.</span></span> <span data-ttu-id="36f44-125">Он заполняет Входные буферы данными и доставляет их в DMO, а DMO записывает новые данные в выходные буферы.</span><span class="sxs-lookup"><span data-stu-id="36f44-125">It fills the input buffers with data and delivers them to the DMO, and the DMO writes new data into the output buffers.</span></span>

<span data-ttu-id="36f44-126">При необходимости DMO может поддерживать «на месте» обработку.</span><span class="sxs-lookup"><span data-stu-id="36f44-126">Optionally, a DMO can support "in-place" processing.</span></span> <span data-ttu-id="36f44-127">При использовании обработки на месте объекты DMO записывают выходные данные непосредственно во входной буфер для исходных данных.</span><span class="sxs-lookup"><span data-stu-id="36f44-127">With in-place processing, the DMO writes the output directly into the input buffer, over the original data.</span></span> <span data-ttu-id="36f44-128">Обработка на месте устраняет необходимость в отдельных буферах.</span><span class="sxs-lookup"><span data-stu-id="36f44-128">In-place processing eliminates the need for separate buffers.</span></span> <span data-ttu-id="36f44-129">С другой стороны, она изменяет исходные данные, которые могут быть неприемлемыми для некоторых приложений.</span><span class="sxs-lookup"><span data-stu-id="36f44-129">On the other hand, it alters the original data, which may not be acceptable for some applications.</span></span>

<span data-ttu-id="36f44-130">Модель буферизации по умолчанию (не на месте) поддерживается через интерфейс [**имедиаобжект**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .</span><span class="sxs-lookup"><span data-stu-id="36f44-130">The default (non-in-place) buffering model is supported through the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span> <span data-ttu-id="36f44-131">Все дмос должны реализовывать этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="36f44-131">All DMOs must implement this interface.</span></span> <span data-ttu-id="36f44-132">Если объект DMO поддерживает обработку на месте, он также предоставляет интерфейс [**имедиаобжектинплаце**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) .</span><span class="sxs-lookup"><span data-stu-id="36f44-132">If a DMO supports in-place processing, it also exposes the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) interface.</span></span> <span data-ttu-id="36f44-133">Клиент несет ответственность за выделение всех буферов, входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="36f44-133">The client is responsible for allocating all buffers, both input and output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36f44-134">См. также</span><span class="sxs-lookup"><span data-stu-id="36f44-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36f44-135">О дмос</span><span class="sxs-lookup"><span data-stu-id="36f44-135">About DMOs</span></span>](about-dmos.md)
</dt> </dl>

 

 



