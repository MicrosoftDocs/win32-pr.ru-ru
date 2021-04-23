---
description: Определяет скалярное произведение двух трехмерных векторов.
ms.assetid: 61aa7751-cc06-4673-929b-d7c1e691e395
title: Функция D3DXVec3Dot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 22d6930a44f129154482f9b1aab24337e8bcdc83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703777"
---
# <a name="d3dxvec3dot-function"></a><span data-ttu-id="e6edb-103">Функция D3DXVec3Dot</span><span class="sxs-lookup"><span data-stu-id="e6edb-103">D3DXVec3Dot function</span></span>

<span data-ttu-id="e6edb-104">Определяет скалярное произведение двух трехмерных векторов.</span><span class="sxs-lookup"><span data-stu-id="e6edb-104">Determines the dot product of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6edb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6edb-105">Syntax</span></span>


```C++
FLOAT D3DXVec3Dot(
  _In_ const D3DXVECTOR3 *pV1,
  _In_ const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="e6edb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6edb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6edb-107">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6edb-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6edb-108">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e6edb-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e6edb-109">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="e6edb-109">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e6edb-110">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6edb-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6edb-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e6edb-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e6edb-112">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="e6edb-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6edb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6edb-113">Return value</span></span>

<span data-ttu-id="e6edb-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6edb-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e6edb-115">Точка-произведение.</span><span class="sxs-lookup"><span data-stu-id="e6edb-115">The dot-product.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6edb-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e6edb-116">Requirements</span></span>



| <span data-ttu-id="e6edb-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e6edb-117">Requirement</span></span> | <span data-ttu-id="e6edb-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e6edb-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6edb-119">Header</span><span class="sxs-lookup"><span data-stu-id="e6edb-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e6edb-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6edb-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e6edb-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e6edb-121">Library</span></span><br/> | <dl> <span data-ttu-id="e6edb-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6edb-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e6edb-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6edb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6edb-124">Математические функции</span><span class="sxs-lookup"><span data-stu-id="e6edb-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e6edb-125">**D3DXVec3Cross**</span><span class="sxs-lookup"><span data-stu-id="e6edb-125">**D3DXVec3Cross**</span></span>](d3dxvec3cross.md)
</dt> </dl>

 

 
