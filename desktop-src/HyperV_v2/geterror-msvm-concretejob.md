---
description: Метод GetObject класса Msvm_ConcreteJob — извлекает объект ошибки для задания, если оно существует.
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
ms.openlocfilehash: c222a7091550b5ee831330f100292549e31ce5ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112192"
---
# <a name="geterror-method-of-the-msvm_concretejob-class"></a><span data-ttu-id="01986-103">Метод method \_ класса мсвм конкретежоб</span><span class="sxs-lookup"><span data-stu-id="01986-103">GetError method of the Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="01986-104">Возвращает объект ошибки для задания, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="01986-104">Retrieves the error object for the job, if one exists.</span></span> <span data-ttu-id="01986-105">Если задание выполняется или завершается без ошибок, этот метод не возвращает объект [**\_ ошибки CIM**](/previous-versions//cc150671(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="01986-105">When the job is executing or has terminated without error, then this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="01986-106">Однако если задание завершилось сбоем из-за внутренней проблемы или из-за завершения задания клиентом, то возвращается экземпляр **\_ ошибки CIM** .</span><span class="sxs-lookup"><span data-stu-id="01986-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="01986-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01986-107">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="01986-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="01986-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01986-109">*Ошибка при* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="01986-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01986-110">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="01986-110">Type: **string**</span></span>

<span data-ttu-id="01986-111">Если рабочее состояние задания не равно 2 (ОК), этот метод возвращает встроенный экземпляр класса [**\_ ошибок мсвм**](msvm-error.md) в формате CIM-XML.</span><span class="sxs-lookup"><span data-stu-id="01986-111">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="01986-112">Если рабочее состояние задания — 2 (ОК), возвращается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="01986-112">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01986-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01986-113">Return value</span></span>

<span data-ttu-id="01986-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01986-114">Type: **uint32**</span></span>

<span data-ttu-id="01986-115">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="01986-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="01986-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="01986-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="01986-117">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="01986-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="01986-118">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="01986-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="01986-119">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="01986-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="01986-120">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="01986-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="01986-121">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="01986-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="01986-122">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="01986-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="01986-123">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="01986-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="01986-124">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="01986-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="01986-125">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="01986-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="01986-126">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="01986-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="01986-127">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="01986-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="01986-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="01986-128">Remarks</span></span>

<span data-ttu-id="01986-129">Доступ к классу [**\_ конкретежоб мсвм**](msvm-concretejob.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="01986-129">Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="01986-130">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="01986-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="01986-131">Требования</span><span class="sxs-lookup"><span data-stu-id="01986-131">Requirements</span></span>



| <span data-ttu-id="01986-132">Требование</span><span class="sxs-lookup"><span data-stu-id="01986-132">Requirement</span></span> | <span data-ttu-id="01986-133">Значение</span><span class="sxs-lookup"><span data-stu-id="01986-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01986-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01986-134">Minimum supported client</span></span><br/> | <span data-ttu-id="01986-135">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="01986-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="01986-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01986-136">Minimum supported server</span></span><br/> | <span data-ttu-id="01986-137">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="01986-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="01986-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="01986-138">Namespace</span></span><br/>                | <span data-ttu-id="01986-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="01986-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="01986-140">MOF</span><span class="sxs-lookup"><span data-stu-id="01986-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01986-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01986-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="01986-142">DLL</span><span class="sxs-lookup"><span data-stu-id="01986-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01986-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="01986-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="01986-144">См. также</span><span class="sxs-lookup"><span data-stu-id="01986-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01986-145">**Мсвм \_ конкретежоб**</span><span class="sxs-lookup"><span data-stu-id="01986-145">**Msvm\_ConcreteJob**</span></span>](msvm-concretejob.md)
</dt> </dl>

 

