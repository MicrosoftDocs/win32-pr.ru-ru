---
description: Разбивает прямоугольное исправление поверхности более высокого порядка в сетку с треугольником.
ms.assetid: d941d994-8a13-49ff-a0b1-b21a3f84ed78
title: Функция D3DXTessellateRectPatch (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateRectPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 887f0035b50efd860149410e50dd6abff301968d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273757"
---
# <a name="d3dxtessellaterectpatch-function"></a><span data-ttu-id="400b9-103">Функция D3DXTessellateRectPatch</span><span class="sxs-lookup"><span data-stu-id="400b9-103">D3DXTessellateRectPatch function</span></span>

<span data-ttu-id="400b9-104">Разбивает прямоугольное исправление поверхности более высокого порядка в сетку с треугольником.</span><span class="sxs-lookup"><span data-stu-id="400b9-104">Tessellates a rectangular higher-order surface patch into a triangle mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="400b9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="400b9-105">Syntax</span></span>


```C++
HRESULT D3DXTessellateRectPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3DRECTPATCH_INFO       *pRectPatchInfo,
  _Inout_       LPD3DXMESH              pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="400b9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="400b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="400b9-107">*ПВБ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="400b9-107">*pVB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="400b9-108">Тип: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span><span class="sxs-lookup"><span data-stu-id="400b9-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span></span>

<span data-ttu-id="400b9-109">Буфер вершин, содержащий данные исправления.</span><span class="sxs-lookup"><span data-stu-id="400b9-109">Vertex buffer containing the patch data.</span></span>

</dd> <dt>

<span data-ttu-id="400b9-110">*пнумсегс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="400b9-110">*pNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="400b9-111">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="400b9-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="400b9-112">Указатель на массив из четырех значений с плавающей запятой, определяющих количество сегментов, на которые должны быть разбиты все границы данного обновления прямоугольника при тесселяции.</span><span class="sxs-lookup"><span data-stu-id="400b9-112">Pointer to an array of four floating-point values that identify the number of segments into which each edge of the rectangle patch should be divided when tessellated.</span></span> <span data-ttu-id="400b9-113">См [**. \_ сведения о D3DRECTPATCH**](d3drectpatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="400b9-113">See [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="400b9-114">*пиндекл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="400b9-114">*pInDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="400b9-115">Тип: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="400b9-115">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="400b9-116">Структура объявления вершин, определяющая данные вершин.</span><span class="sxs-lookup"><span data-stu-id="400b9-116">Vertex declaration structure that defines the vertex data.</span></span> <span data-ttu-id="400b9-117">См. [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="400b9-117">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="400b9-118">*пректпатчинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="400b9-118">*pRectPatchInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="400b9-119">Тип: **const [**D3DRECTPATCH \_ info**](d3drectpatch-info.md) \***</span><span class="sxs-lookup"><span data-stu-id="400b9-119">Type: **const [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md)\***</span></span>

<span data-ttu-id="400b9-120">Описывает прямоугольное исправление.</span><span class="sxs-lookup"><span data-stu-id="400b9-120">Describes a rectangular patch.</span></span> <span data-ttu-id="400b9-121">См [**. \_ сведения о D3DRECTPATCH**](d3drectpatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="400b9-121">See [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="400b9-122">*пмеш* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="400b9-122">*pMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="400b9-123">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="400b9-123">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="400b9-124">Указатель на созданную сетку.</span><span class="sxs-lookup"><span data-stu-id="400b9-124">Pointer to the created mesh.</span></span> <span data-ttu-id="400b9-125">См. [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="400b9-125">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="400b9-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="400b9-126">Return value</span></span>

<span data-ttu-id="400b9-127">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="400b9-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="400b9-128">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="400b9-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="400b9-129">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="400b9-129">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="400b9-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="400b9-130">Remarks</span></span>

<span data-ttu-id="400b9-131">Используйте [**D3DXRectPatchSize**](d3dxrectpatchsize.md) , чтобы получить количество выходных вершин и индексов, необходимых для функции тесселяции.</span><span class="sxs-lookup"><span data-stu-id="400b9-131">Use [**D3DXRectPatchSize**](d3dxrectpatchsize.md) to get the number of output vertices and indices that the tessellation function needs.</span></span>

## <a name="requirements"></a><span data-ttu-id="400b9-132">Требования</span><span class="sxs-lookup"><span data-stu-id="400b9-132">Requirements</span></span>



| <span data-ttu-id="400b9-133">Требование</span><span class="sxs-lookup"><span data-stu-id="400b9-133">Requirement</span></span> | <span data-ttu-id="400b9-134">Значение</span><span class="sxs-lookup"><span data-stu-id="400b9-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="400b9-135">Header</span><span class="sxs-lookup"><span data-stu-id="400b9-135">Header</span></span><br/>  | <dl> <span data-ttu-id="400b9-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="400b9-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="400b9-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="400b9-137">Library</span></span><br/> | <dl> <span data-ttu-id="400b9-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="400b9-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="400b9-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="400b9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="400b9-140">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="400b9-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="400b9-141">**D3DXTessellateTriPatch**</span><span class="sxs-lookup"><span data-stu-id="400b9-141">**D3DXTessellateTriPatch**</span></span>](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
