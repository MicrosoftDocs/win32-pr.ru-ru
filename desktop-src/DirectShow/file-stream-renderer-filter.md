---
description: Фильтр модуля подготовки к потоку файлов
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: Фильтр модуля подготовки к потоку файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64c8d8a0c87dab3aa811c8246be24ded8ee04dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537889"
---
# <a name="file-stream-renderer-filter"></a><span data-ttu-id="8f8f2-103">Фильтр модуля подготовки к потоку файлов</span><span class="sxs-lookup"><span data-stu-id="8f8f2-103">File Stream Renderer Filter</span></span>

<span data-ttu-id="8f8f2-104">Фильтр модуля подготовки отчетов File Stream подготавливает к просмотру имена файлов, которые анализируются фильтром [синтаксического анализатора с несколькими файлами](multi-file-parser-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="8f8f2-104">The File Stream Renderer filter renders file names that are parsed by the [Multi-File Parser](multi-file-parser-filter.md) filter.</span></span> <span data-ttu-id="8f8f2-105">Дополнительные сведения см. в документации по этому фильтру.</span><span class="sxs-lookup"><span data-stu-id="8f8f2-105">For more information, see the documentation for that filter.</span></span>

<span data-ttu-id="8f8f2-106">Использование этого фильтра является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="8f8f2-106">The use of this filter is deprecated.</span></span> <span data-ttu-id="8f8f2-107">Для отрисовки нескольких файлов в одном графе фильтра приложение должно просто вызвать **RenderFile** или **аддсаурцефилтер** несколько раз.</span><span class="sxs-lookup"><span data-stu-id="8f8f2-107">To render multiple files within the same filter graph, the application should simply call **RenderFile** or **AddSourceFilter** multiple times.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8f8f2-108">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="8f8f2-108">Filter interfaces</span></span></td>
<td><span data-ttu-id="8f8f2-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f8f2-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f8f2-110">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="8f8f2-110">Input pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="8f8f2-111">Основной тип: MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="8f8f2-111">Major type: MEDIATYPE_File</span></span></li>
<li><span data-ttu-id="8f8f2-112">Подтип: GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="8f8f2-112">Subtype: GUID_NULL</span></span></li>
<li><span data-ttu-id="8f8f2-113">Тип формата: MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="8f8f2-113">Format type: MEDIATYPE_File</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f8f2-114">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="8f8f2-114">Input pin interfaces</span></span></td>
<td><span data-ttu-id="8f8f2-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f8f2-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f8f2-116">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="8f8f2-116">Output pin media types</span></span></td>
<td><span data-ttu-id="8f8f2-117">Нет</span><span class="sxs-lookup"><span data-stu-id="8f8f2-117">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f8f2-118">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="8f8f2-118">Output pin interfaces</span></span></td>
<td><span data-ttu-id="8f8f2-119"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>истреамбуилдер</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f8f2-119"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f8f2-120">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="8f8f2-120">Filter CLSID</span></span></td>
<td><span data-ttu-id="8f8f2-121">CLSID_FileRend</span><span class="sxs-lookup"><span data-stu-id="8f8f2-121">CLSID_FileRend</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f8f2-122">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="8f8f2-122">Executable</span></span></td>
<td><span data-ttu-id="8f8f2-123">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="8f8f2-123">Quartz.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f8f2-124"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="8f8f2-124"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="8f8f2-125">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="8f8f2-125">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f8f2-126"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="8f8f2-126"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="8f8f2-127">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="8f8f2-127">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="8f8f2-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f8f2-128">Remarks</span></span>

<span data-ttu-id="8f8f2-129">CLSID фильтра не определен в UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="8f8f2-129">The filter's CLSID is not defined in Uuids.h.</span></span> <span data-ttu-id="8f8f2-130">Используйте этот макрос в своем собственном файле заголовка:</span><span class="sxs-lookup"><span data-stu-id="8f8f2-130">Use this macro in your own header file:</span></span>


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a><span data-ttu-id="8f8f2-131">См. также</span><span class="sxs-lookup"><span data-stu-id="8f8f2-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f8f2-132">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="8f8f2-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



