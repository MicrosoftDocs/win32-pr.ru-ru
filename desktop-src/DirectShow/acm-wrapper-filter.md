---
description: Фильтр оболочки ACM
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: Фильтр оболочки ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6aaa56d955fe9cf1966e17c657fbf741b4bb8694a7f18b501b148b0383ea19d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664083"
---
# <a name="acm-wrapper-filter"></a>Фильтр оболочки ACM

Фильтр оболочки ACM включает кодеки (ACM) для подключения к графу фильтра. Он может действовать как фильтр распаковки или как фильтр сжатия.

в качестве фильтра распаковки оболочка ACM отображается в категории «DirectShow фильтры» (CLSID \_ легациамфилтеркатегори) и имеет нештатную подмножество \_ . Тип носителя подключения для входного ПИН-кода определяет, какой кодек использует фильтр. Как правило, приложению не нужно добавлять фильтр к графу фильтра; он автоматически извлекается при необходимости фильтром Graph Manager. Распаковка применяется только к звуку PCM.

Как фильтр сжатия, оболочка ACM отображается в категории "звуковые компрессоры" (CLSID \_ аудиокомпрессоркатегори) и имеет недостаточное количество \_ \_ \_ . Каждый кодек отображается как отдельный экземпляр. Для сжатия нельзя напрямую создать фильтр с помощью CoCreateInstance. Вместо этого необходимо использовать перечислитель системных устройств. Дополнительные сведения см. [в разделе Использование перечислителя системных устройств](using-the-system-device-enumerator.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Интерфейсы фильтра</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a>, IPersist, IPersistPropertyBag</td>
</tr>
<tr class="even">
<td>Типы носителей входных закрепления</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_NULL FORMAT_WaveFormatEx</td>
</tr>
<tr class="odd">
<td>Интерфейсы входных закрепления</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей для выходного ПИН-кода</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_PCM, FORMAT_WaveFormatEx. возможны следующие сочетания следующих вариантов.<br/>
<ul>
<li>Выборок в секунду (кГц): 44,1, 22,05, 11,025 или 8,0.</li>
<li>Каналы: стерео или Mono.</li>
<li>Бит на выборку: 8 или 16.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Интерфейсы выходного ПИН-кода</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>Иамстреамконфиг</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Фильтровать CLSID</td>
<td>CLSID_ACMWrapper</td>
</tr>
<tr class="odd">
<td>CLSID страницы свойств</td>
<td>Нет страницы свойств.</td>
</tr>
<tr class="even">
<td>Исполняемый объект</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Заслуживают</a></td>
<td>MERIT_NORMAL или MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Категория фильтра</a></td>
<td>CLSID_LegacyAmFilterCategory или CLSID_AudioCompressorCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 




