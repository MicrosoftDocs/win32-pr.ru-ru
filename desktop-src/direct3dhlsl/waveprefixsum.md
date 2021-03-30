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
ms.openlocfilehash: b133aa37b522156df73914eef66c4d3695a70ed7
ms.sourcegitcommit: 41c742c88f7d9ce05e107008f186b6e872ff9288
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2021
ms.locfileid: "104986152"
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

## <a name="remarks"></a>Примечания

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
| 0          | неактивно | Недоступно           |
| 1          | active   | = 0           |
| 2          | active   | = 0 + 2         |
| 3          | active   | = 0 + 2 + 2       |
| 4          | неактивно | Недоступно           |
| 5          | active   | = 0 + 2 + 2 + 2     |
| 6          | active   | = 0 + 2 + 2 + 2 + 2   |
| 7          | active   | = 0 + 2 + 2 + 2 + 2 + 2 |

## <a name="see-also"></a>См. также раздел

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Модель шейдеров 6](shader-model-6-0.md)
