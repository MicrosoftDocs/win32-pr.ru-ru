---
title: Функция Сискреатерестореструктуре (Сисбкуп. h)
description: Создает структуру восстановления SIS на основе указанной информации.
ms.assetid: acdd4258-813d-42af-a2e1-e59a1426f86c
keywords:
- Резервное копирование функции Сискреатерестореструктуре
topic_type:
- apiref
api_name:
- SisCreateRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b83ebcdd609b00fdec19666a6915926692a2048
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891658"
---
# <a name="siscreaterestorestructure-function"></a><span data-ttu-id="d9181-104">Функция Сискреатерестореструктуре</span><span class="sxs-lookup"><span data-stu-id="d9181-104">SisCreateRestoreStructure function</span></span>

<span data-ttu-id="d9181-105">Функция **сискреатерестореструктуре** создает структуру восстановления SIS на основе указанной информации.</span><span class="sxs-lookup"><span data-stu-id="d9181-105">The **SisCreateRestoreStructure** function creates a SIS restore structure based on the supplied information.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9181-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9181-106">Syntax</span></span>


```C++
BOOL SisCreateRestoreStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisRestoreStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a><span data-ttu-id="d9181-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9181-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9181-108">*волумерут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9181-108">*volumeRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9181-109">Имя файла корня тома без обратной косой черты тома, для которого будет выполняться резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="d9181-109">File name of the volume root, without the trailing backslash, of the volume to be backed up.</span></span> <span data-ttu-id="d9181-110">Например, укажите "C:", а не "C:" \\ .</span><span class="sxs-lookup"><span data-stu-id="d9181-110">For example, specify "C:" and not "C:\\".</span></span> <span data-ttu-id="d9181-111">Том не может быть системным или загрузочным томом.</span><span class="sxs-lookup"><span data-stu-id="d9181-111">The volume cannot be the system or boot volume.</span></span>

</dd> <dt>

<span data-ttu-id="d9181-112">*сисрестореструктуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d9181-112">*sisRestoreStructure* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9181-113">Возвращенная структура восстановления SIS.</span><span class="sxs-lookup"><span data-stu-id="d9181-113">Returned SIS restore structure.</span></span> <span data-ttu-id="d9181-114">Эта структура должна рассматриваться как непрозрачная вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="d9181-114">This structure should be treated as opaque by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="d9181-115">*коммонсторерутпаснаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d9181-115">*commonStoreRootPathname* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9181-116">Полное имя пути к общему хранилищу указанного тома.</span><span class="sxs-lookup"><span data-stu-id="d9181-116">Fully qualified path name of the specified volume's common store.</span></span> <span data-ttu-id="d9181-117">Например, "c: \\ Общее хранилище SIS".</span><span class="sxs-lookup"><span data-stu-id="d9181-117">For example, "c:\\SIS Common Store".</span></span>

</dd> <dt>

<span data-ttu-id="d9181-118">*каунтофкоммонсторефилесторесторе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d9181-118">*countOfCommonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9181-119">Число файлов, перечисленных в параметре *коммонсторефилесторесторе* .</span><span class="sxs-lookup"><span data-stu-id="d9181-119">Number of files listed in the *commonStoreFilesToRestore* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d9181-120">*коммонсторефилесторесторе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d9181-120">*commonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9181-121">Указатель на массив имен файлов, указывающий список внутренних файлов, используемых SIS для управления указанным томом.</span><span class="sxs-lookup"><span data-stu-id="d9181-121">Pointer to an array of file names that specifies the list of internal files used by SIS to manage the specified volume.</span></span> <span data-ttu-id="d9181-122">Эти файлы следует восстанавливать одновременно и так же, как и файлы общего хранилища, запрашиваемые [**сисксфилестобаккупфорлинк**](siscsfilestobackupforlink.md).</span><span class="sxs-lookup"><span data-stu-id="d9181-122">These files should be restored at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9181-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9181-123">Return value</span></span>

<span data-ttu-id="d9181-124">Эта функция возвращает **значение true** , если она завершается успешно, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d9181-124">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="d9181-125">Вызовите [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) , чтобы получить дополнительные сведения о причине сбоя вызова.</span><span class="sxs-lookup"><span data-stu-id="d9181-125">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9181-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9181-126">Remarks</span></span>

<span data-ttu-id="d9181-127">Эта функция устанавливает среду восстановления на указанном томе таким образом, как [**сискреатебаккупструктуре**](siscreatebackupstructure.md) устанавливает среду резервного копирования на указанном томе.</span><span class="sxs-lookup"><span data-stu-id="d9181-127">This function establishes the restore environment on the specified volume in the way that [**SisCreateBackupStructure**](siscreatebackupstructure.md) establishes the backup environment on the specified volume.</span></span>

<span data-ttu-id="d9181-128">Обратите внимание, что эта функция не обязательно определяет файл или файлы Common-Store, соответствующие набору ссылок SIS на носителе резервной копии, если на диске все еще существуют общие файлы хранилища или файлов.</span><span class="sxs-lookup"><span data-stu-id="d9181-128">Note that this function will not necessarily identify the common-store file or files corresponding to a set of SIS links on the backup media if those common store file or files still exist on disk.</span></span> <span data-ttu-id="d9181-129">Содержимое потока данных файла общего хранилища никогда не изменяется после его создания, поэтому если файл уже существует на диске, его не нужно восстанавливать.</span><span class="sxs-lookup"><span data-stu-id="d9181-129">The contents of a common-store file's data stream never change once it is created, so if the file already exists on the disk there is no need to restore it.</span></span>

<span data-ttu-id="d9181-130">Имена файлов общего хранилища глобально уникальны, чтобы обеспечить целостность операции восстановления, даже если она не выполняется на том же томе с поддержкой SIS, к которому осуществлялся доступ при операции резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="d9181-130">Common-store file names are globally unique to ensure the integrity of the restore operation even if it does not occur on the same SIS-enabled volume that the backup operation has accessed.</span></span>

<span data-ttu-id="d9181-131">После завершения операции восстановления следует освободить память, используемую массивом строк *коммонсторефилесторесторе* , вызвав [**сисфриаллокатедмемори**](sisfreeallocatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="d9181-131">After the restore operation is complete, deallocate the memory used by the *commonStoreFilesToRestore* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9181-132">Требования</span><span class="sxs-lookup"><span data-stu-id="d9181-132">Requirements</span></span>



| <span data-ttu-id="d9181-133">Требование</span><span class="sxs-lookup"><span data-stu-id="d9181-133">Requirement</span></span> | <span data-ttu-id="d9181-134">Значение</span><span class="sxs-lookup"><span data-stu-id="d9181-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9181-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9181-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d9181-136">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d9181-136">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d9181-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9181-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d9181-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d9181-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d9181-139">Header</span><span class="sxs-lookup"><span data-stu-id="d9181-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9181-140"><dt>Сисбкуп. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9181-140"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="d9181-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d9181-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="d9181-142"><dt>Сисбкуп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9181-142"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="d9181-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d9181-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9181-144"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9181-144"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9181-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9181-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9181-146">**сискреатебаккупструктуре**</span><span class="sxs-lookup"><span data-stu-id="d9181-146">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> <dt>

[<span data-ttu-id="d9181-147">**сисксфилестобаккупфорлинк**</span><span class="sxs-lookup"><span data-stu-id="d9181-147">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="d9181-148">**сисфриаллокатедмемори**</span><span class="sxs-lookup"><span data-stu-id="d9181-148">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> <dt>

[<span data-ttu-id="d9181-149">**сисфрибаккупструктуре**</span><span class="sxs-lookup"><span data-stu-id="d9181-149">**SisFreeBackupStructure**</span></span>](sisfreebackupstructure.md)
</dt> </dl>

 

