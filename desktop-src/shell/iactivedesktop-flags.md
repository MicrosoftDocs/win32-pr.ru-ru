---
description: В этом разделе описываются флаги, используемые методами интерфейса Иактиведесктоп.
title: Флаги Иактиведесктоп (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6d1a2f69-0730-4805-8b50-071332ff7070
api_name:
- AD_APPLY_ALL
- AD_APPLY_BUFFERED_REFRESH
- AD_APPLY_DYNAMICREFRESH
- AD_APPLY_FORCE
- AD_APPLY_HTMLGEN
- AD_APPLY_REFRESH
- AD_APPLY_SAVE
- COMP_ELEM_ALL
- COMP_ELEM_CHECKED
- COMP_ELEM_CURITEMSTATE
- COMP_ELEM_FRIENDLYNAME
- COMP_ELEM_NOSCROLL
- COMP_ELEM_ORIGINAL_CSI
- COMP_ELEM_POS_LEFT
- COMP_ELEM_POS_TOP
- COMP_ELEM_POS_ZINDEX
- COMP_ELEM_RESTORED_CSI
- COMP_ELEM_SIZE_HEIGHT
- COMP_ELEM_SIZE_WIDTH
- COMP_ELEM_SOURCE
- COMP_ELEM_TYPE
- COMP_TYPE_CFHTML
- COMP_TYPE_CONTROL
- COMP_TYPE_HTMLDOC
- COMP_TYPE_MAX
- COMP_TYPE_PICTURE
- COMP_TYPE_WEBSITE
- COMPONENT_TOP
- WPSTYLE_CENTER
- WPSTYLE_MAX
- WPSTYLE_STRETCH
- WPSTYLE_TILE
- WPSTYLE_SPAN
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dae164c696ae54963f802a6ddd5cb1f6862b2f14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987488"
---
# <a name="iactivedesktop-flags"></a>Флаги Иактиведесктоп

В этом разделе описываются флаги, используемые методами интерфейса [**иактиведесктоп**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) .

<dl> <dt>

<span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**AD — \_ применить \_ все**
</dt> <dd> <dl> <dt>



Статистическая функция * * * * AD Apply * * * *, * * * * \_ \_ AD \_ Apply хтмлжен * * * * \_ и * * * * AD \_ применить \_ обновление * * * *.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**AD — \_ применение \_ буферизованного \_ обновления**
</dt> <dd> <dl> <dt>



Запускает таймер и объединяет все запросы на обновление, выполненные с этим флагом в течение этого интервала, в одно обновление. Этот интервал задается через пять секунд. В конце интервала, или, если обновление запрашивается в течение интервала без флага * * * * AD \_ Apply \_ rerefresh * * * *, выполняется \_ обновление и таймер останавливается. Этот флаг должен сочетаться с флагом * * * * AD \_ Apply Refresh * * * * * \_ .


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**AD \_ Apply \_ динамикрефреш**
</dt> <dd> <dl> <dt>



[Версия 5,0](versions.md). Используйте динамический HTML, чтобы обновить только те элементы, которые были изменены с момента последнего обновления, а не весь рабочий стол.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**\_применение \_ принудительной установки AD**
</dt> <dd> <dl> <dt>



Принудительное изменение активного рабочего стола.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**AD \_ Apply \_ хтмлжен**
</dt> <dd> <dl> <dt>



Повторно создайте HTML-файл рабочего стола.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**\_Обновление применения \_ AD**
</dt> <dd> <dl> <dt>



Обновите элемент рабочего стола.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**\_сохранение применения \_ AD**
</dt> <dd> <dl> <dt>



Сохраните элемент рабочего стола.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**COMP \_ ELEM \_ все**
</dt> <dd> <dl> <dt>



Статистическая обработка \_ значений Comp ELEM \_ \* .


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**\_Проверка ELEM \_**
</dt> <dd> <dl> <dt>



Элемент был проверен.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**COMP \_ ELEM \_ куритемстате**
</dt> <dd> <dl> <dt>



Текущее состояние элемента рабочего стола.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**COMP \_ ELEM \_ FRIENDLYNAME**
</dt> <dd> <dl> <dt>



Понятное имя элемента.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**\_ELEMная \_ прокрутка Comp**
</dt> <dd> <dl> <dt>



Элемент не поддается прокрутке.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**\_ELEM \_ \_ CSI**
</dt> <dd> <dl> <dt>



Сведения о состоянии исходного элемента рабочего стола.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**COMP \_ ELEM \_ POS \_ Left**
</dt> <dd> <dl> <dt>



Горизонтальное расположение элемента.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**COMP \_ ELEM \_ POS \_ сверху**
</dt> <dd> <dl> <dt>



Вертикальная позиция элемента.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**COMP \_ ELEM \_ POS \_ ZINDEX**
</dt> <dd> <dl> <dt>



Z-индекс элемента.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**\_ELEM, \_ восстановленный \_ CSI**
</dt> <dd> <dl> <dt>



Сведения о состоянии восстановленного элемента рабочего стола.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**\_Высота ELEM \_ размера \_**
</dt> <dd> <dl> <dt>



Высота элемента.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**\_Ширина ELEM \_ размера \_**
</dt> <dd> <dl> <dt>



Ширина элемента.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**\_источник ELEM \_**
</dt> <dd> <dl> <dt>



Исходный источник элемента.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**\_тип ELEMа Comp \_**
</dt> <dd> <dl> <dt>



Тип элемента.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**\_тип Comp \_ кфхтмл**
</dt> <dd> <dl> <dt>



Формат HTML.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**\_ \_ элемент управления типа Comp**
</dt> <dd> <dl> <dt>



Элемент является элементом управления.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**\_тип Comp \_ хтмлдок**
</dt> <dd> <dl> <dt>



Элемент является HTML-документом. Этот флаг следует использовать только при крайней необходимости. Это приводит к вставке HTML-документа в файл Desktop. htt, используемый для управления разметкой рабочего стола. В большинстве случаев для \_ \_ добавления элементов на Рабочий стол следует использовать флаг * * * * Comp Type Web * * * *.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**\_тип Comp \_ Max**
</dt> <dd> <dl> <dt>



Максимальное значение \_ \_ \* флага типа Comp.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**\_изображение типа \_ comp**
</dt> <dd> <dl> <dt>



Элемент является изображением.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**\_ \_ веб-сайт типа Comp**
</dt> <dd> <dl> <dt>



Элемент является веб-сайтом.


</dt> </dl> </dd> <dt>

<span id="COMPONENT_TOP"></span><span id="component_top"></span>**в \_ Начало компонента**
</dt> <dd> <dl> <dt>



Значение z-порядка, означающее, что элемент находится в верхней части.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**ВПСТИЛЕ \_ Center**
</dt> <dd> <dl> <dt>



Фоновый рисунок выравнивается по центру.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**ВПСТИЛЕ \_ Max**
</dt> <dd> <dl> <dt>



Максимальное значение \_ \* флага впстиле.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**ВПСТИЛЕ \_ Stretch**
</dt> <dd> <dl> <dt>



Фоновый рисунок растягивается, чтобы вместить весь экран.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**\_плитка впстиле**
</dt> <dd> <dl> <dt>



Фоновый рисунок является мозаичным.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**\_диапазон впстиле**
</dt> <dd> <dl> <dt>



**Windows 8 и более поздние версии**: фоновый рисунок охватывает несколько мониторов.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
