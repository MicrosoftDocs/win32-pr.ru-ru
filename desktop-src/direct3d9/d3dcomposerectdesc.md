---
description: Задает прямоугольник, используемый для заключения глифов в монохромную поверхность.
ms.assetid: ce5d492f-38d1-4e7b-a9c2-68c791c84d0c
title: Структура D3DCOMPOSERECTDESC (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cf9ad5f1c075f4dc52d68b894b37c7d0f0a7b310
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424346"
---
# <a name="d3dcomposerectdesc-structure"></a><span data-ttu-id="84af9-103">Структура D3DCOMPOSERECTDESC</span><span class="sxs-lookup"><span data-stu-id="84af9-103">D3DCOMPOSERECTDESC structure</span></span>

<span data-ttu-id="84af9-104">Задает прямоугольник, используемый для заключения глифов в монохромную поверхность.</span><span class="sxs-lookup"><span data-stu-id="84af9-104">Specifies the rectangle used to enclose glyphs on a monochrome surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="84af9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84af9-105">Syntax</span></span>


```C++
typedef struct _D3DCOMPOSERECTDESC {
  USHORT X;
  USHORT Y;
  USHORT Width;
  USHORT Height;
} D3DCOMPOSERECTDESC;
```



## <a name="members"></a><span data-ttu-id="84af9-106">Члены</span><span class="sxs-lookup"><span data-stu-id="84af9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="84af9-107">**X**</span><span class="sxs-lookup"><span data-stu-id="84af9-107">**X**</span></span>
</dt> <dd>

<span data-ttu-id="84af9-108">Тип: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84af9-108">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="84af9-109">Левая координата начинается копирование в.</span><span class="sxs-lookup"><span data-stu-id="84af9-109">Left coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="84af9-110">**да**</span><span class="sxs-lookup"><span data-stu-id="84af9-110">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="84af9-111">Тип: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84af9-111">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="84af9-112">Верхняя координата, с которой начинается копирование.</span><span class="sxs-lookup"><span data-stu-id="84af9-112">Top coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="84af9-113">**Width**</span><span class="sxs-lookup"><span data-stu-id="84af9-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="84af9-114">Тип: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84af9-114">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="84af9-115">Число пикселей текстуры от левой координаты.</span><span class="sxs-lookup"><span data-stu-id="84af9-115">Number of texels from left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="84af9-116">**Height**</span><span class="sxs-lookup"><span data-stu-id="84af9-116">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="84af9-117">Тип: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84af9-117">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="84af9-118">Число пикселей текстуры от верхней координаты.</span><span class="sxs-lookup"><span data-stu-id="84af9-118">Number of texels from the top coordinate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84af9-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84af9-119">Remarks</span></span>

<span data-ttu-id="84af9-120">Эта структура используется в вызовах [**компосеректс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) для заключения глифов в исходную область.</span><span class="sxs-lookup"><span data-stu-id="84af9-120">This structure is used in calls to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) to enclose glyphs on the source surface.</span></span> <span data-ttu-id="84af9-121">Буфер вершин (см. [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)), заполненный этими структурами, создается для хранения расположений глифов.</span><span class="sxs-lookup"><span data-stu-id="84af9-121">A vertex buffer (see [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) filled with these structures are created to contain the glyph locations.</span></span> <span data-ttu-id="84af9-122">Элементы USHORT используются для уменьшения объема памяти, насколько это возможно.</span><span class="sxs-lookup"><span data-stu-id="84af9-122">USHORT members are used to reduce the memory footprint as much as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="84af9-123">Требования</span><span class="sxs-lookup"><span data-stu-id="84af9-123">Requirements</span></span>



| <span data-ttu-id="84af9-124">Требование</span><span class="sxs-lookup"><span data-stu-id="84af9-124">Requirement</span></span> | <span data-ttu-id="84af9-125">Значение</span><span class="sxs-lookup"><span data-stu-id="84af9-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="84af9-126">Header</span><span class="sxs-lookup"><span data-stu-id="84af9-126">Header</span></span><br/> | <dl> <span data-ttu-id="84af9-127"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="84af9-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84af9-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84af9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84af9-129">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="84af9-129">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
