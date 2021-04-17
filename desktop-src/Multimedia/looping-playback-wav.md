---
title: Циклическое воспроизведение (волна Audio)
description: Циклическое воспроизведение (волна Audio)
ms.assetid: 8411290b-a3c5-4347-bee3-43c35188f736
keywords:
- звуковая волна, циклический перебор звуков
- аудио-интерфейс, циклический перебор звуков
- звуковая волна, воспроизведение циклов
- аудио-интерфейс, воспроизведение циклов
- Циклическая волна-звук
- Циклическое воспроизведение аудио-сигнала
- Функция Вавеаутврите
- Функция Вавеаутбреаклуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c233799e2d4faf8107b4a2a68a261b544ec1274
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/26/2021
ms.locfileid: "105652299"
---
# <a name="looping-playback"></a><span data-ttu-id="f9a6c-111">Циклическое воспроизведение</span><span class="sxs-lookup"><span data-stu-id="f9a6c-111">Looping Playback</span></span>

<span data-ttu-id="f9a6c-112">Циклический перебор звука контролируется членами **двлупс** и **dwFlags** в структурах [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , передаваемых на устройство с помощью функции [**вавеаутврите**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) .</span><span class="sxs-lookup"><span data-stu-id="f9a6c-112">Looping a sound is controlled by the **dwLoops** and **dwFlags** members in the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structures passed to the device with the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function.</span></span> <span data-ttu-id="f9a6c-113">Используйте флаги **вхдр \_ Бегинлуп** и **Вхдр \_ ендлуп** в элементе **dwFlags** , чтобы указать начальный и конечный блоки данных для циклов.</span><span class="sxs-lookup"><span data-stu-id="f9a6c-113">Use the **WHDR\_BEGINLOOP** and **WHDR\_ENDLOOP** flags in the **dwFlags** member to specify the beginning and ending data blocks for looping.</span></span>

<span data-ttu-id="f9a6c-114">Чтобы перебрать один блок данных, укажите оба флага для одного и того же блока.</span><span class="sxs-lookup"><span data-stu-id="f9a6c-114">To loop a single data block, specify both flags for the same block.</span></span> <span data-ttu-id="f9a6c-115">Чтобы указать число циклов, используйте элемент **двлупс** в структуре [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) для первого блока в цикле.</span><span class="sxs-lookup"><span data-stu-id="f9a6c-115">To specify the number of loops, use the **dwLoops** member in the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure for the first block in the loop.</span></span>

<span data-ttu-id="f9a6c-116">Для завершения циклического звука можно вызвать функцию [**вавеаутбреаклуп**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) .</span><span class="sxs-lookup"><span data-stu-id="f9a6c-116">You can call the [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) function to stop a looping sound.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9a6c-117">См. также</span><span class="sxs-lookup"><span data-stu-id="f9a6c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9a6c-118">Воспроизведение Waveform-Audio файлов</span><span class="sxs-lookup"><span data-stu-id="f9a6c-118">Playing Waveform-Audio Files</span></span>](playing-waveform-audio-files.md)
</dt> </dl>

 

 
