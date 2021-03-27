---
title: Метод ID3DX11EffectRenderTargetViewVariable Сетрендертаржет (D3dx11effect. h)
description: Задайте целевой объект рендеринга.
ms.assetid: caac7190-4f58-4a8e-9764-b6120ac14856
keywords:
- Метод Сетрендертаржет Direct3D 11
- Метод Сетрендертаржет Direct3D 11, интерфейс ID3DX11EffectRenderTargetViewVariable
- Интерфейс ID3DX11EffectRenderTargetViewVariable Direct3D 11, метод Сетрендертаржет
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.SetRenderTarget
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb53f0dff19fcd8990575dc9b305b0fb2f7e149b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914827"
---
# <a name="id3dx11effectrendertargetviewvariablesetrendertarget-method"></a><span data-ttu-id="b4ac8-106">Метод ID3DX11EffectRenderTargetViewVariable:: Сетрендертаржет</span><span class="sxs-lookup"><span data-stu-id="b4ac8-106">ID3DX11EffectRenderTargetViewVariable::SetRenderTarget method</span></span>

<span data-ttu-id="b4ac8-107">Задайте целевой объект рендеринга.</span><span class="sxs-lookup"><span data-stu-id="b4ac8-107">Set a render-target.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4ac8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4ac8-108">Syntax</span></span>


```C++
HRESULT SetRenderTarget(
   ID3D11RenderTargetView *pResource
);
```



## <a name="parameters"></a><span data-ttu-id="b4ac8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4ac8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4ac8-110">*исходный код*</span><span class="sxs-lookup"><span data-stu-id="b4ac8-110">*pResource*</span></span> 
</dt> <dd>

<span data-ttu-id="b4ac8-111">Тип: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\***</span><span class="sxs-lookup"><span data-stu-id="b4ac8-111">Type: **[**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\***</span></span>

<span data-ttu-id="b4ac8-112">Указатель на интерфейс представления, предназначенный для визуализации.</span><span class="sxs-lookup"><span data-stu-id="b4ac8-112">A pointer to a render-target-view interface.</span></span> <span data-ttu-id="b4ac8-113">См. [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span><span class="sxs-lookup"><span data-stu-id="b4ac8-113">See [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4ac8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4ac8-114">Return value</span></span>

<span data-ttu-id="b4ac8-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b4ac8-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b4ac8-116">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b4ac8-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b4ac8-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="b4ac8-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b4ac8-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="b4ac8-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b4ac8-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="b4ac8-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b4ac8-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b4ac8-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b4ac8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b4ac8-121">Requirements</span></span>



| <span data-ttu-id="b4ac8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b4ac8-122">Requirement</span></span> | <span data-ttu-id="b4ac8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b4ac8-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4ac8-124">Header</span><span class="sxs-lookup"><span data-stu-id="b4ac8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b4ac8-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4ac8-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b4ac8-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b4ac8-126">Library</span></span><br/> | <dl> <span data-ttu-id="b4ac8-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="b4ac8-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4ac8-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4ac8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4ac8-129">ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="b4ac8-129">ID3DX11EffectRenderTargetViewVariable</span></span>](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

 





