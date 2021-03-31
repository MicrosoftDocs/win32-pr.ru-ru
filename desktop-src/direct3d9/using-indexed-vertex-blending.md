---
description: Состояния преобразования 256-511 зарезервированы для хранения до 256 матриц, которые можно индексировать с помощью 8-разрядных индексов.
ms.assetid: 4c15cfc5-afdf-48d4-8fd1-b10cbe596a1c
title: Использование индексированного смешения вершин (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120362e4a86081ff51aee9053d1526a9a08f014a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894309"
---
# <a name="using-indexed-vertex-blending-direct3d-9"></a><span data-ttu-id="0af2a-103">Использование индексированного смешения вершин (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0af2a-103">Using Indexed Vertex Blending (Direct3D 9)</span></span>

<span data-ttu-id="0af2a-104">Состояния преобразования 256-511 зарезервированы для хранения до 256 матриц, которые можно индексировать с помощью 8-разрядных индексов.</span><span class="sxs-lookup"><span data-stu-id="0af2a-104">Transform states 256-511 are reserved to store up to 256 matrices that can be indexed using 8-bit indices.</span></span> <span data-ttu-id="0af2a-105">Используйте макрос [**D3DTS \_ ворлдматрикс**](d3dts-worldmatrix.md) , чтобы сопоставлять индексы 0-255 с соответствующими состояниями преобразования.</span><span class="sxs-lookup"><span data-stu-id="0af2a-105">Use the macro [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) to map indices 0-255 to the corresponding transform states.</span></span> <span data-ttu-id="0af2a-106">В следующем примере кода показано, как использовать метод [**IDirect3DDevice9:: сеттрансформ**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) , чтобы установить матрицу с состоянием преобразования с номером 256 в матрицу идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="0af2a-106">The following code example shows how to use the [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) method to set the matrix at transform state number 256 to an identity matrix.</span></span>


```
D3DMATRIX matBlend1;
D3DXMatrixIdentity( &matBlend1 );
m_pD3DDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matBlend );
```



<span data-ttu-id="0af2a-107">Чтобы включить или отключить индексирование вершин, установите \_ для состояния отрисовки D3DRS Индекседвертексбленденабле **значение true**.</span><span class="sxs-lookup"><span data-stu-id="0af2a-107">To enable or disable indexed vertex blending, set the D3DRS\_INDEXEDVERTEXBLENDENABLE render state to **TRUE**.</span></span> <span data-ttu-id="0af2a-108">Если состояние отрисовки включено, то индексы матрицы необходимо передавать в виде упакованных DWORD с каждой вершиной.</span><span class="sxs-lookup"><span data-stu-id="0af2a-108">When the render state is enabled ,you must pass matrix indices as packed DWORDs with every vertex.</span></span> <span data-ttu-id="0af2a-109">Если состояние рендеринга отключено и включено смешение вершин, то оно эквивалентно тому, что в каждой вершине матрица имеет индексы 0, 1, 2 и 3.</span><span class="sxs-lookup"><span data-stu-id="0af2a-109">When this render state is disabled and vertex blending is enabled, it is equivalent to having the matrix indices 0, 1, 2, and 3 in every vertex.</span></span> <span data-ttu-id="0af2a-110">В приведенном ниже примере кода используется метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) для включения индексированного смешения вершин.</span><span class="sxs-lookup"><span data-stu-id="0af2a-110">The code example below uses the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method to enable indexed vertex blending.</span></span>


```
m_pD3DDevice->SetRenderState( D3DRS_INDEXEDVERTEXBLENDENABLE, TRUE );
```



<span data-ttu-id="0af2a-111">Чтобы включить или отключить смешение вершин, установите для состояния отрисовки [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) значение, отличное от D3DRS \_ Disable из перечислимого типа [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) .</span><span class="sxs-lookup"><span data-stu-id="0af2a-111">To enable or disable vertex blending, set the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) render state to a value other than D3DRS\_DISABLE from the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="0af2a-112">Если для этого состояния рендеринга не задано значение D3DRS \_ Disable, необходимо передать необходимое число весов для каждой вершины.</span><span class="sxs-lookup"><span data-stu-id="0af2a-112">If this render state is not set to D3DRS\_DISABLE, then you must pass the required number of weights for each vertex.</span></span> <span data-ttu-id="0af2a-113">В следующем примере кода используется **IDirect3DDevice9:: сетрендерстате** для включения смешения вершин с тремя весовыми коэффициентами для каждой вершины.</span><span class="sxs-lookup"><span data-stu-id="0af2a-113">The following code example uses **IDirect3DDevice9::SetRenderState** to enable vertex blending with three weights for each vertex.</span></span>


```
m_pD3DDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_3WEIGHTS );
```



## <a name="determining-indexed-vertex-blending-support"></a><span data-ttu-id="0af2a-114">Определение поддержки индексированного смешения вершин</span><span class="sxs-lookup"><span data-stu-id="0af2a-114">Determining Indexed Vertex Blending Support</span></span>

<span data-ttu-id="0af2a-115">Чтобы определить максимальный размер для матричной матрицы смешения вершин, проверьте элемент Максвертексблендматриксиндекс структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="0af2a-115">To determine the maximum size for the indexed vertex blending matrix, check the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure's MaxVertexBlendMatrixIndex member.</span></span> <span data-ttu-id="0af2a-116">В приведенном ниже примере кода для получения этого размера используется метод [**IDirect3DDevice9:: жетдевицекапс**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) .</span><span class="sxs-lookup"><span data-stu-id="0af2a-116">The code example below uses the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method to retrieve this size.</span></span>


```
D3DCAPS9 d3dCaps;
    
m_pD3DDevice->GetDeviceCaps( &d3dCaps );
IndexedMatrixMaxSize = d3dCaps.MaxVertexBlendMatrixIndex;
```



<span data-ttu-id="0af2a-117">Если значение, заданное в Максвертексблендматриксиндекс, равно 0, устройство не поддерживает индексированные матрицы.</span><span class="sxs-lookup"><span data-stu-id="0af2a-117">If the value set in MaxVertexBlendMatrixIndex is 0, the device does not support indexed matrices.</span></span>

> [!Note]  
> <span data-ttu-id="0af2a-118">При использовании программной обработки вершин можно использовать матрицы 256 для индексированного смешения вершин с нормальным смешением или без них.</span><span class="sxs-lookup"><span data-stu-id="0af2a-118">When software vertex processing is used, 256 matrices can be used for indexed vertex blending, with or without normal blending.</span></span>

 

## <a name="passing-matrix-indices-to-direct3d"></a><span data-ttu-id="0af2a-119">Передача индексов матрицы в Direct3D</span><span class="sxs-lookup"><span data-stu-id="0af2a-119">Passing Matrix Indices to Direct3D</span></span>

<span data-ttu-id="0af2a-120">Индексы в мировых матрицах можно передавать в Direct3D с помощью устаревших шейдеров вершин-ФВФ-или объявлений.</span><span class="sxs-lookup"><span data-stu-id="0af2a-120">World matrix indices can be passed to Direct3D by using legacy vertex shaders - FVF - or declarations.</span></span>

<span data-ttu-id="0af2a-121">В приведенном ниже примере кода показано, как использовать устаревшие шейдеры вершин.</span><span class="sxs-lookup"><span data-stu-id="0af2a-121">The code example below shows how to use legacy vertex shaders.</span></span>


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
};
    
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZB2 | D3DFVF_LASTBETA_UBYTE4 |
                             D3DFVF_NORMAL);
```



<span data-ttu-id="0af2a-122">Если используется устаревший шейдер вершин, индексы матрицы передаются вместе с позициями вершин с помощью \_ флагов КСИЗБН D3DFVF.</span><span class="sxs-lookup"><span data-stu-id="0af2a-122">When a legacy vertex shader is used, matrix indices are passed together with vertex positions using D3DFVF\_XYZBn flags.</span></span> <span data-ttu-id="0af2a-123">Индексы матрицы передаются как байты внутри DWORD и должны присутствовать сразу после последнего веса вершины.</span><span class="sxs-lookup"><span data-stu-id="0af2a-123">Matrix indices are passed as bytes inside a DWORD and must be present immediately after the last vertex weight.</span></span> <span data-ttu-id="0af2a-124">Весовые коэффициенты вершин также передаются с помощью D3DFVF \_ ксизбн.</span><span class="sxs-lookup"><span data-stu-id="0af2a-124">Vertex weights are also passed using D3DFVF\_XYZBn.</span></span> <span data-ttu-id="0af2a-125">Упакованный DWORD содержит index3, index2, index1 и index0, где index0 находится в наименьшем байте DWORD.</span><span class="sxs-lookup"><span data-stu-id="0af2a-125">A packed DWORD contains index3, index2, index1, and index0, where index0 is located in the lowest byte of the DWORD.</span></span> <span data-ttu-id="0af2a-126">Количество используемых индексов в мировом виде равно числу, переданному количеству матриц, используемых для смешения, как определено в [**D3DRS \_ вертексбленд**](./d3drenderstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="0af2a-126">The number of used world-matrix indices is equal to the number passed to the number of matrices used for blending as defined by [**D3DRS\_VERTEXBLEND**](./d3drenderstatetype.md).</span></span>

<span data-ttu-id="0af2a-127">При использовании объявления D3DVSDE \_ блендиндицес определяет входной регистр вершин для получения индексов матрицы.</span><span class="sxs-lookup"><span data-stu-id="0af2a-127">When a declaration is used, D3DVSDE\_BLENDINDICES defines the input vertex register to get matrix indices from.</span></span> <span data-ttu-id="0af2a-128">Индексы матрицы должны передаваться как D3DVSDT \_ UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="0af2a-128">Matrix indices must be passed as D3DVSDT\_UBYTE4.</span></span>

<span data-ttu-id="0af2a-129">В приведенном ниже примере кода показано, как использовать объявления.</span><span class="sxs-lookup"><span data-stu-id="0af2a-129">The code example below shows how to use declarations.</span></span> <span data-ttu-id="0af2a-130">Обратите внимание, что порядок компонентов больше не важен, если не используется Вершинный шейдер с фиксированной функцией.</span><span class="sxs-lookup"><span data-stu-id="0af2a-130">Note that the order of the components is no longer important unless using a fixed-function vertex shader.</span></span>

<span data-ttu-id="0af2a-131">Ниже приведено описание вершины.</span><span class="sxs-lookup"><span data-stu-id="0af2a-131">Here is the vertex declaration.</span></span>


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
}
```



<span data-ttu-id="0af2a-132">Ниже приведено соответствующее объявление регистра.</span><span class="sxs-lookup"><span data-stu-id="0af2a-132">Here is the corresponding register declaration.</span></span>


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT1, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDWEIGHT, 0 },
    { 0, 16, D3DDECLTYPE_UBYTE4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDINDICES, 0 },
    { 0, 20, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    D3DDECL_END()
};
```



## <a name="related-topics"></a><span data-ttu-id="0af2a-133">См. также</span><span class="sxs-lookup"><span data-stu-id="0af2a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0af2a-134">Наложение индексированных вершин</span><span class="sxs-lookup"><span data-stu-id="0af2a-134">Indexed Vertex Blending</span></span>](indexed-vertex-blending.md)
</dt> </dl>

 

 
