---
description: Возвращает длину кватерниона.
ms.assetid: daa835c2-2370-4427-a4ca-eddfb43d5c67
title: Функция D3DXQuaternionLength (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLength
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7f54136e7e34ba05442f98b25438dd03b7b5f211
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424481"
---
# <a name="d3dxquaternionlength-function"></a><span data-ttu-id="d8503-103">Функция D3DXQuaternionLength</span><span class="sxs-lookup"><span data-stu-id="d8503-103">D3DXQuaternionLength function</span></span>

<span data-ttu-id="d8503-104">Возвращает длину кватерниона.</span><span class="sxs-lookup"><span data-stu-id="d8503-104">Returns the length of a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8503-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8503-105">Syntax</span></span>


```C++
FLOAT D3DXQuaternionLength(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="d8503-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8503-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8503-107">*pQ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8503-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8503-108">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d8503-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d8503-109">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="d8503-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8503-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8503-110">Return value</span></span>

<span data-ttu-id="d8503-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8503-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8503-112">Длина кватерниона.</span><span class="sxs-lookup"><span data-stu-id="d8503-112">The quaternion's length.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8503-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8503-113">Remarks</span></span>

<span data-ttu-id="d8503-114">Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="d8503-114">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8503-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d8503-115">Requirements</span></span>



| <span data-ttu-id="d8503-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d8503-116">Requirement</span></span> | <span data-ttu-id="d8503-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d8503-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8503-118">Header</span><span class="sxs-lookup"><span data-stu-id="d8503-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d8503-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8503-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d8503-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d8503-120">Library</span></span><br/> | <dl> <span data-ttu-id="d8503-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8503-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d8503-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8503-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8503-123">Математические функции</span><span class="sxs-lookup"><span data-stu-id="d8503-123">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d8503-124">**D3DXQuaternionLengthSq**</span><span class="sxs-lookup"><span data-stu-id="d8503-124">**D3DXQuaternionLengthSq**</span></span>](d3dxquaternionlengthsq.md)
</dt> </dl>

 

 
