---
description: Интерфейс ID3DXRenderToSurface используется для обобщения процесса отрисовки на поверхности.
ms.assetid: e9f2ca5e-faa3-45a8-94eb-16f354618e80
title: Интерфейс ID3DXRenderToSurface (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 577e729e4e1a510dd24dc981b2b90bdca27dc0f9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355823"
---
# <a name="id3dxrendertosurface-interface"></a><span data-ttu-id="9eb5e-103">Интерфейс ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="9eb5e-103">ID3DXRenderToSurface interface</span></span>

<span data-ttu-id="9eb5e-104">Интерфейс ID3DXRenderToSurface используется для обобщения процесса отрисовки на поверхности.</span><span class="sxs-lookup"><span data-stu-id="9eb5e-104">The ID3DXRenderToSurface interface is used to generalize the process of rendering to surfaces.</span></span>

## <a name="members"></a><span data-ttu-id="9eb5e-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="9eb5e-105">Members</span></span>

<span data-ttu-id="9eb5e-106">Интерфейс **ID3DXRenderToSurface** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9eb5e-106">The **ID3DXRenderToSurface** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9eb5e-107">**ID3DXRenderToSurface** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9eb5e-107">**ID3DXRenderToSurface** also has these types of members:</span></span>

-   [<span data-ttu-id="9eb5e-108">Методы</span><span class="sxs-lookup"><span data-stu-id="9eb5e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9eb5e-109">Методы</span><span class="sxs-lookup"><span data-stu-id="9eb5e-109">Methods</span></span>

<span data-ttu-id="9eb5e-110">Интерфейс **ID3DXRenderToSurface** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9eb5e-110">The **ID3DXRenderToSurface** interface has these methods.</span></span>



| <span data-ttu-id="9eb5e-111">Метод</span><span class="sxs-lookup"><span data-stu-id="9eb5e-111">Method</span></span>                                                       | <span data-ttu-id="9eb5e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="9eb5e-112">Description</span></span>                                                                                                                                                                                     |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9eb5e-113">**бегинсцене**</span><span class="sxs-lookup"><span data-stu-id="9eb5e-113">**BeginScene**</span></span>](id3dxrendertosurface--beginscene.md)       | <span data-ttu-id="9eb5e-114">Начинает сцену.</span><span class="sxs-lookup"><span data-stu-id="9eb5e-114">Begins a scene.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="9eb5e-115">**ендсцене**</span><span class="sxs-lookup"><span data-stu-id="9eb5e-115">**EndScene**</span></span>](id3dxrendertosurface--endscene.md)           | <span data-ttu-id="9eb5e-116">Завершает сцену.</span><span class="sxs-lookup"><span data-stu-id="9eb5e-116">Ends a scene.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="9eb5e-117">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="9eb5e-117">**GetDesc**</span></span>](id3dxrendertosurface--getdesc.md)             | <span data-ttu-id="9eb5e-118">Извлекает параметры поверхности рендеринга.</span><span class="sxs-lookup"><span data-stu-id="9eb5e-118">Retrieves the parameters of the render surface.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="9eb5e-119">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="9eb5e-119">**GetDevice**</span></span>](id3dxrendertosurface--getdevice.md)         | <span data-ttu-id="9eb5e-120">Извлекает устройство Direct3D, связанное с областью прорисовки.</span><span class="sxs-lookup"><span data-stu-id="9eb5e-120">Retrieves the Direct3D device associated with the render surface.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="9eb5e-121">**онлостдевице**</span><span class="sxs-lookup"><span data-stu-id="9eb5e-121">**OnLostDevice**</span></span>](id3dxrendertosurface--onlostdevice.md)   | <span data-ttu-id="9eb5e-122">Используйте этот метод, чтобы освободить все ссылки на ресурсы видеопамяти и удалить все статеблоккс.</span><span class="sxs-lookup"><span data-stu-id="9eb5e-122">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="9eb5e-123">Этот метод должен вызываться при каждом потере устройства или перед сбросом устройства.</span><span class="sxs-lookup"><span data-stu-id="9eb5e-123">This method should be called whenever a device is lost or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="9eb5e-124">**онресетдевице**</span><span class="sxs-lookup"><span data-stu-id="9eb5e-124">**OnResetDevice**</span></span>](id3dxrendertosurface--onresetdevice.md) | <span data-ttu-id="9eb5e-125">Этот метод используется для повторного получения ресурсов и сохранения начального состояния.</span><span class="sxs-lookup"><span data-stu-id="9eb5e-125">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="9eb5e-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9eb5e-126">Remarks</span></span>

<span data-ttu-id="9eb5e-127">Поверхности могут использоваться различными способами, включая цели рендеринга, отрисовку на экране или отрисовку текстур.</span><span class="sxs-lookup"><span data-stu-id="9eb5e-127">Surfaces can be used in a variety of ways including render targets, off-screen rendering, or rendering to textures.</span></span>

<span data-ttu-id="9eb5e-128">Поверхность можно настроить с помощью отдельного окна просмотра с помощью метода [**ID3DXRenderToSurface:: бегинсцене**](id3dxrendertosurface--beginscene.md) , чтобы предоставить пользовательское представление отрисовки.</span><span class="sxs-lookup"><span data-stu-id="9eb5e-128">A surface can be configured using a separate viewport using the [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md) method, to provide a custom render view.</span></span> <span data-ttu-id="9eb5e-129">Если поверхность не является целевым объектом отрисовки, используется совместимый целевой объект рендеринга, и результат копируется в область в конце сцены.</span><span class="sxs-lookup"><span data-stu-id="9eb5e-129">If the surface is not a render target, a compatible render target is used, and the result is copied to the surface at the end of the scene.</span></span>

<span data-ttu-id="9eb5e-130">Интерфейс **ID3DXRenderToSurface** получается путем вызова функции [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md) .</span><span class="sxs-lookup"><span data-stu-id="9eb5e-130">The **ID3DXRenderToSurface** interface is obtained by calling the [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md) function.</span></span>

<span data-ttu-id="9eb5e-131">Тип LPD3DXRENDERTOSURFACE определяется как указатель на интерфейс **ID3DXRenderToSurface** .</span><span class="sxs-lookup"><span data-stu-id="9eb5e-131">The LPD3DXRENDERTOSURFACE type is defined as a pointer to the **ID3DXRenderToSurface** interface.</span></span>


```
typedef interface ID3DXRenderToSurface ID3DXRenderToSurface;
typedef interface ID3DXRenderToSurface *LPD3DXRENDERTOSURFACE;
```



## <a name="requirements"></a><span data-ttu-id="9eb5e-132">Требования</span><span class="sxs-lookup"><span data-stu-id="9eb5e-132">Requirements</span></span>



| <span data-ttu-id="9eb5e-133">Требование</span><span class="sxs-lookup"><span data-stu-id="9eb5e-133">Requirement</span></span> | <span data-ttu-id="9eb5e-134">Значение</span><span class="sxs-lookup"><span data-stu-id="9eb5e-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb5e-135">Header</span><span class="sxs-lookup"><span data-stu-id="9eb5e-135">Header</span></span><br/>  | <dl> <span data-ttu-id="9eb5e-136"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eb5e-136"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="9eb5e-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9eb5e-137">Library</span></span><br/> | <dl> <span data-ttu-id="9eb5e-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9eb5e-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9eb5e-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9eb5e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eb5e-140">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="9eb5e-140">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
