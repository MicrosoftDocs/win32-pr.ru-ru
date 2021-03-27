---
title: логп — VS
description: Частичная точность логп ₂ (x).
ms.assetid: 8547ca8a-7bde-4e41-9e65-f7fcd65454c1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a261d63ad47dcf12728b8bcd0025ec578ede0b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069353"
---
# <a name="logp---vs"></a>логп — VS

Частичная точность логп ₂ (x).

## <a name="syntax"></a>Синтаксис



| логп DST, src |
|---------------|



 

где

-   DST — это регистр назначения.
-   src является исходным регистром. Для исходного регистра требуется явное использование репликации свиззле, то есть только один из компонентов. x,. y,. z,. w свиззле (или. r,. g,. b,. a эквивалент) должен быть указан.

## <a name="remarks"></a>Примечания



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| логп                   | x    | x    | x    | x     | x    | x     |



 

В следующем фрагменте кода показаны выполняемые операции.


```
float f = abs(src);
if (f != 0)
    dest.x = dest.y = dest.z = dest.w = (float)(log(f)/log(2));
else
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;   
```



Эта инструкция предоставляет логарифм с основанием 2 с частичным точностью до 10 бит.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




