---
description: Сборка шейдера.
ms.assetid: 2977b64a-b8cc-454b-8e28-291f6f2c6fc1
title: Функция D3DXAssembleShaderFromFile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6e355f6ce51158f72757f771114346899557c59
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703826"
---
# <a name="d3dxassembleshaderfromfile-function"></a><span data-ttu-id="3567d-103">Функция D3DXAssembleShaderFromFile</span><span class="sxs-lookup"><span data-stu-id="3567d-103">D3DXAssembleShaderFromFile function</span></span>

<span data-ttu-id="3567d-104">Сборка шейдера.</span><span class="sxs-lookup"><span data-stu-id="3567d-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="3567d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3567d-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShaderFromFile(
  _In_        LPCTSTR       pSrcFile,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="3567d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3567d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3567d-107">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3567d-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3567d-108">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3567d-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3567d-109">Указатель на строку, указывающую имя файла.</span><span class="sxs-lookup"><span data-stu-id="3567d-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="3567d-110">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="3567d-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="3567d-111">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="3567d-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="3567d-112">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="3567d-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3567d-113">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3567d-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3567d-114">Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="3567d-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="3567d-115">Необязательный массив структур [**D3DXMACRO**](d3dxmacro.md) , заканчивающийся **нулевым значением** .</span><span class="sxs-lookup"><span data-stu-id="3567d-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="3567d-116">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="3567d-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3567d-117">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3567d-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3567d-118">Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="3567d-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="3567d-119">Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include.</span><span class="sxs-lookup"><span data-stu-id="3567d-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="3567d-120">Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.</span><span class="sxs-lookup"><span data-stu-id="3567d-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="3567d-121">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3567d-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3567d-122">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3567d-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3567d-123">Параметры компиляции, определяемые различными флагами.</span><span class="sxs-lookup"><span data-stu-id="3567d-123">Compile options identified by various flags.</span></span> <span data-ttu-id="3567d-124">Компилятор Direct3D 10 HLSL теперь является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3567d-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="3567d-125">Дополнительные сведения см. в разделе [Флаги D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="3567d-125">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="3567d-126">*ппшадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3567d-126">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3567d-127">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3567d-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3567d-128">Возвращает буфер, содержащий созданный шейдер.</span><span class="sxs-lookup"><span data-stu-id="3567d-128">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="3567d-129">Этот буфер содержит скомпилированный код шейдера, а также любые внедренные сведения о таблицах отладки и символов.</span><span class="sxs-lookup"><span data-stu-id="3567d-129">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="3567d-130">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3567d-130">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3567d-131">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3567d-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3567d-132">Возвращает буфер, содержащий список ошибок и предупреждений, обнаруженных во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="3567d-132">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="3567d-133">Это те же сообщения, которые отладчик отображает при работе в режиме отладки.</span><span class="sxs-lookup"><span data-stu-id="3567d-133">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="3567d-134">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="3567d-134">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3567d-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3567d-135">Return value</span></span>

<span data-ttu-id="3567d-136">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3567d-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3567d-137">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3567d-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3567d-138">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3567d-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3567d-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3567d-139">Remarks</span></span>

<span data-ttu-id="3567d-140">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="3567d-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="3567d-141">Если определен Юникод, вызов функции разрешается в D3DXAssembleShaderFromFileW.</span><span class="sxs-lookup"><span data-stu-id="3567d-141">If Unicode is defined, the function call resolves to D3DXAssembleShaderFromFileW.</span></span> <span data-ttu-id="3567d-142">В противном случае вызов функции разрешается в D3DXAssembleShaderFromFileA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="3567d-142">Otherwise, the function call resolves to D3DXAssembleShaderFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="3567d-143">Требования</span><span class="sxs-lookup"><span data-stu-id="3567d-143">Requirements</span></span>



| <span data-ttu-id="3567d-144">Требование</span><span class="sxs-lookup"><span data-stu-id="3567d-144">Requirement</span></span> | <span data-ttu-id="3567d-145">Значение</span><span class="sxs-lookup"><span data-stu-id="3567d-145">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3567d-146">Header</span><span class="sxs-lookup"><span data-stu-id="3567d-146">Header</span></span><br/>  | <dl> <span data-ttu-id="3567d-147"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="3567d-147"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="3567d-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3567d-148">Library</span></span><br/> | <dl> <span data-ttu-id="3567d-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3567d-149"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3567d-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3567d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3567d-151">Функции шейдера</span><span class="sxs-lookup"><span data-stu-id="3567d-151">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="3567d-152">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="3567d-152">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="3567d-153">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="3567d-153">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
