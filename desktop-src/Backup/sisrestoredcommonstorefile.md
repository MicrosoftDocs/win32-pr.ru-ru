---
title: Функция Сисресторедкоммонсторефиле (Сисбкуп. h)
description: Сообщает архитектуре SIS о том, что файл Common-Store записан.
ms.assetid: 2b1cd9e7-a19c-4474-a40a-5a27d4feeab7
keywords:
- Резервное копирование функции Сисресторедкоммонсторефиле
topic_type:
- apiref
api_name:
- SisRestoredCommonStoreFile
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093ff5f20db42bcafe62ee0ec57d5027abcf9f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988383"
---
# <a name="sisrestoredcommonstorefile-function"></a><span data-ttu-id="2cbd7-104">Функция Сисресторедкоммонсторефиле</span><span class="sxs-lookup"><span data-stu-id="2cbd7-104">SisRestoredCommonStoreFile function</span></span>

<span data-ttu-id="2cbd7-105">Функция **сисресторедкоммонсторефиле** сообщает архитектуре SIS о том, что файл Common-Store записан.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-105">The **SisRestoredCommonStoreFile** function reports to the SIS architecture that a common-store file has been written.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cbd7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2cbd7-106">Syntax</span></span>


```C++
BOOL SisRestoredCommonStoreFile(
  _In_ PVOID  sisRestoreStructure,
  _In_ PWCHAR commonStoreFileName
);
```



## <a name="parameters"></a><span data-ttu-id="2cbd7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cbd7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cbd7-108">*сисрестореструктуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2cbd7-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cbd7-109">Указатель на структуру восстановления SIS, возвращенную из [**сискреатерестореструктуре**](siscreaterestorestructure.md).</span><span class="sxs-lookup"><span data-stu-id="2cbd7-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="2cbd7-110">*коммонсторефиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2cbd7-110">*commonStoreFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cbd7-111">Имя восстановленного файла common-Store.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-111">Name of the restored common-store file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cbd7-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2cbd7-112">Return value</span></span>

<span data-ttu-id="2cbd7-113">Эта функция возвращает **значение true** , если она завершается успешно, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-113">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="2cbd7-114">Вызовите [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) , чтобы получить дополнительные сведения о причине сбоя вызова.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-114">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cbd7-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2cbd7-115">Remarks</span></span>

<span data-ttu-id="2cbd7-116">Эту функцию следует вызывать после восстановления файла общего хранилища.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-116">This function should be called after you have restored a common-store file.</span></span> <span data-ttu-id="2cbd7-117">Он уведомляет архитектуру SIS о том, что был записан новый файл Common-Store, чтобы архитектура SIS могла выполнять внутренние задачи обслуживания, такие как инициализация внутренних структур данных или исправление ссылок на файл общего хранилища.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-117">It notifies the SIS architecture that a new common-store file has been written, so that the SIS architecture can perform internal maintenance tasks such as initializing its internal data structures or fixing the links to the common-store file.</span></span>

<span data-ttu-id="2cbd7-118">Операция восстановления должна восстанавливать только файлы общего хранилища, указанные в [**сисресторедлинк**](sisrestoredlink.md), даже если на носителе резервных копий имеются дополнительные файлы общего хранилища.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-118">Your restore operation should restore only common-store files reported by [**SisRestoredLink**](sisrestoredlink.md), even if there are additional common-store files on the backup media.</span></span> <span data-ttu-id="2cbd7-119">С помощью операции восстановления можно восстановить ссылки SIS и файлы общего хранилища в любом порядке, который он выбрал. Однако он должен вызвать **сисресторедлинк** после восстановления любой ссылки, и он должен вызвать эту функцию после восстановления любого файла общего хранилища.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-119">Your restore operation can restore the SIS links and common-store files in any order it chooses; however, it must call **SisRestoredLink** after it restores any link, and it must call this function after it restores any common-store file.</span></span> <span data-ttu-id="2cbd7-120">Так как операция восстановления не может определять, какие файлы общего хранилища будут восстановлены до тех пор, пока имена файлов не будут переданы в результате восстановления связи, операция восстановления всегда восстановит файл общего хранилища после восстановления по крайней мере одной ссылки, ссылающейся на него.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-120">Because your restore operation cannot identify which common-store files will be restored until the file names are reported to it as a result of restoring a link, your restore operation will always restore a common-store file after at least one link referring to it is restored.</span></span> <span data-ttu-id="2cbd7-121">Однако после этого можно восстановить дополнительные ссылки SIS, указывающие на этот файл Common-Store.</span><span class="sxs-lookup"><span data-stu-id="2cbd7-121">However, you can then restore additional SIS links that point to that common-store file.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cbd7-122">Требования</span><span class="sxs-lookup"><span data-stu-id="2cbd7-122">Requirements</span></span>



| <span data-ttu-id="2cbd7-123">Требование</span><span class="sxs-lookup"><span data-stu-id="2cbd7-123">Requirement</span></span> | <span data-ttu-id="2cbd7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="2cbd7-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cbd7-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2cbd7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2cbd7-126">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2cbd7-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2cbd7-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2cbd7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2cbd7-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2cbd7-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2cbd7-129">Header</span><span class="sxs-lookup"><span data-stu-id="2cbd7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cbd7-130"><dt>Сисбкуп. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cbd7-130"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="2cbd7-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2cbd7-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="2cbd7-132"><dt>Сисбкуп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cbd7-132"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="2cbd7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2cbd7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cbd7-134"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cbd7-134"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cbd7-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2cbd7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cbd7-136">**сискреатерестореструктуре**</span><span class="sxs-lookup"><span data-stu-id="2cbd7-136">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="2cbd7-137">**сисресторедлинк**</span><span class="sxs-lookup"><span data-stu-id="2cbd7-137">**SisRestoredLink**</span></span>](sisrestoredlink.md)
</dt> </dl>

 

