---
title: 'Функция WavePrefixProduct '
description: Возвращает произведение всех значений в активных желобах в этой волновой области с индексами, меньшими, чем эта полоса.
ms.assetid: 3A5B271D-EF45-4511-9086-A9AD0D215D9A
keywords:
- Функция Вавепрефикспродукт HLSL
topic_type:
- apiref
api_name:
- WavePrefixProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8cb780f951433afc480c38d52c8120e086a91d32117fe9bb566657e0fcf9f24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948964"
---
# <a name="waveprefixproduct-function"></a>Функция WavePrefixProduct 

Возвращает произведение всех значений в активных желобах в этой волновой области с индексами, меньшими, чем эта полоса.

## <a name="syntax"></a>Синтаксис

``` syntax
<type> WavePrefixProduct(
   <type> value
);
```

## <a name="parameters"></a>Параметры

*value* 

Значение для умножения.

## <a name="return-value"></a>Возвращаемое значение

Произведение всех значений.

## <a name="remarks"></a>Remarks

Порядок операций в этой подпрограммы не гарантируется. Таким образом, \[ точный флаг в \] нем игнорируется.

Постфиксный продукт может быть вычислен путем умножения префиксного продукта на значение текущей полосы.

Обратите внимание, что активная полоса с наименьшим индексом всегда будет иметь значение 1 для своего префиксного продукта.

Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера. 

## <a name="examples"></a>Примеры

```hlsl
uint numToMultiply = 2;
uint prefixProduct = WavePrefixProduct( numToMultiply );
```

На компьютере с размером волны 8 и всеми активными дорожками, кроме желобов 0 и 4, в Вавепрефикспродукт будут возвращены следующие значения.

| Индекс полосы | status   | префикспродукт | 
|------------|----------|---------------|
| 0          | неактивно | н/д           |
| 1          | active   |  = 1           |
| 2          | active   | = 1 \* 2        |
| 3          | active   | = 1 \* 2 \* 2     |
| 4          | неактивно | Недоступно           |
| 5          | active   | = 1 \* 2 \* 2 2 \*       |
| 6          | active   | = 1 \* 2 \* 2 \* 2 \* 2    |
| 7          | active   | = 1 \* 2 \* 2 \* 2 \* 2 \* 2 |

## <a name="see-also"></a>См. также

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Модель шейдеров 6](shader-model-6-0.md)
