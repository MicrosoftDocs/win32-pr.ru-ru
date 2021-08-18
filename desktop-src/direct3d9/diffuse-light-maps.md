---
description: При освещении с помощью источника света для матовых поверхностей отображается рассеянный световой отражение.
ms.assetid: a6ed351a-7889-4993-96bf-b03352a815da
title: рассеянный свет Карты (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758fc2b5054a30bf8df703941b3cedf0810c378a5fb459d8c5783bb295ff9abe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044452"
---
# <a name="diffuse-light-maps-direct3d-9"></a>рассеянный свет Карты (Direct3D 9)

При освещении с помощью источника света для матовых поверхностей отображается рассеянный световой отражение. Яркость рассеянного света зависит от расстояния до источника света и угла между нормалью поверхности и вектором направленности источника света. Эффекты рассеянного света, моделируемые с помощью расчетов освещения, обеспечивают создание лишь общих эффектов.

Ваше приложение может моделировать более сложный рассеянный свет с использованием карт освещения для текстур. Для этого добавьте карту рассеянного освещения в базовую текстуру, как показано в следующем примере кода C++.


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface.
// lptexBaseTexture is a valid pointer to a texture.
// lptexDiffuseLightMap is a valid pointer to a texture that contains 
// RGB diffuse light map data.

// Set the base texture.
d3dDevice->SetTexture(0,lptexBaseTexture );

// Set the base texture operation and args.
d3dDevice->SetTextureStageState(0,D3DTSS_COLOROP,
                                D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );

// Set the diffuse light map.
d3dDevice->SetTexture(1,lptexDiffuseLightMap );

// Set the blend stage.
d3dDevice->SetTextureStageState(1, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG2, D3DTA_CURRENT );
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Светлое сопоставление с текстурами](light-mapping-with-textures.md)
</dt> </dl>

 

 



