---
description: В этой статье представлено несколько простых примеров, иллюстрирующих способы реализации пространственного звука с помощью статических пространственных объектов, динамических пространственных объектов и пространственных звуковых объектов, использующих функцию относительных функций Microsoft Head (ХРТФ).
ms.assetid: C99C342E-0BD9-486A-92AA-F8DCB72C1B00
title: Отображение пространственного звука с помощью пространственных звуковых объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd541026aa3e144ec8333c8ac045a17970735f17
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807559"
---
# <a name="render-spatial-sound-using-spatial-audio-objects"></a><span data-ttu-id="e7fdc-103">Отображение пространственного звука с помощью пространственных звуковых объектов</span><span class="sxs-lookup"><span data-stu-id="e7fdc-103">Render Spatial Sound Using Spatial Audio Objects</span></span>

<span data-ttu-id="e7fdc-104">В этой статье представлено несколько простых примеров, иллюстрирующих способы реализации пространственного звука с помощью статических пространственных объектов, динамических пространственных объектов и пространственных звуковых объектов, использующих функцию относительных функций Microsoft Head (ХРТФ).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-104">This article presents some simple examples that illustrate how to implement spatial sound using static spatial audio objects, dynamic spatial audio objects, and spatial audio objects that use Microsoft's Head Relative Transfer Function (HRTF).</span></span> <span data-ttu-id="e7fdc-105">Этапы реализации всех трех методов очень похожи, и в этой статье представлен пример кода для каждого метода.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-105">The implementation steps for all three of these techniques are very similar and this article provides a similarly structured code example for each technique.</span></span> <span data-ttu-id="e7fdc-106">Полный комплексный пример использования пространственных данных для работы с пространственными данными см. в [статье репозиторий GitHub с пространственными звуковыми](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio)данными (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-106">For complete end-to-end examples of real-world spatial audio implementations, see [Microsoft Spatial Sound samples github repository](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio).</span></span> <span data-ttu-id="e7fdc-107">Обзор решения Windows Sonic на уровне платформы для поддержки пространственного звука в Xbox и Windows см. в статье [Пространственный звук](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-107">For an overview of Windows Sonic, Microsoft’s platform-level solution for spatial sound support on Xbox and Windows, see [Spatial Sound](spatial-sound.md).</span></span>

## <a name="render-audio-using-static-spatial-audio-objects"></a><span data-ttu-id="e7fdc-108">Прорисовка звука с помощью статических пространственных объектов Audio</span><span class="sxs-lookup"><span data-stu-id="e7fdc-108">Render audio using static spatial audio objects</span></span>

<span data-ttu-id="e7fdc-109">Статический звуковой объект используется для визуализации звука по одному из 18 статических звуковых каналов, определенных в перечислении [**аудиубжекттипе**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) .</span><span class="sxs-lookup"><span data-stu-id="e7fdc-109">A static audio object is used to render sound to one of 18 static audio channels defined in the [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) enumeration.</span></span> <span data-ttu-id="e7fdc-110">Каждый из этих каналов представляет реальный или виртуализованный динамик в фиксированной точке, которая не перемещается со временем.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-110">Each of these channels represents a real or virtualized speaker at a fixed point in space that does not move over time.</span></span> <span data-ttu-id="e7fdc-111">Статические каналы, доступные на конкретном устройстве, зависят от используемого пространственного звукового формата.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-111">The static channels that are available on a particular device depend on the spatial sound format being used.</span></span> <span data-ttu-id="e7fdc-112">Список поддерживаемых форматов и их количества каналов см. в разделе [Пространственный звук](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-112">For a list of the supported formats and their channel counts, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="e7fdc-113">При инициализации пространственного аудиопотока необходимо указать, какие из доступных статических каналов будут использоваться потоком.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-113">When you initialize a spatial audio stream, you must specify which of the available static channels the stream will use.</span></span> <span data-ttu-id="e7fdc-114">Приведенные ниже примеры определений констант можно использовать для указания общих конфигураций динамиков и получения числа доступных каналов для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-114">The following example constant definitions can be used to specify common speaker configurations and get the number of channels available for each one.</span></span>


```C++
const AudioObjectType ChannelMask_Mono = AudioObjectType_FrontCenter;
const AudioObjectType ChannelMask_Stereo = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight);
const AudioObjectType ChannelMask_2_1 = (AudioObjectType)(ChannelMask_Stereo | AudioObjectType_LowFrequency);
const AudioObjectType ChannelMask_Quad = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight | AudioObjectType_BackLeft | AudioObjectType_BackRight);
const AudioObjectType ChannelMask_4_1 = (AudioObjectType)(ChannelMask_Quad | AudioObjectType_LowFrequency);
const AudioObjectType ChannelMask_5_1 = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight | AudioObjectType_FrontCenter | AudioObjectType_LowFrequency | AudioObjectType_SideLeft | AudioObjectType_SideRight);
const AudioObjectType ChannelMask_7_1 = (AudioObjectType)(ChannelMask_5_1 | AudioObjectType_BackLeft | AudioObjectType_BackRight);

const UINT32 MaxStaticObjectCount_7_1_4 = 12;
const AudioObjectType ChannelMask_7_1_4 = (AudioObjectType)(ChannelMask_7_1 | AudioObjectType_TopFrontLeft | AudioObjectType_TopFrontRight | AudioObjectType_TopBackLeft | AudioObjectType_TopBackRight);

const UINT32 MaxStaticObjectCount_7_1_4_4 = 16;
const AudioObjectType ChannelMask_7_1_4_4 = (AudioObjectType)(ChannelMask_7_1_4 | AudioObjectType_BottomFrontLeft | AudioObjectType_BottomFrontRight |AudioObjectType_BottomBackLeft | AudioObjectType_BottomBackRight);

const UINT32 MaxStaticObjectCount_8_1_4_4 = 17;
const AudioObjectType ChannelMask_8_1_4_4 = (AudioObjectType)(ChannelMask_7_1_4_4 | AudioObjectType_BackCenter);
```



<span data-ttu-id="e7fdc-115">Первым шагом при отрисовке пространственного аудио является получение конечной точки аудио, в которую будут отправляться звуковые данные.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-115">The first step in rendering spatial audio is to get the audio endpoint to which audio data will be sent.</span></span> <span data-ttu-id="e7fdc-116">Создайте экземпляр [**ммдевицеенумератор**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) и вызовите [**жетдефаултаудиоендпоинт**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) , чтобы получить устройство рендеринга звука по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-116">Create an instance of [**MMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) and call [**GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) to get the default audio render device.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="e7fdc-117">При создании пространственного аудиопотока необходимо указать формат звука, который будет использоваться потоком, предоставив структуру [вавеформатекс](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="e7fdc-117">When you create a spatial audio stream, you must specify the audio format the stream will use by providing a [WAVEFORMATEX](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) structure.</span></span> <span data-ttu-id="e7fdc-118">При воспроизведении звука из файла формат обычно определяется форматом звукового файла.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-118">If you are playing back audio from a file, the format is typically determined by the audio file format.</span></span> <span data-ttu-id="e7fdc-119">В этом примере используется формат Mono, 32-bit, 48Hz.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-119">This example uses a mono, 32-bit, 48Hz format.</span></span>


```C++
WAVEFORMATEX format;
format.wFormatTag = WAVE_FORMAT_IEEE_FLOAT;
format.wBitsPerSample = 32;
format.nChannels = 1;
format.nSamplesPerSec = 48000;
format.nBlockAlign = (format.wBitsPerSample >> 3) * format.nChannels;
format.nAvgBytesPerSec = format.nBlockAlign * format.nSamplesPerSec;
format.cbSize = 0;
```



<span data-ttu-id="e7fdc-120">Следующим шагом при подготовке пространственного звука является инициализация пространственного аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-120">The next step in rendering spatial audio is to initialize a spatial audio stream.</span></span> <span data-ttu-id="e7fdc-121">Сначала получите экземпляр [**испатиалаудиоклиент**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) , вызвав [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-121">First, get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="e7fdc-122">Вызовите метод [**испатиалаудиоклиент:: исаудиубжектформатсуппортед**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) , чтобы обеспечить поддержку формата звука, который вы используете.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-122">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="e7fdc-123">Создайте событие, которое будет использоваться конвейером аудиопотока для уведомления приложения о том, что оно готово для дополнительных звуковых данных.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-123">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="e7fdc-124">Заполнение структуры [**спатиалаудиубжектрендерстреамактиватионпарамс**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) , которая будет использоваться для инициализации пространственного аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-124">Populate a [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) structure that will be used to initialize the spatial audio stream.</span></span> <span data-ttu-id="e7fdc-125">В этом примере в поле **статикобжекттипемаск** задана константа **\_ стерео чаннелмаск** , определенная ранее в этой статье, что означает, что аудиопоток может использовать только передний правый и левый каналы.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-125">In this example, the **StaticObjectTypeMask** field is set to the **ChannelMask\_Stereo** constant defined previously in this article, meaning that only the front right and left channels can be used by the audio stream.</span></span> <span data-ttu-id="e7fdc-126">Поскольку в этом примере используются только статические аудио-объекты и нет динамических объектов, поле **максдинамикобжекткаунт** имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-126">Because this example uses only static audio objects and no dynamic objects, the **MaxDynamicObjectCount** field is set to 0.</span></span> <span data-ttu-id="e7fdc-127">Полю **Category** присваивается значение члена перечисления [**\_ \_ категории аудиопотока**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) , которое определяет, как система смешивает звук из этого потока с другими звуковыми источниками.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-127">The **Category** field is set to a member of the [**AUDIO\_STREAM\_CATEGORY**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) enumeration, which defines how the system mixes the sound from this stream with other audio sources.</span></span>

<span data-ttu-id="e7fdc-128">Вызовите метод [**испатиалаудиоклиент:: активатеспатиалаудиостреам**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) , чтобы активировать поток.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-128">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


```C++
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;

// Activate ISpatialAudioClient on the desired audio-device 
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

SpatialAudioObjectRenderStreamActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = ChannelMask_Stereo;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = 0;
streamParams.Category = AudioCategory_SoundEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = nullptr;

PROPVARIANT activationParams;
PropVariantInit(&activationParams);
activationParams.vt = VT_BLOB;
activationParams.blob.cbSize = sizeof(streamParams);
activationParams.blob.pBlobData = reinterpret_cast<BYTE *>(&streamParams);

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStream> spatialAudioStream;
hr = spatialAudioClient->ActivateSpatialAudioStream(&activationParams, __uuidof(spatialAudioStream), (void**)&spatialAudioStream);
```



> [!Note]  
> <span data-ttu-id="e7fdc-129">При использовании интерфейсов [**испатиалаудиоклиент**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) в заголовке Xbox One Development Kit (XDK) сначала необходимо вызвать **енаблеспатиалаудио** перед вызовом [**Иммдевицеенумератор:: Енумаудиоендпоинтс**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) или [**иммдевицеенумератор:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-129">When using the [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) interfaces on an Xbox One Development Kit (XDK) title, you must first call **EnableSpatialAudio** before calling [**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) or [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="e7fdc-130">Несоблюдение этого действия приведет к тому, что при \_ вызове функции активации будет возвращена ошибка "E Interface".</span><span class="sxs-lookup"><span data-stu-id="e7fdc-130">Failure to do so will result in an E\_NOINTERFACE error being returned from the call to Activate.</span></span> <span data-ttu-id="e7fdc-131">**Енаблеспатиалаудио** доступен только для заголовков XDK, и его не нужно вызывать для универсальная платформа Windows приложений, работающих на Xbox One, а также для устройств, не являющихся устройствами Xbox.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-131">**EnableSpatialAudio** is only available for XDK titles, and does not need to be called for Universal Windows Platform apps running on Xbox One, nor for any non-Xbox One devices.</span></span>

 

<span data-ttu-id="e7fdc-132">Объявите указатель для [**испатиалаудиубжект**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) , который будет использоваться для записи звуковых данных в статический канал.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-132">Declare a pointer for an [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) that will be used to write audio data to a static channel.</span></span> <span data-ttu-id="e7fdc-133">Обычные приложения будут использовать объект для каждого канала, указанного в поле **статикобжекттипемаск** .</span><span class="sxs-lookup"><span data-stu-id="e7fdc-133">Typical apps will use an object for each channel specified in the **StaticObjectTypeMask** field.</span></span> <span data-ttu-id="e7fdc-134">Для простоты в этом примере используется только один статический звуковой объект.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-134">For simplicity, this example only uses a single static audio object.</span></span>


```C++
// In this simple example, one object will be rendered
Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObjectFrontLeft;
```



<span data-ttu-id="e7fdc-135">Перед входом в цикл рендеринга звука вызовите [**испатиалаудиубжектрендерстреам:: Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) , чтобы указать конвейеру мультимедиа начать запрашивать звуковые данные.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-135">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStream::Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) to instruct the media pipeline to begin requesting audio data.</span></span> <span data-ttu-id="e7fdc-136">В этом примере используется счетчик, чтобы прерывать отрисовку звука через 5 секунд.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-136">This example uses a counter to stop the rendering of audio after 5 seconds.</span></span>

<span data-ttu-id="e7fdc-137">В цикле подготовки к просмотру дождитесь события завершения буфера, предоставленного при инициализации пространственного аудиопотока, чтобы получать сигнал.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-137">Inside the render loop, wait for the buffer completion event, provided when the spatial audio stream was initialized, to be signaled.</span></span> <span data-ttu-id="e7fdc-138">При ожидании события следует задать разумное время ожидания (например, 100 мс), так как любое изменение типа рендеринга или конечной точки приведет к тому, что событие никогда не будет сигнальным.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-138">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="e7fdc-139">В этом случае можно вызвать метод [**испатиалаудиубжектрендерстреам:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) , чтобы попытаться сбросить пространственный звуковой поток.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-139">In this case, you can call [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="e7fdc-140">Затем вызовите метод [**испатиалаудиубжектрендерстреам:: бегинупдатингаудиубжектс**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) , чтобы сообщить системе о том, что вы собираетесь заполнить буферы звуковых объектов данными.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-140">Next, call [**ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="e7fdc-141">Этот метод возвращает количество доступных динамических звуковых объектов, не используемых в этом примере, и число кадров буфера для звуковых объектов, отображаемых этим потоком.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-141">This method returns the number of available dynamic audio objects, not used in this example, and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="e7fdc-142">Если статический объект пространственного звука еще не создан, создайте один или несколько путем вызова [**испатиалаудиубжектрендерстреам:: активатеспатиалаудиубжект**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject), передав значение из перечисления [**аудиубжекттипе**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) , указывающее статический канал, на который визуализируется звук объекта.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-142">If a static spatial audio object has not yet been created, create one or more by calling [**ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject), passing in a value from the [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) enumeration indicating the static channel to which the object's audio is rendered.</span></span>

<span data-ttu-id="e7fdc-143">Затем вызовите [**испатиалаудиубжект::**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) GetObject, чтобы получить указатель на звуковой буфер объекта пространственного звука.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-143">Next, call [**ISpatialAudioObject::GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="e7fdc-144">Этот метод также возвращает размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-144">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="e7fdc-145">В этом примере используется вспомогательный метод **вритетоаудиубжектбуффер** для заполнения буфера звуковыми данными.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-145">This example uses a helper method, **WriteToAudioObjectBuffer**, to fill the buffer with audio data.</span></span> <span data-ttu-id="e7fdc-146">Этот метод показан далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-146">This method is shown later in this article.</span></span> <span data-ttu-id="e7fdc-147">После записи в буфер в примере проверяется, было ли достигнуто 5-секундное время существования объекта, и, если это так, вызывается [**испатиалаудиубжект:: сетендофстреам**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) , чтобы позволить конвейеру звука узнать, что больше не будет записано никакого звука с помощью этого объекта, а для объекта задано значение **nullptr** , чтобы освободить свои ресурсы.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-147">After writing to the buffer, the example checks to see if the 5 second lifetime of the object has been reached, and if so, [**ISpatialAudioObject::SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="e7fdc-148">После записи данных во все звуковые объекты вызовите метод [**испатиалаудиубжектрендерстреам:: ендупдатингаудиубжектс**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) , чтобы система знала, что данные готовы для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-148">After writing data to all of your audio objects, call [**ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="e7fdc-149">Вызвать метод @ **buffer** можно только между вызовами **бегинупдатингаудиубжектс** и **ендупдатингаудиубжектс**.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-149">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


```C++
// Start streaming / rendering 
hr = spatialAudioStream->Start();

// This example will render 5 seconds of audio samples
UINT totalFrameCount = format.nSamplesPerSec * 5;

bool isRendering = true;
while (isRendering)
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        hr = spatialAudioStream->Reset();

        if (hr != S_OK)
        {
            // handle the error
            break;
        }
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of dynamic objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStream->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    if (audioObjectFrontLeft == nullptr)
    {
        hr = spatialAudioStream->ActivateSpatialAudioObject(AudioObjectType::AudioObjectType_FrontLeft, &audioObjectFrontLeft);
        if (hr != S_OK) break;
    }

    // Get the buffer to write audio data
    hr = audioObjectFrontLeft->GetBuffer(&buffer, &bufferLength);

    if (totalFrameCount >= frameCount)
    {
        // Write audio data to the buffer
        WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, 200.0f, format.nSamplesPerSec);

        totalFrameCount -= frameCount;
    }
    else
    {
        // Write audio data to the buffer
        WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), totalFrameCount, 750.0f, format.nSamplesPerSec);

        // Set end of stream for the last buffer 
        hr = audioObjectFrontLeft->SetEndOfStream(totalFrameCount);

        audioObjectFrontLeft = nullptr; // Release the object

        isRendering = false;
    }

    // Let the audio engine know that the object data are available for processing now
    hr = spatialAudioStream->EndUpdatingAudioObjects();
};
```



<span data-ttu-id="e7fdc-150">Когда вы завершите отрисовку пространственного звука, прервите пространственный поток звука, вызвав [**испатиалаудиубжектрендерстреам:: останавливаться**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-150">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioObjectRenderStream::Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span></span> <span data-ttu-id="e7fdc-151">Если вы не собираетесь повторно использовать поток, освободите его ресурсы, вызвав [**испатиалаудиубжектрендерстреам:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-151">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span></span>


```C++
// Stop the stream
hr = spatialAudioStream->Stop();

// Don't want to start again, so reset the stream to free its resources
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



<span data-ttu-id="e7fdc-152">Вспомогательный метод **вритетоаудиубжектбуффер** записывает либо полный буфер выборок, либо количество оставшихся выборок, заданных ограничением времени, определяемым приложением.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-152">The **WriteToAudioObjectBuffer** helper method writes either a full buffer of samples or the number of remaining samples specified by our app-defined time limit.</span></span> <span data-ttu-id="e7fdc-153">Это также можно определить, например, с учетом количества выборок, остающихся в исходном звуковом файле.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-153">This could also be determined, for example, by the number of samples remaining in a source audio file.</span></span> <span data-ttu-id="e7fdc-154">Простая волна Sin, частота выполнения которой масштабируется с помощью входного параметра *Frequency* , создается и записывается в буфер.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-154">A simple sin wave, the frequency of which is scaled by the *frequency* input parameter, is generated and written to the buffer.</span></span>


```C++
void WriteToAudioObjectBuffer(FLOAT* buffer, UINT frameCount, FLOAT frequency, UINT samplingRate)
{
    const double PI = 4 * atan2(1.0, 1.0);
    static double _radPhase = 0.0;

    double step = 2 * PI * frequency / samplingRate;

    for (UINT i = 0; i < frameCount; i++)
    {
        double sample = sin(_radPhase);

        buffer[i] = FLOAT(sample);

        _radPhase += step; // next frame phase

        if (_radPhase >= 2 * PI)
        {
            _radPhase -= 2 * PI;
        }
    }
}
```



## <a name="render-audio-using-dynamic-spatial-audio-objects"></a><span data-ttu-id="e7fdc-155">Прорисовка звука с помощью динамических пространственных звуковых объектов</span><span class="sxs-lookup"><span data-stu-id="e7fdc-155">Render audio using dynamic spatial audio objects</span></span>

<span data-ttu-id="e7fdc-156">Динамические объекты позволяют визуализировать звук из произвольного расположения в пространстве относительно пользователя.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-156">Dynamic objects allow you to render audio from an arbitrary position in space, relative to the user.</span></span> <span data-ttu-id="e7fdc-157">Расположение и громкость динамического звукового объекта можно изменить с течением времени.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-157">The position and volume of a dynamic audio object can be changed over time.</span></span> <span data-ttu-id="e7fdc-158">Игры обычно используют расположение трехмерного объекта в мире игры для указания расположения динамического звукового объекта, связанного с ним.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-158">Games will typically use the position of a 3D object in the game world to specify the position of the dynamic audio object associated with it.</span></span> <span data-ttu-id="e7fdc-159">В следующем примере будет использоваться простая структура **My3dObject** для хранения минимального набора данных, необходимого для представления объекта.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-159">The following example will use a simple structure, **My3dObject**, to store the minimum set of data needed to represent an object.</span></span> <span data-ttu-id="e7fdc-160">Эти данные включают указатель на [**испатиалаудиубжект**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), расположение, скорость, громкость и частоту тона для объекта, а также значение, которое хранит общее число кадров, для которых объект должен отображать звук.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-160">This data includes a pointer to an [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), the position, velocity, volume, and tone frequency for the object, and a value that stores the total number of frames for which the object should render sound.</span></span>


```C++
struct My3dObject
{
    Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObject;
    Windows::Foundation::Numerics::float3 position;
    Windows::Foundation::Numerics::float3 velocity;
    float volume;
    float frequency; // in Hz
    UINT totalFrameCount;
};
```



<span data-ttu-id="e7fdc-161">Действия по реализации динамических звуковых объектов в основном совпадают с действиями статических звуковых объектов, описанных выше.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-161">The implementation steps for dynamic audio objects is largely the same as the steps for static audio objects described above.</span></span> <span data-ttu-id="e7fdc-162">Сначала получите конечную точку аудио.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-162">First, get an audio endpoint.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="e7fdc-163">Затем инициализируйте пространственный аудиопоток.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-163">Next, initialize the spatial audio stream.</span></span> <span data-ttu-id="e7fdc-164">Получите экземпляр [**испатиалаудиоклиент**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) , вызвав [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-164">Get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="e7fdc-165">Вызовите метод [**испатиалаудиоклиент:: исаудиубжектформатсуппортед**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) , чтобы обеспечить поддержку формата звука, который вы используете.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-165">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="e7fdc-166">Создайте событие, которое будет использоваться конвейером аудиопотока для уведомления приложения о том, что оно готово для дополнительных звуковых данных.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-166">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="e7fdc-167">Вызовите метод [**испатиалаудиоклиент:: жетмаксдинамикобжекткаунт**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) , чтобы получить число динамических объектов, поддерживаемых системой.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-167">Call [**ISpatialAudioClient::GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) to retrieve the number of dynamic objects supported by the system.</span></span> <span data-ttu-id="e7fdc-168">Если этот вызов возвращает значение 0, то динамические пространственные объекты не поддерживаются и не включаются на текущем устройстве.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-168">If this call returns 0, then dynamic spatial audio objects are not supported or enabled on the current device.</span></span> <span data-ttu-id="e7fdc-169">Сведения о включении пространственного аудио и о числе динамических звуковых объектов, доступных для различных пространственных форматов, см. в разделе [Пространственный звук](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-169">For information on enabling spatial audio and for details on the number of dynamic audio objects available for different spatial audio formats, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="e7fdc-170">При заполнении структуры [**спатиалаудиубжектрендерстреамактиватионпарамс**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) задайте в поле **максдинамикобжекткаунт** максимальное число динамических объектов, которое будет использоваться приложением.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-170">When populating the [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) structure, set the **MaxDynamicObjectCount** field to the maximum number of dynamic objects your app will use.</span></span>

<span data-ttu-id="e7fdc-171">Вызовите метод [**испатиалаудиоклиент:: активатеспатиалаудиостреам**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) , чтобы активировать поток.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-171">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


```C++
// Activate ISpatialAudioClient on the desired audio-device 
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

UINT32 maxDynamicObjectCount;
hr = spatialAudioClient->GetMaxDynamicObjectCount(&maxDynamicObjectCount);

if (maxDynamicObjectCount == 0)
{
    // Dynamic objects are unsupported
    return;
}

// Set the maximum number of dynamic audio objects that will be used
SpatialAudioObjectRenderStreamActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = AudioObjectType_None;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = min(maxDynamicObjectCount, 4);
streamParams.Category = AudioCategory_GameEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = nullptr;

PROPVARIANT pv;
PropVariantInit(&pv);
pv.vt = VT_BLOB;
pv.blob.cbSize = sizeof(streamParams);
pv.blob.pBlobData = (BYTE *)&streamParams;

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStream> spatialAudioStream;;
hr = spatialAudioClient->ActivateSpatialAudioStream(&pv, __uuidof(spatialAudioStream), (void**)&spatialAudioStream);
```



<span data-ttu-id="e7fdc-172">Ниже приведен код конкретного приложения, необходимый для поддержки этого примера, который динамически создает случайные позиционированные объекты аудио и сохраняет их в векторе.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-172">The following is some app-specific code to needed support this example, which will dynamically spawn randomly positioned audio objects and store them in a vector.</span></span>


```C++
// Used for generating a vector of randomized My3DObject structs
std::vector<My3dObject> objectVector;
std::default_random_engine gen;
std::uniform_real_distribution<> pos_dist(-25, 25); // uniform distribution for random position
std::uniform_real_distribution<> vel_dist(-1, 1); // uniform distribution for random velocity
std::uniform_real_distribution<> vol_dist(0.5, 1.0); // uniform distribution for random volume
std::uniform_real_distribution<> pitch_dist(40, 400); // uniform distribution for random pitch
int spawnCounter = 0;
```



<span data-ttu-id="e7fdc-173">Перед входом в цикл рендеринга звука вызовите [**испатиалаудиубжектрендерстреам:: Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) , чтобы указать конвейеру мультимедиа начать запрашивать звуковые данные.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-173">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStream::Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) to instruct the media pipeline to begin requesting audio data.</span></span>

<span data-ttu-id="e7fdc-174">В цикле рендеринга дождитесь события завершения буфера, которое мы предоставили при инициализации пространственного звукового потока для получения сигнала.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-174">Inside the render loop, wait for the buffer completion event we provided when the spatial audio stream was initialized to be signaled.</span></span> <span data-ttu-id="e7fdc-175">При ожидании события следует задать разумное время ожидания (например, 100 мс), так как любое изменение типа рендеринга или конечной точки приведет к тому, что событие никогда не будет сигнальным.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-175">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="e7fdc-176">В этом случае можно вызвать метод [**испатиалаудиубжектрендерстреам:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) , чтобы попытаться сбросить пространственный звуковой поток.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-176">In this case, you can call [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="e7fdc-177">Затем вызовите метод [**испатиалаудиубжектрендерстреам:: бегинупдатингаудиубжектс**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) , чтобы сообщить системе о том, что вы собираетесь заполнить буферы звуковых объектов данными.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-177">Next, call [**ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="e7fdc-178">Этот метод возвращает число доступных динамических звуковых объектов и число кадров буфера для звуковых объектов, отображаемых этим потоком.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-178">This method returns the number of available dynamic audio objects and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="e7fdc-179">Каждый раз, когда счетчик порождений достигает указанного значения, мы активируем новый динамический звуковой объект, вызывая [**испатиалаудиубжектрендерстреам:: активатеспатиалаудиубжект**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) , указывая [**аудиубжекттипе \_ dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-179">Whenever the spawn counter reaches the specified value, we will activate a new dynamic audio object by calling [**ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) specifying [**AudioObjectType\_Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span></span> <span data-ttu-id="e7fdc-180">Если все доступные динамические звуковые объекты уже были выделены, этот метод возвратит **сплаудклнт \_ е больше \_ \_ \_ объектов**.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-180">If all available dynamic audio objects have already been allocated, this method will return **SPLAUDCLNT\_E\_NO\_MORE\_OBJECTS**.</span></span> <span data-ttu-id="e7fdc-181">В этом случае можно выбрать выпуск одного или нескольких ранее активированных звуковых объектов на основе приоритета конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-181">In this case, you can choose to release one or more previously activated audio objects based on your app-specific prioritization.</span></span> <span data-ttu-id="e7fdc-182">После создания объекта Dynamic Audio он добавляется в новую структуру **My3dObject** со случайным положением, скоростью, объемом и частотой, которая затем добавляется в список активных объектов.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-182">After the dynamic audio object has been created, it is added to a new **My3dObject** structure, with randomized position, velocity, volume, and frequency values, which is then added to the list of active objects.</span></span>

<span data-ttu-id="e7fdc-183">Затем выполните итерацию всех активных объектов, представленных в этом примере, с помощью определяемой приложением структуры **My3dObject** .</span><span class="sxs-lookup"><span data-stu-id="e7fdc-183">Next, iterate over all of the active objects, represented in this example with the app-defined **My3dObject** structure.</span></span> <span data-ttu-id="e7fdc-184">Для каждого звукового объекта вызовите [**испатиалаудиубжект::**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) GetObject, чтобы получить указатель на звуковой буфер объекта пространственного звука.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-184">For each audio object, call [**ISpatialAudioObject::GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="e7fdc-185">Этот метод также возвращает размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-185">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="e7fdc-186">Вспомогательный метод **вритетоаудиубжектбуффер** для заполнения буфера звуковыми данными.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-186">The helper method, **WriteToAudioObjectBuffer**, to fill the buffer with audio data.</span></span> <span data-ttu-id="e7fdc-187">После записи в буфер в примере обновляется расположение объекта Dynamic Audio путем вызова [**испатиалаудиубжект:: SetPosition**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-187">After writing to the buffer, the example updates the position of the dynamic audio object by calling [**ISpatialAudioObject::SetPosition**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition).</span></span> <span data-ttu-id="e7fdc-188">Громкость объекта audio также может быть изменена путем вызова [**сетволуме**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-188">The volume of the audio object can also be modified by calling [**SetVolume**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume).</span></span> <span data-ttu-id="e7fdc-189">Если вы не обновите расположение или том объекта, он будет хранить свое расположение и том с момента последнего задания.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-189">If you don't update the position or volume of the object, it will retain the position and volume from the last time it was set.</span></span> <span data-ttu-id="e7fdc-190">Если время существования объекта, определяемого приложением, было достигнуто, вызывается [**испатиалаудиубжект:: сетендофстреам**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) , чтобы позволить конвейеру звука узнать, что больше не будет записано никакого звука с помощью этого объекта, а объект имеет значение **nullptr** , чтобы освободить свои ресурсы.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-190">If the object's app-defined lifetime has been reached, [**ISpatialAudioObject::SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="e7fdc-191">После записи данных во все звуковые объекты вызовите метод [**испатиалаудиубжектрендерстреам:: ендупдатингаудиубжектс**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) , чтобы система знала, что данные готовы для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-191">After writing data to all of your audio objects, call [**ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="e7fdc-192">Вызвать метод @ **buffer** можно только между вызовами **бегинупдатингаудиубжектс** и **ендупдатингаудиубжектс**.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-192">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


```C++
// Start streaming / rendering 
hr = spatialAudioStream->Start();

do
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        break;
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of active objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStream->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    // Spawn a new dynamic audio object every 200 iterations
    if (spawnCounter % 200 == 0 && spawnCounter < 1000)
    {
        // Activate a new dynamic audio object
        Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObject;
        hr = spatialAudioStream->ActivateSpatialAudioObject(AudioObjectType::AudioObjectType_Dynamic, &audioObject);

        // If SPTLAUDCLNT_E_NO_MORE_OBJECTS is returned, there are no more available objects
        if (SUCCEEDED(hr))
        {
            // Init new struct with the new audio object.
            My3dObject obj = {
                audioObject,
                Windows::Foundation::Numerics::float3(static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen))),
                Windows::Foundation::Numerics::float3(static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen))),
                static_cast<float>(static_cast<float>(vol_dist(gen))),
                static_cast<float>(static_cast<float>(pitch_dist(gen))),
                format.nSamplesPerSec * 5 // 5 seconds of audio samples
            };

            objectVector.insert(objectVector.begin(), obj);
        }
    }
    spawnCounter++;

    // Loop through all dynamic audio objects
    std::vector<My3dObject>::iterator it = objectVector.begin();
    while (it != objectVector.end())
    {
        it->audioObject->GetBuffer(&buffer, &bufferLength);

        if (it->totalFrameCount >= frameCount)
        {
            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, it->frequency, format.nSamplesPerSec);

            // Update the position and volume of the audio object
            it->audioObject->SetPosition(it->position.x, it->position.y, it->position.z);
            it->position += it->velocity;
            it->audioObject->SetVolume(it->volume);

            it->totalFrameCount -= frameCount;

            ++it;
        }
        else
        {
            // If the audio object reaches its lifetime, set EndOfStream and release the object

            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), it->totalFrameCount, it->frequency, format.nSamplesPerSec);

            // Set end of stream for the last buffer 
            hr = it->audioObject->SetEndOfStream(it->totalFrameCount);

            it->audioObject = nullptr; // Release the object

            it->totalFrameCount = 0;

            it = objectVector.erase(it);
        }
    }

    // Let the audio-engine know that the object data are available for processing now
    hr = spatialAudioStream->EndUpdatingAudioObjects();
} while (objectVector.size() > 0);
```



<span data-ttu-id="e7fdc-193">Когда вы завершите отрисовку пространственного звука, прервите пространственный поток звука, вызвав [**испатиалаудиубжектрендерстреам:: останавливаться**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-193">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioObjectRenderStream::Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span></span> <span data-ttu-id="e7fdc-194">Если вы не собираетесь повторно использовать поток, освободите его ресурсы, вызвав [**испатиалаудиубжектрендерстреам:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-194">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span></span>


```C++
// Stop the stream 
hr = spatialAudioStream->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



## <a name="render-audio-using-dynamic-spatial-audio-objects-for-hrtf"></a><span data-ttu-id="e7fdc-195">Прорисовка звука с помощью динамических пространственных звуковых объектов для ХРТФ</span><span class="sxs-lookup"><span data-stu-id="e7fdc-195">Render audio using dynamic spatial audio objects for HRTF</span></span>

<span data-ttu-id="e7fdc-196">Другой набор API-интерфейсов, [**испатиалаудиорендерстреамфорхртф**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) и [**испатиалаудиубжектфорхртф**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), включает Пространственный звук, который использует функцию Microsoft по относительным функциям передачи (хртф) для затухания звука для имитации положения передатчика в пространстве относительно пользователя, который можно изменить со временем.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-196">Another set of APIs, [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) and [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), enable spatial audio that uses Microsoft's Head-relative Transfer Function (HRTF) to attenuate sounds to simulate the emitter's position in space, relative to the user, which can be changed over time.</span></span> <span data-ttu-id="e7fdc-197">В дополнение к положению, ХРТФ Audio объекты позволяют указать ориентацию в пространстве, директивити, в которой выдается звук, например конус или кардиоид, и модель Decay по мере того, как объект перемещается ближе к виртуальному прослушивателю.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-197">In addition to position, HRTF audio objects allow you to specify an orientation in space, a directivity in which sound is emitted, such as a cone or cardioid shape, and a decay model as the object moves nearer and further from the virtual listener.</span></span> <span data-ttu-id="e7fdc-198">Обратите внимание, что эти интерфейсы ХРТФ доступны, только если пользователь выбрал Windows Sonic для наушников в качестве подсистемы пространственного аудио для устройства.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-198">Note that these HRTF interfaces are only available when the user has selected Windows Sonic for Headphones as the spatial audio engine for the device.</span></span> <span data-ttu-id="e7fdc-199">Сведения о настройке устройства для использования Windows Sonic для наушников см. в разделе [Пространственный звук](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-199">For information on configuring a device to use Windows Sonic for Headphones, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="e7fdc-200">Интерфейсы API [**испатиалаудиорендерстреамфорхртф**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) и [**испатиалаудиубжектфорхртф**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) позволяют приложению явно использовать путь отрисовки Windows Sonic для наушников напрямую.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-200">The [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) and [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) APIs allow an application to explicitly use the Windows Sonic for Headphones render path directly.</span></span> <span data-ttu-id="e7fdc-201">Эти API не поддерживают пространственные звуковые форматы, такие как Dolby атмос для домашнего кинотеатра или Dolby атмос для наушников, а также переключение пользовательского формата вывода с помощью панели управления **звуком** и на динамиках.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-201">These APIs do not support spatial sound formats such as Dolby Atmos for Home Theater or Dolby Atmos for Headphones, nor consumer-controlled output format switching via the **Sound** control panel, nor playback over speakers.</span></span> <span data-ttu-id="e7fdc-202">Эти интерфейсы предназначены для использования в приложениях Windows Mixed Reality, которые хотят использовать возможности Windows Sonic для работы с наушниками (например, предустановки и роллофф на основе расстояния, указанные программно, за пределами типичных конвейеров создания содержимого).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-202">These interfaces are intended for use in Windows Mixed Reality applications that want to use Windows Sonic for Headphones-specific capabilities (such as environmental presets and distance-based rolloff specified programmatically, outside of typical content authoring pipelines).</span></span> <span data-ttu-id="e7fdc-203">В большинстве игр и сценариев Virtual Reality предпочтительнее использовать [**испатиалаудиоклиент**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) .</span><span class="sxs-lookup"><span data-stu-id="e7fdc-203">Most games and virtual reality scenarios will prefer to use [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) instead.</span></span> <span data-ttu-id="e7fdc-204">Действия по реализации обоих наборов API практически идентичны, поэтому можно реализовать обе технологии и переключиться на среду выполнения в зависимости от того, какая функция доступна на текущем устройстве.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-204">The implementation steps for both API sets are almost identical, so it is possible to implement both technologies and switch at runtime depending on which feature is available on the current device.</span></span>

<span data-ttu-id="e7fdc-205">Приложения смешанной реальности обычно используют расположение трехмерного объекта в виртуальном мире, чтобы указать расположение динамического звукового объекта, связанного с ним.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-205">Mixed-reality apps will typically use the position of a 3D object in the virtual world to specify the position of the dynamic audio object associated with it.</span></span> <span data-ttu-id="e7fdc-206">В следующем примере будет использоваться простая структура **My3dObjectForHrtf** для хранения минимального набора данных, необходимого для представления объекта.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-206">The following example will use a simple structure, **My3dObjectForHrtf**, to store the minimum set of data needed to represent an object.</span></span> <span data-ttu-id="e7fdc-207">Эти данные включают указатель на [**испатиалаудиубжектфорхртф**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), положение, ориентацию, скорость и частоту тона для объекта, а также значение, которое хранит общее число кадров, для которых объект должен отображать звук.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-207">This data includes a pointer to an [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), the position, orientation, velocity, and tone frequency for the object, and a value that stores the total number of frames for which the object should render sound.</span></span>


```C++
struct My3dObjectForHrtf
{
    Microsoft::WRL::ComPtr<ISpatialAudioObjectForHrtf> audioObject;
    Windows::Foundation::Numerics::float3 position;
    Windows::Foundation::Numerics::float3 velocity;
    float yRotationRads;
    float deltaYRotation;
    float frequency; // in Hz
    UINT totalFrameCount;
};
```



<span data-ttu-id="e7fdc-208">Действия по реализации динамических ХРТФ аудио-объектов в основном аналогичны шагам для динамических звуковых объектов, описанных в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-208">The implementation steps for dynamic HRTF audio objects is largely the same as the steps for dynamic audio objects described in the previous section.</span></span> <span data-ttu-id="e7fdc-209">Сначала получите конечную точку аудио.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-209">First, get an audio endpoint.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="e7fdc-210">Затем инициализируйте пространственный аудиопоток.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-210">Next, initialize the spatial audio stream.</span></span> <span data-ttu-id="e7fdc-211">Получите экземпляр [**испатиалаудиоклиент**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) , вызвав [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-211">Get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="e7fdc-212">Вызовите метод [**испатиалаудиоклиент:: исаудиубжектформатсуппортед**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) , чтобы обеспечить поддержку формата звука, который вы используете.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-212">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="e7fdc-213">Создайте событие, которое будет использоваться конвейером аудиопотока для уведомления приложения о том, что оно готово для дополнительных звуковых данных.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-213">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="e7fdc-214">Вызовите метод [**испатиалаудиоклиент:: жетмаксдинамикобжекткаунт**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) , чтобы получить число динамических объектов, поддерживаемых системой.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-214">Call [**ISpatialAudioClient::GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) to retrieve the number of dynamic objects supported by the system.</span></span> <span data-ttu-id="e7fdc-215">Если этот вызов возвращает значение 0, то динамические пространственные объекты не поддерживаются и не включаются на текущем устройстве.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-215">If this call returns 0, then dynamic spatial audio objects are not supported or enabled on the current device.</span></span> <span data-ttu-id="e7fdc-216">Сведения о включении пространственного аудио и о числе динамических звуковых объектов, доступных для различных пространственных форматов, см. в разделе [Пространственный звук](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-216">For information on enabling spatial audio and for details on the number of dynamic audio objects available for different spatial audio formats, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="e7fdc-217">При заполнении структуры [**спатиалаудиохртфактиватионпарамс**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) задайте в поле **максдинамикобжекткаунт** максимальное число динамических объектов, которое будет использоваться приложением.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-217">When populating the [**SpatialAudioHrtfActivationParams**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) structure, set the **MaxDynamicObjectCount** field to the maximum number of dynamic objects your app will use.</span></span> <span data-ttu-id="e7fdc-218">Параметры активации для ХРТФ поддерживают несколько дополнительных параметров, таких как [**спатиалаудиохртфдистанцедекай**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay), [**спатиалаудиохртфдирективитюнион**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion), [**спатиалаудиохртфенвиронменттипе**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype)и [**SpatialAudioHrtfOrientation**](spatialaudiohrtforientation.md), которые определяют значения этих параметров по умолчанию для новых объектов, создаваемых из потока.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-218">The activation params for HRTF supports a few additional parameters, such as a [**SpatialAudioHrtfDistanceDecay**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay), a [**SpatialAudioHrtfDirectivityUnion**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion), a [**SpatialAudioHrtfEnvironmentType**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype), and a [**SpatialAudioHrtfOrientation**](spatialaudiohrtforientation.md), which specify the default values of these settings for new objects created from the stream.</span></span> <span data-ttu-id="e7fdc-219">Эти параметры являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-219">These parameters are optional.</span></span> <span data-ttu-id="e7fdc-220">Задайте для полей значение **nullptr** , чтобы не указывать значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-220">Set the fields to **nullptr** to provide no default values.</span></span>

<span data-ttu-id="e7fdc-221">Вызовите метод [**испатиалаудиоклиент:: активатеспатиалаудиостреам**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) , чтобы активировать поток.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-221">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


```C++
// Activate ISpatialAudioClient on the desired audio-device 
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStreamForHrtf>  spatialAudioStreamForHrtf;
hr = spatialAudioClient->IsSpatialAudioStreamAvailable(__uuidof(spatialAudioStreamForHrtf), NULL);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

UINT32 maxDynamicObjectCount;
hr = spatialAudioClient->GetMaxDynamicObjectCount(&maxDynamicObjectCount);

SpatialAudioHrtfActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = AudioObjectType_None;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = min(maxDynamicObjectCount, 4);
streamParams.Category = AudioCategory_GameEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = NULL;

SpatialAudioHrtfDistanceDecay decayModel;
decayModel.CutoffDistance = 100;
decayModel.MaxGain = 3.98f;
decayModel.MinGain = float(1.58439 * pow(10, -5));
decayModel.Type = SpatialAudioHrtfDistanceDecayType::SpatialAudioHrtfDistanceDecay_NaturalDecay;
decayModel.UnityGainDistance = 1;

streamParams.DistanceDecay = &decayModel;

SpatialAudioHrtfDirectivity directivity;
directivity.Type = SpatialAudioHrtfDirectivityType::SpatialAudioHrtfDirectivity_Cone;
directivity.Scaling = 1.0f;

SpatialAudioHrtfDirectivityCone cone;
cone.directivity = directivity;
cone.InnerAngle = 0.1f;
cone.OuterAngle = 0.2f;

SpatialAudioHrtfDirectivityUnion directivityUnion;
directivityUnion.Cone = cone;
streamParams.Directivity = &directivityUnion;

SpatialAudioHrtfEnvironmentType environment = SpatialAudioHrtfEnvironmentType::SpatialAudioHrtfEnvironment_Large;
streamParams.Environment = &environment;

SpatialAudioHrtfOrientation orientation = { 1,0,0,0,1,0,0,0,1 }; // identity matrix
streamParams.Orientation = &orientation;

PROPVARIANT pv;
PropVariantInit(&pv);
pv.vt = VT_BLOB;
pv.blob.cbSize = sizeof(streamParams);
pv.blob.pBlobData = (BYTE *)&streamParams;

hr = spatialAudioClient->ActivateSpatialAudioStream(&pv, __uuidof(spatialAudioStreamForHrtf), (void**)&spatialAudioStreamForHrtf);
```



<span data-ttu-id="e7fdc-222">Ниже приведен код конкретного приложения, необходимый для поддержки этого примера, который динамически создает случайные позиционированные объекты аудио и сохраняет их в векторе.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-222">The following is some app-specific code to needed support this example, which will dynamically spawn randomly positioned audio objects and store them in a vector.</span></span>


```C++
// Used for generating a vector of randomized My3DObject structs
std::vector<My3dObjectForHrtf> objectVector;
std::default_random_engine gen;
std::uniform_real_distribution<> pos_dist(-10, 10); // uniform distribution for random position
std::uniform_real_distribution<> vel_dist(-.02, .02); // uniform distribution for random velocity
std::uniform_real_distribution<> yRotation_dist(-3.14, 3.14); // uniform distribution for y-axis rotation
std::uniform_real_distribution<> deltaYRotation_dist(.01, .02); // uniform distribution for y-axis rotation
std::uniform_real_distribution<> pitch_dist(40, 400); // uniform distribution for random pitch

int spawnCounter = 0;
```



<span data-ttu-id="e7fdc-223">Перед входом в цикл рендеринга звука вызовите [**испатиалаудиубжектрендерстреамфорхртф:: Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) , чтобы указать конвейеру мультимедиа начать запрашивать звуковые данные.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-223">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStreamForHrtf::Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) to instruct the media pipeline to begin requesting audio data.</span></span>

<span data-ttu-id="e7fdc-224">В цикле рендеринга дождитесь события завершения буфера, которое мы предоставили при инициализации пространственного звукового потока для получения сигнала.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-224">Inside the render loop, wait for the buffer completion event we provided when the spatial audio stream was initialized to be signaled.</span></span> <span data-ttu-id="e7fdc-225">При ожидании события следует задать разумное время ожидания (например, 100 мс), так как любое изменение типа рендеринга или конечной точки приведет к тому, что событие никогда не будет сигнальным.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-225">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="e7fdc-226">В этом случае можно вызвать метод [**испатиалаудиорендерстреамфорхртф:: Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) , чтобы попытаться сбросить пространственный звуковой поток.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-226">In this case, you can call [**ISpatialAudioRenderStreamForHrtf::Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="e7fdc-227">Затем вызовите метод [**испатиалаудиорендерстреамфорхртф:: бегинупдатингаудиубжектс**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) , чтобы сообщить системе о том, что вы собираетесь заполнить буферы звуковых объектов данными.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-227">Next, call [**ISpatialAudioRenderStreamForHrtf::BeginUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="e7fdc-228">Этот метод возвращает количество доступных динамических звуковых объектов, не используемых в этом примере, и число кадров буфера для звуковых объектов, отображаемых этим потоком.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-228">This method returns the number of available dynamic audio objects, not used in this example, and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="e7fdc-229">Каждый раз, когда счетчик порождений достигает указанного значения, мы активируем новый динамический звуковой объект, вызывая [**испатиалаудиорендерстреамфорхртф:: активатеспатиалаудиубжектфорхртф**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) , указывая [**аудиубжекттипе \_ dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-229">Whenever the spawn counter reaches the specified value, we will activate a new dynamic audio object by calling [**ISpatialAudioRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) specifying [**AudioObjectType\_Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span></span> <span data-ttu-id="e7fdc-230">Если все доступные динамические звуковые объекты уже были выделены, этот метод возвратит **сплаудклнт \_ е больше \_ \_ \_ объектов**.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-230">If all available dynamic audio objects have already been allocated, this method will return **SPLAUDCLNT\_E\_NO\_MORE\_OBJECTS**.</span></span> <span data-ttu-id="e7fdc-231">В этом случае можно выбрать выпуск одного или нескольких ранее активированных звуковых объектов на основе приоритета конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-231">In this case, you can choose to release one or more previously activated audio objects based on your app-specific prioritization.</span></span> <span data-ttu-id="e7fdc-232">После создания динамического звукового объекта он добавляется в новую структуру **My3dObjectForHrtf** со случайными значениями позиций, вращения, скорости, объема и частоты, которые затем добавляются в список активных объектов.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-232">After the dynamic audio object has been created, it is added to a new **My3dObjectForHrtf** structure, with randomized position, rotation, velocity, volume, and frequency values, which is then added to the list of active objects.</span></span>

<span data-ttu-id="e7fdc-233">Затем выполните итерацию всех активных объектов, представленных в этом примере, с помощью определяемой приложением структуры **My3dObjectForHrtf** .</span><span class="sxs-lookup"><span data-stu-id="e7fdc-233">Next, iterate over all of the active objects, represented in this example with the app-defined **My3dObjectForHrtf** structure.</span></span> <span data-ttu-id="e7fdc-234">Для каждого звукового объекта вызовите [**испатиалаудиубжектфорхртф::**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) GetObject, чтобы получить указатель на звуковой буфер объекта пространственного звука.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-234">For each audio object, call [**ISpatialAudioObjectForHrtf::GetBuffer**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="e7fdc-235">Этот метод также возвращает размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-235">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="e7fdc-236">Вспомогательный метод **вритетоаудиубжектбуффер**, приведенный ранее в этой статье, для заполнения буфера звуковыми данными.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-236">The helper method, **WriteToAudioObjectBuffer**, listed previously in this article, to fill the buffer with audio data.</span></span> <span data-ttu-id="e7fdc-237">После записи в буфер в примере обновляется положение и ориентация объекта audio ХРТФ путем вызова [**испатиалаудиубжектфорхртф:: SetPosition**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) и [**Испатиалаудиубжектфорхртф:: сеториентатион**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-237">After writing to the buffer, the example updates the position and orientation of the HRTF audio object by calling [**ISpatialAudioObjectForHrtf::SetPosition**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) and [**ISpatialAudioObjectForHrtf::SetOrientation**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation).</span></span> <span data-ttu-id="e7fdc-238">В этом примере вспомогательный метод **калкулатимиттерконеориентатионматрикс** используется для вычисления матрицы ориентации с учетом направления, на которое указывает трехмерный объект.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-238">In this example, a helper method, **CalculateEmitterConeOrientationMatrix**, is used to calculate the orientation matrix given the direction the 3D object is pointing.</span></span> <span data-ttu-id="e7fdc-239">Реализация этого метода показана ниже.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-239">The implementation of this method is shown below.</span></span> <span data-ttu-id="e7fdc-240">Громкость объекта audio также может быть изменена путем вызова [**испатиалаудиубжектфорхртф:: сетгаин**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-240">The volume of the audio object can also be modified by calling [**ISpatialAudioObjectForHrtf::SetGain**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain).</span></span> <span data-ttu-id="e7fdc-241">Если вы не обновите положение, ориентацию или объем объекта, он будет хранить положение, ориентацию и том из последней заданной копии.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-241">If you don't update the position, orientation, or volume of the object, it will retain the position, orientation, and volume from the last time it was set.</span></span> <span data-ttu-id="e7fdc-242">Если время существования объекта, определяемого приложением, было достигнуто, вызывается [**испатиалаудиубжектфорхртф:: сетендофстреам**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) , чтобы позволить конвейеру звука узнать, что больше не будет записано никакого звука с помощью этого объекта, а объект имеет значение **nullptr** , чтобы освободить свои ресурсы.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-242">If the object's app-defined lifetime has been reached, [**ISpatialAudioObjectForHrtf::SetEndOfStream**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="e7fdc-243">После записи данных во все звуковые объекты вызовите метод [**испатиалаудиорендерстреамфорхртф:: ендупдатингаудиубжектс**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) , чтобы система знала, что данные готовы для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-243">After writing data to all of your audio objects, call [**ISpatialAudioRenderStreamForHrtf::EndUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="e7fdc-244">Вызвать метод @ **buffer** можно только между вызовами **бегинупдатингаудиубжектс** и **ендупдатингаудиубжектс**.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-244">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


```C++
// Start streaming / rendering 
hr = spatialAudioStreamForHrtf->Start();

do
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        break;
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of active objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStreamForHrtf->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    // Spawn a new dynamic audio object every 200 iterations
    if (spawnCounter % 200 == 0 && spawnCounter < 1000)
    {
        // Activate a new dynamic audio object
        Microsoft::WRL::ComPtr<ISpatialAudioObjectForHrtf> audioObject;
        hr = spatialAudioStreamForHrtf->ActivateSpatialAudioObjectForHrtf(AudioObjectType::AudioObjectType_Dynamic, &audioObject);

        // If SPTLAUDCLNT_E_NO_MORE_OBJECTS is returned, there are no more available objects
        if (SUCCEEDED(hr))
        {
            // Init new struct with the new audio object.
            My3dObjectForHrtf obj = { audioObject,
                Windows::Foundation::Numerics::float3(static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen))),
                Windows::Foundation::Numerics::float3(static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen))),
                static_cast<float>(static_cast<float>(yRotation_dist(gen))),
                static_cast<float>(static_cast<float>(deltaYRotation_dist(gen))),
                static_cast<float>(static_cast<float>(pitch_dist(gen))),
                format.nSamplesPerSec * 5 // 5 seconds of audio samples
            };

            objectVector.insert(objectVector.begin(), obj);
        }
    }
    spawnCounter++;

    // Loop through all dynamic audio objects
    std::vector<My3dObjectForHrtf>::iterator it = objectVector.begin();
    while (it != objectVector.end())
    {
        it->audioObject->GetBuffer(&buffer, &bufferLength);

        if (it->totalFrameCount >= frameCount)
        {
            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, it->frequency, format.nSamplesPerSec);

            // Update the position and volume of the audio object
            it->audioObject->SetPosition(it->position.x, it->position.y, it->position.z);
            it->position += it->velocity;


            Windows::Foundation::Numerics::float3 emitterDirection = Windows::Foundation::Numerics::float3(cos(it->yRotationRads), 0, sin(it->yRotationRads));
            Windows::Foundation::Numerics::float3 listenerDirection = Windows::Foundation::Numerics::float3(0, 0, 1);
            DirectX::XMFLOAT4X4 rotationMatrix;

            DirectX::XMMATRIX rotation = CalculateEmitterConeOrientationMatrix(emitterDirection, listenerDirection);
            XMStoreFloat4x4(&rotationMatrix, rotation);

            SpatialAudioHrtfOrientation orientation = {
                rotationMatrix._11, rotationMatrix._12, rotationMatrix._13,
                rotationMatrix._21, rotationMatrix._22, rotationMatrix._23,
                rotationMatrix._31, rotationMatrix._32, rotationMatrix._33
            };

            it->audioObject->SetOrientation(&orientation);
            it->yRotationRads += it->deltaYRotation;

            it->totalFrameCount -= frameCount;

            ++it;
        }
        else
        {
            // If the audio object reaches its lifetime, set EndOfStream and release the object

            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), it->totalFrameCount, it->frequency, format.nSamplesPerSec);

            // Set end of stream for the last buffer 
            hr = it->audioObject->SetEndOfStream(it->totalFrameCount);

            it->audioObject = nullptr; // Release the object

            it->totalFrameCount = 0;

            it = objectVector.erase(it);
        }
    }

    // Let the audio-engine know that the object data are available for processing now
    hr = spatialAudioStreamForHrtf->EndUpdatingAudioObjects();

} while (objectVector.size() > 0);
```



<span data-ttu-id="e7fdc-245">Когда вы завершите отрисовку пространственного звука, прервите пространственный поток звука, вызвав [**испатиалаудиорендерстреамфорхртф:: останавливаться**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-245">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioRenderStreamForHrtf::Stop**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85)).</span></span> <span data-ttu-id="e7fdc-246">Если вы не собираетесь повторно использовать поток, освободите его ресурсы, вызвав [**испатиалаудиорендерстреамфорхртф:: Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e7fdc-246">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioRenderStreamForHrtf::Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)).</span></span>


```C++
// Stop the stream 
hr = spatialAudioStreamForHrtf->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStreamForHrtf->Reset();

CloseHandle(bufferCompletionEvent);
```



<span data-ttu-id="e7fdc-247">В следующем примере кода показана реализация вспомогательного метода **калкулатимиттерконеориентатионматрикс** , который использовался в приведенном выше примере для вычисления матрицы ориентации с учетом направления, на которое указывает трехмерный объект.</span><span class="sxs-lookup"><span data-stu-id="e7fdc-247">The following code example shows the implementation of the **CalculateEmitterConeOrientationMatrix** helper method which was used in the example above to calculate the orientation matrix given the direction the 3D object is pointing.</span></span>


```C++
DirectX::XMMATRIX CalculateEmitterConeOrientationMatrix(Windows::Foundation::Numerics::float3 listenerOrientationFront, Windows::Foundation::Numerics::float3 emitterDirection)
{
    DirectX::XMVECTOR vListenerDirection = DirectX::XMLoadFloat3(&listenerOrientationFront);
    DirectX::XMVECTOR vEmitterDirection = DirectX::XMLoadFloat3(&emitterDirection);
    DirectX::XMVECTOR vCross = DirectX::XMVector3Cross(vListenerDirection, vEmitterDirection);
    DirectX::XMVECTOR vDot = DirectX::XMVector3Dot(vListenerDirection, vEmitterDirection);
    DirectX::XMVECTOR vAngle = DirectX::XMVectorACos(vDot);
    float angle = DirectX::XMVectorGetX(vAngle);

    // The angle must be non-zero
    if (fabsf(angle) > FLT_EPSILON)
    {
        // And less than PI
        if (fabsf(angle) < DirectX::XM_PI)
        {
            return DirectX::XMMatrixRotationAxis(vCross, angle);
        }

        // If equal to PI, find any other non-collinear vector to generate the perpendicular vector to rotate about
        else
        {
            DirectX::XMFLOAT3 vector = { 1.0f, 1.0f, 1.0f };
            if (listenerOrientationFront.x != 0.0f)
            {
                vector.x = -listenerOrientationFront.x;
            }
            else if (listenerOrientationFront.y != 0.0f)
            {
                vector.y = -listenerOrientationFront.y;
            }
            else // if (_listenerOrientationFront.z != 0.0f)
            {
                vector.z = -listenerOrientationFront.z;
            }
            DirectX::XMVECTOR vVector = DirectX::XMLoadFloat3(&vector);
            vVector = DirectX::XMVector3Normalize(vVector);
            vCross = DirectX::XMVector3Cross(vVector, vEmitterDirection);
            return DirectX::XMMatrixRotationAxis(vCross, angle);
        }
    }

    // If the angle is zero, use an identity matrix
    return DirectX::XMMatrixIdentity();
}
```



## <a name="related-topics"></a><span data-ttu-id="e7fdc-248">См. также</span><span class="sxs-lookup"><span data-stu-id="e7fdc-248">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7fdc-249">Пространственный звук</span><span class="sxs-lookup"><span data-stu-id="e7fdc-249">Spatial Sound</span></span>](spatial-sound.md)
</dt> <dt>

[<span data-ttu-id="e7fdc-250">**испатиалаудиоклиент**</span><span class="sxs-lookup"><span data-stu-id="e7fdc-250">**ISpatialAudioClient**</span></span>](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)
</dt> <dt>

[<span data-ttu-id="e7fdc-251">**испатиалаудиубжект**</span><span class="sxs-lookup"><span data-stu-id="e7fdc-251">**ISpatialAudioObject**</span></span>](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)
</dt> </dl>

 

 
