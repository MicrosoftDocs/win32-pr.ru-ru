---
description: Дескрипторы представления
ms.assetid: 714c8bda-5ce1-47e2-ba73-9304e26b3129
title: Дескрипторы представления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f1581e35fe6d875c691efdd5ef5736c1aa5215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673462"
---
# <a name="presentation-descriptors"></a><span data-ttu-id="2f30c-103">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="2f30c-103">Presentation Descriptors</span></span>

<span data-ttu-id="2f30c-104">*Презентация* — это набор связанных потоков мультимедиа с общим временем презентации.</span><span class="sxs-lookup"><span data-stu-id="2f30c-104">A *presentation* is a set of related media streams that share a common presentation time.</span></span> <span data-ttu-id="2f30c-105">Например, презентация может состоять из видеопотоков и аудио-видео из фильма.</span><span class="sxs-lookup"><span data-stu-id="2f30c-105">For example, a presentation might consist of the audio and video streams from a movie.</span></span> <span data-ttu-id="2f30c-106">*Дескриптор представления* — это объект, содержащий описание конкретной презентации.</span><span class="sxs-lookup"><span data-stu-id="2f30c-106">A *presentation descriptor* is an object that contains the description of a particular presentation.</span></span> <span data-ttu-id="2f30c-107">Дескрипторы презентации используются для настройки источников мультимедиа и некоторых приемников мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2f30c-107">Presentation descriptors are used to configure media sources and some media sinks.</span></span>

<span data-ttu-id="2f30c-108">Каждый дескриптор презентации содержит список из одного или нескольких *потоковых дескрипторов*.</span><span class="sxs-lookup"><span data-stu-id="2f30c-108">Each presentation descriptor contains a list of one or more *stream descriptors*.</span></span> <span data-ttu-id="2f30c-109">Они описывают потоки в презентации.</span><span class="sxs-lookup"><span data-stu-id="2f30c-109">These describe the streams in the presentation.</span></span> <span data-ttu-id="2f30c-110">Можно выбрать или отменить выбор потоков.</span><span class="sxs-lookup"><span data-stu-id="2f30c-110">Streams can be either selected or deselected.</span></span> <span data-ttu-id="2f30c-111">Данные создаются только выбранными потоками.</span><span class="sxs-lookup"><span data-stu-id="2f30c-111">Only the selected streams produce data.</span></span> <span data-ttu-id="2f30c-112">Невыбранные потоки не являются активными и не создают никаких данных.</span><span class="sxs-lookup"><span data-stu-id="2f30c-112">Deselected streams are not active and do not produce any data.</span></span> <span data-ttu-id="2f30c-113">Каждый дескриптор потока имеет *обработчик типа мультимедиа*, который используется для изменения типа носителя потока или получения текущего типа мультимедиа потока.</span><span class="sxs-lookup"><span data-stu-id="2f30c-113">Each stream descriptor has a *media type handler*, which is used to change the stream's media type or get the stream's current media type.</span></span> <span data-ttu-id="2f30c-114">(Дополнительные сведения о типах носителей см. в разделе [типы носителей](media-types.md).)</span><span class="sxs-lookup"><span data-stu-id="2f30c-114">(For more information about media types, see [Media Types](media-types.md).)</span></span>

<span data-ttu-id="2f30c-115">В следующей таблице показаны основные интерфейсы, предоставляемые каждым из этих объектов.</span><span class="sxs-lookup"><span data-stu-id="2f30c-115">The following table shows the primary interfaces that each of these objects exposes.</span></span>



| <span data-ttu-id="2f30c-116">Объект</span><span class="sxs-lookup"><span data-stu-id="2f30c-116">Object</span></span>                  | <span data-ttu-id="2f30c-117">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="2f30c-117">Interface</span></span>                                                      |
|-------------------------|----------------------------------------------------------------|
| <span data-ttu-id="2f30c-118">Дескриптор представления</span><span class="sxs-lookup"><span data-stu-id="2f30c-118">Presentation descriptor</span></span> | [<span data-ttu-id="2f30c-119">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="2f30c-119">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) |
| <span data-ttu-id="2f30c-120">Дескриптор потока</span><span class="sxs-lookup"><span data-stu-id="2f30c-120">Stream descriptor</span></span>       | [<span data-ttu-id="2f30c-121">**имфстреамдескриптор**</span><span class="sxs-lookup"><span data-stu-id="2f30c-121">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)             |
| <span data-ttu-id="2f30c-122">Обработчик типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="2f30c-122">Media type handler</span></span>      | [<span data-ttu-id="2f30c-123">**имфмедиатипехандлер**</span><span class="sxs-lookup"><span data-stu-id="2f30c-123">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)             |



 

## <a name="media-source-presentations"></a><span data-ttu-id="2f30c-124">Презентации источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="2f30c-124">Media Source Presentations</span></span>

<span data-ttu-id="2f30c-125">Каждый источник мультимедиа предоставляет дескриптор представления, описывающий конфигурацию по умолчанию для источника.</span><span class="sxs-lookup"><span data-stu-id="2f30c-125">Every media source provides a presentation descriptor that describes the default configuration for the source.</span></span> <span data-ttu-id="2f30c-126">В конфигурации по умолчанию выбран по крайней мере один поток, и каждый выбранный поток имеет тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2f30c-126">In the default configuration, at least one stream is selected, and every selected stream has a media type.</span></span> <span data-ttu-id="2f30c-127">Чтобы получить дескриптор презентации, вызовите метод [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="2f30c-127">To get the presentation descriptor, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="2f30c-128">Метод возвращает указатель [**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="2f30c-128">The method returns an [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pointer.</span></span>

<span data-ttu-id="2f30c-129">Вы можете изменить дескриптор представления исходного кода, чтобы выбрать другой набор потоков.</span><span class="sxs-lookup"><span data-stu-id="2f30c-129">You can modify the source's presentation descriptor to select a different set of streams.</span></span> <span data-ttu-id="2f30c-130">Не изменяйте дескриптор представления, если источник мультимедиа не остановлен.</span><span class="sxs-lookup"><span data-stu-id="2f30c-130">Do not modify the presentation descriptor unless the media source is stopped.</span></span> <span data-ttu-id="2f30c-131">Изменения применяются при вызове [**имфмедиасаурце:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) для запуска источника.</span><span class="sxs-lookup"><span data-stu-id="2f30c-131">The changes are applied when you call [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) to start the source.</span></span>

<span data-ttu-id="2f30c-132">Чтобы получить количество потоков, вызовите метод [**имфпресентатиондескриптор:: жетстреамдескрипторкаунт**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount).</span><span class="sxs-lookup"><span data-stu-id="2f30c-132">To get the number of streams, call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount).</span></span> <span data-ttu-id="2f30c-133">Чтобы получить дескриптор потока для потока, вызовите метод [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) и передайте индекс потока.</span><span class="sxs-lookup"><span data-stu-id="2f30c-133">To get the stream descriptor for a stream, call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) and pass in the index of the stream.</span></span> <span data-ttu-id="2f30c-134">Потоки индексируются с нуля.</span><span class="sxs-lookup"><span data-stu-id="2f30c-134">Streams are indexed from zero.</span></span> <span data-ttu-id="2f30c-135">Метод **жетстреамдескрипторбиндекс** возвращает указатель [**имфстреамдескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="2f30c-135">The **GetStreamDescriptorByIndex** method returns an [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) pointer.</span></span> <span data-ttu-id="2f30c-136">Он также возвращает логический флаг, указывающий, выбран ли поток.</span><span class="sxs-lookup"><span data-stu-id="2f30c-136">It also returns a Boolean flag indicating whether the stream is selected.</span></span> <span data-ttu-id="2f30c-137">Если выбран поток, источник мультимедиа создает данные для этого потока.</span><span class="sxs-lookup"><span data-stu-id="2f30c-137">If the stream is selected, the media source produces data for that stream.</span></span> <span data-ttu-id="2f30c-138">В противном случае источник не создает никаких данных для этого потока.</span><span class="sxs-lookup"><span data-stu-id="2f30c-138">Otherwise, the source does not produce any data for that stream.</span></span> <span data-ttu-id="2f30c-139">Чтобы выбрать поток, вызовите [**имфпресентатиондескриптор:: селектстреам**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) с индексом потока.</span><span class="sxs-lookup"><span data-stu-id="2f30c-139">To select a stream, call [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) with the index of the stream.</span></span> <span data-ttu-id="2f30c-140">Чтобы отменить выбор потока, вызовите [**имфпресентатиондескриптор::D еселектстреам**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span><span class="sxs-lookup"><span data-stu-id="2f30c-140">To deselect a stream, call [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span></span>

<span data-ttu-id="2f30c-141">В следующем коде показано, как получить дескриптор представления из источника мультимедиа и перечислить потоки.</span><span class="sxs-lookup"><span data-stu-id="2f30c-141">The following code shows how to get the presentation descriptor from a media source and enumerate the streams.</span></span>


```C++
HRESULT hr = S_OK;
DWORD cStreams = 0;
BOOL  fSelected = FALSE;

IMFPresentationDescriptor *pPresentation = NULL;
IMFStreamDescriptor *pStreamDesc = NULL;

hr = pSource->CreatePresentationDescriptor(&pPresentation);

if (SUCCEEDED(hr))
{
    hr = pPresentation->GetStreamDescriptorCount(&cStreams);
}

if (SUCCEEDED(hr))
{
    for (DWORD iStream = 0; iStream < cStreams; iStream++)
    {
        hr = pPresentation->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);

        if (FAILED(hr))
        {
            break;
        }

        /*  Use the stream descriptor. (Not shown.) */

        SAFE_RELEASE(pStreamDesc);
    }
}
SAFE_RELEASE(pPresentation);
SAFE_RELEASE(pStreamDesc);
```



## <a name="media-type-handlers"></a><span data-ttu-id="2f30c-142">Обработчики типов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="2f30c-142">Media Type Handlers</span></span>

<span data-ttu-id="2f30c-143">Чтобы изменить тип носителя потока или получить текущий тип мультимедиа потока, используйте обработчик типа мультимедиа дескриптора потока.</span><span class="sxs-lookup"><span data-stu-id="2f30c-143">To change the stream's media type or to get the stream's current media type, use the stream descriptor's media type handler.</span></span> <span data-ttu-id="2f30c-144">Вызовите метод [**имфстреамдескриптор:: жетмедиатипехандлер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) , чтобы получить обработчик типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2f30c-144">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) to get the media type handler.</span></span> <span data-ttu-id="2f30c-145">Этот метод возвращает указатель [**имфмедиатипехандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) .</span><span class="sxs-lookup"><span data-stu-id="2f30c-145">This method returns an [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) pointer.</span></span>

<span data-ttu-id="2f30c-146">Если нужно просто узнать, какой тип данных находится в потоке, например в аудио или видео, вызовите [**имфмедиатипехандлер:: жетмажортипе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span><span class="sxs-lookup"><span data-stu-id="2f30c-146">If you simply want to know what kind of data is in the stream, such as audio or video, call [**IMFMediaTypeHandler::GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span></span> <span data-ttu-id="2f30c-147">Этот метод возвращает идентификатор GUID для основного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="2f30c-147">This method returns the GUID for the major media type.</span></span> <span data-ttu-id="2f30c-148">Например, приложение воспроизведения обычно подключает звуковой поток к обработчику звука и видеопотоку для модуля подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="2f30c-148">For example, a playback application typically connects an audio stream to the audio renderer and a video stream to the video renderer.</span></span> <span data-ttu-id="2f30c-149">При использовании сеанса мультимедиа или загрузчика топологии для создания топологии основной GUID типа может быть единственным нужным вам сведениям о форматировании.</span><span class="sxs-lookup"><span data-stu-id="2f30c-149">If you use the Media Session or the topology loader to build a topology, the major type GUID might be the only format information that you need.</span></span>

<span data-ttu-id="2f30c-150">Если приложению требуются более подробные сведения о текущем формате, вызовите [**имфмедиатипехандлер:: жеткуррентмедиатипе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype).</span><span class="sxs-lookup"><span data-stu-id="2f30c-150">If your application needs more detailed information about the current format, call [**IMFMediaTypeHandler::GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype).</span></span> <span data-ttu-id="2f30c-151">Этот метод возвращает указатель на интерфейс [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2f30c-151">This method returns a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface of the media type.</span></span> <span data-ttu-id="2f30c-152">Используйте этот интерфейс для получения сведений о формате.</span><span class="sxs-lookup"><span data-stu-id="2f30c-152">Use this interface to get the details of the format.</span></span>

<span data-ttu-id="2f30c-153">Обработчик типа мультимедиа также содержит список поддерживаемых типов носителей для потока.</span><span class="sxs-lookup"><span data-stu-id="2f30c-153">The media type handler also contains a list of supported media types for the stream.</span></span> <span data-ttu-id="2f30c-154">Чтобы получить размер списка, вызовите метод [**имфмедиатипехандлер:: жетмедиатипекаунт**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount).</span><span class="sxs-lookup"><span data-stu-id="2f30c-154">To get the size of the list, call [**IMFMediaTypeHandler::GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount).</span></span> <span data-ttu-id="2f30c-155">Чтобы получить тип мультимедиа из списка, вызовите [**имфмедиатипехандлер:: жетмедиатипебиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) с индексом типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2f30c-155">To get a media type from the list, call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) with the index of the media type.</span></span> <span data-ttu-id="2f30c-156">Типы носителей возвращаются в порядке приближения к приоритету.</span><span class="sxs-lookup"><span data-stu-id="2f30c-156">Media types are returned in the approximate order of preference.</span></span> <span data-ttu-id="2f30c-157">Например, для звуковых форматов предпочтительнее использовать более высокие скорости выборки по сравнению с более низкими тарифами.</span><span class="sxs-lookup"><span data-stu-id="2f30c-157">For example, for audio formats, higher sample rates are preferred over lower sample rates.</span></span> <span data-ttu-id="2f30c-158">Однако нет правила, определяющего порядок, поэтому его следует рассматривать как правило.</span><span class="sxs-lookup"><span data-stu-id="2f30c-158">However, there is no definitive rule that governs the ordering, so you should treat it simply as a guideline.</span></span>

<span data-ttu-id="2f30c-159">Список поддерживаемых типов может не содержать все возможные типы носителей, поддерживаемые потоком.</span><span class="sxs-lookup"><span data-stu-id="2f30c-159">The list of supported types might not contain every possible media type that the stream supports.</span></span> <span data-ttu-id="2f30c-160">Чтобы проверить, поддерживается ли определенный тип носителя, вызовите метод [**имфмедиатипехандлер:: исмедиатипесуппортед**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported).</span><span class="sxs-lookup"><span data-stu-id="2f30c-160">To test whether a particular media type is supported, call [**IMFMediaTypeHandler::IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported).</span></span> <span data-ttu-id="2f30c-161">Чтобы задать тип мультимедиа, вызовите [**имфмедиатипехандлер:: сеткуррентмедиатипе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype).</span><span class="sxs-lookup"><span data-stu-id="2f30c-161">To set the media type, call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype).</span></span> <span data-ttu-id="2f30c-162">Если метод завершится с ошибкой, поток будет содержать данные, которые соответствует указанному формату.</span><span class="sxs-lookup"><span data-stu-id="2f30c-162">If the method succeeds, the stream will contain data that conforms to the specified format.</span></span> <span data-ttu-id="2f30c-163">Метод **сеткуррентмедиатипе** не изменяет список предпочтительных типов.</span><span class="sxs-lookup"><span data-stu-id="2f30c-163">The **SetCurrentMediaType** method does not change the list of preferred types.</span></span>

<span data-ttu-id="2f30c-164">В следующем коде показано, как получить обработчик типа мультимедиа, перечислить предпочтительные типы мультимедиа и задать тип носителя.</span><span class="sxs-lookup"><span data-stu-id="2f30c-164">The following code shows how to get the media type handler, enumerate the preferred media types, and set the media type.</span></span> <span data-ttu-id="2f30c-165">В этом примере предполагается, что приложение имеет некоторый алгоритм, не показанный здесь, для выбора типа носителя.</span><span class="sxs-lookup"><span data-stu-id="2f30c-165">This example assumes that the application has some algorithm, not shown here, for selecting the media type.</span></span> <span data-ttu-id="2f30c-166">Конкретные особенности будут сильно зависеть от вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="2f30c-166">The specifics will depend greatly on your application.</span></span>


```C++
HRESULT hr = S_OK;
DWORD cTypes = 0;
BOOL  bTypeOK = FALSE;

IMFMediaTypeHandler *pHandler = NULL;
IMFMediaType *pMediaType = NULL;

hr = pStreamDesc->GetMediaTypeHandler(&pHandler);

if (SUCCEEDED(hr))
{
    hr = pHandler->GetMediaTypeCount(&cTypes);
}

if (SUCCEEDED(hr))
{
    for (DWORD iType = 0; iType < cTypes; iType++)
    {   
        hr = pHandler->GetMediaTypeByIndex(iType, &pMediaType);

        if (FAILED(hr))
        {
            break;
        }

        /* Examine the media type. (Not shown.)  */

        /* If this media type is acceptable, set the media type. */

        if (bTypeOK)
        {
            hr = pHandler->SetCurrentMediaType(pMediaType);
            break;
        }

        SAFE_RELEASE(pMediaType);
    }
}    

SAFE_RELEASE(pMediaType);
SAFE_RELEASE(pHandler);
```



## <a name="related-topics"></a><span data-ttu-id="2f30c-167">См. также</span><span class="sxs-lookup"><span data-stu-id="2f30c-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f30c-168">Источники мультимедиа</span><span class="sxs-lookup"><span data-stu-id="2f30c-168">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="2f30c-169">Media Foundation API платформы</span><span class="sxs-lookup"><span data-stu-id="2f30c-169">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



