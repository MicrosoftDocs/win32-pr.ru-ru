---
UID: NS:directml.DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
title: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
description: Выполняет функцию умножения матриц для целочисленных данных.
helpviewer_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_matrix_multiply_integer_operator_desc
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
ms.keywords: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC, DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure, direct3d12.dml_matrix_multiply_integer_operator_desc, directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
ms.custom: 19H1
f1_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f6ecccf49b0d7123e6f41321c7ba1bf8e8d4ad87
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719939"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a>Структура DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC (директмл. h)
Выполняет функцию умножения матриц для целочисленных данных.

Этот оператор требует, чтобы матрица ввода данных с десятков входов в значение 4D, отформатированная как `{ BatchCount, ChannelCount, Height, Width }` . Оператор умножения матрицы выполняет Батчкаунт * Чаннелкаунт число независимых матричных матриц.

Например, если *атенсор* имеет *размеры* `{ BatchCount, ChannelCount, M, K }` , а *бтенсор* имеет размеры,  `{ BatchCount, ChannelCount, K, N }` а *аутпуттенсор* имеет *размеры* , `{ BatchCount, ChannelCount, M, N }` то оператор умножения матрицы будет выполнять батчкаунт * чаннелкаунт независимых матричных умножений измерений {m, K} x {K, N} = {m, n}.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a>Члены

`ATensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий данные. Размеры тензорные должны быть `{ BatchCount, ChannelCount, M, K }` .


`AZeroPointTensor`

Тип: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Необязательный тензорные, содержащий данные нулевой точки Атенсор. Ожидаемые размеры объекта `AZeroPointTensor` : `{ 1, 1, 1, 1 }` Если для каждого тензорные дискретизация требуется или `{ 1, 1, M, 1 }` Если требуется дискретизация для каждой строки. Эти значения нулевых точек используются для декуантизинг значений *атенсор* .


`BTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий данные B. Размеры тензорные должны быть `{ BatchCount, ChannelCount, K, N }` .


`BZeroPointTensor`

Тип: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Необязательный тензорные, содержащий данные нулевой точки *бтенсор* . Ожидаемые размеры элемента `BZeroPointTensor` —, `{ 1, 1, 1, 1 }` Если требуется для каждого тензорные дискретизация, или `{ 1, 1, 1, N }` Если требуется для каждого столбца дискретизация. Эти значения нулевых точек используются для декуантизинг значений Бтенсор.


`OutputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, в который записываются результаты. Это тензорные измерения `{ BatchCount, ChannelCount, M, N }` .

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Ограничения тензорные
* *Атенсор* и `AZeroPointTensor` должны иметь один и тот же *тип данных*.
* *Бтенсор* и `BZeroPointTensor` должны иметь один и тот же *тип данных*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Измерения | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| атенсор | Входные данные | {Батчкаунт, Чаннелкаунт, M, K} | 4 | INT8, UINT8 |
| азеропоинттенсор | Необязательный ввод | {1, 1, Азеропоинткаунт, 1} | 4 | INT8, UINT8 |
| бтенсор | Входные данные | {Батчкаунт, Чаннелкаунт, K, N} | 4 | INT8, UINT8 |
| бзеропоинттенсор | Необязательный ввод | {1, 1, 1, Бзеропоинткаунт} | 4 | INT8, UINT8 |
| аутпуттенсор | Выходные данные | {Батчкаунт, Чаннелкаунт, M, N} | 4 | INT32 |



## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |