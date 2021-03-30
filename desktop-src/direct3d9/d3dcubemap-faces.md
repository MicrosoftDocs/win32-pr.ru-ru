---
description: Определяет грани кубической карты.
ms.assetid: 6d18b410-6f22-4202-86ae-6b3ef85e6f69
title: Перечисление D3DCUBEMAP_FACES (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCUBEMAP_FACES
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: eaf482f6f98d695f3aea3198948616c05ed01f72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354403"
---
# <a name="d3dcubemap_faces-enumeration"></a><span data-ttu-id="fd694-103">\_Перечисление D3DCUBEMAP лиц</span><span class="sxs-lookup"><span data-stu-id="fd694-103">D3DCUBEMAP\_FACES enumeration</span></span>

<span data-ttu-id="fd694-104">Определяет грани кубической карты.</span><span class="sxs-lookup"><span data-stu-id="fd694-104">Defines the faces of a cubemap.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd694-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd694-105">Syntax</span></span>


```C++
typedef enum D3DCUBEMAP_FACES { 
  D3DCUBEMAP_FACE_POSITIVE_X   = 0,
  D3DCUBEMAP_FACE_NEGATIVE_X   = 1,
  D3DCUBEMAP_FACE_POSITIVE_Y   = 2,
  D3DCUBEMAP_FACE_NEGATIVE_Y   = 3,
  D3DCUBEMAP_FACE_POSITIVE_Z   = 4,
  D3DCUBEMAP_FACE_NEGATIVE_Z   = 5,
  D3DCUBEMAP_FACE_FORCE_DWORD  = 0xffffffff
} D3DCUBEMAP_FACES, *LPD3DCUBEMAP_FACES;
```



## <a name="constants"></a><span data-ttu-id="fd694-106">Константы</span><span class="sxs-lookup"><span data-stu-id="fd694-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fd694-107"><span id="D3DCUBEMAP_FACE_POSITIVE_X"></span><span id="d3dcubemap_face_positive_x"></span>**D3DCUBEMAP \_ лицо \_ плюс \_ X**</span><span class="sxs-lookup"><span data-stu-id="fd694-107"><span id="D3DCUBEMAP_FACE_POSITIVE_X"></span><span id="d3dcubemap_face_positive_x"></span>**D3DCUBEMAP\_FACE\_POSITIVE\_X**</span></span>
</dt> <dd>

<span data-ttu-id="fd694-108">Положительный x-face кубической карты.</span><span class="sxs-lookup"><span data-stu-id="fd694-108">Positive x-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="fd694-109"><span id="D3DCUBEMAP_FACE_NEGATIVE_X"></span><span id="d3dcubemap_face_negative_x"></span>**D3DCUBEMAP \_ лицевой стороны \_ минус \_ X**</span><span class="sxs-lookup"><span data-stu-id="fd694-109"><span id="D3DCUBEMAP_FACE_NEGATIVE_X"></span><span id="d3dcubemap_face_negative_x"></span>**D3DCUBEMAP\_FACE\_NEGATIVE\_X**</span></span>
</dt> <dd>

<span data-ttu-id="fd694-110">Отрицательное значение x-face кубической карты.</span><span class="sxs-lookup"><span data-stu-id="fd694-110">Negative x-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="fd694-111"><span id="D3DCUBEMAP_FACE_POSITIVE_Y"></span><span id="d3dcubemap_face_positive_y"></span>**D3DCUBEMAP \_ лицо \_ плюс \_ Y**</span><span class="sxs-lookup"><span data-stu-id="fd694-111"><span id="D3DCUBEMAP_FACE_POSITIVE_Y"></span><span id="d3dcubemap_face_positive_y"></span>**D3DCUBEMAP\_FACE\_POSITIVE\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="fd694-112">Положительный y-лицо кубической карты.</span><span class="sxs-lookup"><span data-stu-id="fd694-112">Positive y-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="fd694-113"><span id="D3DCUBEMAP_FACE_NEGATIVE_Y"></span><span id="d3dcubemap_face_negative_y"></span>**D3DCUBEMAP \_ лицевой стороны, \_ отрицательный \_ Y**</span><span class="sxs-lookup"><span data-stu-id="fd694-113"><span id="D3DCUBEMAP_FACE_NEGATIVE_Y"></span><span id="d3dcubemap_face_negative_y"></span>**D3DCUBEMAP\_FACE\_NEGATIVE\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="fd694-114">Отрицательный y-Face кубической карты.</span><span class="sxs-lookup"><span data-stu-id="fd694-114">Negative y-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="fd694-115"><span id="D3DCUBEMAP_FACE_POSITIVE_Z"></span><span id="d3dcubemap_face_positive_z"></span>**D3DCUBEMAP \_ лицо \_ плюс \_ Z**</span><span class="sxs-lookup"><span data-stu-id="fd694-115"><span id="D3DCUBEMAP_FACE_POSITIVE_Z"></span><span id="d3dcubemap_face_positive_z"></span>**D3DCUBEMAP\_FACE\_POSITIVE\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="fd694-116">Положительное z-лицо кубической карты.</span><span class="sxs-lookup"><span data-stu-id="fd694-116">Positive z-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="fd694-117"><span id="D3DCUBEMAP_FACE_NEGATIVE_Z"></span><span id="d3dcubemap_face_negative_z"></span>**D3DCUBEMAP \_ лицевой стороны \_ минус \_ Z**</span><span class="sxs-lookup"><span data-stu-id="fd694-117"><span id="D3DCUBEMAP_FACE_NEGATIVE_Z"></span><span id="d3dcubemap_face_negative_z"></span>**D3DCUBEMAP\_FACE\_NEGATIVE\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="fd694-118">Отрицательное z-лицо кубической карты.</span><span class="sxs-lookup"><span data-stu-id="fd694-118">Negative z-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="fd694-119"><span id="D3DCUBEMAP_FACE_FORCE_DWORD"></span><span id="d3dcubemap_face_force_dword"></span>**D3DCUBEMAP «Force», \_ \_ \_ параметр DWORD**</span><span class="sxs-lookup"><span data-stu-id="fd694-119"><span id="D3DCUBEMAP_FACE_FORCE_DWORD"></span><span id="d3dcubemap_face_force_dword"></span>**D3DCUBEMAP\_FACE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="fd694-120">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="fd694-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="fd694-121">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="fd694-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="fd694-122">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="fd694-122">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd694-123">Требования</span><span class="sxs-lookup"><span data-stu-id="fd694-123">Requirements</span></span>



| <span data-ttu-id="fd694-124">Требование</span><span class="sxs-lookup"><span data-stu-id="fd694-124">Requirement</span></span> | <span data-ttu-id="fd694-125">Значение</span><span class="sxs-lookup"><span data-stu-id="fd694-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd694-126">Header</span><span class="sxs-lookup"><span data-stu-id="fd694-126">Header</span></span><br/> | <dl> <span data-ttu-id="fd694-127"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd694-127"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd694-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd694-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd694-129">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="fd694-129">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="fd694-130">**IDirect3DCubeTexture9:: Адддиртирект**</span><span class="sxs-lookup"><span data-stu-id="fd694-130">**IDirect3DCubeTexture9::AddDirtyRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-adddirtyrect)
</dt> <dt>

[<span data-ttu-id="fd694-131">**IDirect3DCubeTexture9:: Жеткубемапсурфаце**</span><span class="sxs-lookup"><span data-stu-id="fd694-131">**IDirect3DCubeTexture9::GetCubeMapSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
</dt> <dt>

[<span data-ttu-id="fd694-132">**IDirect3DCubeTexture9:: Локкрект**</span><span class="sxs-lookup"><span data-stu-id="fd694-132">**IDirect3DCubeTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="fd694-133">**IDirect3DCubeTexture9:: Унлоккрект**</span><span class="sxs-lookup"><span data-stu-id="fd694-133">**IDirect3DCubeTexture9::UnlockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-unlockrect)
</dt> </dl>

 

 
