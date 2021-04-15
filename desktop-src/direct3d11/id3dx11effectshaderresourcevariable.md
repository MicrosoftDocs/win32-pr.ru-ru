---
title: Интерфейс ID3DX11EffectShaderResourceVariable (D3dx11effect. h)
description: Интерфейс шейдера-ресурса получает доступ к ресурсу шейдера.
ms.assetid: 936a3439-1f7d-4fea-b124-1d6ead528250
keywords:
- Интерфейс ID3DX11EffectShaderResourceVariable Direct3D 11
- Интерфейс ID3DX11EffectShaderResourceVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7abfc2bf29bf3ea5333bf9e7da6630a62c5747aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998762"
---
# <a name="id3dx11effectshaderresourcevariable-interface"></a><span data-ttu-id="401c6-105">Интерфейс ID3DX11EffectShaderResourceVariable</span><span class="sxs-lookup"><span data-stu-id="401c6-105">ID3DX11EffectShaderResourceVariable interface</span></span>

<span data-ttu-id="401c6-106">Интерфейс шейдера-ресурса получает доступ к ресурсу шейдера.</span><span class="sxs-lookup"><span data-stu-id="401c6-106">A shader-resource interface accesses a shader resource.</span></span>

## <a name="members"></a><span data-ttu-id="401c6-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="401c6-107">Members</span></span>

<span data-ttu-id="401c6-108">Интерфейс **ID3DX11EffectShaderResourceVariable** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="401c6-108">The **ID3DX11EffectShaderResourceVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="401c6-109">**ID3DX11EffectShaderResourceVariable** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="401c6-109">**ID3DX11EffectShaderResourceVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="401c6-110">Методы</span><span class="sxs-lookup"><span data-stu-id="401c6-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="401c6-111">Методы</span><span class="sxs-lookup"><span data-stu-id="401c6-111">Methods</span></span>

<span data-ttu-id="401c6-112">Интерфейс **ID3DX11EffectShaderResourceVariable** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="401c6-112">The **ID3DX11EffectShaderResourceVariable** interface has these methods.</span></span>



| <span data-ttu-id="401c6-113">Метод</span><span class="sxs-lookup"><span data-stu-id="401c6-113">Method</span></span>                                                                           | <span data-ttu-id="401c6-114">Описание</span><span class="sxs-lookup"><span data-stu-id="401c6-114">Description</span></span>                                  |
|:---------------------------------------------------------------------------------|:---------------------------------------------|
| [<span data-ttu-id="401c6-115">**Ресурс**</span><span class="sxs-lookup"><span data-stu-id="401c6-115">**GetResource**</span></span>](id3dx11effectshaderresourcevariable-getresource.md)           | <span data-ttu-id="401c6-116">Получение ресурса шейдера.</span><span class="sxs-lookup"><span data-stu-id="401c6-116">Get a shader resource.</span></span><br/>            |
| [<span data-ttu-id="401c6-117">**жетресаурцеаррай**</span><span class="sxs-lookup"><span data-stu-id="401c6-117">**GetResourceArray**</span></span>](id3dx11effectshaderresourcevariable-getresourcearray.md) | <span data-ttu-id="401c6-118">Получение массива ресурсов шейдера.</span><span class="sxs-lookup"><span data-stu-id="401c6-118">Get an array of shader resources.</span></span><br/> |
| [<span data-ttu-id="401c6-119">**сетресаурце**</span><span class="sxs-lookup"><span data-stu-id="401c6-119">**SetResource**</span></span>](id3dx11effectshaderresourcevariable-setresource.md)           | <span data-ttu-id="401c6-120">Задайте ресурс шейдера.</span><span class="sxs-lookup"><span data-stu-id="401c6-120">Set a shader resource.</span></span><br/>            |
| [<span data-ttu-id="401c6-121">**сетресаурцеаррай**</span><span class="sxs-lookup"><span data-stu-id="401c6-121">**SetResourceArray**</span></span>](id3dx11effectshaderresourcevariable-setresourcearray.md) | <span data-ttu-id="401c6-122">Задайте массив ресурсов шейдера.</span><span class="sxs-lookup"><span data-stu-id="401c6-122">Set an array of shader resources.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="401c6-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="401c6-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="401c6-124">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="401c6-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="401c6-125">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="401c6-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="401c6-126">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="401c6-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="401c6-127">Требования</span><span class="sxs-lookup"><span data-stu-id="401c6-127">Requirements</span></span>



| <span data-ttu-id="401c6-128">Требование</span><span class="sxs-lookup"><span data-stu-id="401c6-128">Requirement</span></span> | <span data-ttu-id="401c6-129">Значение</span><span class="sxs-lookup"><span data-stu-id="401c6-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="401c6-130">Header</span><span class="sxs-lookup"><span data-stu-id="401c6-130">Header</span></span><br/>  | <dl> <span data-ttu-id="401c6-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="401c6-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="401c6-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="401c6-132">Library</span></span><br/> | <dl> <span data-ttu-id="401c6-133"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="401c6-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="401c6-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="401c6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="401c6-135">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="401c6-135">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="401c6-136">Effects 11, интерфейсы</span><span class="sxs-lookup"><span data-stu-id="401c6-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="401c6-137">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="401c6-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





