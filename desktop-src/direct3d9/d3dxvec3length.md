---
description: Возвращает длину трехмерного вектора.
ms.assetid: 78da506c-3169-48e9-934c-cc09271a10d4
title: Функция D3DXVec3Length (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Length
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 653e53fb22961c858c7649f95e4453fec08087fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703718"
---
# <a name="d3dxvec3length-function"></a><span data-ttu-id="009e0-103">Функция D3DXVec3Length</span><span class="sxs-lookup"><span data-stu-id="009e0-103">D3DXVec3Length function</span></span>

<span data-ttu-id="009e0-104">Возвращает длину трехмерного вектора.</span><span class="sxs-lookup"><span data-stu-id="009e0-104">Returns the length of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="009e0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="009e0-105">Syntax</span></span>


```C++
FLOAT D3DXVec3Length(
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="009e0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="009e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="009e0-107">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="009e0-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="009e0-108">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="009e0-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="009e0-109">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="009e0-109">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="009e0-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="009e0-110">Return value</span></span>

<span data-ttu-id="009e0-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="009e0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="009e0-112">Длина вектора.</span><span class="sxs-lookup"><span data-stu-id="009e0-112">The vector's length.</span></span>

## <a name="requirements"></a><span data-ttu-id="009e0-113">Требования</span><span class="sxs-lookup"><span data-stu-id="009e0-113">Requirements</span></span>



| <span data-ttu-id="009e0-114">Требование</span><span class="sxs-lookup"><span data-stu-id="009e0-114">Requirement</span></span> | <span data-ttu-id="009e0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="009e0-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="009e0-116">Header</span><span class="sxs-lookup"><span data-stu-id="009e0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="009e0-117"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="009e0-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="009e0-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="009e0-118">Library</span></span><br/> | <dl> <span data-ttu-id="009e0-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="009e0-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="009e0-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="009e0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="009e0-121">Математические функции</span><span class="sxs-lookup"><span data-stu-id="009e0-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="009e0-122">**D3DXVec3LengthSq**</span><span class="sxs-lookup"><span data-stu-id="009e0-122">**D3DXVec3LengthSq**</span></span>](d3dxvec3lengthsq.md)
</dt> </dl>

 

 
