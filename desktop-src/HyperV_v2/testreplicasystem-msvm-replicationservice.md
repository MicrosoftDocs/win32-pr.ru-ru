---
description: Создает новую реплику виртуальной машины с указанным моментальным снимком для целей тестирования.
ms.assetid: 447f3c8f-8c57-4874-9466-91c6aea533bc
title: Метод Тестрепликасистем класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicaSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 029130e619aa36d0aa9b9c1c85a877fb26e1b22b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912571"
---
# <a name="testreplicasystem-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="42b73-103">Метод Тестрепликасистем \_ класса Репликатионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="42b73-103">TestReplicaSystem method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="42b73-104">Создает новую реплику виртуальной машины с указанным моментальным снимком для целей тестирования.</span><span class="sxs-lookup"><span data-stu-id="42b73-104">Creates a new replica of a virtual machine with the specified snapshot for testing purposes.</span></span>

## <a name="syntax"></a><span data-ttu-id="42b73-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42b73-105">Syntax</span></span>


```mof
uint32 TestReplicaSystem(
  [in]  CIM_ComputerSystem           REF ComputerSystem,
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="42b73-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42b73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42b73-107">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42b73-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42b73-108">Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину, для которой должна быть протестирована репликация.</span><span class="sxs-lookup"><span data-stu-id="42b73-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be tested.</span></span>

</dd> <dt>

<span data-ttu-id="42b73-109">*Снапшотсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42b73-109">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42b73-110">Ссылка на экземпляр [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)) , представляющий моментальный снимок, используемый для создания системы тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="42b73-110">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance that represents the snapshot used to create the test failover system.</span></span> <span data-ttu-id="42b73-111">Если этот параметр имеет **значение NULL**, отработка отказа должна быть выполнена за последний момент времени.</span><span class="sxs-lookup"><span data-stu-id="42b73-111">If this parameter is **Null**, the failover is to be performed off the latest point in time.</span></span>

</dd> <dt>

<span data-ttu-id="42b73-112">*Ресултингсистем* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="42b73-112">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42b73-113">Если виртуальная машина успешно определена, получает ссылку на экземпляр класса [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий только что определенную тестовую виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="42b73-113">If a virtual machine is successfully defined, receives a reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the newly defined test virtual machine.</span></span> <span data-ttu-id="42b73-114">Если эта система больше не нужна, удалите ее, вызвав метод [**дестройсистем**](destroysystem-msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="42b73-114">When this system is no longer needed, destroy it by calling the [**DestroySystem**](destroysystem-msvm-virtualsystemmanagementservice.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="42b73-115">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="42b73-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42b73-116">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="42b73-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42b73-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42b73-117">Return value</span></span>

<span data-ttu-id="42b73-118">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="42b73-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="42b73-119">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="42b73-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="42b73-120">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="42b73-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="42b73-121">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="42b73-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="42b73-122">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="42b73-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="42b73-123">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="42b73-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="42b73-124">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="42b73-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="42b73-125">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="42b73-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="42b73-126">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="42b73-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="42b73-127">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="42b73-127">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="42b73-128">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="42b73-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="42b73-129">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="42b73-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="42b73-130">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="42b73-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="42b73-131">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="42b73-131">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="42b73-132">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="42b73-132">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="42b73-133">Требования</span><span class="sxs-lookup"><span data-stu-id="42b73-133">Requirements</span></span>



| <span data-ttu-id="42b73-134">Требование</span><span class="sxs-lookup"><span data-stu-id="42b73-134">Requirement</span></span> | <span data-ttu-id="42b73-135">Значение</span><span class="sxs-lookup"><span data-stu-id="42b73-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42b73-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42b73-136">Minimum supported client</span></span><br/> | <span data-ttu-id="42b73-137">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="42b73-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="42b73-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42b73-138">Minimum supported server</span></span><br/> | <span data-ttu-id="42b73-139">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="42b73-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="42b73-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="42b73-140">Namespace</span></span><br/>                | <span data-ttu-id="42b73-141">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="42b73-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="42b73-142">MOF</span><span class="sxs-lookup"><span data-stu-id="42b73-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42b73-143"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42b73-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="42b73-144">DLL</span><span class="sxs-lookup"><span data-stu-id="42b73-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42b73-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="42b73-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="42b73-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42b73-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42b73-147">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="42b73-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

