---
description: Интерфейс ID3DXLine реализует рисование линий с помощью текстурированных треугольников.
ms.assetid: 87472618-d3e4-4008-9009-ae17fc7b696d
title: Интерфейс ID3DXLine (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c535ff736e9a26e8316e4715f4be4022a6417df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081954"
---
# <a name="id3dxline-interface"></a><span data-ttu-id="085f3-103">Интерфейс ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="085f3-103">ID3DXLine interface</span></span>

<span data-ttu-id="085f3-104">Интерфейс ID3DXLine реализует рисование линий с помощью текстурированных треугольников.</span><span class="sxs-lookup"><span data-stu-id="085f3-104">The ID3DXLine interface implements line drawing using textured triangles.</span></span>

## <a name="members"></a><span data-ttu-id="085f3-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="085f3-105">Members</span></span>

<span data-ttu-id="085f3-106">Интерфейс **ID3DXLine** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="085f3-106">The **ID3DXLine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="085f3-107">**ID3DXLine** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="085f3-107">**ID3DXLine** also has these types of members:</span></span>

-   [<span data-ttu-id="085f3-108">Методы</span><span class="sxs-lookup"><span data-stu-id="085f3-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="085f3-109">Методы</span><span class="sxs-lookup"><span data-stu-id="085f3-109">Methods</span></span>

<span data-ttu-id="085f3-110">Интерфейс **ID3DXLine** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="085f3-110">The **ID3DXLine** interface has these methods.</span></span>



| <span data-ttu-id="085f3-111">Метод</span><span class="sxs-lookup"><span data-stu-id="085f3-111">Method</span></span>                                                | <span data-ttu-id="085f3-112">Описание</span><span class="sxs-lookup"><span data-stu-id="085f3-112">Description</span></span>                                                                                                                                                                                      |
|:------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="085f3-113">**Начать**</span><span class="sxs-lookup"><span data-stu-id="085f3-113">**Begin**</span></span>](id3dxline--begin.md)                     | <span data-ttu-id="085f3-114">Подготавливает устройство для рисования линий.</span><span class="sxs-lookup"><span data-stu-id="085f3-114">Prepares a device for drawing lines.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="085f3-115">**Draw**</span><span class="sxs-lookup"><span data-stu-id="085f3-115">**Draw**</span></span>](id3dxline--draw.md)                       | <span data-ttu-id="085f3-116">Рисует полосу линий в пространстве экрана.</span><span class="sxs-lookup"><span data-stu-id="085f3-116">Draws a line strip in screen space.</span></span> <span data-ttu-id="085f3-117">Входные данные указываются в виде массива, определяющего точки (of [**D3DXVECTOR2**](d3dxvector2.md)) на полосе строк.</span><span class="sxs-lookup"><span data-stu-id="085f3-117">Input is in the form of an array that defines points (of [**D3DXVECTOR2**](d3dxvector2.md)) on the line strip.</span></span><br/>                                   |
| [<span data-ttu-id="085f3-118">**дравтрансформ**</span><span class="sxs-lookup"><span data-stu-id="085f3-118">**DrawTransform**</span></span>](id3dxline--drawtransform.md)     | <span data-ttu-id="085f3-119">Рисует полосу линий в пространстве экрана с заданной матрицей преобразования входных данных.</span><span class="sxs-lookup"><span data-stu-id="085f3-119">Draws a line strip in screen space with a specified input transformation matrix.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="085f3-120">**END**</span><span class="sxs-lookup"><span data-stu-id="085f3-120">**End**</span></span>](id3dxline--end.md)                         | <span data-ttu-id="085f3-121">Восстанавливает состояние устройства в том виде, в котором оно было при вызове [**ID3DXLine:: Begin**](id3dxline--begin.md) .</span><span class="sxs-lookup"><span data-stu-id="085f3-121">Restores the device state to how it was when [**ID3DXLine::Begin**](id3dxline--begin.md) was called.</span></span><br/>                                                                                 |
| [<span data-ttu-id="085f3-122">**жетантиалиас**</span><span class="sxs-lookup"><span data-stu-id="085f3-122">**GetAntialias**</span></span>](id3dxline--getantialias.md)       | <span data-ttu-id="085f3-123">Возвращает состояние сглаживания линии.</span><span class="sxs-lookup"><span data-stu-id="085f3-123">Gets the line antialiasing state.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="085f3-124">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="085f3-124">**GetDevice**</span></span>](id3dxline--getdevice.md)             | <span data-ttu-id="085f3-125">Извлекает устройство Direct3D, связанное с объектом Line.</span><span class="sxs-lookup"><span data-stu-id="085f3-125">Retrieves the Direct3D device associated with the line object.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="085f3-126">**жетгллинес**</span><span class="sxs-lookup"><span data-stu-id="085f3-126">**GetGLLines**</span></span>](id3dxline--getgllines.md)           | <span data-ttu-id="085f3-127">Возвращает режим отображения линий в стиле OpenGL.</span><span class="sxs-lookup"><span data-stu-id="085f3-127">Gets the OpenGL-style line-drawing mode.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="085f3-128">**GetPattern**</span><span class="sxs-lookup"><span data-stu-id="085f3-128">**GetPattern**</span></span>](id3dxline--getpattern.md)           | <span data-ttu-id="085f3-129">Возвращает шаблон линии стиппле.</span><span class="sxs-lookup"><span data-stu-id="085f3-129">Gets the line stipple pattern.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="085f3-130">**жетпаттернскале**</span><span class="sxs-lookup"><span data-stu-id="085f3-130">**GetPatternScale**</span></span>](id3dxline--getpatternscale.md) | <span data-ttu-id="085f3-131">Возвращает значение масштаба стиппле-pattern.</span><span class="sxs-lookup"><span data-stu-id="085f3-131">Gets the stipple-pattern scale value.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="085f3-132">**Полуширинные**</span><span class="sxs-lookup"><span data-stu-id="085f3-132">**GetWidth**</span></span>](id3dxline--getwidth.md)               | <span data-ttu-id="085f3-133">Возвращает толщину линии.</span><span class="sxs-lookup"><span data-stu-id="085f3-133">Gets the thickness of the line.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="085f3-134">**онлостдевице**</span><span class="sxs-lookup"><span data-stu-id="085f3-134">**OnLostDevice**</span></span>](id3dxline--onlostdevice.md)       | <span data-ttu-id="085f3-135">Используйте этот метод, чтобы освободить все ссылки на ресурсы видеопамяти и удалить все статеблоккс.</span><span class="sxs-lookup"><span data-stu-id="085f3-135">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="085f3-136">Этот метод должен вызываться при каждом потере устройства или перед сбросом устройства.</span><span class="sxs-lookup"><span data-stu-id="085f3-136">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="085f3-137">**онресетдевице**</span><span class="sxs-lookup"><span data-stu-id="085f3-137">**OnResetDevice**</span></span>](id3dxline--onresetdevice.md)     | <span data-ttu-id="085f3-138">Этот метод используется для повторного получения ресурсов и сохранения начального состояния.</span><span class="sxs-lookup"><span data-stu-id="085f3-138">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="085f3-139">**сетантиалиас**</span><span class="sxs-lookup"><span data-stu-id="085f3-139">**SetAntialias**</span></span>](id3dxline--setantialias.md)       | <span data-ttu-id="085f3-140">Переключает Сглаживание линии.</span><span class="sxs-lookup"><span data-stu-id="085f3-140">Toggles line antialiasing.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="085f3-141">**сетгллинес**</span><span class="sxs-lookup"><span data-stu-id="085f3-141">**SetGLLines**</span></span>](id3dxline--setgllines.md)           | <span data-ttu-id="085f3-142">Переключает режим для отображения линий в стиле OpenGL.</span><span class="sxs-lookup"><span data-stu-id="085f3-142">Toggles the mode to draw OpenGL-style lines.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="085f3-143">**сетпаттерн**</span><span class="sxs-lookup"><span data-stu-id="085f3-143">**SetPattern**</span></span>](id3dxline--setpattern.md)           | <span data-ttu-id="085f3-144">Применяет к строке шаблон стиппле.</span><span class="sxs-lookup"><span data-stu-id="085f3-144">Applies a stipple pattern to the line.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="085f3-145">**сетпаттернскале**</span><span class="sxs-lookup"><span data-stu-id="085f3-145">**SetPatternScale**</span></span>](id3dxline--setpatternscale.md) | <span data-ttu-id="085f3-146">Растягивает шаблон стиппле вдоль направления линии.</span><span class="sxs-lookup"><span data-stu-id="085f3-146">Stretches the stipple pattern along the line direction.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="085f3-147">**сетвидс**</span><span class="sxs-lookup"><span data-stu-id="085f3-147">**SetWidth**</span></span>](id3dxline--setwidth.md)               | <span data-ttu-id="085f3-148">Задает толщину линии.</span><span class="sxs-lookup"><span data-stu-id="085f3-148">Specifies the thickness of the line.</span></span><br/>                                                                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="085f3-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="085f3-149">Remarks</span></span>

<span data-ttu-id="085f3-150">Создайте объект рисования линий с помощью [**D3DXCreateLine**](d3dxcreateline.md).</span><span class="sxs-lookup"><span data-stu-id="085f3-150">Create a line drawing object with [**D3DXCreateLine**](d3dxcreateline.md).</span></span>

<span data-ttu-id="085f3-151">Тип LPD3DXLINE определяется как указатель на интерфейс **ID3DXLine** .</span><span class="sxs-lookup"><span data-stu-id="085f3-151">The LPD3DXLINE type is defined as a pointer to the **ID3DXLine** interface.</span></span>


```
typedef interface ID3DXLine ID3DXLine;
typedef interface ID3DXLine *LPD3DXLINE;
```



## <a name="requirements"></a><span data-ttu-id="085f3-152">Требования</span><span class="sxs-lookup"><span data-stu-id="085f3-152">Requirements</span></span>



| <span data-ttu-id="085f3-153">Требование</span><span class="sxs-lookup"><span data-stu-id="085f3-153">Requirement</span></span> | <span data-ttu-id="085f3-154">Значение</span><span class="sxs-lookup"><span data-stu-id="085f3-154">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="085f3-155">Header</span><span class="sxs-lookup"><span data-stu-id="085f3-155">Header</span></span><br/>  | <dl> <span data-ttu-id="085f3-156"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="085f3-156"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="085f3-157">Библиотека</span><span class="sxs-lookup"><span data-stu-id="085f3-157">Library</span></span><br/> | <dl> <span data-ttu-id="085f3-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="085f3-158"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="085f3-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="085f3-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="085f3-160">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="085f3-160">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
