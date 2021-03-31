---
title: Изменение размера буфера ввода-вывода
description: Изменение размера буфера ввода-вывода
ms.assetid: eff97399-143e-477b-bb16-7305e83a2317
keywords:
- Ввод-вывод файлов мультимедиа, изменение размера буфера
- Ввод-вывод файлов, изменение размера буфера
- Ввод и вывод (ввод-вывод), изменение размера буфера
- Ввод-вывод (входные и выходные данные), изменение размера буфера
- изменение размера буфера ввода-вывода
- операции ввода-вывода без буферизации
- буферизованный ввод-вывод
- Функция Ммиосетбуффер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2171f4f09b933a3de5ec1e99750261fdda2f80
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104070011"
---
# <a name="changing-the-io-buffer-size"></a><span data-ttu-id="46174-111">Изменение размера буфера ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="46174-111">Changing the I/O Buffer Size</span></span>

<span data-ttu-id="46174-112">В следующем примере открывается файл с именем SAMPLE.TXT для небуферизованного ввода-вывода, а затем включается буферизованный ввод-вывод с внутренним буфером 16 КБ с помощью функции [**ммиосетбуффер**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) .</span><span class="sxs-lookup"><span data-stu-id="46174-112">The following example opens a file named SAMPLE.TXT for unbuffered I/O, and then enables buffered I/O with an internal 16K buffer using the [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) function.</span></span>


```C++
HMMIO hFile; 

if ((hFile = mmioOpen("SAMPLE.TXT", NULL, MMIO_READ)) != NULL) 
{ 
    // File opened successfully; request an I/O buffer. 
    if (mmioSetBuffer(hFile, NULL, 16384L, 0)) 
        // Buffer cannot be allocated. 
    else 
        // Buffer allocated successfully. 
} 
else 
    // File cannot be opened. 
```



 

 