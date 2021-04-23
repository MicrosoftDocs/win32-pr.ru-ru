---
description: Интерфейс Иамтимелинесрк предоставляет методы для управления и установки свойств исходных объектов в службах редактирования DirectShow (DES).
ms.assetid: 39a64718-1fac-4d90-8340-b712d3bad2ec
title: Интерфейс Иамтимелинесрк (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 25733b1353bc0cbd92c40335a8d342473b03a806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674959"
---
# <a name="iamtimelinesrc-interface"></a><span data-ttu-id="44488-103">Интерфейс Иамтимелинесрк</span><span class="sxs-lookup"><span data-stu-id="44488-103">IAMTimelineSrc interface</span></span>

> [!Note]  
> <span data-ttu-id="44488-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="44488-104">\[Deprecated.</span></span> <span data-ttu-id="44488-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="44488-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="44488-106">`IAMTimelineSrc`Интерфейс предоставляет методы для управления и установки свойств исходных объектов в [службах редактирования DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="44488-106">The `IAMTimelineSrc` interface provides methods for manipulating and setting properties on source objects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="44488-107">Исходный объект представляет один поток из источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="44488-107">A source object represents one stream from a media source.</span></span>

<span data-ttu-id="44488-108">Можно использовать часть данных в исходном файле, задав время начала и окончания воспроизведения носителя.</span><span class="sxs-lookup"><span data-stu-id="44488-108">You can use a portion of the data within a source file by setting the media start and media stop times.</span></span> <span data-ttu-id="44488-109">Эти значения указывают начало и конец исходного объекта относительно исходного источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="44488-109">These values specify the beginning and end of the source object, relative to the original media source.</span></span> <span data-ttu-id="44488-110">Время работы с носителями может отличаться от времени начала и окончания работы объекта на временной шкале, что позволяет быстро или медленно воспроизводить воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="44488-110">The media times can differ from the object's start and stop times on the timeline, allowing for fast- or slow-motion playback.</span></span> <span data-ttu-id="44488-111">(С источниками звука происходит сдвиг высоты.)</span><span class="sxs-lookup"><span data-stu-id="44488-111">(With audio sources, pitch shifting occurs.)</span></span>

<span data-ttu-id="44488-112">Чтобы создать исходный объект, вызовите [**иамтимелине:: креатимптиноде**](iamtimeline-createemptynode.md) со значением \_ источник основного типа временной шкалы \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="44488-112">To create a source object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_SOURCE.</span></span> <span data-ttu-id="44488-113">Вы можете запросить возвращенный указатель [**иамтимелинеобж**](iamtimelineobj.md) для интерфейса **иамтимелинесрк** .</span><span class="sxs-lookup"><span data-stu-id="44488-113">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the **IAMTimelineSrc** interface.</span></span> <span data-ttu-id="44488-114">Дополнительные сведения см. в статьях [Создание временной шкалы](constructing-a-timeline.md) и [Работа с источниками](working-with-sources.md).</span><span class="sxs-lookup"><span data-stu-id="44488-114">For more information, see [Constructing a Timeline](constructing-a-timeline.md) and [Working with Sources](working-with-sources.md).</span></span>

## <a name="members"></a><span data-ttu-id="44488-115">Элементы</span><span class="sxs-lookup"><span data-stu-id="44488-115">Members</span></span>

<span data-ttu-id="44488-116">Интерфейс **иамтимелинесрк** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="44488-116">The **IAMTimelineSrc** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="44488-117">**Иамтимелинесрк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="44488-117">**IAMTimelineSrc** also has these types of members:</span></span>

-   [<span data-ttu-id="44488-118">Методы</span><span class="sxs-lookup"><span data-stu-id="44488-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="44488-119">Методы</span><span class="sxs-lookup"><span data-stu-id="44488-119">Methods</span></span>

<span data-ttu-id="44488-120">Интерфейс **иамтимелинесрк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="44488-120">The **IAMTimelineSrc** interface has these methods.</span></span>



| <span data-ttu-id="44488-121">Метод</span><span class="sxs-lookup"><span data-stu-id="44488-121">Method</span></span>                                                    | <span data-ttu-id="44488-122">Описание</span><span class="sxs-lookup"><span data-stu-id="44488-122">Description</span></span>                                                                                              |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44488-123">**фиксмедиатимес**</span><span class="sxs-lookup"><span data-stu-id="44488-123">**FixMediaTimes**</span></span>](iamtimelinesrc-fixmediatimes.md)     | <span data-ttu-id="44488-124">Округляет указанные значения времени до ближайшей границы фрейма.</span><span class="sxs-lookup"><span data-stu-id="44488-124">Rounds the specified time values to the nearest frame boundary.</span></span><br/>                               |
| [<span data-ttu-id="44488-125">**FixMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="44488-125">**FixMediaTimes2**</span></span>](iamtimelinesrc-fixmediatimes2.md)   | <span data-ttu-id="44488-126">Округляет указанные значения времени, заданные как значения **рефтиме** , до ближайшей границы фрейма.</span><span class="sxs-lookup"><span data-stu-id="44488-126">Rounds the specified time values, given as **REFTIME** values, to the nearest frame boundary.</span></span><br/> |
| [<span data-ttu-id="44488-127">**жетдефаултфпс**</span><span class="sxs-lookup"><span data-stu-id="44488-127">**GetDefaultFPS**</span></span>](iamtimelinesrc-getdefaultfps.md)     | <span data-ttu-id="44488-128">Возвращает частоту кадров по умолчанию для исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="44488-128">Retrieves the source object's default frame rate.</span></span><br/>                                             |
| [<span data-ttu-id="44488-129">**жетмедиаленгс**</span><span class="sxs-lookup"><span data-stu-id="44488-129">**GetMediaLength**</span></span>](iamtimelinesrc-getmedialength.md)   | <span data-ttu-id="44488-130">Возвращает длину носителя этого исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="44488-130">Retrieves the media length of this source object.</span></span><br/>                                             |
| [<span data-ttu-id="44488-131">**GetMediaLength2**</span><span class="sxs-lookup"><span data-stu-id="44488-131">**GetMediaLength2**</span></span>](iamtimelinesrc-getmedialength2.md) | <span data-ttu-id="44488-132">Получает длину носителя этого исходного объекта в виде значения **рефтиме** .</span><span class="sxs-lookup"><span data-stu-id="44488-132">Retrieves the media length of this source object, as a **REFTIME** value.</span></span><br/>                     |
| [<span data-ttu-id="44488-133">**жетмедианаме**</span><span class="sxs-lookup"><span data-stu-id="44488-133">**GetMediaName**</span></span>](iamtimelinesrc-getmedianame.md)       | <span data-ttu-id="44488-134">Извлекает имя исходного файла, представленного этим исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="44488-134">Retrieves the name of the source file represented by this source object.</span></span><br/>                      |
| [<span data-ttu-id="44488-135">**жетмедиатимес**</span><span class="sxs-lookup"><span data-stu-id="44488-135">**GetMediaTimes**</span></span>](iamtimelinesrc-getmediatimes.md)     | <span data-ttu-id="44488-136">Получает время начала и окончания воспроизведения носителя.</span><span class="sxs-lookup"><span data-stu-id="44488-136">Retrieves the media start and stop times.</span></span><br/>                                                     |
| [<span data-ttu-id="44488-137">**GetMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="44488-137">**GetMediaTimes2**</span></span>](iamtimelinesrc-getmediatimes2.md)   | <span data-ttu-id="44488-138">Получает время начала и окончания воспроизведения в виде значений **рефтиме** .</span><span class="sxs-lookup"><span data-stu-id="44488-138">Retrieves the media start and stop times, as **REFTIME** values.</span></span><br/>                              |
| [<span data-ttu-id="44488-139">**жетстреамнумбер**</span><span class="sxs-lookup"><span data-stu-id="44488-139">**GetStreamNumber**</span></span>](iamtimelinesrc-getstreamnumber.md) | <span data-ttu-id="44488-140">Возвращает текущий номер потока для исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="44488-140">Retrieves the current stream number for the source object.</span></span><br/>                                    |
| [<span data-ttu-id="44488-141">**жетстретчмоде**</span><span class="sxs-lookup"><span data-stu-id="44488-141">**GetStretchMode**</span></span>](iamtimelinesrc-getstretchmode.md)   | <span data-ttu-id="44488-142">Извлекает режим растяжения для источника видео.</span><span class="sxs-lookup"><span data-stu-id="44488-142">Retrieves the stretch mode of a video source.</span></span><br/>                                                 |
| [<span data-ttu-id="44488-143">**иснормалрате**</span><span class="sxs-lookup"><span data-stu-id="44488-143">**IsNormalRate**</span></span>](iamtimelinesrc-isnormalrate.md)       | <span data-ttu-id="44488-144">Указывает, будет ли воспроизводиться воспроизведение клипа с нормальным темпом воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="44488-144">Indicates whether the clip will play at the normal playback rate.</span></span><br/>                             |
| [<span data-ttu-id="44488-145">**модифистоптиме**</span><span class="sxs-lookup"><span data-stu-id="44488-145">**ModifyStopTime**</span></span>](iamtimelinesrc-modifystoptime.md)   | <span data-ttu-id="44488-146">Задает время окончания относительно временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="44488-146">Sets the stop time, relative to the timeline.</span></span><br/>                                                 |
| [<span data-ttu-id="44488-147">**ModifyStopTime2**</span><span class="sxs-lookup"><span data-stu-id="44488-147">**ModifyStopTime2**</span></span>](iamtimelinesrc-modifystoptime2.md) | <span data-ttu-id="44488-148">Задает время окончания в виде значения **рефтиме** .</span><span class="sxs-lookup"><span data-stu-id="44488-148">Sets the stop time, as a **REFTIME** value.</span></span><br/>                                                   |
| [<span data-ttu-id="44488-149">**сетдефаултфпс**</span><span class="sxs-lookup"><span data-stu-id="44488-149">**SetDefaultFPS**</span></span>](iamtimelinesrc-setdefaultfps.md)     | <span data-ttu-id="44488-150">Задает частоту кадров исходного объекта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="44488-150">Sets the source object's default frame rate.</span></span><br/>                                                  |
| [<span data-ttu-id="44488-151">**сетмедиаленгс**</span><span class="sxs-lookup"><span data-stu-id="44488-151">**SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)   | <span data-ttu-id="44488-152">Указывает длительность исходного файла.</span><span class="sxs-lookup"><span data-stu-id="44488-152">Specifies the duration of the source file.</span></span><br/>                                                    |
| [<span data-ttu-id="44488-153">**SetMediaLength2**</span><span class="sxs-lookup"><span data-stu-id="44488-153">**SetMediaLength2**</span></span>](iamtimelinesrc-setmedialength2.md) | <span data-ttu-id="44488-154">Задает продолжительность исходного файла в виде значения **рефтиме** .</span><span class="sxs-lookup"><span data-stu-id="44488-154">Specifies the duration of the source file, as a **REFTIME** value.</span></span><br/>                            |
| [<span data-ttu-id="44488-155">**сетмедианаме**</span><span class="sxs-lookup"><span data-stu-id="44488-155">**SetMediaName**</span></span>](iamtimelinesrc-setmedianame.md)       | <span data-ttu-id="44488-156">Задает имя исходного файла, представленного этим исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="44488-156">Specifies the name of the source file represented by this source object.</span></span><br/>                      |
| [<span data-ttu-id="44488-157">**сетмедиатимес**</span><span class="sxs-lookup"><span data-stu-id="44488-157">**SetMediaTimes**</span></span>](iamtimelinesrc-setmediatimes.md)     | <span data-ttu-id="44488-158">Задает время начала и окончания воспроизведения носителя.</span><span class="sxs-lookup"><span data-stu-id="44488-158">Sets the media stop and start times.</span></span><br/>                                                          |
| [<span data-ttu-id="44488-159">**SetMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="44488-159">**SetMediaTimes2**</span></span>](iamtimelinesrc-setmediatimes2.md)   | <span data-ttu-id="44488-160">Задает время начала и окончания воспроизведения в виде значений **рефтиме** .</span><span class="sxs-lookup"><span data-stu-id="44488-160">Sets the media stop and start times, as **REFTIME** values.</span></span><br/>                                   |
| [<span data-ttu-id="44488-161">**сетстреамнумбер**</span><span class="sxs-lookup"><span data-stu-id="44488-161">**SetStreamNumber**</span></span>](iamtimelinesrc-setstreamnumber.md) | <span data-ttu-id="44488-162">Указывает, какой поток следует считать из исходного файла, связанного с этим исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="44488-162">Specifies which stream to read from the source file associated with this source object.</span></span><br/>       |
| [<span data-ttu-id="44488-163">**сетстретчмоде**</span><span class="sxs-lookup"><span data-stu-id="44488-163">**SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)   | <span data-ttu-id="44488-164">Задает режим растяжения для источника видео.</span><span class="sxs-lookup"><span data-stu-id="44488-164">Sets the stretch mode of a video source.</span></span><br/>                                                      |
| [<span data-ttu-id="44488-165">**сплицевиснекст**</span><span class="sxs-lookup"><span data-stu-id="44488-165">**SpliceWithNext**</span></span>](iamtimelinesrc-splicewithnext.md)   | <span data-ttu-id="44488-166">Присоединяет этот исходный объект к другому исходному объекту.</span><span class="sxs-lookup"><span data-stu-id="44488-166">Joins this source object to another source object.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="44488-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44488-167">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="44488-168">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="44488-168">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="44488-169">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="44488-169">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="44488-170">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="44488-170">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="44488-171">Требования</span><span class="sxs-lookup"><span data-stu-id="44488-171">Requirements</span></span>



| <span data-ttu-id="44488-172">Требование</span><span class="sxs-lookup"><span data-stu-id="44488-172">Requirement</span></span> | <span data-ttu-id="44488-173">Значение</span><span class="sxs-lookup"><span data-stu-id="44488-173">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44488-174">Header</span><span class="sxs-lookup"><span data-stu-id="44488-174">Header</span></span><br/>  | <dl> <span data-ttu-id="44488-175"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="44488-175"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="44488-176">Библиотека</span><span class="sxs-lookup"><span data-stu-id="44488-176">Library</span></span><br/> | <dl> <span data-ttu-id="44488-177"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44488-177"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
