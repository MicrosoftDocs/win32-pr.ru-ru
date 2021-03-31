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
# <a name="using-vertex-tweening-direct3d-9"></a>Использование анимации вершин (Direct3D 9)

Чтобы определить, поддерживает ли Direct3D анимацию вершин, проверьте \_ флаг анимации D3DVTXPCAPS в элементе вертекспроцессингкапс структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) . В следующем примере кода используется метод [**IDirect3DDevice9:: жетдевицекапс**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) , чтобы определить, поддерживается ли tween-анимация.


```
// This example assumes that m_pD3DDevice is 
// a valid pointer to a IDirect3DDevice9 interface.
//
D3DCAPS9 d3dCaps;

m_pD3DDevice->GetDeviceCaps( &d3dCaps );
if( 0 != (d3dCaps.VertexProcessingCaps & D3DVTXPCAPS_TWEENING) )
    // Vertex tweening is supported.
```



Чтобы использовать анимацию векторной анимации, необходимо сначала настроить пользовательский тип вершин, который использует вторую обычную или вторую точку. В следующем примере кода показан пример объявления, включающего и вторую точку, и вторую позицию.


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



Следующим шагом является задание текущего объявления. В следующем примере кода показано, как это сделать.


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



Дополнительные сведения о создании пользовательского типа вершин и буфера вершин см. в разделе [Создание буфера вершин (Direct3D 9)](creating-a-vertex-buffer.md).

> [!Note]  
> Если включена анимация вершин, в текущем объявлении должна присутствовать вторая или Вторая нормальная.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Анимированная анимация вершин](vertex-tweening.md)
</dt> </dl>

 

 
