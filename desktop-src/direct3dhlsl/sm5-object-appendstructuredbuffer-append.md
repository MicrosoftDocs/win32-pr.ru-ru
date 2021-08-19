---
title: 'Функция Аппендструктуредбуффер:: Append'
description: Добавляет значение в конец буфера.
ms.assetid: 667bc6dc-c0d0-419a-9227-99ce30b9cc73
keywords:
- Функция append HLSL
topic_type:
- apiref
api_name:
- Append
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 863269c5127915af82b8ef82aa36b60b17941d8627b3f81a789f75618219c773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725398"
---
# <a name="append-function"></a>Функция append

Добавляет значение в конец буфера.

## <a name="syntax"></a>Синтаксис

``` syntax
void Append(
  in T value
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ окне\]
</dt> <dd>

Тип: **T**

Входное значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

None

## <a name="remarks"></a>Remarks

T может быть любым типом данных, включая структуры.

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[аппендструктуредбуффер](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




