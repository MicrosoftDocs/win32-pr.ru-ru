---
description: Анимированная анимация вершин объединяет две предоставляемые пользователем положения (или нормали).
ms.assetid: vs|directx_sdk|~\vertex_tweening.htm
title: Анимированная анимация вершин (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a5458e384fa69b91b1eab1623fb526d514591f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262404"
---
# <a name="vertex-tweening-direct3d-9"></a>Анимированная анимация вершин (Direct3D 9)

Анимированная анимация вершин объединяет две предоставляемые пользователем положения (или нормали). Tween-анимация является взаимоисключающей из смешения вершин с весовыми коэффициентами. Tween-анимация выполняется до освещения и обрезки и включается путем установки D3DRS \_ вертексбленд в D3DVBF \_ tween-анимации. Результирующая вершина вершины вычислена следующим образом:


```
POSITION = POSITION1 * (1.0 - TWEENFACTOR) + POSITION2 * TWEENFACTOR
```



Для вычисления нормалей используется тот же подход. Дополнительные сведения см. [в разделе Использование анимации по вершинам (Direct3D 9)](using-vertex-tweening.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Смешение геометрических объектов](geometry-blending.md)
</dt> </dl>

 

 



