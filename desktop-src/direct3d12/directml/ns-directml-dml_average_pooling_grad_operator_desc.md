---
UID: NS:directml.DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
title: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
description: Вычисляет градиенты обратного распространения для среднего количества пулов (см. [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).
helpviewer_keywords:
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC, DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: aaa2b5d2becac421214afe7c643426c1c93cf899
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418013"
---
# <a name="dml_average_pooling_grad_operator_desc-structure-directmlh"></a>Структура DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC (директмл. h)

Вычисляет градиенты обратного распространения для среднего количества пулов (см. [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).

Рассмотрим **DML_AVERAGE_POOLING_OPERATOR_DESC** 2x2 без заполнения и шаг 1, который выполняет следующее.

```
InputTensor             OutputTensor
[[[[1, 2, 3],   AvgPool  [[[[3, 4],
   [4, 5, 6],     -->       [6, 7]]]]
   [7, 8, 9]]]]
```

Каждое окно 2x2 во входном тензорные оценивается как среднее значение для получения одного элемента выходных данных (количество нулей для элементов после края). Ниже приведен пример выходных данных **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** , заданных аналогичными параметрами.

```
InputGradientTensor            OutputGradientTensor
  [[[[1, 2],     AvgPoolGrad  [[[[0.25, 0.75, 0.5],
     [3, 4]]]]       -->         [   1,  2.5, 1.5],
                                 [0.75, 1.75,   1]]]]
```

Обратите внимание, что значения в *аутпутградиенттенсор* представляют взвешенные вклады этого элемента в *аутпуттенсор* во время исходного оператора [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) .

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис

```cpp
struct DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  BOOL IncludePadding;
};
```

## <a name="members"></a>Участники

`InputGradientTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Входящий градиент тензорные. Обычно это получается из выходных данных обратного распространения предыдущего слоя. Как правило, этот тензорные будет иметь те же размеры, что и *выходные данные* соответствующего [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) в рамках прямого прохода.

`OutputGradientTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Выходной тензорные, содержащий нераспространяемые градиенты. Как правило, этот тензорные будет иметь те же размеры, что и *входные данные* соответствующего [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) в прямом прохождении.

`DimensionCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Число элементов в массивах *stride*, *WindowSize*, *стартпаддинг* и *ендпаддинг* . Это значение должно равняться количеству пространственных измерений. Количество пространственных измерений равно 2, если предоставлены десятки или 3, если указаны дополнительные десятки.

`Strides`

Тип: \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***

См. *шаг* в [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

`WindowSize`

Тип: \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***

См. раздел *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

`StartPadding`

Тип: \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***

См. раздел *стартпаддинг* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

`EndPadding`

Тип: \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***

См. раздел *ендпаддинг* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

`IncludePadding`

Тип: <b> <a href="/windows/win32/winprog/windows-data-types">bool</a> .</b>

См. раздел *инклудепаддинг* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Ограничения тензорные
*Инпутградиенттенсор* и *аутпутградиенттенсор* должны иметь одинаковые типы *данных* и *DimensionCount*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпутградиенттенсор | Входные данные | от 4 до 5 | FLOAT32, FLOAT16 |
| аутпутградиенттенсор | Выходные данные | от 4 до 5 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |