---
description: Определяет поддерживаемые функции сравнения.
ms.assetid: 999af3eb-a208-4312-acee-373192ea69e4
title: Перечисление D3DCMPFUNC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCMPFUNC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e49f0e058e795e00349020619f1e6d6310dfd94f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914708"
---
# <a name="d3dcmpfunc-enumeration"></a><span data-ttu-id="c5a4e-103">Перечисление D3DCMPFUNC</span><span class="sxs-lookup"><span data-stu-id="c5a4e-103">D3DCMPFUNC enumeration</span></span>

<span data-ttu-id="c5a4e-104">Определяет поддерживаемые функции сравнения.</span><span class="sxs-lookup"><span data-stu-id="c5a4e-104">Defines the supported compare functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5a4e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5a4e-105">Syntax</span></span>


```C++
typedef enum D3DCMPFUNC { 
  D3DCMP_NEVER         = 1,
  D3DCMP_LESS          = 2,
  D3DCMP_EQUAL         = 3,
  D3DCMP_LESSEQUAL     = 4,
  D3DCMP_GREATER       = 5,
  D3DCMP_NOTEQUAL      = 6,
  D3DCMP_GREATEREQUAL  = 7,
  D3DCMP_ALWAYS        = 8,
  D3DCMP_FORCE_DWORD   = 0x7fffffff
} D3DCMPFUNC, *LPD3DCMPFUNC;
```



## <a name="constants"></a><span data-ttu-id="c5a4e-106">Константы</span><span class="sxs-lookup"><span data-stu-id="c5a4e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c5a4e-107"><span id="D3DCMP_NEVER"></span><span id="d3dcmp_never"></span>**D3DCMP \_ никогда**</span><span class="sxs-lookup"><span data-stu-id="c5a4e-107"><span id="D3DCMP_NEVER"></span><span id="d3dcmp_never"></span>**D3DCMP\_NEVER**</span></span>
</dt> <dd>

<span data-ttu-id="c5a4e-108">Всегда завершать тест неудачей.</span><span class="sxs-lookup"><span data-stu-id="c5a4e-108">Always fail the test.</span></span>

</dd> <dt>

<span data-ttu-id="c5a4e-109"><span id="D3DCMP_LESS"></span><span id="d3dcmp_less"></span>**D3DCMP \_ меньше**</span><span class="sxs-lookup"><span data-stu-id="c5a4e-109"><span id="D3DCMP_LESS"></span><span id="d3dcmp_less"></span>**D3DCMP\_LESS**</span></span>
</dt> <dd>

<span data-ttu-id="c5a4e-110">Принять новую точку, если ее значение меньше значения текущего пикселя.</span><span class="sxs-lookup"><span data-stu-id="c5a4e-110">Accept the new pixel if its value is less than the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="c5a4e-111"><span id="D3DCMP_EQUAL"></span><span id="d3dcmp_equal"></span>**D3DCMP \_ равно**</span><span class="sxs-lookup"><span data-stu-id="c5a4e-111"><span id="D3DCMP_EQUAL"></span><span id="d3dcmp_equal"></span>**D3DCMP\_EQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="c5a4e-112">Принять новую точку, если ее значение равно значению текущего пикселя.</span><span class="sxs-lookup"><span data-stu-id="c5a4e-112">Accept the new pixel if its value equals the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="c5a4e-113"><span id="D3DCMP_LESSEQUAL"></span><span id="d3dcmp_lessequal"></span>**D3DCMP \_ лессекуал**</span><span class="sxs-lookup"><span data-stu-id="c5a4e-113"><span id="D3DCMP_LESSEQUAL"></span><span id="d3dcmp_lessequal"></span>**D3DCMP\_LESSEQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="c5a4e-114">Принять новую точку, если ее значение меньше или равно значению текущего пикселя.</span><span class="sxs-lookup"><span data-stu-id="c5a4e-114">Accept the new pixel if its value is less than or equal to the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="c5a4e-115"><span id="D3DCMP_GREATER"></span><span id="d3dcmp_greater"></span>**D3DCMP \_**</span><span class="sxs-lookup"><span data-stu-id="c5a4e-115"><span id="D3DCMP_GREATER"></span><span id="d3dcmp_greater"></span>**D3DCMP\_GREATER**</span></span>
</dt> <dd>

<span data-ttu-id="c5a4e-116">Принять новую точку, если ее значение больше значения текущего пикселя.</span><span class="sxs-lookup"><span data-stu-id="c5a4e-116">Accept the new pixel if its value is greater than the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="c5a4e-117"><span id="D3DCMP_NOTEQUAL"></span><span id="d3dcmp_notequal"></span>**D3DCMP \_ NOTEQUAL**</span><span class="sxs-lookup"><span data-stu-id="c5a4e-117"><span id="D3DCMP_NOTEQUAL"></span><span id="d3dcmp_notequal"></span>**D3DCMP\_NOTEQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="c5a4e-118">Принять новую точку, если ее значение не равно значению текущего пикселя.</span><span class="sxs-lookup"><span data-stu-id="c5a4e-118">Accept the new pixel if its value does not equal the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="c5a4e-119"><span id="D3DCMP_GREATEREQUAL"></span><span id="d3dcmp_greaterequal"></span>**D3DCMP \_ загруженность**</span><span class="sxs-lookup"><span data-stu-id="c5a4e-119"><span id="D3DCMP_GREATEREQUAL"></span><span id="d3dcmp_greaterequal"></span>**D3DCMP\_GREATEREQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="c5a4e-120">Принять новую точку, если ее значение больше или равно значению текущего пикселя.</span><span class="sxs-lookup"><span data-stu-id="c5a4e-120">Accept the new pixel if its value is greater than or equal to the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="c5a4e-121"><span id="D3DCMP_ALWAYS"></span><span id="d3dcmp_always"></span>**D3DCMP \_ всегда**</span><span class="sxs-lookup"><span data-stu-id="c5a4e-121"><span id="D3DCMP_ALWAYS"></span><span id="d3dcmp_always"></span>**D3DCMP\_ALWAYS**</span></span>
</dt> <dd>

<span data-ttu-id="c5a4e-122">Всегда проверяйте тест.</span><span class="sxs-lookup"><span data-stu-id="c5a4e-122">Always pass the test.</span></span>

</dd> <dt>

<span data-ttu-id="c5a4e-123"><span id="D3DCMP_FORCE_DWORD"></span><span id="d3dcmp_force_dword"></span>**D3DCMP \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c5a4e-123"><span id="D3DCMP_FORCE_DWORD"></span><span id="d3dcmp_force_dword"></span>**D3DCMP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="c5a4e-124">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="c5a4e-124">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="c5a4e-125">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="c5a4e-125">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="c5a4e-126">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="c5a4e-126">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5a4e-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c5a4e-127">Remarks</span></span>

<span data-ttu-id="c5a4e-128">Значения в этом перечислимом типе определяют поддерживаемые функции сравнения для \_ состояний отрисовки D3DRS зфунк, D3DRS \_ АЛФАФУНК и D3DRS \_ стенЦилфунк.</span><span class="sxs-lookup"><span data-stu-id="c5a4e-128">The values in this enumerated type define the supported compare functions for the D3DRS\_ZFUNC, D3DRS\_ALPHAFUNC, and D3DRS\_STENCILFUNC render states.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5a4e-129">Требования</span><span class="sxs-lookup"><span data-stu-id="c5a4e-129">Requirements</span></span>



| <span data-ttu-id="c5a4e-130">Требование</span><span class="sxs-lookup"><span data-stu-id="c5a4e-130">Requirement</span></span> | <span data-ttu-id="c5a4e-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c5a4e-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a4e-132">Header</span><span class="sxs-lookup"><span data-stu-id="c5a4e-132">Header</span></span><br/> | <dl> <span data-ttu-id="c5a4e-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5a4e-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5a4e-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5a4e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5a4e-135">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="c5a4e-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="c5a4e-136">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="c5a4e-136">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
