---
description: Фильтр модуля подготовки к потоку файлов
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: Фильтр модуля подготовки к потоку файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64c8d8a0c87dab3aa811c8246be24ded8ee04dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537889"
---
# <a name="file-stream-renderer-filter"></a>Фильтр модуля подготовки к потоку файлов

Фильтр модуля подготовки отчетов File Stream подготавливает к просмотру имена файлов, которые анализируются фильтром [синтаксического анализатора с несколькими файлами](multi-file-parser-filter.md) . Дополнительные сведения см. в документации по этому фильтру.

Использование этого фильтра является устаревшим. Для отрисовки нескольких файлов в одном графе фильтра приложение должно просто вызвать **RenderFile** или **аддсаурцефилтер** несколько раз.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Интерфейсы фильтра</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей входных закрепления</td>
<td><ul>
<li>Основной тип: MEDIATYPE_File</li>
<li>Подтип: GUID_NULL</li>
<li>Тип формата: MEDIATYPE_File</li>
</ul></td>
</tr>
<tr class="odd">
<td>Интерфейсы входных закрепления</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей для выходного ПИН-кода</td>
<td>Нет</td>
</tr>
<tr class="odd">
<td>Интерфейсы выходного ПИН-кода</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>истреамбуилдер</strong></a></td>
</tr>
<tr class="even">
<td>Фильтровать CLSID</td>
<td>CLSID_FileRend</td>
</tr>
<tr class="odd">
<td>Исполняемый объект</td>
<td>Quartz.dll</td>
</tr>
<tr class="even">
<td><a href="merit.md">Заслуживают</a></td>
<td>MERIT_UNLIKELY</td>
</tr>
<tr class="odd">
<td><a href="filter-categories.md">Категория фильтра</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Комментарии

CLSID фильтра не определен в UUIDs. h. Используйте этот макрос в своем собственном файле заголовка:


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 



