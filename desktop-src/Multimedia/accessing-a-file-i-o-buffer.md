---
title: Доступ к буферу файлового ввода-вывода
description: Доступ к буферу файлового ввода-вывода
ms.assetid: b829d8ef-8e0b-4c30-b8cf-e9feccc63bbf
keywords:
- операции ввода-вывода файлов мультимедиа, доступ к буферам
- Ввод-вывод файлов, доступ к буферам
- входные и выходные данные (ввод-вывод), доступ к буферам
- Ввод-вывод (входные и выходные данные), доступ к буферам
- доступ к буферам ввода-вывода
- буферизованный ввод-вывод
- Функция Ммиосетинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4ab9533f0f121d42f859961b60d405477856faacee8d8cf36a0dfb975e2587
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808644"
---
# <a name="accessing-a-file-io-buffer"></a>Доступ к буферу файлового ввода-вывода

В следующем примере доступ к буферу ввода-вывода осуществляется непосредственно для чтения данных из файла аудио-сигнала.


```C++
HMMIO    hmmio; 
MMIOINFO mmioinfo; 
DWORD    dwDataSize; 
DWORD    dwCount; 
HPSTR    hptr; 

// Get information about the file I/O buffer. 
if (mmioGetInfo(hmmio, &mmioinfo, 0)) 
{ 
    Error("Failed to get I/O buffer info."); 
    . 
    . 
    . 
    mmioClose(hmmio, 0); 
    return; 
} 
 
// Read the entire file by directly reading the file I/O buffer. 
// When the end of the I/O buffer is reached, advance the buffer. 

for (dwCount = dwDataSize, hptr = lpData; dwCount  0; dwCount--) 
{ 
    // Check to see if the I/O buffer must be advanced. 
    if (mmioinfo.pchNext == mmioinfo.pchEndRead) 
    { 
        if(mmioAdvance(hmmio, &mmioinfo, MMIO_READ)) 
        { 
            Error("Failed to advance buffer."); 
            . 
            . 
            . 
            mmioClose(hmmio, 0); 
            return; 
        } 
    } 
 
    // Get a character from the buffer. 
    *hptr++ = *mmioinfo.pchNext++; 
} 
 
// End direct buffer access and close the file. 
mmioSetInfo(hmmio, &mmioinfo, 0); 
mmioClose(hmmio, 0); 

```



По завершении доступа к буферу файлового ввода-вывода вызовите функцию [**ммиосетинфо**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) , передав адрес структуры [**ммиоинфо**](/previous-versions//dd757322(v=vs.85)) , заполненной функцией [**ммиожетинфо**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) . Если вы записали данные в буфер, установите \_ флаг MMIO "грязный" в элементе **DwFlags** структуры **Ммиоинфо** перед вызовом **ммиосетинфо**. В противном случае буфер не будет сброшен на диск.

 

 