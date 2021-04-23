---
title: Метод ID3DX11EffectShaderResourceVariable Жетресаурцеаррай (D3dx11effect. h)
description: Получение массива ресурсов шейдера.
ms.assetid: 7540183d-dabb-46c2-8df1-6d4734b77f25
keywords:
- Метод Жетресаурцеаррай Direct3D 11
- Метод Жетресаурцеаррай Direct3D 11, интерфейс ID3DX11EffectShaderResourceVariable
- Интерфейс ID3DX11EffectShaderResourceVariable Direct3D 11, метод Жетресаурцеаррай
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.GetResourceArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0091d81b7e157aecb8315e1def380800c8155c60
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000532"
---
# <a name="id3dx11effectshaderresourcevariablegetresourcearray-method"></a><span data-ttu-id="a2fc8-106">Метод ID3DX11EffectShaderResourceVariable:: Жетресаурцеаррай</span><span class="sxs-lookup"><span data-stu-id="a2fc8-106">ID3DX11EffectShaderResourceVariable::GetResourceArray method</span></span>

<span data-ttu-id="a2fc8-107">Получение массива ресурсов шейдера.</span><span class="sxs-lookup"><span data-stu-id="a2fc8-107">Get an array of shader resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2fc8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2fc8-108">Syntax</span></span>


```C++
HRESULT GetResourceArray(
   ID3D11ShaderResourceView **ppResources,
   UINT                     Offset,
   UINT                     Count
);
```



## <a name="parameters"></a><span data-ttu-id="a2fc8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2fc8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2fc8-110">*ппресаурцес*</span><span class="sxs-lookup"><span data-stu-id="a2fc8-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="a2fc8-111">Тип: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="a2fc8-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="a2fc8-112">Адрес массива интерфейсов шейдера-представления ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2fc8-112">The address of an array of shader-resource-view interfaces.</span></span> <span data-ttu-id="a2fc8-113">См. [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="a2fc8-113">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="a2fc8-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="a2fc8-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="a2fc8-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a2fc8-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a2fc8-116">Индекс массива, начинающийся с нуля, для получения первого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a2fc8-116">The zero-based array index to get the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="a2fc8-117">*Количество*</span><span class="sxs-lookup"><span data-stu-id="a2fc8-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="a2fc8-118">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a2fc8-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a2fc8-119">Количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="a2fc8-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2fc8-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2fc8-120">Return value</span></span>

<span data-ttu-id="a2fc8-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a2fc8-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a2fc8-122">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a2fc8-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a2fc8-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="a2fc8-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a2fc8-124">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="a2fc8-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a2fc8-125">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="a2fc8-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a2fc8-126">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a2fc8-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a2fc8-127">Требования</span><span class="sxs-lookup"><span data-stu-id="a2fc8-127">Requirements</span></span>



| <span data-ttu-id="a2fc8-128">Требование</span><span class="sxs-lookup"><span data-stu-id="a2fc8-128">Requirement</span></span> | <span data-ttu-id="a2fc8-129">Значение</span><span class="sxs-lookup"><span data-stu-id="a2fc8-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2fc8-130">Header</span><span class="sxs-lookup"><span data-stu-id="a2fc8-130">Header</span></span><br/>  | <dl> <span data-ttu-id="a2fc8-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2fc8-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a2fc8-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a2fc8-132">Library</span></span><br/> | <dl> <span data-ttu-id="a2fc8-133"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="a2fc8-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2fc8-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2fc8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2fc8-135">ID3DX11EffectShaderResourceVariable</span><span class="sxs-lookup"><span data-stu-id="a2fc8-135">ID3DX11EffectShaderResourceVariable</span></span>](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

