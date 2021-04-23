---
title: Метод ID3DX11EffectDepthStencilVariable СетдепсстенЦилстате (D3dx11effect. h)
description: Задает состояние шаблона глубины.
ms.assetid: 4ece246f-4466-4790-8f38-450b67fff7c6
keywords:
- Метод СетдепсстенЦилстате Direct3D 11
- Метод СетдепсстенЦилстате Direct3D 11, интерфейс ID3DX11EffectDepthStencilVariable
- Интерфейс ID3DX11EffectDepthStencilVariable Direct3D 11, метод СетдепсстенЦилстате
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.SetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b82fac869cb15bced76fdc1335967c6f7d017f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987128"
---
# <a name="id3dx11effectdepthstencilvariablesetdepthstencilstate-method"></a><span data-ttu-id="9a9c1-106">Метод ID3DX11EffectDepthStencilVariable:: СетдепсстенЦилстате</span><span class="sxs-lookup"><span data-stu-id="9a9c1-106">ID3DX11EffectDepthStencilVariable::SetDepthStencilState method</span></span>

<span data-ttu-id="9a9c1-107">Задает состояние шаблона глубины.</span><span class="sxs-lookup"><span data-stu-id="9a9c1-107">Sets the depth stencil state.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a9c1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a9c1-108">Syntax</span></span>


```C++
HRESULT SetDepthStencilState(
   UINT                    Index,
   ID3D11DepthStencilState *pDepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="9a9c1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a9c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a9c1-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="9a9c1-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="9a9c1-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9a9c1-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9a9c1-112">Индекс в массиве интерфейсов трафарета глубины.</span><span class="sxs-lookup"><span data-stu-id="9a9c1-112">Index into an array of depth-stencil interfaces.</span></span> <span data-ttu-id="9a9c1-113">Если имеется только один интерфейс трафарета глубины, используйте значение 0.</span><span class="sxs-lookup"><span data-stu-id="9a9c1-113">If there is only one depth-stencil interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="9a9c1-114">*пдепсстенЦилстате*</span><span class="sxs-lookup"><span data-stu-id="9a9c1-114">*pDepthStencilState*</span></span> 
</dt> <dd>

<span data-ttu-id="9a9c1-115">Тип: **[ **ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\***</span><span class="sxs-lookup"><span data-stu-id="9a9c1-115">Type: **[**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\***</span></span>

<span data-ttu-id="9a9c1-116">Указатель на интерфейс [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate) , содержащий новое состояние трафарета глубины.</span><span class="sxs-lookup"><span data-stu-id="9a9c1-116">Pointer to an [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate) interface containing the new depth stencil state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a9c1-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a9c1-117">Return value</span></span>

<span data-ttu-id="9a9c1-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9a9c1-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9a9c1-119">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9a9c1-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9a9c1-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="9a9c1-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9a9c1-121">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="9a9c1-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9a9c1-122">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="9a9c1-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9a9c1-123">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9a9c1-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9a9c1-124">Требования</span><span class="sxs-lookup"><span data-stu-id="9a9c1-124">Requirements</span></span>



| <span data-ttu-id="9a9c1-125">Требование</span><span class="sxs-lookup"><span data-stu-id="9a9c1-125">Requirement</span></span> | <span data-ttu-id="9a9c1-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9a9c1-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a9c1-127">Header</span><span class="sxs-lookup"><span data-stu-id="9a9c1-127">Header</span></span><br/>  | <dl> <span data-ttu-id="9a9c1-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a9c1-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9a9c1-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9a9c1-129">Library</span></span><br/> | <dl> <span data-ttu-id="9a9c1-130"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="9a9c1-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a9c1-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a9c1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a9c1-132">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="9a9c1-132">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

