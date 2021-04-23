---
description: Свойства подизображения DVD определяют цвет, контрастность и вывод для экрана подизображения.
ms.assetid: ddbfb65c-7630-4e9f-8013-c5d65c62c628
title: Набор свойств "подизображение DVD-диска" (Двдмедиа. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a45b83595e8657ee0c60f39cd67f2d0e4c71511
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909092"
---
# <a name="dvd-subpicture-property-set"></a><span data-ttu-id="73961-103">Набор свойств подизображения DVD</span><span class="sxs-lookup"><span data-stu-id="73961-103">DVD Subpicture Property Set</span></span>

<span data-ttu-id="73961-104">Свойства подизображения DVD определяют цвет, контрастность и вывод для экрана подизображения.</span><span class="sxs-lookup"><span data-stu-id="73961-104">DVD Subpicture properties control the color, contrast, and output of the subpicture display.</span></span>

<span data-ttu-id="73961-105">Следующая информация представляет необходимые константы и типы данных, используемые для этого свойства в вызовах методов [**икспропертисет**](ikspropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="73961-105">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="73961-106">Он предоставляет значения для параметров **GUID** (*ГУИДПРОПСЕТ*), идентификатора свойства (*dwPropID*) и типа данных свойства (*ппропдата*).</span><span class="sxs-lookup"><span data-stu-id="73961-106">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



| <span data-ttu-id="73961-107">Метка</span><span class="sxs-lookup"><span data-stu-id="73961-107">Label</span></span> | <span data-ttu-id="73961-108">Значение</span><span class="sxs-lookup"><span data-stu-id="73961-108">Value</span></span> |
|-------------------|----------------------------|
| <span data-ttu-id="73961-109">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="73961-109">Property Set GUID</span></span> | <span data-ttu-id="73961-110">\_Кспропсетид \_ двдсубпик</span><span class="sxs-lookup"><span data-stu-id="73961-110">AM\_KSPROPSETID\_DvdSubPic</span></span> |



 



| <span data-ttu-id="73961-111">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="73961-111">Property ID</span></span>                           | <span data-ttu-id="73961-112">Описание</span><span class="sxs-lookup"><span data-stu-id="73961-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73961-113">\_двдсубпик свойства \_ \_ композиции \_</span><span class="sxs-lookup"><span data-stu-id="73961-113">AM\_PROPERTY\_DVDSUBPIC\_COMPOSIT\_ON</span></span> | <span data-ttu-id="73961-114">Свойство только для установки, которое включает или отключает отображение субтитров.</span><span class="sxs-lookup"><span data-stu-id="73961-114">Set-only property that enables or disables subpicture display.</span></span> <span data-ttu-id="73961-115">DirectShow определяет **\_ \_ композицию свойства \_ AM** для типа данных Boolean для этого свойства, а также \_ \_ композицию свойства PAM \_ в качестве указателя на этот тип данных.</span><span class="sxs-lookup"><span data-stu-id="73961-115">DirectShow defines the **AM\_PROPERTY\_COMPOSIT\_ON** Boolean data type for this property, as well as PAM\_PROPERTY\_COMPOSIT\_ON as a pointer to this data type.</span></span> <span data-ttu-id="73961-116">**Значение true** показывает, что подизображение отображается, а **значение false** — отключить.</span><span class="sxs-lookup"><span data-stu-id="73961-116">**TRUE** indicates display the subpicture, **FALSE** indicates disable it.</span></span> <span data-ttu-id="73961-117">Дополнительные сведения см. в части WDM набора Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="73961-117">See the WDM portion of the Windows DDK for more information.</span></span> |
| <span data-ttu-id="73961-118">\_свойство AM \_ двдсубпик \_ Хли</span><span class="sxs-lookup"><span data-stu-id="73961-118">AM\_PROPERTY\_DVDSUBPIC\_HLI</span></span>          | <span data-ttu-id="73961-119">Свойство только для установки, указывающее прямоугольник подизображения или экрана, цвет или контраст которого будет изменен.</span><span class="sxs-lookup"><span data-stu-id="73961-119">Set-only property that specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="73961-120">Тип данных — [**это \_ свойство \_ сфли**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli).</span><span class="sxs-lookup"><span data-stu-id="73961-120">Data type is [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli).</span></span> <span data-ttu-id="73961-121">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="73961-121">See Remarks.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="73961-122">\_ \_ \_ Палитра двдсубпик свойств</span><span class="sxs-lookup"><span data-stu-id="73961-122">AM\_PROPERTY\_DVDSUBPIC\_PALETTE</span></span>      | <span data-ttu-id="73961-123">Задает палитру для подизображения.</span><span class="sxs-lookup"><span data-stu-id="73961-123">Sets the palette for a subpicture.</span></span> <span data-ttu-id="73961-124">Тип данных — [**это \_ свойство \_ сппал**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).</span><span class="sxs-lookup"><span data-stu-id="73961-124">Data type is [**AM\_PROPERTY\_SPPAL**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).</span></span>                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="73961-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73961-125">Remarks</span></span>

<span data-ttu-id="73961-126">Свойство **AM \_ \_ двдсубпик \_ Хли** имеет значение только Set.</span><span class="sxs-lookup"><span data-stu-id="73961-126">The **AM\_PROPERTY\_DVDSUBPIC\_HLI** property is set-only.</span></span> <span data-ttu-id="73961-127">Он задает прямоугольник подизображения или экрана, цвет или контраст которого будет изменен.</span><span class="sxs-lookup"><span data-stu-id="73961-127">It specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="73961-128">Это отличается от спецификации DVD-Video, в которой DVD-навигатор Майкрософт анализирует все сведения о кнопках и клавиатурах и передает только один выделенный прямоугольник в декодер субтитров в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="73961-128">This differs from the DVD-Video specification, in that the Microsoft DVD navigator parses all button and keyboard information and passes only one highlight rectangle to the subpicture decoder at any given time.</span></span> <span data-ttu-id="73961-129">В результате сведения о выделении отправляются в декодер чаще, чем в потоке DVD.</span><span class="sxs-lookup"><span data-stu-id="73961-129">As a result, highlight information is sent to the decoder more often than it is present in the DVD stream.</span></span>

<span data-ttu-id="73961-130">Сведения о выделении поступают в поток данных асинхронно.</span><span class="sxs-lookup"><span data-stu-id="73961-130">The highlight information arrives asynchronously to the data stream.</span></span> <span data-ttu-id="73961-131">Декодер использует метки времени начала и окончания, чтобы сопоставить сведения о выделении с соответствующими сведениями о подизображении, если они есть.</span><span class="sxs-lookup"><span data-stu-id="73961-131">The decoder uses the highlight Start and End time stamps to correlate the highlight information to the relevant subpicture information, if any.</span></span> <span data-ttu-id="73961-132">Если декодер не получал сведения о потоке субтитров для запрошенных штампов времени, декодер предполагает, что выделенная информация является изолированной и не применяется к подизображению.</span><span class="sxs-lookup"><span data-stu-id="73961-132">If the decoder has not received any subpicture stream information for the requested time stamps, the decoder assumes that the highlight information is stand-alone and does not apply to a subpicture.</span></span> <span data-ttu-id="73961-133">В этом случае декодер предполагает, что цвет и сведения о контрастах имеют одинаковый цвет.</span><span class="sxs-lookup"><span data-stu-id="73961-133">In this case, the decoder assumes the color and contrast information is all the same color.</span></span>

<span data-ttu-id="73961-134">Данные не полностью находятся в формате DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="73961-134">The data is not entirely in DVD disc format.</span></span> <span data-ttu-id="73961-135">Корпорация Майкрософт предоставляет дополнительную структуру типа [**\_ \_ сфли**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) , которая передается в качестве параметра этому свойству.</span><span class="sxs-lookup"><span data-stu-id="73961-135">Microsoft provides an additional structure of type [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) that is passed as the parameter to this property.</span></span> <span data-ttu-id="73961-136">Эта структура описывает выбранную в данный момент кнопку на основе сведений о выделении DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="73961-136">This structure describes the currently selected button from the DVD highlight information.</span></span>

<span data-ttu-id="73961-137">DVD-навигатор обрабатывает все сведения о нажатии клавиш и отправляет новые сведения о выделении при каждом изменении состояния кнопки.</span><span class="sxs-lookup"><span data-stu-id="73961-137">The DVD navigator processes all keystroke information and sends new highlight information each time a button state changes.</span></span> <span data-ttu-id="73961-138">Информация описывает только один режим одной кнопки за раз.</span><span class="sxs-lookup"><span data-stu-id="73961-138">The information describes only one mode of one button at a time.</span></span> <span data-ttu-id="73961-139">Он содержит прямоугольник, отображаемый в пикселях координат экрана, или изображение, если оно присутствует.</span><span class="sxs-lookup"><span data-stu-id="73961-139">It includes a display rectangle in pixel coordinates of the screen, or a display of the subpicture, if present.</span></span> <span data-ttu-id="73961-140">Структура также содержит сведения о цвете и контрасте, но только для текущего состояния выбранной кнопки.</span><span class="sxs-lookup"><span data-stu-id="73961-140">The structure also contains color and contrast information, but only for the present state of the currently selected button.</span></span> <span data-ttu-id="73961-141">Формат определяется в спецификации DVD.</span><span class="sxs-lookup"><span data-stu-id="73961-141">The format is defined in the DVD specification.</span></span>

<span data-ttu-id="73961-142">Выделенные сведения содержат метки времени начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="73961-142">Highlight information contains Start and End time stamps.</span></span> <span data-ttu-id="73961-143">Они находятся в тех же единицах, что и другие отметки времени, с двумя исключениями: метка времени начала 0xFFFFFFFF означает, что свойство выделения вступает в силу после получения, а метка времени окончания 0xFFFFFFFF означает, что свойство выделения допустимо до получения следующего выделения.</span><span class="sxs-lookup"><span data-stu-id="73961-143">These are in the same units as other time stamps, with two exceptions: A Start time stamp of 0xFFFFFFFF means the highlight property is effective upon receipt, and an End time stamp of 0xFFFFFFFF means the highlight property is valid until next highlight received.</span></span>

<span data-ttu-id="73961-144">Поле ХЛИСС определено в спецификации DVD.</span><span class="sxs-lookup"><span data-stu-id="73961-144">The HLISS field is as defined in the DVD specification.</span></span> <span data-ttu-id="73961-145">Нулевое значение означает, что все выделения недопустимы, и декодер должен отключить все выделения.</span><span class="sxs-lookup"><span data-stu-id="73961-145">A value of zero indicates that all highlights are invalid and the decoder should disable all highlights.</span></span>

## <a name="requirements"></a><span data-ttu-id="73961-146">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="73961-146">Requirements</span></span>



| <span data-ttu-id="73961-147">Требование</span><span class="sxs-lookup"><span data-stu-id="73961-147">Requirement</span></span> | <span data-ttu-id="73961-148">Значение</span><span class="sxs-lookup"><span data-stu-id="73961-148">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73961-149">Заголовок</span><span class="sxs-lookup"><span data-stu-id="73961-149">Header</span></span><br/> | <dl> <span data-ttu-id="73961-150"><dt>Двдмедиа. h</dt></span><span class="sxs-lookup"><span data-stu-id="73961-150"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73961-151">См. также</span><span class="sxs-lookup"><span data-stu-id="73961-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73961-152">Наборы свойств</span><span class="sxs-lookup"><span data-stu-id="73961-152">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




