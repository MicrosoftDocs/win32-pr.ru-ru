---
UID: NS:directml.DML_ARGMAX_OPERATOR_DESC
title: DML_ARGMAX_OPERATOR_DESC
description: Выводит индексы элементов с максимальным значением в одном или нескольких измерениях входного тензорные.
helpviewer_keywords:
- DML_ARGMAX_OPERATOR_DESC
- DML_ARGMAX_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMAX_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMAX_OPERATOR_DESC, DML_ARGMAX_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
- directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
ms.openlocfilehash: 4c2852c3d301a12d318c5e3006b26830c6eaa6e1
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418033"
---
# <a name="dml_argmax_operator_desc-structure-directmlh"></a>Структура DML_ARGMAX_OPERATOR_DESC (директмл. h)

Выводит индексы элементов с максимальным значением в одном или нескольких измерениях входного тензорные.

Каждый элемент Output является результатом применения *аргмакс* сокращения для подмножества входных тензорные. Функция *аргмакс* выводит индекс элемента с максимальным значением в наборе входных элементов. Входные элементы, участвующие в каждом уменьшении, определяются предоставленными осями ввода. Аналогичным образом, каждый выходной индекс по отношению к предоставленным осям входных данных. Если указаны все входные оси, оператор применяет одно *аргмаксное* уменьшение и создает один выходной элемент.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_ARGMAX_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a>Участники

`InputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Тензорные, из которого производится чтение.

`OutputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, в который записываются результаты. Каждый элемент Output является результатом *аргмакс* сокращения для подмножества элементов из *инпуттенсор*. 

- *DimensionCount* должен соответствовать *инпуттенсор. DimensionCount* (ранг входного тензорные сохраняется).
- *Размеры* должны соответствовать *инпуттенсор. sizes*, за исключением измерений, содержащихся в сокращенных *осях*, которые должны иметь размер 1.

`AxisCount`

Тип: **[uint](../../winprog/windows-data-types.md)**

Число осей, которые необходимо уменьшить. Это поле определяет размер массива *осей* .

`Axes`

Тип: \_ Field_size \_ (аксискаунт) **const [uint](../../winprog/windows-data-types.md) \***

Оси, которые необходимо уменьшить. Значения должны находиться в диапазоне `[0, InputTensor.DimensionCount - 1]` .

`AxisDirection`

Тип: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**

Определяет, какой индекс следует выбрать, если несколько входных элементов имеют одинаковое значение.
- **DML_AXIS_DIRECTION_INCREASING** возвращает индекс первого элемента с максимальным значением (например, `argmax({3,2,1,2,3}) = 0` ).
- **DML_AXIS_DIRECTION_DECREASING** возвращает индекс последнего элемента с максимальным значением (например, `argmax({3,2,1,2,3}) = 4` ).

## <a name="examples"></a>Примеры

В примерах в этом разделе используется одинаковый двухмерный входной тензорные.

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmax-to-columns"></a>Пример 1. Применение *аргмакс* к столбцам

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[1,  // argmax({1, 3, 2})
  2,  // argmax({2, 0, 5})
  1]] // argmax({3, 4, 2})
```

### <a name="example-2-applying-argmax-to-rows"></a>Пример 2. Применение *аргмакс* к строкам

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[2], // argmax({1, 2, 3})
 [2], // argmax({3, 0, 4})
 [1]] // argmax({2, 5, 2})
```

### <a name="example-3-applying-argmax-to-all-axes-the-entire-tensor"></a>Пример 3. Применение *аргмакс* ко всем осям (весь тензорные)

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[7]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a>Remarks
Размеры выходных тензорные должны совпадать с размерами входных тензорные, за исключением осей с меньшими осями, которые должны иметь значение 1.

Если *аксисдиректион* имеет [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), этот API эквивалентен [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) с [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).

Подмножество этой функции предоставляется с помощью оператора [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) и поддерживается на более ранних уровнях функций директмл.

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Ограничения тензорные
*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковый *DimensionCount*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | от 1 до 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| аутпуттенсор | Выходные данные | от 1 до 8 | INT64, INT32, UINT64, UINT32 |

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |