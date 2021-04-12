---
title: Поиск подфрагмента
description: Поиск подфрагмента
ms.assetid: c494a57f-6395-40a4-a4f2-d200d7ad6223
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
ms.openlocfilehash: 3d6cfb0ecc3223f4a883998e9f192bfbbb5ff276
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337444"
---
# <a name="searching-for-a-subchunk"></a>Поиск подфрагмента

В следующем примере функция [**ммиодесценд**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) используется для поиска фрагмента "fmt" в фрагменте "Metallica" предыдущего примера.


```C++
// Find the format chunk (form type "FMT"); it should be 
// a subchunk of the "RIFF" parent chunk. 
mmckinfoSubchunk.ckid = mmioFOURCC('f', 'm', 't', ' '); 
if (mmioDescend(hmmio, &mmckinfoSubchunk, &mmckinfoParent, 
    MMIO_FINDCHUNK)) 
    // Error, cannot find the "FMT" chunk. 
else 
    // "FMT" chunk found. 
```



Для поиска подфрагмента (т. е. любого фрагмента, отличного от «Metallica» или «LIST»), необходимо задать его родительский фрагмент в параметре *лпккпарент* функции [**ммиодесценд**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) .

Если не указать родительский фрагмент, текущее расположение файла должно находиться в начале фрагмента перед вызовом функции **ммиодесценд** . Если указать родительский фрагмент, текущее расположение файла может находиться в любом месте этого фрагмента.

Если поиск подфрагмента завершается неудачей, текущее расположение файла не определено. Вы можете использовать функцию [**ммиосик**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) и элемент **двдатаоффсет** структуры [**ммккинфо**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) , описывающие родительский блок, чтобы вернуться к началу родительского фрагмента, как показано в следующем примере:


```C++
mmioSeek(hmmio, mmckinfoParent.dwDataOffset + 4, SEEK_SET); 
```



Поскольку **двдатаоффсет** указывает смещение в начале части данных фрагмента, необходимо найти 4 байта после **двдатаоффсет** , чтобы задать положение файла после типа формы.

 

 