---
description: Преобразует данные репрезентативного указания в сведения о смежности сетки.
ms.assetid: 6ae40486-74be-45a8-9971-f20517c8dcf0
title: 'Метод ID3DXBaseMesh:: Конвертпоинтрепстоаджаценци (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertPointRepsToAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b1c38d7790d575bdf6794e0e21f1c4043e80257c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703758"
---
# <a name="id3dxbasemeshconvertpointrepstoadjacency-method"></a><span data-ttu-id="5087e-103">Метод ID3DXBaseMesh:: Конвертпоинтрепстоаджаценци</span><span class="sxs-lookup"><span data-stu-id="5087e-103">ID3DXBaseMesh::ConvertPointRepsToAdjacency method</span></span>

<span data-ttu-id="5087e-104">Преобразует данные репрезентативного указания в сведения о смежности сетки.</span><span class="sxs-lookup"><span data-stu-id="5087e-104">Converts point representative data to mesh adjacency information.</span></span>

## <a name="syntax"></a><span data-ttu-id="5087e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5087e-105">Syntax</span></span>


```C++
HRESULT ConvertPointRepsToAdjacency(
  [in]      const DWORD *pPRep,
  [in, out]       DWORD *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="5087e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5087e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5087e-107">*ппреп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5087e-107">*pPRep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5087e-108">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="5087e-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5087e-109">Указатель на массив из одного DWORD на вершину сетки, которая содержит данные репрезентативного указания.</span><span class="sxs-lookup"><span data-stu-id="5087e-109">Pointer to an array of one DWORD per vertex of the mesh that contains point representative data.</span></span> <span data-ttu-id="5087e-110">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="5087e-110">This parameter is optional.</span></span> <span data-ttu-id="5087e-111">Если указать значение **null** , этот параметр будет интерпретирован как массив "Identity".</span><span class="sxs-lookup"><span data-stu-id="5087e-111">Supplying a **NULL** value will cause this parameter to be interpreted as an "identity" array.</span></span>

</dd> <dt>

<span data-ttu-id="5087e-112">*паджаценци* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="5087e-112">*pAdjacency* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5087e-113">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5087e-113">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5087e-114">Указатель на массив из трех DWORD на грань, который указывает три соседа для каждой грани в сети.</span><span class="sxs-lookup"><span data-stu-id="5087e-114">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="5087e-115">Число байтов в этом массиве должно быть не менее 3 \* [**ID3DXBaseMesh:: жетнумфацес**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).</span><span class="sxs-lookup"><span data-stu-id="5087e-115">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5087e-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5087e-116">Return value</span></span>

<span data-ttu-id="5087e-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5087e-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5087e-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="5087e-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5087e-119">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5087e-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="5087e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="5087e-120">Requirements</span></span>



| <span data-ttu-id="5087e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="5087e-121">Requirement</span></span> | <span data-ttu-id="5087e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="5087e-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5087e-123">Header</span><span class="sxs-lookup"><span data-stu-id="5087e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5087e-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5087e-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5087e-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5087e-125">Library</span></span><br/> | <dl> <span data-ttu-id="5087e-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5087e-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5087e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5087e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5087e-128">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="5087e-128">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
