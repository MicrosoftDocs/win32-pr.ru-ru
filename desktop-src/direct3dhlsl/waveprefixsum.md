---
title: 'Функция WavePrefixSum '
description: Возвращает сумму всех значений в активном желобе с меньшими индексами по сравнению с этим значением.
ms.assetid: F51B90AB-3E85-4521-8A2C-7C16A4ECB1F9
keywords:
- Функция Вавепрефикссум HLSL
topic_type:
- apiref
api_name:
- WavePrefixSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bbb9ced3fbf7e150cbe3b9bca7eb176e61cf6c8881def22a977ae37a2dbf4b1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671094"
---
# <a name="waveprefixsum-function"></a>Функция WavePrefixSum 

Возвращает сумму всех значений в активном желобе с меньшими индексами по сравнению с этим значением.

## <a name="syntax"></a>Синтаксис

``` syntax
<type> WavePrefixSum(
   <type> value
);
```

## <a name="parameters"></a>Параметры

*value* 

Значение для суммирования.

## <a name="return-value"></a>Возвращаемое значение

Сумма значений.

## <a name="remarks"></a>Remarks

Порядок операций в этой подпрограммы не гарантируется. Таким образом, \[ точный флаг в \] нем игнорируется.

Постфиксная сумма может быть вычислена путем добавления суммы префикса к значению текущей полосы.

Обратите внимание, что активная полоса с наименьшим индексом всегда будет иметь значение 0 для своей суммы префикса.

Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера. 

## <a name="examples"></a>Примеры

```hlsl
uint numToSum = 2;
uint prefixSum = WavePrefixSum( numToSum );
```

На компьютере с размером волны 8 и всеми активными дорожками, кроме желобов 0 и 4, в Вавепрефикссум будут возвращены следующие значения.

| Индекс полосы | status   | префикссум     | 
|------------|----------|---------------|
| 0          | неактивно | н/д           |
| 1          | active   | = 0           |
| 2          | active   | = 0 + 2         |
| 3          | active   | = 0 + 2 + 2       |
| 4          | неактивно | Недоступно           |
| 5          | active   | = 0 + 2 + 2 + 2     |
| 6          | active   | = 0 + 2 + 2 + 2 + 2   |
| 7          | active   | = 0 + 2 + 2 + 2 + 2 + 2 |

## <a name="see-also"></a>См. также

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Модель шейдеров 6](shader-model-6-0.md)
