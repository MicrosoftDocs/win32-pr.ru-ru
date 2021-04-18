---
UID: NS:directml.DML_TOP_K1_OPERATOR_DESC
title: DML_TOP_K1_OPERATOR_DESC
description: Выбирает из каждой последовательности элементы с максимальным или наименьшим числом элементов на *оси инпуттенсор* и возвращает значения и индексы *этих элементов в* *аутпутвалуетенсор* и *аутпутиндекстенсор* соответственно.
helpviewer_keywords:
- DML_TOP_K1_OPERATOR_DESC
- DML_TOP_K1_OPERATOR_DESC structure
- direct3d12.dml_top_k1_operator_desc
- directml/DML_TOP_K1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
- DML_TOP_K1_OPERATOR_DESC
- directml/DML_TOP_K1_OPERATOR_DESC
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
- DML_TOP_K1_OPERATOR_DESC
ms.openlocfilehash: 8c5b9bf58a8582588d19878c7e06c602584777fa
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719961"
---
# <a name="dml_top_k1_operator_desc-structure-directmlh"></a>Структура DML_TOP_K1_OPERATOR_DESC (директмл. h)
Выбирает из каждой последовательности элементы с максимальным или наименьшим числом элементов на *оси инпуттенсор* и возвращает значения и индексы *этих элементов в* *аутпутвалуетенсор* и *аутпутиндекстенсор* соответственно. *Последовательность* ссылается на один из наборов элементов, которые существуют вдоль измерения *оси* *инпуттенсор*.

Выбор из большего числа элементов K или наименьших элементов K можно контролировать с помощью *аксисдиректион*.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_TOP_K1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputValueTensor;
  const DML_TENSOR_DESC *OutputIndexTensor;
  UINT                  Axis;
  UINT                  K;
  DML_AXIS_DIRECTION    AxisDirection;
};
```



## <a name="members"></a>Члены

`InputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Входной тензорные, содержащий элементы для выбора.


`OutputValueTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Выходной тензорные для записи значений верхних элементов *K* в. Верхние элементы *K* выбираются в зависимости от того, являются ли они наибольшими или наименьшими, в зависимости от значения *аксисдиректион*. Размер этого тензорные должен равняться *инпуттенсор*, *за исключением* измерения, заданного параметром *Axis* , который должен иметь значение, равное *K*.

Значения *K* , выбранные для каждой входной последовательности, гарантированно сортируются по убыванию (от большего к меньшему), если *аксисдиректион* [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md). В противном случае обратное значение равно true, а выбранные значения гарантированно сортируются по возрастанию (от наименьшего к большему).


`OutputIndexTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Выходной тензорные для записи индексов верхних элементов *K* в. Размер этого тензорные должен равняться *инпуттенсор*, *за исключением* измерения, заданного параметром *Axis* , который должен иметь значение, равное *K*.

Индексы, возвращаемые в этом тензорные, измеряются относительно начала последовательности (в отличие от начала тензорные). Например, индекс 0 всегда ссылается на первый элемент для всех последовательностей на оси.

В случаях, когда два или более элемента в верхнем-K имеют одинаковое значение (т. е. при наличии связи), индексы обоих элементов включаются и гарантированно упорядочиваются по возрастанию индекса элементов. Обратите внимание, что это справедливо независимо от значения *аксисдиректион*.


`Axis`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Индекс измерения, по которому должны быть выбраны элементы. Это значение должно быть меньше значения параметра *DimensionCount* *инпуттенсор*.


`K`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Число выбираемых элементов. Значение *K* должно быть больше 0, но меньше числа элементов в *инпуттенсор* вдоль измерения, заданного *осью*.


`AxisDirection`

Тип: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**

Значение из перечисления [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) . Если задано значение **DML_AXIS_DIRECTION_INCREASING**, то этот оператор возвращает *наименьшие* элементы *K* в порядке возрастания значения. В противном случае он возвращает *самые большие* элементы *K* в порядке убывания.

## <a name="examples"></a>Примеры

### <a name="example-1"></a>Пример 1

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 3
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,2}, DataType:FLOAT32)
[[[[11, 10],
   [ 9,  8],
   [ 7,  6]]]]

OutputIndexTensor: (Sizes:{1,1,3,2}, DataType:UINT32)
[[[[3, 2],
   [2, 3],
   [3, 2]]]]
```

### <a name="example-2-using-a-different-axis"></a>Пример 2. Использование другой оси

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 2
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[[[ 4,  5, 10, 11],
   [ 3,  2,  9,  8]]]]

OutputIndexTensor: (Sizes:{1,1,2,4}, DataType:UINT32)
[[[[2, 2, 0, 0],
   [1, 1, 1, 1]]]]
```

### <a name="example-3-tied-values"></a>Пример 3. Связанные значения

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[3, 2, 2],
   [5, 5, 4],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[3, 1, 2],
   [2, 3, 1],
   [0, 1, 2]]]]
```

### <a name="example-4-increasing-axis-direction"></a>Пример 4. Увеличение направления оси

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[1, 2, 2],
   [3, 4, 5],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[0, 1, 2],
   [0, 1, 2],
   [0, 1, 2]]]]
```


## <a name="remarks"></a>Комментарии
Если *аксисдиректион* имеет значение [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), этот оператор эквивалентен [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Ограничения тензорные
* *Инпуттенсор* и *аутпутвалуетенсор* должны иметь одинаковый *тип данных*.
* *Аутпутиндекстенсор* и *аутпутвалуетенсор* должны иметь одинаковые *размеры*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Измерения | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | { In0, In1, In2, In3 } | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| аутпутвалуетенсор | Выходные данные | { Out0, Out1, Out2, Out3 } | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| аутпутиндекстенсор | Выходные данные | { Out0, Out1, Out2, Out3 } | 4 | ЗНАЧЕНИЕМ |


## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |