---
description: Чтобы повысить производительность отрисовки, можно исключать (или удалять) примитив, который отрывается от камеры.
ms.assetid: b4b8ff3f-aa20-4422-8f6f-34cae25de0e6
title: Состояние отбора (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bf9d8ed8ecea46dcfee146784dc97a38e42f0261b8f78bfc9d45ffaf99ddd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608034"
---
# <a name="culling-state-direct3d-9"></a>Состояние отбора (Direct3D 9)

Чтобы повысить производительность отрисовки, можно исключать (или удалять) примитив, который отрывается от камеры. Для односторонних примитивов это экономит время отрисовки, так как задняя сторона не видна. Чтобы включить отбор, необходимо знать порядок поворота вершин (обычно в противном случае — по часовой стрелке). В этом примере удаляется все примитивы, для которых обратная поверхность направлена вперед (по часовой стрелке):


```
SetRenderState(D3DRS_CULLMODE, D3DCULL_CCW);
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Состояния отрисовки](render-states.md)
</dt> </dl>

 

 



