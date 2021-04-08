---
description: Определяет константы, описывающие тип заднего буфера.
ms.assetid: f099656b-4957-40a7-a92e-2c17e5fa8df9
title: Перечисление D3DBACKBUFFER_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBACKBUFFER_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1641b37242339173fc5f591280d8e2beeff6a9e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000329"
---
# <a name="d3dbackbuffer_type-enumeration"></a><span data-ttu-id="334df-103">\_Перечисление типов D3DBACKBUFFER</span><span class="sxs-lookup"><span data-stu-id="334df-103">D3DBACKBUFFER\_TYPE enumeration</span></span>

<span data-ttu-id="334df-104">Определяет константы, описывающие тип заднего буфера.</span><span class="sxs-lookup"><span data-stu-id="334df-104">Defines constants that describe the type of back buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="334df-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="334df-105">Syntax</span></span>


```C++
typedef enum D3DBACKBUFFER_TYPE { 
  D3DBACKBUFFER_TYPE_MONO         = 0,
  D3DBACKBUFFER_TYPE_LEFT         = 1,
  D3DBACKBUFFER_TYPE_RIGHT        = 2,
  D3DBACKBUFFER_TYPE_FORCE_DWORD  = 0x7fffffff
} D3DBACKBUFFER_TYPE, *LPD3DBACKBUFFER_TYPE;
```



## <a name="constants"></a><span data-ttu-id="334df-106">Константы</span><span class="sxs-lookup"><span data-stu-id="334df-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="334df-107"><span id="D3DBACKBUFFER_TYPE_MONO"></span><span id="d3dbackbuffer_type_mono"></span>**\_Тип D3DBACKBUFFER \_ Mono**</span><span class="sxs-lookup"><span data-stu-id="334df-107"><span id="D3DBACKBUFFER_TYPE_MONO"></span><span id="d3dbackbuffer_type_mono"></span>**D3DBACKBUFFER\_TYPE\_MONO**</span></span>
</dt> <dd>

<span data-ttu-id="334df-108">Указывает нестерео цепочку подкачки.</span><span class="sxs-lookup"><span data-stu-id="334df-108">Specifies a nonstereo swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="334df-109"><span id="D3DBACKBUFFER_TYPE_LEFT"></span><span id="d3dbackbuffer_type_left"></span>**\_Тип D3DBACKBUFFER \_ Left**</span><span class="sxs-lookup"><span data-stu-id="334df-109"><span id="D3DBACKBUFFER_TYPE_LEFT"></span><span id="d3dbackbuffer_type_left"></span>**D3DBACKBUFFER\_TYPE\_LEFT**</span></span>
</dt> <dd>

<span data-ttu-id="334df-110">Задает левую сторону пары стерео в цепочке буферов.</span><span class="sxs-lookup"><span data-stu-id="334df-110">Specifies the left side of a stereo pair in a swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="334df-111"><span id="D3DBACKBUFFER_TYPE_RIGHT"></span><span id="d3dbackbuffer_type_right"></span>**\_Тип D3DBACKBUFFER \_ right**</span><span class="sxs-lookup"><span data-stu-id="334df-111"><span id="D3DBACKBUFFER_TYPE_RIGHT"></span><span id="d3dbackbuffer_type_right"></span>**D3DBACKBUFFER\_TYPE\_RIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="334df-112">Указывает правую сторону пары стерео в цепочке буферов.</span><span class="sxs-lookup"><span data-stu-id="334df-112">Specifies the right side of a stereo pair in a swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="334df-113"><span id="D3DBACKBUFFER_TYPE_FORCE_DWORD"></span><span id="d3dbackbuffer_type_force_dword"></span>**D3DBACKBUFFER \_ тип \_ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="334df-113"><span id="D3DBACKBUFFER_TYPE_FORCE_DWORD"></span><span id="d3dbackbuffer_type_force_dword"></span>**D3DBACKBUFFER\_TYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="334df-114">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="334df-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="334df-115">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="334df-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="334df-116">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="334df-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="334df-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="334df-117">Remarks</span></span>

<span data-ttu-id="334df-118">Direct3D 9 не поддерживает стерео представление, поэтому Direct3D не использует D3DBACKBUFFER \_ типа \_ Left и D3DBACKBUFFER \_ Type \_ right для этого перечислимого типа.</span><span class="sxs-lookup"><span data-stu-id="334df-118">Direct3D 9 does not support stereo view, so Direct3D does not use the D3DBACKBUFFER\_TYPE\_LEFT and D3DBACKBUFFER\_TYPE\_RIGHT values of this enumerated type.</span></span>

## <a name="requirements"></a><span data-ttu-id="334df-119">Требования</span><span class="sxs-lookup"><span data-stu-id="334df-119">Requirements</span></span>



| <span data-ttu-id="334df-120">Требование</span><span class="sxs-lookup"><span data-stu-id="334df-120">Requirement</span></span> | <span data-ttu-id="334df-121">Значение</span><span class="sxs-lookup"><span data-stu-id="334df-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="334df-122">Header</span><span class="sxs-lookup"><span data-stu-id="334df-122">Header</span></span><br/> | <dl> <span data-ttu-id="334df-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="334df-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="334df-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="334df-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="334df-125">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="334df-125">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="334df-126">**IDirect3DDevice9:: Жетбаккбуффер**</span><span class="sxs-lookup"><span data-stu-id="334df-126">**IDirect3DDevice9::GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
</dt> <dt>

[<span data-ttu-id="334df-127">**IDirect3DSwapChain9:: Жетбаккбуффер**</span><span class="sxs-lookup"><span data-stu-id="334df-127">**IDirect3DSwapChain9::GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer)
</dt> </dl>

 

 
