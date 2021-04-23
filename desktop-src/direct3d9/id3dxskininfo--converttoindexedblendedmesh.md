---
description: Принимает сетку и возвращает новую сетку с весовыми коэффициентами перехода на вершину, индексами и комбинацией костей. В таблице описывается, какие палитры костей влияют на подмножества сетки.
ms.assetid: e4758a3b-8a45-4ed3-aa62-9713d12afc56
title: 'Метод ID3DXSkinInfo:: Конверттоиндекседблендедмеш (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToIndexedBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87c8a4b943a647e52d7260f1ff53b32b40756761
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703948"
---
# <a name="id3dxskininfoconverttoindexedblendedmesh-method"></a><span data-ttu-id="9713f-104">Метод ID3DXSkinInfo:: Конверттоиндекседблендедмеш</span><span class="sxs-lookup"><span data-stu-id="9713f-104">ID3DXSkinInfo::ConvertToIndexedBlendedMesh method</span></span>

<span data-ttu-id="9713f-105">Принимает сетку и возвращает новую сетку с весовыми коэффициентами перехода на вершину, индексами и комбинацией костей.</span><span class="sxs-lookup"><span data-stu-id="9713f-105">Takes a mesh and returns a new mesh with per-vertex blend weights, indices, and a bone combination table.</span></span> <span data-ttu-id="9713f-106">В таблице описывается, какие палитры костей влияют на подмножества сетки.</span><span class="sxs-lookup"><span data-stu-id="9713f-106">The table describes which bone palettes affect which subsets of the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="9713f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9713f-107">Syntax</span></span>


```C++
HRESULT ConvertToIndexedBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
  [in]        DWORD        paletteSize,
  [in]  const DWORD        *pAdjacencyIn,
  [in]        LPDWORD      pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap,
  [out]       DWORD        *pMaxVertexInfl,
  [out]       DWORD        *pNumBoneCombinations,
  [out]       LPD3DXBUFFER *ppBoneCombinationTable,
  [out]       LPD3DXMESH   *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="9713f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9713f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9713f-109">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9713f-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9713f-110">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="9713f-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="9713f-111">Входная сетка.</span><span class="sxs-lookup"><span data-stu-id="9713f-111">The input mesh.</span></span> <span data-ttu-id="9713f-112">См. [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="9713f-112">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="9713f-113">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9713f-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9713f-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9713f-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9713f-115">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="9713f-115">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="9713f-116">*палеттесизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9713f-116">*paletteSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9713f-117">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9713f-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9713f-118">Число матриц костей, доступных для обложки палитры матрицы.</span><span class="sxs-lookup"><span data-stu-id="9713f-118">Number of bone matrices available for matrix palette skinning.</span></span>

</dd> <dt>

<span data-ttu-id="9713f-119">*паджаценциин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9713f-119">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9713f-120">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="9713f-120">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9713f-121">Сведения о смежности входной сетки.</span><span class="sxs-lookup"><span data-stu-id="9713f-121">Input mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="9713f-122">*паджаценциаут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9713f-122">*pAdjacencyOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9713f-123">Тип: **[ **лпдворд**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9713f-123">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9713f-124">Сведения о смежной сетке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9713f-124">Output mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="9713f-125">*пфацеремап* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9713f-125">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9713f-126">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9713f-126">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9713f-127">Массив DWORD, по одному на каждое лицо, который определяет исходную сетку, соответствующую каждой грани в смешанной сетке.</span><span class="sxs-lookup"><span data-stu-id="9713f-127">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the blended mesh.</span></span> <span data-ttu-id="9713f-128">Если значение, заданное для этого аргумента, равно **null**, данные сопоставления лиц не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="9713f-128">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="9713f-129">*ппвертексремап* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9713f-129">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9713f-130">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9713f-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9713f-131">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) , который содержит DWORD для каждой вершины, указывающий, как новые вершины сопоставляются со старыми вершинами.</span><span class="sxs-lookup"><span data-stu-id="9713f-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="9713f-132">Такое перераспределение полезно, если необходимо изменить внешние данные на основе нового сопоставления вершин.</span><span class="sxs-lookup"><span data-stu-id="9713f-132">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="9713f-133">Этот параметр является необязательным. Может использоваться **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="9713f-133">This parameter is optional; **NULL** may be used.</span></span>

</dd> <dt>

<span data-ttu-id="9713f-134">*пмаксвертексинфл* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9713f-134">*pMaxVertexInfl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9713f-135">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9713f-135">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9713f-136">Указатель на DWORD, который будет содержать максимальное количество влияния на кость, необходимых для каждого из этих методов.</span><span class="sxs-lookup"><span data-stu-id="9713f-136">Pointer to a DWORD that will contain the maximum number of bone influences required per vertex for this skinning method.</span></span>

</dd> <dt>

<span data-ttu-id="9713f-137">*пнумбонекомбинатионс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9713f-137">*pNumBoneCombinations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9713f-138">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9713f-138">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9713f-139">Указатель на число костей в таблице сочетаний костей.</span><span class="sxs-lookup"><span data-stu-id="9713f-139">Pointer to the number of bones in the bone combination table.</span></span>

</dd> <dt>

<span data-ttu-id="9713f-140">*ппбонекомбинатионтабле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9713f-140">*ppBoneCombinationTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9713f-141">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9713f-141">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9713f-142">Указатель на таблицу сочетаний костей.</span><span class="sxs-lookup"><span data-stu-id="9713f-142">Pointer to the bone combination table.</span></span> <span data-ttu-id="9713f-143">Данные организованы в виде структуры [**D3DXBONECOMBINATION**](d3dxbonecombination.md) .</span><span class="sxs-lookup"><span data-stu-id="9713f-143">The data is organized in a [**D3DXBONECOMBINATION**](d3dxbonecombination.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9713f-144">*ппмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9713f-144">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9713f-145">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="9713f-145">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="9713f-146">Указатель на новую сетку.</span><span class="sxs-lookup"><span data-stu-id="9713f-146">Pointer to the new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9713f-147">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9713f-147">Return value</span></span>

<span data-ttu-id="9713f-148">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9713f-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9713f-149">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="9713f-149">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9713f-150">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="9713f-150">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9713f-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9713f-151">Remarks</span></span>

<span data-ttu-id="9713f-152">Каждый элемент в массивах сопоставления указывает предыдущий индекс для этой позиции.</span><span class="sxs-lookup"><span data-stu-id="9713f-152">Each element in the remap arrays specifies the previous index for that position.</span></span> <span data-ttu-id="9713f-153">Например, если вершина находится в положении 3, но была повторно сопоставлена с позицией 5, то Пятый элемент Пвертексремап будет содержать значение 3.</span><span class="sxs-lookup"><span data-stu-id="9713f-153">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap will contain 3.</span></span>

<span data-ttu-id="9713f-154">Этот метод не выполняется на оборудовании, не поддерживающем смешение вершин с фиксированной функцией.</span><span class="sxs-lookup"><span data-stu-id="9713f-154">This method does not run on hardware that does not support fixed-function vertex blending.</span></span>

## <a name="requirements"></a><span data-ttu-id="9713f-155">Требования</span><span class="sxs-lookup"><span data-stu-id="9713f-155">Requirements</span></span>



| <span data-ttu-id="9713f-156">Требование</span><span class="sxs-lookup"><span data-stu-id="9713f-156">Requirement</span></span> | <span data-ttu-id="9713f-157">Значение</span><span class="sxs-lookup"><span data-stu-id="9713f-157">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9713f-158">Header</span><span class="sxs-lookup"><span data-stu-id="9713f-158">Header</span></span><br/>  | <dl> <span data-ttu-id="9713f-159"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9713f-159"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9713f-160">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9713f-160">Library</span></span><br/> | <dl> <span data-ttu-id="9713f-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9713f-161"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9713f-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9713f-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9713f-163">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="9713f-163">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
