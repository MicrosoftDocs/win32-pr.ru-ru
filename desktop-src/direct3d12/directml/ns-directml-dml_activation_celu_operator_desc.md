---
UID: NS:directml.DML_ACTIVATION_CELU_OPERATOR_DESC
title: DML_ACTIVATION_CELU_OPERATOR_DESC
description: Выполняет постоянную функцию активации дифферентиабле экспоненциального линейного блока (ЦЕЛУ) для каждого элемента в *инпуттенсор*, помещая результат в соответствующий элемент *аутпуттенсор*.
helpviewer_keywords:
- DML_ACTIVATION_CELU_OPERATOR_DESC
- DML_ACTIVATION_CELU_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ACTIVATION_CELU_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ACTIVATION_CELU_OPERATOR_DESC, DML_ACTIVATION_CELU_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ACTIVATION_CELU_OPERATOR_DESC
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
- DML_ACTIVATION_CELU_OPERATOR_DESC
- directml/DML_ACTIVATION_CELU_OPERATOR_DESC
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
- DML_ACTIVATION_CELU_OPERATOR_DESC
ms.openlocfilehash: b6497e995601d7e9e01696f39920672674be07c4
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418092"
---
# <a name="dml_activation_celu_operator_desc-structure-directmlh"></a>Структура DML_ACTIVATION_CELU_OPERATOR_DESC (директмл. h)

Выполняет постоянную функцию активации дифферентиабле экспоненциального линейного блока (ЦЕЛУ) для каждого элемента в *инпуттенсор*, помещая результат в соответствующий элемент *аутпуттенсор*.

```
f(x) = max(0, x) + min(0, Alpha * (exp(x / Alpha) - 1));
```

Где:
* EXP (x) является естественной функцией возведения в степень
* Функция Max (a, b) возвращает большее из двух значений a, b
* min (a, b) Возвращает меньшее из двух значений a, b

Этот оператор поддерживает выполнение на месте. Это означает, что тензорные вывода может иметь псевдоним *инпуттенсор* во время привязки.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_ACTIVATION_CELU_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  FLOAT Alpha;
};
```

## <a name="members"></a>Участники

`InputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Входной тензорные для чтения из.

`OutputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Выходной тензорные для записи результатов в.

`Alpha`

Тип: <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b>

Коэффициент альфа. Стандартное значение по умолчанию для этого параметра — 1,0.

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Ограничения тензорные
*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковый *тип данных*, *DimensionCount* и *размеры*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | от 1 до 8 | FLOAT32, FLOAT16 |
| аутпуттенсор | Выходные данные | от 1 до 8 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |