---
title: 'Функция RWTexture2DArray:: operator'
description: 'Возвращает переменную ресурса. | Функция RWTexture2DArray:: operator'
ms.assetid: ae3d0697-ea0a-450d-bdfe-7bc5d8faf11a
keywords:
- Оператор Function HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8650b4aed51915591438501fb2c929b846e5be1d4de1219017ec1eb45980d552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985924"
---
# <a name="rwtexture2darrayoperator--function"></a>Функция RWTexture2DArray:: operator

Возвращает переменную ресурса.

## <a name="syntax"></a>Синтаксис

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*POS-терминал* \[ окне\]
</dt> <dd>

Тип: **uint3**

Позиция индекса. Первый и второй компоненты содержат координаты (x, y). Третий компонент указывает нужный срез массива.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **R**

Переменная ресурса.

## <a name="remarks"></a>Remarks

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[RWTexture2DArray](sm5-object-rwtexture2darray.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




