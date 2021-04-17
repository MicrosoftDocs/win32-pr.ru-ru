---
description: Фильтр синтаксического анализатора с несколькими файлами
ms.assetid: 8ef06f49-fda4-49e2-9b07-70453a2e897c
title: Фильтр синтаксического анализатора с несколькими файлами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44fc83a56bb12c307b85be875a3a2e7e73b744d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682259"
---
# <a name="multi-file-parser-filter"></a><span data-ttu-id="1f907-103">Фильтр синтаксического анализатора с несколькими файлами</span><span class="sxs-lookup"><span data-stu-id="1f907-103">Multi-File Parser Filter</span></span>

<span data-ttu-id="1f907-104">Фильтр синтаксического анализатора с несколькими файлами анализирует простой формат файла, который позволяет указать несколько имен файлов, как если бы они были одним файлом.</span><span class="sxs-lookup"><span data-stu-id="1f907-104">The Multi-File Parser filter parses a simple file format that enables multiple file names to be specified as though they were one file.</span></span> <span data-ttu-id="1f907-105">Эти файлы имеют формат, показанный в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="1f907-105">These files have the format shown in the following example:</span></span>


```C++
;MULTI
https://server/share/video.mpg
https://server/share/captions.smi
```



<span data-ttu-id="1f907-106">Использование этого фильтра является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="1f907-106">The use of this filter is deprecated.</span></span> <span data-ttu-id="1f907-107">Для отрисовки нескольких файлов в одном графе фильтра приложение должно просто вызвать **RenderFile** или **аддсаурцефилтер** несколько раз.</span><span class="sxs-lookup"><span data-stu-id="1f907-107">To render multiple files within the same filter graph, the application should simply call **RenderFile** or **AddSourceFilter** multiple times.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1f907-108">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="1f907-108">Filter interfaces</span></span></td>
<td><span data-ttu-id="1f907-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f907-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f907-110">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="1f907-110">Input pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="1f907-111">Основной тип: MEDIATYPE_Stream</span><span class="sxs-lookup"><span data-stu-id="1f907-111">Major type: MEDIATYPE_Stream</span></span></li>
<li><span data-ttu-id="1f907-112">Подтип: CLSID_MultFile</span><span class="sxs-lookup"><span data-stu-id="1f907-112">Subtype: CLSID_MultFile</span></span></li>
<li><span data-ttu-id="1f907-113">Тип формата: GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="1f907-113">Format type: GUID_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f907-114">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="1f907-114">Input pin interfaces</span></span></td>
<td><span data-ttu-id="1f907-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f907-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f907-116">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="1f907-116">Output pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="1f907-117">Основной тип: MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="1f907-117">Major type: MEDIATYPE_File</span></span></li>
<li><span data-ttu-id="1f907-118">Подтип: GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="1f907-118">Subtype: GUID_NULL</span></span></li>
<li><span data-ttu-id="1f907-119">Тип формата: MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="1f907-119">Format type: MEDIATYPE_File</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f907-120">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="1f907-120">Output pin interfaces</span></span></td>
<td><span data-ttu-id="1f907-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f907-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f907-122">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="1f907-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="1f907-123">CLSID_MultFile</span><span class="sxs-lookup"><span data-stu-id="1f907-123">CLSID_MultFile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f907-124">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="1f907-124">Executable</span></span></td>
<td><span data-ttu-id="1f907-125">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="1f907-125">Quartz.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f907-126"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="1f907-126"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="1f907-127">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="1f907-127">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f907-128"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="1f907-128"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="1f907-129">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="1f907-129">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="1f907-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f907-130">Remarks</span></span>

<span data-ttu-id="1f907-131">Фильтр создает один выходной ПИН-код для каждого файла, указанного в исходном файле.</span><span class="sxs-lookup"><span data-stu-id="1f907-131">The filter creates one output pin for each file listed in the source file.</span></span> <span data-ttu-id="1f907-132">Тип выходных данных — MEDIATYPE \_ File, а блок формата для выходного типа — это строка расширенных символов, содержащая имя файла.</span><span class="sxs-lookup"><span data-stu-id="1f907-132">The output type is MEDIATYPE\_File, and the format block for the output type is a wide-character string that contains the file name.</span></span> <span data-ttu-id="1f907-133">Каждый ПИН-код подключается к экземпляру фильтра модуля [подготовки к потоку файлов](file-stream-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="1f907-133">Each pin connects to an instance of the [File Stream Renderer](file-stream-renderer-filter.md) filter.</span></span> <span data-ttu-id="1f907-134">Фильтр модуля подготовки к потоку файлов создает один выходной ПИН-код, который предоставляет интерфейс [**истреамбуилдер**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) .</span><span class="sxs-lookup"><span data-stu-id="1f907-134">The File Stream Renderer filter creates one output pin, which exposes the [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) interface.</span></span> <span data-ttu-id="1f907-135">Закрепление вывода подготавливает к просмотру указанный файл.</span><span class="sxs-lookup"><span data-stu-id="1f907-135">The output pin renders the specified file.</span></span> <span data-ttu-id="1f907-136">Данные мультимедиа не передаются между средством синтаксического анализа нескольких файлов и модулем подготовки потока файлов.</span><span class="sxs-lookup"><span data-stu-id="1f907-136">No media data travels between the Multi-File Parser and the File Stream Renderer.</span></span>

<span data-ttu-id="1f907-137">CLSID фильтра не определен в UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="1f907-137">The filter's CLSID is not defined in Uuids.h.</span></span> <span data-ttu-id="1f907-138">Используйте этот макрос в своем собственном файле заголовка:</span><span class="sxs-lookup"><span data-stu-id="1f907-138">Use this macro in your own header file:</span></span>


```C++
// {D51BD5A3-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_MultFile,
0xd51bd5a3, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a><span data-ttu-id="1f907-139">См. также</span><span class="sxs-lookup"><span data-stu-id="1f907-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f907-140">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="1f907-140">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



