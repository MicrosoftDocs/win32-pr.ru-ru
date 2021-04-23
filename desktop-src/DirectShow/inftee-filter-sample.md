---
description: Образец фильтра Инфти
ms.assetid: ba401528-9706-41fb-99d1-2bc3ffc05f1a
title: Образец фильтра Инфти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd0fc5a1d550e0327da0d0d3dd47c8847ffafee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673074"
---
# <a name="inftee-filter-sample"></a><span data-ttu-id="7d8f5-103">Образец фильтра Инфти</span><span class="sxs-lookup"><span data-stu-id="7d8f5-103">InfTee Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="7d8f5-104">Описание</span><span class="sxs-lookup"><span data-stu-id="7d8f5-104">Description</span></span>

<span data-ttu-id="7d8f5-105">Фильтр Инфти предоставляет образец реализации фильтра [tee для неограниченного ПИН-кода](infinite-pin-tee-filter.md) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-105">The InfTee filter provides a sample implementation of the DirectShow [Infinite Pin Tee](infinite-pin-tee-filter.md) filter.</span></span> <span data-ttu-id="7d8f5-106">Фильтр имеет один входной ПИН-код и динамическое число закрепления выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-106">The filter has one input pin and a dynamic number of output pins.</span></span> <span data-ttu-id="7d8f5-107">Все примеры носителей, отправляемые в фильтр, доставляются одновременно со всех выходных контактов.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-107">All media samples sent to the filter are delivered simultaneously from all of the output pins.</span></span>

<span data-ttu-id="7d8f5-108">Этот фильтр отображается в Графедит под именем "пример бесконечного ПИН-кода Tee", чтобы отличать его от стандартного бесконечного фильтра tee, предоставляемого в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-108">This filter appears in GraphEdit under the name "Sample Infinite Pin Tee," to distinguish it from the standard Infinite Pin Tee filter that is provided in DirectShow.</span></span>

## <a name="usage"></a><span data-ttu-id="7d8f5-109">Использование</span><span class="sxs-lookup"><span data-stu-id="7d8f5-109">Usage</span></span>

<span data-ttu-id="7d8f5-110">Поскольку этот фильтр не изменяет данные, которые он получает, все ПИН-коды должны быть согласованы с одним и тем же типом носителя.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-110">Because this filter does not change the data that it receives, all pins must agree to the same media type.</span></span> <span data-ttu-id="7d8f5-111">В процессе подключения фильтр может повторно подключить некоторые ПИН-коды, чтобы обеспечить соответствие типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-111">During the connection process, the filter might reconnect some pins in order to make the media types match.</span></span>

<span data-ttu-id="7d8f5-112">Данные, поступающие во входной ПИН-код, не копируются перед их отправкой на выходные контакты.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-112">Data arriving at the input pin is not copied before it is sent to the output pins.</span></span> <span data-ttu-id="7d8f5-113">Фильтр также гарантирует, что данные доставляются в нисходящие фильтры, чтобы оба выхода получали своевременное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-113">The filter also ensures that the data is delivered to the downstream filters, to guarantee that both outputs receive timely service.</span></span> <span data-ttu-id="7d8f5-114">В частности, если один из выходных данных может быть заблокирован в функции-члене [**каутпуткуеуе:: Receive**](coutputqueue-receive.md) , то Tee выводит поток для доставки примера.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-114">In particular, if one of the outputs can block in the [**COutputQueue::Receive**](coutputqueue-receive.md) member function, then the tee spins off a thread to deliver the sample.</span></span> <span data-ttu-id="7d8f5-115">Если для доставки образца нет потоков, то поток, доставляющий пример к входному заteeу, может передать данные в нисходящий фильтр. на этом этапе он может блокироваться, сохраняя данные из другого подчиненного фильтра в течение длительных периодов времени.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-115">If there were no thread to deliver the sample, then the thread that delivers the sample to the tee input pin might pass the data to a downstream filter; at that point, it might block, keeping data from the other downstream filter for long periods of time.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="7d8f5-116">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="7d8f5-116">Downloading the Sample</span></span>

<span data-ttu-id="7d8f5-117">Чтобы скачать примеры пакета SDK для DirectShow, установите последнюю версию [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7d8f5-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="7d8f5-118">Этот пример устанавливается по следующему пути: *\[ \] корневые примеры SDK* \\ \\ мультимедиа \\ DirectShow \\ фильтры \\ инфти.</span><span class="sxs-lookup"><span data-stu-id="7d8f5-118">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\InfTee.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d8f5-119">См. также</span><span class="sxs-lookup"><span data-stu-id="7d8f5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d8f5-120">Примеры DirectShow</span><span class="sxs-lookup"><span data-stu-id="7d8f5-120">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



