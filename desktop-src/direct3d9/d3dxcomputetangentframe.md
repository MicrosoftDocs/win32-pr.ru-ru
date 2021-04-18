---
description: Вычисление векторов тангенса, бинормал и нормали для сетки.
ms.assetid: 54edb9a5-440d-4191-a58f-296e5b804e0c
title: Функция D3DXComputeTangentFrame (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrame
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b95d8f046499716a2c7972593093dfb409b11f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713925"
---
# <a name="d3dxcomputetangentframe-function"></a><span data-ttu-id="643b2-103">Функция D3DXComputeTangentFrame</span><span class="sxs-lookup"><span data-stu-id="643b2-103">D3DXComputeTangentFrame function</span></span>

<span data-ttu-id="643b2-104">Вычисление векторов тангенса, бинормал и нормали для сетки.</span><span class="sxs-lookup"><span data-stu-id="643b2-104">Compute tangent, binormal, and normal vectors for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="643b2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="643b2-105">Syntax</span></span>


```C++
HRESULT D3DXComputeTangentFrame(
  _In_ ID3DXMesh *pMesh,
  _In_ DWORD     dwOptions
);
```



## <a name="parameters"></a><span data-ttu-id="643b2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="643b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="643b2-107">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="643b2-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="643b2-108">Тип: **[ **ID3DXMesh**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="643b2-108">Type: **[**ID3DXMesh**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="643b2-109">Указатель на входной объект сетки [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="643b2-109">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="643b2-110">*двоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="643b2-110">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="643b2-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="643b2-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="643b2-112">Сочетание одного или нескольких флагов [**D3DXTANGENT**](./d3dxtangent.md) .</span><span class="sxs-lookup"><span data-stu-id="643b2-112">Combination of one or more [**D3DXTANGENT**](./d3dxtangent.md) flags.</span></span>

<span data-ttu-id="643b2-113">Используйте **значение NULL** , чтобы указать следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="643b2-113">Use **NULL** to specify the following options:</span></span>

-   <span data-ttu-id="643b2-114">Установите вес обычной векторной длины на угол в радианах, который выдается двумя краями, оставляемыми вершиной.</span><span class="sxs-lookup"><span data-stu-id="643b2-114">Weight the normal vector length by the angle, in radians, subtended by the two edges leaving the vertex.</span></span>
-   <span data-ttu-id="643b2-115">Вычисление ортогональной декартовой координаты из координат текстуры UV.</span><span class="sxs-lookup"><span data-stu-id="643b2-115">Compute orthogonal Cartesian coordinates from the UV texture coordinates.</span></span>
-   <span data-ttu-id="643b2-116">Текстуры не упаковываются в направлениях U или V</span><span class="sxs-lookup"><span data-stu-id="643b2-116">Textures are not wrapped in either U or V directions</span></span>
-   <span data-ttu-id="643b2-117">Частичные производные от относительно координат текстуры нормализованы.</span><span class="sxs-lookup"><span data-stu-id="643b2-117">Partial derivatives with respect to texture coordinates are normalized.</span></span>
-   <span data-ttu-id="643b2-118">Вершины упорядочиваются в направлении против часовой стрелки вокруг каждого треугольника.</span><span class="sxs-lookup"><span data-stu-id="643b2-118">Vertices are ordered in a counterclockwise direction around each triangle.</span></span>
-   <span data-ttu-id="643b2-119">Используйте одновершинные векторы, уже имеющиеся во входной сетке.</span><span class="sxs-lookup"><span data-stu-id="643b2-119">Use per-vertex normal vectors already present in the input mesh.</span></span>
-   <span data-ttu-id="643b2-120">Результаты будут храниться в исходной входной сетке.</span><span class="sxs-lookup"><span data-stu-id="643b2-120">The results will be stored in the original input mesh.</span></span> <span data-ttu-id="643b2-121">Функция завершится ошибкой, если необходимо создать новые вершины.</span><span class="sxs-lookup"><span data-stu-id="643b2-121">The function will fail if new vertices need to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="643b2-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="643b2-122">Return value</span></span>

<span data-ttu-id="643b2-123">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="643b2-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="643b2-124">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="643b2-124">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="643b2-125">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="643b2-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="643b2-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="643b2-126">Remarks</span></span>

<span data-ttu-id="643b2-127">Эта функция просто вызывает [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) со следующими входными параметрами:</span><span class="sxs-lookup"><span data-stu-id="643b2-127">This function simply calls [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) with the following input parameters:</span></span>


```
D3DXComputeTangentFrameEx(pMesh, D3DDECLUSAGE_TEXCOORD, 0,   
      D3DDECLUSAGE_BINORMAL, 0, D3DDECLUSAGE_TANGENT, 0, 
      D3DDECLUSAGE_NORMAL, 0, 
      dwOptions | D3DXTANGENT_GENERATE_IN_PLACE,
      NULL, 0.01f, 0.25f, 0.01f, NULL, NULL);
```



<span data-ttu-id="643b2-128">Единственные числа обрабатываются по мере необходимости путем группирования краев и разделения вершин.</span><span class="sxs-lookup"><span data-stu-id="643b2-128">Singularities are handled as required by grouping edges and splitting vertices.</span></span> <span data-ttu-id="643b2-129">Если необходимо разделить какие бы то ни было вершины, функция завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="643b2-129">If any vertices need to be split, the function will fail.</span></span> <span data-ttu-id="643b2-130">Вычисленный Стандартный вектор в каждой вершине всегда нормализуется с длиной единицы.</span><span class="sxs-lookup"><span data-stu-id="643b2-130">The computed normal vector at each vertex is always normalized to have unit length.</span></span>

<span data-ttu-id="643b2-131">Наиболее надежное решение для вычисления ортогональных декартных координат — не устанавливать флаги D3DXTANGENT \_ орсогонализе \_ от \_ вас и D3DXTANGENT \_ орсогонализе \_ из \_ V, чтобы ортогональные координаты ВЫчисляться из обеих координат UV-текстуры.</span><span class="sxs-lookup"><span data-stu-id="643b2-131">The most robust solution for computing orthogonal Cartesian coordinates is to not set flags D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V, so that orthogonal coordinates are computed from both UV texture coordinates.</span></span> <span data-ttu-id="643b2-132">Однако в этом случае, если значение U или V равно нулю, функция будет рассчитывать ортогональные координаты с помощью D3DXTANGENT \_ орсогонализе \_ из \_ V или D3DXTANGENT \_ орсогонализе \_ от \_ U соответственно.</span><span class="sxs-lookup"><span data-stu-id="643b2-132">However, in this case, if either U or V is zero, then the function will compute orthogonal coordinates using D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V or D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="643b2-133">Требования</span><span class="sxs-lookup"><span data-stu-id="643b2-133">Requirements</span></span>



| <span data-ttu-id="643b2-134">Требование</span><span class="sxs-lookup"><span data-stu-id="643b2-134">Requirement</span></span> | <span data-ttu-id="643b2-135">Значение</span><span class="sxs-lookup"><span data-stu-id="643b2-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="643b2-136">Header</span><span class="sxs-lookup"><span data-stu-id="643b2-136">Header</span></span><br/>  | <dl> <span data-ttu-id="643b2-137"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="643b2-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="643b2-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="643b2-138">Library</span></span><br/> | <dl> <span data-ttu-id="643b2-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="643b2-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="643b2-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="643b2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="643b2-141">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="643b2-141">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="643b2-142">**D3DXComputeTangentFrameEx**</span><span class="sxs-lookup"><span data-stu-id="643b2-142">**D3DXComputeTangentFrameEx**</span></span>](d3dxcomputetangentframeex.md)
</dt> <dt>

[<span data-ttu-id="643b2-143">**D3DXTANGENT**</span><span class="sxs-lookup"><span data-stu-id="643b2-143">**D3DXTANGENT**</span></span>](./d3dxtangent.md)
</dt> </dl>

 

 
