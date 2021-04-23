---
description: Фильтр записи файлов
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: Фильтр записи файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991536d505ee1bdfcaaaca5ce8660c4480decf6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909692"
---
# <a name="file-writer-filter"></a><span data-ttu-id="474a8-103">Фильтр записи файлов</span><span class="sxs-lookup"><span data-stu-id="474a8-103">File Writer Filter</span></span>

<span data-ttu-id="474a8-104">Фильтр записи файлов можно использовать для записи файлов на диск независимо от формата.</span><span class="sxs-lookup"><span data-stu-id="474a8-104">The File Writer filter can be used to write files to disc regardless of format.</span></span> <span data-ttu-id="474a8-105">Фильтр просто записывает на диск все, что он получает на входном ПИН-коде, поэтому он должен быть подключен к мультиплексору, который может правильно отформатировать файл.</span><span class="sxs-lookup"><span data-stu-id="474a8-105">The filter simply writes to disc whatever it receives on its input pin, so it must be connected upstream to a multiplexer that can format the file correctly.</span></span> <span data-ttu-id="474a8-106">Можно создать новый выходной файл с помощью средства записи файлов или указать существующий файл. Если файл уже существует, он будет полностью перезаписан новыми данными.</span><span class="sxs-lookup"><span data-stu-id="474a8-106">You can create a new output file with the File Writer or specify an existing file; if the file already exists, it will be completely overwritten with the new data.</span></span>

<span data-ttu-id="474a8-107">Фильтр записи файлов использует отметки времени входного потока как смещения файлов и предоставляет произвольный доступ к файлу.</span><span class="sxs-lookup"><span data-stu-id="474a8-107">The file writer filter uses the input stream's time stamps as file offsets and provides random access to the file.</span></span> <span data-ttu-id="474a8-108">Он поддерживает **IStream** , чтобы разрешить чтение и запись заголовка файла после остановки графа.</span><span class="sxs-lookup"><span data-stu-id="474a8-108">It supports **IStream** to allow reading and writing the file header after the graph is stopped.</span></span> <span data-ttu-id="474a8-109">Для повышения производительности он также поддерживает перекрывающиеся записи без буферизации и обрабатывает соответствующее согласование буфера.</span><span class="sxs-lookup"><span data-stu-id="474a8-109">To improve performance it also supports unbuffered overlapped writes and handles the corresponding buffer negotiation.</span></span>

> [!Note]  
> <span data-ttu-id="474a8-110">Для записи файлов ASF используйте фильтр [модуля записи WM ASF](wm-asf-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="474a8-110">To write ASF files, use the [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span>

 



| <span data-ttu-id="474a8-111">Метка</span><span class="sxs-lookup"><span data-stu-id="474a8-111">Label</span></span> | <span data-ttu-id="474a8-112">Значение</span><span class="sxs-lookup"><span data-stu-id="474a8-112">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="474a8-113">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="474a8-113">Filter Interfaces</span></span>                        | <span data-ttu-id="474a8-114">[**Иамфилтермискфлагс**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ифилесинкфилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="474a8-114">[**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream**</span></span> |
| <span data-ttu-id="474a8-115">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="474a8-115">Input Pin Media Types</span></span>                    | <span data-ttu-id="474a8-116">\_Поток MEDIATYPE, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="474a8-116">MEDIATYPE\_Stream, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                              |
| <span data-ttu-id="474a8-117">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="474a8-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="474a8-118">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**</span><span class="sxs-lookup"><span data-stu-id="474a8-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**</span></span>                                                                                |
| <span data-ttu-id="474a8-119">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="474a8-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="474a8-120">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="474a8-120">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="474a8-121">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="474a8-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="474a8-122">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="474a8-122">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="474a8-123">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="474a8-123">Filter CLSID</span></span>                             | <span data-ttu-id="474a8-124">\_FILEWRITER CLSID</span><span class="sxs-lookup"><span data-stu-id="474a8-124">CLSID\_FileWriter</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="474a8-125">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="474a8-125">Property Page CLSID</span></span>                      | <span data-ttu-id="474a8-126">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="474a8-126">No property page</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="474a8-127">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="474a8-127">Executable</span></span>                               | <span data-ttu-id="474a8-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="474a8-128">qcap.dll</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="474a8-129">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="474a8-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="474a8-130">\_ \_ не \_ использовать</span><span class="sxs-lookup"><span data-stu-id="474a8-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="474a8-131">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="474a8-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="474a8-132">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="474a8-132">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="474a8-133">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="474a8-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="474a8-134">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="474a8-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



