---
title: Метод ID3DX11EffectDepthStencilVariable ЖетдепсстенЦилстате (D3dx11effect. h)
description: Получение указателя на интерфейс трафарета глубины.
ms.assetid: 3e8f7fc6-960c-45f5-9276-9aa2a5e7a6c9
keywords:
- Метод ЖетдепсстенЦилстате Direct3D 11
- Метод ЖетдепсстенЦилстате Direct3D 11, интерфейс ID3DX11EffectDepthStencilVariable
- Интерфейс ID3DX11EffectDepthStencilVariable Direct3D 11, метод ЖетдепсстенЦилстате
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.GetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9276c7a126d5441361a4d449c4ee2ece70d995
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987131"
---
# <a name="id3dx11effectdepthstencilvariablegetdepthstencilstate-method"></a><span data-ttu-id="9fcfe-106">Метод ID3DX11EffectDepthStencilVariable:: ЖетдепсстенЦилстате</span><span class="sxs-lookup"><span data-stu-id="9fcfe-106">ID3DX11EffectDepthStencilVariable::GetDepthStencilState method</span></span>

<span data-ttu-id="9fcfe-107">Получение указателя на интерфейс трафарета глубины.</span><span class="sxs-lookup"><span data-stu-id="9fcfe-107">Get a pointer to a depth-stencil interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fcfe-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9fcfe-108">Syntax</span></span>


```C++
HRESULT GetDepthStencilState(
   UINT                    Index,
   ID3D11DepthStencilState **ppDepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="9fcfe-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9fcfe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fcfe-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="9fcfe-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="9fcfe-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9fcfe-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9fcfe-112">Индекс в массиве интерфейсов трафарета глубины.</span><span class="sxs-lookup"><span data-stu-id="9fcfe-112">Index into an array of depth-stencil interfaces.</span></span> <span data-ttu-id="9fcfe-113">Если имеется только один интерфейс трафарета глубины, используйте значение 0.</span><span class="sxs-lookup"><span data-stu-id="9fcfe-113">If there is only one depth-stencil interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="9fcfe-114">*ппдепсстенЦилстате*</span><span class="sxs-lookup"><span data-stu-id="9fcfe-114">*ppDepthStencilState*</span></span> 
</dt> <dd>

<span data-ttu-id="9fcfe-115">Тип: **[ **ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="9fcfe-115">Type: **[**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\*\***</span></span>

<span data-ttu-id="9fcfe-116">Адрес указателя на интерфейс состояния смешения (см. [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)).</span><span class="sxs-lookup"><span data-stu-id="9fcfe-116">The address of a pointer to a blend-state interface (see [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fcfe-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9fcfe-117">Return value</span></span>

<span data-ttu-id="9fcfe-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9fcfe-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9fcfe-119">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9fcfe-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9fcfe-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="9fcfe-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9fcfe-121">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="9fcfe-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9fcfe-122">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="9fcfe-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9fcfe-123">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9fcfe-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9fcfe-124">Требования</span><span class="sxs-lookup"><span data-stu-id="9fcfe-124">Requirements</span></span>



| <span data-ttu-id="9fcfe-125">Требование</span><span class="sxs-lookup"><span data-stu-id="9fcfe-125">Requirement</span></span> | <span data-ttu-id="9fcfe-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9fcfe-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fcfe-127">Header</span><span class="sxs-lookup"><span data-stu-id="9fcfe-127">Header</span></span><br/>  | <dl> <span data-ttu-id="9fcfe-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fcfe-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9fcfe-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9fcfe-129">Library</span></span><br/> | <dl> <span data-ttu-id="9fcfe-130"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="9fcfe-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fcfe-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9fcfe-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fcfe-132">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="9fcfe-132">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

