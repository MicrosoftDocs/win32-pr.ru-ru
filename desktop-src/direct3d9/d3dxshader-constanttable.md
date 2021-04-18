---
description: Вспомогательная структура для управления таблицей констант шейдера. Это также можно сделать с помощью ID3DXConstantTable.
ms.assetid: cc6d66e4-c600-420b-b7b5-1bd10ecb22f9
title: Структура D3DXSHADER_CONSTANTTABLE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTTABLE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: ef4fe6cf9af924d9ae6c358f72bf49f93d85f29d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713646"
---
# <a name="d3dxshader_constanttable-structure"></a><span data-ttu-id="873d5-104">\_Структура КОНСТАНТТАБЛЕ D3DXSHADER</span><span class="sxs-lookup"><span data-stu-id="873d5-104">D3DXSHADER\_CONSTANTTABLE structure</span></span>

<span data-ttu-id="873d5-105">Вспомогательная структура для управления таблицей констант шейдера.</span><span class="sxs-lookup"><span data-stu-id="873d5-105">Helper structure for managing a shader constant table.</span></span> <span data-ttu-id="873d5-106">Это также можно сделать с помощью [**ID3DXConstantTable**](id3dxconstanttable.md).</span><span class="sxs-lookup"><span data-stu-id="873d5-106">This can also be done using [**ID3DXConstantTable**](id3dxconstanttable.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="873d5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="873d5-107">Syntax</span></span>


```C++
typedef struct D3DXSHADER_CONSTANTTABLE {
  DWORD Size;
  DWORD Creator;
  DWORD Version;
  DWORD Constants;
  DWORD ConstantInfo;
  DWORD Flags;
  DWORD Target;
} D3DXSHADER_CONSTANTTABLE, *LPD3DXSHADER_CONSTANTTABLE;
```



## <a name="members"></a><span data-ttu-id="873d5-108">Члены</span><span class="sxs-lookup"><span data-stu-id="873d5-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="873d5-109">**Размер**</span><span class="sxs-lookup"><span data-stu-id="873d5-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="873d5-110">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="873d5-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="873d5-111">Размер структуры.</span><span class="sxs-lookup"><span data-stu-id="873d5-111">Size of the structure.</span></span> <span data-ttu-id="873d5-112">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="873d5-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="873d5-113">**Автор**</span><span class="sxs-lookup"><span data-stu-id="873d5-113">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="873d5-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="873d5-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="873d5-115">Смещение от начала этой структуры (в байтах) к строке, содержащей имя создателя.</span><span class="sxs-lookup"><span data-stu-id="873d5-115">Offset from the beginning of this structure, in bytes, to the string that contains the name of the creator.</span></span>

</dd> <dt>

<span data-ttu-id="873d5-116">**Version**</span><span class="sxs-lookup"><span data-stu-id="873d5-116">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="873d5-117">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="873d5-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="873d5-118">Версия шейдера.</span><span class="sxs-lookup"><span data-stu-id="873d5-118">Shader version.</span></span>

</dd> <dt>

<span data-ttu-id="873d5-119">**Константы**</span><span class="sxs-lookup"><span data-stu-id="873d5-119">**Constants**</span></span>
</dt> <dd>

<span data-ttu-id="873d5-120">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="873d5-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="873d5-121">Число констант.</span><span class="sxs-lookup"><span data-stu-id="873d5-121">Number of constants.</span></span>

</dd> <dt>

<span data-ttu-id="873d5-122">**константинфо**</span><span class="sxs-lookup"><span data-stu-id="873d5-122">**ConstantInfo**</span></span>
</dt> <dd>

<span data-ttu-id="873d5-123">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="873d5-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="873d5-124">Массив константных данных, \_ \[ *константы* D3DXSHADER константинфо \] .</span><span class="sxs-lookup"><span data-stu-id="873d5-124">Array of constant information, D3DXSHADER\_CONSTANTINFO\[*Constants*\].</span></span> <span data-ttu-id="873d5-125">См. раздел [**D3DXSHADER \_ константинфо**](d3dxshader-constantinfo.md).</span><span class="sxs-lookup"><span data-stu-id="873d5-125">See [**D3DXSHADER\_CONSTANTINFO**](d3dxshader-constantinfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="873d5-126">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="873d5-126">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="873d5-127">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="873d5-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="873d5-128">Флаги [флагов D3DXSHADER](d3dxshader-flags.md) , используемые для компиляции шейдера.</span><span class="sxs-lookup"><span data-stu-id="873d5-128">The [D3DXSHADER Flags](d3dxshader-flags.md) flags used to compile the shader.</span></span>

</dd> <dt>

<span data-ttu-id="873d5-129">**Целевой объект**</span><span class="sxs-lookup"><span data-stu-id="873d5-129">**Target**</span></span>
</dt> <dd>

<span data-ttu-id="873d5-130">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="873d5-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="873d5-131">Смещение в строке, содержащей целевой объект.</span><span class="sxs-lookup"><span data-stu-id="873d5-131">Offset into the string that contains the target.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="873d5-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="873d5-132">Remarks</span></span>

<span data-ttu-id="873d5-133">Сведения о константах шейдера включаются в таблицу комментариев, разделенных табуляцией.</span><span class="sxs-lookup"><span data-stu-id="873d5-133">Shader constant information is included in a tab-delimited table of comments.</span></span> <span data-ttu-id="873d5-134">Все смещения измеряются в байтах от начала структуры.</span><span class="sxs-lookup"><span data-stu-id="873d5-134">All offsets are measured in bytes from the beginning of the structure.</span></span> <span data-ttu-id="873d5-135">Записи в таблице констант сортируются по автору в возрастающем порядке.</span><span class="sxs-lookup"><span data-stu-id="873d5-135">Entries in the constant table are sorted by Creator in ascending order.</span></span>

<span data-ttu-id="873d5-136">С помощью интерфейсов [**ID3DXConstantTable**](id3dxconstanttable.md) можно управлять таблицей констант шейдера.</span><span class="sxs-lookup"><span data-stu-id="873d5-136">A shader constant table can be managed with the [**ID3DXConstantTable**](id3dxconstanttable.md) interfaces.</span></span> <span data-ttu-id="873d5-137">Кроме того, можно управлять таблицей констант с помощью **D3DXSHADER \_ константтабле**.</span><span class="sxs-lookup"><span data-stu-id="873d5-137">Alternatively, you can manage the constant table with **D3DXSHADER\_CONSTANTTABLE**.</span></span>

<span data-ttu-id="873d5-138">Этот элемент размера часто инициализируется с помощью следующего:</span><span class="sxs-lookup"><span data-stu-id="873d5-138">This size member is often initialized using the following:</span></span>


```
D3DXSHADER_CONSTANTTABLE constantTable;
constantTable.Size = sizeof(D3DXSHADER_CONSTANTTABLE)
```



## <a name="requirements"></a><span data-ttu-id="873d5-139">Требования</span><span class="sxs-lookup"><span data-stu-id="873d5-139">Requirements</span></span>



| <span data-ttu-id="873d5-140">Требование</span><span class="sxs-lookup"><span data-stu-id="873d5-140">Requirement</span></span> | <span data-ttu-id="873d5-141">Значение</span><span class="sxs-lookup"><span data-stu-id="873d5-141">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="873d5-142">Header</span><span class="sxs-lookup"><span data-stu-id="873d5-142">Header</span></span><br/> | <dl> <span data-ttu-id="873d5-143"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="873d5-143"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="873d5-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="873d5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="873d5-145">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="873d5-145">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="873d5-146">**D3DXGetShaderConstantTable**</span><span class="sxs-lookup"><span data-stu-id="873d5-146">**D3DXGetShaderConstantTable**</span></span>](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
