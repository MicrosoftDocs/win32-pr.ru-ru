---
description: Это реализованный пользователем интерфейс, позволяющий пользователю установить состояние устройства с самого влияния.
ms.assetid: ccd3e456-e27b-4128-b20b-99ff8dafcbe1
title: Интерфейс ID3DXEffectStateManager (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fad9df739634625800c0a21fd9ba2a2823d70f8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355230"
---
# <a name="id3dxeffectstatemanager-interface"></a><span data-ttu-id="cd265-103">Интерфейс ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="cd265-103">ID3DXEffectStateManager interface</span></span>

<span data-ttu-id="cd265-104">Это реализованный пользователем интерфейс, позволяющий пользователю установить состояние устройства с самого влияния.</span><span class="sxs-lookup"><span data-stu-id="cd265-104">This is a user-implemented interface that allows a user to set the device state from an effect.</span></span> <span data-ttu-id="cd265-105">Каждый из методов в этом интерфейсе должен быть реализован пользователем и использоваться в качестве обратных вызовов приложения при выполнении любого из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="cd265-105">Each of the methods in this interface must be implemented by the user and will then be used as callbacks to the application when either of the following occur:</span></span>

-   <span data-ttu-id="cd265-106">Воздействие вызывает [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="cd265-106">An effect calls [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="cd265-107">Состояние эффектов динамически обновляется путем вызова соответствующего API изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="cd265-107">Effect state is dynamically updated by calling the appropriate state change API.</span></span> <span data-ttu-id="cd265-108">Дополнительные сведения см. в разделе страницы отдельных методов.</span><span class="sxs-lookup"><span data-stu-id="cd265-108">See individual method pages for details.</span></span>

<span data-ttu-id="cd265-109">Если приложение использует диспетчер состояний для реализации пользовательских обратных вызовов, то при вызове [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md) и [**ID3DXEffect:: ендпасс**](id3dxeffect--endpass.md)происходит автоматическое сохранение и восстановление состояния.</span><span class="sxs-lookup"><span data-stu-id="cd265-109">When an application uses the state manager to implement custom callbacks, an effect no longer automatically saves and restores state when calling [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md).</span></span> <span data-ttu-id="cd265-110">Так как приложение реализует пользовательское поведение сохранения и восстановления в ответах, это автоматическое поведение обходится.</span><span class="sxs-lookup"><span data-stu-id="cd265-110">Because the application has implemented a custom save and restore behavior in the callbacks, this automatic behavior is bypassed.</span></span>

## <a name="members"></a><span data-ttu-id="cd265-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="cd265-111">Members</span></span>

<span data-ttu-id="cd265-112">Интерфейс **ID3DXEffectStateManager** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cd265-112">The **ID3DXEffectStateManager** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cd265-113">**ID3DXEffectStateManager** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cd265-113">**ID3DXEffectStateManager** also has these types of members:</span></span>

-   [<span data-ttu-id="cd265-114">Методы</span><span class="sxs-lookup"><span data-stu-id="cd265-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cd265-115">Методы</span><span class="sxs-lookup"><span data-stu-id="cd265-115">Methods</span></span>

<span data-ttu-id="cd265-116">Интерфейс **ID3DXEffectStateManager** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="cd265-116">The **ID3DXEffectStateManager** interface has these methods.</span></span>



| <span data-ttu-id="cd265-117">Метод</span><span class="sxs-lookup"><span data-stu-id="cd265-117">Method</span></span>                                                                                | <span data-ttu-id="cd265-118">Описание</span><span class="sxs-lookup"><span data-stu-id="cd265-118">Description</span></span>                                                                                                                  |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd265-119">**Досветлить**</span><span class="sxs-lookup"><span data-stu-id="cd265-119">**LightEnable**</span></span>](id3dxeffectstatemanager--lightenable.md)                           | <span data-ttu-id="cd265-120">Функция обратного вызова, которая должна быть реализована пользователем для включения или отключения освещения.</span><span class="sxs-lookup"><span data-stu-id="cd265-120">A callback function that must be implemented by a user to enable/disable a light.</span></span><br/>                                 |
| [<span data-ttu-id="cd265-121">**сетфвф**</span><span class="sxs-lookup"><span data-stu-id="cd265-121">**SetFVF**</span></span>](id3dxeffectstatemanager--setfvf.md)                                     | <span data-ttu-id="cd265-122">Функция обратного вызова, которая должна быть реализована пользователем для установки кода ФВФ.</span><span class="sxs-lookup"><span data-stu-id="cd265-122">A callback function that must be implemented by a user to set a FVF code.</span></span><br/>                                         |
| [<span data-ttu-id="cd265-123">**сетлигхт**</span><span class="sxs-lookup"><span data-stu-id="cd265-123">**SetLight**</span></span>](id3dxeffectstatemanager--setlight.md)                                 | <span data-ttu-id="cd265-124">Функция обратного вызова, которая должна быть реализована пользователем для установки освещения.</span><span class="sxs-lookup"><span data-stu-id="cd265-124">A callback function that must be implemented by a user to set a light.</span></span><br/>                                            |
| [<span data-ttu-id="cd265-125">**сетматериал**</span><span class="sxs-lookup"><span data-stu-id="cd265-125">**SetMaterial**</span></span>](id3dxeffectstatemanager--setmaterial.md)                           | <span data-ttu-id="cd265-126">Функция обратного вызова, которая должна быть реализована пользователем для задания состояния материала.</span><span class="sxs-lookup"><span data-stu-id="cd265-126">A callback function that must be implemented by a user to set material state.</span></span><br/>                                     |
| [<span data-ttu-id="cd265-127">**сетнпатчмоде**</span><span class="sxs-lookup"><span data-stu-id="cd265-127">**SetNPatchMode**</span></span>](id3dxeffectstatemanager--setnpatchmode.md)                       | <span data-ttu-id="cd265-128">Функция обратного вызова, которая должна быть реализована пользователем для задания числа сегментов подразделений для N-патчей.</span><span class="sxs-lookup"><span data-stu-id="cd265-128">A callback function that must be implemented by a user to set the number of subdivision segments for N-patches.</span></span><br/>   |
| [<span data-ttu-id="cd265-129">**сетпикселшадер**</span><span class="sxs-lookup"><span data-stu-id="cd265-129">**SetPixelShader**</span></span>](id3dxeffectstatemanager--setpixelshader.md)                     | <span data-ttu-id="cd265-130">Функция обратного вызова, которая должна быть реализована пользователем для задания шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="cd265-130">A callback function that must be implemented by a user to set a pixel shader.</span></span><br/>                                     |
| [<span data-ttu-id="cd265-131">**сетпикселшадерконстантб**</span><span class="sxs-lookup"><span data-stu-id="cd265-131">**SetPixelShaderConstantB**</span></span>](id3dxeffectstatemanager--setpixelshaderconstantb.md)   | <span data-ttu-id="cd265-132">Функция обратного вызова, которая должна быть реализована пользователем для задания массива логических констант шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="cd265-132">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span><br/>        |
| [<span data-ttu-id="cd265-133">**сетпикселшадерконстантф**</span><span class="sxs-lookup"><span data-stu-id="cd265-133">**SetPixelShaderConstantF**</span></span>](id3dxeffectstatemanager--setpixelshaderconstantf.md)   | <span data-ttu-id="cd265-134">Функция обратного вызова, которая должна быть реализована пользователем для установки массива констант с плавающей точкой шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="cd265-134">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span><br/> |
| [<span data-ttu-id="cd265-135">**сетпикселшадерконстанти**</span><span class="sxs-lookup"><span data-stu-id="cd265-135">**SetPixelShaderConstantI**</span></span>](id3dxeffectstatemanager--setpixelshaderconstanti.md)   | <span data-ttu-id="cd265-136">Функция обратного вызова, которая должна быть реализована пользователем для задания массива целочисленных констант шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="cd265-136">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span><br/>        |
| [<span data-ttu-id="cd265-137">**сетрендерстате**</span><span class="sxs-lookup"><span data-stu-id="cd265-137">**SetRenderState**</span></span>](id3dxeffectstatemanager--setrenderstate.md)                     | <span data-ttu-id="cd265-138">Функция обратного вызова, которая должна быть реализована пользователем для установки состояния отрисовки.</span><span class="sxs-lookup"><span data-stu-id="cd265-138">A callback function that must be implemented by a user to set render state.</span></span><br/>                                       |
| [<span data-ttu-id="cd265-139">**сетсамплерстате**</span><span class="sxs-lookup"><span data-stu-id="cd265-139">**SetSamplerState**</span></span>](id3dxeffectstatemanager--setsamplerstate.md)                   | <span data-ttu-id="cd265-140">Функция обратного вызова, которая должна быть реализована пользователем для установки образца.</span><span class="sxs-lookup"><span data-stu-id="cd265-140">A callback function that must be implemented by a user to set a sampler.</span></span><br/>                                          |
| [<span data-ttu-id="cd265-141">**сеттекстуре**</span><span class="sxs-lookup"><span data-stu-id="cd265-141">**SetTexture**</span></span>](id3dxeffectstatemanager--settexture.md)                             | <span data-ttu-id="cd265-142">Функция обратного вызова, которая должна быть реализована пользователем для установки текстуры.</span><span class="sxs-lookup"><span data-stu-id="cd265-142">A callback function that must be implemented by a user to set a texture.</span></span><br/>                                          |
| [<span data-ttu-id="cd265-143">**сеттекстурестажестате**</span><span class="sxs-lookup"><span data-stu-id="cd265-143">**SetTextureStageState**</span></span>](id3dxeffectstatemanager--settexturestagestate.md)         | <span data-ttu-id="cd265-144">Функция обратного вызова, которая должна быть реализована пользователем для установки состояния стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="cd265-144">A callback function that must be implemented by a user to set the texture stage state.</span></span><br/>                            |
| [<span data-ttu-id="cd265-145">**сеттрансформ**</span><span class="sxs-lookup"><span data-stu-id="cd265-145">**SetTransform**</span></span>](id3dxeffectstatemanager--settransform.md)                         | <span data-ttu-id="cd265-146">Функция обратного вызова, которая должна быть реализована пользователем для установки преобразования.</span><span class="sxs-lookup"><span data-stu-id="cd265-146">A callback function that must be implemented by a user to set a transform.</span></span><br/>                                        |
| [<span data-ttu-id="cd265-147">**сетвертексшадер**</span><span class="sxs-lookup"><span data-stu-id="cd265-147">**SetVertexShader**</span></span>](id3dxeffectstatemanager--setvertexshader.md)                   | <span data-ttu-id="cd265-148">Функция обратного вызова, которая должна быть реализована пользователем для задания шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="cd265-148">A callback function that must be implemented by a user to set a vertex shader.</span></span><br/>                                    |
| [<span data-ttu-id="cd265-149">**сетвертексшадерконстантб**</span><span class="sxs-lookup"><span data-stu-id="cd265-149">**SetVertexShaderConstantB**</span></span>](id3dxeffectstatemanager--setvertexshaderconstantb.md) | <span data-ttu-id="cd265-150">Функция обратного вызова, которая должна быть реализована пользователем для задания массива логических констант шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="cd265-150">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span><br/>        |
| [<span data-ttu-id="cd265-151">**сетвертексшадерконстантф**</span><span class="sxs-lookup"><span data-stu-id="cd265-151">**SetVertexShaderConstantF**</span></span>](id3dxeffectstatemanager--setvertexshaderconstantf.md) | <span data-ttu-id="cd265-152">Функция обратного вызова, которая должна быть реализована пользователем для установки массива констант с плавающей точкой шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="cd265-152">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span><br/> |
| [<span data-ttu-id="cd265-153">**сетвертексшадерконстанти**</span><span class="sxs-lookup"><span data-stu-id="cd265-153">**SetVertexShaderConstantI**</span></span>](id3dxeffectstatemanager--setvertexshaderconstanti.md) | <span data-ttu-id="cd265-154">Функция обратного вызова, которая должна быть реализована пользователем для задания массива целочисленных констант шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="cd265-154">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="cd265-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd265-155">Remarks</span></span>

<span data-ttu-id="cd265-156">Пользователь создает интерфейс ID3DXEffectStateManager, реализуя класс, производный от этого интерфейса, и реализуя все методы интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cd265-156">A user creates an ID3DXEffectStateManager interface by implementing a class that derives from this interface, and implementing all the interface methods.</span></span> <span data-ttu-id="cd265-157">После создания интерфейса можно получить или задать диспетчер состояний в рамках действия с помощью [**ID3DXEffect:: жетстатеманажер**](id3dxeffect--getstatemanager.md) и [**ID3DXEffect:: сетстатеманажер**](id3dxeffect--setstatemanager.md).</span><span class="sxs-lookup"><span data-stu-id="cd265-157">Once the interface is created, you can get or set the state manager within an effect using [**ID3DXEffect::GetStateManager**](id3dxeffect--getstatemanager.md) and [**ID3DXEffect::SetStateManager**](id3dxeffect--setstatemanager.md).</span></span>

<span data-ttu-id="cd265-158">Тип LPD3DXEFFECTSTATEMANAGER определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="cd265-158">The LPD3DXEFFECTSTATEMANAGER type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffectStateManager ID3DXEffectStateManager;
typedef interface ID3DXEffectStateManager *LPD3DXEFFECTSTATEMANAGER;
```



## <a name="requirements"></a><span data-ttu-id="cd265-159">Требования</span><span class="sxs-lookup"><span data-stu-id="cd265-159">Requirements</span></span>



| <span data-ttu-id="cd265-160">Требование</span><span class="sxs-lookup"><span data-stu-id="cd265-160">Requirement</span></span> | <span data-ttu-id="cd265-161">Значение</span><span class="sxs-lookup"><span data-stu-id="cd265-161">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd265-162">Header</span><span class="sxs-lookup"><span data-stu-id="cd265-162">Header</span></span><br/>  | <dl> <span data-ttu-id="cd265-163"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd265-163"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="cd265-164">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cd265-164">Library</span></span><br/> | <dl> <span data-ttu-id="cd265-165"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd265-165"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cd265-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd265-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd265-167">Интерфейсы эффектов</span><span class="sxs-lookup"><span data-stu-id="cd265-167">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
