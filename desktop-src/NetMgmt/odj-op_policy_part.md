---
title: OP_POLICY_PART
description: Определение OP_POLICY_PART IDL
ms.assetid: 3988b298-b21d-4476-bfa5-ac606bcbd6c8
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 8ad479c2e24d8c38e87a2100658be2afcf37d70d321e99433e3b05a3af35fa60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911484"
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
