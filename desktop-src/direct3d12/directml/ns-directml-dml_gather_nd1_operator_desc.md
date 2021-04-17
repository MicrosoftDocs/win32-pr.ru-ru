---
UID: NS:directml.DML_GATHER_ND1_OPERATOR_DESC
title: DML_GATHER_ND1_OPERATOR_DESC
description: Собирает элементы из входного тензорные, используя индексы тензорные для сопоставления индексов со всеми подблоками входных данных. | DML_GATHER_ND1_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND1_OPERATOR_DESC
- DML_GATHER_ND1_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_GATHER_ND1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_GATHER_ND1_OPERATOR_DESC, DML_GATHER_ND1_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
- directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
ms.openlocfilehash: dc7f33f50fa6a0c1cd2850b8e02aad30d75afeb1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105720852"
---
# <a name="dml_gather_nd1_operator_desc-structure-directmlh"></a>Структура DML_GATHER_ND1_OPERATOR_DESC (директмл. h)

Собирает элементы из входного тензорные, используя индексы тензорные для сопоставления индексов со всеми подблоками входных данных. Этот оператор выполняет следующий псевдокод, где "..." представляет ряд координат с точным поведением, зависящим от количества измерений Batch, input и Indices.

```
output[batch, ...] = input[batch, indices[batch, ...], ...]
```

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис

```cpp
struct DML_GATHER_ND1_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* IndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT InputDimensionCount;
  UINT IndicesDimensionCount;
  UINT BatchDimensionCount;
};
```

## <a name="members"></a>Члены

`InputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Тензорные, из которого производится чтение.

`IndicesTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Тензорные, содержащий индексы. *DimensionCount* этого тензорные должен соответствовать *инпуттенсор. DimensionCount*. Последнее измерение *индицестенсор* на самом деле является числом координат на кортеж индекса и не может превышать *инпуттенсор. DimensionCount*. Например, индексы тензорные *размеров* `{1,4,5,2}` с *индицесдименсионкаунт* = 3 означает 4x5 массив из 2-координатных кортежей, которые индексируются в *инпуттенсор*.

Начиная с `DML_FEATURE_LEVEL_3_0` , этот оператор поддерживает отрицательные значения индекса при использовании целочисленного типа со знаком с этим тензорные. Отрицательные индексы обрабатываются относительно конца соответствующего измерения. Например, индекс-1 ссылается на последний элемент в этом измерении.

`OutputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, в который записываются результаты. *DimensionCount* и *DataType* этого тензорные должны соответствовать *инпуттенсор. DimensionCount*. Ожидаемый *аутпуттенсор. sizes* является объединением *индицестенсор. размеры* ведущих сегментов и *инпуттенсор. sizes* замыкающий сегмент, что приводит к следующему результату.

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

Размеры вычисляются по правому краю, при этом в начале каждого из них в начале *аутпуттенсор. DimensionCount* помещаются начальные значения 1.

Пример приведен ниже.

```
InputTensor.Sizes = {3,4,5,6,7}
InputDimensionCount = 5
IndicesTensor.Sizes = {1,1, 1,2,3}
IndicesDimensionCount = 3 // can be thought of as a {1,2} array of 3-coordinate tuples

// The {1,2} comes from the indices tensor (ignoring last dimension which is the tuple size),
// and the {6,7} comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
OutputTensor.Sizes = {1, 1,2,6,7}
```

`InputDimensionCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Число фактических входных измерений в *инпуттенсор* после пропуска любых несущественных начальных значений, в диапазоне от `[1, *InputTensor.DimensionCount*]` . Например, для заданных *инпуттенсор. sizes*  =  `{1,1,4,6}` и `InputDimensionCount` = 3 фактически значимые индексы имеют значение `{1,4,6}` .

`IndicesDimensionCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Количество фактических измерений индекса в *индицестенсор* после пропуска любых несущественных начальных значений, в диапазоне [1, *индицестенсор. DimensionCount*]. Например, для заданных *индицестенсор. sizes*  =  `{1,1,4,6}` и *индицесдименсионкаунт* = 3 фактически значимые индексы имеют значение `{1,4,6}` .

`BatchDimensionCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Количество измерений в каждом тензорные (*инпуттенсор*, *индицестенсор*, *аутпуттенсор*), которые считаются независимыми пакетами, в диапазоне между [0, *инпуттенсор. DimensionCount*) и [0, *индицестенсор. DimensionCount*). Число пакетов может быть равно 0, что подразумевает наличие одного пакета. Например, для заданных *индицестенсор. sizes*  =  `{1,3,4,5,6,7}` и *индицесдименсионкаунт* = 5 и `BatchDimensionCount` = 2 существуют пакеты `{3,4}` и осмысленные индексы `{5,6,7}` .

## <a name="remarks"></a>Комментарии
**DML_GATHER_ND1_OPERATOR_DESC** добавляет *батчдименсионкаунт* и эквивалентен [DML_GATHER_ND_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) , если *батчдименсионкаунт* = 0.

## <a name="examples"></a>Примеры

### <a name="example-1-1d-remapping"></a>Пример 1. повторное сопоставление 1D

```
InputDimensionCount: 2
IndicesDimensionCount: 2
BatchDimensionCount: 0

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping-with-batch-count"></a>Пример 2. Преобразование 2D с помощью счетчика пакетов

```
InputDimensionCount: 3
IndicesDimensionCount: 3
BatchDimensionCount: 1

// 3 batches.
InputTensor: (Sizes:{1, 3,2,2}, DataType:FLOAT32)
    [
        [[[0,1],[2,3]],   // batch 0
         [[4,5],[6,7]],   // batch 1
         [[8,9],[10,11]]] // batch 2
    ]

// A 3x2 array of 2D tuples indexing into InputTensor.
// e.g. a tuple of <1,0> in batch 1 corresponds to input value 6.
IndicesTensor: (Sizes:{1, 3,2,2}, DataType:UINT32)
    [
        [[[0,0],[1,1]],
         [[1,1],[0,0]],
         [[0,1],[1,0]]]
    ]

// output[batch, x] = input[batch, indices[batch, x, 0], indices[batch, x, 1]]
OutputTensor: (Sizes:{1,1, 3,2}, DataType:FLOAT32)
    [[
        [[0,3],
         [7,4],
         [9,10]]
    ]]
```

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Ограничения тензорные
* *Индицестенсор*, *инпуттенсор* и *аутпуттенсор* должны иметь одинаковые *DimensionCount*.
* *Инпуттенсор* и *аутпуттенсор* должны иметь одинаковый *тип данных*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | от 1 до 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| индицестенсор | Входные данные | от 1 до 8 | INT64, INT32, UINT64, UINT32 |
| аутпуттенсор | Выходные данные | от 1 до 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |
