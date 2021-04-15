---
description: См. Дополнительные сведения о методе Чекквиртуалсистемисмигратаблетосистем класса CIM_VirtualSystemMigrationService
ms.assetid: d3f7c926-804f-4c7c-8964-a8e464155417
title: Метод Чекквиртуалсистемисмигратаблетосистем класса CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: be85c51cb507fea3cea14f1706ffa8f67af06c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683305"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="f7571-103">Метод Чекквиртуалсистемисмигратаблетосистем \_ класса CIM виртуалсистеммигратионсервице</span><span class="sxs-lookup"><span data-stu-id="f7571-103">CheckVirtualSystemIsMigratableToSystem method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="f7571-104">Метод, позволяющий выполнить предварительную проверку, чтобы определить, может ли виртуальная система быть успешно перенесена в целевую систему.</span><span class="sxs-lookup"><span data-stu-id="f7571-104">Method to perform a pre-check to determine whether a virtual system is likely to be successfully migrated to a target system.</span></span> <span data-ttu-id="f7571-105">Этот метод не гарантирует, что последующая миграция всегда будет выполнена из-за динамической доступности ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7571-105">This method does not guarantee that a subsequent migration will always succeed, due to dynamic resource availability.</span></span> <span data-ttu-id="f7571-106">Описание кода возврата:</span><span class="sxs-lookup"><span data-stu-id="f7571-106">Return code description:</span></span>

## <a name="syntax"></a><span data-ttu-id="f7571-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7571-107">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] boolean                IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="f7571-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7571-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7571-109">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f7571-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7571-110">[**Модель CIM \_ Экземпляр ComputerSystem**](cim-computersystem.md) , ссылающийся на систему исходного виртуального компьютера для переноса.</span><span class="sxs-lookup"><span data-stu-id="f7571-110">[**CIM\_ComputerSystem**](cim-computersystem.md) instance referencing the source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="f7571-111">*Дестинатионсистем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f7571-111">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7571-112">[**Модель CIM \_ Экземпляр системы**](cim-system.md) , ссылающийся на целевую систему, на которую будет перенесена виртуальная система.</span><span class="sxs-lookup"><span data-stu-id="f7571-112">[**CIM\_System**](cim-system.md) instance referencing the destination system onto which to migrate the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="f7571-113">*Мигратионсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f7571-113">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7571-114">Строка, содержащая встроенный экземпляр класса [**CIM \_ виртуалсистеммигратионсеттингдата**](cim-virtualsystemmigrationsettingdata.md) , представляющий параметры миграции, применимые к операции миграции.</span><span class="sxs-lookup"><span data-stu-id="f7571-114">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="f7571-115">*Невсистемсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f7571-115">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7571-116">Строка, содержащая встроенный экземпляр класса [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) , представляющий новые свойства, применимые к виртуальной системе после переноса.</span><span class="sxs-lookup"><span data-stu-id="f7571-116">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="f7571-117">*Невресаурцесеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f7571-117">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7571-118">Массив строк, каждый из которых содержит встроенный экземпляр класса [**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md) , представляющий новые свойства, применимые к виртуальным ресурсам в области виртуальной системы после переноса.</span><span class="sxs-lookup"><span data-stu-id="f7571-118">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="f7571-119">*Переносимость* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f7571-119">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7571-120">Результат проверки миграции, указывающий, можно ли успешно выполнить миграцию виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="f7571-120">The migration check result indicating whether or not the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7571-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7571-121">Return value</span></span>

<span data-ttu-id="f7571-122">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="f7571-122">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="f7571-123">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="f7571-123">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="f7571-124">Описание</span><span class="sxs-lookup"><span data-stu-id="f7571-124">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f7571-125"><dt>**Завершено без ошибки**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f7571-125"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="f7571-126">Проверка выполнена; результат, полученный с помощью значения \[ \]  параметра out.</span><span class="sxs-lookup"><span data-stu-id="f7571-126">Check performed; result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="f7571-127"><dt>**Не поддерживается**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f7571-127"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="f7571-128">Метод не поддерживается реализацией.</span><span class="sxs-lookup"><span data-stu-id="f7571-128">Method not supported by implementation.</span></span> <span data-ttu-id="f7571-129">Нет результатов, переданных через значение \[ параметра out \]  .</span><span class="sxs-lookup"><span data-stu-id="f7571-129">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="f7571-130"><dt>**Сбой**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f7571-130"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="f7571-131">Проверка не пройдена по неуказанным причинам.</span><span class="sxs-lookup"><span data-stu-id="f7571-131">Check failed for unspecified reasons.</span></span> <span data-ttu-id="f7571-132">Нет результатов, переданных через значение \[ параметра out \]  .</span><span class="sxs-lookup"><span data-stu-id="f7571-132">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="f7571-133"><dt>**Время ожидания**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f7571-133"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                    | <span data-ttu-id="f7571-134">Время ожидания проверки истекло. Нет результатов, переданных через значение \[ параметра out \]  .</span><span class="sxs-lookup"><span data-stu-id="f7571-134">Check timed out. No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="f7571-135"><dt>**Недопустимый параметр**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f7571-135"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="f7571-136">Один или несколько параметров формально являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="f7571-136">One or more parameters are formally invalid.</span></span> <span data-ttu-id="f7571-137">Например, значение параметра *дестинатионсистем* не включает допустимый путь к объекту.</span><span class="sxs-lookup"><span data-stu-id="f7571-137">For example, the value of the *DestinationSystem* parameter does not comprise a valid object path.</span></span> <span data-ttu-id="f7571-138">Нет результатов, переданных через значение \[ параметра out \]  .</span><span class="sxs-lookup"><span data-stu-id="f7571-138">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="f7571-139"><dt>**Недопустимое состояние**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="f7571-139"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>              | <span data-ttu-id="f7571-140">Исходная виртуальная система, исходная система узла или целевая система узла находятся в состоянии, которое разрешает инициацию запрошенной миграции виртуальной системы. Это может быть временным условием.</span><span class="sxs-lookup"><span data-stu-id="f7571-140">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span> <span data-ttu-id="f7571-141">Нет результатов, переданных через значение \[ параметра out \]  .</span><span class="sxs-lookup"><span data-stu-id="f7571-141">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="f7571-142"><dt>**Несовместимые параметры**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f7571-142"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>    | <span data-ttu-id="f7571-143">Один или несколько входных параметров несовместимы в качестве набора или относительно целевого узла.</span><span class="sxs-lookup"><span data-stu-id="f7571-143">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="f7571-144">Например, значение параметра *невсеттингдата* содержит свойства, которые не поддерживаются целевой системой узла, указанной значением параметра *дестинатионсистем* .</span><span class="sxs-lookup"><span data-stu-id="f7571-144">For example the value of the *NewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationSystem* parameter.</span></span> <span data-ttu-id="f7571-145">Нет результатов, переданных через значение \[ параметра out \]  .</span><span class="sxs-lookup"><span data-stu-id="f7571-145">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="f7571-146"><dt>**Зарезервировано DMTF**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="f7571-146"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="f7571-147"><dt>**Метод reserved**</dt> <dt>4097.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="f7571-147"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="f7571-148"><dt>**Независимый от поставщика**</dt> <dt>32768.65 535</dt></span><span class="sxs-lookup"><span data-stu-id="f7571-148"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="f7571-149">Требования</span><span class="sxs-lookup"><span data-stu-id="f7571-149">Requirements</span></span>



| <span data-ttu-id="f7571-150">Требование</span><span class="sxs-lookup"><span data-stu-id="f7571-150">Requirement</span></span> | <span data-ttu-id="f7571-151">Значение</span><span class="sxs-lookup"><span data-stu-id="f7571-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7571-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7571-152">Minimum supported client</span></span><br/> | <span data-ttu-id="f7571-153">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f7571-153">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f7571-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7571-154">Minimum supported server</span></span><br/> | <span data-ttu-id="f7571-155">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f7571-155">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f7571-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f7571-156">Namespace</span></span><br/>                | <span data-ttu-id="f7571-157">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f7571-157">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f7571-158">MOF</span><span class="sxs-lookup"><span data-stu-id="f7571-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7571-159"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7571-159"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7571-160">DLL</span><span class="sxs-lookup"><span data-stu-id="f7571-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7571-161"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f7571-161"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f7571-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7571-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7571-163">**\_ВИРТУАЛСИСТЕММИГРАТИОНСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="f7571-163">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




