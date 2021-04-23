---
description: Образец фильтра дампа
ms.assetid: 2ce52e6c-a02f-4737-822a-87b2cf2d933d
title: Образец фильтра дампа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd64d1f16b0b504743890543b617a24df6bbaab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537964"
---
# <a name="dump-filter-sample"></a><span data-ttu-id="b01d5-103">Образец фильтра дампа</span><span class="sxs-lookup"><span data-stu-id="b01d5-103">Dump Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="b01d5-104">Описание</span><span class="sxs-lookup"><span data-stu-id="b01d5-104">Description</span></span>

<span data-ttu-id="b01d5-105">Фильтр дампа — это фильтр модуля подготовки отчетов, который записывает полученные примеры мультимедиа в текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="b01d5-105">The Dump Filter is a renderer filter that writes the media samples it receives to a text file.</span></span>

<span data-ttu-id="b01d5-106">В этом примере показано, как использовать базовый класс фильтра [**кбасефилтер**](cbasefilter.md) и отображаемый класс входных ПИН-кодов [**крендерединпутпин**](crenderedinputpin.md).</span><span class="sxs-lookup"><span data-stu-id="b01d5-106">This sample illustrates how to use the base filter class [**CBaseFilter**](cbasefilter.md) and the rendered input pin class [**CRenderedInputPin**](crenderedinputpin.md).</span></span> <span data-ttu-id="b01d5-107">В нем также показано, как реализовать интерфейс [**ифилесинкфилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) .</span><span class="sxs-lookup"><span data-stu-id="b01d5-107">It also demonstrates how to implement the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface.</span></span> <span data-ttu-id="b01d5-108">Фильтр дампа имеет один входной ПИН-код, который записывает каждый пример, который он получает непосредственно в файл.</span><span class="sxs-lookup"><span data-stu-id="b01d5-108">The Dump filter has a single input pin, which writes every sample that it receives directly to a file.</span></span>

## <a name="usage"></a><span data-ttu-id="b01d5-109">Использование</span><span class="sxs-lookup"><span data-stu-id="b01d5-109">Usage</span></span>

<span data-ttu-id="b01d5-110">Этот фильтр является полезным средством отладки.</span><span class="sxs-lookup"><span data-stu-id="b01d5-110">This filter is a useful debugging tool.</span></span> <span data-ttu-id="b01d5-111">Например, можно проверить, поразрядить результаты фильтра преобразования.</span><span class="sxs-lookup"><span data-stu-id="b01d5-111">For example, you can verify, bit by bit, the results of a transform filter.</span></span> <span data-ttu-id="b01d5-112">Граф можно построить вручную с помощью Графедит и подключить фильтр дампа к выходным данным фильтра преобразования или любого другого выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="b01d5-112">You can build a graph manually by using GraphEdit, and connect the Dump filter to the output of a transform filter or any other output pin.</span></span> <span data-ttu-id="b01d5-113">Можно также подключить фильтр tee и разместить фильтр дампа в одной части фильтра tee, а типичные выходные данные — в другом, чтобы отслеживать результаты в сценарии в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="b01d5-113">You can also connect a tee filter and put the Dump filter on one leg of the tee filter and the typical output on another leg to monitor the results in a real-time scenario.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="b01d5-114">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="b01d5-114">Downloading the Sample</span></span>

<span data-ttu-id="b01d5-115">Чтобы скачать примеры пакета SDK для DirectShow, установите последнюю версию [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b01d5-115">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="b01d5-116">Этот пример устанавливается по следующему пути: *\[ \] корневой пример пакета SDK* \\ \\ файлы \\ \\ дампа фильтров мультимедиа DirectShow \\ .</span><span class="sxs-lookup"><span data-stu-id="b01d5-116">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Dump.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b01d5-117">См. также</span><span class="sxs-lookup"><span data-stu-id="b01d5-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b01d5-118">Примеры DirectShow</span><span class="sxs-lookup"><span data-stu-id="b01d5-118">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



