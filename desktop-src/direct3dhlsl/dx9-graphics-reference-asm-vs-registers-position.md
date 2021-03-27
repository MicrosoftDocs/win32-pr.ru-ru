---
title: Регистр позиций
description: Этот выходной регистр шейдера вершин содержит данные о положении на вершину.
ms.assetid: 98f71027-d94b-4dd0-a6b6-4b263954eff9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 89470bb920db7c612b21cefb2c44c2c89d48ce28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776622"
---
# <a name="position-register"></a>Регистр позиций

Этот выходной регистр шейдера вершин содержит данные о положении на вершину.



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Регистр позиций      | x    | x    | x     | x    | x    | x     |



 

Регистр состоит из свойств, определяющих принцип работы каждой ККМ.



| Свойство        | Описание |
|-----------------|-------------|
| Имя            | oPos        |
| Count           | 1 вектор    |
| Разрешения ввода-вывода | Доступный только на запись. |



 

Значение является позицией в однородной вырезанной области. Это значение должно быть записано шейдером вершин.

Например, .


```
    dcl_position v0
    
    def c40, 0.0f,0.0f,0.0f,0.0f;
    // transform into projection space
    m4x4 r0,v0,c8
    max r0.z,c40.z,r0.z //clamp to 0
    max r0.w,c12.x,r0.w //clamp to near clip plane
    mov oPos,r0   
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Регистры шейдеров вершин](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




