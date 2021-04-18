---
description: Скомпилируйте файл шейдера.
ms.assetid: 2ad6042f-3601-4f4a-9624-6319a3372355
title: Функция D3DXCompileShaderFromFile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 865241142fa13ec9d34826bfe334c30b38ca78d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713748"
---
# <a name="d3dxcompileshaderfromfile-function"></a><span data-ttu-id="d8e06-103">Функция D3DXCompileShaderFromFile</span><span class="sxs-lookup"><span data-stu-id="d8e06-103">D3DXCompileShaderFromFile function</span></span>

<span data-ttu-id="d8e06-104">Скомпилируйте файл шейдера.</span><span class="sxs-lookup"><span data-stu-id="d8e06-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="d8e06-105">Вместо использования этой устаревшей функции рекомендуется компилировать автономно с помощью Fxc.exe компилятора командной строки или использовать API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="d8e06-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d8e06-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8e06-106">Syntax</span></span>


```C++
HRESULT D3DXCompileShaderFromFile(
  _In_        LPCTSTR             pSrcFile,
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



## <a name="parameters"></a><span data-ttu-id="d8e06-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8e06-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8e06-108">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8e06-108">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8e06-109">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8e06-109">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8e06-110">Указатель на строку, указывающую имя файла.</span><span class="sxs-lookup"><span data-stu-id="d8e06-110">Pointer to a string that specifies the filename.</span></span>

</dd> <dt>

<span data-ttu-id="d8e06-111">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8e06-111">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8e06-112">Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="d8e06-112">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="d8e06-113">Необязательный массив структур [**D3DXMACRO**](d3dxmacro.md) , заканчивающийся **нулевым значением** .</span><span class="sxs-lookup"><span data-stu-id="d8e06-113">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="d8e06-114">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="d8e06-114">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d8e06-115">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8e06-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8e06-116">Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="d8e06-116">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="d8e06-117">Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include.</span><span class="sxs-lookup"><span data-stu-id="d8e06-117">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="d8e06-118">Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.</span><span class="sxs-lookup"><span data-stu-id="d8e06-118">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="d8e06-119">*пфунктионнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8e06-119">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8e06-120">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8e06-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8e06-121">Указатель на функцию точки входа шейдера, где начинается выполнение.</span><span class="sxs-lookup"><span data-stu-id="d8e06-121">Pointer to the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="d8e06-122">*ппрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8e06-122">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8e06-123">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8e06-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8e06-124">Указатель на профиль шейдера, который определяет набор инструкций шейдера.</span><span class="sxs-lookup"><span data-stu-id="d8e06-124">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="d8e06-125">Список доступных профилей см. в разделе [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) или [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="d8e06-125">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="d8e06-126">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8e06-126">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8e06-127">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8e06-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8e06-128">Параметры компиляции, определяемые различными флагами.</span><span class="sxs-lookup"><span data-stu-id="d8e06-128">Compile options identified by various flags.</span></span> <span data-ttu-id="d8e06-129">Компилятор Direct3D 10 HLSL теперь является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d8e06-129">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="d8e06-130">Дополнительные сведения см. в разделе [Флаги D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="d8e06-130">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="d8e06-131">*ппшадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d8e06-131">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8e06-132">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8e06-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d8e06-133">Возвращает буфер, содержащий созданный шейдер.</span><span class="sxs-lookup"><span data-stu-id="d8e06-133">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="d8e06-134">Этот буфер содержит скомпилированный код шейдера, а также любые внедренные сведения о таблицах отладки и символов.</span><span class="sxs-lookup"><span data-stu-id="d8e06-134">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="d8e06-135">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d8e06-135">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8e06-136">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8e06-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d8e06-137">Возвращает буфер, содержащий список ошибок и предупреждений, обнаруженных во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="d8e06-137">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="d8e06-138">Это те же сообщения, которые отладчик отображает при работе в режиме отладки.</span><span class="sxs-lookup"><span data-stu-id="d8e06-138">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="d8e06-139">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="d8e06-139">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d8e06-140">*ппконстанттабле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d8e06-140">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8e06-141">Тип: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8e06-141">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="d8e06-142">Возвращает интерфейс [**ID3DXConstantTable**](id3dxconstanttable.md) , который можно использовать для доступа к константам шейдера.</span><span class="sxs-lookup"><span data-stu-id="d8e06-142">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="d8e06-143">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="d8e06-143">This value can be **NULL**.</span></span> <span data-ttu-id="d8e06-144">Если приложение компилируется как большой адрес (то есть для работы с адресами, превышающими 2 ГБ, используется параметр компоновщика/LARGEADDRESSAWARE), этот параметр использовать нельзя, и его значение должно быть равно **null**.</span><span class="sxs-lookup"><span data-stu-id="d8e06-144">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="d8e06-145">Вместо этого необходимо использовать функцию [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) , чтобы извлечь таблицу-константу шейдера, внедренную в шейдер.</span><span class="sxs-lookup"><span data-stu-id="d8e06-145">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="d8e06-146">В этом вызове **D3DXGetShaderConstantTableEx** необходимо передать флаг **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** в параметр *flags* , чтобы указать, чтобы получить доступ к 4 ГБ виртуального адресного пространства.</span><span class="sxs-lookup"><span data-stu-id="d8e06-146">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8e06-147">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8e06-147">Return value</span></span>

<span data-ttu-id="d8e06-148">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d8e06-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d8e06-149">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d8e06-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d8e06-150">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ нотимпл, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d8e06-150">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_NOTIMPL, E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="d8e06-151">E \_ нотимпл возвращается при использовании шейдеров 1,1 (VS 1 1 \_ \_ и PS \_ 1 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="d8e06-151">E\_NOTIMPL is returned if you're using 1.1 shaders (vs\_1\_1 and ps\_1\_1).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8e06-152">Требования</span><span class="sxs-lookup"><span data-stu-id="d8e06-152">Requirements</span></span>



| <span data-ttu-id="d8e06-153">Требование</span><span class="sxs-lookup"><span data-stu-id="d8e06-153">Requirement</span></span> | <span data-ttu-id="d8e06-154">Значение</span><span class="sxs-lookup"><span data-stu-id="d8e06-154">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8e06-155">Header</span><span class="sxs-lookup"><span data-stu-id="d8e06-155">Header</span></span><br/>  | <dl> <span data-ttu-id="d8e06-156"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8e06-156"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d8e06-157">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d8e06-157">Library</span></span><br/> | <dl> <span data-ttu-id="d8e06-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8e06-158"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d8e06-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8e06-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8e06-160">Функции шейдера</span><span class="sxs-lookup"><span data-stu-id="d8e06-160">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="d8e06-161">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="d8e06-161">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="d8e06-162">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="d8e06-162">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
