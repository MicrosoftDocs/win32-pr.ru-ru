---
description: 'Интерфейс Иамтимелинеграуп задает и извлекает свойства групп в службах редактирования DirectShow (DES). Группа содержит одну или несколько дорожек и, возможно, одну или несколько композиций, которые, в свою очередь, содержат исходные клипы однородного типа, такие как видео или аудио. Группы — это самые верхние композиции на временной шкале, а также интерфейс Иамтимелинекомп. Временная шкала может содержать несколько групп. Каждая группа имеет следующие атрибуты. Связанный тип мультимедиа. Частота кадров, с которой группа готовится к просмотру, в кадрах в секунду (кадров/с). Все изменения происходят во время, округленное до ближайшей границы фрейма, как определено параметром группы кадров. Уровень приоритета для записи файлов с несколькими потоками одного типа мультимедиа (например, из файла AVI с двумя видеопотоками). Чтобы создать объект группы, вызовите Иамтимелине:: Креатимптиноде с группой значений основной тип временной ШКАЛы \_ \_ \_ . Вы можете запросить возвращенный указатель Иамтимелинеобж для интерфейса Иамтимелинеграуп.'
ms.assetid: c24e5e0a-43a5-4ba7-ac28-6e2ebb341a38
title: Интерфейс Иамтимелинеграуп (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e82a11db65183e343048f594a7457c0a8febf8bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689485"
---
# <a name="iamtimelinegroup-interface"></a><span data-ttu-id="cba05-107">Интерфейс Иамтимелинеграуп</span><span class="sxs-lookup"><span data-stu-id="cba05-107">IAMTimelineGroup interface</span></span>

> [!Note]  
> <span data-ttu-id="cba05-108">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="cba05-108">\[Deprecated.</span></span> <span data-ttu-id="cba05-109">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cba05-109">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cba05-110">`IAMTimelineGroup`Интерфейс задает и получает свойства групп в [службах редактирования DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="cba05-110">The `IAMTimelineGroup` interface sets and retrieves properties on groups in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="cba05-111">Группа содержит одну или несколько дорожек и, возможно, одну или несколько композиций, которые, в свою очередь, содержат исходные клипы однородного типа, такие как видео или аудио.</span><span class="sxs-lookup"><span data-stu-id="cba05-111">A group contains one or more tracks, and possibly one or more compositions, which in turn contain source clips of a uniform type, such as video or audio.</span></span> <span data-ttu-id="cba05-112">Группы — это самые верхние композиции на временной шкале, а также интерфейс [**иамтимелинекомп**](iamtimelinecomp.md) .</span><span class="sxs-lookup"><span data-stu-id="cba05-112">Groups are the topmost compositions in a timeline, and also expose the [**IAMTimelineComp**](iamtimelinecomp.md) interface.</span></span> <span data-ttu-id="cba05-113">Временная шкала может содержать несколько групп.</span><span class="sxs-lookup"><span data-stu-id="cba05-113">A timeline can contain multiple groups.</span></span>

<span data-ttu-id="cba05-114">Каждая группа имеет следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="cba05-114">Each group has the following attributes.</span></span>

-   <span data-ttu-id="cba05-115">Связанный тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cba05-115">An associated media type.</span></span>
-   <span data-ttu-id="cba05-116">Частота кадров, с которой группа готовится к просмотру, в кадрах в секунду (кадров/с).</span><span class="sxs-lookup"><span data-stu-id="cba05-116">The frame rate at which the group renders, in frames per second (FPS).</span></span> <span data-ttu-id="cba05-117">Все изменения происходят во время, округленное до ближайшей границы фрейма, как определено параметром группы кадров.</span><span class="sxs-lookup"><span data-stu-id="cba05-117">All edits occur at a time rounded to the nearest frame boundary, as defined by the group's FPS setting.</span></span>
-   <span data-ttu-id="cba05-118">Уровень приоритета для записи файлов с несколькими потоками одного типа мультимедиа (например, из файла AVI с двумя видеопотоками).</span><span class="sxs-lookup"><span data-stu-id="cba05-118">A priority level, for writing files with multiple streams of the same media type (for example, a two-video-stream AVI file).</span></span>

<span data-ttu-id="cba05-119">Чтобы создать объект группы, вызовите [**иамтимелине:: креатимптиноде**](iamtimeline-createemptynode.md) с группой значений основной тип временной шкалы \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cba05-119">To create a group object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_GROUP.</span></span> <span data-ttu-id="cba05-120">Вы можете запросить возвращенный указатель [**иамтимелинеобж**](iamtimelineobj.md) для интерфейса **иамтимелинеграуп** .</span><span class="sxs-lookup"><span data-stu-id="cba05-120">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the **IAMTimelineGroup** interface.</span></span>

## <a name="members"></a><span data-ttu-id="cba05-121">Элементы</span><span class="sxs-lookup"><span data-stu-id="cba05-121">Members</span></span>

<span data-ttu-id="cba05-122">Интерфейс **иамтимелинеграуп** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cba05-122">The **IAMTimelineGroup** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cba05-123">**Иамтимелинеграуп** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cba05-123">**IAMTimelineGroup** also has these types of members:</span></span>

-   [<span data-ttu-id="cba05-124">Методы</span><span class="sxs-lookup"><span data-stu-id="cba05-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cba05-125">Методы</span><span class="sxs-lookup"><span data-stu-id="cba05-125">Methods</span></span>

<span data-ttu-id="cba05-126">Интерфейс **иамтимелинеграуп** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="cba05-126">The **IAMTimelineGroup** interface has these methods.</span></span>



| <span data-ttu-id="cba05-127">Метод</span><span class="sxs-lookup"><span data-stu-id="cba05-127">Method</span></span>                                                                            | <span data-ttu-id="cba05-128">Описание</span><span class="sxs-lookup"><span data-stu-id="cba05-128">Description</span></span>                                                                                     |
|:----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cba05-129">**клеаррекомпрессформатдирти**</span><span class="sxs-lookup"><span data-stu-id="cba05-129">**ClearRecompressFormatDirty**</span></span>](iamtimelinegroup-clearrecompressformatdirty.md) | <span data-ttu-id="cba05-130">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cba05-130">Not supported.</span></span><br/>                                                                       |
| [<span data-ttu-id="cba05-131">**жетграупнаме**</span><span class="sxs-lookup"><span data-stu-id="cba05-131">**GetGroupName**</span></span>](iamtimelinegroup-getgroupname.md)                             | <span data-ttu-id="cba05-132">Извлекает определяемое приложением имя группы.</span><span class="sxs-lookup"><span data-stu-id="cba05-132">Retrieves the application-defined name of the group.</span></span><br/>                                 |
| [<span data-ttu-id="cba05-133">**жетмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="cba05-133">**GetMediaType**</span></span>](iamtimelinegroup-getmediatype.md)                             | <span data-ttu-id="cba05-134">Извлекает несжатый тип носителя для группы.</span><span class="sxs-lookup"><span data-stu-id="cba05-134">Retrieves the uncompressed media type for the group.</span></span><br/>                                 |
| [<span data-ttu-id="cba05-135">**жетаутпутбуфферинг**</span><span class="sxs-lookup"><span data-stu-id="cba05-135">**GetOutputBuffering**</span></span>](iamtimelinegroup-getoutputbuffering.md)                 | <span data-ttu-id="cba05-136">Возвращает число кадров, отображаемых заранее во время просмотра.</span><span class="sxs-lookup"><span data-stu-id="cba05-136">Retrieves the number of frames rendered in advance during preview.</span></span><br/>                   |
| [<span data-ttu-id="cba05-137">**жетаутпутфпс**</span><span class="sxs-lookup"><span data-stu-id="cba05-137">**GetOutputFPS**</span></span>](iamtimelinegroup-getoutputfps.md)                             | <span data-ttu-id="cba05-138">Возвращает частоту выходных кадров этой группы.</span><span class="sxs-lookup"><span data-stu-id="cba05-138">Retrieves the output frame rate of this group.</span></span><br/>                                       |
| [<span data-ttu-id="cba05-139">**жетпревиевмоде**</span><span class="sxs-lookup"><span data-stu-id="cba05-139">**GetPreviewMode**</span></span>](iamtimelinegroup-getpreviewmode.md)                         | <span data-ttu-id="cba05-140">Возвращает режим предварительного просмотра для группы.</span><span class="sxs-lookup"><span data-stu-id="cba05-140">Retrieves the preview mode for the group.</span></span><br/>                                            |
| [<span data-ttu-id="cba05-141">**GetPriority**</span><span class="sxs-lookup"><span data-stu-id="cba05-141">**GetPriority**</span></span>](iamtimelinegroup-getpriority.md)                               | <span data-ttu-id="cba05-142">Получает приоритет группы.</span><span class="sxs-lookup"><span data-stu-id="cba05-142">Retrieves the group's priority.</span></span><br/>                                                      |
| [<span data-ttu-id="cba05-143">**жетсмартрекомпрессформат**</span><span class="sxs-lookup"><span data-stu-id="cba05-143">**GetSmartRecompressFormat**</span></span>](iamtimelinegroup-getsmartrecompressformat.md)     | <span data-ttu-id="cba05-144">Извлекает текущий формат сжатия для интеллектуального повторного сжатия.</span><span class="sxs-lookup"><span data-stu-id="cba05-144">Retrieves the current compression format for smart recompression.</span></span><br/>                    |
| [<span data-ttu-id="cba05-145">**Временная шкала**</span><span class="sxs-lookup"><span data-stu-id="cba05-145">**GetTimeline**</span></span>](iamtimelinegroup-gettimeline.md)                               | <span data-ttu-id="cba05-146">Извлекает временную шкалу, к которой принадлежит эта группа.</span><span class="sxs-lookup"><span data-stu-id="cba05-146">Retrieves the timeline to which this group belongs.</span></span><br/>                                  |
| [<span data-ttu-id="cba05-147">**исрекомпрессформатдирти**</span><span class="sxs-lookup"><span data-stu-id="cba05-147">**IsRecompressFormatDirty**</span></span>](iamtimelinegroup-isrecompressformatdirty.md)       | <span data-ttu-id="cba05-148">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cba05-148">Not supported.</span></span><br/>                                                                       |
| [<span data-ttu-id="cba05-149">**иссмартрекомпрессформатсет**</span><span class="sxs-lookup"><span data-stu-id="cba05-149">**IsSmartRecompressFormatSet**</span></span>](iamtimelinegroup-issmartrecompressformatset.md) | <span data-ttu-id="cba05-150">Определяет, задан ли для группы формат интеллектуального сжатия.</span><span class="sxs-lookup"><span data-stu-id="cba05-150">Determines whether a smart compression format was set for the group.</span></span><br/>                 |
| [<span data-ttu-id="cba05-151">**сетграупнаме**</span><span class="sxs-lookup"><span data-stu-id="cba05-151">**SetGroupName**</span></span>](iamtimelinegroup-setgroupname.md)                             | <span data-ttu-id="cba05-152">Задает определяемое приложением имя группы.</span><span class="sxs-lookup"><span data-stu-id="cba05-152">Sets the application-defined name of the group.</span></span><br/>                                      |
| [<span data-ttu-id="cba05-153">**сетмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="cba05-153">**SetMediaType**</span></span>](iamtimelinegroup-setmediatype.md)                             | <span data-ttu-id="cba05-154">Задает несжатый тип носителя для группы.</span><span class="sxs-lookup"><span data-stu-id="cba05-154">Sets the uncompressed media type for the group.</span></span><br/>                                      |
| [<span data-ttu-id="cba05-155">**сетмедиатипефорвб**</span><span class="sxs-lookup"><span data-stu-id="cba05-155">**SetMediaTypeForVB**</span></span>](iamtimelinegroup-setmediatypeforvb.md)                   | <span data-ttu-id="cba05-156">Указывает тип носителя группы для клиентов автоматизации.</span><span class="sxs-lookup"><span data-stu-id="cba05-156">Specifies the group media type, for Automation clients.</span></span><br/>                              |
| [<span data-ttu-id="cba05-157">**сетаутпутбуфферинг**</span><span class="sxs-lookup"><span data-stu-id="cba05-157">**SetOutputBuffering**</span></span>](iamtimelinegroup-setoutputbuffering.md)                 | <span data-ttu-id="cba05-158">Указывает число кадров, отображаемых заранее во время просмотра.</span><span class="sxs-lookup"><span data-stu-id="cba05-158">Specifies the number of frames rendered in advance during preview.</span></span><br/>                   |
| [<span data-ttu-id="cba05-159">**сетаутпутфпс**</span><span class="sxs-lookup"><span data-stu-id="cba05-159">**SetOutputFPS**</span></span>](iamtimelinegroup-setoutputfps.md)                             | <span data-ttu-id="cba05-160">Задает несжатую частоту выходного кадра для этой группы.</span><span class="sxs-lookup"><span data-stu-id="cba05-160">Sets the uncompressed output frame rate for this group.</span></span><br/>                              |
| [<span data-ttu-id="cba05-161">**сетпревиевмоде**</span><span class="sxs-lookup"><span data-stu-id="cba05-161">**SetPreviewMode**</span></span>](iamtimelinegroup-setpreviewmode.md)                         | <span data-ttu-id="cba05-162">Задает режим предварительного просмотра для группы.</span><span class="sxs-lookup"><span data-stu-id="cba05-162">Sets the preview mode for the group.</span></span><br/>                                                 |
| [<span data-ttu-id="cba05-163">**сетрекомпформатфромсаурце**</span><span class="sxs-lookup"><span data-stu-id="cba05-163">**SetRecompFormatFromSource**</span></span>](iamtimelinegroup-setrecompformatfromsource.md)   | <span data-ttu-id="cba05-164">Задает формат повторного сжатия видео, используя формат сжатия из исходного файла.</span><span class="sxs-lookup"><span data-stu-id="cba05-164">Sets the video recompression format using the compression format from a source file.</span></span><br/> |
| [<span data-ttu-id="cba05-165">**сетсмартрекомпрессформат**</span><span class="sxs-lookup"><span data-stu-id="cba05-165">**SetSmartRecompressFormat**</span></span>](iamtimelinegroup-setsmartrecompressformat.md)     | <span data-ttu-id="cba05-166">Задает формат сжатия, используемый для интеллектуального повторного сжатия.</span><span class="sxs-lookup"><span data-stu-id="cba05-166">Specifies a compression format to use for smart recompression.</span></span><br/>                       |
| [<span data-ttu-id="cba05-167">**сеттимелине**</span><span class="sxs-lookup"><span data-stu-id="cba05-167">**SetTimeline**</span></span>](iamtimelinegroup-settimeline.md)                               | <span data-ttu-id="cba05-168">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cba05-168">Not supported.</span></span><br/>                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="cba05-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cba05-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cba05-170">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="cba05-170">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cba05-171">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="cba05-171">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cba05-172">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="cba05-172">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cba05-173">Требования</span><span class="sxs-lookup"><span data-stu-id="cba05-173">Requirements</span></span>



| <span data-ttu-id="cba05-174">Требование</span><span class="sxs-lookup"><span data-stu-id="cba05-174">Requirement</span></span> | <span data-ttu-id="cba05-175">Значение</span><span class="sxs-lookup"><span data-stu-id="cba05-175">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cba05-176">Header</span><span class="sxs-lookup"><span data-stu-id="cba05-176">Header</span></span><br/>  | <dl> <span data-ttu-id="cba05-177"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="cba05-177"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cba05-178">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cba05-178">Library</span></span><br/> | <dl> <span data-ttu-id="cba05-179"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cba05-179"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
