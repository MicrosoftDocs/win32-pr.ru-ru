---
description: Описывает данные, содержащиеся в перечислении.
ms.assetid: 6d494fe6-fcd5-4e71-939c-257978b41499
title: Перечисление D3DXPARAMETER_TYPE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 16ff89feb694bb6aae550422b6f9546c2268fc07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354153"
---
# <a name="d3dxparameter_type-enumeration"></a><span data-ttu-id="f544f-103">\_Перечисление типов D3DXPARAMETER</span><span class="sxs-lookup"><span data-stu-id="f544f-103">D3DXPARAMETER\_TYPE enumeration</span></span>

<span data-ttu-id="f544f-104">Описывает данные, содержащиеся в перечислении.</span><span class="sxs-lookup"><span data-stu-id="f544f-104">Describes the data contained by the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="f544f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f544f-105">Syntax</span></span>


```C++
typedef enum D3DXPARAMETER_TYPE { 
  D3DXPT_VOID,
  D3DXPT_BOOL,
  D3DXPT_INT,
  D3DXPT_FLOAT,
  D3DXPT_STRING,
  D3DXPT_TEXTURE,
  D3DXPT_TEXTURE1D,
  D3DXPT_TEXTURE2D,
  D3DXPT_TEXTURE3D,
  D3DXPT_TEXTURECUBE,
  D3DXPT_SAMPLER,
  D3DXPT_SAMPLER1D,
  D3DXPT_SAMPLER2D,
  D3DXPT_SAMPLER3D,
  D3DXPT_SAMPLERCUBE,
  D3DXPT_PIXELSHADER,
  D3DXPT_VERTEXSHADER,
  D3DXPT_PIXELFRAGMENT,
  D3DXPT_VERTEXFRAGMENT,
  D3DXPT_UNSUPPORTED,
  D3DXPT_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_TYPE, *LPD3DXPARAMETER_TYPE;
```



## <a name="constants"></a><span data-ttu-id="f544f-106">Константы</span><span class="sxs-lookup"><span data-stu-id="f544f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f544f-107"><span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT \_ void**</span><span class="sxs-lookup"><span data-stu-id="f544f-107"><span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT\_VOID**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-108">Параметр является указателем void.</span><span class="sxs-lookup"><span data-stu-id="f544f-108">Parameter is a void pointer.</span></span>

</dd> <dt>

<span data-ttu-id="f544f-109"><span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**\_Bool D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="f544f-109"><span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**D3DXPT\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-110">Параметр является логическим.</span><span class="sxs-lookup"><span data-stu-id="f544f-110">Parameter is a Boolean.</span></span> <span data-ttu-id="f544f-111">Любое ненулевое значение, переданное в [**ID3DXConstantTable:: сетбул**](id3dxconstanttable--setbool.md), [**ID3DXConstantTable:: сетбуларрай**](id3dxconstanttable--setboolarray.md), [**ID3DXConstantTable:: SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable:: сетвектор**](id3dxconstanttable--setvector.md)или [**ID3DXConstantTable:: СЕТВЕКТОРАРРАЙ**](id3dxconstanttable--setvectorarray.md) , будет сопоставлено с 1 (true) перед записью в таблицу констант. в противном случае в таблице констант будет задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="f544f-111">Any non-zero value passed into [**ID3DXConstantTable::SetBool**](id3dxconstanttable--setbool.md), [**ID3DXConstantTable::SetBoolArray**](id3dxconstanttable--setboolarray.md), [**ID3DXConstantTable::SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable::SetVector**](id3dxconstanttable--setvector.md), or [**ID3DXConstantTable::SetVectorArray**](id3dxconstanttable--setvectorarray.md) will be mapped to 1 (TRUE) before being written into the constant table; otherwise, the value will be set to 0 in the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="f544f-112"><span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**D3DXPT \_ int**</span><span class="sxs-lookup"><span data-stu-id="f544f-112"><span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**D3DXPT\_INT**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-113">Параметр является целым числом.</span><span class="sxs-lookup"><span data-stu-id="f544f-113">Parameter is an integer.</span></span> <span data-ttu-id="f544f-114">Любые значения с плавающей запятой, передаваемые в [**ID3DXConstantTable:: SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable:: сетвектор**](id3dxconstanttable--setvector.md)или [**ID3DXConstantTable:: сетвектораррай**](id3dxconstanttable--setvectorarray.md) , будут округляться (до нуля десятичных разрядов) перед их записью в таблицу констант.</span><span class="sxs-lookup"><span data-stu-id="f544f-114">Any floating-point values passed into [**ID3DXConstantTable::SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable::SetVector**](id3dxconstanttable--setvector.md), or [**ID3DXConstantTable::SetVectorArray**](id3dxconstanttable--setvectorarray.md) will be rounded off (to zero decimal places) before being written into the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="f544f-115"><span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**D3DXPT \_ float**</span><span class="sxs-lookup"><span data-stu-id="f544f-115"><span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**D3DXPT\_FLOAT**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-116">Параметр является числом с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="f544f-116">Parameter is a floating-point number.</span></span>

</dd> <dt>

<span data-ttu-id="f544f-117"><span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**\_Строка D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="f544f-117"><span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**D3DXPT\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-118">Параметр является строкой.</span><span class="sxs-lookup"><span data-stu-id="f544f-118">Parameter is a string.</span></span>

</dd> <dt>

<span data-ttu-id="f544f-119"><span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**\_Текстура D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="f544f-119"><span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**D3DXPT\_TEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-120">Параметр является текстурой.</span><span class="sxs-lookup"><span data-stu-id="f544f-120">Parameter is a texture.</span></span>

</dd> <dt>

<span data-ttu-id="f544f-121"><span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**D3DXPT \_ TEXTURE1D**</span><span class="sxs-lookup"><span data-stu-id="f544f-121"><span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**D3DXPT\_TEXTURE1D**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-122">Параметр является текстурой 1D.</span><span class="sxs-lookup"><span data-stu-id="f544f-122">Parameter is a 1D texture.</span></span>

</dd> <dt>

<span data-ttu-id="f544f-123"><span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**D3DXPT \_ TEXTURE2D**</span><span class="sxs-lookup"><span data-stu-id="f544f-123"><span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**D3DXPT\_TEXTURE2D**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-124">Параметр является двухмерной текстурой.</span><span class="sxs-lookup"><span data-stu-id="f544f-124">Parameter is a 2D texture.</span></span>

</dd> <dt>

<span data-ttu-id="f544f-125"><span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**D3DXPT \_ TEXTURE3D**</span><span class="sxs-lookup"><span data-stu-id="f544f-125"><span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**D3DXPT\_TEXTURE3D**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-126">Параметр является трехмерной текстурой.</span><span class="sxs-lookup"><span data-stu-id="f544f-126">Parameter is a 3D texture.</span></span>

</dd> <dt>

<span data-ttu-id="f544f-127"><span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**D3DXPT \_ текстурекубе**</span><span class="sxs-lookup"><span data-stu-id="f544f-127"><span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**D3DXPT\_TEXTURECUBE**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-128">Параметр является текстурой Куба.</span><span class="sxs-lookup"><span data-stu-id="f544f-128">Parameter is a cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="f544f-129"><span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**\_Образец D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="f544f-129"><span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**D3DXPT\_SAMPLER**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-130">Параметр — это образец.</span><span class="sxs-lookup"><span data-stu-id="f544f-130">Parameter is a sampler.</span></span>

</dd> <dt>

<span data-ttu-id="f544f-131"><span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**D3DXPT \_ SAMPLER1D**</span><span class="sxs-lookup"><span data-stu-id="f544f-131"><span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**D3DXPT\_SAMPLER1D**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-132">Параметр является одномерной выборкой.</span><span class="sxs-lookup"><span data-stu-id="f544f-132">Parameter is a 1D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="f544f-133"><span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**D3DXPT \_ SAMPLER2D**</span><span class="sxs-lookup"><span data-stu-id="f544f-133"><span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**D3DXPT\_SAMPLER2D**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-134">Параметр — это 2D-образец.</span><span class="sxs-lookup"><span data-stu-id="f544f-134">Parameter is a 2D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="f544f-135"><span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**D3DXPT \_ SAMPLER3D**</span><span class="sxs-lookup"><span data-stu-id="f544f-135"><span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**D3DXPT\_SAMPLER3D**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-136">Параметр представляет собой трехмерный образец.</span><span class="sxs-lookup"><span data-stu-id="f544f-136">Parameter is a 3D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="f544f-137"><span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**D3DXPT \_ самплеркубе**</span><span class="sxs-lookup"><span data-stu-id="f544f-137"><span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**D3DXPT\_SAMPLERCUBE**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-138">Параметр — это образец куба.</span><span class="sxs-lookup"><span data-stu-id="f544f-138">Parameter is a cube sampler.</span></span>

</dd> <dt>

<span data-ttu-id="f544f-139"><span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**D3DXPT \_ PIXELSHADER**</span><span class="sxs-lookup"><span data-stu-id="f544f-139"><span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**D3DXPT\_PIXELSHADER**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-140">Параметр — это построитель текстуры.</span><span class="sxs-lookup"><span data-stu-id="f544f-140">Parameter is a pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="f544f-141"><span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**D3DXPT \_ вертексшадер**</span><span class="sxs-lookup"><span data-stu-id="f544f-141"><span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**D3DXPT\_VERTEXSHADER**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-142">Параметр является шейдером вершин.</span><span class="sxs-lookup"><span data-stu-id="f544f-142">Parameter is a vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="f544f-143"><span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**D3DXPT \_ пикселфрагмент**</span><span class="sxs-lookup"><span data-stu-id="f544f-143"><span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**D3DXPT\_PIXELFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-144">Параметр является фрагментом шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="f544f-144">Parameter is a pixel shader fragment.</span></span>

</dd> <dt>

<span data-ttu-id="f544f-145"><span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**D3DXPT \_ вертексфрагмент**</span><span class="sxs-lookup"><span data-stu-id="f544f-145"><span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**D3DXPT\_VERTEXFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-146">Параметр является фрагментом шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="f544f-146">Parameter is a vertex shader fragment.</span></span>

</dd> <dt>

<span data-ttu-id="f544f-147"><span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**D3DXPT \_ не поддерживается**</span><span class="sxs-lookup"><span data-stu-id="f544f-147"><span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**D3DXPT\_UNSUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-148">Параметр не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f544f-148">Parameter is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f544f-149"><span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f544f-149"><span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="f544f-150">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="f544f-150">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="f544f-151">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="f544f-151">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="f544f-152">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="f544f-152">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f544f-153">Требования</span><span class="sxs-lookup"><span data-stu-id="f544f-153">Requirements</span></span>



| <span data-ttu-id="f544f-154">Требование</span><span class="sxs-lookup"><span data-stu-id="f544f-154">Requirement</span></span> | <span data-ttu-id="f544f-155">Значение</span><span class="sxs-lookup"><span data-stu-id="f544f-155">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f544f-156">Header</span><span class="sxs-lookup"><span data-stu-id="f544f-156">Header</span></span><br/> | <dl> <span data-ttu-id="f544f-157"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f544f-157"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f544f-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f544f-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f544f-159">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="f544f-159">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="f544f-160">**D3DXSHADER \_ TYPEINFO**</span><span class="sxs-lookup"><span data-stu-id="f544f-160">**D3DXSHADER\_TYPEINFO**</span></span>](d3dxshader-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="f544f-161">**D3DXCONSTANT \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="f544f-161">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 




