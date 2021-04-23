---
title: Функция Сискреатебаккупструктуре (Сисбкуп. h)
description: Создает структуру резервного копирования SIS на основе указанной информации.
ms.assetid: a8c48961-fa24-4eb6-92cd-1b9bc83cec41
keywords:
- Резервное копирование функции Сискреатебаккупструктуре
topic_type:
- apiref
api_name:
- SisCreateBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad432095f9d264e124df1d84070056fc827c625e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489819"
---
# <a name="siscreatebackupstructure-function"></a><span data-ttu-id="e98b2-104">Функция Сискреатебаккупструктуре</span><span class="sxs-lookup"><span data-stu-id="e98b2-104">SisCreateBackupStructure function</span></span>

<span data-ttu-id="e98b2-105">Функция **сискреатебаккупструктуре** создает структуру резервного копирования SIS на основе указанной информации.</span><span class="sxs-lookup"><span data-stu-id="e98b2-105">The **SisCreateBackupStructure** function creates a SIS backup structure based on the supplied information.</span></span>

## <a name="syntax"></a><span data-ttu-id="e98b2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e98b2-106">Syntax</span></span>


```C++
BOOL SisCreateBackupStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisBackupStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a><span data-ttu-id="e98b2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e98b2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e98b2-108">*волумерут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e98b2-108">*volumeRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e98b2-109">Имя файла корня тома без обратной косой черты тома, для которого будет выполняться резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="e98b2-109">File name of the volume root, without the trailing backslash, of the volume to be backed up.</span></span> <span data-ttu-id="e98b2-110">Например, укажите "C:", а не "C:" \\ .</span><span class="sxs-lookup"><span data-stu-id="e98b2-110">For example, specify "C:" and not "C:\\".</span></span>

</dd> <dt>

<span data-ttu-id="e98b2-111">*сисбаккупструктуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e98b2-111">*sisBackupStructure* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e98b2-112">Возвращенная структура резервного копирования SIS.</span><span class="sxs-lookup"><span data-stu-id="e98b2-112">Returned SIS backup structure.</span></span>

</dd> <dt>

<span data-ttu-id="e98b2-113">*коммонсторерутпаснаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e98b2-113">*commonStoreRootPathname* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e98b2-114">Полное имя пути к общему хранилищу указанного тома.</span><span class="sxs-lookup"><span data-stu-id="e98b2-114">Fully qualified path name of the specified volume's common store.</span></span> <span data-ttu-id="e98b2-115">Например, "c: \\ Общее хранилище SIS".</span><span class="sxs-lookup"><span data-stu-id="e98b2-115">For example, "c:\\SIS Common Store".</span></span>

</dd> <dt>

<span data-ttu-id="e98b2-116">*каунтофкоммонсторефилестобаккуп* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e98b2-116">*countOfCommonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e98b2-117">Число файлов, перечисленных в параметре *коммонсторефилестобаккуп* .</span><span class="sxs-lookup"><span data-stu-id="e98b2-117">Number of files listed in the *commonStoreFilesToBackUp* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e98b2-118">*коммонсторефилестобаккуп* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e98b2-118">*commonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e98b2-119">Указатель на массив имен файлов, указывающий список внутренних файлов, используемых SIS для управления указанным томом.</span><span class="sxs-lookup"><span data-stu-id="e98b2-119">Pointer to an array of file names that specifies a list of internal files used by SIS to manage the specified volume.</span></span> <span data-ttu-id="e98b2-120">Эти файлы должны создаваться одновременно и так же, как и файлы общего хранилища, запрашиваемые [ **сисксфилестобаккупфорлинк**](siscsfilestobackupforlink.md)</span><span class="sxs-lookup"><span data-stu-id="e98b2-120">These files should be backed up at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e98b2-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e98b2-121">Return value</span></span>

<span data-ttu-id="e98b2-122">Эта функция возвращает **значение true** , если она завершается успешно, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e98b2-122">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="e98b2-123">Вызовите [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) , чтобы получить дополнительные сведения о причине сбоя вызова.</span><span class="sxs-lookup"><span data-stu-id="e98b2-123">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="e98b2-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e98b2-124">Remarks</span></span>

<span data-ttu-id="e98b2-125">Эта функция создает структуру резервного копирования SIS, которая используется API-интерфейсом резервного копирования SIS для создания и обслуживания списка ссылок на файлы в томе и исходных файлах, на которые указывают ссылки.</span><span class="sxs-lookup"><span data-stu-id="e98b2-125">This function creates a SIS backup structure, which is used by the SIS backup API to create and maintain a list of the file links on the volume and the original files the links point to.</span></span> <span data-ttu-id="e98b2-126">Эту функцию следует вызывать только один раз для каждого тома с поддержкой SIS.</span><span class="sxs-lookup"><span data-stu-id="e98b2-126">This function should be called only once for each SIS-enabled volume being backed up.</span></span> <span data-ttu-id="e98b2-127">Все файлы в указанном томе следует рассматривать как файлы общего хранилища и создавать их резервные копии только в том случае, если хранилище единственных копий указывает, что они должны.</span><span class="sxs-lookup"><span data-stu-id="e98b2-127">All files within the specified volume should be treated as common-store files and backed up only if SIS indicates that they should.</span></span>

<span data-ttu-id="e98b2-128">Параметры *каунтофкоммонсторефилестобаккуп* и *коммонсторефилестобаккуп* вместе возвращают список файлов, для которых необходимо создать резервную копию, независимо от того, для каких связей выполняется резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="e98b2-128">The *countOfCommonStoreFilesToBackUp* and *commonStoreFilesToBackUp* parameters together return a list of files that must be backed up regardless of which links are backed up.</span></span>

<span data-ttu-id="e98b2-129">Если *каунтофкоммонсторефилестобаккуп* имеет значение 0, *Коммонсторефилестобаккуп* может быть **пустым** указателем.</span><span class="sxs-lookup"><span data-stu-id="e98b2-129">If *countOfCommonStoreFilesToBackUp* is 0, *commonStoreFilesToBackUp* may be a **NULL** pointer.</span></span> <span data-ttu-id="e98b2-130">Значение параметра *коммонсторефилестобаккуп* должно игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="e98b2-130">The value of the *commonStoreFilesToBackUp* parameter should be ignored.</span></span>

<span data-ttu-id="e98b2-131">После завершения операции резервного копирования следует освободить память, используемую массивом строк *коммонсторефилестобаккуп* , вызвав [**сисфриаллокатедмемори**](sisfreeallocatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="e98b2-131">After the backup operation is complete, deallocate the memory used by the *commonStoreFilesToBackUp* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e98b2-132">Требования</span><span class="sxs-lookup"><span data-stu-id="e98b2-132">Requirements</span></span>



| <span data-ttu-id="e98b2-133">Требование</span><span class="sxs-lookup"><span data-stu-id="e98b2-133">Requirement</span></span> | <span data-ttu-id="e98b2-134">Значение</span><span class="sxs-lookup"><span data-stu-id="e98b2-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e98b2-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e98b2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e98b2-136">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e98b2-136">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e98b2-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e98b2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e98b2-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e98b2-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e98b2-139">Header</span><span class="sxs-lookup"><span data-stu-id="e98b2-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e98b2-140"><dt>Сисбкуп. h</dt></span><span class="sxs-lookup"><span data-stu-id="e98b2-140"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="e98b2-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e98b2-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="e98b2-142"><dt>Сисбкуп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e98b2-142"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="e98b2-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e98b2-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e98b2-144"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e98b2-144"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e98b2-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e98b2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e98b2-146">**сискреатерестореструктуре**</span><span class="sxs-lookup"><span data-stu-id="e98b2-146">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="e98b2-147">**сисксфилестобаккупфорлинк**</span><span class="sxs-lookup"><span data-stu-id="e98b2-147">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="e98b2-148">**сисфриаллокатедмемори**</span><span class="sxs-lookup"><span data-stu-id="e98b2-148">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> </dl>

 

