---
title: Пример записи данных волны
description: Пример записи данных волны
ms.assetid: 8078e5b4-340b-409a-88f9-143b02efebc1
keywords:
- звуковая волна, запись данных волны
- вспомогательный звук, запись данных волны
- запись данных волны
- Структура ВАВЕХДР
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ea78101c33ae7701bc30d70e55c788d826d5a4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069867"
---
# <a name="example-of-writing-waveform-data"></a><span data-ttu-id="83f21-107">Пример записи данных волны</span><span class="sxs-lookup"><span data-stu-id="83f21-107">Example of Writing Waveform Data</span></span>

<span data-ttu-id="83f21-108">В следующем примере показаны шаги, необходимые для выделения и настройки структуры [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) и записи блока данных на выходное устройство звуковой волны.</span><span class="sxs-lookup"><span data-stu-id="83f21-108">The following example illustrates the steps required to allocate and set up a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure and write a block of data to a waveform output device.</span></span>


```C++
// Global variables. 

HANDLE hData  = NULL;  // handle of waveform data memory 
HPSTR  lpData = NULL;  // pointer to waveform data memory 
 
void WriteWaveData(void) 
{ 
    HWAVEOUT    hWaveOut; 
    HGLOBAL     hWaveHdr; 
    LPWAVEHDR   lpWaveHdr; 
    HMMIO       hmmio; 
    UINT        wResult; 
    HANDLE      hFormat; 
    WAVEFORMAT  *pFormat; 
    DWORD       dwDataSize; 

    // Open a waveform device for output using window callback. 

    if (waveOutOpen((LPHWAVEOUT)&hWaveOut, WAVE_MAPPER, 
                    (LPWAVEFORMAT)pFormat, 
                    (LONG)hwndApp, 0L, CALLBACK_WINDOW)) 
    { 
        MessageBox(hwndApp, 
                   "Failed to open waveform output device.", 
                   NULL, MB_OK | MB_ICONEXCLAMATION); 
        LocalUnlock(hFormat); 
        LocalFree(hFormat); 
        mmioClose(hmmio, 0); 
        return; 
    } 
 
    // Allocate and lock memory for the waveform data. 
 
    hData = GlobalAlloc(GMEM_MOVEABLE | GMEM_SHARE, dwDataSize ); 
    if (!hData) 
    { 
        MessageBox(hwndApp, "Out of memory.", 
                   NULL, MB_OK | MB_ICONEXCLAMATION); 
        mmioClose(hmmio, 0); 
        return; 
    } 
    if ((lpData = GlobalLock(hData)) == NULL) 
    { 
        MessageBox(hwndApp, "Failed to lock memory for data chunk.", 
                   NULL, MB_OK | MB_ICONEXCLAMATION); 
        GlobalFree(hData); 
        mmioClose(hmmio, 0); 
        return; 
    } 
 
    // Read the waveform data subchunk. 
 
    if(mmioRead(hmmio, (HPSTR) lpData, dwDataSize) != (LRESULT)dwDataSize) 
    { 
        MessageBox(hwndApp, "Failed to read data chunk.", 
                   NULL, MB_OK | MB_ICONEXCLAMATION); 
        GlobalUnlock(hData); 
        GlobalFree(hData); 
        mmioClose(hmmio, 0); 
        return; 
    } 
 
    // Allocate and lock memory for the header. 

    hWaveHdr = GlobalAlloc(GMEM_MOVEABLE | GMEM_SHARE, 
        (DWORD) sizeof(WAVEHDR)); 
    if (hWaveHdr == NULL) 
    { 
        GlobalUnlock(hData); 
        GlobalFree(hData); 
        MessageBox(hwndApp, "Not enough memory for header.", 
            NULL, MB_OK | MB_ICONEXCLAMATION); 
        return; 
    } 
 
    lpWaveHdr = (LPWAVEHDR) GlobalLock(hWaveHdr); 
    if (lpWaveHdr == NULL) 
    { 
        GlobalUnlock(hData); 
        GlobalFree(hData); 
        MessageBox(hwndApp, 
            "Failed to lock memory for header.", 
            NULL, MB_OK | MB_ICONEXCLAMATION); 
        return; 
    } 
 
    // After allocation, set up and prepare header. 
 
    lpWaveHdr->lpData = lpData; 
    lpWaveHdr->dwBufferLength = dwDataSize; 
    lpWaveHdr->dwFlags = 0L; 
    lpWaveHdr->dwLoops = 0L; 
    waveOutPrepareHeader(hWaveOut, lpWaveHdr, sizeof(WAVEHDR)); 
 
    // Now the data block can be sent to the output device. The 
    // waveOutWrite function returns immediately and waveform 
    // data is sent to the output device in the background. 
 
    wResult = waveOutWrite(hWaveOut, lpWaveHdr, sizeof(WAVEHDR)); 
    if (wResult != 0) 
    { 
        waveOutUnprepareHeader(hWaveOut, lpWaveHdr, 
                               sizeof(WAVEHDR)); 
        GlobalUnlock( hData); 
        GlobalFree(hData); 
        MessageBox(hwndApp, "Failed to write block to device", 
                   NULL, MB_OK | MB_ICONEXCLAMATION); 
        return; 
    } 
} 
```



 

 