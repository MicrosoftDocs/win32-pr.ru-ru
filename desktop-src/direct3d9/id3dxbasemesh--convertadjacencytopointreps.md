---
description: Преобразует сведения о смежности сетки в массив точек зрения.
ms.assetid: b8914f9c-8550-498d-813d-bb1afe0fb5b2
title: 'Метод ID3DXBaseMesh:: Конвертаджаценцитопоинтрепс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertAdjacencyToPointReps
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3a4827473cce115f742a85b99732d09a2c5efa4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273753"
---
# <a name="id3dxbasemeshconvertadjacencytopointreps-method"></a><span data-ttu-id="42d0f-103">Метод ID3DXBaseMesh:: Конвертаджаценцитопоинтрепс</span><span class="sxs-lookup"><span data-stu-id="42d0f-103">ID3DXBaseMesh::ConvertAdjacencyToPointReps method</span></span>

<span data-ttu-id="42d0f-104">Преобразует сведения о смежности сетки в массив точек зрения.</span><span class="sxs-lookup"><span data-stu-id="42d0f-104">Converts mesh adjacency information to an array of point representatives.</span></span>

## <a name="syntax"></a><span data-ttu-id="42d0f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42d0f-105">Syntax</span></span>


```C++
HRESULT ConvertAdjacencyToPointReps(
  [in]      const DWORD *pAdjacency,
  [in, out]       DWORD *pPRep
);
```



## <a name="parameters"></a><span data-ttu-id="42d0f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42d0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42d0f-107">*паджаценци* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42d0f-107">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42d0f-108">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="42d0f-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="42d0f-109">Указатель на массив из трех DWORD на грань, который указывает три соседа для каждой грани в сети.</span><span class="sxs-lookup"><span data-stu-id="42d0f-109">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="42d0f-110">Число байтов в этом массиве должно быть не менее 3 \* [**ID3DXBaseMesh:: жетнумфацес**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).</span><span class="sxs-lookup"><span data-stu-id="42d0f-110">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> <dt>

<span data-ttu-id="42d0f-111">*ппреп* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="42d0f-111">*pPRep* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="42d0f-112">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="42d0f-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="42d0f-113">Указатель на массив из одного DWORD на вершину сетки, которая будет заполнена данными репрезентативной точки.</span><span class="sxs-lookup"><span data-stu-id="42d0f-113">Pointer to an array of one DWORD per vertex of the mesh that will be filled with point representative data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42d0f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42d0f-114">Return value</span></span>

<span data-ttu-id="42d0f-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="42d0f-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="42d0f-116">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="42d0f-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="42d0f-117">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="42d0f-117">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="42d0f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="42d0f-118">Requirements</span></span>



| <span data-ttu-id="42d0f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="42d0f-119">Requirement</span></span> | <span data-ttu-id="42d0f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="42d0f-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42d0f-121">Header</span><span class="sxs-lookup"><span data-stu-id="42d0f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="42d0f-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="42d0f-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="42d0f-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="42d0f-123">Library</span></span><br/> | <dl> <span data-ttu-id="42d0f-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42d0f-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="42d0f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42d0f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42d0f-126">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="42d0f-126">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
