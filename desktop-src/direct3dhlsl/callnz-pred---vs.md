---
title: каллнз, пред. VS
description: Вызывайте, если не равен нулю, с предикатом. Выполняет условный вызов инструкции, помеченной индексом метки. Затенения использует логическое значение, чтобы определить, не нужно ли выполнять инструкцию.
ms.assetid: 3417f3e3-7e73-4131-8069-09c0de1469a7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1449ed9fb061ea2d5a83d37cb7c0d744a4c7e8b6517d49c0d2e32a10f7f5ed9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287028"
---
# <a name="callnz-pred---vs"></a>каллнз, пред. VS

Вызывайте, если не равен нулю, с предикатом. Выполняет условный вызов инструкции, помеченной индексом метки. Затенения использует логическое значение, чтобы определить, не нужно ли выполнять инструкцию.

## <a name="syntax"></a>Синтаксис



| каллнз l \# , \[ ! \] P0. x|&|гармошкой|Белая |
|----------------------------------|



 

где:

-   l \# — это [Метка — VS](label---vs.md) , помечающая начало подпрограммы для вызова.
-   \[!\] является необязательным модификатором отрицания.
-   P0 — это [регистр предикатов](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   {x \| y \| z \| w} — это обязательная репликация свиззле в P0.

## <a name="remarks"></a>Remarks



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| каллнз, пред.            |      |      | x    | x     | x    | x     |



 

Эта инструкция выполняет следующие действия:


```
if (specified register component is not zero)
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

 

 




