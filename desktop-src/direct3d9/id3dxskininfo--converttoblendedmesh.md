---
description: Принимает сетку и возвращает новую сетку с весовым коэффициентом смешения и таблицей сочетаний костей. В таблице описывается, какие кости влияют на подмножества сетки.
ms.assetid: c26a9e84-5731-4394-a047-5f1ffe7688d9
title: 'Метод ID3DXSkinInfo:: Конверттоблендедмеш (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 051c51291416dd7e190c83433a9bf84baeb92957
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713958"
---
# <a name="id3dxskininfoconverttoblendedmesh-method"></a><span data-ttu-id="bba0f-104">Метод ID3DXSkinInfo:: Конверттоблендедмеш</span><span class="sxs-lookup"><span data-stu-id="bba0f-104">ID3DXSkinInfo::ConvertToBlendedMesh method</span></span>

<span data-ttu-id="bba0f-105">Принимает сетку и возвращает новую сетку с весовым коэффициентом смешения и таблицей сочетаний костей.</span><span class="sxs-lookup"><span data-stu-id="bba0f-105">Takes a mesh and returns a new mesh with per-vertex blend weights and a bone combination table.</span></span> <span data-ttu-id="bba0f-106">В таблице описывается, какие кости влияют на подмножества сетки.</span><span class="sxs-lookup"><span data-stu-id="bba0f-106">The table describes which bones affect which subsets of the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="bba0f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bba0f-107">Syntax</span></span>


```C++
HRESULT ConvertToBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
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



## <a name="parameters"></a><span data-ttu-id="bba0f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bba0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bba0f-109">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bba0f-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba0f-110">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="bba0f-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="bba0f-111">Сетка входных данных.</span><span class="sxs-lookup"><span data-stu-id="bba0f-111">Input mesh.</span></span> <span data-ttu-id="bba0f-112">См. [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="bba0f-112">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba0f-113">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bba0f-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba0f-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bba0f-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bba0f-115">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="bba0f-115">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="bba0f-116">*паджаценциин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bba0f-116">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba0f-117">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="bba0f-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bba0f-118">Сведения о смежности входной сетки.</span><span class="sxs-lookup"><span data-stu-id="bba0f-118">Input mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="bba0f-119">*паджаценциаут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bba0f-119">*pAdjacencyOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba0f-120">Тип: **[ **лпдворд**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bba0f-120">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bba0f-121">Сведения о смежной сетке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="bba0f-121">Output mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="bba0f-122">*пфацеремап* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bba0f-122">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bba0f-123">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bba0f-123">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bba0f-124">Массив DWORD, по одному на каждое лицо, который определяет исходную сетку, соответствующую каждой грани в смешанной сетке.</span><span class="sxs-lookup"><span data-stu-id="bba0f-124">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the blended mesh.</span></span> <span data-ttu-id="bba0f-125">Если значение, заданное для этого аргумента, равно **null**, данные сопоставления лиц не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="bba0f-125">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="bba0f-126">*ппвертексремап* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bba0f-126">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bba0f-127">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="bba0f-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="bba0f-128">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) , который содержит DWORD для каждой вершины, указывающий, как новые вершины сопоставляются со старыми вершинами.</span><span class="sxs-lookup"><span data-stu-id="bba0f-128">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="bba0f-129">Такое перераспределение полезно, если необходимо изменить внешние данные на основе нового сопоставления вершин.</span><span class="sxs-lookup"><span data-stu-id="bba0f-129">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="bba0f-130">Этот параметр является необязательным. Может использоваться **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="bba0f-130">This parameter is optional; **NULL** may be used.</span></span>

</dd> <dt>

<span data-ttu-id="bba0f-131">*пмаксвертексинфл* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bba0f-131">*pMaxVertexInfl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bba0f-132">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bba0f-132">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bba0f-133">Указатель на DWORD, который будет содержать максимальное количество влияния на кость, необходимых для каждого из этих методов.</span><span class="sxs-lookup"><span data-stu-id="bba0f-133">Pointer to a DWORD that will contain the maximum number of bone influences required per vertex for this skinning method.</span></span>

</dd> <dt>

<span data-ttu-id="bba0f-134">*пнумбонекомбинатионс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bba0f-134">*pNumBoneCombinations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bba0f-135">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bba0f-135">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bba0f-136">Указатель на число костей в таблице сочетаний костей.</span><span class="sxs-lookup"><span data-stu-id="bba0f-136">Pointer to the number of bones in the bone combination table.</span></span>

</dd> <dt>

<span data-ttu-id="bba0f-137">*ппбонекомбинатионтабле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bba0f-137">*ppBoneCombinationTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bba0f-138">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="bba0f-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="bba0f-139">Указатель на таблицу сочетаний костей.</span><span class="sxs-lookup"><span data-stu-id="bba0f-139">Pointer to the bone combination table.</span></span> <span data-ttu-id="bba0f-140">Данные организованы в виде структуры [**D3DXBONECOMBINATION**](d3dxbonecombination.md) .</span><span class="sxs-lookup"><span data-stu-id="bba0f-140">The data is organized in a [**D3DXBONECOMBINATION**](d3dxbonecombination.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bba0f-141">*ппмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bba0f-141">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bba0f-142">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="bba0f-142">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="bba0f-143">Указатель на новую сетку.</span><span class="sxs-lookup"><span data-stu-id="bba0f-143">Pointer to the new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bba0f-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bba0f-144">Return value</span></span>

<span data-ttu-id="bba0f-145">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bba0f-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bba0f-146">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="bba0f-146">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bba0f-147">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="bba0f-147">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="bba0f-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bba0f-148">Remarks</span></span>

<span data-ttu-id="bba0f-149">Каждый элемент в массиве сопоставления указывает предыдущий индекс для этой позиции.</span><span class="sxs-lookup"><span data-stu-id="bba0f-149">Each element in the remap array specifies the previous index for that position.</span></span> <span data-ttu-id="bba0f-150">Например, если вершина находится в положении 3, но была повторно сопоставлена с позицией 5, то Пятый элемент Пвертексремап будет содержать значение 3.</span><span class="sxs-lookup"><span data-stu-id="bba0f-150">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap will contain 3.</span></span>

<span data-ttu-id="bba0f-151">Этот метод не выполняется на оборудовании, не поддерживающем смешение вершин с фиксированной функцией.</span><span class="sxs-lookup"><span data-stu-id="bba0f-151">This method does not run on hardware that does not support fixed-function vertex blending.</span></span>

## <a name="requirements"></a><span data-ttu-id="bba0f-152">Требования</span><span class="sxs-lookup"><span data-stu-id="bba0f-152">Requirements</span></span>



| <span data-ttu-id="bba0f-153">Требование</span><span class="sxs-lookup"><span data-stu-id="bba0f-153">Requirement</span></span> | <span data-ttu-id="bba0f-154">Значение</span><span class="sxs-lookup"><span data-stu-id="bba0f-154">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bba0f-155">Header</span><span class="sxs-lookup"><span data-stu-id="bba0f-155">Header</span></span><br/>  | <dl> <span data-ttu-id="bba0f-156"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bba0f-156"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bba0f-157">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bba0f-157">Library</span></span><br/> | <dl> <span data-ttu-id="bba0f-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bba0f-158"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bba0f-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bba0f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bba0f-160">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="bba0f-160">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
