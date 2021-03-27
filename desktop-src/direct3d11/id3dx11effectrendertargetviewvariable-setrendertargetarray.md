---
title: Метод ID3DX11EffectRenderTargetViewVariable Сетрендертаржетаррай (D3dx11effect. h)
description: Задайте массив целевых объектов рендеринга.
ms.assetid: 03e1c4ea-292c-439f-a647-070b9e91a044
keywords:
- Метод Сетрендертаржетаррай Direct3D 11
- Метод Сетрендертаржетаррай Direct3D 11, интерфейс ID3DX11EffectRenderTargetViewVariable
- Интерфейс ID3DX11EffectRenderTargetViewVariable Direct3D 11, метод Сетрендертаржетаррай
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.SetRenderTargetArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6ff8a1931e95df4fd78d67a3a71d53150875400
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986840"
---
# <a name="id3dx11effectrendertargetviewvariablesetrendertargetarray-method"></a><span data-ttu-id="3e38d-106">Метод ID3DX11EffectRenderTargetViewVariable:: Сетрендертаржетаррай</span><span class="sxs-lookup"><span data-stu-id="3e38d-106">ID3DX11EffectRenderTargetViewVariable::SetRenderTargetArray method</span></span>

<span data-ttu-id="3e38d-107">Задайте массив целевых объектов рендеринга.</span><span class="sxs-lookup"><span data-stu-id="3e38d-107">Set an array of render-targets.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e38d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e38d-108">Syntax</span></span>


```C++
HRESULT SetRenderTargetArray(
   ID3D11RenderTargetView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a><span data-ttu-id="3e38d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e38d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e38d-110">*ппресаурцес*</span><span class="sxs-lookup"><span data-stu-id="3e38d-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="3e38d-111">Тип: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span><span class="sxs-lookup"><span data-stu-id="3e38d-111">Type: **[**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span></span>

<span data-ttu-id="3e38d-112">Задайте массив интерфейсов представления визуализации-целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="3e38d-112">Set an array of render-target-view interfaces.</span></span> <span data-ttu-id="3e38d-113">См. [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span><span class="sxs-lookup"><span data-stu-id="3e38d-113">See [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span></span>

</dd> <dt>

<span data-ttu-id="3e38d-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="3e38d-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="3e38d-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3e38d-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3e38d-116">Отсчитываемый от нуля индекс массива для хранения первого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3e38d-116">The zero-based array index to store the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="3e38d-117">*Количество*</span><span class="sxs-lookup"><span data-stu-id="3e38d-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="3e38d-118">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3e38d-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3e38d-119">Количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="3e38d-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e38d-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e38d-120">Return value</span></span>

<span data-ttu-id="3e38d-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3e38d-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3e38d-122">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3e38d-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3e38d-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="3e38d-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3e38d-124">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="3e38d-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3e38d-125">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="3e38d-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3e38d-126">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3e38d-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3e38d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="3e38d-127">Requirements</span></span>



| <span data-ttu-id="3e38d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="3e38d-128">Requirement</span></span> | <span data-ttu-id="3e38d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="3e38d-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e38d-130">Header</span><span class="sxs-lookup"><span data-stu-id="3e38d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="3e38d-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e38d-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3e38d-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3e38d-132">Library</span></span><br/> | <dl> <span data-ttu-id="3e38d-133"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="3e38d-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e38d-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e38d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e38d-135">ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="3e38d-135">ID3DX11EffectRenderTargetViewVariable</span></span>](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

