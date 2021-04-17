---
description: Извлекает объявление, описывающее вершины в сетке.
ms.assetid: e9028282-acf1-4ca4-8af0-7fb655dcb5d1
title: Метод ID3DXBaseMesh::-декларация (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 34f8736e822bfe4a959f35f60bb79783e79f2d52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703630"
---
# <a name="id3dxbasemeshgetdeclaration-method"></a><span data-ttu-id="d6762-103">ID3DXBaseMesh:: метод объявления</span><span class="sxs-lookup"><span data-stu-id="d6762-103">ID3DXBaseMesh::GetDeclaration method</span></span>

<span data-ttu-id="d6762-104">Извлекает объявление, описывающее вершины в сетке.</span><span class="sxs-lookup"><span data-stu-id="d6762-104">Retrieves a declaration describing the vertices in the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6762-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6762-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="d6762-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6762-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6762-107">*Объявление* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d6762-107">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6762-108">Тип: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="d6762-108">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="d6762-109">Массив элементов [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , описывающих формат вершин вершин сетки.</span><span class="sxs-lookup"><span data-stu-id="d6762-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="d6762-110">Верхний предел этого массива декларатора — [**Max \_ фвф \_ DECL \_ size**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="d6762-110">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="d6762-111">Массив элементов вершин заканчивается макросом [**D3DDECL \_ End**](d3ddecl-end.md) .</span><span class="sxs-lookup"><span data-stu-id="d6762-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6762-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6762-112">Return value</span></span>

<span data-ttu-id="d6762-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d6762-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d6762-114">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d6762-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d6762-115">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="d6762-115">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6762-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d6762-116">Remarks</span></span>

<span data-ttu-id="d6762-117">Массив элементов включает макрос [**D3DDECL \_ End**](d3ddecl-end.md) , который завершает объявление.</span><span class="sxs-lookup"><span data-stu-id="d6762-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6762-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d6762-118">Requirements</span></span>



| <span data-ttu-id="d6762-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d6762-119">Requirement</span></span> | <span data-ttu-id="d6762-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d6762-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6762-121">Header</span><span class="sxs-lookup"><span data-stu-id="d6762-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d6762-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6762-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d6762-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d6762-123">Library</span></span><br/> | <dl> <span data-ttu-id="d6762-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6762-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d6762-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6762-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6762-126">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="d6762-126">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
