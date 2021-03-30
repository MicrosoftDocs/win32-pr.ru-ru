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
ms.openlocfilehash: 0516e62ce07c60866715591bc59123f38dc5c272
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998279"
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

## <a name="remarks"></a>Примечания



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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




