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
ms.openlocfilehash: 57c89b2376f1bae68d55c76d7731b6ee78f6bf7d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105672274"
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

 

 