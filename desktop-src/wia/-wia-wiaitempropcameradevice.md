---
description: Аппаратные устройства для получения образа Windows (WIA) имеют значения свойств, которые хранятся в реестре Windows. Дополнительные сведения см. в разделе Общие константы свойств устройства.
ms.assetid: 7893137b-194c-4ea1-b15c-59d2f41f972a
title: Константы свойств устройства камеры (Виадеф. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPC_PICTURES_TAKEN
- WIA_DPC_PICTURES_REMAINING
- WIA_DPC_EXPOSURE_MODE
- WIA_DPC_EXPOSURE_COMP
- WIA_DPC_EXPOSURE_TIME
- WIA_DPC_FNUMBER
- WIA_DPC_FLASH_MODE
- WIA_DPC_FOCUS_MODE
- WIA_DPC_FOCUS_MANUAL_DIST
- WIA_DPC_ZOOM_POSITION
- WIA_DPC_PAN_POSITION
- WIA_DPC_TILT_POSITION
- WIA_DPC_TIMER_MODE
- WIA_DPC_TIMER_VALUE
- WIA_DPC_POWER_MODE
- WIA_DPC_BATTERY_STATUS
- WIA_DPC_THUMB_WIDTH
- WIA_DPC_THUMB_HEIGHT
- WIA_DPC_PICT_WIDTH
- WIA_DPC_PICT_HEIGHT
- WIA_DPC_DIMENSION
- WIA_DPC_COMPRESSION_SETTING
- WIA_DPC_FOCUS_METERING
- WIA_DPC_TIMELAPSE_INTERVAL
- WIA_DPC_TIMELAPSE_NUMBER
- WIA_DPC_BURST_INTERVAL
- WIA_DPC_BURST_NUMBER
- WIA_DPC_EFFECT_MODE
- WIA_DPC_DIGITAL_ZOOM
- WIA_DPC_SHARPNESS
- WIA_DPC_CONTRAST
- WIA_DPC_CAPTURE_MODE
- WIA_DPC_CAPTURE_DELAY
- WIA_DPC_EXPOSURE_INDEX
- WIA_DPC_EXPOSURE_METERING_MODE
- WIA_DPC_FOCUS_METERING_MODE
- WIA_DPC_FOCUS_DISTANCE
- WIA_DPC_FOCAL_LENGTH
- WIA_DPC_RGB_GAIN
- WIA_DPC_WHITE_BALANCE
- WIA_DPC_UPLOAD_URL
- WIA_DPC_ARTIST
- WIA_DPC_COPYRIGHT_INFO
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 0114fedd7fd4acf811e71db67376afecc2630cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497535"
---
# <a name="camera-device-property-constants"></a>Константы свойств устройства камеры

Аппаратные устройства для получения образа Windows (WIA) имеют значения свойств, которые хранятся в реестре Windows. Дополнительные сведения см. в разделе [**общие константы свойств устройства**](-wia-wiaitempropcommondevice.md).

Следующие константы свойств устройства со связанными строками относятся к цифровым камерам. Префикс "WIA \_ DPC \_ " указывает свойство устройства для камер и является соглашением об именовании, используемым в C/C++. Для сценариев эти константы используют префикс "Камерадевице" и являются частью перечислимого типа [виаитемпропертид](-wia-wiaitempropertyid.md) . Соответствующее имя элемента из этого перечисления скриптов отображается в круглых скобках рядом с именем константы C/C++ в следующем списке.

> [!Note]  
> WIA не поддерживает камеры в Windows Vista и более поздних версиях. Для этих версий Windows используйте API переносных устройств Windows (WPD), описанный в пакете средств разработки драйверов Windows (DDK), для получения изображений из камер.

 



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
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_TAKEN"></span><span id="wia_dpc_pictures_taken"></span><dl> <dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>камерадевицепиктурестакен</dt> </dl></td>
<td style="text-align: left;">Количество изображений, занятых камерой. Минидривер создает и поддерживает это свойство.<br/> Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_REMAINING"></span><span id="wia_dpc_pictures_remaining"></span><dl> <dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>камерадевицепиктуресремаининг</dt> </dl></td>
<td style="text-align: left;">Количество снимков, которые могут быть выполнены с учетом текущих настроек свойств. Если эти параметры изменяются и изменения влияют на размер образов, создаваемых устройством камеры, то WIA минидривер должен обновить количество оставшихся изображений. Минидривер создает и поддерживает это свойство.<br/> Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_MODE"></span><span id="wia_dpc_exposure_mode"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>камерадевицеекспосуремоде</dt> </dl></td>
<td style="text-align: left;">Указывает текущий режим экспозиции камеры. Приложение изменяет это свойство для управления режимом экспозиции устройства камеры.<br/> Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a><br/> В следующей таблице приведены семь констант, допустимых для этого свойства.<br/> 
<table>
<thead>
<tr class="header">
<th>Режим экспозиции</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EXPOSUREMODE_MANUAL</td>
<td>Скорость затвора и Апертура задаются пользователем.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_AUTO</td>
<td>Скорость затвора и Апертура автоматически устанавливаются камерой.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_APERTURE_PRIORITY</td>
<td>Апертура задается пользователем, а Камера автоматически устанавливает скорость затвора.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_SHUTTER_PRIORITY</td>
<td>Скорость затвора задается пользователем, а Камера автоматически устанавливает апертуру.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_PROGRAM_CREATIVE</td>
<td>Скорость затвора и Апертура автоматически устанавливаются камерой, оптимизированы для всех тем.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_PROGRAM_ACTION</td>
<td>Скорость затвора и Апертура автоматически устанавливаются камерой, оптимизированы для сцен, содержащих быстрое перемещение.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_PORTRAIT</td>
<td>Скорость затвора и Апертура автоматически задаются камерой, оптимизированной для книжной фотографии.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_COMP"></span><span id="wia_dpc_exposure_comp"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>камерадевицеекспосурекомп</dt> </dl></td>
<td style="text-align: left;"><p>Позволяет корректировать точку установки элемента управления автоматической экспозиции цифровой камеры. Например, нулевое значение не изменяет уровень автоэкспозиции фабрики. Единицы находятся в &quot; остановленных единицах &quot; , которые масштабируются с помощью коэффициента 1000, что позволяет использовать дробные значения Stop. Значение 2000 соответствует двум прекращениям (в четыре раза больше энергии на датчике), что дает более яркие образы. Параметр-1000 соответствует одному снижению экспозиции (половина энергии на датчике), что дает более темные образы. Значения параметра относятся к дополнительным системам фотографических раскрытия (ВЕРШИНЕ). Это свойство может быть выражено либо в виде списка, либо в диапазоне значений. Это свойство обычно используется только в том случае, если для устройства свойство <strong>WIA_DPC_EXPOSURE_MODE</strong> имеет значение EXPOSUREMODE_MANUAL.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> или WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_TIME"></span><span id="wia_dpc_exposure_time"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>камерадевицеекспосуретиме</dt> </dl></td>
<td style="text-align: left;"><p>Соответствует скорости затвора в секундах, которая масштабируется на 10 000. Как правило, устройство использует это свойство только в том случае, если свойство <strong>WIA_DPC_EXPOSURE_MODE</strong> имеет значение EXPOSUREMODE_MANUAL или EXPOSUREMODE_SHUTTER_PRIORITY.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> или WIA_PROP_LIST</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FNUMBER"></span><span id="wia_dpc_fnumber"></span><dl> <dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>камерадевицефнумбер</dt> </dl></td>
<td style="text-align: left;"><p>Соответствует апертуре линзы в единицах числа f-останавливаютй, масштабируемых на 100. Значение этого свойства обычно допустимо, только если свойство <strong>WIA_DPC_EXPOSURE_MODE</strong> имеет значение EXPOSUREMODE_MANUAL или EXPOSUREMODE_APERTURE_PRIORITY.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FLASH_MODE"></span><span id="wia_dpc_flash_mode"></span><dl> <dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>камерадевицефлашмоде</dt> </dl></td>
<td style="text-align: left;"><p>Определяет текущую настройку режима вспышки для устройства камеры. Драйвер устройства перечисляет поддерживаемые значения этого свойства. Приложение записывает это свойство, чтобы установить режим вспышки для устройства камеры.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Следующая таблица содержит шесть констант, допустимых для этого свойства.</p>

<table>
<thead>
<tr class="header">
<th>Режим вспышки</th>
<th>Определение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FLASHMODE_AUTO</td>
<td>Устройство камеры определяет правильные параметры Flash.</td>
</tr>
<tr class="even">
<td>FLASHMODE_FILL</td>
<td>Устройство камеры настроено на вспышку независимо от текущих условий освещения.</td>
</tr>
<tr class="odd">
<td>FLASHMODE_OFF</td>
<td>Устройство <em>камеры настроено</em> на невспышку для любых снимков.</td>
</tr>
<tr class="even">
<td>FLASHMODE_REDEYE_AUTO</td>
<td>Устройство камеры определяет правильные параметры Flash, используя сокращение красных глаз, независимо от текущих условий освещения.</td>
</tr>
<tr class="odd">
<td>FLASHMODE_REDEYE_FILL</td>
<td>Устройство камеры настроено для использования сокращения красных глаз и флэш-памяти независимо от текущих условий освещения.</td>
</tr>
<tr class="even">
<td>FLASHMODE_EXTERNALSYNC</td>
<td>Устройство камеры настроено для синхронизации с внешними Flash-устройствами.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MODE"></span><span id="wia_dpc_focus_mode"></span><dl> <dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>камерадевицефокусмоде</dt> </dl></td>
<td style="text-align: left;"><p>Определяет текущее значение режима фокусировки для устройства камеры. Драйвер устройства перечисляет поддерживаемые значения этого свойства. Приложение записывает это свойство, чтобы установить режим фокусировки для устройства камеры.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>В следующей таблице приведены три константы, допустимые для этого свойства.</p>

<table>
<thead>
<tr class="header">
<th>Режим фокусировки</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FOCUSMODE_MANUAL</td>
<td>Устройство камеры настроено для разрешения пользователю сосредоточиться вручную.</td>
</tr>
<tr class="even">
<td>FOCUSMODE_AUTO</td>
<td>Устройство камеры настроено для автоматического фокуса.</td>
</tr>
<tr class="odd">
<td>FOCUSMODE_MACROAUTO</td>
<td>Устройство камеры настроено для автоматического фокусирования с использованием параметров макросов с коротким диапазоном.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MANUAL_DIST"></span><span id="wia_dpc_focus_manual_dist"></span><dl> <dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </dl></td>
<td style="text-align: left;"><p>Зарезервировано, не используйте.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ZOOM_POSITION"></span><span id="wia_dpc_zoom_position"></span><dl> <dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </dl></td>
<td style="text-align: left;"><p>Зарезервировано, не используйте.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PAN_POSITION"></span><span id="wia_dpc_pan_position"></span><dl> <dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>камерадевицепанпоситион</dt> </dl></td>
<td style="text-align: left;"><p>Зарезервировано, не используйте.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TILT_POSITION"></span><span id="wia_dpc_tilt_position"></span><dl> <dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>камерадевицетилтпоситион</dt> </dl></td>
<td style="text-align: left;"><p>Зарезервировано, не используйте.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_MODE"></span><span id="wia_dpc_timer_mode"></span><dl> <dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>камерадевицетимермоде</dt> </dl></td>
<td style="text-align: left;"><p>Зарезервировано, не используйте.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_VALUE"></span><span id="wia_dpc_timer_value"></span><dl> <dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>камерадевицетимервалуе</dt> </dl></td>
<td style="text-align: left;"><p>Зарезервировано, не используйте.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_POWER_MODE"></span><span id="wia_dpc_power_mode"></span><dl> <dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>камерадевицеповермоде</dt> </dl></td>
<td style="text-align: left;"><p>Определяет текущий источник питания для устройства камеры. Приложение считывает это свойство, чтобы определить, какой источник питания используется камерой.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>В следующей таблице приведены две константы, допустимые для этого свойства.</p>

<table>
<thead>
<tr class="header">
<th>Режим питания</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>POWERMODE_LINE</td>
<td>Устройство камеры работает на адаптере питания.</td>
</tr>
<tr class="even">
<td>POWERMODE_BATTERY</td>
<td>Устройство камеры работает с питанием от аккумулятора.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BATTERY_STATUS"></span><span id="wia_dpc_battery_status"></span><dl> <dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>камерадевицебаттеристатус</dt> </dl></td>
<td style="text-align: left;"><p>Процент питания от аккумулятора, который остается в работе устройства камеры. Это значение должно быть целым числом от 0 до 100. Приложение считывает это свойство, чтобы определить оставшийся срок работы аккумулятора устройства камеры.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_WIDTH"></span><span id="wia_dpc_thumb_width"></span><dl> <dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>камерадевицесумбвидс</dt> </dl></td>
<td style="text-align: left;"><p>Ширина (в пикселях) эскиза изображения, используемого для вновь захваченных изображений. Приложение считывает это значение, чтобы получить приблизительный размер для отображения эскизов в пользовательском интерфейсе.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) или только для чтения (WIA_PROP_NONE), допустимые значения: WIA_PROP_LIST или WIA_PROP_NONE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_HEIGHT"></span><span id="wia_dpc_thumb_height"></span><dl> <dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>камерадевицесумбхеигхт</dt> </dl></td>
<td style="text-align: left;"><p>Ширина (в пикселях) эскиза изображения, используемого для вновь захваченных изображений. Приложение считывает это значение, чтобы получить приблизительный размер для отображения эскизов в пользовательском интерфейсе.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) или только для чтения (WIA_PROP_NONE), допустимые значения: WIA_PROP_LIST или WIA_PROP_NONE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICT_WIDTH"></span><span id="wia_dpc_pict_width"></span><dl> <dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>камерадевицепиктвидс</dt> </dl></td>
<td style="text-align: left;"><p>Ширина в пикселях, используемая для вновь захваченных изображений. Список допустимых значений для этого свойства имеет соответствие "один к одному" списку допустимых значений для свойства <strong>WIA_DPC_PICT_HEIGHT</strong> . Если отдельные ширина и высота линейно устанавливаются и ортогональны друг к другу, они могут быть выражены в виде диапазона.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICT_HEIGHT"></span><span id="wia_dpc_pict_height"></span><dl> <dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>камерадевицепиксеигхт</dt> </dl></td>
<td style="text-align: left;"><p>Высота в пикселях, используемая для вновь захваченных изображений. Список допустимых значений для этого свойства имеет соответствие "один к одному" со списком допустимых значений для свойства <strong>WIA_DPC_PICT_WIDTH</strong> . Если отдельные ширина и высота линейно устанавливаются и ортогональны друг к другу, они могут быть выражены в виде диапазона.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIMENSION"></span><span id="wia_dpc_dimension"></span><dl> <dt><strong>WIA_DPC_DIMENSION</strong></dt> </dl></td>
<td style="text-align: left;"><p>Зарезервировано, не используйте.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_COMPRESSION_SETTING"></span><span id="wia_dpc_compression_setting"></span><dl> <dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>камерадевицекомпрессионсеттинг</dt> </dl></td>
<td style="text-align: left;"><p>Предназначен для приблизительного линейного использования в отношении воспринимаемого изображения по широкому спектру содержимого сцены и содержит либо диапазон, либо список целых чисел. Небольшие целые числа используются для представления низкого качества (то есть максимального сжатия), а большие целые числа используются для представления более высокого качества (то есть минимального сжатия). Все доступные параметры на устройстве относительны только для этого устройства и, следовательно, специфичны для устройства.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING"></span><span id="wia_dpc_focus_metering"></span><dl> <dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </dl></td>
<td style="text-align: left;"><p>Зарезервировано, не используйте.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_INTERVAL"></span><span id="wia_dpc_timelapse_interval"></span><dl> <dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>камерадевицетимелапсеинтервал</dt> </dl></td>
<td style="text-align: left;"><p>Время в миллисекундах между записью образа в операции записи промежутка времени.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST или WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_NUMBER"></span><span id="wia_dpc_timelapse_number"></span><dl> <dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>камерадевицетимелапсенумбер</dt> </dl></td>
<td style="text-align: left;"><p>Число образов, которые устройство пытается захватить во время записи промежутка времени.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST или WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BURST_INTERVAL"></span><span id="wia_dpc_burst_interval"></span><dl> <dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>камерадевицебурстинтервал</dt> </dl></td>
<td style="text-align: left;"><p>Время в миллисекундах между записью изображения во время операции пакетной передачи.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST или WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_BURST_NUMBER"></span><span id="wia_dpc_burst_number"></span><dl> <dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>камерадевицебурстнумбер</dt> </dl></td>
<td style="text-align: left;"><p>Число образов, которые устройство пытается захватить во время операции пакетной работы.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST или WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EFFECT_MODE"></span><span id="wia_dpc_effect_mode"></span><dl> <dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>камерадевицееффектмоде</dt> </dl></td>
<td style="text-align: left;"><p>Указывает режим получения специального изображения камеры.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>В следующей таблице приведены три константы, допустимые для этого свойства.</p>

<table>
<thead>
<tr class="header">
<th>Режим эффектов</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EFFECTMODE_STANDARD</td>
<td>Запись изображения в стандартном режиме для камеры.</td>
</tr>
<tr class="even">
<td>EFFECTMODE_BW</td>
<td>Запись изображения в градациях серого.</td>
</tr>
<tr class="odd">
<td>EFFECTMODE_SEPIA</td>
<td>Запишите образ выцветшей.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIGITAL_ZOOM"></span><span id="wia_dpc_digital_zoom"></span><dl> <dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>камерадевицедигиталзум</dt> </dl></td>
<td style="text-align: left;"><p>Эффективное масштабирование полученного образа цифровой камеры с коэффициентом, равным 10. Значение 10 соответствует отсутствию цифрового масштаба (1X), то есть стандартного размера сцены, захваченного камерой. Значение 20 соответствует удвоенному масштабу, где камера захватывает один квартал стандартного размера сцены.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_SHARPNESS"></span><span id="wia_dpc_sharpness"></span><dl> <dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>камерадевицешарпнесс</dt> </dl></td>
<td style="text-align: left;"><p>Воспринимаемая резкость захваченного изображения. Это свойство может использовать либо список значений, либо диапазон значений. Минимальное значение представляет собой наименьший уровень резкости, тогда как максимальное значение представляет максимальную резкость. Обычно значение в середине диапазона представляет нормальную, или по умолчанию четкость.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CONTRAST"></span><span id="wia_dpc_contrast"></span><dl> <dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>камерадевицеконтраст</dt> </dl></td>
<td style="text-align: left;"><p>Воспринимаемая контрастность захваченного изображения. Это свойство может содержать либо список значений, либо диапазон значений. Минимальное поддерживаемое значение представляет наименьшую степень контрастности, в то время как максимальное значение соответствует наибольшему контрасту. Как правило, значение в середине диапазона представляет собой нормальную или по умолчанию, контрастность.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_MODE"></span><span id="wia_dpc_capture_mode"></span><dl> <dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>камерадевицекаптуремоде</dt> </dl></td>
<td style="text-align: left;"><p>Задает режим записи образа.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>В следующей таблице приведены три константы, допустимые для этого свойства.</p>

<table>
<thead>
<tr class="header">
<th>Режим записи</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CAPTUREMODE_NORMAL</td>
<td>Нормальный режим для камеры.</td>
</tr>
<tr class="even">
<td>CAPTUREMODE_BURST</td>
<td>Зафиксируйте более одного образа в быстром выполнении, как определено значениями свойств <strong>WIA_DPC_BURST_NUMBER</strong> и <strong>WIA_DPC_BURST_INTERVAL</strong> .</td>
</tr>
<tr class="odd">
<td>CAPTUREMODE_TIMELAPSE</td>
<td>Захватите более одного образа в случае успеха, как определено в свойствах <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> и <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> .</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_DELAY"></span><span id="wia_dpc_capture_delay"></span><dl> <dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>камерадевицекаптуределай</dt> </dl></td>
<td style="text-align: left;"><p>Значение, представляющее количество времени задержки (в миллисекундах), которое должно быть вставлено между триггером записи и фактической инициацией записи данных. Это свойство не предназначено для описания времени между кадрами для одной инициации, нескольких захватов, таких как пакет или промежуток времени, которые имеют отдельные свойства интервала <strong>WIA_DPC_BURST_INTERVAL</strong> и <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>. В таких случаях он по-прежнему выступает в качестве начальной задержки перед записью первого изображения в ряде, независимо от времени между кадрами. Для без задержки до записи это свойство должно иметь значение 0.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_INDEX"></span><span id="wia_dpc_exposure_index"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>камерадевицеекспосуреиндекс</dt> </dl></td>
<td style="text-align: left;"><p>Разрешает эмуляцию параметров скорости пленки на цифровой камере. Параметры соответствуют стандартам ISO (ASA/DIN). Как правило, устройство поддерживает дискретные перечислимые значения, но возможно непрерывное управление диапазоном значений. Значение 0xFFFF соответствует автоматическому параметру ISO.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_METERING_MODE"></span><span id="wia_dpc_exposure_metering_mode"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>камерадевицеекспосуреметерингмоде</dt> </dl></td>
<td style="text-align: left;"><p>Указывает режим, используемый камерой для автоматической настройки параметра экспозиции.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>

<table>
<thead>
<tr class="header">
<th>Режим измерения экспозиции</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EXPOSUREMETERING_AVERAGE</td>
<td>Установите экспозицию на основе среднего значения всей сцены.</td>
</tr>
<tr class="even">
<td>EXPOSUREMETERING_CENTERWEIGHT</td>
<td>Установите экспозицию на основе среднего взвешенного значения.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMETERING_MULTISPOT</td>
<td>Установите экспозицию на основе многоточечного шаблона.</td>
</tr>
<tr class="even">
<td>EXPOSUREMETERING_CENTERSPOT</td>
<td>Установите экспозицию на основе центральной точки.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING_MODE"></span><span id="wia_dpc_focus_metering_mode"></span><dl> <dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>камерадевицефокусметерингмоде</dt> </dl></td>
<td style="text-align: left;"><p>Указывает режим, используемый камерой для автоматического регулирования фокуса.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>В следующей таблице приведены две константы, допустимые для этого свойства.</p>

<table>
<thead>
<tr class="header">
<th>Режим измерения фокуса</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FOCUSMETERING_CENTERSPOT</td>
<td>Регулировка фокуса на основе центральной точки.</td>
</tr>
<tr class="even">
<td>FOCUSMETERING_MULTISPOT</td>
<td>Настройка фокуса на основе многоточечного шаблона.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_DISTANCE"></span><span id="wia_dpc_focus_distance"></span><dl> <dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>камерадевицефокусдистанце</dt> </dl></td>
<td style="text-align: left;"><p>Расстояние в миллиметрах между плоскостью захвата изображения цифровой камеры и точкой фокусировки. Значение 0xFFFF соответствует параметру, превышающему 655 метров.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCAL_LENGTH"></span><span id="wia_dpc_focal_length"></span><dl> <dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>камерадевицефокалленгс</dt> </dl></td>
<td style="text-align: left;"><p>35mm-эквивалентная Длина фокуса. Значения этого свойства соответствуют фокусной длине в миллиметрах, умноженной на 100. Фокусная длина определяет оптический масштаб.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_RGB_GAIN"></span><span id="wia_dpc_rgb_gain"></span><dl> <dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>камерадевицергбгаин</dt> </dl></td>
<td style="text-align: left;"><p>Строка в Юникоде, заканчивающаяся нулем, которая представляет собой усиление красного, зеленого и синего коэффициента, применяемое к данным изображения соответственно. Например, &quot; 4:25:50 &quot; представляет красную усиление 4, зеленое усиление 25 и синее усиление 50.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_WHITE_BALANCE"></span><span id="wia_dpc_white_balance"></span><dl> <dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>камерадевицевхитебаланце</dt> </dl></td>
<td style="text-align: left;"><p>Указывает, как цветовые каналы плотности цифровых камер.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Ниже приведен список возможных значений для этого свойства.</p>

<table>
<thead>
<tr class="header">
<th>Баланс белого</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WHITEBALANCE_MANUAL</td>
<td>Белый баланс задается непосредственно с помощью свойства <strong>WIA_DPC_RGB_GAIN</strong> .</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_AUTO</td>
<td>Камера использует автоматический механизм для установки баланса белого.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_ONEPUSH_AUTO</td>
<td>Камера определяет параметр баланс белого, когда пользователь нажимает кнопку захвата, указывая камеру на белой поверхности.</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_DAYLIGHT</td>
<td>Камера устанавливает баланс белого по значению, подходящему для использования в летних условиях.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_FLORESCENT</td>
<td>Камера устанавливает баланс белого по значению, подходящему для использования с дневным источником освещения.</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_TUNGSTEN</td>
<td>Камера устанавливает баланс белого на значение, подходящее для использования с источником освещения тунгстен.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_FLASH</td>
<td>Камера устанавливает баланс белого на значение, подходящее для использования с электронной Flash.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_UPLOAD_URL"></span><span id="wia_dpc_upload_url"></span><dl> <dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>камерадевицеуплоадурл</dt> </dl></td>
<td style="text-align: left;"><p>Описывает URL-адрес. URL-адрес, описываемый этим пророперти, — это один из следующих сценариев, в который можно передать изображения или объекты после их получения с устройства.</p>
<ul>
<li>Приложение WIA считывает это свойство и позволяет пользователю автоматически отправлять изображения по URL-адресу.</li>
<li>Приложение задает URL-адрес, а другие устройства (киоски и т. д.) используют это свойство.</li>
</ul>
<p>Microsoft Windows не передает образы сами по себе.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ARTIST"></span><span id="wia_dpc_artist"></span><dl> <dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>камерадевицеартист</dt> </dl></td>
<td style="text-align: left;"><p>Имя владельца (текущего пользователя) устройства. Устройство использует это свойство для заполнения поля исполнителя во всех изображениях EXIF, которые он захватывает.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_COPYRIGHT_INFO"></span><span id="wia_dpc_copyright_info"></span><dl> <dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>камерадевицекопиригхтинфо</dt> </dl></td>
<td style="text-align: left;"><p>Уведомление об авторских правах. Устройство использует это свойство для заполнения поля Copyright в каждом образе EXIF, который он захватывает.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                |
| Header<br/>                   | <dl> <dt>Виадеф. h</dt> </dl> |



 

 




