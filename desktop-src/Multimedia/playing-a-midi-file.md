---
title: Воспроизведение файла MIDI
description: Воспроизведение файла MIDI
ms.assetid: a11b432f-de31-4637-a9cd-eef5fad7591a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7ce9638a5f26a2d701798f72229877dc2758829
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987432"
---
# <a name="playing-a-midi-file"></a><span data-ttu-id="325bd-103">Воспроизведение файла MIDI</span><span class="sxs-lookup"><span data-stu-id="325bd-103">Playing a MIDI File</span></span>

<span data-ttu-id="325bd-104">В следующем примере показано, как открыть устройство MIDI Sequencer, проверить, выбран ли сопоставитель MIDI в качестве порта вывода, воспроизводит файл MIDI, указанный параметром *лпсзмидифиленаме* , и закроет устройство после завершения воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="325bd-104">The following example opens a MIDI sequencer device, verifies that the MIDI mapper was selected as the output port, plays the MIDI file specified by the *lpszMIDIFileName* parameter, and closes the device after playback is complete.</span></span> <span data-ttu-id="325bd-105">В нем используется функция [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="325bd-105">It uses the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>


```C++
// Plays a specified MIDI file by using MCI_OPEN and MCI_PLAY. Returns 
// as soon as playback begins. The window procedure function for the 
// specified window will be notified when playback is complete. 
// Returns 0L on success; otherwise, it returns an MCI error code.

DWORD playMIDIFile(HWND hWndNotify, LPSTR lpszMIDIFileName)
{
    UINT wDeviceID;
    DWORD dwReturn;
    MCI_OPEN_PARMS mciOpenParms;
    MCI_PLAY_PARMS mciPlayParms;
    MCI_STATUS_PARMS mciStatusParms;
    MCI_SEQ_SET_PARMS mciSeqSetParms;

    // Open the device by specifying the device and filename.
    // MCI will attempt to choose the MIDI mapper as the output port.
    mciOpenParms.lpstrDeviceType = "sequencer";
    mciOpenParms.lpstrElementName = lpszMIDIFileName;
    if (dwReturn = mciSendCommand(NULL, MCI_OPEN,
        MCI_OPEN_TYPE | MCI_OPEN_ELEMENT,
        (DWORD)(LPVOID) &mciOpenParms))
    {
        // Failed to open device. Don't close it; just return error.
        return (dwReturn);
    }

    // The device opened successfully; get the device ID.
    wDeviceID = mciOpenParms.wDeviceID;

    // Check if the output port is the MIDI mapper.
    mciStatusParms.dwItem = MCI_SEQ_STATUS_PORT;
    if (dwReturn = mciSendCommand(wDeviceID, MCI_STATUS, 
        MCI_STATUS_ITEM, (DWORD)(LPVOID) &mciStatusParms))
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (dwReturn);
    }

    // The output port is not the MIDI mapper. 
    // Ask if the user wants to continue.
    if (LOWORD(mciStatusParms.dwReturn) != MIDI_MAPPER)
    {
        if (MessageBox(hMainWnd,
            "The MIDI mapper is not available. Continue?",
            "", MB_YESNO) == IDNO)
        {
            // User does not want to continue. Not an error;
            // just close the device and return.
            mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
            return (0L);
        }
    }

    // Begin playback. The window procedure function for the parent 
    // window will be notified with an MM_MCINOTIFY message when 
    // playback is complete. At this time, the window procedure closes 
    // the device.
    mciPlayParms.dwCallback = (DWORD) hWndNotify;
    if (dwReturn = mciSendCommand(wDeviceID, MCI_PLAY, MCI_NOTIFY, 
        (DWORD)(LPVOID) &mciPlayParms))
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (dwReturn);
    }

    return (0L);
}
```



 

 