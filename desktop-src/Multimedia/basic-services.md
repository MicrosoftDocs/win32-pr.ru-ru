---
title: Основные службы
description: Основные службы
ms.assetid: 7b77ed5d-0bd9-4926-b73f-afc7070fe314
keywords:
- файловый ввод-вывод мультимедиа, основные службы
- Ввод-вывод файлов, основные службы
- входные и выходные данные (ввод-вывод), базовые службы
- Ввод-вывод (входные и выходные данные), базовые службы
- Базовый ввод-вывод
- Функция Ммиупен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688dc6b96c612d94524758acce5d8c742fc13a36
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412923"
---
# <a name="basic-services"></a><span data-ttu-id="b4ee5-109">Основные службы</span><span class="sxs-lookup"><span data-stu-id="b4ee5-109">Basic Services</span></span>

<span data-ttu-id="b4ee5-110">Использование базовых служб ввода-вывода аналогично использованию служб ввода-вывода файлов среды выполнения в библиотеке времени выполнения C.</span><span class="sxs-lookup"><span data-stu-id="b4ee5-110">Using the basic I/O services is similar to using the run-time file I/O services of the C run-time library.</span></span> <span data-ttu-id="b4ee5-111">Для чтения или написания файлов их необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="b4ee5-111">Files must be opened before they can be read or written.</span></span> <span data-ttu-id="b4ee5-112">После чтения или записи файл должен быть закрыт.</span><span class="sxs-lookup"><span data-stu-id="b4ee5-112">After reading or writing, the file must be closed.</span></span> <span data-ttu-id="b4ee5-113">Можно также изменить текущее расположение чтения или записи в открытом файле.</span><span class="sxs-lookup"><span data-stu-id="b4ee5-113">You can also change the current read or write location within an open file.</span></span>

<span data-ttu-id="b4ee5-114">Перед началом операций ввода-вывода в файл необходимо открыть файл с помощью функции [**ммиупен**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .</span><span class="sxs-lookup"><span data-stu-id="b4ee5-114">Before you begin any I/O operations to a file, you must open the file by using the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="b4ee5-115">Эта функция возвращает файловый маркер типа **хммио**.</span><span class="sxs-lookup"><span data-stu-id="b4ee5-115">This function returns a file handle of type **HMMIO**.</span></span> <span data-ttu-id="b4ee5-116">Этот файл можно использовать для обнаружения открытого файла при вызове других функций файлового ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="b4ee5-116">You can use this file handle to identify the open file when calling other file I/O functions.</span></span>

> [!Note]  
> <span data-ttu-id="b4ee5-117">Описатель файла **хммио** не является стандартным маркером файла.</span><span class="sxs-lookup"><span data-stu-id="b4ee5-117">An **HMMIO** file handle is not a standard file handle.</span></span> <span data-ttu-id="b4ee5-118">Не используйте дескрипторы файлов **хммио** с функциями ввода-вывода в файлах времени выполнения Win32 или C.</span><span class="sxs-lookup"><span data-stu-id="b4ee5-118">Do not use **HMMIO** file handles with Win32 or C run-time file I/O functions.</span></span>

 

<span data-ttu-id="b4ee5-119">При использовании [**ммиупен**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) для открытия файла используется флаг, указывающий, следует ли открыть его для чтения, записи или и того, и другого.</span><span class="sxs-lookup"><span data-stu-id="b4ee5-119">When you use [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) to open a file, you use a flag to specify whether you are opening it for reading, writing, or both.</span></span> <span data-ttu-id="b4ee5-120">Можно также указать флаги, позволяющие создавать или удалять файлы.</span><span class="sxs-lookup"><span data-stu-id="b4ee5-120">You can also specify flags that enable you to create or delete a file.</span></span> <span data-ttu-id="b4ee5-121">Используйте функцию [**ммиоклосе**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) , чтобы закрыть файл по завершении чтения или записи в него.</span><span class="sxs-lookup"><span data-stu-id="b4ee5-121">Use the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function to close a file when you are finished reading or writing to it.</span></span>

<span data-ttu-id="b4ee5-122">Для чтения и записи файлов можно использовать функции [**ммиореад**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) и [**ммиоврите**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) соответственно.</span><span class="sxs-lookup"><span data-stu-id="b4ee5-122">You can read and write files by using the [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) and [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) functions respectively.</span></span> <span data-ttu-id="b4ee5-123">Следующая операция чтения или записи выполняется в текущем положении файла или в указателе файла в файле.</span><span class="sxs-lookup"><span data-stu-id="b4ee5-123">The next read or write operation occurs at the current file position or file pointer in a file.</span></span> <span data-ttu-id="b4ee5-124">Текущее расположение файла является расширенным при каждом чтении или написании файла.</span><span class="sxs-lookup"><span data-stu-id="b4ee5-124">The current file position is advanced each time a file is read or written.</span></span>

<span data-ttu-id="b4ee5-125">Вы также можете изменить текущее расположение файла с помощью функции [**ммиосик**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) .</span><span class="sxs-lookup"><span data-stu-id="b4ee5-125">You can also change the current file position by using the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function.</span></span> <span data-ttu-id="b4ee5-126">Необходимо убедиться, что указано допустимое расположение в файле.</span><span class="sxs-lookup"><span data-stu-id="b4ee5-126">You should ensure that you specify a valid location in a file.</span></span> <span data-ttu-id="b4ee5-127">Если указать недопустимое расположение, например, после конца файла, **ммиосик** может не вернуть ошибку, но последующие операции ввода-вывода могут завершиться ошибкой.</span><span class="sxs-lookup"><span data-stu-id="b4ee5-127">If you specify an invalid location, such as past the end of the file, **mmioSeek** may not return an error, but subsequent I/O operations could fail.</span></span>

<span data-ttu-id="b4ee5-128">Существуют флаги, которые можно использовать с функцией **ммиупен** для операций за пределами обычного файлового ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="b4ee5-128">There are flags you can use with the **mmioOpen** function for operations beyond basic file I/O.</span></span> <span data-ttu-id="b4ee5-129">Если указать структуру [**ммиоинфо**](/previous-versions//dd757322(v=vs.85)) , можно открыть файлы памяти, указать пользовательскую процедуру ввода-вывода или указать буфер для буферизованного ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="b4ee5-129">By specifying an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure, for example, you can open memory files, specify a custom I/O procedure, or supply a buffer for buffered I/O.</span></span>

 

 