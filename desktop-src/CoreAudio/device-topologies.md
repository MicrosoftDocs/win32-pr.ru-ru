---
description: Топологии устройств
ms.assetid: 5ac421e5-74a4-40e8-af6f-a99a05ebc3e0
title: Топологии устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e0af267bb4a0fa924ee23d36a2a615ac5ae7fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539344"
---
# <a name="device-topologies"></a><span data-ttu-id="711ed-103">Топологии устройств</span><span class="sxs-lookup"><span data-stu-id="711ed-103">Device Topologies</span></span>

<span data-ttu-id="711ed-104">[API девицетопологи](devicetopology-api.md) предоставляет клиентам возможности управления различными внутренними функциями звуковых адаптеров, которые не могут получить доступ через [API ммдевице](mmdevice-api.md), [васапи](wasapi.md)или [API ендпоинтволуме](endpointvolume-api.md).</span><span class="sxs-lookup"><span data-stu-id="711ed-104">The [DeviceTopology API](devicetopology-api.md) gives clients control over a variety of internal functions of audio adapters that they cannot access through the [MMDevice API](mmdevice-api.md), [WASAPI](wasapi.md), or the [EndpointVolume API](endpointvolume-api.md).</span></span>

<span data-ttu-id="711ed-105">Как упоминалось ранее, [API ммдевице](mmdevice-api.md), [Васапи](wasapi.md)и [API ендпоинтволуме](endpointvolume-api.md) представляют микрофоны, динамики, наушники, а также другие входные и выходные устройства в качестве [звуковых конечных](audio-endpoint-devices.md)устройств.</span><span class="sxs-lookup"><span data-stu-id="711ed-105">As explained previously, the [MMDevice API](mmdevice-api.md), [WASAPI](wasapi.md), and the [EndpointVolume API](endpointvolume-api.md) present microphones, speakers, headphones, and other audio input and output devices to clients as [audio endpoint devices](audio-endpoint-devices.md).</span></span> <span data-ttu-id="711ed-106">Модель устройства конечной точки предоставляет клиентам удобный доступ к тому и звуковые элементы управления в звуковых устройствах.</span><span class="sxs-lookup"><span data-stu-id="711ed-106">The endpoint device model provides clients with convenient access to volume and mute controls in audio devices.</span></span> <span data-ttu-id="711ed-107">Клиенты, которым требуются только эти простые элементы управления, могут избежать обхода внутренних топологий аппаратных устройств в звуковых адаптерах.</span><span class="sxs-lookup"><span data-stu-id="711ed-107">Clients that require only these simple controls can avoid traversing the internal topologies of hardware devices in audio adapters.</span></span>

<span data-ttu-id="711ed-108">В Windows Vista механизм аудио автоматически настраивает топологии звуковых устройств для использования в приложениях аудио.</span><span class="sxs-lookup"><span data-stu-id="711ed-108">In Windows Vista, the audio engine automatically configures the topologies of audio devices for use by audio applications.</span></span> <span data-ttu-id="711ed-109">Таким же приложениям редко приходится использовать API Девицетопологи для этой цели.</span><span class="sxs-lookup"><span data-stu-id="711ed-109">Thus, applications rarely, if ever, need to use the DeviceTopology API for this purpose.</span></span> <span data-ttu-id="711ed-110">Например, предположим, что звуковой адаптер содержит мультиплексор ввода, который может записывать поток из входного или микрофона, но не может одновременно записывать потоки из обеих конечных устройств.</span><span class="sxs-lookup"><span data-stu-id="711ed-110">For example, assume that an audio adapter contains an input multiplexer that can capture a stream from either a line input or a microphone, but that cannot capture streams from both endpoint devices at the same time.</span></span> <span data-ttu-id="711ed-111">Предположим, что пользователь включил приложения с монопольным режимом для прерывания использования устройства "Звуковая конечная точка" приложениями общего режима, как описано в разделе [потоки с монопольным режимом](exclusive-mode-streams.md).</span><span class="sxs-lookup"><span data-stu-id="711ed-111">Assume that the user has enabled exclusive-mode applications to preempt the use of an audio endpoint device by shared-mode applications, as described in [Exclusive-Mode Streams](exclusive-mode-streams.md).</span></span> <span data-ttu-id="711ed-112">Если приложение общего режима записывает поток из входных данных во время записи потока из микрофона приложением с монопольным режимом, обработчик звука автоматически переключает мультиплексор из входных данных в микрофон.</span><span class="sxs-lookup"><span data-stu-id="711ed-112">If a shared-mode application is recording a stream from the line input at the time that an exclusive-mode application begins recording a stream from the microphone, the audio engine automatically switches the multiplexer from the line input to the microphone.</span></span> <span data-ttu-id="711ed-113">В более ранних версиях Windows, включая Windows XP, приложение с монопольным режимом в этом примере использовало функции **миксеркскскс** в API мультимедиа Windows для обхода топологий устройств адаптеров, обнаружения мультиплексора и настройки мультиплексора для выбора входных данных с микрофона.</span><span class="sxs-lookup"><span data-stu-id="711ed-113">In contrast, in earlier versions of Windows, including Windows XP, the exclusive-mode application in this example would use the **mixerXxx** functions in the Windows multimedia API to traverse the topologies of the adapter devices, discover the multiplexer, and configure the multiplexer to select the microphone input.</span></span> <span data-ttu-id="711ed-114">В Windows Vista эти действия больше не требуются.</span><span class="sxs-lookup"><span data-stu-id="711ed-114">In Windows Vista, these steps are no longer required.</span></span>

<span data-ttu-id="711ed-115">Однако некоторым клиентам может потребоваться явный контроль над типами элементов управления звуком, которые недоступны через API Ммдевице, ВАСАПИ или API Ендпоинтволуме.</span><span class="sxs-lookup"><span data-stu-id="711ed-115">However, some clients might require explicit control over types of audio hardware controls that cannot be accessed through the MMDevice API, WASAPI, or the EndpointVolume API.</span></span> <span data-ttu-id="711ed-116">Для этих клиентов API Девицетопологи предоставляет возможность обхода топологий устройств адаптеров для обнаружения и управления звуковыми элементами на устройствах.</span><span class="sxs-lookup"><span data-stu-id="711ed-116">For these clients, the DeviceTopology API provides the ability to traverse the topologies of adapter devices to discover and manage the audio controls in the devices.</span></span> <span data-ttu-id="711ed-117">Приложения, использующие API Девицетопологи, должны быть разработаны с осторожностью, чтобы избежать помех в работе политики Windows Audio и нарушения внутренних конфигураций звуковых устройств, используемых совместно с другими приложениями.</span><span class="sxs-lookup"><span data-stu-id="711ed-117">Applications that use the DeviceTopology API must be designed with care to avoid interfering with Windows audio policy and disturbing the internal configurations of audio devices that are shared with other applications.</span></span> <span data-ttu-id="711ed-118">Дополнительные сведения о политике Windows Audio см. в разделе [звуковые компоненты пользовательского режима](user-mode-audio-components.md).</span><span class="sxs-lookup"><span data-stu-id="711ed-118">For more information about Windows audio policy, see [User-Mode Audio Components](user-mode-audio-components.md).</span></span>

<span data-ttu-id="711ed-119">API Девицетопологи предоставляет интерфейсы для обнаружения следующих типов элементов управления звуком в топологии устройства и управления ими:</span><span class="sxs-lookup"><span data-stu-id="711ed-119">The DeviceTopology API provides interfaces for discovering and managing the following types of audio controls in a device topology:</span></span>

-   <span data-ttu-id="711ed-120">Автоматическое усиление контроля</span><span class="sxs-lookup"><span data-stu-id="711ed-120">Automatic gain control</span></span>
-   <span data-ttu-id="711ed-121">Элемент управления басов</span><span class="sxs-lookup"><span data-stu-id="711ed-121">Bass control</span></span>
-   <span data-ttu-id="711ed-122">Селектор ввода (мультиплексор)</span><span class="sxs-lookup"><span data-stu-id="711ed-122">Input selector (multiplexer)</span></span>
-   <span data-ttu-id="711ed-123">Элемент управления громкостью</span><span class="sxs-lookup"><span data-stu-id="711ed-123">Loudness control</span></span>
-   <span data-ttu-id="711ed-124">Элемент управления "средний"</span><span class="sxs-lookup"><span data-stu-id="711ed-124">Midrange control</span></span>
-   <span data-ttu-id="711ed-125">Отключить контроль</span><span class="sxs-lookup"><span data-stu-id="711ed-125">Mute control</span></span>
-   <span data-ttu-id="711ed-126">Селектор выходных данных (демультиплексор)</span><span class="sxs-lookup"><span data-stu-id="711ed-126">Output selector (demultiplexer)</span></span>
-   <span data-ttu-id="711ed-127">Счетчик пиковой нагрузки</span><span class="sxs-lookup"><span data-stu-id="711ed-127">Peak meter</span></span>
-   <span data-ttu-id="711ed-128">Элемент управления "ВЧ"</span><span class="sxs-lookup"><span data-stu-id="711ed-128">Treble control</span></span>
-   <span data-ttu-id="711ed-129">Элемент управления громкостью</span><span class="sxs-lookup"><span data-stu-id="711ed-129">Volume control</span></span>

<span data-ttu-id="711ed-130">Кроме того, API Девицетопологи позволяет клиентам запрашивать устройства адаптеров для получения сведений о поддерживаемых ими форматах потока.</span><span class="sxs-lookup"><span data-stu-id="711ed-130">In addition, the DeviceTopology API enables clients to query adapter devices for information about the stream formats that they support.</span></span> <span data-ttu-id="711ed-131">В файле заголовка Девицетопологи. h определяются интерфейсы в API Девицетопологи.</span><span class="sxs-lookup"><span data-stu-id="711ed-131">The header file Devicetopology.h defines the interfaces in the DeviceTopology API.</span></span>

<span data-ttu-id="711ed-132">На следующей схеме показан пример нескольких топологий подключенных устройств для части адаптера PCI, которая захватывает звук с микрофона, линейного входа и ЛАЗЕРного проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="711ed-132">The following diagram shows an example of several connected device topologies for the portion of a PCI adapter that captures audio from a microphone, line input, and CD player.</span></span>

![Пример четырех топологий подключенных устройств](images/fig2.jpg)

<span data-ttu-id="711ed-134">На предыдущей схеме показаны пути к данным, ведущие от аналоговых входов в системную шину.</span><span class="sxs-lookup"><span data-stu-id="711ed-134">The preceding diagram shows the data paths that lead from the analog inputs to the system bus.</span></span> <span data-ttu-id="711ed-135">Каждое из следующих устройств представлено в виде объекта топологии устройства с интерфейсом [**идевицетопологи**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) :</span><span class="sxs-lookup"><span data-stu-id="711ed-135">Each of the following devices is represented as a device-topology object with an [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) interface:</span></span>

-   <span data-ttu-id="711ed-136">Устройство записи звука</span><span class="sxs-lookup"><span data-stu-id="711ed-136">Wave capture device</span></span>
-   <span data-ttu-id="711ed-137">Устройство для ввода мультиплексора</span><span class="sxs-lookup"><span data-stu-id="711ed-137">Input multiplexer device</span></span>
-   <span data-ttu-id="711ed-138">Устройство A конечной точки</span><span class="sxs-lookup"><span data-stu-id="711ed-138">Endpoint device A</span></span>
-   <span data-ttu-id="711ed-139">Устройство в конечной точке B</span><span class="sxs-lookup"><span data-stu-id="711ed-139">Endpoint device B</span></span>

<span data-ttu-id="711ed-140">Обратите внимание, что схема топологии объединяет устройства адаптеров (устройства для записи звука и мультиплексора ввода) с устройствами конечных точек.</span><span class="sxs-lookup"><span data-stu-id="711ed-140">Note that the topology diagram combines adapter devices (the wave capture and input multiplexer devices) with endpoint devices.</span></span> <span data-ttu-id="711ed-141">Благодаря подключениям между устройствами звуковые данные передаются с одного устройства на другое.</span><span class="sxs-lookup"><span data-stu-id="711ed-141">Through the connections between devices, audio data passes from one device to the next.</span></span> <span data-ttu-id="711ed-142">На каждой стороне соединения находится соединитель (с меткой Con на схеме), с помощью которого данные перемещаются или попадают в устройство.</span><span class="sxs-lookup"><span data-stu-id="711ed-142">On each side of a connection is a connector (labeled Con in the diagram) through which data enters or leaves a device.</span></span>

<span data-ttu-id="711ed-143">На левой границе диаграммы сигналы от входных и микрофонных разъемов поступают в конечные устройства.</span><span class="sxs-lookup"><span data-stu-id="711ed-143">On the left edge of the diagram, signals from the line-input and microphone jacks enter the endpoint devices.</span></span>

<span data-ttu-id="711ed-144">Устройство для записи волнового сигнала и устройство мультиплексора ввода являются функциями потоковой обработки, которые в терминологии API Девицетопологи называются подразделениями.</span><span class="sxs-lookup"><span data-stu-id="711ed-144">Inside the wave capture device and input multiplexer device are stream-processing functions, which, in the terminology of the DeviceTopology API, are called subunits.</span></span> <span data-ttu-id="711ed-145">На предыдущей схеме отображаются следующие типы подразделений.</span><span class="sxs-lookup"><span data-stu-id="711ed-145">The following types of subunits appear in the preceding diagram:</span></span>

-   <span data-ttu-id="711ed-146">Элемент управления "Громкость" (с меткой "Громкость")</span><span class="sxs-lookup"><span data-stu-id="711ed-146">Volume control (labeled Vol)</span></span>
-   <span data-ttu-id="711ed-147">Отключить контроль (с меткой)</span><span class="sxs-lookup"><span data-stu-id="711ed-147">Mute control (labeled Mute)</span></span>
-   <span data-ttu-id="711ed-148">Мультиплексор (или селектор ввода; помеченный МУЛЬТИПЛЕКСОР)</span><span class="sxs-lookup"><span data-stu-id="711ed-148">Multiplexer (or input selector; labeled MUX)</span></span>
-   <span data-ttu-id="711ed-149">Аналоговый для цифрового преобразователя (под названием ADC)</span><span class="sxs-lookup"><span data-stu-id="711ed-149">Analog-to-digital converter (labeled ADC)</span></span>

<span data-ttu-id="711ed-150">Параметры в подразделениях тома, звука и мультиплексора могут управляться клиентами, а API Девицетопологи предоставляет клиентам управляющие интерфейсы для управления ими.</span><span class="sxs-lookup"><span data-stu-id="711ed-150">The settings in the volume, mute, and multiplexer subunits can be controlled by clients, and the DeviceTopology API provides control interfaces to clients for controlling them.</span></span> <span data-ttu-id="711ed-151">В этом примере подмодуль ADC не имеет параметров управления.</span><span class="sxs-lookup"><span data-stu-id="711ed-151">In this example, the ADC subunit has no control settings.</span></span> <span data-ttu-id="711ed-152">Таким же Девицетопологи API не предоставляет интерфейс управления для ADC.</span><span class="sxs-lookup"><span data-stu-id="711ed-152">Thus, the DeviceTopology API provides no control interface for the ADC.</span></span>

<span data-ttu-id="711ed-153">В терминологии API Девицетопологи соединители и подединицы принадлежат к одной общей категории — частям.</span><span class="sxs-lookup"><span data-stu-id="711ed-153">In the terminology of the DeviceTopology API, connectors and subunits belong to the same general category—parts.</span></span> <span data-ttu-id="711ed-154">Все части, независимо от того, являются ли они соединителями или подразделениями, предоставляют общий набор функций.</span><span class="sxs-lookup"><span data-stu-id="711ed-154">All parts, regardless of whether they are connectors or subunits, provide a common set of functions.</span></span> <span data-ttu-id="711ed-155">API Девицетопологи реализует интерфейс [**ипарт**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) для представления универсальных функций, общих для соединителей и подразделений.</span><span class="sxs-lookup"><span data-stu-id="711ed-155">The DeviceTopology API implements an [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) interface to represent the generic functions that are common to connectors and subunits.</span></span> <span data-ttu-id="711ed-156">API реализует интерфейсы [**иконнектор**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) и [**исубунит**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) для представления конкретных аспектов соединителей и подразделений.</span><span class="sxs-lookup"><span data-stu-id="711ed-156">The API implements the [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) and [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) interfaces to represent the specific aspects of connectors and subunits.</span></span>

<span data-ttu-id="711ed-157">API Девицетопологи создает топологии устройства записи звука и устройства мультиплексирования ввода из фильтров потоковой передачи (KS), которые драйвер аудиоподсистемы предоставляет операционной системе для представления этих устройств.</span><span class="sxs-lookup"><span data-stu-id="711ed-157">The DeviceTopology API constructs the topologies of the wave capture device and input multiplexer device from the kernel-streaming (KS) filters that the audio driver exposes to the operating system to represent these devices.</span></span> <span data-ttu-id="711ed-158">(Драйвер адаптера аудиоподсистемы реализует интерфейсы **иминипортвавекскскс** и **иминипорттопологи** , которые представляют зависимые от оборудования части этих фильтров; дополнительные сведения об этих интерфейсах и о фильтрах KS см. в документации по Windows DDK.)</span><span class="sxs-lookup"><span data-stu-id="711ed-158">(The audio adapter driver implements **IMiniportWaveXxx** and **IMiniportTopology** interfaces to represent the hardware-dependent portions of these filters; for more information about these interfaces and about KS filters, see the Windows DDK documentation.)</span></span>

<span data-ttu-id="711ed-159">API Девицетопологи конструирует тривиальные топологии для представления конечных устройств A и B на предыдущей схеме.</span><span class="sxs-lookup"><span data-stu-id="711ed-159">The DeviceTopology API constructs trivial topologies to represent endpoint devices A and B in the preceding diagram.</span></span> <span data-ttu-id="711ed-160">Топология устройства конечной точки состоит из одного соединителя.</span><span class="sxs-lookup"><span data-stu-id="711ed-160">The device topology of an endpoint device consists of a single connector.</span></span> <span data-ttu-id="711ed-161">Эта топология является просто заполнителем для устройства конечной точки и не содержит подразделений для обработки звуковых данных.</span><span class="sxs-lookup"><span data-stu-id="711ed-161">This topology is merely a placeholder for the endpoint device and contains no subunits for processing audio data.</span></span> <span data-ttu-id="711ed-162">На самом деле адаптеры устройств содержат все подединицы, используемые клиентскими приложениями для управления обработкой аудио.</span><span class="sxs-lookup"><span data-stu-id="711ed-162">In fact, adapter devices contain all of the subunits that client applications use to control audio processing.</span></span> <span data-ttu-id="711ed-163">Топология устройства конечной точки в основном используется в качестве отправной точки для изучения топологий устройств адаптеров.</span><span class="sxs-lookup"><span data-stu-id="711ed-163">The device topology of an endpoint device serves primarily as a starting point for exploring the device topologies of adapter devices.</span></span>

<span data-ttu-id="711ed-164">Внутренние соединения между двумя частями в топологии устройства называются ссылками.</span><span class="sxs-lookup"><span data-stu-id="711ed-164">Internal connections between two parts in a device topology are called links.</span></span> <span data-ttu-id="711ed-165">API Девицетопологи предоставляет методы для обхода ссылок из одной части в другую в топологии устройства.</span><span class="sxs-lookup"><span data-stu-id="711ed-165">The DeviceTopology API provides methods for traversing links from one part to the next in a device topology.</span></span> <span data-ttu-id="711ed-166">API также предоставляет методы для обхода соединений между топологиями устройств.</span><span class="sxs-lookup"><span data-stu-id="711ed-166">The API also provides methods for traversing the connections between device topologies.</span></span>

<span data-ttu-id="711ed-167">Чтобы приступить к исследованию набора топологий подключенных устройств, клиентское приложение активирует интерфейс **идевицетопологи** устройства конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="711ed-167">To begin exploration of a set of connected device topologies, a client application activates the **IDeviceTopology** interface of an audio endpoint device.</span></span> <span data-ttu-id="711ed-168">Соединитель на устройстве конечной точки подключается к соединителю в звуковом адаптере или в сети.</span><span class="sxs-lookup"><span data-stu-id="711ed-168">The connector in an endpoint device connects either to a connector in an audio adapter or to a network.</span></span> <span data-ttu-id="711ed-169">Если конечная точка подключается к устройству на звуковом адаптере, методы в API Девицетопологи позволяют приложению выполнять шаг через подключение от конечной точки к адаптеру, получая ссылку на интерфейс **идевицетопологи** устройства адаптера на другой стороне соединения.</span><span class="sxs-lookup"><span data-stu-id="711ed-169">If the endpoint connects to a device on an audio adapter, then the methods in the DeviceTopology API enable the application to step across the connection from the endpoint to the adapter by obtaining a reference to the **IDeviceTopology** interface of the adapter device on the other side of the connection.</span></span> <span data-ttu-id="711ed-170">Сеть, с другой стороны, не имеет топологии устройства.</span><span class="sxs-lookup"><span data-stu-id="711ed-170">A network, on the other hand, has no device topology.</span></span> <span data-ttu-id="711ed-171">Сетевое подключение передает звуковой поток клиенту, который обращается к системе удаленно.</span><span class="sxs-lookup"><span data-stu-id="711ed-171">A network connection pipes an audio stream to a client that is accessing the system remotely.</span></span>

<span data-ttu-id="711ed-172">API Девицетопологи предоставляет доступ только к топологиям аппаратных устройств в аудио адаптере.</span><span class="sxs-lookup"><span data-stu-id="711ed-172">The DeviceTopology API provides access only to the topologies of the hardware devices in an audio adapter.</span></span> <span data-ttu-id="711ed-173">Внешние устройства на левой границе схемы и программные компоненты на правом крае выходят за рамки API.</span><span class="sxs-lookup"><span data-stu-id="711ed-173">The external devices on the left edge of the diagram and the software components on the right edge are beyond the scope of the API.</span></span> <span data-ttu-id="711ed-174">Пунктирные линии на обеих сторонах диаграммы представляют ограничения API Девицетопологи.</span><span class="sxs-lookup"><span data-stu-id="711ed-174">The dashed lines on either side of the diagram represent the limits of the DeviceTopology API.</span></span> <span data-ttu-id="711ed-175">Клиент может использовать API для просмотра пути к данным, который растягивается от розетки ввода к системной шине, но API не может проникнуть за пределы этих границ.</span><span class="sxs-lookup"><span data-stu-id="711ed-175">The client can use the API to explore a data path that stretches from the input jack to the system bus, but the API cannot penetrate beyond these boundaries.</span></span>

<span data-ttu-id="711ed-176">Каждый соединитель на предыдущей схеме имеет связанный тип соединения, указывающий тип соединения, создаваемого соединителем.</span><span class="sxs-lookup"><span data-stu-id="711ed-176">Each connector in the preceding diagram has an associated connection type that indicates the type of connection that the connector makes.</span></span> <span data-ttu-id="711ed-177">Таким же соединители на двух сторонах соединения всегда имеют одинаковые типы соединения.</span><span class="sxs-lookup"><span data-stu-id="711ed-177">Thus, the connectors on the two sides of a connection always have identical connection types.</span></span> <span data-ttu-id="711ed-178">Тип соединения указывается значением перечисления [**коннектортипе**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) — физическим \_ внешним, физическим \_ внутренним, фиксированным программным обеспечением, \_ программным \_ вводом или сетью.</span><span class="sxs-lookup"><span data-stu-id="711ed-178">The connection type is indicated by a [**ConnectorType**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) enumeration value—Physical\_External, Physical\_Internal, Software\_Fixed, Software\_IO, or Network.</span></span> <span data-ttu-id="711ed-179">Соединения между устройством и конечными устройствами входного мультиплексора A и B имеют тип физических внешних. это \_ означает, что соединение представляет физическое подключение к внешнему устройству (иными словами, звуковой разъем, доступный пользователю).</span><span class="sxs-lookup"><span data-stu-id="711ed-179">The connections between the input multiplexer device and endpoint devices A and B are of type Physical\_External, which means that the connection represents a physical connection to an external device (in other words, a user-accessible audio jack).</span></span> <span data-ttu-id="711ed-180">Подключение к аналоговому сигналу от внутреннего проигрывателя компакт-диска имеет тип физический \_ внутренний, что означает физическое подключение к вспомогательному устройству, установленному в системном корпусе.</span><span class="sxs-lookup"><span data-stu-id="711ed-180">The connection to the analog signal from the internal CD player is of type Physical\_Internal, which indicates a physical connection to an auxiliary device that is installed inside the system chassis.</span></span> <span data-ttu-id="711ed-181">Подключение между устройством записи Wave и устройством мультиплексора ввода имеет фиксированное программное обеспечение \_ , которое указывает на постоянное фиксированное подключение и не может быть настроено в разделе Управление программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="711ed-181">The connection between the wave capture device and input multiplexer device is of type Software\_Fixed, which indicates a permanent connection that is fixed and cannot be configured under software control.</span></span> <span data-ttu-id="711ed-182">Наконец, соединение с системной шиной в правой части схемы относится к типу программного \_ ввода-вывода, что означает, что данные ввода/вывода для подключения реализуются модулем DMA в разделе Управление программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="711ed-182">Finally, the connection to the system bus on the right side of the diagram is of type Software\_IO, which indicates that the data I/O for the connection is implemented by a DMA engine under software control.</span></span> <span data-ttu-id="711ed-183">(Схема не включает пример типа сетевого подключения.)</span><span class="sxs-lookup"><span data-stu-id="711ed-183">(The diagram does not include an example of a Network connection type.)</span></span>

<span data-ttu-id="711ed-184">Клиент начинает прохождение пути к данным на устройстве конечной точки.</span><span class="sxs-lookup"><span data-stu-id="711ed-184">The client begins traversing a data path at the endpoint device.</span></span> <span data-ttu-id="711ed-185">Сначала клиент получает интерфейс [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) , представляющий устройство конечной точки, как описано в подразделе [перечисление звуковых устройств](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="711ed-185">First, the client obtains an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface that represents the endpoint device, as explained in [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span> <span data-ttu-id="711ed-186">Чтобы получить интерфейс **идевицетопологи** для устройства конечной точки, клиент вызывает метод [**Иммдевице:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) с параметром *IID* , равным рефиид IID \_ идевицетопологи.</span><span class="sxs-lookup"><span data-stu-id="711ed-186">To obtain the **IDeviceTopology** interface for the endpoint device, the client calls the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method with parameter *iid* set to REFIID IID\_IDeviceTopology.</span></span>

<span data-ttu-id="711ed-187">В примере на предыдущей схеме устройство мультиплексора ввода содержит все аппаратные элементы управления (громкость, звук и мультиплексор) для потоков записи из гнезд ввода и микрофона.</span><span class="sxs-lookup"><span data-stu-id="711ed-187">In the example in the preceding diagram, the input multiplexer device contains all the hardware controls (volume, mute, and multiplexer) for the capture streams from the line-input and microphone jacks.</span></span> <span data-ttu-id="711ed-188">В следующем примере кода показано, как получить интерфейс **идевицетопологи** для устройства входного мультиплексора из интерфейса **иммдевице** для устройства конечной точки для линейного входа или микрофона:</span><span class="sxs-lookup"><span data-stu-id="711ed-188">The following code example shows how to obtain the **IDeviceTopology** interface for the input multiplexer device from the **IMMDevice** interface for the endpoint device for the line input or microphone:</span></span>


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface of an endpoint device. The function
// outputs a pointer (counted reference) to the
// IDeviceTopology interface of the adapter device that
// connects to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);

HRESULT GetHardwareDeviceTopology(
            IMMDevice *pEndptDev,
            IDeviceTopology **ppDevTopo)
{
    HRESULT hr = S_OK;
    IDeviceTopology *pDevTopoEndpt = NULL;
    IConnector *pConnEndpt = NULL;
    IConnector *pConnHWDev = NULL;
    IPart *pPartConn = NULL;

    // Get the endpoint device's IDeviceTopology interface.

    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL,
                      NULL, (void**)&pDevTopoEndpt);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).

    hr = pDevTopoEndpt->GetConnector(0, &pConnEndpt);
    EXIT_ON_ERROR(hr)

    // Use the connector in the endpoint device to get the
    // connector in the adapter device.

    hr = pConnEndpt->GetConnectedTo(&pConnHWDev);
    EXIT_ON_ERROR(hr)

    // Query the connector in the adapter device for
    // its IPart interface.

    hr = pConnHWDev->QueryInterface(
                         IID_IPart, (void**)&pPartConn);
    EXIT_ON_ERROR(hr)

    // Use the connector's IPart interface to get the
    // IDeviceTopology interface for the adapter device.

    hr = pPartConn->GetTopologyObject(ppDevTopo);

Exit:
    SAFE_RELEASE(pDevTopoEndpt)
    SAFE_RELEASE(pConnEndpt)
    SAFE_RELEASE(pConnHWDev)
    SAFE_RELEASE(pPartConn)

    return hr;
}
```



<span data-ttu-id="711ed-189">Функция Жесардваредевицетопологи в предыдущем примере кода выполняет следующие действия, чтобы получить интерфейс **идевицетопологи** для устройства входного мультиплексора:</span><span class="sxs-lookup"><span data-stu-id="711ed-189">The GetHardwareDeviceTopology function in the previous code example performs the following steps to obtain the **IDeviceTopology** interface for the input multiplexer device:</span></span>

1.  <span data-ttu-id="711ed-190">Вызовите метод **иммдевице:: Activate** , чтобы получить интерфейс **идевицетопологи** для устройства конечной точки.</span><span class="sxs-lookup"><span data-stu-id="711ed-190">Call the **IMMDevice::Activate** method to get the **IDeviceTopology** interface for the endpoint device.</span></span>
2.  <span data-ttu-id="711ed-191">С помощью интерфейса **идевицетопологи** , полученного на предыдущем шаге, вызовите метод [**идевицетопологи::-Connect**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) , чтобы получить интерфейс **иконнектор** для одного соединителя (номер соединителя 0) на устройстве конечной точки.</span><span class="sxs-lookup"><span data-stu-id="711ed-191">With the **IDeviceTopology** interface obtained in the preceding step, call the [**IDeviceTopology::GetConnector**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) method to get the **IConnector** interface of the single connector (connector number 0) in the endpoint device.</span></span>
3.  <span data-ttu-id="711ed-192">С помощью интерфейса **иконнектор** , полученного на предыдущем шаге, вызовите метод [**Иконнектор:: жетконнектедто**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) , чтобы получить интерфейс **иконнектор** соединителя на устройстве входного мультиплексора.</span><span class="sxs-lookup"><span data-stu-id="711ed-192">With the **IConnector** interface obtained in the preceding step, call the [**IConnector::GetConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) method to get the **IConnector** interface of the connector in the input multiplexer device.</span></span>
4.  <span data-ttu-id="711ed-193">Запросите интерфейс **иконнектор** , полученный на предыдущем шаге, для своего интерфейса **ипарт** .</span><span class="sxs-lookup"><span data-stu-id="711ed-193">Query the **IConnector** interface obtained in the preceding step for its **IPart** interface.</span></span>
5.  <span data-ttu-id="711ed-194">С помощью интерфейса **ипарт** , полученного на предыдущем шаге, вызовите метод [**Ипарт:: жеттопологйобжект**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) , чтобы получить интерфейс **идевицетопологи** для устройства входного мультиплексора.</span><span class="sxs-lookup"><span data-stu-id="711ed-194">With the **IPart** interface obtained in the preceding step, call the [**IPart::GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) method to get the **IDeviceTopology** interface for the input multiplexer device.</span></span>

<span data-ttu-id="711ed-195">Прежде чем пользователь сможет записать данные с микрофона на предыдущей схеме, клиентское приложение должно убедиться, что мультиплексор выбирает входные микрофона.</span><span class="sxs-lookup"><span data-stu-id="711ed-195">Before the user can record from the microphone in the preceding diagram, the client application must make certain that the multiplexer selects the microphone input.</span></span> <span data-ttu-id="711ed-196">В следующем примере кода показано, как клиент может перемещаться по пути к данным с микрофона, пока не обнаружит мультиплексор, который затем программирует на выбор входного микрофона:</span><span class="sxs-lookup"><span data-stu-id="711ed-196">The following code example shows how a client can traverse the data path from the microphone until it finds the multiplexer, which it then programs to select the microphone input:</span></span>


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface for a capture endpoint device. The
// function traverses the data path that extends from the
// endpoint device to the system bus (for example, PCI)
// or external bus (USB). If the function discovers a MUX
// (input selector) in the path, it selects the MUX input
// that connects to the stream from the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);
const IID IID_IConnector = __uuidof(IConnector);
const IID IID_IAudioInputSelector = __uuidof(IAudioInputSelector);

HRESULT SelectCaptureDevice(IMMDevice *pEndptDev)
{
    HRESULT hr = S_OK;
    DataFlow flow;
    IDeviceTopology *pDeviceTopology = NULL;
    IConnector *pConnFrom = NULL;
    IConnector *pConnTo = NULL;
    IPart *pPartPrev = NULL;
    IPart *pPartNext = NULL;
    IAudioInputSelector *pSelector = NULL;

    if (pEndptDev == NULL)
    {
        EXIT_ON_ERROR(hr = E_POINTER)
    }

    // Get the endpoint device's IDeviceTopology interface.
    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL, NULL,
                      (void**)&pDeviceTopology);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).
    hr = pDeviceTopology->GetConnector(0, &pConnFrom);
    SAFE_RELEASE(pDeviceTopology)
    EXIT_ON_ERROR(hr)

    // Make sure that this is a capture device.
    hr = pConnFrom->GetDataFlow(&flow);
    EXIT_ON_ERROR(hr)

    if (flow != Out)
    {
        // Error -- this is a rendering device.
        EXIT_ON_ERROR(hr = AUDCLNT_E_WRONG_ENDPOINT_TYPE)
    }

    // Outer loop: Each iteration traverses the data path
    // through a device topology starting at the input
    // connector and ending at the output connector.
    while (TRUE)
    {
        BOOL bConnected;
        hr = pConnFrom->IsConnected(&bConnected);
        EXIT_ON_ERROR(hr)

        // Does this connector connect to another device?
        if (bConnected == FALSE)
        {
            // This is the end of the data path that
            // stretches from the endpoint device to the
            // system bus or external bus. Verify that
            // the connection type is Software_IO.
            ConnectorType  connType;
            hr = pConnFrom->GetType(&connType);
            EXIT_ON_ERROR(hr)

            if (connType == Software_IO)
            {
                break;  // finished
            }
            EXIT_ON_ERROR(hr = E_FAIL)
        }

        // Get the connector in the next device topology,
        // which lies on the other side of the connection.
        hr = pConnFrom->GetConnectedTo(&pConnTo);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnFrom)

        // Get the connector's IPart interface.
        hr = pConnTo->QueryInterface(
                        IID_IPart, (void**)&pPartPrev);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnTo)

        // Inner loop: Each iteration traverses one link in a
        // device topology and looks for input multiplexers.
        while (TRUE)
        {
            PartType parttype;
            UINT localId;
            IPartsList *pParts;

            // Follow downstream link to next part.
            hr = pPartPrev->EnumPartsOutgoing(&pParts);
            EXIT_ON_ERROR(hr)

            hr = pParts->GetPart(0, &pPartNext);
            pParts->Release();
            EXIT_ON_ERROR(hr)

            hr = pPartNext->GetPartType(&parttype);
            EXIT_ON_ERROR(hr)

            if (parttype == Connector)
            {
                // We've reached the output connector that
                // lies at the end of this device topology.
                hr = pPartNext->QueryInterface(
                                  IID_IConnector,
                                  (void**)&pConnFrom);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pPartPrev)
                SAFE_RELEASE(pPartNext)
                break;
            }

            // Failure of the following call means only that
            // the part is not a MUX (input selector).
            hr = pPartNext->Activate(
                              CLSCTX_ALL,
                              IID_IAudioInputSelector,
                              (void**)&pSelector);
            if (hr == S_OK)
            {
                // We found a MUX (input selector), so select
                // the input from our endpoint device.
                hr = pPartPrev->GetLocalId(&localId);
                EXIT_ON_ERROR(hr)

                hr = pSelector->SetSelection(localId, NULL);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pSelector)
            }

            SAFE_RELEASE(pPartPrev)
            pPartPrev = pPartNext;
            pPartNext = NULL;
        }
    }

Exit:
    SAFE_RELEASE(pConnFrom)
    SAFE_RELEASE(pConnTo)
    SAFE_RELEASE(pPartPrev)
    SAFE_RELEASE(pPartNext)
    SAFE_RELEASE(pSelector)
    return hr;
}
```



<span data-ttu-id="711ed-197">API Девицетопологи реализует интерфейс [**иаудиоинпутселектор**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) для инкапсуляции мультиплексора, например, на предыдущей схеме.</span><span class="sxs-lookup"><span data-stu-id="711ed-197">The DeviceTopology API implements an [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) interface to encapsulate a multiplexer, such as the one in the preceding diagram.</span></span> <span data-ttu-id="711ed-198">(Интерфейс [**иаудиуутпутселектор**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) инкапсулирует демультиплексор.) В предыдущем примере кода внутренний цикл функции Селекткаптуредевице запрашивает каждую найденную подединицу, чтобы определить, является ли подединица мультиплексором.</span><span class="sxs-lookup"><span data-stu-id="711ed-198">(An [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) interface encapsulates a demultiplexer.) In the preceding code example, the inner loop of the SelectCaptureDevice function queries each subunit that it finds to discover whether the subunit is a multiplexer.</span></span> <span data-ttu-id="711ed-199">Если подединица является мультиплексором, то функция вызывает метод [**иаудиоинпутселектор:: сетселектион**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) , чтобы выбрать входные данные, которые подключаются к потоку с устройства конечной точки.</span><span class="sxs-lookup"><span data-stu-id="711ed-199">If the subunit is a multiplexer, then the function calls the [**IAudioInputSelector::SetSelection**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) method to select the input that connects to the stream from the endpoint device.</span></span>

<span data-ttu-id="711ed-200">В предыдущем примере кода каждая итерация внешнего цикла проходит по одной топологии устройства.</span><span class="sxs-lookup"><span data-stu-id="711ed-200">In the preceding code example, each iteration of the outer loop traverses one device topology.</span></span> <span data-ttu-id="711ed-201">При просмотре топологий устройств на предыдущей схеме первая итерация проходит по устройству входного мультиплексора, а вторая итерация проходит по устройству записи звука.</span><span class="sxs-lookup"><span data-stu-id="711ed-201">When traversing the device topologies in the preceding diagram, the first iteration traverses the input multiplexer device and the second iteration traverses the wave capture device.</span></span> <span data-ttu-id="711ed-202">Функция будет завершена при достижении соединителя на правой границе схемы.</span><span class="sxs-lookup"><span data-stu-id="711ed-202">The function will terminate when it reaches the connector at the right edge of the diagram.</span></span> <span data-ttu-id="711ed-203">Завершение происходит, когда функция обнаруживает соединитель с типом соединения с программным обеспечением \_ ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="711ed-203">Termination occurs when the function detects a connector with a Software\_IO connection type.</span></span> <span data-ttu-id="711ed-204">Этот тип подключения определяет точку, в которой устройство адаптера подключается к системной шине.</span><span class="sxs-lookup"><span data-stu-id="711ed-204">This connection type identifies the point at which the adapter device connects to the system bus.</span></span>

<span data-ttu-id="711ed-205">Вызов метода [**ипарт:: жетпарттипе**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) в предыдущем примере кода получает значение перечисления **ипарттипе** , указывающее, является ли текущая часть соединителем или подединицей обработки звука.</span><span class="sxs-lookup"><span data-stu-id="711ed-205">The call to the [**IPart::GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) method in the preceding code example obtains an **IPartType** enumeration value that indicates whether the current part is a connector or an audio-processing subunit.</span></span>

<span data-ttu-id="711ed-206">Внутренний цикл в предыдущем примере кода выполняет шаги по ссылке из одной части в другую путем вызова метода [**ипарт:: енумпартсаутгоинг**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) .</span><span class="sxs-lookup"><span data-stu-id="711ed-206">The inner loop in the preceding code example steps across the link from one part to the next by calling the [**IPart::EnumPartsOutgoing**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) method.</span></span> <span data-ttu-id="711ed-207">(Существует также метод [**ипарт:: енумпартсинкоминг**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) для пошагового выполнения в обратном направлении.) Этот метод извлекает объект [**ипартслист**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) , содержащий список всех исходящих частей.</span><span class="sxs-lookup"><span data-stu-id="711ed-207">(There's also an [**IPart::EnumPartsIncoming**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) method for stepping in the opposite direction.) This method retrieves an [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) object that contains a list of all the outgoing parts.</span></span> <span data-ttu-id="711ed-208">Однако любая часть, которую функция Селекткаптуредевице должна столкнуться на устройстве записи, всегда будет содержать только одну исходящую часть.</span><span class="sxs-lookup"><span data-stu-id="711ed-208">However, any part that the SelectCaptureDevice function expects to encounter in a capture device will always have exactly one outgoing part.</span></span> <span data-ttu-id="711ed-209">Таким образом, последующий вызов [**ипартслист::-Part**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) всегда запрашивает первую часть в списке, часть номер 0, поскольку функция предполагает, что это единственная часть в списке.</span><span class="sxs-lookup"><span data-stu-id="711ed-209">Thus, the subsequent call to [**IPartsList::GetPart**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) always requests the first part in the list, part number 0, because the function assumes that this is the only part in the list.</span></span>

<span data-ttu-id="711ed-210">Если функция Селекткаптуредевице встречает топологию, для которой это допущение является недопустимым, функция может не настроить устройство должным образом.</span><span class="sxs-lookup"><span data-stu-id="711ed-210">If the SelectCaptureDevice function encounters a topology for which that assumption is not valid, the function might fail to configure the device correctly.</span></span> <span data-ttu-id="711ed-211">Чтобы избежать такого сбоя, более универсальная версия функции может выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="711ed-211">To avoid such a failure, a more general-purpose version of the function might do the following:</span></span>

-   <span data-ttu-id="711ed-212">Вызовите метод [**ипартслист:: NOCOUNT**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) , чтобы определить количество исходящих частей.</span><span class="sxs-lookup"><span data-stu-id="711ed-212">Call the [**IPartsList::GetCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) method to determine the number of outgoing parts.</span></span>
-   <span data-ttu-id="711ed-213">Для каждой исходящей части вызовите **ипартслист::** , чтобы начать проход по пути к данным, который ведет от части.</span><span class="sxs-lookup"><span data-stu-id="711ed-213">For each outgoing part, call **IPartsList::GetPart** to begin to traverse the data path that leads from the part.</span></span>

<span data-ttu-id="711ed-214">Некоторые, но не обязательно все компоненты имеют связанные элементы управления оборудованием, которые клиенты могут устанавливать или получать.</span><span class="sxs-lookup"><span data-stu-id="711ed-214">Some, but not necessarily all, parts have associated hardware controls that clients can set or get.</span></span> <span data-ttu-id="711ed-215">Конкретная часть может иметь ноль, один или несколько аппаратных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="711ed-215">A particular part might have zero, one, or more hardware controls.</span></span> <span data-ttu-id="711ed-216">Аппаратный элемент управления представлен следующей парой интерфейсов:</span><span class="sxs-lookup"><span data-stu-id="711ed-216">A hardware control is represented by the following pair of interfaces:</span></span>

-   <span data-ttu-id="711ed-217">Универсальный интерфейс элемента управления [**иконтролинтерфаце**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface), который содержит методы, общие для всех элементов управления оборудования.</span><span class="sxs-lookup"><span data-stu-id="711ed-217">A generic control interface, [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface), which has methods that are common to all hardware controls.</span></span>
-   <span data-ttu-id="711ed-218">Интерфейс, зависящий от функции (например, [**иаудиоволумелевел**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)), который предоставляет параметры управления для конкретного типа аппаратного управления (например, регулятора громкости).</span><span class="sxs-lookup"><span data-stu-id="711ed-218">A function-specific interface (for example, [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)) that exposes the control parameters for a particular type of hardware control (for example, a volume control).</span></span>

<span data-ttu-id="711ed-219">Чтобы перечислить аппаратные элементы управления для части, клиент сначала вызывает метод [**ипарт:: жетконтролинтерфацекаунт**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) , чтобы определить количество аппаратных элементов управления, связанных с частью.</span><span class="sxs-lookup"><span data-stu-id="711ed-219">To enumerate the hardware controls for a part, the client first calls the [**IPart::GetControlInterfaceCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) method to determine the number of hardware controls that are associated with the part.</span></span> <span data-ttu-id="711ed-220">Затем клиент выполняет ряд вызовов метода [**ипарт:: жетконтролинтерфаце**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) , чтобы получить интерфейс **иконтролинтерфаце** для каждого аппаратного управления.</span><span class="sxs-lookup"><span data-stu-id="711ed-220">Next, the client makes a series of calls to the [**IPart::GetControlInterface**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) method to obtain the **IControlInterface** interface for each hardware control.</span></span> <span data-ttu-id="711ed-221">Наконец, клиент получает интерфейс функции для каждого аппаратного управления, вызывая метод [**иконтролинтерфаце:: жетиид**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) для получения идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="711ed-221">Finally, the client obtains the function-specific interface for each hardware control by calling the [**IControlInterface::GetIID**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) method to obtain the interface ID.</span></span> <span data-ttu-id="711ed-222">Клиент вызывает метод [**ипарт:: Activate**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) с этим идентификатором для получения интерфейса, зависящего от функции.</span><span class="sxs-lookup"><span data-stu-id="711ed-222">The client calls the [**IPart::Activate**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) method with this ID to obtain the function-specific interface.</span></span>

<span data-ttu-id="711ed-223">Часть, которая является соединителем, может поддерживать один из следующих интерфейсов элементов управления, зависящих от функции:</span><span class="sxs-lookup"><span data-stu-id="711ed-223">A part that is a connector might support one of the following function-specific control interfaces:</span></span>

-   [<span data-ttu-id="711ed-224">**иксформатсуппорт**</span><span class="sxs-lookup"><span data-stu-id="711ed-224">**IKsFormatSupport**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)
-   [<span data-ttu-id="711ed-225">**иксжаккдескриптион**</span><span class="sxs-lookup"><span data-stu-id="711ed-225">**IKsJackDescription**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)

<span data-ttu-id="711ed-226">Часть, которая является подединицей, может поддерживать один или несколько следующих интерфейсов элементов управления, зависящих от функции:</span><span class="sxs-lookup"><span data-stu-id="711ed-226">A part that is a subunit might support one or more of the following function-specific control interfaces:</span></span>

-   [<span data-ttu-id="711ed-227">**иаудиоаутогаинконтрол**</span><span class="sxs-lookup"><span data-stu-id="711ed-227">**IAudioAutoGainControl**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)
-   [<span data-ttu-id="711ed-228">**иаудиобасс**</span><span class="sxs-lookup"><span data-stu-id="711ed-228">**IAudioBass**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)
-   [<span data-ttu-id="711ed-229">**иаудиочаннелконфиг**</span><span class="sxs-lookup"><span data-stu-id="711ed-229">**IAudioChannelConfig**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)
-   [<span data-ttu-id="711ed-230">**иаудиоинпутселектор**</span><span class="sxs-lookup"><span data-stu-id="711ed-230">**IAudioInputSelector**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)
-   [<span data-ttu-id="711ed-231">**иаудиолауднесс**</span><span class="sxs-lookup"><span data-stu-id="711ed-231">**IAudioLoudness**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)
-   [<span data-ttu-id="711ed-232">**иаудиомидранже**</span><span class="sxs-lookup"><span data-stu-id="711ed-232">**IAudioMidrange**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)
-   [<span data-ttu-id="711ed-233">**иаудиомуте**</span><span class="sxs-lookup"><span data-stu-id="711ed-233">**IAudioMute**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)
-   [<span data-ttu-id="711ed-234">**иаудиуутпутселектор**</span><span class="sxs-lookup"><span data-stu-id="711ed-234">**IAudioOutputSelector**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)
-   [<span data-ttu-id="711ed-235">**иаудиопеакметер**</span><span class="sxs-lookup"><span data-stu-id="711ed-235">**IAudioPeakMeter**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)
-   [<span data-ttu-id="711ed-236">**иаудиотребле**</span><span class="sxs-lookup"><span data-stu-id="711ed-236">**IAudioTreble**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)
-   [<span data-ttu-id="711ed-237">**иаудиоволумелевел**</span><span class="sxs-lookup"><span data-stu-id="711ed-237">**IAudioVolumeLevel**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)
-   [<span data-ttu-id="711ed-238">**идевицеспеЦификпроперти**</span><span class="sxs-lookup"><span data-stu-id="711ed-238">**IDeviceSpecificProperty**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)

<span data-ttu-id="711ed-239">Часть поддерживает интерфейс **идевицеспеЦификпроперти** , только если базовый аппаратный элемент управления имеет зависящее от устройства значение элемента управления, и элемент управления не может быть адекватно представлен каким-либо другим интерфейсом, зависящим от функции, в приведенном выше списке.</span><span class="sxs-lookup"><span data-stu-id="711ed-239">A part supports the **IDeviceSpecificProperty** interface only if the underlying hardware control has a device-specific control value and the control cannot be adequately represented by any other function-specific interface in the preceding list.</span></span> <span data-ttu-id="711ed-240">Как правило, свойство для конкретного устройства удобно использовать только для клиента, который может определить значение свойства из таких сведений, как тип части, подтип части и имя части.</span><span class="sxs-lookup"><span data-stu-id="711ed-240">Typically, a device-specific property is useful only to a client that can infer the meaning of the property value from information such as the part type, part subtype, and part name.</span></span> <span data-ttu-id="711ed-241">Клиент может получить эти сведения, вызвав методы [**ипарт:: жетпарттипе**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype), [**Ипарт:: жетсубтипе**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype)и [**ипарт:: Name**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) .</span><span class="sxs-lookup"><span data-stu-id="711ed-241">The client can obtain this information by calling the [**IPart::GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype), [**IPart::GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype), and [**IPart::GetName**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="711ed-242">См. также</span><span class="sxs-lookup"><span data-stu-id="711ed-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="711ed-243">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="711ed-243">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
