---
description: Предварительно обрабатывает файл шейдера без выполнения компиляции. Это разрешает все \# определения и \# включает, предоставляя автономный шейдер для последующей компиляции.
ms.assetid: 1be68cc0-b4a3-41b4-b956-b96ed439be9e
title: Функция D3DXPreprocessShaderFromFile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1ba9cf35418bbbe6fe4b39341031fd1e056b27dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354780"
---
# <a name="d3dxpreprocessshaderfromfile-function"></a><span data-ttu-id="64e0a-104">Функция D3DXPreprocessShaderFromFile</span><span class="sxs-lookup"><span data-stu-id="64e0a-104">D3DXPreprocessShaderFromFile function</span></span>

<span data-ttu-id="64e0a-105">Предварительно обрабатывает файл шейдера без выполнения компиляции.</span><span class="sxs-lookup"><span data-stu-id="64e0a-105">Preprocesses a shader file without performing compilation.</span></span> <span data-ttu-id="64e0a-106">Это разрешает все \# определения и \# включает, предоставляя автономный шейдер для последующей компиляции.</span><span class="sxs-lookup"><span data-stu-id="64e0a-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="64e0a-107">Вместо использования этой устаревшей функции рекомендуется использовать API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="64e0a-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="64e0a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64e0a-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShaderFromFile(
  _In_        LPCSTR        pSrcFile,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="64e0a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="64e0a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64e0a-110">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64e0a-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64e0a-111">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64e0a-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64e0a-112">Указатель на строку, указывающую имя файла шейдера.</span><span class="sxs-lookup"><span data-stu-id="64e0a-112">Pointer to a string that specifies the filename of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="64e0a-113">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64e0a-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64e0a-114">Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="64e0a-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="64e0a-115">Необязательный массив структур [**D3DXMACRO**](d3dxmacro.md) , заканчивающийся **нулевым значением** .</span><span class="sxs-lookup"><span data-stu-id="64e0a-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="64e0a-116">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="64e0a-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="64e0a-117">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64e0a-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64e0a-118">Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="64e0a-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="64e0a-119">Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include.</span><span class="sxs-lookup"><span data-stu-id="64e0a-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="64e0a-120">Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.</span><span class="sxs-lookup"><span data-stu-id="64e0a-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="64e0a-121">*ппшадертекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="64e0a-121">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64e0a-122">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="64e0a-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="64e0a-123">Возвращает буфер, содержащий одну крупную строку, представляющую полученный отформатированный поток токенов.</span><span class="sxs-lookup"><span data-stu-id="64e0a-123">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="64e0a-124">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="64e0a-124">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64e0a-125">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="64e0a-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="64e0a-126">Возвращает буфер, содержащий список ошибок и предупреждений, обнаруженных во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="64e0a-126">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="64e0a-127">Это те же сообщения, которые отладчик отображает при работе в режиме отладки.</span><span class="sxs-lookup"><span data-stu-id="64e0a-127">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="64e0a-128">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="64e0a-128">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64e0a-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64e0a-129">Return value</span></span>

<span data-ttu-id="64e0a-130">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="64e0a-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="64e0a-131">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="64e0a-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="64e0a-132">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="64e0a-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="64e0a-133">Требования</span><span class="sxs-lookup"><span data-stu-id="64e0a-133">Requirements</span></span>



| <span data-ttu-id="64e0a-134">Требование</span><span class="sxs-lookup"><span data-stu-id="64e0a-134">Requirement</span></span> | <span data-ttu-id="64e0a-135">Значение</span><span class="sxs-lookup"><span data-stu-id="64e0a-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="64e0a-136">Header</span><span class="sxs-lookup"><span data-stu-id="64e0a-136">Header</span></span><br/>  | <dl> <span data-ttu-id="64e0a-137"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="64e0a-137"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="64e0a-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="64e0a-138">Library</span></span><br/> | <dl> <span data-ttu-id="64e0a-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64e0a-139"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="64e0a-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64e0a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64e0a-141">Функции шейдера</span><span class="sxs-lookup"><span data-stu-id="64e0a-141">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="64e0a-142">**D3DXPreprocessShader**</span><span class="sxs-lookup"><span data-stu-id="64e0a-142">**D3DXPreprocessShader**</span></span>](d3dxpreprocessshader.md)
</dt> <dt>

[<span data-ttu-id="64e0a-143">**D3DXPreprocessShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="64e0a-143">**D3DXPreprocessShaderFromResource**</span></span>](d3dxpreprocessshaderfromresource.md)
</dt> </dl>

 

 
