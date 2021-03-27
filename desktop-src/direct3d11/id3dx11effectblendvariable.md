---
title: Интерфейс ID3DX11EffectBlendVariable (D3dx11effect. h)
description: Интерфейс Blend-Variable получает доступ к состоянию смешения.
ms.assetid: 8a6e6e7e-2f1e-4e16-8d28-ffc7f3f018d6
keywords:
- Интерфейс ID3DX11EffectBlendVariable Direct3D 11
- Интерфейс ID3DX11EffectBlendVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57a0a8a3ec0c2a3d92dfc9579fff8b3769dcfc5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000521"
---
# <a name="id3dx11effectblendvariable-interface"></a><span data-ttu-id="2ccb4-105">Интерфейс ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="2ccb4-105">ID3DX11EffectBlendVariable interface</span></span>

<span data-ttu-id="2ccb4-106">Интерфейс Blend-Variable получает доступ к состоянию смешения.</span><span class="sxs-lookup"><span data-stu-id="2ccb4-106">The blend-variable interface accesses blend state.</span></span>

## <a name="members"></a><span data-ttu-id="2ccb4-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="2ccb4-107">Members</span></span>

<span data-ttu-id="2ccb4-108">Интерфейс **ID3DX11EffectBlendVariable** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="2ccb4-108">The **ID3DX11EffectBlendVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="2ccb4-109">**ID3DX11EffectBlendVariable** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2ccb4-109">**ID3DX11EffectBlendVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="2ccb4-110">Методы</span><span class="sxs-lookup"><span data-stu-id="2ccb4-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2ccb4-111">Методы</span><span class="sxs-lookup"><span data-stu-id="2ccb4-111">Methods</span></span>

<span data-ttu-id="2ccb4-112">Интерфейс **ID3DX11EffectBlendVariable** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2ccb4-112">The **ID3DX11EffectBlendVariable** interface has these methods.</span></span>



| <span data-ttu-id="2ccb4-113">Метод</span><span class="sxs-lookup"><span data-stu-id="2ccb4-113">Method</span></span>                                                                    | <span data-ttu-id="2ccb4-114">Описание</span><span class="sxs-lookup"><span data-stu-id="2ccb4-114">Description</span></span>                                          |
|:--------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="2ccb4-115">**жетбаккингсторе**</span><span class="sxs-lookup"><span data-stu-id="2ccb4-115">**GetBackingStore**</span></span>](id3dx11effectblendvariable-getbackingstore.md)     | <span data-ttu-id="2ccb4-116">Получает указатель на переменную состояния Blend.</span><span class="sxs-lookup"><span data-stu-id="2ccb4-116">Get a pointer to a blend-state variable.</span></span><br/>  |
| [<span data-ttu-id="2ccb4-117">**жетблендстате**</span><span class="sxs-lookup"><span data-stu-id="2ccb4-117">**GetBlendState**</span></span>](id3dx11effectblendvariable-getblendstate.md)         | <span data-ttu-id="2ccb4-118">Получает указатель на интерфейс состояния смешения.</span><span class="sxs-lookup"><span data-stu-id="2ccb4-118">Get a pointer to a blend-state interface.</span></span><br/> |
| [<span data-ttu-id="2ccb4-119">**сетблендстате**</span><span class="sxs-lookup"><span data-stu-id="2ccb4-119">**SetBlendState**</span></span>](id3dx11effectblendvariable-setblendstate.md)         | <span data-ttu-id="2ccb4-120">Задает состояние смешения для действия.</span><span class="sxs-lookup"><span data-stu-id="2ccb4-120">Sets an effect's blend-state.</span></span><br/>             |
| [<span data-ttu-id="2ccb4-121">**ундосетблендстате**</span><span class="sxs-lookup"><span data-stu-id="2ccb4-121">**UndoSetBlendState**</span></span>](id3dx11effectblendvariable-undosetblendstate.md) | <span data-ttu-id="2ccb4-122">Восстанавливает ранее установленное состояние Blend.</span><span class="sxs-lookup"><span data-stu-id="2ccb4-122">Reverts a previously set blend-state.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="2ccb4-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="2ccb4-123">Remarks</span></span>

<span data-ttu-id="2ccb4-124">Интерфейс [**ID3DX11EffectVariable**](id3dx11effectvariable.md) создается при считывании воздействия в память.</span><span class="sxs-lookup"><span data-stu-id="2ccb4-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="2ccb4-125">Переменные эффектов сохраняются в памяти в резервном хранилище; При применении метода значения в резервном хранилище копируются на устройство.</span><span class="sxs-lookup"><span data-stu-id="2ccb4-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="2ccb4-126">Для возврата состояния можно использовать любой из этих методов.</span><span class="sxs-lookup"><span data-stu-id="2ccb4-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="2ccb4-127">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="2ccb4-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2ccb4-128">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="2ccb4-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2ccb4-129">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2ccb4-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2ccb4-130">Требования</span><span class="sxs-lookup"><span data-stu-id="2ccb4-130">Requirements</span></span>



| <span data-ttu-id="2ccb4-131">Требование</span><span class="sxs-lookup"><span data-stu-id="2ccb4-131">Requirement</span></span> | <span data-ttu-id="2ccb4-132">Значение</span><span class="sxs-lookup"><span data-stu-id="2ccb4-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ccb4-133">Header</span><span class="sxs-lookup"><span data-stu-id="2ccb4-133">Header</span></span><br/>  | <dl> <span data-ttu-id="2ccb4-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ccb4-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2ccb4-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2ccb4-135">Library</span></span><br/> | <dl> <span data-ttu-id="2ccb4-136"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="2ccb4-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ccb4-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ccb4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ccb4-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="2ccb4-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="2ccb4-139">Effects 11, интерфейсы</span><span class="sxs-lookup"><span data-stu-id="2ccb4-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="2ccb4-140">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="2ccb4-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





