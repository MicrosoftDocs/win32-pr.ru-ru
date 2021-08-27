---
description: следующие константы указывают допустимый набор свойств элемента сканера Windows изображений (WIA).
ms.assetid: c7c5b10b-81e8-4a30-b20a-ea187724ddd4
title: Константы свойства элемента сканера WIA (Виадеф. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPS_AUTO_DESKEW
- WIA_IPS_BRIGHTNESS
- WIA_IPS_CONTRAST
- WIA_IPS_CUR_INTENT
- WIA_IPS_DESKEW_X
- WIA_IPS_DESKEW_Y
- WIA_IPS_DOCUMENT_HANDLING_SELECT
- WIA_IPS_FILM_NODE_NAME
- WIA_IPS_FILM_SCAN_MODE
- WIA_IPS_INVERT
- WIA_IPA_ITEMS_STORED
- WIA_IPS_LAMP
- WIA_IPS_LAMP_AUTO_OFF
- WIA_IPS_MAX_HORIZONTAL_SIZE
- WIA_IPS_MAX_VERTICAL_SIZE
- WIA_IPS_MIN_HORIZONTAL_SIZE
- WIA_IPS_MIN_VERTICAL_SIZE
- WIA_IPS_MIRROR
- WIA_IPS_OPTICAL_XRES
- WIA_IPS_OPTICAL_YRES
- WIA_IPS_ORIENTATION
- WIA_IPS_PAGE_SIZE
- WIA_IPS_PAGE_HEIGHT
- WIA_IPS_PAGE_WIDTH
- WIA_IPS_PAGES
- WIA_IPS_PHOTOMETRIC_INTERP
- WIA_IPS_PREVIEW
- WIA_IPS_PREVIEW_TYPE
- WIA_IPS_ROTATION
- WIA_IPS_SEGMENTATION
- WIA_IPS_SHEET_FEEDER_REGISTRATION
- WIA_IPS_SHOW_PREVIEW_CONTROL
- WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION
- WIA_IPS_THRESHOLD
- WIA_IPS_TRANSFER_CAPABILITIES
- WIA_IPA_UPLOAD_ITEM_SIZE
- WIA_IPS_WARM_UP_TIME
- WIA_IPS_XEXTENT
- WIA_IPS_XPOS
- WIA_IPS_XRES
- WIA_IPS_XSCALING
- WIA_IPS_YEXTENT
- WIA_IPS_YPOS
- WIA_IPS_YRES
- WIA_IPS_YSCALING
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 3202a4ae6bec7808d2d71fe890f248e6b4d3c397
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624770"
---
# <a name="scanner-wia-item-property-constants"></a>Константы свойства элемента сканера WIA

следующие константы указывают допустимый набор свойств элемента сканера Windows изображений (WIA).

Префикс "WIA- \_ адреса \_ " указывает свойство элемента для устройств сканера и является соглашением об именовании, используемым в C/C++. Для сценариев эти константы используют префикс "Сканнерпиктуре" и являются частью перечислимого типа [виаитемпропертид](-wia-wiaitempropertyid.md) . Соответствующее имя элемента из этого перечисления скриптов отображается в круглых скобках рядом с именем константы C/C++ в следующем списке.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Константа/значение</th>
<th >Описание:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><span id="WIA_IPS_AUTO_DESKEW"></span><span id="wia_ips_auto_deskew"></span><dl> <dt><strong>WIA_IPS_AUTO_DESKEW</strong></dt> <dt>сканнерпиктуреаутодескев</dt> </dl></td>
<td ><blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
<br/> Включает или выключает автоматический декоса.<br/> Необязательно только для WIA_CATEGORY_FEEDER.<br/> Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a><br/> В следующей таблице приведены константы, допустимые для этого свойства. 
<table>
<thead>
<tr class="header">
<th>Константа</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_AUTO_DESKEW_ON</td>
<td>Включите автоматический декоса.</td>
</tr>
<tr class="even">
<td>WIA_AUTO_DESKEW_OFF</td>
<td>Отключите автоматический декоса.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_BRIGHTNESS"></span><span id="wia_ips_brightness"></span><dl> <dt><strong>WIA_IPS_BRIGHTNESS</strong></dt> <dt>сканнерпиктуребригхтнесс</dt> </dl></td>
<td ><p>Значения яркости изображения, доступные в сканере.</p>
<p>Содержит текущую настройку яркости оборудования для устройства. Приложение задает для этого свойства значение яркости оборудования. Минидривер создает и поддерживает это свойство.</p>
<p>Значения должны сопоставляться в диапазоне от-1000 до 1000, где 1000 соответствует максимальной яркости, 0 соответствует стандартной яркости, а-1000 соответствует минимальной яркости.</p>
<p>Требуется для всех элементов в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK и WIA_CATEGORY_FILM. Необязательно, но рекомендуется для WIA_CATEGORY_FINISHED_FILE элементов, поддерживающих предварительный просмотр.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_CONTRAST"></span><span id="wia_ips_contrast"></span><dl> <dt><strong>WIA_IPS_CONTRAST</strong></dt> <dt>сканнерпиктуреконтраст</dt> </dl></td>
<td ><p>Содержит текущую настройку аппаратной контрастности для устройства. Приложение задает для этого свойства значение контрастности оборудования. Минидривер создает и поддерживает это свойство.</p>
<p>Значения должны сопоставляться в диапазоне от-1000 до 1000, где-1000 соответствует минимальному контрасту, 0 соответствует нормальным контрастам, а 1000 соответствует максимальной контрастности.</p>
<p>Требуется для всех элементов в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK и WIA_CATEGORY_FILM. Необязательно, но рекомендуется для WIA_CATEGORY_FINISHED_FILE элементов, поддерживающих предварительный просмотр.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_CUR_INTENT"></span><span id="wia_ips_cur_intent"></span><dl> <dt><strong>WIA_IPS_CUR_INTENT</strong></dt> <dt>сканнерпиктурекуринтент</dt> </dl></td>
<td ><p>Содержит текущие параметры намерения. Минидривер создает и поддерживает это свойство.</p>
<p>Требуется для всех элементов с включенным приобретением; то есть элементы в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK и WIA_CATEGORY_FILM. Он не поддерживается для WIA_CATEGORY_FINISHED_FILE и WIA_CATEGORY_FOLDER элементов.</p>
<p>Тип: <strong>VT_I4</strong> доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_FLAGS</a></p>
<p>Драйвер использует их для предустановки свойств элемента на основе предполагаемого использования образа приложением. Это может быть, например, максимальное качество, минимальный размер и т. д.</p>
<p>Драйвер выбирает битовую глубину в точках на дюйм, а другие параметры, которые он определяет, подходят для выбранной цели. Приложение может считать текущие параметры, чтобы определить, какие свойства были изменены. Приложение задает это свойство для автоматической установки свойств WIA для конкретной цели приобретения. Это свойство является обязательным для всех сканеров.</p>
<p>Приложение задает это свойство для автоматического задания свойств WIA для конкретной цели приобретения.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Флаги можно сочетать с оператором побитового <strong>или</strong> , но изображение не может одновременно быть в оттенках серого и Color.
</blockquote>
</div>
<div>
 
</div>
<p>Это свойство является обязательным для всех сканеров.</p>
<p>В следующей таблице содержатся флаги типа Image и их определения. Эти флаги используются для задания того, какой тип изображения предназначен: цвет, оттенки серого и т. д.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Предназначенные флаги типа образа</th>
<th>Описание:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_INTENT_NONE</td>
<td>Значение по умолчанию. Намерение не указано.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_IMAGE_TYPE_COLOR</td>
<td>Приложение планирует подготовить устройство для цветной проверки.</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_IMAGE_TYPE_GRAYSCALE</td>
<td>Приложение планирует подготовить устройство для сканирования в градациях серого.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_IMAGE_TYPE_TEXT</td>
<td>Приложение планирует подготовить устройство для сканирования текста.</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_IMAGE_TYPE_MASK</td>
<td>Маска для всех флагов типа изображения.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>В следующей таблице содержатся флаги качества и размера, а также их определения. Эти флаги используются для настройки требуемого уровня качества.</p>

<table>
<thead>
<tr class="header">
<th>Предполагаемый размер изображения/флаги качества</th>
<th>Описание:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_INTENT_MINIMIZE_SIZE</td>
<td>Приложение планирует подготовить устройство к сканированию образа, который является незначительным сканированием.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_MAXIMIZE_QUALITY</td>
<td>Приложение планирует подготовить устройство для сканирования высококачественного изображения.</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_SIZE_MASK</td>
<td>Этот флаг является маской для всех флагов размера и качества.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_BEST_PREVIEW</td>
<td>Приложение планирует подготовить устройство для сканирования предварительной версии.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_DESKEW_X"></span><span id="wia_ips_deskew_x"></span><dl> <dt><strong>WIA_IPS_DESKEW_X</strong></dt> <dt>сканнерпиктуредескевкс</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Содержит число пикселей в направлении по оси x от WIA_IPS_XPOS до координат по оси x верхнего угла изображения, которое необходимо вычислить. Таким образом, в сочетании с WIA_IPS_DESKEW_Y, где два верхних угла наклоненного изображения расположены в ограничивающем прямоугольнике, определяемом WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT и WIA_IPS_YEXTENT. его свойство реализуется драйвером сканера, если он поддерживает деравномерность.</p>
<p>Допустимые значения для WIA_IPS_DESKEW_X должны находиться в диапазоне от 0 до (WIA_IPS_XEXTENT-1). Значение 0 означает, что не следует выполнять декосая.</p>
<p>Это свойство является необязательным для элементов категорий WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER и WIA_CATEGORY_FILM; он недоступен для элементов WIA_CATEGORY_FINISHED_FILE и WIA_CATEGORY_FOLDER.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_DESKEW_Y"></span><span id="wia_ips_deskew_y"></span><dl> <dt><strong>WIA_IPS_DESKEW_Y</strong></dt> <dt>сканнерпиктуредескеви</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Содержит количество пикселей в направлении по оси y от WIA_IPS_YPOS до координат по оси y левого угла изображения, которое нужно деравномерное раскрывающий. Таким образом, в сочетании с WIA_IPS_DESKEW_X, где два верхних угла наклоненного изображения расположены в ограничивающем прямоугольнике, определяемом WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT и WIA_IPS_YEXTENT. Это свойство реализуется драйвером сканера, если он поддерживает деравномерность.</p>
<p>Допустимые значения для WIA_IPS_DESKEW_Y должны находиться в диапазоне от 0 до (WIA_IPS_YEXTENT-1). Значение 0 означает, что не следует выполнять декосая.</p>
<p>Это свойство является необязательным для элементов категорий WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER и WIA_CATEGORY_FILM; он недоступен для элементов WIA_CATEGORY_FINISHED_FILE и WIA_CATEGORY_FOLDER.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_ips_document_handling_select"></span><dl> <dt><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>сканнерпиктуредокуменсандлингселект</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Содержит текущий источник и режим получения сканера. Минидривер создает и поддерживает это свойство.</p>
<p>Приложение считывает это свойство, чтобы определить текущий источник получения сканера или записать это свойство, чтобы задать источник и режим сканера. Кроме того, приложения используют это свойство для включения и отключения функции дуплексного режима.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>В следующей таблице приведены константы, допустимые для этого свойства. </p>
<table>
<thead>
<tr class="header">
<th>Флаги</th>
<th>Описание:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>УСТРОЙСТВА</td>
<td>Сканирование с помощью операций дуплексного устройства. Сканирование обеих сторон документа с помощью общих параметров, настроенных для элемента-податчика (WIA_CATEGORY_FEEDER). ДУПЛЕКСные и ADVANCE_DUPLEX не могут быть заданы одновременно.</td>
</tr>
<tr class="even">
<td>ADVANCED_DUPLEX</td>
<td>Сканирование с использованием отдельных параметров, настроенных для каждого элемента дочернего веб-канала (WIA_CATEGORY_FEEDER_FRONT и WIA_CATEGORY_FEEDER_BACK). ДУПЛЕКСные и ADVANCE_DUPLEX не могут быть заданы одновременно.</td>
</tr>
<tr class="odd">
<td>FRONT_FIRST</td>
<td>Сначала просканируйте передний план документа. Это значение допустимо, если задан ДУПЛЕКСный или ADVANCED_DUPLEX.</td>
</tr>
<tr class="even">
<td>BACK_FIRST</td>
<td>Сначала просканируйте задний план документа. Это значение допустимо, если задан ДУПЛЕКСный или ADVANCED_DUPLEX.</td>
</tr>
<tr class="odd">
<td>FRONT_ONLY</td>
<td>Сканирование только на передней панели.</td>
</tr>
<tr class="even">
<td>BACK_ONLY</td>
<td>Проверка только обратного просмотра. Это значение допустимо, если задан ДУПЛЕКСный или ADVANCED_DUPLEX.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_FILM_NODE_NAME"></span><span id="wia_ips_film_node_name"></span><dl> <dt><strong>WIA_IPS_FILM_NODE_NAME</strong></dt> <dt>сканнерпиктурефилмноденаме</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Включает спецификацию конкретного вложения для сканирования пленки при наличии более одного.</p>
<p>Это свойство требуется для элементов WIA_CATEGORY_FILM, если имеется несколько элементов для сканирования на пленке. Если устройство поддерживает только один элемент фотопленки, это свойство является необязательным.</p>
<p>Тип: <strong>VT_BSTR</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Допустимые значения: BSTR должен иметь вид @ResourceBinary ,- <ResourceID> чтобы разрешить локализацию, так как эта строка будет предоставляться пользователю через пользовательский интерфейс сканирования пленки.</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_FILM_SCAN_MODE"></span><span id="wia_ips_film_scan_mode"></span><dl> <dt><strong>WIA_IPS_FILM_SCAN_MODE</strong></dt> <dt>сканнерпиктурефилмсканмоде</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Включает настройку текущей проверки пленки.</p>
<p>Это свойство является обязательным для элемента WIA_CATEGORY_FILM.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>В следующей таблице приведены константы, допустимые для этого свойства. </p>
<table>
<thead>
<tr class="header">
<th>Константа</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_FILM_COLOR_SLIDE</td>
<td>Сканирование для цветного слайда.</td>
</tr>
<tr class="even">
<td>WIA_FILM_COLOR_NEGATIVE</td>
<td>Сканировать для отрицательного цвета.</td>
</tr>
<tr class="odd">
<td>WIA_FILM_BW_NEGATIVE</td>
<td>Проверка на наличие черного и белого отрицательных результатов.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_INVERT"></span><span id="wia_ips_invert"></span><dl> <dt><strong>WIA_IPS_INVERT</strong></dt> <dt>сканнерпиктуреинверт</dt> </dl></td>
<td ><p>Зарезервировано для будущего использования и в настоящее время не реализовано.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>сканнерпиктуреинверт</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Указывает, сколько элементов хранится в элементе WIA_CATEGORY_FOLDER.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_LAMP"></span><span id="wia_ips_lamp"></span><dl> <dt><strong>WIA_IPS_LAMP</strong></dt> <dt>сканнерпиктуреламп</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Включает или выключает лампу сканера.</p>
<p>Необязательно для элементов WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER и WIA_CATEGORY_FILM и рекомендуется для WIA_CATEGORY_FILM.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>В следующей таблице приведены константы, допустимые для этого свойства. </p>
<table>
<thead>
<tr class="header">
<th>Константа</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_LAMP_ON</td>
<td>Включите лампу.</td>
</tr>
<tr class="even">
<td>WIA_LAMP_OFF</td>
<td>Выключите лампу.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_LAMP_AUTO_OFF"></span><span id="wia_ips_lamp_auto_off"></span><dl> <dt><strong>WIA_IPS_LAMP_AUTO_OFF</strong></dt> <dt>сканнерпиктурелампаутуфф</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Задает максимальное время, в течение которого должна удерживаться лампа, если сканер не используется.</p>
<p>Необязательно для элементов WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER и WIA_CATEGORY_FILM и рекомендуется для WIA_CATEGORY_FILM.</p>
<p>Тип: <strong>VT_UI4</strong>, доступ: чтение и запись, допустимые значения: 0 — 0xfff секунд</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_MAX_HORIZONTAL_SIZE"></span><span id="wia_ips_max_horizontal_size"></span><dl> <dt><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></dt> <dt>сканнерпиктуремаксхоризонталсизе</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Задает максимальную ширину в тысячах дюйма, которая просматривается на горизонтальной оси (X) при текущем разрешении. В зависимости от типа элемента это может быть ширина податчика листа или сканера.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_MAX_VERTICAL_SIZE"></span><span id="wia_ips_max_vertical_size"></span><dl> <dt><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></dt> <dt>сканнерпиктуремаксвертикалсизе</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Задает максимальную высоту в тысячах дюйма, которая просматривается на вертикальной оси (Y) при текущем разрешении. Это может быть высота податчика листа или сканера в соответствии с типом элемента.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_MIN_HORIZONTAL_SIZE"></span><span id="wia_ips_min_horizontal_size"></span><dl> <dt><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></dt> <dt>сканнерпиктуреминхоризонталсизе</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Задает минимальную ширину в тысячах дюйма, которая просматривается на горизонтальной оси (X) при текущем разрешении.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_MIN_VERTICAL_SIZE"></span><span id="wia_ips_min_vertical_size"></span><dl> <dt><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></dt> <dt>сканнерпиктуреминвертикалсизе</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Задает минимальную высоту (в тысячах) дюйма, которая просматривается по вертикальной оси (Y) при текущем разрешении.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_MIRROR"></span><span id="wia_ips_mirror"></span><dl> <dt><strong>WIA_IPS_MIRROR</strong></dt> <dt>сканнерпиктуремиррор</dt> </dl></td>
<td ><p>Зарезервировано для будущего использования и в настоящее время не реализовано.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_OPTICAL_XRES"></span><span id="wia_ips_optical_xres"></span><dl> <dt><strong>WIA_IPS_OPTICAL_XRES</strong></dt> <dt>сканнерпиктуреоптикалксрес</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Горизонтальное разрешение оптического экрана. Самое высокое поддерживаемое оптическое разрешение по горизонтали в DPI. Это свойство имеет одно значение. Это не список всех разрешений, которые могут быть созданы устройством. Вместо этого это разрешение оптики устройства. Минидривер создает и поддерживает это свойство. Это свойство является обязательным для всех элементов.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_OPTICAL_YRES"></span><span id="wia_ips_optical_yres"></span><dl> <dt><strong>WIA_IPS_OPTICAL_YRES</strong></dt> <dt>сканнерпиктуреоптикалирес</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Вертикальное оптическое разрешение. Максимальное поддерживаемое вертикальное оптическое разрешение в DPI. Это свойство имеет одно значение. Это не список всех разрешений, создаваемых устройством. Вместо этого это разрешение оптики устройства. Минидривер создает и поддерживает это свойство. Это свойство является обязательным для всех элементов.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_ORIENTATION"></span><span id="wia_ips_orientation"></span><dl> <dt><strong>WIA_IPS_ORIENTATION</strong></dt> <dt>сканнерпиктуреориентатион</dt> </dl></td>
<td ><p>Указывает текущую ориентацию сканируемых документов. Минидривер создает и поддерживает это свойство.</p>
<p>Приложение задает это свойство, чтобы определить исходную ориентацию страницы или изображения, которые должны быть получены. Сведения об использовании WIA_IPS_ORIENTATION см. в разделе <strong>WIA_IPS_PAGE_SIZE</strong>.</p>
<div class="alert">
<blockquote>
[!Note]<br />
WIA_IPS_ORIENTATION указывает на расположение документа, который будет проверяться на сканере или в податчике. Это ориентация документа относительно направления сканирования. WIA_IPS_ROTATION относится к повороту, который применяется к изображению после его сканирования, непосредственно перед передачей изображения в приложение.
</blockquote>
</div>
<div>
 
</div>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>В следующей таблице приведены четыре константы, допустимые для этого свойства.</p>

<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Определение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>КНИЖНОЙ ориентации</td>
<td>0 градусов.</td>
</tr>
<tr class="even">
<td>СВЕРХУ</td>
<td>коэффициент в 90 градусов — поворот по часовой стрелке относительно КНИЖной ориентации.</td>
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

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_PAGE_SIZE"></span><span id="wia_ips_page_size"></span><dl> <dt><strong>WIA_IPS_PAGE_SIZE</strong></dt> <dt>сканнерпиктурепажесизе</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Содержит размер страницы, для которой в настоящий момент выбрана проверка. Приложение задает это свойство, чтобы выбрать размеры сканируемой страницы. Минидривер создает и поддерживает это свойство.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Константы, которые можно использовать с этим свойством, см. в разделе <a href="-wia-wia2-pagesizeconstants.md"><strong>константы размера страницы WIA 2,0</strong></a>. Обратите внимание на следующие нефиксированные размеры, в частности: </p>
<table>
<thead>
<tr class="header">
<th>Значение</th>
<th>Определение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PAGE_CUSTOM</td>
<td>Определяется значениями свойств <strong>WIA_IPS_PAGE_HEIGHT</strong> и <strong>WIA_IPS_PAGE_WIDTH</strong> .</td>
</tr>
<tr class="even">
<td>WIA_PAGE_AUTO</td>
<td>Размер страницы определяется устройством автоматически.</td>
</tr>
<tr class="odd">
<td>WIA_PAGE_CUSTOM_BASE</td>
<td>Пользовательский размер страницы, размеры которого уже известны приложению и драйверу устройства.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Значение свойства <strong>WIA_IPS_ORIENTATION</strong> определяет ориентацию текущей выбранной страницы. Свойства <strong>WIA_IPS_PAGE_WIDTH</strong> и <strong>WIA_IPS_PAGE_HEIGHT</strong> сообщают о размерах страницы в тысячах дюйма. Эти свойства должны быть согласованы с <strong>WIA_IPS_XEXTENT</strong> и <strong>WIA_IPS_YEXTENT</strong>, которые содержат размеры страницы в пикселях.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Допустимые значения типа WIA_PROP_LIST зависят от допустимых параметров свойства <strong>WIA_IPS_ORIENTATION</strong> . Если, например, устройство не может сканировать альбомные документы с помощью параметра WIA_PAGE_A4, WIA_PAGE_A4 не является допустимым значением свойства <strong>WIA_IPS_PAGE_SIZE</strong> , если <strong>WIA_IPS_ORIENTATION</strong> установлен в альбомную ориентацию.
</blockquote>
</div>
<div>
 
</div>
<p>Если приложение устанавливает <strong>WIA_IPS_PAGE_SIZE</strong> любое значение, отличное от трех в таблице выше, минидривер должен скорректировать значения <strong>WIA_IPS_PAGE_WIDTH</strong> и <strong>WIA_IPS_PAGE_HEIGHT</strong> в размерах страницы в тысячах дюйма. Он также должен скорректировать значения <strong>WIA_IPS_XEXTENT</strong> и <strong>WIA_IPS_YEXTENT</strong> к размерам страницы в пикселях.</p>
<p>Если параметр экстента (<strong>WIA_IPS_XEXTENT</strong> или <strong>WIA_IPS_YEXTENT</strong>) изменяется на значение, не совпадающее с текущим параметром размера страницы, минидривер должен изменить значение свойства <strong>WIA_IPS_PAGE_SIZE</strong> на WIA_PAGE_CUSTOM. Минидривер также должен изменить <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a> или <strong>WIA_IPS_PAGE_HEIGHT</strong> в соответствии с новым параметром экстента.</p>
<p>Если параметр <strong>WIA_IPS_ORIENTATION</strong> имеет значение альбомная, параметры экстента будут передаваться относительно их обычных значений. Например, если приложение устанавливает <strong>WIA_IPS_PAGE_SIZE</strong> в WIA_PAGE_A4, минидривер устанавливает для <strong>WIA_IPS_PAGE_WIDTH</strong> значение 11692, а <strong>WIA_IPS_PAGE_HEIGHT</strong> — 8267. (Минидривер также должен соответствующим образом скорректировать <strong>WIA_IPS_XEXTENT</strong> и <strong>WIA_IPS_YEXTENT</strong> .)</p>
<div class="alert">
<blockquote>
[!Note]<br />
Если <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_SIZE</strong></a> имеет значение WIA_PAGE_CUSTOM, параметр ориентации не используется для определения размеров сканируемой страницы.
</blockquote>
</div>
<div>
 
</div>
<p>Минидривер отвечает за обеспечение соответствия свойства <strong>WIA_IPS_ORIENTATION</strong> с текущей областью выбора. Если приложение изменяет значение <strong>WIA_IPS_ORIENTATION</strong> на другое, недопустимое для текущего выбранного размера страницы, минидривер должен изменить значение <strong>WIA_IPS_PAGE_SIZE</strong> на размер страницы, поддерживаемый новым значением ориентации.</p>
<p>Если приложение задает для свойства <strong>WIA_IPS_PAGE_SIZE</strong> значение WIA_PAGE_CUSTOM, то область текущего выбора не изменяется. WIA минидривер должен получить текущий макет изображения, начиная с текущих параметров свойств <strong>WIA_IPS_XPOS</strong> и <strong>WIA_IPS_YPOS</strong> . Если параметр размера страницы приводит к выделению области выделения, находящегося за пределами испытательного сканера, минидривер должен автоматически скорректировать значения <strong>WIA_IPS_XPOS</strong> и <strong>WIA_IPS_YPOS</strong> свойства на допустимые параметры. Если свойства <strong>WIA_IPS_PAGE_SIZE</strong> и <strong>WIA_IPS_ORIENTATION</strong> задаются одновременно и являются недопустимыми при их применении в сочетании, минидривер не должен возвращать параметры приложения, возвращая ошибку в <a href="https://msdn.microsoft.com/library/ms794145.aspx">ивиаминидрв::d рввалидатеитемпропертиес</a>.</p>
<p>В следующих четырех примерах показаны различные сценарии <strong>WIA_IPS_PAGE_SIZE</strong> .</p>
<ol>
<li>Драйвер сообщает о параметрах.</li>
<li>Приложение задает для свойства <strong>WIA_IPS_PAGE_SIZE</strong> значение WIA_PAGE_LETTER.</li>
<li>Приложение устанавливает для свойства <strong>WIA_IPS_ORIENTATION</strong> значение альбомная ориентация.</li>
<li>Приложение изменяет свойство <strong>WIA_IPS_XEXTENT</strong> на меньшее значение.</li>
</ol>
<p><strong>Пример 1. минидривер сообщает о параметрах</strong></p>
<p>В следующем примере минидривер задает настраиваемую область выбора до того, как приложение установит все свойства WIA. В этом случае область выбора представляет все стекло.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_WIDTH = 11500
WIA_IPS_PAGE_HEIGHT = 14000
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
<p><strong>Пример 2. приложение задает</strong> <strong></strong><strong>для свойства</strong> WIA_IPS_PAGE_SIZE значение WIA_PAGE_LETTER  </p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_PAGE_HEIGHT = 11000
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
<p><strong>Пример 3. приложение задает</strong> <strong></strong><strong>для свойства WIA_IPS_ORIENTATION значение альбомная</strong>  </p>
<p>Физическая среда должна иметь возможность получить страницу, которая изначально была в альбомной ориентации.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_HEIGHT = 11000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
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
<p><strong>Пример 4. приложение изменяет</strong> свойство <strong>WIA_IPS_XEXTENT</strong> <strong>на меньшее значение</strong></p>
<p>В следующем примере приложение изменяет свойство <strong>WIA_IPS_XEXTENT</strong> на 1000. Минидривер должен предположить, что новое значение, содержащееся в <strong>WIA_IPS_XEXTENT</strong> , больше не является допустимым для свойства <strong>WIA_IPS_PAGE_SIZE</strong> и, таким образом, изменит <strong>WIA_IPS_PAGE_SIZE</strong> на WIA_PAGE_CUSTOM. Минидривер также должен корректировать <strong>WIA_IPS_PAGE_WIDTH</strong>.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_HEIGHT = 10000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
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
<td ><span id="WIA_IPS_PAGE_HEIGHT"></span><span id="wia_ips_page_height"></span><dl> <dt><strong>WIA_IPS_PAGE_HEIGHT</strong></dt> <dt>сканнерпиктурепажехеигхт</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Содержит высоту (в тысячах дюйма) текущей выбранной страницы. Минидривер создает и поддерживает свойство <strong>WIA_IPS_PAGE_HEIGHT</strong> . Приложение считывает это свойство, чтобы определить физические размеры сканируемой страницы. Если параметры экстента отличаются от размеров известных страниц, это свойство сообщает высоту страницы, для которой свойство <strong>WIA_IPS_PAGE_SIZE</strong> имеет значение WIA_PAGE_CUSTOM (которое является значением свойства <strong>WIA_IPS_PAGE_SIZE</strong> ). <strong>WIA_IPS_PAGE_HEIGHT</strong> должны быть синхронизированы с <strong>WIA_IPS_XEXTENT</strong>, которая сообщает высоту сканируемой страницы в пикселях.</p>
<p>Это свойство является обязательным для WIA_CATEGORY_FEEDER элементов.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_PAGE_WIDTH"></span><span id="wia_ips_page_width"></span><dl> <dt><strong>WIA_IPS_PAGE_WIDTH</strong></dt> <dt>сканнерпиктурепажевидс</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Содержит ширину текущей выбранной страницы в тысячах дюйма. Приложение считывает это свойство, чтобы определить физические размеры сканируемой страницы. Если параметры экстента отличаются от размеров известных страниц, это свойство сообщает ширину страницы, для которой свойство <strong>WIA_IPS_PAGE_SIZE</strong> имеет значение WIA_PAGE_CUSTOM. <strong>WIA_IPS_PAGE_WIDTH</strong> должны быть синхронизированы со значением <strong>WIA_IPS_XEXTENT</strong>, которое показывает ширину сканируемой страницы в пикселях. Минидривер создает и поддерживает это свойство.</p>
<p>Это свойство является обязательным для WIA_CATEGORY_FEEDER элементов.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_PAGES"></span><span id="wia_ips_pages"></span><dl> <dt><strong>WIA_IPS_PAGES</strong></dt> <dt>сканнерпиктурепажес</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Содержит текущее число страниц, получаемых из автоматического устройства подачи документов. Минидривер создает и поддерживает это свойство.</p>
<p>Тип: <strong>VT_I4</strong>; Доступ: чтение и запись; Допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> это ноль до максимального количества страниц, которое может сканировать сканер. Значение ALL_PAGES (= 0), если сканер может сканироваться непрерывно.</p>
<p>Приложение считывает это свойство для определения емкости страницы устройства подачи документов. Приложение также задает для этого свойства число страниц, которое он будет сканировать.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Если включен дуплексный режим (<strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong> установлен в "Feed" | ДУПЛЕКС | ADVANCED_DUPLEX) <strong>WIA_IPS_PAGES</strong> по-прежнему равно числу сканируемых страниц.
</blockquote>
</div>
<div>
 
</div>
<p>Один лист бумаги автоматически будет содержать две страницы, если ДУПЛЕКСный режим включен, даже если обратная сторона страницы пуста.</p>
<p>Если задать для <strong>WIA_IPS_PAGES</strong> значение 1, то сканер будет обрабатывать одну сторону страницы. Рекомендуется, если сканер не может сканировать только одну сторону страницы в режиме дуплекса, вы изменяете значение <strong>WIA_IPS_PAGES</strong> для элемента Inc элемента Range структуры WIA_PROPERTY_INFO на 2. Это значение сигнализирует приложению, что оно должно запрашивать страницы, кратные двум. Значение ALL_PAGES (= 0) означает, что будут проверяться <em>все</em> страницы, загруженные в данный момент в устройство подачи документов.</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_PHOTOMETRIC_INTERP"></span><span id="wia_ips_photometric_interp"></span><dl> <dt><strong>WIA_IPS_PHOTOMETRIC_INTERP</strong></dt> <dt>сканнерпиктурефотометриЦинтерп</dt> </dl></td>
<td ><p>Содержит текущее значение для белых и черных пикселей. Минидривер создает и поддерживает это свойство.</p>
<p>Приложение считывает это значение, чтобы определить значение белого или черного (в зависимости от того, что делает приложение).</p>
<p>Требуется для всех включенных приобретений или сохраненных элементов; то есть элементы в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE и WIA_CATEGORY_FILM. Он не поддерживается для WIA_CATEGORY_FOLDER элементов.</p>
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
<td>WIA_PHOTO_WHITE_0</td>
<td>БЕЛЫЙ цвет равен 0, а черный — 1.</td>
</tr>
<tr class="even">
<td>WIA_PHOTO_WHITE_1</td>
<td>БЕЛЫЙ цвет равен 1, а черный — 0.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_PREVIEW"></span><span id="wia_ips_preview"></span><dl> <dt><strong>WIA_IPS_PREVIEW</strong></dt> <dt>сканнерпиктурепревиев</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Указывает режим предварительного просмотра для устройства. Приложение задает это свойство, чтобы перевести устройство в режим предварительного просмотра.</p>
<p>Это свойство является обязательным для элементов WIA_CATEGORY_FLATBED и WIA_CATEGORY_FILM, необязательно для элемента WIA_CATEGORY_FEEDER.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>В следующей таблице приведены константы, допустимые для этого свойства. </p>
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
<tr class="even">
<td ><span id="WIA_IPS_PREVIEW_TYPE"></span><span id="wia_ips_preview_type"></span><dl> <dt><strong>WIA_IPS_PREVIEW_TYPE</strong></dt> <dt>сканнерпиктурепревиевтипе</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Указывает, можно ли обновить существующее изображение предварительного просмотра во время просмотра изображения (в ответ на изменение свойств WIA_IPA_DATATYPE или WIA_IPA_DEPTH).</p>
<p>Это свойство является необязательным для всех элементов с включенным приобретением, поддерживающих предварительные проверки. то есть WIA_IPS_PREVIEW поддерживается с WIA_PREVIEW_SCAN. К ним относятся элементы типов WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK и WIA_CATEGORY_FILM.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>В следующей таблице приведены константы, допустимые для этого свойства. </p>
<table>
<thead>
<tr class="header">
<th>Константа</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_ADVANCED_PREVIEW</td>
<td>Возможно обновление существующего образа.</td>
</tr>
<tr class="even">
<td>WIA_BASIC_PREVIEW</td>
<td>Необходимо выполнить еще одну предварительную проверку, так как обновление существующего образа невозможно.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_ROTATION"></span><span id="wia_ips_rotation"></span><dl> <dt><strong>WIA_IPS_ROTATION</strong></dt> <dt>сканнерпиктуреротатион</dt> </dl></td>
<td ><p>Содержит текущий параметр вращения, если он реализован. Минидривер создает и поддерживает это свойство.</p>
<p>Приложение задает это свойство, чтобы сообщить драйверу, какой объем (если вообще) нужно повернуть изображение, прежде чем драйвер вернет его в приложение.</p>
<div class="alert">
<blockquote>
[!Note]<br />
WIA_IPS_ORIENTATION указывает на расположение документа, который будет проверяться на сканере или в податчике. Это ориентация документа относительно направления сканирования. WIA_IPS_ROTATION относится к повороту, который применяется к изображению после его сканирования, непосредственно перед передачей изображения в приложение.
</blockquote>
</div>
<div>
 
</div>
<p>WIA-минидривер отвечает за вращение данных изображения перед их отправкой обратно в приложение. Приложение несет ответственность за проверку заголовков изображений, чтобы увидеть только что повернутые значения.</p>
<p>Существует значительная путаница, связанная с разрешением воздействия вращения на область выбора текущего изображения (которая определяется свойствами <strong>WIA_IPS_XPOS</strong>, <strong>WIA_IPS_YPOS</strong>, <strong>WIA_IPS_XEXTENT</strong> и <strong>WIA_IPS_YEXTENT</strong> ).</p>
<p><em>Область выбора</em> относится к выбранной области физической сканера, из которой запрашивается изображение. <strong>WIA_IPS_ROTATION</strong> не изменяет область выбора. Драйвер применяет поворот против часовой стрелки в соответствии с <strong>WIA_IPS_ROTATION</strong> только после того, как драйвер приобрел соответствующую область выбора. <strong>WIA_IPS_ROTATION</strong> влияет на размеры выходного изображения, поэтому эти измерения должны быть отражены в заголовке данных полученного изображения.</p>
<p>Необязательно для всех элементов с включенным приобретением; то есть элементы в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK и WIA_CATEGORY_FILM.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Определены следующие константы вращения.</p>

<table>
<thead>
<tr class="header">
<th>Константа</th>
<th>Определение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>КНИЖНОЙ ориентации</td>
<td>Драйвер не будет поворачивать образ.</td>
</tr>
<tr class="even">
<td>СВЕРХУ</td>
<td>Драйвер Tне поворачивает изображение 90 градусов против часовой стрелки.</td>
</tr>
<tr class="odd">
<td>ROT180</td>
<td>Драйвер поворачивает изображение 180 градусов против часовой стрелки.</td>
</tr>
<tr class="even">
<td>ROT270</td>
<td>Драйвер поворачивает изображение 270 градусов против часовой стрелки.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_SEGMENTATION"></span><span id="wia_ips_segmentation"></span><dl> <dt><strong>WIA_IPS_SEGMENTATION</strong></dt> <dt>сканнерпиктуресегментатион</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Указывает, должен ли приложение использовать фильтр сегментации драйвера для сканирования в нескольких регионах. WIA_IPS_SEGMENTATION должны быть реализованы для WIA_CATEGORY_FLATBED и WIA_CATEGORY_FILM элементов, если они поддерживают создание дочерних элементов с фильтром сегментации или если сам драйвер создает дочерние элементы для фиксированных кадров.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
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
<td>WIA_USE_SEGMENTATION_FILTER</td>
<td>Приложение должно использовать фильтр сегментации для сканирования в нескольких регионах.</td>
</tr>
<tr class="even">
<td>WIA_DONT_USE_SEGMENTATION_FILTER</td>
<td>Драйвер создает дочерние элементы для поиска в нескольких регионах. Обычно это происходит, если сканер использует для этой цели фиксированные кадры.</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
Драйвер может поступать с фильтром сегментации, но по-прежнему имеет WIA_IPS_SEGMENTATION WIA_DONT_USE_SEGMENTATION_FILTER для одного из его элементов (например, элемент WIA_CATEGORY_FILM). Это может быть так, если сканер использует фиксированные кадры для сканирования пленки, но не для обычного сканирования из WIA_CATEGORY_FLATBED элементов.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_ips_sheet_feeder_registration"></span><dl> <dt><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>сканнерпиктурешитфидеррегистратион</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
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
<tr class="even">
<td ><span id="WIA_IPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_ips_show_preview_control"></span><dl> <dt><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>сканнерпиктурешовпревиевконтрол</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Указывает, должен ли элемент отображаться в элементе управления предварительной версии. Минидривер создает и поддерживает это свойство.</p>
<p>Необязательно для всех элементов с поддержкой перемещения. Обычно это просто элементы категорий WIA_ITEM_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM и WIA_CATEGORY_FINISHED_FILE.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>В следующей таблице приведены константы, допустимые для этого свойства. </p>
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
<tr class="odd">
<td ><span id="WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION"></span><span id="wia_ips_supports_child_item_creation"></span><dl> <dt><strong>WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION</strong></dt> <dt>сканнерпиктуресуппортсчилдитемкреатион</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Указывает, могут ли приложение (или фильтры) создавать дочерние элементы в текущем элементе.</p>
<p>Необязательно для всех категорий элементов с поддержкой перемещения: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM и даже WIA_CATEGORY_FOLDER. (Если хранилище не поддерживает отправку новых элементов, это свойство должно быть неподдерживаемым или не поддерживаться со значением <strong>false</strong> .)</p>
<p>Элементы, поддерживающие WIA_IPS_SEGMENTATION и WIA_USE_SEGMENTATION_FILTER, также должны поддерживать WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION и иметь значение <strong>true</strong>.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <strong>true</strong> и <strong>false</strong></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_THRESHOLD"></span><span id="wia_ips_threshold"></span><dl> <dt><strong>WIA_IPS_THRESHOLD</strong></dt> <dt>сканнерпиктуресрешолд</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Задает значение градации серого, которое определяет, будет ли при преобразовании изображения в монохромное изображение преобразовано в белый или черный цвет. Пиксели выше порогового значения становятся белыми. Пиксели ниже порогового значения становятся белым.</p>
<p>Это свойство требуется для элементов сбора, поддерживающих сканирование 1 бит и имеющее для свойства WIA_IPA_DATATYPE значение WIA_DATA_THRESHOLD.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_TRANSFER_CAPABILITIES"></span><span id="wia_ips_transfer_capabilities"></span><dl> <dt><strong>WIA_IPS_TRANSFER_CAPABILITIES</strong></dt> <dt>сканнерпиктуретрансферкапабилитиес</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Указывает, способен ли драйвер передавать несколько дочерних элементов в одном вызове передачи.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>Единственное возможное значение для этого свойства — WIA_TRANSFER_CHILDREN_SINGLE_SCAN. Если этот флаг установлен, драйвер способен передавать несколько дочерних элементов в одном вызове функции перемещения. Если флаг не установлен, служба WIA будет рекурсивно проходить по дочерним элементам, а затем переносить каждый из этих элементов.</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>сканнерпиктуреинверт</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Указывает число байтов для отправки для элемента.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_WARM_UP_TIME"></span><span id="wia_ips_warm_up_time"></span><dl> <dt><strong>WIA_IPS_WARM_UP_TIME</strong></dt> <dt>сканнерпиктуревармуптиме</dt> </dl></td>
<td ><p>Указывает максимальное время прогрева (в миллисекундах), необходимое устройству перед запуском операции сканирования. Минидривер создает и поддерживает это свойство.</p>
<p>Приложение может прочитать это свойство, чтобы определить максимальное время прогрева для этого устройства. Затем он может предоставить &quot; диалоговое окно ожидание прогрева устройства &quot; , чтобы сообщить пользователю о том, что ожидание или пауза может произойти до чего-либо.</p>
<p>Это свойство является обязательным для всех элементов с включенным приобретением; то есть элементы в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK и WIA_CATEGORY_FILM.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_XEXTENT"></span><span id="wia_ips_xextent"></span><dl> <dt><strong>WIA_IPS_XEXTENT</strong></dt> <dt>сканнерпиктурексекстент</dt> </dl></td>
<td ><p>Содержит текущую ширину (в пикселях) выбранного изображения для получения. Приложение задает это свойство, чтобы пометить ширину области выбора для получения. Это свойство должно быть согласовано со свойством <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> . Минидривер создает и поддерживает это свойство.</p>
<p>Требуется для всех элементов с включенным приобретением; то есть элементы в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK и WIA_CATEGORY_FILM.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_XPOS"></span><span id="wia_ips_xpos"></span><dl> <dt><strong>WIA_IPS_XPOS</strong></dt> <dt>сканнерпиктурекспос</dt> </dl></td>
<td ><p>Содержит координату x (в пикселях) верхнего левого угла выбранного изображения. Приложение задает это свойство, чтобы пометить левый верхний угол области выделения. Минидривер создает и поддерживает это свойство.</p>
<p>Требуется для всех элементов с включенным приобретением; то есть элементы в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE и WIA_CATEGORY_FILM. Он не поддерживается для WIA_CATEGORY_FOLDER элементов.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_XRES"></span><span id="wia_ips_xres"></span><dl> <dt><strong>WIA_IPS_XRES</strong></dt> <dt>сканнерпиктурексрес</dt> </dl></td>
<td ><p>Содержит текущее разрешение по горизонтали (в пикселях на дюйм) для устройства. Приложение задает это свойство для установки разрешения по горизонтали. Минидривер создает и поддерживает это свойство.</p>
<p>Если для устройства можно задать только одно значение, создайте тип <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> и поместите в него допустимое значение. Это также случай, когда один параметр разрешения зависит от другого разрешения. (Разрешение по вертикали может зависеть от разрешения по горизонтали.)</p>
<p>Требуется для всех элементов с включенным приобретением; то есть элементы в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE и WIA_CATEGORY_FILM. Он не поддерживается для WIA_CATEGORY_FOLDER элементов.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: для чтения, записи или только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> или WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_XSCALING"></span><span id="wia_ips_xscaling"></span><dl> <dt><strong>WIA_IPS_XSCALING</strong></dt> <dt>сканнерпиктурексскалинг</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Задает горизонтальное масштабирование в процентах, которое может быть применено к отсканированным изображениям в устройстве сканера или его драйвере.</p>
<p>Это свойство является необязательным для всех элементов с включенным приобретением. то есть элементы типов WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK и WIA_CATEGORY_FILM.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: для чтения, записи или только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE.</p>
<p>Значения могут быть от 1 до максимального VT_I4 (0xFFFF). Например, 100 означает отсутствие масштабирования, 050 означает масштабирование до 50% от размера Оригнал, а 200 означает масштабирование до 200% исходного размера.</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_YEXTENT"></span><span id="wia_ips_yextent"></span><dl> <dt><strong>WIA_IPS_YEXTENT</strong></dt> <dt>сканнерпиктурэйекстент</dt> </dl></td>
<td ><p>Содержит текущую высоту (в пикселях) выбранного изображения для получения. Приложение задает это свойство, чтобы пометить высоту области выделения. Это свойство должно быть согласовано со значением свойства <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> . Минидривер создает и поддерживает это свойство.</p>
<p>Требуется для всех элементов с включенным приобретением; то есть элементы в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK и WIA_CATEGORY_FILM.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_YPOS"></span><span id="wia_ips_ypos"></span><dl> <dt><strong>WIA_IPS_YPOS</strong></dt> <dt>сканнерпиктурэйпос</dt> </dl></td>
<td ><p>Текущая координата y (в пикселях) верхнего левого угла выбранного изображения. Приложение задает это свойство, чтобы пометить левый верхний угол области выделения. Минидривер создает и поддерживает это свойство.</p>
<p>Требуется для всех элементов с включенным приобретением; то есть элементы в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE и WIA_CATEGORY_FILM. Он не поддерживается для WIA_CATEGORY_FOLDER элементов.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_YRES"></span><span id="wia_ips_yres"></span><dl> <dt><strong>WIA_IPS_YRES</strong></dt> <dt>сканнерпиктурэйрес</dt> </dl></td>
<td ><p>Содержит текущее разрешение по вертикали (в пикселях на дюйм) для устройства. Приложение задает это свойство для установки разрешения по вертикали. Минидривер создает и поддерживает это свойство.</p>
<p>Если для устройства можно задать только одно значение, создайте тип <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> и поместите в него допустимое значение. Это также случай, когда один параметр разрешения зависит от другого разрешения. (Разрешение по горизонтали может зависеть от вертикального разрешения.)</p>
<p>Требуется для всех элементов с включенным приобретением; то есть элементы в категориях: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE и WIA_CATEGORY_FILM. Он не поддерживается для WIA_CATEGORY_FOLDER элементов.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: для чтения, записи или только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> или WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_YSCALING"></span><span id="wia_ips_yscaling"></span><dl> <dt><strong>WIA_IPS_YSCALING</strong></dt> <dt>сканнерпиктурэйскалинг</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
это свойство поддерживается только Windows Vista и более поздних версий.
</blockquote>
</div>
<div>
 
</div>
<p>Задает вертикальное масштабирование в процентах, которое может быть применено к отсканированным изображениям в устройстве сканера или его драйвере.</p>
<p>Это свойство является необязательным для всех элементов с включенным приобретением. то есть элементы типов WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK и WIA_CATEGORY_FILM.</p>
<p>Тип: <strong>VT_I4</strong>, доступ: для чтения, записи или только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE.</p>
<p>Значения могут быть от 1 до максимального VT_I4 (0xFFFF). Например, 100 означает отсутствие масштабирования, 050 означает масштабирование до 50% от размера Оригнал, а 200 означает масштабирование до 200% исходного размера.</p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>              |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Виадеф. h</dt> </dl> |



 

 




