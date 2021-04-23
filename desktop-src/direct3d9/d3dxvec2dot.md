---
description: Определяет скалярное произведение двух двумерных векторов.
ms.assetid: ae77ff29-44be-4b67-9c63-aaffa4fe8d59
title: Функция D3DXVec2Dot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 79b65127c415695b3df9f927b6edff8fcdd5c58d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703724"
---
# <a name="d3dxvec2dot-function"></a><span data-ttu-id="4c2e2-103">Функция D3DXVec2Dot</span><span class="sxs-lookup"><span data-stu-id="4c2e2-103">D3DXVec2Dot function</span></span>

<span data-ttu-id="4c2e2-104">Определяет скалярное произведение двух двумерных векторов.</span><span class="sxs-lookup"><span data-stu-id="4c2e2-104">Determines the dot product of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c2e2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c2e2-105">Syntax</span></span>


```C++
FLOAT D3DXVec2Dot(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="4c2e2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c2e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c2e2-107">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c2e2-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c2e2-108">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="4c2e2-108">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="4c2e2-109">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="4c2e2-109">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4c2e2-110">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c2e2-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c2e2-111">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="4c2e2-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="4c2e2-112">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="4c2e2-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c2e2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c2e2-113">Return value</span></span>

<span data-ttu-id="4c2e2-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c2e2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4c2e2-115">Скалярное произведение.</span><span class="sxs-lookup"><span data-stu-id="4c2e2-115">The dot product.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c2e2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4c2e2-116">Requirements</span></span>



| <span data-ttu-id="4c2e2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4c2e2-117">Requirement</span></span> | <span data-ttu-id="4c2e2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4c2e2-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c2e2-119">Header</span><span class="sxs-lookup"><span data-stu-id="4c2e2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4c2e2-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c2e2-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4c2e2-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4c2e2-121">Library</span></span><br/> | <dl> <span data-ttu-id="4c2e2-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c2e2-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4c2e2-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c2e2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c2e2-124">Математические функции</span><span class="sxs-lookup"><span data-stu-id="4c2e2-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4c2e2-125">**D3DXVec2CCW**</span><span class="sxs-lookup"><span data-stu-id="4c2e2-125">**D3DXVec2CCW**</span></span>](d3dxvec2ccw.md)
</dt> </dl>

 

 
