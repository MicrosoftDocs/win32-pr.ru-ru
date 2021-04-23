---
description: Значения альфа могут также предоставляться текстурами.
ms.assetid: b9f53783-d4d8-4339-8cf3-5ad8305ff627
title: Текстура Alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 694f8a72d3faede36c3e69ce1b6841b8f6450a3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105662061"
---
# <a name="texture-alpha-direct3d-9"></a><span data-ttu-id="1109a-103">Текстура Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1109a-103">Texture Alpha (Direct3D 9)</span></span>

<span data-ttu-id="1109a-104">Значения альфа могут также предоставляться текстурами.</span><span class="sxs-lookup"><span data-stu-id="1109a-104">Alpha values can also be provided by textures.</span></span> <span data-ttu-id="1109a-105">Сначала необходимо создать текстуру.</span><span class="sxs-lookup"><span data-stu-id="1109a-105">First, the texture must be created.</span></span> <span data-ttu-id="1109a-106">Во-вторых, в текстуру необходимо добавить альфа-значения.</span><span class="sxs-lookup"><span data-stu-id="1109a-106">Second, the alpha values must be added to the texture.</span></span> <span data-ttu-id="1109a-107">Для отображения с текстурой задайте текстуру на стадии текстуры и выберите соответствующую операцию на этапе текстуры и операнды.</span><span class="sxs-lookup"><span data-stu-id="1109a-107">To render with the texture, set the texture to a texture stage and select the appropriate texture stage operation and operands.</span></span> <span data-ttu-id="1109a-108">При вызове Draw примитив будет подготовлен к просмотру с прозрачностью.</span><span class="sxs-lookup"><span data-stu-id="1109a-108">When draw is called, the primitive will be rendered with transparency.</span></span> <span data-ttu-id="1109a-109">В этом примере создается ресурс текстуры, а затем загружается альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="1109a-109">This example creates a texture resource, and then loads the alpha channel.</span></span>


```
LPDIRECT3DTEXTURE9 m_pTexture;

// Create an alpha texture
D3DXCreateTexture(m_d3dDevice, 128, 128, 0, D3DUSAGE_RENDERTARGET, 
    D3DFMT_A8R8G8B8, D3DPOOL_MANAGED, &m_pTexture);

// Initialize the alpha channel
int  yGrad, xGrad;
D3DLOCKED_RECT lockedRect;

if(SUCCEEDED(pTexture->LockRect(0, &lockedRect, NULL, D3DLOCK_DISCARD )))
{
    m_pRGBAData = new DWORD[128*128];
    if( m_pRGBAData != NULL )
    {
        for( DWORD y=0; y < m_dwHeight; y++ )
        {   
            DWORD dwOffset = y*m_dwWidth;
            yGrad = (int)(((float)y/(float)m_dwWidth) * 255.0f);
            
            for( DWORD x=0; x < m_dwWidth; x )
            {
                xGrad = (int)(((float)x/(float)m_dwWidth) * 255.0f);

                DWORD b = (DWORD)(xGrad + (255 - yGrad))/2 & 0xFF;
                DWORD g = (DWORD)((255 - xGrad) + yGrad)/2 & 0xFF;
                DWORD r = (DWORD)(xGrad + yGrad)/2 & 0xFF;
                DWORD a = (DWORD)(xGrad + yGrad)/2 & 0xFF;

                lockedRect.pBits[dwOffset+x] = ((a<<24L)+(r<<16L)+(g<<8L)+(b));
                x++;
            }
        }
    }
    pTexture->UnlockRect(&lockedRect);
}
```



<span data-ttu-id="1109a-110">Значение альфа вычисляется на основе относительного положения x/y текущего пикселя в пределах размера текстуры.</span><span class="sxs-lookup"><span data-stu-id="1109a-110">The alpha value is calculated based on the current pixel's relative x/y position within the texture size.</span></span> <span data-ttu-id="1109a-111">Затем назначьте текстуру на стадии текстуры и настройте стадию текстуры.</span><span class="sxs-lookup"><span data-stu-id="1109a-111">Next, assign the texture to a texture stage and set up the texture stage.</span></span>


```
#define D3DFVF_LVERTEX ( D3DFVF_XYZ | D3DFVF_DIFFUSE | D3DFVF_SPECULAR | \
                        D3DFVF_TEX0 )

// Assign texture
m_pd3dDevice->SetTexture(0, m_pTexture);

// Texture stage states
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE);
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE);  

m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_MODULATE);

m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE);
m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAARG2, D3DTA_DIFFUSE);

m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAOP, D3DTOP_MODULATE);

```



<span data-ttu-id="1109a-112">Это приводит к примитиву с градиентом прозрачности.</span><span class="sxs-lookup"><span data-stu-id="1109a-112">This results in a primitive with a transparency gradient.</span></span> <span data-ttu-id="1109a-113">Градиент прозрачен, где x = 0, и непрозрачный, где x — это максимальное значение.</span><span class="sxs-lookup"><span data-stu-id="1109a-113">The gradient is transparent where x = 0, and opaque where x is its maximum value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1109a-114">См. также</span><span class="sxs-lookup"><span data-stu-id="1109a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1109a-115">Альфа-смешение</span><span class="sxs-lookup"><span data-stu-id="1109a-115">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



