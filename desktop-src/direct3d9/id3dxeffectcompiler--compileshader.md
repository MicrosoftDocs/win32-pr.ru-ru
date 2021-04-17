---
description: Компилирует шейдер из действия, содержащего одну или несколько функций.
ms.assetid: f34a2975-dcd5-4917-9b11-ed40583272f9
title: 'Метод ID3DXEffectCompiler:: Компилешадер (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 375646202e102623053c179398329ad2286e6c1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703879"
---
# <a name="id3dxeffectcompilercompileshader-method"></a><span data-ttu-id="95df4-103">Метод ID3DXEffectCompiler:: Компилешадер</span><span class="sxs-lookup"><span data-stu-id="95df4-103">ID3DXEffectCompiler::CompileShader method</span></span>

<span data-ttu-id="95df4-104">Компилирует шейдер из действия, содержащего одну или несколько функций.</span><span class="sxs-lookup"><span data-stu-id="95df4-104">Compiles a shader from an effect that contains one or more functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="95df4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95df4-105">Syntax</span></span>


```C++
HRESULT CompileShader(
  [in]          D3DXHANDLE          hFunction,
  [in]          LPCSTR              pTarget,
  [in]          DWORD               Flags,
  [out, retval] LPD3DXBUFFER        *ppShader,
  [out, retval] LPD3DXBUFFER        *ppErrorMsgs,
  [out]         LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="95df4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="95df4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95df4-107">*хфунктион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95df4-107">*hFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95df4-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="95df4-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="95df4-109">Уникальный идентификатор компилируемой функции.</span><span class="sxs-lookup"><span data-stu-id="95df4-109">Unique identifier to the function to be compiled.</span></span> <span data-ttu-id="95df4-110">Это значение не должно быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="95df4-110">This value must not be **NULL**.</span></span> <span data-ttu-id="95df4-111">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="95df4-111">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="95df4-112">*птаржет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95df4-112">*pTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95df4-113">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95df4-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95df4-114">Указатель на профиль шейдера, который определяет набор инструкций шейдера.</span><span class="sxs-lookup"><span data-stu-id="95df4-114">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="95df4-115">Список доступных профилей см. в разделе [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) или [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="95df4-115">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="95df4-116">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95df4-116">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95df4-117">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95df4-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95df4-118">Параметры компиляции, определяемые различными флагами.</span><span class="sxs-lookup"><span data-stu-id="95df4-118">Compile options identified by various flags.</span></span> <span data-ttu-id="95df4-119">Компилятор Direct3D 10 HLSL теперь является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="95df4-119">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="95df4-120">Дополнительные сведения см. в разделе [Флаги D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="95df4-120">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="95df4-121">*ппшадер* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="95df4-121">*ppShader* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="95df4-122">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="95df4-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="95df4-123">Буфер, содержащий скомпилированный шейдер.</span><span class="sxs-lookup"><span data-stu-id="95df4-123">Buffer containing the compiled shader.</span></span> <span data-ttu-id="95df4-124">Шейдер компилятора — это массив DWORD.</span><span class="sxs-lookup"><span data-stu-id="95df4-124">The compiler shader is an array of DWORDs.</span></span> <span data-ttu-id="95df4-125">Дополнительные сведения о доступе к буферу см. в разделе [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="95df4-125">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="95df4-126">*пперрормсгс* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="95df4-126">*ppErrorMsgs* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="95df4-127">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="95df4-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="95df4-128">Буфер, содержащий по крайней мере первое сообщение об ошибке компиляции.</span><span class="sxs-lookup"><span data-stu-id="95df4-128">Buffer containing at least the first compile error message that occurred.</span></span> <span data-ttu-id="95df4-129">Это относится к ошибкам компилятора и ошибкам при компиляции на высоком уровне.</span><span class="sxs-lookup"><span data-stu-id="95df4-129">This includes effect compiler errors and high-level language compile errors.</span></span> <span data-ttu-id="95df4-130">Дополнительные сведения о доступе к буферу см. в разделе [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="95df4-130">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="95df4-131">*ппконстанттабле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="95df4-131">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95df4-132">Тип: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="95df4-132">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="95df4-133">Возвращает интерфейс [**ID3DXConstantTable**](id3dxconstanttable.md) , который можно использовать для доступа к константам шейдера.</span><span class="sxs-lookup"><span data-stu-id="95df4-133">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="95df4-134">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="95df4-134">This value can be **NULL**.</span></span> <span data-ttu-id="95df4-135">Если приложение компилируется как большой адрес (то есть для работы с адресами, превышающими 2 ГБ, используется параметр компоновщика/LARGEADDRESSAWARE), этот параметр использовать нельзя, и его значение должно быть равно **null**.</span><span class="sxs-lookup"><span data-stu-id="95df4-135">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="95df4-136">Вместо этого необходимо использовать функцию [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) , чтобы извлечь таблицу-константу шейдера, внедренную в шейдер.</span><span class="sxs-lookup"><span data-stu-id="95df4-136">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="95df4-137">В этом вызове **D3DXGetShaderConstantTableEx** необходимо передать флаг **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** в параметр *flags* , чтобы указать, чтобы получить доступ к 4 ГБ виртуального адресного пространства.</span><span class="sxs-lookup"><span data-stu-id="95df4-137">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95df4-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95df4-138">Return value</span></span>

<span data-ttu-id="95df4-139">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95df4-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95df4-140">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="95df4-140">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="95df4-141">Если аргументы недопустимы, метод возвратит D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="95df4-141">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="95df4-142">Если метод завершается с ошибкой, возвращается значение E \_ Failed.</span><span class="sxs-lookup"><span data-stu-id="95df4-142">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="95df4-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95df4-143">Remarks</span></span>

<span data-ttu-id="95df4-144">Целевые объекты можно указать для шейдеров вершин, шейдеров пикселей и функций заливки текстур.</span><span class="sxs-lookup"><span data-stu-id="95df4-144">Targets can be specified for vertex shaders, pixel shaders, and texture fill functions.</span></span>



|                       |                                                                       |
|-----------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="95df4-145">Цели шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="95df4-145">Vertex shader targets</span></span> | <span data-ttu-id="95df4-146">VS \_ 1 \_ , vs 2 \_ \_ 0, VS \_ 2 \_ SW, VS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="95df4-146">vs\_1\_1, vs\_2\_0, vs\_2\_sw, vs\_3\_0</span></span>                               |
| <span data-ttu-id="95df4-147">Цели шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="95df4-147">Pixel shader targets</span></span>  | <span data-ttu-id="95df4-148">PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4, PS \_ 2 \_ 0, PS \_ 2 \_ SW, PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="95df4-148">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4, ps\_2\_0, ps\_2\_sw, ps\_3\_0</span></span> |
| <span data-ttu-id="95df4-149">Цели заливки текстур</span><span class="sxs-lookup"><span data-stu-id="95df4-149">Texture fill targets</span></span>  | <span data-ttu-id="95df4-150">TX \_ 0, TX \_ 1</span><span class="sxs-lookup"><span data-stu-id="95df4-150">tx\_0, tx\_1</span></span>                                                          |



 

<span data-ttu-id="95df4-151">Этот метод компилирует шейдер из функции, написанной на языке C.</span><span class="sxs-lookup"><span data-stu-id="95df4-151">This method compiles a shader from a function that is written in a C-like language.</span></span> <span data-ttu-id="95df4-152">Подробнее: [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="95df4-152">For more information, see [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95df4-153">Требования</span><span class="sxs-lookup"><span data-stu-id="95df4-153">Requirements</span></span>



| <span data-ttu-id="95df4-154">Требование</span><span class="sxs-lookup"><span data-stu-id="95df4-154">Requirement</span></span> | <span data-ttu-id="95df4-155">Значение</span><span class="sxs-lookup"><span data-stu-id="95df4-155">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="95df4-156">Header</span><span class="sxs-lookup"><span data-stu-id="95df4-156">Header</span></span><br/>  | <dl> <span data-ttu-id="95df4-157"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="95df4-157"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="95df4-158">Библиотека</span><span class="sxs-lookup"><span data-stu-id="95df4-158">Library</span></span><br/> | <dl> <span data-ttu-id="95df4-159"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95df4-159"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="95df4-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95df4-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95df4-161">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="95df4-161">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="95df4-162">**D3DXGetShaderConstantTable**</span><span class="sxs-lookup"><span data-stu-id="95df4-162">**D3DXGetShaderConstantTable**</span></span>](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
