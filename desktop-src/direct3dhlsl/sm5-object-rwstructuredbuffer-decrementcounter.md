---
title: 'Рвструктуредбуффер: функция Екременткаунтер:D (Хттпсерв. h)'
description: Уменьшает значение скрытого счетчика объекта.
ms.assetid: 24bc0b63-a482-4fa5-9898-2d43bca20cf4
keywords:
- Функция Декременткаунтер HLSL
topic_type:
- apiref
api_name:
- DecrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8302f31cd07b81f4f78abe6a0a1fbcb2e6a1028f6153da69e55e0fb34977b585
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671394"
---
# <a name="decrementcounter-function"></a>Функция Декременткаунтер

Уменьшает значение скрытого счетчика объекта.

## <a name="syntax"></a>Синтаксис

``` syntax
uint DecrementCounter(void);
```

## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **uint**

Значение счетчика после уменьшения.

## <a name="remarks"></a>Remarks

Для связанного представления неупорядоченного доступа должен быть [**установлен \_ \_ \_ \_ Счетчик флагов UAV buffer D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) во время работы креатионфор этого метода.

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Хттпсерв. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[рвструктуредбуффер](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

