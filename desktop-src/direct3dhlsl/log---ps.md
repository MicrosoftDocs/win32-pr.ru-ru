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
ms.openlocfilehash: 4be7061b6e2e0bfa4fd86ffaeef1651cd114996bb9252192582f4c447aac09ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854154"
---
# <a name="log---ps"></a>log-PS

Полная точность журнала ₂ (x).

## <a name="syntax"></a>Синтаксис



| Журнал DST, src |
|--------------|



 

where

-   DST — это регистр назначения.
-   src является исходным регистром. Регистр исходного кода требует явного использования репликации свиззле; то есть необходимо указать только один из компонентов. x,. y,. z,. w свиззле (или. r,. g,. b,. a эквивалент).

## <a name="remarks"></a>Remarks



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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




