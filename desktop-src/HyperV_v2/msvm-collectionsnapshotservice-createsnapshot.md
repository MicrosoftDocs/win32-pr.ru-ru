---
description: Создает моментальный снимок коллекции виртуальных систем.
ms.assetid: 2512d82f-06b9-4613-b920-d3a9be884a75
title: Метод CreateSnapshot класса Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 653dae65cc5fe50416b069da6a66e8c678c1b512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812515"
---
# <a name="createsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="81c48-103">Метод CreateSnapshot \_ класса Коллектионснапшотсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="81c48-103">CreateSnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="81c48-104">Создает моментальный снимок коллекции виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="81c48-104">Creates a snapshot of a virtual system collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="81c48-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81c48-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_CollectionOfMSEs REF Collection,
  [in]      string                   SnapshotSettings,
  [in]      uint16                   SnapshotType,
  [in, out] CIM_Collection       REF ResultingSnapshotCollection,
  [out]     CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="81c48-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="81c48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81c48-107">*Коллекция* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81c48-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81c48-108">Ссылка на [**\_ коллектионофмсес CIM**](cim-collectionofmses.md) , описывающая затронутую коллекцию виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="81c48-108">Reference to a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) that describes the affected virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="81c48-109">*Снапшотсеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81c48-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81c48-110">Содержит настройки параметров.</span><span class="sxs-lookup"><span data-stu-id="81c48-110">Contains the parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="81c48-111">*Снапшоттипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81c48-111">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81c48-112">Запрошенный тип моментального снимка:</span><span class="sxs-lookup"><span data-stu-id="81c48-112">Requested snapshot type:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81c48-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="81c48-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>

<span data-ttu-id="81c48-114"><span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**Стандартный моментальный снимок** (1)</span><span class="sxs-lookup"><span data-stu-id="81c48-114"><span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**Standard Snapshot** (1)</span></span>


</dt> <dd>

<span data-ttu-id="81c48-115">Стандартный моментальный снимок виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="81c48-115">Standard snapshot of the virtual system.</span></span>

</dd> <dt>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>

<span data-ttu-id="81c48-116"><span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**Моментальный снимок восстановления** (2)</span><span class="sxs-lookup"><span data-stu-id="81c48-116"><span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**Recovery Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="81c48-117">Моментальный снимок сценариев восстановления, включая репликацию и резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="81c48-117">Snapshot for recovery scenarios including failover replication and backup.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="81c48-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="81c48-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="81c48-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="81c48-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="81c48-120">*Ресултингснапшотколлектион* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="81c48-120">*ResultingSnapshotCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="81c48-121">При успешном выполнении возвращает ссылку на [**\_ коллекцию CIM**](cim-collection.md) , содержащую моментальный снимок виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="81c48-121">On success, returns a [**CIM\_Collection**](cim-collection.md) reference containing the virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="81c48-122">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="81c48-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81c48-123">Необязательная ссылка, которая возвращается, если операция выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="81c48-123">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="81c48-124">При наличии возвращаемой ссылки на экземпляр [**CIM \_ конкретежоб**](cim-concretejob.md) можно использовать для отслеживания хода выполнения и получения результата метода.</span><span class="sxs-lookup"><span data-stu-id="81c48-124">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81c48-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81c48-125">Return value</span></span>

<span data-ttu-id="81c48-126">При успешном выполнении возвращает значение 0 (завершено) или 4096 (задание запущено); в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="81c48-126">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="81c48-127">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="81c48-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81c48-128">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="81c48-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="81c48-129">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="81c48-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="81c48-130">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="81c48-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="81c48-131">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="81c48-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="81c48-132">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="81c48-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="81c48-133">**Недопустимый тип** (6)</span><span class="sxs-lookup"><span data-stu-id="81c48-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="81c48-134">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="81c48-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="81c48-135">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="81c48-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="81c48-136">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="81c48-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="81c48-137">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="81c48-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="81c48-138">Требования</span><span class="sxs-lookup"><span data-stu-id="81c48-138">Requirements</span></span>



| <span data-ttu-id="81c48-139">Требование</span><span class="sxs-lookup"><span data-stu-id="81c48-139">Requirement</span></span> | <span data-ttu-id="81c48-140">Значение</span><span class="sxs-lookup"><span data-stu-id="81c48-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81c48-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81c48-141">Minimum supported client</span></span><br/> | <span data-ttu-id="81c48-142">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="81c48-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="81c48-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81c48-143">Minimum supported server</span></span><br/> | <span data-ttu-id="81c48-144">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="81c48-144">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="81c48-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="81c48-145">Namespace</span></span><br/>                | <span data-ttu-id="81c48-146">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="81c48-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="81c48-147">MOF</span><span class="sxs-lookup"><span data-stu-id="81c48-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81c48-148"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81c48-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="81c48-149">DLL</span><span class="sxs-lookup"><span data-stu-id="81c48-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81c48-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="81c48-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="81c48-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81c48-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81c48-152">**Мсвм \_ коллектионснапшотсервице**</span><span class="sxs-lookup"><span data-stu-id="81c48-152">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




