---
description: Об API аудио Windows Core
ms.assetid: 657cf75f-3d72-4a5f-ae29-299e826b2b86
title: Об API аудио Windows Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30763d70bae4340436145a303763c0aad57171f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896462"
---
# <a name="about-the-windows-core-audio-apis"></a><span data-ttu-id="3e864-103">Об API аудио Windows Core</span><span class="sxs-lookup"><span data-stu-id="3e864-103">About the Windows Core Audio APIs</span></span>

<span data-ttu-id="3e864-104">Эта документация содержит сведения об основных API-интерфейсах аудиоподсистемы для семейства операционных систем Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3e864-104">This documentation provides information about Core Audio APIs for the Microsoft Windows family of operating systems.</span></span>

<span data-ttu-id="3e864-105">Основные API аудио появились в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3e864-105">The Core Audio APIs were introduced in Windows Vista.</span></span> <span data-ttu-id="3e864-106">Это новый набор звуковых компонентов пользовательского режима, предоставляющий клиентским приложениям улучшенные возможности работы с аудио.</span><span class="sxs-lookup"><span data-stu-id="3e864-106">This is a new set of user-mode audio components provides client applications with improved audio capabilities.</span></span> <span data-ttu-id="3e864-107">К этим возможностям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="3e864-107">These capabilities include the following:</span></span>

-   <span data-ttu-id="3e864-108">Низкая задержка, отказоустойчивая звуковая потоковая передача.</span><span class="sxs-lookup"><span data-stu-id="3e864-108">Low-latency, glitch-resilient audio streaming.</span></span>
-   <span data-ttu-id="3e864-109">Повышенная надежность (многие функции аудио переведены из режима ядра в пользовательский режим).</span><span class="sxs-lookup"><span data-stu-id="3e864-109">Improved reliability (many audio functions have moved from kernel mode to user mode).</span></span>
-   <span data-ttu-id="3e864-110">Улучшенная безопасность (обработка защищенного аудио-содержимого выполняется в безопасном и более низком уровне полномочий).</span><span class="sxs-lookup"><span data-stu-id="3e864-110">Improved security (processing of protected audio content takes place in a secure, lower-privilege process).</span></span>
-   <span data-ttu-id="3e864-111">Назначение определенных системных ролей (консоль, мультимедиа и связь) отдельным звуковым устройствам.</span><span class="sxs-lookup"><span data-stu-id="3e864-111">Assignment of particular system-wide roles (console, multimedia, and communications) to individual audio devices.</span></span>
-   <span data-ttu-id="3e864-112">Программная абстракция устройств конечных точек звука (например, динамики, наушники и микрофоны), которые пользователь напрямую управляет.</span><span class="sxs-lookup"><span data-stu-id="3e864-112">Software abstraction of the audio endpoint devices (for example, speakers, headphones, and microphones) that the user manipulates directly.</span></span>

<span data-ttu-id="3e864-113">В Windows 7 были улучшены основные API аудио.</span><span class="sxs-lookup"><span data-stu-id="3e864-113">The Core Audio APIs have been improved in Windows 7.</span></span> <span data-ttu-id="3e864-114">Дополнительные сведения об улучшениях и новых возможностях см. [в статье новые возможности основных API-интерфейсов аудиоподсистемы в Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).</span><span class="sxs-lookup"><span data-stu-id="3e864-114">For more information about the improvements and new features added, see [What's New for Core Audio APIs in Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).</span></span>

<span data-ttu-id="3e864-115">В этой документации описываются основные API аудио.</span><span class="sxs-lookup"><span data-stu-id="3e864-115">This documentation describes the Core Audio APIs.</span></span> <span data-ttu-id="3e864-116">Эти API служат основой для следующих интерфейсов API более высокого уровня:</span><span class="sxs-lookup"><span data-stu-id="3e864-116">These APIs serve as the foundation for the following higher-level APIs:</span></span>

-   <span data-ttu-id="3e864-117">Звука</span><span class="sxs-lookup"><span data-stu-id="3e864-117">DirectSound</span></span>
-   <span data-ttu-id="3e864-118">DirectMusic</span><span class="sxs-lookup"><span data-stu-id="3e864-118">DirectMusic</span></span>
-   <span data-ttu-id="3e864-119">Функции **вавекскскс** и **миксеркскскс** Windows мультимедиа</span><span class="sxs-lookup"><span data-stu-id="3e864-119">Windows multimedia **waveXxx** and **mixerXxx** functions</span></span>
-   <span data-ttu-id="3e864-120">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3e864-120">Media Foundation</span></span>

<span data-ttu-id="3e864-121">Эти API более высокого уровня используют основные API аудио для предоставления доступа к звуковым устройствам.</span><span class="sxs-lookup"><span data-stu-id="3e864-121">These higher-level APIs use the Core Audio APIs to share access to audio devices.</span></span> <span data-ttu-id="3e864-122">Media Foundation в Windows Vista, в то время как DirectSound, DirectMusic и функции **вавекскскс** и **миксеркскскс** поддерживаются в Windows 98, Windows Millennium Edition и в Windows 2000 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="3e864-122">Media Foundation is new with Windows Vista, whereas DirectSound, DirectMusic, and the **waveXxx** and **mixerXxx** functions are supported in Windows 98, Windows Millennium Edition, and in Windows 2000 and later.</span></span>

<span data-ttu-id="3e864-123">Большинство звуковых приложений взаимодействуют с интерфейсами API более высокого уровня вместо прямого взаимодействия с основными API-интерфейсами аудио.</span><span class="sxs-lookup"><span data-stu-id="3e864-123">Most audio applications communicate with the higher-level APIs instead of communicating directly with the Core Audio APIs.</span></span> <span data-ttu-id="3e864-124">Ниже приведены некоторые примеры приложений, использующих API более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="3e864-124">Some examples of applications that use higher-level APIs are:</span></span>

-   <span data-ttu-id="3e864-125">Проигрыватели мультимедиа</span><span class="sxs-lookup"><span data-stu-id="3e864-125">Media players</span></span>
-   <span data-ttu-id="3e864-126">DVD-проигрыватели</span><span class="sxs-lookup"><span data-stu-id="3e864-126">DVD players</span></span>
-   <span data-ttu-id="3e864-127">Игры</span><span class="sxs-lookup"><span data-stu-id="3e864-127">Games</span></span>
-   <span data-ttu-id="3e864-128">Бизнес-приложения, такие как Microsoft Office PowerPoint, воспроизводят звуковые файлы</span><span class="sxs-lookup"><span data-stu-id="3e864-128">Business applications, such as Microsoft Office PowerPoint, that play sound files</span></span>

<span data-ttu-id="3e864-129">Как правило, эти приложения взаимодействуют с интерфейсами API DirectSound или Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="3e864-129">Typically, these applications communicate with the DirectSound or Media Foundation APIs.</span></span>

<span data-ttu-id="3e864-130">Прямое взаимодействие с основными API-интерфейсами аудиоподсистемы может оказаться непригодным для многих звуковых приложений общего назначения.</span><span class="sxs-lookup"><span data-stu-id="3e864-130">Direct communication with the Core Audio APIs might not be suitable for many general-purpose audio applications.</span></span> <span data-ttu-id="3e864-131">Например, для основных интерфейсов аудио API требуется, чтобы звуковые потоки использовали собственные форматы данных звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="3e864-131">For example, the Core Audio APIs require audio streams to use an audio device's native data formats.</span></span> <span data-ttu-id="3e864-132">Однако разработчики программного обеспечения сторонних разработчиков, разрабатывающих следующие типы продуктов, могут потребовать специальных возможностей основных API-интерфейсов аудио:</span><span class="sxs-lookup"><span data-stu-id="3e864-132">However, third-party software developers who are developing the following types of products might require the special capabilities of the Core Audio APIs:</span></span>

-   <span data-ttu-id="3e864-133">Профессиональные звуковые приложения ("Pro Audio")</span><span class="sxs-lookup"><span data-stu-id="3e864-133">Professional audio ("pro audio") applications</span></span>
-   <span data-ttu-id="3e864-134">Приложения для обмена данными в реальном времени (RTC)</span><span class="sxs-lookup"><span data-stu-id="3e864-134">Real-time communication (RTC) applications</span></span>
-   <span data-ttu-id="3e864-135">Сторонние аудио API</span><span class="sxs-lookup"><span data-stu-id="3e864-135">Third-party audio APIs</span></span>

<span data-ttu-id="3e864-136">"Pro Audio" или "RTC" может требовать прямой доступ к функциям нижнего уровня основных API аудио, чтобы добиться минимальной задержки, получая эксклюзивный доступ к звуковому оборудованию.</span><span class="sxs-lookup"><span data-stu-id="3e864-136">A "pro audio" or RTC application might need direct access to the low-level features of the Core Audio APIs to achieve minimum latency by obtaining exclusive access to audio hardware.</span></span> <span data-ttu-id="3e864-137">Сторонний аудио API может потребовать прямого доступа к основным интерфейсам API аудио для реализации набора функций, которые могут быть не полностью поддерживаются любым ИНТЕРФЕЙСом высокоуровневой аудиоподсистемы, предоставляемым с Windows.</span><span class="sxs-lookup"><span data-stu-id="3e864-137">A third-party audio API might require direct access to the Core Audio APIs to implement a set of features that might not be entirely supported by any single high-level audio API that is supplied with Windows.</span></span>

<span data-ttu-id="3e864-138">Приложение, использующее Старый API аудио для воспроизведения или записи звука, может потребовать дополнительных возможностей, которые не поддерживаются устаревшим аудио API, но поддерживаются основными API-интерфейсами аудио.</span><span class="sxs-lookup"><span data-stu-id="3e864-138">An application that uses a legacy audio API to play or record audio might require additional capabilities that are not supported by the legacy audio API, but that are supported by the Core Audio APIs.</span></span> <span data-ttu-id="3e864-139">Во многих случаях приложение может получить доступ к этим возможностям напрямую через основные API, которые можно использовать в сочетании с устаревшим API аудио.</span><span class="sxs-lookup"><span data-stu-id="3e864-139">In many cases, the application can access these capabilities directly through the Core Audio APIs, which can be used in conjunction with the legacy audio API.</span></span>

<span data-ttu-id="3e864-140">Основные API-интерфейсы аудиоподсистемы:</span><span class="sxs-lookup"><span data-stu-id="3e864-140">The Core Audio APIs are:</span></span>

-   <span data-ttu-id="3e864-141">[API мультимедийного устройства (ммдевице)](mmdevice-api.md).</span><span class="sxs-lookup"><span data-stu-id="3e864-141">[Multimedia Device (MMDevice) API](mmdevice-api.md).</span></span> <span data-ttu-id="3e864-142">Клиенты используют этот API для перечисления устройств конечных точек звука в системе.</span><span class="sxs-lookup"><span data-stu-id="3e864-142">Clients use this API to enumerate the audio endpoint devices in the system.</span></span>
-   <span data-ttu-id="3e864-143">[API Windows Audio Session (васапи)](wasapi.md).</span><span class="sxs-lookup"><span data-stu-id="3e864-143">[Windows Audio Session API (WASAPI)](wasapi.md).</span></span> <span data-ttu-id="3e864-144">Клиенты используют этот API для создания и управления звуковыми потоками на устройствах конечных точек аудио.</span><span class="sxs-lookup"><span data-stu-id="3e864-144">Clients use this API to create and manage audio streams to and from audio endpoint devices.</span></span>
-   <span data-ttu-id="3e864-145">[API девицетопологи](devicetopology-api.md).</span><span class="sxs-lookup"><span data-stu-id="3e864-145">[DeviceTopology API](devicetopology-api.md).</span></span> <span data-ttu-id="3e864-146">Клиенты используют этот API для прямого доступа к функциям топологическом (например, элементам управления громкостью и мультиплексорам), которые находятся вдоль путей к данным внутри устройств в звуковых адаптерах.</span><span class="sxs-lookup"><span data-stu-id="3e864-146">Clients use this API to directly access the topological features (for example, volume controls and multiplexers) that lie along the data paths inside hardware devices in audio adapters.</span></span>
-   <span data-ttu-id="3e864-147">[API ендпоинтволуме](endpointvolume-api.md).</span><span class="sxs-lookup"><span data-stu-id="3e864-147">[EndpointVolume API](endpointvolume-api.md).</span></span> <span data-ttu-id="3e864-148">Клиенты используют этот API для прямого доступа к элементам управления громкости на устройствах конечных точек аудио.</span><span class="sxs-lookup"><span data-stu-id="3e864-148">Clients use this API to directly access the volume controls on audio endpoint devices.</span></span> <span data-ttu-id="3e864-149">Этот API в основном используется приложениями, которые управляют звуковыми потоками в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="3e864-149">This API is primarily used by applications that manage exclusive-mode audio streams.</span></span>

<span data-ttu-id="3e864-150">Эти API-интерфейсы поддерживают понятное для пользователя понятие устройства конечной точки, которое описано в статье [устройства конечных точек аудио](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="3e864-150">These APIs support the user-friendly notion of an endpoint device, which is described in [Audio Endpoint Devices](audio-endpoint-devices.md).</span></span>

<span data-ttu-id="3e864-151">Корпорация Майкрософт не планирует создавать основные интерфейсы API аудио, которые описаны здесь для использования в более ранних версиях Windows, включая Microsoft Windows Server 2003, Windows XP, Windows Millennium Edition, Windows 2000 и Windows 98.</span><span class="sxs-lookup"><span data-stu-id="3e864-151">Microsoft does not plan to make the Core Audio APIs that are described here available for use with earlier versions of Windows, including Microsoft Windows Server 2003, Windows XP, Windows Millennium Edition, Windows 2000, and Windows 98.</span></span>

<span data-ttu-id="3e864-152">Этот обзор содержит следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="3e864-152">This overview contains the following topics.</span></span>



| <span data-ttu-id="3e864-153">**Раздел**</span><span class="sxs-lookup"><span data-stu-id="3e864-153">**Topic**</span></span>                                                                                      | <span data-ttu-id="3e864-154">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3e864-154">**Description**</span></span>                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e864-155">Новые возможности для основных API-интерфейсов аудиоподсистемы в Windows 7</span><span class="sxs-lookup"><span data-stu-id="3e864-155">What's New for Core Audio APIs in Windows 7</span></span>](what-s-new-for-core-audio-apis-in-windows-7.md) | <span data-ttu-id="3e864-156">Содержит сводные сведения о новых возможностях и улучшениях основных API-интерфейсов аудио.</span><span class="sxs-lookup"><span data-stu-id="3e864-156">Summarizes the new features and the improvements to the Core Audio APIs</span></span>                   |
| [<span data-ttu-id="3e864-157">Файлы заголовков и системные компоненты</span><span class="sxs-lookup"><span data-stu-id="3e864-157">Header Files and System Components</span></span>](header-files-and-system-components.md)                   | <span data-ttu-id="3e864-158">Описание файлов заголовков и системных компонентов для основных API-интерфейсов аудио.</span><span class="sxs-lookup"><span data-stu-id="3e864-158">Describes the header files and system components for the Core Audio APIs.</span></span>                 |
| [<span data-ttu-id="3e864-159">Примеры пакетов SDK, использующих основные API аудио</span><span class="sxs-lookup"><span data-stu-id="3e864-159">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)       | <span data-ttu-id="3e864-160">Список примеров в Windows SDK, использующих основные API аудио.</span><span class="sxs-lookup"><span data-stu-id="3e864-160">Lists the samples in the Windows SDK that use the Core Audio APIs.</span></span>                        |




 

## <a name="related-topics"></a><span data-ttu-id="3e864-161">См. также</span><span class="sxs-lookup"><span data-stu-id="3e864-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e864-162">API-интерфейсы аудиоподсистемы Core</span><span class="sxs-lookup"><span data-stu-id="3e864-162">Core Audio APIs</span></span>](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



