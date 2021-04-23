---
description: Возвращает объекты ошибок для задания миграции, если они существуют.
ms.assetid: 8526e28c-bfc8-42b3-850c-0a875a52a42c
title: Метод Жетеррорекс класса Msvm_MigrationJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b51bc0c439add0e0959d3fd375fad477e51ba35f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682794"
---
# <a name="geterrorex-method-of-the-msvm_migrationjob-class"></a><span data-ttu-id="dab9c-103">Метод Жетеррорекс \_ класса Мигратионжоб мсвм</span><span class="sxs-lookup"><span data-stu-id="dab9c-103">GetErrorEx method of the Msvm\_MigrationJob class</span></span>

<span data-ttu-id="dab9c-104">Возвращает объекты ошибок для задания миграции, если они существуют.</span><span class="sxs-lookup"><span data-stu-id="dab9c-104">Retrieves the error objects for the migration job, if any exist.</span></span> <span data-ttu-id="dab9c-105">При выполнении или завершении задания без ошибок этот метод не возвращает экземпляр [**\_ ошибки мсвм**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="dab9c-105">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="dab9c-106">Однако если задание завершилось сбоем из-за внутренней проблемы или из-за завершения задания клиентом, возвращается один или несколько экземпляров **мсвм \_ Error** .</span><span class="sxs-lookup"><span data-stu-id="dab9c-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="dab9c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dab9c-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="dab9c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dab9c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dab9c-109">*Ошибки* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dab9c-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dab9c-110">Если рабочее состояние задания не равно 2 (ОК), этот метод возвращает один или несколько внедренных экземпляров класса [**\_ ошибок мсвм**](msvm-error.md) в формате CIM-XML, которые представляют ошибки, возникшие в задании.</span><span class="sxs-lookup"><span data-stu-id="dab9c-110">If the operational status of the job is not 2 (OK), this method returns one or more embedded instances of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format, that represent the errors encountered in the job.</span></span> <span data-ttu-id="dab9c-111">Если рабочее состояние задания — 2 (ОК), возвращается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="dab9c-111">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dab9c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dab9c-112">Return value</span></span>

<span data-ttu-id="dab9c-113">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="dab9c-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="dab9c-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="dab9c-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dab9c-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="dab9c-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="dab9c-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="dab9c-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="dab9c-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="dab9c-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="dab9c-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="dab9c-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="dab9c-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="dab9c-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="dab9c-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="dab9c-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="dab9c-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="dab9c-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="dab9c-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="dab9c-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="dab9c-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="dab9c-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="dab9c-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="dab9c-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="dab9c-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="dab9c-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="dab9c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="dab9c-126">Requirements</span></span>



| <span data-ttu-id="dab9c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="dab9c-127">Requirement</span></span> | <span data-ttu-id="dab9c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="dab9c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dab9c-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dab9c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dab9c-130">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dab9c-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dab9c-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dab9c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dab9c-132">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dab9c-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dab9c-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dab9c-133">Namespace</span></span><br/>                | <span data-ttu-id="dab9c-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="dab9c-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dab9c-135">MOF</span><span class="sxs-lookup"><span data-stu-id="dab9c-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dab9c-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dab9c-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dab9c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="dab9c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dab9c-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dab9c-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dab9c-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dab9c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dab9c-140">**Мсвм \_ мигратионжоб**</span><span class="sxs-lookup"><span data-stu-id="dab9c-140">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)
</dt> </dl>

 

 




