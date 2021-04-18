---
description: Хранит запись таблицы атрибутов.
ms.assetid: 81c77dc9-e078-46a1-a435-4b241e36ec13
title: Структура D3DX10_ATTRIBUTE_RANGE (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_RANGE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: ddf7f10882e08232467130b3abbc6fb723a843ed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713914"
---
# <a name="d3dx10_attribute_range-structure"></a><span data-ttu-id="075ec-103">\_ \_ Структура диапазона атрибутов D3DX10</span><span class="sxs-lookup"><span data-stu-id="075ec-103">D3DX10\_ATTRIBUTE\_RANGE structure</span></span>

<span data-ttu-id="075ec-104">Хранит запись таблицы атрибутов.</span><span class="sxs-lookup"><span data-stu-id="075ec-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="075ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="075ec-105">Syntax</span></span>


```C++
typedef struct D3DX10_ATTRIBUTE_RANGE {
  UINT AttribId;
  UINT FaceStart;
  UINT FaceCount;
  UINT VertexStart;
  UINT VertexCount;
} D3DX10_ATTRIBUTE_RANGE, *LPD3DX10_ATTRIBUTE_RANGE;
```



## <a name="members"></a><span data-ttu-id="075ec-106">Члены</span><span class="sxs-lookup"><span data-stu-id="075ec-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="075ec-107">**аттрибид**</span><span class="sxs-lookup"><span data-stu-id="075ec-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="075ec-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="075ec-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="075ec-109">Идентификатор таблицы атрибутов.</span><span class="sxs-lookup"><span data-stu-id="075ec-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="075ec-110">**фацестарт**</span><span class="sxs-lookup"><span data-stu-id="075ec-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="075ec-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="075ec-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="075ec-112">Начальная поверхность.</span><span class="sxs-lookup"><span data-stu-id="075ec-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="075ec-113">**фацекаунт**</span><span class="sxs-lookup"><span data-stu-id="075ec-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="075ec-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="075ec-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="075ec-115">Число лиц.</span><span class="sxs-lookup"><span data-stu-id="075ec-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="075ec-116">**вертексстарт**</span><span class="sxs-lookup"><span data-stu-id="075ec-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="075ec-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="075ec-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="075ec-118">Начальная вершина.</span><span class="sxs-lookup"><span data-stu-id="075ec-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="075ec-119">**вертекскаунт**</span><span class="sxs-lookup"><span data-stu-id="075ec-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="075ec-120">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="075ec-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="075ec-121">Число вершин.</span><span class="sxs-lookup"><span data-stu-id="075ec-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="075ec-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="075ec-122">Remarks</span></span>

<span data-ttu-id="075ec-123">Таблица атрибутов используется для поиска областей сетки, которые должны рисоваться с разными текстурами, состояниями рендеринга, материалами и т. д.</span><span class="sxs-lookup"><span data-stu-id="075ec-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="075ec-124">Кроме того, приложение может использовать таблицу атрибутов для скрытия частей сетки, не рисуя заданный идентификатор атрибута (Аттрибид) при рисовании рамки.</span><span class="sxs-lookup"><span data-stu-id="075ec-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="075ec-125">\_ \_ Тип диапазона атрибута LPD3DX определяется как указатель на \_ \_ структуру диапазона атрибутов D3DX.</span><span class="sxs-lookup"><span data-stu-id="075ec-125">The LPD3DX\_ATTRIBUTE\_RANGE type is defined as a pointer to the D3DX\_ATTRIBUTE\_RANGE structure.</span></span>


```
typedef D3DX_ATTRIBUTE_RANGE* LPD3DX_ATTRIBUTE_RANGE;
```



## <a name="requirements"></a><span data-ttu-id="075ec-126">Требования</span><span class="sxs-lookup"><span data-stu-id="075ec-126">Requirements</span></span>



| <span data-ttu-id="075ec-127">Требование</span><span class="sxs-lookup"><span data-stu-id="075ec-127">Requirement</span></span> | <span data-ttu-id="075ec-128">Значение</span><span class="sxs-lookup"><span data-stu-id="075ec-128">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="075ec-129">Header</span><span class="sxs-lookup"><span data-stu-id="075ec-129">Header</span></span><br/> | <dl> <span data-ttu-id="075ec-130"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="075ec-130"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="075ec-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="075ec-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="075ec-132">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="075ec-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
