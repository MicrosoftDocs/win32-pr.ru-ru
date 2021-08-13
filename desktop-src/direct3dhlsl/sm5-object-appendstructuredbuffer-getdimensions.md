---
title: 'Функция Аппендструктуредбуффер:: Dimension'
description: 'Возвращает размеры ресурсов. | Функция Аппендструктуредбуффер:: Dimension'
ms.assetid: 41ed86d5-25c0-48bd-add9-792eb89605c3
keywords:
- Функция Dimension HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96f40417834b8e23a9e746e4e4e3df93b96c1fc2affc7cd9147842e389dc99d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790655"
---
# <a name="appendstructuredbuffergetdimensions-function"></a>Функция Аппендструктуредбуффер:: Dimension

Возвращает размеры ресурсов.

## <a name="syntax"></a>Синтаксис

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*нумструктс* \[ заполняет\]
</dt> <dd>

Тип: **uint**

Число структур.

</dd> <dt>

*Шаг с шагом* \[ заполняет\]
</dt> <dd>

Тип: **uint**

Число байтов в каждом элементе.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

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

 

 




