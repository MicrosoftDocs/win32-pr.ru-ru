---
title: Структура BG_FILE_PROGRESS (Deliveryoptimization. h)
description: Структура BG_FILE_PROGRESS предоставляет сведения о ходе выполнения, связанные с файлами, например число переданных байтов.
ms.assetid: 49BDFEEE-D7BF-489A-8BC1-951549B06252
keywords:
- Структура BG_FILE_PROGRESS
topic_type:
- apiref
api_name:
- BG_FILE_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 93507b8aeefa9c0ea16f70f67e221ecc4218427f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803299"
---
# <a name="bg_file_progress-structure"></a><span data-ttu-id="44037-104">Структура BG_FILE_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="44037-104">BG_FILE_PROGRESS structure</span></span>

<span data-ttu-id="44037-105">Структура **BG_FILE_PROGRESS** предоставляет сведения о ходе выполнения, связанные с файлами, например число переданных байтов.</span><span class="sxs-lookup"><span data-stu-id="44037-105">The **BG_FILE_PROGRESS** structure provides file-related progress information, such as the number of bytes transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="44037-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44037-106">Syntax</span></span>


```C++
typedef struct _BG_FILE_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  BOOL   Completed;
} BG_FILE_PROGRESS;
```



## <a name="members"></a><span data-ttu-id="44037-107">Члены</span><span class="sxs-lookup"><span data-stu-id="44037-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="44037-108">**BytesTotal**</span><span class="sxs-lookup"><span data-stu-id="44037-108">**BytesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="44037-109">Размер файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="44037-109">Size of the file in bytes.</span></span> <span data-ttu-id="44037-110">Если не удается определить размер файла (например, если файл или сервер не существует), значение DO_UNKNOWN_FILE_SIZE.</span><span class="sxs-lookup"><span data-stu-id="44037-110">If DO cannot determine the size of the file (for example, if the file or server does not exist), the value is DO_UNKNOWN_FILE_SIZE.</span></span>

<span data-ttu-id="44037-111">Если вы скачиваете диапазоны из файла, **битестотал** отражает общее число байтов, которое необходимо скачать из файла.</span><span class="sxs-lookup"><span data-stu-id="44037-111">If you are downloading ranges from a file, **BytesTotal** reflects the total number of bytes you want to download from the file.</span></span>

</dd> <dt>

<span data-ttu-id="44037-112">**BytesTransferred**</span><span class="sxs-lookup"><span data-stu-id="44037-112">**BytesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="44037-113">Число переданных байтов.</span><span class="sxs-lookup"><span data-stu-id="44037-113">Number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="44037-114">**Завершено**</span><span class="sxs-lookup"><span data-stu-id="44037-114">**Completed**</span></span>
</dt> <dd>

<span data-ttu-id="44037-115">Для загрузки значение равно **true** , если файл доступен пользователю; в противном случае значение равно **false**.</span><span class="sxs-lookup"><span data-stu-id="44037-115">For downloads, the value is **TRUE** if the file is available to the user; otherwise, the value is **FALSE**.</span></span> <span data-ttu-id="44037-116">Файлы доступны пользователю после вызова метода [**использованием метода ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="44037-116">Files are available to the user after calling the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span> <span data-ttu-id="44037-117">Если метод **Complete** создает временную ошибку, то эти файлы, обработанные до возникновения ошибки, становятся доступными для пользователя. другие — нет.</span><span class="sxs-lookup"><span data-stu-id="44037-117">If the **Complete** method generates a transient error, those files processed before the error occurred are available to the user; the others are not.</span></span> <span data-ttu-id="44037-118">Используйте **завершенный** член, чтобы определить, доступен ли файл пользователю при сбое **завершения** .</span><span class="sxs-lookup"><span data-stu-id="44037-118">Use the **Completed** member to determine if the file is available to the user when **Complete** fails.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44037-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44037-119">Remarks</span></span>

<span data-ttu-id="44037-120">Чтобы определить, передавался ли файл, можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="44037-120">To determine if DO transferred the file, you can:</span></span>

-   <span data-ttu-id="44037-121">Сравните **BytesTransferred** с **битестотал**.</span><span class="sxs-lookup"><span data-stu-id="44037-121">Compare **BytesTransferred** to **BytesTotal**.</span></span>

## <a name="requirements"></a><span data-ttu-id="44037-122">Требования</span><span class="sxs-lookup"><span data-stu-id="44037-122">Requirements</span></span>



| <span data-ttu-id="44037-123">Требование</span><span class="sxs-lookup"><span data-stu-id="44037-123">Requirement</span></span> | <span data-ttu-id="44037-124">Значение</span><span class="sxs-lookup"><span data-stu-id="44037-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44037-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44037-125">Minimum supported client</span></span><br/> | <span data-ttu-id="44037-126">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="44037-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="44037-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44037-127">Minimum supported server</span></span><br/> | <span data-ttu-id="44037-128">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="44037-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="44037-129">Header</span><span class="sxs-lookup"><span data-stu-id="44037-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="44037-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="44037-130"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44037-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44037-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44037-132">**BG_JOB_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="44037-132">**BG_JOB_PROGRESS**</span></span>](bg-job-progress.md)
</dt> <dt>

[<span data-ttu-id="44037-133">**Ибаккграундкопифиле:: Progress**</span><span class="sxs-lookup"><span data-stu-id="44037-133">**IBackgroundCopyFile::GetProgress**</span></span>](ibackgroundcopyfile-getprogress-method.md)
</dt> </dl>

 

 





