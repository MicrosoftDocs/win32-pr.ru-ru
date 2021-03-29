---
title: Метод ID3DX11EffectDepthStencilViewVariable ЖетдепсстенЦил (D3dx11effect. h)
description: Получите ресурс представления глубины-трафаретов.
ms.assetid: 7d94d98b-7070-41ee-9a9d-fe848f8914f2
keywords:
- Метод ЖетдепсстенЦил Direct3D 11
- Метод ЖетдепсстенЦил Direct3D 11, интерфейс ID3DX11EffectDepthStencilViewVariable
- Интерфейс ID3DX11EffectDepthStencilViewVariable Direct3D 11, метод ЖетдепсстенЦил
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.GetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49206f051922982ac77265e68fa3d7b7397d1348
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987122"
---
# <a name="id3dx11effectdepthstencilviewvariablegetdepthstencil-method"></a><span data-ttu-id="06e0f-106">Метод ID3DX11EffectDepthStencilViewVariable:: ЖетдепсстенЦил</span><span class="sxs-lookup"><span data-stu-id="06e0f-106">ID3DX11EffectDepthStencilViewVariable::GetDepthStencil method</span></span>

<span data-ttu-id="06e0f-107">Получите ресурс представления глубины-трафаретов.</span><span class="sxs-lookup"><span data-stu-id="06e0f-107">Get a depth-stencil-view resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="06e0f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06e0f-108">Syntax</span></span>


```C++
HRESULT GetDepthStencil(
   ID3D11DepthStencilView **ppResource
);
```



## <a name="parameters"></a><span data-ttu-id="06e0f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="06e0f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06e0f-110">*ппресаурце*</span><span class="sxs-lookup"><span data-stu-id="06e0f-110">*ppResource*</span></span> 
</dt> <dd>

<span data-ttu-id="06e0f-111">Тип: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span><span class="sxs-lookup"><span data-stu-id="06e0f-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span></span>

<span data-ttu-id="06e0f-112">Адрес указателя на интерфейс представления глубины-трафарета.</span><span class="sxs-lookup"><span data-stu-id="06e0f-112">The address of a pointer to a depth-stencil-view interface.</span></span> <span data-ttu-id="06e0f-113">См. [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="06e0f-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06e0f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06e0f-114">Return value</span></span>

<span data-ttu-id="06e0f-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="06e0f-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="06e0f-116">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="06e0f-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="06e0f-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="06e0f-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="06e0f-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="06e0f-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="06e0f-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="06e0f-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="06e0f-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="06e0f-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="06e0f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="06e0f-121">Requirements</span></span>



| <span data-ttu-id="06e0f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="06e0f-122">Requirement</span></span> | <span data-ttu-id="06e0f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="06e0f-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06e0f-124">Header</span><span class="sxs-lookup"><span data-stu-id="06e0f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="06e0f-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="06e0f-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="06e0f-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="06e0f-126">Library</span></span><br/> | <dl> <span data-ttu-id="06e0f-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="06e0f-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06e0f-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06e0f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06e0f-129">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="06e0f-129">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

 





