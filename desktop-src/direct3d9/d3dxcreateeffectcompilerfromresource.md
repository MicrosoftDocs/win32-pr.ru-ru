---
description: Создает ID3DXEffectCompiler из описания ASCII Effect.
ms.assetid: 041e0a3f-3dc6-4cc3-8380-d4a79a3f647a
title: Функция D3DXCreateEffectCompilerFromResource (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1a3dabe0a2690c84e125af6d321397cbe3765f83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273827"
---
# <a name="d3dxcreateeffectcompilerfromresource-function"></a><span data-ttu-id="3e319-103">Функция D3DXCreateEffectCompilerFromResource</span><span class="sxs-lookup"><span data-stu-id="3e319-103">D3DXCreateEffectCompilerFromResource function</span></span>

<span data-ttu-id="3e319-104">Создает [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) из описания ASCII Effect.</span><span class="sxs-lookup"><span data-stu-id="3e319-104">Creates an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e319-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e319-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompilerFromResource(
  _In_        HMODULE              hSrcModule,
  _In_        LPCTSTR              pSrcResource,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="3e319-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e319-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e319-107">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e319-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e319-108">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e319-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e319-109">Обработчик для модуля, содержащего описание результата.</span><span class="sxs-lookup"><span data-stu-id="3e319-109">Handle to a module containing the effect description.</span></span> <span data-ttu-id="3e319-110">Если этот параметр имеет **значение NULL**, будет использоваться текущий модуль.</span><span class="sxs-lookup"><span data-stu-id="3e319-110">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="3e319-111">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e319-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e319-112">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e319-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e319-113">Указатель на ресурс.</span><span class="sxs-lookup"><span data-stu-id="3e319-113">Pointer to the resource.</span></span> <span data-ttu-id="3e319-114">Этот параметр поддерживает строки в Юникоде и ANSI.</span><span class="sxs-lookup"><span data-stu-id="3e319-114">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="3e319-115">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="3e319-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3e319-116">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e319-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e319-117">Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="3e319-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="3e319-118">Необязательный завершающий **нуль** массив структур [**D3DXMACRO**](d3dxmacro.md) , описывающих определения препроцессора.</span><span class="sxs-lookup"><span data-stu-id="3e319-118">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="3e319-119">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="3e319-119">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3e319-120">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e319-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e319-121">Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="3e319-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="3e319-122">Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include.</span><span class="sxs-lookup"><span data-stu-id="3e319-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="3e319-123">Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.</span><span class="sxs-lookup"><span data-stu-id="3e319-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="3e319-124">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e319-124">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e319-125">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e319-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e319-126">Параметры компиляции, определяемые различными флагами (см. раздел [Флаги D3DXSHADER](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="3e319-126">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="3e319-127">Компилятор Direct3D 10 HLSL теперь является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3e319-127">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="3e319-128">Дополнительные сведения см. в разделе [средство компилятора Effect](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="3e319-128">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="3e319-129">*ппеффекткомпилер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3e319-129">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e319-130">Тип: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="3e319-130">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="3e319-131">Адрес указателя на интерфейс [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) , содержащий компилятор эффектов.</span><span class="sxs-lookup"><span data-stu-id="3e319-131">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface, containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="3e319-132">*пппарсиррорс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3e319-132">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e319-133">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3e319-133">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3e319-134">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) , содержащий все сообщения об ошибках, произошедшие во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="3e319-134">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="3e319-135">Этот параметр может иметь значение **null** , чтобы игнорировать сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="3e319-135">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e319-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e319-136">Return value</span></span>

<span data-ttu-id="3e319-137">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3e319-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3e319-138">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3e319-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3e319-139">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3e319-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e319-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3e319-140">Remarks</span></span>

<span data-ttu-id="3e319-141">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="3e319-141">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="3e319-142">В противном случае тип данных LPCTSTR разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="3e319-142">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="3e319-143">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="3e319-143">The compiler setting also determines the function version.</span></span> <span data-ttu-id="3e319-144">Если определен Юникод, вызов функции разрешается в D3DXCreateEffectCompilerFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="3e319-144">If Unicode is defined, the function call resolves to D3DXCreateEffectCompilerFromResourceW.</span></span> <span data-ttu-id="3e319-145">В противном случае вызов функции разрешается в D3DXCreateEffectCompilerFromResourceA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="3e319-145">Otherwise, the function call resolves to D3DXCreateEffectCompilerFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e319-146">Требования</span><span class="sxs-lookup"><span data-stu-id="3e319-146">Requirements</span></span>



| <span data-ttu-id="3e319-147">Требование</span><span class="sxs-lookup"><span data-stu-id="3e319-147">Requirement</span></span> | <span data-ttu-id="3e319-148">Значение</span><span class="sxs-lookup"><span data-stu-id="3e319-148">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e319-149">Header</span><span class="sxs-lookup"><span data-stu-id="3e319-149">Header</span></span><br/>  | <dl> <span data-ttu-id="3e319-150"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e319-150"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="3e319-151">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3e319-151">Library</span></span><br/> | <dl> <span data-ttu-id="3e319-152"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e319-152"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3e319-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e319-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e319-154">Функции эффектов</span><span class="sxs-lookup"><span data-stu-id="3e319-154">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="3e319-155">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="3e319-155">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="3e319-156">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="3e319-156">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> </dl>

 

 
