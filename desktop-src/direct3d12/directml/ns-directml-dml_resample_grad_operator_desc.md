---
UID: NS:directml.DML_RESAMPLE_GRAD_OPERATOR_DESC
title: DML_RESAMPLE_GRAD_OPERATOR_DESC
description: Вычисление градиентов обратного распространения для повторной выборки (см. [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).
helpviewer_keywords:
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- DML_RESAMPLE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RESAMPLE_GRAD_OPERATOR_DESC, DML_RESAMPLE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.openlocfilehash: 5808381f2e812ac20399b46672e51acd063bc6a5
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719993"
---
# <a name="dml_resample_grad_operator_desc-structure-directmlh"></a>Структура DML_RESAMPLE_GRAD_OPERATOR_DESC (директмл. h)

Вычисление градиентов обратного распространения для повторной выборки (см. [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).

**DML_RESAMPLE1_OPERATOR_DESC** выполняет масштабирование произвольных измерений входного тензорные, используя либо ближайшую выборку, либо билинейной интерполяцию. При наличии *инпутградиенттенсор* с теми же размерами, что и в *выходных данных* эквивалентного **DML_RESAMPLE1_OPERATOR_DESC**, этот оператор создает *аутпутградиенттенсор* с теми же размерами, что и *входные данные* **DML_RESAMPLE1_OPERATOR_DESC**.

В качестве примера рассмотрим **DML_RESAMPLE1_OPERATOR_DESC** , которая выполняет масштабирование по ширине в 1,5 x в ширину, а 0,5 x — по высоте.

```
InputTensor           OutputTensor
[[1, 2],   Resample    [1, 1, 2]
 [3, 4]]      -->      
```

Обратите внимание, что элемент 0-ом входного тензорные (со значением 1) участвует в двух элементах в выходных данных, первый элемент (со значением 2) участвует в одном элементе выходных данных, а второй и третий элементы (со значениями 3 и 4) не вносят элементов в выходные данные.

Соответствующий **DML_RESAMPLE_GRAD_OPERATOR_DESC** будет выполнять следующие действия.

```
InputGradientTensor           OutputGradientTensor
    [4, 5, 6]      ResampleGrad    [[9, 6],
                       -->          [0, 0]]
```

Обратите внимание, что значения в *аутпутградиенттенсор* представляют взвешенные вклады этого элемента в *аутпуттенсор* во время исходного оператора **DML_RESAMPLE1_OPERATOR_DESC** .

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис

```cpp
struct DML_RESAMPLE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const FLOAT* Scales;
  _Field_size_(DimensionCount) const FLOAT* InputPixelOffsets;
  _Field_size_(DimensionCount) const FLOAT* OutputPixelOffsets;
};
```

## <a name="members"></a>Члены

`InputGradientTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Входящий градиент тензорные. Обычно это получается из выходных данных обратного распространения предыдущего слоя. Как правило, этот тензорные будет иметь те же размеры, что и *выходные данные* соответствующего [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) в рамках прямого прохода.

`OutputGradientTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Выходной тензорные, содержащий нераспространяемые градиенты. Как правило, этот тензорные будет иметь те же размеры, что и *входные данные* соответствующего [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) в прямом прохождении.

`InterpolationMode`

Тип: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

См. раздел *интерполатионмоде* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`DimensionCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Число *элементов в массивах Scale,* *инпутпикселоффсетс* и *аутпутпикселоффсетс* . Это значение должно равняться *DimensionCount* , указанному в *инпутградиенттенсор* и *аутпутградиенттенсор*.

`Scales`

Тип: \_ \_ Размер поля \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***

См. раздел *масштабирование* в [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`InputPixelOffsets`

Тип: \_ \_ Размер поля \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***

См. раздел *инпутпикселоффсетс* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`OutputPixelOffsets`

Тип: \_ \_ Размер поля \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***

См. раздел *аутпутпикселоффсетс* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Ограничения тензорные
*Инпутградиенттенсор* и *аутпутградиенттенсор* должны иметь одинаковый *тип данных*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпутградиенттенсор | Входные данные | 4 | FLOAT32, FLOAT16 |
| аутпутградиенттенсор | Выходные данные | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |