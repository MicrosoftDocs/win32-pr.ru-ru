---
title: Функция Сисфрибаккупструктуре (Сисбкуп. h)
description: Освобождает указанную структуру резервного копирования SIS.
ms.assetid: 34d5e919-e4bf-4105-ac15-a2ff5adfbdee
keywords:
- Резервное копирование функции Сисфрибаккупструктуре
topic_type:
- apiref
api_name:
- SisFreeBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a135c4787ff116ec10efd61fa1492033393c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801672"
---
# <a name="sisfreebackupstructure-function"></a><span data-ttu-id="d5b7d-104">Функция Сисфрибаккупструктуре</span><span class="sxs-lookup"><span data-stu-id="d5b7d-104">SisFreeBackupStructure function</span></span>

<span data-ttu-id="d5b7d-105">Функция **сисфрибаккупструктуре** освобождает указанную структуру резервного копирования SIS.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-105">The **SisFreeBackupStructure** function frees the specified SIS backup structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5b7d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5b7d-106">Syntax</span></span>


```C++
BOOL SisFreeBackupStructure(
  _In_ PVOID sisBackupStructure
);
```



## <a name="parameters"></a><span data-ttu-id="d5b7d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5b7d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5b7d-108">*сисбаккупструктуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5b7d-108">*sisBackupStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5b7d-109">Указатель на структуру резервного копирования SIS, возвращенную из [**сискреатебаккупструктуре**](siscreatebackupstructure.md).</span><span class="sxs-lookup"><span data-stu-id="d5b7d-109">Pointer to the SIS backup structure returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5b7d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5b7d-110">Return value</span></span>

<span data-ttu-id="d5b7d-111">Эта функция возвращает **значение true** , если она завершается успешно, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-111">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="d5b7d-112">Вызовите [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) , чтобы получить дополнительные сведения о причине сбоя вызова.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-112">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5b7d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5b7d-113">Remarks</span></span>

<span data-ttu-id="d5b7d-114">Эта функция должна вызываться после завершения операции резервного копирования для тома, определенного значением параметра *сисбаккупструктуре* .</span><span class="sxs-lookup"><span data-stu-id="d5b7d-114">This function should be called after the backup operation is completed for the volume identified by the value of the *sisBackupStructure* parameter.</span></span>

<span data-ttu-id="d5b7d-115">Обратите внимание, что нельзя предположить, что это освобождает только память.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-115">Note that it is not safe to assume that this only deallocates memory.</span></span> <span data-ttu-id="d5b7d-116">Например, эта функция может также выполнять дополнительные административные операции для архитектуры SIS.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-116">For example, this function may also perform additional administrative operations for the SIS architecture.</span></span> <span data-ttu-id="d5b7d-117">Поэтому Вызывайте эту функцию, даже если операция резервного копирования будет завершена сразу же после этого.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-117">Therefore, call this function even if your backup operation will exit immediately afterward.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5b7d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d5b7d-118">Requirements</span></span>



| <span data-ttu-id="d5b7d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d5b7d-119">Requirement</span></span> | <span data-ttu-id="d5b7d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d5b7d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5b7d-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5b7d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d5b7d-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d5b7d-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d5b7d-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5b7d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d5b7d-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d5b7d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d5b7d-125">Header</span><span class="sxs-lookup"><span data-stu-id="d5b7d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5b7d-126"><dt>Сисбкуп. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5b7d-126"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="d5b7d-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d5b7d-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5b7d-128"><dt>Сисбкуп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5b7d-128"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="d5b7d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d5b7d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5b7d-130"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5b7d-130"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5b7d-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5b7d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5b7d-132">**сискреатебаккупструктуре**</span><span class="sxs-lookup"><span data-stu-id="d5b7d-132">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> </dl>

 

