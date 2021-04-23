---
title: Справочник по операциям файлового ввода-вывода мультимедиа
description: Справочник по операциям файлового ввода-вывода мультимедиа
ms.assetid: 1f24432e-7407-4b97-80ab-0a0c40c09253
keywords:
- Windows мультимедиа, Справочник по файловым операциям ввода-вывода
- мультимедиа, Справочник по файловым операциям ввода-вывода
- входные данные мультимедиа, Справочник по файлового ввода-вывода
- Ввод-вывод файлов мультимедиа, Справочник
- файловый ввод-вывод, Справочник
- Ввод и вывод (ввод-вывод), Справочник
- Ввод-вывод (входные и выходные данные), Справочник
- Справочник по файловым операциям ввода-вывода мультимедиа, о
- Справочник по файловым операциям ввода-вывода мультимедиа, сведения
- Справочник по файлового ввода-вывода, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0f833b7fb6677e064c19897e276d3961038cfc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789763"
---
# <a name="multimedia-file-io-reference"></a><span data-ttu-id="94473-113">Справочник по операциям файлового ввода-вывода мультимедиа</span><span class="sxs-lookup"><span data-stu-id="94473-113">Multimedia File I/O Reference</span></span>

<span data-ttu-id="94473-114">В этом разделе описываются функции, макросы, сообщения и структуры, связанные с входными и выходными файлами мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="94473-114">This section describes the functions, macros, messages, and structures associated with multimedia file input and output.</span></span> <span data-ttu-id="94473-115">Эти элементы группируются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="94473-115">These elements are grouped as follows.</span></span>

## <a name="basic-io"></a><span data-ttu-id="94473-116">Базовый ввод-вывод</span><span class="sxs-lookup"><span data-stu-id="94473-116">Basic I/O</span></span>

-   [<span data-ttu-id="94473-117">**ммиоклосе**</span><span class="sxs-lookup"><span data-stu-id="94473-117">**mmioClose**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [<span data-ttu-id="94473-118">**ммиупен**</span><span class="sxs-lookup"><span data-stu-id="94473-118">**mmioOpen**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [<span data-ttu-id="94473-119">**ммиореад**</span><span class="sxs-lookup"><span data-stu-id="94473-119">**mmioRead**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [<span data-ttu-id="94473-120">**ммиоренаме**</span><span class="sxs-lookup"><span data-stu-id="94473-120">**mmioRename**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [<span data-ttu-id="94473-121">**ммиосик**</span><span class="sxs-lookup"><span data-stu-id="94473-121">**mmioSeek**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [<span data-ttu-id="94473-122">**ммиоврите**</span><span class="sxs-lookup"><span data-stu-id="94473-122">**mmioWrite**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="buffered-io"></a><span data-ttu-id="94473-123">Буферизованный ввод-вывод</span><span class="sxs-lookup"><span data-stu-id="94473-123">Buffered I/O</span></span>

-   [<span data-ttu-id="94473-124">**ммиоадванце**</span><span class="sxs-lookup"><span data-stu-id="94473-124">**mmioAdvance**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [<span data-ttu-id="94473-125">**ммиофлуш**</span><span class="sxs-lookup"><span data-stu-id="94473-125">**mmioFlush**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [<span data-ttu-id="94473-126">**ммиожетинфо**</span><span class="sxs-lookup"><span data-stu-id="94473-126">**mmioGetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   <span data-ttu-id="94473-127">[**ммиоинфо**](/previous-versions//dd757322(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="94473-127">[**MMIOINFO**](/previous-versions//dd757322(v=vs.85))</span></span>
-   [<span data-ttu-id="94473-128">**ммиосетбуффер**</span><span class="sxs-lookup"><span data-stu-id="94473-128">**mmioSetBuffer**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [<span data-ttu-id="94473-129">**ммиосетинфо**</span><span class="sxs-lookup"><span data-stu-id="94473-129">**mmioSetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)

## <a name="riff-io"></a><span data-ttu-id="94473-130">ВВОД-ВЫВОД METALLICA</span><span class="sxs-lookup"><span data-stu-id="94473-130">RIFF I/O</span></span>

-   [<span data-ttu-id="94473-131">**ммиоасценд**</span><span class="sxs-lookup"><span data-stu-id="94473-131">**mmioAscend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [<span data-ttu-id="94473-132">**ммккинфо**</span><span class="sxs-lookup"><span data-stu-id="94473-132">**MMCKINFO**</span></span>](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo)
-   [<span data-ttu-id="94473-133">**ммиокреатечунк**</span><span class="sxs-lookup"><span data-stu-id="94473-133">**mmioCreateChunk**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [<span data-ttu-id="94473-134">**ммиодесценд**</span><span class="sxs-lookup"><span data-stu-id="94473-134">**mmioDescend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [<span data-ttu-id="94473-135">**ммиофауркк**</span><span class="sxs-lookup"><span data-stu-id="94473-135">**mmioFOURCC**</span></span>](/windows/win32/api/vfw/nf-vfw-mmiofourcc)
-   [<span data-ttu-id="94473-136">**ммиострингтофауркк**</span><span class="sxs-lookup"><span data-stu-id="94473-136">**mmioStringToFOURCC**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)

## <a name="custom-io-procedures"></a><span data-ttu-id="94473-137">Пользовательские процедуры ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="94473-137">Custom I/O Procedures</span></span>

-   <span data-ttu-id="94473-138">[**иопрок**](/previous-versions//dd757098(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="94473-138">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span></span>
-   [<span data-ttu-id="94473-139">**ммиоинсталлиопрок**</span><span class="sxs-lookup"><span data-stu-id="94473-139">**mmioInstallIOProc**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [<span data-ttu-id="94473-140">**ММИОМ \_ Закрыть**</span><span class="sxs-lookup"><span data-stu-id="94473-140">**MMIOM\_CLOSE**</span></span>](mmiom-close.md)
-   [<span data-ttu-id="94473-141">**ММИОМ \_ Открыть**</span><span class="sxs-lookup"><span data-stu-id="94473-141">**MMIOM\_OPEN**</span></span>](mmiom-open.md)
-   [<span data-ttu-id="94473-142">**ММИОМ \_ чтение**</span><span class="sxs-lookup"><span data-stu-id="94473-142">**MMIOM\_READ**</span></span>](mmiom-read.md)
-   [<span data-ttu-id="94473-143">**\_Переименование ммиом**</span><span class="sxs-lookup"><span data-stu-id="94473-143">**MMIOM\_RENAME**</span></span>](mmiom-rename.md)
-   [<span data-ttu-id="94473-144">**ММИОМ \_ Поиск**</span><span class="sxs-lookup"><span data-stu-id="94473-144">**MMIOM\_SEEK**</span></span>](mmiom-seek.md)
-   [<span data-ttu-id="94473-145">**ММИОМ \_ запись**</span><span class="sxs-lookup"><span data-stu-id="94473-145">**MMIOM\_WRITE**</span></span>](mmiom-write.md)
-   [<span data-ttu-id="94473-146">**ММИОМ \_ вритефлуш**</span><span class="sxs-lookup"><span data-stu-id="94473-146">**MMIOM\_WRITEFLUSH**</span></span>](mmiom-writeflush.md)
-   [<span data-ttu-id="94473-147">**ммиосендмессаже**</span><span class="sxs-lookup"><span data-stu-id="94473-147">**mmioSendMessage**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)

## <a name="related-topics"></a><span data-ttu-id="94473-148">См. также</span><span class="sxs-lookup"><span data-stu-id="94473-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94473-149">Файловый ввод-вывод мультимедиа</span><span class="sxs-lookup"><span data-stu-id="94473-149">Multimedia File I/O</span></span>](multimedia-file-i-o.md)
</dt> </dl>

 

 