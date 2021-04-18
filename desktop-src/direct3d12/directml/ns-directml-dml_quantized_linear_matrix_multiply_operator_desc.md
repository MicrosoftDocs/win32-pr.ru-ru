---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: Выполняет функцию умножения матрицы для данных квантования. Этот оператор математически эквивалентен декуантизинг входным данным, затем выполняет умножение матрицы и затем куантизинг выходные данные.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_matrix_multiply_operator_desc
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.openlocfilehash: d0b20a37bca6ddf6083b116b53290a6b6b2084f4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719995"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a>Структура DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC (директмл. h)
Выполняет функцию умножения матрицы для данных квантования. Этот оператор математически эквивалентен декуантизинг входным данным, затем выполняет умножение матрицы и затем куантизинг выходные данные.

Этот оператор требует, чтобы матрица ввода данных с десятков входов в значение 4D была отформатирована как `{ BatchCount, ChannelCount, Height, Width }` . Оператор умножения матрицы выполняет Батчкаунт * Чаннелкаунт число независимых матричных матриц. 

Например, если *атенсор* имеет *размеры* `{ BatchCount, ChannelCount, M, K }` , а *бтенсор* имеет размеры,  `{ BatchCount, ChannelCount, K, N }` а *аутпуттенсор* имеет *размеры* , `{ BatchCount, ChannelCount, M, N }` то оператор умножения матрицы будет выполнять батчкаунт * чаннелкаунт независимых матричных умножений измерений {m, K} x {K, N} = {m, n}. 

### <a name="dequantize-function"></a>Функция декуантизе

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a>Функция квантуем

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AScaleTensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BScaleTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a>Члены

`ATensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий данные. Размеры тензорные должны быть `{ BatchCount, ChannelCount, M, K }` .


`AScaleTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий данные шкалы Атенсор. Ожидаемые размеры элемента `AScaleTensor` —, `{ 1, 1, 1, 1 }` Если требуется для каждого тензорные дискретизация, или `{ 1, 1, M, 1 }` Если требуется дискретизация строки. Эти значения масштаба используются для декуантизинг значений.


`AZeroPointTensor`

Тип: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Необязательный тензорные, содержащий данные нулевой точки *атенсор* . Ожидаемые размеры Азеропоинттенсор, `{ 1, 1, 1, 1 }` Если требуется по тензорные дискретизация, или `{ 1, 1, M, 1 }` Если требуется строка дискретизация. Эти значения нулевых точек используются для декуантизинг значений Атенсор.


`BTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий данные B. Размеры тензорные должны быть `{ BatchCount, ChannelCount, K, N }` .


`BScaleTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий данные шкалы *бтенсор* . Ожидаемые размеры элемента `BScaleTensor` —, `{ 1, 1, 1, 1 }` Если требуется для каждого тензорные дискретизация, или `{ 1, 1, 1, N }` Если требуется для каждого столбца дискретизация. Эти значения масштаба используются для декуантизинг значений *бтенсор* .


`BZeroPointTensor`

Тип: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Необязательный тензорные, содержащий данные нулевой точки *бтенсор* . Ожидаемые размеры элемента `BZeroPointTensor` —, `{ 1, 1, 1, 1 }` Если требуется для каждого тензорные дискретизация, или `{ 1, 1, 1, N }` Если требуется для каждого столбца дискретизация. Эти значения нулевых точек используются для декуантизинг значений *бтенсор* .


`OutputScaleTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий данные шкалы фильтра. Ожидаемые размеры элемента `OutputScaleTensor` —, `{ 1, 1, 1, 1 }` Если требуется для каждого тензорные дискретизация, или `{ 1, 1, M, 1 }` Если требуется дискретизация строки. Это значение шкалы используется для декуантизинг значений фильтра.


`OutputZeroPointTensor`

Тип: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Необязательный тензорные, содержащий данные нулевой точки фильтра. Ожидаемые размеры объекта `OutputZeroPointTensor` — `{ 1, 1, 1, 1 }` Если для каждого тензорные дискретизация требуется или `{ 1, 1, M, 1 }` Если требуется дискретизация строки. Это значение нулевой точки используется для декуантизинг значений фильтра.


`OutputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, в который записываются результаты. Это тензорные измерения `{ BatchCount, ChannelCount, M, N }` .

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Ограничения тензорные
* *Атенсор* и `AZeroPointTensor` должны иметь один и тот же *тип данных*.
* *Бтенсор* и `BZeroPointTensor` должны иметь один и тот же *тип данных*.
* *Аутпуттенсор* и `OutputZeroPointTensor` должны иметь один и тот же *тип данных*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| атенсор | Входные данные | 4 | INT8, UINT8 |
| аскалетенсор | Входные данные | 4 | FLOAT32 |
| азеропоинттенсор | Необязательный ввод | 4 | INT8, UINT8 |
| бтенсор | Входные данные | 4 | INT8, UINT8 |
| бскалетенсор | Входные данные | 4 | FLOAT32 |
| бзеропоинттенсор | Необязательный ввод | 4 | INT8, UINT8 |
| аутпутскалетенсор | Входные данные | 4 | FLOAT32 |
| аутпутзеропоинттенсор | Необязательный ввод | 4 | INT8, UINT8 |
| аутпуттенсор | Выходные данные | 4 | INT8, UINT8 |



## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |