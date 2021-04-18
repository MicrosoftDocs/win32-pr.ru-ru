---
UID: NS:directml.DML_CONVOLUTION_INTEGER_OPERATOR_DESC
title: DML_CONVOLUTION_INTEGER_OPERATOR_DESC
description: Выполняет свертывание *филтертенсор* с *инпуттенсор*. Этот оператор выполняет пересылку по целочисленным данным.
helpviewer_keywords:
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CONVOLUTION_INTEGER_OPERATOR_DESC, DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.openlocfilehash: c16690ea1e3049ffeba398bbbaca2003f965a832
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719983"
---
# <a name="dml_convolution_integer_operator_desc-structure-directmlh"></a>Структура DML_CONVOLUTION_INTEGER_OPERATOR_DESC (директмл. h)

Выполняет свертывание *филтертенсор* с *инпуттенсор*. Этот оператор выполняет пересылку по целочисленным данным. Необязательные десятки точек нулевой точки также можно использовать для вычитания значений нулевой точки из входных данных и фильтра тензорные.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_CONVOLUTION_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
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

Объект тензорные, содержащий входные данные. Ожидаемые размеры *инпуттенсор* : `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .


`InputZeroPointTensor`

Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Необязательный тензорные, содержащий входные данные нулевой точки. Ожидаемые размеры *инпутзеропоинттенсор* : `{ 1, 1, 1, 1 }` .


`FilterTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий данные фильтра. Ожидаемые размеры *филтертенсор* : `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .


`FilterZeroPointTensor`

Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Необязательный тензорные, содержащий данные нулевой точки фильтра. Ожидаемые размеры *филтерзеропоинттенсор* , `{ 1, 1, 1, 1 }` Если требуется по тензорные дискретизация, или `{ 1, OutputChannelCount, 1, 1 }` Если требуется дискретизация для каждого канала.


`OutputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, в который записываются результаты. Ожидаемые размеры *аутпуттенсор* : `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .


`DimensionCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Количество пространственных измерений для операции свертки. Пространственные измерения — это нижние измерения *филтертенсор* свертки. Это значение также определяет размер массивов *stride*, *дилатионс*, *стартпаддинг* и *ендпаддинг* . Поддерживается только значение 2.


`Strides`

Тип: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***

Массив, содержащий шаг операции свертки. Эти шаг применяются к фильтру свертки. Они отделены от тензорные STRIDE, которые включены в [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).


`Dilations`

Тип: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***

Массив, содержащий дилатионс операции свертки. Дилатионс — это шаг, примененный к элементам ядра фильтра. Это влияет на моделирование ядра более крупного фильтра, добавляя внутренние элементы ядра фильтрации с нулями.


`StartPadding`

Тип: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***

Массив, содержащий значения заполнения, применяемые к началу каждого пространственного измерения фильтра и входного тензорные операции свертки.


`EndPadding`

Тип: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***

Массив, содержащий значения заполнения, применяемые к концу каждого пространственного измерения фильтра и входного тензорные операции свертки.


`GroupCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Число групп, в которые необходимо разделить операцию свертки. *Граупкаунт* можно использовать для достижения более глубокого свертки, задав *граупкаунт* равным количеству входных каналов. Это делит свертывание в отдельное свертка на входной канал.

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Ограничения тензорные
* *Филтертенсор* и *филтерзеропоинттенсор* должны иметь одинаковый *тип данных*.
* *Инпуттенсор* и *инпутзеропоинттенсор* должны иметь одинаковый *тип данных*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Измерения | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | {Батчкаунт, Инпутчаннелкаунт, Инпусеигхт, Инпутвидс} | 4 | INT8, UINT8 |
| инпутзеропоинттенсор | Необязательный ввод | {1, 1, 1, 1} | 4 | INT8, UINT8 |
| филтертенсор | Входные данные | {Филтербатчкаунт, Филтерчаннелкаунт, Филтерхеигхт, Филтервидс} | 4 | INT8, UINT8 |
| филтерзеропоинттенсор | Необязательный ввод | {1, Филтерзеропоинтчаннелкаунт, 1, 1} | 4 | INT8, UINT8 |
| аутпуттенсор | Выходные данные | {Батчкаунт, Аутпутчаннелкаунт, Аутпусеигхт, Аутпутвидс} | 4 | INT32 |



## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |