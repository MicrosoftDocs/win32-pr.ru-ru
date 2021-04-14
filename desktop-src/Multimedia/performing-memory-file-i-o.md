---
title: Выполнение файлового ввода-вывода в памяти
description: Выполнение файлового ввода-вывода в памяти
ms.assetid: c0a5c8a0-978f-47d9-8ef0-ad391b9d1e63
keywords:
- файловый ввод-вывод в формате мультимедиа, память
- файловый ввод-вывод, память
- входные и выходные данные (ввод-вывод), память
- Ввод-вывод (входные и выходные данные), память
- Ввод-вывод в память
- Функция Ммиупен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c3e98bbd3636fb88c834957ba2c3fb856406a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487537"
---
# <a name="performing-memory-file-io"></a><span data-ttu-id="e4fc8-109">Выполнение файлового ввода-вывода в памяти</span><span class="sxs-lookup"><span data-stu-id="e4fc8-109">Performing Memory File I/O</span></span>

<span data-ttu-id="e4fc8-110">Службы файлового ввода-вывода позволяют обрабатывать блок памяти как файл.</span><span class="sxs-lookup"><span data-stu-id="e4fc8-110">The multimedia file I/O services let you treat a block of memory as a file.</span></span> <span data-ttu-id="e4fc8-111">Это может быть полезно, если в памяти уже имеется образ файла.</span><span class="sxs-lookup"><span data-stu-id="e4fc8-111">This can be useful if you already have a file image in memory.</span></span> <span data-ttu-id="e4fc8-112">Файлы памяти позволяют сократить количество особых условий в коде, поскольку для операций ввода-вывода файлы памяти можно рассматривать как файлы на диске.</span><span class="sxs-lookup"><span data-stu-id="e4fc8-112">Memory files let you reduce the number of special-case conditions in your code because, for I/O purposes, you can treat memory files as if they were disk-based files.</span></span> <span data-ttu-id="e4fc8-113">Также можно использовать файлы памяти с буфером обмена.</span><span class="sxs-lookup"><span data-stu-id="e4fc8-113">You can also use memory files with the clipboard.</span></span>

<span data-ttu-id="e4fc8-114">Как и в случае с буферами ввода-вывода, файлы памяти могут использовать память, выделенную приложением или диспетчером файлового ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="e4fc8-114">As with I/O buffers, memory files can use memory allocated by the application or by the file I/O manager.</span></span> <span data-ttu-id="e4fc8-115">Кроме того, файлы памяти могут быть расширяемыми или нерасширяемыми.</span><span class="sxs-lookup"><span data-stu-id="e4fc8-115">In addition, memory files can be either expandable or nonexpandable.</span></span> <span data-ttu-id="e4fc8-116">Когда файловый диспетчер ввода-вывода достигает конца расширяемого файла памяти, он разворачивает файл памяти по заранее определенному инкременту.</span><span class="sxs-lookup"><span data-stu-id="e4fc8-116">When the file I/O manager reaches the end of an expandable memory file, it expands the memory file by a predefined increment.</span></span>

<span data-ttu-id="e4fc8-117">Чтобы открыть файл памяти, используйте функцию [**ммиупен**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) с параметром *сзфиленаме* , для которого установлено **значение NULL** , и \_ флаг MMIO ReadWrite, установленный в параметре *двопенфлагс* .</span><span class="sxs-lookup"><span data-stu-id="e4fc8-117">To open a memory file, use the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function with the *szFilename* parameter set to **NULL** and the MMIO\_READWRITE flag set in the *dwOpenFlags* parameter.</span></span> <span data-ttu-id="e4fc8-118">Задайте параметр *лпммиоинфо* , чтобы он указывал на структуру [**ммиоинфо**](/previous-versions//dd757322(v=vs.85)) , которая была настроена следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e4fc8-118">Set the *lpmmioinfo* parameter to point to an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure that has been set up as follows:</span></span>

1.  <span data-ttu-id="e4fc8-119">Установите для элемента **Пиопрок** **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e4fc8-119">Set the **pIOProc** member to **NULL**.</span></span>
2.  <span data-ttu-id="e4fc8-120">Установите для элемента **фкЦиопрок** значение FOURCC \_ MEM.</span><span class="sxs-lookup"><span data-stu-id="e4fc8-120">Set the **fccIOProc** member to FOURCC\_MEM.</span></span>
3.  <span data-ttu-id="e4fc8-121">Установите элемент **пчбуффер** , чтобы он указывал на блок памяти.</span><span class="sxs-lookup"><span data-stu-id="e4fc8-121">Set the **pchBuffer** member to point to the memory block.</span></span> <span data-ttu-id="e4fc8-122">Чтобы запросить, что диспетчер файлового ввода-вывода выделяет блок памяти, установите  для Пчбуффер **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e4fc8-122">To request that the file I/O manager allocate the memory block, set **pchBuffer** to **NULL**.</span></span>
4.  <span data-ttu-id="e4fc8-123">Задайте для элемента **кчбуффер** начальный размер блока памяти.</span><span class="sxs-lookup"><span data-stu-id="e4fc8-123">Set the **cchBuffer** member to the initial size of the memory block.</span></span>
5.  <span data-ttu-id="e4fc8-124">Задайте для элемента **адвинфо** минимальный размер расширения блока памяти.</span><span class="sxs-lookup"><span data-stu-id="e4fc8-124">Set the **adwInfo** member to the minimum expansion size of the memory block.</span></span> <span data-ttu-id="e4fc8-125">Для нерасширяемого файла памяти задайте для **Адвинфо** **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e4fc8-125">For a nonexpandable memory file, set **adwInfo** to **NULL**.</span></span>
6.  <span data-ttu-id="e4fc8-126">Задайте для всех остальных элементов нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="e4fc8-126">Set all other members to zero.</span></span>

<span data-ttu-id="e4fc8-127">Не существует ограничений на выделение памяти для использования в качестве нерасширяемого файла памяти.</span><span class="sxs-lookup"><span data-stu-id="e4fc8-127">There are no restrictions on allocating memory for use as a nonexpandable memory file.</span></span>

 

 