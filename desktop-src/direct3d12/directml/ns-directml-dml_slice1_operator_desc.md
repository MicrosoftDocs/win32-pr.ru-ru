---
UID: NS:directml.DML_SLICE1_OPERATOR_DESC
title: DML_SLICE1_OPERATOR_DESC
description: Извлекает одну подобласть (срез) входного тензорные.
helpviewer_keywords:
- DML_SLICE1_OPERATOR_DESC
- DML_SLICE1_OPERATOR_DESC structure
- direct3d12.dml_slice1_operator_desc
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
ms.openlocfilehash: f34525865be9541da879e66e88c29d4a2ab74f00
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803947"
---
# <a name="dml_slice1_operator_desc-structure-directmlh"></a>Структура DML_SLICE1_OPERATOR_DESC (директмл. h)
Извлекает одну подобласть (срез) входного тензорные.

В *окне ввода* описываются границы входных тензорные, которые следует учитывать в срезе. Окно определяется с использованием трех значений для каждого измерения.

- *Смещение* отмечает *начало окна* в измерении.
- *Размер* отмечает область окна в измерении. В качестве *конца окна* в измерении используется `offset + size - 1` .
- *Шаг* указывает, как перемещаться по элементам измерения.
  - Величина шага указывает, сколько элементов следует продвинуть при копировании в пределах окна.
  - Если шаг с шагом положительный, элементы копируются начиная с *начала* окна в измерении.
  - Если шаг по индексу отрицательный, элементы копируются, начиная с *конца* окна в измерении.

В следующем псевдо-коде показано, как копируются элементы с помощью окна ввода. Обратите внимание, как копируются элементы в измерении с начала до конца с положительным шагом и копируются из End в начало с отрицательным шагом.

```
CopyStart = InputWindowOffsets
for dimension i in [0, DimensionCount - 1]:
    if InputWindowStrides[i] < 0:
        CopyStart[i] += InputWindowSizes[i] - 1 // start at the end of the window in this dimension

OutputTensor[OutputCoordinates] = InputTensor[CopyStart + InputWindowStrides * OutputCoordinates]
```

Окно ввода не должны быть пустым в любом измерении, а окно не должны выходит за пределы размера входного тензорные (операции чтения вне границ не разрешены). Размер и шаг окна фактически ограничивают количество элементов, которые могут быть скопированы из каждого измерения `i` входного тензорные.

```
MaxCopiedElements[i] = 1 + (InputWindowSize[i] - 1) / InputWindowStrides[i]
```

Выходной тензорные не требуется для копирования всех достижимых элементов в окне. Срез допустим, пока `1 <= OutputSizes[i] <= MaxCopiedElements[i]` .

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_SLICE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *InputWindowOffsets;
  const UINT            *InputWindowSizes;
  const INT             *InputWindowStrides;
};
```



## <a name="members"></a>Члены

`InputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Тензорные, из которого извлекаются срезы.


`OutputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, в который записываются результаты среза данных.


`DimensionCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Число измерений. Это поле определяет размер массивов *инпутвиндовоффсетс*, *инпутвиндовсизес* и *инпутвиндовстридес* . Это значение должно соответствовать *DimensionCountным* десяткам входных и выходных данных. Это значение должно находиться в диапазоне от 1 до 8 включительно, начиная с `DML_FEATURE_LEVEL_3_0` версии. для более ранних уровней компонентов требуется значение 4 или 5.


`InputWindowOffsets`

Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Массив, содержащий начало (в элементах) окна ввода в каждом измерении. Значения в массиве должны соответствовать ограничению `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`


`InputWindowSizes`

Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Массив, содержащий экстент (в элементах) окна ввода в каждом измерении. Значения в массиве должны соответствовать ограничению `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`


`InputWindowStrides`

Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Массив, содержащий шаг среза по каждому измерению входного тензорные в элементах. Величина шага указывает, сколько элементов следует продвинуть при копировании в окне ввода. Знак шага определяет, копируются ли элементы, начиная с начала окна (положительный шаг) или заканчивая окном (отрицательный шаг). Шаг не может быть равен 0.

## <a name="examples"></a>Примеры

В следующих примерах используется такой же входной тензорные.

```
InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[ 1,  2,  3,  4],
   [ 5,  6,  7,  8],
   [ 9, 10, 11, 12],
   [13, 14, 15, 16]]]]
```

### <a name="example-1-strided-slice-with-positive-strides"></a>Пример 1. Срез с шагом с положительным шагом

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, 2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[ 2,  4],
   [10, 12]]]]
```

Скопированные элементы рассчитываются следующим образом. 
```
Output[0,0,0,0] = {0,0,0,1} + {1,1,2,2} * {0,0,0,0} = Input[{0,0,0,1}] = 2
Output[0,0,0,1] = {0,0,0,1} + {1,1,2,2} * {0,0,0,1} = Input[{0,0,0,3}] = 4
Output[0,0,1,0] = {0,0,0,1} + {1,1,2,2} * {0,0,1,0} = Input[{0,0,2,1}] = 10
Output[0,0,1,1] = {0,0,0,1} + {1,1,2,2} * {0,0,1,1} = Input[{0,0,2,3}] = 12
```

### <a name="example-2-strided-slice-with-negative-strides"></a>Пример 2. Срез с шагом с отрицательным шагом

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, -2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[14, 16],
   [ 6,  8]]]]
```

Помните, что измерения с отрицательным шагом окна начинают копирование в конец окна ввода для этого измерения; Это делается путем добавления `InputWindowSize[i] - 1` к смещению окна. Измерения с положительным шагом просто начинаются с `InputWindowOffset[i]` .
- Ось 0 ( `+1` Window STRIDE) начинает копирование в `InputWindowOffsets[0] = 0` . 
- Ось 1 ( `+1` Window STRIDE) начинает копирование в `InputWindowOffsets[1] = 0` . 
- Ось 2 ( `-2` Window STRIDE) начинает копирование в `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3` . 
- Ось 3 ( `+2` Window STRIDE) начинает копирование в `InputWindowOffsets[3] = 1` . 

Скопированные элементы рассчитываются следующим образом. 
```
Output[0,0,0,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,0} = Input[{0,0,3,1}] = 14
Output[0,0,0,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,1} = Input[{0,0,3,3}] = 16
Output[0,0,1,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,0} = Input[{0,0,1,1}] = 6
Output[0,0,1,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,1} = Input[{0,0,1,3}] = 8
```


## <a name="remarks"></a>Комментарии
Этот оператор аналогичен [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc), но он отличается двумя важными способами.

- Шаг среза может быть отрицательным, что позволяет реверсировать значения по измерениям.
- Размеры окна ввода не обязательно должны совпадать с размерами выходных тензорные.

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Ограничения тензорные
*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковые типы *данных* и *DimensionCount*.

## <a name="tensor-support"></a>Поддержка тензорные
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 и выше
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | от 1 до 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| аутпуттенсор | Выходные данные | от 1 до 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 и выше
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | от 4 до 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| аутпуттенсор | Выходные данные | от 4 до 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |


## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |