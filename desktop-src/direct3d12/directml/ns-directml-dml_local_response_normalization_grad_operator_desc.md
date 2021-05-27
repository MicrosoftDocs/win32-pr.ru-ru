---
UID: NS:directml.DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
description: Вычисление градиентов обратного распространения для [нормализации локальных ответов](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).
helpviewer_keywords:
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_local_response_normalization_grad_operator_desc
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: e858b8ce20df4b1bf12ac9efe360941eb93c54d1
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550409"
---
# <a name="dml_local_response_normalization_grad_operator_desc-directmlh"></a>DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (директмл. h)

Вычисление градиентов обратного распространения для [нормализации локальных ответов](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).

Тип данных и размер всех десятков должны быть одинаковыми.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,5 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    BOOL CrossChannel;
    UINT LocalSize;
    FLOAT Alpha;
    FLOAT Beta;
    FLOAT Bias;
};
```

## <a name="members"></a>Участники

`InputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Тензорные, содержащий входные данные. *Размеры* тензорные должны быть `{ BatchCount, ChannelCount, Height, Width }` .

`InputGradientTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Входящий градиент тензорные. Обычно это получается из выходных данных обратного распространения предыдущего слоя.

`OutputGradientTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Выходной тензорные, содержащий нераспространяемые градиенты.

`CrossChannel`

Тип: **[bool](../../winprog/windows-data-types.md) .**

**Значение true** , если уровень ЛРН по каналам; **Значение false** , если ЛРН уровень в пространственных измерениях.

`LocalSize`

Тип: **[uint](../../winprog/windows-data-types.md)**

Максимальное число элементов для суммирования по измерению (локальная область обрезается таким образом, что все элементы находятся в границах). Если *кроссчаннел* имеет **значение true**, то это ширина и высота локальной области. Если *кроссчаннел* имеет **значение false**, то это число элементов в локальном регионе. Минимальное значение — 1.

`Alpha`

Тип: **[float](../../winprog/windows-data-types.md)**

Значение параметра масштабирования. В качестве значения по умолчанию рекомендуется использовать значение 0,0001.

`Beta`

Тип: **[float](../../winprog/windows-data-types.md)**

Значение экспоненты. В качестве значения по умолчанию рекомендуется использовать значение 0,75.

`Bias`

Тип: **[float](../../winprog/windows-data-types.md)**

Значение смещения. В качестве значения по умолчанию рекомендуется использовать значение 1.

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Ограничения тензорные
*Инпутградиенттенсор*, *инпуттенсор* и *Аутпутградиенттенсор* должны иметь одинаковые типы *данных* и *размеры*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | 4 | FLOAT32, FLOAT16 |
| инпутградиенттенсор | Входные данные | 4 | FLOAT32, FLOAT16 |
| аутпутградиенттенсор | Выходные данные | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |