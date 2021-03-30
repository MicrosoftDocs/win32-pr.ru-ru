---
description: Определяет константы, описывающие режим тумана.
ms.assetid: cd83c914-bc1d-4f66-b5a6-7984b7ec52cd
title: Перечисление D3DFOGMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFOGMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8436a52edbb9460c6945c1526513629939ec444b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355240"
---
# <a name="d3dfogmode-enumeration"></a><span data-ttu-id="995ee-103">Перечисление D3DFOGMODE</span><span class="sxs-lookup"><span data-stu-id="995ee-103">D3DFOGMODE enumeration</span></span>

<span data-ttu-id="995ee-104">Определяет константы, описывающие режим тумана.</span><span class="sxs-lookup"><span data-stu-id="995ee-104">Defines constants that describe the fog mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="995ee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="995ee-105">Syntax</span></span>


```C++
typedef enum D3DFOGMODE { 
  D3DFOG_NONE         = 0,
  D3DFOG_EXP          = 1,
  D3DFOG_EXP2         = 2,
  D3DFOG_LINEAR       = 3,
  D3DFOG_FORCE_DWORD  = 0x7fffffff
} D3DFOGMODE, *LPD3DFOGMODE;
```



## <a name="constants"></a><span data-ttu-id="995ee-106">Константы</span><span class="sxs-lookup"><span data-stu-id="995ee-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="995ee-107"><span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG \_ None**</span><span class="sxs-lookup"><span data-stu-id="995ee-107"><span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="995ee-108">Нет воздействия на туман.</span><span class="sxs-lookup"><span data-stu-id="995ee-108">No fog effect.</span></span>

</dd> <dt>

<span data-ttu-id="995ee-109"><span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG \_ exp**</span><span class="sxs-lookup"><span data-stu-id="995ee-109"><span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG\_EXP**</span></span>
</dt> <dd>

<span data-ttu-id="995ee-110">Воздействие тумана в экспоненциальном виде усиливается в соответствии со следующей формулой.</span><span class="sxs-lookup"><span data-stu-id="995ee-110">Fog effect intensifies exponentially, according to the following formula.</span></span>

![Формула интенсивности эффектов тумана](images/fogexp.png)

</dd> <dt>

<span data-ttu-id="995ee-112"><span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG \_ EXP2**</span><span class="sxs-lookup"><span data-stu-id="995ee-112"><span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG\_EXP2**</span></span>
</dt> <dd>

<span data-ttu-id="995ee-113">Воздействие тумана экспоненциально усиливается квадратом расстояния в соответствии со следующей формулой.</span><span class="sxs-lookup"><span data-stu-id="995ee-113">Fog effect intensifies exponentially with the square of the distance, according to the following formula.</span></span>

![Формула интенсивности влияния тумана на основе квадрата расстояния](images/fogexp2.png)

</dd> <dt>

<span data-ttu-id="995ee-115"><span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**\_Линейная D3DFOG**</span><span class="sxs-lookup"><span data-stu-id="995ee-115"><span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**D3DFOG\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="995ee-116">Воздействие тумана усиливается линейно между начальной и конечной точками в соответствии со следующей формулой.</span><span class="sxs-lookup"><span data-stu-id="995ee-116">Fog effect intensifies linearly between the start and end points, according to the following formula.</span></span>

![Формула интенсивности эффектов тумана на основе начальной и конечной точек](images/fogliner.png)

<span data-ttu-id="995ee-118">В настоящее время поддерживается только этот режим тумана.</span><span class="sxs-lookup"><span data-stu-id="995ee-118">This is the only fog mode currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="995ee-119"><span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="995ee-119"><span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="995ee-120">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="995ee-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="995ee-121">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="995ee-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="995ee-122">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="995ee-122">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="995ee-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="995ee-123">Remarks</span></span>

<span data-ttu-id="995ee-124">Значения в этом перечислимом типе используются в \_ \_ состояниях отрисовки D3DRS ФОГТАБЛЕМОДЕ и D3DRS фогвертексмоде.</span><span class="sxs-lookup"><span data-stu-id="995ee-124">The values in this enumerated type are used by the D3DRS\_FOGTABLEMODE and D3DRS\_FOGVERTEXMODE render states.</span></span>

<span data-ttu-id="995ee-125">Туман может считаться мерой видимости: чем меньше значение тумана, созданное уравнением тумана, тем менее видимым является объект.</span><span class="sxs-lookup"><span data-stu-id="995ee-125">Fog can be considered a measure of visibility: the lower the fog value produced by a fog equation, the less visible an object is.</span></span>

## <a name="requirements"></a><span data-ttu-id="995ee-126">Требования</span><span class="sxs-lookup"><span data-stu-id="995ee-126">Requirements</span></span>



| <span data-ttu-id="995ee-127">Требование</span><span class="sxs-lookup"><span data-stu-id="995ee-127">Requirement</span></span> | <span data-ttu-id="995ee-128">Значение</span><span class="sxs-lookup"><span data-stu-id="995ee-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="995ee-129">Header</span><span class="sxs-lookup"><span data-stu-id="995ee-129">Header</span></span><br/> | <dl> <span data-ttu-id="995ee-130"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="995ee-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="995ee-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="995ee-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="995ee-132">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="995ee-132">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="995ee-133">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="995ee-133">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
