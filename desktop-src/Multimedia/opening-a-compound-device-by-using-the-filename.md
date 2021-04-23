---
title: Открытие составного устройства с помощью имени файла
description: Открытие составного устройства с помощью имени файла
ms.assetid: 5199bb68-44be-4fad-af5b-8fe89f27caee
keywords:
- Функция МЦисендкомманд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20eb271658f77c5af4d35db96dd7bdbe6753af08
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337153"
---
# <a name="opening-a-compound-device-by-using-the-filename"></a><span data-ttu-id="f93e3-104">Открытие составного устройства с помощью имени файла</span><span class="sxs-lookup"><span data-stu-id="f93e3-104">Opening a Compound Device by Using the Filename</span></span>

<span data-ttu-id="f93e3-105">В следующем примере показано, как открыть устройство аудио-сигнала, указав звуковой файл с именем "ЛИТАВРЕ". WAV "с помощью функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f93e3-105">The following example opens the waveform-audio device by specifying a waveform-audio file named "TIMPANI.WAV" using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>


```C++
UINT wDeviceID;
DWORD dwReturn;
MCI_OPEN_PARMS mciOpenParms;
 
// Opens a waveform-audio device by specifying the device and 
// file name.

mciOpenParms.lpstrDeviceType = "waveaudio";
mciOpenParms.lpstrElementName = "timpani.wav";

if (dwReturn = mciSendCommand(NULL, MCI_OPEN,
    MCI_OPEN_TYPE | MCI_OPEN_ELEMENT, (DWORD)(LPVOID) &mciOpenParms))
{
    
    // Error, unable to open device.
    
}

// The device opened successfully; get the device ID.
wDeviceID = mciOpenParms.wDeviceID;
```



 

 