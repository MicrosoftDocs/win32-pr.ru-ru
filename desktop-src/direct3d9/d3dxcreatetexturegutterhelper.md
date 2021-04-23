---
description: Создает объект ID3DXTextureGutterHelper из входной сетки и данных текстуры.
ms.assetid: 1696fc3d-5b35-48cc-a79b-c0d4ed44e420
title: Функция D3DXCreateTextureGutterHelper (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureGutterHelper
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8957649f3cef6ea67932579918163613160ee993
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703797"
---
# <a name="d3dxcreatetexturegutterhelper-function"></a><span data-ttu-id="59b8e-103">Функция D3DXCreateTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="59b8e-103">D3DXCreateTextureGutterHelper function</span></span>

<span data-ttu-id="59b8e-104">Создает объект [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) из входной сетки и данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="59b8e-104">Creates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object from an input mesh and texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="59b8e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59b8e-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureGutterHelper(
  _In_    UINT                      Width,
  _In_    UINT                      Height,
  _In_    LPD3DXMESH                pMesh,
  _In_    FLOAT                     GutterSize,
  _Inout_ LPD3DXTEXTUREGUTTERHELPER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="59b8e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="59b8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59b8e-107">*Ширина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59b8e-107">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b8e-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59b8e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59b8e-109">Ширина текстуры в пикселях.</span><span class="sxs-lookup"><span data-stu-id="59b8e-109">Width of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="59b8e-110">*Высота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59b8e-110">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b8e-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59b8e-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59b8e-112">Высота текстуры (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="59b8e-112">Height of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="59b8e-113">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59b8e-113">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b8e-114">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="59b8e-114">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="59b8e-115">Указатель на входной объект сетки [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="59b8e-115">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="59b8e-116">*Гуттерсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59b8e-116">*GutterSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b8e-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59b8e-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59b8e-118">Число пикселей текстуры, на которое будет перевышена текстура и создана область переплета.</span><span class="sxs-lookup"><span data-stu-id="59b8e-118">Number of texels by which to over-sample the texture and create the gutter region.</span></span> <span data-ttu-id="59b8e-119">Должно быть не менее 1.</span><span class="sxs-lookup"><span data-stu-id="59b8e-119">Must be at least 1.</span></span>

</dd> <dt>

<span data-ttu-id="59b8e-120">*ппбуффер* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="59b8e-120">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="59b8e-121">Тип: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***</span><span class="sxs-lookup"><span data-stu-id="59b8e-121">Type: **[**LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***</span></span>

<span data-ttu-id="59b8e-122">Указатель на объект [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) , который необходимо создать.</span><span class="sxs-lookup"><span data-stu-id="59b8e-122">Pointer to an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59b8e-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59b8e-123">Return value</span></span>

<span data-ttu-id="59b8e-124">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="59b8e-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="59b8e-125">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="59b8e-125">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="59b8e-126">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="59b8e-126">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="59b8e-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59b8e-127">Remarks</span></span>

<span data-ttu-id="59b8e-128">Используйте [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) для преобразования сцены в новые координаты.</span><span class="sxs-lookup"><span data-stu-id="59b8e-128">Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) to transform a scene to new coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="59b8e-129">Требования</span><span class="sxs-lookup"><span data-stu-id="59b8e-129">Requirements</span></span>



| <span data-ttu-id="59b8e-130">Требование</span><span class="sxs-lookup"><span data-stu-id="59b8e-130">Requirement</span></span> | <span data-ttu-id="59b8e-131">Значение</span><span class="sxs-lookup"><span data-stu-id="59b8e-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59b8e-132">Header</span><span class="sxs-lookup"><span data-stu-id="59b8e-132">Header</span></span><br/>  | <dl> <span data-ttu-id="59b8e-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="59b8e-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="59b8e-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="59b8e-134">Library</span></span><br/> | <dl> <span data-ttu-id="59b8e-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59b8e-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="59b8e-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59b8e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59b8e-137">Предварительно вычисленные функции пересылки Радианце</span><span class="sxs-lookup"><span data-stu-id="59b8e-137">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
