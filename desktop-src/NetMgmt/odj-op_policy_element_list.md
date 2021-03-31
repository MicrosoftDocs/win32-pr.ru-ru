---
title: OP_POLICY_ELEMENT_LIST
description: Определение OP_POLICY_ELEMENT_LIST IDL
ms.assetid: 1eebbdd2-655b-4bd3-938c-6bc687ffe7bb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 3c46e7208e6c142b9f58a7704be9bd3461c845b2
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "103797173"
---
# <a name="op_policy_element_list-structure"></a>Структура OP_POLICY_ELEMENT_LIST

Определяет корневой раздел реестра и массив элементов разделов реестра, которые должны быть настроены в этом разделе.

## <a name="syntax"></a>Синтаксис

```C++
typedef struct _OP_POLICY_ELEMENT_LIST
{
    [string] wchar_t                            *pSource;
    ULONG                                       ulRootKeyId;
    ULONG                                       cElements;
    [size_is(cElements)]    POP_POLICY_ELEMENT  pElements;
} OP_POLICY_ELEMENT_LIST, *POP_POLICY_ELEMENT_LIST;
```

## <a name="members"></a>Члены

### <a name="psource"></a>псаурце

Содержит путь к файлу групповая политика, из которого были получены исходные элементы.

### <a name="ulrootkeyid"></a>улруткэйид

Содержит идентификатор корневого раздела реестра. в настоящее время необходимо задать значение HKEY_LOCAL_MACHINE.

### <a name="celements"></a>целементс

Содержит количество элементов в Пелементс.

### <a name="pelements"></a>пелементс

Содержит массив элементов OP_POLICY_ELEMENT.

## <a name="see-also"></a>См. также раздел

[**Определения IDL для автономного присоединение к домену**](odj-idl.md)

[**\_элемент политики \_ Op**](odj-op_policy_element.md)
