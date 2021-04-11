---
description: Вспомогательная структура, содержащая сведения о типе элемента.
ms.assetid: 5580122d-c700-4632-8fcf-903519f2429e
title: Структура D3DXSHADER_TYPEINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_TYPEINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 71b9cc893cdcfdc9802aca173627cd9da4f9ca4b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354713"
---
# <a name="d3dxshader_typeinfo-structure"></a><span data-ttu-id="c5ccd-103">\_Структура TYPEINFO D3DXSHADER</span><span class="sxs-lookup"><span data-stu-id="c5ccd-103">D3DXSHADER\_TYPEINFO structure</span></span>

<span data-ttu-id="c5ccd-104">Вспомогательная структура, содержащая сведения о типе элемента.</span><span class="sxs-lookup"><span data-stu-id="c5ccd-104">A helper structure containing member type information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ccd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5ccd-105">Syntax</span></span>


```C++
typedef struct D3DXSHADER_TYPEINFO {
  WORD  Class;
  WORD  Type;
  WORD  Rows;
  WORD  Columns;
  WORD  Elements;
  WORD  StructMembers;
  DWORD StructMemberInfo;
} D3DXSHADER_TYPEINFO, *LPD3DXSHADER_TYPEINFO;
```



## <a name="members"></a><span data-ttu-id="c5ccd-106">Члены</span><span class="sxs-lookup"><span data-stu-id="c5ccd-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c5ccd-107">**Класс**</span><span class="sxs-lookup"><span data-stu-id="c5ccd-107">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="c5ccd-108">Тип: **[ **слово**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5ccd-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c5ccd-109">Тип объекта шейдера.</span><span class="sxs-lookup"><span data-stu-id="c5ccd-109">Shader object type.</span></span> <span data-ttu-id="c5ccd-110">См. раздел [**\_ класс D3DXPARAMETER**](./d3dxparameter-class.md).</span><span class="sxs-lookup"><span data-stu-id="c5ccd-110">See [**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5ccd-111">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c5ccd-111">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="c5ccd-112">Тип: **[ **слово**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5ccd-112">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c5ccd-113">Тип данных.</span><span class="sxs-lookup"><span data-stu-id="c5ccd-113">Data type.</span></span> <span data-ttu-id="c5ccd-114">См. раздел [**\_ тип D3DXPARAMETER**](./d3dxparameter-type.md).</span><span class="sxs-lookup"><span data-stu-id="c5ccd-114">See [**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5ccd-115">**Строки**</span><span class="sxs-lookup"><span data-stu-id="c5ccd-115">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="c5ccd-116">Тип: **[ **слово**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5ccd-116">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c5ccd-117">Число строк матрицы (матрицы).</span><span class="sxs-lookup"><span data-stu-id="c5ccd-117">Number of matrix rows (matrices).</span></span>

</dd> <dt>

<span data-ttu-id="c5ccd-118">**Столбцы**</span><span class="sxs-lookup"><span data-stu-id="c5ccd-118">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="c5ccd-119">Тип: **[ **слово**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5ccd-119">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c5ccd-120">Число столбцов (векторов и матриц).</span><span class="sxs-lookup"><span data-stu-id="c5ccd-120">Number of columns (vectors and matrices).</span></span>

</dd> <dt>

<span data-ttu-id="c5ccd-121">**Elements (XElement Dynamic Property)** (Elements (Динамическое свойство XElement))</span><span class="sxs-lookup"><span data-stu-id="c5ccd-121">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="c5ccd-122">Тип: **[ **слово**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5ccd-122">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c5ccd-123">Измерение массива.</span><span class="sxs-lookup"><span data-stu-id="c5ccd-123">Array dimension.</span></span>

</dd> <dt>

<span data-ttu-id="c5ccd-124">**структмемберс**</span><span class="sxs-lookup"><span data-stu-id="c5ccd-124">**StructMembers**</span></span>
</dt> <dd>

<span data-ttu-id="c5ccd-125">Тип: **[ **слово**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5ccd-125">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c5ccd-126">Число элементов структуры.</span><span class="sxs-lookup"><span data-stu-id="c5ccd-126">Number of structure members.</span></span>

</dd> <dt>

<span data-ttu-id="c5ccd-127">**структмемберинфо**</span><span class="sxs-lookup"><span data-stu-id="c5ccd-127">**StructMemberInfo**</span></span>
</dt> <dd>

<span data-ttu-id="c5ccd-128">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5ccd-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c5ccd-129">Массив сведений о члене структуры, D3DXSHADER \_ структмемберинфо \[ *структмемберс* \] .</span><span class="sxs-lookup"><span data-stu-id="c5ccd-129">Array of structure member information, D3DXSHADER\_STRUCTMEMBERINFO\[*StructMembers*\].</span></span> <span data-ttu-id="c5ccd-130">См. раздел [**D3DXSHADER \_ структмемберинфо**](d3dxshader-structmemberinfo.md).</span><span class="sxs-lookup"><span data-stu-id="c5ccd-130">See [**D3DXSHADER\_STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5ccd-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c5ccd-131">Remarks</span></span>

<span data-ttu-id="c5ccd-132">Сведения о типе являются частью [**D3DXSHADER \_ структмемберинфо**](d3dxshader-structmemberinfo.md).</span><span class="sxs-lookup"><span data-stu-id="c5ccd-132">The type information is part of [**D3DXSHADER\_STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ccd-133">Требования</span><span class="sxs-lookup"><span data-stu-id="c5ccd-133">Requirements</span></span>



| <span data-ttu-id="c5ccd-134">Требование</span><span class="sxs-lookup"><span data-stu-id="c5ccd-134">Requirement</span></span> | <span data-ttu-id="c5ccd-135">Значение</span><span class="sxs-lookup"><span data-stu-id="c5ccd-135">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ccd-136">Header</span><span class="sxs-lookup"><span data-stu-id="c5ccd-136">Header</span></span><br/> | <dl> <span data-ttu-id="c5ccd-137"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5ccd-137"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5ccd-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5ccd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ccd-139">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="c5ccd-139">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="c5ccd-140">**D3DXSHADER \_ константинфо**</span><span class="sxs-lookup"><span data-stu-id="c5ccd-140">**D3DXSHADER\_CONSTANTINFO**</span></span>](d3dxshader-constantinfo.md)
</dt> </dl>

 

 
