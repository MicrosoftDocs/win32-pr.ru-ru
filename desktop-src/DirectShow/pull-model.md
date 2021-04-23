---
description: Модель извлечения
ms.assetid: b5246dfe-e6ee-4b91-bfe3-2ec8b8723938
title: Модель извлечения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd4becd54bffb39acf30b6d29fca45e6a117989
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537160"
---
# <a name="pull-model"></a><span data-ttu-id="3324a-103">Модель извлечения</span><span class="sxs-lookup"><span data-stu-id="3324a-103">Pull Model</span></span>

<span data-ttu-id="3324a-104">В интерфейсе [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) вышестоящий фильтр определяет, какие данные следует отправить, и передает их в нисходящий фильтр.</span><span class="sxs-lookup"><span data-stu-id="3324a-104">In the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, the upstream filter determines what data to send, and it pushes the data to the downstream filter.</span></span> <span data-ttu-id="3324a-105">Для некоторых фильтров лучше подходит модель *извлечения* .</span><span class="sxs-lookup"><span data-stu-id="3324a-105">For some filters, a *pull* model is more appropriate.</span></span> <span data-ttu-id="3324a-106">В этом случае нисходящий фильтр запрашивает данные из вышестоящего фильтра.</span><span class="sxs-lookup"><span data-stu-id="3324a-106">Here, the downstream filter requests data from the upstream filter.</span></span> <span data-ttu-id="3324a-107">Примеры по-прежнему перемещаются дальше, от выходного закрепления до входного ПИН-кода, но нисходящий фильтр инициирует поток данных.</span><span class="sxs-lookup"><span data-stu-id="3324a-107">Samples still travel downstream, from output pin to input pin, but the downstream filter initiates the data flow.</span></span> <span data-ttu-id="3324a-108">Этот тип соединения использует интерфейс [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="3324a-108">This type of connection uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

<span data-ttu-id="3324a-109">Обычно для модели извлечения используется воспроизведение файла.</span><span class="sxs-lookup"><span data-stu-id="3324a-109">The typical use for the pull model is in file playback.</span></span> <span data-ttu-id="3324a-110">Например, в графе воспроизведения AVI фильтр [источника Async File](file-source--async--filter.md) выполняет общие операции чтения файлов и доставляет данные в виде байтового потока без сведений о форматировании.</span><span class="sxs-lookup"><span data-stu-id="3324a-110">For example, in an AVI playback graph, the [Async File Source](file-source--async--filter.md) filter performs generic file reading operations and delivers the data as a byte stream, with no format information.</span></span> <span data-ttu-id="3324a-111">Фильтр [разделителя AVI](avi-splitter-filter.md) СЧИТЫВАЕТ заголовки AVI и анализирует поток в видеороликах и образцах аудио.</span><span class="sxs-lookup"><span data-stu-id="3324a-111">The [AVI Splitter](avi-splitter-filter.md) filter reads the AVI headers and parses the stream into video and audio samples.</span></span> <span data-ttu-id="3324a-112">Разделитель AVI позволяет определить, какие данные требуются лучше фильтра «асинхронный файл», и, следовательно, использовать **иасинкреадер** вместо **имеминпутпин**.</span><span class="sxs-lookup"><span data-stu-id="3324a-112">The AVI Splitter can determine what data it needs better than the Async File Source filter, and therefore it uses **IAsyncReader** instead of **IMemInputPin**.</span></span>

<span data-ttu-id="3324a-113">Для запроса данных из выходного контакта входной ПИН-код вызывает один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="3324a-113">To request data from the output pin, the input pin calls one of the following methods:</span></span>

-   [<span data-ttu-id="3324a-114">**Иасинкреадер:: Request**</span><span class="sxs-lookup"><span data-stu-id="3324a-114">**IAsyncReader::Request**</span></span>](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [<span data-ttu-id="3324a-115">**Иасинкреадер:: Синкреад**</span><span class="sxs-lookup"><span data-stu-id="3324a-115">**IAsyncReader::SyncRead**</span></span>](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   <span data-ttu-id="3324a-116">[**Иасинкреадер:: синкреадалигнед**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span><span class="sxs-lookup"><span data-stu-id="3324a-116">[**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span></span>

<span data-ttu-id="3324a-117">Первый метод является асинхронным и поддерживает множественные операции чтения с перекрытием.</span><span class="sxs-lookup"><span data-stu-id="3324a-117">The first method is asynchronous, to support multiple overlapped reads.</span></span> <span data-ttu-id="3324a-118">Остальные являются синхронными.</span><span class="sxs-lookup"><span data-stu-id="3324a-118">The others are synchronous.</span></span>

<span data-ttu-id="3324a-119">Теоретически любой фильтр может поддерживать **иасинкреадер**, но на практике он предназначен для фильтров источников, подключающихся к фильтрам синтаксического анализатора.</span><span class="sxs-lookup"><span data-stu-id="3324a-119">In theory, any filter can support **IAsyncReader**, but in practice it is designed for source filters that connect to parser filters.</span></span> <span data-ttu-id="3324a-120">Средство синтаксического анализа работает во многом подобно фильтру источника в модели push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3324a-120">The parser acts very much like a source filter in the push model.</span></span> <span data-ttu-id="3324a-121">При приостановке он создает поток потоковой передачи, который извлекает данные из подключения **иасинкреадер** и отправляет его дальше.</span><span class="sxs-lookup"><span data-stu-id="3324a-121">When it pauses, it creates a streaming thread that pulls data from the **IAsyncReader** connection and pushes it downstream.</span></span> <span data-ttu-id="3324a-122">В закреплениях выходных данных используется **имеминпутпин**, а в остальной части графа используется стандартная модель push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3324a-122">The output pins use **IMemInputPin**, and the rest of the graph uses the standard push model.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3324a-123">См. также</span><span class="sxs-lookup"><span data-stu-id="3324a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3324a-124">Поток данных в графе фильтра</span><span class="sxs-lookup"><span data-stu-id="3324a-124">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



