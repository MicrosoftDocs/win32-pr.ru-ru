---
description: Сборка шейдера.
ms.assetid: 24c3dcae-9397-4856-b072-0ae340157bf9
title: Функция D3DXAssembleShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7268d394021c7dc1be665f8ed8781a827d1fcdb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694200"
---
# <a name="d3dxassembleshader-function"></a><span data-ttu-id="1bdf2-103">Функция D3DXAssembleShader</span><span class="sxs-lookup"><span data-stu-id="1bdf2-103">D3DXAssembleShader function</span></span>

<span data-ttu-id="1bdf2-104">Сборка шейдера.</span><span class="sxs-lookup"><span data-stu-id="1bdf2-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bdf2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1bdf2-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShader(
  _In_        LPCSTR        pSrcData,
  _In_        UINT          SrcDataLen,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="1bdf2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1bdf2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bdf2-107">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1bdf2-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bdf2-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1bdf2-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1bdf2-109">Указатель на буфер памяти, содержащий данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="1bdf2-109">Pointer to a memory buffer that contains the shader data.</span></span>

</dd> <dt>

<span data-ttu-id="1bdf2-110">*Сркдатален* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1bdf2-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bdf2-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1bdf2-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1bdf2-112">Длина данных эффектов в байтах.</span><span class="sxs-lookup"><span data-stu-id="1bdf2-112">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1bdf2-113">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1bdf2-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bdf2-114">Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="1bdf2-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="1bdf2-115">Необязательный массив структур [**D3DXMACRO**](d3dxmacro.md) , заканчивающийся **нулевым значением** .</span><span class="sxs-lookup"><span data-stu-id="1bdf2-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="1bdf2-116">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="1bdf2-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1bdf2-117">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1bdf2-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bdf2-118">Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="1bdf2-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="1bdf2-119">Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include.</span><span class="sxs-lookup"><span data-stu-id="1bdf2-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="1bdf2-120">Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.</span><span class="sxs-lookup"><span data-stu-id="1bdf2-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="1bdf2-121">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1bdf2-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bdf2-122">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1bdf2-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1bdf2-123">Параметры компиляции, определяемые различными флагами.</span><span class="sxs-lookup"><span data-stu-id="1bdf2-123">Compile options identified by various flags.</span></span> <span data-ttu-id="1bdf2-124">Компилятор Direct3D 10 HLSL теперь является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1bdf2-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="1bdf2-125">Дополнительные сведения см. в разделе [Флаги D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="1bdf2-125">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="1bdf2-126">*ппшадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1bdf2-126">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1bdf2-127">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1bdf2-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1bdf2-128">Возвращает буфер, содержащий созданный шейдер.</span><span class="sxs-lookup"><span data-stu-id="1bdf2-128">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="1bdf2-129">Этот буфер содержит скомпилированный код шейдера, а также любые внедренные сведения о таблицах отладки и символов.</span><span class="sxs-lookup"><span data-stu-id="1bdf2-129">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="1bdf2-130">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1bdf2-130">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1bdf2-131">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1bdf2-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1bdf2-132">Возвращает буфер, содержащий список ошибок и предупреждений, обнаруженных во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="1bdf2-132">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="1bdf2-133">Это те же сообщения, которые отладчик отображает при работе в режиме отладки.</span><span class="sxs-lookup"><span data-stu-id="1bdf2-133">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="1bdf2-134">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="1bdf2-134">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bdf2-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1bdf2-135">Return value</span></span>

<span data-ttu-id="1bdf2-136">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1bdf2-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1bdf2-137">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="1bdf2-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1bdf2-138">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1bdf2-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bdf2-139">Требования</span><span class="sxs-lookup"><span data-stu-id="1bdf2-139">Requirements</span></span>



| <span data-ttu-id="1bdf2-140">Требование</span><span class="sxs-lookup"><span data-stu-id="1bdf2-140">Requirement</span></span> | <span data-ttu-id="1bdf2-141">Значение</span><span class="sxs-lookup"><span data-stu-id="1bdf2-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bdf2-142">Header</span><span class="sxs-lookup"><span data-stu-id="1bdf2-142">Header</span></span><br/>  | <dl> <span data-ttu-id="1bdf2-143"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bdf2-143"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1bdf2-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1bdf2-144">Library</span></span><br/> | <dl> <span data-ttu-id="1bdf2-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bdf2-145"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1bdf2-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1bdf2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bdf2-147">Функции шейдера</span><span class="sxs-lookup"><span data-stu-id="1bdf2-147">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="1bdf2-148">**D3DXAssembleShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="1bdf2-148">**D3DXAssembleShaderFromFile**</span></span>](d3dxassembleshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="1bdf2-149">**D3DXAssembleShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="1bdf2-149">**D3DXAssembleShaderFromResource**</span></span>](d3dxassembleshaderfromresource.md)
</dt> </dl>

 

 
