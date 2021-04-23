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
# <a name="accessing-a-file-io-buffer"></a><span data-ttu-id="281e6-110">Доступ к буферу файлового ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="281e6-110">Accessing a File I/O Buffer</span></span>

<span data-ttu-id="281e6-111">В следующем примере доступ к буферу ввода-вывода осуществляется непосредственно для чтения данных из файла аудио-сигнала.</span><span class="sxs-lookup"><span data-stu-id="281e6-111">The following example accesses an I/O buffer directly to read data from a waveform-audio file.</span></span>


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



<span data-ttu-id="281e6-112">По завершении доступа к буферу файлового ввода-вывода вызовите функцию [**ммиосетинфо**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) , передав адрес структуры [**ммиоинфо**](/previous-versions//dd757322(v=vs.85)) , заполненной функцией [**ммиожетинфо**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) .</span><span class="sxs-lookup"><span data-stu-id="281e6-112">When you finish accessing a file I/O buffer, call the [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) function, passing an address of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure filled by the [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) function.</span></span> <span data-ttu-id="281e6-113">Если вы записали данные в буфер, установите \_ флаг MMIO "грязный" в элементе **DwFlags** структуры **Ммиоинфо** перед вызовом **ммиосетинфо**.</span><span class="sxs-lookup"><span data-stu-id="281e6-113">If you wrote to the buffer, set the MMIO\_DIRTY flag in the **dwFlags** member of the **MMIOINFO** structure before calling **mmioSetInfo**.</span></span> <span data-ttu-id="281e6-114">В противном случае буфер не будет сброшен на диск.</span><span class="sxs-lookup"><span data-stu-id="281e6-114">Otherwise, the buffer will not be flushed to disk.</span></span>

 

 