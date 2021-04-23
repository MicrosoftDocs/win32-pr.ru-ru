---
description: Возвращает квадрат длины трехмерного вектора.
ms.assetid: 25dc50cc-542b-4989-a858-9b37603393a0
title: Функция D3DXVec3LengthSq (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3LengthSq
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7bb7d17d4f1bc06d68a73a2cff9288d159381387
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694328"
---
# <a name="d3dxvec3lengthsq-function"></a><span data-ttu-id="e4563-103">Функция D3DXVec3LengthSq</span><span class="sxs-lookup"><span data-stu-id="e4563-103">D3DXVec3LengthSq function</span></span>

<span data-ttu-id="e4563-104">Возвращает квадрат длины трехмерного вектора.</span><span class="sxs-lookup"><span data-stu-id="e4563-104">Returns the square of the length of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4563-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4563-105">Syntax</span></span>


```C++
FLOAT D3DXVec3LengthSq(
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="e4563-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4563-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4563-107">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e4563-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4563-108">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4563-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e4563-109">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="e4563-109">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4563-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4563-110">Return value</span></span>

<span data-ttu-id="e4563-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4563-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4563-112">Длина квадрата вектора.</span><span class="sxs-lookup"><span data-stu-id="e4563-112">The vector's squared length.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4563-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e4563-113">Requirements</span></span>



| <span data-ttu-id="e4563-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e4563-114">Requirement</span></span> | <span data-ttu-id="e4563-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e4563-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4563-116">Header</span><span class="sxs-lookup"><span data-stu-id="e4563-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e4563-117"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4563-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e4563-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e4563-118">Library</span></span><br/> | <dl> <span data-ttu-id="e4563-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4563-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e4563-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4563-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4563-121">Математические функции</span><span class="sxs-lookup"><span data-stu-id="e4563-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e4563-122">**D3DXVec3Length**</span><span class="sxs-lookup"><span data-stu-id="e4563-122">**D3DXVec3Length**</span></span>](d3dxvec3length.md)
</dt> </dl>

 

 
