---
description: Транспорты
ms.assetid: 63c5ff5b-293d-4a80-92e8-3ece41321095
title: Транспорты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3d87ffacc871fc45ef1e8e645849afc956fb1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683632"
---
# <a name="transports"></a><span data-ttu-id="13cf0-103">Транспорты</span><span class="sxs-lookup"><span data-stu-id="13cf0-103">Transports</span></span>

<span data-ttu-id="13cf0-104">Для перемещения данных мультимедиа с помощью графа фильтра фильтр DirectShow должен поддерживать один из нескольких возможных протоколов.</span><span class="sxs-lookup"><span data-stu-id="13cf0-104">In order to move media data through the filter graph, a DirectShow filter must support one of several possible protocols.</span></span> <span data-ttu-id="13cf0-105">Эти протоколы называются транспортами.</span><span class="sxs-lookup"><span data-stu-id="13cf0-105">These protocols are called transports.</span></span> <span data-ttu-id="13cf0-106">При подключении двух фильтров они должны поддерживать один и тот же транспорт. в противном случае они не могут обмениваться данными мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="13cf0-106">When two filters connect, they must support the same transport; otherwise they cannot exchange media data.</span></span> <span data-ttu-id="13cf0-107">Как правило, для транспорта требуется, чтобы один из ПИН-кодов поддерживал определенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="13cf0-107">Typically, a transport requires that one of the pins support a particular interface.</span></span> <span data-ttu-id="13cf0-108">При подключении фильтров один закрепление запрашивает другой для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="13cf0-108">When the filters connect, one pin queries the other for the interface.</span></span>

<span data-ttu-id="13cf0-109">Большинство фильтров DirectShow хранят данные мультимедиа в основной памяти и доставляют их другим фильтрам по ПИН-соединениям.</span><span class="sxs-lookup"><span data-stu-id="13cf0-109">Most DirectShow filters hold media data in main memory, and deliver it to other filters across pin connections.</span></span> <span data-ttu-id="13cf0-110">Этот тип транспорта называется транспортом локальной памяти.</span><span class="sxs-lookup"><span data-stu-id="13cf0-110">This type of transport is called local memory transport.</span></span> <span data-ttu-id="13cf0-111">Хотя транспорт локальной памяти является наиболее распространенным транспортом в DirectShow, не все фильтры используют его.</span><span class="sxs-lookup"><span data-stu-id="13cf0-111">Although local memory transport is the most common transport in DirectShow, not all filters use it.</span></span> <span data-ttu-id="13cf0-112">Например, некоторые фильтры отправляют данные мультимедиа по пути оборудования и используют ПИН-коды только для предоставления управляющих данных.</span><span class="sxs-lookup"><span data-stu-id="13cf0-112">For example, some filters send media data along a hardware path, and use pins only to deliver control information.</span></span> <span data-ttu-id="13cf0-113">Например, см. интерфейс [**иоверлай**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) .</span><span class="sxs-lookup"><span data-stu-id="13cf0-113">For example, see the [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) interface.</span></span>

<span data-ttu-id="13cf0-114">DirectShow определяет два механизма транспорта локальной памяти, модель push-уведомлений и модель извлечения.</span><span class="sxs-lookup"><span data-stu-id="13cf0-114">DirectShow defines two mechanisms for local memory transport, the push model and the pull model.</span></span> <span data-ttu-id="13cf0-115">В модели отправки фильтр источника создает данные и доставляет их следующему фильтру.</span><span class="sxs-lookup"><span data-stu-id="13cf0-115">In the push model, a source filter generates data and delivers it to the next filter downstream.</span></span> <span data-ttu-id="13cf0-116">Этот фильтр успешно получает данные, обрабатывает их и отправляет дальше по нисходящей.</span><span class="sxs-lookup"><span data-stu-id="13cf0-116">That filter passively receives the data, processes it, and sends it further downstream.</span></span> <span data-ttu-id="13cf0-117">В модели извлечения фильтр источника подключен к фильтру анализатора.</span><span class="sxs-lookup"><span data-stu-id="13cf0-117">In the pull model, the source filter is connected to a parser filter.</span></span> <span data-ttu-id="13cf0-118">Фильтр средства синтаксического анализа запрашивает данные из фильтра источника.</span><span class="sxs-lookup"><span data-stu-id="13cf0-118">The parser filter requests data from the source filter.</span></span> <span data-ttu-id="13cf0-119">Фильтр источника отвечает на запросы, предоставляя данные.</span><span class="sxs-lookup"><span data-stu-id="13cf0-119">The source filter responds to the requests by delivering data.</span></span> <span data-ttu-id="13cf0-120">В модели push-уведомлений используется интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , а в модели извлечения используется интерфейс [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="13cf0-120">The push model uses the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, and the pull model uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

<span data-ttu-id="13cf0-121">Модель push-уведомлений чаще всего используется по сравнению с моделью извлечения.</span><span class="sxs-lookup"><span data-stu-id="13cf0-121">The push model is more common than the pull model.</span></span> <span data-ttu-id="13cf0-122">Поэтому в следующих статьях предполагается модель push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="13cf0-122">Therefore, the articles that follow assume a push model.</span></span> <span data-ttu-id="13cf0-123">Последняя статья в этом разделе « [модель извлечения](pull-model.md)» описывает, как интерфейс **Иасинкреадер** отличается от **имеминпутпин**.</span><span class="sxs-lookup"><span data-stu-id="13cf0-123">The last article in this section, [Pull Model](pull-model.md), describes how the **IAsyncReader** interface differs from **IMemInputPin**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13cf0-124">См. также</span><span class="sxs-lookup"><span data-stu-id="13cf0-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13cf0-125">Поток данных в графе фильтра</span><span class="sxs-lookup"><span data-stu-id="13cf0-125">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



