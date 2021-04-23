---
title: Реализация пользовательского перечислителя конечной точки аудио
description: Начиная с Windows Server 2008 R2, можно реализовать настраиваемый перечислитель конечных точек удаленных аудио в составе поставщика удаленный рабочий стол протокола.
ms.assetid: 684bd62e-1e28-4330-a3c5-6bce684d652d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435ab2a572169f20a7f8f9db194449be5361e409
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "105672425"
---
# <a name="implementing-a-custom-audio-endpoint-enumerator"></a><span data-ttu-id="daa93-103">Реализация пользовательского перечислителя конечной точки аудио</span><span class="sxs-lookup"><span data-stu-id="daa93-103">Implementing a Custom Audio Endpoint Enumerator</span></span>

<span data-ttu-id="daa93-104">Начиная с Windows Server 2008 R2, можно реализовать настраиваемый перечислитель конечных точек удаленных аудио в составе поставщика удаленный рабочий стол протокола.</span><span class="sxs-lookup"><span data-stu-id="daa93-104">Beginning with Windows Server 2008 R2, you can implement a custom remote audio endpoint enumerator as part of a Remote Desktop protocol provider.</span></span> <span data-ttu-id="daa93-105">Поставщик протокола удаленный рабочий стол может использовать пользовательский перечислитель конечной точки аудио для получения коллекции звуковых конечных точек, имеющих конкретный набор возможностей.</span><span class="sxs-lookup"><span data-stu-id="daa93-105">A Remote Desktop protocol provider can use a custom audio endpoint enumerator to retrieve a collection of audio endpoints that have a specific set of capabilities.</span></span>

<span data-ttu-id="daa93-106">**Реализация настраиваемого перечислителя конечной точки удаленной аудиоподсистемы**</span><span class="sxs-lookup"><span data-stu-id="daa93-106">**To implement a custom remote audio endpoint enumerator**</span></span>

1.  <span data-ttu-id="daa93-107">Решение перечислителя пользовательской конечной точки должно реализовывать четыре основных типа объектов: объекты перечислителя устройств, объекты коллекции устройств, объекты устройств и объекты хранилища свойств.</span><span class="sxs-lookup"><span data-stu-id="daa93-107">Your custom endpoint enumerator solution should implement four main types of objects: device enumerator objects, device collection objects, device objects, and property store objects.</span></span>

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="daa93-108">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="daa93-108">Object type</span></span></th>
    <th><span data-ttu-id="daa93-109">Описание:</span><span class="sxs-lookup"><span data-stu-id="daa93-109">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="daa93-110">Объект перечислителя устройства</span><span class="sxs-lookup"><span data-stu-id="daa93-110">Device enumerator object</span></span><br/></td>
    <td><span data-ttu-id="daa93-111">Объект перечислителя устройства предоставляет функциональные возможности перечислителя конечных точек.</span><span class="sxs-lookup"><span data-stu-id="daa93-111">A device enumerator object provides the endpoint enumerator functionality.</span></span> <span data-ttu-id="daa93-112">Он предоставляет методы, возвращающие конечную точку по умолчанию и указанные коллекции конечных точек.</span><span class="sxs-lookup"><span data-stu-id="daa93-112">It exposes methods that return a default endpoint and specified collections of endpoints.</span></span> <span data-ttu-id="daa93-113">Например, в зависимости от указанных критериев перечислитель может возвращать конечные точки связи, конечные точки воспроизведения или конечные точки записи.</span><span class="sxs-lookup"><span data-stu-id="daa93-113">For example, depending on the criteria specified, the enumerator can return communication endpoints, playback endpoints, or capture endpoints.</span></span> <span data-ttu-id="daa93-114">Объект перечислителя устройства должен реализовывать интерфейс <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>иммдевицеенумератор</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="daa93-114">The device enumerator object must implement the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>IMMDeviceEnumerator</strong></a> interface.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="daa93-115">Объект коллекции устройств</span><span class="sxs-lookup"><span data-stu-id="daa93-115">Device collection object</span></span><br/></td>
    <td><span data-ttu-id="daa93-116">Объект коллекции устройств представляет коллекцию звуковых устройств.</span><span class="sxs-lookup"><span data-stu-id="daa93-116">A device collection object represents a collection of audio devices.</span></span> <span data-ttu-id="daa93-117">Он должен реализовывать интерфейс <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>иммдевицеколлектион</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="daa93-117">It must implement the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>IMMDeviceCollection</strong></a> interface.</span></span><br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="daa93-118">Объект устройства</span><span class="sxs-lookup"><span data-stu-id="daa93-118">Device object</span></span><br/></td>
    <td><span data-ttu-id="daa93-119">Объект устройства представляет конкретное звуковое устройство.</span><span class="sxs-lookup"><span data-stu-id="daa93-119">A device object represents a particular audio device.</span></span> <span data-ttu-id="daa93-120">Он предоставляет доступ к хранилищу свойств звукового устройства и предоставляет интерфейсы воспроизведения и записи звука, доступные на устройстве.</span><span class="sxs-lookup"><span data-stu-id="daa93-120">It provides access to the audio device's property store and exposes the audio playback and capture interfaces available on the device.</span></span> <span data-ttu-id="daa93-121">Объект устройства должен реализовывать интерфейсы <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>иммдевице</strong></a> и <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>иммендпоинт</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="daa93-121">The device object must implement the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>IMMDevice</strong></a> and <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>IMMEndpoint</strong></a> interfaces.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="daa93-122">Объект хранилища свойств</span><span class="sxs-lookup"><span data-stu-id="daa93-122">Property store object</span></span><br/></td>
    <td><span data-ttu-id="daa93-123">Объект хранилища свойств предоставляет свойства, связанные с звуковым устройством.</span><span class="sxs-lookup"><span data-stu-id="daa93-123">A property store object exposes the properties associated with an audio device.</span></span> <span data-ttu-id="daa93-124">Некоторые из этих свойств используются системой, но приложения могут также хранить произвольные свойства с конечной точкой аудио.</span><span class="sxs-lookup"><span data-stu-id="daa93-124">Some of these properties are used by the system, but applications can store arbitrary properties with the audio endpoint as well.</span></span><br/> <span data-ttu-id="daa93-125">Все звуковые устройства имеют следующие три свойства:</span><span class="sxs-lookup"><span data-stu-id="daa93-125">All audio devices have the following three properties:</span></span><br/>
    <ul>
    <li><span data-ttu-id="daa93-126"><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></span><span class="sxs-lookup"><span data-stu-id="daa93-126"><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></span></span></li>
    <li><span data-ttu-id="daa93-127"><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></span><span class="sxs-lookup"><span data-stu-id="daa93-127"><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></span></span></li>
    <li><span data-ttu-id="daa93-128"><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></span><span class="sxs-lookup"><span data-stu-id="daa93-128"><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></span></span></li>
    </ul>
<span data-ttu-id="daa93-129">Объект хранилища свойств должен реализовывать интерфейс <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">ипропертисторе</a> .</span><span class="sxs-lookup"><span data-stu-id="daa93-129">The property store object must implement the <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface.</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="daa93-130">Пользовательский перечислитель конечной точки должен быть реализован в библиотеке DLL, которая может быть загружена в звуковую систему и другие приложения.</span><span class="sxs-lookup"><span data-stu-id="daa93-130">The custom endpoint enumerator must be implemented in a DLL that can be loaded into the audio system and other applications.</span></span> <span data-ttu-id="daa93-131">Библиотека DLL должна быть подписана так, чтобы защищенные процессы могли загрузить ее.</span><span class="sxs-lookup"><span data-stu-id="daa93-131">The DLL must be signed so that secure processes can load it.</span></span> <span data-ttu-id="daa93-132">Библиотека DLL должна реализовывать и экспортировать функцию [**жеттсаудиоендпоинтенумераторфорсессион**](gettsaudioendpointenumeratorforsession.md) , которая выступает в качестве точки входа в пользовательский перечислитель конечной точки.</span><span class="sxs-lookup"><span data-stu-id="daa93-132">The DLL must implement and export the [**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md) function, which acts as an entry point to the custom endpoint enumerator.</span></span>

<span data-ttu-id="daa93-133">Служба службы удаленных рабочих столов вызывает метод [**куерипроперти**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty) и задает для параметра *QueryType* значение **ВТС \_ Query \_ аудиоенум \_ DLL** для получения имени объекта перечислителя.</span><span class="sxs-lookup"><span data-stu-id="daa93-133">The Remote Desktop Services service calls the [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty) method and sets the *QueryType* parameter to **WTS\_QUERY\_AUDIOENUM\_DLL** to retrieve the name of the enumerator object.</span></span>

<span data-ttu-id="daa93-134">Пользовательские объекты перечислителя используют COM-подобные интерфейсы и механизм подсчета ссылок, подобный COM, но они не являются истинными COM-объектами.</span><span class="sxs-lookup"><span data-stu-id="daa93-134">Custom enumerator objects use COM-like interfaces and a COM-like reference counting mechanism, but they are not true COM objects.</span></span> <span data-ttu-id="daa93-135">Пользовательский перечислитель конечной точки должен иметь возможность работать с устаревшими звуковыми интерфейсами, используемыми приложениями, которые не поддерживают COM.</span><span class="sxs-lookup"><span data-stu-id="daa93-135">The custom endpoint enumerator must have the ability to work with legacy audio interfaces used by applications that do not support COM.</span></span> <span data-ttu-id="daa93-136">По этой причине пользовательский перечислитель конечной точки не должен полагаться на механизм управления жизненным циклом COM.</span><span class="sxs-lookup"><span data-stu-id="daa93-136">For this reason, the custom endpoint enumerator must not rely on COM's life cycle management mechanism.</span></span> <span data-ttu-id="daa93-137">Потребители в перечислителе конечных точек аудио, такие как MMDevAPI.dll, загружают библиотеку DLL перечислителя пользовательской конечной точки, если это требуется для пользовательских приложений, и не выгружают перечислитель, когда перечислитель содержит ссылку на объект перечислителя устройства, объект коллекции устройств, объект устройства или объект хранилища свойств.</span><span class="sxs-lookup"><span data-stu-id="daa93-137">Consumers of your audio endpoint enumerator, such as MMDevAPI.dll, load the custom endpoint enumerator DLL when required by user applications, and they will not unload the enumerator while the enumerator holds a reference to a device enumerator object, device collection object, device object, or property store object.</span></span> <span data-ttu-id="daa93-138">Однако невозможно для этих потребителей отслеживание ссылок на другие типы объектов, принадлежащих перечислителю пользовательской конечной точки.</span><span class="sxs-lookup"><span data-stu-id="daa93-138">It is not possible, however, for these consumers to track references to other types of objects owned by the custom endpoint enumerator.</span></span> <span data-ttu-id="daa93-139">Соответственно, мы рекомендуем, чтобы пользовательский перечислитель конечной точки не мог создавать объекты, которые могут разжить эти четыре типа объектов.</span><span class="sxs-lookup"><span data-stu-id="daa93-139">Accordingly, we recommend that your custom endpoint enumerator not create any objects that could outlive these four types of objects.</span></span>

## <a name="to-implement-a-custom-audio-endpoint"></a><span data-ttu-id="daa93-140">Реализация пользовательской конечной точки звука</span><span class="sxs-lookup"><span data-stu-id="daa93-140">To implement a custom audio endpoint</span></span>

<span data-ttu-id="daa93-141">Для реализации пользовательского перечислителя аудио-устройств необходимо реализовать пользовательскую конечную точку звука.</span><span class="sxs-lookup"><span data-stu-id="daa93-141">To implement a custom audio device enumerator, you must implement a custom audio endpoint.</span></span> <span data-ttu-id="daa93-142">Способ связи пользовательских звуковых устройств заключается в использовании следующих двух операторов:</span><span class="sxs-lookup"><span data-stu-id="daa93-142">The way that your custom audio devices are linked is by using the following two statements:</span></span>

-   `IMMDevice::Activate(IAudioOutputEndpointRT)`
-   `IMMDevice::Activate(IAudioInputEndpointRT)`

<span data-ttu-id="daa93-143">Мы не планируем реализовать полный список интерфейсов [**иммдевице:: Activate**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) в пользовательском перечислителе звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="daa93-143">We do not expect you to implement the full list of [**IMMDevice::Activate**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) interfaces in your custom audio device enumerator.</span></span> <span data-ttu-id="daa93-144">Вместо этого следует реализовать [**иаудиуутпутендпоинтрт**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) и [**иаудиоинпутендпоинтрт**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span><span class="sxs-lookup"><span data-stu-id="daa93-144">Instead, you should implement [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) and [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span></span> <span data-ttu-id="daa93-145">При необходимости можно реализовать еще несколько возможностей, например [**иаудиоендпоинтволуме**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume).</span><span class="sxs-lookup"><span data-stu-id="daa93-145">You can optionally implement a few more, such as [**IAudioEndpointVolume**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume).</span></span> <span data-ttu-id="daa93-146">Для любого интерфейса, который не реализуется, следует вернуть **\_ интерфейс E** (необходимо использовать этот код ошибки).</span><span class="sxs-lookup"><span data-stu-id="daa93-146">For any interface you do not implement, you should return **E\_NOINTERFACE** (you must use this specific failure code).</span></span> <span data-ttu-id="daa93-147">Затем Windows перейдет к реализации на бирже интерфейса (например, [**IAudioClient2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)).</span><span class="sxs-lookup"><span data-stu-id="daa93-147">Windows will then fall back to a stock implementation of the interface (for example, [**IAudioClient2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)).</span></span>

<span data-ttu-id="daa93-148">Дополнительную справочную документацию по реализации и регистрации конечных точек аудио см. в разделе [**иаудиоинпутендпоинтрт**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span><span class="sxs-lookup"><span data-stu-id="daa93-148">For additional reference documentation about how to implement and register audio endpoints, see [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span></span> <span data-ttu-id="daa93-149">Схему, в которой показано, как работает ВАСАПИ, см. в разделе [аудио-компоненты пользовательского режима](/windows/desktop/CoreAudio/user-mode-audio-components).</span><span class="sxs-lookup"><span data-stu-id="daa93-149">For a diagram that shows how WASAPI works, see [User-Mode Audio Components](/windows/desktop/CoreAudio/user-mode-audio-components).</span></span> <span data-ttu-id="daa93-150">Обратите внимание, что все аудио в пользовательском режиме являются новыми, начиная с Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="daa93-150">Note that all of user-mode audio is new beginning with Windows Server 2008.</span></span>

## <a name="related-topics"></a><span data-ttu-id="daa93-151">См. также</span><span class="sxs-lookup"><span data-stu-id="daa93-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="daa93-152">Создание поставщика протокол удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="daa93-152">Creating a Remote Desktop Protocol Provider</span></span>](creating-a-custom-remote-protocol.md)
</dt> <dt>

[<span data-ttu-id="daa93-153">**жеттсаудиоендпоинтенумераторфорсессион**</span><span class="sxs-lookup"><span data-stu-id="daa93-153">**GetTSAudioEndpointEnumeratorForSession**</span></span>](gettsaudioendpointenumeratorforsession.md)
</dt> <dt>

[<span data-ttu-id="daa93-154">**иммдевице**</span><span class="sxs-lookup"><span data-stu-id="daa93-154">**IMMDevice**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[<span data-ttu-id="daa93-155">**иммдевицеколлектион**</span><span class="sxs-lookup"><span data-stu-id="daa93-155">**IMMDeviceCollection**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
</dt> <dt>

[<span data-ttu-id="daa93-156">**иммдевицеенумератор**</span><span class="sxs-lookup"><span data-stu-id="daa93-156">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[<span data-ttu-id="daa93-157">**иммендпоинт**</span><span class="sxs-lookup"><span data-stu-id="daa93-157">**IMMEndpoint**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint)
</dt> <dt>

[<span data-ttu-id="daa93-158">ипропертисторе</span><span class="sxs-lookup"><span data-stu-id="daa93-158">IPropertyStore</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> </dl>