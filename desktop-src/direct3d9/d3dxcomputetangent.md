---
description: Выполняет вычисление векторов касательных координат текстуры, заданных на стадии текстуры. Предоставляется для поддержки устаревших приложений. Используйте D3DXComputeTangentFrameEx для улучшения результатов.
ms.assetid: 39748459-3f9b-4b48-ae13-7143eb29c292
title: Функция D3DXComputeTangent (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangent
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cdb6a9dae3bdbad0f239fa61ba066d7b1bffb14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713651"
---
# <a name="d3dxcomputetangent-function"></a><span data-ttu-id="46f3d-105">Функция D3DXComputeTangent</span><span class="sxs-lookup"><span data-stu-id="46f3d-105">D3DXComputeTangent function</span></span>

<span data-ttu-id="46f3d-106">Выполняет вычисление векторов касательных координат текстуры, заданных на стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="46f3d-106">Computes the tangent vectors for the texture coordinates given in the texture stage.</span></span> <span data-ttu-id="46f3d-107">Предоставляется для поддержки устаревших приложений.</span><span class="sxs-lookup"><span data-stu-id="46f3d-107">Provided to support legacy applications.</span></span> <span data-ttu-id="46f3d-108">Используйте [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) для улучшения результатов.</span><span class="sxs-lookup"><span data-stu-id="46f3d-108">Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) for better results.</span></span>

## <a name="syntax"></a><span data-ttu-id="46f3d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46f3d-109">Syntax</span></span>


```C++
HRESULT D3DXComputeTangent(
  _In_       LPD3DXMESH Mesh,
  _In_       DWORD      TexStageIndex,
  _In_       DWORD      TangentIndex,
  _In_       DWORD      BinormIndex,
  _In_       DWORD      Wrap,
  _In_ const DWORD      *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="46f3d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="46f3d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46f3d-111">*Сетка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46f3d-111">*Mesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46f3d-112">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="46f3d-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="46f3d-113">Указатель на интерфейс [**ID3DXMesh**](id3dxmesh.md) , который представляет входную сетку.</span><span class="sxs-lookup"><span data-stu-id="46f3d-113">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface that represent the input mesh.</span></span>

</dd> <dt>

<span data-ttu-id="46f3d-114">*Тексстажеиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46f3d-114">*TexStageIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46f3d-115">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46f3d-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46f3d-116">Индекс, представляющий этап текстуры.</span><span class="sxs-lookup"><span data-stu-id="46f3d-116">Index that represents the texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="46f3d-117">*Танжентиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46f3d-117">*TangentIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46f3d-118">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46f3d-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46f3d-119">Индекс, предоставляющий индекс использования для данных касательно.</span><span class="sxs-lookup"><span data-stu-id="46f3d-119">Index that provides the usage index for the tangent data.</span></span> <span data-ttu-id="46f3d-120">Объявление вершины подразумевает использование; Этот индекс изменяет использование с помощью индекса использования.</span><span class="sxs-lookup"><span data-stu-id="46f3d-120">The vertex declaration implies the usage; this index modifies the usage with the usage index.</span></span> <span data-ttu-id="46f3d-121">Дополнительные сведения об объявлении вершин см. в разделе [объявление вершины (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="46f3d-121">For more information about a vertex declaration, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> <dt>

<span data-ttu-id="46f3d-122">*Бинорминдекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46f3d-122">*BinormIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46f3d-123">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46f3d-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46f3d-124">Индекс, предоставляющий индекс использования для данных бинормал.</span><span class="sxs-lookup"><span data-stu-id="46f3d-124">Index that provides the usage index for the binormal data.</span></span> <span data-ttu-id="46f3d-125">Объявление вершины подразумевает использование; Этот индекс изменяет использование с помощью индекса использования.</span><span class="sxs-lookup"><span data-stu-id="46f3d-125">The vertex declaration implies the usage; this index modifies the usage with the usage index.</span></span> <span data-ttu-id="46f3d-126">Дополнительные сведения об объявлении вершин см. в разделе [объявление вершины (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="46f3d-126">For more information about a vertex declaration, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> <dt>

<span data-ttu-id="46f3d-127">*Перенос по словам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46f3d-127">*Wrap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46f3d-128">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46f3d-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46f3d-129">Присвойте этому параметру значение 0, чтобы не выполнять перенос, или значение 1 для переноса в нужные и V направлениях.</span><span class="sxs-lookup"><span data-stu-id="46f3d-129">Set this value to 0 for no wrapping, or to 1 for wrapping in the U and V directions.</span></span>

</dd> <dt>

<span data-ttu-id="46f3d-130">*паджаценци* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46f3d-130">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46f3d-131">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="46f3d-131">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="46f3d-132">Указатель на массив из трех DWORD на грань, который должен быть заполнен смежными индексами граней.</span><span class="sxs-lookup"><span data-stu-id="46f3d-132">Pointer to an array of three DWORDs per face to be filled with adjacent face indices.</span></span> <span data-ttu-id="46f3d-133">Число байтов в этом массиве должно быть не меньше ((3 \* [**жетнумфацес**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)).</span><span class="sxs-lookup"><span data-stu-id="46f3d-133">The number of bytes in this array must be at least ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof(DWORD)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46f3d-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46f3d-134">Return value</span></span>

<span data-ttu-id="46f3d-135">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="46f3d-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="46f3d-136">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="46f3d-136">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="46f3d-137">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="46f3d-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="46f3d-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46f3d-138">Remarks</span></span>

<span data-ttu-id="46f3d-139">Если в объявлении вершины сетки заданы поля тангенса или бинормал, **D3DXComputeTangent** будет обновлять любые данные о тангенсе или бинормал данных, предоставляемые пользователем.</span><span class="sxs-lookup"><span data-stu-id="46f3d-139">If the mesh vertex declaration specifies tangent or binormal fields, **D3DXComputeTangent** will update any user-supplied tangent or binormal data.</span></span> <span data-ttu-id="46f3d-140">Кроме того, задайте для Танжентиндекс значение [D3DX \_ по умолчанию](other-d3dx-constants.md) , чтобы не обновлять предоставляемые пользователем данные касательно, или задайте для бинорминдекс значение D3DX \_ по умолчанию, чтобы не обновлять данные бинормал, предоставляемые пользователем.</span><span class="sxs-lookup"><span data-stu-id="46f3d-140">Alternatively, set TangentIndex to [D3DX\_DEFAULT](other-d3dx-constants.md) to not update the user-supplied tangent data, or set BinormIndex to D3DX\_DEFAULT to not update the user-supplied binormal data.</span></span> <span data-ttu-id="46f3d-141">Тексстажеиндекс не может иметь значение D3DX \_ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46f3d-141">TexStageIndex cannot be set to D3DX\_DEFAULT.</span></span>

<span data-ttu-id="46f3d-142">**D3DXComputeTangent** зависит от объявления вершины сетки, содержащего либо поле Бинормал (бинорминдекс), либо поле тангенса (танжентиндекс), либо и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="46f3d-142">**D3DXComputeTangent** depends on the mesh vertex declaration containing either the binormal field (BinormIndex), the tangent field (TangentIndex), or both.</span></span> <span data-ttu-id="46f3d-143">Если оба этих флажка отсутствуют, эта функция завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="46f3d-143">If both are missing, this function will fail.</span></span>

<span data-ttu-id="46f3d-144">Эта функция просто вызывает [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) со следующими входными параметрами:</span><span class="sxs-lookup"><span data-stu-id="46f3d-144">This function simply calls [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) with the following input parameters:</span></span>


```
D3DXComputeTangentFrameEx( Mesh,
                           D3DDECLUSAGE_TEXCOORD,
                           TexStageIndex,
                           ( BinormIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_BINORMAL,
                               // provides backward function compatibility
                           BinormIndex,
                           ( TangentIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_TANGENT,
                           TangentIndex,
                           D3DX_DEFAULT, // do not store normals
                           0,
                           ( Wrap ? D3DXTANGENT_WRAP_UV : 0 )
                               | D3DXTANGENT_GENERATE_IN_PLACE
                               | D3DXTANGENT_ORTHOGONALIZE_FROM_U,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a><span data-ttu-id="46f3d-145">Требования</span><span class="sxs-lookup"><span data-stu-id="46f3d-145">Requirements</span></span>



| <span data-ttu-id="46f3d-146">Требование</span><span class="sxs-lookup"><span data-stu-id="46f3d-146">Requirement</span></span> | <span data-ttu-id="46f3d-147">Значение</span><span class="sxs-lookup"><span data-stu-id="46f3d-147">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46f3d-148">Header</span><span class="sxs-lookup"><span data-stu-id="46f3d-148">Header</span></span><br/>  | <dl> <span data-ttu-id="46f3d-149"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="46f3d-149"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="46f3d-150">Библиотека</span><span class="sxs-lookup"><span data-stu-id="46f3d-150">Library</span></span><br/> | <dl> <span data-ttu-id="46f3d-151"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46f3d-151"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="46f3d-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46f3d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46f3d-153">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="46f3d-153">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
