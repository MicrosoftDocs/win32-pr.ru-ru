---
description: В этой статье представлено несколько простых примеров, иллюстрирующих способы реализации пространственного звука с помощью статических пространственных объектов, динамических пространственных объектов и пространственных звуковых объектов, использующих функцию относительных функций Microsoft Head (ХРТФ).
ms.assetid: C99C342E-0BD9-486A-92AA-F8DCB72C1B00
title: Отображение пространственного звука с помощью пространственных звуковых объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9498b1792ed884624afef859f3f8c70d6001d91be5dff15211717651dc4767
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642504"
---
# <a name="render-spatial-sound-using-spatial-audio-objects"></a>Отображение пространственного звука с помощью пространственных звуковых объектов

В этой статье представлено несколько простых примеров, иллюстрирующих способы реализации пространственного звука с помощью статических пространственных объектов, динамических пространственных объектов и пространственных звуковых объектов, использующих функцию относительных функций Microsoft Head (ХРТФ). Этапы реализации всех трех методов очень похожи, и в этой статье представлен пример кода для каждого метода. Полный комплексный пример использования пространственных данных для работы с пространственными данными см. в [статье репозиторий GitHub с пространственными звуковыми](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio)данными (Майкрософт). обзор Windows Sonic, решения майкрософт на уровне платформы для поддержки пространственного звука на Xbox и Windows, см. в разделе [пространственный звук](spatial-sound.md).

## <a name="render-audio-using-static-spatial-audio-objects"></a>Прорисовка звука с помощью статических пространственных объектов Audio

Статический звуковой объект используется для визуализации звука по одному из 18 статических звуковых каналов, определенных в перечислении [**аудиубжекттипе**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) . Каждый из этих каналов представляет реальный или виртуализованный динамик в фиксированной точке, которая не перемещается со временем. Статические каналы, доступные на конкретном устройстве, зависят от используемого пространственного звукового формата. Список поддерживаемых форматов и их количества каналов см. в разделе [Пространственный звук](spatial-sound.md).

При инициализации пространственного аудиопотока необходимо указать, какие из доступных статических каналов будут использоваться потоком. Приведенные ниже примеры определений констант можно использовать для указания общих конфигураций динамиков и получения числа доступных каналов для каждого из них.


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



Первым шагом при отрисовке пространственного аудио является получение конечной точки аудио, в которую будут отправляться звуковые данные. Создайте экземпляр [**ммдевицеенумератор**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) и вызовите [**жетдефаултаудиоендпоинт**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) , чтобы получить устройство рендеринга звука по умолчанию.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



При создании пространственного аудиопотока необходимо указать формат звука, который будет использоваться потоком, предоставив структуру [вавеформатекс](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) . При воспроизведении звука из файла формат обычно определяется форматом звукового файла. В этом примере используется формат Mono, 32-bit, 48Hz.


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



Следующим шагом при подготовке пространственного звука является инициализация пространственного аудиопотока. Сначала получите экземпляр [**испатиалаудиоклиент**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) , вызвав [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate). Вызовите метод [**испатиалаудиоклиент:: исаудиубжектформатсуппортед**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) , чтобы обеспечить поддержку формата звука, который вы используете. Создайте событие, которое будет использоваться конвейером аудиопотока для уведомления приложения о том, что оно готово для дополнительных звуковых данных.

Заполнение структуры [**спатиалаудиубжектрендерстреамактиватионпарамс**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) , которая будет использоваться для инициализации пространственного аудиопотока. В этом примере в поле **статикобжекттипемаск** задана константа **\_ стерео чаннелмаск** , определенная ранее в этой статье, что означает, что аудиопоток может использовать только передний правый и левый каналы. Поскольку в этом примере используются только статические аудио-объекты и нет динамических объектов, поле **максдинамикобжекткаунт** имеет значение 0. Полю **Category** присваивается значение члена перечисления [**\_ \_ категории аудиопотока**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) , которое определяет, как система смешивает звук из этого потока с другими звуковыми источниками.

Вызовите метод [**испатиалаудиоклиент:: активатеспатиалаудиостреам**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) , чтобы активировать поток.


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
> при использовании интерфейсов [**испатиалаудиоклиент**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) в заголовке пакета средств разработки Xbox One (XDK) сначала необходимо вызвать **енаблеспатиалаудио** перед вызовом [**иммдевицеенумератор:: енумаудиоендпоинтс**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) или [**иммдевицеенумератор:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Несоблюдение этого действия приведет к тому, что при \_ вызове функции активации будет возвращена ошибка "E Interface". **енаблеспатиалаудио** доступен только для заголовков XDK, и его не нужно вызывать для универсальная платформа Windows приложений, выполняющихся на Xbox One, и для устройств, не являющихся Xbox One.

 

Объявите указатель для [**испатиалаудиубжект**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) , который будет использоваться для записи звуковых данных в статический канал. Обычные приложения будут использовать объект для каждого канала, указанного в поле **статикобжекттипемаск** . Для простоты в этом примере используется только один статический звуковой объект.


```C++
// In this simple example, one object will be rendered
Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObjectFrontLeft;
```



Перед входом в цикл рендеринга звука вызовите [**испатиалаудиубжектрендерстреам:: Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) , чтобы указать конвейеру мультимедиа начать запрашивать звуковые данные. В этом примере используется счетчик, чтобы прерывать отрисовку звука через 5 секунд.

В цикле подготовки к просмотру дождитесь события завершения буфера, предоставленного при инициализации пространственного аудиопотока, чтобы получать сигнал. При ожидании события следует задать разумное время ожидания (например, 100 мс), так как любое изменение типа рендеринга или конечной точки приведет к тому, что событие никогда не будет сигнальным. В этом случае можно вызвать метод [**испатиалаудиубжектрендерстреам:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) , чтобы попытаться сбросить пространственный звуковой поток.

Затем вызовите метод [**испатиалаудиубжектрендерстреам:: бегинупдатингаудиубжектс**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) , чтобы сообщить системе о том, что вы собираетесь заполнить буферы звуковых объектов данными. Этот метод возвращает количество доступных динамических звуковых объектов, не используемых в этом примере, и число кадров буфера для звуковых объектов, отображаемых этим потоком.

Если статический объект пространственного звука еще не создан, создайте один или несколько путем вызова [**испатиалаудиубжектрендерстреам:: активатеспатиалаудиубжект**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject), передав значение из перечисления [**аудиубжекттипе**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) , указывающее статический канал, на который визуализируется звук объекта.

Затем вызовите [**испатиалаудиубжект::**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) GetObject, чтобы получить указатель на звуковой буфер объекта пространственного звука. Этот метод также возвращает размер буфера в байтах. В этом примере используется вспомогательный метод **вритетоаудиубжектбуффер** для заполнения буфера звуковыми данными. Этот метод показан далее в этой статье. После записи в буфер в примере проверяется, было ли достигнуто 5-секундное время существования объекта, и, если это так, вызывается [**испатиалаудиубжект:: сетендофстреам**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) , чтобы позволить конвейеру звука узнать, что больше не будет записано никакого звука с помощью этого объекта, а для объекта задано значение **nullptr** , чтобы освободить свои ресурсы.

После записи данных во все звуковые объекты вызовите метод [**испатиалаудиубжектрендерстреам:: ендупдатингаудиубжектс**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) , чтобы система знала, что данные готовы для подготовки к просмотру. Вызвать метод @ **buffer** можно только между вызовами **бегинупдатингаудиубжектс** и **ендупдатингаудиубжектс**.


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



Когда вы завершите отрисовку пространственного звука, прервите пространственный поток звука, вызвав [**испатиалаудиубжектрендерстреам:: останавливаться**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop). Если вы не собираетесь повторно использовать поток, освободите его ресурсы, вызвав [**испатиалаудиубжектрендерстреам:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).


```C++
// Stop the stream
hr = spatialAudioStream->Stop();

// Don't want to start again, so reset the stream to free its resources
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



Вспомогательный метод **вритетоаудиубжектбуффер** записывает либо полный буфер выборок, либо количество оставшихся выборок, заданных ограничением времени, определяемым приложением. Это также можно определить, например, с учетом количества выборок, остающихся в исходном звуковом файле. Простая волна Sin, частота выполнения которой масштабируется с помощью входного параметра *Frequency* , создается и записывается в буфер.


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



## <a name="render-audio-using-dynamic-spatial-audio-objects"></a>Прорисовка звука с помощью динамических пространственных звуковых объектов

Динамические объекты позволяют визуализировать звук из произвольного расположения в пространстве относительно пользователя. Расположение и громкость динамического звукового объекта можно изменить с течением времени. Игры обычно используют расположение трехмерного объекта в мире игры для указания расположения динамического звукового объекта, связанного с ним. В следующем примере будет использоваться простая структура **My3dObject** для хранения минимального набора данных, необходимого для представления объекта. Эти данные включают указатель на [**испатиалаудиубжект**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), расположение, скорость, громкость и частоту тона для объекта, а также значение, которое хранит общее число кадров, для которых объект должен отображать звук.


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



Действия по реализации динамических звуковых объектов в основном совпадают с действиями статических звуковых объектов, описанных выше. Сначала получите конечную точку аудио.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



Затем инициализируйте пространственный аудиопоток. Получите экземпляр [**испатиалаудиоклиент**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) , вызвав [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate). Вызовите метод [**испатиалаудиоклиент:: исаудиубжектформатсуппортед**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) , чтобы обеспечить поддержку формата звука, который вы используете. Создайте событие, которое будет использоваться конвейером аудиопотока для уведомления приложения о том, что оно готово для дополнительных звуковых данных.

Вызовите метод [**испатиалаудиоклиент:: жетмаксдинамикобжекткаунт**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) , чтобы получить число динамических объектов, поддерживаемых системой. Если этот вызов возвращает значение 0, то динамические пространственные объекты не поддерживаются и не включаются на текущем устройстве. Сведения о включении пространственного аудио и о числе динамических звуковых объектов, доступных для различных пространственных форматов, см. в разделе [Пространственный звук](spatial-sound.md).

При заполнении структуры [**спатиалаудиубжектрендерстреамактиватионпарамс**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) задайте в поле **максдинамикобжекткаунт** максимальное число динамических объектов, которое будет использоваться приложением.

Вызовите метод [**испатиалаудиоклиент:: активатеспатиалаудиостреам**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) , чтобы активировать поток.


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



Ниже приведен код конкретного приложения, необходимый для поддержки этого примера, который динамически создает случайные позиционированные объекты аудио и сохраняет их в векторе.


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



Перед входом в цикл рендеринга звука вызовите [**испатиалаудиубжектрендерстреам:: Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) , чтобы указать конвейеру мультимедиа начать запрашивать звуковые данные.

В цикле рендеринга дождитесь события завершения буфера, которое мы предоставили при инициализации пространственного звукового потока для получения сигнала. При ожидании события следует задать разумное время ожидания (например, 100 мс), так как любое изменение типа рендеринга или конечной точки приведет к тому, что событие никогда не будет сигнальным. В этом случае можно вызвать метод [**испатиалаудиубжектрендерстреам:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) , чтобы попытаться сбросить пространственный звуковой поток.

Затем вызовите метод [**испатиалаудиубжектрендерстреам:: бегинупдатингаудиубжектс**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) , чтобы сообщить системе о том, что вы собираетесь заполнить буферы звуковых объектов данными. Этот метод возвращает число доступных динамических звуковых объектов и число кадров буфера для звуковых объектов, отображаемых этим потоком.

Каждый раз, когда счетчик порождений достигает указанного значения, мы активируем новый динамический звуковой объект, вызывая [**испатиалаудиубжектрендерстреам:: активатеспатиалаудиубжект**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) , указывая [**аудиубжекттипе \_ dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype). Если все доступные динамические звуковые объекты уже были выделены, этот метод возвратит **сплаудклнт \_ е больше \_ \_ \_ объектов**. В этом случае можно выбрать выпуск одного или нескольких ранее активированных звуковых объектов на основе приоритета конкретного приложения. После создания объекта Dynamic Audio он добавляется в новую структуру **My3dObject** со случайным положением, скоростью, объемом и частотой, которая затем добавляется в список активных объектов.

Затем выполните итерацию всех активных объектов, представленных в этом примере, с помощью определяемой приложением структуры **My3dObject** . Для каждого звукового объекта вызовите [**испатиалаудиубжект::**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) GetObject, чтобы получить указатель на звуковой буфер объекта пространственного звука. Этот метод также возвращает размер буфера в байтах. Вспомогательный метод **вритетоаудиубжектбуффер** для заполнения буфера звуковыми данными. После записи в буфер в примере обновляется расположение объекта Dynamic Audio путем вызова [**испатиалаудиубжект:: SetPosition**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition). Громкость объекта audio также может быть изменена путем вызова [**сетволуме**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume). Если вы не обновите расположение или том объекта, он будет хранить свое расположение и том с момента последнего задания. Если время существования объекта, определяемого приложением, было достигнуто, вызывается [**испатиалаудиубжект:: сетендофстреам**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) , чтобы позволить конвейеру звука узнать, что больше не будет записано никакого звука с помощью этого объекта, а объект имеет значение **nullptr** , чтобы освободить свои ресурсы.

После записи данных во все звуковые объекты вызовите метод [**испатиалаудиубжектрендерстреам:: ендупдатингаудиубжектс**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) , чтобы система знала, что данные готовы для подготовки к просмотру. Вызвать метод @ **buffer** можно только между вызовами **бегинупдатингаудиубжектс** и **ендупдатингаудиубжектс**.


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



Когда вы завершите отрисовку пространственного звука, прервите пространственный поток звука, вызвав [**испатиалаудиубжектрендерстреам:: останавливаться**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop). Если вы не собираетесь повторно использовать поток, освободите его ресурсы, вызвав [**испатиалаудиубжектрендерстреам:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).


```C++
// Stop the stream 
hr = spatialAudioStream->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



## <a name="render-audio-using-dynamic-spatial-audio-objects-for-hrtf"></a>Прорисовка звука с помощью динамических пространственных звуковых объектов для ХРТФ

Другой набор API-интерфейсов, [**испатиалаудиорендерстреамфорхртф**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) и [**испатиалаудиубжектфорхртф**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), включает Пространственный звук, который использует функцию Microsoft по относительным функциям передачи (хртф) для затухания звука для имитации положения передатчика в пространстве относительно пользователя, который можно изменить со временем. В дополнение к положению, ХРТФ Audio объекты позволяют указать ориентацию в пространстве, директивити, в которой выдается звук, например конус или кардиоид, и модель Decay по мере того, как объект перемещается ближе к виртуальному прослушивателю. обратите внимание, что эти интерфейсы хртф доступны только в том случае, если пользователь выбрал Windows Sonic для наушников как пространственный звуковой обработчик для устройства. сведения о настройке устройства для использования Windows Sonic для наушников см. в разделе [пространственный звук](spatial-sound.md).

интерфейсы api [**испатиалаудиорендерстреамфорхртф**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) и [**испатиалаудиубжектфорхртф**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) позволяют приложению явно использовать Windows Sonic для наушников путь отображения. эти api-интерфейсы не поддерживают пространственные форматы, такие как Dolby Atmos for Home Theater или Dolby Atmos for Headphones, а также переключение пользовательского формата вывода с помощью панели управления **звуком** или воспроизведение поверх динамиков. эти интерфейсы предназначены для использования в Windows Mixed Reality приложениях, которые хотят использовать специальные возможности Windows Sonic для наушников (например, предустановки и роллофф на основе расстояния, которые задаются программно, за пределами типичных конвейеров создания содержимого). В большинстве игр и сценариев Virtual Reality предпочтительнее использовать [**испатиалаудиоклиент**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) . Действия по реализации обоих наборов API практически идентичны, поэтому можно реализовать обе технологии и переключиться на среду выполнения в зависимости от того, какая функция доступна на текущем устройстве.

Приложения смешанной реальности обычно используют расположение трехмерного объекта в виртуальном мире, чтобы указать расположение динамического звукового объекта, связанного с ним. В следующем примере будет использоваться простая структура **My3dObjectForHrtf** для хранения минимального набора данных, необходимого для представления объекта. Эти данные включают указатель на [**испатиалаудиубжектфорхртф**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), положение, ориентацию, скорость и частоту тона для объекта, а также значение, которое хранит общее число кадров, для которых объект должен отображать звук.


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



Действия по реализации динамических ХРТФ аудио-объектов в основном аналогичны шагам для динамических звуковых объектов, описанных в предыдущем разделе. Сначала получите конечную точку аудио.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



Затем инициализируйте пространственный аудиопоток. Получите экземпляр [**испатиалаудиоклиент**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) , вызвав [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate). Вызовите метод [**испатиалаудиоклиент:: исаудиубжектформатсуппортед**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) , чтобы обеспечить поддержку формата звука, который вы используете. Создайте событие, которое будет использоваться конвейером аудиопотока для уведомления приложения о том, что оно готово для дополнительных звуковых данных.

Вызовите метод [**испатиалаудиоклиент:: жетмаксдинамикобжекткаунт**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) , чтобы получить число динамических объектов, поддерживаемых системой. Если этот вызов возвращает значение 0, то динамические пространственные объекты не поддерживаются и не включаются на текущем устройстве. Сведения о включении пространственного аудио и о числе динамических звуковых объектов, доступных для различных пространственных форматов, см. в разделе [Пространственный звук](spatial-sound.md).

При заполнении структуры [**спатиалаудиохртфактиватионпарамс**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) задайте в поле **максдинамикобжекткаунт** максимальное число динамических объектов, которое будет использоваться приложением. Параметры активации для ХРТФ поддерживают несколько дополнительных параметров, таких как [**спатиалаудиохртфдистанцедекай**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay), [**спатиалаудиохртфдирективитюнион**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion), [**спатиалаудиохртфенвиронменттипе**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype)и [**SpatialAudioHrtfOrientation**](spatialaudiohrtforientation.md), которые определяют значения этих параметров по умолчанию для новых объектов, создаваемых из потока. Эти параметры являются необязательными. Задайте для полей значение **nullptr** , чтобы не указывать значения по умолчанию.

Вызовите метод [**испатиалаудиоклиент:: активатеспатиалаудиостреам**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) , чтобы активировать поток.


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



Ниже приведен код конкретного приложения, необходимый для поддержки этого примера, который динамически создает случайные позиционированные объекты аудио и сохраняет их в векторе.


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



Перед входом в цикл рендеринга звука вызовите [**испатиалаудиубжектрендерстреамфорхртф:: Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) , чтобы указать конвейеру мультимедиа начать запрашивать звуковые данные.

В цикле рендеринга дождитесь события завершения буфера, которое мы предоставили при инициализации пространственного звукового потока для получения сигнала. При ожидании события следует задать разумное время ожидания (например, 100 мс), так как любое изменение типа рендеринга или конечной точки приведет к тому, что событие никогда не будет сигнальным. В этом случае можно вызвать метод [**испатиалаудиорендерстреамфорхртф:: Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) , чтобы попытаться сбросить пространственный звуковой поток.

Затем вызовите метод [**испатиалаудиорендерстреамфорхртф:: бегинупдатингаудиубжектс**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) , чтобы сообщить системе о том, что вы собираетесь заполнить буферы звуковых объектов данными. Этот метод возвращает количество доступных динамических звуковых объектов, не используемых в этом примере, и число кадров буфера для звуковых объектов, отображаемых этим потоком.

Каждый раз, когда счетчик порождений достигает указанного значения, мы активируем новый динамический звуковой объект, вызывая [**испатиалаудиорендерстреамфорхртф:: активатеспатиалаудиубжектфорхртф**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) , указывая [**аудиубжекттипе \_ dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype). Если все доступные динамические звуковые объекты уже были выделены, этот метод возвратит **сплаудклнт \_ е больше \_ \_ \_ объектов**. В этом случае можно выбрать выпуск одного или нескольких ранее активированных звуковых объектов на основе приоритета конкретного приложения. После создания динамического звукового объекта он добавляется в новую структуру **My3dObjectForHrtf** со случайными значениями позиций, вращения, скорости, объема и частоты, которые затем добавляются в список активных объектов.

Затем выполните итерацию всех активных объектов, представленных в этом примере, с помощью определяемой приложением структуры **My3dObjectForHrtf** . Для каждого звукового объекта вызовите [**испатиалаудиубжектфорхртф::**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) GetObject, чтобы получить указатель на звуковой буфер объекта пространственного звука. Этот метод также возвращает размер буфера в байтах. Вспомогательный метод **вритетоаудиубжектбуффер**, приведенный ранее в этой статье, для заполнения буфера звуковыми данными. После записи в буфер в примере обновляется положение и ориентация объекта audio ХРТФ путем вызова [**испатиалаудиубжектфорхртф:: SetPosition**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) и [**Испатиалаудиубжектфорхртф:: сеториентатион**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation). В этом примере вспомогательный метод **калкулатимиттерконеориентатионматрикс** используется для вычисления матрицы ориентации с учетом направления, на которое указывает трехмерный объект. Реализация этого метода показана ниже. Громкость объекта audio также может быть изменена путем вызова [**испатиалаудиубжектфорхртф:: сетгаин**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain). Если вы не обновите положение, ориентацию или объем объекта, он будет хранить положение, ориентацию и том из последней заданной копии. Если время существования объекта, определяемого приложением, было достигнуто, вызывается [**испатиалаудиубжектфорхртф:: сетендофстреам**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) , чтобы позволить конвейеру звука узнать, что больше не будет записано никакого звука с помощью этого объекта, а объект имеет значение **nullptr** , чтобы освободить свои ресурсы.

После записи данных во все звуковые объекты вызовите метод [**испатиалаудиорендерстреамфорхртф:: ендупдатингаудиубжектс**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) , чтобы система знала, что данные готовы для подготовки к просмотру. Вызвать метод @ **buffer** можно только между вызовами **бегинупдатингаудиубжектс** и **ендупдатингаудиубжектс**.


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



Когда вы завершите отрисовку пространственного звука, прервите пространственный поток звука, вызвав [**испатиалаудиорендерстреамфорхртф:: останавливаться**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85)). Если вы не собираетесь повторно использовать поток, освободите его ресурсы, вызвав [**испатиалаудиорендерстреамфорхртф:: Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)).


```C++
// Stop the stream 
hr = spatialAudioStreamForHrtf->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStreamForHrtf->Reset();

CloseHandle(bufferCompletionEvent);
```



В следующем примере кода показана реализация вспомогательного метода **калкулатимиттерконеориентатионматрикс** , который использовался в приведенном выше примере для вычисления матрицы ориентации с учетом направления, на которое указывает трехмерный объект.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Пространственный звук](spatial-sound.md)
</dt> <dt>

[**испатиалаудиоклиент**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)
</dt> <dt>

[**испатиалаудиубжект**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)
</dt> </dl>

 

 
