---
title: Метод ID3DX11EffectRenderTargetViewVariable Жетрендертаржетаррай (D3dx11effect. h)
description: Получение массива целевых объектов рендеринга.
ms.assetid: cc98a3b3-c2a2-48d0-86a8-77b914a199ec
keywords:
- Метод Жетрендертаржетаррай Direct3D 11
- Метод Жетрендертаржетаррай Direct3D 11, интерфейс ID3DX11EffectRenderTargetViewVariable
- Интерфейс ID3DX11EffectRenderTargetViewVariable Direct3D 11, метод Жетрендертаржетаррай
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.GetRenderTargetArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3521b05bbc4e603264b993b6fe7b677a5cf46aee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998729"
---
# <a name="id3dx11effectrendertargetviewvariablegetrendertargetarray-method"></a><span data-ttu-id="26136-106">Метод ID3DX11EffectRenderTargetViewVariable:: Жетрендертаржетаррай</span><span class="sxs-lookup"><span data-stu-id="26136-106">ID3DX11EffectRenderTargetViewVariable::GetRenderTargetArray method</span></span>

<span data-ttu-id="26136-107">Получение массива целевых объектов рендеринга.</span><span class="sxs-lookup"><span data-stu-id="26136-107">Get an array of render-targets.</span></span>

## <a name="syntax"></a><span data-ttu-id="26136-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26136-108">Syntax</span></span>


```C++
HRESULT GetRenderTargetArray(
   ID3D11RenderTargetView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a><span data-ttu-id="26136-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="26136-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26136-110">*ппресаурцес*</span><span class="sxs-lookup"><span data-stu-id="26136-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="26136-111">Тип: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span><span class="sxs-lookup"><span data-stu-id="26136-111">Type: **[**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span></span>

<span data-ttu-id="26136-112">Указатель на массив интерфейсов визуализации-целевого представления.</span><span class="sxs-lookup"><span data-stu-id="26136-112">A pointer to an array of render-target-view interfaces.</span></span> <span data-ttu-id="26136-113">См. [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span><span class="sxs-lookup"><span data-stu-id="26136-113">See [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span></span>

</dd> <dt>

<span data-ttu-id="26136-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="26136-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="26136-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="26136-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="26136-116">Индекс массива, начинающийся с нуля, для получения первого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="26136-116">The zero-based array index to get the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="26136-117">*Количество*</span><span class="sxs-lookup"><span data-stu-id="26136-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="26136-118">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="26136-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="26136-119">Количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="26136-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26136-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26136-120">Return value</span></span>

<span data-ttu-id="26136-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="26136-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="26136-122">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="26136-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="26136-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="26136-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="26136-124">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="26136-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="26136-125">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="26136-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="26136-126">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="26136-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="26136-127">Требования</span><span class="sxs-lookup"><span data-stu-id="26136-127">Requirements</span></span>



| <span data-ttu-id="26136-128">Требование</span><span class="sxs-lookup"><span data-stu-id="26136-128">Requirement</span></span> | <span data-ttu-id="26136-129">Значение</span><span class="sxs-lookup"><span data-stu-id="26136-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26136-130">Header</span><span class="sxs-lookup"><span data-stu-id="26136-130">Header</span></span><br/>  | <dl> <span data-ttu-id="26136-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="26136-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="26136-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="26136-132">Library</span></span><br/> | <dl> <span data-ttu-id="26136-133"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="26136-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26136-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26136-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26136-135">ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="26136-135">ID3DX11EffectRenderTargetViewVariable</span></span>](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

