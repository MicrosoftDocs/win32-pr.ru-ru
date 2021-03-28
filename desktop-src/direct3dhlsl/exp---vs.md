---
title: EXP — VS
description: Обеспечивает полную экспоненциальную точность 2. | EXP — VS
ms.assetid: 3644046b-3257-4257-9880-146ca50f6b0b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5b49b69e1270075aef4368dedca5791c2784657
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998222"
---
# <a name="exp---vs"></a>EXP — VS

Обеспечивает полную экспоненциальную точность 2<sup>x</sup>.

## <a name="syntax"></a>Синтаксис



| EXP DST, src |
|--------------|



 

где

-   DST — это регистр назначения.
-   src является исходным регистром. Для исходного регистра требуется явное использование репликации свиззле, то есть только один из компонентов. x,. y,. z,. w свиззле (или. r,. g,. b,. a эквивалент) должен быть указан. См. раздел [Source Register группирующие](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md).

## <a name="remarks"></a>Примечания



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| exp                    | x    | x    | x    | x     | x    | x     |



 

Эта инструкция предоставляет по меньшей мере 21 бит точности.

В следующем фрагменте кода показаны выполняемые операции.


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




