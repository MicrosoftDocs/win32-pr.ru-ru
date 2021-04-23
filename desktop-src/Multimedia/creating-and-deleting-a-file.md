---
title: Создание и удаление файла
description: Создание и удаление файла
ms.assetid: a4b4a310-7230-4f1d-b084-c47db39adaac
keywords:
- Ввод-вывод файлов мультимедиа, создание файлов
- Ввод-вывод файлов, создание файлов
- входные и выходные данные (ввод-вывод), создание файлов
- Ввод-вывод (входные и выходные данные), создание файлов
- Создание файлов ввода-вывода
- операции ввода-вывода файлов мультимедиа, удаление файлов
- Ввод-вывод файлов, удаление файлов
- Ввод и вывод (ввод-вывод), удаление файлов
- Ввод-вывод (входные и выходные данные), удаление файлов
- Удаление файлов ввода-вывода
- Функция Ммиупен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c22cd6330874d0b5da74d69193359c025c709c79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790177"
---
# <a name="creating-and-deleting-a-file"></a><span data-ttu-id="2f004-114">Создание и удаление файла</span><span class="sxs-lookup"><span data-stu-id="2f004-114">Creating and Deleting a File</span></span>

<span data-ttu-id="2f004-115">Чтобы создать файл, присвойте параметру *двопенфлагс* функции [**ммиупен**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) значение MMIO \_ Create.</span><span class="sxs-lookup"><span data-stu-id="2f004-115">To create a file, set the *dwOpenFlags* parameter of the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function to MMIO\_CREATE.</span></span> <span data-ttu-id="2f004-116">В следующем примере создается файл, который открывается для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="2f004-116">The following example creates a file and opens it for reading and writing.</span></span>


```C++
HMMIO hFile; 

hFile = mmioOpen("NEWFILE.TXT", NULL, MMIO_CREATE | MMIO_READWRITE); 
if (hFile != NULL) 
    // File created successfully. 
else 
    // File cannot be created. 
```



<span data-ttu-id="2f004-117">Если создаваемый файл уже существует, он будет обрезан до нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="2f004-117">If the file you are creating already exists, it will be truncated to zero length.</span></span>

<span data-ttu-id="2f004-118">Чтобы удалить файл, присвойте параметру *двопенфлагс* функции **ммиупен** значение MMIO \_ Delete.</span><span class="sxs-lookup"><span data-stu-id="2f004-118">To delete a file, set the *dwOpenFlags* parameter of the **mmioOpen** function to MMIO\_DELETE.</span></span> <span data-ttu-id="2f004-119">После удаления файла его нельзя восстановить с помощью стандартных средств.</span><span class="sxs-lookup"><span data-stu-id="2f004-119">After you delete a file, it cannot be recovered by any standard means.</span></span> <span data-ttu-id="2f004-120">Если приложение удаляет файл по запросу пользователя, запросите пользователя перед удалением файла, чтобы убедиться, что пользователь хочет его удалить.</span><span class="sxs-lookup"><span data-stu-id="2f004-120">If your application is deleting a file at the request of a user, query the user before deleting the file to make sure the user wants to delete it.</span></span>

 

 