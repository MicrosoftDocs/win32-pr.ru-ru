---
description: Тесселяция треугольного исправления поверхности с более высоким порядком в сетке с треугольником.
ms.assetid: bcc9143f-fec0-491a-8d32-1df961b8dade
title: Функция D3DXTessellateTriPatch (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateTriPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 61d5a426f9fe3331b85c4a881219319622283820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821045"
---
# <a name="d3dxtessellatetripatch-function"></a><span data-ttu-id="dadef-103">Функция D3DXTessellateTriPatch</span><span class="sxs-lookup"><span data-stu-id="dadef-103">D3DXTessellateTriPatch function</span></span>

<span data-ttu-id="dadef-104">Тесселяция треугольного исправления поверхности с более высоким порядком в сетке с треугольником.</span><span class="sxs-lookup"><span data-stu-id="dadef-104">Tessellates a triangular higher-order surface patch into a triangle mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="dadef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dadef-105">Syntax</span></span>


```C++
HRESULT D3DXTessellateTriPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3TRIPATCH_INFO         *pTriPatchInfo,
  _Inout_       LPD3DXMESH              pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="dadef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dadef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dadef-107">*ПВБ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dadef-107">*pVB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dadef-108">Тип: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span><span class="sxs-lookup"><span data-stu-id="dadef-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span></span>

<span data-ttu-id="dadef-109">Буфер вершин, содержащий данные исправления.</span><span class="sxs-lookup"><span data-stu-id="dadef-109">Vertex buffer containing the patch data.</span></span>

</dd> <dt>

<span data-ttu-id="dadef-110">*пнумсегс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dadef-110">*pNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dadef-111">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="dadef-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dadef-112">Указатель на массив из трех значений с плавающей запятой, определяющих количество сегментов, на которые должно быть разбито каждое из них.</span><span class="sxs-lookup"><span data-stu-id="dadef-112">Pointer to an array of three floating-point values that identify the number of segments into which each edge of the triangle patch should be divided when tessellated.</span></span> <span data-ttu-id="dadef-113">См [**. \_ сведения о D3DTRIPATCH**](d3dtripatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="dadef-113">See [**D3DTRIPATCH\_INFO**](d3dtripatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="dadef-114">*пиндекл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dadef-114">*pInDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dadef-115">Тип: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="dadef-115">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="dadef-116">Структура объявления вершин, определяющая данные вершин.</span><span class="sxs-lookup"><span data-stu-id="dadef-116">Vertex declaration structure that defines the vertex data.</span></span> <span data-ttu-id="dadef-117">См. [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="dadef-117">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="dadef-118">*птрипатчинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dadef-118">*pTriPatchInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dadef-119">Тип: **const [**D3TRIPATCH \_ info**](d3dtripatch-info.md) \***</span><span class="sxs-lookup"><span data-stu-id="dadef-119">Type: **const [**D3TRIPATCH\_INFO**](d3dtripatch-info.md)\***</span></span>

<span data-ttu-id="dadef-120">Описывает исправление треугольника.</span><span class="sxs-lookup"><span data-stu-id="dadef-120">Describes a triangle patch.</span></span> <span data-ttu-id="dadef-121">См [**. \_ сведения о D3DTRIPATCH**](d3dtripatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="dadef-121">See [**D3DTRIPATCH\_INFO**](d3dtripatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="dadef-122">*пмеш* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="dadef-122">*pMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dadef-123">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="dadef-123">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="dadef-124">Указатель на созданную сетку.</span><span class="sxs-lookup"><span data-stu-id="dadef-124">Pointer to the created mesh.</span></span> <span data-ttu-id="dadef-125">См. [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="dadef-125">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dadef-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dadef-126">Return value</span></span>

<span data-ttu-id="dadef-127">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dadef-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dadef-128">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="dadef-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dadef-129">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="dadef-129">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="dadef-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dadef-130">Remarks</span></span>

<span data-ttu-id="dadef-131">Используйте [**D3DXTriPatchSize**](d3dxtripatchsize.md) , чтобы получить количество выходных вершин и индексов, необходимых для функции тесселяции.</span><span class="sxs-lookup"><span data-stu-id="dadef-131">Use [**D3DXTriPatchSize**](d3dxtripatchsize.md) to get the number of output vertices and indices that the tessellation function needs.</span></span>

## <a name="requirements"></a><span data-ttu-id="dadef-132">Требования</span><span class="sxs-lookup"><span data-stu-id="dadef-132">Requirements</span></span>



| <span data-ttu-id="dadef-133">Требование</span><span class="sxs-lookup"><span data-stu-id="dadef-133">Requirement</span></span> | <span data-ttu-id="dadef-134">Значение</span><span class="sxs-lookup"><span data-stu-id="dadef-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dadef-135">Header</span><span class="sxs-lookup"><span data-stu-id="dadef-135">Header</span></span><br/>  | <dl> <span data-ttu-id="dadef-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dadef-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dadef-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dadef-137">Library</span></span><br/> | <dl> <span data-ttu-id="dadef-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dadef-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dadef-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dadef-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dadef-140">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="dadef-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="dadef-141">**D3DXTessellateRectPatch**</span><span class="sxs-lookup"><span data-stu-id="dadef-141">**D3DXTessellateRectPatch**</span></span>](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
