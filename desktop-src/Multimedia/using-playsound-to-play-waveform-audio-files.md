---
title: Использование функции PlaySound для воспроизведения Waveform-Audio файлов
description: Использование функции PlaySound для воспроизведения Waveform-Audio файлов
ms.assetid: 8b7d191b-6b0c-4dff-84de-cb3a5c314b80
keywords:
- волна Audio, функция PlaySound
- звуковая волна, воспроизведение файлов
- звуковая волна, расширение имени файла WAV
- Функция PlaySound, воспроизведение аудио-файлов
- Воспроизведение аудио-файлов, функция PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9d5dde46827b7892217f760c749e75e19f368f5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987503"
---
# <a name="using-playsound-to-play-waveform-audio-files"></a><span data-ttu-id="7db80-108">Использование функции PlaySound для воспроизведения Waveform-Audio файлов</span><span class="sxs-lookup"><span data-stu-id="7db80-108">Using PlaySound to Play Waveform-Audio Files</span></span>

<span data-ttu-id="7db80-109">В большинстве звуковых файлов с аудио-файлами используется. Расширение имени файла WAV.</span><span class="sxs-lookup"><span data-stu-id="7db80-109">Most waveform-audio files use the .WAV filename extension.</span></span>

<span data-ttu-id="7db80-110">Следующая инструкция воспроизводит сигналы C: \\ Sounds \\ . WAV файл:</span><span class="sxs-lookup"><span data-stu-id="7db80-110">The following statement plays the C:\\SOUNDS\\BELLS.WAV file:</span></span>


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC); 
```



<span data-ttu-id="7db80-111">Если указанный файл не существует или файл не умещается в доступную память, то [**PlaySound**](/previous-versions//dd743680(v=vs.85)) воспроизводит системный звук по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7db80-111">If the specified file does not exist, or if the file does not fit into the available memory, [**PlaySound**](/previous-versions//dd743680(v=vs.85)) plays the default system sound.</span></span> <span data-ttu-id="7db80-112">Если системный звук по умолчанию не определен, **PlaySound** завершается сбоем без какого бы то ни было звука.</span><span class="sxs-lookup"><span data-stu-id="7db80-112">If no default system sound has been defined, **PlaySound** fails without producing any sound.</span></span> <span data-ttu-id="7db80-113">Если вы не хотите воспроизводить системный звук по умолчанию, укажите флаг "SND" \_ по умолчанию, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="7db80-113">If you do not want the default system sound to play, specify the SND\_NODEFAULT flag, as shown in the following example:</span></span>


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC | SND_NODEFAULT); 
```



 

 