---
title: Функция Граупмеморибарриер
description: Блокирует выполнение всех потоков в группе до тех пор, пока не завершится общий доступ к группе.
ms.assetid: cebd4277-47a0-401a-bfbe-8d956412f254
keywords:
- Функция Граупмеморибарриер HLSL
topic_type:
- apiref
api_name:
- GroupMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9889be841df54f6ae18b7ac52d7117f780af37662c5a1d4f6c29af858350345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743864"
---
# <a name="groupmemorybarrier-function"></a>Функция Граупмеморибарриер

Блокирует выполнение всех потоков в группе до тех пор, пока не завершится общий доступ к группе.

## <a name="syntax"></a>Синтаксис

``` syntax
void GroupMemoryBarrier(void);
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



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Встроенные функции](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




