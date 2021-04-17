---
description: Интерфейс ID3DXRenderToEnvMap используется для подготовки процесса визуализации к картам среды.
ms.assetid: d72db260-5493-4381-9269-521ad333f0b2
title: Интерфейс ID3DXRenderToEnvMap (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c3fdfc37c206b6360fc0b7296bbf90c319652e28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647886"
---
# <a name="id3dxrendertoenvmap-interface"></a><span data-ttu-id="dccc2-103">Интерфейс ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="dccc2-103">ID3DXRenderToEnvMap interface</span></span>

<span data-ttu-id="dccc2-104">Интерфейс ID3DXRenderToEnvMap используется для подготовки процесса визуализации к картам среды.</span><span class="sxs-lookup"><span data-stu-id="dccc2-104">The ID3DXRenderToEnvMap interface is used to generalize the process of rendering to environment maps.</span></span>

## <a name="members"></a><span data-ttu-id="dccc2-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="dccc2-105">Members</span></span>

<span data-ttu-id="dccc2-106">Интерфейс **ID3DXRenderToEnvMap** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dccc2-106">The **ID3DXRenderToEnvMap** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dccc2-107">**ID3DXRenderToEnvMap** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dccc2-107">**ID3DXRenderToEnvMap** also has these types of members:</span></span>

-   [<span data-ttu-id="dccc2-108">Методы</span><span class="sxs-lookup"><span data-stu-id="dccc2-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dccc2-109">Методы</span><span class="sxs-lookup"><span data-stu-id="dccc2-109">Methods</span></span>

<span data-ttu-id="dccc2-110">Интерфейс **ID3DXRenderToEnvMap** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="dccc2-110">The **ID3DXRenderToEnvMap** interface has these methods.</span></span>



| <span data-ttu-id="dccc2-111">Метод</span><span class="sxs-lookup"><span data-stu-id="dccc2-111">Method</span></span>                                                          | <span data-ttu-id="dccc2-112">Описание</span><span class="sxs-lookup"><span data-stu-id="dccc2-112">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dccc2-113">**бегинкубе**</span><span class="sxs-lookup"><span data-stu-id="dccc2-113">**BeginCube**</span></span>](id3dxrendertoenvmap--begincube.md)             | <span data-ttu-id="dccc2-114">Инициация отрисовки схемы кубической среды.</span><span class="sxs-lookup"><span data-stu-id="dccc2-114">Initiate the rendering of a cubic environment map.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="dccc2-115">**бегинхемисфере**</span><span class="sxs-lookup"><span data-stu-id="dccc2-115">**BeginHemisphere**</span></span>](id3dxrendertoenvmap--beginhemisphere.md) | <span data-ttu-id="dccc2-116">Инициация отрисовки схемы среды хемисферик.</span><span class="sxs-lookup"><span data-stu-id="dccc2-116">Initiate the rendering of a hemispheric environment map.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="dccc2-117">**бегинпараболик**</span><span class="sxs-lookup"><span data-stu-id="dccc2-117">**BeginParabolic**</span></span>](id3dxrendertoenvmap--beginparabolic.md)   | <span data-ttu-id="dccc2-118">Инициация отрисовки схемы среды параболическим.</span><span class="sxs-lookup"><span data-stu-id="dccc2-118">Initiate the rendering of a parabolic environment map.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="dccc2-119">**бегинсфере**</span><span class="sxs-lookup"><span data-stu-id="dccc2-119">**BeginSphere**</span></span>](id3dxrendertoenvmap--beginsphere.md)         | <span data-ttu-id="dccc2-120">Инициация отрисовки сферической схемы среды.</span><span class="sxs-lookup"><span data-stu-id="dccc2-120">Initiate the rendering of a spherical environment map.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="dccc2-121">**END**</span><span class="sxs-lookup"><span data-stu-id="dccc2-121">**End**</span></span>](id3dxrendertoenvmap--end.md)                         | <span data-ttu-id="dccc2-122">Восстановите все целевые объекты отрисовки и при необходимости сформируйте все отрисованные лица в области схемы среды.</span><span class="sxs-lookup"><span data-stu-id="dccc2-122">Restore all render targets and, if needed, compose all the rendered faces into the environment map surface.</span></span><br/>                                                                           |
| [<span data-ttu-id="dccc2-123">**Распознавание лиц**</span><span class="sxs-lookup"><span data-stu-id="dccc2-123">**Face**</span></span>](id3dxrendertoenvmap--face.md)                       | <span data-ttu-id="dccc2-124">Инициирует рисование каждой грани схемы среды.</span><span class="sxs-lookup"><span data-stu-id="dccc2-124">Initiate the drawing of each face of an environment map.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="dccc2-125">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="dccc2-125">**GetDesc**</span></span>](id3dxrendertoenvmap--getdesc.md)                 | <span data-ttu-id="dccc2-126">Извлекает описание поверхности рендеринга.</span><span class="sxs-lookup"><span data-stu-id="dccc2-126">Retrieves the description of the render surface.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="dccc2-127">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="dccc2-127">**GetDevice**</span></span>](id3dxrendertoenvmap--getdevice.md)             | <span data-ttu-id="dccc2-128">Извлекает устройство Direct3D, связанное с картой среды.</span><span class="sxs-lookup"><span data-stu-id="dccc2-128">Retrieves the Direct3D device associated with the environment map.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="dccc2-129">**онлостдевице**</span><span class="sxs-lookup"><span data-stu-id="dccc2-129">**OnLostDevice**</span></span>](id3dxrendertoenvmap--onlostdevice.md)       | <span data-ttu-id="dccc2-130">Используйте этот метод, чтобы освободить все ссылки на ресурсы видеопамяти и удалить все статеблоккс.</span><span class="sxs-lookup"><span data-stu-id="dccc2-130">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="dccc2-131">Этот метод должен вызываться при каждом потере устройства или перед сбросом устройства.</span><span class="sxs-lookup"><span data-stu-id="dccc2-131">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="dccc2-132">**онресетдевице**</span><span class="sxs-lookup"><span data-stu-id="dccc2-132">**OnResetDevice**</span></span>](id3dxrendertoenvmap--onresetdevice.md)     | <span data-ttu-id="dccc2-133">Этот метод используется для повторного получения ресурсов и сохранения начального состояния.</span><span class="sxs-lookup"><span data-stu-id="dccc2-133">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="dccc2-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dccc2-134">Remarks</span></span>

<span data-ttu-id="dccc2-135">Схема окружения используется для создания геометрии текстурной схемы, чтобы обеспечить более сложную сцену без использования сложной геометрии.</span><span class="sxs-lookup"><span data-stu-id="dccc2-135">An environment map is used to texture-map scene geometry to provide a more sophisticated scene without using complex geometry.</span></span> <span data-ttu-id="dccc2-136">Этот интерфейс поддерживает создание поверхностей для следующих видов геометрии: Cube, 1/2 Sphere или хемисферик, параболическим или Sphere.</span><span class="sxs-lookup"><span data-stu-id="dccc2-136">This interface supports creating surfaces for the following kinds of geometry: cube, half sphere or hemispheric, parabolic, or sphere.</span></span>

<span data-ttu-id="dccc2-137">Интерфейс **ID3DXRenderToEnvMap** получается путем вызова функции [**D3DXCreateRenderToEnvMap**](d3dxcreaterendertoenvmap.md) .</span><span class="sxs-lookup"><span data-stu-id="dccc2-137">The **ID3DXRenderToEnvMap** interface is obtained by calling the [**D3DXCreateRenderToEnvMap**](d3dxcreaterendertoenvmap.md) function.</span></span>

<span data-ttu-id="dccc2-138">Тип LPD3DXRenderToEnvMap определяется как указатель на интерфейс **ID3DXRenderToEnvMap** .</span><span class="sxs-lookup"><span data-stu-id="dccc2-138">The LPD3DXRenderToEnvMap type is defined as a pointer to the **ID3DXRenderToEnvMap** interface.</span></span>


```
typedef interface ID3DXRenderToEnvMap ID3DXRenderToEnvMap;
typedef interface ID3DXRenderToEnvMap *LPD3DXRenderToEnvMap;
```



## <a name="requirements"></a><span data-ttu-id="dccc2-139">Требования</span><span class="sxs-lookup"><span data-stu-id="dccc2-139">Requirements</span></span>



| <span data-ttu-id="dccc2-140">Требование</span><span class="sxs-lookup"><span data-stu-id="dccc2-140">Requirement</span></span> | <span data-ttu-id="dccc2-141">Значение</span><span class="sxs-lookup"><span data-stu-id="dccc2-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dccc2-142">Header</span><span class="sxs-lookup"><span data-stu-id="dccc2-142">Header</span></span><br/>  | <dl> <span data-ttu-id="dccc2-143"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="dccc2-143"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="dccc2-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dccc2-144">Library</span></span><br/> | <dl> <span data-ttu-id="dccc2-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dccc2-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dccc2-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dccc2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dccc2-147">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="dccc2-147">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
