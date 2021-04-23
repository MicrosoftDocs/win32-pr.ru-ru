---
description: Фильтр модуля подготовки отчетов для команды внутреннего скрипта
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: Фильтр модуля подготовки отчетов для команды внутреннего скрипта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b241643d991e9348015dc51ea5b2f1c4875f079d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537349"
---
# <a name="internal-script-command-renderer-filter"></a><span data-ttu-id="bce6f-103">Фильтр модуля подготовки отчетов для команды внутреннего скрипта</span><span class="sxs-lookup"><span data-stu-id="bce6f-103">Internal Script Command Renderer Filter</span></span>

<span data-ttu-id="bce6f-104">Получает команды сценария и отправляет их в приложение.</span><span class="sxs-lookup"><span data-stu-id="bce6f-104">Receives script commands and dispatches them to the application.</span></span>

<span data-ttu-id="bce6f-105">Этот фильтр принимает команды сценария в одном из двух форматов:</span><span class="sxs-lookup"><span data-stu-id="bce6f-105">This filter accepts script commands in one of two formats:</span></span>

-   <span data-ttu-id="bce6f-106">MEDIATYPE \_ Text: каждый пример носителя содержит текстовую строку ANSI.</span><span class="sxs-lookup"><span data-stu-id="bce6f-106">MEDIATYPE\_Text: Each media sample contains an ANSI text string.</span></span>
-   <span data-ttu-id="bce6f-107">MEDIATYPE \_ команду скрипта. Каждый пример носителя содержит две строки в Юникоде, заканчивающиеся нулем, сцепленные вместе.</span><span class="sxs-lookup"><span data-stu-id="bce6f-107">MEDIATYPE\_ScriptCommand: Each media sample contains two NULL-terminated Unicode strings, concatenated together.</span></span> <span data-ttu-id="bce6f-108">Первая строка описывает тип команды, а вторая — команду скрипта.</span><span class="sxs-lookup"><span data-stu-id="bce6f-108">The first string describes the command type and the second string is the script command.</span></span>

    <span data-ttu-id="bce6f-109">Когда фильтр получает образец, он отправляет уведомление о событии [**EC \_ OLE \_**](ec-ole-event.md) .</span><span class="sxs-lookup"><span data-stu-id="bce6f-109">When the filter receives a sample, it sends an [**EC\_OLE\_EVENT**](ec-ole-event.md) event notification.</span></span> <span data-ttu-id="bce6f-110">Первый параметр события — это **BSTR** с типом команды, или, `Text` Если используется формат MEDIATYPE \_ Text.</span><span class="sxs-lookup"><span data-stu-id="bce6f-110">The first event parameter is a **BSTR** with the command type, or `Text` if the format is MEDIATYPE\_Text.</span></span> <span data-ttu-id="bce6f-111">Вторым параметром события является **BSTR** с командой скрипта.</span><span class="sxs-lookup"><span data-stu-id="bce6f-111">The second event parameter is a **BSTR** with the script command.</span></span> <span data-ttu-id="bce6f-112">Приложение может получить событие и ответить на команду скрипта.</span><span class="sxs-lookup"><span data-stu-id="bce6f-112">The application can retrieve the event and respond to the script command.</span></span>

<span data-ttu-id="bce6f-113">Пример использования этого фильтра см. в разделе [средство синтаксического анализа Sami (CC)](sami--cc--parser-filter.md).</span><span class="sxs-lookup"><span data-stu-id="bce6f-113">For an example of how to use this filter, see [SAMI (CC) Parser](sami--cc--parser-filter.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bce6f-114">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="bce6f-114">Filter Interfaces</span></span></td>
<td><span data-ttu-id="bce6f-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a></span><span class="sxs-lookup"><span data-stu-id="bce6f-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bce6f-116">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="bce6f-116">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="bce6f-117">MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="bce6f-117">MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</span></span></li>
<li><span data-ttu-id="bce6f-118">MEDIATYPE_Text, MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="bce6f-118">MEDIATYPE_Text, MEDIASUBTYPE_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bce6f-119">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="bce6f-119">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="bce6f-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="bce6f-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bce6f-121">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="bce6f-121">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="bce6f-122">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="bce6f-122">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bce6f-123">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="bce6f-123">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="bce6f-124">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="bce6f-124">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bce6f-125">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="bce6f-125">Filter CLSID</span></span></td>
<td><span data-ttu-id="bce6f-126">{48025243-2D39-11CE-875D-00608CB78066}</span><span class="sxs-lookup"><span data-stu-id="bce6f-126">{48025243-2D39-11CE-875D-00608CB78066}</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bce6f-127">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="bce6f-127">Property Page CLSID</span></span></td>
<td><span data-ttu-id="bce6f-128">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="bce6f-128">No property page</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bce6f-129">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="bce6f-129">Executable</span></span></td>
<td><span data-ttu-id="bce6f-130">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="bce6f-130">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bce6f-131"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="bce6f-131"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="bce6f-132">MERIT_PREFERRED + 1</span><span class="sxs-lookup"><span data-stu-id="bce6f-132">MERIT_PREFERRED + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bce6f-133"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="bce6f-133"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="bce6f-134">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="bce6f-134">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="bce6f-135">См. также</span><span class="sxs-lookup"><span data-stu-id="bce6f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bce6f-136">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="bce6f-136">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



