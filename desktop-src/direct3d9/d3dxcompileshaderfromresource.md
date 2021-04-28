---
description: Функция D3DXCompileShaderFromResource — Скомпилируйте файл шейдера.
ms.assetid: e944ae61-0c27-4795-8381-0ec9b3d8c3f4
title: Функция D3DXCompileShaderFromResource (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de94754004cc42bcc6914d9513588a71a1a593dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115812"
---
# <a name="d3dxcompileshaderfromresource-function"></a><span data-ttu-id="cc1d0-103">Функция D3DXCompileShaderFromResource</span><span class="sxs-lookup"><span data-stu-id="cc1d0-103">D3DXCompileShaderFromResource function</span></span>

<span data-ttu-id="cc1d0-104">Скомпилируйте файл шейдера.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="cc1d0-105">Вместо использования этой устаревшей функции рекомендуется компилировать автономно с помощью Fxc.exe компилятора командной строки или использовать API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="cc1d0-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="cc1d0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc1d0-106">Syntax</span></span>


```C++
HRESULT D3DXCompileShaderFromResource(
  _In_        HMODULE             hSrcModule,
  _In_        LPCSTR              pSrcResource,
  _In_  const D3DXMACRO           *pDefines,
  _In_        LPD3DXINCLUDE       pInclude,
  _In_        LPCSTR              pFunctionName,
  _In_        LPCSTR              pProfile,
  _In_        DWORD               Flags,
  _Out_       LPD3DXBUFFER        *ppShader,
  _Out_       LPD3DXBUFFER        *ppErrorMsgs,
  _Out_       LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="cc1d0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc1d0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc1d0-108">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc1d0-108">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc1d0-109">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc1d0-109">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc1d0-110">Обработчик для модуля, содержащего описание результата.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-110">Handle to a module containing the effect description.</span></span> <span data-ttu-id="cc1d0-111">Если этот параметр имеет **значение NULL**, будет использоваться текущий модуль.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-111">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="cc1d0-112">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc1d0-112">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc1d0-113">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc1d0-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc1d0-114">Указатель на строку, указывающую имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-114">Pointer to a string that specifies the resource name.</span></span>

</dd> <dt>

<span data-ttu-id="cc1d0-115">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc1d0-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc1d0-116">Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="cc1d0-116">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="cc1d0-117">Необязательный массив структур [**D3DXMACRO**](d3dxmacro.md) , заканчивающийся **нулевым значением** .</span><span class="sxs-lookup"><span data-stu-id="cc1d0-117">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="cc1d0-118">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-118">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cc1d0-119">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc1d0-119">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc1d0-120">Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="cc1d0-120">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="cc1d0-121">Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-121">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="cc1d0-122">Если это значение равно **null**, то \# включается либо при компиляции из файла, либо при компиляции из ресурса или памяти.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-122">If this value is **NULL**, \#includes will either be honored when compiling from a file, or will error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="cc1d0-123">*пфунктионнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc1d0-123">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc1d0-124">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc1d0-124">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc1d0-125">Указатель на функцию точки входа шейдера, где начинается выполнение.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-125">Pointer to the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="cc1d0-126">*ппрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc1d0-126">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc1d0-127">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc1d0-127">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc1d0-128">Указатель на профиль шейдера, который определяет набор инструкций шейдера.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-128">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="cc1d0-129">Список доступных профилей см. в разделе [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) или [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="cc1d0-129">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="cc1d0-130">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc1d0-130">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc1d0-131">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc1d0-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc1d0-132">Параметры компиляции, определяемые различными флагами.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-132">Compile options identified by various flags.</span></span> <span data-ttu-id="cc1d0-133">Компилятор Direct3D 10 HLSL теперь является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-133">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="cc1d0-134">Дополнительные сведения см. в разделе [Флаги D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="cc1d0-134">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="cc1d0-135">*ппшадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cc1d0-135">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc1d0-136">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="cc1d0-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="cc1d0-137">Возвращает буфер, содержащий созданный шейдер.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-137">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="cc1d0-138">Этот буфер содержит скомпилированный код шейдера, а также любые внедренные сведения о таблицах отладки и символов.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-138">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="cc1d0-139">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cc1d0-139">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc1d0-140">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="cc1d0-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="cc1d0-141">Возвращает буфер, содержащий список ошибок и предупреждений, обнаруженных во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-141">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="cc1d0-142">Это те же сообщения, которые отладчик отображает при работе в режиме отладки.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-142">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="cc1d0-143">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-143">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cc1d0-144">*ппконстанттабле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cc1d0-144">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc1d0-145">Тип: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="cc1d0-145">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="cc1d0-146">Возвращает интерфейс [**ID3DXConstantTable**](id3dxconstanttable.md) , который можно использовать для доступа к константам шейдера.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-146">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="cc1d0-147">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-147">This value can be **NULL**.</span></span> <span data-ttu-id="cc1d0-148">Если приложение компилируется как большой адрес (то есть для работы с адресами, превышающими 2 ГБ, используется параметр компоновщика/LARGEADDRESSAWARE), этот параметр использовать нельзя, и его значение должно быть равно **null**.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-148">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="cc1d0-149">Вместо этого необходимо использовать функцию [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) , чтобы извлечь таблицу-константу шейдера, внедренную в шейдер.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-149">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="cc1d0-150">В этом вызове **D3DXGetShaderConstantTableEx** необходимо передать флаг **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** в параметр *flags* , чтобы указать, чтобы получить доступ к 4 ГБ виртуального адресного пространства.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-150">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc1d0-151">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc1d0-151">Return value</span></span>

<span data-ttu-id="cc1d0-152">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cc1d0-152">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cc1d0-153">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-153">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cc1d0-154">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="cc1d0-154">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc1d0-155">Требования</span><span class="sxs-lookup"><span data-stu-id="cc1d0-155">Requirements</span></span>



| <span data-ttu-id="cc1d0-156">Требование</span><span class="sxs-lookup"><span data-stu-id="cc1d0-156">Requirement</span></span> | <span data-ttu-id="cc1d0-157">Значение</span><span class="sxs-lookup"><span data-stu-id="cc1d0-157">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc1d0-158">Header</span><span class="sxs-lookup"><span data-stu-id="cc1d0-158">Header</span></span><br/>  | <dl> <span data-ttu-id="cc1d0-159"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc1d0-159"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="cc1d0-160">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cc1d0-160">Library</span></span><br/> | <dl> <span data-ttu-id="cc1d0-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc1d0-161"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cc1d0-162">См. также</span><span class="sxs-lookup"><span data-stu-id="cc1d0-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc1d0-163">Функции шейдера</span><span class="sxs-lookup"><span data-stu-id="cc1d0-163">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="cc1d0-164">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="cc1d0-164">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="cc1d0-165">**D3DXCompileShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="cc1d0-165">**D3DXCompileShaderFromFile**</span></span>](d3dxcompileshaderfromfile.md)
</dt> </dl>

 

 
