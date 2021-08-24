---
title: Функция Граупмеморибарриервисграупсинк
description: Блокирует выполнение всех потоков в группе до тех пор, пока все общие группы доступа не будут завершены и все потоки в группе достигли этого вызова.
ms.assetid: 64dd78e1-c597-4bd0-8a9b-592123178de5
keywords:
- Функция Граупмеморибарриервисграупсинк HLSL
topic_type:
- apiref
api_name:
- GroupMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bbcfdea451c0cb7ad2b84297c422fa6865b1f45d757612a7b5d220a8829a99b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854454"
---
# <a name="groupmemorybarrierwithgroupsync-function"></a>Функция Граупмеморибарриервисграупсинк

Блокирует выполнение всех потоков в группе до тех пор, пока все общие группы доступа не будут завершены и все потоки в группе достигли этого вызова.

## <a name="syntax"></a>Синтаксис

``` syntax
void GroupMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

### <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                | Поддерживается |
|-----------------------------------------------------------------------------|-----------|
| [Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров | Да       |



 

Эта функция поддерживается в следующих типах шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[Встроенные функции](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




