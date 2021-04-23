---
title: Метод ID3DX11EffectVariable АсдепсстенЦилвиев (D3dx11effect. h)
description: Получите переменную представления с глубиной набора элементов.
ms.assetid: 491ca6e1-a74c-4996-a25c-ea40910f0f36
keywords:
- Метод АсдепсстенЦилвиев Direct3D 11
- Метод АсдепсстенЦилвиев Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод АсдепсстенЦилвиев
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsDepthStencilView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 432ba5018f1e233e7fb1b4ad4efae1d4f27cb141
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273744"
---
# <a name="id3dx11effectvariableasdepthstencilview-method"></a><span data-ttu-id="b755d-106">Метод ID3DX11EffectVariable:: АсдепсстенЦилвиев</span><span class="sxs-lookup"><span data-stu-id="b755d-106">ID3DX11EffectVariable::AsDepthStencilView method</span></span>

<span data-ttu-id="b755d-107">Получите переменную представления с глубиной набора элементов.</span><span class="sxs-lookup"><span data-stu-id="b755d-107">Get a depth-stencil-view variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b755d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b755d-108">Syntax</span></span>


```C++
ID3DX11EffectDepthStencilViewVariable* AsDepthStencilView();
```



## <a name="parameters"></a><span data-ttu-id="b755d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b755d-109">Parameters</span></span>

<span data-ttu-id="b755d-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b755d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b755d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b755d-111">Return value</span></span>

<span data-ttu-id="b755d-112">Тип: **[ **ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="b755d-112">Type: **[**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)\***</span></span>

<span data-ttu-id="b755d-113">Указатель на переменную представления с набором элементов depth.</span><span class="sxs-lookup"><span data-stu-id="b755d-113">A pointer to a depth-stencil-view variable.</span></span> <span data-ttu-id="b755d-114">См. [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md).</span><span class="sxs-lookup"><span data-stu-id="b755d-114">See [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b755d-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="b755d-115">Remarks</span></span>

<span data-ttu-id="b755d-116">Этот метод возвращает версию переменной Effect, которая была специализированной для переменной представления глубины-трафарет-View.</span><span class="sxs-lookup"><span data-stu-id="b755d-116">This method returns a version of the effect variable that has been specialized to a depth-stencil-view variable.</span></span> <span data-ttu-id="b755d-117">Как и в приведении, эта специализация вернет недопустимый объект, если переменная действия не содержит данных представления глубины-трафарета.</span><span class="sxs-lookup"><span data-stu-id="b755d-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain depth-stencil-view data.</span></span>

<span data-ttu-id="b755d-118">Приложения могут проверить возвращаемый объект на допустимость, вызвав [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="b755d-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="b755d-119">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="b755d-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b755d-120">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="b755d-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b755d-121">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b755d-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b755d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b755d-122">Requirements</span></span>



| <span data-ttu-id="b755d-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b755d-123">Requirement</span></span> | <span data-ttu-id="b755d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b755d-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b755d-125">Header</span><span class="sxs-lookup"><span data-stu-id="b755d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b755d-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b755d-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b755d-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b755d-127">Library</span></span><br/> | <dl> <span data-ttu-id="b755d-128"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="b755d-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b755d-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b755d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b755d-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="b755d-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





