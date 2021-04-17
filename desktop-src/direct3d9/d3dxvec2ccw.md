---
description: Возвращает компонент z, используя перекрестное произведение двух двумерных векторов.
ms.assetid: daec19f2-cd0f-4a68-affc-9a42bda8912c
title: Функция D3DXVec2CCW (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CCW
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71c6e14171a9e7d12d86c30f05885cecf50ce973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703767"
---
# <a name="d3dxvec2ccw-function"></a><span data-ttu-id="b976f-103">Функция D3DXVec2CCW</span><span class="sxs-lookup"><span data-stu-id="b976f-103">D3DXVec2CCW function</span></span>

<span data-ttu-id="b976f-104">Возвращает компонент z, используя перекрестное произведение двух двумерных векторов.</span><span class="sxs-lookup"><span data-stu-id="b976f-104">Returns the z-component by taking the cross product of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="b976f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b976f-105">Syntax</span></span>


```C++
FLOAT D3DXVec2CCW(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="b976f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b976f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b976f-107">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b976f-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b976f-108">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="b976f-108">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="b976f-109">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="b976f-109">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b976f-110">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b976f-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b976f-111">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="b976f-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="b976f-112">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="b976f-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b976f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b976f-113">Return value</span></span>

<span data-ttu-id="b976f-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b976f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b976f-115">Компонент z.</span><span class="sxs-lookup"><span data-stu-id="b976f-115">The z-component.</span></span>

## <a name="remarks"></a><span data-ttu-id="b976f-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b976f-116">Remarks</span></span>

<span data-ttu-id="b976f-117">Эта функция определяет компонент z, определяя перекрестные произведения на основе следующей формулы: ((x1, y1, 0) Cross (x2, Y2, 0)).</span><span class="sxs-lookup"><span data-stu-id="b976f-117">This function determines the z-component by determining the cross-product based on the following formula: ((x1,y1,0) cross (x2,y2,0)).</span></span> <span data-ttu-id="b976f-118">Или, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="b976f-118">Or as shown in the following example.</span></span>


```
pV1->x * pV2->y - pV1->y * pV2->x
```



<span data-ttu-id="b976f-119">Если значение z-компонента положительное, вектор v2 имеет против часовой стрелки от вектора v1.</span><span class="sxs-lookup"><span data-stu-id="b976f-119">If the value of the z-component is positive, the vector V2 is counterclockwise from the vector V1.</span></span> <span data-ttu-id="b976f-120">Эти сведения полезны для отбора обратной стороны.</span><span class="sxs-lookup"><span data-stu-id="b976f-120">This information is useful for back-face culling.</span></span>

## <a name="requirements"></a><span data-ttu-id="b976f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b976f-121">Requirements</span></span>



| <span data-ttu-id="b976f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b976f-122">Requirement</span></span> | <span data-ttu-id="b976f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b976f-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b976f-124">Header</span><span class="sxs-lookup"><span data-stu-id="b976f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b976f-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b976f-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b976f-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b976f-126">Library</span></span><br/> | <dl> <span data-ttu-id="b976f-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b976f-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b976f-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b976f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b976f-129">Математические функции</span><span class="sxs-lookup"><span data-stu-id="b976f-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b976f-130">**D3DXVec2Dot**</span><span class="sxs-lookup"><span data-stu-id="b976f-130">**D3DXVec2Dot**</span></span>](d3dxvec2dot.md)
</dt> </dl>

 

 
