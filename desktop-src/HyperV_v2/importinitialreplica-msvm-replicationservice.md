---
description: Импортирует начальную репликацию для виртуальной машины.
ms.assetid: 151211fe-e58e-4fd4-87cd-cdb2ad55c0b1
title: Метод Импортинитиалреплика класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ImportInitialReplica
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b60ab10c6387127c294a472c9e1e86be7fd84146
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155547"
---
# <a name="importinitialreplica-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="9fb08-103">Метод Импортинитиалреплика \_ класса Репликатионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="9fb08-103">ImportInitialReplica method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="9fb08-104">Импортирует начальную репликацию для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9fb08-104">Imports the initial replication for a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fb08-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9fb08-105">Syntax</span></span>


```mof
uint32 ImportInitialReplica(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 InitialReplicationImportLocation,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="9fb08-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9fb08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fb08-107">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9fb08-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb08-108">Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину, для которой должна быть импортирована начальная репликация.</span><span class="sxs-lookup"><span data-stu-id="9fb08-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the initial replication should be imported.</span></span>

</dd> <dt>

<span data-ttu-id="9fb08-109">*Инитиалрепликатионимпортлокатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9fb08-109">*InitialReplicationImportLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb08-110">Полный путь к каталогу, из которого должна быть импортирована начальная репликация.</span><span class="sxs-lookup"><span data-stu-id="9fb08-110">The fully qualified path of the directory from which the initial replication is to be imported.</span></span> <span data-ttu-id="9fb08-111">Это значение не может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="9fb08-111">This cannot be **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9fb08-112">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9fb08-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb08-113">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9fb08-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fb08-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9fb08-114">Return value</span></span>

<span data-ttu-id="9fb08-115">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9fb08-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9fb08-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="9fb08-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9fb08-117">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="9fb08-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9fb08-118">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="9fb08-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9fb08-119">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="9fb08-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9fb08-120">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="9fb08-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9fb08-121">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="9fb08-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9fb08-122">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="9fb08-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9fb08-123">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="9fb08-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9fb08-124">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="9fb08-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9fb08-125">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="9fb08-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9fb08-126">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="9fb08-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9fb08-127">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="9fb08-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9fb08-128">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="9fb08-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="9fb08-129">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="9fb08-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9fb08-130">Требования</span><span class="sxs-lookup"><span data-stu-id="9fb08-130">Requirements</span></span>



| <span data-ttu-id="9fb08-131">Требование</span><span class="sxs-lookup"><span data-stu-id="9fb08-131">Requirement</span></span> | <span data-ttu-id="9fb08-132">Значение</span><span class="sxs-lookup"><span data-stu-id="9fb08-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fb08-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9fb08-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9fb08-134">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9fb08-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9fb08-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9fb08-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9fb08-136">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9fb08-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9fb08-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9fb08-137">Namespace</span></span><br/>                | <span data-ttu-id="9fb08-138">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9fb08-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9fb08-139">MOF</span><span class="sxs-lookup"><span data-stu-id="9fb08-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fb08-140"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9fb08-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9fb08-141">DLL</span><span class="sxs-lookup"><span data-stu-id="9fb08-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fb08-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9fb08-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9fb08-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9fb08-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fb08-144">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="9fb08-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

