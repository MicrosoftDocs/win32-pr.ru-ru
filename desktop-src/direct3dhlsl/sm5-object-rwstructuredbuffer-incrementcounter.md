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
ms.openlocfilehash: c39a857fc9a7a108cea05060caf86ce61479a382c5160f4f051c11423bc6a5d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095174"
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

## <a name="remarks"></a>Remarks

Чтобы этот метод работал, в связанном представлении неупорядоченного доступа должен быть задан [**\_ \_ \_ \_ Счетчик флагов UAV buffer D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) .

Структурированный ресурс можно дополнительно индексировать на основе имен компонентов структур.

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Хттпсерв. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[рвструктуредбуффер](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

