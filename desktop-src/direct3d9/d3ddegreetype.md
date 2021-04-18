---
description: Определяет степень переменных в уравнении, описывающее кривую.
ms.assetid: 52a9c57e-a48d-4d8a-a208-97a3d09e7abf
title: Перечисление D3DDEGREETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEGREETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 773ef3a8dd8fc5f4657119c2021c5723e54a3bd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713583"
---
# <a name="d3ddegreetype-enumeration"></a><span data-ttu-id="87373-103">Перечисление D3DDEGREETYPE</span><span class="sxs-lookup"><span data-stu-id="87373-103">D3DDEGREETYPE enumeration</span></span>

<span data-ttu-id="87373-104">Определяет степень переменных в уравнении, описывающее кривую.</span><span class="sxs-lookup"><span data-stu-id="87373-104">Defines the degree of the variables in the equation that describes a curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="87373-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87373-105">Syntax</span></span>


```C++
typedef enum D3DDEGREETYPE { 
  D3DDEGREE_LINEAR     = 1,
  D3DDEGREE_QUADRATIC  = 2,
  D3DDEGREE_CUBIC      = 3,
  D3DDEGREE_QUINTIC    = 5,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DDEGREETYPE, *LPD3DDEGREETYPE;
```



## <a name="constants"></a><span data-ttu-id="87373-106">Константы</span><span class="sxs-lookup"><span data-stu-id="87373-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="87373-107"><span id="D3DDEGREE_LINEAR"></span><span id="d3ddegree_linear"></span>**\_Линейная D3DDEGREE**</span><span class="sxs-lookup"><span data-stu-id="87373-107"><span id="D3DDEGREE_LINEAR"></span><span id="d3ddegree_linear"></span>**D3DDEGREE\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="87373-108">Кривая описывается переменными первого порядка.</span><span class="sxs-lookup"><span data-stu-id="87373-108">Curve is described by variables of first order.</span></span>

</dd> <dt>

<span data-ttu-id="87373-109"><span id="D3DDEGREE_QUADRATIC"></span><span id="d3ddegree_quadratic"></span>**D3DDEGREE, \_ квадрат**</span><span class="sxs-lookup"><span data-stu-id="87373-109"><span id="D3DDEGREE_QUADRATIC"></span><span id="d3ddegree_quadratic"></span>**D3DDEGREE\_QUADRATIC**</span></span>
</dt> <dd>

<span data-ttu-id="87373-110">Кривая описывается переменными второго порядка.</span><span class="sxs-lookup"><span data-stu-id="87373-110">Curve is described by variables of second order.</span></span>

</dd> <dt>

<span data-ttu-id="87373-111"><span id="D3DDEGREE_CUBIC"></span><span id="d3ddegree_cubic"></span>**D3DDEGREE \_ кубический**</span><span class="sxs-lookup"><span data-stu-id="87373-111"><span id="D3DDEGREE_CUBIC"></span><span id="d3ddegree_cubic"></span>**D3DDEGREE\_CUBIC**</span></span>
</dt> <dd>

<span data-ttu-id="87373-112">Кривая описывается переменными третьего порядка.</span><span class="sxs-lookup"><span data-stu-id="87373-112">Curve is described by variables of third order.</span></span>

</dd> <dt>

<span data-ttu-id="87373-113"><span id="D3DDEGREE_QUINTIC"></span><span id="d3ddegree_quintic"></span>**D3DDEGREE \_ куинтик**</span><span class="sxs-lookup"><span data-stu-id="87373-113"><span id="D3DDEGREE_QUINTIC"></span><span id="d3ddegree_quintic"></span>**D3DDEGREE\_QUINTIC**</span></span>
</dt> <dd>

<span data-ttu-id="87373-114">Кривая описывается с помощью переменных четвертого порядка.</span><span class="sxs-lookup"><span data-stu-id="87373-114">Curve is described by variables of fourth order.</span></span>

</dd> <dt>

<span data-ttu-id="87373-115"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="87373-115"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="87373-116">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="87373-116">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="87373-117">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="87373-117">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="87373-118">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="87373-118">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87373-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87373-119">Remarks</span></span>

<span data-ttu-id="87373-120">Значения в этом перечислении используются для описания кривых, используемых в обновлениях прямоугольника и треугольника.</span><span class="sxs-lookup"><span data-stu-id="87373-120">The values in this enumeration are used to describe the curves used by rectangle and triangle patches.</span></span> <span data-ttu-id="87373-121">Дополнительные сведения см. в разделе D3DRS \_ куллмоде.</span><span class="sxs-lookup"><span data-stu-id="87373-121">For more information, see D3DRS\_CULLMODE.</span></span>

## <a name="requirements"></a><span data-ttu-id="87373-122">Требования</span><span class="sxs-lookup"><span data-stu-id="87373-122">Requirements</span></span>



| <span data-ttu-id="87373-123">Требование</span><span class="sxs-lookup"><span data-stu-id="87373-123">Requirement</span></span> | <span data-ttu-id="87373-124">Значение</span><span class="sxs-lookup"><span data-stu-id="87373-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87373-125">Header</span><span class="sxs-lookup"><span data-stu-id="87373-125">Header</span></span><br/> | <dl> <span data-ttu-id="87373-126"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="87373-126"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87373-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87373-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87373-128">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="87373-128">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="87373-129">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="87373-129">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="87373-130">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="87373-130">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
