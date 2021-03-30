---
description: Скомпилируйте файл шейдера.
ms.assetid: 9b19ab67-d5d5-482d-b3fe-ce20b64d7ad8
title: Функция D3DXCompileShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65dd9f74280abe7ee2fe427a4772b14b88742e97
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354730"
---
# <a name="d3dxcompileshader-function"></a><span data-ttu-id="247fc-103">Функция D3DXCompileShader</span><span class="sxs-lookup"><span data-stu-id="247fc-103">D3DXCompileShader function</span></span>

<span data-ttu-id="247fc-104">Скомпилируйте файл шейдера.</span><span class="sxs-lookup"><span data-stu-id="247fc-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="247fc-105">Вместо использования этой устаревшей функции рекомендуется компилировать автономно с помощью Fxc.exe компилятора командной строки или использовать API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="247fc-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="247fc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="247fc-106">Syntax</span></span>


```C++
HRESULT D3DXCompileShader(
  _In_        LPCSTR              pSrcData,
  _In_        UINT                srcDataLen,
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



## <a name="parameters"></a><span data-ttu-id="247fc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="247fc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="247fc-108">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="247fc-108">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="247fc-109">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="247fc-109">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="247fc-110">Указатель на строку, содержащую шейдер.</span><span class="sxs-lookup"><span data-stu-id="247fc-110">Pointer to a string that contains the shader.</span></span>

</dd> <dt>

<span data-ttu-id="247fc-111">*сркдатален* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="247fc-111">*srcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="247fc-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="247fc-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="247fc-113">Длина данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="247fc-113">Length of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="247fc-114">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="247fc-114">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="247fc-115">Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="247fc-115">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="247fc-116">Необязательный массив структур [**D3DXMACRO**](d3dxmacro.md) , заканчивающийся **нулевым значением** .</span><span class="sxs-lookup"><span data-stu-id="247fc-116">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="247fc-117">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="247fc-117">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="247fc-118">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="247fc-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="247fc-119">Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="247fc-119">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="247fc-120">Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include.</span><span class="sxs-lookup"><span data-stu-id="247fc-120">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="247fc-121">Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.</span><span class="sxs-lookup"><span data-stu-id="247fc-121">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="247fc-122">*пфунктионнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="247fc-122">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="247fc-123">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="247fc-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="247fc-124">Указатель на строку, содержащую имя функции точки входа шейдера, в которой начинается выполнение.</span><span class="sxs-lookup"><span data-stu-id="247fc-124">Pointer to a string that contains the name of the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="247fc-125">*ппрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="247fc-125">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="247fc-126">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="247fc-126">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="247fc-127">Указатель на профиль шейдера, который определяет набор инструкций шейдера.</span><span class="sxs-lookup"><span data-stu-id="247fc-127">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="247fc-128">Список доступных профилей см. в разделе [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) или [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="247fc-128">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="247fc-129">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="247fc-129">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="247fc-130">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="247fc-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="247fc-131">Параметры компиляции, определяемые различными флагами.</span><span class="sxs-lookup"><span data-stu-id="247fc-131">Compile options identified by various flags.</span></span> <span data-ttu-id="247fc-132">Компилятор Direct3D 10 HLSL теперь является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="247fc-132">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="247fc-133">Дополнительные сведения см. в разделе [Флаги D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="247fc-133">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="247fc-134">*ппшадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="247fc-134">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="247fc-135">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="247fc-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="247fc-136">Возвращает буфер, содержащий созданный шейдер.</span><span class="sxs-lookup"><span data-stu-id="247fc-136">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="247fc-137">Этот буфер содержит скомпилированный код шейдера, а также любые внедренные сведения о таблицах отладки и символов.</span><span class="sxs-lookup"><span data-stu-id="247fc-137">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="247fc-138">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="247fc-138">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="247fc-139">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="247fc-139">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="247fc-140">Возвращает буфер, содержащий список ошибок и предупреждений, обнаруженных во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="247fc-140">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="247fc-141">Это те же сообщения, которые отладчик отображает при работе в режиме отладки.</span><span class="sxs-lookup"><span data-stu-id="247fc-141">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="247fc-142">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="247fc-142">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="247fc-143">*ппконстанттабле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="247fc-143">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="247fc-144">Тип: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="247fc-144">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="247fc-145">Возвращает интерфейс [**ID3DXConstantTable**](id3dxconstanttable.md) , который можно использовать для доступа к константам шейдера.</span><span class="sxs-lookup"><span data-stu-id="247fc-145">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="247fc-146">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="247fc-146">This value can be **NULL**.</span></span> <span data-ttu-id="247fc-147">Если приложение компилируется как большой адрес (то есть для работы с адресами, превышающими 2 ГБ, используется параметр компоновщика/LARGEADDRESSAWARE), этот параметр использовать нельзя, и его значение должно быть равно **null**.</span><span class="sxs-lookup"><span data-stu-id="247fc-147">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="247fc-148">Вместо этого необходимо использовать функцию [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) , чтобы извлечь таблицу-константу шейдера, внедренную в шейдер.</span><span class="sxs-lookup"><span data-stu-id="247fc-148">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="247fc-149">В этом вызове **D3DXGetShaderConstantTableEx** необходимо передать флаг **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** в параметр *flags* , чтобы указать, чтобы получить доступ к 4 ГБ виртуального адресного пространства.</span><span class="sxs-lookup"><span data-stu-id="247fc-149">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="247fc-150">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="247fc-150">Return value</span></span>

<span data-ttu-id="247fc-151">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="247fc-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="247fc-152">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="247fc-152">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="247fc-153">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="247fc-153">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="247fc-154">Требования</span><span class="sxs-lookup"><span data-stu-id="247fc-154">Requirements</span></span>



| <span data-ttu-id="247fc-155">Требование</span><span class="sxs-lookup"><span data-stu-id="247fc-155">Requirement</span></span> | <span data-ttu-id="247fc-156">Значение</span><span class="sxs-lookup"><span data-stu-id="247fc-156">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="247fc-157">Header</span><span class="sxs-lookup"><span data-stu-id="247fc-157">Header</span></span><br/>  | <dl> <span data-ttu-id="247fc-158"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="247fc-158"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="247fc-159">Библиотека</span><span class="sxs-lookup"><span data-stu-id="247fc-159">Library</span></span><br/> | <dl> <span data-ttu-id="247fc-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="247fc-160"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="247fc-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="247fc-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="247fc-162">Функции шейдера</span><span class="sxs-lookup"><span data-stu-id="247fc-162">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="247fc-163">**D3DXCompileShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="247fc-163">**D3DXCompileShaderFromFile**</span></span>](d3dxcompileshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="247fc-164">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="247fc-164">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
