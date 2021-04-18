---
description: Возвращает размер исправления треугольника.
ms.assetid: 3bfbed4c-59af-43eb-a462-478e89cfe9ae
title: Функция D3DXTriPatchSize (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTriPatchSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5ee254b12485153f4d5c5ba0843189399d1aed0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713632"
---
# <a name="d3dxtripatchsize-function"></a><span data-ttu-id="17823-103">Функция D3DXTriPatchSize</span><span class="sxs-lookup"><span data-stu-id="17823-103">D3DXTriPatchSize function</span></span>

<span data-ttu-id="17823-104">Возвращает размер исправления треугольника.</span><span class="sxs-lookup"><span data-stu-id="17823-104">Gets the size of the triangle patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="17823-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17823-105">Syntax</span></span>


```C++
HRESULT D3DXTriPatchSize(
  _In_  const FLOAT *pfNumSegs,
  _Out_       DWORD *pdwTriangles,
  _Out_       DWORD *pdwVertices
);
```



## <a name="parameters"></a><span data-ttu-id="17823-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="17823-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17823-107">*пфнумсегс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17823-107">*pfNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17823-108">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="17823-108">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="17823-109">Число сегментов на границе для тесселяции.</span><span class="sxs-lookup"><span data-stu-id="17823-109">Number of segments per edge to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="17823-110">*пдвтрианглес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="17823-110">*pdwTriangles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17823-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="17823-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="17823-112">Указатель на DWORD, содержащий число треугольников в исправлении.</span><span class="sxs-lookup"><span data-stu-id="17823-112">Pointer to a DWORD that contains the number of triangles in the patch.</span></span>

</dd> <dt>

<span data-ttu-id="17823-113">*пдввертицес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="17823-113">*pdwVertices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17823-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="17823-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="17823-115">Указатель на DWORD, содержащий число вершин в исправлении треугольника.</span><span class="sxs-lookup"><span data-stu-id="17823-115">Pointer to a DWORD that contains the number of vertices in the triangle patch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17823-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17823-116">Return value</span></span>

<span data-ttu-id="17823-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="17823-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="17823-118">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="17823-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="17823-119">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="17823-119">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="17823-120">Требования</span><span class="sxs-lookup"><span data-stu-id="17823-120">Requirements</span></span>



| <span data-ttu-id="17823-121">Требование</span><span class="sxs-lookup"><span data-stu-id="17823-121">Requirement</span></span> | <span data-ttu-id="17823-122">Значение</span><span class="sxs-lookup"><span data-stu-id="17823-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17823-123">Header</span><span class="sxs-lookup"><span data-stu-id="17823-123">Header</span></span><br/>  | <dl> <span data-ttu-id="17823-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="17823-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="17823-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="17823-125">Library</span></span><br/> | <dl> <span data-ttu-id="17823-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17823-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="17823-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17823-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17823-128">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="17823-128">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="17823-129">**D3DXTessellateTriPatch**</span><span class="sxs-lookup"><span data-stu-id="17823-129">**D3DXTessellateTriPatch**</span></span>](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
