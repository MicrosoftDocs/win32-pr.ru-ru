---
description: Сведения об API Ммдевице
ms.assetid: 3a8fd734-0761-4b5b-ba04-677c7c040988
title: Сведения об API Ммдевице
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82843bbecf004d0931575d73ec2459c3e72a3cf3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807733"
---
# <a name="about-mmdevice-api"></a><span data-ttu-id="4ec81-103">Сведения об API Ммдевице</span><span class="sxs-lookup"><span data-stu-id="4ec81-103">About MMDevice API</span></span>

<span data-ttu-id="4ec81-104">API-интерфейс устройства Windows мультимедиа (Ммдевице) позволяет клиентам аудио находить [устройства конечных точек аудио](audio-endpoint-devices.md), определять их возможности и создавать экземпляры драйверов для этих устройств.</span><span class="sxs-lookup"><span data-stu-id="4ec81-104">The Windows Multimedia Device (MMDevice) API enables audio clients to discover [audio endpoint devices](audio-endpoint-devices.md), determine their capabilities, and create driver instances for those devices.</span></span>

<span data-ttu-id="4ec81-105">Файл заголовка Ммдевицеапи. h определяет интерфейсы в API Ммдевице.</span><span class="sxs-lookup"><span data-stu-id="4ec81-105">Header file Mmdeviceapi.h defines the interfaces in the MMDevice API.</span></span>

<span data-ttu-id="4ec81-106">API Ммдевице состоит из нескольких интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="4ec81-106">The MMDevice API consists of several interfaces.</span></span> <span data-ttu-id="4ec81-107">Первый из них — интерфейс [**иммдевицеенумератор**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .</span><span class="sxs-lookup"><span data-stu-id="4ec81-107">The first of these is the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="4ec81-108">Для доступа к интерфейсам в API Ммдевице клиент получает ссылку на интерфейс **иммдевицеенумератор** объекта перечислителя устройства, вызвав функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , как показано в следующем фрагменте кода:</span><span class="sxs-lookup"><span data-stu-id="4ec81-108">To access the interfaces in the MMDevice API, a client obtains a reference to the **IMMDeviceEnumerator** interface of a device-enumerator object by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function, as shown in the following code fragment:</span></span>


```C++
  const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
  const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
  hr = CoCreateInstance(
         CLSID_MMDeviceEnumerator, NULL,
         CLSCTX_ALL, IID_IMMDeviceEnumerator,
         (void**)&pEnumerator);
```



<span data-ttu-id="4ec81-109">В предыдущем фрагменте кода CLSID \_ ммдевицеенумератор и IID \_ иммдевицеенумератор — это значения GUID, которые присоединяются как атрибуты к объекту **ммдевицеенумератор** Class и к интерфейсу [**иммдевицеенумератор**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .</span><span class="sxs-lookup"><span data-stu-id="4ec81-109">In the preceding code fragment, CLSID\_MMDeviceEnumerator and IID\_IMMDeviceEnumerator are the GUID values that are attached as attributes to the **MMDeviceEnumerator** class object and to the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="4ec81-110">Вызов [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) передает эти значения по ссылке.</span><span class="sxs-lookup"><span data-stu-id="4ec81-110">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) call passes these values by reference.</span></span> <span data-ttu-id="4ec81-111">Переменная `hr` имеет тип **HRESULT**, а переменная `pEnumerator` — указатель на интерфейс **иммдевицеенумератор** объекта перечислителя устройства.</span><span class="sxs-lookup"><span data-stu-id="4ec81-111">Variable `hr` is of type **HRESULT**, and variable `pEnumerator` is a pointer to the **IMMDeviceEnumerator** interface of a device-enumerator object.</span></span> <span data-ttu-id="4ec81-112">**Иммдевицеенумератор** предоставляет методы для перечисления устройств конечных точек аудио.</span><span class="sxs-lookup"><span data-stu-id="4ec81-112">**IMMDeviceEnumerator** provides methods for enumerating audio endpoint devices.</span></span> <span data-ttu-id="4ec81-113">Сведения об операторе **\_ \_ ууидоф** , функции **CoCreateInstance** и \_ константах клскткс *xxx* см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4ec81-113">For information about the **\_\_uuidof** operator, the **CoCreateInstance** function, and the CLSCTX\_*Xxx* constants, see the Windows SDK documentation.</span></span>

<span data-ttu-id="4ec81-114">С помощью интерфейса [**иммдевицеенумератор**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) клиент может получить ссылки на другие интерфейсы в API ммдевице.</span><span class="sxs-lookup"><span data-stu-id="4ec81-114">Through the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface, the client can obtain references to the other interfaces in the MMDevice API.</span></span> <span data-ttu-id="4ec81-115">API Ммдевице реализует следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="4ec81-115">The MMDevice API implements the following interfaces.</span></span>



| <span data-ttu-id="4ec81-116">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="4ec81-116">Interface</span></span>                                          | <span data-ttu-id="4ec81-117">Описание</span><span class="sxs-lookup"><span data-stu-id="4ec81-117">Description</span></span>                                     |
|----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="4ec81-118">**иммдевице**</span><span class="sxs-lookup"><span data-stu-id="4ec81-118">**IMMDevice**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                     | <span data-ttu-id="4ec81-119">Представляет звуковое устройство.</span><span class="sxs-lookup"><span data-stu-id="4ec81-119">Represents an audio device.</span></span>                     |
| [<span data-ttu-id="4ec81-120">**иммдевицеколлектион**</span><span class="sxs-lookup"><span data-stu-id="4ec81-120">**IMMDeviceCollection**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) | <span data-ttu-id="4ec81-121">Представляет коллекцию звуковых устройств.</span><span class="sxs-lookup"><span data-stu-id="4ec81-121">Represents a collection of audio devices.</span></span>       |
| [<span data-ttu-id="4ec81-122">**иммдевицеенумератор**</span><span class="sxs-lookup"><span data-stu-id="4ec81-122">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) | <span data-ttu-id="4ec81-123">Предоставляет методы для перечисления звуковых устройств.</span><span class="sxs-lookup"><span data-stu-id="4ec81-123">Provides methods for enumerating audio devices.</span></span> |
| [<span data-ttu-id="4ec81-124">**иммендпоинт**</span><span class="sxs-lookup"><span data-stu-id="4ec81-124">**IMMEndpoint**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                 | <span data-ttu-id="4ec81-125">Представляет устройство звуковой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="4ec81-125">Represents an audio endpoint device.</span></span>            |



 

<span data-ttu-id="4ec81-126">Кроме того, клиенты API Ммдевице, которым требуется уведомление об изменениях состояния на устройствах конечных точек аудио, должны реализовать следующий интерфейс.</span><span class="sxs-lookup"><span data-stu-id="4ec81-126">In addition, clients of the MMDevice API that require notification of status changes in audio endpoint devices should implement the following interface.</span></span>



| <span data-ttu-id="4ec81-127">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="4ec81-127">Interface</span></span>                                              | <span data-ttu-id="4ec81-128">Описание</span><span class="sxs-lookup"><span data-stu-id="4ec81-128">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ec81-129">**иммнотификатионклиент**</span><span class="sxs-lookup"><span data-stu-id="4ec81-129">**IMMNotificationClient**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | <span data-ttu-id="4ec81-130">Предоставляет уведомления при добавлении или удалении устройства конечной точки аудио, при изменении состояния или свойств устройства, а также при изменении роли по умолчанию, назначенной устройству.</span><span class="sxs-lookup"><span data-stu-id="4ec81-130">Provides notifications when an audio endpoint device is added or removed, when the state or properties of a device change, or when there is a change in the default role assigned to a device.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4ec81-131">См. также</span><span class="sxs-lookup"><span data-stu-id="4ec81-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ec81-132">Устройства конечных точек звука</span><span class="sxs-lookup"><span data-stu-id="4ec81-132">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> <dt>

[<span data-ttu-id="4ec81-133">**Справочник по программированию**</span><span class="sxs-lookup"><span data-stu-id="4ec81-133">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 
