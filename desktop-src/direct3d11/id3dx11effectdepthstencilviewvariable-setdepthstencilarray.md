---
title: Метод ID3DX11EffectDepthStencilViewVariable СетдепсстенЦиларрай (D3dx11effect. h)
description: Установите массив ресурсов представления глубины набора элементов.
ms.assetid: 7a00ca3e-fb07-4185-a361-36228f72dcea
keywords:
- Метод СетдепсстенЦиларрай Direct3D 11
- Метод СетдепсстенЦиларрай Direct3D 11, интерфейс ID3DX11EffectDepthStencilViewVariable
- Интерфейс ID3DX11EffectDepthStencilViewVariable Direct3D 11, метод СетдепсстенЦиларрай
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.SetDepthStencilArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329f91fff70d78c51475b799a08dec1c6d34a157
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986975"
---
# <a name="id3dx11effectdepthstencilviewvariablesetdepthstencilarray-method"></a><span data-ttu-id="158c6-106">Метод ID3DX11EffectDepthStencilViewVariable:: СетдепсстенЦиларрай</span><span class="sxs-lookup"><span data-stu-id="158c6-106">ID3DX11EffectDepthStencilViewVariable::SetDepthStencilArray method</span></span>

<span data-ttu-id="158c6-107">Установите массив ресурсов представления глубины набора элементов.</span><span class="sxs-lookup"><span data-stu-id="158c6-107">Set an array of depth-stencil-view resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="158c6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="158c6-108">Syntax</span></span>


```C++
HRESULT SetDepthStencilArray(
   ID3D11DepthStencilView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a><span data-ttu-id="158c6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="158c6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="158c6-110">*ппресаурцес*</span><span class="sxs-lookup"><span data-stu-id="158c6-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="158c6-111">Тип: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span><span class="sxs-lookup"><span data-stu-id="158c6-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span></span>

<span data-ttu-id="158c6-112">Указатель на массив интерфейсов представления в виде набора элементов глубины.</span><span class="sxs-lookup"><span data-stu-id="158c6-112">A pointer to an array of depth-stencil-view interfaces.</span></span> <span data-ttu-id="158c6-113">См. [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="158c6-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> <dt>

<span data-ttu-id="158c6-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="158c6-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="158c6-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="158c6-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="158c6-116">Индекс массива, начинающийся с нуля, для установки первого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="158c6-116">The zero-based array index to set the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="158c6-117">*Количество*</span><span class="sxs-lookup"><span data-stu-id="158c6-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="158c6-118">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="158c6-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="158c6-119">Количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="158c6-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="158c6-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="158c6-120">Return value</span></span>

<span data-ttu-id="158c6-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="158c6-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="158c6-122">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="158c6-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="158c6-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="158c6-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="158c6-124">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="158c6-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="158c6-125">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="158c6-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="158c6-126">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="158c6-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="158c6-127">Требования</span><span class="sxs-lookup"><span data-stu-id="158c6-127">Requirements</span></span>



| <span data-ttu-id="158c6-128">Требование</span><span class="sxs-lookup"><span data-stu-id="158c6-128">Requirement</span></span> | <span data-ttu-id="158c6-129">Значение</span><span class="sxs-lookup"><span data-stu-id="158c6-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="158c6-130">Header</span><span class="sxs-lookup"><span data-stu-id="158c6-130">Header</span></span><br/>  | <dl> <span data-ttu-id="158c6-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="158c6-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="158c6-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="158c6-132">Library</span></span><br/> | <dl> <span data-ttu-id="158c6-133"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="158c6-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="158c6-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="158c6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="158c6-135">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="158c6-135">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

