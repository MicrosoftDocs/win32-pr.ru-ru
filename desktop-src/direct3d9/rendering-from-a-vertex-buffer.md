---
description: 'Отрисовка данных вершин из буфера вершин требует выполнения нескольких шагов. Сначала необходимо задать источник потока, вызвав метод IDirect3DDevice9:: Сетстреамсаурце, как показано в следующем примере.'
ms.assetid: a0435a3d-e1dd-4365-904d-8e5713e379ce
title: Подготовка к просмотру из буфера вершин (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cebb68c5395a827a9aee4ea1f8465257c436bb7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139271"
---
# <a name="rendering-from-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="8bd5c-104">Подготовка к просмотру из буфера вершин (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8bd5c-104">Rendering from a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="8bd5c-105">Отрисовка данных вершин из буфера вершин требует выполнения нескольких шагов.</span><span class="sxs-lookup"><span data-stu-id="8bd5c-105">Rendering vertex data from a vertex buffer requires a few steps.</span></span> <span data-ttu-id="8bd5c-106">Сначала необходимо задать источник потока, вызвав метод [**IDirect3DDevice9:: сетстреамсаурце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="8bd5c-106">First, you need to set the stream source by calling the [**IDirect3DDevice9::SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) method, as shown in the following example.</span></span>


```
d3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
```



<span data-ttu-id="8bd5c-107">Первый параметр [**IDirect3DDevice9:: сетстреамсаурце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) указывает Direct3D на источник потока данных устройства.</span><span class="sxs-lookup"><span data-stu-id="8bd5c-107">The first parameter of [**IDirect3DDevice9::SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) tells Direct3D the source of the device data stream.</span></span> <span data-ttu-id="8bd5c-108">Вторым параметром является буфер вершин для привязки к потоку данных.</span><span class="sxs-lookup"><span data-stu-id="8bd5c-108">The second parameter is the vertex buffer to bind to the data stream.</span></span> <span data-ttu-id="8bd5c-109">Третий параметр — смещение от начала потока до начала данных вершин в байтах.</span><span class="sxs-lookup"><span data-stu-id="8bd5c-109">The third parameter is the offset from the beginning of the stream to the beginning of the vertex data, in bytes.</span></span> <span data-ttu-id="8bd5c-110">Четвертый параметр — это шаг компонента в байтах.</span><span class="sxs-lookup"><span data-stu-id="8bd5c-110">The fourth parameter is the stride of the component, in bytes.</span></span> <span data-ttu-id="8bd5c-111">В приведенном выше образце кода размер КУСТОМВЕРТЕКС используется для шага компонента.</span><span class="sxs-lookup"><span data-stu-id="8bd5c-111">In the sample code above, the size of a CUSTOMVERTEX is used for the stride of the component.</span></span>

<span data-ttu-id="8bd5c-112">Следующим шагом является информирование Direct3D о том, какой шейдер вершин использовать, вызвав метод [**IDirect3DDevice9:: сетвертексшадер**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) .</span><span class="sxs-lookup"><span data-stu-id="8bd5c-112">The next step is to inform Direct3D which vertex shader to use by calling the [**IDirect3DDevice9::SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) method.</span></span> <span data-ttu-id="8bd5c-113">В следующем примере кода задается код ФВФ для шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="8bd5c-113">The following sample code sets an FVF code for the vertex shader.</span></span> <span data-ttu-id="8bd5c-114">Это информирует Direct3D о типах вершин, с которыми он работает.</span><span class="sxs-lookup"><span data-stu-id="8bd5c-114">This informs Direct3D of the types of vertices it is dealing with.</span></span>


```
d3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
```



<span data-ttu-id="8bd5c-115">После установки источника потока и шейдера вершин все методы рисования будут использовать буфер вершин.</span><span class="sxs-lookup"><span data-stu-id="8bd5c-115">After setting the stream source and vertex shader, any draw methods will use the vertex buffer.</span></span> <span data-ttu-id="8bd5c-116">В приведенном ниже примере кода показано, как визуализировать вершины из буфера вершин с помощью метода [**IDirect3DDevice9::D равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .</span><span class="sxs-lookup"><span data-stu-id="8bd5c-116">The code example below shows how to render vertices from a vertex buffer with the [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method.</span></span>


```
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 1 );
```



<span data-ttu-id="8bd5c-117">Второй параметр, [**IDirect3DDevice9::D равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) , принимает индекс первого вектора в буфере вершин для загрузки.</span><span class="sxs-lookup"><span data-stu-id="8bd5c-117">The second parameter that [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) accepts is the index of the first vector in the vertex buffer to load.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8bd5c-118">См. также</span><span class="sxs-lookup"><span data-stu-id="8bd5c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bd5c-119">Буферы вершин</span><span class="sxs-lookup"><span data-stu-id="8bd5c-119">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> <dt>

[<span data-ttu-id="8bd5c-120">Отрисовка из буферов вершин и индексов (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8bd5c-120">Rendering from Vertex and Index Buffers (Direct3D 9)</span></span>](rendering-from-vertex-and-index-buffers.md)
</dt> </dl>

 

 
