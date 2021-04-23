---
description: Типы носителей для демультиплексирования MPEG-2
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: Типы носителей для демультиплексирования MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9b5276b975771ba62118976c8e63b4d5faa53d
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910002"
---
# <a name="mpeg-2-demultiplexer-media-types"></a><span data-ttu-id="24695-103">Типы носителей для демультиплексирования MPEG-2</span><span class="sxs-lookup"><span data-stu-id="24695-103">MPEG-2 Demultiplexer Media Types</span></span>

<span data-ttu-id="24695-104">Фильтр [демультиплексора MPEG-2](mpeg-2-demultiplexer.md) распознает следующие типы носителей.</span><span class="sxs-lookup"><span data-stu-id="24695-104">The [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) filter recognizes the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="24695-105">Типы входных данных</span><span class="sxs-lookup"><span data-stu-id="24695-105">Input Types</span></span>

<span data-ttu-id="24695-106">Основной тип всегда является **\_ потоком типа MEDIATYPE**.</span><span class="sxs-lookup"><span data-stu-id="24695-106">The major type is always **MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="24695-107">Подтип может быть любым из следующих.</span><span class="sxs-lookup"><span data-stu-id="24695-107">The subtype can be any of the following.</span></span>



| <span data-ttu-id="24695-108">Идентификатор GUID</span><span class="sxs-lookup"><span data-stu-id="24695-108">GUID</span></span>                                             | <span data-ttu-id="24695-109">Описание</span><span class="sxs-lookup"><span data-stu-id="24695-109">Description</span></span>                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24695-110">**\_ \_ \_ Транспорт BDA MPEG2 для подтипа ксдатаформат \_**</span><span class="sxs-lookup"><span data-stu-id="24695-110">**KSDATAFORMAT\_SUBTYPE\_BDA\_MPEG2\_TRANSPORT**</span></span> | <span data-ttu-id="24695-111">Транспортный поток из фильтра устройств на основе широковещательной архитектуры драйверов (BDA).</span><span class="sxs-lookup"><span data-stu-id="24695-111">Transport stream from a Broadcast Driver Architecture (BDA) device filter.</span></span> <span data-ttu-id="24695-112">Демультиплексор MPEG-2 обрабатывает этот подтип одинаково для **медиасубтипеного \_ \_ транспорта MPEG2**.</span><span class="sxs-lookup"><span data-stu-id="24695-112">The MPEG-2 demultiplexer treats this subtype identically to **MEDIASUBTYPE\_MPEG2\_TRANSPORT**.</span></span>                                |
| <span data-ttu-id="24695-113">**\_Программа медиасубтипе MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="24695-113">**MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span>                 | <span data-ttu-id="24695-114">Поток программы</span><span class="sxs-lookup"><span data-stu-id="24695-114">Program stream</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="24695-115">**\_Транспорт медиасубтипе MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="24695-115">**MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span>               | <span data-ttu-id="24695-116">Транспортный поток (TS) с 188-байтными пакетами</span><span class="sxs-lookup"><span data-stu-id="24695-116">Transport stream (TS), with 188-byte packets</span></span>                                                                                                                                                              |
| <span data-ttu-id="24695-117">**\_ \_ Шаг транспорта медиасубтипе \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="24695-117">**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**</span></span>       | <span data-ttu-id="24695-118">Транспортный поток с "пошаговыми" пакетами.</span><span class="sxs-lookup"><span data-stu-id="24695-118">Transport stream with "strided" packets.</span></span> <span data-ttu-id="24695-119">Этот подтип указывает, что пакеты служб терминалов могут быть дополнены дополнительными байтами.</span><span class="sxs-lookup"><span data-stu-id="24695-119">This subtype indicates that the TS packets may be padded with extra bytes.</span></span> <span data-ttu-id="24695-120">Дополнительные сведения см. в разделе параметр [**\_ \_ транспорта MPEG2**](mpeg2-transport-stride.md).</span><span class="sxs-lookup"><span data-stu-id="24695-120">For more information, see [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> |



 

<span data-ttu-id="24695-121">Для транспортных транспортных пакетов **( \_ \_ \_ Шаг с медиасубтипеом для транспорта MPEG2**) каждый пример носителя должен содержать целое число транспортных пакетов, как описано в разделе [**\_ транспорт MPEG2 \_ stride**](mpeg2-transport-stride.md).</span><span class="sxs-lookup"><span data-stu-id="24695-121">For strided transport packets (**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**), each media sample must contain an integral number of transport packets, as described in [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> <span data-ttu-id="24695-122">Для всех остальных типов входных данных нет ограничений на границы выборки; отдельные пакеты могут охватывать границы выборки.</span><span class="sxs-lookup"><span data-stu-id="24695-122">For all other input types, there are no restrictions on sample boundaries; individual packets can span sample boundaries.</span></span>

### <a name="output-types"></a><span data-ttu-id="24695-123">Типы вывода</span><span class="sxs-lookup"><span data-stu-id="24695-123">Output Types</span></span>

<span data-ttu-id="24695-124">Демультиплексор MPEG-2 не проверяет типы выходных данных. нисходящий фильтр отвечает за анализ данных, получаемых от демультиплексора.</span><span class="sxs-lookup"><span data-stu-id="24695-124">The MPEG-2 Demultiplexer does not validate output types; the downstream filter is responsible for parsing the data it receives from the demultiplexer.</span></span> <span data-ttu-id="24695-125">Однако следующие типы обычно принимаются нисходящими фильтрами в качестве выходных данных от демультиплексора.</span><span class="sxs-lookup"><span data-stu-id="24695-125">However, the following types are commonly accepted by downstream filters as output from the demultiplexer.</span></span>

### <a name="mpeg-2-sections"></a><span data-ttu-id="24695-126">Разделы MPEG-2</span><span class="sxs-lookup"><span data-stu-id="24695-126">MPEG-2 Sections</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="24695-127">Основной тип</span><span class="sxs-lookup"><span data-stu-id="24695-127">Major Type</span></span></td>
<td><span data-ttu-id="24695-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span><span class="sxs-lookup"><span data-stu-id="24695-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24695-129">Subtype</span><span class="sxs-lookup"><span data-stu-id="24695-129">Subtype</span></span></td>
<td><span data-ttu-id="24695-130">Любое из следующих:</span><span class="sxs-lookup"><span data-stu-id="24695-130">Any of the following:</span></span><br/>
<ul>
<li><span data-ttu-id="24695-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: сведения о службе ATSC.</span><span class="sxs-lookup"><span data-stu-id="24695-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: ATSC Service Information.</span></span></li>
<li><span data-ttu-id="24695-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: сведения о службе DVB.</span><span class="sxs-lookup"><span data-stu-id="24695-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: DVB Service Information.</span></span></li>
<li><span data-ttu-id="24695-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: сведения о службе Digital ШИРОКОВЕЩАНИЯ (ISDB) для интегрированных служб.</span><span class="sxs-lookup"><span data-stu-id="24695-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: Integrated Services Digital Broadcasting (ISDB) Service Information.</span></span></li>
<li><span data-ttu-id="24695-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: данные раздела MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="24695-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: MPEG-2 section data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24695-135">Тип формата</span><span class="sxs-lookup"><span data-stu-id="24695-135">Format Type</span></span></td>
<td><span data-ttu-id="24695-136">None</span><span class="sxs-lookup"><span data-stu-id="24695-136">None</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="mpeg-2-video"></a><span data-ttu-id="24695-137">Видео MPEG-2</span><span class="sxs-lookup"><span data-stu-id="24695-137">MPEG-2 Video</span></span>



| <span data-ttu-id="24695-138">Метка</span><span class="sxs-lookup"><span data-stu-id="24695-138">Label</span></span> | <span data-ttu-id="24695-139">Значение</span><span class="sxs-lookup"><span data-stu-id="24695-139">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="24695-140">Основной тип</span><span class="sxs-lookup"><span data-stu-id="24695-140">Major type</span></span>       | <span data-ttu-id="24695-141">**\_Видео MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="24695-141">**MEDIATYPE\_Video**</span></span>                     |
| <span data-ttu-id="24695-142">Subtype</span><span class="sxs-lookup"><span data-stu-id="24695-142">Subtype</span></span>          | <span data-ttu-id="24695-143">**\_Видео медиасубтипе MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="24695-143">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           |
| <span data-ttu-id="24695-144">Тип формата</span><span class="sxs-lookup"><span data-stu-id="24695-144">Format Type</span></span>      | <span data-ttu-id="24695-145">**ФОРМАТ \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="24695-145">**FORMAT\_MPEG2Video**</span></span>                   |
| <span data-ttu-id="24695-146">Структура формата</span><span class="sxs-lookup"><span data-stu-id="24695-146">Format Structure</span></span> | [<span data-ttu-id="24695-147">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="24695-147">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a><span data-ttu-id="24695-148">Звук MPEG-2</span><span class="sxs-lookup"><span data-stu-id="24695-148">MPEG-2 Audio</span></span>



| <span data-ttu-id="24695-149">Метка</span><span class="sxs-lookup"><span data-stu-id="24695-149">Label</span></span> | <span data-ttu-id="24695-150">Значение</span><span class="sxs-lookup"><span data-stu-id="24695-150">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="24695-151">Основной тип</span><span class="sxs-lookup"><span data-stu-id="24695-151">Major type</span></span>       | <span data-ttu-id="24695-152">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="24695-152">**MEDIATYPE\_Audio**</span></span>                 |
| <span data-ttu-id="24695-153">Subtype</span><span class="sxs-lookup"><span data-stu-id="24695-153">Subtype</span></span>          | <span data-ttu-id="24695-154">**МЕДИАСУБТИПЕ \_ MPEG2 \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="24695-154">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>       |
| <span data-ttu-id="24695-155">Тип формата</span><span class="sxs-lookup"><span data-stu-id="24695-155">Format Type</span></span>      | <span data-ttu-id="24695-156">**ФОРМАТ \_ вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="24695-156">**FORMAT\_WaveFormatEx**</span></span>             |
| <span data-ttu-id="24695-157">Структура формата</span><span class="sxs-lookup"><span data-stu-id="24695-157">Format Structure</span></span> | <span data-ttu-id="24695-158">[**вавеформатекс**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24695-158">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="24695-159">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="24695-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24695-160">Типы мультимедиа MPEG-2</span><span class="sxs-lookup"><span data-stu-id="24695-160">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
