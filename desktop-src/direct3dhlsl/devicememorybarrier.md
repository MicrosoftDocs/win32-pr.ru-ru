---
title: Функция Девицемеморибарриер
description: Блокирует выполнение всех потоков в группе до тех пор, пока не будут завершены все доступ к памяти устройства.
ms.assetid: 904ab8f6-4849-4b13-8fac-3967cf66574e
keywords:
- Функция Девицемеморибарриер HLSL
topic_type:
- apiref
api_name:
- DeviceMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f3629f7eaf8b3e271ca988b73e1dedab1e428136cc86663b64b838597d1b98c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855264"
---
# <a name="devicememorybarrier-function"></a>Функция Девицемеморибарриер

Блокирует выполнение всех потоков в группе до тех пор, пока не будут завершены все доступ к памяти устройства.

## <a name="syntax"></a>Синтаксис

``` syntax
void DeviceMemoryBarrier(void);
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
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Встроенные функции](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




