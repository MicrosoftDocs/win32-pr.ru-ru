---
description: Фильтр сжатия МЖПЕГ
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: Фильтр сжатия МЖПЕГ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a20c559bb889750959a4868fa08c03b3eb12dfb5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673083"
---
# <a name="mjpeg-compressor-filter"></a><span data-ttu-id="491a5-103">Фильтр сжатия МЖПЕГ</span><span class="sxs-lookup"><span data-stu-id="491a5-103">MJPEG Compressor Filter</span></span>

<span data-ttu-id="491a5-104">Этот фильтр сжимает несжатый видеопоток, используя сжатие JPEG.</span><span class="sxs-lookup"><span data-stu-id="491a5-104">This filter compresses an uncompressed video stream, using motion JPEG compression.</span></span>



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="491a5-105">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="491a5-105">Filter Interfaces</span></span>                        | <span data-ttu-id="491a5-106">[**Ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="491a5-106">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="491a5-107">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="491a5-107">Input Pin Media Types</span></span>                    | <span data-ttu-id="491a5-108">\_устройство MEDIATYPE, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="491a5-108">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="491a5-109">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="491a5-109">Input Pin Interfaces</span></span>                     | <span data-ttu-id="491a5-110">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="491a5-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="491a5-111">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="491a5-111">Output Pin Media Types</span></span>                   | <span data-ttu-id="491a5-112">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ мжпг</span><span class="sxs-lookup"><span data-stu-id="491a5-112">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="491a5-113">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="491a5-113">Output Pin Interfaces</span></span>                    | <span data-ttu-id="491a5-114">[**Иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="491a5-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="491a5-115">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="491a5-115">Filter CLSID</span></span>                             | <span data-ttu-id="491a5-116">\_МЖПЖЕНК CLSID</span><span class="sxs-lookup"><span data-stu-id="491a5-116">CLSID\_MJPGEnc</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="491a5-117">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="491a5-117">Property Page CLSID</span></span>                      | <span data-ttu-id="491a5-118">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="491a5-118">No property page</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="491a5-119">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="491a5-119">Executable</span></span>                               | <span data-ttu-id="491a5-120">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="491a5-120">quartz.dll</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="491a5-121">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="491a5-121">Merit</span></span>](merit.md)                       | <span data-ttu-id="491a5-122">\_ \_ не \_ использовать</span><span class="sxs-lookup"><span data-stu-id="491a5-122">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="491a5-123">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="491a5-123">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="491a5-124">\_ВИДЕОКОМПРЕССОРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="491a5-124">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="491a5-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="491a5-125">Remarks</span></span>

<span data-ttu-id="491a5-126">Этот фильтр кодирует с помощью подтипа носителя МЕДИАСУБТИПЕ \_ мжпг, соответствующего коду FourCC "мжпг".</span><span class="sxs-lookup"><span data-stu-id="491a5-126">This filter encodes using the media subtype MEDIASUBTYPE\_MJPG, which corresponds to the FOURCC code 'MJPG'.</span></span>

## <a name="related-topics"></a><span data-ttu-id="491a5-127">См. также</span><span class="sxs-lookup"><span data-stu-id="491a5-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="491a5-128">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="491a5-128">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



