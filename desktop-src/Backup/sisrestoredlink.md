---
title: Функция Сисресторедлинк (Сисбкуп. h)
description: Возвращает имена файлов или файлов общего хранилища, на которые указывает указанная восстановленная ссылка SIS.
ms.assetid: 4eefd975-6055-44c0-93ab-900638948f3e
keywords:
- Резервное копирование функции Сисресторедлинк
topic_type:
- apiref
api_name:
- SisRestoredLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd539d1ad6c203441b2bcd469a7d8f2fe8bdfc7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988382"
---
# <a name="sisrestoredlink-function"></a><span data-ttu-id="51e87-104">Функция Сисресторедлинк</span><span class="sxs-lookup"><span data-stu-id="51e87-104">SisRestoredLink function</span></span>

<span data-ttu-id="51e87-105">Функция **сисресторедлинк** возвращает имена файлов или файлов общего хранилища, на которые указывает указанная восстановленная ссылка SIS.</span><span class="sxs-lookup"><span data-stu-id="51e87-105">The **SisRestoredLink** function returns the names of the common-store file or files pointed to by the specified restored SIS link.</span></span>

## <a name="syntax"></a><span data-ttu-id="51e87-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51e87-106">Syntax</span></span>


```C++
BOOL SisRestoredLink(
  _In_  PVOID  sisRestoreStructure,
  _In_  PWCHAR restoredFileName,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a><span data-ttu-id="51e87-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="51e87-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51e87-108">*сисрестореструктуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="51e87-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51e87-109">Указатель на структуру восстановления SIS, возвращенную из [**сискреатерестореструктуре**](siscreaterestorestructure.md).</span><span class="sxs-lookup"><span data-stu-id="51e87-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="51e87-110">*ресторедфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="51e87-110">*restoredFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51e87-111">Полное имя восстановленного файла канала SIS.</span><span class="sxs-lookup"><span data-stu-id="51e87-111">Fully qualified file name of the restored SIS link file.</span></span>

</dd> <dt>

<span data-ttu-id="51e87-112">*репарседата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="51e87-112">*reparseData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51e87-113">Указатель на содержимое точки повторного анализа SIS.</span><span class="sxs-lookup"><span data-stu-id="51e87-113">Pointer to the contents of the SIS reparse point.</span></span> <span data-ttu-id="51e87-114">Эта точка повторного анализа содержит данные, описывающие восстановленную ссылку на SIS.</span><span class="sxs-lookup"><span data-stu-id="51e87-114">This reparse point contains data describing the restored SIS link.</span></span> <span data-ttu-id="51e87-115">Чтобы получить данные точки повторного анализа для файла, используйте управляющий код [**" \_ Получение \_ \_ точки**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) повторного анализа фсктл".</span><span class="sxs-lookup"><span data-stu-id="51e87-115">To retrieve the reparse point data for a file, use the [**FSCTL\_GET\_REPARSE\_POINT**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) control code.</span></span>

</dd> <dt>

<span data-ttu-id="51e87-116">*репарседатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="51e87-116">*reparseDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51e87-117">Размер содержимого точки повторной обработки SIS, на которую указывает *репарседата*, в байтах.</span><span class="sxs-lookup"><span data-stu-id="51e87-117">Size of the contents of the SIS reparse point pointed to by *reparseData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="51e87-118">*каунтофкоммонсторефилесторесторе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="51e87-118">*countOfCommonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51e87-119">Число файлов, перечисленных в параметре *коммонсторефилесторесторе* .</span><span class="sxs-lookup"><span data-stu-id="51e87-119">Number of files listed in the *commonStoreFilesToRestore* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="51e87-120">*коммонсторефилесторесторе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="51e87-120">*commonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51e87-121">Указатель на массив имен файлов общего хранилища.</span><span class="sxs-lookup"><span data-stu-id="51e87-121">Pointer to an array of common-store file names.</span></span> <span data-ttu-id="51e87-122">Эти файлы следует восстанавливать одновременно и так же, как и файлы общего хранилища, запрашиваемые [**сисксфилестобаккупфорлинк**](siscsfilestobackupforlink.md).</span><span class="sxs-lookup"><span data-stu-id="51e87-122">These files should be restored at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span></span>

<span data-ttu-id="51e87-123">Если значение параметра *каунтофкоммонсторефилесторесторе* не равно 0, то значение параметра *коммонсторефилесторесторе* будет содержать имена файлов общего хранилища, которые будут восстановлены в результате восстановления связи SIS.</span><span class="sxs-lookup"><span data-stu-id="51e87-123">If the value of the *countOfCommonStoreFilesToRestore* parameter is not 0, the value of the *commonStoreFilesToRestore* parameter will contain the names of the common-store files to be restored as a result of restoring the SIS link.</span></span> <span data-ttu-id="51e87-124">Если значение равно 0, то либо файлы общего хранилища были возвращены один раз, либо они уже имеются в томе.</span><span class="sxs-lookup"><span data-stu-id="51e87-124">If the value is 0, then either the common-store files have been returned once, or they are already present on the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51e87-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51e87-125">Return value</span></span>

<span data-ttu-id="51e87-126">Эта функция возвращает **значение true** , если она завершается успешно, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="51e87-126">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="51e87-127">Вызовите [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) , чтобы получить дополнительные сведения о причине сбоя вызова.</span><span class="sxs-lookup"><span data-stu-id="51e87-127">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="51e87-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51e87-128">Remarks</span></span>

<span data-ttu-id="51e87-129">Эту функцию следует вызывать для каждого восстановленного канала SIS.</span><span class="sxs-lookup"><span data-stu-id="51e87-129">You should call this function for each SIS link that has been restored.</span></span>

<span data-ttu-id="51e87-130">Эта функция будет возвращать каждый файл Common-Store не чаще для каждой операции восстановления. Любая попытка восстановить дополнительные каналы SIS, которые видят один и тот же файл общего хранилища, не приведет к возвращению имени файла общего хранилища.</span><span class="sxs-lookup"><span data-stu-id="51e87-130">This function will return each common-store file at most once for each restore operation; any attempt to restore additional SIS links that see the same common-store file will not result in that common-store file name being returned.</span></span>

<span data-ttu-id="51e87-131">Эта функция не возвращает файл общего хранилища, который также не был возвращен при вызове [**сисксфилестобаккупфорлинк**](siscsfilestobackupforlink.md) во время операции резервного копирования, предполагая, что данные повторной обработки SIS, хранящиеся на носителе, не повреждены.</span><span class="sxs-lookup"><span data-stu-id="51e87-131">This function will not return a common-store file that was not also returned in a call to [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md) during the backup operation, assuming that the SIS reparse data stored on the media has not been corrupted.</span></span>

<span data-ttu-id="51e87-132">При восстановлении канала SIS операция восстановления должна создать только соответствующий разреженный файл, инициализировать все выделенные диапазоны, а затем записать данные повторной обработки SIS в том виде, в котором они были считаны во время операции резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="51e87-132">When restoring a SIS link, your restore operation should create only the appropriate sparse file, initialize any allocated ranges, and then write the SIS reparse data exactly as it was read during the backup operation.</span></span> <span data-ttu-id="51e87-133">Крайне важно, чтобы операция восстановления создания разреженных файлов с нераспределенными диапазонами, а не разреженными файлами (или неэкономными файлами), инициализированными нулями.</span><span class="sxs-lookup"><span data-stu-id="51e87-133">It is crucial that your restore operation create sparse files with unallocated ranges rather than sparse files (or nonsparse files) initialized with zeroes.</span></span>

<span data-ttu-id="51e87-134">Обратите внимание, что эта функция не обязательно определяет файл или файлы общего хранилища, соответствующие набору ссылок SIS на носителе резервной копии, если на диске остались файлы общих или файлов общего хранилища.</span><span class="sxs-lookup"><span data-stu-id="51e87-134">Note that this function will not necessarily identify the common-store file or files corresponding to a set of SIS links on the backup media if those common-store file or files still exist on disk.</span></span> <span data-ttu-id="51e87-135">Содержимое потока данных файла общего хранилища никогда не изменяется после его создания, поэтому, если файл уже существует на диске, его не нужно восстанавливать.</span><span class="sxs-lookup"><span data-stu-id="51e87-135">The contents of a common-store file's data stream never changes once it is created, so if the file already exists on the disk there is no need to restore it.</span></span>

<span data-ttu-id="51e87-136">Имена файлов общего хранилища глобально уникальны, чтобы обеспечить целостность операции восстановления, даже если она не выполняется на том же томе с поддержкой SIS, к которому осуществлялся доступ при операции резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="51e87-136">Common-store file names are globally unique to ensure the integrity of the restore operation even if it does not occur on the same SIS-enabled volume that the backup operation has accessed.</span></span>

## <a name="requirements"></a><span data-ttu-id="51e87-137">Требования</span><span class="sxs-lookup"><span data-stu-id="51e87-137">Requirements</span></span>



| <span data-ttu-id="51e87-138">Требование</span><span class="sxs-lookup"><span data-stu-id="51e87-138">Requirement</span></span> | <span data-ttu-id="51e87-139">Значение</span><span class="sxs-lookup"><span data-stu-id="51e87-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51e87-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51e87-140">Minimum supported client</span></span><br/> | <span data-ttu-id="51e87-141">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="51e87-141">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="51e87-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51e87-142">Minimum supported server</span></span><br/> | <span data-ttu-id="51e87-143">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="51e87-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="51e87-144">Header</span><span class="sxs-lookup"><span data-stu-id="51e87-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="51e87-145"><dt>Сисбкуп. h</dt></span><span class="sxs-lookup"><span data-stu-id="51e87-145"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="51e87-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="51e87-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="51e87-147"><dt>Сисбкуп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51e87-147"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="51e87-148">DLL</span><span class="sxs-lookup"><span data-stu-id="51e87-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51e87-149"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51e87-149"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51e87-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51e87-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51e87-151">**сискреатерестореструктуре**</span><span class="sxs-lookup"><span data-stu-id="51e87-151">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="51e87-152">**сисксфилестобаккупфорлинк**</span><span class="sxs-lookup"><span data-stu-id="51e87-152">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> </dl>

 

