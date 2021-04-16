---
description: Direct3D позволяет выбрать один режим заливки одновременно.
ms.assetid: 9531947d-4cd8-43c3-8825-4c48a0d69395
title: Настройка режима заливки (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f93d79e4507d9e9d08569e5cbd75bb8b42aa4f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495315"
---
# <a name="setting-the-shading-mode-direct3d-9"></a>Настройка режима заливки (Direct3D 9)

Direct3D позволяет выбрать один режим заливки одновременно. По умолчанию выбрана заливка Гуро. В C++ режим заливки можно изменить, вызвав метод [**IDirect3DDevice9:: сетрендерстате**](/windows/desktop/api) . Задайте для параметра *State* значение D3DRS \_ шадемоде. Параметр *State* должен быть задан членом перечисления [**D3DSHADEMODE**](./d3dshademode.md) . В следующих примерах кода показано, как текущий режим заливки приложения Direct3D может быть установлен в плоский режим или в режиме заливки Гуро.


```
// Set to flat shading.
// This code example assumes that pDev is a valid pointer to 
// an IDirect3DDevice9 interface.
hr = pDev->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}

// Set to Gouraud shading. This is the default for Direct3D.
hr = pDev->SetRenderState(D3DRS_SHADEMODE,
                            D3DSHADE_GOURAUD);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Заливка](shading.md)
</dt> </dl>

 

 
