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
ms.openlocfilehash: 25bbac15a26beb535a91155cdd4c411c3c669e0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647143"
---
# <a name="accepthitandendsearch-function"></a>Функция AcceptHitAndEndSearch

Используется в [любом шейдере нажатия](any-hit-shader.md) для фиксации текущего попадания, а затем для поиска большего числа попаданий для луча. Если выполняется шейдер пересечения, выполнение останавливается.  Выполнение передается в [ближайший шейдер](closest-hit-shader.md), если он включен, при достижении ближайшей записи на данный момент.

## <a name="syntax"></a>Синтаксис

```
void AcceptHitAndEndSearch();
```




## <a name="return-value"></a>Возвращаемое значение

**void**

## <a name="remarks"></a>Комментарии

Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:

* [**Вызываемый шейдер**](callable-shader.md)
* [**Шейдер ближайшего попадания**](closest-hit-shader.md)
* [**Шейдер непопаданий**](miss-shader.md)
* [**Шейдер создания лучей**](ray-generation-shader.md)



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Справочник по HLSL для трассировки лучей в Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




