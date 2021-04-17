---
description: Типы носителей для демультиплексирования MPEG-2
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: Типы носителей для демультиплексирования MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b21eecff138b987c791ecd97056fb4cf417dd98d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684774"
---
# <a name="mpeg-2-demultiplexer-media-types"></a><span data-ttu-id="4db78-103">Типы носителей для демультиплексирования MPEG-2</span><span class="sxs-lookup"><span data-stu-id="4db78-103">MPEG-2 Demultiplexer Media Types</span></span>

<span data-ttu-id="4db78-104">Фильтр [демультиплексора MPEG-2](mpeg-2-demultiplexer.md) распознает следующие типы носителей.</span><span class="sxs-lookup"><span data-stu-id="4db78-104">The [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) filter recognizes the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="4db78-105">Типы входных данных</span><span class="sxs-lookup"><span data-stu-id="4db78-105">Input Types</span></span>

<span data-ttu-id="4db78-106">Основной тип всегда является **\_ потоком типа MEDIATYPE**.</span><span class="sxs-lookup"><span data-stu-id="4db78-106">The major type is always **MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="4db78-107">Подтип может быть любым из следующих.</span><span class="sxs-lookup"><span data-stu-id="4db78-107">The subtype can be any of the following.</span></span>



| <span data-ttu-id="4db78-108">Идентификатор GUID</span><span class="sxs-lookup"><span data-stu-id="4db78-108">GUID</span></span>                                             | <span data-ttu-id="4db78-109">Описание</span><span class="sxs-lookup"><span data-stu-id="4db78-109">Description</span></span>                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4db78-110">**\_ \_ \_ Транспорт BDA MPEG2 для подтипа ксдатаформат \_**</span><span class="sxs-lookup"><span data-stu-id="4db78-110">**KSDATAFORMAT\_SUBTYPE\_BDA\_MPEG2\_TRANSPORT**</span></span> | <span data-ttu-id="4db78-111">Транспортный поток из фильтра устройств на основе широковещательной архитектуры драйверов (BDA).</span><span class="sxs-lookup"><span data-stu-id="4db78-111">Transport stream from a Broadcast Driver Architecture (BDA) device filter.</span></span> <span data-ttu-id="4db78-112">Демультиплексор MPEG-2 обрабатывает этот подтип одинаково для **медиасубтипеного \_ \_ транспорта MPEG2**.</span><span class="sxs-lookup"><span data-stu-id="4db78-112">The MPEG-2 demultiplexer treats this subtype identically to **MEDIASUBTYPE\_MPEG2\_TRANSPORT**.</span></span>                                |
| <span data-ttu-id="4db78-113">**\_Программа медиасубтипе MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="4db78-113">**MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span>                 | <span data-ttu-id="4db78-114">Поток программы</span><span class="sxs-lookup"><span data-stu-id="4db78-114">Program stream</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="4db78-115">**\_Транспорт медиасубтипе MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="4db78-115">**MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span>               | <span data-ttu-id="4db78-116">Транспортный поток (TS) с 188-байтными пакетами</span><span class="sxs-lookup"><span data-stu-id="4db78-116">Transport stream (TS), with 188-byte packets</span></span>                                                                                                                                                              |
| <span data-ttu-id="4db78-117">**\_ \_ Шаг транспорта медиасубтипе \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="4db78-117">**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**</span></span>       | <span data-ttu-id="4db78-118">Транспортный поток с "пошаговыми" пакетами.</span><span class="sxs-lookup"><span data-stu-id="4db78-118">Transport stream with "strided" packets.</span></span> <span data-ttu-id="4db78-119">Этот подтип указывает, что пакеты служб терминалов могут быть дополнены дополнительными байтами.</span><span class="sxs-lookup"><span data-stu-id="4db78-119">This subtype indicates that the TS packets may be padded with extra bytes.</span></span> <span data-ttu-id="4db78-120">Дополнительные сведения см. в разделе параметр [**\_ \_ транспорта MPEG2**](mpeg2-transport-stride.md).</span><span class="sxs-lookup"><span data-stu-id="4db78-120">For more information, see [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> |



 

<span data-ttu-id="4db78-121">Для транспортных транспортных пакетов **( \_ \_ \_ Шаг с медиасубтипеом для транспорта MPEG2**) каждый пример носителя должен содержать целое число транспортных пакетов, как описано в разделе [**\_ транспорт MPEG2 \_ stride**](mpeg2-transport-stride.md).</span><span class="sxs-lookup"><span data-stu-id="4db78-121">For strided transport packets (**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**), each media sample must contain an integral number of transport packets, as described in [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> <span data-ttu-id="4db78-122">Для всех остальных типов входных данных нет ограничений на границы выборки; отдельные пакеты могут охватывать границы выборки.</span><span class="sxs-lookup"><span data-stu-id="4db78-122">For all other input types, there are no restrictions on sample boundaries; individual packets can span sample boundaries.</span></span>

### <a name="output-types"></a><span data-ttu-id="4db78-123">Типы вывода</span><span class="sxs-lookup"><span data-stu-id="4db78-123">Output Types</span></span>

<span data-ttu-id="4db78-124">Демультиплексор MPEG-2 не проверяет типы выходных данных. нисходящий фильтр отвечает за анализ данных, получаемых от демультиплексора.</span><span class="sxs-lookup"><span data-stu-id="4db78-124">The MPEG-2 Demultiplexer does not validate output types; the downstream filter is responsible for parsing the data it receives from the demultiplexer.</span></span> <span data-ttu-id="4db78-125">Однако следующие типы обычно принимаются нисходящими фильтрами в качестве выходных данных от демультиплексора.</span><span class="sxs-lookup"><span data-stu-id="4db78-125">However, the following types are commonly accepted by downstream filters as output from the demultiplexer.</span></span>

### <a name="mpeg-2-sections"></a><span data-ttu-id="4db78-126">Разделы MPEG-2</span><span class="sxs-lookup"><span data-stu-id="4db78-126">MPEG-2 Sections</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4db78-127">Основной тип</span><span class="sxs-lookup"><span data-stu-id="4db78-127">Major Type</span></span></td>
<td><span data-ttu-id="4db78-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span><span class="sxs-lookup"><span data-stu-id="4db78-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4db78-129">Subtype</span><span class="sxs-lookup"><span data-stu-id="4db78-129">Subtype</span></span></td>
<td><span data-ttu-id="4db78-130">Любое из следующих:</span><span class="sxs-lookup"><span data-stu-id="4db78-130">Any of the following:</span></span><br/>
<ul>
<li><span data-ttu-id="4db78-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: сведения о службе ATSC.</span><span class="sxs-lookup"><span data-stu-id="4db78-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: ATSC Service Information.</span></span></li>
<li><span data-ttu-id="4db78-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: сведения о службе DVB.</span><span class="sxs-lookup"><span data-stu-id="4db78-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: DVB Service Information.</span></span></li>
<li><span data-ttu-id="4db78-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: сведения о службе Digital ШИРОКОВЕЩАНИЯ (ISDB) для интегрированных служб.</span><span class="sxs-lookup"><span data-stu-id="4db78-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: Integrated Services Digital Broadcasting (ISDB) Service Information.</span></span></li>
<li><span data-ttu-id="4db78-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: данные раздела MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="4db78-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: MPEG-2 section data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4db78-135">Тип формата</span><span class="sxs-lookup"><span data-stu-id="4db78-135">Format Type</span></span></td>
<td><span data-ttu-id="4db78-136">Нет</span><span class="sxs-lookup"><span data-stu-id="4db78-136">None</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="mpeg-2-video"></a><span data-ttu-id="4db78-137">Видео MPEG-2</span><span class="sxs-lookup"><span data-stu-id="4db78-137">MPEG-2 Video</span></span>



|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="4db78-138">Основной тип</span><span class="sxs-lookup"><span data-stu-id="4db78-138">Major type</span></span>       | <span data-ttu-id="4db78-139">**\_Видео MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="4db78-139">**MEDIATYPE\_Video**</span></span>                     |
| <span data-ttu-id="4db78-140">Subtype</span><span class="sxs-lookup"><span data-stu-id="4db78-140">Subtype</span></span>          | <span data-ttu-id="4db78-141">**\_Видео медиасубтипе MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="4db78-141">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           |
| <span data-ttu-id="4db78-142">Тип формата</span><span class="sxs-lookup"><span data-stu-id="4db78-142">Format Type</span></span>      | <span data-ttu-id="4db78-143">**ФОРМАТ \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="4db78-143">**FORMAT\_MPEG2Video**</span></span>                   |
| <span data-ttu-id="4db78-144">Структура формата</span><span class="sxs-lookup"><span data-stu-id="4db78-144">Format Structure</span></span> | [<span data-ttu-id="4db78-145">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="4db78-145">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a><span data-ttu-id="4db78-146">Звук MPEG-2</span><span class="sxs-lookup"><span data-stu-id="4db78-146">MPEG-2 Audio</span></span>



|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="4db78-147">Основной тип</span><span class="sxs-lookup"><span data-stu-id="4db78-147">Major type</span></span>       | <span data-ttu-id="4db78-148">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="4db78-148">**MEDIATYPE\_Audio**</span></span>                 |
| <span data-ttu-id="4db78-149">Subtype</span><span class="sxs-lookup"><span data-stu-id="4db78-149">Subtype</span></span>          | <span data-ttu-id="4db78-150">**МЕДИАСУБТИПЕ \_ MPEG2 \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="4db78-150">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>       |
| <span data-ttu-id="4db78-151">Тип формата</span><span class="sxs-lookup"><span data-stu-id="4db78-151">Format Type</span></span>      | <span data-ttu-id="4db78-152">**ФОРМАТ \_ вавеформатекс**</span><span class="sxs-lookup"><span data-stu-id="4db78-152">**FORMAT\_WaveFormatEx**</span></span>             |
| <span data-ttu-id="4db78-153">Структура формата</span><span class="sxs-lookup"><span data-stu-id="4db78-153">Format Structure</span></span> | <span data-ttu-id="4db78-154">[**вавеформатекс**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4db78-154">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4db78-155">См. также</span><span class="sxs-lookup"><span data-stu-id="4db78-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4db78-156">Типы мультимедиа MPEG-2</span><span class="sxs-lookup"><span data-stu-id="4db78-156">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
