---
description: Чтобы определить, поддерживает ли Direct3D анимацию вершин, проверьте \_ флаг анимации D3DVTXPCAPS в элементе вертекспроцессингкапс структуры D3DCAPS9.
ms.assetid: b60c7f96-3752-4703-9059-486d9906c508
title: Использование анимации вершин (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ca56cc521b5bff01a5d6af5c2d4ab6b02cd49e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894518"
---
# <a name="using-vertex-tweening-direct3d-9"></a><span data-ttu-id="d36b9-103">Использование анимации вершин (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d36b9-103">Using Vertex Tweening (Direct3D 9)</span></span>

<span data-ttu-id="d36b9-104">Чтобы определить, поддерживает ли Direct3D анимацию вершин, проверьте \_ флаг анимации D3DVTXPCAPS в элементе вертекспроцессингкапс структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="d36b9-104">To determine if Direct3D supports vertex tweening, check for the D3DVTXPCAPS\_TWEENING flag in the VertexProcessingCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span> <span data-ttu-id="d36b9-105">В следующем примере кода используется метод [**IDirect3DDevice9:: жетдевицекапс**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) , чтобы определить, поддерживается ли tween-анимация.</span><span class="sxs-lookup"><span data-stu-id="d36b9-105">The following code example uses the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method to determine if tweening is supported.</span></span>


```
// This example assumes that m_pD3DDevice is 
// a valid pointer to a IDirect3DDevice9 interface.
//
D3DCAPS9 d3dCaps;

m_pD3DDevice->GetDeviceCaps( &d3dCaps );
if( 0 != (d3dCaps.VertexProcessingCaps & D3DVTXPCAPS_TWEENING) )
    // Vertex tweening is supported.
```



<span data-ttu-id="d36b9-106">Чтобы использовать анимацию векторной анимации, необходимо сначала настроить пользовательский тип вершин, который использует вторую обычную или вторую точку.</span><span class="sxs-lookup"><span data-stu-id="d36b9-106">To use vector tweening, you must first set up a custom vertex type that uses a second normal or a second position.</span></span> <span data-ttu-id="d36b9-107">В следующем примере кода показан пример объявления, включающего и вторую точку, и вторую позицию.</span><span class="sxs-lookup"><span data-stu-id="d36b9-107">The following code example shows a sample declaration that includes both a second point and a second position.</span></span>


```
struct TEX_VERTEX
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DVECTOR position2;
    D3DVECTOR normal2;
};

//Create a vertex buffer with the type TEX_VERTEX.
```



<span data-ttu-id="d36b9-108">Следующим шагом является задание текущего объявления.</span><span class="sxs-lookup"><span data-stu-id="d36b9-108">The next step is to set the current declaration.</span></span> <span data-ttu-id="d36b9-109">В следующем примере кода показано, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="d36b9-109">The code example below shows how to do this.</span></span>


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    { 0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 1 },
    { 0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 1 },
    D3DDECL_END()
};
```



<span data-ttu-id="d36b9-110">Дополнительные сведения о создании пользовательского типа вершин и буфера вершин см. в разделе [Создание буфера вершин (Direct3D 9)](creating-a-vertex-buffer.md).</span><span class="sxs-lookup"><span data-stu-id="d36b9-110">For more information about creating a custom vertex type and a vertex buffer, see [Creating a Vertex Buffer (Direct3D 9)](creating-a-vertex-buffer.md).</span></span>

> [!Note]  
> <span data-ttu-id="d36b9-111">Если включена анимация вершин, в текущем объявлении должна присутствовать вторая или Вторая нормальная.</span><span class="sxs-lookup"><span data-stu-id="d36b9-111">When vertex tweening is enabled, a second position or a second normal must be present in the current declaration.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d36b9-112">См. также</span><span class="sxs-lookup"><span data-stu-id="d36b9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d36b9-113">Анимированная анимация вершин</span><span class="sxs-lookup"><span data-stu-id="d36b9-113">Vertex Tweening</span></span>](vertex-tweening.md)
</dt> </dl>

 

 
