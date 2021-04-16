---
description: Возвращает объект ошибки для задания, если оно существует.
ms.assetid: 7E810CBE-F18F-4EFA-B52E-631CD071D136
title: Метод method класса Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 63279d8bc08f0b9f1955f694470a3744defd8054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662462"
---
# <a name="geterror-method-of-the-msvm_concretejob-class"></a><span data-ttu-id="250f2-103">Метод method \_ класса мсвм конкретежоб</span><span class="sxs-lookup"><span data-stu-id="250f2-103">GetError method of the Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="250f2-104">Возвращает объект ошибки для задания, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="250f2-104">Retrieves the error object for the job, if one exists.</span></span> <span data-ttu-id="250f2-105">Если задание выполняется или завершается без ошибок, этот метод не возвращает объект [**\_ ошибки CIM**](/previous-versions//cc150671(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="250f2-105">When the job is executing or has terminated without error, then this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="250f2-106">Однако если задание завершилось сбоем из-за внутренней проблемы или из-за завершения задания клиентом, то возвращается экземпляр **\_ ошибки CIM** .</span><span class="sxs-lookup"><span data-stu-id="250f2-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="250f2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="250f2-107">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="250f2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="250f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="250f2-109">*Ошибка при* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="250f2-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="250f2-110">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="250f2-110">Type: **string**</span></span>

<span data-ttu-id="250f2-111">Если рабочее состояние задания не равно 2 (ОК), этот метод возвращает встроенный экземпляр класса [**\_ ошибок мсвм**](msvm-error.md) в формате CIM-XML.</span><span class="sxs-lookup"><span data-stu-id="250f2-111">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="250f2-112">Если рабочее состояние задания — 2 (ОК), возвращается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="250f2-112">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="250f2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="250f2-113">Return value</span></span>

<span data-ttu-id="250f2-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="250f2-114">Type: **uint32**</span></span>

<span data-ttu-id="250f2-115">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="250f2-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="250f2-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="250f2-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="250f2-117">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="250f2-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="250f2-118">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="250f2-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="250f2-119">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="250f2-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="250f2-120">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="250f2-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="250f2-121">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="250f2-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="250f2-122">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="250f2-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="250f2-123">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="250f2-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="250f2-124">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="250f2-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="250f2-125">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="250f2-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="250f2-126">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="250f2-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="250f2-127">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="250f2-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="250f2-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="250f2-128">Remarks</span></span>

<span data-ttu-id="250f2-129">Доступ к классу [**\_ конкретежоб мсвм**](msvm-concretejob.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="250f2-129">Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="250f2-130">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="250f2-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="250f2-131">Требования</span><span class="sxs-lookup"><span data-stu-id="250f2-131">Requirements</span></span>



| <span data-ttu-id="250f2-132">Требование</span><span class="sxs-lookup"><span data-stu-id="250f2-132">Requirement</span></span> | <span data-ttu-id="250f2-133">Значение</span><span class="sxs-lookup"><span data-stu-id="250f2-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="250f2-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="250f2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="250f2-135">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="250f2-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="250f2-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="250f2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="250f2-137">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="250f2-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="250f2-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="250f2-138">Namespace</span></span><br/>                | <span data-ttu-id="250f2-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="250f2-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="250f2-140">MOF</span><span class="sxs-lookup"><span data-stu-id="250f2-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="250f2-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="250f2-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="250f2-142">DLL</span><span class="sxs-lookup"><span data-stu-id="250f2-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="250f2-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="250f2-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="250f2-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="250f2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="250f2-145">**Мсвм \_ конкретежоб**</span><span class="sxs-lookup"><span data-stu-id="250f2-145">**Msvm\_ConcreteJob**</span></span>](msvm-concretejob.md)
</dt> </dl>

 

