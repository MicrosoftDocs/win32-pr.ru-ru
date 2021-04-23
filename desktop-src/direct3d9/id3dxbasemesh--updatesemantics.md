---
description: Этот метод позволяет пользователю изменить объявление сетки, не изменяя макет данных в буфере вершин. Вызов допустим только в том случае, если форматы старого и нового объявлений имеют одинаковый размер вершины.
ms.assetid: ed2ad479-e0f7-4580-a20a-d3649759876a
title: 'Метод ID3DXBaseMesh:: Упдатесемантикс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.UpdateSemantics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e31a6fe424d085467bfa795c7ce7b2d445a1f69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081877"
---
# <a name="id3dxbasemeshupdatesemantics-method"></a><span data-ttu-id="e8fe2-104">Метод ID3DXBaseMesh:: Упдатесемантикс</span><span class="sxs-lookup"><span data-stu-id="e8fe2-104">ID3DXBaseMesh::UpdateSemantics method</span></span>

<span data-ttu-id="e8fe2-105">Этот метод позволяет пользователю изменить объявление сетки, не изменяя макет данных в буфере вершин.</span><span class="sxs-lookup"><span data-stu-id="e8fe2-105">This method allows the user to change the mesh declaration without changing the data layout of the vertex buffer.</span></span> <span data-ttu-id="e8fe2-106">Вызов допустим только в том случае, если форматы старого и нового объявлений имеют одинаковый размер вершины.</span><span class="sxs-lookup"><span data-stu-id="e8fe2-106">The call is valid only if the old and new declaration formats have the same vertex size.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8fe2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8fe2-107">Syntax</span></span>


```C++
HRESULT UpdateSemantics(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="e8fe2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8fe2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8fe2-109">*Объявление* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e8fe2-109">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8fe2-110">Тип: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="e8fe2-110">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="e8fe2-111">Массив элементов [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , описывающих формат вершин вершин сетки.</span><span class="sxs-lookup"><span data-stu-id="e8fe2-111">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="e8fe2-112">Верхний предел этого массива декларатора — [**Max \_ фвф \_ DECL \_ size**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="e8fe2-112">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8fe2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8fe2-113">Return value</span></span>

<span data-ttu-id="e8fe2-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e8fe2-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e8fe2-115">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e8fe2-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e8fe2-116">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="e8fe2-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8fe2-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8fe2-117">Remarks</span></span>

<span data-ttu-id="e8fe2-118">[**ID3DXBaseMesh:: клонемеш**](id3dxbasemesh--clonemesh.md) используется для переформатирования и изменения макета данных вершин.</span><span class="sxs-lookup"><span data-stu-id="e8fe2-118">[**ID3DXBaseMesh::CloneMesh**](id3dxbasemesh--clonemesh.md) is used to reformat and change the vertex data layout.</span></span> <span data-ttu-id="e8fe2-119">Например, используйте его для добавления пространства для нормалей, текстурных координат, цветов, весов и т. д., которые отсутствовали ранее.</span><span class="sxs-lookup"><span data-stu-id="e8fe2-119">For example, use it to to add space for normals, texture coordinates, colors, weights, etc. that were not present before.</span></span>

<span data-ttu-id="e8fe2-120">**ID3DXBaseMesh:: упдатесемантикс** — это метод обновления объявления вершины с другой семантической информацией без изменения макета буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="e8fe2-120">**ID3DXBaseMesh::UpdateSemantics** is a method for updating the vertex declaration with different semantic information, without changing the layout of the vertex buffer.</span></span> <span data-ttu-id="e8fe2-121">Например, используйте его для переметки координаты трехмерной текстуры как бинормал или тангенса или наоборот.</span><span class="sxs-lookup"><span data-stu-id="e8fe2-121">For example, use it to relabel a 3D texture coordinate as a binormal or tangent, or vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8fe2-122">Требования</span><span class="sxs-lookup"><span data-stu-id="e8fe2-122">Requirements</span></span>



| <span data-ttu-id="e8fe2-123">Требование</span><span class="sxs-lookup"><span data-stu-id="e8fe2-123">Requirement</span></span> | <span data-ttu-id="e8fe2-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e8fe2-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8fe2-125">Header</span><span class="sxs-lookup"><span data-stu-id="e8fe2-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e8fe2-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8fe2-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e8fe2-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e8fe2-127">Library</span></span><br/> | <dl> <span data-ttu-id="e8fe2-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8fe2-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e8fe2-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8fe2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8fe2-130">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="e8fe2-130">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="e8fe2-131">**ID3DXBaseMesh:: Клонемешфвф**</span><span class="sxs-lookup"><span data-stu-id="e8fe2-131">**ID3DXBaseMesh::CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[<span data-ttu-id="e8fe2-132">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="e8fe2-132">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
