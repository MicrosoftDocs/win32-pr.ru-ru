---
description: Представляет собранные штрихи рукописного ввода в пределах пространства рукописного ввода.
ms.assetid: f942d6a3-f303-49df-a128-de9760b508ef
title: Класс Инкдисп (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDisp
- InkDisp.IInkDisp
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 429cbf85bdc92753cda1e58a0e89086b4b5b8b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808807"
---
# <a name="inkdisp-class"></a><span data-ttu-id="a5ef2-103">Класс Инкдисп</span><span class="sxs-lookup"><span data-stu-id="a5ef2-103">InkDisp class</span></span>

<span data-ttu-id="a5ef2-104">Представляет собранные штрихи рукописного ввода в пределах пространства рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-104">Represents the collected strokes of ink within an ink space.</span></span>

<span data-ttu-id="a5ef2-105">**Инкдисп** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a5ef2-105">**InkDisp** has these types of members:</span></span>

-   [<span data-ttu-id="a5ef2-106">События</span><span class="sxs-lookup"><span data-stu-id="a5ef2-106">Events</span></span>](#events)
-   [<span data-ttu-id="a5ef2-107">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="a5ef2-107">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="a5ef2-108">Методы</span><span class="sxs-lookup"><span data-stu-id="a5ef2-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="a5ef2-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="a5ef2-109">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="a5ef2-110">События</span><span class="sxs-lookup"><span data-stu-id="a5ef2-110">Events</span></span>

<span data-ttu-id="a5ef2-111">Класс **инкдисп** содержит следующие события.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-111">The **InkDisp** class has these events.</span></span>



| <span data-ttu-id="a5ef2-112">Событие</span><span class="sxs-lookup"><span data-stu-id="a5ef2-112">Event</span></span>                                    | <span data-ttu-id="a5ef2-113">Описание</span><span class="sxs-lookup"><span data-stu-id="a5ef2-113">Description</span></span>                                                             |
|:-----------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="a5ef2-114">**инкаддед**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-114">**InkAdded**</span></span>](inkdisp-inkadded.md)     | <span data-ttu-id="a5ef2-115">Происходит при добавлении штриха к объекту **инкдисп** .</span><span class="sxs-lookup"><span data-stu-id="a5ef2-115">Occurs when a stroke is added to the **InkDisp** object.</span></span><br/>     |
| [<span data-ttu-id="a5ef2-116">**инкделетед**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-116">**InkDeleted**</span></span>](inkdisp-inkdeleted.md) | <span data-ttu-id="a5ef2-117">Происходит при удалении штриха из объекта **инкдисп** .</span><span class="sxs-lookup"><span data-stu-id="a5ef2-117">Occurs when a stroke is deleted from the **InkDisp** object.</span></span><br/> |



 

### <a name="interfaces"></a><span data-ttu-id="a5ef2-118">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="a5ef2-118">Interfaces</span></span>

<span data-ttu-id="a5ef2-119">Класс **инкдисп** определяет эти интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-119">The **InkDisp** class defines these interfaces.</span></span>



| <span data-ttu-id="a5ef2-120">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="a5ef2-120">Interface</span></span>    | <span data-ttu-id="a5ef2-121">Описание</span><span class="sxs-lookup"><span data-stu-id="a5ef2-121">Description</span></span>                                                       |
|:-------------|:------------------------------------------------------------------|
| <span data-ttu-id="a5ef2-122">**иинкдисп**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-122">**IInkDisp**</span></span> | <span data-ttu-id="a5ef2-123">Этот объект реализует COM-интерфейс **иинкдисп** .</span><span class="sxs-lookup"><span data-stu-id="a5ef2-123">This object implements the **IInkDisp** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="a5ef2-124">Методы</span><span class="sxs-lookup"><span data-stu-id="a5ef2-124">Methods</span></span>

<span data-ttu-id="a5ef2-125">Класс **инкдисп** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-125">The **InkDisp** class has these methods.</span></span>



| <span data-ttu-id="a5ef2-126">Метод</span><span class="sxs-lookup"><span data-stu-id="a5ef2-126">Method</span></span>                                                                   | <span data-ttu-id="a5ef2-127">Описание</span><span class="sxs-lookup"><span data-stu-id="a5ef2-127">Description</span></span>                                                                                                                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5ef2-128">**аддстрокесатректангле**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-128">**AddStrokesAtRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle)           | <span data-ttu-id="a5ef2-129">Вставляет коллекцию штрихов в объект **инкдисп** на заданном прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-129">Inserts a stroke collection into the **InkDisp** object at the specified rectangle.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="a5ef2-130">**канпасте**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-130">**CanPaste**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                     | <span data-ttu-id="a5ef2-131">Указывает, можно ли преобразовать [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) в объект **инкдисп** .</span><span class="sxs-lookup"><span data-stu-id="a5ef2-131">Indicates whether the [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) can be converted to an **InkDisp** object.</span></span><br/>                                                                                       |
| [<span data-ttu-id="a5ef2-132">**Усечения**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-132">**Clip**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip)                                      | <span data-ttu-id="a5ef2-133">Удаляет части штриха или коллекции штрихов, находящихся за пределами прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-133">Removes portions of a stroke or collection of strokes that are outside a rectangle.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="a5ef2-134">**клипбоардкопи**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-134">**ClipboardCopy**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                           | <span data-ttu-id="a5ef2-135">Копирует коллекцию [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-135">Copies the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection to the Clipboard.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="a5ef2-136">**клипбоардкопивисректангле**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-136">**ClipboardCopyWithRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle) | <span data-ttu-id="a5ef2-137">Копирует объекты [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , содержащиеся в известном прямоугольнике, в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-137">Copies the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects that are contained within the known rectangle to the Clipboard.</span></span><br/>                                                               |
| [<span data-ttu-id="a5ef2-138">**клипбоардпасте**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-138">**ClipboardPaste**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                         | <span data-ttu-id="a5ef2-139">Копирует [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) из буфера обмена в объект **инкдисп** .</span><span class="sxs-lookup"><span data-stu-id="a5ef2-139">Copies the [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) from the Clipboard to the **InkDisp** object.</span></span><br/>                                                                                               |
| [<span data-ttu-id="a5ef2-140">**Клонировать**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-140">**Clone**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                           | <span data-ttu-id="a5ef2-141">Создает дубликат объекта **инкдисп** .</span><span class="sxs-lookup"><span data-stu-id="a5ef2-141">Creates a duplicate **InkDisp** object.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="a5ef2-142">**креатестроке**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-142">**CreateStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstroke)                             | <span data-ttu-id="a5ef2-143">Создает штрих по точкам или данным пакетов.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-143">Creates a stroke from points or packet data.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="a5ef2-144">**креатестрокес**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-144">**CreateStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstrokes)                           | <span data-ttu-id="a5ef2-145">Создает коллекцию [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) для этого объекта **инкдисп** .</span><span class="sxs-lookup"><span data-stu-id="a5ef2-145">Creates an [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection for this **InkDisp** object.</span></span><br/>                                                                                                |
| [<span data-ttu-id="a5ef2-146">**делетестроке**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-146">**DeleteStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke)                             | <span data-ttu-id="a5ef2-147">Удаляет штрих из объекта **инкдисп** .</span><span class="sxs-lookup"><span data-stu-id="a5ef2-147">Deletes a stroke from the **InkDisp** object.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="a5ef2-148">**делетестрокес**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-148">**DeleteStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes)                           | <span data-ttu-id="a5ef2-149">Удаляет штрихи из объекта **инкдисп** .</span><span class="sxs-lookup"><span data-stu-id="a5ef2-149">Deletes strokes from the **InkDisp** object.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="a5ef2-150">**Метод Екстрактстрокес**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-150">**ExtractStrokes Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes)                  | <span data-ttu-id="a5ef2-151">Извлекает штрихи из объекта **инкдисп** и возвращает новый объект **инкдисп** , содержащий извлеченные штрихи.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-151">Extracts strokes from the **InkDisp** object and returns a new **InkDisp** object containing the extracted strokes.</span></span><br/>                                                                       |
| [<span data-ttu-id="a5ef2-152">**Метод Екстрактвисректангле**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-152">**ExtractWithRectangle Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle)      | <span data-ttu-id="a5ef2-153">Вырезает или копирует штрихи из существующего объекта **класса инкдисп** и вставляет их в новый объект **класса инкдисп** , используя известный прямоугольник для определения штрихов, которые нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-153">Cuts or copies strokes from an existing **InkDisp Class** object and pastes them into a new **InkDisp Class** object, by using the known rectangle to determine which strokes to extract.</span></span><br/> |
| [<span data-ttu-id="a5ef2-154">**жетбаундингбокс**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-154">**GetBoundingBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)                  | <span data-ttu-id="a5ef2-155">Извлекает ограничивающий прямоугольник всех штрихов в объекте **инкдисп** .</span><span class="sxs-lookup"><span data-stu-id="a5ef2-155">Retrieves the bounding box of all of the strokes in the **InkDisp** object.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="a5ef2-156">**хиттестЦиркле**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-156">**HitTestCircle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle)                   | <span data-ttu-id="a5ef2-157">Извлекает коллекцию [**инкстрокес**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , которая полностью находится внутри известного круга или пересекается ей.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-157">Retrieves the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that are either completely inside or intersected by a known circle.</span></span><br/>                                                  |
| [<span data-ttu-id="a5ef2-158">**хиттествислассо**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-158">**HitTestWithLasso**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithlasso)              | <span data-ttu-id="a5ef2-159">Извлекает штрихи в области выделения ломаной линии.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-159">Retrieves the strokes within a polyline selection area.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="a5ef2-160">**хиттествисректангле**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-160">**HitTestWithRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle)        | <span data-ttu-id="a5ef2-161">Извлекает штрихи, содержащиеся в указанном прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-161">Retrieves the strokes that are contained within a specified rectangle.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="a5ef2-162">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-162">**Load**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load)                                             | <span data-ttu-id="a5ef2-163">Заполняет новый объект **инкдисп** известными двоичными данными.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-163">Populates a new **InkDisp** object with known binary data.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="a5ef2-164">**неарестпоинт**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-164">**NearestPoint**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-nearestpoint)                             | <span data-ttu-id="a5ef2-165">Извлекает [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) в объекте **инкдисп** , который является ближайшим к известной точке, при необходимости предоставляя дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-165">Retrieves the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) within the **InkDisp** object that is nearest to a known point, optionally providing additional information.</span></span><br/>                       |
| [<span data-ttu-id="a5ef2-166">**Сохранить**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-166">**Save**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save)                                             | <span data-ttu-id="a5ef2-167">Преобразует рукописный ввод в указанный формат и возвращает двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-167">Converts the ink to a specified format and returns the binary data.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="a5ef2-168">Свойства</span><span class="sxs-lookup"><span data-stu-id="a5ef2-168">Properties</span></span>

<span data-ttu-id="a5ef2-169">Класс **инкдисп** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-169">The **InkDisp** class has these properties.</span></span>



| <span data-ttu-id="a5ef2-170">Свойство</span><span class="sxs-lookup"><span data-stu-id="a5ef2-170">Property</span></span>                                                                           | <span data-ttu-id="a5ef2-171">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="a5ef2-171">Access type</span></span>           | <span data-ttu-id="a5ef2-172">Описание</span><span class="sxs-lookup"><span data-stu-id="a5ef2-172">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5ef2-173">**кустомстрокес**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-173">**CustomStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes)<br/>                          | <span data-ttu-id="a5ef2-174">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5ef2-174">Read-only</span></span><br/>  | <span data-ttu-id="a5ef2-175">Возвращает коллекцию [**иинккустомстрокес**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) , которая должна быть сохранена с рукописным вводом.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-175">Gets the [**IInkCustomStrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) collection to be persisted with the ink.</span></span><br/>                             |
| [<span data-ttu-id="a5ef2-176">**Бит**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-176">**Dirty**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty)<br/>                                          | <span data-ttu-id="a5ef2-177">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="a5ef2-177">Read/write</span></span><br/> | <span data-ttu-id="a5ef2-178">Возвращает или задает значение, указывающее, был ли изменен объект **инкдисп** со времени последнего сохранения рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-178">Gets or sets the value that indicates whether an **InkDisp** object has been modified since the last time the ink was saved.</span></span><br/> |
| [<span data-ttu-id="a5ef2-179">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-179">**ExtendedProperties**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | <span data-ttu-id="a5ef2-180">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5ef2-180">Read-only</span></span><br/>  | <span data-ttu-id="a5ef2-181">Возвращает коллекцию определяемых приложением данных.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-181">Gets the collection of application-defined data.</span></span><br/>                                                                             |
| [<span data-ttu-id="a5ef2-182">**Strokes**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-182">**Strokes**</span></span>](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)<br/>                           | <span data-ttu-id="a5ef2-183">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5ef2-183">Read-only</span></span><br/>  | <span data-ttu-id="a5ef2-184">Возвращает коллекцию [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , содержащуюся в объекте **инкдисп** .</span><span class="sxs-lookup"><span data-stu-id="a5ef2-184">Gets the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection contained in the **InkDisp** object.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="a5ef2-185">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5ef2-185">Remarks</span></span>

<span data-ttu-id="a5ef2-186">Для создания экземпляра этого объекта можно вызвать метод [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) в C++.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-186">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

> [!Note]  
> <span data-ttu-id="a5ef2-187">Первый экземпляр этого объекта также приводит к созданию экземпляра GDI+.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-187">The first instantiation of this object causes GDI+ to be instantiated as well.</span></span> <span data-ttu-id="a5ef2-188">Побочный результат заключается в том, что если вы используете один объект рукописного ввода в цикле и создаете и уничтожаете его в цикле, вы заставите экземпляр GDI+ выполняться повторно.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-188">A side-effect is that if you are using a single ink object in a loop and create and destroy it within the loop, you will cause GDI+ to be instantiated over and over.</span></span> <span data-ttu-id="a5ef2-189">Это может привести к снижению производительности приложения.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-189">This can cause a performance degradation in your application.</span></span> <span data-ttu-id="a5ef2-190">Чтобы предотвратить это, следует постоянно размещать один экземпляр объекта рукописного ввода, пока приложение использует рукописный ввод.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-190">To prevent this, keep a single instance of an ink object at all times while your application is using ink.</span></span>

 

<span data-ttu-id="a5ef2-191">Объект **инкдисп** — это контейнер данных росчерка (Point).</span><span class="sxs-lookup"><span data-stu-id="a5ef2-191">An **InkDisp** object is a container of stroke (point) data.</span></span> <span data-ttu-id="a5ef2-192">Данные штриха или точки, собранные пером, помещаются в объект **инкдисп** .</span><span class="sxs-lookup"><span data-stu-id="a5ef2-192">The stroke data, or the points collected by the pen, are put into an **InkDisp** object.</span></span> <span data-ttu-id="a5ef2-193">Свойство [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) содержит данные для всех штрихов в объекте **инкдисп** .</span><span class="sxs-lookup"><span data-stu-id="a5ef2-193">The [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property contains the data for all strokes within the **InkDisp** object.</span></span>

<span data-ttu-id="a5ef2-194">Объект [**InkCollector**](inkcollector-class.md) , объект [**InkOverlay**](inkoverlay-class.md) и элемент управления [InkPicture](inkpicture-control-reference.md) собирают точки из входного устройства и помещают их в объект **инкдисп** .</span><span class="sxs-lookup"><span data-stu-id="a5ef2-194">The [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, and [InkPicture](inkpicture-control-reference.md) control collects points from the input device and puts them into an **InkDisp** object.</span></span> <span data-ttu-id="a5ef2-195">Эти объекты по сути действуют как источник, который распределяет рукописный ввод в один или несколько различных объектов **инкдисп** , которые действуют как контейнеры, содержащие распределенные рукописные данные.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-195">These objects essentially act as the source that distributes ink into one or many different **InkDisp** objects, which act as containers that hold the distributed ink.</span></span>

<span data-ttu-id="a5ef2-196">Пространство для рукописного ввода — это виртуальное пространство координат, с которым сопоставляются координаты контекста планшета.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-196">The ink space is a virtual coordinate space to which the coordinates of the tablet context are mapped.</span></span> <span data-ttu-id="a5ef2-197">Это пространство зафиксировано в системе координат HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-197">This space is fixed to a HIMETRIC coordinate system.</span></span> <span data-ttu-id="a5ef2-198">В координатах рукописного пространства перемещение от 0 до 1 равно 1 HIMETRIC единице.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-198">In ink space coordinates, a move from 0 to 1 equals 1 HIMETRIC unit.</span></span> <span data-ttu-id="a5ef2-199">Это сопоставление упрощает связывание нескольких объектов **инкдисп** .</span><span class="sxs-lookup"><span data-stu-id="a5ef2-199">This mapping makes it easy to relate multiple **InkDisp** objects.</span></span>

<span data-ttu-id="a5ef2-200">Объект [**инкрендерер**](inkrenderer-class.md) управляет сопоставлениями рукописного ввода и окна отображения.</span><span class="sxs-lookup"><span data-stu-id="a5ef2-200">The [**InkRenderer**](inkrenderer-class.md) object manages the mappings between ink and the display window.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5ef2-201">Требования</span><span class="sxs-lookup"><span data-stu-id="a5ef2-201">Requirements</span></span>



| <span data-ttu-id="a5ef2-202">Требование</span><span class="sxs-lookup"><span data-stu-id="a5ef2-202">Requirement</span></span> | <span data-ttu-id="a5ef2-203">Значение</span><span class="sxs-lookup"><span data-stu-id="a5ef2-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5ef2-204">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5ef2-204">Minimum supported client</span></span><br/> | <span data-ttu-id="a5ef2-205">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a5ef2-205">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a5ef2-206">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5ef2-206">Minimum supported server</span></span><br/> | <span data-ttu-id="a5ef2-207">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a5ef2-207">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a5ef2-208">Header</span><span class="sxs-lookup"><span data-stu-id="a5ef2-208">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5ef2-209"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a5ef2-209"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a5ef2-210">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a5ef2-210">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5ef2-211"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5ef2-211"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a5ef2-212">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5ef2-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5ef2-213">**Интерфейс Иинкстрокедисп**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-213">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

<span data-ttu-id="a5ef2-214">[Коллекция Инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a5ef2-214">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a5ef2-215">**Интерфейс Иинктаблет**</span><span class="sxs-lookup"><span data-stu-id="a5ef2-215">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

