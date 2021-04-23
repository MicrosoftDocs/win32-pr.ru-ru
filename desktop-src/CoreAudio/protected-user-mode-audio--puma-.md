---
description: В Windows Vista появился звуковой режим защищенного пользователя (PUMA), обработчик аудио пользовательского режима в защищенной среде (PE), предоставляющий более безопасную среду для обработки аудио и подготовки к просмотру.
ms.assetid: 27a50026-9e48-48b1-9249-7528a97333c9
title: Звуковой режим защищенного пользователя (PUMA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233dc82109feb66472e66e4235031696937d70d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896334"
---
# <a name="protected-user-mode-audio-puma"></a><span data-ttu-id="e53b0-103">Звуковой режим защищенного пользователя (PUMA)</span><span class="sxs-lookup"><span data-stu-id="e53b0-103">Protected User Mode Audio (PUMA)</span></span>

<span data-ttu-id="e53b0-104">В Windows Vista появился звуковой режим защищенного пользователя (PUMA), обработчик аудио пользовательского режима в защищенной среде (PE), предоставляющий более безопасную среду для обработки аудио и подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="e53b0-104">Windows Vista introduced Protected User Mode Audio (PUMA), the user-mode audio engine in the Protected Environment (PE) that provides a safer environment for audio processing and rendering.</span></span> <span data-ttu-id="e53b0-105">Он позволяет включить только допустимые звуковые выходные данные и обеспечивает надежное отключение выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e53b0-105">It allows only the acceptable audio outputs to be enabled and ensures that the outputs are disabled reliably.</span></span> <span data-ttu-id="e53b0-106">Дополнительные сведения о PUMA см. в разделе [Output защита содержимого и Windows Vista](https://download.microsoft.com/download/5/D/6/5D6EAF2B-7DDF-476B-93DC-7CF0072878E6/output_protect.doc).</span><span class="sxs-lookup"><span data-stu-id="e53b0-106">For more information about PUMA, see [Output Content Protection and Windows Vista](https://download.microsoft.com/download/5/D/6/5D6EAF2B-7DDF-476B-93DC-7CF0072878E6/output_protect.doc).</span></span>

<span data-ttu-id="e53b0-107">PUMA был обновлен для Windows 7, чтобы предоставить следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="e53b0-107">PUMA has been updated for Windows 7 to provide the following features:</span></span>

-   <span data-ttu-id="e53b0-108">Установка битов системы управления последовательного копирования (СКМС) в конечных точках S/PDIF и высокоскоростных цифровых Защита содержимого (HDCP) на конечных точках High-Definitionного интерфейса (HDMI).</span><span class="sxs-lookup"><span data-stu-id="e53b0-108">Setting Serial Copying Management System (SCMS) bits on S/PDIF endpoints and High-bandwidth Digital Content Protection (HDCP) bits on High-Definition Multimedia Interface (HDMI) endpoints.</span></span>
-   <span data-ttu-id="e53b0-109">Включение элементов управления защиты СКМС и HDMI за пределами защищенной среды (PE).</span><span class="sxs-lookup"><span data-stu-id="e53b0-109">Enabling SCMS and HDMI protection controls outside of a Protected Environment (PE).</span></span>

## <a name="drm-protection-in-audio-drivers"></a><span data-ttu-id="e53b0-110">Защита DRM в аудио драйверах</span><span class="sxs-lookup"><span data-stu-id="e53b0-110">DRM Protection in Audio Drivers</span></span>

<span data-ttu-id="e53b0-111">Цифровые Rights Management (DRM) обеспечивают возможность упаковки данных мультимедиа в безопасном контейнере и прикрепление к содержимому правил использования.</span><span class="sxs-lookup"><span data-stu-id="e53b0-111">Digital Rights Management (DRM) provides the ability to package media data in a secure container and attach usage rules to the content.</span></span> <span data-ttu-id="e53b0-112">Например, поставщик содержимого может использовать **защиту от копирования** или **цифровой выход** для отключения прямых цифровых копий или передачи из системы ПК.</span><span class="sxs-lookup"><span data-stu-id="e53b0-112">For example, the content provider might use **Copy Protection** or **Digital Output Disable** to disable direct digital copies or transmission out of the PC system.</span></span>

<span data-ttu-id="e53b0-113">Звуковой стек в некоторых продуктах Майкрософт поддерживает DRM, реализуя правила использования, управляющие воспроизведением аудио содержимого.</span><span class="sxs-lookup"><span data-stu-id="e53b0-113">The audio stack in certain Microsoft products supports DRM by implementing the usage rules that govern playback of the audio content.</span></span> <span data-ttu-id="e53b0-114">Для воспроизведения защищенного содержимого основным драйвером должен быть *доверенный драйвер*. то есть драйвер должен быть сертифицирован на получение логотипа для Дрмлевел 1300.</span><span class="sxs-lookup"><span data-stu-id="e53b0-114">To play the protected content, the underlying audio driver must be a *trusted driver*; that is, the driver must be logo-certified for DRMLevel 1300.</span></span> <span data-ttu-id="e53b0-115">Сведения о разработке надежных драйверов можно получить с помощью интерфейсов, определенных в пакете средств разработки драйверов для Windows 2000 ("DDK") или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="e53b0-115">For information about developing trusted drivers, you can use interfaces that are defined in the Windows 2000 Driver Development Kit ("DDK") or later.</span></span> <span data-ttu-id="e53b0-116">Драйверы, разработанные с помощью DDK, реализуют необходимые интерфейсы для DRM.</span><span class="sxs-lookup"><span data-stu-id="e53b0-116">Drivers developed with the DDK will implement the necessary interfaces to DRM.</span></span> <span data-ttu-id="e53b0-117">Дополнительные сведения см. в статье [Digital Rights Management](/windows-hardware/drivers/audio/digital-rights-management).</span><span class="sxs-lookup"><span data-stu-id="e53b0-117">For more information, see [Digital Rights Management](/windows-hardware/drivers/audio/digital-rights-management).</span></span>

<span data-ttu-id="e53b0-118">Для подготовки к просмотру защищенного содержимого доверенный драйвер должен проверить, установлены ли для содержимого, переходящего через стек звука, **защиту от копирования** и **отключать цифровые выходные данные** , а также соответствующим образом реагировать на соответствующие параметры.</span><span class="sxs-lookup"><span data-stu-id="e53b0-118">To render the protected content, the trusted driver must check whether **Copy Protection** and **Digital Output Disable** are set on the content flowing through the audio stack, and respond to the settings accordingly.</span></span>

### <a name="copy-protection-rule"></a><span data-ttu-id="e53b0-119">Копировать правило защиты</span><span class="sxs-lookup"><span data-stu-id="e53b0-119">Copy Protection Rule</span></span>

<span data-ttu-id="e53b0-120">**Защита от копирования** означает, что в системе не разрешены прямые цифровые копии.</span><span class="sxs-lookup"><span data-stu-id="e53b0-120">**Copy Protection** indicates that direct digital copies are not allowed on the system.</span></span> <span data-ttu-id="e53b0-121">В соответствии с соглашением тестирования WHQL, приложение B было обновлено, чтобы отразить новые ожидания и требования к драйверу, когда для содержимого установлена **Защита от копирования** .</span><span class="sxs-lookup"><span data-stu-id="e53b0-121">Exhibit B to the WHQL Testing Agreement has been updated to reflect the new expectations and requirements of a driver when **Copy Protection** is set on the content.</span></span> <span data-ttu-id="e53b0-122">Для Windows 7 встроенный драйвер класса HD Audio соответствует последним требованиям.</span><span class="sxs-lookup"><span data-stu-id="e53b0-122">For Windows 7, the built-in HD audio class driver complies with the latest requirements.</span></span>

<span data-ttu-id="e53b0-123">Кроме того, что содержимое не может быть передано другому компоненту или сохранено на любом непостоянном носителе, не прошедшем проверку подлинности системой DRM, аудио драйвер выполняет следующие задачи, когда устанавливается **Защита от копирования** .</span><span class="sxs-lookup"><span data-stu-id="e53b0-123">In addition to ensuring that content is not allowed to pass to another component or be stored on any nonvolatile storage medium that is not authenticated by the DRM system, the audio driver performs the following tasks when **Copy Protection** is set:</span></span>

-   <span data-ttu-id="e53b0-124">Драйвер включает HDCP в конечных точках HDMI.</span><span class="sxs-lookup"><span data-stu-id="e53b0-124">The driver enables HDCP on HDMI endpoints.</span></span>
-   <span data-ttu-id="e53b0-125">Для интерфейсов S/PDIF драйвер проверяет, что сочетание битов кода L, CP и Category указывает, что СКМС состояние "никогда не задано", как определено в IEC 60958.</span><span class="sxs-lookup"><span data-stu-id="e53b0-125">For S/PDIF interfaces, the driver validates that the combination of L, Cp and Category Code bits indicates an SCMS state of "Copy Never", as defined in IEC 60958.</span></span>
-   <span data-ttu-id="e53b0-126">Бит L имеет значение 0, а код категории имеет значение "микшер цифрового сигнала".</span><span class="sxs-lookup"><span data-stu-id="e53b0-126">The L bit is set to 0 and the Category Code is set to "Digital Signal Mixer".</span></span>

<span data-ttu-id="e53b0-127">Структура **дрмригхтс** , используемая надежными звуковыми драйверами, указывает права содержимого DRM, назначенные ПИН-коду KS или объекту потока драйвера класса порта.</span><span class="sxs-lookup"><span data-stu-id="e53b0-127">The **DRMRIGHTS** structure, used by trusted audio drivers, specifies the DRM content rights assigned to a KS audio pin or to a port-class driver's stream object.</span></span> <span data-ttu-id="e53b0-128">Элемент **копипротект** указывает, задана ли **Защита копирования** для звукового содержимого.</span><span class="sxs-lookup"><span data-stu-id="e53b0-128">The **CopyProtect** member indicates whether **Copy Protection** is set on the audio content.</span></span>

<span data-ttu-id="e53b0-129">В Windows 7 использование **копипротект** является более четким.</span><span class="sxs-lookup"><span data-stu-id="e53b0-129">For Windows 7, the use of **CopyProtect** is stricter.</span></span> <span data-ttu-id="e53b0-130">Драйвер гарантирует, что для звуковых интерфейсов установлены элементы управления защитой, HDCP задается для выходных данных HDMI, а СКМС — для выходных данных S/PDIF, установив для состояния значение "никогда не копировать".</span><span class="sxs-lookup"><span data-stu-id="e53b0-130">The driver ensures that the protection controls are set on the audio interfaces, HDCP is set for HDMI output, and SCMS is set for S/PDIF output by setting the state to "Copy Never".</span></span>

### <a name="digital-output-disable-rule"></a><span data-ttu-id="e53b0-131">Правило отключения цифровых выходных данных</span><span class="sxs-lookup"><span data-stu-id="e53b0-131">Digital Output Disable Rule</span></span>

<span data-ttu-id="e53b0-132">**Отключение цифрового вывода** означает, что содержимое не может быть передано из системы.</span><span class="sxs-lookup"><span data-stu-id="e53b0-132">**Digital Output Disable** indicates that the content is not allowed to be transmitted out of the system.</span></span> <span data-ttu-id="e53b0-133">В Windows 7 встроенный драйвер класса HD Audio реагирует на этот параметр, включив HDCP в конечных точках HDMI.</span><span class="sxs-lookup"><span data-stu-id="e53b0-133">In Windows 7, the built-in HD audio class driver responds to this setting by enabling HDCP on HDMI endpoints.</span></span> <span data-ttu-id="e53b0-134">Это похоже на ответ драйвера на параметр **защиты от копирования** .</span><span class="sxs-lookup"><span data-stu-id="e53b0-134">This is similar to the driver's response to the **Copy Protection** setting.</span></span>

## <a name="enabling-content-protection-mechanisms-outside-of-a-protected-environment"></a><span data-ttu-id="e53b0-135">Включение механизмов защиты содержимого за пределами защищенной среды</span><span class="sxs-lookup"><span data-stu-id="e53b0-135">Enabling Content-Protection Mechanisms Outside of a Protected Environment</span></span>

<span data-ttu-id="e53b0-136">PUMA находится в отдельном процессе в защищенной среде (PE).</span><span class="sxs-lookup"><span data-stu-id="e53b0-136">PUMA resides in a separate process in the Protected Environment (PE).</span></span> <span data-ttu-id="e53b0-137">В Windows Vista для использования элементов управления защитой звука, предлагаемых PUMA, приложение мультимедиа должно находиться в PE-файле.</span><span class="sxs-lookup"><span data-stu-id="e53b0-137">In Windows Vista, to use the audio content protection controls offered by PUMA, a media application must be in a PE.</span></span> <span data-ttu-id="e53b0-138">Так как только интерфейсы API Media Foundation могут взаимодействовать с PE, элементы управления защиты содержимого ограничиваются приложениями, использующими Media Foundation интерфейсы API для потоковой передачи звукового содержимого.</span><span class="sxs-lookup"><span data-stu-id="e53b0-138">Because only Media Foundation APIs can interact with a PE, the content protection controls are limited to applications using Media Foundation APIs to stream audio content.</span></span>

<span data-ttu-id="e53b0-139">В Windows 7 любое приложение может получить доступ к элементам управления защитой содержимого, предоставляемым PUMAым доверием (OTA), независимо от того, находятся ли они в PE или используют Media Foundation API для воспроизведения звука.</span><span class="sxs-lookup"><span data-stu-id="e53b0-139">In Windows 7, any application can access the content protection controls provided by the PUMA Output Trust Authority (OTA), regardless of whether they are in a PE or using Media Foundation APIs for audio playback.</span></span>

## <a name="implementation-instructions"></a><span data-ttu-id="e53b0-140">Инструкции по реализации</span><span class="sxs-lookup"><span data-stu-id="e53b0-140">Implementation Instructions</span></span>

<span data-ttu-id="e53b0-141">Следующие шаги необходимы для того, чтобы звуковое приложение было управлять защитой содержимого СКМС или HDCP на конечной точке аудио.</span><span class="sxs-lookup"><span data-stu-id="e53b0-141">The following steps are required for an audio application to control SCMS or HDCP content protection on an audio endpoint.</span></span> <span data-ttu-id="e53b0-142">Поддерживаемые аудио API: DirectShow, DirectSound и ВАСАПИ.</span><span class="sxs-lookup"><span data-stu-id="e53b0-142">Supported Audio APIs are DirectShow, DirectSound, and WASAPI.</span></span>

<span data-ttu-id="e53b0-143">В этом примере кода используются следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="e53b0-143">This example code uses the following interfaces.</span></span>

-   [<span data-ttu-id="e53b0-144">**иммдевицеенумератор**</span><span class="sxs-lookup"><span data-stu-id="e53b0-144">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [<span data-ttu-id="e53b0-145">**иммдевице**</span><span class="sxs-lookup"><span data-stu-id="e53b0-145">**IMMDevice**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [<span data-ttu-id="e53b0-146">**иаудиоклиент**</span><span class="sxs-lookup"><span data-stu-id="e53b0-146">**IAudioClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)
-   [<span data-ttu-id="e53b0-147">**иммдевицеколлектион**</span><span class="sxs-lookup"><span data-stu-id="e53b0-147">**IMMDeviceCollection**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
-   [<span data-ttu-id="e53b0-148">**имфтрустедаутпут**</span><span class="sxs-lookup"><span data-stu-id="e53b0-148">**IMFTrustedOutput**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput)
-   [<span data-ttu-id="e53b0-149">**имфаутпутполици**</span><span class="sxs-lookup"><span data-stu-id="e53b0-149">**IMFOutputPolicy**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy)

<span data-ttu-id="e53b0-150">Приложение мультимедиа должно выполнять следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="e53b0-150">The media application must perform the following tasks.</span></span>

1.  <span data-ttu-id="e53b0-151">Настройте среду разработки.</span><span class="sxs-lookup"><span data-stu-id="e53b0-151">Set up the development environment.</span></span>
    -   <span data-ttu-id="e53b0-152">Сослаться на необходимые интерфейсы, включите заголовки, показанные в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="e53b0-152">Reference the required interfaces, include the headers shown in the following code.</span></span>
        ```cpp
        #include <MMdeviceapi.h>        // Device endpoint definitions
        #include <Mfidl.h>              // OTA interface definitions
        ```

        

    -   <span data-ttu-id="e53b0-153">Чтобы использовать интерфейсы OTA, необходимо создать ссылку на Мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="e53b0-153">Link to the Mfuuid.lib to use the OTA interfaces.</span></span>
    -   <span data-ttu-id="e53b0-154">Отключите отладчик ядра и средство проверки драйверов, чтобы избежать ошибок проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e53b0-154">Disable the kernel debugger and driver verifier to avoid any authentication checking errors.</span></span>
2.  <span data-ttu-id="e53b0-155">Перечислите все конечные точки в системе и выберите целевую конечную точку из коллекции конечных точек, как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="e53b0-155">Enumerate all endpoints in the system and select the target endpoint from the endpoint collection, as shown in the following code.</span></span> <span data-ttu-id="e53b0-156">Дополнительные сведения о перечислении устройств см. в разделе [перечисление звуковых устройств](/previous-versions//ms678716(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e53b0-156">For more information about enumerating devices, see [Enumerating Audio Devices](/previous-versions//ms678716(v=vs.85)).</span></span>
    ```cpp
    BOOL IsDigitalEndpoint(IMMDevice *pDevice)
    {
       PROPVARIANT         var;
       IPropertyStore      *pProperties = NULL;
       EndpointFormFactor  formfactor;
       BOOL                bResult = FALSE;
       HRESULT             hr = S_OK;
       PropVariantInit(&var);
       // Open endpoint properties
       hr = pDevice->OpenPropertyStore(STGM_READ, &pProperties);
       IF_FAILED_JUMP(hr, Exit);

       // get form factor 
       hr = pProperties->GetValue(PKEY_AudioEndpoint_FormFactor, &var);
       IF_FAILED_JUMP(hr, Exit);
       formfactor = (EndpointFormFactor)var.uiVal;
       // DigitalAudioDisplayDevice is defined same as HDMI formfactor
       if ((SPDIF == formfactor) || (DigitalAudioDisplayDevice == formfactor))
       {
           bResult = TRUE;
       }

    Exit:
       PropVariantClear(&var);
       SAFE_RELEASE(pProperties);
       return bResult;
    }
    ```

    

    ```cpp
    /******************************************************************
    *                                                                 *
    *  GetDevice:  Selects an endpoint that meets the requirements.   *
    *                                                                 *
    *  ppDevice: Receives a pointer to an IMMDevice interface of      *
    *            the device's endpoint object                         *                                             *                                            *
    *                                                                 *
    ******************************************************************/
    HRESULT GetDevice(IMMDevice** ppDevice)
    {
       IMMDeviceEnumerator    *pEnumerator = NULL;
       IMMDevice              *pDevice = NULL;
       IMMDeviceCollection    *pEndpoints = NULL;
       UINT                    cEndpoints = 0;

       const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
       const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

       // Get enumerator for audio endpoint devices
       hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, 
           NULL,
           CLSCTX_ALL, 
           IID_IMMDeviceEnumerator,
           (void**)&pEnumerator));


       EXIT_ON_ERROR(hr)

       // Enumerate all active endpoints,
       hr = pEnumerator->EnumAudioEndpoints (
           eRender,
           DEVICE_STATE_ACTIVE,
           &pEndpoints);
       EXIT_ON_ERROR(hr)

       hr = pEndpoints->GetCount(&cEndpoints);
       EXIT_ON_ERROR(hr)

       for (UINT i = 0; i < cEndpoints; i++)
       {
           hr = pEndpoints->Item(i, &pDevice);
           IF_FAILED_JUMP(hr, Exit);
           {
               // Select the endpoint that meets the requirements.
               // For example, SPDIF analog output or HDMI
               if (IsDigitalEndpoint(pDevice))
               {
                   *(ppDevice) = pDevice;
                   (*ppDevice)->AddRef();
                   break;
               }
           }
           SAFE_RELEASE(pDevice);
       }
    Exit:
       if (FAILED(hr))
       {
           // Notify error.
           // Not Shown.
       }
       SAFE_RELEASE(pEndpoints);
       SAFE_RELEASE(pEnumerator);
    }
    ```

    

3.  <span data-ttu-id="e53b0-157">Используйте указатель [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) для конечной точки, возвращенной процессом перечисления, чтобы активировать требуемый API потоковой передачи аудио и подготовить для потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="e53b0-157">Use the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) pointer to the endpoint returned by the enumeration process to activate the desired audio streaming API and prepare for streaming.</span></span> <span data-ttu-id="e53b0-158">Для разных интерфейсов аудио API требуется немного другая подготовка.</span><span class="sxs-lookup"><span data-stu-id="e53b0-158">Different audio APIs require slightly different preparation.</span></span>
    -   <span data-ttu-id="e53b0-159">Для звуковых приложений DShow:</span><span class="sxs-lookup"><span data-stu-id="e53b0-159">For DShow audio applications:</span></span>
        1.  <span data-ttu-id="e53b0-160">Создайте COM-объект DirectShow, вызвав [**иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) и указав IID \_ ибасефилтер в качестве идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e53b0-160">Create a DirectShow COM object by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) and specifying IID\_IBaseFilter as the interface identifier.</span></span>
            ```cpp
            IUnknown *pDShowFilter = NULL;
            ...
            hr = pDevice->Activate (
                              IID_IBaseFilter,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pDShowFilter));
            ```

            

        2.  <span data-ttu-id="e53b0-161">Создание графа фильтра DirectShow с этим COM-объектом, активируемым устройством.</span><span class="sxs-lookup"><span data-stu-id="e53b0-161">Build a DirectShow filter graph with this COM object activated by the device.</span></span> <span data-ttu-id="e53b0-162">Дополнительные сведения об этом процессе см. в разделе «Создание графа фильтра» документации по пакету SDK для DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e53b0-162">For more information about this process, see "Building the Filter Graph" in DirectShow SDK documentation.</span></span>
    -   <span data-ttu-id="e53b0-163">Для приложений Дсаунд Audio:</span><span class="sxs-lookup"><span data-stu-id="e53b0-163">For DSound audio applications:</span></span>
        1.  <span data-ttu-id="e53b0-164">Создайте COM-объект Дсаунд, вызвав [**иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) и указав IID \_ IDirectSound8 в качестве идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e53b0-164">Create a DSound COM object by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) and specifying IID\_IDirectSound8 as the interface identifier.</span></span>
            ```cpp
            IDirectSound8  *pDSSound8;
            ...
            hr = pDevice->Activate (
                              IID_IDirectSound8,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pDSSound8));
            ```

            

        2.  <span data-ttu-id="e53b0-165">Используйте созданный выше объект Дсаунд для программы Дсаунд для потоковой передаче.</span><span class="sxs-lookup"><span data-stu-id="e53b0-165">Use DSound object created above to program DSound for steaming.</span></span> <span data-ttu-id="e53b0-166">Дополнительные сведения об этом процессе см. в разделе [DirectSound](/previous-versions//bb219818(v=vs.85)) на сайте MSDN.</span><span class="sxs-lookup"><span data-stu-id="e53b0-166">For more information about this process, see [DirectSound](/previous-versions//bb219818(v=vs.85)) on MSDN.</span></span>
    -   <span data-ttu-id="e53b0-167">Для ВАСАПИ:</span><span class="sxs-lookup"><span data-stu-id="e53b0-167">For WASAPI:</span></span>
        1.  <span data-ttu-id="e53b0-168">Создайте COM-объект [**иаудиоклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) , вызвав [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) и указав IID \_ иаудиоклиент в качестве идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e53b0-168">Create an [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) COM object by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) and specifying IID\_IAudioClient as the interface identifier.</span></span>
            ```cpp
            IAudioClient *pIAudioClient = NULL;
            ...
            hr = pDevice->Activate (
                              IID_IAudioClient,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pIAudioClient));
            ```

            

        2.  <span data-ttu-id="e53b0-169">Откройте аудиопоток.</span><span class="sxs-lookup"><span data-stu-id="e53b0-169">Open the audio stream.</span></span>
            ```cpp
            hr = pIAudioClient->Initialize(...);
            ```

            
4.  <span data-ttu-id="e53b0-170">Начните потоковую передачу звука.</span><span class="sxs-lookup"><span data-stu-id="e53b0-170">Start audio streaming.</span></span>
5.  <span data-ttu-id="e53b0-171">Задайте политику защиты для потока.</span><span class="sxs-lookup"><span data-stu-id="e53b0-171">Set the protection policy on the stream.</span></span>
    1.  <span data-ttu-id="e53b0-172">Для клиентов ВАСАПИ получите ссылку на интерфейс [**имфтрустедаутпут**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) объекта OTA для потока, вызвав [**иаудиоклиент::**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) GetObject и указав IID \_ имфтрустедаутпут в качестве идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e53b0-172">For WASAPI clients, get a reference to the [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) interface of the output trust authority (OTA) object for the stream by calling [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) and specifying IID\_IMFTrustedOutput as the interface identifier.</span></span>
        ```cpp
        IMFTrustedOutput*       pTrustedOutput = NULL;
        hr = pIAudioClient>GetService(
                       __uuidof(IMFTrustedOutput),
                       (void**)& pTrustedOutput);
        ```

        

    2.  <span data-ttu-id="e53b0-173">Получите количество доступных объектов OTA, вызвав [**имфтрустедаутпут:: жетаутпуттрустаусоритикаунт**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritycount).</span><span class="sxs-lookup"><span data-stu-id="e53b0-173">Get a count of the available OTA objects by calling [**IMFTrustedOutput::GetOutputTrustAuthorityCount**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritycount).</span></span>
        ```cpp
        hr = pTrustedOutput->GetOutputTrustAuthorityCount(&m_dwCountOTA);
        ```

        

    3.  <span data-ttu-id="e53b0-174">Перечислите коллекцию OTA и получите ссылку на объект OTA, который поддерживает действие ПЕАКТИОН \_ Play.</span><span class="sxs-lookup"><span data-stu-id="e53b0-174">Enumerate the OTA collection and get a reference to the OTA object that supports the action PEACTION\_PLAY.</span></span> <span data-ttu-id="e53b0-175">Все Отас предоставляют интерфейс [**имфаутпуттрустаусорити**](/windows/win32/api/mfidl/nn-mfidl-imfoutputtrustauthority) .</span><span class="sxs-lookup"><span data-stu-id="e53b0-175">All OTAs expose the [**IMFOutputTrustAuthority**](/windows/win32/api/mfidl/nn-mfidl-imfoutputtrustauthority) interface.</span></span>
        ```cpp
        hr = pMFTrustedOutput->GetOutputTrustAuthorityByIndex(I, &pMFOutputTrustAuthority);
        hr = pMFOutputTrustAuthority->GetAction(&action) 
        ```

        

    4.  <span data-ttu-id="e53b0-176">Используйте интерфейс [**имфтрустедаутпут**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) , чтобы задать политику защиты для потока.</span><span class="sxs-lookup"><span data-stu-id="e53b0-176">Use the [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) interface to set the protection policy on the stream.</span></span>

        ```cpp
        hr = pTrustedOutput ->SetPolicy(&pPolicy, nPolicy, &pbTicket, &cbTicket);
        ```

        

        > [!Note]
        > <span data-ttu-id="e53b0-177">Если вы используете евр, [**сетполици**](/windows/win32/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) вызывает событие [МЕПОЛИЦИСЕТ](../medfound/mepolicyset.md) и возвращает MF \_ S, \_ ожидая \_ \_ \_ установки политики, чтобы указать, что OTA будет принудительно применять политику в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="e53b0-177">If you are using the EVR, [**SetPolicy**](/windows/win32/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) raises the [MEPolicySet](../medfound/mepolicyset.md) event and returns MF\_S\_WAIT\_FOR\_POLICY\_SET to indicate that the OTA will enforce the policy asynchronously.</span></span> <span data-ttu-id="e53b0-178">Однако в этом примере кода приложение является прямым клиентом ВАСАПИ, который получил объект OTA от клиента Audio (шаг 5 а).</span><span class="sxs-lookup"><span data-stu-id="e53b0-178">However, in this example code, the application is a direct WASAPI client that retrieved the OTA object from the audio client (Step 5 a).</span></span> <span data-ttu-id="e53b0-179">В отличие от Евр, аудио клиент и другие объекты ВАСАПИ не реализуют генераторы событий мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e53b0-179">Unlike the EVR, an audio client and other WASAPI objects do not implement media event generators.</span></span> <span data-ttu-id="e53b0-180">Без генераторов событий мультимедиа **имфтрустедаутпут:: сетполици** не возвращает MF \_ S \_ Wait \_ для \_ набора политик \_ .</span><span class="sxs-lookup"><span data-stu-id="e53b0-180">Without media event generators, **IMFTrustedOutput::SetPolicy** does not return MF\_S\_WAIT\_FOR\_POLICY\_SET.</span></span>
        >
        > <span data-ttu-id="e53b0-181">Параметры политики аудио должны быть заданы после запуска потоковой передачи звука, в противном случае [**имфтрустедаутпут:: жетаутпуттрустаусоритибиндекс**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritybyindex) завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e53b0-181">The audio policy settings must be set after audio streaming starts, otherwise [**IMFTrustedOutput::GetOutputTrustAuthorityByIndex**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritybyindex) fails.</span></span> <span data-ttu-id="e53b0-182">Кроме того, для поддержки этой функции основным драйвером аудиоподсистемы должен быть *доверенный драйвер*.</span><span class="sxs-lookup"><span data-stu-id="e53b0-182">Also, to support this feature, the underlying audio driver must be a *trusted driver*.</span></span>

         

        <span data-ttu-id="e53b0-183">В примере кода *пполици* является указателем на интерфейс [**имфаутпутполици**](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) объекта политики, реализованного клиентом.</span><span class="sxs-lookup"><span data-stu-id="e53b0-183">In the example code, *pPolicy* is a pointer to the [**IMFOutputPolicy**](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) interface of a client-implemented policy object.</span></span> <span data-ttu-id="e53b0-184">Дополнительные сведения см. в документации по [Media Foundation SDK](../medfound/microsoft-media-foundation-sdk.md) .</span><span class="sxs-lookup"><span data-stu-id="e53b0-184">For information, see [Media Foundation SDK](../medfound/microsoft-media-foundation-sdk.md) documentation.</span></span>

        <span data-ttu-id="e53b0-185">В реализации метода [**имфаутпутполици:: женератерекуиредсчемас**](/windows/win32/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) необходимо создать коллекцию систем защиты выходных данных (схем), которые должны быть принудительно соблюдены OTA.</span><span class="sxs-lookup"><span data-stu-id="e53b0-185">In the implementation of the [**IMFOutputPolicy::GenerateRequiredSchemas**](/windows/win32/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) method, a collection of the output protection systems (schemas) must be generated that the OTA must enforce.</span></span> <span data-ttu-id="e53b0-186">Каждая схема идентифицируется по идентификатору GUID и содержит данные конфигурации для системы защиты.</span><span class="sxs-lookup"><span data-stu-id="e53b0-186">Each schema is identified by a GUID and contains configuration data for the protection system.</span></span> <span data-ttu-id="e53b0-187">Убедитесь, что системы защиты в коллекции ограничены использованием надежных звуковых драйверов.</span><span class="sxs-lookup"><span data-stu-id="e53b0-187">Make sure that the protection systems in the collection are restricted to using trusted audio drivers.</span></span> <span data-ttu-id="e53b0-188">Это ограничение определяется по идентификатору GUID, **мфпротектион \_ трустедаудиодриверс**, Disable или констриктаудио.</span><span class="sxs-lookup"><span data-stu-id="e53b0-188">This restriction is identified by the GUID, **MFPROTECTION\_TRUSTEDAUDIODRIVERS**,DISABLE, or CONSTRICTAUDIO.</span></span> <span data-ttu-id="e53b0-189">Если \_ используется мфпротектион трустедаудиодриверс, то данные конфигурации для этой схемы являются DWORD.</span><span class="sxs-lookup"><span data-stu-id="e53b0-189">If MFPROTECTION\_TRUSTEDAUDIODRIVERS is used, the configuration data for this schema is a DWORD.</span></span> <span data-ttu-id="e53b0-190">Дополнительные сведения о схемах и связанных данных конфигурации см. в документации по пакету SDK для защищенной среды.</span><span class="sxs-lookup"><span data-stu-id="e53b0-190">For more information about the schemas and the related configuration data, see Protected Environment SDK documentation.</span></span>

        <span data-ttu-id="e53b0-191">Клиент также должен предоставить определение схемы, реализовав интерфейс [**имфаутпутсчема**](/windows/win32/api/mfidl/nn-mfidl-imfoutputschema) .</span><span class="sxs-lookup"><span data-stu-id="e53b0-191">The client must also provide the schema definition, by implementing the [**IMFOutputSchema**](/windows/win32/api/mfidl/nn-mfidl-imfoutputschema) interface.</span></span> <span data-ttu-id="e53b0-192">[**Имфаутпутсчема:: жетсчематипе**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getschematype) извлекает **мфпротектион \_ трустедаудиодриверс** в качестве GUID схемы.</span><span class="sxs-lookup"><span data-stu-id="e53b0-192">[**IMFOutputSchema::GetSchemaType**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getschematype) retrieves **MFPROTECTION\_TRUSTEDAUDIODRIVERS** as the schema GUID.</span></span> <span data-ttu-id="e53b0-193">[**Имфаутпутсчема:: жетконфигуратиондата**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getconfigurationdata) возвращает указатель на данные конфигурации схемы.</span><span class="sxs-lookup"><span data-stu-id="e53b0-193">[**IMFOutputSchema::GetConfigurationData**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getconfigurationdata) returns a pointer to the schema's configuration data.</span></span>

6.  <span data-ttu-id="e53b0-194">Продолжить потоковую передачу звука.</span><span class="sxs-lookup"><span data-stu-id="e53b0-194">Continue audio streaming.</span></span>
7.  <span data-ttu-id="e53b0-195">Убедитесь, что политика защиты была очищена перед остановкой потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="e53b0-195">Make sure the protection policy is clear before stopping streaming.</span></span>

    <span data-ttu-id="e53b0-196">Отпустите приведенные выше ссылки на интерфейс политики.</span><span class="sxs-lookup"><span data-stu-id="e53b0-196">Release the related policy interface references above.</span></span>

    <span data-ttu-id="e53b0-197">Вызовы выпуска удаляют ранее установленные параметры политики.</span><span class="sxs-lookup"><span data-stu-id="e53b0-197">The release calls clear the previously set policy settings.</span></span>

    > [!Note]  
    > <span data-ttu-id="e53b0-198">При каждом перезапуске потока политика защиты должна быть снова установлена в потоке.</span><span class="sxs-lookup"><span data-stu-id="e53b0-198">Every time a stream is restarted, the protection policy must be set again on the stream.</span></span> <span data-ttu-id="e53b0-199">Процедура описана в шаге 5-d.</span><span class="sxs-lookup"><span data-stu-id="e53b0-199">The procedure is described in step 5-d.</span></span>

    ```cpp
    pMFOutputTrustAuthority->Release()
    pMFTrustedOutput->Release()
    ```
  

<span data-ttu-id="e53b0-200">В следующих примерах кода показан пример реализации политики и объектов схемы.</span><span class="sxs-lookup"><span data-stu-id="e53b0-200">The following code examples show a sample implementation of the policy and schema objects.</span></span>


```cpp
//OTADsoundSample.cpp
#include <stdio.h>
#include <tchar.h>
#include <initguid.h>
#include <windows.h>
#include <mmreg.h>
#include <dsound.h>

#include <mfidl.h>
#include <Mmdeviceapi.h>
#include <AVEndpointKeys.h>
#include "OTADSoundSample.h"

#define STATIC_KSDATAFORMAT_SUBTYPE_AC3\
    DEFINE_WAVEFORMATEX_GUID(WAVE_FORMAT_DOLBY_AC3_SPDIF)
DEFINE_GUIDSTRUCT("00000092-0000-0010-8000-00aa00389b71", KSDATAFORMAT_SUBTYPE_AC3);
#define KSDATAFORMAT_SUBTYPE_AC3 DEFINE_GUIDNAMED(KSDATAFORMAT_SUBTYPE_AC3)


HRESULT SetOTAPolicy(IMMDevice *_pMMDevice,
                     DWORD _dwConfigData,
                     IMFTrustedOutput **_ppMFTrustedOutput,
                     IMFOutputTrustAuthority **ppMFOutputTrustAuthority,
                     IMFOutputPolicy **_ppMFOutputPolicy);
HRESULT ClearOTAPolicy(IMFTrustedOutput *_pMFTrustedOutput,
                       IMFOutputTrustAuthority *_pMFOutputTrustAuthority,
                       IMFOutputPolicy *_pMFOutputPolicy);


const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

BOOL IsDigitalEndpoint(IMMDevice *pDevice)
{
    PROPVARIANT         var;
    IPropertyStore      *pProperties = NULL;
    EndpointFormFactor  formfactor;
    BOOL                bResult = FALSE;
    HRESULT             hr = S_OK;
    PropVariantInit(&var);

    // Open endpoint properties
    hr = pDevice->OpenPropertyStore(STGM_READ, &pProperties);
    IF_FAILED_JUMP(hr, Exit);

    // get form factor 
    hr = pProperties->GetValue(PKEY_AudioEndpoint_FormFactor, &var);
    IF_FAILED_JUMP(hr, Exit);

    formfactor = (EndpointFormFactor)var.uiVal;
    if ((SPDIF == formfactor) || (DigitalAudioDisplayDevice == formfactor))
    {
        bResult = TRUE;
    }

Exit:
    PropVariantClear(&var);
    SAFE_RELEASE(pProperties);

    return bResult;
}


HRESULT GetDigitalAudioEndpoint(IMMDevice** ppDevice)
{
    IMMDeviceEnumerator    *pEnumerator = NULL;
    IMMDevice              *pDevice = NULL;
    IMMDeviceCollection    *pEndpoints = NULL;
    UINT                    cEndpoints = 0;
    HRESULT hr = S_OK;

    *ppDevice = NULL;
    // Get enumerator for audio endpoint devices.
    hr = CoCreateInstance(CLSID_MMDeviceEnumerator, NULL,
                          CLSCTX_ALL, IID_IMMDeviceEnumerator,
                          (void**)&pEnumerator);
    IF_FAILED_JUMP(hr, Exit);

    // Enumerate all active render endpoints, 
    hr = pEnumerator->EnumAudioEndpoints(eRender, DEVICE_STATE_ACTIVE, &pEndpoints);
    IF_FAILED_JUMP(hr, Exit);

    hr = pEndpoints->GetCount(&cEndpoints);
    IF_FAILED_JUMP(hr, Exit);

    for (UINT i = 0; i < cEndpoints; i++)
    {
        hr = pEndpoints->Item(i, &pDevice);
        IF_FAILED_JUMP(hr, Exit);
        // Select the endpoint that meets the requirements.
        // For example, SPDIF analog output or HDMI
        // Not Shown.
        if (IsDigitalEndpoint(pDevice))
        {
            *ppDevice = pDevice;
            (*ppDevice)->AddRef();
            break;
        }
        SAFE_RELEASE(pDevice);
    }
Exit:
    if (FAILED(hr))
    {
        // Notify error.
        // Not Shown.
    }
    SAFE_RELEASE(pEndpoints);
    SAFE_RELEASE(pEnumerator);
    return hr; 
}


//-------------------------------------------------------------------
int __cdecl wmain(int argc, char* argv[])
{
    IMMDevice *pEndpoint=NULL;
    HRESULT hr = S_OK;

    // DSound related variables
    IDirectSound8*          DSSound8 = NULL; 
    IDirectSoundBuffer*     DSBuffer = NULL; 
    DSBUFFERDESC            DSBufferDesc;
    WAVEFORMATEXTENSIBLE    wfext;
    WORD nChannels = 2;
    DWORD nSamplesPerSec = 48000;
    WORD wBitsPerSample = 16;

    // OTA related variables
    IMFTrustedOutput *pMFTrustedOutput=NULL;
    IMFOutputPolicy *pMFOutputPolicy=NULL;
    IMFOutputTrustAuthority *pMFOutputTrustAuthority=NULL;
    DWORD dwConfigData=0;

    // Initialize COM
    hr = CoInitialize(NULL);
    IF_FAILED_JUMP(hr, Exit);

    printf("OTA test app for DSound\n");

    hr = GetDigitalAudioEndpoint(&pEndpoint);
    IF_FAILED_JUMP(hr, Exit);

    if (pEndpoint)
    {
        printf("Found digital audio endpoint.\n");
    }
    //
    // Active DSound interface
    //
    hr = pEndpoint->Activate(IID_IDirectSound8, CLSCTX_INPROC_SERVER, NULL, reinterpret_cast<void **>(&DSSound8));
    IF_FAILED_JUMP(hr, Exit);

    nChannels = 2;
    nSamplesPerSec = 48000;
    wBitsPerSample = 16;

    ZeroMemory(&wfext, sizeof(wfext));
    wfext.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
    wfext.Format.nChannels = nChannels;
    wfext.Format.nSamplesPerSec = nSamplesPerSec;
    wfext.Format.wBitsPerSample = wBitsPerSample;
    wfext.Format.nBlockAlign = (nChannels * wBitsPerSample) / 8;
    wfext.Format.nAvgBytesPerSec = nSamplesPerSec * ((nChannels * wBitsPerSample) / 8);
    wfext.Format.cbSize = 22;
    wfext.Samples.wValidBitsPerSample = wBitsPerSample;
    wfext.dwChannelMask = 0x3;
    wfext.SubFormat = KSDATAFORMAT_SUBTYPE_PCM;
#if 1 
    wfext.SubFormat = KSDATAFORMAT_SUBTYPE_AC3;
#endif

    ZeroMemory(&DSBufferDesc, sizeof(DSBufferDesc));
    DSBufferDesc.dwSize = sizeof(DSBufferDesc);
    DSBufferDesc.dwFlags = DSBCAPS_GLOBALFOCUS | DSBCAPS_LOCSOFTWARE | DSBCAPS_GETCURRENTPOSITION2;
    DSBufferDesc.lpwfxFormat = (WAVEFORMATEX *)&wfext;
    DSBufferDesc.dwBufferBytes = wfext.Format.nAvgBytesPerSec / 100;

    HWND hwnd = GetForegroundWindow();
    hr = DSSound8->SetCooperativeLevel(hwnd, DSSCL_PRIORITY);
    IF_FAILED_JUMP(hr, Exit);

    hr = DSSound8->CreateSoundBuffer(&DSBufferDesc, &DSBuffer, NULL);
    IF_FAILED_JUMP(hr, Exit);

    hr = DSBuffer->Play(0, 0, DSBPLAY_LOOPING);
    IF_FAILED_JUMP(hr, Exit);

    printf("Will set the following audio policy:\n");
    printf("Test Certificate Enable: %s\n", TRUE ? "True" : "False");
    printf("Copy OK: %s\n", FALSE ? "True" : "False");
    printf("Digital Output Disable: %s\n", FALSE ? "True" : "False");
    printf("DRM Level: %u\n", 1300);

    // Set policy when the stream is in RUN state
    dwConfigData = MAKE_MFPROTECTIONDATA_TRUSTEDAUDIODRIVERS2(TRUE, /*_bTestCertificateEnable*/ 
                                                              FALSE, /*_bDigitalOutputDisable*/ 
                                                              FALSE, /*_bCopyOK*/ 
                                                              1300 /*_dwDrmLevel*/);

    hr = SetOTAPolicy(pEndpoint,dwConfigData, &pMFTrustedOutput, &pMFOutputTrustAuthority,&pMFOutputPolicy); 
    IF_FAILED_JUMP(hr, Exit);

    //
    // Perform all the necessary streaming operations here.
    //

    // stop audio streaming
    DSBuffer->Stop();

    // In order for the stream to restart successfully 
    // Need to release the following OutputTrust* interface to release audio endpoint
    hr = ClearOTAPolicy(pMFTrustedOutput,pMFOutputTrustAuthority,pMFOutputPolicy);
    IF_FAILED_JUMP(hr, Exit);

    // After above release operations, the following Play() will succeed without without device-in-use error message 0x8889000A
    DSBuffer->SetCurrentPosition(0);
    hr = DSBuffer->Play(0, 0, DSBPLAY_LOOPING);
    IF_FAILED_JUMP(hr, Exit);

    // Need to reset the new audio protection state because previous settings were gone with the ClearOTAPolicy call.
    dwConfigData = MAKE_MFPROTECTIONDATA_TRUSTEDAUDIODRIVERS2(TRUE, /*_bTestCertificateEnable*/ 
                                                              FALSE, /*_bDigitalOutputDisable*/ 
                                                              FALSE, /*_bCopyOK*/ 
                                                              1300 /*_dwDrmLevel*/);

    hr = SetOTAPolicy(pEndpoint,dwConfigData, &pMFTrustedOutput, &pMFOutputTrustAuthority,&pMFOutputPolicy); 
    IF_FAILED_JUMP(hr, Exit);

    // Clean up setting before leaving your streaming app.
    hr = ClearOTAPolicy(pMFTrustedOutput,pMFOutputTrustAuthority,pMFOutputPolicy);
    IF_FAILED_JUMP(hr, Exit);

    DSBuffer->SetCurrentPosition(0);

Exit:
    SAFE_RELEASE(DSBuffer);
    SAFE_RELEASE(DSSound8);

    SAFE_RELEASE(pEndpoint);

    CoUninitialize();

    return 0;
}
```




```cpp
//OTADSoundSample.h
// Macro defines
#define IF_FAILED_JUMP(_hresult, label)                         \
    if(FAILED(_hresult))                                        \
    {                                                           \
        goto label;                                             \
    }

#define SAFE_RELEASE(p) \
    if (NULL != p) { \
        (p)->Release(); \
        (p) = NULL; \
    }

#define IF_TRUE_ACTION_JUMP(condition, action, label)           \
    if(condition)                                               \
    {                                                           \
        action;                                                 \
        goto label;                                             \
    }
```




```cpp
// outputpolicy.h

class CTrustedAudioDriversOutputPolicy : public CMFAttributesImpl<IMFOutputPolicy> 
{
friend
    HRESULT CreateTrustedAudioDriversOutputPolicy(DWORD dwConfigData, IMFOutputPolicy **ppMFOutputPolicy);
private:
    ULONG m_cRefCount;
    DWORD m_dwConfigData;
    GUID m_guidOriginator;
    IMFOutputSchema *m_pOutputSchema;
    
    CTrustedAudioDriversOutputPolicy(DWORD dwConfigData, HRESULT &hr);
    ~CTrustedAudioDriversOutputPolicy();

public:
    // IUnknown methods
    HRESULT STDMETHODCALLTYPE QueryInterface(/* [in] */ REFIID riid,/* [out] */ LPVOID *ppvObject);
    ULONG STDMETHODCALLTYPE AddRef();
    ULONG STDMETHODCALLTYPE Release();
    
    // IMFOutputPolicy methods
    HRESULT STDMETHODCALLTYPE
        GenerateRequiredSchemas( 
            /* [in] */ DWORD dwAttributes,
            /* [in] */ GUID guidOutputSubType,
            /* [in] */ GUID *rgGuidProtectionSchemasSupported,
            /* [in] */ DWORD cProtectionSchemasSupported,
            /* [annotation][out] */ 
            __out  IMFCollection **ppRequiredProtectionSchemas);

    HRESULT STDMETHODCALLTYPE GetOriginatorID(/* [annotation][out] */ __out  GUID *pguidOriginatorID);

    HRESULT STDMETHODCALLTYPE GetMinimumGRLVersion(/* [annotation][out] */ __out  DWORD *pdwMinimumGRLVersion);
}; // CTrustedAudioDriversOutputPolicy

class CTrustedAudioDriversOutputSchema : public CMFAttributesImpl<IMFOutputSchema> 
{

friend
    HRESULT CreateTrustedAudioDriversOutputSchema(
        DWORD dwConfigData,
        GUID guidOriginatorID,
        IMFOutputSchema **ppMFOutputSchema
    );

private:
    CTrustedAudioDriversOutputSchema(DWORD dwConfigData, GUID guidOriginatorID);
    ~CTrustedAudioDriversOutputSchema();

    ULONG m_cRefCount;
    DWORD m_dwConfigData;
    GUID m_guidOriginatorID;
    
public:
    // IUnknown methods
    HRESULT STDMETHODCALLTYPE QueryInterface(
       /* [in] */ REFIID riid,
       /* [out] */ LPVOID *ppvObject
    );
    ULONG STDMETHODCALLTYPE AddRef();
    ULONG STDMETHODCALLTYPE Release();

    // IMFOutputSchema methods
    HRESULT STDMETHODCALLTYPE GetConfigurationData(__out DWORD *pdwVal);
    HRESULT STDMETHODCALLTYPE GetOriginatorID(__out GUID *pguidOriginatorID);
    HRESULT STDMETHODCALLTYPE GetSchemaType(__out GUID *pguidSchemaType);

}; // CTrustedAudioDriversOutputSchema
```




```cpp
// outputpolicy.cpp

#include <windows.h>
#include <tchar.h>
#include <mfidl.h>
#include <atlstr.h>
#include <attributesbase.h>
#include "OTADSoundSample.h"

#include <Mmdeviceapi.h>
#include "OutputPolicy.h"

#define RETURN_INTERFACE(T, iid, ppOut) \
    if (IsEqualIID(__uuidof(T), (iid))) { \
        this->AddRef(); \
        *(ppOut) = static_cast<T *>(this); \
        return S_OK; \
    } else {} (void)0

//--------------------------------------------------------------------------
// Implementation for CTrustedAudioDriversOutputPolicy
//--------------------------------------------------------------------------
// constructor
CTrustedAudioDriversOutputPolicy::CTrustedAudioDriversOutputPolicy(DWORD dwConfigData, HRESULT &hr)
: m_cRefCount(1), m_dwConfigData(dwConfigData), m_pOutputSchema(NULL)
{
    hr = CoCreateGuid(&m_guidOriginator);
    IF_FAILED_JUMP(hr, Exit);

    hr = CreateTrustedAudioDriversOutputSchema(dwConfigData, m_guidOriginator, &m_pOutputSchema);
    IF_FAILED_JUMP(hr, Exit);

Exit:
    if (FAILED(hr))
    {
        printf("CreateTrustedAudioDriversOutputSchema failed: hr = 0x%08x", hr);
    }
    return;
}

// destructor
CTrustedAudioDriversOutputPolicy::~CTrustedAudioDriversOutputPolicy()
{
    if (NULL != m_pOutputSchema) 
    {
        m_pOutputSchema->Release();
    }
}


// IUnknown::QueryInterface
HRESULT STDMETHODCALLTYPE
    CTrustedAudioDriversOutputPolicy::QueryInterface(
        /* [in] */ REFIID riid,
        /* [out] */ LPVOID *ppvObject)
{
    HRESULT hr = E_NOINTERFACE;

    IF_TRUE_ACTION_JUMP((NULL == ppvObject), hr = E_POINTER, Exit);

    *ppvObject = NULL;

    RETURN_INTERFACE(IUnknown, riid, ppvObject);
    RETURN_INTERFACE(IMFAttributes, riid, ppvObject);
    RETURN_INTERFACE(IMFOutputPolicy, riid, ppvObject);    

Exit:
    return hr;
}

// IUnknown::AddRef
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::AddRef() 
{
    ULONG uNewRefCount = InterlockedIncrement(&m_cRefCount);
    return uNewRefCount;
}

// IUnknown::Release
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::Release() 
{
    ULONG uNewRefCount = InterlockedDecrement(&m_cRefCount);
    if (0 == uNewRefCount) 
    {
        delete this;
    }
    return uNewRefCount;
}

// IMFOutputPolicy::GenerateRequiredSchemas
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::GenerateRequiredSchemas
( 
        /* [in] */ DWORD dwAttributes,
        /* [in] */ GUID guidOutputSubType,
        /* [in] */ GUID *rgGuidProtectionSchemasSupported,
        /* [in] */ DWORD cProtectionSchemasSupported,
        /* [annotation][out] */ 
        __out  IMFCollection **ppRequiredProtectionSchemas
)
{
    HRESULT hr = S_OK;
    bool bTrustedAudioDriversSupported = false;
    // if we've made it this far then the Output Trust Authority supports Trusted Audio Drivers
    // create a collection and put our output policy in it
    // then give that collection to the caller
    CComPtr<IMFCollection> pMFCollection;

    // sanity checks
    IF_TRUE_ACTION_JUMP((NULL == ppRequiredProtectionSchemas), hr = E_POINTER, Exit); 
    *ppRequiredProtectionSchemas = NULL;

    IF_TRUE_ACTION_JUMP((NULL == rgGuidProtectionSchemasSupported) && (0 != cProtectionSchemasSupported), 
                    hr = E_POINTER, Exit); 

    // log all the supported protection schemas
    for (DWORD i = 0; i < cProtectionSchemasSupported; i++) 
    {
        if (IsEqualIID(MFPROTECTION_TRUSTEDAUDIODRIVERS, rgGuidProtectionSchemasSupported[i])) 
        {
            bTrustedAudioDriversSupported = true;
        }
    }

    if (!bTrustedAudioDriversSupported) 
    {
        return HRESULT_FROM_WIN32(ERROR_RANGE_NOT_FOUND);
    }


    // create the collection
    hr = MFCreateCollection(&pMFCollection);
    if (FAILED(hr)) 
    {
        return hr;
    }

    // add our output policy to the collection
    hr = pMFCollection->AddElement(m_pOutputSchema);
    if (FAILED(hr)) 
    {
        return hr;
    }
Exit:
    // give the collection to the caller
    return pMFCollection.CopyTo(ppRequiredProtectionSchemas); // increments refcount
}// GenerateRequiredSchemas

HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::GetOriginatorID(__out  GUID *pguidOriginatorID) 
{
    if (NULL == pguidOriginatorID) 
    {
        return E_POINTER;
    }
    *pguidOriginatorID = m_guidOriginator;
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::GetMinimumGRLVersion(__out  DWORD *pdwMinimumGRLVersion) 
{
    if (NULL == pdwMinimumGRLVersion) 
    {
        return E_POINTER;
    }
    *pdwMinimumGRLVersion = 0;
    return S_OK;
}

//--------------------------------------------------------------------------
// Implementation for CTrustedAudioDriversOutputSchema
//--------------------------------------------------------------------------
// constructor
CTrustedAudioDriversOutputSchema::CTrustedAudioDriversOutputSchema
(    
    DWORD dwConfigData, 
    GUID guidOriginatorID
)
: m_cRefCount(1)
, m_dwConfigData(dwConfigData)
, m_guidOriginatorID(guidOriginatorID)
{}

// destructor
CTrustedAudioDriversOutputSchema::~CTrustedAudioDriversOutputSchema() {}

// IUnknown::QueryInterface
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::QueryInterface
(
        /* [in] */ REFIID riid,
        /* [out] */ LPVOID *ppvObject
) 
{
    HRESULT hr = E_NOINTERFACE;

    IF_TRUE_ACTION_JUMP((NULL == ppvObject), hr = E_POINTER, Exit);
    *ppvObject = NULL;

    RETURN_INTERFACE(IUnknown, riid, ppvObject);
    RETURN_INTERFACE(IMFAttributes, riid, ppvObject);
    RETURN_INTERFACE(IMFOutputSchema, riid, ppvObject);

Exit:
    return hr;
}

// IUnknown::AddRef
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::AddRef() 
{
    ULONG uNewRefCount = InterlockedIncrement(&m_cRefCount);
    return uNewRefCount;
}

// IUnknown::Release
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::Release() 
{
    ULONG uNewRefCount = InterlockedDecrement(&m_cRefCount);
    if (0 == uNewRefCount) 
    {
        delete this;
    }
    return uNewRefCount;
}
// IMFOutputSchema::GetConfigurationData
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::GetConfigurationData(__out DWORD *pdwVal) 
{
    if (NULL == pdwVal) { return E_POINTER; }
    *pdwVal = m_dwConfigData;
    return S_OK;
}

// IMFOutputSchema::GetOriginatorID
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::GetOriginatorID(__out GUID *pguidOriginatorID) 
{
    if (NULL == pguidOriginatorID) { return E_POINTER; }
    *pguidOriginatorID = m_guidOriginatorID;
    return S_OK;
}
// IMFOutputSchema::GetSchemaType
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::GetSchemaType(__out GUID *pguidSchemaType) 
{
    if (NULL == pguidSchemaType) { return E_POINTER; }
    *pguidSchemaType = MFPROTECTION_TRUSTEDAUDIODRIVERS;
    return S_OK;
}

//---------------------------------------------------------------------------------------------------
//
// Other subroutine declarations
//
//---------------------------------------------------------------------------------------------------
HRESULT CreateTrustedAudioDriversOutputPolicy(DWORD dwConfigData, IMFOutputPolicy **ppMFOutputPolicy) 
{
    if (NULL == ppMFOutputPolicy) 
    {
        return E_POINTER;
    }

    *ppMFOutputPolicy = NULL;

    HRESULT hr = S_OK;
    CTrustedAudioDriversOutputPolicy *pPolicy = new CTrustedAudioDriversOutputPolicy(dwConfigData, hr);
    if (NULL == pPolicy) 
    {
        return E_OUTOFMEMORY;
    }
    if (FAILED(hr)) 
    {
        delete pPolicy;
        return hr;
    }
    *ppMFOutputPolicy = static_cast<IMFOutputPolicy *>(pPolicy);
    return S_OK;
}// CreateTrustedAudioDriversOutputPolicy

HRESULT CreateTrustedAudioDriversOutputSchema
(
    DWORD dwConfigData,
    GUID guidOriginatorID,
    IMFOutputSchema **ppMFOutputSchema) 
{
    if (NULL == ppMFOutputSchema) 
    {
        return E_POINTER;
    }

    *ppMFOutputSchema = NULL;

    CTrustedAudioDriversOutputSchema *pSchema =
        new CTrustedAudioDriversOutputSchema(dwConfigData, guidOriginatorID);

    if (NULL == pSchema) 
    {
        return E_OUTOFMEMORY;
    }

    *ppMFOutputSchema = static_cast<IMFOutputSchema *>(pSchema);

    return S_OK;
}// CreateTrustedAudioDriversOutputSchema



HRESULT SetOTAPolicy(IMMDevice *_pMMDevice,
                     DWORD _dwConfigData,
                     IMFTrustedOutput **_ppMFTrustedOutput,
                     IMFOutputTrustAuthority **ppMFOutputTrustAuthority,
                     IMFOutputPolicy **_ppMFOutputPolicy)
{
    HRESULT hr = S_OK;

    DWORD dwCountOfOTAs = 0;
    bool bRet = false;

    hr = CreateTrustedAudioDriversOutputPolicy(_dwConfigData, _ppMFOutputPolicy);
    IF_FAILED_JUMP(hr, Exit);

    // activate IMFTrustedOutput
    hr = _pMMDevice->Activate(__uuidof(IMFTrustedOutput), CLSCTX_ALL, NULL,
                             (void**)_ppMFTrustedOutput);
    IF_FAILED_JUMP(hr, Exit);

    // get count of Output Trust Authorities on this trusted output
    hr = (*_ppMFTrustedOutput)->GetOutputTrustAuthorityCount(&dwCountOfOTAs);
    IF_FAILED_JUMP(hr, Exit);

    // sanity check - fail on endpoints with no output trust authorities
    IF_TRUE_ACTION_JUMP((0 == dwCountOfOTAs), hr = E_NOTFOUND, Exit);

    printf("dwCountOfOTAs = %d\n", dwCountOfOTAs);

     
    // loop over each output trust authority on the endpoint
    for (DWORD i = 0; i < dwCountOfOTAs; i++) 
    {
        // get the output trust authority
        hr = (*_ppMFTrustedOutput)->GetOutputTrustAuthorityByIndex(i, ppMFOutputTrustAuthority);
        IF_FAILED_JUMP(hr, Exit);


        // log the purpose of the output trust authority
        MFPOLICYMANAGER_ACTION action;
        hr = (*ppMFOutputTrustAuthority)->GetAction(&action);
        if (FAILED(hr)) 
        {
            return hr;
        }

        printf(" It's %s.", (PEACTION_PLAY==action) ? "PEACTION_PLAY" :
                            (PEACTION_COPY==action) ? "PEACTION_COPY" :
                            "Others");
 
        // only PEACTION_PLAY Output Trust Authorities are relevant
        if (PEACTION_PLAY != action) 
        {
            printf("Skipping as the OTA action is not PEACTION_PLAY");
            SAFE_RELEASE(*ppMFOutputTrustAuthority);
            continue;
        }

        BYTE *pbTicket = NULL;
        DWORD cbTicket = 0;
        // audio ota does not support ticket, leaving it NULL is ok.
        hr = (*ppMFOutputTrustAuthority)->SetPolicy(_ppMFOutputPolicy, 1, &pbTicket, &cbTicket);
        IF_FAILED_JUMP(hr, Exit);
        printf("SetPolicy succeeded.\n");

        bRet = true;
        break;

    }// for each output trust authority

Exit:
    if (bRet)
    {
        hr = S_OK;
    }
    if (FAILED(hr))
    {
        printf("failure code is 0x%0x\n", hr);
        SAFE_RELEASE(*ppMFOutputTrustAuthority);
        SAFE_RELEASE(*_ppMFTrustedOutput);
        if (*_ppMFOutputPolicy)
        {
            delete (*_ppMFOutputPolicy);
        }
    }

    return hr;
}


HRESULT ClearOTAPolicy(IMFTrustedOutput *_pMFTrustedOutput,
                       IMFOutputTrustAuthority *_pMFOutputTrustAuthority,
                       IMFOutputPolicy *_pMFOutputPolicy)
{
    SAFE_RELEASE(_pMFOutputTrustAuthority);
    SAFE_RELEASE(_pMFTrustedOutput);
    if (_pMFOutputPolicy)
    {
        delete _pMFOutputPolicy;
    }
    return S_OK;
}
```




```cpp
//OTADSoundSample.rc
#include "windows.h"

/////////////////////////////////////////////////////////////////////////////
// Version
#include <ntverp.h>

#define VER_FILETYPE                VFT_DLL
#define VER_FILESUBTYPE             VFT2_UNKNOWN
#define VER_FILEDESCRIPTION_STR     "Default Device Heuristic Dumper"
#define VER_INTERNALNAME_STR        "DefaultDeviceDump.exe"
#define VER_ORIGINALFILENAME_STR    "DefaultDeviceDump.exe"

#include "common.ver"
```




```cpp
Sources file:

TARGETNAME=OTADSoundSample
TARGETTYPE=PROGRAM
TARGET_DESTINATION=retail
UMTYPE=console
UMENTRY=wmain
UMBASE=0x1000000
#_NT_TARGET_VERSION=$(_NT_TARGET_VERSION_VISTA)
MSC_WARNING_LEVEL=$(MSC_WARNING_LEVEL) /WX
USE_ATL=1
ATL_VER=70
USE_NATIVE_EH=1
USE_MSVCRT=1
C_DEFINES=-DUNICODE -D_UNICODE
INCLUDES=$(INCLUDES);  

SOURCES=OTADSoundSample.cpp \
        OTADSoundSample.rc \
        outputpolicy.cpp\

TARGETLIBS=\
       $(SDK_LIB_PATH)\advapi32.lib         \
       $(SDK_LIB_PATH)\kernel32.lib         \
       $(SDK_LIB_PATH)\User32.lib           \
       $(SDK_LIB_PATH)\shlwapi.lib          \
       $(SDK_LIB_PATH)\ole32.lib            \
       $(SDK_LIB_PATH)\oleaut32.lib         \
       $(SDK_LIB_PATH)\rpcrt4.lib           \
       $(SDK_LIB_PATH)\strmiids.lib         \
       $(SDK_LIB_PATH)\uuid.lib             \
       $(SDK_LIB_PATH)\SetupAPI.lib         \
       $(SDK_LIB_PATH)\mfplat.lib \
```



## <a name="related-topics"></a><span data-ttu-id="e53b0-201">См. также</span><span class="sxs-lookup"><span data-stu-id="e53b0-201">Related topics</span></span>

[<span data-ttu-id="e53b0-202">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="e53b0-202">Programming Guide</span></span>](programming-guide.md)

[<span data-ttu-id="e53b0-203">Звуковые компоненты пользовательского режима</span><span class="sxs-lookup"><span data-stu-id="e53b0-203">User-Mode Audio Components</span></span>](user-mode-audio-components.md)
