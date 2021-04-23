---
description: Настройка параметров IP сетевых адаптеров для применения к виртуальной машине после отработки отказа.
ms.assetid: a49d089e-f5dc-4bfb-9f66-2593304b9795
title: Метод Сетфаиловернетворкадаптерсеттингс класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.SetFailoverNetworkAdapterSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: da5bb8c820e1dbca5103c430a7b2ce2a525a8fca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683370"
---
# <a name="setfailovernetworkadaptersettings-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="81a5c-103">Метод Сетфаиловернетворкадаптерсеттингс \_ класса Репликатионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="81a5c-103">SetFailoverNetworkAdapterSettings method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="81a5c-104">Настройка IP-параметров сетевого адаптера для применения к виртуальной машине после отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="81a5c-104">Configures the network adapter's IP settings to be applied to a virtual machine after a failover.</span></span> <span data-ttu-id="81a5c-105">Эти параметры конфигурации применяются после операции отработки отказа сразу же после установки связи с компонентом интеграции KVP Exchange, работающим в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="81a5c-105">These configuration parameters are applied after a failover operation, immediately upon establishing communication with the KVP Exchange integration component running within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="81a5c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81a5c-106">Syntax</span></span>


```mof
uint32 SetFailoverNetworkAdapterSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkSettings[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="81a5c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="81a5c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81a5c-108">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81a5c-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81a5c-109">Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину, сетевые адаптеры которой необходимо настроить.</span><span class="sxs-lookup"><span data-stu-id="81a5c-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine whose network adapters are to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="81a5c-110">*Нетворксеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81a5c-110">*NetworkSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81a5c-111">Массив внедренных экземпляров объектов [**мсвм \_ фаиловернетворкадаптерсеттингдата**](msvm-failovernetworkadaptersettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="81a5c-111">An array of embedded instances of [**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) objects.</span></span> <span data-ttu-id="81a5c-112">Каждый экземпляр описывает параметры конфигурации для одного из сетевых адаптеров в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="81a5c-112">Each instance describes the configuration parameters for one of the network adapters within the virtual machine.</span></span> <span data-ttu-id="81a5c-113">Свойства **ipaddresses** и **DHCPEnabled** должны быть указаны в каждом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="81a5c-113">The **IPAddresses** and **DHCPEnabled** properties must be specified on each instance.</span></span>

</dd> <dt>

<span data-ttu-id="81a5c-114">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="81a5c-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81a5c-115">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81a5c-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81a5c-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81a5c-116">Return value</span></span>

<span data-ttu-id="81a5c-117">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="81a5c-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="81a5c-118">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="81a5c-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81a5c-119">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="81a5c-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="81a5c-120">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="81a5c-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="81a5c-121">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="81a5c-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="81a5c-122">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="81a5c-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="81a5c-123">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="81a5c-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="81a5c-124">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="81a5c-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="81a5c-125">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="81a5c-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="81a5c-126">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="81a5c-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="81a5c-127">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="81a5c-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="81a5c-128">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="81a5c-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="81a5c-129">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="81a5c-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="81a5c-130">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="81a5c-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="81a5c-131">Требования</span><span class="sxs-lookup"><span data-stu-id="81a5c-131">Requirements</span></span>



| <span data-ttu-id="81a5c-132">Требование</span><span class="sxs-lookup"><span data-stu-id="81a5c-132">Requirement</span></span> | <span data-ttu-id="81a5c-133">Значение</span><span class="sxs-lookup"><span data-stu-id="81a5c-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81a5c-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81a5c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="81a5c-135">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="81a5c-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="81a5c-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81a5c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="81a5c-137">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="81a5c-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="81a5c-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="81a5c-138">Namespace</span></span><br/>                | <span data-ttu-id="81a5c-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="81a5c-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="81a5c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="81a5c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81a5c-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81a5c-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="81a5c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="81a5c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81a5c-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="81a5c-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="81a5c-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81a5c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81a5c-145">**инитиатефаиловер**</span><span class="sxs-lookup"><span data-stu-id="81a5c-145">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="81a5c-146">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="81a5c-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="81a5c-147">**ревертфаиловер**</span><span class="sxs-lookup"><span data-stu-id="81a5c-147">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)
</dt> </dl>

 

