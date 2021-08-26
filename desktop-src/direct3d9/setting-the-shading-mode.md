---
description: Direct3D позволяет выбрать один режим заливки одновременно.
ms.assetid: 9531947d-4cd8-43c3-8825-4c48a0d69395
title: Настройка режима заливки (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769908513d4388fafae73f5a6788aef37c3ac9456a00f2e3280c57e04c18b462
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068964"
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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Заливка](shading.md)
</dt> </dl>

 

 
