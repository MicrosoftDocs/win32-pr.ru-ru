---
description: Метод Msvm_CopyFileToGuestJob::-Error — извлекает объект ошибки для задания, если оно существует.
ms.assetid: 478E9170-A523-4CE1-BD97-57D713FAF71B
title: 'Метод Msvm_CopyFileToGuestJob:: с ошибкой'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7cecaf7254788ae064ca42f2ae0c26e8ad83d7e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119372"
---
# <a name="msvm_copyfiletoguestjobgeterror-method"></a><span data-ttu-id="7a5b2-103">Мсвм \_ копифилетогуестжоб:: метод Error</span><span class="sxs-lookup"><span data-stu-id="7a5b2-103">Msvm\_CopyFileToGuestJob::GetError method</span></span>

<span data-ttu-id="7a5b2-104">Возвращает объект ошибки для задания, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="7a5b2-104">Retrieves the error object for the job, if one exists.</span></span> <span data-ttu-id="7a5b2-105">Если задание выполняется или завершается без ошибок, этот метод не возвращает объект [**\_ ошибки CIM**](/previous-versions//cc150671(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7a5b2-105">When the job is executing or has terminated without error, this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="7a5b2-106">Однако если задание завершилось сбоем из-за внутренней проблемы или из-за завершения задания клиентом, возвращается экземпляр **\_ ошибки CIM** .</span><span class="sxs-lookup"><span data-stu-id="7a5b2-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a5b2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a5b2-107">Syntax</span></span>


```C++
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="7a5b2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a5b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a5b2-109">*Ошибка при* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7a5b2-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a5b2-110">Если рабочее состояние задания не равно 2 (ОК), этот метод возвращает встроенный экземпляр класса [**\_ ошибок мсвм**](msvm-error.md) в формате CIM-XML.</span><span class="sxs-lookup"><span data-stu-id="7a5b2-110">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="7a5b2-111">Если рабочее состояние задания — 2 (ОК), возвращается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="7a5b2-111">If the operational status of the job is 2 (OK), **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a5b2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a5b2-112">Return value</span></span>

<span data-ttu-id="7a5b2-113">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7a5b2-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7a5b2-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="7a5b2-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7a5b2-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="7a5b2-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="7a5b2-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="7a5b2-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="7a5b2-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="7a5b2-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="7a5b2-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="7a5b2-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="7a5b2-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="7a5b2-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="7a5b2-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="7a5b2-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="7a5b2-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="7a5b2-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="7a5b2-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="7a5b2-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="7a5b2-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="7a5b2-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="7a5b2-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="7a5b2-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="7a5b2-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="7a5b2-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7a5b2-126">Требования</span><span class="sxs-lookup"><span data-stu-id="7a5b2-126">Requirements</span></span>



| <span data-ttu-id="7a5b2-127">Требование</span><span class="sxs-lookup"><span data-stu-id="7a5b2-127">Requirement</span></span> | <span data-ttu-id="7a5b2-128">Значение</span><span class="sxs-lookup"><span data-stu-id="7a5b2-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a5b2-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a5b2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7a5b2-130">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7a5b2-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="7a5b2-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a5b2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7a5b2-132">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7a5b2-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7a5b2-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7a5b2-133">Namespace</span></span><br/>                | <span data-ttu-id="7a5b2-134">\\\\Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7a5b2-134">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="7a5b2-135">MOF</span><span class="sxs-lookup"><span data-stu-id="7a5b2-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a5b2-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a5b2-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a5b2-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7a5b2-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a5b2-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7a5b2-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7a5b2-139">См. также</span><span class="sxs-lookup"><span data-stu-id="7a5b2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a5b2-140">**Мсвм \_ копифилетогуестжоб**</span><span class="sxs-lookup"><span data-stu-id="7a5b2-140">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

