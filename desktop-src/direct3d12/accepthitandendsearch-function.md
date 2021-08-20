---
description: Используется в любом шейдере нажатия для фиксации текущего попадания, а затем для поиска большего числа попаданий для луча.
ms.assetid: ''
title: Функция AcceptHitAndEndSearch
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- AcceptHitAndEndSearch
api_type:
- NA
ms.openlocfilehash: 35073145a9b9a4788c6aed3bbae0633f0a9f5b85
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813035"
---
# <a name="accepthitandendsearch-function"></a>Функция AcceptHitAndEndSearch

Используется в [любом шейдере нажатия](any-hit-shader.md) для фиксации текущего попадания, а затем для поиска большего числа попаданий для луча. Если выполняется шейдер пересечения, выполнение останавливается.  Выполнение передается в [ближайший шейдер](closest-hit-shader.md), если он включен, при достижении ближайшей записи на данный момент.

## <a name="syntax"></a>Синтаксис

```
void AcceptHitAndEndSearch();
```




## <a name="return-value"></a>Возвращаемое значение

**void**

## <a name="remarks"></a>Remarks

Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:

* [**Вызываемый шейдер**](callable-shader.md)
* [**Шейдер ближайшего попадания**](closest-hit-shader.md)
* [**Шейдер непопаданий**](miss-shader.md)
* [**Шейдер создания лучей**](ray-generation-shader.md)



## <a name="see-also"></a>См. также

* [Справочник по Direct3D 12 райтраЦинг HLSL](direct3d-12-raytracing-hlsl-reference.md)
