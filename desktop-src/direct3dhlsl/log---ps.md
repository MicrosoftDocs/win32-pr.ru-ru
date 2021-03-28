---
title: log-PS
description: Полная точность журнала ₂ (x). | log-PS
ms.assetid: e540a082-5916-4111-b908-bb229c9e7dc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8face264d5221cf4b39f99260bec476ee5742f0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986690"
---
# <a name="log---ps"></a>log-PS

Полная точность журнала ₂ (x).

## <a name="syntax"></a>Синтаксис



| Журнал DST, src |
|--------------|



 

где

-   DST — это регистр назначения.
-   src является исходным регистром. Регистр исходного кода требует явного использования репликации свиззле; то есть необходимо указать только один из компонентов. x,. y,. z,. w свиззле (или. r,. g,. b,. a эквивалент).

## <a name="remarks"></a>Примечания



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| log                   |      |      |      |      | x    | x    | x     | x    | x     |



 

В следующем фрагменте кода показаны выполняемые операции.


```
float v = abs(src);
if (v != 0)
{
    dest.x = dest.y = dest.z = dest.w = 
        (float)(log(v)/log(2));  
}
else
{
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;
}
```



Эта инструкция принимает скалярный источник, бит подписи которого не учитывается. Результат реплицируется на все четыре канала.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




