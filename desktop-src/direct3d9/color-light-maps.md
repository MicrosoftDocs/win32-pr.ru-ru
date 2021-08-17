---
description: Приложение обычно визуализирует трехмерные сцены более реалистично, если в нем используются цветные карты. Карта цветного света использует данные RGB на карте света для получения информации об освещении.
ms.assetid: 47760884-7b9f-45de-9d4a-faf822da899f
title: Карты цветового освещения (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbff9fe246131fc90bda8ac9b5f1c49cd2413c412a7b3da5c013b1e936aa6f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989304"
---
# <a name="color-light-maps-direct3d-9"></a>Карты цветового освещения (Direct3D 9)

Приложение обычно визуализирует трехмерные сцены более реалистично, если в нем используются цветные карты. Карта цветного света использует данные RGB на карте света для получения информации об освещении.

В следующем примере кода C++ показано освещение с помощью цветовых данных RGB.


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains RGB light map data.

// Set the light map texture as the first texture.
d3dDevice->SetTexture(0, lptexLightMap);

d3dDevice->SetTextureStageState( 0,D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );
```



В этом примере в качестве первой текстуры устанавливается Текстурная схема. Затем он устанавливает состояние первого этапа смешивания для модуляции входящих данных текстуры. В нем используется первая текстура и текущий цвет примитива в качестве аргументов для операции модуляции.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Светлое сопоставление с текстурами](light-mapping-with-textures.md)
</dt> </dl>

 

 



