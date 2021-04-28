---
description: Метод ID3DXPatchMesh::-Декларация Возвращает объявление вершины.
ms.assetid: 53ff2fb5-68b6-4edd-b48f-e06df306ee3f
title: Метод ID3DXPatchMesh::-декларация (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0fde070b1b013e651c84ffea7098eb8225aed8f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093302"
---
# <a name="id3dxpatchmeshgetdeclaration-method"></a><span data-ttu-id="56590-103">ID3DXPatchMesh:: метод объявления</span><span class="sxs-lookup"><span data-stu-id="56590-103">ID3DXPatchMesh::GetDeclaration method</span></span>

<span data-ttu-id="56590-104">Возвращает объявление вершины.</span><span class="sxs-lookup"><span data-stu-id="56590-104">Gets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="56590-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56590-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [out] LPD3DVERTEXELEMENT9 pDeclaration
);
```



## <a name="parameters"></a><span data-ttu-id="56590-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="56590-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56590-107">*пдекларатион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="56590-107">*pDeclaration* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56590-108">Тип: **[ **LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="56590-108">Type: **[**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="56590-109">Массив элементов [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , описывающих формат вершин вершин сетки.</span><span class="sxs-lookup"><span data-stu-id="56590-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="56590-110">Измерение этого массива деклараторов является [**максимальным \_ \_ \_ размером фвф DECL**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="56590-110">The dimension of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="56590-111">Массив элементов вершин заканчивается макросом [**D3DDECL \_ End**](d3ddecl-end.md) .</span><span class="sxs-lookup"><span data-stu-id="56590-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56590-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56590-112">Return value</span></span>

<span data-ttu-id="56590-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="56590-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="56590-114">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="56590-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="56590-115">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="56590-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="56590-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="56590-116">Remarks</span></span>

<span data-ttu-id="56590-117">Массив элементов включает макрос [**D3DDECL \_ End**](d3ddecl-end.md) , который завершает объявление.</span><span class="sxs-lookup"><span data-stu-id="56590-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="56590-118">Требования</span><span class="sxs-lookup"><span data-stu-id="56590-118">Requirements</span></span>



| <span data-ttu-id="56590-119">Требование</span><span class="sxs-lookup"><span data-stu-id="56590-119">Requirement</span></span> | <span data-ttu-id="56590-120">Значение</span><span class="sxs-lookup"><span data-stu-id="56590-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56590-121">Header</span><span class="sxs-lookup"><span data-stu-id="56590-121">Header</span></span><br/>  | <dl> <span data-ttu-id="56590-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="56590-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="56590-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="56590-123">Library</span></span><br/> | <dl> <span data-ttu-id="56590-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56590-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="56590-125">См. также</span><span class="sxs-lookup"><span data-stu-id="56590-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56590-126">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="56590-126">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
