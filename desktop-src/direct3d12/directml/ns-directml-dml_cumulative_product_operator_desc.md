---
UID: NS:directml.DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
title: DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
description: Умножает элементы тензорные вдоль оси, записывая выполняющийся высокий коэффициент произведения в выходном тензорные.
helpviewer_keywords:
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC structure
- direct3d12.dml_cumulative_product_operator_desc
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.openlocfilehash: 68b001467496ab9affc559e76ecac5461902399c
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521201"
---
# <a name="dml_cumulative_product_operator_desc-directmlh"></a>DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (директмл. h)

Умножает элементы тензорные вдоль оси, записывая выполняющийся высокий коэффициент произведения в выходном тензорные.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,5 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* OutputTensor;
    UINT Axis;
    DML_AXIS_DIRECTION AxisDirection;
    BOOL HasExclusiveProduct;
};
```

## <a name="members"></a>Участники

`InputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий входные данные. Обычно это те же тензорные, которые были предоставлены в качестве *инпуттенсор* для [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) в рамках прямого прохода.

Входной тензорные, содержащий элементы для умножения.

`OutputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Выходной тензорные для записи итоговых совокупных продуктов в. Этот тензорные должен иметь те же размеры и тип данных, что и *инпуттенсор*.

`Axis`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Индекс измерения, по которому необходимо умножить элементы. Это значение должно быть меньше значения параметра *DimensionCount* *инпуттенсор*.

`AxisDirection`

Тип: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**

Одно из значений перечисления [DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction) . Если задано значение **DML_AXIS_DIRECTION_INCREASING**, то продукт выполняется путем просмотра тензорные вдоль указанной оси по возрастанию индекса элементов. Если задано значение **DML_AXIS_DIRECTION_DECREASING**, возвращается обратное значение true, а продукт выполняется путем обхода элементов по убыванию индекса.

`HasExclusiveProduct`

Тип: <b> <a href="/windows/win32/winprog/windows-data-types">bool</a> .</b>

Если значение — **true**, значение текущего элемента исключается при записи выполняемого счетчика в выходной тензорные. При значении **false** значение текущего элемента включается в счетчик выполняется.

## <a name="examples"></a>Примеры

В примерах в этом разделе используются те же входные тензорные.

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-product-across-horizontal-slivers"></a>Пример 1. Совокупный продукт по горизонтали сливерс

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  2,   6,  30],       // i.e. [2, 2*1, 2*1*3, 2*1*3*5]
   [3, 24, 168, 504],       //      [...                   ]
   [9, 54, 108, 432]]]]     //      [...                   ]
```

### <a name="example-2-exclusive-products"></a>Пример 2. Эксклюзивные продукты

Установка параметра *хасексклусивепродукт* в **значение true** оказывает за исключением значения текущего элемента из счетчика, выполняемого при записи в выходной тензорные.

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2,  2,   6],      // Notice the product is written before multiplying the input,
   [1, 3, 24, 168],      // and the final total is not written to any output.
   [1, 9, 54, 108]]]]
```

### <a name="example-3-axis-direction"></a>Пример 3. Направление оси

Установка параметра *аксисдиректион* в значение [**DML_AXIS_DIRECTION_DECREASING**](/windows/win32/api/directml/ne-directml-dml_axis_direction) оказывает обратный порядок обхода элементов при вычислении счетчика выполнения.

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 30,  15, 15, 5],    // i.e. [2*1*3*5, 1*3*5, 3*5, 5]
   [504, 168, 21, 3],    //      [...                   ]
   [432,  48,  8, 4]]]]  //      [...                   ]
```

### <a name="example-4-multiplying-along-a-different-axis"></a>Пример 4. Умножение вдоль другой оси

В этом примере продукт выполняется вертикально вдоль оси высоты (второе измерение).

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 6,  8, 21, 15],   //      [2*3,  ...]
   [54, 48, 42, 60]]]] //      [2*3*9 ...]
```

## <a name="remarks"></a>Remarks
Этот оператор поддерживает выполнение на месте. Это означает, что тензорные вывода может иметь псевдоним *инпуттенсор* во время привязки.

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Ограничения тензорные
*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковые типы *данных* и *размеры*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |
| аутпуттенсор | Выходные данные | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |