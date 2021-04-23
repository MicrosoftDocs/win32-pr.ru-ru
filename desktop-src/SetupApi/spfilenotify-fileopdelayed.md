---
description: Уведомление СПФИЛЕНОТИФИ \_ филеопделайед отправляется сетупинсталлфиликс или сетупкоммитфилекуеуе в подпрограммы обратного вызова, когда файл был отложен, так как файл уже используется. Операция будет обработана при следующей перезагрузке системы.
ms.assetid: a0b38e2b-2390-49e5-b288-77c31636e696
title: Сообщение SPFILENOTIFY_FILEOPDELAYED (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38975506ff998ec09c4549ec95d9ddb620466cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908811"
---
# <a name="spfilenotify_fileopdelayed-message"></a><span data-ttu-id="49341-104">\_Сообщение спфиленотифи филеопделайед</span><span class="sxs-lookup"><span data-stu-id="49341-104">SPFILENOTIFY\_FILEOPDELAYED message</span></span>

<span data-ttu-id="49341-105">Уведомление **спфиленотифи \_ филеопделайед** отправляется [**сетупинсталлфиликс**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) или [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) в подпрограммы обратного вызова, когда файл был отложен, так как файл уже используется.</span><span class="sxs-lookup"><span data-stu-id="49341-105">The **SPFILENOTIFY\_FILEOPDELAYED** notification is sent by [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) or [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) to a callback routine when a file operation was delayed because the file was in use.</span></span> <span data-ttu-id="49341-106">Операция будет обработана при следующей перезагрузке системы.</span><span class="sxs-lookup"><span data-stu-id="49341-106">The operation will be processed the next time the system is rebooted.</span></span>


```C++
SPFILENOTIFY_FILEOPDELAYED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="49341-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="49341-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49341-108">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="49341-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="49341-109">Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="49341-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

<span data-ttu-id="49341-110">Если отложенная операция является операцией копирования файлов, структура [**filePaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) содержит следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="49341-110">If the delayed operation is a file copy operation, the [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure contains the following information.</span></span>



| <span data-ttu-id="49341-111">Элемент FILEPATHs</span><span class="sxs-lookup"><span data-stu-id="49341-111">FILEPATHS member</span></span> | <span data-ttu-id="49341-112">Значение</span><span class="sxs-lookup"><span data-stu-id="49341-112">Value</span></span>                                |
|------------------|--------------------------------------|
| <span data-ttu-id="49341-113">**Win32Error**</span><span class="sxs-lookup"><span data-stu-id="49341-113">**Win32Error**</span></span>   | <span data-ttu-id="49341-114">БЕЗ \_ ошибок</span><span class="sxs-lookup"><span data-stu-id="49341-114">NO\_ERROR</span></span>                            |
| <span data-ttu-id="49341-115">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="49341-115">**Flags**</span></span>        | <span data-ttu-id="49341-116">\_копирование филеоп</span><span class="sxs-lookup"><span data-stu-id="49341-116">FILEOP\_COPY</span></span>                         |
| <span data-ttu-id="49341-117">**Источник**</span><span class="sxs-lookup"><span data-stu-id="49341-117">**Source**</span></span>       | <span data-ttu-id="49341-118">Полный путь к временному файлу.</span><span class="sxs-lookup"><span data-stu-id="49341-118">Full path of the temporary file.</span></span>     |
| <span data-ttu-id="49341-119">**Целевой объект**</span><span class="sxs-lookup"><span data-stu-id="49341-119">**Target**</span></span>       | <span data-ttu-id="49341-120">Полный путь к фактическому целевому файлу.</span><span class="sxs-lookup"><span data-stu-id="49341-120">Full path of the actual target file.</span></span> |



 

<span data-ttu-id="49341-121">Этот временный файл будет скопирован в целевой каталог при перезагрузке системы.</span><span class="sxs-lookup"><span data-stu-id="49341-121">This temporary file will be copied to the target directory when the system is rebooted.</span></span> <span data-ttu-id="49341-122">Функции установки автоматически создают путь для временного файла.</span><span class="sxs-lookup"><span data-stu-id="49341-122">The setup functions automatically generate a path for the temporary file.</span></span>

<span data-ttu-id="49341-123">Если отложенная операция является операцией удаления файла, структура [**filePaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) содержит следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="49341-123">If the delayed operation is a file delete operation, the [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure contains the following information.</span></span>



| <span data-ttu-id="49341-124">Элемент FILEPATHs</span><span class="sxs-lookup"><span data-stu-id="49341-124">FILEPATHS member</span></span> | <span data-ttu-id="49341-125">Значение</span><span class="sxs-lookup"><span data-stu-id="49341-125">Value</span></span>                                |
|------------------|--------------------------------------|
| <span data-ttu-id="49341-126">**Win32Error**</span><span class="sxs-lookup"><span data-stu-id="49341-126">**Win32Error**</span></span>   | <span data-ttu-id="49341-127">БЕЗ \_ ошибок</span><span class="sxs-lookup"><span data-stu-id="49341-127">NO\_ERROR</span></span>                            |
| <span data-ttu-id="49341-128">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="49341-128">**Flags**</span></span>        | <span data-ttu-id="49341-129">ФИЛЕОП \_ Удаление</span><span class="sxs-lookup"><span data-stu-id="49341-129">FILEOP\_DELETE</span></span>                       |
| <span data-ttu-id="49341-130">**Источник**</span><span class="sxs-lookup"><span data-stu-id="49341-130">**Source**</span></span>       | <span data-ttu-id="49341-131">NULL</span><span class="sxs-lookup"><span data-stu-id="49341-131">NULL</span></span>                                 |
| <span data-ttu-id="49341-132">**Целевой объект**</span><span class="sxs-lookup"><span data-stu-id="49341-132">**Target**</span></span>       | <span data-ttu-id="49341-133">Полный путь к удаляемому файлу.</span><span class="sxs-lookup"><span data-stu-id="49341-133">Full path of the file to be deleted.</span></span> |



 

</dd> <dt>

<span data-ttu-id="49341-134">*Param2*</span><span class="sxs-lookup"><span data-stu-id="49341-134">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="49341-135">Не используется.</span><span class="sxs-lookup"><span data-stu-id="49341-135">Is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49341-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49341-136">Return value</span></span>

<span data-ttu-id="49341-137">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="49341-137">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="49341-138">Требования</span><span class="sxs-lookup"><span data-stu-id="49341-138">Requirements</span></span>



| <span data-ttu-id="49341-139">Требование</span><span class="sxs-lookup"><span data-stu-id="49341-139">Requirement</span></span> | <span data-ttu-id="49341-140">Значение</span><span class="sxs-lookup"><span data-stu-id="49341-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49341-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49341-141">Minimum supported client</span></span><br/> | <span data-ttu-id="49341-142">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="49341-142">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="49341-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49341-143">Minimum supported server</span></span><br/> | <span data-ttu-id="49341-144">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="49341-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49341-145">Header</span><span class="sxs-lookup"><span data-stu-id="49341-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="49341-146"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="49341-146"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49341-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49341-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49341-148">Обзор</span><span class="sxs-lookup"><span data-stu-id="49341-148">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="49341-149">Уведомления</span><span class="sxs-lookup"><span data-stu-id="49341-149">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="49341-150">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="49341-150">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="49341-151">**сетупкоммитфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="49341-151">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="49341-152">**сетупинсталлфиле**</span><span class="sxs-lookup"><span data-stu-id="49341-152">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="49341-153">**сетупинсталлфиликс**</span><span class="sxs-lookup"><span data-stu-id="49341-153">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="49341-154">**сетупинсталлфроминфсектион**</span><span class="sxs-lookup"><span data-stu-id="49341-154">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




