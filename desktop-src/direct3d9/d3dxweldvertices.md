---
description: Расшов объединяет реплицированные вершины с одинаковыми атрибутами. Этот метод использует указанные значения Эпсилон для сравнения на равенство.
ms.assetid: bddf6e0c-55a1-40d2-8681-e7f0f9002bfa
title: Функция D3DXWeldVertices (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWeldVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 76e0a6f259bc8ba547a02b2e95cccf718d54e904
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821133"
---
# <a name="d3dxweldvertices-function"></a><span data-ttu-id="1eab7-104">Функция D3DXWeldVertices</span><span class="sxs-lookup"><span data-stu-id="1eab7-104">D3DXWeldVertices function</span></span>

<span data-ttu-id="1eab7-105">Расшов объединяет реплицированные вершины с одинаковыми атрибутами.</span><span class="sxs-lookup"><span data-stu-id="1eab7-105">Welds together replicated vertices that have equal attributes.</span></span> <span data-ttu-id="1eab7-106">Этот метод использует указанные значения Эпсилон для сравнения на равенство.</span><span class="sxs-lookup"><span data-stu-id="1eab7-106">This method uses specified epsilon values for equality comparisons.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eab7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1eab7-107">Syntax</span></span>


```C++
HRESULT D3DXWeldVertices(
  _In_          LPD3DXMESH       pMesh,
  _In_          DWORD            Flags,
  _In_    const D3DXWeldEpsilons *pEpsilons,
  _In_    const DWORD            *pAdjacencyIn,
  _Inout_       DWORD            *pAdjacencyOut,
  _Out_         DWORD            *pFaceRemap,
  _Out_         LPD3DXBUFFER     *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="1eab7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1eab7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eab7-109">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1eab7-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eab7-110">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="1eab7-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="1eab7-111">Указатель на объект [**ID3DXMesh**](id3dxmesh.md) — сетку, из которой следует расшов вершины.</span><span class="sxs-lookup"><span data-stu-id="1eab7-111">Pointer to an [**ID3DXMesh**](id3dxmesh.md) object, the mesh from which to weld vertices.</span></span>

</dd> <dt>

<span data-ttu-id="1eab7-112">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1eab7-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eab7-113">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1eab7-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1eab7-114">Сочетание одного или нескольких флагов из [**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md).</span><span class="sxs-lookup"><span data-stu-id="1eab7-114">Combination of one or more flags from [**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md).</span></span>

</dd> <dt>

<span data-ttu-id="1eab7-115">*пепсилонс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1eab7-115">*pEpsilons* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eab7-116">Тип: **const [**D3DXWeldEpsilons**](d3dxweldepsilons.md) \***</span><span class="sxs-lookup"><span data-stu-id="1eab7-116">Type: **const [**D3DXWeldEpsilons**](d3dxweldepsilons.md)\***</span></span>

<span data-ttu-id="1eab7-117">Указатель на структуру [**D3DXWeldEpsilons**](d3dxweldepsilons.md) , в которой указываются значения Эпсилон, используемые для этого метода.</span><span class="sxs-lookup"><span data-stu-id="1eab7-117">Pointer to a [**D3DXWeldEpsilons**](d3dxweldepsilons.md) structure, specifying the epsilon values to be used for this method.</span></span> <span data-ttu-id="1eab7-118">Используйте **значение NULL** , чтобы инициализировать все члены структуры до значения по умолчанию 1.0 e-6f.</span><span class="sxs-lookup"><span data-stu-id="1eab7-118">Use **NULL** to initialize all structure members to a default value of 1.0e-6f.</span></span>

</dd> <dt>

<span data-ttu-id="1eab7-119">*паджаценциин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1eab7-119">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eab7-120">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1eab7-120">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1eab7-121">Указатель на массив из трех DWORD на грань, который указывает три соседа для каждой грани в исходной сетке.</span><span class="sxs-lookup"><span data-stu-id="1eab7-121">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="1eab7-122">Если у границы нет смежных сторон, значение равно 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="1eab7-122">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="1eab7-123">Если этот параметр имеет значение **null**, будет вызван [**ID3DXBaseMesh:: женератеаджаценци**](id3dxbasemesh--generateadjacency.md) для создания логической информации о соседства.</span><span class="sxs-lookup"><span data-stu-id="1eab7-123">If this parameter is set to **NULL**, [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md) will be called to create logical adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="1eab7-124">*паджаценциаут* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="1eab7-124">*pAdjacencyOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eab7-125">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eab7-125">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1eab7-126">Указатель на массив из трех DWORD на грань, который указывает три соседа для каждой грани в оптимизированной сетке.</span><span class="sxs-lookup"><span data-stu-id="1eab7-126">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="1eab7-127">Если у границы нет смежных сторон, значение равно 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="1eab7-127">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="1eab7-128">*пфацеремап* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1eab7-128">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eab7-129">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eab7-129">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1eab7-130">Массив DWORD, по одному на каждый из них, который определяет исходную сетку, соответствующую каждой грани в раскадровой сетке.</span><span class="sxs-lookup"><span data-stu-id="1eab7-130">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the welded mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1eab7-131">*ппвертексремап* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1eab7-131">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eab7-132">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eab7-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1eab7-133">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) , который содержит DWORD для каждой вершины, указывающий, как новые вершины сопоставляются со старыми вершинами.</span><span class="sxs-lookup"><span data-stu-id="1eab7-133">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="1eab7-134">Такое перераспределение полезно, если необходимо изменить внешние данные на основе нового сопоставления вершин.</span><span class="sxs-lookup"><span data-stu-id="1eab7-134">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eab7-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1eab7-135">Return value</span></span>

<span data-ttu-id="1eab7-136">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1eab7-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1eab7-137">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="1eab7-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1eab7-138">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1eab7-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1eab7-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1eab7-139">Remarks</span></span>

<span data-ttu-id="1eab7-140">Эта функция использует предоставляемые сведения о смежности для определения реплицируемых точек.</span><span class="sxs-lookup"><span data-stu-id="1eab7-140">This function uses supplied adjacency information to determine the points that are replicated.</span></span> <span data-ttu-id="1eab7-141">Вершины сливаются на основе сравнения Эпсилон.</span><span class="sxs-lookup"><span data-stu-id="1eab7-141">Vertices are merged based on an epsilon comparison.</span></span> <span data-ttu-id="1eab7-142">Вершины с равным положением уже должны быть вычислены и представлены данными-представителями.</span><span class="sxs-lookup"><span data-stu-id="1eab7-142">Vertices with equal position must already have been calculated and represented by point-representative data.</span></span>

<span data-ttu-id="1eab7-143">Эта функция сочетает в себе логически разпепсилонс вершины, имеющие аналогичные компоненты, такие как нормали или координаты текстуры в.</span><span class="sxs-lookup"><span data-stu-id="1eab7-143">This function combines logically-welded vertices that have similar components, such as normals or texture coordinates within pEpsilons.</span></span>

<span data-ttu-id="1eab7-144">В следующем примере кода вызывается эта функция с включенным Велдинг.</span><span class="sxs-lookup"><span data-stu-id="1eab7-144">The following example code calls this function with welding enabled.</span></span> <span data-ttu-id="1eab7-145">Вершины сравниваются с использованием значений Эпсилон для обычных векторов и позиций вершин.</span><span class="sxs-lookup"><span data-stu-id="1eab7-145">Vertices are compared using epsilon values for normal vector and vertex position.</span></span> <span data-ttu-id="1eab7-146">Указатель возвращается в массив пересопоставления лицевой стороны (*пфацеремап*).</span><span class="sxs-lookup"><span data-stu-id="1eab7-146">A pointer is returned to a face remapping array (*pFaceRemap*).</span></span>


```
TCHAR            strMediaPath[512];       // X-file path 
LPD3DXBUFFER     pAdjacencyBuffer = NULL; // adjacency data buffer
LPD3DXBUFFER     pD3DXMtrlBuffer  = NULL; // material buffer
LPD3DXMESH       pMesh            = NULL; // mesh object
DWORD            m_dwNumMaterials;        // number of materials
D3DXWELDEPSILONS Epsilons;                // structure with epsilon values
DWORD            *pFaceRemap[65536];      // face remapping array
DWORD            i;                       // internal variable
    
    // Load the mesh from the specified file
    hr = D3DXLoadMeshFromX ( strMediaPath,
                         D3DXMESH_MANAGED,
                         m_pd3dDevice,
                         &pAdjacencyBuffer,
                         &pD3DXMtrlBuffer,
                         NULL,
                         &m_dwNumMaterials,
                         &pMesh ) )
                             
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
    
    // Set epsilon values
    Epsilons.Normal = 0.001;
    Epsilons.Position = 0.1;
    
    // Weld the vertices
    for( i=0; i < 65536; i++ )
    { 
        pFaceRemap[i] = 0; 
    }
    
    hr = D3DXWeldVertices ( pMesh,
                            D3DXWELDEPSILONS_WELDPARTIALMATCHES,
                            &Epsilons,
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pFaceRemap,
                            NULL )
                            
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
```



## <a name="requirements"></a><span data-ttu-id="1eab7-147">Требования</span><span class="sxs-lookup"><span data-stu-id="1eab7-147">Requirements</span></span>



| <span data-ttu-id="1eab7-148">Требование</span><span class="sxs-lookup"><span data-stu-id="1eab7-148">Requirement</span></span> | <span data-ttu-id="1eab7-149">Значение</span><span class="sxs-lookup"><span data-stu-id="1eab7-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1eab7-150">Header</span><span class="sxs-lookup"><span data-stu-id="1eab7-150">Header</span></span><br/>  | <dl> <span data-ttu-id="1eab7-151"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1eab7-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1eab7-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1eab7-152">Library</span></span><br/> | <dl> <span data-ttu-id="1eab7-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1eab7-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1eab7-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1eab7-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eab7-155">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="1eab7-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
