---
title: Интерфейс ID3DX11EffectRenderTargetViewVariable (D3dx11effect. h)
description: Интерфейс представления визуализации-целевого объекта обращается к целевому объекту прорисовки.
ms.assetid: 35c4e1da-05a8-4f1c-8730-58e3c90ad213
keywords:
- Интерфейс ID3DX11EffectRenderTargetViewVariable Direct3D 11
- Интерфейс ID3DX11EffectRenderTargetViewVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5b20f83639fd973016bbe263d9d21dae7b295c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986876"
---
# <a name="id3dx11effectrendertargetviewvariable-interface"></a><span data-ttu-id="f4fd7-105">Интерфейс ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="f4fd7-105">ID3DX11EffectRenderTargetViewVariable interface</span></span>

<span data-ttu-id="f4fd7-106">Интерфейс представления визуализации-целевого объекта обращается к целевому объекту прорисовки.</span><span class="sxs-lookup"><span data-stu-id="f4fd7-106">A render-target-view interface accesses a render target.</span></span>

## <a name="members"></a><span data-ttu-id="f4fd7-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="f4fd7-107">Members</span></span>

<span data-ttu-id="f4fd7-108">Интерфейс **ID3DX11EffectRenderTargetViewVariable** наследует от [**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="f4fd7-108">The **ID3DX11EffectRenderTargetViewVariable** interface inherits from [**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="f4fd7-109">**ID3DX11EffectRenderTargetViewVariable** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f4fd7-109">**ID3DX11EffectRenderTargetViewVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="f4fd7-110">Методы</span><span class="sxs-lookup"><span data-stu-id="f4fd7-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f4fd7-111">Методы</span><span class="sxs-lookup"><span data-stu-id="f4fd7-111">Methods</span></span>

<span data-ttu-id="f4fd7-112">Интерфейс **ID3DX11EffectRenderTargetViewVariable** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f4fd7-112">The **ID3DX11EffectRenderTargetViewVariable** interface has these methods.</span></span>



| <span data-ttu-id="f4fd7-113">Метод</span><span class="sxs-lookup"><span data-stu-id="f4fd7-113">Method</span></span>                                                                                     | <span data-ttu-id="f4fd7-114">Описание</span><span class="sxs-lookup"><span data-stu-id="f4fd7-114">Description</span></span>                                |
|:-------------------------------------------------------------------------------------------|:-------------------------------------------|
| [<span data-ttu-id="f4fd7-115">**жетрендертаржет**</span><span class="sxs-lookup"><span data-stu-id="f4fd7-115">**GetRenderTarget**</span></span>](id3dx11effectrendertargetviewvariable-getrendertarget.md)           | <span data-ttu-id="f4fd7-116">Получение целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="f4fd7-116">Get a render-target.</span></span><br/>            |
| [<span data-ttu-id="f4fd7-117">**жетрендертаржетаррай**</span><span class="sxs-lookup"><span data-stu-id="f4fd7-117">**GetRenderTargetArray**</span></span>](id3dx11effectrendertargetviewvariable-getrendertargetarray.md) | <span data-ttu-id="f4fd7-118">Получение массива целевых объектов рендеринга.</span><span class="sxs-lookup"><span data-stu-id="f4fd7-118">Get an array of render-targets.</span></span><br/> |
| [<span data-ttu-id="f4fd7-119">**сетрендертаржет**</span><span class="sxs-lookup"><span data-stu-id="f4fd7-119">**SetRenderTarget**</span></span>](id3dx11effectrendertargetviewvariable-setrendertarget.md)           | <span data-ttu-id="f4fd7-120">Задайте целевой объект рендеринга.</span><span class="sxs-lookup"><span data-stu-id="f4fd7-120">Set a render-target.</span></span><br/>            |
| [<span data-ttu-id="f4fd7-121">**сетрендертаржетаррай**</span><span class="sxs-lookup"><span data-stu-id="f4fd7-121">**SetRenderTargetArray**</span></span>](id3dx11effectrendertargetviewvariable-setrendertargetarray.md) | <span data-ttu-id="f4fd7-122">Задайте массив целевых объектов рендеринга.</span><span class="sxs-lookup"><span data-stu-id="f4fd7-122">Set an array of render-targets.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f4fd7-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="f4fd7-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f4fd7-124">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="f4fd7-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f4fd7-125">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="f4fd7-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f4fd7-126">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f4fd7-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f4fd7-127">Требования</span><span class="sxs-lookup"><span data-stu-id="f4fd7-127">Requirements</span></span>



| <span data-ttu-id="f4fd7-128">Требование</span><span class="sxs-lookup"><span data-stu-id="f4fd7-128">Requirement</span></span> | <span data-ttu-id="f4fd7-129">Значение</span><span class="sxs-lookup"><span data-stu-id="f4fd7-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4fd7-130">Header</span><span class="sxs-lookup"><span data-stu-id="f4fd7-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f4fd7-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4fd7-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f4fd7-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f4fd7-132">Library</span></span><br/> | <dl> <span data-ttu-id="f4fd7-133"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="f4fd7-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4fd7-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4fd7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4fd7-135">**ID3DX11EffectRasterizerVariable**</span><span class="sxs-lookup"><span data-stu-id="f4fd7-135">**ID3DX11EffectRasterizerVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="f4fd7-136">Effects 11, интерфейсы</span><span class="sxs-lookup"><span data-stu-id="f4fd7-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f4fd7-137">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="f4fd7-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





