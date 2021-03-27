---
title: 'Функция Рвструктуредбуффер:: Инкременткаунтер (Хттпсерв. h)'
description: Увеличивает значение скрытого счетчика объекта.
ms.assetid: 66385d4f-6db8-49ae-a73a-49089695f5ee
keywords:
- Функция Инкременткаунтер HLSL
topic_type:
- apiref
api_name:
- IncrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0002f82873de1c56ce5a7d79c9adb13bdf7ebc0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355493"
---
# <a name="incrementcounter-function"></a>Функция Инкременткаунтер

Увеличивает значение скрытого счетчика объекта.

## <a name="syntax"></a>Синтаксис

``` syntax
uint IncrementCounter(void);
```

## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **uint**

Предварительно увеличенное значение счетчика.

## <a name="remarks"></a>Примечания

Чтобы этот метод работал, в связанном представлении неупорядоченного доступа должен быть задан [**\_ \_ \_ \_ Счетчик флагов UAV buffer D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) .

Структурированный ресурс можно дополнительно индексировать на основе имен компонентов структур.

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Хттпсерв. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[рвструктуредбуффер](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

