---
title: Функция Сисфриаллокатедмемори (Сисбкуп. h)
description: Освобождает память, выделенную функциями API SIS.
ms.assetid: 8fab79c8-593c-46df-a885-09a59620a977
keywords:
- Резервное копирование функции Сисфриаллокатедмемори
topic_type:
- apiref
api_name:
- SisFreeAllocatedMemory
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724970817b89f6a9f2490b0776775f6a3a4e69ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891657"
---
# <a name="sisfreeallocatedmemory-function"></a><span data-ttu-id="286fc-104">Функция Сисфриаллокатедмемори</span><span class="sxs-lookup"><span data-stu-id="286fc-104">SisFreeAllocatedMemory function</span></span>

<span data-ttu-id="286fc-105">Функция **сисфриаллокатедмемори** освобождает память, выделенную ФУНКЦИЯМИ API SIS.</span><span class="sxs-lookup"><span data-stu-id="286fc-105">The **SisFreeAllocatedMemory** function frees memory allocated by SIS API functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="286fc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="286fc-106">Syntax</span></span>


```C++
void SisFreeAllocatedMemory(
  _In_ PVOID allocatedSpace
);
```



## <a name="parameters"></a><span data-ttu-id="286fc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="286fc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="286fc-108">*аллокатедспаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="286fc-108">*allocatedSpace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="286fc-109">Указатель на память, выделенную API SIS.</span><span class="sxs-lookup"><span data-stu-id="286fc-109">Pointer to the memory allocated by the SIS API.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="286fc-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="286fc-110">Return value</span></span>

<span data-ttu-id="286fc-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="286fc-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="286fc-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="286fc-112">Remarks</span></span>

<span data-ttu-id="286fc-113">После завершения вызова этой функции вызывающий может больше не обращаться к освобожденной памяти.</span><span class="sxs-lookup"><span data-stu-id="286fc-113">After the call to this function completes, the caller may no longer access the freed memory.</span></span>

<span data-ttu-id="286fc-114">Этот вызов следует использовать для освобождения памяти, выделенной для строк параметров *коммонсторерутпаснаме* , возвращаемых из [**сискреатебаккупструктуре**](siscreatebackupstructure.md) и [**сискреатерестореструктуре**](siscreaterestorestructure.md), и массива строк, содержащих имена файлов общего хранилища, возвращаемые из **сискреатебаккупструктуре**, [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md), **SisCreateRestoreStructure** и [**SisRestoredLink**](sisrestoredlink.md).</span><span class="sxs-lookup"><span data-stu-id="286fc-114">This call should be used to deallocate the memory allocated for the *commonStoreRootPathname* parameter strings returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md) and [**SisCreateRestoreStructure**](siscreaterestorestructure.md), and the array of strings containing common-store file names returned from **SisCreateBackupStructure**, [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md), **SisCreateRestoreStructure**, and [**SisRestoredLink**](sisrestoredlink.md).</span></span> <span data-ttu-id="286fc-115">В последнем случае массив также должен быть освобожден путем вызова **сисфриаллокатедмемори**.</span><span class="sxs-lookup"><span data-stu-id="286fc-115">In the latter case, the array itself also must be freed by calling **SisFreeAllocatedMemory**.</span></span>

## <a name="requirements"></a><span data-ttu-id="286fc-116">Требования</span><span class="sxs-lookup"><span data-stu-id="286fc-116">Requirements</span></span>



| <span data-ttu-id="286fc-117">Требование</span><span class="sxs-lookup"><span data-stu-id="286fc-117">Requirement</span></span> | <span data-ttu-id="286fc-118">Значение</span><span class="sxs-lookup"><span data-stu-id="286fc-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="286fc-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="286fc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="286fc-120">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="286fc-120">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="286fc-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="286fc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="286fc-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="286fc-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="286fc-123">Header</span><span class="sxs-lookup"><span data-stu-id="286fc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="286fc-124"><dt>Сисбкуп. h</dt></span><span class="sxs-lookup"><span data-stu-id="286fc-124"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="286fc-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="286fc-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="286fc-126"><dt>Сисбкуп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="286fc-126"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="286fc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="286fc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="286fc-128"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="286fc-128"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="286fc-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="286fc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="286fc-130">**сискреатебаккупструктуре**</span><span class="sxs-lookup"><span data-stu-id="286fc-130">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> <dt>

[<span data-ttu-id="286fc-131">**сискреатерестореструктуре**</span><span class="sxs-lookup"><span data-stu-id="286fc-131">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="286fc-132">**сисксфилестобаккупфорлинк**</span><span class="sxs-lookup"><span data-stu-id="286fc-132">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="286fc-133">**сисресторедлинк**</span><span class="sxs-lookup"><span data-stu-id="286fc-133">**SisRestoredLink**</span></span>](sisrestoredlink.md)
</dt> </dl>

 

 





