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
ms.openlocfilehash: 826fabfb7e51b80bf406721b3d5e7b094f83c1c3fe2061f7edea0810a41dc639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145087"
---
# <a name="changing-the-io-buffer-size"></a>Изменение размера буфера ввода-вывода

В следующем примере открывается файл с именем SAMPLE.TXT для небуферизованного ввода-вывода, а затем включается буферизованный ввод-вывод с внутренним буфером 16 КБ с помощью функции [**ммиосетбуффер**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) .


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



 

 