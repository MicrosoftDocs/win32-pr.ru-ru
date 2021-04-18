---
description: Direct3D поддерживает как плоские, так и заливку по методу Гуро. Значение по умолчанию — заливка по методу Гуро. Для управления текущим режимом заливки приложение C++ указывает Член перечисляемого типа D3DSHADEMODE для \_ состояния визуализации D3DRS шадемоде.
ms.assetid: 0019b1b7-65f2-4009-8d0f-5a99cf32a410
title: Состояние заливки (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebac826704fee0e1903c1aa2a2348bff4a089c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710625"
---
# <a name="shading-state-direct3d-9"></a>Состояние заливки (Direct3D 9)

Direct3D поддерживает как плоские, так и заливку по методу Гуро. Значение по умолчанию — заливка по методу Гуро. Для управления текущим режимом заливки приложение C++ указывает Член перечисляемого типа [**D3DSHADEMODE**](./d3dshademode.md) для \_ состояния визуализации D3DRS шадемоде.

В следующем примере кода C++ демонстрируется процесс установки состояния затенения в режим плоской заливки.


```
// This code example assumes that d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface.
// Set the shading state.
d3dDevice->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Состояния отрисовки](render-states.md)
</dt> </dl>

 

 
