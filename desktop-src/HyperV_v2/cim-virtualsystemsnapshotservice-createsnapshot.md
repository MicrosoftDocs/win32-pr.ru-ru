---
description: Создает моментальный снимок виртуальной системы.
ms.assetid: cad4cb4f-523f-4fda-ac88-8cece7abc227
title: Метод CreateSnapshot класса CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ee96098477501123cffc1fd59a52734bbbea35d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663993"
---
# <a name="createsnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="84224-103">Метод CreateSnapshot \_ класса CIM виртуалсистемснапшотсервице</span><span class="sxs-lookup"><span data-stu-id="84224-103">CreateSnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="84224-104">Создает моментальный снимок виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="84224-104">Creates a snapshot of a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="84224-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84224-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="84224-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="84224-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84224-107">*Аффектедсистем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84224-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84224-108">Ссылка [**CIM \_ ComputerSystem**](cim-computersystem.md) на затронутую виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="84224-108">A [**CIM\_ComputerSystem**](cim-computersystem.md) reference to the affected virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="84224-109">*Снапшотсеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84224-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84224-110">Параметры параметров.</span><span class="sxs-lookup"><span data-stu-id="84224-110">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="84224-111">*Снапшоттипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84224-111">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84224-112">Запрошенный тип моментального снимка:</span><span class="sxs-lookup"><span data-stu-id="84224-112">Requested snapshot type:</span></span>

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span data-ttu-id="84224-113"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Полный моментальный снимок** (2)</span><span class="sxs-lookup"><span data-stu-id="84224-113"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Full Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="84224-114">Завершите создание моментального снимка виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="84224-114">Complete snapshot of the virtual system.</span></span>

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span data-ttu-id="84224-115"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Моментальный снимок диска** (3)</span><span class="sxs-lookup"><span data-stu-id="84224-115"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Disk Snapshot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="84224-116">Моментальный снимок дисков виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="84224-116">Snapshot of virtual system disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="84224-117"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="84224-117"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="84224-118"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="84224-118"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="84224-119">*Ресултингснапшот* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="84224-119">*ResultingSnapshot* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="84224-120">Ссылка [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) на полученный моментальный снимок виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="84224-120">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the resulting virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="84224-121">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="84224-121">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84224-122">Если операция выполняется долго, при необходимости может быть возвращено задание.</span><span class="sxs-lookup"><span data-stu-id="84224-122">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="84224-123">В этом случае экземпляр класса [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) , представляющий новый моментальный снимок виртуальной системы, представлен с помощью связи [**CIM \_ аффектеджобелемент**](cim-affectedjobelement.md) со значением свойства **аффектеделемент** , ссылающегося на новый экземпляр класса **CIM \_ виртуалсистемсеттингдата** , представляющего моментальный снимок виртуальной системы, а значение **ElementEffects** установлено в 5 (Create).</span><span class="sxs-lookup"><span data-stu-id="84224-123">In this case, the instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing the new virtual system snapshot is presented via the [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) association with the value of the **AffectedElement** property referring to the new instance of the **CIM\_VirtualSystemSettingData** class representing the virtual system snapshot and the value of the **ElementEffects** set to 5 (Create).</span></span>

> [!Note]  
> <span data-ttu-id="84224-124">Этот параметр был доступен для чтения и записи в Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="84224-124">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84224-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84224-125">Return value</span></span>

<span data-ttu-id="84224-126">При успешном выполнении возвращает 0; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="84224-126">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="84224-127">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="84224-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84224-128">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="84224-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="84224-129">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="84224-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="84224-130">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="84224-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="84224-131">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="84224-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="84224-132">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="84224-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="84224-133">**Недопустимый тип** (6)</span><span class="sxs-lookup"><span data-stu-id="84224-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="84224-134">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="84224-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="84224-135">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="84224-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="84224-136">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="84224-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="84224-137">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="84224-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="84224-138">Требования</span><span class="sxs-lookup"><span data-stu-id="84224-138">Requirements</span></span>



| <span data-ttu-id="84224-139">Требование</span><span class="sxs-lookup"><span data-stu-id="84224-139">Requirement</span></span> | <span data-ttu-id="84224-140">Значение</span><span class="sxs-lookup"><span data-stu-id="84224-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84224-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84224-141">Minimum supported client</span></span><br/> | <span data-ttu-id="84224-142">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="84224-142">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="84224-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84224-143">Minimum supported server</span></span><br/> | <span data-ttu-id="84224-144">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="84224-144">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="84224-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="84224-145">Namespace</span></span><br/>                | <span data-ttu-id="84224-146">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="84224-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="84224-147">MOF</span><span class="sxs-lookup"><span data-stu-id="84224-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84224-148"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84224-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="84224-149">DLL</span><span class="sxs-lookup"><span data-stu-id="84224-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84224-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="84224-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="84224-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84224-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84224-152">**\_ВИРТУАЛСИСТЕМСНАПШОТСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="84224-152">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




