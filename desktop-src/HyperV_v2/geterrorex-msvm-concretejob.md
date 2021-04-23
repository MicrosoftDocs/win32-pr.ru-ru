---
description: Возвращает объекты ошибок для задания, если таковые существуют.
ms.assetid: B4B4F60C-9221-4125-8D42-F0F1D32C3E79
title: Метод Жетеррорекс класса Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e938d41afad430051bebb08fc77d6edf6da44691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682795"
---
# <a name="geterrorex-method-of-the-msvm_concretejob-class"></a><span data-ttu-id="68159-103">Метод Жетеррорекс \_ класса Конкретежоб мсвм</span><span class="sxs-lookup"><span data-stu-id="68159-103">GetErrorEx method of the Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="68159-104">Возвращает объекты ошибок для задания, если таковые существуют.</span><span class="sxs-lookup"><span data-stu-id="68159-104">Retrieves the error objects for the job, if any exist.</span></span> <span data-ttu-id="68159-105">При выполнении или завершении задания без ошибок этот метод не возвращает экземпляр [**\_ ошибки мсвм**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="68159-105">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="68159-106">Однако если задание завершилось сбоем из-за внутренней проблемы или из-за завершения задания клиентом, возвращается один или несколько экземпляров **мсвм \_ Error** .</span><span class="sxs-lookup"><span data-stu-id="68159-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="68159-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68159-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="68159-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="68159-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68159-109">*Ошибки* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="68159-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68159-110">Тип: **строка \[ \]**</span><span class="sxs-lookup"><span data-stu-id="68159-110">Type: **string\[\]**</span></span>

<span data-ttu-id="68159-111">Если рабочее состояние задания не равно 2 (ОК), этот метод возвращает один или несколько внедренных экземпляров класса [**\_ ошибок мсвм**](msvm-error.md) в формате CIM-XML, которые представляют ошибки, возникшие в задании.</span><span class="sxs-lookup"><span data-stu-id="68159-111">If the operational status of the job is not 2 (OK), this method returns one or more embedded instances of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format, that represent the errors encountered in the job.</span></span> <span data-ttu-id="68159-112">Если рабочее состояние задания — 2 (ОК), возвращается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="68159-112">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68159-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68159-113">Return value</span></span>

<span data-ttu-id="68159-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68159-114">Type: **uint32**</span></span>

<span data-ttu-id="68159-115">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="68159-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="68159-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="68159-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="68159-117">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="68159-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="68159-118">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="68159-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="68159-119">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="68159-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="68159-120">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="68159-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="68159-121">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="68159-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="68159-122">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="68159-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="68159-123">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="68159-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="68159-124">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="68159-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="68159-125">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="68159-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="68159-126">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="68159-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="68159-127">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="68159-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="68159-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68159-128">Remarks</span></span>

<span data-ttu-id="68159-129">Доступ к классу [**\_ конкретежоб мсвм**](msvm-concretejob.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="68159-129">Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="68159-130">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="68159-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="68159-131">Требования</span><span class="sxs-lookup"><span data-stu-id="68159-131">Requirements</span></span>



| <span data-ttu-id="68159-132">Требование</span><span class="sxs-lookup"><span data-stu-id="68159-132">Requirement</span></span> | <span data-ttu-id="68159-133">Значение</span><span class="sxs-lookup"><span data-stu-id="68159-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68159-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68159-134">Minimum supported client</span></span><br/> | <span data-ttu-id="68159-135">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="68159-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="68159-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68159-136">Minimum supported server</span></span><br/> | <span data-ttu-id="68159-137">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="68159-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="68159-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="68159-138">Namespace</span></span><br/>                | <span data-ttu-id="68159-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="68159-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="68159-140">MOF</span><span class="sxs-lookup"><span data-stu-id="68159-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68159-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68159-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="68159-142">DLL</span><span class="sxs-lookup"><span data-stu-id="68159-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68159-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="68159-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="68159-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68159-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68159-145">**Мсвм \_ конкретежоб**</span><span class="sxs-lookup"><span data-stu-id="68159-145">**Msvm\_ConcreteJob**</span></span>](msvm-concretejob.md)
</dt> </dl>

 

