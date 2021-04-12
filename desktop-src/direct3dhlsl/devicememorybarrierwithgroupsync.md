---
title: Функция Девицемеморибарриервисграупсинк
description: Блокирует выполнение всех потоков в группе до тех пор, пока не будут завершены все доступ к памяти устройства и все потоки в группе достигли этого вызова.
ms.assetid: 77c54064-a996-4c51-84b5-7da60e884c4f
keywords:
- Функция Девицемеморибарриервисграупсинк HLSL
topic_type:
- apiref
api_name:
- DeviceMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a7a4a27b3256fb78c7b60b960fc5383cfd5b5d4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334403"
---
# <a name="devicememorybarrierwithgroupsync-function"></a>Функция Девицемеморибарриервисграупсинк

Блокирует выполнение всех потоков в группе до тех пор, пока не будут завершены все доступ к памяти устройства и все потоки в группе достигли этого вызова.

## <a name="syntax"></a>Синтаксис

``` syntax
void DeviceMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Примечания

### <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                | Поддерживается |
|-----------------------------------------------------------------------------|-----------|
| [Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров | да       |



 

Эта функция поддерживается в следующих типах шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Встроенные функции](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




