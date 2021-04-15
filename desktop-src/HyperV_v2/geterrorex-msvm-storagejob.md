---
description: При выполнении или завершении задания без ошибок этот метод не возвращает \_ экземпляр ошибки мсвм.
ms.assetid: 119E7EFD-78C9-46F1-8A53-C51A7A34B32E
title: Метод Жетеррорекс класса Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 26d5aff37631de00cffccd49cf54f0ba09ce5a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662459"
---
# <a name="geterrorex-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="237dc-103">Метод Жетеррорекс \_ класса Сторажежоб мсвм</span><span class="sxs-lookup"><span data-stu-id="237dc-103">GetErrorEx method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="237dc-104">При выполнении или завершении задания без ошибок этот метод не возвращает экземпляр [**\_ ошибки мсвм**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="237dc-104">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="237dc-105">Однако если задание завершилось сбоем из-за внутренней проблемы или из-за завершения задания клиентом, возвращается один или несколько экземпляров **мсвм \_ Error** .</span><span class="sxs-lookup"><span data-stu-id="237dc-105">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="237dc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="237dc-106">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="237dc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="237dc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="237dc-108">*Ошибки* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="237dc-108">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="237dc-109">Тип: **строка \[ \]**</span><span class="sxs-lookup"><span data-stu-id="237dc-109">Type: **string\[\]**</span></span>

<span data-ttu-id="237dc-110">Если оперативное состояние задания не равно "ОК", этот метод возвращает массив экземпляров [**\_ ошибок мсвм**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="237dc-110">If the operational status of the job is not "OK", this method returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="237dc-111">В противном случае, если задано "ОК", возвращается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="237dc-111">Otherwise, if the job is "OK", **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="237dc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="237dc-112">Return value</span></span>

<span data-ttu-id="237dc-113">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="237dc-113">Type: **uint32**</span></span>

<span data-ttu-id="237dc-114">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="237dc-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="237dc-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="237dc-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="237dc-116">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="237dc-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="237dc-117">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="237dc-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="237dc-118">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="237dc-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="237dc-119">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="237dc-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="237dc-120">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="237dc-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="237dc-121">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="237dc-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="237dc-122">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="237dc-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="237dc-123">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="237dc-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="237dc-124">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="237dc-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="237dc-125">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="237dc-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="237dc-126">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="237dc-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="237dc-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="237dc-127">Remarks</span></span>

<span data-ttu-id="237dc-128">Доступ к классу [**\_ сторажежоб мсвм**](msvm-storagejob.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="237dc-128">Access to the [**Msvm\_StorageJob**](msvm-storagejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="237dc-129">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="237dc-129">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="237dc-130">Требования</span><span class="sxs-lookup"><span data-stu-id="237dc-130">Requirements</span></span>



| <span data-ttu-id="237dc-131">Требование</span><span class="sxs-lookup"><span data-stu-id="237dc-131">Requirement</span></span> | <span data-ttu-id="237dc-132">Значение</span><span class="sxs-lookup"><span data-stu-id="237dc-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="237dc-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="237dc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="237dc-134">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="237dc-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="237dc-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="237dc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="237dc-136">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="237dc-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="237dc-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="237dc-137">Namespace</span></span><br/>                | <span data-ttu-id="237dc-138">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="237dc-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="237dc-139">MOF</span><span class="sxs-lookup"><span data-stu-id="237dc-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="237dc-140"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="237dc-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="237dc-141">DLL</span><span class="sxs-lookup"><span data-stu-id="237dc-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="237dc-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="237dc-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="237dc-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="237dc-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="237dc-144">**Мсвм \_ сторажежоб**</span><span class="sxs-lookup"><span data-stu-id="237dc-144">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

