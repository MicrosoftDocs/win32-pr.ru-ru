---
description: Инициирует восстановление размещения для виртуальной машины восстановления.
ms.assetid: F4AE1911-46B2-4412-A17F-3CA7D388276F
title: 'Метод Msvm_ReplicationService:: Инитиатефаилбакк'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailback
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b356982296427212287ea11b528a7878dc166245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662719"
---
# <a name="msvm_replicationserviceinitiatefailback-method"></a><span data-ttu-id="94dde-103">Мсвм \_ репликатионсервице:: инитиатефаилбакк, метод</span><span class="sxs-lookup"><span data-stu-id="94dde-103">Msvm\_ReplicationService::InitiateFailback method</span></span>

<span data-ttu-id="94dde-104">Инициирует восстановление размещения для виртуальной машины восстановления.</span><span class="sxs-lookup"><span data-stu-id="94dde-104">Initiates the failback for a recovery virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="94dde-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94dde-105">Syntax</span></span>


```C++
uint32 InitiateFailback(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [in]  string                 RecoveryPointIdentifier,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="94dde-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="94dde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94dde-107">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94dde-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94dde-108">Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину, для которой необходимо инициировать восстановление размещения.</span><span class="sxs-lookup"><span data-stu-id="94dde-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to initiate a failback.</span></span>

</dd> <dt>

<span data-ttu-id="94dde-109">*Репликатионсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94dde-109">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94dde-110">Строковое представление внедренного экземпляра класса [**мсвм \_ репликатионсеттингдата**](msvm-replicationsettingdata.md) , определяющего параметры репликации для восстановления размещения.</span><span class="sxs-lookup"><span data-stu-id="94dde-110">A string representation of an embedded instance of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the replication settings for the failback.</span></span>

</dd> <dt>

<span data-ttu-id="94dde-111">*Рековерипоинтидентифиер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94dde-111">*RecoveryPointIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94dde-112">Необязательный ввод, определяющий точку восстановления, в которую запрашивается восстановление размещения.</span><span class="sxs-lookup"><span data-stu-id="94dde-112">Optional input that identifies the recovery point to which failback is requested.</span></span>

</dd> <dt>

<span data-ttu-id="94dde-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="94dde-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94dde-114">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94dde-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="94dde-115">Эта ссылка может использоваться для отслеживания хода выполнения и получения результата метода.</span><span class="sxs-lookup"><span data-stu-id="94dde-115">This reference can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94dde-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94dde-116">Return value</span></span>

<span data-ttu-id="94dde-117">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="94dde-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="94dde-118">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="94dde-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="94dde-119">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="94dde-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="94dde-120">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="94dde-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="94dde-121">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="94dde-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="94dde-122">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="94dde-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="94dde-123">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="94dde-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="94dde-124">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="94dde-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="94dde-125">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="94dde-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="94dde-126">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="94dde-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="94dde-127">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="94dde-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="94dde-128">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="94dde-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="94dde-129">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="94dde-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="94dde-130">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="94dde-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="94dde-131">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="94dde-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="94dde-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94dde-132">Remarks</span></span>

<span data-ttu-id="94dde-133">**Инитиатефаилбакк** работает на виртуальной машине восстановления и переводит виртуальную машину в состояние *ваитингфорфаилбакк* .</span><span class="sxs-lookup"><span data-stu-id="94dde-133">**InitiateFailback** works on a recovery virtual machine and takes the virtual machine to *WaitingForFailback* state.</span></span> <span data-ttu-id="94dde-134">**Инитиатефаилбакк** перенаправляет запрос на восстановление размещения соответствующему поставщику, который выполняет обратную синхронизацию точки восстановления с новой стороны.</span><span class="sxs-lookup"><span data-stu-id="94dde-134">**InitiateFailback** forwards the failback request to the corresponding provider, which reverse-resyncs the recovery point from new-primary side.</span></span> <span data-ttu-id="94dde-135">После завершения восстановления размещения запрошенной точки восстановления состояние репликации переходит в состояние *фаилбакккомплетед* .</span><span class="sxs-lookup"><span data-stu-id="94dde-135">After failback of the requested recovery point completes, the replication state moves to *FailbackCompleted* state.</span></span>

## <a name="requirements"></a><span data-ttu-id="94dde-136">Требования</span><span class="sxs-lookup"><span data-stu-id="94dde-136">Requirements</span></span>



| <span data-ttu-id="94dde-137">Требование</span><span class="sxs-lookup"><span data-stu-id="94dde-137">Requirement</span></span> | <span data-ttu-id="94dde-138">Значение</span><span class="sxs-lookup"><span data-stu-id="94dde-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94dde-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94dde-139">Minimum supported client</span></span><br/> | <span data-ttu-id="94dde-140">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="94dde-140">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="94dde-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94dde-141">Minimum supported server</span></span><br/> | <span data-ttu-id="94dde-142">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="94dde-142">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="94dde-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="94dde-143">Namespace</span></span><br/>                | <span data-ttu-id="94dde-144">\\\\Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="94dde-144">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="94dde-145">MOF</span><span class="sxs-lookup"><span data-stu-id="94dde-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94dde-146"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94dde-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="94dde-147">DLL</span><span class="sxs-lookup"><span data-stu-id="94dde-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94dde-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="94dde-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="94dde-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94dde-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94dde-150">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="94dde-150">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

