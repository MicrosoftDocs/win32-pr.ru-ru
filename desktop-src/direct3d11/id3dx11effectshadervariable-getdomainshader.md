---
title: Метод ID3DX11EffectShaderVariable Жетдомаиншадер (D3dx11effect. h)
description: Получите шейдер домена.
ms.assetid: fd95a4f0-7df3-4098-843f-0a1e22209603
keywords:
- Метод Жетдомаиншадер Direct3D 11
- Метод Жетдомаиншадер Direct3D 11, интерфейс ID3DX11EffectShaderVariable
- Интерфейс ID3DX11EffectShaderVariable Direct3D 11, метод Жетдомаиншадер
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetDomainShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b7f097fb950b60aaa9c7fa2d5b763b393d5e275
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273983"
---
# <a name="id3dx11effectshadervariablegetdomainshader-method"></a><span data-ttu-id="92cdd-106">Метод ID3DX11EffectShaderVariable:: Жетдомаиншадер</span><span class="sxs-lookup"><span data-stu-id="92cdd-106">ID3DX11EffectShaderVariable::GetDomainShader method</span></span>

<span data-ttu-id="92cdd-107">Получите шейдер домена.</span><span class="sxs-lookup"><span data-stu-id="92cdd-107">Get a domain shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="92cdd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92cdd-108">Syntax</span></span>


```C++
HRESULT GetDomainShader(
   UINT               ShaderIndex,
   ID3D11DomainShader **ppPS
);
```



## <a name="parameters"></a><span data-ttu-id="92cdd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="92cdd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92cdd-110">*шадериндекс*</span><span class="sxs-lookup"><span data-stu-id="92cdd-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="92cdd-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="92cdd-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="92cdd-112">Индекс шейдера домена.</span><span class="sxs-lookup"><span data-stu-id="92cdd-112">Index of the domain shader.</span></span>

</dd> <dt>

<span data-ttu-id="92cdd-113">*пппс*</span><span class="sxs-lookup"><span data-stu-id="92cdd-113">*ppPS*</span></span> 
</dt> <dd>

<span data-ttu-id="92cdd-114">Тип: **[ **ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="92cdd-114">Type: **[**ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader)\*\***</span></span>

<span data-ttu-id="92cdd-115">Указатель на указатель [**ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader) , для которого будет задан шейдер домена при возврате.</span><span class="sxs-lookup"><span data-stu-id="92cdd-115">Pointer to an [**ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader) pointer that will be set to the domain shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92cdd-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92cdd-116">Return value</span></span>

<span data-ttu-id="92cdd-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="92cdd-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="92cdd-118">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="92cdd-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="92cdd-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="92cdd-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="92cdd-120">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="92cdd-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="92cdd-121">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="92cdd-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="92cdd-122">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="92cdd-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="92cdd-123">Требования</span><span class="sxs-lookup"><span data-stu-id="92cdd-123">Requirements</span></span>



| <span data-ttu-id="92cdd-124">Требование</span><span class="sxs-lookup"><span data-stu-id="92cdd-124">Requirement</span></span> | <span data-ttu-id="92cdd-125">Значение</span><span class="sxs-lookup"><span data-stu-id="92cdd-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92cdd-126">Header</span><span class="sxs-lookup"><span data-stu-id="92cdd-126">Header</span></span><br/>  | <dl> <span data-ttu-id="92cdd-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="92cdd-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="92cdd-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="92cdd-128">Library</span></span><br/> | <dl> <span data-ttu-id="92cdd-129"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="92cdd-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92cdd-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92cdd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92cdd-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="92cdd-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

