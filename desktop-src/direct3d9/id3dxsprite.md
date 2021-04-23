---
description: Интерфейс ID3DXSprite предоставляет набор методов, упрощающих процесс рисования спрайтов с помощью Microsoft Direct3D.
ms.assetid: ccf34fac-91a7-4734-bc62-aedaf4d66522
title: Интерфейс ID3DXSprite (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3703132cd8a0f7744119d9b8cb5d9d48f260094c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914752"
---
# <a name="id3dxsprite-interface"></a><span data-ttu-id="93369-103">Интерфейс ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="93369-103">ID3DXSprite interface</span></span>

<span data-ttu-id="93369-104">Интерфейс ID3DXSprite предоставляет набор методов, упрощающих процесс рисования спрайтов с помощью Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="93369-104">The ID3DXSprite interface provides a set of methods that simplify the process of drawing sprites using Microsoft Direct3D.</span></span>

## <a name="members"></a><span data-ttu-id="93369-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="93369-105">Members</span></span>

<span data-ttu-id="93369-106">Интерфейс **ID3DXSprite** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="93369-106">The **ID3DXSprite** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="93369-107">**ID3DXSprite** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="93369-107">**ID3DXSprite** also has these types of members:</span></span>

-   [<span data-ttu-id="93369-108">Методы</span><span class="sxs-lookup"><span data-stu-id="93369-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="93369-109">Методы</span><span class="sxs-lookup"><span data-stu-id="93369-109">Methods</span></span>

<span data-ttu-id="93369-110">Интерфейс **ID3DXSprite** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="93369-110">The **ID3DXSprite** interface has these methods.</span></span>



| <span data-ttu-id="93369-111">Метод</span><span class="sxs-lookup"><span data-stu-id="93369-111">Method</span></span>                                                | <span data-ttu-id="93369-112">Описание</span><span class="sxs-lookup"><span data-stu-id="93369-112">Description</span></span>                                                                                                                                                                                                                  |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93369-113">**Начать**</span><span class="sxs-lookup"><span data-stu-id="93369-113">**Begin**</span></span>](id3dxsprite--begin.md)                   | <span data-ttu-id="93369-114">Подготавливает устройство для рисования спрайтов.</span><span class="sxs-lookup"><span data-stu-id="93369-114">Prepares a device for drawing sprites.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="93369-115">**Draw**</span><span class="sxs-lookup"><span data-stu-id="93369-115">**Draw**</span></span>](id3dxsprite--draw.md)                     | <span data-ttu-id="93369-116">Добавляет спрайт в список пакетных спрайтов.</span><span class="sxs-lookup"><span data-stu-id="93369-116">Adds a sprite to the list of batched sprites.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="93369-117">**END**</span><span class="sxs-lookup"><span data-stu-id="93369-117">**End**</span></span>](id3dxsprite--end.md)                       | <span data-ttu-id="93369-118">Вызывает [**ID3DXSprite:: Flush**](id3dxsprite--flush.md) и восстанавливает состояние устройства до вызова [**ID3DXSprite:: Begin**](id3dxsprite--begin.md) .</span><span class="sxs-lookup"><span data-stu-id="93369-118">Calls [**ID3DXSprite::Flush**](id3dxsprite--flush.md) and restores the device state to how it was before [**ID3DXSprite::Begin**](id3dxsprite--begin.md) was called.</span></span><br/>                                            |
| [<span data-ttu-id="93369-119">**Очистка**</span><span class="sxs-lookup"><span data-stu-id="93369-119">**Flush**</span></span>](id3dxsprite--flush.md)                   | <span data-ttu-id="93369-120">Принудительная отправка всех пакетированных спрайтов на устройство.</span><span class="sxs-lookup"><span data-stu-id="93369-120">Forces all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="93369-121">Состояния устройств остаются в том виде, в котором они были после последнего вызова [**ID3DXSprite:: Begin**](id3dxsprite--begin.md).</span><span class="sxs-lookup"><span data-stu-id="93369-121">Device states remain as they were after the last call to [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span> <span data-ttu-id="93369-122">Затем список пакетных спрайтов удаляется.</span><span class="sxs-lookup"><span data-stu-id="93369-122">The list of batched sprites is then cleared.</span></span><br/> |
| [<span data-ttu-id="93369-123">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="93369-123">**GetDevice**</span></span>](id3dxsprite--getdevice.md)           | <span data-ttu-id="93369-124">Извлекает устройство, связанное с объектом Sprite.</span><span class="sxs-lookup"><span data-stu-id="93369-124">Retrieves the device associated with the sprite object.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="93369-125">**Преобразование**</span><span class="sxs-lookup"><span data-stu-id="93369-125">**GetTransform**</span></span>](id3dxsprite--gettransform.md)     | <span data-ttu-id="93369-126">Возвращает преобразование спрайта.</span><span class="sxs-lookup"><span data-stu-id="93369-126">Gets the sprite transform.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="93369-127">**онлостдевице**</span><span class="sxs-lookup"><span data-stu-id="93369-127">**OnLostDevice**</span></span>](id3dxsprite--onlostdevice.md)     | <span data-ttu-id="93369-128">Используйте этот метод, чтобы освободить все ссылки на ресурсы видеопамяти и удалить все статеблоккс.</span><span class="sxs-lookup"><span data-stu-id="93369-128">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="93369-129">Этот метод должен вызываться при каждом потере устройства или перед сбросом устройства.</span><span class="sxs-lookup"><span data-stu-id="93369-129">This method should be called whenever a device is lost or before resetting a device.</span></span><br/>                              |
| [<span data-ttu-id="93369-130">**онресетдевице**</span><span class="sxs-lookup"><span data-stu-id="93369-130">**OnResetDevice**</span></span>](id3dxsprite--onresetdevice.md)   | <span data-ttu-id="93369-131">Этот метод используется для повторного получения ресурсов и сохранения начального состояния.</span><span class="sxs-lookup"><span data-stu-id="93369-131">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="93369-132">**сеттрансформ**</span><span class="sxs-lookup"><span data-stu-id="93369-132">**SetTransform**</span></span>](id3dxsprite--settransform.md)     | <span data-ttu-id="93369-133">Задает преобразование спрайта.</span><span class="sxs-lookup"><span data-stu-id="93369-133">Sets the sprite transform.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="93369-134">**сетворлдвиевлх**</span><span class="sxs-lookup"><span data-stu-id="93369-134">**SetWorldViewLH**</span></span>](id3dxsprite--setworldviewlh.md) | <span data-ttu-id="93369-135">Задает для спрайта левое преобразование представления мира.</span><span class="sxs-lookup"><span data-stu-id="93369-135">Sets the left-handed world-view transform for a sprite.</span></span> <span data-ttu-id="93369-136">Перед объявлением или сортировкой спрайтов необходимо вызвать этот метод.</span><span class="sxs-lookup"><span data-stu-id="93369-136">A call to this method is required before billboarding or sorting sprites.</span></span><br/>                                                                                 |
| [<span data-ttu-id="93369-137">**сетворлдвиеврх**</span><span class="sxs-lookup"><span data-stu-id="93369-137">**SetWorldViewRH**</span></span>](id3dxsprite--setworldviewrh.md) | <span data-ttu-id="93369-138">Задает для спрайта правое преобразование представления мира.</span><span class="sxs-lookup"><span data-stu-id="93369-138">Sets the right-handed world-view transform for a sprite.</span></span> <span data-ttu-id="93369-139">Перед объявлением или сортировкой спрайтов необходимо вызвать этот метод.</span><span class="sxs-lookup"><span data-stu-id="93369-139">A call to this method is required before billboarding or sorting sprites.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="93369-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93369-140">Remarks</span></span>

<span data-ttu-id="93369-141">Интерфейс **ID3DXSprite** получается путем вызова функции [**D3DXCreateSprite**](d3dxcreatesprite.md) .</span><span class="sxs-lookup"><span data-stu-id="93369-141">The **ID3DXSprite** interface is obtained by calling the [**D3DXCreateSprite**](d3dxcreatesprite.md) function.</span></span>

<span data-ttu-id="93369-142">Приложение, как правило, сначала вызывает [**ID3DXSprite:: Begin**](id3dxsprite--begin.md), что позволяет управлять состоянием отрисовки устройства, альфа-смешением и преобразованием и сортировкой спрайтов.</span><span class="sxs-lookup"><span data-stu-id="93369-142">The application typically first calls [**ID3DXSprite::Begin**](id3dxsprite--begin.md), which allows control over the device render state, alpha blending, and sprite transformation and sorting.</span></span> <span data-ttu-id="93369-143">Затем для отображения каждого спрайта вызовите [**ID3DXSprite::D RAW**](id3dxsprite--draw.md).</span><span class="sxs-lookup"><span data-stu-id="93369-143">Then for each sprite to be displayed, call [**ID3DXSprite::Draw**](id3dxsprite--draw.md).</span></span> <span data-ttu-id="93369-144">**ID3DXSprite::D RAW** можно вызывать многократно для хранения любого числа спрайтов.</span><span class="sxs-lookup"><span data-stu-id="93369-144">**ID3DXSprite::Draw** can be called repeatedly to store any number of sprites.</span></span> <span data-ttu-id="93369-145">Чтобы отобразить пакетные спрайты на устройстве, вызовите метод [**ID3DXSprite:: end**](id3dxsprite--end.md) или [**ID3DXSprite:: Flush**](id3dxsprite--flush.md).</span><span class="sxs-lookup"><span data-stu-id="93369-145">To display the batched sprites to the device, call [**ID3DXSprite::End**](id3dxsprite--end.md) or [**ID3DXSprite::Flush**](id3dxsprite--flush.md).</span></span>

<span data-ttu-id="93369-146">Тип LPD3DXSPRITE определяется как указатель на интерфейс **ID3DXSprite** .</span><span class="sxs-lookup"><span data-stu-id="93369-146">The LPD3DXSPRITE type is defined as a pointer to the **ID3DXSprite** interface.</span></span>


```
typedef interface ID3DXSprite ID3DXSprite;
typedef interface ID3DXSprite *LPD3DXSPRITE;
```



## <a name="requirements"></a><span data-ttu-id="93369-147">Требования</span><span class="sxs-lookup"><span data-stu-id="93369-147">Requirements</span></span>



| <span data-ttu-id="93369-148">Требование</span><span class="sxs-lookup"><span data-stu-id="93369-148">Requirement</span></span> | <span data-ttu-id="93369-149">Значение</span><span class="sxs-lookup"><span data-stu-id="93369-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93369-150">Header</span><span class="sxs-lookup"><span data-stu-id="93369-150">Header</span></span><br/>  | <dl> <span data-ttu-id="93369-151"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="93369-151"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="93369-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="93369-152">Library</span></span><br/> | <dl> <span data-ttu-id="93369-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93369-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="93369-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93369-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93369-155">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="93369-155">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
