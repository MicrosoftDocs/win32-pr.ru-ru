---
description: Анимированная анимация вершин объединяет две предоставляемые пользователем положения (или нормали).
ms.assetid: vs|directx_sdk|~\vertex_tweening.htm
title: Анимированная анимация вершин (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8486f53e4eb1a3a003b15255baeb50d30f0ed205f4259625d7d66ba33e8274c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519225"
---
# <a name="vertex-tweening-direct3d-9"></a>Анимированная анимация вершин (Direct3D 9)

Анимированная анимация вершин объединяет две предоставляемые пользователем положения (или нормали). Tween-анимация является взаимоисключающей из смешения вершин с весовыми коэффициентами. Tween-анимация выполняется до освещения и обрезки и включается путем установки D3DRS \_ вертексбленд в D3DVBF \_ tween-анимации. Результирующая вершина вершины вычислена следующим образом:


```
POSITION = POSITION1 * (1.0 - TWEENFACTOR) + POSITION2 * TWEENFACTOR
```



Для вычисления нормалей используется тот же подход. Дополнительные сведения см. [в разделе Использование анимации по вершинам (Direct3D 9)](using-vertex-tweening.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Смешение геометрических объектов](geometry-blending.md)
</dt> </dl>

 

 



