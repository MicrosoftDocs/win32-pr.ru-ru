---
title: OP_POLICY_PART
description: Определение OP_POLICY_PART IDL
ms.assetid: 3988b298-b21d-4476-bfa5-ac606bcbd6c8
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: ef0e3b96ce564ed7ff8e2ce0886e33ca474a1cf8
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "104414045"
---
# <a name="op_policy_part-structure"></a>Структура OP_POLICY_PART

Содержит массив структур OP_POLICY_ELEMENT_LIST.

## <a name="syntax"></a>Синтаксис

```C++
typedef struct _OP_POLICY_PART
{
    ULONG                                       cElementLists;
    [size_is(cElementLists)]
                        POP_POLICY_ELEMENT_LIST pElementLists;
    OP_BLOB                                     Extension;
} OP_POLICY_PART, *POP_POLICY_PART;
```

## <a name="members"></a>Члены

### <a name="celementlists"></a>целементлистс

Содержит количество элементов в Пелементлистс.

### <a name="pelementlists"></a>пелементлистс

Содержит массив структур OP_POLICY_ELEMENT_LIST.

### <a name="extension"></a>Расширение

Зарезервировано для будущего использования и должно содержать все нули.

## <a name="see-also"></a>См. также раздел

[**Определения IDL для автономного присоединение к домену**](odj-idl.md)

[**\_ \_ список элементов политики \_ Op**](odj-op_policy_element_list.md)
