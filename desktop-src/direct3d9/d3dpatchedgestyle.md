---
description: Определяет, является ли текущий режим тесселяции дискретным или непрерывным.
ms.assetid: d8055a25-6a8e-4018-a993-762f6f0e0cd3
title: Перечисление D3DPATCHEDGESTYLE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPATCHEDGESTYLE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e625b7c4ff12f9859efdcc2b10b551a2223adab6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914748"
---
# <a name="d3dpatchedgestyle-enumeration"></a><span data-ttu-id="caed6-103">Перечисление D3DPATCHEDGESTYLE</span><span class="sxs-lookup"><span data-stu-id="caed6-103">D3DPATCHEDGESTYLE enumeration</span></span>

<span data-ttu-id="caed6-104">Определяет, является ли текущий режим тесселяции дискретным или непрерывным.</span><span class="sxs-lookup"><span data-stu-id="caed6-104">Defines whether the current tessellation mode is discrete or continuous.</span></span>

## <a name="syntax"></a><span data-ttu-id="caed6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="caed6-105">Syntax</span></span>


```C++
typedef enum D3DPATCHEDGESTYLE { 
  D3DPATCHEDGE_DISCRETE     = 0,
  D3DPATCHEDGE_CONTINUOUS   = 1,
  D3DPATCHEDGE_FORCE_DWORD  = 0x7fffffff
} D3DPATCHEDGESTYLE, *LPD3DPATCHEDGESTYLE;
```



## <a name="constants"></a><span data-ttu-id="caed6-106">Константы</span><span class="sxs-lookup"><span data-stu-id="caed6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="caed6-107"><span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**\_Дискретный D3DPATCHEDGE**</span><span class="sxs-lookup"><span data-stu-id="caed6-107"><span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE\_DISCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="caed6-108">Дискретный стиль ребра.</span><span class="sxs-lookup"><span data-stu-id="caed6-108">Discrete edge style.</span></span> <span data-ttu-id="caed6-109">В дискретном режиме можно указать тесселяцию с плавающей запятой, но оно будет усечено до целых чисел.</span><span class="sxs-lookup"><span data-stu-id="caed6-109">In discrete mode, you can specify float tessellation but it will be truncated to integers.</span></span>

</dd> <dt>

<span data-ttu-id="caed6-110"><span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE \_ непрерывно**</span><span class="sxs-lookup"><span data-stu-id="caed6-110"><span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE\_CONTINUOUS**</span></span>
</dt> <dd>

<span data-ttu-id="caed6-111">Стиль непрерывного ребра.</span><span class="sxs-lookup"><span data-stu-id="caed6-111">Continuous edge style.</span></span> <span data-ttu-id="caed6-112">В непрерывном режиме тесселяция задается как значения float, которые могут быть плавно изменяться для сокращения числа "выталкивания".</span><span class="sxs-lookup"><span data-stu-id="caed6-112">In continuous mode, tessellation is specified as float values that can be smoothly varied to reduce "popping" artifacts.</span></span>

</dd> <dt>

<span data-ttu-id="caed6-113"><span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="caed6-113"><span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="caed6-114">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="caed6-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="caed6-115">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="caed6-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="caed6-116">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="caed6-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="caed6-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="caed6-117">Remarks</span></span>

<span data-ttu-id="caed6-118">Обратите внимание, что непрерывная тесселяция создает совершенно другой шаблон тесселяции из дискретного для тех же значений тесселяции (это более очевидно в режиме каркаса).</span><span class="sxs-lookup"><span data-stu-id="caed6-118">Note that continuous tessellation produces a completely different tessellation pattern from the discrete one for the same tessellation values (this is more apparent in wireframe mode).</span></span> <span data-ttu-id="caed6-119">Таким образом, 4,0 непрерывная не совпадает с 4 дискретной.</span><span class="sxs-lookup"><span data-stu-id="caed6-119">Thus, 4.0 continuous is not the same as 4 discrete.</span></span>

## <a name="requirements"></a><span data-ttu-id="caed6-120">Требования</span><span class="sxs-lookup"><span data-stu-id="caed6-120">Requirements</span></span>



| <span data-ttu-id="caed6-121">Требование</span><span class="sxs-lookup"><span data-stu-id="caed6-121">Requirement</span></span> | <span data-ttu-id="caed6-122">Значение</span><span class="sxs-lookup"><span data-stu-id="caed6-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="caed6-123">Header</span><span class="sxs-lookup"><span data-stu-id="caed6-123">Header</span></span><br/> | <dl> <span data-ttu-id="caed6-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="caed6-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caed6-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="caed6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caed6-126">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="caed6-126">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




