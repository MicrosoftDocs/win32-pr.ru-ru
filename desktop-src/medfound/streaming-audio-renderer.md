---
description: Потоковая прорисовка звука (САР) — это приемник мультимедиа, который визуализирует звук.
ms.assetid: 5884a128-597d-432b-a706-e10c894d7965
title: Потоковая прорисовка звука
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59c5b55f197d5e9770c6f1be55f680c7f9136f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692580"
---
# <a name="streaming-audio-renderer"></a><span data-ttu-id="6ed81-103">Потоковая прорисовка звука</span><span class="sxs-lookup"><span data-stu-id="6ed81-103">Streaming Audio Renderer</span></span>

<span data-ttu-id="6ed81-104">Потоковая прорисовка звука (САР) — это приемник мультимедиа, который визуализирует звук.</span><span class="sxs-lookup"><span data-stu-id="6ed81-104">The streaming audio renderer (SAR) is a media sink that renders audio.</span></span> <span data-ttu-id="6ed81-105">Каждый экземпляр САР визуализирует один аудиопоток.</span><span class="sxs-lookup"><span data-stu-id="6ed81-105">Each instance of the SAR renders a single audio stream.</span></span> <span data-ttu-id="6ed81-106">Для отображения нескольких потоков используйте несколько экземпляров.</span><span class="sxs-lookup"><span data-stu-id="6ed81-106">To render multiple streams, use multiple instances of the SAR.</span></span>

<span data-ttu-id="6ed81-107">Чтобы создать САР, вызовите одну из следующих функций:</span><span class="sxs-lookup"><span data-stu-id="6ed81-107">To create the SAR, call either of the following functions:</span></span>

-   <span data-ttu-id="6ed81-108">[**Мфкреатеаудиорендерер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer).</span><span class="sxs-lookup"><span data-stu-id="6ed81-108">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer).</span></span> <span data-ttu-id="6ed81-109">Возвращает указатель на САР.</span><span class="sxs-lookup"><span data-stu-id="6ed81-109">Returns a pointer to the SAR.</span></span>
-   <span data-ttu-id="6ed81-110">[**Мфкреатеаудиорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate).</span><span class="sxs-lookup"><span data-stu-id="6ed81-110">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate).</span></span> <span data-ttu-id="6ed81-111">Возвращает указатель на объект активации, который можно использовать для создания области САР.</span><span class="sxs-lookup"><span data-stu-id="6ed81-111">Returns a pointer to an activation object, which can be used to create the SAR.</span></span>

<span data-ttu-id="6ed81-112">Вторая функция, которая возвращает объект активации, является обязательной при воспроизведении защищенного содержимого, так как объект активации должен быть сериализован в защищенный процесс.</span><span class="sxs-lookup"><span data-stu-id="6ed81-112">The second function, which returns an activation object, is required if you are playing protected content, because the activation object must be serialized to the protected process.</span></span> <span data-ttu-id="6ed81-113">Для очистки содержимого можно использовать любую из функций.</span><span class="sxs-lookup"><span data-stu-id="6ed81-113">For clear content, you can use either function.</span></span>

<span data-ttu-id="6ed81-114">В области САР можно получить несжатое аудио в формате PCM или IEEE с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="6ed81-114">The SAR can receive uncompressed audio in either PCM or IEEE floating-point format.</span></span> <span data-ttu-id="6ed81-115">Если скорость воспроизведения меньше 1 ×, то в САР автоматически настраивается шаг.</span><span class="sxs-lookup"><span data-stu-id="6ed81-115">If the playback rate is faster or slower than 1×, the SAR automatically adjusts the pitch.</span></span>

## <a name="configuring-the-audio-renderer"></a><span data-ttu-id="6ed81-116">Настройка модуля подготовки звука</span><span class="sxs-lookup"><span data-stu-id="6ed81-116">Configuring the Audio Renderer</span></span>

<span data-ttu-id="6ed81-117">В области «САР» поддерживается несколько атрибутов конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6ed81-117">The SAR supports several configuration attributes.</span></span> <span data-ttu-id="6ed81-118">Механизм установки этих атрибутов зависит от того, какая функция вызывается для создания САР.</span><span class="sxs-lookup"><span data-stu-id="6ed81-118">The mechanism for setting these attributes depends on which function you call to create the SAR.</span></span> <span data-ttu-id="6ed81-119">При использовании функции [**мфкреатеаудиорендерер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6ed81-119">If you use the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function, do the following:</span></span>

1.  <span data-ttu-id="6ed81-120">Создайте новое хранилище атрибутов, вызвав [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span><span class="sxs-lookup"><span data-stu-id="6ed81-120">Create a new attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="6ed81-121">Добавьте атрибуты в хранилище атрибутов.</span><span class="sxs-lookup"><span data-stu-id="6ed81-121">Add the attributes to the attribute store.</span></span>
3.  <span data-ttu-id="6ed81-122">Передайте хранилище атрибутов в функцию [**мфкреатеаудиорендерер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) в параметре *паудиоаттрибутес* .</span><span class="sxs-lookup"><span data-stu-id="6ed81-122">Pass the attribute store to the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function in the *pAudioAttributes* parameter.</span></span>

<span data-ttu-id="6ed81-123">При использовании функции [**мфкреатеаудиорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) функция возвращает указатель на интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) в параметре *ппактивате* .</span><span class="sxs-lookup"><span data-stu-id="6ed81-123">If you use the [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) function, the function returns a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface in the *ppActivate* parameter.</span></span> <span data-ttu-id="6ed81-124">Используйте этот указатель, чтобы добавить атрибуты.</span><span class="sxs-lookup"><span data-stu-id="6ed81-124">Use this pointer to add the attributes.</span></span>

<span data-ttu-id="6ed81-125">Список атрибутов конфигурации см. в разделе [атрибуты модуля подготовки звука](audio-renderer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="6ed81-125">For a list of configuration attributes, see [Audio Renderer Attributes](audio-renderer-attributes.md).</span></span>

## <a name="selecting-the-audio-endpoint-device"></a><span data-ttu-id="6ed81-126">Выбор устройства для конечной точки аудио</span><span class="sxs-lookup"><span data-stu-id="6ed81-126">Selecting the Audio Endpoint Device</span></span>

<span data-ttu-id="6ed81-127">*Устройство конечной точки аудио* — это устройство, которое либо визуализирует, либо фиксирует звук.</span><span class="sxs-lookup"><span data-stu-id="6ed81-127">An *audio endpoint device* is a hardware device that either renders or captures audio.</span></span> <span data-ttu-id="6ed81-128">К примерам относятся динамики, наушники, микрофоны и проигрыватели компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="6ed81-128">Examples include speakers, headphones, microphones, and CD players.</span></span> <span data-ttu-id="6ed81-129">В САР всегда используется устройство отображения звука.</span><span class="sxs-lookup"><span data-stu-id="6ed81-129">The SAR always uses an audio rendering device.</span></span> <span data-ttu-id="6ed81-130">Выбрать устройство можно двумя способами.</span><span class="sxs-lookup"><span data-stu-id="6ed81-130">There are two ways to select the device.</span></span>

<span data-ttu-id="6ed81-131">Первый подход заключается в перечислении устройств рендеринга звука в системе с помощью интерфейса [**иммдевицеенумератор**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .</span><span class="sxs-lookup"><span data-stu-id="6ed81-131">The first approach is to enumerate the audio rendering devices on the system, using the [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="6ed81-132">Этот интерфейс описан в основной документации по API аудио.</span><span class="sxs-lookup"><span data-stu-id="6ed81-132">This interface is documented in the core audio API documentation.</span></span>

1.  <span data-ttu-id="6ed81-133">Создайте объект перечислителя устройств.</span><span class="sxs-lookup"><span data-stu-id="6ed81-133">Create the device enumerator object.</span></span>
2.  <span data-ttu-id="6ed81-134">Используйте перечислитель устройств для перечисления устройств рендеринга звука.</span><span class="sxs-lookup"><span data-stu-id="6ed81-134">Use the device enumerator to enumerate audio rendering devices.</span></span> <span data-ttu-id="6ed81-135">Каждое устройство представлено указателем на интерфейс [**иммдевице**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) .</span><span class="sxs-lookup"><span data-stu-id="6ed81-135">Each device is represented by a pointer to the [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) interface.</span></span>
3.  <span data-ttu-id="6ed81-136">Выберите устройство в зависимости от свойств устройства или выбора пользователя.</span><span class="sxs-lookup"><span data-stu-id="6ed81-136">Select a device, based on the device properties or the user's selection.</span></span>
4.  <span data-ttu-id="6ed81-137">Вызовите [**иммдевице:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) , чтобы получить идентификатор устройства.</span><span class="sxs-lookup"><span data-stu-id="6ed81-137">Call [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to get the device identifier.</span></span>
5.  <span data-ttu-id="6ed81-138">Задайте идентификатор устройства в качестве значения атрибута [**\_ \_ \_ \_ \_ идентификатора конечной точки для атрибута "модуль подготовки звука MF**](mf-audio-renderer-attribute-endpoint-id-attribute.md) ".</span><span class="sxs-lookup"><span data-stu-id="6ed81-138">Set the device identifier as the value of the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID**](mf-audio-renderer-attribute-endpoint-id-attribute.md) attribute.</span></span>

<span data-ttu-id="6ed81-139">Вместо перечисления устройств можно указать звуковое устройство, указав его *роль*.</span><span class="sxs-lookup"><span data-stu-id="6ed81-139">Rather than enumerate devices, you can specify the audio device by its *role*.</span></span> <span data-ttu-id="6ed81-140">Роль аудио определяет общую категорию использования.</span><span class="sxs-lookup"><span data-stu-id="6ed81-140">An audio role identifies a general category of usage.</span></span> <span data-ttu-id="6ed81-141">Например, роль *консоли* определена для игр и системных уведомлений, а роль *мультимедиа* определена для музыки и фильмов.</span><span class="sxs-lookup"><span data-stu-id="6ed81-141">For example, the *console* role is defined for games and system notifications, while the *multimedia* role is defined for music and movies.</span></span> <span data-ttu-id="6ed81-142">Каждой роли назначено одно устройство отрисовки аудио, и пользователь может изменить эти назначения.</span><span class="sxs-lookup"><span data-stu-id="6ed81-142">Each role has one audio rendering device assigned to it, and the user can change these assignments.</span></span> <span data-ttu-id="6ed81-143">Если вы указали роль устройства, то в САР используется любое звуковое устройство, назначенное для этой роли.</span><span class="sxs-lookup"><span data-stu-id="6ed81-143">If you specify a device role, the SAR uses whatever audio device has been assigned for that role.</span></span> <span data-ttu-id="6ed81-144">Чтобы указать роль устройства, задайте атрибут [**\_ \_ \_ \_ \_ роли конечной точки атрибута подготовки звука MF**](mf-audio-renderer-attribute-endpoint-role-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="6ed81-144">To specify the device role, set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE**](mf-audio-renderer-attribute-endpoint-role-attribute.md) attribute.</span></span>

<span data-ttu-id="6ed81-145">Два атрибута, перечисленные в этом разделе, являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="6ed81-145">The two attributes listed in this section are mutually exclusive.</span></span> <span data-ttu-id="6ed81-146">Если вы не настроили какой-либо из них, в САР используется звуковое устройство, назначенное роли **еконсоле** .</span><span class="sxs-lookup"><span data-stu-id="6ed81-146">If you do not set either of them, the SAR uses the audio device that is assigned to the **eConsole** role.</span></span>

<span data-ttu-id="6ed81-147">Следующий код перечисляет устройства отрисовки аудио и назначает первое устройство в списке в формате САР.</span><span class="sxs-lookup"><span data-stu-id="6ed81-147">The following code enumerates the audio rendering devices and assigns the first device in the list to the SAR.</span></span> <span data-ttu-id="6ed81-148">В этом примере используется функция [**мфкреатеаудиорендерер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) для создания области САР.</span><span class="sxs-lookup"><span data-stu-id="6ed81-148">This example uses the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function to create the SAR.</span></span>


```C++
#include <mmdeviceapi.h>

HRESULT hr = S_OK;

IMMDeviceEnumerator *pEnum = NULL;      // Audio device enumerator.
IMMDeviceCollection *pDevices = NULL;   // Audio device collection.
IMMDevice *pDevice = NULL;              // An audio device.
IMFAttributes *pAttributes = NULL;      // Attribute store.
IMFMediaSink *pSink = NULL;             // Streaming audio renderer (SAR)

LPWSTR wstrID = NULL;                   // Device ID.

// Create the device enumerator.
hr = CoCreateInstance(
    __uuidof(MMDeviceEnumerator), 
    NULL,
    CLSCTX_ALL, 
    __uuidof(IMMDeviceEnumerator), 
    (void**)&pEnum
    );

// Enumerate the rendering devices.
if (SUCCEEDED(hr))
{
    hr = pEnum->EnumAudioEndpoints(eRender, DEVICE_STATE_ACTIVE, &pDevices);
}

// Get ID of the first device in the list.
if (SUCCEEDED(hr))
{
    hr = pDevices->Item(0, &pDevice);
}

if (SUCCEEDED(hr))
{
    hr = pDevice->GetId(&wstrID);
}

// Create an attribute store and set the device ID attribute.
if (SUCCEEDED(hr))
{
    hr = MFCreateAttributes(&pAttributes, 2);
}

if (SUCCEEDED(hr))
{
    hr = pAttributes->SetString(
        MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID, 
        wstrID
        );
}

// Create the audio renderer.
if (SUCCEEDED(hr))
{
    hr = MFCreateAudioRenderer(pAttributes, &pSink);    
}

SAFE_RELEASE(pEnum);
SAFE_RELEASE(pDevices);
SAFE_RELEASE(pDevice); 
SAFE_RELEASE(pAttributes);
CoTaskMemFree(wstrID);
```



<span data-ttu-id="6ed81-149">Чтобы создать объект активации для САР, измените код, который появляется после вызова [**иммдевице:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6ed81-149">To create the activation object for the SAR, change the code that appears after the call to [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to the following:</span></span>


```C++
IMFActivate *pActivate = NULL;          // Activation object.

if (SUCCEEDED(hr))
{
    hr = MFCreateAudioRendererActivate(&pActivate);    
}

if (SUCCEEDED(hr))
{
    hr = pActivate->SetString(
        MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID, 
        wstrID
        );
}

SAFE_RELEASE(pActivate);
```



## <a name="selecting-the-audio-session"></a><span data-ttu-id="6ed81-150">Выбор сеанса звука</span><span class="sxs-lookup"><span data-stu-id="6ed81-150">Selecting the Audio Session</span></span>

<span data-ttu-id="6ed81-151">Сеанс звука — это группа связанных звуковых потоков, которыми может управлять приложение.</span><span class="sxs-lookup"><span data-stu-id="6ed81-151">An audio session is a group of related audio streams that an application can manage collectively.</span></span> <span data-ttu-id="6ed81-152">Приложение может управлять уровнем громкости и выключить состояние каждого сеанса.</span><span class="sxs-lookup"><span data-stu-id="6ed81-152">The application can control the volume level and mute state of each session.</span></span> <span data-ttu-id="6ed81-153">Сеансы идентифицируются по идентификатору GUID.</span><span class="sxs-lookup"><span data-stu-id="6ed81-153">Sessions are identified by GUID.</span></span> <span data-ttu-id="6ed81-154">Чтобы указать сеанс звука для САР, используйте атрибут [ \_ \_ \_ \_ \_ ID сеанса для атрибута "обработчик звука MF](mf-audio-renderer-attribute-session-id-attribute.md) ".</span><span class="sxs-lookup"><span data-stu-id="6ed81-154">To specify the audio session for the SAR, use the [MF\_AUDIO\_RENDERER\_ATTRIBUTE\_SESSION\_ID](mf-audio-renderer-attribute-session-id-attribute.md) attribute.</span></span> <span data-ttu-id="6ed81-155">Если этот атрибут не задан, то САР соединяет сеанс по умолчанию для этого процесса, идентифицируемый по **GUID \_ null**.</span><span class="sxs-lookup"><span data-stu-id="6ed81-155">If you do not set this attribute, the SAR joins the default session for that process, identified by **GUID\_NULL**.</span></span>

<span data-ttu-id="6ed81-156">По умолчанию для сеанса звука используется конкретный процесс, то есть он содержит только потоки из вызывающего процесса.</span><span class="sxs-lookup"><span data-stu-id="6ed81-156">By default, an audio session is process-specific, meaning it contains only streams from the calling process.</span></span> <span data-ttu-id="6ed81-157">Чтобы присоединиться к межпроцессному сеансу, задайте атрибуту [ \_ \_ \_ \_ Флаги](mf-audio-renderer-attribute-flags-attribute.md) атрибута модуля подготовки звука **MF \_ \_ \_ \_ Флаги \_ Кросспроцесс**.</span><span class="sxs-lookup"><span data-stu-id="6ed81-157">To join a cross-process session, set the [MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS](mf-audio-renderer-attribute-flags-attribute.md) attribute with the value **MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_CROSSPROCESS**.</span></span>

<span data-ttu-id="6ed81-158">После создания САР вы используете интерфейс [**имфаудиополици**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) , чтобы присоединить сеанс к группе сеансов, все из которых управляются одним и тем же элементом управления громкостью на панели управления.</span><span class="sxs-lookup"><span data-stu-id="6ed81-158">After you create the SAR, you use the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface to join the session to a group of sessions, all of which are controlled by the same volume control in the control panel.</span></span> <span data-ttu-id="6ed81-159">Этот интерфейс также можно использовать для задания отображаемого имени и значка, отображаемого в элементе управления "Громкость".</span><span class="sxs-lookup"><span data-stu-id="6ed81-159">You can also use this interface to set the display name and the icon that appear in the volume control.</span></span>

## <a name="controlling-volume-levels"></a><span data-ttu-id="6ed81-160">Управление уровнями тома</span><span class="sxs-lookup"><span data-stu-id="6ed81-160">Controlling Volume Levels</span></span>

<span data-ttu-id="6ed81-161">Чтобы управлять основным уровнем громкости всех потоков в сеансе аудио в САР, используйте интерфейс [**имфсимплеаудиоволуме**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) .</span><span class="sxs-lookup"><span data-stu-id="6ed81-161">To control the master volume level of all the streams in the SAR's audio session, use the [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) interface.</span></span> <span data-ttu-id="6ed81-162">Чтобы управлять объемом отдельного потока или управлять объемом отдельных каналов в потоке, используйте интерфейс [**имфаудиостреамволуме**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) .</span><span class="sxs-lookup"><span data-stu-id="6ed81-162">To control the volume of an individual stream, or to control the volume of individual channels within a stream, use the [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) interface.</span></span> <span data-ttu-id="6ed81-163">Оба интерфейса получаются путем вызова [**имфжетсервице:: WebService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice).</span><span class="sxs-lookup"><span data-stu-id="6ed81-163">Both interfaces are obtained by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice).</span></span> <span data-ttu-id="6ed81-164">Можно вызвать метод **WebService** непосредственно в области САР или вызвать его в сеансе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6ed81-164">You can call **GetService** directly on the SAR, or call it on the Media Session.</span></span> <span data-ttu-id="6ed81-165">Уровни тома выражаются как значения затухания.</span><span class="sxs-lookup"><span data-stu-id="6ed81-165">Volume levels are expressed as attenuation values.</span></span> <span data-ttu-id="6ed81-166">Для каждого канала уровень затухания — это продукт главного тома и тома канала.</span><span class="sxs-lookup"><span data-stu-id="6ed81-166">For each channel, the attenuation level is the product of the master volume and the channel volume.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ed81-167">См. также</span><span class="sxs-lookup"><span data-stu-id="6ed81-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ed81-168">Воспроизведение звука/видео</span><span class="sxs-lookup"><span data-stu-id="6ed81-168">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 
