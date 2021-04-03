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
# <a name="using-playsound-to-play-waveform-audio-files"></a>Использование функции PlaySound для воспроизведения Waveform-Audio файлов

В большинстве звуковых файлов с аудио-файлами используется. Расширение имени файла WAV.

Следующая инструкция воспроизводит сигналы C: \\ Sounds \\ . WAV файл:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC); 
```



Если указанный файл не существует или файл не умещается в доступную память, то [**PlaySound**](/previous-versions//dd743680(v=vs.85)) воспроизводит системный звук по умолчанию. Если системный звук по умолчанию не определен, **PlaySound** завершается сбоем без какого бы то ни было звука. Если вы не хотите воспроизводить системный звук по умолчанию, укажите флаг "SND" \_ по умолчанию, как показано в следующем примере:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC | SND_NODEFAULT); 
```



 

 