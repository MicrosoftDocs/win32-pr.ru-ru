---
description: Файлы заголовков и системные компоненты
ms.assetid: de2776be-72e6-4391-8e6c-56694d683d57
title: Файлы заголовков и системные компоненты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a47125853b51a71f2f05dacf4534ce33cfedec
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424294"
---
# <a name="header-files-and-system-components"></a><span data-ttu-id="67db8-103">Файлы заголовков и системные компоненты</span><span class="sxs-lookup"><span data-stu-id="67db8-103">Header Files and System Components</span></span>

<span data-ttu-id="67db8-104">В следующей таблице перечислены файлы заголовков, содержащие определения интерфейсов для четырех основных компонентов аудио.</span><span class="sxs-lookup"><span data-stu-id="67db8-104">The following table lists the header files that contain the interface definitions for the four Core Audio components.</span></span>



| <span data-ttu-id="67db8-105">Основной звуковой компонент</span><span class="sxs-lookup"><span data-stu-id="67db8-105">Core Audio component</span></span>                         | <span data-ttu-id="67db8-106">Файл заголовка</span><span class="sxs-lookup"><span data-stu-id="67db8-106">Header file</span></span>                  |
|----------------------------------------------|------------------------------|
| [<span data-ttu-id="67db8-107">API Ммдевице</span><span class="sxs-lookup"><span data-stu-id="67db8-107">MMDevice API</span></span>](mmdevice-api.md)             | <span data-ttu-id="67db8-108">Ммдевицеапи. h</span><span class="sxs-lookup"><span data-stu-id="67db8-108">Mmdeviceapi.h</span></span>                |
| [<span data-ttu-id="67db8-109">васапи</span><span class="sxs-lookup"><span data-stu-id="67db8-109">WASAPI</span></span>](wasapi.md)                         | <span data-ttu-id="67db8-110">Аудиоклиент. h, Аудиополици. h</span><span class="sxs-lookup"><span data-stu-id="67db8-110">Audioclient.h, Audiopolicy.h</span></span> |
| [<span data-ttu-id="67db8-111">API Девицетопологи</span><span class="sxs-lookup"><span data-stu-id="67db8-111">DeviceTopology API</span></span>](devicetopology-api.md) | <span data-ttu-id="67db8-112">Девицетопологи. h</span><span class="sxs-lookup"><span data-stu-id="67db8-112">Devicetopology.h</span></span>             |
| [<span data-ttu-id="67db8-113">API Ендпоинтволуме</span><span class="sxs-lookup"><span data-stu-id="67db8-113">EndpointVolume API</span></span>](endpointvolume-api.md) | <span data-ttu-id="67db8-114">Ендпоинтволуме. h</span><span class="sxs-lookup"><span data-stu-id="67db8-114">Endpointvolume.h</span></span>             |



 

<span data-ttu-id="67db8-115">Другой файл заголовка Аудиосессионтипес. h определяет константы, используемые ВАСАПИ.</span><span class="sxs-lookup"><span data-stu-id="67db8-115">Another header file, Audiosessiontypes.h, defines constants that are used by WASAPI.</span></span> <span data-ttu-id="67db8-116">Эти файлы заголовков расположены в каталоге% Мссдк% \\ include, где% мссдк% — это корневой каталог установки Windows SDK на компьютере.</span><span class="sxs-lookup"><span data-stu-id="67db8-116">These header files are located in the directory %MSSdk%\\include, where %MSSdk% is the root directory of the Windows SDK installation on your computer.</span></span>

<span data-ttu-id="67db8-117">Каждый API в предыдущей таблице состоит из набора связанных COM-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="67db8-117">Each API in the preceding table consists of a set of related COM interfaces.</span></span> <span data-ttu-id="67db8-118">Поскольку некоторые аспекты потоковой передачи данных зависят от низкой задержки и точной синхронизации, реализации интерфейсов API Ммдевице, ВАСАПИ, Девицетопологи и Ендпоинтволуме не используют Microsoft .NET Framework или среду управляемого выполнения.</span><span class="sxs-lookup"><span data-stu-id="67db8-118">Because some aspects of audio streaming depend on low latency and precise synchronization, the implementations of the MMDevice, WASAPI, DeviceTopology, and EndpointVolume APIs do not use the Microsoft .NET Framework or managed-execution environment.</span></span>

<span data-ttu-id="67db8-119">Основные API аудио реализуются в пользовательских компонентах системы Audioses.dll и Mmdevapi.dll.</span><span class="sxs-lookup"><span data-stu-id="67db8-119">The Core Audio APIs are implemented in the user-mode system components Audioses.dll and Mmdevapi.dll.</span></span> <span data-ttu-id="67db8-120">Клиентские приложения не обращаются к точкам входа в этих библиотеках DLL напрямую.</span><span class="sxs-lookup"><span data-stu-id="67db8-120">Client applications do not access the entry points in these DLLs directly.</span></span> <span data-ttu-id="67db8-121">Вместо этого клиенты вызывают функцию **CoCreateInstance** или **кокреатеинстанцеекс** для получения интерфейса [**иммдевицеенумератор**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) объекта класса ммдевицеенумератор.</span><span class="sxs-lookup"><span data-stu-id="67db8-121">Instead, clients call the **CoCreateInstance** or **CoCreateInstanceEx** function to obtain the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface of the MMDeviceEnumerator class object.</span></span> <span data-ttu-id="67db8-122">Этот объект перечисляет [устройства конечных точек звука](audio-endpoint-devices.md) в системе.</span><span class="sxs-lookup"><span data-stu-id="67db8-122">This object enumerates the [audio endpoint devices](audio-endpoint-devices.md) in the system.</span></span> <span data-ttu-id="67db8-123">Интерфейс **иммдевицеенумератор** является частью API ммдевице.</span><span class="sxs-lookup"><span data-stu-id="67db8-123">The **IMMDeviceEnumerator** interface is part of the MMDevice API.</span></span> <span data-ttu-id="67db8-124">С помощью этого интерфейса клиенты могут напрямую или косвенно получить другие интерфейсы в API Ммдевице, включая интерфейс [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) .</span><span class="sxs-lookup"><span data-stu-id="67db8-124">From this interface, clients can directly or indirectly obtain the other interfaces in the MMDevice API, including the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface.</span></span> <span data-ttu-id="67db8-125">**Иммдевице** представляет конкретное устройство звуковой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="67db8-125">**IMMDevice** represents a particular audio endpoint device.</span></span> <span data-ttu-id="67db8-126">С помощью **иммдевице** клиенты могут напрямую или косвенно получить интерфейсы для конкретных устройств в ВАСАПИ, API ДЕВИЦЕТОПОЛОГИ и API ендпоинтволуме.</span><span class="sxs-lookup"><span data-stu-id="67db8-126">Through **IMMDevice**, clients can directly or indirectly obtain the device-specific interfaces in WASAPI, the DeviceTopology API, and the EndpointVolume API.</span></span> <span data-ttu-id="67db8-127">Дополнительные сведения о **CoCreateInstance** и **кокреатеинстанцеекс** см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="67db8-127">For more information about **CoCreateInstance** and **CoCreateInstanceEx**, see the Windows SDK documentation.</span></span> <span data-ttu-id="67db8-128">Дополнительные сведения о доступе к интерфейсам в основных API аудио см. в разделе [перечисление звуковых устройств](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="67db8-128">For more information about accessing the interfaces in the Core Audio APIs, see [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="67db8-129">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="67db8-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67db8-130">Об API аудио Windows Core</span><span class="sxs-lookup"><span data-stu-id="67db8-130">About the Windows Core Audio APIs</span></span>](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 



