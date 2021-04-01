---
title: Простое воспроизведение звука
description: Простое воспроизведение звука
ms.assetid: 51a0244d-123d-4efe-92e9-972e914cef78
keywords:
- мультимедийные аудио, волна
- аудио, волна
- звуковая волна, простое воспроизведение
- Функция Мессажебип
- Функция Сндплайсаунд
- Функция PlaySound, простое воспроизведение
- мультимедиа Audio, функция PlaySound
- Audio, функция PlaySound
- волна Audio, функция PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256feded06de4ee92ee415f14bb08adc7fb4456e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987430"
---
# <a name="simple-audio-playback"></a><span data-ttu-id="1bcc3-112">Простое воспроизведение звука</span><span class="sxs-lookup"><span data-stu-id="1bcc3-112">Simple Audio Playback</span></span>

<span data-ttu-id="1bcc3-113">Для воспроизведения звуковых аудио в приложении в одном вызове функции можно использовать следующие функции.</span><span class="sxs-lookup"><span data-stu-id="1bcc3-113">You can use the following functions to play waveform audio in your application in a single function call.</span></span>



| <span data-ttu-id="1bcc3-114">Функция</span><span class="sxs-lookup"><span data-stu-id="1bcc3-114">Function</span></span>                                                      | <span data-ttu-id="1bcc3-115">Описание</span><span class="sxs-lookup"><span data-stu-id="1bcc3-115">Description</span></span>                                                                                                         |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1bcc3-116">мессажебип</span><span class="sxs-lookup"><span data-stu-id="1bcc3-116">MessageBeep</span></span>](/windows/win32/api/winuser/nf-winuser-messagebeep) | <span data-ttu-id="1bcc3-117">Воспроизводит звук, соответствующий указанному уровню оповещения системы.</span><span class="sxs-lookup"><span data-stu-id="1bcc3-117">Plays the sound that corresponds to a specified system-alert level.</span></span>                                                 |
| <span data-ttu-id="1bcc3-118">[**сндплайсаунд**](/previous-versions//dd798676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1bcc3-118">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span></span>                          | <span data-ttu-id="1bcc3-119">Воспроизводит звук, соответствующий системному звуку, введенному в реестр, или содержимому указанного файла.</span><span class="sxs-lookup"><span data-stu-id="1bcc3-119">Plays the sound that corresponds to the system sound entered in the registry or the contents of the specified file.</span></span> |
| <span data-ttu-id="1bcc3-120">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1bcc3-120">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span></span>                                | <span data-ttu-id="1bcc3-121">Предоставляет все функции [**сндплайсаунд**](/previous-versions//dd798676(v=vs.85)) и может напрямую обращаться к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="1bcc3-121">Provides all the functionality of [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) and can directly access resources.</span></span>           |



 

<span data-ttu-id="1bcc3-122">Функция **мессажебип** является стандартной частью API Win32. так как его возможности очень ограничены и описаны в других местах, это не рассматривается здесь.</span><span class="sxs-lookup"><span data-stu-id="1bcc3-122">The **MessageBeep** function is a standard part of the Win32 API; because its capabilities are very limited and it is documented elsewhere, it is not discussed here.</span></span>

<span data-ttu-id="1bcc3-123">Перечисленные функции поддерживают следующие источники звуковой волны:</span><span class="sxs-lookup"><span data-stu-id="1bcc3-123">The functions listed support the following sources of waveform audio:</span></span>

-   <span data-ttu-id="1bcc3-124">Аудио-файлы, связанные с уровнями оповещения системы</span><span class="sxs-lookup"><span data-stu-id="1bcc3-124">Waveform-audio files associated with system-alert levels</span></span>
-   <span data-ttu-id="1bcc3-125">Аудио-файлы, указанные записями в реестре</span><span class="sxs-lookup"><span data-stu-id="1bcc3-125">Waveform-audio files specified by entries in the registry</span></span>
-   <span data-ttu-id="1bcc3-126">Ресурсы звукозаписи в памяти</span><span class="sxs-lookup"><span data-stu-id="1bcc3-126">In-memory WAVE resources</span></span>
-   <span data-ttu-id="1bcc3-127">Аудио-файлы, указанные по имени</span><span class="sxs-lookup"><span data-stu-id="1bcc3-127">Waveform-audio files specified by name</span></span>

<span data-ttu-id="1bcc3-128">Функции [**сндплайсаунд**](/previous-versions//dd798676(v=vs.85)) и [**PlaySound**](/previous-versions//dd743680(v=vs.85)) загружают весь звуковой файл аудио в память и, по сути, ограничивают размер файла, который они могут воспроизвести.</span><span class="sxs-lookup"><span data-stu-id="1bcc3-128">The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) and [**PlaySound**](/previous-versions//dd743680(v=vs.85)) functions load an entire waveform-audio file into memory and, in effect, limit the size of the file they can play.</span></span> <span data-ttu-id="1bcc3-129">Используйте **сндплайсаунд** и **PlaySound** для воспроизведения звуковых файлов с небольшими размерами, вплоть до 100 КБ.</span><span class="sxs-lookup"><span data-stu-id="1bcc3-129">Use **sndPlaySound** and **PlaySound** to play waveform-audio files that are small — up to about 100K.</span></span> <span data-ttu-id="1bcc3-130">Эти две функции также занимают звуковые данные в формате, воспроизводимом одним из установленных драйверов аудио с форматом аудио, включая средство сопоставления волн.</span><span class="sxs-lookup"><span data-stu-id="1bcc3-130">These two functions also require the sound data to be in a format that is playable by one of the installed waveform-audio drivers, including the wave mapper.</span></span>

<span data-ttu-id="1bcc3-131">Для больших звуковых файлов используйте службы интерфейса управления мультимедиа (MCI).</span><span class="sxs-lookup"><span data-stu-id="1bcc3-131">For larger sound files, use the Media Control Interface (MCI) services.</span></span> <span data-ttu-id="1bcc3-132">Дополнительные сведения см. в разделе [MCI](mci.md).</span><span class="sxs-lookup"><span data-stu-id="1bcc3-132">For more information, see [MCI](mci.md).</span></span>

 

 