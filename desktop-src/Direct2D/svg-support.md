---
title: Поддержка SVG
description: Начиная с годовщины Windows 10, Direct2D поддерживает рендеринг цветовых шрифтов, содержащих контуры глифов SVG, как описано в спецификации OpenType (см. таблицу SVG).
ms.assetid: 5cb4cb7c-9b96-e110-bff9-d75ad1980010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678c5d9ef42a53c854bb2f175fac63816345c519
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413008"
---
# <a name="svg-support"></a>Поддержка SVG

Начиная с годовщины Windows 10, Direct2D поддерживает визуализацию [цветовых шрифтов](../directwrite/color-fonts.md) , содержащих контуры глифов SVG, как описано в [спецификации OpenType](/typography/opentype/spec/) (см. [таблицу SVG](/typography/opentype/spec/svg)). Начиная с Windows 10 Creators Update, Direct2D также поддерживает визуализацию автономных изображений SVG. Однако некоторые функции SVG запрещены в шрифтах SVG OpenType, и некоторые функции SVG в настоящее время не поддерживаются Direct2D.  

В этом разделе указывается набор функций [SVG 1,1](https://www.w3.org/TR/SVG11/) , поддерживаемых Direct2D в юбилейном обновлении и более новых версиях для Windows 10. Этот документ относится к SVG в шрифтах OpenType, а также к отдельным изображениям SVG.

## <a name="supported-svg-elements-and-attributes"></a>Поддерживаемые элементы и атрибуты SVG

Direct2D поддерживает визуализацию следующих элементов SVG и связанных с ними атрибутов для каждого элемента. Другие элементы и обычные атрибуты игнорируются.



| Элемент                                                                                  | Поддерживаемые обычные атрибуты                                                             |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [круглая](https://www.w3.org/TR/SVG11/shapes.mdl#circleelement)                           | Идентификатор, стиль, преобразование, CX, CY, r                                                          |
| [клиппас](https://www.w3.org/TR/SVG11/masking.mdl#clippathelement)                      | Идентификатор, стиль, преобразование, Клиппасунитс                                                      |
| [дефс](https://www.w3.org/TR/SVG11/struct.mdl#defselement)                               | Идентификатор, стиль, преобразование                                                                     |
| [desc](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup>  | идентификатор                                                                                       |
| [эллипс](https://www.w3.org/TR/SVG11/shapes.mdl#ellipseelement)                         | Идентификатор, стиль, преобразование, CX, CY, RX, дые                                                     |
| [g](https://www.w3.org/TR/SVG11/struct.mdl#gelement)                                     | Идентификатор, стиль, преобразование                                                                     |
| [image](https://www.w3.org/TR/SVG11/struct.mdl#imageelement)                             | идентификаторы, стили, преобразования, x, y, ширина, высота, Пресервеаспектратио, XLink: href               |
| [line](https://www.w3.org/TR/SVG11/shapes.mdl#lineelement)                               | Идентификатор, стиль, преобразование, x1, y1, x2, Y2                                                     |
| [линеарградиент](https://www.w3.org/TR/SVG11/pservers.mdl#lineargradientelement)         | ID, Style, x1, y1, x2, Y2, Градиентунитс, Градиенттрансформ, Спреадмесод, XLink: href    |
| [путь](https://www.w3.org/TR/SVG11/paths.mdl#pathelement)                                | Идентификатор, стиль, преобразование, d                                                                  |
| [фигуры](https://www.w3.org/TR/SVG11/shapes.mdl#polygonelement)                         | Идентификатор, стиль, преобразование, точки                                                             |
| [линию](https://www.w3.org/TR/SVG11/shapes.mdl#polylineelement)                       | Идентификатор, стиль, преобразование, точки                                                             |
| [радиалградиент](https://www.w3.org/TR/SVG11/pservers.mdl#radialgradientelement)         | ID, Style, CX, CY, r, FX, FY, Градиентунитс, Градиенттрансформ, Спреадмесод, XLink: href |
| [перетаскиваемые](https://www.w3.org/TR/SVG11/shapes.mdl#rectelement)                               | Идентификатор, стиль, преобразование, x, y, ширина, высота, RX, дые                                        |
| [stop](https://www.w3.org/TR/SVG11/pservers.mdl#stopelement)                             | Идентификатор, стиль, смещение                                                                        |
| [SVG](https://www.w3.org/TR/SVG11/struct.mdl#svgelement)                                 | идентификаторы, стили, x, y, ширина, высота, viewBox, Пресервеаспектратио                             |
| [Титуль](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup> | идентификатор                                                                                       |
| [use](https://www.w3.org/TR/SVG11/struct.mdl#useelement)                                 | Идентификатор, стиль, преобразование, x, y, ширина, высота, XLink: href                                    |



 

<sup>\*</sup> Поддерживается только в Windows 10 Creators Update и более новых версиях

## <a name="supported-svg-presentation-attributes"></a>Поддерживаемые атрибуты представления SVG

Direct2D также поддерживает следующие атрибуты представления. Они могут быть заданы для любых элементов SVG, но они влияют только на внешний вид определенных элементов, как описано в спецификации SVG (см. [атрибуты презентации](https://www.w3.org/TR/SVG11/attindex.mdl#presentationattributes)).

-   Clip-Path
-   обрезать-правило
-   color
-   монитор<sup>\*</sup>
-   fill
-   Заливка — непрозрачность
-   Заливка-правило
-   непрозрачность
-   переполнение
-   конец-цвет
-   приостанавливает — непрозрачность
-   stroke
-   Stroke — дашаррай
-   Stroke — дашоффсет
-   Stroke — линекап
-   Stroke — линежоин
-   Stroke — митерлимит
-   непрозрачность обводки
-   Толщина линии
-   доступности<sup>\*</sup>

<sup>\*</sup> Поддерживается только в Windows 10 Creators Update и более новых версиях

## <a name="unsupported-svg-features"></a>Неподдерживаемые функции SVG

### <a name="unsupported-elements-and-attributes"></a>Неподдерживаемые элементы и атрибуты

Все элементы или атрибуты, не включенные в перечисленные выше списки, считаются неподдерживаемыми Direct2D. При синтаксическом анализе содержимого SVG, содержащего неподдерживаемый элемент или атрибут, неподдерживаемая сущность игнорируется. Оставшаяся часть содержимого визуализируется точно так же, как это возможно.

### <a name="unsupported-length-units"></a>Неподдерживаемые единицы длины

Начиная с годовщины Windows 10, Direct2D поддерживает только значения длины пространства пользователя и значения процентной длины. Длины с суффиксами единиц измерения, например "mm" или "EM", не поддерживаются.

Начиная с обновления для дизайнеров Windows 10, Direct2D также поддерживает абсолютные идентификаторы устройств: px, PT, PC, cm, mm и в. Относительные идентификаторы единиц измерения (EM, ex) не поддерживаются.

### <a name="unsupported-image-sources"></a>Неподдерживаемые источники изображений

Элемент Image поддерживается только в том случае, если атрибут XLink: href установлен в образ в кодировке Base64. Удаленные ссылки не поддерживаются.

 

 