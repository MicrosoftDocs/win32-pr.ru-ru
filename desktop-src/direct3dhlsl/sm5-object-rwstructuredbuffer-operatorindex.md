---
title: 'Функция Рвструктуредбуффер:: operator'
description: 'Возвращает переменную ресурса. | Функция Рвструктуредбуффер:: operator'
ms.assetid: e821b60e-38db-463f-b0c6-47f2a4c9ccee
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
ms.openlocfilehash: ad2e8085a52a920f7fe87a2820398877167a137c14c4ebe39bacd71ae2ba0324
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509323"
---
# <a name="rwstructuredbufferoperator--function"></a>Функция Рвструктуредбуффер:: operator

Возвращает переменную ресурса.

## <a name="syntax"></a>Синтаксис

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*POS-терминал* \[ окне\]
</dt> <dd>

Тип: **uint**

Позиция индекса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **R**

Переменная ресурса.

## <a name="remarks"></a>Remarks

Структурированный ресурс можно дополнительно индексировать на основе имен компонентов структур.

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[рвструктуредбуффер](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




