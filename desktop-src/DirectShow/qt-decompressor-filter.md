---
description: Фильтр раскомпрессоров QT
ms.assetid: d013075f-deab-40ef-8438-4fb09820da3e
title: Фильтр раскомпрессоров QT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e586eb9d65ee00509f4a434f3283bd762d535b26
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494859"
---
# <a name="qt-decompressor-filter"></a><span data-ttu-id="02aa9-103">Фильтр раскомпрессоров QT</span><span class="sxs-lookup"><span data-stu-id="02aa9-103">QT Decompressor Filter</span></span>

<span data-ttu-id="02aa9-104">Этот компонент был удален из Windows Vista и более поздних операционных систем.</span><span class="sxs-lookup"><span data-stu-id="02aa9-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="02aa9-105">Он доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="02aa9-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="02aa9-106">Фильтр "декомпрессор QT" распаковывает видео Apple® QuickTime® 2,0.</span><span class="sxs-lookup"><span data-stu-id="02aa9-106">The QT Decompressor filter decompresses Apple® QuickTime® 2.0 video.</span></span> <span data-ttu-id="02aa9-107">Этот формат обычно используется в старых файлах QuickTime.</span><span class="sxs-lookup"><span data-stu-id="02aa9-107">This format is typically used in older QuickTime files.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02aa9-108">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="02aa9-108">Filter Interfaces</span></span></td>
<td><span data-ttu-id="02aa9-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a></span><span class="sxs-lookup"><span data-stu-id="02aa9-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02aa9-110">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="02aa9-110">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="02aa9-111">MEDIATYPE_Video, FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="02aa9-111">MEDIATYPE_Video, FORMAT_VideoInfo</span></span><br/> <span data-ttu-id="02aa9-112">Допустимы следующие подтипы:</span><span class="sxs-lookup"><span data-stu-id="02aa9-112">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="02aa9-113">MEDIASUBTYPE_QTRpza</span><span class="sxs-lookup"><span data-stu-id="02aa9-113">MEDIASUBTYPE_QTRpza</span></span></li>
<li><span data-ttu-id="02aa9-114">MEDIASUBTYPE_QTSmc</span><span class="sxs-lookup"><span data-stu-id="02aa9-114">MEDIASUBTYPE_QTSmc</span></span></li>
<li><span data-ttu-id="02aa9-115">MEDIASUBTYPE_QTRle</span><span class="sxs-lookup"><span data-stu-id="02aa9-115">MEDIASUBTYPE_QTRle</span></span></li>
<li><span data-ttu-id="02aa9-116">MEDIASUBTYPE_QTJpeg</span><span class="sxs-lookup"><span data-stu-id="02aa9-116">MEDIASUBTYPE_QTJpeg</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02aa9-117">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="02aa9-117">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="02aa9-118"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="02aa9-118"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02aa9-119">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="02aa9-119">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="02aa9-120">MEDIATYPE_Video, MEDIASUBTYPE_NULL FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="02aa9-120">MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02aa9-121">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="02aa9-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="02aa9-122"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="02aa9-122"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02aa9-123">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="02aa9-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="02aa9-124">CLSID_QTDec</span><span class="sxs-lookup"><span data-stu-id="02aa9-124">CLSID_QTDec</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02aa9-125">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="02aa9-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="02aa9-126">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="02aa9-126">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02aa9-127">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="02aa9-127">Executable</span></span></td>
<td><span data-ttu-id="02aa9-128">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="02aa9-128">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02aa9-129"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="02aa9-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="02aa9-130">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="02aa9-130">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02aa9-131"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="02aa9-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="02aa9-132">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="02aa9-132">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="02aa9-133">См. также</span><span class="sxs-lookup"><span data-stu-id="02aa9-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02aa9-134">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="02aa9-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




