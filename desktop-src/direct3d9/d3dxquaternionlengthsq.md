---
description: Возвращает квадрат длины кватерниона.
ms.assetid: 358d2a2b-7baf-4ae9-9b92-7a7f01ca843b
title: Функция D3DXQuaternionLengthSq (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLengthSq
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0771d571b15ef690b115f12e5fa1d8ff6fea4dad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713903"
---
# <a name="d3dxquaternionlengthsq-function"></a><span data-ttu-id="82f9d-103">Функция D3DXQuaternionLengthSq</span><span class="sxs-lookup"><span data-stu-id="82f9d-103">D3DXQuaternionLengthSq function</span></span>

<span data-ttu-id="82f9d-104">Возвращает квадрат длины кватерниона.</span><span class="sxs-lookup"><span data-stu-id="82f9d-104">Returns the square of the length of a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="82f9d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82f9d-105">Syntax</span></span>


```C++
FLOAT D3DXQuaternionLengthSq(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="82f9d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="82f9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82f9d-107">*pQ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="82f9d-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82f9d-108">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="82f9d-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="82f9d-109">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="82f9d-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82f9d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82f9d-110">Return value</span></span>

<span data-ttu-id="82f9d-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82f9d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82f9d-112">Длина квадрата кватерниона.</span><span class="sxs-lookup"><span data-stu-id="82f9d-112">The quaternion's squared length.</span></span>

## <a name="remarks"></a><span data-ttu-id="82f9d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82f9d-113">Remarks</span></span>

<span data-ttu-id="82f9d-114">Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="82f9d-114">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="82f9d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="82f9d-115">Requirements</span></span>



| <span data-ttu-id="82f9d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="82f9d-116">Requirement</span></span> | <span data-ttu-id="82f9d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="82f9d-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82f9d-118">Header</span><span class="sxs-lookup"><span data-stu-id="82f9d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="82f9d-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="82f9d-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="82f9d-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="82f9d-120">Library</span></span><br/> | <dl> <span data-ttu-id="82f9d-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82f9d-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="82f9d-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82f9d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82f9d-123">Математические функции</span><span class="sxs-lookup"><span data-stu-id="82f9d-123">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="82f9d-124">**D3DXQuaternionLength**</span><span class="sxs-lookup"><span data-stu-id="82f9d-124">**D3DXQuaternionLength**</span></span>](d3dxquaternionlength.md)
</dt> </dl>

 

 
