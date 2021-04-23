---
title: Интерфейс Ивмпконтролс (VB и C) (WMP. h)
description: Предоставляет способ управления воспроизведением элемента мультимедиа путем представления элементов управления транспорта Windows Media Player, таких как воспроизведение, остановка и приостановка. интерфейс Ивмпконтролс предоставляет следующие свойства.
ms.assetid: 46603d98-c7dd-4c20-a4ae-1472b3af8d52
keywords:
- Ивмпконтролс (VB и C) интерфейс проигрывателя Windows Media
- Ивмпконтролс (VB и C) интерфейс проигрывателя Windows Media, описание
topic_type:
- apiref
api_name:
- IWMPControls (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b544978d801f3a9d5d5cbd9644f1d32ac53791e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688849"
---
# <a name="iwmpcontrols-vb-and-c-interface"></a><span data-ttu-id="5c621-105">Интерфейс Ивмпконтролс (VB и C#)</span><span class="sxs-lookup"><span data-stu-id="5c621-105">IWMPControls (VB and C#) interface</span></span>

<span data-ttu-id="5c621-106">Предоставляет способ управления воспроизведением элемента мультимедиа путем представления элементов управления транспорта Windows Media Player, таких как воспроизведение, остановка и пауза.</span><span class="sxs-lookup"><span data-stu-id="5c621-106">Provides a way to manipulate the playback of a media item by representing the transport controls of Windows Media Player, such as Play, Stop, and Pause.</span></span>

<span data-ttu-id="5c621-107">Интерфейс **ивмпконтролс** предоставляет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5c621-107">The **IWMPControls** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="5c621-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="5c621-108">Members</span></span>

<span data-ttu-id="5c621-109">Интерфейс **ивмпконтролс (VB и C#)** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5c621-109">The **IWMPControls (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="5c621-110">Методы</span><span class="sxs-lookup"><span data-stu-id="5c621-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="5c621-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="5c621-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5c621-112">Методы</span><span class="sxs-lookup"><span data-stu-id="5c621-112">Methods</span></span>

<span data-ttu-id="5c621-113">Интерфейс **ивмпконтролс (VB и C#)** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="5c621-113">The **IWMPControls (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="5c621-114">Метод</span><span class="sxs-lookup"><span data-stu-id="5c621-114">Method</span></span>                                                                       | <span data-ttu-id="5c621-115">Описание</span><span class="sxs-lookup"><span data-stu-id="5c621-115">Description</span></span>                                                                                 |
|:-----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c621-116">**фастфорвард**</span><span class="sxs-lookup"><span data-stu-id="5c621-116">**fastForward**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md) | <span data-ttu-id="5c621-117">Запускает быстрое воспроизведение элемента мультимедиа в прямом направлении.</span><span class="sxs-lookup"><span data-stu-id="5c621-117">Starts fast play of the media item in the forward direction.</span></span><br/>                     |
| [<span data-ttu-id="5c621-118">**фастреверсе**</span><span class="sxs-lookup"><span data-stu-id="5c621-118">**fastReverse**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md) | <span data-ttu-id="5c621-119">Запускает быстрое воспроизведение элемента мультимедиа в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="5c621-119">Starts fast play of the media item in the reverse direction.</span></span><br/>                     |
| [<span data-ttu-id="5c621-120">**очеред**</span><span class="sxs-lookup"><span data-stu-id="5c621-120">**next**</span></span>](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)               | <span data-ttu-id="5c621-121">Задает следующий элемент списка воспроизведения в качестве текущего элемента.</span><span class="sxs-lookup"><span data-stu-id="5c621-121">Sets the next item in the playlist as the current item.</span></span><br/>                          |
| [<span data-ttu-id="5c621-122">**работу**</span><span class="sxs-lookup"><span data-stu-id="5c621-122">**pause**</span></span>](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)             | <span data-ttu-id="5c621-123">Приостанавливает воспроизведение элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="5c621-123">Pauses playback of the media item.</span></span><br/>                                               |
| [<span data-ttu-id="5c621-124">**воспроизводит**</span><span class="sxs-lookup"><span data-stu-id="5c621-124">**play**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)               | <span data-ttu-id="5c621-125">Начинает воспроизведение текущего элемента мультимедиа или возобновляет воспроизведение приостановленного элемента.</span><span class="sxs-lookup"><span data-stu-id="5c621-125">Begins playback of the current media item, or resumes playback of a paused item.</span></span><br/> |
| [<span data-ttu-id="5c621-126">**плайитем**</span><span class="sxs-lookup"><span data-stu-id="5c621-126">**playItem**</span></span>](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)       | <span data-ttu-id="5c621-127">Воспроизводит указанный элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="5c621-127">Plays the specified media item.</span></span><br/>                                                  |
| [<span data-ttu-id="5c621-128">**прошлом**</span><span class="sxs-lookup"><span data-stu-id="5c621-128">**previous**</span></span>](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)       | <span data-ttu-id="5c621-129">Устанавливает предыдущий элемент списка воспроизведения в качестве текущего элемента.</span><span class="sxs-lookup"><span data-stu-id="5c621-129">Sets the previous item in the playlist as the current item.</span></span><br/>                      |
| [<span data-ttu-id="5c621-130">**позиции**</span><span class="sxs-lookup"><span data-stu-id="5c621-130">**stop**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)               | <span data-ttu-id="5c621-131">Останавливает воспроизведение элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="5c621-131">Stops playback of the media item.</span></span><br/>                                                |



 

### <a name="properties"></a><span data-ttu-id="5c621-132">Свойства</span><span class="sxs-lookup"><span data-stu-id="5c621-132">Properties</span></span>

<span data-ttu-id="5c621-133">Интерфейс **ивмпконтролс (VB и C#)** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5c621-133">The **IWMPControls (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="5c621-134">Свойство</span><span class="sxs-lookup"><span data-stu-id="5c621-134">Property</span></span>                                                                                                    | <span data-ttu-id="5c621-135">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="5c621-135">Access type</span></span>           | <span data-ttu-id="5c621-136">Описание</span><span class="sxs-lookup"><span data-stu-id="5c621-136">Description</span></span>                                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c621-137">**currentItem**</span><span class="sxs-lookup"><span data-stu-id="5c621-137">**currentItem**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)<br/>                     | <span data-ttu-id="5c621-138">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="5c621-138">Read/write</span></span><br/> | <span data-ttu-id="5c621-139">Возвращает или задает текущий элемент мультимедиа в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="5c621-139">Gets or sets the current media item in a playlist.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="5c621-140">**куррентмаркер**</span><span class="sxs-lookup"><span data-stu-id="5c621-140">**currentMarker**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentmarker--vb-and-c.md)<br/>                 | <span data-ttu-id="5c621-141">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="5c621-141">Read/write</span></span><br/> | <span data-ttu-id="5c621-142">Возвращает или задает номер текущего маркера.</span><span class="sxs-lookup"><span data-stu-id="5c621-142">Gets or sets the current marker number.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="5c621-143">**currentPosition**</span><span class="sxs-lookup"><span data-stu-id="5c621-143">**currentPosition**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)<br/>             | <span data-ttu-id="5c621-144">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="5c621-144">Read/write</span></span><br/> | <span data-ttu-id="5c621-145">Возвращает или задает текущую позицию в элементе мультимедиа в секундах с начала.</span><span class="sxs-lookup"><span data-stu-id="5c621-145">Gets or sets the current position in the media item in seconds from the beginning.</span></span><br/>                                                                                    |
| [<span data-ttu-id="5c621-146">**куррентпоситионстринг**</span><span class="sxs-lookup"><span data-stu-id="5c621-146">**currentPositionString**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)<br/> | <span data-ttu-id="5c621-147">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c621-147">Read-only</span></span><br/>  | <span data-ttu-id="5c621-148">Возвращает текущую позицию в элементе мультимедиа в виде **System. String**.</span><span class="sxs-lookup"><span data-stu-id="5c621-148">Gets the current position in the media item as a **System.String**.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="5c621-149">**isAvailable**</span><span class="sxs-lookup"><span data-stu-id="5c621-149">**isAvailable**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)<br/>                                        | <span data-ttu-id="5c621-150">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c621-150">Read-only</span></span><br/>  | <span data-ttu-id="5c621-151">Возвращает значение, указывающее, доступен ли указанный тип сведений, или может быть выполнено указанное действие.</span><span class="sxs-lookup"><span data-stu-id="5c621-151">Gets a value indicating whether a specified type of information is available or a specified action can be performed.</span></span> <span data-ttu-id="5c621-152">В C# это метод Get- **\_ Available** .</span><span class="sxs-lookup"><span data-stu-id="5c621-152">In C#, this is the **get\_isAvailable** method.</span></span><br/> |



 

<span data-ttu-id="5c621-153">Получите интерфейс **ивмпконтролс** с помощью следующего свойства.</span><span class="sxs-lookup"><span data-stu-id="5c621-153">Get an **IWMPControls** interface by using the following property.</span></span>



| <span data-ttu-id="5c621-154">Объект</span><span class="sxs-lookup"><span data-stu-id="5c621-154">Object</span></span>                                                                   | <span data-ttu-id="5c621-155">Свойство</span><span class="sxs-lookup"><span data-stu-id="5c621-155">Property</span></span>                                                                   |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="5c621-156">Объект Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="5c621-156">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="5c621-157">**ктлконтролс**</span><span class="sxs-lookup"><span data-stu-id="5c621-157">**Ctlcontrols**</span></span>](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="5c621-158">Требования</span><span class="sxs-lookup"><span data-stu-id="5c621-158">Requirements</span></span>



| <span data-ttu-id="5c621-159">Требование</span><span class="sxs-lookup"><span data-stu-id="5c621-159">Requirement</span></span> | <span data-ttu-id="5c621-160">Значение</span><span class="sxs-lookup"><span data-stu-id="5c621-160">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5c621-161">Header</span><span class="sxs-lookup"><span data-stu-id="5c621-161">Header</span></span><br/> | <dl> <span data-ttu-id="5c621-162"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c621-162"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c621-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c621-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c621-164">**Интерфейсы для Visual Basic .NET и C #**</span><span class="sxs-lookup"><span data-stu-id="5c621-164">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="5c621-165">**Интерфейс IWMPControls2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="5c621-165">**IWMPControls2 Interface (VB and C#)**</span></span>](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5c621-166">**Интерфейс IWMPControls3 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="5c621-166">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





