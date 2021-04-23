---
description: Описание константы в таблице констант.
ms.assetid: d1970536-7195-4270-a1b9-b082ebe4f17f
title: Структура D3DXCONSTANT_DESC (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: d737fa1d95a119668602aeb056e15bc4248200aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713926"
---
# <a name="d3dxconstant_desc-structure"></a><span data-ttu-id="5fe6c-103">\_Структура D3DXCONSTANT DESC</span><span class="sxs-lookup"><span data-stu-id="5fe6c-103">D3DXCONSTANT\_DESC structure</span></span>

<span data-ttu-id="5fe6c-104">Описание константы в таблице констант.</span><span class="sxs-lookup"><span data-stu-id="5fe6c-104">A description of a constant in a constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fe6c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fe6c-105">Syntax</span></span>


```C++
typedef struct D3DXCONSTANT_DESC {
  LPCSTR              Name;
  D3DXREGISTER_SET    RegisterSet;
  UINT                RegisterIndex;
  UINT                RegisterCount;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                StructMembers;
  UINT                Bytes;
  LPCVOID             DefaultValue;
} D3DXCONSTANT_DESC, *LPD3DXCONSTANT_DESC;
```



## <a name="members"></a><span data-ttu-id="5fe6c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="5fe6c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5fe6c-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="5fe6c-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5fe6c-109">Имя константы.</span><span class="sxs-lookup"><span data-stu-id="5fe6c-109">Name of the constant.</span></span>

</dd> <dt>

<span data-ttu-id="5fe6c-110">**Register**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-110">**RegisterSet**</span></span>
</dt> <dd>

<span data-ttu-id="5fe6c-111">Тип: **[ **D3DXREGISTER \_ Set** .](./d3dxregister-set.md)**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-111">Type: **[**D3DXREGISTER\_SET**](./d3dxregister-set.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5fe6c-112">Постоянный тип данных.</span><span class="sxs-lookup"><span data-stu-id="5fe6c-112">Constant data type.</span></span> <span data-ttu-id="5fe6c-113">См. раздел [**D3DXREGISTER \_ Set**](./d3dxregister-set.md).</span><span class="sxs-lookup"><span data-stu-id="5fe6c-113">See [**D3DXREGISTER\_SET**](./d3dxregister-set.md).</span></span>

</dd> <dt>

<span data-ttu-id="5fe6c-114">**регистериндекс**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-114">**RegisterIndex**</span></span>
</dt> <dd>

<span data-ttu-id="5fe6c-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5fe6c-116">Отсчитываемый от нуля индекс константы в таблице.</span><span class="sxs-lookup"><span data-stu-id="5fe6c-116">Zero-based index of the constant in the table.</span></span>

</dd> <dt>

<span data-ttu-id="5fe6c-117">**регистеркаунт**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-117">**RegisterCount**</span></span>
</dt> <dd>

<span data-ttu-id="5fe6c-118">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5fe6c-119">Количество регистров, содержащих данные.</span><span class="sxs-lookup"><span data-stu-id="5fe6c-119">Number of registers that contain data.</span></span>

</dd> <dt>

<span data-ttu-id="5fe6c-120">**Класс**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-120">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="5fe6c-121">Тип: **[ **\_ класс D3DXPARAMETER**](./d3dxparameter-class.md)**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-121">Type: **[**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5fe6c-122">Класс параметра.</span><span class="sxs-lookup"><span data-stu-id="5fe6c-122">Parameter class.</span></span> <span data-ttu-id="5fe6c-123">См. раздел [**\_ класс D3DXPARAMETER**](./d3dxparameter-class.md).</span><span class="sxs-lookup"><span data-stu-id="5fe6c-123">See [**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="5fe6c-124">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-124">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="5fe6c-125">Тип: **[ **D3DXPARAMETER \_ тип**](./d3dxparameter-type.md)**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-125">Type: **[**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5fe6c-126">Тип параметра.</span><span class="sxs-lookup"><span data-stu-id="5fe6c-126">Parameter type.</span></span> <span data-ttu-id="5fe6c-127">См. раздел [**\_ тип D3DXPARAMETER**](./d3dxparameter-type.md).</span><span class="sxs-lookup"><span data-stu-id="5fe6c-127">See [**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="5fe6c-128">**Строки**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-128">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="5fe6c-129">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5fe6c-130">Число строк.</span><span class="sxs-lookup"><span data-stu-id="5fe6c-130">Number of rows.</span></span>

</dd> <dt>

<span data-ttu-id="5fe6c-131">**Столбцы**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-131">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="5fe6c-132">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5fe6c-133">Число столбцов.</span><span class="sxs-lookup"><span data-stu-id="5fe6c-133">Number of columns.</span></span>

</dd> <dt>

<span data-ttu-id="5fe6c-134">**Elements (XElement Dynamic Property)** (Elements (Динамическое свойство XElement))</span><span class="sxs-lookup"><span data-stu-id="5fe6c-134">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="5fe6c-135">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5fe6c-136">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="5fe6c-136">Number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="5fe6c-137">**структмемберс**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-137">**StructMembers**</span></span>
</dt> <dd>

<span data-ttu-id="5fe6c-138">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-138">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5fe6c-139">Число подпараметров элемента структуры.</span><span class="sxs-lookup"><span data-stu-id="5fe6c-139">Number of structure member sub-parameters.</span></span>

</dd> <dt>

<span data-ttu-id="5fe6c-140">**Байт**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-140">**Bytes**</span></span>
</dt> <dd>

<span data-ttu-id="5fe6c-141">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-141">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5fe6c-142">Размер данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="5fe6c-142">Data size in number of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5fe6c-143">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-143">**DefaultValue**</span></span>
</dt> <dd>

<span data-ttu-id="5fe6c-144">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-144">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5fe6c-145">Указатель на значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5fe6c-145">Pointer to the default value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5fe6c-146">Требования</span><span class="sxs-lookup"><span data-stu-id="5fe6c-146">Requirements</span></span>



| <span data-ttu-id="5fe6c-147">Требование</span><span class="sxs-lookup"><span data-stu-id="5fe6c-147">Requirement</span></span> | <span data-ttu-id="5fe6c-148">Значение</span><span class="sxs-lookup"><span data-stu-id="5fe6c-148">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fe6c-149">Header</span><span class="sxs-lookup"><span data-stu-id="5fe6c-149">Header</span></span><br/> | <dl> <span data-ttu-id="5fe6c-150"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fe6c-150"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fe6c-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5fe6c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fe6c-152">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="5fe6c-152">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="5fe6c-153">**D3DXCONSTANTTABLE \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="5fe6c-153">**D3DXCONSTANTTABLE\_DESC**</span></span>](d3dxconstanttable-desc.md)
</dt> </dl>

 

 
