---
title: Интерфейс ID3DX11EffectDepthStencilVariable (D3dx11effect. h)
description: Интерфейс переменной с глубиной и набором элементов имеет доступ к состоянию шаблона глубины.
ms.assetid: 8fb1be19-eed4-4d69-bbbe-94484531eba2
keywords:
- Интерфейс ID3DX11EffectDepthStencilVariable Direct3D 11
- Интерфейс ID3DX11EffectDepthStencilVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d7aa520df0c13c81435421d5f605f901a61da6e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000477"
---
# <a name="id3dx11effectdepthstencilvariable-interface"></a><span data-ttu-id="c04bc-105">Интерфейс ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="c04bc-105">ID3DX11EffectDepthStencilVariable interface</span></span>

<span data-ttu-id="c04bc-106">Интерфейс переменной с глубиной и набором элементов имеет доступ к состоянию шаблона глубины.</span><span class="sxs-lookup"><span data-stu-id="c04bc-106">A depth-stencil-variable interface accesses depth-stencil state.</span></span>

## <a name="members"></a><span data-ttu-id="c04bc-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="c04bc-107">Members</span></span>

<span data-ttu-id="c04bc-108">Интерфейс **ID3DX11EffectDepthStencilVariable** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="c04bc-108">The **ID3DX11EffectDepthStencilVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="c04bc-109">**ID3DX11EffectDepthStencilVariable** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c04bc-109">**ID3DX11EffectDepthStencilVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="c04bc-110">Методы</span><span class="sxs-lookup"><span data-stu-id="c04bc-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c04bc-111">Методы</span><span class="sxs-lookup"><span data-stu-id="c04bc-111">Methods</span></span>

<span data-ttu-id="c04bc-112">Интерфейс **ID3DX11EffectDepthStencilVariable** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c04bc-112">The **ID3DX11EffectDepthStencilVariable** interface has these methods.</span></span>



| <span data-ttu-id="c04bc-113">Метод</span><span class="sxs-lookup"><span data-stu-id="c04bc-113">Method</span></span>                                                                                         | <span data-ttu-id="c04bc-114">Описание</span><span class="sxs-lookup"><span data-stu-id="c04bc-114">Description</span></span>                                                               |
|:-----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="c04bc-115">**жетбаккингсторе**</span><span class="sxs-lookup"><span data-stu-id="c04bc-115">**GetBackingStore**</span></span>](id3dx11effectdepthstencilvariable-getbackingstore.md)                   | <span data-ttu-id="c04bc-116">Получает указатель на переменную, которая содержит состояние шаблона глубины.</span><span class="sxs-lookup"><span data-stu-id="c04bc-116">Get a pointer to a variable that contains depth-stencil state.</span></span><br/> |
| [<span data-ttu-id="c04bc-117">**жетдепсстенЦилстате**</span><span class="sxs-lookup"><span data-stu-id="c04bc-117">**GetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-getdepthstencilstate.md)         | <span data-ttu-id="c04bc-118">Получение указателя на интерфейс трафарета глубины.</span><span class="sxs-lookup"><span data-stu-id="c04bc-118">Get a pointer to a depth-stencil interface.</span></span><br/>                    |
| [<span data-ttu-id="c04bc-119">**сетдепсстенЦилстате**</span><span class="sxs-lookup"><span data-stu-id="c04bc-119">**SetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)         | <span data-ttu-id="c04bc-120">Задает состояние шаблона глубины.</span><span class="sxs-lookup"><span data-stu-id="c04bc-120">Sets the depth stencil state.</span></span><br/>                                  |
| [<span data-ttu-id="c04bc-121">**ундосетдепсстенЦилстате**</span><span class="sxs-lookup"><span data-stu-id="c04bc-121">**UndoSetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md) | <span data-ttu-id="c04bc-122">Восстанавливает ранее заданное состояние трафарета глубины.</span><span class="sxs-lookup"><span data-stu-id="c04bc-122">Reverts a previously set depth stencil state.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="c04bc-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="c04bc-123">Remarks</span></span>

<span data-ttu-id="c04bc-124">Интерфейс [**ID3DX11EffectVariable**](id3dx11effectvariable.md) создается при считывании воздействия в память.</span><span class="sxs-lookup"><span data-stu-id="c04bc-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="c04bc-125">Переменные эффектов сохраняются в памяти в резервном хранилище; При применении метода значения в резервном хранилище копируются на устройство.</span><span class="sxs-lookup"><span data-stu-id="c04bc-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="c04bc-126">Для возврата состояния можно использовать любой из этих методов.</span><span class="sxs-lookup"><span data-stu-id="c04bc-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="c04bc-127">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="c04bc-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c04bc-128">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="c04bc-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c04bc-129">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c04bc-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c04bc-130">Требования</span><span class="sxs-lookup"><span data-stu-id="c04bc-130">Requirements</span></span>



| <span data-ttu-id="c04bc-131">Требование</span><span class="sxs-lookup"><span data-stu-id="c04bc-131">Requirement</span></span> | <span data-ttu-id="c04bc-132">Значение</span><span class="sxs-lookup"><span data-stu-id="c04bc-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c04bc-133">Header</span><span class="sxs-lookup"><span data-stu-id="c04bc-133">Header</span></span><br/>  | <dl> <span data-ttu-id="c04bc-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c04bc-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c04bc-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c04bc-135">Library</span></span><br/> | <dl> <span data-ttu-id="c04bc-136"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="c04bc-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c04bc-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c04bc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c04bc-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="c04bc-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="c04bc-139">Effects 11, интерфейсы</span><span class="sxs-lookup"><span data-stu-id="c04bc-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="c04bc-140">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="c04bc-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





