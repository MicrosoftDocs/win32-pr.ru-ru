---
description: Если вы не лампочки с шейдером вершин или шейдером пикселей, вы можете использовать механизм освещения в среде выполнения.
ms.assetid: vs|directx_sdk|~\lighting_state.htm
title: Состояние освещения (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5935590c46776c621535968f4d457f3738d83d02342ffddf832cbf0278bbd9ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674274"
---
# <a name="lighting-state-direct3d-9"></a>Состояние освещения (Direct3D 9)

Если вы не лампочки с шейдером вершин или шейдером пикселей, вы можете использовать механизм освещения в среде выполнения. Подсистема освещения требует, чтобы данные вершин содержали нормали для вершины, вершины без обычных данных будут формировать точку с нулевым значением во всех вычислениях освещения. Вычисления освещения рассматриваются более подробно в [математике освещения (Direct3D 9)](mathematics-of-lighting.md).

Чтобы включить механизм освещения, используйте:


```
SetRenderState(D3DRS_LIGHTING, TRUE); 
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Состояния отрисовки](render-states.md)
</dt> </dl>

 

 



