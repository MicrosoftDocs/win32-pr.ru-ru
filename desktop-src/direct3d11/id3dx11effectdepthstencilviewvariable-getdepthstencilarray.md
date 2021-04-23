---
title: Метод ID3DX11EffectDepthStencilViewVariable ЖетдепсстенЦиларрай (D3dx11effect. h)
description: Получите массив ресурсов представления глубины набора элементов.
ms.assetid: 92b2d9b1-6cf8-4523-88e0-bcd09b95477c
keywords:
- Метод ЖетдепсстенЦиларрай Direct3D 11
- Метод ЖетдепсстенЦиларрай Direct3D 11, интерфейс ID3DX11EffectDepthStencilViewVariable
- Интерфейс ID3DX11EffectDepthStencilViewVariable Direct3D 11, метод ЖетдепсстенЦиларрай
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.GetDepthStencilArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b7b886049413be542108257a47a3b1e3899910
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987119"
---
# <a name="id3dx11effectdepthstencilviewvariablegetdepthstencilarray-method"></a><span data-ttu-id="111c3-106">Метод ID3DX11EffectDepthStencilViewVariable:: ЖетдепсстенЦиларрай</span><span class="sxs-lookup"><span data-stu-id="111c3-106">ID3DX11EffectDepthStencilViewVariable::GetDepthStencilArray method</span></span>

<span data-ttu-id="111c3-107">Получите массив ресурсов представления глубины набора элементов.</span><span class="sxs-lookup"><span data-stu-id="111c3-107">Get an array of depth-stencil-view resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="111c3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="111c3-108">Syntax</span></span>


```C++
HRESULT GetDepthStencilArray(
   ID3D11DepthStencilView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a><span data-ttu-id="111c3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="111c3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="111c3-110">*ппресаурцес*</span><span class="sxs-lookup"><span data-stu-id="111c3-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="111c3-111">Тип: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span><span class="sxs-lookup"><span data-stu-id="111c3-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span></span>

<span data-ttu-id="111c3-112">Указатель на массив интерфейсов представления в виде набора элементов глубины.</span><span class="sxs-lookup"><span data-stu-id="111c3-112">A pointer to an array of depth-stencil-view interfaces.</span></span> <span data-ttu-id="111c3-113">См. [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="111c3-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> <dt>

<span data-ttu-id="111c3-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="111c3-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="111c3-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="111c3-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="111c3-116">Индекс массива, начинающийся с нуля, для получения первого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="111c3-116">The zero-based array index to get the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="111c3-117">*Количество*</span><span class="sxs-lookup"><span data-stu-id="111c3-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="111c3-118">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="111c3-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="111c3-119">Количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="111c3-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="111c3-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="111c3-120">Return value</span></span>

<span data-ttu-id="111c3-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="111c3-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="111c3-122">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="111c3-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="111c3-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="111c3-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="111c3-124">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="111c3-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="111c3-125">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="111c3-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="111c3-126">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="111c3-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="111c3-127">Требования</span><span class="sxs-lookup"><span data-stu-id="111c3-127">Requirements</span></span>



| <span data-ttu-id="111c3-128">Требование</span><span class="sxs-lookup"><span data-stu-id="111c3-128">Requirement</span></span> | <span data-ttu-id="111c3-129">Значение</span><span class="sxs-lookup"><span data-stu-id="111c3-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="111c3-130">Header</span><span class="sxs-lookup"><span data-stu-id="111c3-130">Header</span></span><br/>  | <dl> <span data-ttu-id="111c3-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="111c3-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="111c3-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="111c3-132">Library</span></span><br/> | <dl> <span data-ttu-id="111c3-133"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="111c3-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="111c3-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="111c3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="111c3-135">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="111c3-135">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

