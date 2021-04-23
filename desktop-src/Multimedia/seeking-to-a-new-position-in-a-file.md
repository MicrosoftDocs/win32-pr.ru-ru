---
title: Поиск новой позицией в файле
description: Поиск новой позицией в файле
ms.assetid: 276c3e43-bf9f-4a0a-b33a-7eaa701e92a6
keywords:
- операции ввода-вывода файлов мультимедиа, перемещение в начало файлов
- Ввод-вывод файлов, перемещение в начало файлов
- Ввод и вывод (ввод-вывод), перемещение в начало файлов
- Ввод-вывод (ввод и вывод), перемещение в начало файлов
- Перемещение в начало файлов ввода-вывода
- Ввод-вывод файлов мультимедиа, поиск новых позиций в файлах
- Ввод-вывод файлов, поиск новой позицией в файлах
- Ввод и вывод (ввод-вывод), поиск новой позицией в файлах
- Ввод-вывод (ввод и вывод), поиск новой позицией в файлах
- Поиск новой должности в файлах ввода-вывода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 949ca3e9d118fdd83e5b53ae9336ad8ab601c64b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336857"
---
# <a name="seeking-to-a-new-position-in-a-file"></a><span data-ttu-id="2603d-113">Поиск новой позицией в файле</span><span class="sxs-lookup"><span data-stu-id="2603d-113">Seeking to a New Position in a File</span></span>

<span data-ttu-id="2603d-114">В следующем примере показано перемещение в начало открытого файла с помощью функции [**ммиосик**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) .</span><span class="sxs-lookup"><span data-stu-id="2603d-114">The following example moves to the beginning of an open file using the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function.</span></span>


```C++
mmioSeek(hFile, 0L, SEEK_SET); 
```



<span data-ttu-id="2603d-115">В следующем примере перемещается в конец открытого файла.</span><span class="sxs-lookup"><span data-stu-id="2603d-115">The following example moves to the end of an open file.</span></span>


```C++
mmioSeek(hFile, 0L, SEEK_END); 
```



<span data-ttu-id="2603d-116">В следующем примере перемещается в точку с 10 байтами из конца открытого файла.</span><span class="sxs-lookup"><span data-stu-id="2603d-116">The following example moves to a position 10 bytes from the end of an open file.</span></span>


```C++
mmioSeek(hFile, -10L, SEEK_END); 

```



 

 