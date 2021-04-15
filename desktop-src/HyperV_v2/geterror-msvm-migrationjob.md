---
description: Возвращает объект ошибки для задания миграции, если оно существует.
ms.assetid: 83a68ded-086a-42d9-b76d-e46af70d9b43
title: Метод method класса Msvm_MigrationJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6dce1cb3728c854b1dac742099a3ca035d4865a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662461"
---
# <a name="geterror-method-of-the-msvm_migrationjob-class"></a><span data-ttu-id="e106a-103">Метод method \_ класса мсвм мигратионжоб</span><span class="sxs-lookup"><span data-stu-id="e106a-103">GetError method of the Msvm\_MigrationJob class</span></span>

<span data-ttu-id="e106a-104">Возвращает объект ошибки для задания миграции, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="e106a-104">Retrieves the error object for the migration job, if one exists.</span></span> <span data-ttu-id="e106a-105">Если задание выполняется или завершается без ошибок, этот метод не возвращает объект [**\_ ошибки CIM**](/previous-versions//cc150671(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e106a-105">When the job is executing or has terminated without error, then this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="e106a-106">Однако если задание завершилось сбоем из-за внутренней проблемы или из-за завершения задания клиентом, то возвращается экземпляр **\_ ошибки CIM** .</span><span class="sxs-lookup"><span data-stu-id="e106a-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="e106a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e106a-107">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="e106a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e106a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e106a-109">*Ошибка при* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e106a-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e106a-110">Если рабочее состояние задания не равно 2 (ОК), этот метод возвращает встроенный экземпляр класса [**\_ ошибок мсвм**](msvm-error.md) в формате CIM-XML.</span><span class="sxs-lookup"><span data-stu-id="e106a-110">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="e106a-111">Если рабочее состояние задания — 2 (ОК), возвращается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="e106a-111">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e106a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e106a-112">Return value</span></span>

<span data-ttu-id="e106a-113">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e106a-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e106a-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="e106a-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e106a-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="e106a-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e106a-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="e106a-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e106a-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="e106a-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e106a-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="e106a-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e106a-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="e106a-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e106a-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="e106a-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e106a-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="e106a-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e106a-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="e106a-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e106a-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="e106a-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e106a-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="e106a-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e106a-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="e106a-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e106a-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e106a-126">Requirements</span></span>



| <span data-ttu-id="e106a-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e106a-127">Requirement</span></span> | <span data-ttu-id="e106a-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e106a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e106a-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e106a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e106a-130">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e106a-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e106a-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e106a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e106a-132">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e106a-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e106a-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e106a-133">Namespace</span></span><br/>                | <span data-ttu-id="e106a-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e106a-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e106a-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e106a-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e106a-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e106a-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e106a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e106a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e106a-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e106a-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e106a-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e106a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e106a-140">**Мсвм \_ мигратионжоб**</span><span class="sxs-lookup"><span data-stu-id="e106a-140">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)
</dt> </dl>

 

