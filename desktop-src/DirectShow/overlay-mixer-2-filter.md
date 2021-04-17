---
description: Наложение фильтра микшера 2
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: Наложение фильтра микшера 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22976a58b272cf04c098c102d32d154e361b8b9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682275"
---
# <a name="overlay-mixer-2-filter"></a>Наложение фильтра микшера 2

Фильтр оверлея 2 идентичен фильтру [микшера](overlay-mixer-filter.md) наложения, за исключением:

-   Он поддерживает только типы мультимедиа с форматами [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .
-   Он имеет более высокий уровень, что позволяет автоматически добавлять его в граф фильтра.

Микшер наложения 2 обеспечивает, что диспетчер графов фильтров добавляет его к графу при подготовке к просмотру видео в формате MPEG-2, отличном от DVD. Возможность использования микшера наложения или наложения 2 обрабатывается компонентом, который создает граф, диспетчер графов фильтров, Построитель графов записи или построитель DVD Graph. С точки зрения приложения они представляют собой один и тот же фильтр с одинаковыми интерфейсами и функциональными возможностями.

Следующая таблица содержит сведения, относящиеся к микшеру наложения 2. Сведения о всех других данных фильтра см. в документации по микшеру наложения.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Типы носителей входных закрепления</td>
<td>Тип формата: Format_VIDEOINFO2</td>
</tr>
<tr class="even">
<td>Фильтровать CLSID</td>
<td>CLSID_OverlayMixer2</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Заслуживают</a></td>
<td><ul>
<li>MERIT_UNLIKELY</li>
<li>Windows Vista или более поздней версии: MERIT_DO_NOT_USE</li>
</ul></td>
</tr>
</tbody>
</table>



 

В Windows Vista или более поздней версии фильтр оверлея 2 не \_ \_ \_ используется, так как новые модули подготовки видео (VMR-7, VMR-9 и Евр) поддерживают форматы **VIDEOINFOHEADER2** , поэтому нет необходимости использовать микшер наложения.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 



