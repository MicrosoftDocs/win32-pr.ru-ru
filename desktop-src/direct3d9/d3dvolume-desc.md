---
description: Описывает том.
ms.assetid: c0224f4e-3d32-4bdd-b56c-4e8aa291bb27
title: Структура D3DVOLUME_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVOLUME_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b736333cefcfc8a3307ff7a0cecd53cd96bc0af2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355190"
---
# <a name="d3dvolume_desc-structure"></a><span data-ttu-id="79d7b-103">\_Структура D3DVOLUME DESC</span><span class="sxs-lookup"><span data-stu-id="79d7b-103">D3DVOLUME\_DESC structure</span></span>

<span data-ttu-id="79d7b-104">Описывает том.</span><span class="sxs-lookup"><span data-stu-id="79d7b-104">Describes a volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="79d7b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79d7b-105">Syntax</span></span>


```C++
typedef struct D3DVOLUME_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Width;
  UINT            Height;
  UINT            Depth;
} D3DVOLUME_DESC, *LPD3DVOLUME_DESC;
```



## <a name="members"></a><span data-ttu-id="79d7b-106">Члены</span><span class="sxs-lookup"><span data-stu-id="79d7b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="79d7b-107">**Формат**</span><span class="sxs-lookup"><span data-stu-id="79d7b-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="79d7b-108">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="79d7b-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="79d7b-109">Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий формат поверхности тома.</span><span class="sxs-lookup"><span data-stu-id="79d7b-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the volume.</span></span>

</dd> <dt>

<span data-ttu-id="79d7b-110">**Тип**</span><span class="sxs-lookup"><span data-stu-id="79d7b-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="79d7b-111">Тип: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="79d7b-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="79d7b-112">Член перечисляемого типа [**D3DRESOURCETYPE**](./d3dresourcetype.md) , который определяет этот ресурс как том.</span><span class="sxs-lookup"><span data-stu-id="79d7b-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as a volume.</span></span>

</dd> <dt>

<span data-ttu-id="79d7b-113">**Использование**</span><span class="sxs-lookup"><span data-stu-id="79d7b-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="79d7b-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79d7b-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="79d7b-115">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="79d7b-115">Currently not used.</span></span> <span data-ttu-id="79d7b-116">Всегда возвращает значение 0.</span><span class="sxs-lookup"><span data-stu-id="79d7b-116">Always returned as 0.</span></span>

</dd> <dt>

<span data-ttu-id="79d7b-117">**Пул.**</span><span class="sxs-lookup"><span data-stu-id="79d7b-117">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="79d7b-118">Тип: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="79d7b-118">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="79d7b-119">Член перечисляемого типа [**D3DPOOL**](./d3dpool.md) , указывающий класс памяти, выделенной для этого тома.</span><span class="sxs-lookup"><span data-stu-id="79d7b-119">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this volume.</span></span>

</dd> <dt>

<span data-ttu-id="79d7b-120">**Width**</span><span class="sxs-lookup"><span data-stu-id="79d7b-120">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="79d7b-121">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79d7b-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="79d7b-122">Ширина тома (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="79d7b-122">Width of the volume, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="79d7b-123">**Height**</span><span class="sxs-lookup"><span data-stu-id="79d7b-123">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="79d7b-124">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79d7b-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="79d7b-125">Высота тома (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="79d7b-125">Height of the volume, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="79d7b-126">**Depth**</span><span class="sxs-lookup"><span data-stu-id="79d7b-126">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="79d7b-127">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79d7b-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="79d7b-128">Глубина тома в пикселях.</span><span class="sxs-lookup"><span data-stu-id="79d7b-128">Depth of the volume, in pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79d7b-129">Требования</span><span class="sxs-lookup"><span data-stu-id="79d7b-129">Requirements</span></span>



| <span data-ttu-id="79d7b-130">Требование</span><span class="sxs-lookup"><span data-stu-id="79d7b-130">Requirement</span></span> | <span data-ttu-id="79d7b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="79d7b-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="79d7b-132">Header</span><span class="sxs-lookup"><span data-stu-id="79d7b-132">Header</span></span><br/> | <dl> <span data-ttu-id="79d7b-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="79d7b-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79d7b-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79d7b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79d7b-135">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="79d7b-135">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="79d7b-136">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="79d7b-136">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-getdesc)
</dt> <dt>

[<span data-ttu-id="79d7b-137">**жетлевелдеск**</span><span class="sxs-lookup"><span data-stu-id="79d7b-137">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-getleveldesc)
</dt> </dl>

 

 
