---
UID: NS:directml.DML_SLICE_GRAD_OPERATOR_DESC
title: DML_SLICE_GRAD_OPERATOR_DESC
description: Вычисление градиентов обратного распространения для среза (см. [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).
helpviewer_keywords:
- DML_SLICE_GRAD_OPERATOR_DESC
- DML_SLICE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_SLICE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_SLICE_GRAD_OPERATOR_DESC, DML_SLICE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
- directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
ms.openlocfilehash: a22efe9b0b74f5fdc7b498b97784086f40f243b9
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417650"
---
# <a name="dml_slice_grad_operator_desc-structure-directmlh"></a>Структура DML_SLICE_GRAD_OPERATOR_DESC (директмл. h)

Вычисление градиентов обратного распространения для среза (см. [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).

Помните, что [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) извлекает подобласть входного тензорные. При наличии *инпутградиенттенсор* с теми же размерами, что и в *выходных данных* эквивалентного **DML_SLICE1_OPERATOR_DESC**, этот оператор создает *аутпутградиенттенсор* с теми же размерами, что и *входные данные* **DML_SLICE1_OPERATOR_DESC**. Фрагментированные элементы распространяются на выходные данные, а все остальные элементы устанавливаются в значение 0.

В качестве примера рассмотрим **DML_SLICE1_OPERATOR_DESC** , который извлекает из тензорные следующие элементы:

```
InputTensor            OutputTensor
[[a, b, c, d],
 [e, f, g, h],   Slice   [[a, c],
 [i, j, k, l],    -->     [i, k]]
 [m, n, o, p]]
```

Если указаны те же  / *размеры* инпутвиндовоффсетс /  , что и в приведенном выше примере, этот оператор будет выполнять следующее преобразование.

```
InputGradientTensor       OutputGradientTensor
                             [[a, 0, c, 0],
      [[a, c],   SliceGrad    [0, 0, 0, 0],
       [i, k]]      -->       [i, 0, k, 0],
                              [0, 0, 0, 0]]
```

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис

```cpp
struct DML_SLICE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* InputWindowOffsets;
  _Field_size_(DimensionCount) const UINT* InputWindowSizes;
  _Field_size_(DimensionCount) const INT* InputWindowStrides;
};
```

## <a name="members"></a>Участники

`InputGradientTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Входящий градиент тензорные. Обычно это получается из выходных данных обратного распространения предыдущего слоя. Как правило, этот тензорные будет иметь те же размеры, что и *выходные данные* соответствующего [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) в прямом прохождении.

`OutputGradientTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Выходной тензорные, содержащий нераспространяемые градиенты. Как правило, этот тензорные будет иметь те же размеры, что и *входные данные* соответствующего [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) в прямом прохождении.

`DimensionCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Число элементов в массивах *инпутвиндовоффсетс*, *инпутвиндовсизес* и *инпутвиндовстридес* . Это значение должно равняться *DimensionCount* , указанному в *инпутградиенттенсор* и *аутпутградиенттенсор*.

`InputWindowOffsets`

Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

См. раздел *инпутвиндовоффсетс* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).

`InputWindowSizes`

Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

См. раздел *инпутвиндовсизес* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).

`InputWindowStrides`

Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

См. раздел *инпутвиндовстридес* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).

Обратите внимание, что в отличие от **DML_SLICE1_OPERATOR_DESC** этот оператор требует ненулевой STRIDE. Это обусловлено тем, что с нулевым шагом, что элемент input должен сопоставляться с каждым выходным элементом, поэтому невозможно выполнить обратное распространение. Как и **DML_SLICE1_OPERATOR_DESC**, отрицательный шаг переворачивает направление окна ввода по этой оси.

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Ограничения тензорные
*Инпутградиенттенсор* и *аутпутградиенттенсор* должны иметь одинаковые типы *данных* и *DimensionCount*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпутградиенттенсор | Входные данные | от 1 до 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| аутпутградиенттенсор | Выходные данные | от 1 до 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |