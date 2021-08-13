---
description: Потоковая прорисовка звука (САР) — это приемник мультимедиа, который визуализирует звук.
ms.assetid: 5884a128-597d-432b-a706-e10c894d7965
title: Потоковая прорисовка звука
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01752cbec7d801177b39d939baeca93f720e12aafeaf9845c1aa0ded033c3fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238269"
---
# <a name="streaming-audio-renderer"></a>Потоковая прорисовка звука

Потоковая прорисовка звука (САР) — это приемник мультимедиа, который визуализирует звук. Каждый экземпляр САР визуализирует один аудиопоток. Для отображения нескольких потоков используйте несколько экземпляров.

Чтобы создать САР, вызовите одну из следующих функций:

-   [**Мфкреатеаудиорендерер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer). Возвращает указатель на САР.
-   [**Мфкреатеаудиорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate). Возвращает указатель на объект активации, который можно использовать для создания области САР.

Вторая функция, которая возвращает объект активации, является обязательной при воспроизведении защищенного содержимого, так как объект активации должен быть сериализован в защищенный процесс. Для очистки содержимого можно использовать любую из функций.

В области САР можно получить несжатое аудио в формате PCM или IEEE с плавающей точкой. Если скорость воспроизведения меньше 1 ×, то в САР автоматически настраивается шаг.

## <a name="configuring-the-audio-renderer"></a>Настройка модуля подготовки звука

В области «САР» поддерживается несколько атрибутов конфигурации. Механизм установки этих атрибутов зависит от того, какая функция вызывается для создания САР. При использовании функции [**мфкреатеаудиорендерер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) выполните следующие действия.

1.  Создайте новое хранилище атрибутов, вызвав [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).
2.  Добавьте атрибуты в хранилище атрибутов.
3.  Передайте хранилище атрибутов в функцию [**мфкреатеаудиорендерер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) в параметре *паудиоаттрибутес* .

При использовании функции [**мфкреатеаудиорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) функция возвращает указатель на интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) в параметре *ппактивате* . Используйте этот указатель, чтобы добавить атрибуты.

Список атрибутов конфигурации см. в разделе [атрибуты модуля подготовки звука](audio-renderer-attributes.md).

## <a name="selecting-the-audio-endpoint-device"></a>Выбор устройства для конечной точки аудио

*Устройство конечной точки аудио* — это устройство, которое либо визуализирует, либо фиксирует звук. К примерам относятся динамики, наушники, микрофоны и проигрыватели компакт-дисков. В САР всегда используется устройство отображения звука. Выбрать устройство можно двумя способами.

Первый подход заключается в перечислении устройств рендеринга звука в системе с помощью интерфейса [**иммдевицеенумератор**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) . Этот интерфейс описан в основной документации по API аудио.

1.  Создайте объект перечислителя устройств.
2.  Используйте перечислитель устройств для перечисления устройств рендеринга звука. Каждое устройство представлено указателем на интерфейс [**иммдевице**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) .
3.  Выберите устройство в зависимости от свойств устройства или выбора пользователя.
4.  Вызовите [**иммдевице:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) , чтобы получить идентификатор устройства.
5.  Задайте идентификатор устройства в качестве значения атрибута [**\_ \_ \_ \_ \_ идентификатора конечной точки для атрибута "модуль подготовки звука MF**](mf-audio-renderer-attribute-endpoint-id-attribute.md) ".

Вместо перечисления устройств можно указать звуковое устройство, указав его *роль*. Роль аудио определяет общую категорию использования. Например, роль *консоли* определена для игр и системных уведомлений, а роль *мультимедиа* определена для музыки и фильмов. Каждой роли назначено одно устройство отрисовки аудио, и пользователь может изменить эти назначения. Если вы указали роль устройства, то в САР используется любое звуковое устройство, назначенное для этой роли. Чтобы указать роль устройства, задайте атрибут [**\_ \_ \_ \_ \_ роли конечной точки атрибута подготовки звука MF**](mf-audio-renderer-attribute-endpoint-role-attribute.md) .

Два атрибута, перечисленные в этом разделе, являются взаимоисключающими. Если вы не настроили какой-либо из них, в САР используется звуковое устройство, назначенное роли **еконсоле** .

Следующий код перечисляет устройства отрисовки аудио и назначает первое устройство в списке в формате САР. В этом примере используется функция [**мфкреатеаудиорендерер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) для создания области САР.


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



Чтобы создать объект активации для САР, измените код, который появляется после вызова [**иммдевице:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) следующим образом:


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



## <a name="selecting-the-audio-session"></a>Выбор сеанса звука

Сеанс звука — это группа связанных звуковых потоков, которыми может управлять приложение. Приложение может управлять уровнем громкости и выключить состояние каждого сеанса. Сеансы идентифицируются по идентификатору GUID. Чтобы указать сеанс звука для САР, используйте атрибут [ \_ \_ \_ \_ \_ ID сеанса для атрибута "обработчик звука MF](mf-audio-renderer-attribute-session-id-attribute.md) ". Если этот атрибут не задан, то САР соединяет сеанс по умолчанию для этого процесса, идентифицируемый по **GUID \_ null**.

По умолчанию для сеанса звука используется конкретный процесс, то есть он содержит только потоки из вызывающего процесса. Чтобы присоединиться к межпроцессному сеансу, задайте атрибуту [ \_ \_ \_ \_ Флаги](mf-audio-renderer-attribute-flags-attribute.md) атрибута модуля подготовки звука **MF \_ \_ \_ \_ Флаги \_ Кросспроцесс**.

После создания САР вы используете интерфейс [**имфаудиополици**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) , чтобы присоединить сеанс к группе сеансов, все из которых управляются одним и тем же элементом управления громкостью на панели управления. Этот интерфейс также можно использовать для задания отображаемого имени и значка, отображаемого в элементе управления "Громкость".

## <a name="controlling-volume-levels"></a>Управление уровнями тома

Чтобы управлять основным уровнем громкости всех потоков в сеансе аудио в САР, используйте интерфейс [**имфсимплеаудиоволуме**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) . Чтобы управлять объемом отдельного потока или управлять объемом отдельных каналов в потоке, используйте интерфейс [**имфаудиостреамволуме**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) . Оба интерфейса получаются путем вызова [**имфжетсервице:: WebService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice). Можно вызвать метод **WebService** непосредственно в области САР или вызвать его в сеансе мультимедиа. Уровни тома выражаются как значения затухания. Для каждого канала уровень затухания — это продукт главного тома и тома канала.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Воспроизведение звука/видео](audio-video-playback.md)
</dt> </dl>

 

 
