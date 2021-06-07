---
UID: NS:directml.DML_SCATTER_ND_OPERATOR_DESC
title: DML_SCATTER_ND_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC)
description: Копирует весь входной тензорные в выходные данные, а затем перезаписывает выбранные индексы соответствующими значениями из тензорные обновлений.
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
- DML_SCATTER_ND_OPERATOR_DESC
f1_keywords:
- DML_SCATTER_ND_OPERATOR_DESC
- directml/DML_SCATTER_ND_OPERATOR_DESC
ms.openlocfilehash: 6c987e01862d849c6215a2d25fe957ef0a22e7af
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418004"
---
# <a name="dml_scatter_nd_operator_desc-structure-directmlh"></a>Структура DML_SCATTER_ND_OPERATOR_DESC (директмл. h)
Копирует весь входной тензорные в выходные данные, а затем перезаписывает выбранные индексы соответствующими значениями из тензорные обновлений. Этот оператор выполняет следующий псевдокод, где "..." представляет ряд координат с точным поведением, определяемым осью и размером индексов.

```
output = input
output[indices[...]] = updates[...]
```

Если два индекса элементов вывода перекрываются (что недопустимо), последняя запись WINS не гарантируется.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_SCATTER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *UpdatesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
};
```



## <a name="members"></a>Участники

`InputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Тензорные, из которого производится чтение.


`IndicesTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий индексы. *DimensionCount* этого тензорные должен соответствовать *инпуттенсор. DimensionCount*. Последнее измерение *индицестенсор* на самом деле является числом координат на кортеж индекса, и не должны превышает *инпуттенсор. DimensionCount*. Например, индексы тензорные размера `{1,4,5,2}` с *индицесдименсионкаунт* = 3 означает 4x5 массив кортежей координат из двух значений, которые индексируются в *инпуттенсор*.

Начиная с `DML_FEATURE_LEVEL_3_0` , этот оператор поддерживает отрицательные значения индекса при использовании целочисленного типа со знаком с этим тензорные. Отрицательные индексы обрабатываются относительно конца соответствующего измерения. Например, индекс-1 ссылается на последний элемент в этом измерении.


`UpdatesTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий новые значения для замены существующих входных значений по соответствующим индексам. *DimensionCount* этого тензорные должен соответствовать *инпуттенсор. DimensionCount*. Ожидаемый *упдатестенсор. sizes* является объединением *индицестенсор. размеры* ведущих сегментов и *инпуттенсор. sizes* в конце сегмента, чтобы получить следующий результат.

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
UpdatesTensor.Sizes = [
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
]
```

Размеры вычисляются по правому краю, при этом в начале каждого из них в начале *упдатестенсор. DimensionCount* помещаются начальные значения 1.

Рассмотрим пример.

```
InputTensor.Sizes = [3,4,5,6,7]
InputDimensionCount = 5
IndicesTensor.Sizes = [1,1, 1,2,3]
IndicesDimensionCount = 3 // can be thought of as a [1,2] array of 3-coordinate tuples

// The [1,2] comes from the indices tensor (ignoring last dimension, which is the tuple size),
// and the [6,7] comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
UpdatesTensor.Sizes = [1, 1,2,6,7]
```


`OutputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, в который записываются результаты. *Размеры* и *тип данных* этого тензорные должны соответствовать *инпуттенсор. sizes*.


`InputDimensionCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Число фактических входных измерений в *инпуттенсор* после пропуска любых несущественных начальных значений, в диапазоне [1, *инпуттенсор. DimensionCount*). Например, для заданных *инпуттенсор. sizes* = {1,1,4,6} и *инпутдименсионкаунт* = 3 фактически значимые индексы имеют значение {1,4,6} .


`IndicesDimensionCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Количество фактических измерений индекса в *индицестенсор* после пропуска любых несущественных начальных значений, в диапазоне [1, *индицестенсор. DimensionCount*). Например, для заданных *индицестенсор. sizes* = {1,1,4,6} и *индицесдименсионкаунт* = 3 фактически значимые индексы имеют значение {1,4,6} .

## <a name="examples"></a>Примеры

```
InputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 2, 3, 4, 5, 6, 7, 8]

IndicesTensor: (Sizes:{4,1}, DataType:FLOAT32)
    [[4], [3], [1], [7]]

UpdatesTensor: (Sizes:{4}, DataType:FLOAT32)
    [9, 10, 11, 12]

// output = input
// output[indices[x, 0]] = updates[x]
OutputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 11, 3, 10, 9, 6, 7, 12]
```

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Ограничения тензорные
* *Индицестенсор*, *инпуттенсор*, *Аутпуттенсор* и `UpdatesTensor` должны иметь одинаковые *DimensionCount*.
* *Инпуттенсор*, *аутпуттенсор* и `UpdatesTensor` должны иметь одинаковый *тип данных*.

## <a name="tensor-support"></a>Поддержка тензорные
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 и выше
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | от 1 до 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| индицестенсор | Входные данные | от 1 до 8 | INT64, INT32, UINT64, UINT32 |
| упдатестенсор | Входные данные | от 1 до 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| аутпуттенсор | Выходные данные | от 1 до 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 и выше
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| индицестенсор | Входные данные | 4 | ЗНАЧЕНИЕМ |
| упдатестенсор | Входные данные | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| аутпуттенсор | Выходные данные | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |



## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |