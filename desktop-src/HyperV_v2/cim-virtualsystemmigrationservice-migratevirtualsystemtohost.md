---
description: Метод для перемещения, переноса или повторного размещения виртуальной системы на целевом узле, заданном сетевым именем или IP-адресом.
ms.assetid: 09fdc0b2-641c-47f5-b270-e26e3acf7ea5
title: Метод Мигратевиртуалсистемтохост класса CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.MigrateVirtualSystemToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d1a90e3adadbb5efc5f9cae3b7710e07c1e05000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683304"
---
# <a name="migratevirtualsystemtohost-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="eb91c-103">Метод Мигратевиртуалсистемтохост \_ класса CIM виртуалсистеммигратионсервице</span><span class="sxs-lookup"><span data-stu-id="eb91c-103">MigrateVirtualSystemToHost method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="eb91c-104">Метод для перемещения, переноса или повторного размещения виртуальной системы на целевом узле, заданном сетевым именем или IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="eb91c-104">Method to move, migrate or relocate a virtual system to a target host specified by a network name or IP address.</span></span>

> [!Note]  
> <span data-ttu-id="eb91c-105">Этот метод предназначен как переходное решение только после того, как будет доступно моделирование поддержки кластера.</span><span class="sxs-lookup"><span data-stu-id="eb91c-105">This method is intended as a transitional solution only until modeling of cluster support is available.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="eb91c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb91c-106">Syntax</span></span>


```mof
uint32 MigrateVirtualSystemToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="eb91c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb91c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb91c-108">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eb91c-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb91c-109">Система исходного виртуального компьютера для переноса.</span><span class="sxs-lookup"><span data-stu-id="eb91c-109">Source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="eb91c-110">*Дестинатионхост* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eb91c-110">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb91c-111">Целевая система узла для миграции.</span><span class="sxs-lookup"><span data-stu-id="eb91c-111">Target host system for the migration.</span></span>

<span data-ttu-id="eb91c-112">Допустимые форматы для этого параметра передаются через значения элементов  \[ \] свойства массива дестинатионхостформатссуппортед в экземпляре [**модели CIM \_ виртуалсистеммигратионкапабилитиес**](cim-virtualsystemmigrationcapabilities.md) , связанной с Ассоциацией [**\_ елементкапабилитиес CIM**](cim-elementcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="eb91c-112">Acceptable formats for this parameter are conveyed through values of elements of the **DestinationHostFormatsSupported**\[ \] array property in the instance of the [**CIM\_VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md) that is associated through the [**CIM\_ElementCapabilities**](cim-elementcapabilities.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="eb91c-113">*Мигратионсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eb91c-113">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb91c-114">Строка, содержащая встроенный экземпляр класса [**CIM \_ виртуалсистеммигратионсеттингдата**](cim-virtualsystemmigrationsettingdata.md) , представляющий параметры миграции, применимые к операции миграции.</span><span class="sxs-lookup"><span data-stu-id="eb91c-114">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="eb91c-115">*Невсистемсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eb91c-115">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb91c-116">Строка, содержащая встроенный экземпляр класса [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) , представляющий новые свойства, применимые к виртуальной системе после переноса.</span><span class="sxs-lookup"><span data-stu-id="eb91c-116">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="eb91c-117">*Невресаурцесеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eb91c-117">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb91c-118">Массив строк, каждый из которых содержит встроенный экземпляр класса [**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md) , представляющий новые свойства, применимые к виртуальным ресурсам в области виртуальной системы после переноса.</span><span class="sxs-lookup"><span data-stu-id="eb91c-118">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="eb91c-119">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="eb91c-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb91c-120">Если операция выполняется долго, может быть возвращена также [**\_ конкретежоб CIM**](cim-concretejob.md) , представляющая задание.</span><span class="sxs-lookup"><span data-stu-id="eb91c-120">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb91c-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb91c-121">Return value</span></span>

<span data-ttu-id="eb91c-122">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="eb91c-122">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="eb91c-123">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="eb91c-123">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="eb91c-124">Описание</span><span class="sxs-lookup"><span data-stu-id="eb91c-124">Description</span></span>                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eb91c-125"><dt>**Завершено без ошибки**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="eb91c-125"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="eb91c-126">Миграция виртуальной системы выполнена.</span><span class="sxs-lookup"><span data-stu-id="eb91c-126">Virtual system was migrated.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="eb91c-127"><dt>**Не поддерживается**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="eb91c-127"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="eb91c-128">Метод не поддерживается реализацией.</span><span class="sxs-lookup"><span data-stu-id="eb91c-128">Method not supported by implementation.</span></span><br/>                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="eb91c-129"><dt>**Сбой**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="eb91c-129"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                                     | <span data-ttu-id="eb91c-130">Не удалось выполнить миграцию виртуальной системы по неуказанным причинам.</span><span class="sxs-lookup"><span data-stu-id="eb91c-130">Virtual system migration failed for unspecified reasons.</span></span><br/>                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="eb91c-131"><dt>**Время ожидания**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="eb91c-131"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                                    | <span data-ttu-id="eb91c-132">Время ожидания миграции виртуальной системы. состояние виртуальной системы неизвестно.</span><span class="sxs-lookup"><span data-stu-id="eb91c-132">Virtual system migration time out; the virtual system state is unknown.</span></span><br/>                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="eb91c-133"><dt>**Недопустимый параметр**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="eb91c-133"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="eb91c-134">Один или несколько параметров формально являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="eb91c-134">One or more parameters are formally invalid.</span></span> <span data-ttu-id="eb91c-135">Например, значение параметра *дестинатионхост* могло быть указано в неподдерживаемом формате.</span><span class="sxs-lookup"><span data-stu-id="eb91c-135">For example, the value of the *DestinationHost* parameter could have been specified in an unsupported format.</span></span><br/>                                                                                                                                    |
| <dl> <span data-ttu-id="eb91c-136"><dt>**Недопустимое состояние**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="eb91c-136"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>                              | <span data-ttu-id="eb91c-137">Исходная виртуальная система, исходная система узла или целевая система узла находятся в состоянии, которое разрешает инициацию запрошенной миграции виртуальной системы. Это может быть временным условием.</span><span class="sxs-lookup"><span data-stu-id="eb91c-137">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="eb91c-138"><dt>**Несовместимые параметры**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="eb91c-138"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>                    | <span data-ttu-id="eb91c-139">Один или несколько входных параметров несовместимы в качестве набора или относительно целевого узла.</span><span class="sxs-lookup"><span data-stu-id="eb91c-139">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="eb91c-140">Например, значение параметра *мигратионневсеттингдата* содержит свойства, которые не поддерживаются целевой системой узла, указанной значением параметра *дестинатионхост* .</span><span class="sxs-lookup"><span data-stu-id="eb91c-140">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationHost* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="eb91c-141"><dt>**Зарезервировано DMTF**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="eb91c-141"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="eb91c-142"><dt>**Параметры метода проверены — задание запущено**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="eb91c-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="eb91c-143"><dt>**Метод reserved**</dt> <dt>4097.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="eb91c-143"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="eb91c-144"><dt>**Независимый от поставщика**</dt> <dt>32768.65 535</dt></span><span class="sxs-lookup"><span data-stu-id="eb91c-144"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="eb91c-145">Требования</span><span class="sxs-lookup"><span data-stu-id="eb91c-145">Requirements</span></span>



| <span data-ttu-id="eb91c-146">Требование</span><span class="sxs-lookup"><span data-stu-id="eb91c-146">Requirement</span></span> | <span data-ttu-id="eb91c-147">Значение</span><span class="sxs-lookup"><span data-stu-id="eb91c-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb91c-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb91c-148">Minimum supported client</span></span><br/> | <span data-ttu-id="eb91c-149">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="eb91c-149">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="eb91c-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb91c-150">Minimum supported server</span></span><br/> | <span data-ttu-id="eb91c-151">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="eb91c-151">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="eb91c-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="eb91c-152">Namespace</span></span><br/>                | <span data-ttu-id="eb91c-153">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="eb91c-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="eb91c-154">MOF</span><span class="sxs-lookup"><span data-stu-id="eb91c-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb91c-155"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb91c-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb91c-156">DLL</span><span class="sxs-lookup"><span data-stu-id="eb91c-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb91c-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eb91c-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eb91c-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb91c-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb91c-159">**\_ВИРТУАЛСИСТЕММИГРАТИОНСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="eb91c-159">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




