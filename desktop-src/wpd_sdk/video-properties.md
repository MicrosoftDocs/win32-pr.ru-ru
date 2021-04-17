---
description: Портативные устройства Windows поддерживают следующие свойства видео.
ms.assetid: e6df5b2d-ceb8-4de0-b60b-9102c77143fe
title: Свойства видео (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Video
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1f44f32ab19c5ad10cc9c8dd5bdb8816ccc944f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717858"
---
# <a name="video-properties"></a><span data-ttu-id="e83e8-103">Свойства видео</span><span class="sxs-lookup"><span data-stu-id="e83e8-103">Video Properties</span></span>

<span data-ttu-id="e83e8-104">Портативные устройства Windows поддерживают следующие свойства видео.</span><span class="sxs-lookup"><span data-stu-id="e83e8-104">Windows Portable Devices supports the following video properties.</span></span>



| <span data-ttu-id="e83e8-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="e83e8-105">Property</span></span>                                         | <span data-ttu-id="e83e8-106">VarType</span><span class="sxs-lookup"><span data-stu-id="e83e8-106">VarType</span></span>        | <span data-ttu-id="e83e8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e83e8-107">Description</span></span>                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e83e8-108">**\_ \_ создатель видео WPD**</span><span class="sxs-lookup"><span data-stu-id="e83e8-108">**WPD\_VIDEO\_AUTHOR**</span></span>                           | <span data-ttu-id="e83e8-109">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="e83e8-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="e83e8-110">Автор видеофайла.</span><span class="sxs-lookup"><span data-stu-id="e83e8-110">The author of the video file.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="e83e8-111">**\_скорость видео \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="e83e8-111">**WPD\_VIDEO\_BITRATE**</span></span>                          | <span data-ttu-id="e83e8-112">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="e83e8-112">**VT\_UI4**</span></span>    | <span data-ttu-id="e83e8-113">Скорость воспроизведения видеофайла.</span><span class="sxs-lookup"><span data-stu-id="e83e8-113">The bit rate of the video file.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="e83e8-114">**\_ \_ Размер буфера видео \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="e83e8-114">**WPD\_VIDEO\_BUFFER\_SIZE**</span></span>                     | <span data-ttu-id="e83e8-115">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="e83e8-115">**VT\_UI4**</span></span>    | <span data-ttu-id="e83e8-116">Значение, указывающее размер требуемого видеобуфера для подготовки к просмотру этого файла.</span><span class="sxs-lookup"><span data-stu-id="e83e8-116">A value that specifies the required video buffer size to render this file.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="e83e8-117">**\_кредиты видео о WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e83e8-117">**WPD\_VIDEO\_CREDITS**</span></span>                          | <span data-ttu-id="e83e8-118">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="e83e8-118">**VT\_LPWSTR**</span></span> | <span data-ttu-id="e83e8-119">Кредиты, в которых перечислены приведения и сотрудников для видео.</span><span class="sxs-lookup"><span data-stu-id="e83e8-119">The credits listing the cast and crew for the video.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="e83e8-120">**\_код Video \_ FourCC для WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e83e8-120">**WPD\_VIDEO\_FOURCC\_CODE**</span></span>                     | <span data-ttu-id="e83e8-121">**VT \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e83e8-121">**VT\_DWORD**</span></span>  | <span data-ttu-id="e83e8-122">Зарегистрированный код FourCC, указывающий кодек, который использовался для файла видео.</span><span class="sxs-lookup"><span data-stu-id="e83e8-122">The registered FourCC code that indicates the codec that was used for the video file.</span></span> <span data-ttu-id="e83e8-123">Список форматов FourCC см. в статье [зарегистрированные коды FourCC и форматы Wave](https://msdn2.microsoft.com/library/ms867195.aspx) на веб-сайте MSDN.</span><span class="sxs-lookup"><span data-stu-id="e83e8-123">For a listing of FourCC formats, see the article [Registered FOURCC Codes and WAVE Formats](https://msdn2.microsoft.com/library/ms867195.aspx) on the MSDN Web site.</span></span> |
| <span data-ttu-id="e83e8-124">**\_Видеочастота видео WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e83e8-124">**WPD\_VIDEO\_FRAMERATE**</span></span>                        | <span data-ttu-id="e83e8-125">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="e83e8-125">**VT\_UI4**</span></span>    | <span data-ttu-id="e83e8-126">Частота кадров видеофайла в кадрах/сек x 1 000.</span><span class="sxs-lookup"><span data-stu-id="e83e8-126">The frame rate of the video file, in frames/second x 1,000.</span></span> <span data-ttu-id="e83e8-127">Например, частота кадров 29,97 представлена как 29970.</span><span class="sxs-lookup"><span data-stu-id="e83e8-127">For example, a frame rate of 29.97 is represented as 29970.</span></span>                                                                                                                                 |
| <span data-ttu-id="e83e8-128">**\_Жанр видео \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="e83e8-128">**WPD\_VIDEO\_GENRE**</span></span>                            | <span data-ttu-id="e83e8-129">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="e83e8-129">**VT\_LPWSTR**</span></span> | <span data-ttu-id="e83e8-130">Жанр этого видеофайла.</span><span class="sxs-lookup"><span data-stu-id="e83e8-130">The genre of this video file.</span></span> <span data-ttu-id="e83e8-131">Нет стандартных определений жанра.</span><span class="sxs-lookup"><span data-stu-id="e83e8-131">There are no standard genre definitions.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="e83e8-132">**\_ \_ \_ расстояние между кадрами ВИДЕОключа WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e83e8-132">**WPD\_VIDEO\_KEY\_FRAME\_DISTANCE**</span></span>             | <span data-ttu-id="e83e8-133">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="e83e8-133">**VT\_UI4**</span></span>    | <span data-ttu-id="e83e8-134">Интервал между опорными кадрами в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="e83e8-134">The interval between key frames, in milliseconds.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="e83e8-135">**\_ \_ Настройка качества видео \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="e83e8-135">**WPD\_VIDEO\_QUALITY\_SETTING**</span></span>                 | <span data-ttu-id="e83e8-136">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="e83e8-136">**VT\_UI4**</span></span>    | <span data-ttu-id="e83e8-137">Параметр качества для файла видео.</span><span class="sxs-lookup"><span data-stu-id="e83e8-137">The quality setting for the video file.</span></span> <span data-ttu-id="e83e8-138">Это зависит от кодека.</span><span class="sxs-lookup"><span data-stu-id="e83e8-138">This is codec-dependent.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="e83e8-139">**\_ \_ \_ номер канала рекордедтв видео \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="e83e8-139">**WPD\_VIDEO\_RECORDEDTV\_CHANNEL\_NUMBER**</span></span>      | <span data-ttu-id="e83e8-140">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="e83e8-140">**VT\_UI4**</span></span>    | <span data-ttu-id="e83e8-141">Номер канала телевидения, из которого записано видео.</span><span class="sxs-lookup"><span data-stu-id="e83e8-141">The television channel number the video was recorded from.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="e83e8-142">**\_ \_ \_ Описание программы WPD Video \_ рекордедтв**</span><span class="sxs-lookup"><span data-stu-id="e83e8-142">**WPD\_VIDEO\_RECORDEDTV\_PROGRAM\_DESCRIPTION**</span></span> | <span data-ttu-id="e83e8-143">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="e83e8-143">**VT\_LPWSTR**</span></span> | <span data-ttu-id="e83e8-144">Описание записанной телепрограммы.</span><span class="sxs-lookup"><span data-stu-id="e83e8-144">A description of the recorded television program.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="e83e8-145">**\_ \_ Повторная РЕКОРДЕДТВ видео WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e83e8-145">**WPD\_VIDEO\_RECORDEDTV\_REPEAT**</span></span>               | <span data-ttu-id="e83e8-146">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="e83e8-146">**VT\_BOOL**</span></span>   | <span data-ttu-id="e83e8-147">Логическое значение, указывающее, была ли Телепрограмма показана повтор.</span><span class="sxs-lookup"><span data-stu-id="e83e8-147">A Boolean value that specifies whether the television program was a repeat showing.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="e83e8-148">**\_ \_ \_ имя станции рекордедтв ВИДЕОролика WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e83e8-148">**WPD\_VIDEO\_RECORDEDTV\_STATION\_NAME**</span></span>        | <span data-ttu-id="e83e8-149">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="e83e8-149">**VT\_LPWSTR**</span></span> | <span data-ttu-id="e83e8-150">Телевизионная станция, из которой записано видео.</span><span class="sxs-lookup"><span data-stu-id="e83e8-150">The television station that the video was recorded from.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="e83e8-151">**\_Тип сканирования видеороликов WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e83e8-151">**WPD\_VIDEO\_SCAN\_TYPE**</span></span>                       | <span data-ttu-id="e83e8-152">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="e83e8-152">**VT\_UI4**</span></span>    | <span data-ttu-id="e83e8-153">Перечислитель [**\_ \_ \_ типов сканирования видео WPD**](wpd-video-scan-types.md) , указывающий чересстрочную развертку видеофайла.</span><span class="sxs-lookup"><span data-stu-id="e83e8-153">A [**WPD\_VIDEO\_SCAN\_TYPES**](wpd-video-scan-types.md) enumerator that specifies the interlacing of the video file.</span></span>                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="e83e8-154">Требования</span><span class="sxs-lookup"><span data-stu-id="e83e8-154">Requirements</span></span>



| <span data-ttu-id="e83e8-155">Требование</span><span class="sxs-lookup"><span data-stu-id="e83e8-155">Requirement</span></span> | <span data-ttu-id="e83e8-156">Значение</span><span class="sxs-lookup"><span data-stu-id="e83e8-156">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e83e8-157">Header</span><span class="sxs-lookup"><span data-stu-id="e83e8-157">Header</span></span><br/> | <dl> <span data-ttu-id="e83e8-158"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="e83e8-158"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e83e8-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e83e8-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e83e8-160">**Свойства и атрибуты WPD**</span><span class="sxs-lookup"><span data-stu-id="e83e8-160">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




