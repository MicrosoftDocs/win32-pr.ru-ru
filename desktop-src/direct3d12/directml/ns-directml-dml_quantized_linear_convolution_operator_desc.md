---
UID: NS:directml.DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
description: Выполняет свертывание *филтертенсор* с *инпуттенсор*. Этот оператор выполняет пересылку данных квантования. Этот оператор математически эквивалентен декуантизинг входным данным, включающим, а затем куантизинг выходные данные.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_convolution_operator_desc
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
ms.openlocfilehash: 4dd50d80dfe4ae60e3fe7e67124ef00bfbc7bf2b
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803876"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a>Структура DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC (директмл. h)
Выполняет свертывание *филтертенсор* с *инпуттенсор*. Этот оператор выполняет пересылку данных квантования. Этот оператор математически эквивалентен декуантизинг входным данным, включающим, а затем куантизинг выходные данные. 

К линейным функциям квантуем, используемым этим оператором, относятся линейные функции дискретизация

### <a name="dequantize-function"></a>Функция декуантизе

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a>Функция квантуем

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputScaleTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterScaleTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *BiasTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```



## <a name="members"></a>Члены

`InputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий входные данные. Ожидаемые размеры *инпуттенсор* : `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` .


`InputScaleTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий входные данные шкалы. Ожидаемые размеры `InputScaleTensor` — `{ 1, 1, 1, 1 }` . Это значение шкалы используется для декуантизинг входных значений.


`InputZeroPointTensor`

Тип: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Необязательный тензорные, содержащий входные данные нулевой точки. Ожидаемые размеры *инпутзеропоинттенсор* : `{ 1, 1, 1, 1 }` . Это значение нулевой точки используется для декуантизинг входных значений.


`FilterTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий данные фильтра. Ожидаемые размеры *филтертенсор* : `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .


`FilterScaleTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий данные шкалы фильтра. Ожидаемыми размерами `FilterScaleTensor` являются, `{ 1, 1, 1, 1 }` Если требуется для каждого тензорные дискретизация, или `{ 1, OutputChannelCount, 1, 1 }` Если требуется дискретизация на канал. Это значение шкалы используется для декуантизинг значений фильтра.


`FilterZeroPointTensor`

Тип: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Необязательный тензорные, содержащий данные нулевой точки фильтра. Ожидаемые размеры *филтерзеропоинттенсор* , `{ 1, 1, 1, 1 }` Если требуется по тензорные дискретизация, или `{ 1, OutputChannelCount, 1, 1 }` Если требуется дискретизация по каналу. Это значение нулевой точки используется для декуантизинг значений фильтра.


`BiasTensor`

Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий данные смещения. Тензорные смещения — это тензорные, содержащий данные, которые рассылаются по выходным тензорные в конце свертки, который добавляется к результату. Ожидаемые размеры Биастенсор `{ 1, OutputChannelCount, 1, 1 }` для 4d.


`OutputScaleTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий данные шкалы выходных данных. Ожидаемые размеры Аутпутскалетенсор: `{ 1, 1, 1, 1 }` . Это значение входной шкалы используется для куантизинг выходных значений свертки.


`OutputZeroPointTensor`

Тип: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Необязательный тензорные, содержащий данные нулевой точки фильтра. Ожидаемые размеры Аутпутзеропоинттенсор: `{ 1, 1, 1, 1 }` . Это значение ввода нулевой точки используется для куантизинг для свертки выходных значений.


`OutputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, в который записываются результаты. Ожидаемые размеры Аутпуттенсор: `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .


`DimensionCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Количество пространственных измерений для операции свертки. Пространственные измерения — это нижние измерения фильтра свертки тензорные *филтертенсор*. Это значение также определяет размер массивов *stride*, *дилатионс*, *стартпаддинг* и *ендпаддинг* . Поддерживается только значение 2.


`Strides`

Тип: \_ Field_size \_ (DimensionCount) **const [uint](/windows/win32/winprog/windows-data-types) \***

Шаг операции свертки. Эти шаг применяются к фильтру свертки. Они отделены от тензорные STRIDE, которые включены в [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).


`Dilations`

Тип: \_ Field_size \_ (DimensionCount) **const [uint](/windows/win32/winprog/windows-data-types) \***

Дилатионс операции свертки. Дилатионс — это шаг, примененный к элементам ядра фильтра. Это влияет на моделирование ядра более крупного фильтра, добавляя внутренние элементы ядра фильтрации с нулями.


`StartPadding`

Тип: \_ Field_size \_ (DimensionCount) **const [uint](/windows/win32/winprog/windows-data-types) \***

Значения заполнения, применяемые к началу каждого пространственного измерения фильтра и входного тензорные операции свертки.


`EndPadding`

Тип: \_ Field_size \_ (DimensionCount) **const [uint](/windows/win32/winprog/windows-data-types) \***

Значения заполнения, применяемые к концу каждого пространственного измерения фильтра и входного тензорные операции свертки.


`GroupCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Число групп, в которые следует разделить операцию свертки. *Граупкаунт* можно использовать для достижения более глубокого свертки, задав *граупкаунт* равным количеству входных каналов. Это делит свертывание в отдельное свертка на входной канал. 

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Ограничения тензорные
* *Филтертенсор* и *филтерзеропоинттенсор* должны иметь одинаковый *тип данных*.
* *Инпуттенсор* и *инпутзеропоинттенсор* должны иметь одинаковый *тип данных*.
* *Аутпуттенсор* и `OutputZeroPointTensor` должны иметь один и тот же *тип данных*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | 4 | INT8, UINT8 |
| инпутскалетенсор | Входные данные | 4 | FLOAT32 |
| инпутзеропоинттенсор | Необязательный ввод | 4 | INT8, UINT8 |
| филтертенсор | Входные данные | 4 | INT8, UINT8 |
| филтерскалетенсор | Входные данные | 4 | FLOAT32 |
| филтерзеропоинттенсор | Необязательный ввод | 4 | INT8, UINT8 |
| биастенсор | Необязательный ввод | 4 | INT32 |
| аутпутскалетенсор | Входные данные | 4 | FLOAT32 |
| аутпутзеропоинттенсор | Необязательный ввод | 4 | INT8, UINT8 |
| аутпуттенсор | Выходные данные | 4 | INT8, UINT8 |



## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |