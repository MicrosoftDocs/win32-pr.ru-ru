---
description: Сводка по потокам фильтров
ms.assetid: b7e42101-75c9-428d-9dc7-e625242dbc1e
title: Сводка по потокам фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa0a7c4ce19c46a0f7b05db3cb4d82e8f2aa0beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674338"
---
# <a name="summary-of-filter-threading"></a><span data-ttu-id="2aaff-103">Сводка по потокам фильтров</span><span class="sxs-lookup"><span data-stu-id="2aaff-103">Summary of Filter Threading</span></span>

<span data-ttu-id="2aaff-104">В потоке потоковой передачи вызываются следующие методы:</span><span class="sxs-lookup"><span data-stu-id="2aaff-104">The following methods are called on the streaming thread:</span></span>

-   [<span data-ttu-id="2aaff-105">**Имеминпутпин:: Receive**</span><span class="sxs-lookup"><span data-stu-id="2aaff-105">**IMemInputPin::Receive**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [<span data-ttu-id="2aaff-106">**Имеминпутпин:: Рецеивемултипле**</span><span class="sxs-lookup"><span data-stu-id="2aaff-106">**IMemInputPin::ReceiveMultiple**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [<span data-ttu-id="2aaff-107">**Ипин:: EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="2aaff-107">**IPin::EndOfStream**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [<span data-ttu-id="2aaff-108">**Ипин:: Невсегмент**</span><span class="sxs-lookup"><span data-stu-id="2aaff-108">**IPin::NewSegment**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)
-   [<span data-ttu-id="2aaff-109">**Имемаллокатор:: buffer**</span><span class="sxs-lookup"><span data-stu-id="2aaff-109">**IMemAllocator::GetBuffer**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)

<span data-ttu-id="2aaff-110">В потоке приложения вызываются следующие методы:</span><span class="sxs-lookup"><span data-stu-id="2aaff-110">The following methods are called on the application thread:</span></span>

-   <span data-ttu-id="2aaff-111">Изменения состояния: [**ибасефилтер:: жоинфилтерграф**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph), [**имедиафилтер::P Аусе**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**имедиафилтер:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**имедиафилтер:: останавливаться**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop), [**икуалитиконтрол:: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink).</span><span class="sxs-lookup"><span data-stu-id="2aaff-111">State changes: [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph), [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop), [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink).</span></span>
-   <span data-ttu-id="2aaff-112">Ссылочное время: [**имедиафилтер:: жетсинксаурце**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource), [**Имедиафилтер:: сетсинксаурце**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource).</span><span class="sxs-lookup"><span data-stu-id="2aaff-112">Reference clock: [**IMediaFilter::GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource), [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource).</span></span>
-   <span data-ttu-id="2aaff-113">Операции закрепления: [**ибасефилтер:: финдпин**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin), [**Ипин:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect), [**Ипин:: Коннектедто**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto), [**ипин:: коннектионмедиатипе**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype), [**Ипин::D соединения**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect), [**Ипин:: рецеивеконнектион**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection).</span><span class="sxs-lookup"><span data-stu-id="2aaff-113">Pin operations: [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin), [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect), [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto), [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype), [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect), [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection).</span></span>
-   <span data-ttu-id="2aaff-114">Функции распределителя: [**имеминпутпин:: распределителе**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator), [**Имеминпутпин:: нотифяллокатор**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator).</span><span class="sxs-lookup"><span data-stu-id="2aaff-114">Allocator functions: [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator), [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator).</span></span>
-   <span data-ttu-id="2aaff-115">Идет сброс: [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span><span class="sxs-lookup"><span data-stu-id="2aaff-115">Flushing: [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span></span>

<span data-ttu-id="2aaff-116">Этот список не является исчерпывающим.</span><span class="sxs-lookup"><span data-stu-id="2aaff-116">This list is not exhaustive.</span></span> <span data-ttu-id="2aaff-117">При реализации фильтра необходимо определить, какие методы изменяют состояние фильтра, и какие методы выполняют потоковые операции.</span><span class="sxs-lookup"><span data-stu-id="2aaff-117">When you implement a filter, you must consider which methods change the filter state, and which methods perform streaming operations.</span></span>

 

 



