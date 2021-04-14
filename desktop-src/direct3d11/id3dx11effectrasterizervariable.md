---
title: Интерфейс ID3DX11EffectRasterizerVariable (D3dx11effect. h)
description: Интерфейс переменной средства прорисовки имеет доступ к состоянию программной прорисовки.
ms.assetid: d039e3c5-c066-4658-bead-92a5d705ed89
keywords:
- Интерфейс ID3DX11EffectRasterizerVariable Direct3D 11
- Интерфейс ID3DX11EffectRasterizerVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a19c5d529d6134ebad238be6e7c6195dc628a7f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998735"
---
# <a name="id3dx11effectrasterizervariable-interface"></a><span data-ttu-id="11cc9-105">Интерфейс ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="11cc9-105">ID3DX11EffectRasterizerVariable interface</span></span>

<span data-ttu-id="11cc9-106">Интерфейс переменной средства прорисовки имеет доступ к состоянию программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="11cc9-106">A rasterizer-variable interface accesses rasterizer state.</span></span>

## <a name="members"></a><span data-ttu-id="11cc9-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="11cc9-107">Members</span></span>

<span data-ttu-id="11cc9-108">Интерфейс **ID3DX11EffectRasterizerVariable** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="11cc9-108">The **ID3DX11EffectRasterizerVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="11cc9-109">**ID3DX11EffectRasterizerVariable** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="11cc9-109">**ID3DX11EffectRasterizerVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="11cc9-110">Методы</span><span class="sxs-lookup"><span data-stu-id="11cc9-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="11cc9-111">Методы</span><span class="sxs-lookup"><span data-stu-id="11cc9-111">Methods</span></span>

<span data-ttu-id="11cc9-112">Интерфейс **ID3DX11EffectRasterizerVariable** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="11cc9-112">The **ID3DX11EffectRasterizerVariable** interface has these methods.</span></span>



| <span data-ttu-id="11cc9-113">Метод</span><span class="sxs-lookup"><span data-stu-id="11cc9-113">Method</span></span>                                                                                   | <span data-ttu-id="11cc9-114">Описание</span><span class="sxs-lookup"><span data-stu-id="11cc9-114">Description</span></span>                                                            |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="11cc9-115">**жетбаккингсторе**</span><span class="sxs-lookup"><span data-stu-id="11cc9-115">**GetBackingStore**</span></span>](id3dx11effectrasterizervariable-getbackingstore.md)               | <span data-ttu-id="11cc9-116">Возвращает указатель на переменную, которая содержит состояние растерисер.</span><span class="sxs-lookup"><span data-stu-id="11cc9-116">Get a pointer to a variable that contains rasteriser state.</span></span><br/> |
| [<span data-ttu-id="11cc9-117">**жетрастеризерстате**</span><span class="sxs-lookup"><span data-stu-id="11cc9-117">**GetRasterizerState**</span></span>](id3dx11effectrasterizervariable-getrasterizerstate.md)         | <span data-ttu-id="11cc9-118">Получение указателя на интерфейс средства программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="11cc9-118">Get a pointer to a rasterizer interface.</span></span><br/>                    |
| [<span data-ttu-id="11cc9-119">**сетрастеризерстате**</span><span class="sxs-lookup"><span data-stu-id="11cc9-119">**SetRasterizerState**</span></span>](id3dx11effectrasterizervariable-setrasterizerstate.md)         | <span data-ttu-id="11cc9-120">Задает состояние средства программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="11cc9-120">Sets the rasterizer state.</span></span><br/>                                  |
| [<span data-ttu-id="11cc9-121">**ундосетрастеризерстате**</span><span class="sxs-lookup"><span data-stu-id="11cc9-121">**UndoSetRasterizerState**</span></span>](id3dx11effectrasterizervariable-undosetrasterizerstate.md) | <span data-ttu-id="11cc9-122">Возвращает ранее установленное состояние средства отображения программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="11cc9-122">Reverts a previously set rasterizer state.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="11cc9-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="11cc9-123">Remarks</span></span>

<span data-ttu-id="11cc9-124">Интерфейс [**ID3DX11EffectVariable**](id3dx11effectvariable.md) создается при считывании воздействия в память.</span><span class="sxs-lookup"><span data-stu-id="11cc9-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="11cc9-125">Переменные эффектов сохраняются в памяти в резервном хранилище; При применении метода значения в резервном хранилище копируются на устройство.</span><span class="sxs-lookup"><span data-stu-id="11cc9-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="11cc9-126">Для возврата состояния можно использовать любой из этих методов.</span><span class="sxs-lookup"><span data-stu-id="11cc9-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="11cc9-127">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="11cc9-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="11cc9-128">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="11cc9-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="11cc9-129">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="11cc9-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="11cc9-130">Требования</span><span class="sxs-lookup"><span data-stu-id="11cc9-130">Requirements</span></span>



| <span data-ttu-id="11cc9-131">Требование</span><span class="sxs-lookup"><span data-stu-id="11cc9-131">Requirement</span></span> | <span data-ttu-id="11cc9-132">Значение</span><span class="sxs-lookup"><span data-stu-id="11cc9-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11cc9-133">Header</span><span class="sxs-lookup"><span data-stu-id="11cc9-133">Header</span></span><br/>  | <dl> <span data-ttu-id="11cc9-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="11cc9-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="11cc9-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="11cc9-135">Library</span></span><br/> | <dl> <span data-ttu-id="11cc9-136"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="11cc9-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11cc9-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11cc9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11cc9-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="11cc9-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="11cc9-139">Effects 11, интерфейсы</span><span class="sxs-lookup"><span data-stu-id="11cc9-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="11cc9-140">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="11cc9-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





