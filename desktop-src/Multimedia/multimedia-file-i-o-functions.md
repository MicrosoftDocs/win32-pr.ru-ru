---
title: Функции файлового ввода-вывода мультимедиа
description: Функции файлового ввода-вывода мультимедиа
ms.assetid: a5d51906-881f-4fe0-a988-c10776a3b40d
keywords:
- Мультимедиа Windows, функции файлового ввода-вывода
- мультимедиа, функции файлового ввода-вывода
- входные данные мультимедиа, функции файлового ввода-вывода
- операции файлового ввода-вывода мультимедиа, функции
- Ввод-вывод файлов, функции
- входные и выходные данные (ввод-вывод), функции
- Ввод-вывод (входные и выходные данные), функции
- Справочник по операциям файлового ввода-вывода мультимедиа, функции
- Справочник по операциям файлового ввода-вывода мультимедиа, функции
- Справочник по файлового ввода-вывода, функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b62b8daf8e84953acebcca9106165f27b350ef2f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533113"
---
# <a name="multimedia-file-io-functions"></a><span data-ttu-id="0301b-113">Функции файлового ввода-вывода мультимедиа</span><span class="sxs-lookup"><span data-stu-id="0301b-113">Multimedia File I/O Functions</span></span>

<span data-ttu-id="0301b-114">Для файлового ввода-вывода мультимедиа используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="0301b-114">The following functions are used with multimedia file I/O.</span></span>

-   <span data-ttu-id="0301b-115">[**иопрок**](/previous-versions//dd757098(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0301b-115">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span></span>
-   [<span data-ttu-id="0301b-116">**ммиоадванце**</span><span class="sxs-lookup"><span data-stu-id="0301b-116">**mmioAdvance**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [<span data-ttu-id="0301b-117">**ммиоасценд**</span><span class="sxs-lookup"><span data-stu-id="0301b-117">**mmioAscend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [<span data-ttu-id="0301b-118">**ммиоклосе**</span><span class="sxs-lookup"><span data-stu-id="0301b-118">**mmioClose**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [<span data-ttu-id="0301b-119">**ммиокреатечунк**</span><span class="sxs-lookup"><span data-stu-id="0301b-119">**mmioCreateChunk**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [<span data-ttu-id="0301b-120">**ммиодесценд**</span><span class="sxs-lookup"><span data-stu-id="0301b-120">**mmioDescend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [<span data-ttu-id="0301b-121">**ммиофлуш**</span><span class="sxs-lookup"><span data-stu-id="0301b-121">**mmioFlush**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [<span data-ttu-id="0301b-122">**ммиожетинфо**</span><span class="sxs-lookup"><span data-stu-id="0301b-122">**mmioGetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   [<span data-ttu-id="0301b-123">**ммиоинсталлиопрок**</span><span class="sxs-lookup"><span data-stu-id="0301b-123">**mmioInstallIOProc**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [<span data-ttu-id="0301b-124">**ммиупен**</span><span class="sxs-lookup"><span data-stu-id="0301b-124">**mmioOpen**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [<span data-ttu-id="0301b-125">**ммиореад**</span><span class="sxs-lookup"><span data-stu-id="0301b-125">**mmioRead**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [<span data-ttu-id="0301b-126">**ммиоренаме**</span><span class="sxs-lookup"><span data-stu-id="0301b-126">**mmioRename**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [<span data-ttu-id="0301b-127">**ммиосик**</span><span class="sxs-lookup"><span data-stu-id="0301b-127">**mmioSeek**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [<span data-ttu-id="0301b-128">**ммиосендмессаже**</span><span class="sxs-lookup"><span data-stu-id="0301b-128">**mmioSendMessage**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)
-   [<span data-ttu-id="0301b-129">**ммиосетбуффер**</span><span class="sxs-lookup"><span data-stu-id="0301b-129">**mmioSetBuffer**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [<span data-ttu-id="0301b-130">**ммиосетинфо**</span><span class="sxs-lookup"><span data-stu-id="0301b-130">**mmioSetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)
-   [<span data-ttu-id="0301b-131">**ммиострингтофауркк**</span><span class="sxs-lookup"><span data-stu-id="0301b-131">**mmioStringToFOURCC**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)
-   [<span data-ttu-id="0301b-132">**ммиоврите**</span><span class="sxs-lookup"><span data-stu-id="0301b-132">**mmioWrite**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="related-topics"></a><span data-ttu-id="0301b-133">См. также</span><span class="sxs-lookup"><span data-stu-id="0301b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0301b-134">Справочник по операциям файлового ввода-вывода мультимедиа</span><span class="sxs-lookup"><span data-stu-id="0301b-134">Multimedia File I/O Reference</span></span>](multimedia-file-i-o-reference.md)
</dt> </dl>

 

 