---
description: Позволяет задать параметры анимации.
ms.assetid: 727b4d87-4164-4915-b158-d21fe7d1b729
title: AnimationOptions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 346eaa1b94637fa357f09cd701ac9d99d5ddf2076ee12654076e54bce82527fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069434"
---
# <a name="animationoptions"></a>AnimationOptions

Позволяет задать параметры анимации.

``` syntax
template AnimationOptions
{
    < E2BF56C0-840F-11cf-8F52-0040333594A3 >
    DWORD openclosed;
    DWORD positionquality;
} 
```

Где:

-   опенклосед — используйте 0 для закрытой анимации или 1 для открытой анимации. По умолчанию анимация закрыта.
-   поситионкуалити — задайте качество расположения для всех указанных ключей позиционирования. Используйте 0 для позиционирования сплайна или 1 для линейных позиций.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Шаблоны](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



