---
title: Функция D3D11Reflect
description: Возвращает указатель на интерфейс отражения.
ms.assetid: 855097c7-988b-4ab6-90c5-e5dd0bc9e1e0
keywords:
- Функция D3D11Reflect HLSL
topic_type:
- apiref
api_name:
- D3D11Reflect
api_location:
- D3dcompiler_47.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e54a1f388ebb122398ad33c3a8d942496fa55393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157243"
---
# <a name="d3d11reflect-function"></a><span data-ttu-id="242de-104">Функция D3D11Reflect</span><span class="sxs-lookup"><span data-stu-id="242de-104">D3D11Reflect function</span></span>

<span data-ttu-id="242de-105">Возвращает указатель на интерфейс отражения.</span><span class="sxs-lookup"><span data-stu-id="242de-105">Gets a pointer to a reflection interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="242de-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="242de-106">Syntax</span></span>

``` syntax
HRESULT D3D11Reflect(
  in  LPCVOID pSrcData,
  in  SIZE_T SrcDataSize,
  out ID3D11ShaderReflection ppReflector
);
```

## <a name="parameters"></a><span data-ttu-id="242de-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="242de-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="242de-108">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="242de-108">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="242de-109">Тип: **[ **лпквоид**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="242de-109">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="242de-110">Указатель на исходные данные в виде скомпилированного кода HLSL.</span><span class="sxs-lookup"><span data-stu-id="242de-110">A pointer to source data as compiled HLSL code.</span></span>

</dd> <dt>

<span data-ttu-id="242de-111">*Сркдатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="242de-111">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="242de-112">Type: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="242de-112">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="242de-113">Длина *псркдата*.</span><span class="sxs-lookup"><span data-stu-id="242de-113">Length of *pSrcData*.</span></span>

</dd> <dt>

<span data-ttu-id="242de-114">*ппрефлектор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="242de-114">*ppReflector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="242de-115">Тип: **[ **ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***</span><span class="sxs-lookup"><span data-stu-id="242de-115">Type: **[**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***</span></span>

<span data-ttu-id="242de-116">Адрес указателя на интерфейс [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) .</span><span class="sxs-lookup"><span data-stu-id="242de-116">The address of a pointer to the [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="242de-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="242de-117">Return value</span></span>

<span data-ttu-id="242de-118">Тип: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="242de-118">Type: **[**HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="242de-119">Возвращает один из кодов возврата, описанных в разделе [коды возврата Direct3D 11](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues).</span><span class="sxs-lookup"><span data-stu-id="242de-119">Returns one of the return codes described in the topic [Direct3D 11 Return Codes](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues).</span></span>

## <a name="remarks"></a><span data-ttu-id="242de-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="242de-120">Remarks</span></span>

<span data-ttu-id="242de-121">Встроенная функция компилятора **D3D11Reflect** является оболочкой для функции компилятора [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) .</span><span class="sxs-lookup"><span data-stu-id="242de-121">The inline **D3D11Reflect** compiler function is a wrapper for the [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) compiler function.</span></span> <span data-ttu-id="242de-122">**D3D11Reflect** может получать интерфейс [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) только из шейдера.</span><span class="sxs-lookup"><span data-stu-id="242de-122">**D3D11Reflect** can retrieve only a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface from a shader.</span></span> <span data-ttu-id="242de-123">**D3DReflect** может получить интерфейс **ID3D11ShaderReflection** или интерфейс отражения direct3d 10 или Direct3D 10,1, например [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).</span><span class="sxs-lookup"><span data-stu-id="242de-123">**D3DReflect** can retrieve a **ID3D11ShaderReflection** interface or a Direct3D 10 or Direct3D 10.1 reflection interface, for example, [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).</span></span>

<span data-ttu-id="242de-124">Код шейдера содержит метаданные, которые можно проверить с помощью API-интерфейсов отражения.</span><span class="sxs-lookup"><span data-stu-id="242de-124">Shader code contains metadata that can be inspected using the reflection APIs.</span></span>

<span data-ttu-id="242de-125">В следующем коде показано, как получить интерфейс [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) из шейдера.</span><span class="sxs-lookup"><span data-stu-id="242de-125">The following code shows how to retrieve a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface from a shader.</span></span>


```C++
pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
                               pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader );

ID3D11ShaderReflection* pReflector = NULL; 
D3D11Reflect( pPixelShaderBuffer->GetBufferPointer(), pPixelShaderBuffer->GetBufferSize(), 
            &pReflector);
```



## <a name="requirements"></a><span data-ttu-id="242de-126">Требования</span><span class="sxs-lookup"><span data-stu-id="242de-126">Requirements</span></span>



| <span data-ttu-id="242de-127">Требование</span><span class="sxs-lookup"><span data-stu-id="242de-127">Requirement</span></span> | <span data-ttu-id="242de-128">Значение</span><span class="sxs-lookup"><span data-stu-id="242de-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="242de-129">Header</span><span class="sxs-lookup"><span data-stu-id="242de-129">Header</span></span><br/>  | <dl> <span data-ttu-id="242de-130"><dt>D3DCompiler. inl</dt></span><span class="sxs-lookup"><span data-stu-id="242de-130"><dt>D3DCompiler.inl</dt></span></span> </dl>     |
| <span data-ttu-id="242de-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="242de-131">Library</span></span><br/> | <dl> <span data-ttu-id="242de-132"><dt>D3dcompiler \_ 47. lib</dt></span><span class="sxs-lookup"><span data-stu-id="242de-132"><dt>D3dcompiler\_47.lib</dt></span></span> </dl> |
| <span data-ttu-id="242de-133">DLL</span><span class="sxs-lookup"><span data-stu-id="242de-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="242de-134"><dt>D3dcompiler \_47.dll</dt></span><span class="sxs-lookup"><span data-stu-id="242de-134"><dt>D3dcompiler\_47.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="242de-135">См. также</span><span class="sxs-lookup"><span data-stu-id="242de-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="242de-136">Функции</span><span class="sxs-lookup"><span data-stu-id="242de-136">Functions</span></span>](dx-graphics-d3dcompiler-reference-functions.md)
</dt> </dl>

 

