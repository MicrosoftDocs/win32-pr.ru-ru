---
description: Определяет константы, описывающие поддерживаемые режимы адресации текстуры.
ms.assetid: 5c03c55f-4a74-4b0e-ba05-e4a6582ff47c
title: Перечисление D3DTEXTUREADDRESS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREADDRESS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2cb1893541f80efb9bf85ea444b27bebba5dea29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081850"
---
# <a name="d3dtextureaddress-enumeration"></a><span data-ttu-id="d4edf-103">Перечисление D3DTEXTUREADDRESS</span><span class="sxs-lookup"><span data-stu-id="d4edf-103">D3DTEXTUREADDRESS enumeration</span></span>

<span data-ttu-id="d4edf-104">Определяет константы, описывающие поддерживаемые режимы адресации текстуры.</span><span class="sxs-lookup"><span data-stu-id="d4edf-104">Defines constants that describe the supported texture-addressing modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4edf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4edf-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREADDRESS { 
  D3DTADDRESS_WRAP         = 1,
  D3DTADDRESS_MIRROR       = 2,
  D3DTADDRESS_CLAMP        = 3,
  D3DTADDRESS_BORDER       = 4,
  D3DTADDRESS_MIRRORONCE   = 5,
  D3DTADDRESS_FORCE_DWORD  = 0x7fffffff
} D3DTEXTUREADDRESS, *LPD3DTEXTUREADDRESS;
```



## <a name="constants"></a><span data-ttu-id="d4edf-106">Константы</span><span class="sxs-lookup"><span data-stu-id="d4edf-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d4edf-107"><span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**D3DTADDRESS \_ Перенос**</span><span class="sxs-lookup"><span data-stu-id="d4edf-107"><span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**D3DTADDRESS\_WRAP**</span></span>
</dt> <dd>

<span data-ttu-id="d4edf-108">Мозаичное заполнение текстуры на каждой одноцелочисленной дизъюнкции.</span><span class="sxs-lookup"><span data-stu-id="d4edf-108">Tile the texture at every integer junction.</span></span> <span data-ttu-id="d4edf-109">Например, для значений в диапазоне от 0 до 3 текстура повторяется три раза; Зеркальное отображение не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d4edf-109">For example, for u values between 0 and 3, the texture is repeated three times; no mirroring is performed.</span></span>

</dd> <dt>

<span data-ttu-id="d4edf-110"><span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**\_Зеркальное отображение D3DTADDRESS**</span><span class="sxs-lookup"><span data-stu-id="d4edf-110"><span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**D3DTADDRESS\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="d4edf-111">Аналогично D3DTADDRESS \_ переносу, за исключением того, что текстура перемещается на каждое целое число.</span><span class="sxs-lookup"><span data-stu-id="d4edf-111">Similar to D3DTADDRESS\_WRAP, except that the texture is flipped at every integer junction.</span></span> <span data-ttu-id="d4edf-112">для значений в диапазоне от 0 до 1, например, текстура обнаправлена обычным образом; в диапазоне от 1 до 2 текстура зеркально отражается (зеркальная); в диапазоне от 2 до 3 текстура является нормальной. и т. д.</span><span class="sxs-lookup"><span data-stu-id="d4edf-112">For u values between 0 and 1, for example, the texture is addressed normally; between 1 and 2, the texture is flipped (mirrored); between 2 and 3, the texture is normal again; and so on.</span></span>

</dd> <dt>

<span data-ttu-id="d4edf-113"><span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**D3DTADDRESSный \_ срез**</span><span class="sxs-lookup"><span data-stu-id="d4edf-113"><span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**D3DTADDRESS\_CLAMP**</span></span>
</dt> <dd>

<span data-ttu-id="d4edf-114">Координаты текстуры за пределами диапазона \[ 0,0, 1,0 \] задаются в качестве цвета текстуры в 0,0 или 1,0 соответственно.</span><span class="sxs-lookup"><span data-stu-id="d4edf-114">Texture coordinates outside the range \[0.0, 1.0\] are set to the texture color at 0.0 or 1.0, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="d4edf-115"><span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**\_Граница D3DTADDRESS**</span><span class="sxs-lookup"><span data-stu-id="d4edf-115"><span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**D3DTADDRESS\_BORDER**</span></span>
</dt> <dd>

<span data-ttu-id="d4edf-116">Координаты текстуры за пределами диапазона \[ 0,0, 1,0 \] задаются цветом границы.</span><span class="sxs-lookup"><span data-stu-id="d4edf-116">Texture coordinates outside the range \[0.0, 1.0\] are set to the border color.</span></span>

</dd> <dt>

<span data-ttu-id="d4edf-117"><span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**D3DTADDRESS \_ мирроронце**</span><span class="sxs-lookup"><span data-stu-id="d4edf-117"><span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**D3DTADDRESS\_MIRRORONCE**</span></span>
</dt> <dd>

<span data-ttu-id="d4edf-118">Аналогично \_ зеркальному D3DTADDRESS и D3DTADDRESSному \_ срезу.</span><span class="sxs-lookup"><span data-stu-id="d4edf-118">Similar to D3DTADDRESS\_MIRROR and D3DTADDRESS\_CLAMP.</span></span> <span data-ttu-id="d4edf-119">Принимает абсолютное значение координаты текстуры (то есть зеркальное отображение 0), а затем выполняет фиксацию до максимального значения.</span><span class="sxs-lookup"><span data-stu-id="d4edf-119">Takes the absolute value of the texture coordinate (thus, mirroring around 0), and then clamps to the maximum value.</span></span> <span data-ttu-id="d4edf-120">Чаще всего используется для текстур томов, где поддержка полного \_ режима адресации ТЕКСТУР D3DTADDRESS мирроронце не требуется, но данные являются симметричными вокруг одной оси.</span><span class="sxs-lookup"><span data-stu-id="d4edf-120">The most common usage is for volume textures, where support for the full D3DTADDRESS\_MIRRORONCE texture-addressing mode is not necessary, but the data is symmetric around the one axis.</span></span>

</dd> <dt>

<span data-ttu-id="d4edf-121"><span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d4edf-121"><span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="d4edf-122">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="d4edf-122">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="d4edf-123">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="d4edf-123">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="d4edf-124">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="d4edf-124">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4edf-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d4edf-125">Requirements</span></span>



| <span data-ttu-id="d4edf-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d4edf-126">Requirement</span></span> | <span data-ttu-id="d4edf-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d4edf-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4edf-128">Header</span><span class="sxs-lookup"><span data-stu-id="d4edf-128">Header</span></span><br/> | <dl> <span data-ttu-id="d4edf-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4edf-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4edf-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4edf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4edf-131">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="d4edf-131">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="d4edf-132">**D3DSAMPLERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="d4edf-132">**D3DSAMPLERSTATETYPE**</span></span>](./d3dsamplerstatetype.md)
</dt> </dl>

 

 
