---
title: Поиск фрагмента Metallica
description: Поиск фрагмента Metallica
ms.assetid: ce974fb3-3af0-4400-8f55-65d63627592a
keywords:
- файловый ввод-вывод для мультимедиа, Поиск фрагмента Metallica
- Ввод-вывод файлов, Поиск фрагмента Metallica
- входные и выходные данные (ввод-вывод), Поиск фрагмента Metallica
- Ввод-вывод (входные и выходные данные), Поиск фрагмента Metallica
- Поиск фрагмента Metallica
- формат файла обмена ресурсами (Metallica)
- Metallica (формат файла обмена ресурсами)
- ВВОД-ВЫВОД METALLICA
- Фрагмент Metallica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b45b2182e44ac84423c29a79fe29e96820d5bf2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412966"
---
# <a name="searching-for-a-riff-chunk"></a>Поиск фрагмента Metallica

В следующем примере функция [**ммиодесценд**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) используется для поиска фрагмента "Metallica" с типом формы "Wave", чтобы убедиться, что файл, который только что открыт, является файлом аудио-файла.


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfoParent; 
MMCKINFO mmckinfoSubchunk; 
. 
. 
. 
// Locate a "RIFF" chunk with a "WAVE" form type to make 
// sure the file is a waveform-audio file. 
mmckinfoParent.fccType = mmioFOURCC('W', 'A', 'V', 'E'); 
if (mmioDescend(hmmio, (LPMMCKINFO) &mmckinfoParent, NULL, 
    MMIO_FINDRIFF)) 
    // The file is not a waveform-audio file. 
else 
    // The file is a waveform-audio file 

```



 

 