---
description: Предварительно обрабатывает ресурс шейдера без выполнения компиляции. Это разрешает все \# определения и \# включает, предоставляя автономный шейдер для последующей компиляции.
ms.assetid: a00c2db9-d7ba-48ab-80e3-dc20774e1b1e
title: Функция D3DXPreprocessShaderFromResource (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c45073d0b84ef6fb33d378c4c18f862f55c6b84a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354653"
---
# <a name="d3dxpreprocessshaderfromresource-function"></a><span data-ttu-id="3e34f-104">Функция D3DXPreprocessShaderFromResource</span><span class="sxs-lookup"><span data-stu-id="3e34f-104">D3DXPreprocessShaderFromResource function</span></span>

<span data-ttu-id="3e34f-105">Предварительно обрабатывает ресурс шейдера без выполнения компиляции.</span><span class="sxs-lookup"><span data-stu-id="3e34f-105">Preprocesses a shader resource without performing compilation.</span></span> <span data-ttu-id="3e34f-106">Это разрешает все \# определения и \# включает, предоставляя автономный шейдер для последующей компиляции.</span><span class="sxs-lookup"><span data-stu-id="3e34f-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="3e34f-107">Вместо использования этой устаревшей функции рекомендуется использовать API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="3e34f-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3e34f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e34f-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShaderFromResource(
  _In_        HMODULE       hSrcModule,
  _In_        LPCSTR        pSrcResource,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="3e34f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e34f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e34f-110">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e34f-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e34f-111">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e34f-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e34f-112">Обработчик для модуля, содержащего ресурс шейдера.</span><span class="sxs-lookup"><span data-stu-id="3e34f-112">Handle to the module that holds the shader resource.</span></span> <span data-ttu-id="3e34f-113">Если это значение равно **null**, будет использоваться текущий модуль.</span><span class="sxs-lookup"><span data-stu-id="3e34f-113">If this value is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="3e34f-114">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e34f-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e34f-115">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e34f-115">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e34f-116">Строка, представляющая имя ресурса в модуле.</span><span class="sxs-lookup"><span data-stu-id="3e34f-116">String that represents the name of the resource in the module.</span></span>

</dd> <dt>

<span data-ttu-id="3e34f-117">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e34f-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e34f-118">Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="3e34f-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="3e34f-119">Необязательный массив структур [**D3DXMACRO**](d3dxmacro.md) , заканчивающийся **нулевым значением** .</span><span class="sxs-lookup"><span data-stu-id="3e34f-119">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="3e34f-120">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="3e34f-120">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3e34f-121">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e34f-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e34f-122">Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="3e34f-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="3e34f-123">Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include.</span><span class="sxs-lookup"><span data-stu-id="3e34f-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="3e34f-124">Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.</span><span class="sxs-lookup"><span data-stu-id="3e34f-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="3e34f-125">*ппшадертекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3e34f-125">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e34f-126">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3e34f-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3e34f-127">Возвращает буфер, содержащий одну крупную строку, представляющую полученный отформатированный поток токенов.</span><span class="sxs-lookup"><span data-stu-id="3e34f-127">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="3e34f-128">*пперрормсгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3e34f-128">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e34f-129">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3e34f-129">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3e34f-130">Возвращает буфер, содержащий список ошибок и предупреждений, обнаруженных во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="3e34f-130">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="3e34f-131">Это те же сообщения, которые отладчик отображает при работе в режиме отладки.</span><span class="sxs-lookup"><span data-stu-id="3e34f-131">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="3e34f-132">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="3e34f-132">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e34f-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e34f-133">Return value</span></span>

<span data-ttu-id="3e34f-134">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3e34f-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3e34f-135">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3e34f-135">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3e34f-136">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3e34f-136">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e34f-137">Требования</span><span class="sxs-lookup"><span data-stu-id="3e34f-137">Requirements</span></span>



| <span data-ttu-id="3e34f-138">Требование</span><span class="sxs-lookup"><span data-stu-id="3e34f-138">Requirement</span></span> | <span data-ttu-id="3e34f-139">Значение</span><span class="sxs-lookup"><span data-stu-id="3e34f-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e34f-140">Header</span><span class="sxs-lookup"><span data-stu-id="3e34f-140">Header</span></span><br/>  | <dl> <span data-ttu-id="3e34f-141"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e34f-141"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="3e34f-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3e34f-142">Library</span></span><br/> | <dl> <span data-ttu-id="3e34f-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e34f-143"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3e34f-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e34f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e34f-145">Функции шейдера</span><span class="sxs-lookup"><span data-stu-id="3e34f-145">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="3e34f-146">**D3DXPreprocessShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="3e34f-146">**D3DXPreprocessShaderFromFile**</span></span>](d3dxpreprocessshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="3e34f-147">**D3DXPreprocessShader**</span><span class="sxs-lookup"><span data-stu-id="3e34f-147">**D3DXPreprocessShader**</span></span>](d3dxpreprocessshader.md)
</dt> </dl>

 

 
