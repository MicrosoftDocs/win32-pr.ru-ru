---
title: Воспроизведение файла AVI
description: Воспроизведение файла AVI
ms.assetid: 6b3845c4-40ec-4824-88c8-6e4ac458f720
keywords:
- Функция МЦисендкомманд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e0c490a61bbd53dd62a8223a3ded1aa047ce071d1d2544a2b26d1a9152450b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038023"
---
# <a name="playing-the-avi-file"></a>Воспроизведение файла AVI

Перед использованием функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) для отправки команды [**MCI \_ Play**](mci-play.md) приложение выделяет память для структуры, инициализирует элементы, которые она будет использовать, и устанавливает флаги, соответствующие элементам, используемым в структуре. (Если приложение не устанавливает флаг для члена структуры, драйверы MCI игнорируют этот элемент.) Например, в следующем примере демонстрируется воспроизведение фильма с начальной позицией, заданной параметром **двфром** , в конечное расположение, заданное параметром **двто**. (Если любая из этих позиций равна нулю, этот пример записывается так, чтобы не использовать эту точку.)


```C++
DWORD PlayMovie(WORD wDevID, DWORD dwFrom, DWORD dwTo) 
{ 
    MCI_DGV_PLAY_PARMS mciPlay;    // play parameters 
    DWORD dwFlags = 0; 
 
    // Check dwFrom. If it is != 0 then set parameters and flags. 
    if (dwFrom){ 
        mciPlay.dwFrom = dwFrom; // set parameter 
        dwFlags |= MCI_FROM;     // set flag to validate member 
    } 
 
    // Check dwTo. If it is != 0 then set parameters and flags. 
    if (dwTo){ 
        mciPlay.dwTo = dwTo;    // set parameter 
        dwFlags |= MCI_TO;      // set flag to validate member 
    } 
 
    // Send the MCI_PLAY command and return the result. 
    return mciSendCommand(wDevID, MCI_PLAY, dwFlags, 
       (DWORD)(LPVOID)&mciPlay); 
} 
```



 

 