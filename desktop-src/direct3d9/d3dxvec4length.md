---
description: Возвращает длину вектора 4D.
ms.assetid: cb332160-3e3d-41b9-bfb0-e3b743d2eafd
title: Функция D3DXVec4Length (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Length
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3ea16c6406c217f5e5d76af68a5da3a0c8bd17b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000534"
---
# <a name="d3dxvec4length-function"></a><span data-ttu-id="87798-103">Функция D3DXVec4Length</span><span class="sxs-lookup"><span data-stu-id="87798-103">D3DXVec4Length function</span></span>

<span data-ttu-id="87798-104">Возвращает длину вектора 4D.</span><span class="sxs-lookup"><span data-stu-id="87798-104">Returns the length of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="87798-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87798-105">Syntax</span></span>


```C++
FLOAT D3DXVec4Length(
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="87798-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="87798-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87798-107">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87798-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87798-108">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="87798-108">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="87798-109">Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="87798-109">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87798-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87798-110">Return value</span></span>

<span data-ttu-id="87798-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87798-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87798-112">Длина вектора.</span><span class="sxs-lookup"><span data-stu-id="87798-112">The vector's length.</span></span>

## <a name="requirements"></a><span data-ttu-id="87798-113">Требования</span><span class="sxs-lookup"><span data-stu-id="87798-113">Requirements</span></span>



| <span data-ttu-id="87798-114">Требование</span><span class="sxs-lookup"><span data-stu-id="87798-114">Requirement</span></span> | <span data-ttu-id="87798-115">Значение</span><span class="sxs-lookup"><span data-stu-id="87798-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87798-116">Header</span><span class="sxs-lookup"><span data-stu-id="87798-116">Header</span></span><br/>  | <dl> <span data-ttu-id="87798-117"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="87798-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="87798-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="87798-118">Library</span></span><br/> | <dl> <span data-ttu-id="87798-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87798-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="87798-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87798-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87798-121">Математические функции</span><span class="sxs-lookup"><span data-stu-id="87798-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="87798-122">**D3DXVec4LengthSq**</span><span class="sxs-lookup"><span data-stu-id="87798-122">**D3DXVec4LengthSq**</span></span>](d3dxvec4lengthsq.md)
</dt> </dl>

 

 
