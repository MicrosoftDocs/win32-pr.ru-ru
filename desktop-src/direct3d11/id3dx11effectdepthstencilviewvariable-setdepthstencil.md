---
title: Метод ID3DX11EffectDepthStencilViewVariable СетдепсстенЦил (D3dx11effect. h)
description: Задайте ресурс представления глубины-набор.
ms.assetid: 35cbcd3b-6fc8-448d-a82e-724f91038d07
keywords:
- Метод СетдепсстенЦил Direct3D 11
- Метод СетдепсстенЦил Direct3D 11, интерфейс ID3DX11EffectDepthStencilViewVariable
- Интерфейс ID3DX11EffectDepthStencilViewVariable Direct3D 11, метод СетдепсстенЦил
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.SetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 723be51bc769982acf43c19482978bd581cafa13
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998477"
---
# <a name="id3dx11effectdepthstencilviewvariablesetdepthstencil-method"></a><span data-ttu-id="3adbb-106">Метод ID3DX11EffectDepthStencilViewVariable:: СетдепсстенЦил</span><span class="sxs-lookup"><span data-stu-id="3adbb-106">ID3DX11EffectDepthStencilViewVariable::SetDepthStencil method</span></span>

<span data-ttu-id="3adbb-107">Задайте ресурс представления глубины-набор.</span><span class="sxs-lookup"><span data-stu-id="3adbb-107">Set a depth-stencil-view resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="3adbb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3adbb-108">Syntax</span></span>


```C++
HRESULT SetDepthStencil(
   ID3D11DepthStencilView *pResource
);
```



## <a name="parameters"></a><span data-ttu-id="3adbb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3adbb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3adbb-110">*исходный код*</span><span class="sxs-lookup"><span data-stu-id="3adbb-110">*pResource*</span></span> 
</dt> <dd>

<span data-ttu-id="3adbb-111">Тип: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\***</span><span class="sxs-lookup"><span data-stu-id="3adbb-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\***</span></span>

<span data-ttu-id="3adbb-112">Указатель на интерфейс представления глубины-трафарета.</span><span class="sxs-lookup"><span data-stu-id="3adbb-112">A pointer to a depth-stencil-view interface.</span></span> <span data-ttu-id="3adbb-113">См. [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="3adbb-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3adbb-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3adbb-114">Return value</span></span>

<span data-ttu-id="3adbb-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3adbb-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3adbb-116">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3adbb-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3adbb-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="3adbb-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3adbb-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="3adbb-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3adbb-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="3adbb-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3adbb-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3adbb-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3adbb-121">Требования</span><span class="sxs-lookup"><span data-stu-id="3adbb-121">Requirements</span></span>



| <span data-ttu-id="3adbb-122">Требование</span><span class="sxs-lookup"><span data-stu-id="3adbb-122">Requirement</span></span> | <span data-ttu-id="3adbb-123">Значение</span><span class="sxs-lookup"><span data-stu-id="3adbb-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3adbb-124">Header</span><span class="sxs-lookup"><span data-stu-id="3adbb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3adbb-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3adbb-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3adbb-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3adbb-126">Library</span></span><br/> | <dl> <span data-ttu-id="3adbb-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="3adbb-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3adbb-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3adbb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3adbb-129">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="3adbb-129">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

 





