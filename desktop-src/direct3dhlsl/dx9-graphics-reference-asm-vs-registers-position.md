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
ms.openlocfilehash: cda82431990ed3ea545adfcc5e6eb2801be0607d8bac45aa1bcd8c0e121f3d68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023904"
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

Пример


```
    dcl_position v0
    
    def c40, 0.0f,0.0f,0.0f,0.0f;
    // transform into projection space
    m4x4 r0,v0,c8
    max r0.z,c40.z,r0.z //clamp to 0
    max r0.w,c12.x,r0.w //clamp to near clip plane
    mov oPos,r0   
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Регистры шейдеров вершин](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




