---
title: Структура BG_JOB_PROGRESS (Deliveryoptimization. h)
description: Структура BG_JOB_PROGRESS предоставляет сведения о ходе выполнения, связанные с заданиями, такие как число переданных байтов и файлов. Для заданий отправки это состояние применяется к файлу отправки, а не к файлу ответов.
ms.assetid: F07BBDDE-FD34-4779-9E17-3789A8098616
keywords:
- Структура BG_JOB_PROGRESS
topic_type:
- apiref
api_name:
- BG_JOB_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e45c4a2833f80644ff763fc85a6846f9858fb3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534934"
---
# <a name="bg_job_progress-structure"></a><span data-ttu-id="1c1a9-105">Структура BG_JOB_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="1c1a9-105">BG_JOB_PROGRESS structure</span></span>

<span data-ttu-id="1c1a9-106">Структура **BG_JOB_PROGRESS** предоставляет сведения о ходе выполнения, связанные с заданиями, такие как число переданных байтов и файлов.</span><span class="sxs-lookup"><span data-stu-id="1c1a9-106">The **BG_JOB_PROGRESS** structure provides job-related progress information, such as the number of bytes and files transferred.</span></span> <span data-ttu-id="1c1a9-107">Для заданий отправки это состояние применяется к файлу отправки, а не к файлу ответов.</span><span class="sxs-lookup"><span data-stu-id="1c1a9-107">For upload jobs, the progress applies to the upload file, not the reply file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c1a9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c1a9-108">Syntax</span></span>


```C++
typedef struct _BG_JOB_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  ULONG  FilesTotal;
  ULONG  FilesTransferred;
} BG_JOB_PROGRESS;
```



## <a name="members"></a><span data-ttu-id="1c1a9-109">Члены</span><span class="sxs-lookup"><span data-stu-id="1c1a9-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="1c1a9-110">**BytesTotal**</span><span class="sxs-lookup"><span data-stu-id="1c1a9-110">**BytesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="1c1a9-111">Общее число байтов для пересылки для всех файлов в задании.</span><span class="sxs-lookup"><span data-stu-id="1c1a9-111">Total number of bytes to transfer for all files in the job.</span></span> <span data-ttu-id="1c1a9-112">Если значение равно BG_SIZE_UNKNOWN, общий размер всех файлов в задании не определен.</span><span class="sxs-lookup"><span data-stu-id="1c1a9-112">If the value is BG_SIZE_UNKNOWN, the total size of all files in the job has not been determined.</span></span> <span data-ttu-id="1c1a9-113">Не задавайте это значение, если не удается определить размер одного из файлов.</span><span class="sxs-lookup"><span data-stu-id="1c1a9-113">DO does not set this value if it cannot determine the size of one of the files.</span></span> <span data-ttu-id="1c1a9-114">Например, если указанный файл или сервер не существует, не удается определить размер файла.</span><span class="sxs-lookup"><span data-stu-id="1c1a9-114">For example, if the specified file or server does not exist, DO cannot determine the size of the file.</span></span>

<span data-ttu-id="1c1a9-115">При скачивании диапазонов из файла **битестотал** включает в себя общее число байтов, которое необходимо скачать из файла.</span><span class="sxs-lookup"><span data-stu-id="1c1a9-115">If you are downloading ranges from the file, **BytesTotal** includes the total number of bytes you want to download from the file.</span></span>

</dd> <dt>

<span data-ttu-id="1c1a9-116">**BytesTransferred**</span><span class="sxs-lookup"><span data-stu-id="1c1a9-116">**BytesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="1c1a9-117">Число переданных байтов.</span><span class="sxs-lookup"><span data-stu-id="1c1a9-117">Number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="1c1a9-118">**филестотал**</span><span class="sxs-lookup"><span data-stu-id="1c1a9-118">**FilesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="1c1a9-119">Общее число переносимых файлов для этого задания.</span><span class="sxs-lookup"><span data-stu-id="1c1a9-119">Total number of files to transfer for this job.</span></span>

</dd> <dt>

<span data-ttu-id="1c1a9-120">**филестрансферред**</span><span class="sxs-lookup"><span data-stu-id="1c1a9-120">**FilesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="1c1a9-121">Число переданных файлов.</span><span class="sxs-lookup"><span data-stu-id="1c1a9-121">Number of files transferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1c1a9-122">Требования</span><span class="sxs-lookup"><span data-stu-id="1c1a9-122">Requirements</span></span>



| <span data-ttu-id="1c1a9-123">Требование</span><span class="sxs-lookup"><span data-stu-id="1c1a9-123">Requirement</span></span> | <span data-ttu-id="1c1a9-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1c1a9-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c1a9-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c1a9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1c1a9-126">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="1c1a9-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1c1a9-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c1a9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1c1a9-128">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="1c1a9-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1c1a9-129">Header</span><span class="sxs-lookup"><span data-stu-id="1c1a9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c1a9-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c1a9-130"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c1a9-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c1a9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c1a9-132">**BG_FILE_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="1c1a9-132">**BG_FILE_PROGRESS**</span></span>](bg-file-progress.md)
</dt> <dt>

[<span data-ttu-id="1c1a9-133">**Использованием метода ibackgroundcopyjob:: Progress**</span><span class="sxs-lookup"><span data-stu-id="1c1a9-133">**IBackgroundCopyJob::GetProgress**</span></span>](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





