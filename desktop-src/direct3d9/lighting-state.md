---
description: Если вы не лампочки с шейдером вершин или шейдером пикселей, вы можете использовать механизм освещения в среде выполнения.
ms.assetid: vs|directx_sdk|~\lighting_state.htm
title: Состояние освещения (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74f0e7b7ec4a8bcf0ee27c9bc1e643536819d8fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105701099"
---
# <a name="lighting-state-direct3d-9"></a>Состояние освещения (Direct3D 9)

Если вы не лампочки с шейдером вершин или шейдером пикселей, вы можете использовать механизм освещения в среде выполнения. Подсистема освещения требует, чтобы данные вершин содержали нормали для вершины, вершины без обычных данных будут формировать точку с нулевым значением во всех вычислениях освещения. Вычисления освещения рассматриваются более подробно в [математике освещения (Direct3D 9)](mathematics-of-lighting.md).

Чтобы включить механизм освещения, используйте:


```
SetRenderState(D3DRS_LIGHTING, TRUE); 
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Состояния отрисовки](render-states.md)
</dt> </dl>

 

 



