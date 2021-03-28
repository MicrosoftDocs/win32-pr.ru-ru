---
title: Модификаторы инструкций (Справочник по HLSL VS)
description: Модификаторы инструкций
ms.assetid: b713d847-c858-4492-918c-7a105f751624
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 573f2ef618c4cd29092fb38fb4c805bdeeecc219
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "104487200"
---
# <a name="instruction-modifiers-hlsl-vs-reference"></a>Модификаторы инструкций (Справочник по HLSL VS)

Модификаторы инструкций влияют на результат инструкции перед его записью в регистр назначения.

## <a name="_sat"></a>\_Кот

Насыщенность (или фиксации) результата инструкции в \[ 0, 1 \] диапазон перед записью в регистр назначения.

Например:


```
add_sat dst, src0, src1
```



Где:

DST = срез \_ между \_ 0 \_ и \_ 1 (src0 + src1)

\_Модификатор инструкции "Кот" не требует дополнительных слотов инструкций.

Если поддерживается, \_ Модификатор инструкции «Кот» можно использовать с любыми инструкциями, кроме: [ФРК-VS](frc---vs.md), [синкос-VS](sincos---vs.md)и [текслдл-VS](texldl---vs.md).



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| \_Кот                  |      |      |      |       | x    | x     |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




