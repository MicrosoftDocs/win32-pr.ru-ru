---
description: Описывает параметр, используемый для объекта Effect.
ms.assetid: 60d19b52-67ef-4903-bbde-922a8fac1ad8
title: Структура D3DXPARAMETER_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 2256e24daa6dc8b6e5da1528e9a5e5aefce8ec99
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273701"
---
# <a name="d3dxparameter_desc-structure"></a><span data-ttu-id="a17da-103">\_Структура D3DXPARAMETER DESC</span><span class="sxs-lookup"><span data-stu-id="a17da-103">D3DXPARAMETER\_DESC structure</span></span>

<span data-ttu-id="a17da-104">Описывает параметр, используемый для объекта Effect.</span><span class="sxs-lookup"><span data-stu-id="a17da-104">Describes a parameter used for an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a17da-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a17da-105">Syntax</span></span>


```C++
typedef struct D3DXPARAMETER_DESC {
  LPCSTR              Name;
  LPCSTR              Semantic;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                Annotations;
  UINT                StructMembers;
  DWORD               Flags;
  UINT                Bytes;
} D3DXPARAMETER_DESC, *LPD3DXPARAMETER_DESC;
```



## <a name="members"></a><span data-ttu-id="a17da-106">Члены</span><span class="sxs-lookup"><span data-stu-id="a17da-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a17da-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="a17da-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="a17da-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a17da-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a17da-109">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="a17da-109">Name of the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a17da-110">**Семантическ**</span><span class="sxs-lookup"><span data-stu-id="a17da-110">**Semantic**</span></span>
</dt> <dd>

<span data-ttu-id="a17da-111">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a17da-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a17da-112">Семантическое значение, также называемое использованием.</span><span class="sxs-lookup"><span data-stu-id="a17da-112">Semantic meaning, also called the usage.</span></span>

</dd> <dt>

<span data-ttu-id="a17da-113">**Класс**</span><span class="sxs-lookup"><span data-stu-id="a17da-113">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="a17da-114">Тип: **[ **\_ класс D3DXPARAMETER**](./d3dxparameter-class.md)**</span><span class="sxs-lookup"><span data-stu-id="a17da-114">Type: **[**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a17da-115">Класс параметра.</span><span class="sxs-lookup"><span data-stu-id="a17da-115">Parameter class.</span></span> <span data-ttu-id="a17da-116">Задайте для этого параметра одно из значений в [**\_ классе D3DXPARAMETER**](./d3dxparameter-class.md).</span><span class="sxs-lookup"><span data-stu-id="a17da-116">Set this to one of the values in [**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="a17da-117">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a17da-117">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="a17da-118">Тип: **[ **D3DXPARAMETER \_ тип**](./d3dxparameter-type.md)**</span><span class="sxs-lookup"><span data-stu-id="a17da-118">Type: **[**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a17da-119">Тип параметра.</span><span class="sxs-lookup"><span data-stu-id="a17da-119">Parameter type.</span></span> <span data-ttu-id="a17da-120">Задайте для него одно из значений [**\_ типа D3DXPARAMETER**](./d3dxparameter-type.md).</span><span class="sxs-lookup"><span data-stu-id="a17da-120">Set this to one of the values in [**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="a17da-121">**Строки**</span><span class="sxs-lookup"><span data-stu-id="a17da-121">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="a17da-122">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a17da-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a17da-123">Количество строк в массиве.</span><span class="sxs-lookup"><span data-stu-id="a17da-123">Number of rows in the array.</span></span>

</dd> <dt>

<span data-ttu-id="a17da-124">**Столбцы**</span><span class="sxs-lookup"><span data-stu-id="a17da-124">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="a17da-125">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a17da-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a17da-126">Число столбцов в массиве.</span><span class="sxs-lookup"><span data-stu-id="a17da-126">Number of columns in the array.</span></span>

</dd> <dt>

<span data-ttu-id="a17da-127">**Elements (XElement Dynamic Property)** (Elements (Динамическое свойство XElement))</span><span class="sxs-lookup"><span data-stu-id="a17da-127">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="a17da-128">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a17da-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a17da-129">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="a17da-129">Number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="a17da-130">**Заметки**</span><span class="sxs-lookup"><span data-stu-id="a17da-130">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="a17da-131">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a17da-131">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a17da-132">Число заметок.</span><span class="sxs-lookup"><span data-stu-id="a17da-132">Number of annotations.</span></span>

</dd> <dt>

<span data-ttu-id="a17da-133">**структмемберс**</span><span class="sxs-lookup"><span data-stu-id="a17da-133">**StructMembers**</span></span>
</dt> <dd>

<span data-ttu-id="a17da-134">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a17da-134">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a17da-135">Число элементов структуры.</span><span class="sxs-lookup"><span data-stu-id="a17da-135">Number of structure members.</span></span>

</dd> <dt>

<span data-ttu-id="a17da-136">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="a17da-136">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="a17da-137">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a17da-137">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a17da-138">Атрибуты параметра.</span><span class="sxs-lookup"><span data-stu-id="a17da-138">Parameter attributes.</span></span> <span data-ttu-id="a17da-139">См. раздел [константы эффектов](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a17da-139">See [Effect Constants](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a17da-140">**Байт**</span><span class="sxs-lookup"><span data-stu-id="a17da-140">**Bytes**</span></span>
</dt> <dd>

<span data-ttu-id="a17da-141">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a17da-141">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a17da-142">Размер параметра в байтах.</span><span class="sxs-lookup"><span data-stu-id="a17da-142">The size of the parameter, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a17da-143">Требования</span><span class="sxs-lookup"><span data-stu-id="a17da-143">Requirements</span></span>



| <span data-ttu-id="a17da-144">Требование</span><span class="sxs-lookup"><span data-stu-id="a17da-144">Requirement</span></span> | <span data-ttu-id="a17da-145">Значение</span><span class="sxs-lookup"><span data-stu-id="a17da-145">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a17da-146">Header</span><span class="sxs-lookup"><span data-stu-id="a17da-146">Header</span></span><br/> | <dl> <span data-ttu-id="a17da-147"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a17da-147"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a17da-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a17da-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a17da-149">Структуры эффектов</span><span class="sxs-lookup"><span data-stu-id="a17da-149">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
