---
description: Метод, позволяющий выполнить предварительную проверку, чтобы определить, может ли виртуальная система быть успешно перенесена на целевой узел, заданный сетевым именем или IP-адресом.
ms.assetid: bfcd4063-30fe-4d18-9df9-7b84a680814c
title: Метод Чекквиртуалсистемисмигратаблетохост класса CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5769691a792b8f74225b640b0058ad4bd0e27c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683306"
---
# <a name="checkvirtualsystemismigratabletohost-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="5ce32-103">Метод Чекквиртуалсистемисмигратаблетохост \_ класса CIM виртуалсистеммигратионсервице</span><span class="sxs-lookup"><span data-stu-id="5ce32-103">CheckVirtualSystemIsMigratableToHost method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="5ce32-104">Метод, позволяющий выполнить предварительную проверку, чтобы определить, может ли виртуальная система быть успешно перенесена на целевой узел, заданный сетевым именем или IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="5ce32-104">Method to perform a pre-check to determine whether a virtual system is likely to be successfully migrated to a target host specified by a network name or IP address.</span></span> <span data-ttu-id="5ce32-105">Этот метод не гарантирует, что последующая миграция всегда будет выполнена из-за динамической доступности ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5ce32-105">This method does not guarantee that a subsequent migration will always succeed, due to dynamic resource availability.</span></span>

<span data-ttu-id="5ce32-106">Описание кода возврата:</span><span class="sxs-lookup"><span data-stu-id="5ce32-106">Return code description:</span></span>

<span data-ttu-id="5ce32-107">Примечание. Этот метод предназначен как переходное решение только после того, как будет доступно моделирование поддержки кластера.</span><span class="sxs-lookup"><span data-stu-id="5ce32-107">Note: This method is intended as a transitional solution only until modeling of cluster support is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ce32-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ce32-108">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] boolean                IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="5ce32-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ce32-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ce32-110">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ce32-110">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ce32-111">Ссылка [**CIM \_ ComputerSystem**](cim-computersystem.md) на систему исходного виртуального компьютера для переноса.</span><span class="sxs-lookup"><span data-stu-id="5ce32-111">A [**CIM\_ComputerSystem**](cim-computersystem.md) reference to the source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="5ce32-112">*Дестинатионхост* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ce32-112">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ce32-113">Целевая система узла для миграции.</span><span class="sxs-lookup"><span data-stu-id="5ce32-113">Target host system for the migration.</span></span>

<span data-ttu-id="5ce32-114">Допустимые форматы для этого параметра передаются через значения элементов  \[ \] свойства массива дестинатионхостформатссуппортед в экземпляре [**модели CIM \_ виртуалсистеммигратионкапабилитиес**](cim-virtualsystemmigrationcapabilities.md) , связанной с Ассоциацией [**\_ елементкапабилитиес CIM**](cim-elementcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="5ce32-114">Acceptable formats for this parameter are conveyed through values of elements of the **DestinationHostFormatsSupported**\[ \] array property in the instance of the [**CIM\_VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md) that is associated through the [**CIM\_ElementCapabilities**](cim-elementcapabilities.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="5ce32-115">*Мигратионсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ce32-115">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ce32-116">Строка, содержащая встроенный экземпляр класса [**CIM \_ виртуалсистеммигратионсеттингдата**](cim-virtualsystemmigrationsettingdata.md) , представляющий параметры миграции, применимые к операции миграции.</span><span class="sxs-lookup"><span data-stu-id="5ce32-116">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="5ce32-117">*Невсистемсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ce32-117">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ce32-118">Строка, содержащая встроенный экземпляр класса [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) , представляющий новые свойства, применимые к виртуальной системе после переноса.</span><span class="sxs-lookup"><span data-stu-id="5ce32-118">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="5ce32-119">*Невресаурцесеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ce32-119">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ce32-120">Массив строк, каждый из которых содержит встроенный экземпляр класса [**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md) , представляющий новые свойства, применимые к виртуальным ресурсам в области виртуальной системы после переноса.</span><span class="sxs-lookup"><span data-stu-id="5ce32-120">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="5ce32-121">*Переносимость* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5ce32-121">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ce32-122">Результат проверки миграции, указывающий, можно ли успешно выполнить миграцию виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="5ce32-122">The migration check result indicating whether or not the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ce32-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ce32-123">Return value</span></span>

<span data-ttu-id="5ce32-124">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="5ce32-124">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="5ce32-125">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="5ce32-125">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="5ce32-126">Описание</span><span class="sxs-lookup"><span data-stu-id="5ce32-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5ce32-127"><dt>**Завершено без ошибки**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5ce32-127"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="5ce32-128">Проверка выполнена; результат, полученный с помощью значения \[ \]  параметра out.</span><span class="sxs-lookup"><span data-stu-id="5ce32-128">Check performed; result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="5ce32-129"><dt>**Не поддерживается**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5ce32-129"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="5ce32-130">Метод не поддерживается реализацией.</span><span class="sxs-lookup"><span data-stu-id="5ce32-130">Method not supported by implementation.</span></span> <span data-ttu-id="5ce32-131">Нет результатов, переданных через значение \[ параметра out \]  .</span><span class="sxs-lookup"><span data-stu-id="5ce32-131">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="5ce32-132"><dt>**Сбой**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5ce32-132"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="5ce32-133">Проверка не пройдена по неуказанным причинам.</span><span class="sxs-lookup"><span data-stu-id="5ce32-133">Check failed for unspecified reasons.</span></span> <span data-ttu-id="5ce32-134">Нет результатов, переданных через значение \[ параметра out \]  .</span><span class="sxs-lookup"><span data-stu-id="5ce32-134">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="5ce32-135"><dt>**Время ожидания**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5ce32-135"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                    | <span data-ttu-id="5ce32-136">Время ожидания проверки истекло. Нет результатов, переданных через значение \[ параметра out \]  .</span><span class="sxs-lookup"><span data-stu-id="5ce32-136">Check timed out. No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="5ce32-137"><dt>**Недопустимый параметр**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="5ce32-137"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="5ce32-138">Один или несколько параметров формально являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="5ce32-138">One or more parameters are formally invalid.</span></span> <span data-ttu-id="5ce32-139">Например, значение параметра *дестинатионхост* могло быть указано в неподдерживаемом формате.</span><span class="sxs-lookup"><span data-stu-id="5ce32-139">For example, the value of the *DestinationHost* parameter could have been specified in an unsupported format.</span></span> <span data-ttu-id="5ce32-140">Нет результатов, переданных через значение \[ параметра out \]  .</span><span class="sxs-lookup"><span data-stu-id="5ce32-140">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                    |
| <dl> <span data-ttu-id="5ce32-141"><dt>**Недопустимое состояние**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="5ce32-141"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>              | <span data-ttu-id="5ce32-142">Исходная виртуальная система, исходная система узла или целевая система узла находятся в состоянии, которое разрешает инициацию запрошенной миграции виртуальной системы. Это может быть временным условием.</span><span class="sxs-lookup"><span data-stu-id="5ce32-142">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span> <span data-ttu-id="5ce32-143">Нет результатов, переданных через значение \[ параметра out \]  .</span><span class="sxs-lookup"><span data-stu-id="5ce32-143">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="5ce32-144"><dt>**Несовместимые параметры**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="5ce32-144"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>    | <span data-ttu-id="5ce32-145">Один или несколько входных параметров несовместимы в качестве набора или относительно целевого узла.</span><span class="sxs-lookup"><span data-stu-id="5ce32-145">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="5ce32-146">Например, значение параметра *мигратионневсеттингдата* содержит свойства, которые не поддерживаются целевой системой узла, указанной значением параметра *дестинатионхост* .</span><span class="sxs-lookup"><span data-stu-id="5ce32-146">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationHost* parameter.</span></span> <span data-ttu-id="5ce32-147">Нет результатов, переданных через значение \[ параметра out \]  .</span><span class="sxs-lookup"><span data-stu-id="5ce32-147">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="5ce32-148"><dt>**Зарезервировано DMTF**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="5ce32-148"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="5ce32-149"><dt>**Метод reserved**</dt> <dt>4097.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="5ce32-149"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="5ce32-150"><dt>**Независимый от поставщика**</dt> <dt>32768.65 535</dt></span><span class="sxs-lookup"><span data-stu-id="5ce32-150"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="requirements"></a><span data-ttu-id="5ce32-151">Требования</span><span class="sxs-lookup"><span data-stu-id="5ce32-151">Requirements</span></span>



| <span data-ttu-id="5ce32-152">Требование</span><span class="sxs-lookup"><span data-stu-id="5ce32-152">Requirement</span></span> | <span data-ttu-id="5ce32-153">Значение</span><span class="sxs-lookup"><span data-stu-id="5ce32-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ce32-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ce32-154">Minimum supported client</span></span><br/> | <span data-ttu-id="5ce32-155">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5ce32-155">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="5ce32-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ce32-156">Minimum supported server</span></span><br/> | <span data-ttu-id="5ce32-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5ce32-157">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="5ce32-158">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5ce32-158">Namespace</span></span><br/>                | <span data-ttu-id="5ce32-159">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="5ce32-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5ce32-160">MOF</span><span class="sxs-lookup"><span data-stu-id="5ce32-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ce32-161"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ce32-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ce32-162">DLL</span><span class="sxs-lookup"><span data-stu-id="5ce32-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ce32-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5ce32-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5ce32-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ce32-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ce32-165">**\_ВИРТУАЛСИСТЕММИГРАТИОНСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="5ce32-165">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




