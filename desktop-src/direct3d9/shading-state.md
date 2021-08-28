---
description: Direct3D поддерживает как плоские, так и заливку по методу Гуро. Значение по умолчанию — заливка по методу Гуро. Для управления текущим режимом заливки приложение C++ указывает Член перечисляемого типа D3DSHADEMODE для \_ состояния визуализации D3DRS шадемоде.
ms.assetid: 0019b1b7-65f2-4009-8d0f-5a99cf32a410
title: Состояние заливки (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f28514fefbf39e75bd84a0ae56324fd859f0fd85fa4a25449e349ce592ab3b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727604"
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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Состояния отрисовки](render-states.md)
</dt> </dl>

 

 
