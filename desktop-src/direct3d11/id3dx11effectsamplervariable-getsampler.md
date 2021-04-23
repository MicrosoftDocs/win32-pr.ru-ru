---
title: Метод ID3DX11EffectSamplerVariable-Sample (D3dx11effect. h)
description: Получение указателя на интерфейс образца.
ms.assetid: ac2a05f1-e3ca-4ebf-b655-34133c4e50ac
keywords:
- Метод "выборке" Direct3D 11
- Метод ID3DX11EffectSamplerVariable Direct3D 11, интерфейс для примера
- Интерфейс ID3DX11EffectSamplerVariable Direct3D 11, метод «выборке»
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.GetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53260a07e544d5f69a9575851614f694b778619
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000506"
---
# <a name="id3dx11effectsamplervariablegetsampler-method"></a><span data-ttu-id="12fd5-106">Метод ID3DX11EffectSamplerVariable:: Sample</span><span class="sxs-lookup"><span data-stu-id="12fd5-106">ID3DX11EffectSamplerVariable::GetSampler method</span></span>

<span data-ttu-id="12fd5-107">Получение указателя на интерфейс образца.</span><span class="sxs-lookup"><span data-stu-id="12fd5-107">Get a pointer to a sampler interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="12fd5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12fd5-108">Syntax</span></span>


```C++
HRESULT GetSampler(
   UINT               Index,
   ID3D11SamplerState **ppSampler
);
```



## <a name="parameters"></a><span data-ttu-id="12fd5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="12fd5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12fd5-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="12fd5-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="12fd5-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="12fd5-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="12fd5-112">Индекс в массиве интерфейсов образцов.</span><span class="sxs-lookup"><span data-stu-id="12fd5-112">Index into an array of sampler interfaces.</span></span> <span data-ttu-id="12fd5-113">Если имеется только один интерфейс выборки, используйте значение 0.</span><span class="sxs-lookup"><span data-stu-id="12fd5-113">If there is only one sampler interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="12fd5-114">*ппсамплер*</span><span class="sxs-lookup"><span data-stu-id="12fd5-114">*ppSampler*</span></span> 
</dt> <dd>

<span data-ttu-id="12fd5-115">Тип: **[ **ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="12fd5-115">Type: **[**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\*\***</span></span>

<span data-ttu-id="12fd5-116">Адрес указателя на интерфейс образца (см. [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)).</span><span class="sxs-lookup"><span data-stu-id="12fd5-116">The address of a pointer to a sampler interface (see [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12fd5-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12fd5-117">Return value</span></span>

<span data-ttu-id="12fd5-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="12fd5-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="12fd5-119">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="12fd5-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="12fd5-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="12fd5-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="12fd5-121">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="12fd5-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="12fd5-122">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="12fd5-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="12fd5-123">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="12fd5-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="12fd5-124">Требования</span><span class="sxs-lookup"><span data-stu-id="12fd5-124">Requirements</span></span>



| <span data-ttu-id="12fd5-125">Требование</span><span class="sxs-lookup"><span data-stu-id="12fd5-125">Requirement</span></span> | <span data-ttu-id="12fd5-126">Значение</span><span class="sxs-lookup"><span data-stu-id="12fd5-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12fd5-127">Header</span><span class="sxs-lookup"><span data-stu-id="12fd5-127">Header</span></span><br/>  | <dl> <span data-ttu-id="12fd5-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="12fd5-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="12fd5-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="12fd5-129">Library</span></span><br/> | <dl> <span data-ttu-id="12fd5-130"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="12fd5-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12fd5-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12fd5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12fd5-132">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="12fd5-132">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 

