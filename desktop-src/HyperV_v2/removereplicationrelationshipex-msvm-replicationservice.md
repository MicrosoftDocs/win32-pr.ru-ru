---
description: Удаляет указанное отношение репликации виртуальной машины.
ms.assetid: 0D5013CE-7BAE-4A99-ABF2-F1ECC644A1B2
title: 'Метод Msvm_ReplicationService:: Ремоверепликатионрелатионшипекс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveReplicationRelationshipEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c57ed7f9a88789d04a20de0fd199d460b47c1eb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662508"
---
# <a name="msvm_replicationserviceremovereplicationrelationshipex-method"></a><span data-ttu-id="b994f-103">Мсвм \_ репликатионсервице:: ремоверепликатионрелатионшипекс, метод</span><span class="sxs-lookup"><span data-stu-id="b994f-103">Msvm\_ReplicationService::RemoveReplicationRelationshipEx method</span></span>

<span data-ttu-id="b994f-104">Удаляет указанное отношение репликации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b994f-104">Removes the specified virtual machine replication relationship.</span></span>

## <a name="syntax"></a><span data-ttu-id="b994f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b994f-105">Syntax</span></span>


```C++
uint32 RemoveReplicationRelationshipEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="b994f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b994f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b994f-107">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b994f-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b994f-108">Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину, для которой необходимо удалить репликацию.</span><span class="sxs-lookup"><span data-stu-id="b994f-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to remove the replication.</span></span>

</dd> <dt>

<span data-ttu-id="b994f-109">*Репликатионрелатионшип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b994f-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b994f-110">Строковое представление внедренного экземпляра класса [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) , определяющего отношение репликации для удаления.</span><span class="sxs-lookup"><span data-stu-id="b994f-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship to remove.</span></span>

</dd> <dt>

<span data-ttu-id="b994f-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b994f-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b994f-112">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b994f-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="b994f-113">Если задача завершена, ссылка может иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="b994f-113">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b994f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b994f-114">Return value</span></span>

<span data-ttu-id="b994f-115">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b994f-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b994f-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="b994f-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b994f-117">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="b994f-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b994f-118">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="b994f-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b994f-119">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="b994f-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b994f-120">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="b994f-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b994f-121">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="b994f-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b994f-122">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="b994f-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b994f-123">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="b994f-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b994f-124">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="b994f-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b994f-125">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="b994f-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b994f-126">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="b994f-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b994f-127">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="b994f-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b994f-128">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="b994f-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="b994f-129">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="b994f-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="b994f-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b994f-130">Remarks</span></span>

<span data-ttu-id="b994f-131">Для виртуальной машины реплики невозможно удалить первичную репликацию, если включена расширенная репликация.</span><span class="sxs-lookup"><span data-stu-id="b994f-131">For a replica virtual machine, primary replication can't be removed if extended replication is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="b994f-132">Требования</span><span class="sxs-lookup"><span data-stu-id="b994f-132">Requirements</span></span>



| <span data-ttu-id="b994f-133">Требование</span><span class="sxs-lookup"><span data-stu-id="b994f-133">Requirement</span></span> | <span data-ttu-id="b994f-134">Значение</span><span class="sxs-lookup"><span data-stu-id="b994f-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b994f-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b994f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b994f-136">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b994f-136">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b994f-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b994f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b994f-138">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b994f-138">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b994f-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b994f-139">Namespace</span></span><br/>                | <span data-ttu-id="b994f-140">\\\\Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="b994f-140">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="b994f-141">MOF</span><span class="sxs-lookup"><span data-stu-id="b994f-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b994f-142"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b994f-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b994f-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b994f-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b994f-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b994f-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b994f-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b994f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b994f-146">**CreateReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="b994f-146">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="b994f-147">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="b994f-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

