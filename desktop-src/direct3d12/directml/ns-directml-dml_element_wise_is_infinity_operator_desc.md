---
UID: NS:directml.DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
title: DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
description: Проверяет каждый элемент *инпуттенсор* для IEEE-754-INF, INF или обоих параметров в зависимости от заданной *инфинитимоде* и помещает результат (1 для true, 0 для false) в соответствующий элемент *аутпуттенсор*.
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
targetos: Windows
req.construct-type: structure
req.ddi-compliance: ''
req.dll: ''
req.header: directml.h
req.include-header: ''
req.kmdf-ver: ''
req.lib: ''
req.max-support: ''
req.redist: ''
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: Windows
req.typenames: ''
req.umdf-ver: ''
req.unicode-ansi: ''
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- directml.h
api_name:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
f1_keywords:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
dev_langs:
- c++
ms.openlocfilehash: 41be7751b542436b481da784c60ae79ad554cd12
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418008"
---
# <a name="dml_element_wise_is_infinity_operator_desc-structure-directmlh"></a>Структура DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC (директмл. h)

Проверяет каждый элемент *инпуттенсор* для IEEE-754-INF, INF или обоих параметров в зависимости от заданной *инфинитимоде* и помещает результат (1 для true, 0 для false) в соответствующий элемент *аутпуттенсор*.

```
f(x) = isinf(x) && (
       (x > 0 && InfinityMode == DML_IS_INFINITY_MODE_POSITIVE) ||
       (x < 0 && InfinityMode == DML_IS_INFINITY_MODE_NEGATIVE) ||
                 InfinityMode == DML_IS_INFINITY_MODE_EITHER)
```

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_IS_INFINITY_MODE  InfinityMode;
};
```

## <a name="members"></a>Участники

`InputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Входной тензорные для чтения из.


`OutputTensor`

Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Выходной тензорные для записи результатов в.


`InfinityMode`

Тип: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**

[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) , определяющий знак бесконечности для проверки.

* Если **DML_IS_INFINITY_MODE_EITHER**, возвращается значение 1, если элемент имеет значение-INF или INF; в противном случае — значение 0.
* Если **DML_IS_INFINITY_MODE_POSITIVE**, то возвращается значение 1, если элемент является INF, в противном случае — 0.
* Если **DML_IS_INFINITY_MODE_NEGATIVE**", то возвращается значение 1, если элемент имеет значение-INF; в противном случае — 0.


## <a name="remarks"></a>Remarks
## <a name="availability"></a>Доступность
Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Ограничения тензорные
*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковые *DimensionCount* и *размеры*.

## <a name="tensor-support"></a>Поддержка тензорные
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 и выше
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | от 1 до 8 | FLOAT32, FLOAT16 |
| аутпуттенсор | Выходные данные | от 1 до 8 | UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 и выше
| Тензорные | Вид | Поддерживаемые счетчики измерений | Поддерживаемые типы данных |
| ------ | ---- | -------------------------- | -------------------- |
| инпуттенсор | Входные данные | 4 | FLOAT32, FLOAT16 |
| аутпуттенсор | Выходные данные | 4 | UINT8 |


## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, версия 2004 (10,0; Сборка 19041) |
| **Минимальная версия сервера** | Windows Server, версия 2004 (10,0; Сборка 19041) |
| **Header** | директмл. h |