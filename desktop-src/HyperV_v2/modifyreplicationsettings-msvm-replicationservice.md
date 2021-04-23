---
description: Изменяет параметры репликации для виртуальной машины. Когда клиент вызывает этот метод для реплики виртуальной машины, он изменяет параметры репликации отношения репликации с расширенной репликой.
ms.assetid: e68514a5-f508-4047-8dcc-6a95f3e3353e
title: Метод Модифирепликатионсеттингс класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyReplicationSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d1c932f06350324e0d84559724f7ba0412dfb3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683968"
---
# <a name="modifyreplicationsettings-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="5aba9-104">Метод Модифирепликатионсеттингс \_ класса Репликатионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="5aba9-104">ModifyReplicationSettings method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="5aba9-105">Изменяет параметры репликации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5aba9-105">Modifies the replication settings for a virtual machine.</span></span> <span data-ttu-id="5aba9-106">Когда клиент вызывает этот метод для реплики виртуальной машины, он изменяет параметры репликации отношения репликации с расширенной репликой.</span><span class="sxs-lookup"><span data-stu-id="5aba9-106">When a client calls this method for a replica virtual machine, it modifies the replication settings of the replication relationship with the extended replica.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aba9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5aba9-107">Syntax</span></span>


```mof
uint32 ModifyReplicationSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5aba9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5aba9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aba9-109">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5aba9-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aba9-110">Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину, для которой необходимо изменить параметры репликации.</span><span class="sxs-lookup"><span data-stu-id="5aba9-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication settings should be modified.</span></span>

</dd> <dt>

<span data-ttu-id="5aba9-111">*Репликатионсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5aba9-111">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aba9-112">Строковое представление класса [**мсвм \_ репликатионсеттингдата**](msvm-replicationsettingdata.md) , определяющего новые параметры репликации.</span><span class="sxs-lookup"><span data-stu-id="5aba9-112">A string representation of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the new replication settings.</span></span>

</dd> <dt>

<span data-ttu-id="5aba9-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5aba9-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5aba9-114">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5aba9-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aba9-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5aba9-115">Return value</span></span>

<span data-ttu-id="5aba9-116">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="5aba9-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="5aba9-117">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="5aba9-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5aba9-118">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="5aba9-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5aba9-119">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="5aba9-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="5aba9-120">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="5aba9-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="5aba9-121">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="5aba9-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="5aba9-122">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="5aba9-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="5aba9-123">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="5aba9-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="5aba9-124">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="5aba9-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="5aba9-125">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="5aba9-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="5aba9-126">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="5aba9-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="5aba9-127">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="5aba9-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="5aba9-128">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="5aba9-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="5aba9-129">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="5aba9-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="5aba9-130">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="5aba9-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="5aba9-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5aba9-131">Remarks</span></span>

<span data-ttu-id="5aba9-132">**Модифирепликатионсеттингс** принимает экземпляр [**МСВМ \_ репликатионсеттингдата**](msvm-replicationsettingdata.md) (фрсд) в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="5aba9-132">**ModifyReplicationSettings** takes an [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) instance (FRSD) as input.</span></span> <span data-ttu-id="5aba9-133">По умолчанию используется связанный ФРСД для виртуальной машины в качестве поставщика услуг размещения.</span><span class="sxs-lookup"><span data-stu-id="5aba9-133">The associated FRSD for the virtual machine as host-to-host provider is the default choice.</span></span> <span data-ttu-id="5aba9-134">Входные ФРСД проверяются на допустимые параметры для каждого свойства для поставщика по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5aba9-134">Input FRSD is validated for valid settings for each property for the default provider.</span></span> <span data-ttu-id="5aba9-135">В этой таблице перечислены различия проверки по отношению к внешнему поставщику.</span><span class="sxs-lookup"><span data-stu-id="5aba9-135">This table summarizes the validation differences with respect to the external provider.</span></span>



| <span data-ttu-id="5aba9-136">Свойство</span><span class="sxs-lookup"><span data-stu-id="5aba9-136">Property</span></span>                                             | <span data-ttu-id="5aba9-137">Внешние поставщики</span><span class="sxs-lookup"><span data-stu-id="5aba9-137">External providers</span></span>                                 |
|------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="5aba9-138">репликатионпровидер</span><span class="sxs-lookup"><span data-stu-id="5aba9-138">ReplicationProvider</span></span>                                  | <span data-ttu-id="5aba9-139">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5aba9-139">Same as default provider</span></span>                           |
| <span data-ttu-id="5aba9-140">authenticationType</span><span class="sxs-lookup"><span data-stu-id="5aba9-140">AuthenticationType</span></span>                                   | <span data-ttu-id="5aba9-141">Не учитывается</span><span class="sxs-lookup"><span data-stu-id="5aba9-141">Ignored</span></span>                                            |
| <span data-ttu-id="5aba9-142">CertificateThumbPrint</span><span class="sxs-lookup"><span data-stu-id="5aba9-142">CertificateThumbPrint</span></span>                                | <span data-ttu-id="5aba9-143">Не учитывается</span><span class="sxs-lookup"><span data-stu-id="5aba9-143">Ignored</span></span>                                            |
| <span data-ttu-id="5aba9-144">Рутцертификатесумбпринт (RO)</span><span class="sxs-lookup"><span data-stu-id="5aba9-144">RootCertificateThumbPrint (RO)</span></span>                       | <span data-ttu-id="5aba9-145">Не учитывается</span><span class="sxs-lookup"><span data-stu-id="5aba9-145">Ignored</span></span>                                            |
| <span data-ttu-id="5aba9-146">компрессионенаблед</span><span class="sxs-lookup"><span data-stu-id="5aba9-146">CompressionEnabled</span></span>                                   | <span data-ttu-id="5aba9-147">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5aba9-147">Same as default provider</span></span>                           |
| <span data-ttu-id="5aba9-148">бипасспроксисервер</span><span class="sxs-lookup"><span data-stu-id="5aba9-148">BypassProxyServer</span></span>                                    | <span data-ttu-id="5aba9-149">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5aba9-149">Same as default provider</span></span>                           |
| <span data-ttu-id="5aba9-150">рековериконнектионпоинт</span><span class="sxs-lookup"><span data-stu-id="5aba9-150">RecoveryConnectionPoint</span></span>                              | <span data-ttu-id="5aba9-151">Игнорируется \* (может измениться, если поставщик имеет требование)</span><span class="sxs-lookup"><span data-stu-id="5aba9-151">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="5aba9-152">Рековерихостсистем (RO)</span><span class="sxs-lookup"><span data-stu-id="5aba9-152">RecoveryHostSystem (RO)</span></span>                              | <span data-ttu-id="5aba9-153">Не учитывается</span><span class="sxs-lookup"><span data-stu-id="5aba9-153">Ignored</span></span>                                            |
| <span data-ttu-id="5aba9-154">Примариконнектионпоинт (RO)</span><span class="sxs-lookup"><span data-stu-id="5aba9-154">PrimaryConnectionPoint (RO)</span></span>                          | <span data-ttu-id="5aba9-155">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5aba9-155">Same as default provider</span></span>                           |
| <span data-ttu-id="5aba9-156">Примарихостсистем (RO)</span><span class="sxs-lookup"><span data-stu-id="5aba9-156">PrimaryHostSystem (RO)</span></span>                               | <span data-ttu-id="5aba9-157">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5aba9-157">Same as default provider</span></span>                           |
| <span data-ttu-id="5aba9-158">рековерисерверпортнумбер</span><span class="sxs-lookup"><span data-stu-id="5aba9-158">RecoveryServerPortNumber</span></span>                             | <span data-ttu-id="5aba9-159">Игнорируется \* (может измениться, если поставщик имеет требование)</span><span class="sxs-lookup"><span data-stu-id="5aba9-159">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="5aba9-160">репликатехостквпитемс</span><span class="sxs-lookup"><span data-stu-id="5aba9-160">ReplicateHostKvpItems</span></span>                                | <span data-ttu-id="5aba9-161">Не учитывается</span><span class="sxs-lookup"><span data-stu-id="5aba9-161">Ignored</span></span>                                            |
| <span data-ttu-id="5aba9-162">аппликатионконсистентснапшотинтервал</span><span class="sxs-lookup"><span data-stu-id="5aba9-162">ApplicationConsistentSnapshotInterval</span></span>                | <span data-ttu-id="5aba9-163">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5aba9-163">Same as default provider</span></span>                           |
| <span data-ttu-id="5aba9-164">рековерихистори</span><span class="sxs-lookup"><span data-stu-id="5aba9-164">RecoveryHistory</span></span>                                      | <span data-ttu-id="5aba9-165">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5aba9-165">Same as default provider</span></span>                           |
| <span data-ttu-id="5aba9-166">инклудеддискс\[\]</span><span class="sxs-lookup"><span data-stu-id="5aba9-166">IncludedDisks\[\]</span></span>                                    | <span data-ttu-id="5aba9-167">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5aba9-167">Same as default provider</span></span>                           |
| <span data-ttu-id="5aba9-168">ауторесинчронизинаблед</span><span class="sxs-lookup"><span data-stu-id="5aba9-168">AutoResynchronizeEnabled</span></span>                             | <span data-ttu-id="5aba9-169">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5aba9-169">Same as default provider</span></span>                           |
| <span data-ttu-id="5aba9-170">ауторесинчронизеинтервалстарт</span><span class="sxs-lookup"><span data-stu-id="5aba9-170">AutoResynchronizeIntervalStart</span></span>                       | <span data-ttu-id="5aba9-171">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5aba9-171">Same as default provider</span></span>                           |
| <span data-ttu-id="5aba9-172">ауторесинчронизеинтерваленд</span><span class="sxs-lookup"><span data-stu-id="5aba9-172">AutoResynchronizeIntervalEnd</span></span>                         | <span data-ttu-id="5aba9-173">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5aba9-173">Same as default provider</span></span>                           |
| <span data-ttu-id="5aba9-174">Енаблевритеордерпресерватионакроссдискс (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="5aba9-174">EnableWriteOrderPreservationAcrossDisks (Deprecated)</span></span> | <span data-ttu-id="5aba9-175">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5aba9-175">Same as default provider</span></span>                           |
| <span data-ttu-id="5aba9-176">ReplicationInterval</span><span class="sxs-lookup"><span data-stu-id="5aba9-176">ReplicationInterval</span></span>                                  | <span data-ttu-id="5aba9-177">То же, что и поставщик по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5aba9-177">Same as default provider</span></span>                           |



 

## <a name="requirements"></a><span data-ttu-id="5aba9-178">Требования</span><span class="sxs-lookup"><span data-stu-id="5aba9-178">Requirements</span></span>



| <span data-ttu-id="5aba9-179">Требование</span><span class="sxs-lookup"><span data-stu-id="5aba9-179">Requirement</span></span> | <span data-ttu-id="5aba9-180">Значение</span><span class="sxs-lookup"><span data-stu-id="5aba9-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aba9-181">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5aba9-181">Minimum supported client</span></span><br/> | <span data-ttu-id="5aba9-182">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5aba9-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5aba9-183">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5aba9-183">Minimum supported server</span></span><br/> | <span data-ttu-id="5aba9-184">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5aba9-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5aba9-185">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5aba9-185">Namespace</span></span><br/>                | <span data-ttu-id="5aba9-186">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="5aba9-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5aba9-187">MOF</span><span class="sxs-lookup"><span data-stu-id="5aba9-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5aba9-188"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5aba9-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5aba9-189">DLL</span><span class="sxs-lookup"><span data-stu-id="5aba9-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5aba9-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5aba9-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5aba9-191">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5aba9-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aba9-192">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="5aba9-192">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

