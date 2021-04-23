---
title: Метод ID3DX11EffectPass Жеткомпутешадердеск (D3dx11effect. h)
description: Получение описания вычислений для шейдера.
ms.assetid: 9c3a702f-2016-4b1a-a832-d1bb968aec2d
keywords:
- Метод Жеткомпутешадердеск Direct3D 11
- Метод Жеткомпутешадердеск Direct3D 11, интерфейс ID3DX11EffectPass
- Интерфейс ID3DX11EffectPass Direct3D 11, метод Жеткомпутешадердеск
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetComputeShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21cc13699553b0da60498209ddffd31a56607809
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000473"
---
# <a name="id3dx11effectpassgetcomputeshaderdesc-method"></a><span data-ttu-id="6b45a-106">Метод ID3DX11EffectPass:: Жеткомпутешадердеск</span><span class="sxs-lookup"><span data-stu-id="6b45a-106">ID3DX11EffectPass::GetComputeShaderDesc method</span></span>

<span data-ttu-id="6b45a-107">Получение описания вычислений для шейдера.</span><span class="sxs-lookup"><span data-stu-id="6b45a-107">Get a compute-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b45a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b45a-108">Syntax</span></span>


```C++
HRESULT GetComputeShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="6b45a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b45a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b45a-110">*пдеск*</span><span class="sxs-lookup"><span data-stu-id="6b45a-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="6b45a-111">Тип: **[ **D3DX11 \_ Pass \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="6b45a-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="6b45a-112">Указатель на описание для вычислений с шейдером (см. раздел [**D3DX11 \_ Pass \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="6b45a-112">A pointer to a compute-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b45a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b45a-113">Return value</span></span>

<span data-ttu-id="6b45a-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6b45a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6b45a-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6b45a-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6b45a-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="6b45a-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6b45a-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="6b45a-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6b45a-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="6b45a-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6b45a-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6b45a-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6b45a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="6b45a-120">Requirements</span></span>



| <span data-ttu-id="6b45a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="6b45a-121">Requirement</span></span> | <span data-ttu-id="6b45a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6b45a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b45a-123">Header</span><span class="sxs-lookup"><span data-stu-id="6b45a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6b45a-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b45a-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6b45a-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6b45a-125">Library</span></span><br/> | <dl> <span data-ttu-id="6b45a-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="6b45a-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b45a-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b45a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b45a-128">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="6b45a-128">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





