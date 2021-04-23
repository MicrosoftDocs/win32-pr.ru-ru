---
title: Метод ID3DX11EffectBlendVariable Жетблендстате (D3dx11effect. h)
description: Получает указатель на интерфейс состояния смешения.
ms.assetid: ab4ee765-b5ad-4dc3-9b00-48052528d3bd
keywords:
- Метод Жетблендстате Direct3D 11
- Метод Жетблендстате Direct3D 11, интерфейс ID3DX11EffectBlendVariable
- Интерфейс ID3DX11EffectBlendVariable Direct3D 11, метод Жетблендстате
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.GetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48092b496fa8a38be7c9dd8aea67a26e8b56f4f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355523"
---
# <a name="id3dx11effectblendvariablegetblendstate-method"></a><span data-ttu-id="ad97c-106">Метод ID3DX11EffectBlendVariable:: Жетблендстате</span><span class="sxs-lookup"><span data-stu-id="ad97c-106">ID3DX11EffectBlendVariable::GetBlendState method</span></span>

<span data-ttu-id="ad97c-107">Получает указатель на интерфейс состояния смешения.</span><span class="sxs-lookup"><span data-stu-id="ad97c-107">Get a pointer to a blend-state interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad97c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad97c-108">Syntax</span></span>


```C++
HRESULT GetBlendState(
   UINT             Index,
   ID3D11BlendState **ppBlendState
);
```



## <a name="parameters"></a><span data-ttu-id="ad97c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad97c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad97c-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="ad97c-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="ad97c-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ad97c-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ad97c-112">Индекс в массиве интерфейсов состояния смешения.</span><span class="sxs-lookup"><span data-stu-id="ad97c-112">Index into an array of blend-state interfaces.</span></span> <span data-ttu-id="ad97c-113">Если имеется только один интерфейс состояния Blend, используйте значение 0.</span><span class="sxs-lookup"><span data-stu-id="ad97c-113">If there is only one blend-state interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="ad97c-114">*ппблендстате*</span><span class="sxs-lookup"><span data-stu-id="ad97c-114">*ppBlendState*</span></span> 
</dt> <dd>

<span data-ttu-id="ad97c-115">Тип: **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="ad97c-115">Type: **[**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\*\***</span></span>

<span data-ttu-id="ad97c-116">Адрес указателя на интерфейс состояния смешения (см. [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)).</span><span class="sxs-lookup"><span data-stu-id="ad97c-116">The address of a pointer to a blend-state interface (see [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad97c-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad97c-117">Return value</span></span>

<span data-ttu-id="ad97c-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ad97c-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ad97c-119">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ad97c-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ad97c-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="ad97c-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ad97c-121">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="ad97c-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ad97c-122">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="ad97c-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ad97c-123">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ad97c-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ad97c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="ad97c-124">Requirements</span></span>



| <span data-ttu-id="ad97c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="ad97c-125">Requirement</span></span> | <span data-ttu-id="ad97c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ad97c-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad97c-127">Header</span><span class="sxs-lookup"><span data-stu-id="ad97c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ad97c-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad97c-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ad97c-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ad97c-129">Library</span></span><br/> | <dl> <span data-ttu-id="ad97c-130"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="ad97c-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad97c-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad97c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad97c-132">ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="ad97c-132">ID3DX11EffectBlendVariable</span></span>](id3dx11effectblendvariable.md)
</dt> </dl>

 

