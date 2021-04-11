---
title: Создание фрагмента Metallica
description: Создание фрагмента Metallica
ms.assetid: d17f6215-f04f-4776-826e-eedb245f549b
keywords:
- файловый ввод-вывод с мультимедийными файлами, создание фрагмента Metallica
- Ввод-вывод файлов, создание фрагмента Metallica
- Ввод и вывод (I/O), создание фрагмента Metallica
- Ввод-вывод (входные и выходные данные), создание фрагмента Metallica
- Создание фрагмента Metallica
- Функция Ммиокреатечунк
- формат файла обмена ресурсами (Metallica)
- Metallica (формат файла обмена ресурсами)
- ВВОД-ВЫВОД METALLICA
- Фрагмент Metallica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca2cca96b45ecf0313f811b5df4e966be8fc0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890545"
---
# <a name="creating-a-riff-chunk"></a>Создание фрагмента Metallica

В следующем примере функция [**ммиокреатечунк**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) используется для создания фрагмента с идентификатором фрагмента "Metallica" и типом формы "рдиб".


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfo; 
. 
. 
. 
mmckinfo.fccType = mmioFOURCC('R', 'D', 'I', 'B'); 
mmioCreateChunk(hmmio, &mmckinfo, MMIO_CREATERIFF); 
```



При создании фрагмента "Metallica" или "LIST" необходимо указать тип формы или списка в элементе **фкктипе** структуры [**ммккинфо**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) . В предыдущем примере «РДИБ» — это тип формы.

Если вы знакомы с размером поля данных в новом фрагменте, можно задать элемент **кксизе** структуры **ммккинфо** при создании фрагмента. Это значение будет записано в поле Размер данных в новом фрагменте. Если это значение неверно при вызове [**ммиоасценд**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) для пометки конца фрагмента, он будет автоматически переписан для отражения правильного размера поля данных.

После создания фрагмента с помощью функции [**ммиокреатечунк**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) в качестве расположения файла устанавливается значение поля данных фрагмента (8 байт с начала фрагмента). Если фрагмент является блоком "Metallica" или "LIST", позиция файла устанавливается в расположение, следующее за типом или типом списка (12 байт с начала фрагмента).

 

 