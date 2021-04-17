---
description: Интерфейс Имедиадет извлекает сведения о файле мультимедиа, например число потоков, тип носителя, длительность и частоту кадров каждого потока.
ms.assetid: 596fc84e-a88a-4e1b-aa48-b6dc9031db31
title: Интерфейс Имедиадет (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ca5c87a1424872491aba5dcf4e01011872e9ff36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674977"
---
# <a name="imediadet-interface"></a><span data-ttu-id="b5c76-103">Интерфейс Имедиадет</span><span class="sxs-lookup"><span data-stu-id="b5c76-103">IMediaDet interface</span></span>

> [!Note]  
> <span data-ttu-id="b5c76-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="b5c76-104">\[Deprecated.</span></span> <span data-ttu-id="b5c76-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b5c76-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b5c76-106">`IMediaDet`Интерфейс получает сведения о файле мультимедиа, например число потоков, тип носителя, длительность и частоту кадров каждого потока.</span><span class="sxs-lookup"><span data-stu-id="b5c76-106">The `IMediaDet` interface retrieves information about a media file, such as the number of streams, and the media type, duration, and frame rate of each stream.</span></span> <span data-ttu-id="b5c76-107">Он также содержит методы для извлечения отдельных кадров из потока видео.</span><span class="sxs-lookup"><span data-stu-id="b5c76-107">It also contains methods for retrieving individual frames from a video stream.</span></span> <span data-ttu-id="b5c76-108">Объект [детектора мультимедиа (медиадет)](media-detector--mediadet.md) предоставляет этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="b5c76-108">The [Media Detector (MediaDet)](media-detector--mediadet.md) object exposes this interface.</span></span>

<span data-ttu-id="b5c76-109">Чтобы получить сведения о файле с помощью этого интерфейса, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b5c76-109">To obtain information about a file using this interface, perform the following steps:</span></span>

1.  <span data-ttu-id="b5c76-110">Создайте экземпляр объекта Медиадет, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="b5c76-110">Create an instance of the MediaDet object by calling **CoCreateInstance**.</span></span> <span data-ttu-id="b5c76-111">Идентификатор класса — CLSID \_ медиадет.</span><span class="sxs-lookup"><span data-stu-id="b5c76-111">The class ID is CLSID\_MediaDet.</span></span>
2.  <span data-ttu-id="b5c76-112">Вызовите [**имедиадет::p UT \_ filename**](imediadet-put-filename.md) , чтобы указать имя исходного файла.</span><span class="sxs-lookup"><span data-stu-id="b5c76-112">Call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to specify the name of the source file.</span></span>
3.  <span data-ttu-id="b5c76-113">Вызовите метод [**имедиадет:: Get \_ аутпутстреамс**](imediadet-get-outputstreams.md) , чтобы получить число потоков вывода в источнике.</span><span class="sxs-lookup"><span data-stu-id="b5c76-113">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to obtain the number of output streams in the source.</span></span>
4.  <span data-ttu-id="b5c76-114">Вызовите [**имедиадет::p UT \_ куррентстреам**](imediadet-put-currentstream.md) , чтобы указать конкретный поток.</span><span class="sxs-lookup"><span data-stu-id="b5c76-114">Call [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md) to specify a particular stream.</span></span>
5.  <span data-ttu-id="b5c76-115">Вызовите любой из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="b5c76-115">Call any of the following methods:</span></span>
    -   [<span data-ttu-id="b5c76-116">**Имедиадет:: получение \_ частоты кадров**</span><span class="sxs-lookup"><span data-stu-id="b5c76-116">**IMediaDet::get\_FrameRate**</span></span>](imediadet-get-framerate.md)
    -   [<span data-ttu-id="b5c76-117">**Имедиадет:: Get \_ стреамленгс**</span><span class="sxs-lookup"><span data-stu-id="b5c76-117">**IMediaDet::get\_StreamLength**</span></span>](imediadet-get-streamlength.md)
    -   [<span data-ttu-id="b5c76-118">**Имедиадет:: Get \_ стреаммедиатипе**</span><span class="sxs-lookup"><span data-stu-id="b5c76-118">**IMediaDet::get\_StreamMediaType**</span></span>](imediadet-get-streammediatype.md)
    -   [<span data-ttu-id="b5c76-119">**Имедиадет:: Get \_ стреамтипе**</span><span class="sxs-lookup"><span data-stu-id="b5c76-119">**IMediaDet::get\_StreamType**</span></span>](imediadet-get-streamtype.md)

<span data-ttu-id="b5c76-120">Чтобы получить кадр видео, вызовите метод [**имедиадет:: жетбитмапбитс**](imediadet-getbitmapbits.md) или [**Имедиадет:: вритебитмапбитс**](imediadet-writebitmapbits.md).</span><span class="sxs-lookup"><span data-stu-id="b5c76-120">To retrieve a video frame, call [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md).</span></span> <span data-ttu-id="b5c76-121">Возвращаемый кадр всегда находится в 24-разрядном формате RGB.</span><span class="sxs-lookup"><span data-stu-id="b5c76-121">The returned frame is always in 24-bit RGB format.</span></span>

> [!Note]  
> <span data-ttu-id="b5c76-122">Не используйте один и тот же объект Медиадет с несколькими файлами.</span><span class="sxs-lookup"><span data-stu-id="b5c76-122">Do not use the same MediaDet object with multiple files.</span></span> <span data-ttu-id="b5c76-123">Чтобы получить информацию или видеокадры из нескольких файлов, используйте отдельные экземпляры Медиадет.</span><span class="sxs-lookup"><span data-stu-id="b5c76-123">To get information or video frames from more than one file, use separate MediaDet instances.</span></span>

 

<span data-ttu-id="b5c76-124">Интерфейс **имедиадет** не поддерживает форматы [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , поэтому этот интерфейс нельзя использовать для получения полей с чередованием или сведений о чересстрочную развертке.</span><span class="sxs-lookup"><span data-stu-id="b5c76-124">The **IMediaDet** interface does not support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats, so you cannot use this interface to get interlaced fields or information about interlacing.</span></span> <span data-ttu-id="b5c76-125">Кроме того, если вышестоящий декодер поддерживает только **VIDEOINFOHEADER2**, нельзя использовать `IMediaDet` .</span><span class="sxs-lookup"><span data-stu-id="b5c76-125">Also, if the upstream decoder supports only **VIDEOINFOHEADER2**, you cannot use `IMediaDet`.</span></span> <span data-ttu-id="b5c76-126">Это может быть, например, с помощью декодера MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="b5c76-126">This might be the case with an MPEG-2 decoder, for example.</span></span> <span data-ttu-id="b5c76-127">Кроме того, `IMediaDet` интерфейс игнорирует любые потоки в файле, которые не являются видео или аудио.</span><span class="sxs-lookup"><span data-stu-id="b5c76-127">Also, the `IMediaDet` interface ignores any streams in the file that are not video or audio.</span></span> <span data-ttu-id="b5c76-128">Например, если файл содержит аудио-поток, поток данных и видеопоток, метод **Get \_ аутпутстреамс** будет сообщать только о двух потоках (аудио и видео).</span><span class="sxs-lookup"><span data-stu-id="b5c76-128">For example, if the file contains an audio stream, a data stream, and a video stream, the **get\_OutputStreams** method will report only two streams (the audio and video).</span></span>

## <a name="members"></a><span data-ttu-id="b5c76-129">Элементы</span><span class="sxs-lookup"><span data-stu-id="b5c76-129">Members</span></span>

<span data-ttu-id="b5c76-130">Интерфейс **имедиадет** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b5c76-130">The **IMediaDet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b5c76-131">**Имедиадет** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b5c76-131">**IMediaDet** also has these types of members:</span></span>

-   [<span data-ttu-id="b5c76-132">Методы</span><span class="sxs-lookup"><span data-stu-id="b5c76-132">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b5c76-133">Методы</span><span class="sxs-lookup"><span data-stu-id="b5c76-133">Methods</span></span>

<span data-ttu-id="b5c76-134">Интерфейс **имедиадет** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b5c76-134">The **IMediaDet** interface has these methods.</span></span>



| <span data-ttu-id="b5c76-135">Метод</span><span class="sxs-lookup"><span data-stu-id="b5c76-135">Method</span></span>                                                        | <span data-ttu-id="b5c76-136">Описание</span><span class="sxs-lookup"><span data-stu-id="b5c76-136">Description</span></span>                                                                                                |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5c76-137">**ентербитмапграбмоде**</span><span class="sxs-lookup"><span data-stu-id="b5c76-137">**EnterBitmapGrabMode**</span></span>](imediadet-enterbitmapgrabmode.md)  | <span data-ttu-id="b5c76-138">Переключает детектор мультимедиа в режим захвата точечного рисунка и выполняет поиск графа фильтра в указанное время.</span><span class="sxs-lookup"><span data-stu-id="b5c76-138">Switches the media detector to bitmap grab mode and seeks the filter graph to a specified time.</span></span><br/> |
| [<span data-ttu-id="b5c76-139">**получить \_ куррентстреам**</span><span class="sxs-lookup"><span data-stu-id="b5c76-139">**get\_CurrentStream**</span></span>](imediadet-get-currentstream.md)     | <span data-ttu-id="b5c76-140">Возвращает номер потока, который в настоящее время используется средством обнаружения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b5c76-140">Retrieves the stream number currently used by the media detector.</span></span><br/>                               |
| [<span data-ttu-id="b5c76-141">**получить \_ имя файла**</span><span class="sxs-lookup"><span data-stu-id="b5c76-141">**get\_Filename**</span></span>](imediadet-get-filename.md)               | <span data-ttu-id="b5c76-142">Получает имя исходного файла, который в настоящее время используется средством обнаружения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b5c76-142">Retrieves the name of the source file currently used by the media detector.</span></span><br/>                     |
| [<span data-ttu-id="b5c76-143">**получить \_ Фильтр**</span><span class="sxs-lookup"><span data-stu-id="b5c76-143">**get\_Filter**</span></span>](imediadet-get-filter.md)                   | <span data-ttu-id="b5c76-144">Получает указатель на фильтр источника, используемый в настоящий момент средством обнаружения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b5c76-144">Retrieves a pointer to the source filter currently used by the media detector.</span></span><br/>                  |
| [<span data-ttu-id="b5c76-145">**получить частоту \_ кадров**</span><span class="sxs-lookup"><span data-stu-id="b5c76-145">**get\_FrameRate**</span></span>](imediadet-get-framerate.md)             | <span data-ttu-id="b5c76-146">Возвращает частоту кадров текущего потока.</span><span class="sxs-lookup"><span data-stu-id="b5c76-146">Retrieves the frame rate of the current stream.</span></span><br/>                                                 |
| [<span data-ttu-id="b5c76-147">**получить \_ аутпутстреамс**</span><span class="sxs-lookup"><span data-stu-id="b5c76-147">**get\_OutputStreams**</span></span>](imediadet-get-outputstreams.md)     | <span data-ttu-id="b5c76-148">Возвращает количество аудио и видеопотоков, содержащихся в источнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b5c76-148">Retrieves the number of audio and video streams contained in the media source.</span></span><br/>                  |
| [<span data-ttu-id="b5c76-149">**получить \_ стреамленгс**</span><span class="sxs-lookup"><span data-stu-id="b5c76-149">**get\_StreamLength**</span></span>](imediadet-get-streamlength.md)       | <span data-ttu-id="b5c76-150">Возвращает длительность текущего потока.</span><span class="sxs-lookup"><span data-stu-id="b5c76-150">Retrieves the duration of the current stream.</span></span><br/>                                                   |
| [<span data-ttu-id="b5c76-151">**получить \_ стреаммедиатипе**</span><span class="sxs-lookup"><span data-stu-id="b5c76-151">**get\_StreamMediaType**</span></span>](imediadet-get-streammediatype.md) | <span data-ttu-id="b5c76-152">Возвращает тип носителя текущего потока.</span><span class="sxs-lookup"><span data-stu-id="b5c76-152">Retrieves the media type of the current stream.</span></span><br/>                                                 |
| [<span data-ttu-id="b5c76-153">**получить \_ стреамтипе**</span><span class="sxs-lookup"><span data-stu-id="b5c76-153">**get\_StreamType**</span></span>](imediadet-get-streamtype.md)           | <span data-ttu-id="b5c76-154">Получает глобальный уникальный идентификатор (GUID) для типа носителя текущего потока.</span><span class="sxs-lookup"><span data-stu-id="b5c76-154">Retrieves the globally unique identifier (GUID) for the media type of the current stream.</span></span><br/>       |
| [<span data-ttu-id="b5c76-155">**получить \_ стреамтипеб**</span><span class="sxs-lookup"><span data-stu-id="b5c76-155">**get\_StreamTypeB**</span></span>](imediadet-get-streamtypeb.md)         | <span data-ttu-id="b5c76-156">Извлекает строку, представляющую идентификатор GUID типа носителя для текущего потока.</span><span class="sxs-lookup"><span data-stu-id="b5c76-156">Retrieves a string representing the GUID of the media type for the current stream.</span></span><br/>              |
| [<span data-ttu-id="b5c76-157">**жетбитмапбитс**</span><span class="sxs-lookup"><span data-stu-id="b5c76-157">**GetBitmapBits**</span></span>](imediadet-getbitmapbits.md)              | <span data-ttu-id="b5c76-158">Извлекает кадр видео в указанное время носителя.</span><span class="sxs-lookup"><span data-stu-id="b5c76-158">Retrieves a video frame at the specified media time.</span></span><br/>                                            |
| [<span data-ttu-id="b5c76-159">**жетсамплеграббер**</span><span class="sxs-lookup"><span data-stu-id="b5c76-159">**GetSampleGrabber**</span></span>](imediadet-getsamplegrabber.md)        | <span data-ttu-id="b5c76-160">Получает указатель на интерфейс [**исамплеграббер**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="b5c76-160">Retrieves a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span><br/>                  |
| [<span data-ttu-id="b5c76-161">**разместить \_ куррентстреам**</span><span class="sxs-lookup"><span data-stu-id="b5c76-161">**put\_CurrentStream**</span></span>](imediadet-put-currentstream.md)     | <span data-ttu-id="b5c76-162">Указывает номер потока для использования средством обнаружения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b5c76-162">Specifies the stream number for the media detector to use.</span></span><br/>                                      |
| [<span data-ttu-id="b5c76-163">**вставить \_ имя файла**</span><span class="sxs-lookup"><span data-stu-id="b5c76-163">**put\_Filename**</span></span>](imediadet-put-filename.md)               | <span data-ttu-id="b5c76-164">Указывает имя исходного файла, в котором будет использоваться средство обнаружения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b5c76-164">Specifies the name of the source file for the media detector to use.</span></span><br/>                            |
| [<span data-ttu-id="b5c76-165">**разместить \_ Фильтр**</span><span class="sxs-lookup"><span data-stu-id="b5c76-165">**put\_Filter**</span></span>](imediadet-put-filter.md)                   | <span data-ttu-id="b5c76-166">Задает фильтр источника для использования средством обнаружения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b5c76-166">Specifies a source filter for the media detector to use.</span></span><br/>                                        |
| [<span data-ttu-id="b5c76-167">**вритебитмапбитс**</span><span class="sxs-lookup"><span data-stu-id="b5c76-167">**WriteBitmapBits**</span></span>](imediadet-writebitmapbits.md)          | <span data-ttu-id="b5c76-168">Извлекает кадр видео в указанное время мультимедиа и записывает его в файл.</span><span class="sxs-lookup"><span data-stu-id="b5c76-168">Retrieves a video frame at the specified media time and writes it to a file.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="b5c76-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5c76-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b5c76-170">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="b5c76-170">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b5c76-171">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b5c76-171">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b5c76-172">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="b5c76-172">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b5c76-173">Требования</span><span class="sxs-lookup"><span data-stu-id="b5c76-173">Requirements</span></span>



| <span data-ttu-id="b5c76-174">Требование</span><span class="sxs-lookup"><span data-stu-id="b5c76-174">Requirement</span></span> | <span data-ttu-id="b5c76-175">Значение</span><span class="sxs-lookup"><span data-stu-id="b5c76-175">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5c76-176">Header</span><span class="sxs-lookup"><span data-stu-id="b5c76-176">Header</span></span><br/>  | <dl> <span data-ttu-id="b5c76-177"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5c76-177"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b5c76-178">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b5c76-178">Library</span></span><br/> | <dl> <span data-ttu-id="b5c76-179"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5c76-179"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
