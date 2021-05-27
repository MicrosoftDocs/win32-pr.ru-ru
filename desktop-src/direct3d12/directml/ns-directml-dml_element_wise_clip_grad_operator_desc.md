---
UID: NS:directml.DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
title: DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
description: Вычисление градиентов обратного распространения для [элемента, ориентированного на элемент](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc).
helpviewer_keywords:
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC structure
- direct3d12.dml_element_wise_clip_grad_operator_desc
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
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
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
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
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
ms.openlocfilehash: 3b993ca1c027119ae64157db2327a2836445bf43
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550209"
---
# <a name="dml_element_wise_clip_grad_operator_desc-directmlh"></a>DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC (директмл. h)

Вычисление градиентов обратного распространения для [элемента, ориентированного на элемент](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc).

```
f(x, gradient) = if x <= Min then 0
                 if x >= Max then 0
                 else        then gradient
```

Этот оператор поддерживает выполнение на месте, что означает, что в `OutputTensor` процессе привязки допускается псевдоним *инпуттенсор* .

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,5 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    FLOAT Min;
    FLOAT Max;
};
```

## <a name="members"></a>Участники

`InputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Входная функция тензорные. Обычно это те же тензорные, которые были предоставлены в качестве *инпуттенсор* для [DML_ELEMENT_WISE_CLIP_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc) в рамках прямого прохода.

`InputGradientTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Входящий градиент тензорные. Обычно это получается из выходных данных обратного распространения предыдущего слоя. Как правило, этот тензорные будет иметь те же размеры, что и *выходные данные* соответствующего **DML_OPERATOR_ELEMENT_WISE_CLIP** в рамках прямого прохода.

`OutputGradientTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Выходной тензорные, содержащий нераспространяемые градиенты. Как правило, этот тензорные будет иметь те же размеры, что и *входные данные* соответствующего **DML_OPERATOR_ELEMENT_WISE_CLIP** в прямом прохождении.

`Min`

Тип: **[float](../../winprog/windows-data-types.md)**

Минимальное значение. Если x находится в или ниже этого значения, то результат градиента равен 0.

`Max`

Тип: **[float](../../winprog/windows-data-types.md)**

Максимальное значение. Если x находится в или выше этого значения, градиентный результат равен 0.

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Ограничения тензорные
*Инпутградиенттенсор*, *инпуттенсор* и *Аутпутградиенттенсор* должны иметь одинаковые типы *данных*, *DimensionCount* и *размеры*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | от 1 до 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| инпутградиенттенсор | Входные данные | от 1 до 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| аутпутградиенттенсор | Выходные данные | от 1 до 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |