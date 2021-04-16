---
description: Предварительно обрабатывает шейдер без выполнения компиляции. Это разрешает все \# определения и \# включает, предоставляя автономный шейдер для последующей компиляции.
ms.assetid: d91258ed-6206-487a-aa81-e7c2bcea21ea
title: Функция D3DXPreprocessShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 042cebe4e678ac1715a37ec3425ec0f21561797c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547831"
---
# <a name="d3dxpreprocessshader-function"></a><span data-ttu-id="c7c41-104">Функция D3DXPreprocessShader</span><span class="sxs-lookup"><span data-stu-id="c7c41-104">D3DXPreprocessShader function</span></span>

<span data-ttu-id="c7c41-105">Предварительно обрабатывает шейдер без выполнения компиляции.</span><span class="sxs-lookup"><span data-stu-id="c7c41-105">Preprocesses a shader without performing compilation.</span></span> <span data-ttu-id="c7c41-106">Это разрешает все \# определения и \# включает, предоставляя автономный шейдер для последующей компиляции.</span><span class="sxs-lookup"><span data-stu-id="c7c41-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="c7c41-107">Вместо использования этой устаревшей функции рекомендуется использовать API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="c7c41-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c7c41-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7c41-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShader(
  _In_        LPCSTR        pSrcData,
  _In_        UINT          SrcDataSize,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="c7c41-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7c41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7c41-110">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7c41-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c41-111">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7c41-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c7c41-112">Указатель на строку, содержащую шейдер.</span><span class="sxs-lookup"><span data-stu-id="c7c41-112">Pointer to a string that contains the shader.</span></span>

</dd> <dt>

<span data-ttu-id="c7c41-113">*Сркдатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7c41-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c41-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7c41-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c7c41-115">Длина данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="c7c41-115">Length of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c7c41-116">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7c41-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c41-117">Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="c7c41-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="c7c41-118">Необязательный массив структур [**D3DXMACRO**](d3dxmacro.md) , заканчивающийся **нулевым значением** .</span><span class="sxs-lookup"><span data-stu-id="c7c41-118">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="c7c41-119">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="c7c41-119">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c7c41-120">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7c41-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c41-121">Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="c7c41-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="c7c41-122">Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include.</span><span class="sxs-lookup"><span data-stu-id="c7c41-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="c7c41-123">Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.</span><span class="sxs-lookup"><span data-stu-id="c7c41-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="c7c41-124">*ппшадертекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c7c41-124">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c41-125">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c7c41-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c7c41-126">Возвращает буфер, содержащий одну крупную строку, представляющую полученный отформатированный поток токенов.</span><span class="sxs-lookup"><span data-stu-id="c7c41-126">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="c7c41-127">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c7c41-127">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c41-128">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c7c41-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c7c41-129">Возвращает буфер, содержащий список ошибок и предупреждений, обнаруженных во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="c7c41-129">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="c7c41-130">Это те же сообщения, которые отладчик отображает при работе в режиме отладки.</span><span class="sxs-lookup"><span data-stu-id="c7c41-130">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="c7c41-131">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="c7c41-131">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7c41-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7c41-132">Return value</span></span>

<span data-ttu-id="c7c41-133">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c7c41-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c7c41-134">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c7c41-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c7c41-135">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c7c41-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7c41-136">Требования</span><span class="sxs-lookup"><span data-stu-id="c7c41-136">Requirements</span></span>



| <span data-ttu-id="c7c41-137">Требование</span><span class="sxs-lookup"><span data-stu-id="c7c41-137">Requirement</span></span> | <span data-ttu-id="c7c41-138">Значение</span><span class="sxs-lookup"><span data-stu-id="c7c41-138">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c41-139">Header</span><span class="sxs-lookup"><span data-stu-id="c7c41-139">Header</span></span><br/>  | <dl> <span data-ttu-id="c7c41-140"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7c41-140"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c7c41-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c7c41-141">Library</span></span><br/> | <dl> <span data-ttu-id="c7c41-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7c41-142"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c7c41-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7c41-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7c41-144">Функции шейдера</span><span class="sxs-lookup"><span data-stu-id="c7c41-144">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="c7c41-145">**D3DXPreprocessShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="c7c41-145">**D3DXPreprocessShaderFromFile**</span></span>](d3dxpreprocessshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="c7c41-146">**D3DXPreprocessShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="c7c41-146">**D3DXPreprocessShaderFromResource**</span></span>](d3dxpreprocessshaderfromresource.md)
</dt> </dl>

 

 
