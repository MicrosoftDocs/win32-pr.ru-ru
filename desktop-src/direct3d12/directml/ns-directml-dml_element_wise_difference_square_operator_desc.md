---
UID: NS:directml.DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
title: DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
description: Вычитает каждый элемент из *бтенсор* из соответствующего элемента *атенсор*, умножает результат на себя и помещает результат в соответствующий элемент *аутпуттенсор*.
helpviewer_keywords:
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC structure
- direct3d12.dml_element_wise_atan_yx_operator_desc
- directml/DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
ms.openlocfilehash: 3e3e7ab8f222f42def82a168ed861e58347f3b20
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804483"
---
# <a name="dml_element_wise_difference_square_operator_desc-directmlh"></a>DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC (директмл. h)

Вычитает каждый элемент из *бтенсор* из соответствующего элемента *атенсор*, умножает результат на себя и помещает результат в соответствующий элемент *аутпуттенсор*.

```
f(a, b) = (a - b) * (a - b)
```

Этот оператор поддерживает выполнение на месте, что означает, что *аутпуттенсор* может иметь псевдоним *атенсор* или *бтенсор* во время привязки.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,5 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
{
    const DML_TENSOR_DESC* ATensor;
    const DML_TENSOR_DESC* BTensor;
    const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a>Члены

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
Этот оператор появился в `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Ограничения тензорные
*Атенсор*, *бтенсор* и *Аутпуттенсор* должны иметь одинаковые типы *данных*, *DimensionCount* и *размеры*.

## <a name="tensor-support"></a>Поддержка тензорные
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| атенсор | Входные данные | от 1 до 8 | FLOAT32, FLOAT16, INT32, UINT32 |
| бтенсор | Входные данные | от 1 до 8 | FLOAT32, FLOAT16, INT32, UINT32 |
| аутпуттенсор | Выходные данные | от 1 до 8 | FLOAT32, FLOAT16, INT32, UINT32 |

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |
