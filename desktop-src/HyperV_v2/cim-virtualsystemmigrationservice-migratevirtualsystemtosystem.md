---
description: Метод для перемещения, переноса или повторного размещения виртуальной системы в целевой системе.
ms.assetid: 210d31f1-093f-4fd5-afd7-5f028b4cb343
title: Метод Мигратевиртуалсистемтосистем класса CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1459d80785725914cbaa5dda5b81e8d2fabad5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909192"
---
# <a name="migratevirtualsystemtosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="e07e1-103">Метод Мигратевиртуалсистемтосистем \_ класса CIM виртуалсистеммигратионсервице</span><span class="sxs-lookup"><span data-stu-id="e07e1-103">MigrateVirtualSystemToSystem method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="e07e1-104">Метод для перемещения, переноса или повторного размещения виртуальной системы в целевой системе.</span><span class="sxs-lookup"><span data-stu-id="e07e1-104">Method to move, migrate or relocate a virtual system to a target system.</span></span>

<span data-ttu-id="e07e1-105">Описание кода возврата:</span><span class="sxs-lookup"><span data-stu-id="e07e1-105">Return code description:</span></span>

## <a name="syntax"></a><span data-ttu-id="e07e1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e07e1-106">Syntax</span></span>


```mof
uint32 MigrateVirtualSystemToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ComputerSystem REF NewComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e07e1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e07e1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e07e1-108">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e07e1-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e07e1-109">Система исходного виртуального компьютера для переноса.</span><span class="sxs-lookup"><span data-stu-id="e07e1-109">Source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="e07e1-110">*Дестинатионсистем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e07e1-110">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e07e1-111">Целевая система узла вхерето перенесите виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="e07e1-111">Destination host system whereto migrate the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="e07e1-112">*Мигратионсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e07e1-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e07e1-113">Строка, содержащая встроенный экземпляр класса [**CIM \_ виртуалсистеммигратионсеттингдата**](cim-virtualsystemmigrationsettingdata.md) , представляющий параметры миграции, применимые к операции миграции.</span><span class="sxs-lookup"><span data-stu-id="e07e1-113">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="e07e1-114">*Невсистемсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e07e1-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e07e1-115">Строка, содержащая встроенный экземпляр класса [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) , представляющий новые свойства, применимые к виртуальной системе после переноса.</span><span class="sxs-lookup"><span data-stu-id="e07e1-115">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="e07e1-116">*Невресаурцесеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e07e1-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e07e1-117">Массив строк, каждый из которых содержит встроенный экземпляр класса [**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md) , представляющий новые свойства, применимые к виртуальным ресурсам в области виртуальной системы после переноса.</span><span class="sxs-lookup"><span data-stu-id="e07e1-117">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="e07e1-118">*Невкомпутерсистем* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e07e1-118">*NewComputerSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e07e1-119">Ссылка на экземпляр класса системы [**CIM, \_**](cim-computersystem.md) представляющий систему виртуального компьютера после переноса.</span><span class="sxs-lookup"><span data-stu-id="e07e1-119">Reference to an instance of the [**CIM\_ComputerSystem**](cim-computersystem.md) class representing the virtual computer system after it has been migrated.</span></span>

</dd> <dt>

<span data-ttu-id="e07e1-120">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e07e1-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e07e1-121">Если операция выполняется долго, может быть возвращена также [**\_ конкретежоб CIM**](cim-concretejob.md) , представляющая задание.</span><span class="sxs-lookup"><span data-stu-id="e07e1-121">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e07e1-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e07e1-122">Return value</span></span>

<span data-ttu-id="e07e1-123">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="e07e1-123">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="e07e1-124">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="e07e1-124">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="e07e1-125">Описание</span><span class="sxs-lookup"><span data-stu-id="e07e1-125">Description</span></span>                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e07e1-126"><dt>**Завершено без ошибки**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e07e1-126"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="e07e1-127">Миграция виртуальной системы выполнена.</span><span class="sxs-lookup"><span data-stu-id="e07e1-127">Virtual system was migrated.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="e07e1-128"><dt>**Не поддерживается**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e07e1-128"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="e07e1-129">Метод не поддерживается реализацией.</span><span class="sxs-lookup"><span data-stu-id="e07e1-129">Method not supported by implementation.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="e07e1-130"><dt>**Сбой**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e07e1-130"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                                     | <span data-ttu-id="e07e1-131">Не удалось выполнить миграцию виртуальной системы по неуказанным причинам.</span><span class="sxs-lookup"><span data-stu-id="e07e1-131">Virtual system migration failed for unspecified reasons.</span></span><br/>                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="e07e1-132"><dt>**Время ожидания**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e07e1-132"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                                    | <span data-ttu-id="e07e1-133">Время ожидания миграции виртуальной системы. состояние виртуальной системы неизвестно.</span><span class="sxs-lookup"><span data-stu-id="e07e1-133">Virtual system migration time out; the virtual system state is unknown.</span></span><br/>                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="e07e1-134"><dt>**Недопустимый параметр**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e07e1-134"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="e07e1-135">Один или несколько параметров формально являются недопустимыми, например, значение системного параметра назначения не содержит допустимого пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="e07e1-135">One or more parameters are formally invalid For example, the value of the Destination System parameter does not contain a valid object path.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="e07e1-136"><dt>**Недопустимое состояние**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e07e1-136"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>                              | <span data-ttu-id="e07e1-137">Исходная виртуальная система, исходная система узла или целевая система узла находятся в состоянии, которое разрешает инициацию запрошенной миграции виртуальной системы. Это может быть временным условием.</span><span class="sxs-lookup"><span data-stu-id="e07e1-137">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="e07e1-138"><dt>**Несовместимые параметры**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e07e1-138"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>                    | <span data-ttu-id="e07e1-139">Один или несколько входных параметров несовместимы в качестве набора или относительно целевого узла.</span><span class="sxs-lookup"><span data-stu-id="e07e1-139">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="e07e1-140">Например, значение параметра *мигратионневсеттингдата* содержит свойства, которые не поддерживаются целевой системой узла, указанной значением параметра *дестинатионсистем* .</span><span class="sxs-lookup"><span data-stu-id="e07e1-140">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationSystem* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="e07e1-141"><dt>**Зарезервировано DMTF**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="e07e1-141"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="e07e1-142"><dt>**Параметры метода проверены — задание запущено**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="e07e1-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="e07e1-143"><dt>**Метод reserved**</dt> <dt>4097.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="e07e1-143"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="e07e1-144"><dt>**Независимый от поставщика**</dt> <dt>32768.65 535</dt></span><span class="sxs-lookup"><span data-stu-id="e07e1-144"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="e07e1-145">Требования</span><span class="sxs-lookup"><span data-stu-id="e07e1-145">Requirements</span></span>



| <span data-ttu-id="e07e1-146">Требование</span><span class="sxs-lookup"><span data-stu-id="e07e1-146">Requirement</span></span> | <span data-ttu-id="e07e1-147">Значение</span><span class="sxs-lookup"><span data-stu-id="e07e1-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e07e1-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e07e1-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e07e1-149">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e07e1-149">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="e07e1-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e07e1-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e07e1-151">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e07e1-151">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="e07e1-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e07e1-152">Namespace</span></span><br/>                | <span data-ttu-id="e07e1-153">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e07e1-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e07e1-154">MOF</span><span class="sxs-lookup"><span data-stu-id="e07e1-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e07e1-155"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e07e1-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e07e1-156">DLL</span><span class="sxs-lookup"><span data-stu-id="e07e1-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e07e1-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e07e1-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e07e1-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e07e1-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e07e1-159">**\_ВИРТУАЛСИСТЕММИГРАТИОНСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="e07e1-159">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




