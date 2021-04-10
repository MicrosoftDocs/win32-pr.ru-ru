---
description: Представляет Управление сопоставлениями от рукописного ввода к окну отображения. Используйте объект Инкрендерер для вывода рукописного ввода в окне. Его также можно использовать для изменения расположения и изменения размера штриха.
ms.assetid: 66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7
title: Класс Инкрендерер (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRenderer
- InkRenderer.IInkRenderer
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 5d29448e2f8ae98c4e15d6c3a51747257d20c62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272841"
---
# <a name="inkrenderer-class"></a><span data-ttu-id="f02a6-105">Класс Инкрендерер</span><span class="sxs-lookup"><span data-stu-id="f02a6-105">InkRenderer class</span></span>

<span data-ttu-id="f02a6-106">Представляет Управление сопоставлениями от рукописного ввода к окну отображения.</span><span class="sxs-lookup"><span data-stu-id="f02a6-106">Represents the management of mappings from ink to the display window.</span></span> <span data-ttu-id="f02a6-107">Используйте объект **инкрендерер** для вывода рукописного ввода в окне.</span><span class="sxs-lookup"><span data-stu-id="f02a6-107">Use the **InkRenderer** object to display ink in a window.</span></span> <span data-ttu-id="f02a6-108">Его также можно использовать для изменения расположения и изменения размера штриха.</span><span class="sxs-lookup"><span data-stu-id="f02a6-108">You can also use it to reposition and resize stroke.</span></span>

<span data-ttu-id="f02a6-109">**Инкрендерер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f02a6-109">**InkRenderer** has these types of members:</span></span>

-   [<span data-ttu-id="f02a6-110">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="f02a6-110">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="f02a6-111">Методы</span><span class="sxs-lookup"><span data-stu-id="f02a6-111">Methods</span></span>](#methods)

### <a name="interfaces"></a><span data-ttu-id="f02a6-112">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="f02a6-112">Interfaces</span></span>

<span data-ttu-id="f02a6-113">Класс **инкрендерер** определяет эти интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="f02a6-113">The **InkRenderer** class defines these interfaces.</span></span>



| <span data-ttu-id="f02a6-114">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="f02a6-114">Interface</span></span>        | <span data-ttu-id="f02a6-115">Описание</span><span class="sxs-lookup"><span data-stu-id="f02a6-115">Description</span></span>                                                           |
|:-----------------|:----------------------------------------------------------------------|
| <span data-ttu-id="f02a6-116">**иинкрендерер**</span><span class="sxs-lookup"><span data-stu-id="f02a6-116">**IInkRenderer**</span></span> | <span data-ttu-id="f02a6-117">Этот объект реализует COM-интерфейс **иинкрендерер** .</span><span class="sxs-lookup"><span data-stu-id="f02a6-117">This object implements the **IInkRenderer** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="f02a6-118">Методы</span><span class="sxs-lookup"><span data-stu-id="f02a6-118">Methods</span></span>

<span data-ttu-id="f02a6-119">Класс **инкрендерер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f02a6-119">The **InkRenderer** class has these methods.</span></span>



| <span data-ttu-id="f02a6-120">Метод</span><span class="sxs-lookup"><span data-stu-id="f02a6-120">Method</span></span>                                                                     | <span data-ttu-id="f02a6-121">Описание</span><span class="sxs-lookup"><span data-stu-id="f02a6-121">Description</span></span>                                                                                                                                              |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f02a6-122">**Draw**</span><span class="sxs-lookup"><span data-stu-id="f02a6-122">**Draw**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw)                                           | <span data-ttu-id="f02a6-123">Рисует штрихи в контексте устройства.</span><span class="sxs-lookup"><span data-stu-id="f02a6-123">Draws strokes on a device context.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="f02a6-124">**дравстроке**</span><span class="sxs-lookup"><span data-stu-id="f02a6-124">**DrawStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)                               | <span data-ttu-id="f02a6-125">Рисует штрих для указанного контекста устройства Windows.</span><span class="sxs-lookup"><span data-stu-id="f02a6-125">Draws a stroke on the specified windows device context.</span></span><br/>                                                                                       |
| [<span data-ttu-id="f02a6-126">**жетобжекттрансформ**</span><span class="sxs-lookup"><span data-stu-id="f02a6-126">**GetObjectTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform)               | <span data-ttu-id="f02a6-127">Возвращает преобразование объекта, которое использовалось для отрисовки рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="f02a6-127">Retrieves the object transform that was used to render ink.</span></span><br/>                                                                                   |
| [<span data-ttu-id="f02a6-128">**жетвиевтрансформ**</span><span class="sxs-lookup"><span data-stu-id="f02a6-128">**GetViewTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform)                   | <span data-ttu-id="f02a6-129">Возвращает преобразование представления, используемое для визуализации рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="f02a6-129">Retrieves the view transform that is used to render ink.</span></span><br/>                                                                                      |
| [<span data-ttu-id="f02a6-130">**инкспацетопиксел**</span><span class="sxs-lookup"><span data-stu-id="f02a6-130">**InkSpaceToPixel**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel)                     | <span data-ttu-id="f02a6-131">Преобразует положение в координатах рукописного пространства в виде пиксельного пространства.</span><span class="sxs-lookup"><span data-stu-id="f02a6-131">Converts a location in ink space coordinates to be in pixel space.</span></span><br/>                                                                            |
| [<span data-ttu-id="f02a6-132">**инкспацетопикселфромпоинтс**</span><span class="sxs-lookup"><span data-stu-id="f02a6-132">**InkSpaceToPixelFromPoints**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints) | <span data-ttu-id="f02a6-133">Преобразует массив точек в координатах рукописного пространства в пиксельное пространство.</span><span class="sxs-lookup"><span data-stu-id="f02a6-133">Converts an array of points in ink space coordinates to pixel space.</span></span><br/>                                                                          |
| [<span data-ttu-id="f02a6-134">**Мера**</span><span class="sxs-lookup"><span data-stu-id="f02a6-134">**Measure**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-measure)                                     | <span data-ttu-id="f02a6-135">Вычисляет прямоугольник в контексте устройства, который будет содержать коллекцию штрихов, если они были выведены с помощью объекта **инкрендерер** .</span><span class="sxs-lookup"><span data-stu-id="f02a6-135">Calculates the rectangle on the device context that would contain a collection of strokes if they were drawn with the **InkRenderer** object.</span></span><br/> |
| [<span data-ttu-id="f02a6-136">**меасурестроке**</span><span class="sxs-lookup"><span data-stu-id="f02a6-136">**MeasureStroke**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkrenderer-measurestroke)                         | <span data-ttu-id="f02a6-137">Вычисляет прямоугольник в контексте устройства, который будет содержать штрих, если они были выведены с помощью объекта **инкрендерер** .</span><span class="sxs-lookup"><span data-stu-id="f02a6-137">Calculates the rectangle on the device context that would contain a stroke if they were drawn with the **InkRenderer** object.</span></span><br/>                |
| [<span data-ttu-id="f02a6-138">**Переместить**</span><span class="sxs-lookup"><span data-stu-id="f02a6-138">**Move**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-move)                                           | <span data-ttu-id="f02a6-139">Применяет перевод к преобразованию представления в координатах рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="f02a6-139">Applies a translation to the view transform in ink space coordinates.</span></span><br/>                                                                         |
| [<span data-ttu-id="f02a6-140">**пикселтоинкспаце**</span><span class="sxs-lookup"><span data-stu-id="f02a6-140">**PixelToInkSpace**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace)                     | <span data-ttu-id="f02a6-141">Преобразует положение в координатах пикселей в виде рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="f02a6-141">Converts a location in pixel coordinates to be in ink space.</span></span><br/>                                                                                  |
| [<span data-ttu-id="f02a6-142">**пикселтоинкспацефромпоинтс**</span><span class="sxs-lookup"><span data-stu-id="f02a6-142">**PixelToInkSpaceFromPoints**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints) | <span data-ttu-id="f02a6-143">Преобразует массив точек в координатах пиксельного пространства в область рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="f02a6-143">Converts an array of points in pixel space coordinates to ink space.</span></span><br/>                                                                          |
| [<span data-ttu-id="f02a6-144">**Поворот**</span><span class="sxs-lookup"><span data-stu-id="f02a6-144">**Rotate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-rotate)                                       | <span data-ttu-id="f02a6-145">Применяет поворот к преобразованию представления.</span><span class="sxs-lookup"><span data-stu-id="f02a6-145">Applies a rotation to the view transform.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="f02a6-146">**ScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="f02a6-146">**ScaleTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-scaletransform)                       | <span data-ttu-id="f02a6-147">Масштабирует преобразование представления в измерении X и Y.</span><span class="sxs-lookup"><span data-stu-id="f02a6-147">Scales the view transform in the X and Y dimension.</span></span><br/>                                                                                           |
| [<span data-ttu-id="f02a6-148">**сетобжекттрансформ**</span><span class="sxs-lookup"><span data-stu-id="f02a6-148">**SetObjectTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)               | <span data-ttu-id="f02a6-149">Задает преобразование объекта, используемое для отрисовки рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="f02a6-149">Sets the object transform that is used to render ink.</span></span><br/>                                                                                         |
| [<span data-ttu-id="f02a6-150">**сетвиевтрансформ**</span><span class="sxs-lookup"><span data-stu-id="f02a6-150">**SetViewTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform)                   | <span data-ttu-id="f02a6-151">Задает преобразование представления, используемое для визуализации рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="f02a6-151">Sets the view transform that is used to render ink.</span></span><br/>                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="f02a6-152">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f02a6-152">Remarks</span></span>

<span data-ttu-id="f02a6-153">Печать также выполняется через объект **инкрендерер** .</span><span class="sxs-lookup"><span data-stu-id="f02a6-153">Printing is also done through the **InkRenderer** object.</span></span>

<span data-ttu-id="f02a6-154">Для создания экземпляра этого объекта можно вызвать метод [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) в C++.</span><span class="sxs-lookup"><span data-stu-id="f02a6-154">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="f02a6-155">Требования</span><span class="sxs-lookup"><span data-stu-id="f02a6-155">Requirements</span></span>



| <span data-ttu-id="f02a6-156">Требование</span><span class="sxs-lookup"><span data-stu-id="f02a6-156">Requirement</span></span> | <span data-ttu-id="f02a6-157">Значение</span><span class="sxs-lookup"><span data-stu-id="f02a6-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f02a6-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f02a6-158">Minimum supported client</span></span><br/> | <span data-ttu-id="f02a6-159">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f02a6-159">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f02a6-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f02a6-160">Minimum supported server</span></span><br/> | <span data-ttu-id="f02a6-161">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f02a6-161">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f02a6-162">Header</span><span class="sxs-lookup"><span data-stu-id="f02a6-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="f02a6-163"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f02a6-163"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f02a6-164">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f02a6-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="f02a6-165"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f02a6-165"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f02a6-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f02a6-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f02a6-167">**Свойство модуля подготовки отчетов**</span><span class="sxs-lookup"><span data-stu-id="f02a6-167">**Renderer Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)
</dt> <dt>

[<span data-ttu-id="f02a6-168">**Класс Инкдравингаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="f02a6-168">**InkDrawingAttributes Class**</span></span>](inkdrawingattributes-class.md)
</dt> <dt>

[<span data-ttu-id="f02a6-169">**Интерфейс Иинкстрокедисп**</span><span class="sxs-lookup"><span data-stu-id="f02a6-169">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

<span data-ttu-id="f02a6-170">[Коллекция Инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f02a6-170">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> </dl>

 

