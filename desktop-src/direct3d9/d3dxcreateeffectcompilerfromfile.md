---
description: Функция D3DXCreateEffectCompilerFromFile — создает компилятор эффектов из описания ASCII-результата.
ms.assetid: 87438a1e-4149-42ef-aa7a-9f0549eb7982
title: Функция D3DXCreateEffectCompilerFromFile (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromFile
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0c054b31b1ab70d1378c794be13058204b994ee2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087982"
---
# <a name="d3dxcreateeffectcompilerfromfile-function"></a><span data-ttu-id="7f7c5-103">Функция D3DXCreateEffectCompilerFromFile</span><span class="sxs-lookup"><span data-stu-id="7f7c5-103">D3DXCreateEffectCompilerFromFile function</span></span>

<span data-ttu-id="7f7c5-104">Создает компилятор эффектов из описания ASCII Effect.</span><span class="sxs-lookup"><span data-stu-id="7f7c5-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f7c5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f7c5-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompilerFromFile(
  _In_        LPCTSTR              pSrcFile,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="7f7c5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f7c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f7c5-107">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f7c5-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f7c5-108">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f7c5-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f7c5-109">Указатель на имя файла.</span><span class="sxs-lookup"><span data-stu-id="7f7c5-109">Pointer to the filename.</span></span> <span data-ttu-id="7f7c5-110">Этот параметр поддерживает строки в Юникоде и ANSI.</span><span class="sxs-lookup"><span data-stu-id="7f7c5-110">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="7f7c5-111">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="7f7c5-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7f7c5-112">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f7c5-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f7c5-113">Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="7f7c5-113">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="7f7c5-114">Необязательный завершающий **нуль** массив структур [**D3DXMACRO**](d3dxmacro.md) , описывающих определения препроцессора.</span><span class="sxs-lookup"><span data-stu-id="7f7c5-114">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="7f7c5-115">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="7f7c5-115">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7f7c5-116">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f7c5-116">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f7c5-117">Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="7f7c5-117">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="7f7c5-118">Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include.</span><span class="sxs-lookup"><span data-stu-id="7f7c5-118">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="7f7c5-119">Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.</span><span class="sxs-lookup"><span data-stu-id="7f7c5-119">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="7f7c5-120">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f7c5-120">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f7c5-121">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f7c5-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f7c5-122">Параметры компиляции, определяемые различными флагами (см. раздел [Флаги D3DXSHADER](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="7f7c5-122">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="7f7c5-123">Компилятор Direct3D 10 HLSL теперь является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7f7c5-123">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="7f7c5-124">Дополнительные сведения см. в разделе [средство компилятора Effect](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="7f7c5-124">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="7f7c5-125">*ппеффекткомпилер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7f7c5-125">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f7c5-126">Тип: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="7f7c5-126">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="7f7c5-127">Адрес указателя на интерфейс [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) , содержащий компилятор эффектов.</span><span class="sxs-lookup"><span data-stu-id="7f7c5-127">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface, containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="7f7c5-128">*пппарсиррорс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7f7c5-128">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f7c5-129">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7f7c5-129">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7f7c5-130">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) , содержащий все сообщения об ошибках, произошедшие во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="7f7c5-130">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="7f7c5-131">Этот параметр может иметь значение **null** , чтобы игнорировать сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="7f7c5-131">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f7c5-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f7c5-132">Return value</span></span>

<span data-ttu-id="7f7c5-133">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7f7c5-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7f7c5-134">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7f7c5-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7f7c5-135">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7f7c5-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f7c5-136">Remarks</span><span class="sxs-lookup"><span data-stu-id="7f7c5-136">Remarks</span></span>

<span data-ttu-id="7f7c5-137">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="7f7c5-137">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="7f7c5-138">В противном случае тип данных LPCTSTR разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="7f7c5-138">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="7f7c5-139">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="7f7c5-139">The compiler setting also determines the function version.</span></span> <span data-ttu-id="7f7c5-140">Если определен Юникод, вызов функции разрешается в D3DXCreateEffectCompilerFromFileW.</span><span class="sxs-lookup"><span data-stu-id="7f7c5-140">If Unicode is defined, the function call resolves to D3DXCreateEffectCompilerFromFileW.</span></span> <span data-ttu-id="7f7c5-141">В противном случае вызов функции разрешается в D3DXCreateEffectCompilerFromFileA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="7f7c5-141">Otherwise, the function call resolves to D3DXCreateEffectCompilerFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f7c5-142">Требования</span><span class="sxs-lookup"><span data-stu-id="7f7c5-142">Requirements</span></span>



| <span data-ttu-id="7f7c5-143">Требование</span><span class="sxs-lookup"><span data-stu-id="7f7c5-143">Requirement</span></span> | <span data-ttu-id="7f7c5-144">Значение</span><span class="sxs-lookup"><span data-stu-id="7f7c5-144">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f7c5-145">Header</span><span class="sxs-lookup"><span data-stu-id="7f7c5-145">Header</span></span><br/>  | <dl> <span data-ttu-id="7f7c5-146"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f7c5-146"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="7f7c5-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7f7c5-147">Library</span></span><br/> | <dl> <span data-ttu-id="7f7c5-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f7c5-148"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7f7c5-149">См. также</span><span class="sxs-lookup"><span data-stu-id="7f7c5-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f7c5-150">Функции эффектов</span><span class="sxs-lookup"><span data-stu-id="7f7c5-150">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="7f7c5-151">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="7f7c5-151">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="7f7c5-152">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="7f7c5-152">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
