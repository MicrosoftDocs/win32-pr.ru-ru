---
title: Открытие файла с помощью Ммиупен
description: Открытие файла с помощью Ммиупен
ms.assetid: 947d1b1c-ec00-4bd9-948a-4b8e3bfb84f6
keywords:
- Ввод-вывод файлов мультимедиа, открытие файлов
- Ввод-вывод файлов, открытие файлов
- входные и выходные данные (ввод-вывод), открытие файлов
- Ввод-вывод (входные и выходные данные), открытие файлов
- файловый ввод-вывод, функция Ммиупен
- файловый ввод-вывод, функция Ммиупен
- входные и выходные данные (ввод-вывод), функция Ммиупен
- Ввод-вывод (входные и выходные данные), функция Ммиупен
- Функция Ммиупен
- Открытие файлов ввода-вывода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2123b73c5f3a93cbb6e72711a7137652f7534b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487697"
---
# <a name="opening-a-file-with-mmioopen"></a><span data-ttu-id="6200a-113">Открытие файла с помощью Ммиупен</span><span class="sxs-lookup"><span data-stu-id="6200a-113">Opening a File with mmioOpen</span></span>

<span data-ttu-id="6200a-114">Чтобы открыть файл для базовых операций ввода-вывода, установите для параметра *лпммиоинфо* функции [**ммиупен**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6200a-114">To open a file for basic I/O operations, set the *lpmmioinfo* parameter of the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function to **NULL**.</span></span> <span data-ttu-id="6200a-115">В следующем примере открывается файл с именем «C: \\ samples \\SAMPLE1.TXT» для чтения и проверяется возвращаемое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="6200a-115">The following example opens a file named "C:\\SAMPLES\\SAMPLE1.TXT" for reading, and checks the return value for error.</span></span>


```C++
HMMIO hFile; 

if ((hFile = mmioOpen("C:\\SAMPLES\\SAMPLE1.TXT", NULL, 
    MMIO_READ)) != NULL) 
    // File opened successfully. 
else 
    // File cannot be opened. 
```



<span data-ttu-id="6200a-116">Используйте параметр *dwFlags* параметра **ммиупен** , чтобы задать флаги для открытия файла.</span><span class="sxs-lookup"><span data-stu-id="6200a-116">Use the *dwFlags* parameter of **mmioOpen** to specify flags for opening a file.</span></span>

 

 