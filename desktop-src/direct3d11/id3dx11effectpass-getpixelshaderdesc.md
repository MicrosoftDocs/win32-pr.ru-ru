---
title: Метод ID3DX11EffectPass Жетпикселшадердеск (D3dx11effect. h)
description: Получите описание пиксельного шейдера.
ms.assetid: 5772f197-7ac5-4492-9a41-eedb1a8b22c9
keywords:
- Метод Жетпикселшадердеск Direct3D 11
- Метод Жетпикселшадердеск Direct3D 11, интерфейс ID3DX11EffectPass
- Интерфейс ID3DX11EffectPass Direct3D 11, метод Жетпикселшадердеск
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetPixelShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c04479a58eed0aa94616f0ffc092f17d52d9af4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986921"
---
# <a name="id3dx11effectpassgetpixelshaderdesc-method"></a><span data-ttu-id="220e1-106">Метод ID3DX11EffectPass:: Жетпикселшадердеск</span><span class="sxs-lookup"><span data-stu-id="220e1-106">ID3DX11EffectPass::GetPixelShaderDesc method</span></span>

<span data-ttu-id="220e1-107">Получите описание пиксельного шейдера.</span><span class="sxs-lookup"><span data-stu-id="220e1-107">Get a pixel-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="220e1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="220e1-108">Syntax</span></span>


```C++
HRESULT GetPixelShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="220e1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="220e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="220e1-110">*пдеск*</span><span class="sxs-lookup"><span data-stu-id="220e1-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="220e1-111">Тип: **[ **D3DX11 \_ Pass \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="220e1-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="220e1-112">Указатель на описание пиксельного шейдера (см. раздел [**D3DX11 \_ Pass \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="220e1-112">A pointer to a pixel-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="220e1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="220e1-113">Return value</span></span>

<span data-ttu-id="220e1-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="220e1-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="220e1-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="220e1-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="220e1-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="220e1-116">Remarks</span></span>

<span data-ttu-id="220e1-117">Передача результата может содержать назначения состояния визуализации и назначения объектов шейдера.</span><span class="sxs-lookup"><span data-stu-id="220e1-117">An effect pass can contain render state assignments and shader object assignments.</span></span>

> [!Note]  
> <span data-ttu-id="220e1-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="220e1-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="220e1-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="220e1-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="220e1-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="220e1-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="220e1-121">Требования</span><span class="sxs-lookup"><span data-stu-id="220e1-121">Requirements</span></span>



| <span data-ttu-id="220e1-122">Требование</span><span class="sxs-lookup"><span data-stu-id="220e1-122">Requirement</span></span> | <span data-ttu-id="220e1-123">Значение</span><span class="sxs-lookup"><span data-stu-id="220e1-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="220e1-124">Header</span><span class="sxs-lookup"><span data-stu-id="220e1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="220e1-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="220e1-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="220e1-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="220e1-126">Library</span></span><br/> | <dl> <span data-ttu-id="220e1-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="220e1-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="220e1-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="220e1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="220e1-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="220e1-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





