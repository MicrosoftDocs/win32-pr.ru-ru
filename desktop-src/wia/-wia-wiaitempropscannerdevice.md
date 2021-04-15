---
description: Аппаратные устройства для получения образа Windows (WIA) имеют значения свойств, которые хранятся в реестре Windows.
ms.assetid: 78caa3af-927b-4143-9e88-4b5c918d00a4
title: Константы свойств устройства сканера (Виадеф. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPS_DEVICE_ID
- WIA_DPS_DITHER_PATTERN_DATA
- WIA_DPS_DITHER_SELECT
- WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES
- WIA_DPS_DOCUMENT_HANDLING_SELECT
- WIA_DPS_DOCUMENT_HANDLING_STATUS
- WIA_DPS_ENDORSER_CHARACTERS
- WIA_DPS_ENDORSER_STRING
- WIA_DPS_FILTER_SELECT
- WIA_DPS_GLOBAL_IDENTITY
- WIA_DPS_HORIZONTAL_BED_REGISTRATION
- WIA_DPS_HORIZONTAL_BED_SIZE
- WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MAX_SCAN_TIME
- WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE
- WIA_DPS_OPTICAL_XRES
- WIA_DPS_OPTICAL_YRES
- WIA_DPS_ORIENTATION
- WIA_DPS_PAD_COLOR
- WIA_DPS_PAGE_HEIGHT
- WIA_DPS_PAGE_SIZE
- WIA_DPS_PAGE_WIDTH
- WIA_DPS_PAGES
- WIA_DPS_PLATEN_COLOR
- WIA_DPS_PREVIEW
- WIA_DPS_SCAN_AHEAD_PAGES
- WIA_DPS_SCAN_AVAILABLE_ITEM
- WIA_DPS_SERVICE_ID
- WIA_DPS_SHEET_FEEDER_REGISTRATION
- WIA_DPS_SHOW_PREVIEW_CONTROL
- WIA_DPS_USER_NAME
- WIA_DPS_VERTICAL_BED_REGISTRATION
- WIA_DPS_VERTICAL_BED_SIZE
- WIA_DPS_VERTICAL_SHEET_FEED_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: af50f5d319e368ce2a672c040dc9d23843436121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701586"
---
# <a name="scanner-device-property-constants"></a>Константы свойств устройства сканера

Аппаратные устройства для получения образа Windows (WIA) имеют значения свойств, которые хранятся в реестре Windows. Дополнительные сведения см. в разделе [**общие константы свойств устройства**](-wia-wiaitempropcommondevice.md). Следующие константы свойств устройства со связанными строками относятся к сканерам цифровых изображений.

Префикс "WIA \_ DPS \_ " указывает на свойство устройства для устройств сканера и является соглашением об именовании, используемым в C/C++. Для сценариев эти константы используют префикс "Сканнердевице" и являются частью перечислимого типа [виаитемпропертид](-wia-wiaitempropertyid.md) . Соответствующее имя элемента из этого перечисления скриптов отображается в круглых скобках рядом с именем константы C/C++ в следующем списке.



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
<td style="text-align: left;"><span id="WIA_DPS_DEVICE_ID"></span><span id="wia_dps_device_id"></span><dl> <dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>сканнердевицедевицеид</dt> </dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Это свойство поддерживается только в Windows Vista и более поздних версиях.
</blockquote>
<br/> Содержит уникальный идентификатор экземпляра функции для устройства сканера веб-служб. Этот идентификатор представляет веб-службу на устройстве сканера, с которой взаимодействует мини-драйвер WIA. Никаких предположений о форме этого идентификатора не должно быть. Мини-драйвер WIA создает и поддерживает это свойство. <br/> Приложения WIA могут использовать значение WIA_DPS_DEVICE_ID для поиска, используя API обнаружения функций, объект экземпляра функции, представляющий устройство сканера веб-служб, используемое в текущем сеансе WIA 2,0.<br/> Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_PATTERN_DATA"></span><span id="wia_dps_dither_pattern_data"></span><dl> <dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </dl></td>
<td style="text-align: left;">Зарезервировано, не используйте.<br/> Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_SELECT"></span><span id="wia_dps_dither_select"></span><dl> <dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </dl></td>
<td style="text-align: left;">Зарезервировано, не используйте.<br/> Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES"></span><span id="wia_dps_document_handling_capabilities"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>сканнердевицедокуменсандлингкапабилитиес</dt> </dl></td>
<td style="text-align: left;">Содержит возможности сканера. Минидривер создает и поддерживает это свойство. <br/> Приложение считывает это свойство, чтобы определить, есть ли у сканера планшетный, веб-устройство подачи документов или установленный дуплекс. Это свойство также используется для дальнейшего определения установленных компонентов.<br/> Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> В следующей таблице описаны константы, допустимые только в Windows 7.<br/> 
<table>
<thead>
<tr class="header">
<th>Флаги</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AUTO_SOURCE</td>
<td>В сканере установлен автоматический обработчик документов.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>В следующей таблице описаны константы, допустимые только в Windows 7 и Windows Vista.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Флаги</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ADVANCED_DUP</td>
<td>Устройство поддерживает расширенную конфигурацию дуплексного сканирования. Используйте WIA_IPS_DUPLEX_SETTINGS, чтобы переключаться между использованием базовой и расширенной дуплексных конфигураций.</td>
</tr>
<tr class="even">
<td>DETECT_FILM_TPA</td>
<td>Сканер может определить, когда адаптер прозрачности или пленки готов к сканированию.</td>
</tr>
<tr class="odd">
<td>DETECT_STOR</td>
<td>Средство проверки может обнаруживать наличие документов во внутреннем хранилище.</td>
</tr>
<tr class="even">
<td>FILM_TPA</td>
<td>Сканер оснащен адаптером сканирования прозрачности или пленки.</td>
</tr>
<tr class="odd">
<td>стор</td>
<td>Сканер оснащен внутренним устройством хранения изображений.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>В следующей таблице описаны константы, допустимые в Windows XP и более поздних версиях.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Флаги</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DETECT_FEED</td>
<td>Средство проверки может обнаружить документ в веб-канале.</td>
</tr>
<tr class="even">
<td>DETECT_FLAT</td>
<td>Сканер может обнаружить документ на планшетном Платен.</td>
</tr>
<tr class="odd">
<td>DETECT_SCAN</td>
<td>Средство проверки может обнаружить документ в веб-канале только при сканировании.</td>
</tr>
<tr class="even">
<td>DUP</td>
<td>Сканер имеет дуплексный модуль.</td>
</tr>
<tr class="odd">
<td>КАНАЛ</td>
<td>В сканере установлен автоматический обработчик документов.</td>
</tr>
<tr class="even">
<td>ВЫПУКЛАЯ</td>
<td>Сканер имеет планшетный Платен.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>В следующей таблице описаны константы, допустимые только в Windows XP. Эти значения являются устаревшими для Windows 7 и Windows Vista и не должны использоваться.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Флаги</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DETECT_DUP</td>
<td>Сканер может обнаружить запрос на дуплексное сканирование от пользователя.</td>
</tr>
<tr class="even">
<td>DETECT_DUP_AVAIL</td>
<td>Сканер может определить, когда был установлен дуплекс.</td>
</tr>
<tr class="odd">
<td>DETECT_FEED_AVAIL</td>
<td>Сканер может определить, когда установлен автоматический веб-канал документов.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_dps_document_handling_select"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>сканнердевицедокуменсандлингселект</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство не поддерживается в Windows Vista и более поздних версиях. Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Содержит текущий источник и режим получения сканера. Минидривер создает и поддерживает это свойство.</p>
<p>Приложение считывает это свойство, чтобы определить текущий источник получения сканера или записать это свойство, чтобы задать источник и режим сканера. Кроме того, приложения используют это свойство для включения и отключения функции дуплексного режима.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>В следующей таблице содержится десять констант, допустимых для этого свойства. </p>
<table>
<thead>
<tr class="header">
<th>Флаги</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ФЕЙЕРВЕРК</td>
<td>Сканирование с помощью устройства подачи документов.</td>
</tr>
<tr class="even">
<td>СТЕКЛО</td>
<td>Сканирование с помощью планшета.</td>
</tr>
<tr class="odd">
<td>УСТРОЙСТВА</td>
<td>Сканирование с помощью операций дуплексного устройства.</td>
</tr>
<tr class="even">
<td>AUTO_ADVANCE</td>
<td>Включает автоматическое подача следующего документа после проверки.</td>
</tr>
<tr class="odd">
<td>FRONT_FIRST</td>
<td>Сначала просканируйте передний план документа. Это значение допустимо, если задан дуплекс.</td>
</tr>
<tr class="even">
<td>BACK_FIRST</td>
<td>Сначала просканируйте задний план документа. Это значение допустимо, если задан дуплекс.</td>
</tr>
<tr class="odd">
<td>FRONT_ONLY</td>
<td>Сканирование только на передней панели. Это значение допустимо, если задан дуплекс.</td>
</tr>
<tr class="even">
<td>BACK_ONLY</td>
<td>Проверка только обратного просмотра. Это значение допустимо, если задан дуплекс.</td>
</tr>
<tr class="odd">
<td>NEXT_PAGE</td>
<td>Сканирование следующей страницы документа.</td>
</tr>
<tr class="even">
<td>Предподача</td>
<td>Включить режим предварительного перевода. Предварительное размещение следующего документа во время сканирования.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_STATUS"></span><span id="wia_dps_document_handling_status"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>сканнердевицедокуменсандлингстатус</dt> </dl></td>
<td style="text-align: left;"><p>Содержит текущее состояние установленного сканера, устройства подачи документов или дуплексного устройства. Минидривер создает и поддерживает это свойство.</p>
<p>Приложение считывает это свойство, чтобы определить, готово ли устройство сканера к использованию. Это идеальный способ проверить, находится ли бумага в податчике перед получением изображения.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>В следующей таблице приведены константы, допустимые для этого свойства. Звездочка * означает, что флаг не поддерживается в Windows Vista или более поздней версии. Символ <strong>V</strong> означает, что флаг поддерживается только в Windows Vista и более поздних версиях. </p>
<table>
<thead>
<tr class="header">
<th>Флаги</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FEED_READY</td>
<td>Планшетный объект готов к использованию.</td>
</tr>
<tr class="even">
<td>FLAT_READY</td>
<td>Сканер содержит документ на планшетном Платен.</td>
</tr>
<tr class="odd">
<td>DUP_READY</td>
<td>Дуплексный модуль включен и готов к использованию.</td>
</tr>
<tr class="even">
<td>FLAT_COVER_UP</td>
<td>Плоский испытательный картон.</td>
</tr>
<tr class="odd">
<td>PATH_COVER_UP</td>
<td>Путь к документу охватывается и препятствует правильной работе.</td>
</tr>
<tr class="even">
<td>PAPER_JAM</td>
<td>Документ застрял в податчике документов.</td>
</tr>
<tr class="odd">
<td>FILM_TPA_READY<strong>V</strong></td>
<td>Адаптер прозрачности установлен и готов к использованию.</td>
</tr>
<tr class="even">
<td>STORAGE_READY<strong>V</strong></td>
<td>Внутреннее запоминающее устройство готово.</td>
</tr>
<tr class="odd">
<td>STORAGE_FULL<strong>V</strong></td>
<td>Хранилище заполнено, операции отправки невозможно.</td>
</tr>
<tr class="even">
<td>MULTIPLE_FEED<strong>V</strong></td>
<td>Произошло условие множественного веб-канала (обычно с PAPER_JAM).</td>
</tr>
<tr class="odd">
<td>DEVICE_ATTENTION<strong>V</strong></td>
<td>Ошибка, требующая вмешательства пользователя на устройстве.</td>
</tr>
<tr class="even">
<td>LAMP_ERR<strong>V</strong></td>
<td>Сканер не готов из-за проблемы лампы.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_CHARACTERS"></span><span id="wia_dps_endorser_characters"></span><dl> <dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>сканнердевицеендорсерчарактерс</dt> </dl></td>
<td style="text-align: left;"><p>Содержит все допустимые символы, которые приложение может использовать для создания допустимых строк подтверждения. Заверение — это принтер, установленный на сканере, который печатает текстовое сообщение на каждой сканируемой странице. Минидривер должен проверять значение свойства <strong>WIA_DPS_ENDORSER_STRING</strong> по отношению к допустимой кодировке в этом свойстве. Минидривер создает и поддерживает это свойство.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_STRING"></span><span id="wia_dps_endorser_string"></span><dl> <dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>сканнердевицеендорсерстринг</dt> </dl></td>
<td style="text-align: left;"><p>Содержит строку, которая должна быть одобрена (иными словами, напечатана) на каждой странице, которую минидривер просматривает. Приложение задает это свойство, используя допустимую кодировку, сообщаемую в свойстве <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> . Минидривер должен заменять документы только в том случае, если в этом свойстве задана строка. Пустая строка означает, что функция подтверждения отключена.</p>
<p>Так как это обязанность драйвера для интерпретации строки подтверждения, драйвер может использовать специальные символы в <strong>WIA_DPS_ENDORSER_STRING</strong>. Однако эти символы будут понятны только вашим приложениям.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Драйвер, поддерживающий свойство <strong>WIA_DPS_ENDORSER_STRING</strong> , должен поддерживать следующий список токенов. </p>
<table>
<thead>
<tr class="header">
<th>Токен</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>$DATE $</td>
<td>Дата в формате гггг/мм/дд.</td>
</tr>
<tr class="even">
<td>$DAY $</td>
<td>День в формате DD.</td>
</tr>
<tr class="odd">
<td>$MONTH $</td>
<td>Месяц года в формате MM.</td>
</tr>
<tr class="even">
<td>$PAGE _COUNT $</td>
<td>Число передаваемых страниц.</td>
</tr>
<tr class="odd">
<td>$TIME $</td>
<td>Время суток в формате чч: мм: СС.</td>
</tr>
<tr class="even">
<td>$YEAR $</td>
<td>Год в формате гггг.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_FILTER_SELECT"></span><span id="wia_dps_filter_select"></span><dl> <dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </dl></td>
<td style="text-align: left;"><p>Зарезервировано, не используйте.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_GLOBAL_IDENTITY"></span><span id="wia_dps_global_identity"></span><dl> <dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>сканнердевицеглобалидентити</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство поддерживается только в Windows Vista и более поздних версиях.
</blockquote>
</div>
<div>
 
</div>
<p>Содержит адрес SOAP устройства со сканером веб-служб. Мини-драйвер WIA 2,0 создает и поддерживает это свойство.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_REGISTRATION"></span><span id="wia_dps_horizontal_bed_registration"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>сканнердевицехоризонталбедрегистратион</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство не поддерживается в Windows Vista и более поздних версиях.
</blockquote>
</div>
<div>
 
</div>
<p>Содержит регистрацию или выравнивание по горизонтали для документов, размещенных на планшете. Минидривер создает и поддерживает это свойство.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>В следующей таблице приведены три константы, допустимые для этого свойства.</p>

<table>
<thead>
<tr class="header">
<th>Константа</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LEFT_JUSTIFIED</td>
<td>Документ выравнивается по левому краю.</td>
</tr>
<tr class="even">
<td>ПО центру</td>
<td>Документ выравнивается по центру.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>Документ выровнен по правому краю.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>См. также:</strong></p>
<p><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_SIZE"></span><span id="wia_dps_horizontal_bed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>сканнердевицехоризонталбедсизе</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство не поддерживается в Windows Vista и более поздних версиях. Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Задает максимальную ширину (в тысячах) дюйма, которая сканируется по горизонтальной оси (X) от Платен сканера в текущем разрешении. Это свойство также применяется к автоматическим податчикам документов, которые перемещают листы в Платен сканера для сканирования. Это свойство является обязательным для сканеров, имеющих Платен. Для других типов сканера вместо этого будет реализовано свойство <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> .</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>сканнердевицехоризонталшитфидсизе</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство не поддерживается в Windows Vista и более поздних версиях. Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Задает максимальную ширину в тысячах дюйма, которая просматривается на горизонтальной оси (X) при текущем разрешении. Это свойство также применяется к автоматическим податчикам документов, которые просматриваются без перемещения листов в Платен сканера для планшетов. Это свойство является обязательным для сканеров подачи листов, прокрутки и ручной проверки.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MAX_SCAN_TIME"></span><span id="wia_dps_max_scan_time"></span><dl> <dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>сканнердевицемаксскантиме</dt> </dl></td>
<td style="text-align: left;"><p>Содержит максимальное время сканирования одной страницы с текущими настройками свойств (в миллисекундах). Приложение считывает это свойство, чтобы оценить время, которое займет сканирование страницы. Это полезно при определении условий устройства, которое перестало отвечать. Минидривер создает и поддерживает это свойство. Это свойство является обязательным для всех сканеров.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>сканнердевицеминхоризонталшитфидсизе</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство не поддерживается в Windows Vista и более поздних версиях. Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Содержит физические горизонтальные размеры наименьшей страницы, которую может сканировать устройство подачи документов сканера, в тысячах дюйма. Минидривер создает и поддерживает это свойство.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>См. также:</strong></p>
<p><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>сканнердевицеминвертикалшитфидсизе</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство не поддерживается в Windows Vista и более поздних версиях. Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Содержит физические вертикальные размеры наименьшей страницы, которую может сканировать устройство подачи документов сканера, в тысячах дюйма. Минидривер создает и поддерживает это свойство.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>См. также:</strong></p>
<p><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_XRES"></span><span id="wia_dps_optical_xres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>сканнердевицеоптикалксрес</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство не поддерживается в Windows Vista. Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Горизонтальное разрешение оптического экрана. Самое высокое поддерживаемое оптическое разрешение по горизонтали в DPI. Это свойство имеет одно значение. Это не список всех разрешений, которые могут быть созданы устройством. Вместо этого это разрешение оптики устройства. Минидривер создает и поддерживает это свойство. Это свойство является обязательным для всех сканеров.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_YRES"></span><span id="wia_dps_optical_yres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>сканнердевицеоптикалирес</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство не поддерживается в Windows Vista. Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Вертикальное оптическое разрешение. Максимальное поддерживаемое вертикальное оптическое разрешение в DPI. Это свойство имеет одно значение. Это не список всех разрешений, создаваемых устройством. Вместо этого это разрешение оптики устройства. Минидривер создает и поддерживает это свойство. Это свойство является обязательным для всех сканеров.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ORIENTATION"></span><span id="wia_dps_orientation"></span><dl> <dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>сканнердевицеориентатион</dt> </dl></td>
<td style="text-align: left;"><p>Содержит текущую настройку ориентации. Минидривер создает и поддерживает это свойство.</p>
<p>Приложение задает свойство <strong>WIA_DPS_ORIENTATION</strong> , чтобы определить исходную ориентацию страницы или изображения, которые должны быть получены. Сведения об использовании WIA_DPS_ORIENTATION см. в разделе <strong>WIA_DPS_PAGE_SIZE</strong></p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>В следующей таблице приведены четыре константы, допустимые для этого свойства.</p>

<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>дефинатион</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>СВЕРХУ</td>
<td>коэффициент в 90 градусов — поворот по часовой стрелке относительно КНИЖной ориентации.</td>
</tr>
<tr class="even">
<td>КНИЖНОЙ ориентации</td>
<td>0 градусов.</td>
</tr>
<tr class="odd">
<td>ROT180</td>
<td>коэффициент в 180 градусов — поворот по часовой стрелке относительно КНИЖной ориентации.</td>
</tr>
<tr class="even">
<td>ROT270</td>
<td>коэффициент в 270 градусов — поворот по часовой стрелке относительно КНИЖной ориентации.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>См. также:</strong></p>
<p><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAD_COLOR"></span><span id="wia_dps_pad_color"></span><dl> <dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>сканнердевицепадколор</dt> </dl></td>
<td style="text-align: left;"><p>Цвет, используемый для заполнения при недостаточном объеме данных изображения, чтобы заполнить запрошенный буфер. Это свойство реализуется для сканеров, которые заполняют буфер. Это свойство является необязательным для всех сканеров. Минидривер создает и поддерживает это свойство.</p>
<p>Тип: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Формат сведений о цвете — <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">ргбкуад</a>.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_HEIGHT"></span><span id="wia_dps_page_height"></span><dl> <dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>сканнердевицепажехеигхт</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство не поддерживается в Windows Vista. Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Содержит высоту (в тысячах дюйма) текущей выбранной страницы. Минидривер создает и поддерживает свойство <strong>WIA_DPS_PAGE_HEIGHT</strong> . Приложение считывает это свойство, чтобы определить физические размеры сканируемой страницы. Если параметры экстента отличаются от размеров известных страниц, это свойство сообщает высоту страницы, для которой свойство <strong>WIA_DPS_PAGE_SIZE</strong> имеет значение WIA_PAGE_CUSTOM (которое является значением свойства <strong>WIA_DPS_PAGE_SIZE</strong> ). <strong>WIA_DPS_PAGE_HEIGHT</strong> должны быть синхронизированы с <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, которая сообщает высоту сканируемой страницы в пикселях.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_SIZE"></span><span id="wia_dps_page_size"></span><dl> <dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>сканнердевицепажесизе</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство не поддерживается в Windows Vista. Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Содержит размер страницы, которая в настоящий момент выбрана для сканирования. Чтобы выбрать размеры сканируемой страницы, приложение задает это свойство. Минидривер создает и поддерживает это свойство.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>В следующей таблице приведены три константы, допустимые для этого свойства. </p>
<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Определение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PAGE_A4</td>
<td>8267 X 11692 (КНИЖная ориентация)</td>
</tr>
<tr class="even">
<td>WIA_PAGE_CUSTOM</td>
<td>Определяется значениями свойств <strong>WIA_DPS_PAGE_HEIGHT</strong> и <strong>WIA_DPS_PAGE_WIDTH</strong></td>
</tr>
<tr class="odd">
<td>WIA_PAGE_LETTER</td>
<td>8500 X 11000 (КНИЖная ориентация)</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Значение свойства <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> определяет ориентацию текущей выбранной страницы. Свойства <strong>WIA_DPS_PAGE_WIDTH</strong> и <strong>WIA_DPS_PAGE_HEIGHT</strong> сообщают о размерах страницы в тысячах дюйма. Обратите внимание, что эти свойства должны быть согласованы с <strong>WIA_IPS_XEXTENT</strong> и <strong>WIA_IPS_YEXTENT</strong>, которые содержат размеры страницы в пикселях. Допустимые значения типа WIA_PROP_LIST должны зависеть от допустимых настроек свойства <strong>WIA_IPS_ORIENTATION</strong> . Если устройство не может сканировать документы, ориентированные на альбомную ориентацию, с параметром WIA_PAGE_A4, WIA_PAGE_A4 не должны отображаться в списке допустимых значений для свойства <strong>WIA_DPS_PAGE_SIZE</strong> , если <strong>WIA_IPS_ORIENTATION</strong> имеет значение ланскапе.</p>
<p>Если приложение устанавливает <strong>WIA_DPS_PAGE_SIZE</strong> любое значение, отличное от WIA_PAGE_CUSTOM, минидривер должен изменить значения <strong>WIA_DPS_PAGE_WIDTH</strong> и <strong>WIA_DPS_PAGE_HEIGHT</strong> на размеры страницы в тысячах дюйма. Он также должен скорректировать значения <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> и <strong>WIA_IPS_YEXTENT</strong> к размерам страницы в пикселях.</p>
<p>Если параметр экстента (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> или <strong>WIA_IPS_YEXTENT</strong>) изменяется на значение, не совпадающее с текущим параметром размера страницы, минидривер должен изменить значение свойства <strong>WIA_DPS_PAGE_SIZE</strong> на WIA_PAGE_CUSTOM. Минидривер также должен изменить <strong>WIA_DPS_PAGE_WIDTH</strong> или <strong>WIA_DPS_PAGE_HEIGHT</strong> в соответствии с новым параметром экстента.</p>
<p>Если для <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> задано значение ланскапе, то параметры экстента будут &quot; отражены. &quot; Например, если приложение задает <strong>WIA_DPS_PAGE_SIZE</strong> для WIA_PAGE_A4, минидривер должен установить для параметра <strong>WIA_DPS_PAGE_WIDTH</strong> значение 11692, а для <strong>WIA_DPS_PAGE_HEIGHT</strong> — 8267. (Минидривер также должен задавать <strong>WIA_IPS_XEXTENT</strong> и <strong>WIA_IPS_YEXTENT</strong> соответственно.) Обратите внимание, что если <strong>WIA_DPS_PAGE_SIZE</strong> имеет значение WIA_PAGE_CUSTOM, Настройка ориентации не используется для определения размеров сканируемой страницы.</p>
<p>Минидривер отвечает за обеспечение соответствия свойства <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> с текущей областью выбора. Если приложение изменяет значение <strong>WIA_IPS_ORIENTATION</strong> на другое, недопустимое для текущего выбранного размера страницы, минидривер должен изменить значение <strong>WIA_DPS_PAGE_SIZE</strong> на размер страницы, поддерживаемый новым значением ориентации.</p>
<p>Если приложение задает для свойства <strong>WIA_DPS_PAGE_SIZE</strong> значение WIA_PAGE_CUSTOM, то область текущего выбора не изменяется. WIA минидривер должен получить текущий макет изображения, начиная с текущих параметров свойств <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> и <strong>WIA_IPS_YPOS</strong> . Если параметр размера страницы приводит к выделению области выделения, находящегося за пределами испытательного сканера, минидривер должен автоматически скорректировать значения <strong>WIA_IPS_XPOS</strong> и <strong>WIA_IPS_YPOS</strong> свойства на допустимые параметры. Если свойства <strong>WIA_DPS_PAGE_SIZE</strong> и <strong>WIA_IPS_ORIENTATION</strong> задаются одновременно и являются недопустимыми при их применении в сочетании, минидривер не должен возвращать параметры приложения, возвращая ошибку в <a href="https://msdn.microsoft.com/library/ms794145.aspx">ивиаминидрв::d рввалидатеитемпропертиес</a>. .</p>
<p>В следующих четырех примерах показаны различные сценарии <strong>WIA_DPS_PAGE_SIZE</strong> .</p>
<ol>
<li>Драйвер сообщает о параметрах.</li>
<li>Приложение задает для свойства <strong>WIA_DPS_PAGE_SIZE</strong> значение WIA_PAGE_LETTER.</li>
<li>Приложение задает для свойства <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> значение ланскапе.</li>
<li>Приложение изменяет свойство <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> на меньшее значение.</li>
</ol>
<p><strong>Пример 1. минидривер сообщает о параметрах</strong></p>
<p>В следующем примере минидривер задает настраиваемую область выбора до того, как приложение установит все свойства WIA. В этом случае область выбора представляет все стекло.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_WIDTH = 11500
WIA_DPS_PAGE_HEIGHT = 14000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1150
WIA_IPS_YEXTENT = 1400
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><strong>Пример 2. приложение задает</strong> <strong></strong><strong>для свойства</strong> WIA_DPS_PAGE_SIZE значение WIA_PAGE_LETTER  </p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_WIDTH = 8500
WIA_DPS_PAGE_HEIGHT = 11000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 850
WIA_IPS_YEXTENT = 1100
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><strong>Пример 3. приложение задает</strong> <a href="-wia-wiaitempropscanneritem.md"><strong></strong></a><strong>для свойства</strong> WIA_IPS_ORIENTATION значение ланскапе  </p>
<p>Физическая среда должна иметь возможность получить страницу, которая изначально была в альбомной ориентации.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_HEIGHT = 11000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1100
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><strong>Пример 4. приложение изменяет</strong> свойство <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>  <strong>на меньшее значение</strong></p>
<p>В следующем примере приложение изменяет свойство <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> на 1000. Минидривер должен предположить, что новое значение, содержащееся в <strong>WIA_IPS_XEXTENT</strong> , больше не является допустимым для свойства <strong>WIA_DPS_PAGE_SIZE</strong> и, таким образом, изменит <strong>WIA_DPS_PAGE_SIZE</strong> на WIA_PAGE_CUSTOM. Минидривер также должен корректировать <strong>WIA_DPS_PAGE_WIDTH</strong>.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_HEIGHT = 10000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1000
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_WIDTH"></span><span id="wia_dps_page_width"></span><dl> <dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>сканнердевицепажевидс</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство не поддерживается в Windows Vista. Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Содержит ширину текущей выбранной страницы в тысячах дюйма. Приложение считывает это свойство, чтобы определить физические размеры сканируемой страницы. Если параметры экстента отличаются от размеров известных страниц, это свойство сообщает ширину страницы, для которой свойство <strong>WIA_DPS_PAGE_SIZE</strong> имеет значение WIA_PAGE_CUSTOM. <strong>WIA_DPS_PAGE_WIDTH</strong> должны быть синхронизированы со значением <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, которое показывает ширину сканируемой страницы в пикселях. Минидривер создает и поддерживает это свойство.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGES"></span><span id="wia_dps_pages"></span><dl> <dt><strong>WIA_DPS_PAGES</strong></dt> <dt>сканнердевицепажес</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство не поддерживается в Windows Vista. Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Содержит текущее число страниц, получаемых из автоматического устройства подачи документов. Минидривер создает и поддерживает это свойство.</p>
<p>Тип: <strong>VT_I4</strong>; Доступ: чтение и запись; Допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (от нуля до максимального количества страниц, которое может храниться в податчике документов)</p>
<p>Приложение считывает это свойство для определения емкости страницы устройства подачи документов. Приложение также задает для этого свойства число страниц, которое он будет сканировать.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Если включен дуплексный режим (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> установлен в "Feed" | ДУПЛЕКСная), <strong>WIA_DPS_PAGES</strong> по-прежнему равно числу сканируемых страниц.
</blockquote>
</div>
<div>
 
</div>
<p>Один лист бумаги автоматически будет содержать две страницы, если ДУПЛЕКСный режим включен, даже если обратная сторона страницы пуста.</p>
<p>Установка <strong>WIA_DPS_PAGES</strong> в значение 1 приводит к тому, что сканер обрабатывает одну из сторон страницы. Если сканер не может сканировать только одну сторону страницы в режиме дуплекса, <strong>WIA_DPS_PAGES</strong> допустимое значение для элемента Inc в структуре WIA_PROPERTY_INFO необходимо изменить на 2. Это значение сигнализирует приложению, что оно должно запрашивать страницы, кратные двум. Нулевое значение означает, что проверяются <em>все</em> страницы, загруженные в устройство подачи документов.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PLATEN_COLOR"></span><span id="wia_dps_platen_color"></span><dl> <dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>сканнердевицеплатенколор</dt> </dl></td>
<td style="text-align: left;"><p>Задает цвет платена в обратной стороне сканируемой страницы. Это свойство является необязательным для сканеров, имеющих Платен. Минидривер создает и поддерживает это свойство.</p>
<p>Тип: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Формат сведений о цвете — <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">ргбкуад</a>.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PREVIEW"></span><span id="wia_dps_preview"></span><dl> <dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>сканнердевицепревиев</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство не поддерживается в Windows Vista. Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Указывает режим предварительного просмотра для устройства. Приложение задает это свойство, чтобы перевести устройство в режим предварительного просмотра.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>В следующей таблице приведены две константы, допустимые для этого свойства. </p>
<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Определение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_FINAL_SCAN</td>
<td>Приложение выполнит окончательную проверку.</td>
</tr>
<tr class="even">
<td>WIA_PREVIEW_SCAN</td>
<td>Приложение будет выполнять предварительную проверку.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AHEAD_PAGES"></span><span id="wia_dps_scan_ahead_pages"></span><dl> <dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>сканнердевицесканахеадпажес</dt> </dl></td>
<td style="text-align: left;"><p>Содержит значение, указывающее, будет ли сканер кэшировать страницы в буфере сканера перед их отправкой в приложение.</p>
<p>Нулевое значение отключает сканирование, и страницы не просматриваются заранее. При обычной передаче данных в буферизованный элемент с упреждающим просмотром получает буферизованные страницы. Свойства WIA не могут быть изменены во время операции предварительного просмотра. Это необязательное свойство.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> от нуля до максимального количества страниц, которое может храниться в податчике документов.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AVAILABLE_ITEM"></span><span id="wia_dps_scan_available_item"></span><dl> <dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>сканнердевицесканаваилаблеитем</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство поддерживается только в Windows 7 и более поздних версиях.
</blockquote>
</div>
<div>
 
</div>
<p>Указывает источник входных данных (планшетный, автоматический веб-устройство подачи документов или адаптер сканирования файлов) для сканирования или место хранения, из которого следует передавать данные.</p>
<p>Событие Scan уведомляет приложение о том, что пользователь инициировал сканирование, но событие не предоставляет имя элемента WIA, представляющего источник входных данных. Обработчик событий приложения может запросить свойство WIA_DPS_SCAN_AVAILABLE_ITEM корневого элемента, чтобы получить имя входного элемента источника.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> от нуля до максимального количества страниц, которое может храниться в податчике документов.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SERVICE_ID"></span><span id="wia_dps_service_id"></span><dl> <dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>сканнердевицесервицеид</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство поддерживается только в Windows Vista и более поздних версиях.
</blockquote>
</div>
<div>
 
</div>
<p>Содержит идентификатор службы сканера веб-служб. Мини-драйвер WIA 2,0 создает и поддерживает это свойство.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_dps_sheet_feeder_registration"></span><dl> <dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>сканнердевицешитфидеррегистратион</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство не поддерживается в Windows Vista и более поздних версиях. Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Содержит регистрацию, выравнивание и обнаружение краев для документов, размещенных на планшете. Минидривер создает и поддерживает это свойство. Это свойство указывает, как располагается лист горизонтально в заголовке сканирования карманного компьютера или сканера с листовой подачи. Свойство используется для прогнозирования места размещения документа по заголовку сканирования.</p>
<p>Для сканеров, поддерживающих несколько заголовков сканирования, это свойство задается относительно самого верхнего заголовка сканирования. Это свойство является обязательным для сканеров подачи листов, прокрутки и карманных устройств.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>В следующей таблице приведены три константы, допустимые для этого свойства.</p>

<table>
<thead>
<tr class="header">
<th>Константа</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LEFT_JUSTIFIED</td>
<td>Лист располагается слева относительно заголовка сканирования.</td>
</tr>
<tr class="even">
<td>ПО центру</td>
<td>Лист выравнивается по заголовку сканирования.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>Лист располагается вправо относительно головного поиска.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_dps_show_preview_control"></span><dl> <dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>сканнердевицешовпревиевконтрол</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство не поддерживается в Windows Vista. Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Указывает, должен ли элемент отображаться в элементе управления предварительной версии. Минидривер создает и поддерживает это свойство.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>В следующей таблице приведены две константы, допустимые для этого свойства. </p>
<table>
<thead>
<tr class="header">
<th>Константа</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_SHOW_PREVIEW_CONTROL</td>
<td>Отображение элемента управления предварительным просмотром для пользователя, так как это устройство может выполнять предварительную версию.</td>
</tr>
<tr class="even">
<td>WIA_DONT_SHOW_PREVIEW_CONTROL</td>
<td>Не показывать пользователю элемент управления предварительной версии, так как это устройство не может выполнить предварительную версию.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_USER_NAME"></span><span id="wia_dps_user_name"></span><dl> <dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>сканнердевицеусернаме</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство поддерживается только в Windows Vista и более поздних версиях.
</blockquote>
</div>
<div>
 
</div>
<p>Используется службой WIA для информирования мини-драйвера о имени учетной записи пользователя (включая имя сетевого домена, если применимо) сеанса, в котором выполняется текущее приложение WIA.</p>
<p>Это свойство корневого элемента, управляемое службой WIA.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_REGISTRATION"></span><span id="wia_dps_vertical_bed_registration"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>сканнердевицевертикалбедрегистратион</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство не поддерживается в Windows Vista и более поздних версиях.
</blockquote>
</div>
<div>
 
</div>
<p>Содержит регистрацию или вертикальное выравнивание и обнаружение краев для документов, размещенных на планшете. Минидривер создает и поддерживает это свойство.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>В следующей таблице приведены три константы, допустимые для этого свойства. </p>
<table>
<thead>
<tr class="header">
<th>Константа</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TOP_JUSTIFIED</td>
<td>Документ выровнен по верхнему краю.</td>
</tr>
<tr class="even">
<td>ПО центру</td>
<td>Документ выравнивается по центру.</td>
</tr>
<tr class="odd">
<td>BOTTOM_JUSTIFIED</td>
<td>Документ выровнен по нижнему краю.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>См. также</strong>.</p>
<p><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_SIZE"></span><span id="wia_dps_vertical_bed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>сканнердевицевертикалбедсизе</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство не поддерживается в Windows Vista и более поздних версиях. Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Задает максимальную высоту в тысячах дюйма, которая просматривается по вертикальной оси (Y) от Платен сканера для планшетов с текущим разрешением. Это свойство также применяется к автоматическим податчикам документов, которые перемещают листы в Платен сканера для сканирования. Это свойство является обязательным для сканеров, имеющих Платен. Для других типов сканера вместо этого будет реализовано свойство <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> .</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>сканнердевицевертикалшитфидсизе</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Это свойство не поддерживается в Windows Vista и более поздних версиях. Используйте <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Задает максимальную высоту в тысячах дюйма, которая просматривается по вертикальной оси (Y) из сканера карманного или электронного канала при текущем разрешении. Это свойство также применяется к автоматическим податчикам документов, которые просматриваются без перемещения листов в Платен сканера для планшетов. Это свойство является обязательным для сканеров подачи листов. Сканеры с прокруткой и ручной поддержкой не должны реализовывать это свойство.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                |
| Header<br/>                   | <dl> <dt>Виадеф. h</dt> </dl> |



 

 
