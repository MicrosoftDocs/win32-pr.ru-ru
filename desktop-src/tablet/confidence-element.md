---
description: Содержит Рейтинг достоверности, возвращенный анализатором рукописного ввода журнала для Инкворд.
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: Элемент достоверности
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86e4169767f3bf40d49e71e84214d50d3c0c0b4ecf5d3f7a9034ee6c8ea279d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936984"
---
# <a name="confidence-element"></a>Элемент достоверности

Содержит Рейтинг достоверности, возвращенный анализатором рукописного ввода журнала для [**инкворд**](inkword-element.md).

## <a name="definition"></a>Определение

``` syntax
<xs:element name="Confidence" type="xs:string" minOccurs="0" />
```

## <a name="parent-elements"></a>Родительские элементы

[**инкворд**](inkword-element.md)

## <a name="values"></a>Значения

Допустимые значения для этого поля: "0", "1" и "2". 0 означает высокую достоверность, 1 означает промежуточную уверенность, а 2 — низкую уверенность.

## <a name="child-elements"></a>Дочерние элементы

Отсутствует.

## <a name="attributes"></a>Атрибуты

Отсутствует.

## <a name="element-information"></a>Сведения об элементе



|                  | Значение                                      |
|------------------|--------------------------------------------|
| **Тип элемента** | xs:string                                  |
| **Пространство имен**    | urn: schemas-microsoft-com: TabletPC: ричинк |
| **Имя схемы**  | Средство чтения журнала                             |



 

 

 



