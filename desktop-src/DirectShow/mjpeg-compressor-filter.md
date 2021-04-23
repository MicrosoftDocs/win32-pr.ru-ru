---
description: Фильтр сжатия МЖПЕГ
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: Фильтр сжатия МЖПЕГ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02928df4d09b50c0ac152aed99ed87dc6362fb70
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910012"
---
# <a name="mjpeg-compressor-filter"></a><span data-ttu-id="1bfb7-103">Фильтр сжатия МЖПЕГ</span><span class="sxs-lookup"><span data-stu-id="1bfb7-103">MJPEG Compressor Filter</span></span>

<span data-ttu-id="1bfb7-104">Этот фильтр сжимает несжатый видеопоток, используя сжатие JPEG.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-104">This filter compresses an uncompressed video stream, using motion JPEG compression.</span></span>



| <span data-ttu-id="1bfb7-105">Метка</span><span class="sxs-lookup"><span data-stu-id="1bfb7-105">Label</span></span> | <span data-ttu-id="1bfb7-106">Значение</span><span class="sxs-lookup"><span data-stu-id="1bfb7-106">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bfb7-107">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="1bfb7-107">Filter Interfaces</span></span>                        | <span data-ttu-id="1bfb7-108">[**Ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="1bfb7-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="1bfb7-109">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="1bfb7-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="1bfb7-110">\_устройство MEDIATYPE, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="1bfb7-110">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="1bfb7-111">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="1bfb7-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="1bfb7-112">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="1bfb7-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="1bfb7-113">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="1bfb7-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="1bfb7-114">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ мжпг</span><span class="sxs-lookup"><span data-stu-id="1bfb7-114">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="1bfb7-115">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="1bfb7-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="1bfb7-116">[**Иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="1bfb7-116">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="1bfb7-117">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="1bfb7-117">Filter CLSID</span></span>                             | <span data-ttu-id="1bfb7-118">\_МЖПЖЕНК CLSID</span><span class="sxs-lookup"><span data-stu-id="1bfb7-118">CLSID\_MJPGEnc</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="1bfb7-119">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="1bfb7-119">Property Page CLSID</span></span>                      | <span data-ttu-id="1bfb7-120">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="1bfb7-120">No property page</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="1bfb7-121">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="1bfb7-121">Executable</span></span>                               | <span data-ttu-id="1bfb7-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="1bfb7-122">quartz.dll</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="1bfb7-123">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="1bfb7-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="1bfb7-124">\_ \_ не \_ использовать</span><span class="sxs-lookup"><span data-stu-id="1bfb7-124">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="1bfb7-125">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="1bfb7-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="1bfb7-126">\_ВИДЕОКОМПРЕССОРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="1bfb7-126">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="1bfb7-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1bfb7-127">Remarks</span></span>

<span data-ttu-id="1bfb7-128">Этот фильтр кодирует с помощью подтипа носителя МЕДИАСУБТИПЕ \_ мжпг, соответствующего коду FourCC "мжпг".</span><span class="sxs-lookup"><span data-stu-id="1bfb7-128">This filter encodes using the media subtype MEDIASUBTYPE\_MJPG, which corresponds to the FOURCC code 'MJPG'.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bfb7-129">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="1bfb7-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bfb7-130">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="1bfb7-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



