---
title: Управление устройствами (мультимедиа Windows)
description: Управление устройством
ms.assetid: b4479803-f1da-4646-909e-c4ef412ebdcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0e0b59127d160cc44418fd4bce1f9f670d13de
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104071001"
---
# <a name="device-control-windows-multimedia"></a>Управление устройствами (мультимедиа Windows)

Для управления устройством MCI Откройте устройство, отправьте в него необходимые команды, а затем закройте устройство. Команды могут быть очень похожи, даже для совершенно разных устройств MCI. Например, приведенная ниже серия команд MCI выполняет шестой мониторинг звукового компакт-диска с помощью функции [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :


```C++
mciSendString("open cdaudio", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("set cdaudio time format tmsf", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("play cdaudio from 6 to 7", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close cdaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



В следующем примере показана аналогичная серия команд MCI, которая воспроизводит первые 10 000 образцов аудио-файла с волнами:


```C++
mciSendString(
    "open c:\mmdata\purplefi.wav type waveaudio alias finch", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
mciSendString("set finch time format samples", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("play finch from 1 to 10000", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close finch", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



В этих примерах показаны некоторые интересные факты о командах MCI:

-   Одни и те же основные команды ([**Open**](open.md), [**Set**](set.md), [**Play**](play.md)и [**Close**](close.md)) используются с устройствами воспроизведения аудио-и звуковых устройств. Те же команды MCI используются со всеми устройствами MCI.
-   Команда Open для устройства аудио-аудио содержит спецификацию имени файла. Устройство аудио-аудио является *составным устройством* (связанным с файлом данных), а устройство чтения компакт-дисков — *простым устройством* (одно без связанного файла данных).
-   В каждом случае команда Set задает форматы времени, но флаг формата времени для устройства CD Audio указывает формат дорожек/минут/секунд/кадров (ТМСФ), а формат времени, используемый для устройства аудио-аудио, — "Samples".
-   Переменные, используемые с флагами "from" и "to", соответствуют соответствующему формату времени. Например, для устройства CD Audio переменные указывают диапазон дорожек, но для устройства аудио-аудио переменные указывают диапазон выборок.

 

 
