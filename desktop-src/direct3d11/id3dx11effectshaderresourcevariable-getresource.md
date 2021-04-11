---
title: Метод ID3DX11EffectShaderResourceVariable-Resource (D3dx11effect. h)
description: Получение ресурса шейдера.
ms.assetid: 7c56aba0-ce60-4b50-9c1a-802bf1d73c6b
keywords:
- Метод WebMethod Direct3D 11
- Метод ID3DX11EffectShaderResourceVariable Direct3D 11, интерфейс
- Интерфейс ID3DX11EffectShaderResourceVariable Direct3D 11, метод.
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.GetResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea841ae63646958603396d5b65305c242961942
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273709"
---
# <a name="id3dx11effectshaderresourcevariablegetresource-method"></a><span data-ttu-id="f914a-106">Метод ID3DX11EffectShaderResourceVariable::</span><span class="sxs-lookup"><span data-stu-id="f914a-106">ID3DX11EffectShaderResourceVariable::GetResource method</span></span>

<span data-ttu-id="f914a-107">Получение ресурса шейдера.</span><span class="sxs-lookup"><span data-stu-id="f914a-107">Get a shader resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="f914a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f914a-108">Syntax</span></span>


```C++
HRESULT GetResource(
   ID3D11ShaderResourceView **ppResource
);
```



## <a name="parameters"></a><span data-ttu-id="f914a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f914a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f914a-110">*ппресаурце*</span><span class="sxs-lookup"><span data-stu-id="f914a-110">*ppResource*</span></span> 
</dt> <dd>

<span data-ttu-id="f914a-111">Тип: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="f914a-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="f914a-112">Адрес указателя на интерфейс представления шейдера-ресурса.</span><span class="sxs-lookup"><span data-stu-id="f914a-112">The address of a pointer to a shader-resource-view interface.</span></span> <span data-ttu-id="f914a-113">См. [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="f914a-113">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f914a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f914a-114">Return value</span></span>

<span data-ttu-id="f914a-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f914a-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f914a-116">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f914a-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f914a-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="f914a-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f914a-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="f914a-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f914a-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="f914a-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f914a-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f914a-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f914a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f914a-121">Requirements</span></span>



| <span data-ttu-id="f914a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f914a-122">Requirement</span></span> | <span data-ttu-id="f914a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f914a-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f914a-124">Header</span><span class="sxs-lookup"><span data-stu-id="f914a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f914a-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f914a-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f914a-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f914a-126">Library</span></span><br/> | <dl> <span data-ttu-id="f914a-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="f914a-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f914a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f914a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f914a-129">ID3DX11EffectShaderResourceVariable</span><span class="sxs-lookup"><span data-stu-id="f914a-129">ID3DX11EffectShaderResourceVariable</span></span>](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

 





