---
description: Фильтр декомпрессора МЖПЕГ
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: Фильтр декомпрессора МЖПЕГ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebe8f5f19cb94d75c1ce01cd94dc723100560de
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537994"
---
# <a name="mjpeg-decompressor-filter"></a><span data-ttu-id="80aa0-103">Фильтр декомпрессора МЖПЕГ</span><span class="sxs-lookup"><span data-stu-id="80aa0-103">MJPEG Decompressor Filter</span></span>

<span data-ttu-id="80aa0-104">Этот фильтр декодирует видеопоток из изображения перемещения JPEG в несжатое видео.</span><span class="sxs-lookup"><span data-stu-id="80aa0-104">This filter decodes a video stream from motion JPEG to uncompressed video.</span></span> <span data-ttu-id="80aa0-105">Некоторые цифровые видеокамеры создают поток видео в формате JPEG.</span><span class="sxs-lookup"><span data-stu-id="80aa0-105">Some digital video cameras produce a motion JPEG video stream.</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80aa0-106">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="80aa0-106">Filter Interfaces</span></span>                        | [<span data-ttu-id="80aa0-107">**ибасефилтер**</span><span class="sxs-lookup"><span data-stu-id="80aa0-107">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="80aa0-108">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="80aa0-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="80aa0-109">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ мжпг</span><span class="sxs-lookup"><span data-stu-id="80aa0-109">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                               |
| <span data-ttu-id="80aa0-110">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="80aa0-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="80aa0-111">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="80aa0-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="80aa0-112">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="80aa0-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="80aa0-113">\_устройство MEDIATYPE, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="80aa0-113">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                               |
| <span data-ttu-id="80aa0-114">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="80aa0-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="80aa0-115">[**Имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="80aa0-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="80aa0-116">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="80aa0-116">Filter CLSID</span></span>                             | <span data-ttu-id="80aa0-117">\_МЖПЕГДЕК CLSID</span><span class="sxs-lookup"><span data-stu-id="80aa0-117">CLSID\_MjpegDec</span></span>                                                                                                                                    |
| <span data-ttu-id="80aa0-118">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="80aa0-118">Property Page CLSID</span></span>                      | <span data-ttu-id="80aa0-119">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="80aa0-119">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="80aa0-120">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="80aa0-120">Executable</span></span>                               | <span data-ttu-id="80aa0-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="80aa0-121">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="80aa0-122">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="80aa0-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="80aa0-123">неуспешный \_ режим</span><span class="sxs-lookup"><span data-stu-id="80aa0-123">MERIT\_NORMAL</span></span>                                                                                                                                      |
| [<span data-ttu-id="80aa0-124">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="80aa0-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="80aa0-125">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="80aa0-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="80aa0-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80aa0-126">Remarks</span></span>

<span data-ttu-id="80aa0-127">Этот фильтр совместим с видео о перемещении JPEG, в котором используется код FOURCC "МЖПГ".</span><span class="sxs-lookup"><span data-stu-id="80aa0-127">This filter is compatible with motion JPEG video that uses the FOURCC code 'MJPG'.</span></span> <span data-ttu-id="80aa0-128">Он не может декодировать другие виды перемещения JPEG.</span><span class="sxs-lookup"><span data-stu-id="80aa0-128">It cannot decode other varieties of motion JPEG.</span></span> <span data-ttu-id="80aa0-129">Для этого необходимо использовать фильтр декодера стороннего производителя.</span><span class="sxs-lookup"><span data-stu-id="80aa0-129">For these, you will need to use a third-party decoder filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80aa0-130">См. также</span><span class="sxs-lookup"><span data-stu-id="80aa0-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80aa0-131">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="80aa0-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



