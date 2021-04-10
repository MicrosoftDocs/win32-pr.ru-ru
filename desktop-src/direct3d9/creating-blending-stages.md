---
description: Этап наложения — это набор операций с текстурами и их аргументов, определяющих наложение текстур.
ms.assetid: 7f9e3041-a270-44a9-a8e1-bca5ea25a71e
title: Создание стадий смешения (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f5029d540433b22b1380435dd8092546917338
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141599"
---
# <a name="creating-blending-stages-direct3d-9"></a>Создание стадий смешения (Direct3D 9)

Этап наложения — это набор операций с текстурами и их аргументов, определяющих наложение текстур. При выполнении этапа смешения приложения C++ вызывают метод [**IDirect3DDevice9:: сеттекстурестажестате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) . Первый вызов задает выполняемую операцию. Два дополнительных вызова определяют аргументы, к которым применяется операция. В следующем примере кода показано создание этапа смешения.


```
// This example assumes that lpD3DDev is a valid pointer to an
// IDirect3DDevice9 interface.

// Set the operation for the first texture.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_ADD);

// Set argument 1 to the texture color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE);

// Set argument 2 to the iterated diffuse color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE);
```



Данные шаг текселя в текстурах содержат значения цвета и альфа-канала. Приложения могут определять отдельные операции для цветов и альфа-значений на одном этапе смешения. У каждой операции, цвета и альфа-канала есть собственные аргументы. Дополнительные сведения см. в разделе [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).

Несмотря на то, что не входит в API Direct3D, в приложение можно вставить следующие макросы, чтобы сократить код, необходимый для создания стадий смешения текстур.


```
#define SetTextureColorStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_COLOROP, op);      \
    dev->SetTextureStageState( i, D3DTSS_COLORARG1, arg1 ); \
    dev->SetTextureStageState( i, D3DTSS_COLORARG2, arg2 );

#define SetTextureAlphaStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_ALPHAOP, op);      \
    dev->SetTextureStageState( i, D3DTSS_ALPHAARG1, arg1 );  \
    dev->SetTextureStageState( i  D3DTSS_ALPHAARG2, arg2 );
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Смешение текстур](texture-blending.md)
</dt> </dl>

 

 
