---
description: 'Метод Msvm_CopyFileToGuestJob:: Жетеррорекс — получает объекты ошибок для задания, если таковые существуют.'
ms.assetid: 817AF83B-B601-4AE4-AB5B-CFEACB9A7F41
title: 'Метод Msvm_CopyFileToGuestJob:: Жетеррорекс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 81a570c42457257212e83f9c0c034c4a390e4c04
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109672"
---
# <a name="msvm_copyfiletoguestjobgeterrorex-method"></a><span data-ttu-id="dd76f-103">Мсвм \_ копифилетогуестжоб:: жетеррорекс, метод</span><span class="sxs-lookup"><span data-stu-id="dd76f-103">Msvm\_CopyFileToGuestJob::GetErrorEx method</span></span>

<span data-ttu-id="dd76f-104">Возвращает объекты ошибок для задания, если таковые существуют.</span><span class="sxs-lookup"><span data-stu-id="dd76f-104">Retrieves the error objects for the job, if any exist.</span></span> <span data-ttu-id="dd76f-105">При выполнении или завершении задания без ошибок этот метод не возвращает экземпляр [**\_ ошибки мсвм**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="dd76f-105">When the job is executing or has terminated without error, this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="dd76f-106">Однако если задание завершилось сбоем из-за внутренней проблемы или из-за завершения задания клиентом, возвращается один или несколько экземпляров **мсвм \_ Error** .</span><span class="sxs-lookup"><span data-stu-id="dd76f-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd76f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd76f-107">Syntax</span></span>


```C++
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="dd76f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd76f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd76f-109">*Ошибки* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dd76f-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd76f-110">Если рабочее состояние задания не равно 2 (ОК), этот метод возвращает один или несколько внедренных экземпляров класса [**\_ ошибок мсвм**](msvm-error.md) в формате CIM-XML, которые представляют ошибки, возникшие в задании.</span><span class="sxs-lookup"><span data-stu-id="dd76f-110">If the operational status of the job is not 2 (OK), this method returns one or more embedded instances of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format, that represent the errors encountered in the job.</span></span> <span data-ttu-id="dd76f-111">Если рабочее состояние задания — 2 (ОК), возвращается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="dd76f-111">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd76f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd76f-112">Return value</span></span>

<span data-ttu-id="dd76f-113">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="dd76f-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="dd76f-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="dd76f-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dd76f-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="dd76f-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="dd76f-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="dd76f-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="dd76f-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="dd76f-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="dd76f-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="dd76f-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="dd76f-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="dd76f-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="dd76f-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="dd76f-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="dd76f-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="dd76f-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="dd76f-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="dd76f-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="dd76f-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="dd76f-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="dd76f-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="dd76f-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="dd76f-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="dd76f-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="dd76f-126">Требования</span><span class="sxs-lookup"><span data-stu-id="dd76f-126">Requirements</span></span>



| <span data-ttu-id="dd76f-127">Требование</span><span class="sxs-lookup"><span data-stu-id="dd76f-127">Requirement</span></span> | <span data-ttu-id="dd76f-128">Значение</span><span class="sxs-lookup"><span data-stu-id="dd76f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd76f-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd76f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dd76f-130">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dd76f-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="dd76f-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd76f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dd76f-132">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd76f-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dd76f-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dd76f-133">Namespace</span></span><br/>                | <span data-ttu-id="dd76f-134">\\\\Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="dd76f-134">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="dd76f-135">MOF</span><span class="sxs-lookup"><span data-stu-id="dd76f-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd76f-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd76f-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd76f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="dd76f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd76f-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dd76f-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dd76f-139">См. также</span><span class="sxs-lookup"><span data-stu-id="dd76f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd76f-140">**Мсвм \_ копифилетогуестжоб**</span><span class="sxs-lookup"><span data-stu-id="dd76f-140">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




