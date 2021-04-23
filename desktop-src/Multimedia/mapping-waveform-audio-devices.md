---
title: Сопоставление устройств Waveform-Audio
description: Сопоставление устройств Waveform-Audio
ms.assetid: e23919c9-c5fa-4406-920c-1fdbeea4821d
keywords:
- мультимедийные аудио, сопоставление аудио-устройств
- аудио, сопоставление устройств аудио-аудиосигналов
- Диспетчер аудиосжатия (ACM), сопоставление устройств аудио-аудиосигнала
- ACM (диспетчер аудиосжатия), сопоставление аудио-устройств
- Сопоставление аудио-устройств
- мультимедийные аудио, сопоставитель
- аудио, сопоставитель
- Диспетчер аудиосжатия (ACM), сопоставитель
- ACM (диспетчер аудиосжатия), сопоставитель
- mapper
- звуковая волна, сопоставление устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9cdd269e21eb992244dd0e5979c7e0d193ba92b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888099"
---
# <a name="mapping-waveform-audio-devices"></a><span data-ttu-id="32c9d-114">Сопоставление устройств Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="32c9d-114">Mapping Waveform-Audio Devices</span></span>

<span data-ttu-id="32c9d-115">Windows предоставляет набор стандартных функций для звуковых устройств.</span><span class="sxs-lookup"><span data-stu-id="32c9d-115">Windows provides a set of standard functions for audio devices.</span></span> <span data-ttu-id="32c9d-116">Эти функции выдают вызовы к драйверам устройств, которые управляют аппаратными устройствами.</span><span class="sxs-lookup"><span data-stu-id="32c9d-116">These functions issue calls to device drivers that manage hardware devices.</span></span> <span data-ttu-id="32c9d-117">Система использует модуль "средство сопоставления" для управления установленными устройствами.</span><span class="sxs-lookup"><span data-stu-id="32c9d-117">The system uses a module called a "mapper" to manage installed devices.</span></span> <span data-ttu-id="32c9d-118">Средство сопоставления использует специальные обработчики в интерфейсе драйвера для перехвата вызовов и действия в качестве посредника между системой и драйверами, установленными в системе.</span><span class="sxs-lookup"><span data-stu-id="32c9d-118">The mapper uses special hooks in the driver interface to intercept calls and to act as an intermediary between the system and the drivers installed in the system.</span></span> <span data-ttu-id="32c9d-119">Модуль сопоставления отвечает за сопоставление запросов приложения для доступа к устройству с доступными устройствами, а также для поиска устройства, удовлетворяющего требованиям к аудио в текущем приложении.</span><span class="sxs-lookup"><span data-stu-id="32c9d-119">The mapper is responsible for matching an application's requests for access to a device with the available devices and for finding a device that meets the current application's audio requirements.</span></span> <span data-ttu-id="32c9d-120">Система предоставляет средства сопоставления для стандартных типов драйверов: аудио-аудио, MIDI (цифровой интерфейс музыкального инструмента) и дополнительные устройства.</span><span class="sxs-lookup"><span data-stu-id="32c9d-120">The system provides mappers for standard driver types: waveform-audio, MIDI (Musical Instrument Digital Interface), and auxiliary devices.</span></span>

<span data-ttu-id="32c9d-121">ACM является расширением базовой системы мультимедиа и устанавливается в качестве модуля сопоставления.</span><span class="sxs-lookup"><span data-stu-id="32c9d-121">The ACM is an extension of the basic multimedia system and is installed as a mapper.</span></span> <span data-ttu-id="32c9d-122">Это означает, что ACM использует обработчики сопоставителя интерфейсов драйверов для устройств аудио-аудиосигнала.</span><span class="sxs-lookup"><span data-stu-id="32c9d-122">This means the ACM uses the driver-interface mapper hooks for waveform-audio devices.</span></span> <span data-ttu-id="32c9d-123">Использование этих обработчиков позволяет ACM декодировать или кодировать аудио-файлы перед передачей данных в драйвер устройства аудио-Audio.</span><span class="sxs-lookup"><span data-stu-id="32c9d-123">Using these hooks allows the ACM to decode or encode waveform-audio data before passing it to or from a waveform-audio device driver.</span></span> <span data-ttu-id="32c9d-124">Разница между ACM и стандартным средством сопоставления систем заключается в том, что ACM может искать устройство аудио аудио, поддерживающее указанный формат, или находить комбинацию устройства аудио-аудио, а также ACM компрессор или декомпрессор, поддерживающие указанный формат.</span><span class="sxs-lookup"><span data-stu-id="32c9d-124">The difference between the ACM and the standard system mapper is that the ACM can search for a waveform-audio device that supports a specified format or find a combination of a waveform-audio device and an ACM compressor or decompressor that supports a specified format.</span></span>

<span data-ttu-id="32c9d-125">Когда приложение запрашивает, что система открывает устройство аудио-аудио для ввода или вывода, запрос указывает формат и устройство.</span><span class="sxs-lookup"><span data-stu-id="32c9d-125">When an application requests that the system open a waveform-audio device for input or output, the request specifies the format and device.</span></span> <span data-ttu-id="32c9d-126">Если указанное устройство является модулем сопоставления, средство сопоставления должно найти устройство, которое поддерживает указанный формат.</span><span class="sxs-lookup"><span data-stu-id="32c9d-126">When the specified device is the mapper, the mapper must find a device that supports the specified format.</span></span> <span data-ttu-id="32c9d-127">Модуль сопоставления, реализованный в ACM, выполняет поиск установленного устройства аудио-аудио, поддерживающего указанный формат.</span><span class="sxs-lookup"><span data-stu-id="32c9d-127">The mapper implemented in the ACM searches for an installed waveform-audio device that supports the specified format.</span></span> <span data-ttu-id="32c9d-128">Если ACM не удается найти такое устройство, он выполняет поиск устройства аудио-аудио и программы сжатия или декомпрессора, которые поддерживают этот формат.</span><span class="sxs-lookup"><span data-stu-id="32c9d-128">If the ACM cannot find such a device, it searches for a waveform-audio device and a compressor or decompressor that together support the format.</span></span> <span data-ttu-id="32c9d-129">В частности, ACM ищет программу сжатия или декомпрессора, преобразующую указанный формат в формат, поддерживаемый установленным устройством аудио-звука.</span><span class="sxs-lookup"><span data-stu-id="32c9d-129">Specifically, the ACM searches for a compressor or decompressor that converts the specified format into a format that is supported by an installed waveform-audio device.</span></span> <span data-ttu-id="32c9d-130">После того, как ACM обнаружит устройство, которое поддерживает преобразованный формат, оно может обрабатывать запросы на воспроизведение или запись первоначально запрошенного формата, даже если устройство аудио аудио не поддерживает этот формат напрямую.</span><span class="sxs-lookup"><span data-stu-id="32c9d-130">After the ACM finds a device that supports the converted format, it can honor requests to play or record the format originally requested, even though no installed waveform-audio device directly supports that format.</span></span>

<span data-ttu-id="32c9d-131">В дополнение к преобразованию формата ACM также предлагает службы для поддержки сжатия, распаковки, фильтрации, форматирования и выбора фильтра.</span><span class="sxs-lookup"><span data-stu-id="32c9d-131">In addition to format conversion, the ACM also offers services to support compression, decompression, filtering, format selection, and filter selection.</span></span> <span data-ttu-id="32c9d-132">Он предоставляет стандартный API, который он поддерживает, вызывая собственные драйверы.</span><span class="sxs-lookup"><span data-stu-id="32c9d-132">It provides a standard API that it supports by calling its own drivers.</span></span>

 

 




