---
title: OP_POLICY_ELEMENT
description: Определение OP_POLICY_ELEMENT IDL
ms.assetid: 69f6e0e7-3f47-4fee-8a4c-df94093dcffa
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: df6fc6852a5efd0a6a2e01a805878ed51bc7c263
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "104339832"
---
# <a name="op_policy_element-structure"></a>Структура OP_POLICY_ELEMENT

Определяет раздел реестра и имя значения, тип и значение, которые должны быть настроены в этом разделе.

## <a name="syntax"></a>Синтаксис

```C++
typedef struct _OP_POLICY_ELEMENT
{
    [string] wchar_t                *pKeyPath;
    [string] wchar_t                *pValueName;
    ULONG                           ulValueType;
    ULONG                           cbValueData;
    [size_is(cbValueData)]  PBYTE   pValueData;
} OP_POLICY_ELEMENT, *POP_POLICY_ELEMENT;
```

## <a name="members"></a>Члены

### <a name="pkeypath"></a>пкэйпас

Содержит путь к разделу реестра.

### <a name="pvaluename"></a>пвалуенаме

Содержит имя значения реестра.

### <a name="ulvaluetype"></a>улвалуетипе

Содержит одно из значений из [типов значений реестра](../sysinfo/registry-value-types.md).

### <a name="cbvaluedata"></a>кбвалуедата

Содержит размер Пвалуедата в байтах.

### <a name="ulvaluetype"></a>улвалуетипе

Содержит значение реестра.

## <a name="see-also"></a>См. также раздел

[**Определения IDL для автономного присоединение к домену**](odj-idl.md)