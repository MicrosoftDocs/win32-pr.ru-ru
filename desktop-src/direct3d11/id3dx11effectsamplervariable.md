---
title: Интерфейс ID3DX11EffectSamplerVariable (D3dx11effect. h)
description: Интерфейс образца имеет доступ к состоянию выборки.
ms.assetid: 8d21f829-2145-45f2-a9b4-2fdc06e0a879
keywords:
- Интерфейс ID3DX11EffectSamplerVariable Direct3D 11
- Интерфейс ID3DX11EffectSamplerVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5019022cea823566611410cd6e8fd5013380b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157255"
---
# <a name="id3dx11effectsamplervariable-interface"></a><span data-ttu-id="31535-105">Интерфейс ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="31535-105">ID3DX11EffectSamplerVariable interface</span></span>

<span data-ttu-id="31535-106">Интерфейс образца имеет доступ к состоянию выборки.</span><span class="sxs-lookup"><span data-stu-id="31535-106">A sampler interface accesses sampler state.</span></span>

## <a name="members"></a><span data-ttu-id="31535-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="31535-107">Members</span></span>

<span data-ttu-id="31535-108">Интерфейс **ID3DX11EffectSamplerVariable** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="31535-108">The **ID3DX11EffectSamplerVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="31535-109">**ID3DX11EffectSamplerVariable** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="31535-109">**ID3DX11EffectSamplerVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="31535-110">Методы</span><span class="sxs-lookup"><span data-stu-id="31535-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="31535-111">Методы</span><span class="sxs-lookup"><span data-stu-id="31535-111">Methods</span></span>

<span data-ttu-id="31535-112">Интерфейс **ID3DX11EffectSamplerVariable** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="31535-112">The **ID3DX11EffectSamplerVariable** interface has these methods.</span></span>



| <span data-ttu-id="31535-113">Метод</span><span class="sxs-lookup"><span data-stu-id="31535-113">Method</span></span>                                                                  | <span data-ttu-id="31535-114">Описание</span><span class="sxs-lookup"><span data-stu-id="31535-114">Description</span></span>                                                         |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="31535-115">**жетбаккингсторе**</span><span class="sxs-lookup"><span data-stu-id="31535-115">**GetBackingStore**</span></span>](id3dx11effectsamplervariable-getbackingstore.md) | <span data-ttu-id="31535-116">Возвращает указатель на переменную, содержащую состояние выборки.</span><span class="sxs-lookup"><span data-stu-id="31535-116">Get a pointer to a variable that contains sampler state.</span></span><br/> |
| [<span data-ttu-id="31535-117">**Выборка**</span><span class="sxs-lookup"><span data-stu-id="31535-117">**GetSampler**</span></span>](id3dx11effectsamplervariable-getsampler.md)           | <span data-ttu-id="31535-118">Получение указателя на интерфейс образца.</span><span class="sxs-lookup"><span data-stu-id="31535-118">Get a pointer to a sampler interface.</span></span><br/>                    |
| [<span data-ttu-id="31535-119">**сетсамплер**</span><span class="sxs-lookup"><span data-stu-id="31535-119">**SetSampler**</span></span>](id3dx11effectsamplervariable-setsampler.md)           | <span data-ttu-id="31535-120">Задать состояние образца.</span><span class="sxs-lookup"><span data-stu-id="31535-120">Set sampler state.</span></span><br/>                                       |
| [<span data-ttu-id="31535-121">**ундосетсамплер**</span><span class="sxs-lookup"><span data-stu-id="31535-121">**UndoSetSampler**</span></span>](id3dx11effectsamplervariable-undosetsampler.md)   | <span data-ttu-id="31535-122">Отменить ранее установленное состояние образца.</span><span class="sxs-lookup"><span data-stu-id="31535-122">Revert a previously set sampler state.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="31535-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="31535-123">Remarks</span></span>

<span data-ttu-id="31535-124">Интерфейс [**ID3DX11EffectVariable**](id3dx11effectvariable.md) создается при считывании воздействия в память.</span><span class="sxs-lookup"><span data-stu-id="31535-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="31535-125">Переменные эффектов сохраняются в памяти в резервном хранилище; При применении метода значения в резервном хранилище копируются на устройство.</span><span class="sxs-lookup"><span data-stu-id="31535-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="31535-126">Для возврата состояния можно использовать любой из этих методов.</span><span class="sxs-lookup"><span data-stu-id="31535-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="31535-127">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="31535-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="31535-128">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="31535-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="31535-129">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="31535-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="31535-130">Требования</span><span class="sxs-lookup"><span data-stu-id="31535-130">Requirements</span></span>



| <span data-ttu-id="31535-131">Требование</span><span class="sxs-lookup"><span data-stu-id="31535-131">Requirement</span></span> | <span data-ttu-id="31535-132">Значение</span><span class="sxs-lookup"><span data-stu-id="31535-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31535-133">Header</span><span class="sxs-lookup"><span data-stu-id="31535-133">Header</span></span><br/>  | <dl> <span data-ttu-id="31535-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="31535-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="31535-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="31535-135">Library</span></span><br/> | <dl> <span data-ttu-id="31535-136"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="31535-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31535-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31535-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31535-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="31535-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="31535-139">Effects 11, интерфейсы</span><span class="sxs-lookup"><span data-stu-id="31535-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="31535-140">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="31535-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





