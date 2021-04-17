---
description: Используется для установки и запроса эффектов, а также для выбора методов. Объект Effect может содержать несколько методов для визуализации одного и того же результата.
ms.assetid: bffc64ab-12e7-44e9-b296-262b0459a68a
title: Интерфейс ID3DXEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 275376234739964940d70381a34331ff5b89f2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703696"
---
# <a name="id3dxeffect-interface"></a><span data-ttu-id="573af-104">Интерфейс ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="573af-104">ID3DXEffect interface</span></span>

<span data-ttu-id="573af-105">Используется для установки и запроса эффектов, а также для выбора методов.</span><span class="sxs-lookup"><span data-stu-id="573af-105">Used to set and query effects, and to choose techniques.</span></span> <span data-ttu-id="573af-106">Объект Effect может содержать несколько методов для визуализации одного и того же результата.</span><span class="sxs-lookup"><span data-stu-id="573af-106">An effect object can contain multiple techniques to render the same effect.</span></span>

## <a name="members"></a><span data-ttu-id="573af-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="573af-107">Members</span></span>

<span data-ttu-id="573af-108">Интерфейс **ID3DXEffect** наследует от [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span><span class="sxs-lookup"><span data-stu-id="573af-108">The **ID3DXEffect** interface inherits from [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span></span> <span data-ttu-id="573af-109">**ID3DXEffect** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="573af-109">**ID3DXEffect** also has these types of members:</span></span>

-   [<span data-ttu-id="573af-110">Методы</span><span class="sxs-lookup"><span data-stu-id="573af-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="573af-111">Методы</span><span class="sxs-lookup"><span data-stu-id="573af-111">Methods</span></span>

<span data-ttu-id="573af-112">Интерфейс **ID3DXEffect** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="573af-112">The **ID3DXEffect** interface has these methods.</span></span>



| <span data-ttu-id="573af-113">Метод</span><span class="sxs-lookup"><span data-stu-id="573af-113">Method</span></span>                                                                | <span data-ttu-id="573af-114">Описание</span><span class="sxs-lookup"><span data-stu-id="573af-114">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="573af-115">**апплипараметерблокк**</span><span class="sxs-lookup"><span data-stu-id="573af-115">**ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)       | <span data-ttu-id="573af-116">Применить значения в блоке состояния к текущему состоянию системы.</span><span class="sxs-lookup"><span data-stu-id="573af-116">Apply the values in a state block to the current effect system state.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="573af-117">**Начать**</span><span class="sxs-lookup"><span data-stu-id="573af-117">**Begin**</span></span>](id3dxeffect--begin.md)                                   | <span data-ttu-id="573af-118">Запускает активный метод.</span><span class="sxs-lookup"><span data-stu-id="573af-118">Starts an active technique.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="573af-119">**бегинпараметерблокк**</span><span class="sxs-lookup"><span data-stu-id="573af-119">**BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)       | <span data-ttu-id="573af-120">Начать запись изменений состояния в блоке параметров.</span><span class="sxs-lookup"><span data-stu-id="573af-120">Start capturing state changes in a parameter block.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="573af-121">**бегинпасс**</span><span class="sxs-lookup"><span data-stu-id="573af-121">**BeginPass**</span></span>](id3dxeffect--beginpass.md)                           | <span data-ttu-id="573af-122">Начинает проход в активном методе.</span><span class="sxs-lookup"><span data-stu-id="573af-122">Begins a pass, within the active technique.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="573af-123">**клониффект**</span><span class="sxs-lookup"><span data-stu-id="573af-123">**CloneEffect**</span></span>](id3dxeffect--cloneeffect.md)                       | <span data-ttu-id="573af-124">Создает копию результата.</span><span class="sxs-lookup"><span data-stu-id="573af-124">Creates a copy of an effect.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="573af-125">**CommitChanges**</span><span class="sxs-lookup"><span data-stu-id="573af-125">**CommitChanges**</span></span>](id3dxeffect--commitchanges.md)                   | <span data-ttu-id="573af-126">Распространите изменения состояния, происходящие внутри активного прохода на устройстве перед отрисовкой.</span><span class="sxs-lookup"><span data-stu-id="573af-126">Propagate state changes that occur inside of an active pass to the device before rendering.</span></span><br/>                                                                                           |
| [<span data-ttu-id="573af-127">**делетепараметерблокк**</span><span class="sxs-lookup"><span data-stu-id="573af-127">**DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)     | <span data-ttu-id="573af-128">Удаляет блок параметров.</span><span class="sxs-lookup"><span data-stu-id="573af-128">Delete a parameter block.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="573af-129">**END**</span><span class="sxs-lookup"><span data-stu-id="573af-129">**End**</span></span>](id3dxeffect--end.md)                                       | <span data-ttu-id="573af-130">Завершает активный метод.</span><span class="sxs-lookup"><span data-stu-id="573af-130">Ends an active technique.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="573af-131">**ендпараметерблокк**</span><span class="sxs-lookup"><span data-stu-id="573af-131">**EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)           | <span data-ttu-id="573af-132">Прерывать изменения состояния параметров эффектов записи.</span><span class="sxs-lookup"><span data-stu-id="573af-132">Stop capturing effect parameter state changes.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="573af-133">**ендпасс**</span><span class="sxs-lookup"><span data-stu-id="573af-133">**EndPass**</span></span>](id3dxeffect--endpass.md)                               | <span data-ttu-id="573af-134">Завершение активного прохода.</span><span class="sxs-lookup"><span data-stu-id="573af-134">End an active pass.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="573af-135">**финднекствалидтечникуе**</span><span class="sxs-lookup"><span data-stu-id="573af-135">**FindNextValidTechnique**</span></span>](id3dxeffect--findnextvalidtechnique.md) | <span data-ttu-id="573af-136">Выполняет поиск следующего допустимого метода, начиная с метода после указанного метода.</span><span class="sxs-lookup"><span data-stu-id="573af-136">Searches for the next valid technique, starting at the technique after the specified technique.</span></span><br/>                                                                                       |
| [<span data-ttu-id="573af-137">**жеткурренттечникуе**</span><span class="sxs-lookup"><span data-stu-id="573af-137">**GetCurrentTechnique**</span></span>](id3dxeffect--getcurrenttechnique.md)       | <span data-ttu-id="573af-138">Возвращает текущий метод.</span><span class="sxs-lookup"><span data-stu-id="573af-138">Gets the current technique.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="573af-139">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="573af-139">**GetDevice**</span></span>](id3dxeffect--getdevice.md)                           | <span data-ttu-id="573af-140">Извлекает устройство, связанное с этим действием.</span><span class="sxs-lookup"><span data-stu-id="573af-140">Retrieves the device associated with the effect.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="573af-141">**GetPool**</span><span class="sxs-lookup"><span data-stu-id="573af-141">**GetPool**</span></span>](id3dxeffect--getpool.md)                               | <span data-ttu-id="573af-142">Возвращает указатель на пул общих параметров.</span><span class="sxs-lookup"><span data-stu-id="573af-142">Gets a pointer to the pool of shared parameters.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="573af-143">**жетстатеманажер**</span><span class="sxs-lookup"><span data-stu-id="573af-143">**GetStateManager**</span></span>](id3dxeffect--getstatemanager.md)               | <span data-ttu-id="573af-144">Получение диспетчера состояний эффектов.</span><span class="sxs-lookup"><span data-stu-id="573af-144">Get the effect state manager.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="573af-145">**испараметерусед**</span><span class="sxs-lookup"><span data-stu-id="573af-145">**IsParameterUsed**</span></span>](id3dxeffect--isparameterused.md)               | <span data-ttu-id="573af-146">Определяет, используется ли параметр методом.</span><span class="sxs-lookup"><span data-stu-id="573af-146">Determines if a parameter is used by the technique.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="573af-147">**онлостдевице**</span><span class="sxs-lookup"><span data-stu-id="573af-147">**OnLostDevice**</span></span>](id3dxeffect--onlostdevice.md)                     | <span data-ttu-id="573af-148">Используйте этот метод, чтобы освободить все ссылки на ресурсы видеопамяти и удалить все статеблоккс.</span><span class="sxs-lookup"><span data-stu-id="573af-148">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="573af-149">Этот метод должен вызываться при каждом потере устройства или перед сбросом устройства.</span><span class="sxs-lookup"><span data-stu-id="573af-149">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="573af-150">**онресетдевице**</span><span class="sxs-lookup"><span data-stu-id="573af-150">**OnResetDevice**</span></span>](id3dxeffect--onresetdevice.md)                   | <span data-ttu-id="573af-151">Этот метод используется для повторного получения ресурсов и сохранения начального состояния.</span><span class="sxs-lookup"><span data-stu-id="573af-151">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="573af-152">**сетраввалуе**</span><span class="sxs-lookup"><span data-stu-id="573af-152">**SetRawValue**</span></span>](id3dxeffect--setrawvalue.md)                       | <span data-ttu-id="573af-153">Установка непрерывного диапазона констант шейдера с копированием в памяти.</span><span class="sxs-lookup"><span data-stu-id="573af-153">Set a contiguous range of shader constants with a memory copy.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="573af-154">**сетстатеманажер**</span><span class="sxs-lookup"><span data-stu-id="573af-154">**SetStateManager**</span></span>](id3dxeffect--setstatemanager.md)               | <span data-ttu-id="573af-155">Задайте диспетчер состояний эффектов.</span><span class="sxs-lookup"><span data-stu-id="573af-155">Set the effect state manager.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="573af-156">**сеттечникуе**</span><span class="sxs-lookup"><span data-stu-id="573af-156">**SetTechnique**</span></span>](id3dxeffect--settechnique.md)                     | <span data-ttu-id="573af-157">Задает активный метод.</span><span class="sxs-lookup"><span data-stu-id="573af-157">Sets the active technique.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="573af-158">**валидатетечникуе**</span><span class="sxs-lookup"><span data-stu-id="573af-158">**ValidateTechnique**</span></span>](id3dxeffect--validatetechnique.md)           | <span data-ttu-id="573af-159">Проверка метода.</span><span class="sxs-lookup"><span data-stu-id="573af-159">Validate a technique.</span></span><br/>                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="573af-160">Комментарии</span><span class="sxs-lookup"><span data-stu-id="573af-160">Remarks</span></span>

<span data-ttu-id="573af-161">Интерфейс ID3DXEffect получается путем вызова [**D3DXCreateEffect**](d3dxcreateeffect.md), [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)или [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md).</span><span class="sxs-lookup"><span data-stu-id="573af-161">The ID3DXEffect interface is obtained by calling [**D3DXCreateEffect**](d3dxcreateeffect.md), [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md), or [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md).</span></span>

<span data-ttu-id="573af-162">Тип LPD3DXEFFECT определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="573af-162">The LPD3DXEFFECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffect ID3DXEffect;
typedef interface ID3DXEffect *LPD3DXEFFECT;
```



## <a name="requirements"></a><span data-ttu-id="573af-163">Требования</span><span class="sxs-lookup"><span data-stu-id="573af-163">Requirements</span></span>



| <span data-ttu-id="573af-164">Требование</span><span class="sxs-lookup"><span data-stu-id="573af-164">Requirement</span></span> | <span data-ttu-id="573af-165">Значение</span><span class="sxs-lookup"><span data-stu-id="573af-165">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="573af-166">Header</span><span class="sxs-lookup"><span data-stu-id="573af-166">Header</span></span><br/>  | <dl> <span data-ttu-id="573af-167"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="573af-167"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="573af-168">Библиотека</span><span class="sxs-lookup"><span data-stu-id="573af-168">Library</span></span><br/> | <dl> <span data-ttu-id="573af-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="573af-169"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="573af-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="573af-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="573af-171">**ID3DXBaseEffect**</span><span class="sxs-lookup"><span data-stu-id="573af-171">**ID3DXBaseEffect**</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="573af-172">Интерфейсы эффектов</span><span class="sxs-lookup"><span data-stu-id="573af-172">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[<span data-ttu-id="573af-173">**D3DXCreateEffect**</span><span class="sxs-lookup"><span data-stu-id="573af-173">**D3DXCreateEffect**</span></span>](d3dxcreateeffect.md)
</dt> <dt>

[<span data-ttu-id="573af-174">**D3DXCreateEffectFromFile**</span><span class="sxs-lookup"><span data-stu-id="573af-174">**D3DXCreateEffectFromFile**</span></span>](d3dxcreateeffectfromfile.md)
</dt> <dt>

[<span data-ttu-id="573af-175">**D3DXCreateEffectFromResource**</span><span class="sxs-lookup"><span data-stu-id="573af-175">**D3DXCreateEffectFromResource**</span></span>](d3dxcreateeffectfromresource.md)
</dt> </dl>

 

 




