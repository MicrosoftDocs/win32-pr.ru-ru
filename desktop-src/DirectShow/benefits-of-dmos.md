---
description: Преимущества дмос
ms.assetid: 7ff3fd9c-9423-4915-8ce2-22783ed455fb
title: Преимущества дмос
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972b4f49ee19b271cbee970401933b6c7d6bd3ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262443"
---
# <a name="benefits-of-dmos"></a><span data-ttu-id="b56ef-103">Преимущества дмос</span><span class="sxs-lookup"><span data-stu-id="b56ef-103">Benefits of DMOs</span></span>

<span data-ttu-id="b56ef-104">Дмос предлагают следующие преимущества:</span><span class="sxs-lookup"><span data-stu-id="b56ef-104">DMOs offer the following advantages:</span></span>

-   <span data-ttu-id="b56ef-105">Они обычно меньше и проще, чем фильтры DirectShow, так как они поддерживают меньше функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="b56ef-105">They are generally smaller and simpler than DirectShow filters, because they support less functionality.</span></span>
-   <span data-ttu-id="b56ef-106">Они являются более гибкими, чем фильтры DirectShow, так как они не нуждаются в графе фильтра.</span><span class="sxs-lookup"><span data-stu-id="b56ef-106">They are more flexible than DirectShow filters because they do not require a filter graph.</span></span> <span data-ttu-id="b56ef-107">Их можно использовать с DirectShow, если вам нужны службы, предоставляемые DirectShow, такие как синхронизация, интеллектуальное подключение, автоматическая обработка потока данных и управление потоками.</span><span class="sxs-lookup"><span data-stu-id="b56ef-107">You can use them with DirectShow when you need the services that DirectShow provides, such as synchronization, intelligent connection, automatic handling of data flow, and thread management.</span></span> <span data-ttu-id="b56ef-108">Клиенты, которым не требуются эти службы, могут напрямую обращаться к дмос.</span><span class="sxs-lookup"><span data-stu-id="b56ef-108">Clients that do not need these services can access DMOs directly.</span></span>
-   <span data-ttu-id="b56ef-109">Дмос всегда выполняет синхронную обработку данных, что устраняет многие проблемы с потоками, которые необходимо учитывать при написании фильтра.</span><span class="sxs-lookup"><span data-stu-id="b56ef-109">DMOs always perform synchronous data processing, which eliminates many of the threading issues that you must consider if you write a filter.</span></span>
-   <span data-ttu-id="b56ef-110">В отличие от традиционных кодеков ACM и ВКМ, дмос основаны на модели COM, поэтому их можно расширить с помощью **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="b56ef-110">Unlike traditional ACM and VCM codecs, DMOs are based on the Component Object Model (COM), so they can be extended through **QueryInterface**.</span></span>
-   <span data-ttu-id="b56ef-111">Дмос поддерживает более обобщенную потоковую модель, чем кодеки ACM или ВКМ.</span><span class="sxs-lookup"><span data-stu-id="b56ef-111">DMOs support a more generalized streaming model than ACM or VCM codecs.</span></span> <span data-ttu-id="b56ef-112">Как и фильтры DirectShow, дмос может поддерживать несколько входов и несколько выходов.</span><span class="sxs-lookup"><span data-stu-id="b56ef-112">Like DirectShow filters, DMOs can support multiple inputs and multiple outputs.</span></span>

<span data-ttu-id="b56ef-113">По этим причинам в качестве решения для написания кодировщиков, декодеров и звуковых эффектов рекомендуется использовать дмос.</span><span class="sxs-lookup"><span data-stu-id="b56ef-113">For these reasons, DMOs are now recommended as the solution for writing encoders, decoders, and audio effects.</span></span> <span data-ttu-id="b56ef-114">Также возможны и другие сценарии, в зависимости от потребностей приложения.</span><span class="sxs-lookup"><span data-stu-id="b56ef-114">Many other scenarios are possible as well, depending on the needs of the application.</span></span>

<span data-ttu-id="b56ef-115">Отличие дмос от фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="b56ef-115">How DMOs Differ from DirectShow Filters</span></span>

<span data-ttu-id="b56ef-116">Фильтры DirectShow не могут работать за пределами графа фильтра DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b56ef-116">DirectShow filters cannot function outside of a DirectShow filter graph.</span></span> <span data-ttu-id="b56ef-117">В DirectShow диспетчер графов фильтров подбирает между приложением и фильтрами.</span><span class="sxs-lookup"><span data-stu-id="b56ef-117">In DirectShow, the Filter Graph Manager mediates between the application and the filters.</span></span> <span data-ttu-id="b56ef-118">Фильтры DirectShow выполняют большую часть работы, необходимой для потоковой передачи данных, в том числе:</span><span class="sxs-lookup"><span data-stu-id="b56ef-118">DirectShow filters do most of the work required to stream data, including:</span></span>

-   <span data-ttu-id="b56ef-119">Выделение буферов.</span><span class="sxs-lookup"><span data-stu-id="b56ef-119">Allocating buffers.</span></span>
-   <span data-ttu-id="b56ef-120">Согласование типов мультимедиа и подключений к другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="b56ef-120">Negotiating media types and connections to other filters.</span></span>
-   <span data-ttu-id="b56ef-121">Отправка данных через граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="b56ef-121">Pushing data through the filter graph.</span></span>
-   <span data-ttu-id="b56ef-122">Отправка событий в Диспетчер графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="b56ef-122">Sending events to the Filter Graph Manager.</span></span>
-   <span data-ttu-id="b56ef-123">Синхронизация нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="b56ef-123">Synchronizing multiple threads.</span></span>

<span data-ttu-id="b56ef-124">Напротив, DMO не выполняет ни одно из этих действий.</span><span class="sxs-lookup"><span data-stu-id="b56ef-124">In contrast, a DMO does none of these things.</span></span> <span data-ttu-id="b56ef-125">Вместо этого ответственность за выполнение этих задач несет клиент, использующий DMO.</span><span class="sxs-lookup"><span data-stu-id="b56ef-125">Instead, these kinds of tasks are the responsibility of the client using the DMO.</span></span> <span data-ttu-id="b56ef-126">Клиент выделяет буферы, заполняет их данными и доставляет их в DMO.</span><span class="sxs-lookup"><span data-stu-id="b56ef-126">The client allocates buffers, fills them with data, and delivers them to the DMO.</span></span> <span data-ttu-id="b56ef-127">DMO обрабатывает данные, и клиент получает результирующие буферы вывода.</span><span class="sxs-lookup"><span data-stu-id="b56ef-127">The DMO processes the data, and the client retrieves the resulting output buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b56ef-128">См. также</span><span class="sxs-lookup"><span data-stu-id="b56ef-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b56ef-129">О дмос</span><span class="sxs-lookup"><span data-stu-id="b56ef-129">About DMOs</span></span>](about-dmos.md)
</dt> </dl>

 

 



