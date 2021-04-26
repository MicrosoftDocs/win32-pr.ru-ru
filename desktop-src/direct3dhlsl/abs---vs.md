---
title: ABS-VS
description: Вычисление абсолютного значения. | ABS-VS
ms.assetid: d3b4cf06-dc87-4c71-aa2d-5ade4cf98caa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4d73ee738f575d93c2316e4ec47dced7cb128d3
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994751"
---
# <a name="abs---vs"></a>ABS-VS

Вычисление абсолютного значения.

## <a name="syntax"></a>Синтаксис



|              |
|--------------|
| ABS DST, src |



 

where

-   DST — это регистр назначения.
-   src является исходным регистром.

## <a name="remarks"></a>Примечания



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| abs                    |      | x    | x    | x     | x    | x     |



 

Эта инструкция работает, как показано здесь.


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




