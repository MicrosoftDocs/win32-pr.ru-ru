---
title: Функция Сисфрирестореструктуре (Сисбкуп. h)
description: Освобождает память, выделенную для указанной структуры восстановления SIS, и выполняет задачи, подготавливающие фильтр SIS для правильной настройки ссылок, созданных во время операции восстановления.
ms.assetid: dbdccb53-b38e-465d-a6d0-ee86923a5879
keywords:
- Резервное копирование функции Сисфрирестореструктуре
topic_type:
- apiref
api_name:
- SisFreeRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7293514d798fe65c82863a83549039b05ec8eb3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492621"
---
# <a name="sisfreerestorestructure-function"></a><span data-ttu-id="3c36d-104">Функция Сисфрирестореструктуре</span><span class="sxs-lookup"><span data-stu-id="3c36d-104">SisFreeRestoreStructure function</span></span>

<span data-ttu-id="3c36d-105">Функция **сисфрирестореструктуре** освобождает память, выделенную для указанной структуры восстановления SIS, и выполняет задачи, подготавливающие фильтр SIS для правильной настройки ссылок, созданных во время операции восстановления.</span><span class="sxs-lookup"><span data-stu-id="3c36d-105">The **SisFreeRestoreStructure** function frees the memory allocated for the specified SIS restore structure, and performs tasks that prepare the SIS filter to properly set up the links created during the restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c36d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c36d-106">Syntax</span></span>


```C++
BOOL SisFreeRestoreStructure(
  _In_ PVOID sisRestoreStructure
);
```



## <a name="parameters"></a><span data-ttu-id="3c36d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c36d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c36d-108">*сисрестореструктуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c36d-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c36d-109">Указатель на структуру восстановления SIS, возвращенную из [**сискреатерестореструктуре**](siscreaterestorestructure.md).</span><span class="sxs-lookup"><span data-stu-id="3c36d-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c36d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c36d-110">Return value</span></span>

<span data-ttu-id="3c36d-111">Эта функция возвращает **значение true** , если она завершается успешно, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3c36d-111">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="3c36d-112">Вызовите [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) , чтобы получить дополнительные сведения о причине сбоя вызова.</span><span class="sxs-lookup"><span data-stu-id="3c36d-112">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c36d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c36d-113">Remarks</span></span>

<span data-ttu-id="3c36d-114">Доступ к ссылкам SIS до завершения вызова этой функции может привести к проверке тома или частичному чтению содержимого ссылки.</span><span class="sxs-lookup"><span data-stu-id="3c36d-114">Accessing the SIS links before the call to this function completes can result in a volume check or a partial read of the link's contents.</span></span>

<span data-ttu-id="3c36d-115">Обратите внимание, что нельзя предположить, что это освобождает только память.</span><span class="sxs-lookup"><span data-stu-id="3c36d-115">Note that it is not safe to assume that this only deallocates memory.</span></span> <span data-ttu-id="3c36d-116">Например, эта функция может также выполнять дополнительные административные операции для архитектуры SIS.</span><span class="sxs-lookup"><span data-stu-id="3c36d-116">For example, this function may also perform additional administrative operations for the SIS architecture.</span></span> <span data-ttu-id="3c36d-117">Поэтому Вызывайте эту функцию, даже если операция восстановления будет завершена сразу же после этого.</span><span class="sxs-lookup"><span data-stu-id="3c36d-117">Therefore, call this function even if your restore operation will exit immediately afterward.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c36d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="3c36d-118">Requirements</span></span>



| <span data-ttu-id="3c36d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="3c36d-119">Requirement</span></span> | <span data-ttu-id="3c36d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="3c36d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c36d-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c36d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3c36d-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3c36d-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3c36d-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c36d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3c36d-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3c36d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3c36d-125">Header</span><span class="sxs-lookup"><span data-stu-id="3c36d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c36d-126"><dt>Сисбкуп. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c36d-126"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c36d-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3c36d-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c36d-128"><dt>Сисбкуп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c36d-128"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="3c36d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3c36d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c36d-130"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c36d-130"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c36d-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c36d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c36d-132">**сискреатерестореструктуре**</span><span class="sxs-lookup"><span data-stu-id="3c36d-132">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> </dl>

 

