---
description: Задает исходный глиф и расположение в монохромной поверхности, в которую копируются глифы.
ms.assetid: eda6fc82-6a06-4a59-a3ab-9f7e5c5bb5a1
title: Структура D3DCOMPOSERECTDESTINATION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESTINATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 56843bc78943a4c76fe4fe0f5e18242728a979c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713570"
---
# <a name="d3dcomposerectdestination-structure"></a><span data-ttu-id="9abd1-103">Структура D3DCOMPOSERECTDESTINATION</span><span class="sxs-lookup"><span data-stu-id="9abd1-103">D3DCOMPOSERECTDESTINATION structure</span></span>

<span data-ttu-id="9abd1-104">Задает исходный глиф и расположение в монохромной поверхности, в которую копируются глифы.</span><span class="sxs-lookup"><span data-stu-id="9abd1-104">Specifies the source glyph and location in a monochrome surface to copy glyphs into.</span></span>

## <a name="syntax"></a><span data-ttu-id="9abd1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9abd1-105">Syntax</span></span>


```C++
typedef struct _D3DCOMPOSERECTDESTINATION {
  USHORT SrcRectIndex;
  USHORT Reserved;
  USHORT X;
  USHORT Y;
} D3DCOMPOSERECTDESTINATION;
```



## <a name="members"></a><span data-ttu-id="9abd1-106">Члены</span><span class="sxs-lookup"><span data-stu-id="9abd1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9abd1-107">**сркректиндекс**</span><span class="sxs-lookup"><span data-stu-id="9abd1-107">**SrcRectIndex**</span></span>
</dt> <dd>

<span data-ttu-id="9abd1-108">Тип: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9abd1-108">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9abd1-109">Определенный индексом глиф из буфера вершин, содержащего структуры [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) .</span><span class="sxs-lookup"><span data-stu-id="9abd1-109">Index particular glyph from vertex buffer containing [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="9abd1-110">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="9abd1-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="9abd1-111">Тип: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9abd1-111">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9abd1-112">Зарезервировано для целей выравнивания.</span><span class="sxs-lookup"><span data-stu-id="9abd1-112">Reserved for alignment purposes.</span></span>

</dd> <dt>

<span data-ttu-id="9abd1-113">**X**</span><span class="sxs-lookup"><span data-stu-id="9abd1-113">**X**</span></span>
</dt> <dd>

<span data-ttu-id="9abd1-114">Тип: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9abd1-114">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9abd1-115">Левая координата начинается копирование в.</span><span class="sxs-lookup"><span data-stu-id="9abd1-115">Left coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="9abd1-116">**да**</span><span class="sxs-lookup"><span data-stu-id="9abd1-116">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="9abd1-117">Тип: **[ **UShort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9abd1-117">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9abd1-118">Верхняя координата, с которой начинается копирование.</span><span class="sxs-lookup"><span data-stu-id="9abd1-118">Top coordinate to begin copy at.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9abd1-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9abd1-119">Remarks</span></span>

<span data-ttu-id="9abd1-120">Эта структура используется в вызовах [**компосеректс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) , чтобы указать, куда должны копироваться глифы расположения и какой именно глиф следует копировать.</span><span class="sxs-lookup"><span data-stu-id="9abd1-120">This structure is used in calls to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) to indicate the location glyphs should be copied to and which particular glyph should be copied.</span></span> <span data-ttu-id="9abd1-121">Буфер вершин (см. [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)), заполненный этими структурами, создается для хранения расположений глифов.</span><span class="sxs-lookup"><span data-stu-id="9abd1-121">A vertex buffer (see [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) filled with these structures are created to contain the glyph locations.</span></span> <span data-ttu-id="9abd1-122">Элементы USHORT используются для уменьшения объема памяти, насколько это возможно.</span><span class="sxs-lookup"><span data-stu-id="9abd1-122">USHORT members are used to reduce the memory footprint as much as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="9abd1-123">Требования</span><span class="sxs-lookup"><span data-stu-id="9abd1-123">Requirements</span></span>



| <span data-ttu-id="9abd1-124">Требование</span><span class="sxs-lookup"><span data-stu-id="9abd1-124">Requirement</span></span> | <span data-ttu-id="9abd1-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9abd1-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9abd1-126">Header</span><span class="sxs-lookup"><span data-stu-id="9abd1-126">Header</span></span><br/> | <dl> <span data-ttu-id="9abd1-127"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9abd1-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9abd1-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9abd1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9abd1-129">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="9abd1-129">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
