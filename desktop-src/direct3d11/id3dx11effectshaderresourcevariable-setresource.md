---
title: Метод ID3DX11EffectShaderResourceVariable Сетресаурце (D3dx11effect. h)
description: Задайте ресурс шейдера.
ms.assetid: f85c33ff-dc00-4421-939c-74f9317faadc
keywords:
- Метод Сетресаурце Direct3D 11
- Метод Сетресаурце Direct3D 11, интерфейс ID3DX11EffectShaderResourceVariable
- Интерфейс ID3DX11EffectShaderResourceVariable Direct3D 11, метод Сетресаурце
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.SetResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddec6c7daa2db552d6b5befee02bf57c6047dc5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356100"
---
# <a name="id3dx11effectshaderresourcevariablesetresource-method"></a><span data-ttu-id="4d50d-106">Метод ID3DX11EffectShaderResourceVariable:: Сетресаурце</span><span class="sxs-lookup"><span data-stu-id="4d50d-106">ID3DX11EffectShaderResourceVariable::SetResource method</span></span>

<span data-ttu-id="4d50d-107">Задайте ресурс шейдера.</span><span class="sxs-lookup"><span data-stu-id="4d50d-107">Set a shader resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d50d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d50d-108">Syntax</span></span>


```C++
HRESULT SetResource(
   ID3D11ShaderResourceView *pResource
);
```



## <a name="parameters"></a><span data-ttu-id="4d50d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d50d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d50d-110">*исходный код*</span><span class="sxs-lookup"><span data-stu-id="4d50d-110">*pResource*</span></span> 
</dt> <dd>

<span data-ttu-id="4d50d-111">Тип: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***</span><span class="sxs-lookup"><span data-stu-id="4d50d-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***</span></span>

<span data-ttu-id="4d50d-112">Адрес указателя на интерфейс представления шейдера-ресурса.</span><span class="sxs-lookup"><span data-stu-id="4d50d-112">The address of a pointer to a shader-resource-view interface.</span></span> <span data-ttu-id="4d50d-113">См. [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="4d50d-113">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d50d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4d50d-114">Return value</span></span>

<span data-ttu-id="4d50d-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4d50d-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4d50d-116">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4d50d-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4d50d-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="4d50d-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4d50d-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="4d50d-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4d50d-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="4d50d-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4d50d-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4d50d-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4d50d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4d50d-121">Requirements</span></span>



| <span data-ttu-id="4d50d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4d50d-122">Requirement</span></span> | <span data-ttu-id="4d50d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4d50d-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d50d-124">Header</span><span class="sxs-lookup"><span data-stu-id="4d50d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4d50d-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d50d-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4d50d-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4d50d-126">Library</span></span><br/> | <dl> <span data-ttu-id="4d50d-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="4d50d-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d50d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d50d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d50d-129">ID3DX11EffectShaderResourceVariable</span><span class="sxs-lookup"><span data-stu-id="4d50d-129">ID3DX11EffectShaderResourceVariable</span></span>](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

 





