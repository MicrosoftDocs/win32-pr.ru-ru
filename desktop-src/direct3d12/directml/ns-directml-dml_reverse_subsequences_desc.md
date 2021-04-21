---
UID: NS:directml.DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
title: DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
description: Меняет местами элементы одной или нескольких вложенных *последовательностей* тензорные. Набор подпоследовательностей, которые должны быть отменены, выбирается на основе указанной оси и длины последовательности.
helpviewer_keywords:
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure
- direct3d12.dml_reverse_subsequences_operator_desc
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
ms.openlocfilehash: 3deddea3d60db1a8689ceabfac92ff17393b7606
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803998"
---
# <a name="dml_reverse_subsequences_operator_desc-structure-directmlh"></a>Структура DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC (директмл. h)
Меняет местами элементы одной или нескольких вложенных *последовательностей* тензорные. Набор подпоследовательностей, которые должны быть отменены, выбирается на основе указанной оси и длины последовательности.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *SequenceLengthsTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a>Члены

`InputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Входной тензорные, содержащий элементы для обращения.


`SequenceLengthsTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий значение для каждой подпоследовательности, которая должна быть отменена, обозначающая длину в элементах этой вложенной последовательности. Обращены только элементы в пределах длины вложенной последовательности. остальные элементы вдоль этой оси копируются в выходные данные без изменений.

Этот тензорные должен иметь количество измерений и размеры, равные *инпуттенсор*, *за исключением* измерения, заданного параметром *Axis* . Размер измерения *оси* должен быть равен 1. Например, если *инпуттенсор* имеет размеры `{2,3,4,5}` , а *ось* — 1, то размеры *секуенцеленгсстенсор* должны быть `{2,1,4,5}` .

Если длина подпоследовательности превышает максимальное количество элементов на этой оси, то этот оператор ведет себя так, как если бы значение было обработано до максимума.


`OutputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Выходной тензорные для записи результатов в. Этот тензорные должен иметь те же размеры и тип данных, что и *инпуттенсор*.


`Axis`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Индекс измерения, по которому нужно обратить элементы. Это значение должно быть меньше значения параметра DimensionCount *инпуттенсор*.

## <a name="examples"></a>Примеры

### <a name="example-1"></a>Пример 1

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,3,1}, DataType:UINT32)
[[[[2],
   [4],
   [3]]]]

Axis: 3

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  4],
   [ 8,  7,  6,  5],
   [11, 10,  9, 12]]]]
```

### <a name="example-2-reversing-along-a-different-axis"></a>Пример 2. Реверс вдоль другой оси

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,1,4}, DataType:UINT32)
[[[[2, 3, 1, 0]]]]

Axis: 2

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[5, 10,  3,  4], // Notice that sequence lengths of 1 and 0 are effective nops
   [1,  6,  7,  8],
   [9,  2, 11, 12]]]]
```

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Ограничения тензорные
* *Инпуттенсор*, *аутпуттенсор* и *секуенцеленгсстенсор* должны иметь одинаковые *DimensionCount*.
* *Инпуттенсор* и *аутпуттенсор* должны иметь одинаковый *тип данных*.

## <a name="tensor-support"></a>Поддержка тензорные
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 и выше
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | от 4 до 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| секуенцеленгсстенсор | Входные данные | от 4 до 5 | ЗНАЧЕНИЕМ |
| аутпуттенсор | Выходные данные | от 4 до 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 и выше
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| секуенцеленгсстенсор | Входные данные | 4 | ЗНАЧЕНИЕМ |
| аутпуттенсор | Выходные данные | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |



## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |