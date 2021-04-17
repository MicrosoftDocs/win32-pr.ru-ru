---
description: Следующие константы свойств устройств должны поддерживаться всеми интерфейсами интерфейса Ивиаитем, IWiaItem2 и Ивиадрвитем, если в их описаниях не указано иное.
ms.assetid: ef48313e-4df4-4ccd-a085-f714100885a7
title: Стандартные константы свойств элементов WIA (Виадеф. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPA_ACCESS_RIGHTS
- WIA_IPA_APP_COLOR_MAPPING
- WIA_IPA_BITS_PER_CHANNEL
- WIA_IPA_BUFFER_SIZE
- WIA_IPA_BYTES_PER_LINE
- WIA_IPA_CHANNELS_PER_PIXEL
- WIA_IPA_COLOR_PROFILE
- WIA_IPA_COMPRESSION
- WIA_IPA_DATATYPE
- WIA_IPA_DEPTH
- WIA_IPA_FILENAME_EXTENSION
- WIA_IPA_FORMAT
- WIA_IPA_FULL_ITEM_NAME
- WIA_IPA_GAMMA_CURVES
- WIA_IPA_ICM_PROFILE_NAME
- WIA_IPA_ITEM_CATEGORY
- WIA_IPA_ITEM_FLAGS
- WIA_IPA_ITEM_NAME
- WIA_IPA_ITEM_SIZE
- WIA_IPA_ITEM_TIME
- WIA_IPA_ITEMS_STORED
- WIA_IPA_MIN_BUFFER_SIZE
- WIA_IPA_NUMBER_OF_LINES
- WIA_IPA_PIXELS_PER_LINE
- WIA_IPA_PLANAR
- WIA_IPA_PREFERRED_FORMAT
- WIA_IPA_PROP_STREAM_COMPAT_ID
- WIA_IPA_RAW_BITS_PER_CHANNEL
- WIA_IPA_REGION_TYPE
- WIA_IPA_SUPPRESS_PROPERTY_PAGE
- WIA_IPA_TYMED
- WIA_IPA_UPLOAD_ITEM_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: d36a390256c6a9d183caa0f9231d2a92035d83da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701588"
---
# <a name="common-wia-item-property-constants"></a>Стандартные константы свойств элементов WIA

Следующие константы свойств устройств должны поддерживаться всеми интерфейсами интерфейса [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem), [**IWiaItem2**](-wia-iwiaitem2.md) и [ивиадрвитем](https://msdn.microsoft.com/library/ms793976.aspx) , если в их описаниях не указано иное.

Префикс "WIA \_ IPA \_ " указывает свойство элемента для всех устройств и является соглашением об именовании, используемым в C/C++. Для сценариев эти константы используют префикс "Picture" и являются частью перечислимого типа [виаитемпропертид](-wia-wiaitempropertyid.md) . Соответствующее имя элемента из этого перечисления скриптов отображается в круглых скобках рядом с именем константы C/C++ в следующем списке.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Константа/значение</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ACCESS_RIGHTS"></span><span id="wia_ipa_access_rights"></span><dl> <dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>пиктуреакцессригхтс</dt> </dl></td>
<td style="text-align: left;">Этот флаг управляет доступом к элементу, а также тем, удаляется ли элемент.<br/> Требуется для всех элементов WIA 2,0.<br/> Тип: <strong>VT_I4</strong>; Чтение, запись или чтение (только для чтения) в зависимости от способности элемента изменять права доступа; Допустимые значения: WIA_PROP_FLAG<br/> В следующей таблице приведены пять флагов, допустимых для этого свойства.<br/> 
<table>
<thead>
<tr class="header">
<th>Право доступа</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_ITEM_READ</td>
<td>Элемент имеет доступ только для чтения.</td>
</tr>
<tr class="even">
<td>WIA_ITEM_WRITE</td>
<td>Элемент имеет доступ только на запись.</td>
</tr>
<tr class="odd">
<td>WIA_ITEM_CAN_BE_DELETED</td>
<td>Элемент имеет доступ только на удаление.</td>
</tr>
<tr class="even">
<td>WIA_ITEM_RD</td>
<td>WIA_ITEM_READ | WIA_ITEM_CAN_BE_DELETED</td>
</tr>
<tr class="odd">
<td>WIA_ITEM_RWD</td>
<td>WIA_ITEM_READ | WIA_ITEM_WRITE | WIA_ITEM_CAN_BE_DELETED</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_APP_COLOR_MAPPING"></span><span id="wia_ipa_app_color_mapping"></span><dl> <dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>пиктуреаппколормаппинг</dt> </dl></td>
<td style="text-align: left;"><p>Это свойство зарезервировано для будущего использования и не реализовано в данный момент.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BITS_PER_CHANNEL"></span><span id="wia_ipa_bits_per_channel"></span><dl> <dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>пиктуребитсперчаннел</dt> </dl></td>
<td style="text-align: left;"><p>Содержит количество бит на канал для образа. Минидривер создает и поддерживает это свойство.</p>
<p>Требуется для всех элементов изображений, доступных для получения или сохранения в WIA 2,0.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_BUFFER_SIZE"></span><span id="wia_ipa_buffer_size"></span><dl> <dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>пиктуребуфферсизе</dt> </dl></td>
<td style="text-align: left;"><p>Содержит размер буфера (в байтах), используемого при переносе данных. Минидривер создает и поддерживает это свойство.</p>
<p>Приложение может прочитать это свойство, чтобы определить размер буфера, заданный драйвером для передачи данных. Служба WIA также считывает это свойство для выделения памяти для минидривер во время обмена данными.</p>
<p>Необязательно для всех элементов WIA 2,0, поддерживающих перемещение.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<div class="alert">
<blockquote>
[!Note]<br />
Свойство <strong>WIA_IPA_BUFFER_SIZE</strong> содержит минимальный объем данных, которые приложение может запросить в любое заданное время. Чем больше размер буфера, тем больше будет запросов к устройству. Это может заставить устройство работать медленнее и не реагировать, может снизить общую производительность системы и может потреблять чрезмерные ресурсы. Слишком малые размеры буфера могут снизить производительность при переносе данных, так как они требуют большого количества небольших запросов. Выберите приемлемый размер буфера, учитывая типичный размер запроса данных на устройстве и балансировку количества запросов по размеру этих запросов.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BYTES_PER_LINE"></span><span id="wia_ipa_bytes_per_line"></span><dl> <dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>пиктуребитесперлине</dt> </dl></td>
<td style="text-align: left;"><p>Содержит число байтов в одной строке просмотра изображения. Минидривер создает и поддерживает это свойство.</p>
<p>Необязательно для всех элементов WIA 2,0.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_CHANNELS_PER_PIXEL"></span><span id="wia_ipa_channels_per_pixel"></span><dl> <dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>пиктуречаннелсперпиксел</dt> </dl></td>
<td style="text-align: left;"><p>Содержит число каналов на пиксель для образа. Минидривер создает и поддерживает это свойство.</p>
<p>Требуется для всех элементов изображений, доступных для получения или сохранения в WIA 2,0.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_COLOR_PROFILE"></span><span id="wia_ipa_color_profile"></span><dl> <dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>пиктуреколорпрофиле</dt> </dl></td>
<td style="text-align: left;"><p>Это свойство зарезервировано для будущего использования и не реализовано в данный момент.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_COMPRESSION"></span><span id="wia_ipa_compression"></span><dl> <dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>пиктурекомпрессион</dt> </dl></td>
<td style="text-align: left;"><p>Содержит текущий используемый тип сжатия. Минидривер создает и поддерживает это свойство.</p>
<p>Приложение считывает это свойство для определения типа сжатия изображения или задает это свойство для настройки параметра сжатия.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>В следующей таблице приведены константы, допустимые для этого свойства. Символ <strong>V</strong> указывает, что константа поддерживается только в Windows Vista и более поздних версиях. (Он доступен только через интерфейс <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .)</p>

<table>
<thead>
<tr class="header">
<th>Тип сжатия</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_COMPRESSION_NONE</td>
<td>Без сжатия. Дополнительные сведения см. в разделе <strong>Примечание</strong> .</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_AUTO</td>
<td>Режим автоматического сжатия. Дополнительные сведения см. в разделе <strong>Примечание</strong> .</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_BI_RLE4</td>
<td>Сжатие RLE4</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_BI_RLE8</td>
<td>Сжатие RLE8</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_G3</td>
<td>Сжатие группы 3</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_G4</td>
<td>Сжатие группы 4</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_JPEG</td>
<td>Сжатие JPEG.</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_JBIG<strong>V</strong></td>
<td>Сжатие ЖБИГ.</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_JPEG2K<strong>V</strong></td>
<td>Сжатие JPEG 2000.</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_PNG<strong>V</strong></td>
<td>Сжатие PNG.</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
<p>[!Note]</p>
<p>Если это свойство имеет значение WIA_COMPRESSION_NONE, а WIA_IPA_FORMAT — либо WiaImgFmt_PDFA, либо WiaImgFmt_XPS; затем WIA_COMPRESSION_NONE означает, что режим сжатия не определен, и сканер должен выбрать режим.</p>
<p>WIA_COMPRESSION_AUTO — это новое значение свойства, определенное для свойства WIA_IPA_COMPRESSION. Это значение допустимо для всех программируемых элементов источника данных образа, включая планшет и устройство подачи. Если это значение поддерживается мини-драйвером WIA, клиент приложения WIA может задать WIA_IPA_COMPRESSION, чтобы включить автоматическое обнаружение режима сжатия на устройстве. WIA_COMPRESSION_AUTO могут работать с и без полного автоцвета (WIA_DATA_AUTO и WIA_DEPTH_AUTO).</p>
<p>WIA_COMPRESSION_AUTO наиболее полезна при переносе форматов файлов, поддерживающих несколько типов данных и битовых глубин, таких как WiaImgFmt_RAW. Дополнительные сведения о переносе форматов файлов см. в разделе WIA_IPA_FORMAT в этой таблице.</p>
<p>Опитонал поддержка WIA_COMPRESSION_AUTO для мини-драйвера WIA. Если он поддерживается, Мини-драйвер WIA не должен задавать его в качестве значения по умолчанию для WIA_IPA_COMPRESSION; Это значение может быть задано только для приложения WIA.</p>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_DATATYPE"></span><span id="wia_ipa_datatype"></span><dl> <dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>пиктуредататипе</dt> </dl></td>
<td style="text-align: left;"><p>Содержит текущий параметр типа данных для устройства. Минидривер создает и поддерживает это свойство.</p>
<p>Приложение считывает это свойство для определения типа данных изображения. Приложение записывает это свойство, чтобы задать текущий тип данных изображения, которое будет передано.</p>
<p>Это свойство является обязательным для всех элементов WIA 2,0. Он должен быть доступен для чтения и записи для всех элементов с включенным приобретением WIA 2,0 и доступен только для чтения для элементов хранилища WIA 2,0.</p>
<p>Тип: <strong>VT_I4</strong>; Доступ для операционных систем, предшествующих Windows Vista: это свойство доступно только для чтения для камер и чтения и записи для сканеров. Доступ для Windows Vista и более поздних версий: это свойство предназначено только для чтения для WIA_CATEGORY_FOLDER и WIA_CATEGORY_FINISHED_FILE элементов, а для чтения и записи для всех остальных категорий элементов WIA 2,0. Допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Следующая таблица содержит шесть констант, допустимых с параметром, если <strong>WIA_IPA_FORMAT</strong> не имеет значение WiaImgFmt_RAW.</p>

<table>
<thead>
<tr class="header">
<th>Тип данных</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DATA_AUTO</td>
<td>Допустимы для всех программируемых элементов источника данных образа, включая планшет и устройство подачи. Если это значение поддерживается мини-драйвером WIA, клиент приложения WIA может задать WIA_IPA_DATATYPE, чтобы включить автоматическое обнаружение цветов на устройстве. Если задан параметр WIA_DATA_AUTO, Мини-драйвер WIA должен обновить WIA_IPA_DEPTH того же элемента на WIA_DEPTH_AUTO (это значение должно быть поддерживаемым, если устройство поддерживает автоматический цвет).<br/> Это необязательное значение, но оно требуется, если для WIA_IPA_DEPTH поддерживается WIA_DEPTH_AUTO.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_COLOR</td>
<td>Данные сканирования имеют цвет красного, зеленого, синего (RGB). Полный формат цвета описывается с помощью следующих свойств WIA: <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong><br/> <strong>WIA_IPA_BITS_PER_CHANNEL</strong><br/> <strong>WIA_IPA_PLANAR</strong><br/> <strong>WIA_IPA_PIXELS_PER_LINE</strong><br/> <strong>WIA_IPA_BYTES_PER_LINE</strong><br/> <strong>WIA_IPA_NUMBER_OF_LINES</strong><br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_COLOR_DITHER</td>
<td>То же, что и WIA_DATA_COLOR за исключением того, что данные отменяются с помощью выбранного шаблона сглаживания.</td>
</tr>
<tr class="even">
<td>WIA_DATA_COLOR_THRESHOLD</td>
<td>То же, что и WIA_DATA_COLOR за исключением того, что при сканировании данных используется пороговое значение. Значения цвета в <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> значения преобразуются в полную яркость; цвета под этим значением преобразуются в черный.</td>
</tr>
<tr class="odd">
<td>WIA_DATA_DITHER</td>
<td>Данные сканирования отменяются с помощью выбранного шаблона сглаживания.</td>
</tr>
<tr class="even">
<td>WIA_DATA_GRAYSCALE</td>
<td>Данные сканирования представляют интенсивность. Палитра представляет собой фиксированную серую шкалу с одинаковыми пробелами с глубиной, заданной свойством <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> .</td>
</tr>
<tr class="odd">
<td>WIA_DATA_THRESHOLD</td>
<td>Пороговое значение — один бит на пиксель с черно-белыми данными. Данные из текущего значения <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> преобразуются в белые; данные с этим значением преобразуются в черный.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Свойство <strong>WIA_IPA_DATATYPE</strong> также используется для описания типа перемещения необработанных данных, который будет использоваться, когда приложение задает WiaImgFmt_RAW. Драйвер должен задать свойству <strong>WIA_IPA_DATATYPE</strong> список допустимых значений, из которых приложение может выбрать один из них.</p>
<p>Если для устройства можно задать только одно значение, создайте тип <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> и поместите в него допустимое значение.</p>
<p>Проверьте свойство <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> , чтобы определить битовую глубину. Это свойство обычно содержит одно значение для камер.</p>
<p>В следующей таблице перечислены константы, допустимые с <strong>WIA_IPA_DATATYPE</strong> , если <strong>WIA_IPA_FORMAT</strong> имеет значение WiaImgFmt_RAW.</p>

<table>
<thead>
<tr class="header">
<th>Тип данных</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DATA_GRAYSCALE</td>
<td>Данные сканирования представляют интенсивность. Палитра представляет собой фиксированные оттенки серого с глубиной, заданной свойством <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> . Значение <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> должно быть равно 1.</td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_BGR</td>
<td>Данные сканирования находятся в BGR (синий-зеленый-красный) колорспаце. Полный формат цвета описывается с помощью Фолловингвиапропертиес: <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a><br/> <a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a><br/> <a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a><br/> <a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a><br/> <a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a><br/> Значение <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> должно быть равно 3.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_CMY</td>
<td>Данные сканирования находятся в голубом/пурпурном цвете (КМИ) колорспаце. Полный формат цвета описывается с помощью тех же свойств WIA, что и в WIA_DATA_RAW_BGR. Значение <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> должно быть равно 3.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_CMYK</td>
<td>Данные сканирования находятся в цвете голубой-пурпурный-желтый-черный (CMYK) колорспаце. Полный формат цвета описывается с помощью тех же свойств WIA, что и в WIA_DATA_RAW_BGR. Значение <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> должно быть равно 4.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_RGB</td>
<td>Данные сканирования находятся в колорспацее красный-зеленый-синий цвет (RGB). Полный формат цвета описывается с помощью тех же свойств WIA, что и в WIA_DATA_RAW_BGR. Значение <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> должно быть равно 3.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_YUV</td>
<td>Данные сканирования находятся в цвете «светимость» — «разница» — «Красная разница» (YUV) колорспаце. Полный формат цвета описывается с помощью тех же свойств WIA, что и в WIA_DATA_RAW_BGR. Значение <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> должно быть равно 3.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_YUVK</td>
<td>Данные сканирования находятся в цвете «светимость-синий» — «Красная разница» — «черная» (ЮВК) колорспаце. Полный формат цвета описывается с помощью тех же свойств WIA, что и в WIA_DATA_RAW_BGR. Значение <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> должно быть равно 4.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_DEPTH"></span><span id="wia_ipa_depth"></span><dl> <dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>пиктуредепс</dt> </dl></td>
<td style="text-align: left;"><p>WIA_IPA_DEPTH содержит значение битовой глубины изображения. Минидривер создает и поддерживает это свойство. Приложение считывает это свойство, чтобы определить битовую глубину изображения. Приложение может также иметь возможность задать для этого значения нужную глубину.</p>
<p>Если для устройства можно задать только одно значение, создайте тип <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> и поместите в него допустимое значение.</p>
<p>Это свойство является обязательным для всех элементов WIA 2,0. Он должен быть доступен для чтения и записи для всех элементов с включенным приобретением WIA 2,0 и доступен только для чтения для элементов хранилища WIA 2,0.</p>
<p>Тип: <strong>VT_I4</strong>; Доступ для операционных систем, предшествующих Windows Vista: чтение и запись; Доступ для Windows Vista и более поздних версий: это свойство предназначено только для чтения для WIA_CATEGORY_FOLDER и WIA_CATEGORY_FINISHED_FILE элементов, а для чтения и записи для всех остальных категорий элементов WIA 2,0. Допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>WIA_DEPTH_AUTO определяется как 0 бит на пиксель, а это новое значение свойства, определенное для WIA_IPA_DEPTH. Это значение допустимо для всех программируемых элементов источника данных образа, включая планшет и устройство подачи. Если WIA_DEPTH_AUTO поддерживается мини-драйвером WIA, клиент приложения WIA может установить WIA_IPA_DEPTH это значение, чтобы включить автоматическое обнаружение цветов на устройстве. Если WIA_DEPTH_AUTO установлен, Мини-драйвер WIA должен обновить WIA_IPA_DATATYPE на том же элементе, чтобы WIA_DATA_AUTO (это значение должно быть поддерживаемым, если устройство поддерживает автоматический цвет).</p>
<p>WIA_DEPTH_AUTO является необязательным значением, но оно становится обязательным, если для WIA_IPA_DATATYPE поддерживается WIA_DATA_AUTO.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FILENAME_EXTENSION"></span><span id="wia_ipa_filename_extension"></span><dl> <dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>пиктурефиленамикстенсион</dt> </dl></td>
<td style="text-align: left;"><p>Содержит расширение имени файла для определенного формата файла. Минидривер создает и поддерживает это свойство.</p>
<p>Необязательно для всех элементов WIA 2,0, поддерживающих перемещение.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Драйвер обновляет это свойство, чтобы отразить текущее значение свойства <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> .</p>
<p>Например, если <strong>WIA_IPA_FORMAT</strong> WiaImgFmt_JPEG, <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> должен иметь значение <strong>JPG</strong>. Если <strong>WIA_IPA_FORMAT</strong> WiaImgFmt_BMP, то WIA_IPA_FILENAME_EXTENSION должно быть BMP.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Расширение имени файла не включает точку.
</blockquote>
</div>
<div>
 
</div>
<p>Это свойство рекомендуется использовать для драйверов, которые поддерживают стандартные форматы и необходимы для драйверов, реализующих определенные пользователем форматы. Он информирует приложение о правильном расширении имени файла для использования во время перемещения файлов в частном формате. Например, если корпорация A. Datum создала драйвер WIA, который передавал файл в новом формате, компания может указать расширение &quot; ADC &quot; . Это позволяет приложениям передавать данные в этом формате в файл и создавать имя файла, например <em>MyFile. ADC</em>, которое полезно для других пользователей, которые понимают новое расширение.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_FORMAT"></span><span id="wia_ipa_format"></span><dl> <dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>пиктуреформат</dt> </dl></td>
<td style="text-align: left;"><p>Содержит текущий формат изображения, которое будет передано.</p>
<p>Приложение считывает это свойство, чтобы определить формат получаемого изображения. Приложение записывает это свойство для задания формата. Это свойство зависит от свойства <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> . Минидривер создает и поддерживает это свойство.</p>
<p>Если для устройства можно задать только одно значение, создайте тип <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> и поместите в него допустимое значение.</p>
<p>Тип: <strong>CLSID</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>В следующей таблице перечислены константы, допустимые для этого свойства. Звездочка * указывает, что константа не поддерживается в Windows Vista. (Он доступен только через интерфейс <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>ивиаитем</strong></a> .) Двойная звездочка * * указывает, что константа не поддерживается в Windows Server 2003 или Windows Vista. Символ <strong>V</strong> указывает, что константа поддерживается только в Windows Vista и более поздних версиях. (Он доступен только через интерфейс <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .)</p>

<table>
<thead>
<tr class="header">
<th>Формат</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaAudFmt_AIFF</td>
<td>Формат аудиозаписей в формате AIFF</td>
</tr>
<tr class="even">
<td>WiaAudFmt_MP3</td>
<td>Формат аудио в формате MP3</td>
</tr>
<tr class="odd">
<td>WiaAudFmt_WAV</td>
<td>Звуковой формат WAV</td>
</tr>
<tr class="even">
<td>WiaAudFmt_WMA</td>
<td>Аудио формат WMA</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_ASF * *</td>
<td>Формат видео ASF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_AVI * *</td>
<td>Видео в формате AVI</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_BMP</td>
<td>Точечный рисунок Windows с файлом заголовка</td>
</tr>
<tr class="even">
<td>WiaImgFmt_CIFF *</td>
<td>Формат файла изображения камеры</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_DPOF</td>
<td>Формат печати ДПОФ</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EMF</td>
<td>Расширенный метафайл Windows</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_EXEC</td>
<td>Исполняемый файл</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EXIF</td>
<td>Формат файла Exchange</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_FLASHPIX</td>
<td>Формат Флашпикс</td>
</tr>
<tr class="even">
<td>WiaImgFmt_GIF</td>
<td>Формат изображения GIF</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_HTML</td>
<td>Формат HTML</td>
</tr>
<tr class="even">
<td>WiaImgFmt_ICO</td>
<td>Формат файла значка Windows</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JBIG<strong>V</strong></td>
<td>Совместный формат группы экспертов по обработке изображений (ЖБИГ).</td>
</tr>
<tr class="even">
<td>WiaImgFmt_JPEG</td>
<td>Сжатый формат JPEG</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JPEG2K</td>
<td>Сжатый формат JPEG 2000</td>
</tr>
<tr class="even">
<td>WiaImgFmt_JPEG2KX</td>
<td>Сжатый формат JPEG 2000</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_MEMORYBMP</td>
<td>Точечный рисунок Windows без файла заголовка</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PDFA<strong>V</strong></td>
<td>Формат PDF/A (ISO/CD 19005-1).</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_MPG * *</td>
<td>Формат видео MPEG</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PHOTOCD</td>
<td>Формат файлов еастман Kodak</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_PICT</td>
<td>Формат файлов Apple</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PNG</td>
<td>Формат W3C PNG</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_RAW</td>
<td>Формат RAW только для передачи данных</td>
</tr>
<tr class="even">
<td>WiaImgFmt_RAWRGB</td>
<td>Необработанный формат RGB</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_RTF</td>
<td>Формат форматированного текста</td>
</tr>
<tr class="even">
<td>WiaImgFmt_SCRIPT</td>
<td>Файл скрипта</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_TIFF</td>
<td>TIFF (Tag Image File Format)</td>
</tr>
<tr class="even">
<td>WiaImgFmt_TXT</td>
<td>текстовый файл</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_UNICODE16</td>
<td>16-разрядная кодировка Юникода</td>
</tr>
<tr class="even">
<td>WiaImgFmt_WMF</td>
<td>Метафайл Windows</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_XML</td>
<td>XML-файл</td>
</tr>
<tr class="even">
<td>WiaImgFmt_XPS<strong>V</strong></td>
<td>Формат пакета XPS</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
Если это свойство имеет значение WiaImgFmt_PDFA или WiaImgFmt_XPS, а WIA_IPA_COMPRESSION — WIA_COMPRESSION_NONE; Второе значение означает, что режим сжатия не определен, и сканер должен выбрать режим.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FULL_ITEM_NAME"></span><span id="wia_ipa_full_item_name"></span><dl> <dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>пиктурефуллитемнаме</dt> </dl></td>
<td style="text-align: left;"><p>Содержит полное имя элемента (имя элемента вместе со сведениями о пути). Полное имя элемента совпадает с параметром <em>бстрфуллитемнаме</em> функции служебной программы <a href="https://msdn.microsoft.com/library/ms794649.aspx">виаскреатедрвитем</a> Service. Приложение считывает это свойство, чтобы определить, какой элемент в настоящий момент используется, и где этот элемент находится в дереве элементов. Каждый элемент должен иметь уникальное имя. Приложения обычно используют полное имя элемента для поиска элементов в дереве элементов. Служба WIA создает и поддерживает это свойство.</p>
<p>Требуется для всех элементов WIA 2,0.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_GAMMA_CURVES"></span><span id="wia_ipa_gamma_curves"></span><dl> <dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>пиктурегаммакурвес</dt> </dl></td>
<td style="text-align: left;"><p>Это свойство зарезервировано для будущего использования и в настоящее время не реализовано.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ICM_PROFILE_NAME"></span><span id="wia_ipa_icm_profile_name"></span><dl> <dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>пиктуреикмпрофиленаме</dt> </dl></td>
<td style="text-align: left;"><p>Содержит имя профиля ICM, необходимое для правильного декодирования изображения. Приложение считывает это свойство, чтобы определить профиль ICM, используемый при обработке изображения. Служба WIA создает и поддерживает это свойство на основе записи Икмпрофилес в файле установки драйвера.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_CATEGORY"></span><span id="wia_ipa_item_category"></span><dl> <dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>пиктуреитемкатегори</dt> </dl></td>
<td style="text-align: left;"><p>Поддерживается только в Windows Vista и более поздних версиях.</p>
<p>Элементы WIA 2,0 группируются по категориям, которые определяют способ обработки или использования <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> . Например, если элемент представляет устройство подачи, то приложение должно содержать необходимые свойства устройства подачи документов и действовать как устройство подачи документов. Если элемент представляет готовый файл, то приложение WIA 2,0 должно обрабатывать его таким образом, предполагая, что данные статичны и расположены на устройстве. (Правила для каждого элемента будут определены в отдельных документах спецификации.)</p>
<p>Требуется для всех элементов WIA 2,0.</p>
<p>Тип: <strong>VT_CLSID</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-wia2-itemcategoryguids.md"><strong>идентификаторы GUID категорий элементов</strong></a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_FLAGS"></span><span id="wia_ipa_item_flags"></span><dl> <dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>пиктуреитемфлагс</dt> </dl></td>
<td style="text-align: left;"><p>Содержит описательные флаги для элемента WIA. Флаги элемента те же, что и в параметре <em>лобжектфлагс</em> функции служебной программы <a href="https://msdn.microsoft.com/library/ms794649.aspx">виаскреатедрвитем</a> Service. Служба WIA создает и поддерживает это свойство.</p>
<p>Приложение считывает это свойство для определения значений флагов элемента.</p>
<p>Тип: <strong>VT_I4</strong> доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>В следующей таблице приведены флаги, допустимые для этого свойства. Звездочка * означает, что флаг не поддерживается в Windows Vista или более поздней версии. (Он доступен только через интерфейс <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>ивиаитем</strong></a> .) Двойная звездочка * * означает, что флаг не поддерживается в Windows Server 2003 или Windows Vista или более поздней версии. Символ <strong>V</strong> означает, что флаг поддерживается только в Windows Vista и более поздних версиях. (Он доступен только через интерфейс <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .)</p>

<table>
<thead>
<tr class="header">
<th>Flag</th>
<th>Определение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Виаитемтипеанализе *</td>
<td>Этот элемент поддерживает метод <strong>ивиаитем:: анализеитем</strong> (описан в документации по Platform SDK). Этот элемент также поддерживает автоматическое создание дочерних элементов. Эта возможность полезна для обнаружения региона или декомпозиции страниц.</td>
</tr>
<tr class="even">
<td>виаитемтипеаудио</td>
<td>Этот элемент поддерживает аудио. Этот флаг допустим только для элементов, для которых также установлен флаг <strong>виаитемтипефиле</strong> .</td>
</tr>
<tr class="odd">
<td>Виаитемтипебурст *</td>
<td>Только для папок. Этот флаг указывает, что изображения в этой папке были собраны в непрерывной последовательности времени.</td>
</tr>
<tr class="even">
<td>виаитемтипеделетед</td>
<td>Этот элемент помечен для удаления, этот элемент был удален, этот элемент не существует или содержимое этого элемента недопустимо.</td>
</tr>
<tr class="odd">
<td>Виаитемтипедокумент<strong>V</strong></td>
<td>Этот элемент является файлом документа в одном из форматов документов, содержащихся в свойстве <strong>WIA_IPA_FORMAT</strong> . (Эти форматы включают в себя файлы, не являющиеся изображениями, такие как txt, htm и doc.)</td>
</tr>
<tr class="even">
<td>виаитемтипедевице</td>
<td>Этот элемент представляет подключенное устройство.</td>
</tr>
<tr class="odd">
<td>виаитемтипедисконнектед</td>
<td>Этот элемент представляет отключенное устройство.</td>
</tr>
<tr class="even">
<td>виаитемтипефиле</td>
<td>Элемент поддерживает передачу файлов.</td>
</tr>
<tr class="odd">
<td>виаитемтипефолдер</td>
<td>Элемент является папкой.</td>
</tr>
<tr class="even">
<td>виаитемтипефри</td>
<td>Элемент не инициализирован или был удален.</td>
</tr>
<tr class="odd">
<td>виаитемтипеженератед</td>
<td>Этот элемент был создан приложением или драйвером.</td>
</tr>
<tr class="even">
<td>Виаитемтипехасаттачментс *</td>
<td>Этот элемент поддерживает вложения и в настоящее время содержит вложения.</td>
</tr>
<tr class="odd">
<td>Виаитемтипехпанорама *</td>
<td>Этот элемент представляет горизонтальный панорамный рисунок. Этот флаг допустим только для элементов, для которых также установлен флаг <strong>виаитемтипефолдер</strong> .</td>
</tr>
<tr class="even">
<td>виаитемтипеимаже</td>
<td>Элемент является файлом изображения. Этот флаг допустим только для элементов, для которых также установлен флаг <strong>виаитемтипефиле</strong> .</td>
</tr>
<tr class="odd">
<td>Виаитемтипепрограммабледатасаурце<strong>V</strong></td>
<td>Элемент является программируемым источником данных и соответствует набору предварительно определенных правил конфигурации, которые основаны на <strong>WIA_IPA_ITEM_CATEGORY</strong>.</td>
</tr>
<tr class="even">
<td>Виаитемтиперут<strong>V</strong></td>
<td>Этот элемент является корневым элементом, который является родительским для всех элементов компонента, поддерживаемых устройством.</td>
</tr>
<tr class="odd">
<td>виаитемтипестораже</td>
<td>Этот флаг указывает дополнительное хранилище для элементов папок. Драйверы WIA определяют свои элементы в терминах изображений и папок. Не существует свойств WIA, описывающих характеристики элемента хранения (например, объем хранилища, скорость записи или тип носителя). Можно добавить свойства, относящиеся к поставщику, которые предоставляют эту информацию. Эти свойства доступны только для приложений или расширений, написанных для их распознавания.</td>
</tr>
<tr class="even">
<td>виаитемтипетрансфер</td>
<td>Этот элемент можно использовать для перемещения данных.</td>
</tr>
<tr class="odd">
<td>виаитемтипетваинкапабилитипасссраугх</td>
<td>Этот тип указывает, что устройство WIA может получать данные о возможности TWAIN на уровне совместимости TWAIN. Если этот тип задан, то все возможности TWAIN, не распознаваемые уровнем совместимости TWAIN, передаются в драйвер Севиа. Это допустимо только для корневого элемента.</td>
</tr>
<tr class="even">
<td>Виаитемтипевидео * *</td>
<td>Этот элемент поддерживает потоковую передачу видео.</td>
</tr>
<tr class="odd">
<td>Виаитемтипевпанорама *</td>
<td>Этот элемент представляет вертикальную панорамную изображение. Этот флаг допустим только для элементов, для которых также установлен флаг <strong>виаитемтипефолдер</strong> .</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Некоторые из этих флагов являются обязательными или необязательными для элементов WIA 2,0 в соответствии с категорией элемента, как показано в этой таблице.</p>

<table>
<thead>
<tr class="header">
<th>Категория элемента</th>
<th>Обязательно</th>
<th>Необязательно</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_CATEGORY_ROOT</td>
<td>Виаитемтиперут Виаитемтипефолдер</td>
<td>Виаитемтипедевице Виаитемтипедисконнектед</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FLATBED</td>
<td>Виаитемтипепрограммабледатасаурце Виаитемтипетрансфер Виаитемтипеимаже Виаитемтипефиле</td>
<td>Виаитемтипефолдер (если поддерживается несколько элементов регионов сканирования, этот флаг необязателен только для корневого элемента WIA_CATEGORY_FLATBED.)</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</td>
<td>Виаитемтипепрограммабледатасаурце Виаитемтипетрансфер Виаитемтипеимаже Виаитемтипефиле</td>
<td>Виаитемтипефолдер (если имеются WIA_CATEGORY_FEEDER_FRONT и WIA_CATEGORY_FEEDER_BACK элементы, этот флаг является необязательным только для корневого элемента WIA_CATEGORY_FEEDER.)</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FILM (корневой)</td>
<td>Виаитемтипепрограммабледатасаурце Виаитемтипетрансфер Виаитемтипеимаже Виаитемтипефиле WiaItemTypeFolder</td>
<td>Нет</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FILM (дочерние элементы)</td>
<td>Виаитемтипепрограммабледатасаурце Виаитемтипетрансфер Виаитемтипеимаже Виаитемтипефиле</td>
<td>Нет</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FOLDER</td>
<td>Виаитемтипестораже Виаитемтипефолдер</td>
<td>виаитемтипеделетед</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FINISHED_FILE</td>
<td>Виаитемтипефиле Виаитемтипетрансфер</td>
<td>Виаитемтипеимаже Виаитемтипеаудио Виаитемтипеделетед</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_NAME"></span><span id="wia_ipa_item_name"></span><dl> <dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>пиктуреитемнаме</dt> </dl></td>
<td style="text-align: left;"><p>Содержит имя элемента. Приложение считывает это свойство, чтобы определить, какой элемент в данный момент используется. Каждый элемент имеет уникальное имя. Служба WIA создает и поддерживает это свойство.</p>
<p>Требуется для всех элементов WIA 2,0.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_SIZE"></span><span id="wia_ipa_item_size"></span><dl> <dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>пиктуреитемсизе</dt> </dl></td>
<td style="text-align: left;"><p>Содержит текущий размер (в байтах) данных, связанных с элементом. Минидривер создает и поддерживает это свойство.</p>
<p>Содержит общий размер передаваемых данных. Если это значение равно нулю, это означает, что минидривер не содержит сведений о точном размере данных. (Это распространено для сжатых данных.) Приложение считывает это значение, чтобы определить размер приобретения перед тем, как оно будет происходить. Служба WIA считывает это свойство для помощи при выделении памяти для передачи данных. Дополнительные сведения см. в разделе <a href="https://msdn.microsoft.com/library/ms792198.aspx">Передача данных в приложение WIA</a> , если свойство имеет значение 0, а тимед настроен для передачи файла, служба WIA не выделяет память для WIA-минидривер.</p>
<p>Требуется для всех элементов WIA 2,0, поддерживающих перемещение.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_TIME"></span><span id="wia_ipa_item_time"></span><dl> <dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>пиктуреитемтиме</dt> </dl></td>
<td style="text-align: left;"><p>Содержит время первоначальной записи образа. Минидривер создает и поддерживает это свойство. Это свойство должно быть представлено в виде вектора из восьми значений <strong>слов</strong> в виде структуры SYSTEMTIME (описывается в документации по Platform SDK).</p>
<p>Необязательно для всех элементов WIA 2,0.</p>
<p>Тип: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong> доступ: только для чтения, записи или чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>пиктуреитемитемссторед</dt> </dl></td>
<td style="text-align: left;"><p>Поддерживается только в Windows Vista и более поздних версиях.</p>
<p>Указывает, сколько элементов хранится в элементе WIA_CATEGORY_FOLDER.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_MIN_BUFFER_SIZE"></span><span id="wia_ipa_min_buffer_size"></span><dl> <dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>пиктуреминбуфферсизе</dt> </dl></td>
<td style="text-align: left;"><p>Указывает минимальный размер буфера, используемого при передаче данных. Если перенос данных выполняется через механизм обратного вызова, значение свойства может быть меньше 64 КБ. Однако если перемещение выполняется в файл, значение свойства равно количеству байтов, необходимых для одновременного перемещения одной страницы данных. Минидривер создает и поддерживает это свойство WIA.</p>
<p>Необязательно для всех элементов WIA 2,0, поддерживающих перемещение.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_NUMBER_OF_LINES"></span><span id="wia_ipa_number_of_lines"></span><dl> <dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>пиктуренумберофлинес</dt> </dl></td>
<td style="text-align: left;"><p>Содержит число строк, содержащихся в изображении (вертикальная высота изображения в пикселях). Минидривер создает и поддерживает это свойство.</p>
<p>Необязательно для всех элементов WIA 2,0.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PIXELS_PER_LINE"></span><span id="wia_ipa_pixels_per_line"></span><dl> <dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>пиктурепикселсперлине</dt> </dl></td>
<td style="text-align: left;"><p>Содержит количество пикселей в каждой строке изображения (ширина изображения в пикселях). Минидривер создает и поддерживает это свойство.</p>
<p>Необязательно для всех элементов WIA 2,0.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PLANAR"></span><span id="wia_ipa_planar"></span><dl> <dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>пиктурепланар</dt> </dl></td>
<td style="text-align: left;"><p>Это свойство не поддерживается в Windows Vista и более поздних версиях.</p>
<p>Содержит параметры упаковки данных изображения. Минидривер создает и поддерживает это свойство.</p>
<p>Приложение считывает это свойство для определения параметров упаковки изображения или задает параметры упаковки текущего изображения.</p>
<p>Тип: <strong>VT_I4</strong>; Доступ: чтение и запись; Допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>. Если для устройства можно задать только одно значение, создайте тип WIA_PROP_LIST и поместите в него допустимое значение.</p>
<p>В следующей таблице приведены две константы, допустимые для этого свойства.</p>

<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Определение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PACKED_PIXEL</td>
<td>Данные изображения находятся в формате упакованных пикселей.</td>
</tr>
<tr class="even">
<td>WIA_PLANAR</td>
<td>Данные изображения имеют плоский формат.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PREFERRED_FORMAT"></span><span id="wia_ipa_preferred_format"></span><dl> <dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>пиктурепреферредформат</dt> </dl></td>
<td style="text-align: left;"><p>Содержит предпочтительный формат для изображений, которые передает этот минидривер. Минидривер создает и поддерживает это свойство.</p>
<p>Требуется для всех элементов WIA 2,0, поддерживающих перемещение.</p>
<p>Тип: <strong>CLSID</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PROP_STREAM_COMPAT_ID"></span><span id="wia_ipa_prop_stream_compat_id"></span><dl> <dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>пиктурепропстреамкомпатид</dt> </dl></td>
<td style="text-align: left;"><p>Указывает CLSID, представляющий набор значений свойств устройства. Если драйвер устройства реализует эту функцию, приложения используют это свойство, чтобы определить, поддерживает ли устройство набор значений.</p>
<p>Тип: <strong>CLSID</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>В следующей таблице приведены 12 констант, допустимых для этого свойства.</p>

<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Определение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaImgFmt_BMP</td>
<td>Точечный рисунок Микрософтвиндовс с файлом заголовка</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EMF</td>
<td>Расширенный метафайл Windows</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_EXIF</td>
<td>Формат файла Exchange</td>
</tr>
<tr class="even">
<td>WiaImgFmt_FLASHPIX</td>
<td>Формат Флашпикс</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_GIF</td>
<td>Формат изображения GIF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_ICO</td>
<td>Формат файла значка Windows</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JPEG</td>
<td>Сжатый формат JPEG</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PHOTOCD</td>
<td>Формат файлов еастман Kodak</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_PNG</td>
<td>Формат W3C PNG</td>
</tr>
<tr class="even">
<td>WiaImgFmt_MEMORYBMP</td>
<td>Точечный рисунок Windows без файла заголовка</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_TIFF</td>
<td>TIFF (Tag Image File Format)</td>
</tr>
<tr class="even">
<td>WiaImgFmt_WMF</td>
<td>Метафайл Windows</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_RAW_BITS_PER_CHANNEL"></span><span id="wia_ipa_raw_bits_per_channel"></span><dl> <dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>пиктуреравбитсперчаннел</dt> </dl></td>
<td style="text-align: left;"><p>Поддерживается только в Windows Vista и более поздних версиях.</p>
<p>Содержит количество битов в каждом канале. Это свойство должно быть представлено в виде вектора, равного количеству БАЙТОВ, так как есть каналы, где первый байт соответствует количеству битов в первом канале, второй байт — к числу битов во втором канале и т. д. Должно быть столько записей, сколько каналов в соответствии с WIA_IPA_CHANNELS_PER_PIXEL. Драйвер задает это свойство, когда приложение переключается на WiaImgFmt_RAW. Для хорошо известных подтипов существует столько же записей, сколько указано в таблице в разделе WIA_IPA_RAW_SUBTYPE.</p>
<p>Тип: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_REGION_TYPE"></span><span id="wia_ipa_region_type"></span><dl> <dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>пиктуререгионтипе</dt> </dl></td>
<td style="text-align: left;"><p>Это свойство зарезервировано для будущего использования и не реализовано в данный момент.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_SUPPRESS_PROPERTY_PAGE"></span><span id="wia_ipa_suppress_property_page"></span><dl> <dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>пиктуресуппресспропертипаже</dt> </dl></td>
<td style="text-align: left;"><p>Указывает, следует ли подавлять Общие страницы свойств для элементов на устройстве.</p>
<p>Это свойство доступно в Windows XP и более поздних версиях.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>В следующей таблице приведены константы, допустимые для этого свойства. Звездочка * указывает, что константа не является допустимой в Windows Vista и более поздних версиях. (Он доступен только через интерфейс <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>ивиаитем</strong></a> .)</p>

<table>
<thead>
<tr class="header">
<th>Константа</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PROPPAGE_CAMERA_ITEM_GENERAL *</td>
<td>Подавляет страницу свойств элемента «общие» для камеры.</td>
</tr>
<tr class="even">
<td>WIA_PROPPAGE_SCANNER_ITEM_GENERAL</td>
<td>Подавляет страницу свойств элемента "Общие" для сканера.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_TYMED"></span><span id="wia_ipa_tymed"></span><dl> <dt><strong>WIA_IPA_TYMED</strong></dt> <dt>пиктуретимед</dt> </dl></td>
<td style="text-align: left;"><p>Это свойство содержит параметр метода перемещения. Минидривер создает и поддерживает это свойство.</p>
<p>Приложение считывает это свойство для определения метода перемещения данных минидривер.</p>
<p>Требуется для всех элементов WIA 2,0, поддерживающих перемещение.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>В следующей таблице приведены константы, допустимые для этого свойства. Звездочка * указывает константы, которые не являются допустимыми в Windows Vista и более поздних версиях. (Они доступны только через интерфейс <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>ивиаитем</strong></a> .)</p>

<table>
<thead>
<tr class="header">
<th>Тип переноса</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TYMED_CALLBACK *</td>
<td>Перенос изображения в память в полосах.</td>
</tr>
<tr class="even">
<td>TYMED_MULTIPAGE_CALLBACK *</td>
<td>Перемещение нескольких образов в память в полосах.</td>
</tr>
<tr class="odd">
<td>TYMED_FILE</td>
<td>Перенос изображения в файл.</td>
</tr>
<tr class="even">
<td>TYMED_MULTIPAGE_FILE</td>
<td>Перенос изображения в файл.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>пиктуреитемуплоадитемсизе</dt> </dl></td>
<td style="text-align: left;"><p>Поддерживается только в Windows Vista и более поздних версиях.</p>
<p>Указывает число байтов для отправки для элемента.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                |
| Header<br/>                   | <dl> <dt>Виадеф. h</dt> </dl> |



 

 




