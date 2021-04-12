---
description: Фильтр записи файлов
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: Фильтр записи файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f438f13f8d63b2856efd147c57ba6f071af26ff8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262450"
---
# <a name="file-writer-filter"></a><span data-ttu-id="209c4-103">Фильтр записи файлов</span><span class="sxs-lookup"><span data-stu-id="209c4-103">File Writer Filter</span></span>

<span data-ttu-id="209c4-104">Фильтр записи файлов можно использовать для записи файлов на диск независимо от формата.</span><span class="sxs-lookup"><span data-stu-id="209c4-104">The File Writer filter can be used to write files to disc regardless of format.</span></span> <span data-ttu-id="209c4-105">Фильтр просто записывает на диск все, что он получает на входном ПИН-коде, поэтому он должен быть подключен к мультиплексору, который может правильно отформатировать файл.</span><span class="sxs-lookup"><span data-stu-id="209c4-105">The filter simply writes to disc whatever it receives on its input pin, so it must be connected upstream to a multiplexer that can format the file correctly.</span></span> <span data-ttu-id="209c4-106">Можно создать новый выходной файл с помощью средства записи файлов или указать существующий файл. Если файл уже существует, он будет полностью перезаписан новыми данными.</span><span class="sxs-lookup"><span data-stu-id="209c4-106">You can create a new output file with the File Writer or specify an existing file; if the file already exists, it will be completely overwritten with the new data.</span></span>

<span data-ttu-id="209c4-107">Фильтр записи файлов использует отметки времени входного потока как смещения файлов и предоставляет произвольный доступ к файлу.</span><span class="sxs-lookup"><span data-stu-id="209c4-107">The file writer filter uses the input stream's time stamps as file offsets and provides random access to the file.</span></span> <span data-ttu-id="209c4-108">Он поддерживает **IStream** , чтобы разрешить чтение и запись заголовка файла после остановки графа.</span><span class="sxs-lookup"><span data-stu-id="209c4-108">It supports **IStream** to allow reading and writing the file header after the graph is stopped.</span></span> <span data-ttu-id="209c4-109">Для повышения производительности он также поддерживает перекрывающиеся записи без буферизации и обрабатывает соответствующее согласование буфера.</span><span class="sxs-lookup"><span data-stu-id="209c4-109">To improve performance it also supports unbuffered overlapped writes and handles the corresponding buffer negotiation.</span></span>

> [!Note]  
> <span data-ttu-id="209c4-110">Для записи файлов ASF используйте фильтр [модуля записи WM ASF](wm-asf-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="209c4-110">To write ASF files, use the [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span>

 



|                                          |                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="209c4-111">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="209c4-111">Filter Interfaces</span></span>                        | <span data-ttu-id="209c4-112">[**Иамфилтермискфлагс**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ифилесинкфилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="209c4-112">[**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream**</span></span> |
| <span data-ttu-id="209c4-113">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="209c4-113">Input Pin Media Types</span></span>                    | <span data-ttu-id="209c4-114">\_Поток MEDIATYPE, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="209c4-114">MEDIATYPE\_Stream, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                              |
| <span data-ttu-id="209c4-115">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="209c4-115">Input Pin Interfaces</span></span>                     | <span data-ttu-id="209c4-116">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**</span><span class="sxs-lookup"><span data-stu-id="209c4-116">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**</span></span>                                                                                |
| <span data-ttu-id="209c4-117">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="209c4-117">Output Pin Media Types</span></span>                   | <span data-ttu-id="209c4-118">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="209c4-118">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="209c4-119">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="209c4-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="209c4-120">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="209c4-120">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="209c4-121">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="209c4-121">Filter CLSID</span></span>                             | <span data-ttu-id="209c4-122">\_FILEWRITER CLSID</span><span class="sxs-lookup"><span data-stu-id="209c4-122">CLSID\_FileWriter</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="209c4-123">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="209c4-123">Property Page CLSID</span></span>                      | <span data-ttu-id="209c4-124">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="209c4-124">No property page</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="209c4-125">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="209c4-125">Executable</span></span>                               | <span data-ttu-id="209c4-126">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="209c4-126">qcap.dll</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="209c4-127">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="209c4-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="209c4-128">\_ \_ не \_ использовать</span><span class="sxs-lookup"><span data-stu-id="209c4-128">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="209c4-129">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="209c4-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="209c4-130">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="209c4-130">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="209c4-131">См. также</span><span class="sxs-lookup"><span data-stu-id="209c4-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="209c4-132">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="209c4-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



