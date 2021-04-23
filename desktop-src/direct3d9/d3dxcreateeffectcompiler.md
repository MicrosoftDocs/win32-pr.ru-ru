---
description: Создает компилятор эффектов из описания ASCII Effect.
ms.assetid: 96e883f4-4055-4b8b-940a-164bbf893af4
title: Функция D3DXCreateEffectCompiler (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompiler
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 513b11ba12abe05126c122f8bc9bfcfa978df3fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821397"
---
# <a name="d3dxcreateeffectcompiler-function"></a><span data-ttu-id="25506-103">Функция D3DXCreateEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="25506-103">D3DXCreateEffectCompiler function</span></span>

<span data-ttu-id="25506-104">Создает компилятор эффектов из описания ASCII Effect.</span><span class="sxs-lookup"><span data-stu-id="25506-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="25506-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25506-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompiler(
  _In_        LPCSTR               pSrcData,
  _In_        UINT                 SrcDataLen,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="25506-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="25506-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25506-107">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25506-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25506-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25506-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25506-109">Указатель на буфер, содержащий описание действия.</span><span class="sxs-lookup"><span data-stu-id="25506-109">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="25506-110">*Сркдатален* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25506-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25506-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25506-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25506-112">Длина данных эффектов в байтах.</span><span class="sxs-lookup"><span data-stu-id="25506-112">Length, in bytes, of the effect data.</span></span>

</dd> <dt>

<span data-ttu-id="25506-113">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25506-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25506-114">Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="25506-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="25506-115">Необязательный завершающий **нуль** массив структур [**D3DXMACRO**](d3dxmacro.md) , описывающих определения препроцессора.</span><span class="sxs-lookup"><span data-stu-id="25506-115">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="25506-116">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="25506-116">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="25506-117">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25506-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25506-118">Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="25506-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="25506-119">Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include.</span><span class="sxs-lookup"><span data-stu-id="25506-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="25506-120">Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.</span><span class="sxs-lookup"><span data-stu-id="25506-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="25506-121">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25506-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25506-122">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25506-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25506-123">Параметры компиляции, определяемые различными флагами (см. раздел [Флаги D3DXSHADER](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="25506-123">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="25506-124">Компилятор Direct3D 10 HLSL теперь является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="25506-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="25506-125">Дополнительные сведения см. в разделе [средство компилятора Effect](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="25506-125">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="25506-126">*ппеффекткомпилер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="25506-126">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25506-127">Тип: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="25506-127">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="25506-128">Адрес указателя на интерфейс [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) , содержащий компилятор эффектов.</span><span class="sxs-lookup"><span data-stu-id="25506-128">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="25506-129">*пппарсиррорс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="25506-129">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25506-130">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="25506-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="25506-131">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) , содержащий любые сообщения об ошибках, произошедшие во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="25506-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="25506-132">Этот параметр может иметь значение **null** , чтобы игнорировать сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="25506-132">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25506-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25506-133">Return value</span></span>

<span data-ttu-id="25506-134">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="25506-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="25506-135">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="25506-135">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="25506-136">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="25506-136">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="25506-137">Требования</span><span class="sxs-lookup"><span data-stu-id="25506-137">Requirements</span></span>



| <span data-ttu-id="25506-138">Требование</span><span class="sxs-lookup"><span data-stu-id="25506-138">Requirement</span></span> | <span data-ttu-id="25506-139">Значение</span><span class="sxs-lookup"><span data-stu-id="25506-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="25506-140">Header</span><span class="sxs-lookup"><span data-stu-id="25506-140">Header</span></span><br/>  | <dl> <span data-ttu-id="25506-141"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="25506-141"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="25506-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="25506-142">Library</span></span><br/> | <dl> <span data-ttu-id="25506-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25506-143"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="25506-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25506-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25506-145">Функции эффектов</span><span class="sxs-lookup"><span data-stu-id="25506-145">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="25506-146">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="25506-146">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[<span data-ttu-id="25506-147">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="25506-147">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
