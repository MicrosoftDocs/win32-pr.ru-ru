---
description: Флаги, указывающие метод, используемый программой растеризации для создания изображения на поверхности.
ms.assetid: 55cf790e-ebe9-4791-a2be-a90fc76bae57
title: Перечисление D3DSCANLINEORDERING (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSCANLINEORDERING
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2eaed36577f881266c12b0a927cfcdc2494f0d57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714016"
---
# <a name="d3dscanlineordering-enumeration"></a><span data-ttu-id="ef06e-103">Перечисление D3DSCANLINEORDERING</span><span class="sxs-lookup"><span data-stu-id="ef06e-103">D3DSCANLINEORDERING enumeration</span></span>

<span data-ttu-id="ef06e-104">Флаги, указывающие метод, используемый программой растеризации для создания изображения на поверхности.</span><span class="sxs-lookup"><span data-stu-id="ef06e-104">Flags indicating the method the rasterizer uses to create an image on a surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef06e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef06e-105">Syntax</span></span>


```C++
typedef enum D3DSCANLINEORDERING { 
  D3DSCANLINEORDERING_PROGRESSIVE  = 1,
  D3DSCANLINEORDERING_INTERLACED   = 2
} D3DSCANLINEORDERING, *LPD3DSCANLINEORDERING;
```



## <a name="constants"></a><span data-ttu-id="ef06e-106">Константы</span><span class="sxs-lookup"><span data-stu-id="ef06e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ef06e-107"><span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**D3DSCANLINEORDERING \_ прогрессивный**</span><span class="sxs-lookup"><span data-stu-id="ef06e-107"><span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**D3DSCANLINEORDERING\_PROGRESSIVE**</span></span>
</dt> <dd>

<span data-ttu-id="ef06e-108">Изображение создается из первого сканлине к последнему без пропуска.</span><span class="sxs-lookup"><span data-stu-id="ef06e-108">The image is created from the first scanline to the last without skipping any.</span></span>

</dd> <dt>

<span data-ttu-id="ef06e-109"><span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**D3DSCANLINEORDERING с \_ чередованием**</span><span class="sxs-lookup"><span data-stu-id="ef06e-109"><span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**D3DSCANLINEORDERING\_INTERLACED**</span></span>
</dt> <dd>

<span data-ttu-id="ef06e-110">Изображение создается с помощью метода чередования, в котором нечетные нумерованные линии рисуются на нечетных этапах, а даже линии рисуются с четными числами.</span><span class="sxs-lookup"><span data-stu-id="ef06e-110">The image is created using the interlaced method in which odd-numbered lines are drawn on odd-numbered passes and even lines are drawn on even-numbered passes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef06e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef06e-111">Remarks</span></span>

<span data-ttu-id="ef06e-112">Это перечисление используется в качестве члена в [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) и [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md).</span><span class="sxs-lookup"><span data-stu-id="ef06e-112">This enumeration is used as a member in [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) and [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef06e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ef06e-113">Requirements</span></span>



| <span data-ttu-id="ef06e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ef06e-114">Requirement</span></span> | <span data-ttu-id="ef06e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ef06e-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef06e-116">Header</span><span class="sxs-lookup"><span data-stu-id="ef06e-116">Header</span></span><br/> | <dl> <span data-ttu-id="ef06e-117"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef06e-117"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef06e-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef06e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef06e-119">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="ef06e-119">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




