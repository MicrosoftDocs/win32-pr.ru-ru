---
description: Инициирует отработку отказа для виртуальной машины в приложение или образ точки репликации уровня "Стандартный".
ms.assetid: cd7e9398-c234-4637-906d-69b46ebf3f51
title: Метод Инитиатефаиловер класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0f05a9b126028b741782d253ac12b79f9f88e1e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344542"
---
# <a name="initiatefailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="ebb65-103">Метод Инитиатефаиловер \_ класса Репликатионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="ebb65-103">InitiateFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="ebb65-104">Инициирует отработку отказа для виртуальной машины в приложение или образ точки репликации уровня "Стандартный".</span><span class="sxs-lookup"><span data-stu-id="ebb65-104">Initiates a failover for a virtual machine to an application or standard replication point image.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebb65-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebb65-105">Syntax</span></span>


```mof
uint32 InitiateFailover(
  [in]  CIM_ComputerSystem           REF ComputerSystem,
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ebb65-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ebb65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebb65-107">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ebb65-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebb65-108">Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину, для которой необходимо инициировать отработку отказа.</span><span class="sxs-lookup"><span data-stu-id="ebb65-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to initiate a failover.</span></span>

</dd> <dt>

<span data-ttu-id="ebb65-109">*Снапшотсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ebb65-109">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebb65-110">Ссылка на экземпляр [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)) , представляющий моментальный снимок, используемый для отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="ebb65-110">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance that represents the snapshot used for the failover.</span></span> <span data-ttu-id="ebb65-111">Если этот параметр имеет **значение NULL**, отработка отказа выполняется до последней точки во времени.</span><span class="sxs-lookup"><span data-stu-id="ebb65-111">If this parameter is **Null**, the failover is to be performed to the latest point in time.</span></span>

</dd> <dt>

<span data-ttu-id="ebb65-112">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ebb65-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebb65-113">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ebb65-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebb65-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ebb65-114">Return value</span></span>

<span data-ttu-id="ebb65-115">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ebb65-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ebb65-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="ebb65-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ebb65-117">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="ebb65-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ebb65-118">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="ebb65-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ebb65-119">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="ebb65-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ebb65-120">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="ebb65-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ebb65-121">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="ebb65-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ebb65-122">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="ebb65-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ebb65-123">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="ebb65-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ebb65-124">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="ebb65-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ebb65-125">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="ebb65-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ebb65-126">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="ebb65-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ebb65-127">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="ebb65-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ebb65-128">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="ebb65-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="ebb65-129">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="ebb65-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ebb65-130">Требования</span><span class="sxs-lookup"><span data-stu-id="ebb65-130">Requirements</span></span>



| <span data-ttu-id="ebb65-131">Требование</span><span class="sxs-lookup"><span data-stu-id="ebb65-131">Requirement</span></span> | <span data-ttu-id="ebb65-132">Значение</span><span class="sxs-lookup"><span data-stu-id="ebb65-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebb65-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ebb65-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ebb65-134">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ebb65-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ebb65-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ebb65-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ebb65-136">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ebb65-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ebb65-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ebb65-137">Namespace</span></span><br/>                | <span data-ttu-id="ebb65-138">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ebb65-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ebb65-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ebb65-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ebb65-140"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ebb65-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ebb65-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ebb65-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebb65-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ebb65-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ebb65-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ebb65-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebb65-144">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="ebb65-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="ebb65-145">**ревертфаиловер**</span><span class="sxs-lookup"><span data-stu-id="ebb65-145">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="ebb65-146">**сетфаиловернетворкадаптерсеттингс**</span><span class="sxs-lookup"><span data-stu-id="ebb65-146">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md)
</dt> </dl>

 

