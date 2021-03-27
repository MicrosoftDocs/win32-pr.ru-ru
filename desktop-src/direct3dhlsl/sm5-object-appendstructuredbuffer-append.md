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
ms.openlocfilehash: 79db73558cb243437560cc77ed66b64f2807fe13
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "103987039"
---
# <a name="append-function"></a>Функция append

Добавляет значение в конец буфера.

## <a name="syntax"></a>Синтаксис

``` syntax
void Append(
  in T value
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



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[аппендструктуредбуффер](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




