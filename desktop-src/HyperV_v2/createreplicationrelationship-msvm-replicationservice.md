---
description: Создает новое отношение репликации для виртуальной машины. Когда клиент вызывает этот метод для реплики виртуальной машины, он расширяет отношение репликации с указанным поставщиком.
ms.assetid: 44d3b5aa-46c2-4fe9-9a1d-6ee699d3640d
title: Метод CreateReplicationRelationship класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.CreateReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c44628aef9aa278170a1292a74621419bb6256b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663737"
---
# <a name="createreplicationrelationship-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="6d8f4-104">Метод CreateReplicationRelationship \_ класса Репликатионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="6d8f4-104">CreateReplicationRelationship method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="6d8f4-105">Создает новое отношение репликации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6d8f4-105">Creates a new replication relationship for a virtual machine.</span></span> <span data-ttu-id="6d8f4-106">Когда клиент вызывает этот метод для реплики виртуальной машины, он расширяет отношение репликации с указанным поставщиком.</span><span class="sxs-lookup"><span data-stu-id="6d8f4-106">When a client calls this method for a replica virtual machine, it extends the replication relationship to the specified provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d8f4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d8f4-107">Syntax</span></span>


```mof
uint32 CreateReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6d8f4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d8f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d8f4-109">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d8f4-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d8f4-110">Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину, для которой должна быть включена репликация.</span><span class="sxs-lookup"><span data-stu-id="6d8f4-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="6d8f4-111">*Репликатионсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d8f4-111">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d8f4-112">Строковое представление экземпляра класса [**мсвм \_ репликатионсеттингдата**](msvm-replicationsettingdata.md) , определяющего параметры репликации для нового отношения репликации, создаваемого для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6d8f4-112">A string representation of an instance of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the replication settings for the new replication relationship to be created for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="6d8f4-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6d8f4-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d8f4-114">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6d8f4-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d8f4-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d8f4-115">Return value</span></span>

<span data-ttu-id="6d8f4-116">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6d8f4-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6d8f4-117">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6d8f4-118">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6d8f4-119">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6d8f4-120">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6d8f4-121">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6d8f4-122">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6d8f4-123">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6d8f4-124">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6d8f4-125">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6d8f4-126">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6d8f4-127">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6d8f4-128">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6d8f4-129">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="6d8f4-130">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="6d8f4-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d8f4-131">Remarks</span></span>

<span data-ttu-id="6d8f4-132">**CreateReplicationRelationship** принимает экземпляр [**МСВМ \_ репликатионсеттингдата**](msvm-replicationsettingdata.md) (фрсд) в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="6d8f4-132">**CreateReplicationRelationship** takes an [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) instance (FRSD) as input.</span></span> <span data-ttu-id="6d8f4-133">По умолчанию используется связанный ФРСД для виртуальной машины в качестве поставщика услуг размещения.</span><span class="sxs-lookup"><span data-stu-id="6d8f4-133">The associated FRSD for the virtual machine as host-to-host provider is the default choice.</span></span> <span data-ttu-id="6d8f4-134">Входные ФРСД проверяются на допустимые параметры для каждого свойства для поставщика по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6d8f4-134">Input FRSD is validated for valid settings for each property for the default provider.</span></span> <span data-ttu-id="6d8f4-135">В этой таблице перечислены различия проверки по отношению к внешнему поставщику.</span><span class="sxs-lookup"><span data-stu-id="6d8f4-135">This table summarizes the validation differences with respect to the external provider.</span></span>



| <span data-ttu-id="6d8f4-136">Свойство</span><span class="sxs-lookup"><span data-stu-id="6d8f4-136">Property</span></span>                                             | <span data-ttu-id="6d8f4-137">Внешние поставщики</span><span class="sxs-lookup"><span data-stu-id="6d8f4-137">External providers</span></span>                                 |
|------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="6d8f4-138">репликатионпровидер</span><span class="sxs-lookup"><span data-stu-id="6d8f4-138">ReplicationProvider</span></span>                                  | <span data-ttu-id="6d8f4-139">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6d8f4-139">Same as default provider</span></span>                           |
| <span data-ttu-id="6d8f4-140">authenticationType</span><span class="sxs-lookup"><span data-stu-id="6d8f4-140">AuthenticationType</span></span>                                   | <span data-ttu-id="6d8f4-141">Не учитывается</span><span class="sxs-lookup"><span data-stu-id="6d8f4-141">Ignored</span></span>                                            |
| <span data-ttu-id="6d8f4-142">CertificateThumbPrint</span><span class="sxs-lookup"><span data-stu-id="6d8f4-142">CertificateThumbPrint</span></span>                                | <span data-ttu-id="6d8f4-143">Не учитывается</span><span class="sxs-lookup"><span data-stu-id="6d8f4-143">Ignored</span></span>                                            |
| <span data-ttu-id="6d8f4-144">Рутцертификатесумбпринт (RO)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-144">RootCertificateThumbPrint (RO)</span></span>                       | <span data-ttu-id="6d8f4-145">Не учитывается</span><span class="sxs-lookup"><span data-stu-id="6d8f4-145">Ignored</span></span>                                            |
| <span data-ttu-id="6d8f4-146">компрессионенаблед</span><span class="sxs-lookup"><span data-stu-id="6d8f4-146">CompressionEnabled</span></span>                                   | <span data-ttu-id="6d8f4-147">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6d8f4-147">Same as default provider</span></span>                           |
| <span data-ttu-id="6d8f4-148">бипасспроксисервер</span><span class="sxs-lookup"><span data-stu-id="6d8f4-148">BypassProxyServer</span></span>                                    | <span data-ttu-id="6d8f4-149">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6d8f4-149">Same as default provider</span></span>                           |
| <span data-ttu-id="6d8f4-150">рековериконнектионпоинт</span><span class="sxs-lookup"><span data-stu-id="6d8f4-150">RecoveryConnectionPoint</span></span>                              | <span data-ttu-id="6d8f4-151">Игнорируется \* (может измениться, если поставщик имеет требование)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-151">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="6d8f4-152">Рековерихостсистем (RO)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-152">RecoveryHostSystem (RO)</span></span>                              | <span data-ttu-id="6d8f4-153">Не учитывается</span><span class="sxs-lookup"><span data-stu-id="6d8f4-153">Ignored</span></span>                                            |
| <span data-ttu-id="6d8f4-154">Примариконнектионпоинт (RO)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-154">PrimaryConnectionPoint (RO)</span></span>                          | <span data-ttu-id="6d8f4-155">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6d8f4-155">Same as default provider</span></span>                           |
| <span data-ttu-id="6d8f4-156">Примарихостсистем (RO)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-156">PrimaryHostSystem (RO)</span></span>                               | <span data-ttu-id="6d8f4-157">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6d8f4-157">Same as default provider</span></span>                           |
| <span data-ttu-id="6d8f4-158">рековерисерверпортнумбер</span><span class="sxs-lookup"><span data-stu-id="6d8f4-158">RecoveryServerPortNumber</span></span>                             | <span data-ttu-id="6d8f4-159">Игнорируется \* (может измениться, если поставщик имеет требование)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-159">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="6d8f4-160">репликатехостквпитемс</span><span class="sxs-lookup"><span data-stu-id="6d8f4-160">ReplicateHostKvpItems</span></span>                                | <span data-ttu-id="6d8f4-161">Не учитывается</span><span class="sxs-lookup"><span data-stu-id="6d8f4-161">Ignored</span></span>                                            |
| <span data-ttu-id="6d8f4-162">аппликатионконсистентснапшотинтервал</span><span class="sxs-lookup"><span data-stu-id="6d8f4-162">ApplicationConsistentSnapshotInterval</span></span>                | <span data-ttu-id="6d8f4-163">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6d8f4-163">Same as default provider</span></span>                           |
| <span data-ttu-id="6d8f4-164">рековерихистори</span><span class="sxs-lookup"><span data-stu-id="6d8f4-164">RecoveryHistory</span></span>                                      | <span data-ttu-id="6d8f4-165">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6d8f4-165">Same as default provider</span></span>                           |
| <span data-ttu-id="6d8f4-166">инклудеддискс\[\]</span><span class="sxs-lookup"><span data-stu-id="6d8f4-166">IncludedDisks\[\]</span></span>                                    | <span data-ttu-id="6d8f4-167">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6d8f4-167">Same as default provider</span></span>                           |
| <span data-ttu-id="6d8f4-168">ауторесинчронизинаблед</span><span class="sxs-lookup"><span data-stu-id="6d8f4-168">AutoResynchronizeEnabled</span></span>                             | <span data-ttu-id="6d8f4-169">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6d8f4-169">Same as default provider</span></span>                           |
| <span data-ttu-id="6d8f4-170">ауторесинчронизеинтервалстарт</span><span class="sxs-lookup"><span data-stu-id="6d8f4-170">AutoResynchronizeIntervalStart</span></span>                       | <span data-ttu-id="6d8f4-171">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6d8f4-171">Same as default provider</span></span>                           |
| <span data-ttu-id="6d8f4-172">ауторесинчронизеинтерваленд</span><span class="sxs-lookup"><span data-stu-id="6d8f4-172">AutoResynchronizeIntervalEnd</span></span>                         | <span data-ttu-id="6d8f4-173">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6d8f4-173">Same as default provider</span></span>                           |
| <span data-ttu-id="6d8f4-174">Енаблевритеордерпресерватионакроссдискс (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="6d8f4-174">EnableWriteOrderPreservationAcrossDisks (Deprecated)</span></span> | <span data-ttu-id="6d8f4-175">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6d8f4-175">Same as default provider</span></span>                           |
| <span data-ttu-id="6d8f4-176">ReplicationInterval</span><span class="sxs-lookup"><span data-stu-id="6d8f4-176">ReplicationInterval</span></span>                                  | <span data-ttu-id="6d8f4-177">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6d8f4-177">Same as default provider</span></span>                           |



 

## <a name="requirements"></a><span data-ttu-id="6d8f4-178">Требования</span><span class="sxs-lookup"><span data-stu-id="6d8f4-178">Requirements</span></span>



| <span data-ttu-id="6d8f4-179">Требование</span><span class="sxs-lookup"><span data-stu-id="6d8f4-179">Requirement</span></span> | <span data-ttu-id="6d8f4-180">Значение</span><span class="sxs-lookup"><span data-stu-id="6d8f4-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d8f4-181">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d8f4-181">Minimum supported client</span></span><br/> | <span data-ttu-id="6d8f4-182">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6d8f4-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6d8f4-183">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d8f4-183">Minimum supported server</span></span><br/> | <span data-ttu-id="6d8f4-184">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6d8f4-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6d8f4-185">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6d8f4-185">Namespace</span></span><br/>                | <span data-ttu-id="6d8f4-186">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6d8f4-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6d8f4-187">MOF</span><span class="sxs-lookup"><span data-stu-id="6d8f4-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d8f4-188"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d8f4-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d8f4-189">DLL</span><span class="sxs-lookup"><span data-stu-id="6d8f4-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d8f4-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6d8f4-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6d8f4-191">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d8f4-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d8f4-192">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="6d8f4-192">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="6d8f4-193">**ремоверепликатионрелатионшипекс**</span><span class="sxs-lookup"><span data-stu-id="6d8f4-193">**RemoveReplicationRelationshipEx**</span></span>](removereplicationrelationshipex-msvm-replicationservice.md)
</dt> </dl>

 

