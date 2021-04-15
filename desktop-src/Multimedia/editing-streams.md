---
title: Изменение потоков
description: Изменение потоков
ms.assetid: 1653ff90-e96a-43fc-b509-6d8ad4ddcd2c
keywords:
- Функция Креатидитаблестреам
- Функция Едитстреамкут
- Функция Едитстреамкопи
- Функция Едитстреампасте
- Функция Едитстреамклоне
- Функция Едитстреамсетинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29eb687eb36ff9dfe0b1d3477bff095bdd78a135
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486893"
---
# <a name="editing-streams"></a><span data-ttu-id="5287f-109">Изменение потоков</span><span class="sxs-lookup"><span data-stu-id="5287f-109">Editing Streams</span></span>

<span data-ttu-id="5287f-110">Можно создать поток, который можно изменить с помощью функции [**креатидитаблестреам**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) .</span><span class="sxs-lookup"><span data-stu-id="5287f-110">You can create a stream that you can edit by using the [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) function.</span></span> <span data-ttu-id="5287f-111">Эта функция инициализирует среду для редактирования потока.</span><span class="sxs-lookup"><span data-stu-id="5287f-111">This function initializes the environment for editing a stream.</span></span> <span data-ttu-id="5287f-112">Это включает в себя создание интерфейса для нового потока, а также внутренние таблицы редактирования, которые отписывают изменения, внесенные в поток.</span><span class="sxs-lookup"><span data-stu-id="5287f-112">This includes creating an interface to the new stream, and internal edit tables that track changes made to the stream.</span></span> <span data-ttu-id="5287f-113">**Креатидитаблестреам** возвращает указатель потока на редактируемый поток, необходимый другим функциям редактирования потока.</span><span class="sxs-lookup"><span data-stu-id="5287f-113">**CreateEditableStream** returns a stream pointer to an editable stream that is required by other stream-editing functions.</span></span> <span data-ttu-id="5287f-114">Изменяемый указатель потока также может использоваться другими функциями Авифиле, принимающими указатели потоков.</span><span class="sxs-lookup"><span data-stu-id="5287f-114">The editable stream pointer can also be used by other AVIFile functions that accept stream pointers.</span></span>

<span data-ttu-id="5287f-115">Можно вырезать один или несколько выборок из редактируемого потока с помощью функции [**едитстреамкут**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) .</span><span class="sxs-lookup"><span data-stu-id="5287f-115">You can cut one or more samples from an editable stream by using the [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) function.</span></span> <span data-ttu-id="5287f-116">Чтобы удалить образцы из редактируемого потока, эта функция добавляет запись в таблицу редактирования.</span><span class="sxs-lookup"><span data-stu-id="5287f-116">To remove samples from the editable stream, this function adds an entry to the edit table.</span></span> <span data-ttu-id="5287f-117">Затем функция помещает копию примеров вырезания в новый временный поток, указатель интерфейса которого возвращается в переменной.</span><span class="sxs-lookup"><span data-stu-id="5287f-117">The function then places a copy of the cut samples in a new temporary stream whose interface pointer is returned in a variable.</span></span>

<span data-ttu-id="5287f-118">Можно скопировать один или несколько выборок из редактируемого потока во временный поток с помощью функции [**едитстреамкопи**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) .</span><span class="sxs-lookup"><span data-stu-id="5287f-118">You can copy one or more samples from an editable stream into a temporary stream by using the [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) function.</span></span> <span data-ttu-id="5287f-119">**Едитстреамкопи** помещает копии образцов в новый временный поток, указатель интерфейса которого возвращается в переменной.</span><span class="sxs-lookup"><span data-stu-id="5287f-119">**EditStreamCopy** places copies of the samples in a new temporary stream whose interface pointer is returned in a variable.</span></span>

<span data-ttu-id="5287f-120">Можно скопировать один или несколько выборок из потока и вставить их в изменяемый поток с помощью функции [**едитстреампасте**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) .</span><span class="sxs-lookup"><span data-stu-id="5287f-120">You can copy one or more samples from a stream and paste them into an editable stream by using the [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) function.</span></span> <span data-ttu-id="5287f-121">Чтобы вставить образцы в указанную точку, эта функция добавляет запись в таблицу редактирования целевого редактируемого потока.</span><span class="sxs-lookup"><span data-stu-id="5287f-121">To insert the samples at the specified position, this function adds an entry in the edit table of the target editable stream.</span></span>

<span data-ttu-id="5287f-122">Можно дублировать редактируемый поток с помощью функции [**едитстреамклоне**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) .</span><span class="sxs-lookup"><span data-stu-id="5287f-122">You can duplicate an editable stream by using the [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) function.</span></span> <span data-ttu-id="5287f-123">Эта функция возвращает указатель на интерфейс потока нового потока.</span><span class="sxs-lookup"><span data-stu-id="5287f-123">This function returns a pointer to the stream interface of the new stream.</span></span> <span data-ttu-id="5287f-124">Вы можете скопировать эти потоки в буфер обмена или использовать их для сохранения изменений, внесенных в поток.</span><span class="sxs-lookup"><span data-stu-id="5287f-124">You can copy these streams to the clipboard or use them to maintain a trail of edits made to a stream.</span></span>

<span data-ttu-id="5287f-125">Можно изменить некоторые характеристики редактируемого потока с помощью функции [**едитстреамсетинфо**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) .</span><span class="sxs-lookup"><span data-stu-id="5287f-125">You can change several of the characteristics of an editable stream by using the [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) function.</span></span> <span data-ttu-id="5287f-126">Эта функция обновляет значение приоритета, язык, масштаб и скорость, время начала, параметр качества, размеры прямоугольника назначения и координаты, а также текстовое описание потока.</span><span class="sxs-lookup"><span data-stu-id="5287f-126">This function updates the priority setting, language, scale and rate, starting time, quality setting, destination rectangle dimensions and coordinates, and the textual description of the stream.</span></span> <span data-ttu-id="5287f-127">Эти элементы хранятся в структуре [**авистреаминфо**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) , связанной с редактируемым потоком.</span><span class="sxs-lookup"><span data-stu-id="5287f-127">These items are stored in the [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) structure associated with the editable stream.</span></span>

<span data-ttu-id="5287f-128">Также можно изменить текстовое описание редактируемого потока с помощью функции [**едитстреамсетнаме**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) .</span><span class="sxs-lookup"><span data-stu-id="5287f-128">You can also change the textual description of an editable stream by using the [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) function.</span></span> <span data-ttu-id="5287f-129">Эта функция обновляет член **szName** структуры **авистреаминфо** , связанной с изменяемым потоком.</span><span class="sxs-lookup"><span data-stu-id="5287f-129">This function updates the **szName** member of the **AVISTREAMINFO** structure associated with the editable stream.</span></span>

<span data-ttu-id="5287f-130">Функции редактирования работают с потоками.</span><span class="sxs-lookup"><span data-stu-id="5287f-130">The editing functions work on streams.</span></span> <span data-ttu-id="5287f-131">Необходимо вырезать и вставить каждый поток по отдельности, а затем использовать функцию [**авимакефилефромстреамс**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) для создания нового указателя файла.</span><span class="sxs-lookup"><span data-stu-id="5287f-131">You need to cut and paste each stream individually, and then use the [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) function to create a new file pointer.</span></span>

> [!Note]  
> <span data-ttu-id="5287f-132">Таблицы редактирования в редактируемом потоке сохраняют все изменения для потока.</span><span class="sxs-lookup"><span data-stu-id="5287f-132">The edit tables in an editable stream maintain all the changes for a stream.</span></span> <span data-ttu-id="5287f-133">Исходный поток никогда не изменяется.</span><span class="sxs-lookup"><span data-stu-id="5287f-133">The source stream is never changed.</span></span>

 

 

 




