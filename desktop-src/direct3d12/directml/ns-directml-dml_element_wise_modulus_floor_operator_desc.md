---
UID: NS:directml.DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
title: DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
description: Выполняет вычисление модуля с теми же результатами, что и у модуля Python, для каждой пары соответствующих элементов из входных десятков, помещая результат в соответствующий элемент *аутпуттенсор*.
helpviewer_keywords:
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC structure
- direct3d12.dml_element_wise_modulus_floor_operator_desc
- directml/DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
ms.openlocfilehash: 8c70bd4649a57270807ac408802fe07edd36d98e
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418084"
---
# <a name="dml_element_wise_modulus_floor_operator_desc-structure-directmlh"></a>Структура DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC (директмл. h)

Выполняет вычисление модуля с теми же результатами, что и у модуля Python, для каждой пары соответствующих элементов из входных десятков, помещая результат в соответствующий элемент *аутпуттенсор*.

Так как значение частного округляется в сторону-INF, результат будет иметь тот же знак, что и делитель.

```
f(a, b) = a - (b * floor(a / b))
```

Этот оператор поддерживает выполнение на месте, что означает, что *аутпуттенсор* может использовать псевдонимы для одного из входных десятков во время привязки.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a>Участники

`ATensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий входные данные левого края.


`BTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Объект тензорные, содержащий правые входные данные.


`OutputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Выходной тензорные для записи результатов в.

## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Ограничения тензорные
*Атенсор*, *бтенсор* и *Аутпуттенсор* должны иметь одинаковые типы *данных*, *DimensionCount* и *размеры*.

## <a name="tensor-support"></a>Поддержка тензорные
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 и выше
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| атенсор | Входные данные | от 1 до 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| бтенсор | Входные данные | от 1 до 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| аутпуттенсор | Выходные данные | от 1 до 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 и выше
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| атенсор | Входные данные | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| бтенсор | Входные данные | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| аутпуттенсор | Выходные данные | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |



## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |