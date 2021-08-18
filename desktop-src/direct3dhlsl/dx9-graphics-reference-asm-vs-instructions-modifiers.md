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
ms.openlocfilehash: b2bdad90d13fe960c0d7a5cabfbb508d8abba890e8114c6d4ae1e47d1977e7d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119698"
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



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




