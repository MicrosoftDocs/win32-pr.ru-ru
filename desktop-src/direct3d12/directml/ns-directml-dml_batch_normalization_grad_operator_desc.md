---
UID: NS:directml.DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
description: Вычисляются градиенты обратного распространения для [нормализации пакетной обработки](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc).
helpviewer_keywords:
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_batch_normalization_grad_operator_desc
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: 2b94ac1dcf389d424aaf74d615f36cdf7acc804c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550439"
---
# <a name="dml_batch_normalization_grad_operator_desc-directmlh"></a>DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (директмл. h)

Вычисляются градиенты обратного распространения для [нормализации пакетной обработки](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc). **DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** выполняет несколько вычислений, которые подробно описаны в отдельных выходных описаниях.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,5 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* MeanTensor;
    const DML_TENSOR_DESC* VarianceTensor;
    const DML_TENSOR_DESC* ScaleTensor;

    const DML_TENSOR_DESC* OutputGradientTensor;
    const DML_TENSOR_DESC* OutputScaleGradientTensor;
    const DML_TENSOR_DESC* OutputBiasGradientTensor;

    FLOAT Epsilon;
};
```

## <a name="members"></a>Участники

`InputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий входные данные. Обычно это те же тензорные, которые были предоставлены в качестве *инпуттенсор* для [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) в рамках прямого прохода.

`InputGradientTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Входящий градиент тензорные. Обычно это получается из выходных данных обратного распространения предыдущего слоя. Этот тензорные должен иметь те же размеры измерений, что и *инпуттенсор*.

`MeanTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий средние данные. Обычно это те же тензорные, которые были предоставлены в качестве *меантенсор* для [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) в рамках прямого прохода.

Все измерения, размер которых отличается от размера соответствующего измерения *инпуттенсор* , должны иметь размер 1, чтобы их можно было транслировать в соответствии с входными данными.

Например, допустимы следующие размеры.

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 4, 1, 1] or [3, 4, 1, 1] or [3, 4, 5, 1] or [3, 4, 5, 6] or [1, 1, 1, 1]
```

Ниже приведена ошибка, так как для обеспечения совместимости с широковещательной рассылкой все измерения, которые не соответствуют, должны иметь размер 1.

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 2, 1, 1]  // 2 causes an error.
```

`VarianceTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий данные дисперсии. Обычно это те же тензорные, которые были предоставлены в качестве *варианцетенсор* для [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) в рамках прямого прохода. Этот тензорные должен иметь те же размеры измерений, что и *меантенсор*.

`ScaleTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий данные шкалы. Обычно это те же тензорные, которые были предоставлены в качестве *скалетенсор* для [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) в рамках прямого прохода. Этот тензорные должен иметь те же размеры измерений, что и *меантенсор*.

`OutputGradientTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Для каждого соответствующего значения во входных данных — `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))` .

Этот тензорные должен иметь те же размеры измерений, что и *инпуттенсор* / *инпутградиенттенсор*.

`OutputScaleGradientTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Эти тензорные должны иметь те же размеры измерений, что и *меантенсор* / *варианцетенсор* / *скалетенсор*.

Выполняются следующие вычисления или каждое соответствующее значение во входных данных.

`OutputScaleGradient = sum(InputGradient * (Input - Mean) / sqrt(Variance + Epsilon))`

`sum`Вычисляются для всех измерений, которые необходимо транслировать. Если вещание не требуется, сумма не требуется.

Пример приведен ниже.

```
InputTensor              : [3, 4, 5, 6]  
MeanTensor               : [1, 4, 1, 1] // dimensions 0, 2, 3 needed broadcasting  
OutputScaleGradientTensor: [1, 4, 1, 1]  
```

Элемент [0, **0**, 0, 0] из `OutputScaleGradientTensor` является суммой `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` для всех элементов 90 (3 \* 5 \* 6) [[0, 2], **0**, [0, 4], [0, 5]].

`OutputBiasGradientTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Эти тензорные должны иметь те же размеры измерений, что и *меантенсор* / *варианцетенсор* / *скалетенсор*.

Выполняются следующие вычисления или каждое соответствующее значение во входных данных.

`OutputBiasGradient = sum(InputGradient)`  

Значение `sum` вычисляются для всех измерений, которые необходимо транслировать (см. пример для *аутпутскалеградиенттенсор*). Если вещание не требуется, сумма не требуется.

`Epsilon`

Тип: **[float](../../winprog/windows-data-types.md)**

Небольшое значение, добавляемое к дисперсии, чтобы избежать нулевого значения.

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Ограничения тензорные
*Инпутградиенттенсор*, *инпуттенсор*, *меантенсор*, *аутпутбиасградиенттенсор*, *аутпутградиенттенсор*, *OutputScaleGradientTensor*, *ScaleTensor* и *VarianceTensor* должны иметь одинаковые типы *данных* и *DimensionCount*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | от 1 до 8 | FLOAT32, FLOAT16 |
| инпутградиенттенсор | Входные данные | от 1 до 8 | FLOAT32, FLOAT16 |
| меантенсор | Входные данные | от 1 до 8 | FLOAT32, FLOAT16 |
| варианцетенсор | Входные данные | от 1 до 8 | FLOAT32, FLOAT16 |
| скалетенсор | Входные данные | от 1 до 8 | FLOAT32, FLOAT16 |
| аутпутградиенттенсор | Выходные данные | от 1 до 8 | FLOAT32, FLOAT16 |
| аутпутскалеградиенттенсор | Выходные данные | от 1 до 8 | FLOAT32, FLOAT16 |
| аутпутбиасградиенттенсор | Выходные данные | от 1 до 8 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |