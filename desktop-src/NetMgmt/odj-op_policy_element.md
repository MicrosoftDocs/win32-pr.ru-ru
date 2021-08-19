---
title: OP_POLICY_ELEMENT
description: Определение OP_POLICY_ELEMENT IDL
ms.assetid: 69f6e0e7-3f47-4fee-8a4c-df94093dcffa
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 74e81f09f4d45d42f5e9df585b88051ac1e96e8cd33e4c15807701e61825b43b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983388"
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

## <a name="see-also"></a>См. также

[**Определения IDL для автономного присоединение к домену**](odj-idl.md)