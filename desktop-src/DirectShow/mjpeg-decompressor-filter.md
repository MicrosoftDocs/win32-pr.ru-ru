---
description: Фильтр декомпрессора МЖПЕГ
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: Фильтр декомпрессора МЖПЕГ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23a3e3c09d218a83f5243bf6702d3b5fc3ae1c16
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910022"
---
# <a name="mjpeg-decompressor-filter"></a><span data-ttu-id="d7979-103">Фильтр декомпрессора МЖПЕГ</span><span class="sxs-lookup"><span data-stu-id="d7979-103">MJPEG Decompressor Filter</span></span>

<span data-ttu-id="d7979-104">Этот фильтр декодирует видеопоток из изображения перемещения JPEG в несжатое видео.</span><span class="sxs-lookup"><span data-stu-id="d7979-104">This filter decodes a video stream from motion JPEG to uncompressed video.</span></span> <span data-ttu-id="d7979-105">Некоторые цифровые видеокамеры создают поток видео в формате JPEG.</span><span class="sxs-lookup"><span data-stu-id="d7979-105">Some digital video cameras produce a motion JPEG video stream.</span></span>



| <span data-ttu-id="d7979-106">Метка</span><span class="sxs-lookup"><span data-stu-id="d7979-106">Label</span></span> | <span data-ttu-id="d7979-107">Значение</span><span class="sxs-lookup"><span data-stu-id="d7979-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7979-108">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="d7979-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="d7979-109">**ибасефилтер**</span><span class="sxs-lookup"><span data-stu-id="d7979-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="d7979-110">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="d7979-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="d7979-111">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ мжпг</span><span class="sxs-lookup"><span data-stu-id="d7979-111">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                               |
| <span data-ttu-id="d7979-112">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="d7979-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="d7979-113">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="d7979-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="d7979-114">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="d7979-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="d7979-115">\_устройство MEDIATYPE, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="d7979-115">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                               |
| <span data-ttu-id="d7979-116">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="d7979-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="d7979-117">[**Имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="d7979-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="d7979-118">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="d7979-118">Filter CLSID</span></span>                             | <span data-ttu-id="d7979-119">\_МЖПЕГДЕК CLSID</span><span class="sxs-lookup"><span data-stu-id="d7979-119">CLSID\_MjpegDec</span></span>                                                                                                                                    |
| <span data-ttu-id="d7979-120">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="d7979-120">Property Page CLSID</span></span>                      | <span data-ttu-id="d7979-121">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="d7979-121">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="d7979-122">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="d7979-122">Executable</span></span>                               | <span data-ttu-id="d7979-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="d7979-123">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="d7979-124">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="d7979-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="d7979-125">неуспешный \_ режим</span><span class="sxs-lookup"><span data-stu-id="d7979-125">MERIT\_NORMAL</span></span>                                                                                                                                      |
| [<span data-ttu-id="d7979-126">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="d7979-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="d7979-127">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="d7979-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="d7979-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7979-128">Remarks</span></span>

<span data-ttu-id="d7979-129">Этот фильтр совместим с видео о перемещении JPEG, в котором используется код FOURCC "МЖПГ".</span><span class="sxs-lookup"><span data-stu-id="d7979-129">This filter is compatible with motion JPEG video that uses the FOURCC code 'MJPG'.</span></span> <span data-ttu-id="d7979-130">Он не может декодировать другие виды перемещения JPEG.</span><span class="sxs-lookup"><span data-stu-id="d7979-130">It cannot decode other varieties of motion JPEG.</span></span> <span data-ttu-id="d7979-131">Для этого необходимо использовать фильтр декодера стороннего производителя.</span><span class="sxs-lookup"><span data-stu-id="d7979-131">For these, you will need to use a third-party decoder filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7979-132">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d7979-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7979-133">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="d7979-133">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



