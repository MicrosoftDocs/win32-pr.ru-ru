---
title: каллнз bool-PS
description: Вызовите, если не равен нулю. Выполняет условный вызов инструкции, помеченной индексом метки. | каллнз bool-PS
ms.assetid: 1b9ff276-c2b8-46cc-96ac-a5b5455c5cc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 793feb1934b86b46f26050a67b5f26d94b9f277e31735c4d1912805374bab903
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516634"
---
# <a name="callnz-bool---ps"></a>каллнз bool-PS

Вызовите, если не равен нулю. Выполняет условный вызов инструкции, помеченной индексом метки.

## <a name="syntax"></a>Синтаксис



| каллнз l \# , \[ ! \] &\# |
|----------------------|



 

Где:

-   l \# — [Метка-PS](label---ps.md) , помечающая начало подпрограммы для вызова.
-   \[!\] является необязательным модификатором отрицания.
-   b \# определяет [константу логического регистра](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).

## <a name="remarks"></a>Remarks



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| bool каллнз           |      |      |      |      |      | x    | x     | x    | x     |



 

Эта инструкция выполняет следующие действия:


```
if (specified Boolean register is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




