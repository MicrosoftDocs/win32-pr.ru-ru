---
title: Создание текстуры
description: В этом разделе показано, как создать текстуру.
ms.assetid: dfe88635-b2c2-48f8-a21e-cce845b518fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d3c4715bb4c790ea772dcbba4834051946747e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777594"
---
# <a name="how-to-create-a-texture"></a><span data-ttu-id="51270-103">Как создать текстуру</span><span class="sxs-lookup"><span data-stu-id="51270-103">How to: Create a Texture</span></span>

<span data-ttu-id="51270-104">Самый простой способ создать текстуру — описать ее свойства и вызвать API создания текстуры.</span><span class="sxs-lookup"><span data-stu-id="51270-104">The simplest way to create a texture is to describe its properties and call the texture creation API.</span></span> <span data-ttu-id="51270-105">В этом разделе показано, как создать текстуру.</span><span class="sxs-lookup"><span data-stu-id="51270-105">This topic shows how to create a texture.</span></span>

<span data-ttu-id="51270-106">**Создание текстуры**</span><span class="sxs-lookup"><span data-stu-id="51270-106">**To create a texture**</span></span>

1.  <span data-ttu-id="51270-107">Заполните структуру [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) , указав описание параметров текстуры.</span><span class="sxs-lookup"><span data-stu-id="51270-107">Fill in a [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) structure with a description of the texture parameters.</span></span>
2.  <span data-ttu-id="51270-108">Создайте текстуру, вызвав [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) с описанием текстуры.</span><span class="sxs-lookup"><span data-stu-id="51270-108">Create the texture by calling [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) with the texture description.</span></span>

<span data-ttu-id="51270-109">В этом примере создается текстура 256 x 256 с [**динамическим использованием**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)для использования в качестве [**ресурса шейдера**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) с [**доступом на запись ЦП**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).</span><span class="sxs-lookup"><span data-stu-id="51270-109">This example creates a 256 x 256 texture, with [**dynamic usage**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), for use as a [**shader resource**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) with [**cpu write access**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).</span></span>


```
D3D11_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D11_USAGE_DYNAMIC;
desc.BindFlags = D3D11_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
desc.MiscFlags = 0;

ID3D11Device *pd3dDevice; // Don't forget to initialize this
ID3D11Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



## <a name="related-topics"></a><span data-ttu-id="51270-110">См. также</span><span class="sxs-lookup"><span data-stu-id="51270-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51270-111">Использование Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="51270-111">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="51270-112">Текстуры</span><span class="sxs-lookup"><span data-stu-id="51270-112">Textures</span></span>](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




