---
description: Определяет макет данных вершин. Каждая вершина может содержать один или несколько типов данных, и каждый тип данных описывается элементом вершины.
ms.assetid: 6f3c40a0-b28e-48d6-acad-ef80a919c5d7
title: Структура D3DVERTEXELEMENT9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXELEMENT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e6c5e9508185124673ca7464b31d741cdf8035c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664983"
---
# <a name="d3dvertexelement9-structure"></a><span data-ttu-id="6c687-104">Структура D3DVERTEXELEMENT9</span><span class="sxs-lookup"><span data-stu-id="6c687-104">D3DVERTEXELEMENT9 structure</span></span>

<span data-ttu-id="6c687-105">Определяет макет данных вершин.</span><span class="sxs-lookup"><span data-stu-id="6c687-105">Defines the vertex data layout.</span></span> <span data-ttu-id="6c687-106">Каждая вершина может содержать один или несколько типов данных, и каждый тип данных описывается элементом вершины.</span><span class="sxs-lookup"><span data-stu-id="6c687-106">Each vertex can contain one or more data types, and each data type is described by a vertex element.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c687-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c687-107">Syntax</span></span>


```C++
typedef struct D3DVERTEXELEMENT9 {
  WORD Stream;
  WORD Offset;
  BYTE Type;
  BYTE Method;
  BYTE Usage;
  BYTE UsageIndex;
} D3DVERTEXELEMENT9, *LPD3DVERTEXELEMENT9;
```



## <a name="members"></a><span data-ttu-id="6c687-108">Члены</span><span class="sxs-lookup"><span data-stu-id="6c687-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6c687-109">**Stream**</span><span class="sxs-lookup"><span data-stu-id="6c687-109">**Stream**</span></span>
</dt> <dd>

<span data-ttu-id="6c687-110">Тип: **[ **слово**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c687-110">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6c687-111">Номер потока.</span><span class="sxs-lookup"><span data-stu-id="6c687-111">Stream number.</span></span>

</dd> <dt>

<span data-ttu-id="6c687-112">**Offset**</span><span class="sxs-lookup"><span data-stu-id="6c687-112">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="6c687-113">Тип: **[ **слово**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c687-113">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6c687-114">Смещение от начала данных вершины до данных, связанных с определенным типом данных.</span><span class="sxs-lookup"><span data-stu-id="6c687-114">Offset from the beginning of the vertex data to the data associated with the particular data type.</span></span>

</dd> <dt>

<span data-ttu-id="6c687-115">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6c687-115">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="6c687-116">Тип: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c687-116">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6c687-117">Тип данных, указанный как [**D3DDECLTYPE**](./d3ddecltype.md).</span><span class="sxs-lookup"><span data-stu-id="6c687-117">The data type, specified as a [**D3DDECLTYPE**](./d3ddecltype.md).</span></span> <span data-ttu-id="6c687-118">Один из нескольких предопределенных типов, определяющих размер данных.</span><span class="sxs-lookup"><span data-stu-id="6c687-118">One of several predefined types that define the data size.</span></span> <span data-ttu-id="6c687-119">Некоторые методы имеют неявный тип.</span><span class="sxs-lookup"><span data-stu-id="6c687-119">Some methods have an implied type.</span></span>

</dd> <dt>

<span data-ttu-id="6c687-120">**Метод**</span><span class="sxs-lookup"><span data-stu-id="6c687-120">**Method**</span></span>
</dt> <dd>

<span data-ttu-id="6c687-121">Тип: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c687-121">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6c687-122">Метод задает обработку тесселяции, которая определяет способ интерпретации (или обработки) данных вершин.</span><span class="sxs-lookup"><span data-stu-id="6c687-122">The method specifies the tessellator processing, which determines how the tessellator interprets (or operates on) the vertex data.</span></span> <span data-ttu-id="6c687-123">Дополнительные сведения см. в разделе [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span><span class="sxs-lookup"><span data-stu-id="6c687-123">For more information, see [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c687-124">**Использование**</span><span class="sxs-lookup"><span data-stu-id="6c687-124">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="6c687-125">Тип: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c687-125">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6c687-126">Определяет, для каких данных будут использоваться данные; то есть взаимодействие между макетами данных вершин и шейдерами вершин.</span><span class="sxs-lookup"><span data-stu-id="6c687-126">Defines what the data will be used for; that is, the interoperability between vertex data layouts and vertex shaders.</span></span> <span data-ttu-id="6c687-127">Каждое использование служит для привязки объявления вершины к шейдеру вершин.</span><span class="sxs-lookup"><span data-stu-id="6c687-127">Each usage acts to bind a vertex declaration to a vertex shader.</span></span> <span data-ttu-id="6c687-128">В некоторых случаях они имеют специальную интерпретацию.</span><span class="sxs-lookup"><span data-stu-id="6c687-128">In some cases, they have a special interpretation.</span></span> <span data-ttu-id="6c687-129">Например, элемент, указывающий D3DDECLUSAGE \_ нормаль или D3DDECLUSAGE, \_ используется тесселяцией N-patch для настройки тесселяции.</span><span class="sxs-lookup"><span data-stu-id="6c687-129">For example, an element that specifies D3DDECLUSAGE\_NORMAL or D3DDECLUSAGE\_POSITION is used by the N-patch tessellator to set up tessellation.</span></span> <span data-ttu-id="6c687-130">Список доступных семантик см. в разделе [**D3DDECLUSAGE**](./d3ddeclusage.md) .</span><span class="sxs-lookup"><span data-stu-id="6c687-130">See [**D3DDECLUSAGE**](./d3ddeclusage.md) for a list of the available semantics.</span></span> <span data-ttu-id="6c687-131">D3DDECLUSAGE \_ текскурд можно использовать для определяемых пользователем полей (для которых не определено использование).</span><span class="sxs-lookup"><span data-stu-id="6c687-131">D3DDECLUSAGE\_TEXCOORD can be used for user-defined fields (which don't have an existing usage defined).</span></span>

</dd> <dt>

<span data-ttu-id="6c687-132">**усажеиндекс**</span><span class="sxs-lookup"><span data-stu-id="6c687-132">**UsageIndex**</span></span>
</dt> <dd>

<span data-ttu-id="6c687-133">Тип: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c687-133">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6c687-134">Изменяет данные об использовании, чтобы разрешить пользователю указывать несколько типов использования.</span><span class="sxs-lookup"><span data-stu-id="6c687-134">Modifies the usage data to allow the user to specify multiple usage types.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c687-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c687-135">Remarks</span></span>

<span data-ttu-id="6c687-136">Данные вершин определяются с помощью массива структур **D3DVERTEXELEMENT9** .</span><span class="sxs-lookup"><span data-stu-id="6c687-136">Vertex data is defined using an array of **D3DVERTEXELEMENT9** structures.</span></span> <span data-ttu-id="6c687-137">Используйте [**D3DDECL \_ End**](d3ddecl-end.md) , чтобы объявить последний элемент в объявлении.</span><span class="sxs-lookup"><span data-stu-id="6c687-137">Use [**D3DDECL\_END**](d3ddecl-end.md) to declare the last element in the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c687-138">Требования</span><span class="sxs-lookup"><span data-stu-id="6c687-138">Requirements</span></span>



| <span data-ttu-id="6c687-139">Требование</span><span class="sxs-lookup"><span data-stu-id="6c687-139">Requirement</span></span> | <span data-ttu-id="6c687-140">Значение</span><span class="sxs-lookup"><span data-stu-id="6c687-140">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c687-141">Header</span><span class="sxs-lookup"><span data-stu-id="6c687-141">Header</span></span><br/> | <dl> <span data-ttu-id="6c687-142"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c687-142"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c687-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c687-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c687-144">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="6c687-144">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="6c687-145">Объявление вершины (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6c687-145">Vertex Declaration (Direct3D 9)</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
