---
description: В данных вершин можно указать альфа-данные. Чтобы включить вершинную альфа-версию, задайте для параметра D3DRS \_ диффусематериалсаурце \_ значение D3DMCS COLOR1, чтобы среда выполнения Direct3D воспользулись рассеянным значением из рассеянного цвета, а не из материала.
ms.assetid: 2b0d842d-ee7d-4633-846d-96697153adc7
title: Вершинная альфа-версия (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f661c013e324a0bf209b4faca41d1974a41e81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139651"
---
# <a name="vertex-alpha-direct3d-9"></a><span data-ttu-id="0aee6-104">Вершинная альфа-версия (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0aee6-104">Vertex Alpha (Direct3D 9)</span></span>

<span data-ttu-id="0aee6-105">В данных вершин можно указать альфа-данные.</span><span class="sxs-lookup"><span data-stu-id="0aee6-105">Alpha data can be supplied in the vertex data.</span></span> <span data-ttu-id="0aee6-106">Чтобы включить вершинную альфа-версию, задайте для параметра D3DRS \_ диффусематериалсаурце \_ значение D3DMCS COLOR1, чтобы среда выполнения Direct3D воспользулись рассеянным значением из рассеянного цвета, а не из материала.</span><span class="sxs-lookup"><span data-stu-id="0aee6-106">To enable vertex alpha, set the D3DRS\_DIFFUSEMATERIALSOURCE to D3DMCS\_COLOR1 so that the Direct3D runtime takes the diffuse value from the diffuse color rather than the material.</span></span>


```
m_pd3dDevice->SetRenderState( D3DRS_DIFFUSEMATERIALSOURCE,  
                                D3DMCS_COLOR1 );
```



<span data-ttu-id="0aee6-107">Затем укажите альфа-значения в рассеянном цвете.</span><span class="sxs-lookup"><span data-stu-id="0aee6-107">Then, provide alpha values in the diffuse color.</span></span> <span data-ttu-id="0aee6-108">Функция Аддалфатоасфере добавляет альфа-канал в вершины сферы.</span><span class="sxs-lookup"><span data-stu-id="0aee6-108">The AddAlphaToASphere function, adds alpha to the vertices of a sphere.</span></span> <span data-ttu-id="0aee6-109">Ниже приведен пример того, как предоставить функции сведения о альфа-составляющей.</span><span class="sxs-lookup"><span data-stu-id="0aee6-109">Here's an example of how to provide the alpha information to the function.</span></span>


```
AddAlphaToASphere( m_pObstacleVertices, 12,  
                    D3DRGBA(light.dcvDiffuse.r, light.dcvDiffuse.g, 
                            light.dcvDiffuse.b, vAlpha ));
```



<span data-ttu-id="0aee6-110">Вот как выглядит функция.</span><span class="sxs-lookup"><span data-stu-id="0aee6-110">This is what the function looks like.</span></span>


```
 
void AddAlphaToASphere(D3DLVERTEX* pVertices, DWORD dwNumRings, D3DCOLOR lightcolor)
{
    WORD x, y;
    // rings around
    for( y=0; y < dwNumRings; y++ )
        for( x=0; x < (dwNumRings*2)+1; x++ )
            (pVertices++)->color = lightcolor;

    // top and bottom
    (pVertices++)->color = lightcolor;
    (pVertices++)->color = lightcolor;
}
```



<span data-ttu-id="0aee6-111">Аддалфатоасфере просто изменяет элемент цвета каждой вершины, имеющей тип D3DLVERTEX, чтобы включить альфа-информацию.</span><span class="sxs-lookup"><span data-stu-id="0aee6-111">AddAlphaToASphere simply modifies the color member of each vertex, which are of type D3DLVERTEX, to include the alpha information.</span></span>

<span data-ttu-id="0aee6-112">D3DLVERTEX выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="0aee6-112">D3DLVERTEX looks like this.</span></span>


```
 
// Lit vertex
typedef struct {
    D3DVALUE x, y, z;
    DWORD dwReserved;
    D3DCOLOR color, specular;
    D3DVALUE tu, tv;
} D3DLVERTEX, *LPD3DLVERTEX;
```



<span data-ttu-id="0aee6-113">Рисование сферы,</span><span class="sxs-lookup"><span data-stu-id="0aee6-113">Drawing the sphere,</span></span>


```
#define D3DFVF_LVERTEX ( D3DFVF_XYZ | D3DFVF_DIFFUSE | D3DFVF_SPECULAR | \
                        D3DFVF_TEX0 )

//...

// Draw the lit sphere
m_pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, D3DFVF_LVERTEX,
                                    m_pObstacleVertices, m_dwNumObstacleVertices,
                                    m_pObstacleIndices,  m_dwNumObstacleIndices, 0 );
```



<span data-ttu-id="0aee6-114">приводит к прозрачной сфере с использованием вершин альфа.</span><span class="sxs-lookup"><span data-stu-id="0aee6-114">results in a transparent sphere using vertex alpha.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0aee6-115">См. также</span><span class="sxs-lookup"><span data-stu-id="0aee6-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aee6-116">Альфа-смешение</span><span class="sxs-lookup"><span data-stu-id="0aee6-116">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



