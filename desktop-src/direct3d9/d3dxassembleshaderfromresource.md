---
description: Функция D3DXAssembleShaderFromResource — формирование шейдера.
ms.assetid: a0d31b15-db79-4aa8-afd8-fa1e20c61725
title: Функция D3DXAssembleShaderFromResource (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 78df978201df37269b7d33058effc16eadc9d16f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116021"
---
# <a name="d3dxassembleshaderfromresource-function"></a><span data-ttu-id="8db7c-103">Функция D3DXAssembleShaderFromResource</span><span class="sxs-lookup"><span data-stu-id="8db7c-103">D3DXAssembleShaderFromResource function</span></span>

<span data-ttu-id="8db7c-104">Сборка шейдера.</span><span class="sxs-lookup"><span data-stu-id="8db7c-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="8db7c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8db7c-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShaderFromResource(
  _In_        HMODULE       hSrcModule,
  _In_        LPCTSTR       pSrcResource,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="8db7c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8db7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8db7c-107">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8db7c-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8db7c-108">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8db7c-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8db7c-109">Обработчик для модуля, содержащего описание результата.</span><span class="sxs-lookup"><span data-stu-id="8db7c-109">Handle to a module containing the effect description.</span></span> <span data-ttu-id="8db7c-110">Если этот параметр имеет **значение NULL**, будет использоваться текущий модуль.</span><span class="sxs-lookup"><span data-stu-id="8db7c-110">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="8db7c-111">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8db7c-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8db7c-112">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8db7c-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8db7c-113">Указатель на строку, указывающую имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="8db7c-113">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="8db7c-114">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="8db7c-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="8db7c-115">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="8db7c-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="8db7c-116">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="8db7c-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8db7c-117">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8db7c-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8db7c-118">Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="8db7c-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="8db7c-119">Необязательный массив структур [**D3DXMACRO**](d3dxmacro.md) , заканчивающийся **нулевым значением** .</span><span class="sxs-lookup"><span data-stu-id="8db7c-119">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="8db7c-120">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="8db7c-120">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8db7c-121">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8db7c-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8db7c-122">Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="8db7c-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="8db7c-123">Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include.</span><span class="sxs-lookup"><span data-stu-id="8db7c-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="8db7c-124">Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.</span><span class="sxs-lookup"><span data-stu-id="8db7c-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="8db7c-125">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8db7c-125">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8db7c-126">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8db7c-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8db7c-127">Параметры компиляции, определяемые различными флагами.</span><span class="sxs-lookup"><span data-stu-id="8db7c-127">Compile options identified by various flags.</span></span> <span data-ttu-id="8db7c-128">Компилятор Direct3D 10 HLSL теперь является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8db7c-128">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="8db7c-129">Дополнительные сведения см. в разделе [Флаги D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="8db7c-129">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="8db7c-130">*ппшадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8db7c-130">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8db7c-131">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8db7c-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8db7c-132">Возвращает буфер, содержащий созданный шейдер.</span><span class="sxs-lookup"><span data-stu-id="8db7c-132">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="8db7c-133">Этот буфер содержит скомпилированный код шейдера, а также любые внедренные сведения о таблицах отладки и символов.</span><span class="sxs-lookup"><span data-stu-id="8db7c-133">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="8db7c-134">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8db7c-134">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8db7c-135">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8db7c-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8db7c-136">Возвращает буфер, содержащий список ошибок и предупреждений, обнаруженных во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="8db7c-136">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="8db7c-137">Это те же сообщения, которые отладчик отображает при работе в режиме отладки.</span><span class="sxs-lookup"><span data-stu-id="8db7c-137">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="8db7c-138">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="8db7c-138">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8db7c-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8db7c-139">Return value</span></span>

<span data-ttu-id="8db7c-140">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8db7c-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8db7c-141">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="8db7c-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8db7c-142">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8db7c-142">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8db7c-143">Remarks</span><span class="sxs-lookup"><span data-stu-id="8db7c-143">Remarks</span></span>

<span data-ttu-id="8db7c-144">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="8db7c-144">The compiler setting also determines the function version.</span></span> <span data-ttu-id="8db7c-145">Если определен Юникод, вызов функции разрешается в D3DXAssembleShaderFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="8db7c-145">If Unicode is defined, the function call resolves to D3DXAssembleShaderFromResourceW.</span></span> <span data-ttu-id="8db7c-146">В противном случае вызов функции разрешается в D3DXAssembleShaderFromResourceA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="8db7c-146">Otherwise, the function call resolves to D3DXAssembleShaderFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="8db7c-147">Требования</span><span class="sxs-lookup"><span data-stu-id="8db7c-147">Requirements</span></span>



| <span data-ttu-id="8db7c-148">Требование</span><span class="sxs-lookup"><span data-stu-id="8db7c-148">Requirement</span></span> | <span data-ttu-id="8db7c-149">Значение</span><span class="sxs-lookup"><span data-stu-id="8db7c-149">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8db7c-150">Header</span><span class="sxs-lookup"><span data-stu-id="8db7c-150">Header</span></span><br/>  | <dl> <span data-ttu-id="8db7c-151"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8db7c-151"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8db7c-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8db7c-152">Library</span></span><br/> | <dl> <span data-ttu-id="8db7c-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8db7c-153"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8db7c-154">См. также</span><span class="sxs-lookup"><span data-stu-id="8db7c-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8db7c-155">Функции шейдера</span><span class="sxs-lookup"><span data-stu-id="8db7c-155">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="8db7c-156">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="8db7c-156">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="8db7c-157">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="8db7c-157">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
