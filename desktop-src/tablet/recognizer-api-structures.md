---
description: В этом разделе описываются структуры распознавателя.
ms.assetid: 4c17391f-7af4-42ab-b77f-e3c39cadc0b6
title: Структуры распознавателя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: addaccf3e69f35b99379710d681fe8ac45559ea1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703044"
---
# <a name="recognizer-structures"></a>Структуры распознавателя

В этом разделе описываются структуры распознавателя.

## <a name="in-this-section"></a>в этом разделе



| Структура                                                    | Описание                                                                                                                                                   |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_диапазон символов**](/windows/win32/api/rectypes/ns-rectypes-character_range)                  | Задает диапазон точек Юникода (символов).<br/>                                                                                                  |
| [**\_метрики LATTICE**](/windows/win32/api/rectypes/ns-rectypes-lattice_metrics)                  | Описывает базовые показатели и высоту заполнение нажатием клавиши.<br/>                                                                                                     |
| [**\_сегмент линии**](/windows/win32/api/rectypes/ns-rectypes-line_segment)                        | Описывает начальную и конечную точки сегмента распознавания линии, такие как базовые показатели или заполнение нажатием клавиши.<br/>                                                 |
| [**\_Описание пакета**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)            | Описывает содержимое пакета для конкретного контекста планшета.<br/>                                                                               |
| [**\_свойство пакета**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property)                  | Описывает свойство пакета, сообщаемое драйвером планшета.<br/>                                                                                 |
| [**\_метрики свойств**](/windows/desktop/api/tpcshrd/ns-tpcshrd-property_metrics)                | Определяет диапазон и разрешение свойства пакета.<br/>                                                                                             |
| [**СОСТО \_ attr**](/windows/win32/api/rectypes/ns-rectypes-reco_attrs)                            | Извлекает атрибуты распознавателя или определяет, какие атрибуты следует использовать при поиске установленного распознавателя.<br/>                         |
| [**СОСТО \_ Guide**](/windows/win32/api/rectypes/ns-rectypes-reco_guide)                            | Определяет границы рукописного ввода для распознавателя.<br/>                                                                                               |
| [**СОСТО \_ LATTICE**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice)                        | Выступает в качестве точки входа в Lattice.<br/>                                                                                                          |
| [**СОСТО \_ LATTICE, \_ столбец**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column)         | Представляет столбец в Lattice.<br/>                                                                                                                |
| [**СОСТО \_ LATTICE, \_ элемент**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)       | Соответствует одному слову или одному Восточно-Азиатскому символу, обычно; Однако элемент может также соответствовать жесту, фигуре или другому коду.<br/> |
| [**\_Свойства LATTICE \_ состо**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_properties) | Содержит массив указателей на структуры свойств.<br/>                                                                                              |
| [**СОСТО \_ LATTICE, \_ свойство**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_property)     | Содержит свойство, используемое в Lattice.<br/>                                                                                                           |
| [**\_диапазон состо**](/windows/win32/api/rectypes/ns-rectypes-reco_range)                            | Определяет диапазон символов в результирующей строке.<br/>                                                                                             |
| [**\_диапазон штрихов**](/windows/win32/api/tpcshrd/ns-tpcshrd-stroke_range)                        | Задает диапазон штрихов в объекте [**инкдисп**](inkdisp-class.md) .<br/>                                                                       |



 

 

 




