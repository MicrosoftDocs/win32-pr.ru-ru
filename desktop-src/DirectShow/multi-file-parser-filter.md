---
description: Фильтр синтаксического анализатора с несколькими файлами
ms.assetid: 8ef06f49-fda4-49e2-9b07-70453a2e897c
title: Фильтр синтаксического анализатора с несколькими файлами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44fc83a56bb12c307b85be875a3a2e7e73b744d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682259"
---
# <a name="multi-file-parser-filter"></a>Фильтр синтаксического анализатора с несколькими файлами

Фильтр синтаксического анализатора с несколькими файлами анализирует простой формат файла, который позволяет указать несколько имен файлов, как если бы они были одним файлом. Эти файлы имеют формат, показанный в следующем примере:


```C++
;MULTI
https://server/share/video.mpg
https://server/share/captions.smi
```



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
<li>Основной тип: MEDIATYPE_Stream</li>
<li>Подтип: CLSID_MultFile</li>
<li>Тип формата: GUID_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>Интерфейсы входных закрепления</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей для выходного ПИН-кода</td>
<td><ul>
<li>Основной тип: MEDIATYPE_File</li>
<li>Подтип: GUID_NULL</li>
<li>Тип формата: MEDIATYPE_File</li>
</ul></td>
</tr>
<tr class="odd">
<td>Интерфейсы выходного ПИН-кода</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Фильтровать CLSID</td>
<td>CLSID_MultFile</td>
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

Фильтр создает один выходной ПИН-код для каждого файла, указанного в исходном файле. Тип выходных данных — MEDIATYPE \_ File, а блок формата для выходного типа — это строка расширенных символов, содержащая имя файла. Каждый ПИН-код подключается к экземпляру фильтра модуля [подготовки к потоку файлов](file-stream-renderer-filter.md) . Фильтр модуля подготовки к потоку файлов создает один выходной ПИН-код, который предоставляет интерфейс [**истреамбуилдер**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) . Закрепление вывода подготавливает к просмотру указанный файл. Данные мультимедиа не передаются между средством синтаксического анализа нескольких файлов и модулем подготовки потока файлов.

CLSID фильтра не определен в UUIDs. h. Используйте этот макрос в своем собственном файле заголовка:


```C++
// {D51BD5A3-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_MultFile,
0xd51bd5a3, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 



