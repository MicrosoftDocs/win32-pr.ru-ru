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
# <a name="device-control-windows-multimedia"></a><span data-ttu-id="8eb4c-103">Управление устройствами (мультимедиа Windows)</span><span class="sxs-lookup"><span data-stu-id="8eb4c-103">Device Control (Windows Multimedia)</span></span>

<span data-ttu-id="8eb4c-104">Для управления устройством MCI Откройте устройство, отправьте в него необходимые команды, а затем закройте устройство.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-104">To control an MCI device, you open the device, send the necessary commands to it, and then close the device.</span></span> <span data-ttu-id="8eb4c-105">Команды могут быть очень похожи, даже для совершенно разных устройств MCI.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-105">The commands can be very similar, even for completely different MCI devices.</span></span> <span data-ttu-id="8eb4c-106">Например, приведенная ниже серия команд MCI выполняет шестой мониторинг звукового компакт-диска с помощью функции [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :</span><span class="sxs-lookup"><span data-stu-id="8eb4c-106">For example, the following series of MCI commands plays the sixth track of an audio CD by using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function:</span></span>


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



<span data-ttu-id="8eb4c-107">В следующем примере показана аналогичная серия команд MCI, которая воспроизводит первые 10 000 образцов аудио-файла с волнами:</span><span class="sxs-lookup"><span data-stu-id="8eb4c-107">The next example shows a similar series of MCI commands that plays the first 10,000 samples of a waveform-audio file:</span></span>


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



<span data-ttu-id="8eb4c-108">В этих примерах показаны некоторые интересные факты о командах MCI:</span><span class="sxs-lookup"><span data-stu-id="8eb4c-108">These examples illustrate some interesting facts about MCI commands:</span></span>

-   <span data-ttu-id="8eb4c-109">Одни и те же основные команды ([**Open**](open.md), [**Set**](set.md), [**Play**](play.md)и [**Close**](close.md)) используются с устройствами воспроизведения аудио-и звуковых устройств.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-109">The same basic commands ([**open**](open.md), [**set**](set.md), [**play**](play.md), and [**close**](close.md)) are used with CD audio and waveform-audio devices.</span></span> <span data-ttu-id="8eb4c-110">Те же команды MCI используются со всеми устройствами MCI.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-110">The same MCI commands are used with all MCI devices.</span></span>
-   <span data-ttu-id="8eb4c-111">Команда Open для устройства аудио-аудио содержит спецификацию имени файла.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-111">The open command for the waveform-audio device includes a filename specification.</span></span> <span data-ttu-id="8eb4c-112">Устройство аудио-аудио является *составным устройством* (связанным с файлом данных), а устройство чтения компакт-дисков — *простым устройством* (одно без связанного файла данных).</span><span class="sxs-lookup"><span data-stu-id="8eb4c-112">The waveform-audio device is a *compound device* (one associated with a data file), while the CD audio device is a *simple device* (one without an associated data file).</span></span>
-   <span data-ttu-id="8eb4c-113">В каждом случае команда Set задает форматы времени, но флаг формата времени для устройства CD Audio указывает формат дорожек/минут/секунд/кадров (ТМСФ), а формат времени, используемый для устройства аудио-аудио, — "Samples".</span><span class="sxs-lookup"><span data-stu-id="8eb4c-113">The set command specifies time formats in each case, but the time-format flag for the CD audio device specifies tracks/minutes/seconds/frames (TMSF) format, while the time format used with the waveform-audio device specifies "samples".</span></span>
-   <span data-ttu-id="8eb4c-114">Переменные, используемые с флагами "from" и "to", соответствуют соответствующему формату времени.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-114">The variables used with the "from" and "to" flags are appropriate to the respective time format.</span></span> <span data-ttu-id="8eb4c-115">Например, для устройства CD Audio переменные указывают диапазон дорожек, но для устройства аудио-аудио переменные указывают диапазон выборок.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-115">For example, for the CD audio device, the variables specify a range of tracks, but for the waveform-audio device, the variables specify a range of samples.</span></span>

 

 
