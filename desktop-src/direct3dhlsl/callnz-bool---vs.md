---
title: каллнз bool — VS
description: Вызовите, если не равен нулю. Выполняет условный вызов инструкции, помеченной индексом метки. | каллнз bool — VS
ms.assetid: 9be030b9-fa21-459f-bd6c-f34ad6f177fc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a6d5a7646670d182b0b685ab742fb5b2094a89a717a31019165054bcbc4816b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287262"
---
# <a name="callnz-bool---vs"></a>каллнз bool — VS

Вызовите, если не равен нулю. Выполняет условный вызов инструкции, помеченной индексом метки.

## <a name="syntax"></a>Синтаксис



| каллнз l \# , \[ ! \] &\# |
|----------------------|



 

где:

-   где l \# — [Метка — VS](label---vs.md) отмечает начало подпрограммы, которую необходимо вызвать.
-   \[!\] Необязательный логический модификатор NOT.
-   b \# определяет [константу логического регистра](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).

## <a name="remarks"></a>Remarks



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| bool каллнз            |      | x    | x    | x     | x    | x     |



 

Эта инструкция выполняет следующие действия:


```
if (specified boolean register is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



Эта инструкция использует один слот инструкций шейдера вершин.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




