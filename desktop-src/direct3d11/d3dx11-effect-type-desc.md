---
title: Структура D3DX11_EFFECT_TYPE_DESC (D3dx11effect. h)
description: Описывает тип переменной влияния.
ms.assetid: bf2aa5b7-c68c-42bb-ae70-2fe16f8669a4
keywords:
- D3DX11_EFFECT_TYPE_DESC структура Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_TYPE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f4e8af391fed5717f47bb4b80398129cb98ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914799"
---
# <a name="d3dx11_effect_type_desc-structure"></a><span data-ttu-id="745fb-104">\_Структура D3DX11 \_ типа \_ эффектов</span><span class="sxs-lookup"><span data-stu-id="745fb-104">D3DX11\_EFFECT\_TYPE\_DESC structure</span></span>

<span data-ttu-id="745fb-105">Описывает тип переменной влияния.</span><span class="sxs-lookup"><span data-stu-id="745fb-105">Describes an effect-variable type.</span></span>

## <a name="syntax"></a><span data-ttu-id="745fb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="745fb-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_TYPE_DESC {
  LPCSTR                      TypeName;
  D3D10_SHADER_VARIABLE_CLASS Class;
  D3D10_SHADER_VARIABLE_TYPE  Type;
  UINT                        Elements;
  UINT                        Members;
  UINT                        Rows;
  UINT                        Columns;
  UINT                        PackedSize;
  UINT                        UnpackedSize;
  UINT                        Stride;
} D3DX11_EFFECT_TYPE_DESC;
```



## <a name="members"></a><span data-ttu-id="745fb-107">Участники</span><span class="sxs-lookup"><span data-stu-id="745fb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="745fb-108">**Имени**</span><span class="sxs-lookup"><span data-stu-id="745fb-108">**TypeName**</span></span>
</dt> <dd>

<span data-ttu-id="745fb-109">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="745fb-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="745fb-110">Имя типа, например "float4" или "MyStruct".</span><span class="sxs-lookup"><span data-stu-id="745fb-110">Name of the type, for example "float4" or "MyStruct".</span></span>

</dd> <dt>

<span data-ttu-id="745fb-111">**Класс**</span><span class="sxs-lookup"><span data-stu-id="745fb-111">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="745fb-112">Тип: **[ **\_ \_ \_ класс переменной шейдера D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**</span><span class="sxs-lookup"><span data-stu-id="745fb-112">Type: **[**D3D10\_SHADER\_VARIABLE\_CLASS**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**</span></span>

</dd> <dd>

<span data-ttu-id="745fb-113">Класс переменных (см. [**раздел \_ \_ \_ класс переменных шейдера D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).</span><span class="sxs-lookup"><span data-stu-id="745fb-113">The variable class (see [**D3D10\_SHADER\_VARIABLE\_CLASS**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).</span></span>

</dd> <dt>

<span data-ttu-id="745fb-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="745fb-114">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="745fb-115">Тип: **[ **\_ \_ \_ тип переменной шейдера D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**</span><span class="sxs-lookup"><span data-stu-id="745fb-115">Type: **[**D3D10\_SHADER\_VARIABLE\_TYPE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**</span></span>

</dd> <dd>

<span data-ttu-id="745fb-116">Тип переменной (см. [**раздел \_ \_ \_ тип переменной шейдера D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).</span><span class="sxs-lookup"><span data-stu-id="745fb-116">The variable type (see [**D3D10\_SHADER\_VARIABLE\_TYPE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).</span></span>

</dd> <dt>

<span data-ttu-id="745fb-117">**Elements (XElement Dynamic Property)** (Elements (Динамическое свойство XElement))</span><span class="sxs-lookup"><span data-stu-id="745fb-117">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="745fb-118">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="745fb-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="745fb-119">Число элементов в этом типе (0, если не является массивом).</span><span class="sxs-lookup"><span data-stu-id="745fb-119">Number of elements in this type (0 if not an array).</span></span>

</dd> <dt>

<span data-ttu-id="745fb-120">**Члены**</span><span class="sxs-lookup"><span data-stu-id="745fb-120">**Members**</span></span>
</dt> <dd>

<span data-ttu-id="745fb-121">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="745fb-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="745fb-122">Число элементов (0, если структура не является структурой).</span><span class="sxs-lookup"><span data-stu-id="745fb-122">Number of members (0 if not a structure).</span></span>

</dd> <dt>

<span data-ttu-id="745fb-123">**Строки**</span><span class="sxs-lookup"><span data-stu-id="745fb-123">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="745fb-124">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="745fb-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="745fb-125">Число строк в этом типе (0, если не является числовым примитивом).</span><span class="sxs-lookup"><span data-stu-id="745fb-125">Number of rows in this type (0 if not a numeric primitive).</span></span>

</dd> <dt>

<span data-ttu-id="745fb-126">**Столбцы**</span><span class="sxs-lookup"><span data-stu-id="745fb-126">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="745fb-127">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="745fb-127">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="745fb-128">Число столбцов в этом типе (0, если не является числовым примитивом).</span><span class="sxs-lookup"><span data-stu-id="745fb-128">Number of columns in this type (0 if not a numeric primitive).</span></span>

</dd> <dt>

<span data-ttu-id="745fb-129">**паккедсизе**</span><span class="sxs-lookup"><span data-stu-id="745fb-129">**PackedSize**</span></span>
</dt> <dd>

<span data-ttu-id="745fb-130">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="745fb-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="745fb-131">Число байтов, необходимое для представления этого типа данных при тесном упаковке.</span><span class="sxs-lookup"><span data-stu-id="745fb-131">Number of bytes required to represent this data type, when tightly packed.</span></span>

</dd> <dt>

<span data-ttu-id="745fb-132">**унпаккедсизе**</span><span class="sxs-lookup"><span data-stu-id="745fb-132">**UnpackedSize**</span></span>
</dt> <dd>

<span data-ttu-id="745fb-133">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="745fb-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="745fb-134">Число байтов, занимаемых этим типом данных, при его размещении в буфере констант.</span><span class="sxs-lookup"><span data-stu-id="745fb-134">Number of bytes occupied by this data type, when laid out in a constant buffer.</span></span>

</dd> <dt>

<span data-ttu-id="745fb-135">**Stride**</span><span class="sxs-lookup"><span data-stu-id="745fb-135">**Stride**</span></span>
</dt> <dd>

<span data-ttu-id="745fb-136">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="745fb-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="745fb-137">Число байтов для поиска элементов при их размещении в буфере констант.</span><span class="sxs-lookup"><span data-stu-id="745fb-137">Number of bytes to seek between elements, when laid out in a constant buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="745fb-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="745fb-138">Remarks</span></span>

<span data-ttu-id="745fb-139">D3DX11 \_ \_ тип эффектов \_ DESC используется с [ **ID3DX11EffectType:: DESC**](id3dx11effecttype-getdesc.md)</span><span class="sxs-lookup"><span data-stu-id="745fb-139">D3DX11\_EFFECT\_TYPE\_DESC is used with [**ID3DX11EffectType::GetDesc**](id3dx11effecttype-getdesc.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="745fb-140">Требования</span><span class="sxs-lookup"><span data-stu-id="745fb-140">Requirements</span></span>



| <span data-ttu-id="745fb-141">Требование</span><span class="sxs-lookup"><span data-stu-id="745fb-141">Requirement</span></span> | <span data-ttu-id="745fb-142">Значение</span><span class="sxs-lookup"><span data-stu-id="745fb-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="745fb-143">Header</span><span class="sxs-lookup"><span data-stu-id="745fb-143">Header</span></span><br/> | <dl> <span data-ttu-id="745fb-144"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="745fb-144"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="745fb-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="745fb-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="745fb-146">Эффекты с 11 по структурам</span><span class="sxs-lookup"><span data-stu-id="745fb-146">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

