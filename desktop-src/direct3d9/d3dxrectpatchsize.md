---
description: Возвращает размер обновления прямоугольника.
ms.assetid: d25373ef-789d-4515-83da-7049f040c9a4
title: Функция D3DXRectPatchSize (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRectPatchSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5770e05493164db9da75fb38fa1e41594bfae8f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105684986"
---
# <a name="d3dxrectpatchsize-function"></a><span data-ttu-id="610bb-103">Функция D3DXRectPatchSize</span><span class="sxs-lookup"><span data-stu-id="610bb-103">D3DXRectPatchSize function</span></span>

<span data-ttu-id="610bb-104">Возвращает размер обновления прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="610bb-104">Gets the size of the rectangle patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="610bb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="610bb-105">Syntax</span></span>


```C++
HRESULT D3DXRectPatchSize(
  _In_  const FLOAT *pfNumSegs,
  _Out_       DWORD *pdwTriangles,
  _Out_       DWORD *pwdVertices
);
```



## <a name="parameters"></a><span data-ttu-id="610bb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="610bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="610bb-107">*пфнумсегс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="610bb-107">*pfNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="610bb-108">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="610bb-108">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="610bb-109">Число сегментов на границе для тесселяции.</span><span class="sxs-lookup"><span data-stu-id="610bb-109">Number of segments per edge to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="610bb-110">*пдвтрианглес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="610bb-110">*pdwTriangles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="610bb-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="610bb-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="610bb-112">Указатель на DWORD, содержащий число треугольников в исправлении.</span><span class="sxs-lookup"><span data-stu-id="610bb-112">Pointer to a DWORD that contains the number of triangles in the patch.</span></span>

</dd> <dt>

<span data-ttu-id="610bb-113">*пвдвертицес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="610bb-113">*pwdVertices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="610bb-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="610bb-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="610bb-115">Указатель на DWORD, содержащий количество вершин в исправлении.</span><span class="sxs-lookup"><span data-stu-id="610bb-115">Pointer to a DWORD that contains the number of vertices in the patch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="610bb-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="610bb-116">Return value</span></span>

<span data-ttu-id="610bb-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="610bb-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="610bb-118">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="610bb-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="610bb-119">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="610bb-119">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="610bb-120">Требования</span><span class="sxs-lookup"><span data-stu-id="610bb-120">Requirements</span></span>



| <span data-ttu-id="610bb-121">Требование</span><span class="sxs-lookup"><span data-stu-id="610bb-121">Requirement</span></span> | <span data-ttu-id="610bb-122">Значение</span><span class="sxs-lookup"><span data-stu-id="610bb-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="610bb-123">Header</span><span class="sxs-lookup"><span data-stu-id="610bb-123">Header</span></span><br/>  | <dl> <span data-ttu-id="610bb-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="610bb-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="610bb-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="610bb-125">Library</span></span><br/> | <dl> <span data-ttu-id="610bb-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="610bb-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="610bb-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="610bb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="610bb-128">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="610bb-128">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="610bb-129">**D3DXTessellateRectPatch**</span><span class="sxs-lookup"><span data-stu-id="610bb-129">**D3DXTessellateRectPatch**</span></span>](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
