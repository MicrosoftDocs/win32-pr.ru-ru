---
description: В следующих таблицах перечислены идентификаторы CLSID для категорий фильтров DirectShow.
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: Фильтровать категории
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4ccb9443c405abcbd0b9afbd406d6faf2558a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416444"
---
# <a name="filter-categories"></a><span data-ttu-id="6fe21-103">Фильтровать категории</span><span class="sxs-lookup"><span data-stu-id="6fe21-103">Filter Categories</span></span>

<span data-ttu-id="6fe21-104">В следующих таблицах перечислены идентификаторы CLSID для категорий фильтров DirectShow.</span><span class="sxs-lookup"><span data-stu-id="6fe21-104">The following tables list the CLSIDs for the DirectShow filter categories.</span></span>

-   [<span data-ttu-id="6fe21-105">Категории фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="6fe21-105">DirectShow Filter Categories</span></span>](#directshow-filter-categories)
-   [<span data-ttu-id="6fe21-106">Другие категории фильтров</span><span class="sxs-lookup"><span data-stu-id="6fe21-106">Other Filter Categories</span></span>](#other-filter-categories)
-   [<span data-ttu-id="6fe21-107">Meta-Категория фильтра DirectShow</span><span class="sxs-lookup"><span data-stu-id="6fe21-107">DirectShow Filter Meta-Category</span></span>](#directshow-filter-meta-category)
-   [<span data-ttu-id="6fe21-108">Категории DMO</span><span class="sxs-lookup"><span data-stu-id="6fe21-108">DMO Categories</span></span>](#dmo-categories)
-   [<span data-ttu-id="6fe21-109">См. также</span><span class="sxs-lookup"><span data-stu-id="6fe21-109">Related topics</span></span>](#related-topics)

## <a name="directshow-filter-categories"></a><span data-ttu-id="6fe21-110">Категории фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="6fe21-110">DirectShow Filter Categories</span></span>

<span data-ttu-id="6fe21-111">Перечисленные здесь категории перечисляются с помощью модуля [сопоставления фильтров](filter-mapper.md).</span><span class="sxs-lookup"><span data-stu-id="6fe21-111">The categories listed here are enumerated by the [Filter Mapper](filter-mapper.md).</span></span> <span data-ttu-id="6fe21-112">Однако по умолчанию средство сопоставления фильтров не учитывает категории с \_ \_ недоступностью и не использует их \_ .</span><span class="sxs-lookup"><span data-stu-id="6fe21-112">By default, however, the Filter Mapper ignores categories with merits of MERIT\_DO\_NOT\_USE or less.</span></span> <span data-ttu-id="6fe21-113">Дополнительные сведения см. в разделе [**IFilterMapper2:: енумматчингфилтерс**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters).</span><span class="sxs-lookup"><span data-stu-id="6fe21-113">For more information, see [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters).</span></span> <span data-ttu-id="6fe21-114">Все перечисленные здесь категории также можно перечислить с помощью [перечислителя системных устройств](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="6fe21-114">All of the categories listed here can also be enumerated with the [System Device Enumerator](system-device-enumerator.md).</span></span>

<span data-ttu-id="6fe21-115">Следующие категории объявляются в UUID. h.</span><span class="sxs-lookup"><span data-stu-id="6fe21-115">The following categories are declared in Uuids.h.</span></span> <span data-ttu-id="6fe21-116">Включите заголовочный файл DShow. h.</span><span class="sxs-lookup"><span data-stu-id="6fe21-116">Include the header file Dshow.h.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6fe21-117">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="6fe21-117">Friendly Name</span></span></th>
<th><span data-ttu-id="6fe21-118">CLSID</span><span class="sxs-lookup"><span data-stu-id="6fe21-118">CLSID</span></span></th>
<th><span data-ttu-id="6fe21-119">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="6fe21-119">Merit</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6fe21-120">Источники записи звука</span><span class="sxs-lookup"><span data-stu-id="6fe21-120">Audio Capture Sources</span></span></td>
<td><span data-ttu-id="6fe21-121"><strong>CLSID_AudioInputDeviceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-121"><strong>CLSID_AudioInputDeviceCategory</strong></span></span></td>
<td><span data-ttu-id="6fe21-122"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-122"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fe21-123">Звуковые компрессоры</span><span class="sxs-lookup"><span data-stu-id="6fe21-123">Audio Compressors</span></span></td>
<td><span data-ttu-id="6fe21-124"><strong>CLSID_AudioCompressorCategory</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-124"><strong>CLSID_AudioCompressorCategory</strong></span></span></td>
<td><span data-ttu-id="6fe21-125"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-125"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fe21-126">Модули подготовки звука</span><span class="sxs-lookup"><span data-stu-id="6fe21-126">Audio Renderers</span></span></td>
<td><span data-ttu-id="6fe21-127"><strong>CLSID_AudioRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-127"><strong>CLSID_AudioRendererCategory</strong></span></span></td>
<td><span data-ttu-id="6fe21-128"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-128"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fe21-129">Фильтры управления устройствами</span><span class="sxs-lookup"><span data-stu-id="6fe21-129">Device Control Filters</span></span></td>
<td><span data-ttu-id="6fe21-130"><strong>CLSID_DeviceControlCategory</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-130"><strong>CLSID_DeviceControlCategory</strong></span></span></td>
<td><span data-ttu-id="6fe21-131"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-131"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fe21-132">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="6fe21-132">DirectShow Filters</span></span></td>
<td><span data-ttu-id="6fe21-133"><strong>CLSID_LegacyAmFilterCategory</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-133"><strong>CLSID_LegacyAmFilterCategory</strong></span></span></td>
<td><span data-ttu-id="6fe21-134"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-134"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fe21-135">Внешние модули подготовки отчетов</span><span class="sxs-lookup"><span data-stu-id="6fe21-135">External Renderers</span></span></td>
<td><span data-ttu-id="6fe21-136"><strong>CLSID_TransmitCategory</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-136"><strong>CLSID_TransmitCategory</strong></span></span></td>
<td><span data-ttu-id="6fe21-137"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-137"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fe21-138">Модули подготовки MIDI</span><span class="sxs-lookup"><span data-stu-id="6fe21-138">Midi Renderers</span></span></td>
<td><span data-ttu-id="6fe21-139"><strong>CLSID_MidiRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-139"><strong>CLSID_MidiRendererCategory</strong></span></span></td>
<td><span data-ttu-id="6fe21-140"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-140"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fe21-141">Источники видеозаписи</span><span class="sxs-lookup"><span data-stu-id="6fe21-141">Video Capture Sources</span></span></td>
<td><span data-ttu-id="6fe21-142"><strong>CLSID_VideoInputDeviceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-142"><strong>CLSID_VideoInputDeviceCategory</strong></span></span></td>
<td><span data-ttu-id="6fe21-143"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-143"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fe21-144">Видео программы сжатия</span><span class="sxs-lookup"><span data-stu-id="6fe21-144">Video Compressors</span></span></td>
<td><span data-ttu-id="6fe21-145"><strong>CLSID_VideoCompressorCategory</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-145"><strong>CLSID_VideoCompressorCategory</strong></span></span></td>
<td><span data-ttu-id="6fe21-146"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-146"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fe21-147">Устройства распаковки WDM Stream</span><span class="sxs-lookup"><span data-stu-id="6fe21-147">WDM Stream Decompression Devices</span></span></td>
<td><span data-ttu-id="6fe21-148"><strong>CLSID_DVDHWDecodersCategory</strong>
</span><span class="sxs-lookup"><span data-stu-id="6fe21-148"><strong>CLSID_DVDHWDecodersCategory</strong>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="6fe21-149">В этой категории содержатся аппаратные декодеры DVD.</span><span class="sxs-lookup"><span data-stu-id="6fe21-149">This category contains hardware DVD decoders.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="6fe21-150"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-150"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fe21-151">Устройства захвата WDM Streaming</span><span class="sxs-lookup"><span data-stu-id="6fe21-151">WDM Streaming Capture Devices</span></span></td>
<td><span data-ttu-id="6fe21-152"><strong>AM_KSCATEGORY_CAPTURE</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-152"><strong>AM_KSCATEGORY_CAPTURE</strong></span></span></td>
<td><span data-ttu-id="6fe21-153"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-153"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fe21-154">Устройства микширования WDM Streaming</span><span class="sxs-lookup"><span data-stu-id="6fe21-154">WDM Streaming Crossbar Devices</span></span></td>
<td><span data-ttu-id="6fe21-155"><strong>AM_KSCATEGORY_CROSSBAR</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-155"><strong>AM_KSCATEGORY_CROSSBAR</strong></span></span></td>
<td><span data-ttu-id="6fe21-156"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-156"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fe21-157">Устройства отрисовки WDM Streaming</span><span class="sxs-lookup"><span data-stu-id="6fe21-157">WDM Streaming Rendering Devices</span></span></td>
<td><span data-ttu-id="6fe21-158"><strong>AM_KSCATEGORY_RENDER</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-158"><strong>AM_KSCATEGORY_RENDER</strong></span></span></td>
<td><span data-ttu-id="6fe21-159"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-159"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fe21-160">Устройства tee/разделитель WDM Streaming</span><span class="sxs-lookup"><span data-stu-id="6fe21-160">WDM Streaming Tee/Splitter Devices</span></span></td>
<td><span data-ttu-id="6fe21-161"><strong>AM_KSCATEGORY_SPLITTER</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-161"><strong>AM_KSCATEGORY_SPLITTER</strong></span></span></td>
<td><span data-ttu-id="6fe21-162"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-162"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fe21-163">Аудиоустройства потоковой передачи WDM Streaming</span><span class="sxs-lookup"><span data-stu-id="6fe21-163">WDM Streaming TV Audio Devices</span></span></td>
<td><span data-ttu-id="6fe21-164"><strong>AM_KSCATEGORY_TVAUDIO</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-164"><strong>AM_KSCATEGORY_TVAUDIO</strong></span></span></td>
<td><span data-ttu-id="6fe21-165"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-165"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fe21-166">Устройства ТВ-тюнера WDM Streaming</span><span class="sxs-lookup"><span data-stu-id="6fe21-166">WDM Streaming TV Tuner Devices</span></span></td>
<td><span data-ttu-id="6fe21-167"><strong>AM_KSCATEGORY_TVTUNER</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-167"><strong>AM_KSCATEGORY_TVTUNER</strong></span></span></td>
<td><span data-ttu-id="6fe21-168"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-168"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fe21-169">ВБИ кодеки WDM Streaming</span><span class="sxs-lookup"><span data-stu-id="6fe21-169">WDM Streaming VBI Codecs</span></span></td>
<td><span data-ttu-id="6fe21-170"><strong>AM_KSCATEGORY_VBICODEC</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-170"><strong>AM_KSCATEGORY_VBICODEC</strong></span></span></td>
<td><span data-ttu-id="6fe21-171"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="6fe21-171"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6fe21-172">Следующие категории объявляются в файле заголовка KS. h.</span><span class="sxs-lookup"><span data-stu-id="6fe21-172">The following categories are declared in the header file Ks.h.</span></span>



| <span data-ttu-id="6fe21-173">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="6fe21-173">Friendly Name</span></span>                          | <span data-ttu-id="6fe21-174">CLSID</span><span class="sxs-lookup"><span data-stu-id="6fe21-174">CLSID</span></span>                                   | <span data-ttu-id="6fe21-175">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="6fe21-175">Merit</span></span>                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| <span data-ttu-id="6fe21-176">Преобразования связи WDM Streaming</span><span class="sxs-lookup"><span data-stu-id="6fe21-176">WDM Streaming Communication Transforms</span></span> | <span data-ttu-id="6fe21-177">**КСКАТЕГОРИ \_ коммуникатионстрансформ**</span><span class="sxs-lookup"><span data-stu-id="6fe21-177">**KSCATEGORY\_COMMUNICATIONSTRANSFORM**</span></span> | <span data-ttu-id="6fe21-178">**\_ \_ не \_ использовать**</span><span class="sxs-lookup"><span data-stu-id="6fe21-178">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="6fe21-179">Преобразования данных потоковой передачи WDM</span><span class="sxs-lookup"><span data-stu-id="6fe21-179">WDM Streaming Data Transforms</span></span>          | <span data-ttu-id="6fe21-180">**\_Преобразование кскатегори**</span><span class="sxs-lookup"><span data-stu-id="6fe21-180">**KSCATEGORY\_DATATRANSFORM**</span></span>           | <span data-ttu-id="6fe21-181">**\_ \_ не \_ использовать**</span><span class="sxs-lookup"><span data-stu-id="6fe21-181">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="6fe21-182">Преобразования интерфейса потоковой передачи WDM</span><span class="sxs-lookup"><span data-stu-id="6fe21-182">WDM Streaming Interface Transforms</span></span>     | <span data-ttu-id="6fe21-183">**КСКАТЕГОРИ \_ интерфацетрансформ**</span><span class="sxs-lookup"><span data-stu-id="6fe21-183">**KSCATEGORY\_INTERFACETRANSFORM**</span></span>      | <span data-ttu-id="6fe21-184">**\_ \_ не \_ использовать**</span><span class="sxs-lookup"><span data-stu-id="6fe21-184">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="6fe21-185">Устройства микшера потоковой передачи WDM</span><span class="sxs-lookup"><span data-stu-id="6fe21-185">WDM Streaming Mixer Devices</span></span>            | <span data-ttu-id="6fe21-186">**\_микшер кскатегори**</span><span class="sxs-lookup"><span data-stu-id="6fe21-186">**KSCATEGORY\_MIXER**</span></span>                   | <span data-ttu-id="6fe21-187">**\_ \_ не \_ использовать**</span><span class="sxs-lookup"><span data-stu-id="6fe21-187">**MERIT\_DO\_NOT\_USE**</span></span> |



 

<span data-ttu-id="6fe21-188">Следующие категории объявляются в файле заголовка Бдамедиа. h.</span><span class="sxs-lookup"><span data-stu-id="6fe21-188">The following categories are declared in the header file Bdamedia.h.</span></span> <span data-ttu-id="6fe21-189">Включите следующие файлы заголовков: KS. h, ксмедиа. h и бдамедиа. h.</span><span class="sxs-lookup"><span data-stu-id="6fe21-189">Include the following header files: ks.h, ksmedia.h, and bdamedia.h.</span></span>



| <span data-ttu-id="6fe21-190">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="6fe21-190">Friendly Name</span></span>                       | <span data-ttu-id="6fe21-191">CLSID</span><span class="sxs-lookup"><span data-stu-id="6fe21-191">CLSID</span></span>                                       | <span data-ttu-id="6fe21-192">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="6fe21-192">Merit</span></span>                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| <span data-ttu-id="6fe21-193">BDA сетевые поставщики</span><span class="sxs-lookup"><span data-stu-id="6fe21-193">BDA Network Providers</span></span>               | <span data-ttu-id="6fe21-194">**\_ \_ поставщик сети BDA \_ кскатегори**</span><span class="sxs-lookup"><span data-stu-id="6fe21-194">**KSCATEGORY\_BDA\_NETWORK\_PROVIDER**</span></span>      | <span data-ttu-id="6fe21-195">**неуспешный \_ режим**</span><span class="sxs-lookup"><span data-stu-id="6fe21-195">**MERIT\_NORMAL**</span></span>       |
| <span data-ttu-id="6fe21-196">Компоненты приемника BDA</span><span class="sxs-lookup"><span data-stu-id="6fe21-196">BDA Receiver Components</span></span>             | <span data-ttu-id="6fe21-197">**\_ \_ компонент приемника BDA кскатегори \_**</span><span class="sxs-lookup"><span data-stu-id="6fe21-197">**KSCATEGORY\_BDA\_RECEIVER\_COMPONENT**</span></span>    | <span data-ttu-id="6fe21-198">**\_ \_ не \_ использовать**</span><span class="sxs-lookup"><span data-stu-id="6fe21-198">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="6fe21-199">Фильтры визуализации BDA</span><span class="sxs-lookup"><span data-stu-id="6fe21-199">BDA Rendering Filters</span></span>               | <span data-ttu-id="6fe21-200">**\_приемник IP-адресов кскатегори \_**</span><span class="sxs-lookup"><span data-stu-id="6fe21-200">**KSCATEGORY\_IP\_SINK**</span></span>                    | <span data-ttu-id="6fe21-201">**\_ \_ не \_ использовать**</span><span class="sxs-lookup"><span data-stu-id="6fe21-201">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="6fe21-202">BDA фильтры источников</span><span class="sxs-lookup"><span data-stu-id="6fe21-202">BDA Source Filters</span></span>                  | <span data-ttu-id="6fe21-203">**КСКАТЕГОРИ \_ BDA \_ Network \_ тюнер**</span><span class="sxs-lookup"><span data-stu-id="6fe21-203">**KSCATEGORY\_BDA\_NETWORK\_TUNER**</span></span>         | <span data-ttu-id="6fe21-204">**\_ \_ не \_ использовать**</span><span class="sxs-lookup"><span data-stu-id="6fe21-204">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="6fe21-205">Средства подготовки отчетов для передачи данных BDA</span><span class="sxs-lookup"><span data-stu-id="6fe21-205">BDA Transport Information Renderers</span></span> | <span data-ttu-id="6fe21-206">**\_ \_ сведения о транспорте кскатегори BDA \_**</span><span class="sxs-lookup"><span data-stu-id="6fe21-206">**KSCATEGORY\_BDA\_TRANSPORT\_INFORMATION**</span></span> | <span data-ttu-id="6fe21-207">**неуспешный \_ режим**</span><span class="sxs-lookup"><span data-stu-id="6fe21-207">**MERIT\_NORMAL**</span></span>       |



 

> [!Note]  
> <span data-ttu-id="6fe21-208">Декодеры регистрируются в категории "фильтры DirectShow" (CLSID \_ легациамфилтеркатегори).</span><span class="sxs-lookup"><span data-stu-id="6fe21-208">Decoders are registered under the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory).</span></span>

 

## <a name="other-filter-categories"></a><span data-ttu-id="6fe21-209">Другие категории фильтров</span><span class="sxs-lookup"><span data-stu-id="6fe21-209">Other Filter Categories</span></span>

<span data-ttu-id="6fe21-210">Перечисленные здесь категории можно перечислить с помощью перечислителя системных устройств, но они не видны для модуля сопоставления фильтров и не используются [интеллектуальным соединением](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="6fe21-210">The categories listed here can be enumerated with the System Device Enumerator, but are not visible to the Filter Mapper and are not used by [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="6fe21-211">Следующие категории объявляются в файле заголовка Кедит. h.</span><span class="sxs-lookup"><span data-stu-id="6fe21-211">The following categories are declared in the header file Qedit.h.</span></span>



| <span data-ttu-id="6fe21-212">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="6fe21-212">Friendly Name</span></span>            | <span data-ttu-id="6fe21-213">клид</span><span class="sxs-lookup"><span data-stu-id="6fe21-213">CLID</span></span>                             | <span data-ttu-id="6fe21-214">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="6fe21-214">Merit</span></span>                   |
|--------------------------|----------------------------------|-------------------------|
| <span data-ttu-id="6fe21-215">Видеоэффекты (1 вход)</span><span class="sxs-lookup"><span data-stu-id="6fe21-215">Video Effects (1 input)</span></span>  | <span data-ttu-id="6fe21-216">**\_VIDEOEFFECTS1CATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="6fe21-216">**CLSID\_VideoEffects1Category**</span></span> | <span data-ttu-id="6fe21-217">**\_ \_ не \_ использовать**</span><span class="sxs-lookup"><span data-stu-id="6fe21-217">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="6fe21-218">Видеоэффекты (2 входа)</span><span class="sxs-lookup"><span data-stu-id="6fe21-218">Video Effects (2 inputs)</span></span> | <span data-ttu-id="6fe21-219">**\_VIDEOEFFECTS2CATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="6fe21-219">**CLSID\_VideoEffects2Category**</span></span> | <span data-ttu-id="6fe21-220">**\_ \_ не \_ использовать**</span><span class="sxs-lookup"><span data-stu-id="6fe21-220">**MERIT\_DO\_NOT\_USE**</span></span> |



 

<span data-ttu-id="6fe21-221">Эти категории содержат видеоэффекты и переходы для [служб редактирования DirectShow](directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="6fe21-221">These categories contain video effects and transitions for [DirectShow Editing Services](directshow-editing-services.md):</span></span>

-   <span data-ttu-id="6fe21-222">"Видеоролики (1 Ввод)" содержит видеоэффекты.</span><span class="sxs-lookup"><span data-stu-id="6fe21-222">"Video Effects (1 input)" contains video effects.</span></span>
-   <span data-ttu-id="6fe21-223">"Видеоэффекты (2 входные данные)" содержат видеопереходы.</span><span class="sxs-lookup"><span data-stu-id="6fe21-223">"Video Effects (2 input)" contains video transitions.</span></span>

<span data-ttu-id="6fe21-224">Дополнительные сведения см. в разделе [перечисление эффектов и переходов](enumerating-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="6fe21-224">For more information, see [Enumerating Effects and Transitions](enumerating-effects-and-transitions.md).</span></span>

<span data-ttu-id="6fe21-225">Следующие категории объявляются в файле заголовков UUID. h.</span><span class="sxs-lookup"><span data-stu-id="6fe21-225">The following categories are declared in the header file Uuids.h.</span></span> <span data-ttu-id="6fe21-226">Включите заголовочный файл DShow. h.</span><span class="sxs-lookup"><span data-stu-id="6fe21-226">Include the header file Dshow.h.</span></span>



| <span data-ttu-id="6fe21-227">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="6fe21-227">Friendly Name</span></span>       | <span data-ttu-id="6fe21-228">клид</span><span class="sxs-lookup"><span data-stu-id="6fe21-228">CLID</span></span>                                | <span data-ttu-id="6fe21-229">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="6fe21-229">Merit</span></span>                   |
|---------------------|-------------------------------------|-------------------------|
| <span data-ttu-id="6fe21-230">Кодировщики Енкапи</span><span class="sxs-lookup"><span data-stu-id="6fe21-230">EncAPI Encoders</span></span>     | <span data-ttu-id="6fe21-231">**\_МЕДИАЕНКОДЕРКАТЕГОРИ CLSID**</span><span class="sxs-lookup"><span data-stu-id="6fe21-231">**CLSID\_MediaEncoderCategory**</span></span>     | <span data-ttu-id="6fe21-232">**\_ \_ не \_ использовать**</span><span class="sxs-lookup"><span data-stu-id="6fe21-232">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="6fe21-233">Мультиплексоры Енкапи</span><span class="sxs-lookup"><span data-stu-id="6fe21-233">EncAPI Multiplexers</span></span> | <span data-ttu-id="6fe21-234">**\_МЕДИАМУЛТИПЛЕКСЕРКАТЕГОРИ CLSID**</span><span class="sxs-lookup"><span data-stu-id="6fe21-234">**CLSID\_MediaMultiplexerCategory**</span></span> | <span data-ttu-id="6fe21-235">**\_ \_ не \_ использовать**</span><span class="sxs-lookup"><span data-stu-id="6fe21-235">**MERIT\_DO\_NOT\_USE**</span></span> |



 

## <a name="directshow-filter-meta-category"></a><span data-ttu-id="6fe21-236">Meta-Category фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="6fe21-236">DirectShow Filter Meta-Category</span></span>



| <span data-ttu-id="6fe21-237">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="6fe21-237">Friendly Name</span></span>                 | <span data-ttu-id="6fe21-238">CLSID</span><span class="sxs-lookup"><span data-stu-id="6fe21-238">CLSID</span></span>                            | <span data-ttu-id="6fe21-239">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="6fe21-239">Merit</span></span>          |
|-------------------------------|----------------------------------|----------------|
| <span data-ttu-id="6fe21-240">Категории фильтра ActiveMovie</span><span class="sxs-lookup"><span data-stu-id="6fe21-240">ActiveMovie Filter Categories</span></span> | <span data-ttu-id="6fe21-241">**\_АКТИВЕМОВИЕКАТЕГОРИЕС CLSID**</span><span class="sxs-lookup"><span data-stu-id="6fe21-241">**CLSID\_ActiveMovieCategories**</span></span> | <span data-ttu-id="6fe21-242">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="6fe21-242">Not applicable</span></span> |



 

<span data-ttu-id="6fe21-243">Эта мета-категория содержит список категорий фильтров.</span><span class="sxs-lookup"><span data-stu-id="6fe21-243">This meta-category contains a list of filter categories.</span></span> <span data-ttu-id="6fe21-244">Если Категория фильтра не отображается в этом списке, то средство [сопоставления фильтров](filter-mapper.md) игнорирует категорию, что означает, что фильтр недоступен для [интеллектуального соединения](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="6fe21-244">If a filter category does not appear within this list, the [Filter Mapper](filter-mapper.md) ignores the category, which means the filter is not available for [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="6fe21-245">Чтобы перечислить список категорий фильтров, вызовите [**икреатедевенум:: креатеклассенумератор**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) со значением CLSID \_ активемовиекатегориес.</span><span class="sxs-lookup"><span data-stu-id="6fe21-245">To enumerate the list of filter categories, call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the value CLSID\_ActiveMovieCategories.</span></span> <span data-ttu-id="6fe21-246">Моникеры, возвращаемые этим методом, поддерживают следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6fe21-246">The monikers returned by this method support the following properties.</span></span>



| <span data-ttu-id="6fe21-247">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="6fe21-247">Property Name</span></span>  | <span data-ttu-id="6fe21-248">Описание</span><span class="sxs-lookup"><span data-stu-id="6fe21-248">Description</span></span>                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fe21-249">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6fe21-249">"FriendlyName"</span></span> | <span data-ttu-id="6fe21-250">Имя категории (VT \_ BSTR).</span><span class="sxs-lookup"><span data-stu-id="6fe21-250">Category name (VT\_BSTR).</span></span>                                                              |
| <span data-ttu-id="6fe21-251">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="6fe21-251">"Merit"</span></span>        | <span data-ttu-id="6fe21-252">Категория заслуживает (VT \_ i4).</span><span class="sxs-lookup"><span data-stu-id="6fe21-252">Category merit (VT\_I4).</span></span> <span data-ttu-id="6fe21-253">Если это свойство отсутствует, **\_ \_ \_ обработайте его как недоступное**.</span><span class="sxs-lookup"><span data-stu-id="6fe21-253">If this property is absent, treat as **MERIT\_DO\_NOT\_USE**.</span></span> |
| <span data-ttu-id="6fe21-254">ЭТОМУ</span><span class="sxs-lookup"><span data-stu-id="6fe21-254">"CLSID"</span></span>        | <span data-ttu-id="6fe21-255">CLSID категории (VT \_ BSTR).</span><span class="sxs-lookup"><span data-stu-id="6fe21-255">Category CLSID (VT\_BSTR).</span></span>                                                             |



 

<span data-ttu-id="6fe21-256">Чтобы добавить новую категорию фильтра в этот список, вызовите метод [**IFilterMapper2:: креатекатегори**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).</span><span class="sxs-lookup"><span data-stu-id="6fe21-256">To add a new filter category to this list, call [**IFilterMapper2::CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).</span></span>

## <a name="dmo-categories"></a><span data-ttu-id="6fe21-257">Категории DMO</span><span class="sxs-lookup"><span data-stu-id="6fe21-257">DMO Categories</span></span>

<span data-ttu-id="6fe21-258">Объекты мультимедиа DirectX (дмос) используют другой механизм перечисления из фильтров DirectShow.</span><span class="sxs-lookup"><span data-stu-id="6fe21-258">DirectX Media Objects (DMOs) use a different enumeration mechanism from DirectShow filters.</span></span> <span data-ttu-id="6fe21-259">Дополнительные сведения см. [в разделе Регистрация DMO](registering-a-dmo.md).</span><span class="sxs-lookup"><span data-stu-id="6fe21-259">For more information, see [Registering a DMO](registering-a-dmo.md).</span></span> <span data-ttu-id="6fe21-260">Однако можно использовать перечислитель системных устройств для перечисления категорий DMO.</span><span class="sxs-lookup"><span data-stu-id="6fe21-260">However, you can use the System Device Enumerator to enumerate DMO categories.</span></span> <span data-ttu-id="6fe21-261">Моникеры привязываются к [фильтру оболочки DMO](dmo-wrapper-filter.md) и автоматически инициализируют фильтр с помощью DMO.</span><span class="sxs-lookup"><span data-stu-id="6fe21-261">The monikers bind to the [DMO Wrapper Filter](dmo-wrapper-filter.md) and automatically initialize the filter with the DMO.</span></span>

<span data-ttu-id="6fe21-262">Кроме того, некоторые категории DMO сопоставляются с категориями фильтров DirectShow в целях интеллектуального подключения:</span><span class="sxs-lookup"><span data-stu-id="6fe21-262">In addition, some of the DMO categories are mapped to DirectShow filter categories for the purposes of intelligent connect:</span></span>



| <span data-ttu-id="6fe21-263">Категория DMO</span><span class="sxs-lookup"><span data-stu-id="6fe21-263">DMO Category</span></span>                    | <span data-ttu-id="6fe21-264">Эквивалент DirectShow</span><span class="sxs-lookup"><span data-stu-id="6fe21-264">DirectShow Equivalent</span></span>              |
|---------------------------------|------------------------------------|
| <span data-ttu-id="6fe21-265">**\_КОДИРОВЩИК дмокатегори Audio \_**</span><span class="sxs-lookup"><span data-stu-id="6fe21-265">**DMOCATEGORY\_AUDIO\_ENCODER**</span></span> | <span data-ttu-id="6fe21-266">**\_АУДИОКОМПРЕССОРКАТЕГОРИ CLSID**</span><span class="sxs-lookup"><span data-stu-id="6fe21-266">**CLSID\_AudioCompressorCategory**</span></span> |
| <span data-ttu-id="6fe21-267">**\_декодер дмокатегори Audio \_**</span><span class="sxs-lookup"><span data-stu-id="6fe21-267">**DMOCATEGORY\_AUDIO\_DECODER**</span></span> | <span data-ttu-id="6fe21-268">**\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID**</span><span class="sxs-lookup"><span data-stu-id="6fe21-268">**CLSID\_LegacyAmFilterCategory**</span></span>  |
| <span data-ttu-id="6fe21-269">**\_кодировщик видео \_ дмокатегори**</span><span class="sxs-lookup"><span data-stu-id="6fe21-269">**DMOCATEGORY\_VIDEO\_ENCODER**</span></span> | <span data-ttu-id="6fe21-270">**\_ВИДЕОКОМПРЕССОРКАТЕГОРИ CLSID**</span><span class="sxs-lookup"><span data-stu-id="6fe21-270">**CLSID\_VideoCompressorCategory**</span></span> |
| <span data-ttu-id="6fe21-271">**\_декодер видео \_ дмокатегори**</span><span class="sxs-lookup"><span data-stu-id="6fe21-271">**DMOCATEGORY\_VIDEO\_DECODER**</span></span> | <span data-ttu-id="6fe21-272">**\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID**</span><span class="sxs-lookup"><span data-stu-id="6fe21-272">**CLSID\_LegacyAmFilterCategory**</span></span>  |



 

<span data-ttu-id="6fe21-273">Обратите внимание, что категории эффектов видео и звуковых эффектов не сопоставлены ни с одной из категорий DirectShow.</span><span class="sxs-lookup"><span data-stu-id="6fe21-273">Note that the video effect and audio effect categories are not mapped to any DirectShow categories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fe21-274">См. также</span><span class="sxs-lookup"><span data-stu-id="6fe21-274">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fe21-275">Константы и идентификаторы GUID</span><span class="sxs-lookup"><span data-stu-id="6fe21-275">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="6fe21-276">Перечисление устройств и фильтров</span><span class="sxs-lookup"><span data-stu-id="6fe21-276">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="6fe21-277">Интеллектуальное подключение</span><span class="sxs-lookup"><span data-stu-id="6fe21-277">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> <dt>

[<span data-ttu-id="6fe21-278">Структура разделов реестра</span><span class="sxs-lookup"><span data-stu-id="6fe21-278">Layout of the Registry Keys</span></span>](layout-of-the-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="6fe21-279">Использование средства сопоставления фильтров</span><span class="sxs-lookup"><span data-stu-id="6fe21-279">Using the Filter Mapper</span></span>](using-the-filter-mapper.md)
</dt> <dt>

[<span data-ttu-id="6fe21-280">Использование перечислителя системных устройств</span><span class="sxs-lookup"><span data-stu-id="6fe21-280">Using the System Device Enumerator</span></span>](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




