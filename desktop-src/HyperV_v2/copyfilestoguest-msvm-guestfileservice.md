---
description: Копирует файлы с узла Hyper-V на виртуальную машину.
ms.assetid: 76667557-13B2-4286-BC6B-E32FADE62A7A
title: 'Метод Msvm_GuestFileService:: Копифилестогуест'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService.CopyFilesToGuest
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9424dee6d28e0bd9cd6ac43c15ad27cdebdb7017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663743"
---
# <a name="msvm_guestfileservicecopyfilestoguest-method"></a><span data-ttu-id="0aef5-103">Мсвм \_ гуестфилесервице:: копифилестогуест, метод</span><span class="sxs-lookup"><span data-stu-id="0aef5-103">Msvm\_GuestFileService::CopyFilesToGuest method</span></span>

<span data-ttu-id="0aef5-104">Копирует файлы с узла Hyper-V на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="0aef5-104">Copies files from the Hyper-V host to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aef5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0aef5-105">Syntax</span></span>


```C++
uint32 CopyFilesToGuest(
  [in]            string                  CopyFileToGuestSettings[],
  [out]           CIM_ConcreteJob     Job,
  [out, optional] Msvm_CopyFileToGuestJob ParentPools[]
);
```



## <a name="parameters"></a><span data-ttu-id="0aef5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0aef5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aef5-107">*Копифилетогуестсеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0aef5-107">*CopyFileToGuestSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aef5-108">Массив экземпляров класса [**мсвм \_ копифилетогуестсеттингдата**](msvm-copyfiletoguestsettingdata.md) , представляющий задание операции гостевой файловой службы.</span><span class="sxs-lookup"><span data-stu-id="0aef5-108">An array of instances of the [**Msvm\_CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md) class that represents a guest file service operation job.</span></span>

</dd> <dt>

<span data-ttu-id="0aef5-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0aef5-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0aef5-110">Необязательный параметр для отслеживания хода выполнения операции, который используется, если метод не может быть выполнен синхронно.</span><span class="sxs-lookup"><span data-stu-id="0aef5-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="0aef5-111">Если операция выполняется асинхронно, возвращается значение 4096.</span><span class="sxs-lookup"><span data-stu-id="0aef5-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

> [!Note]  
> <span data-ttu-id="0aef5-112">Этот параметр был добавлен в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0aef5-112">This parameter was added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="0aef5-113">*Парентпулс* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="0aef5-113">*ParentPools* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0aef5-114">Необязательный массив ссылок на [**мсвм \_ копифилетогуестжоб**](msvm-copyfiletoguestjob.md) , которые используются для отслеживания хода выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="0aef5-114">An optional array of [**Msvm\_CopyFileToGuestJob**](msvm-copyfiletoguestjob.md) references that are used for monitoring progress of the operation.</span></span> <span data-ttu-id="0aef5-115">**Копифилестогуест** использует *парентпулс* , если он не может выполняться синхронно.</span><span class="sxs-lookup"><span data-stu-id="0aef5-115">**CopyFilesToGuest** uses *ParentPools* if it can't execute synchronously.</span></span> <span data-ttu-id="0aef5-116">Если операция выполняется асинхронно, возвращается значение 4096.</span><span class="sxs-lookup"><span data-stu-id="0aef5-116">If the operation executes asynchronously, the return value is 4096.</span></span>

> [!Note]  
> <span data-ttu-id="0aef5-117">Этот параметр был удален в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0aef5-117">This parameter was removed in Windows 10.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aef5-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0aef5-118">Return value</span></span>

<span data-ttu-id="0aef5-119">При успешном выполнении возвращает 0; в противном случае возвращает значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="0aef5-119">On success, returns 0; otherwise, returns an error value.</span></span>

<dl> <dt>

<span data-ttu-id="0aef5-120">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="0aef5-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0aef5-121">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="0aef5-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0aef5-122">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="0aef5-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0aef5-123">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="0aef5-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0aef5-124">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="0aef5-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0aef5-125">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="0aef5-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0aef5-126">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="0aef5-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0aef5-127">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="0aef5-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0aef5-128">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="0aef5-128">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0aef5-129">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="0aef5-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0aef5-130">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="0aef5-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0aef5-131">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="0aef5-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0aef5-132">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="0aef5-132">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0aef5-133">Требования</span><span class="sxs-lookup"><span data-stu-id="0aef5-133">Requirements</span></span>



| <span data-ttu-id="0aef5-134">Требование</span><span class="sxs-lookup"><span data-stu-id="0aef5-134">Requirement</span></span> | <span data-ttu-id="0aef5-135">Значение</span><span class="sxs-lookup"><span data-stu-id="0aef5-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aef5-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0aef5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0aef5-137">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0aef5-137">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="0aef5-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0aef5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0aef5-139">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0aef5-139">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0aef5-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0aef5-140">Namespace</span></span><br/>                | <span data-ttu-id="0aef5-141">\\\\Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0aef5-141">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="0aef5-142">MOF</span><span class="sxs-lookup"><span data-stu-id="0aef5-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0aef5-143"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0aef5-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0aef5-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0aef5-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0aef5-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0aef5-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0aef5-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0aef5-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aef5-147">**Мсвм \_ гуестфилесервице**</span><span class="sxs-lookup"><span data-stu-id="0aef5-147">**Msvm\_GuestFileService**</span></span>](msvm-guestfileservice.md)
</dt> </dl>

 

 




