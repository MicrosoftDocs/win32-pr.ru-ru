---
description: Настраивает сетевые адаптеры в гостевой операционной системе.
ms.assetid: 698e0c17-f8bd-433f-b982-5481f9701ba6
title: Метод Сетгуестнетворкадаптерконфигуратион класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.SetGuestNetworkAdapterConfiguration
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 02c79df7aa08faa842e2b702b4cf18944e96bdfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545415"
---
# <a name="setguestnetworkadapterconfiguration-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="2720d-103">Метод Сетгуестнетворкадаптерконфигуратион \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="2720d-103">SetGuestNetworkAdapterConfiguration method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="2720d-104">Настраивает сетевые адаптеры в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="2720d-104">Configures the network adapters within the guest operating system.</span></span> <span data-ttu-id="2720d-105">Эти параметры конфигурации применяются сразу же после установления связи с компонентом интеграции KVP Exchange, работающим в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="2720d-105">These configuration parameters are applied immediately upon establishing communication with the KVP Exchange integration component running within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="2720d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2720d-106">Syntax</span></span>


```mof
uint32 SetGuestNetworkAdapterConfiguration(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkConfiguration[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2720d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2720d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2720d-108">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2720d-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2720d-109">Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , сетевые адаптеры которого должны быть настроены.</span><span class="sxs-lookup"><span data-stu-id="2720d-109">A reference to the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance whose network adapters are to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="2720d-110">*NetworkConfiguration* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2720d-110">*NetworkConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2720d-111">Массив внедренных экземпляров класса [**мсвм \_ гуестнетворкадаптерконфигуратион**](msvm-guestnetworkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="2720d-111">An array of embedded instances of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class.</span></span> <span data-ttu-id="2720d-112">Каждый экземпляр описывает параметры конфигурации для одного из сетевых адаптеров в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="2720d-112">Each instance describes the configuration parameters for one of the network adapters within the virtual machine.</span></span> <span data-ttu-id="2720d-113">Для каждого экземпляра необходимо указать свойство **DHCPEnabled** .</span><span class="sxs-lookup"><span data-stu-id="2720d-113">The **DHCPEnabled** property must be specified for each instance.</span></span>

</dd> <dt>

<span data-ttu-id="2720d-114">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2720d-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2720d-115">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2720d-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2720d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2720d-116">Return value</span></span>

<span data-ttu-id="2720d-117">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="2720d-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2720d-118">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="2720d-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2720d-119">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="2720d-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2720d-120">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="2720d-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2720d-121">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="2720d-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2720d-122">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="2720d-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2720d-123">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="2720d-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2720d-124">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="2720d-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2720d-125">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="2720d-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2720d-126">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="2720d-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2720d-127">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="2720d-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2720d-128">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="2720d-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2720d-129">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="2720d-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2720d-130">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="2720d-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2720d-131">Требования</span><span class="sxs-lookup"><span data-stu-id="2720d-131">Requirements</span></span>



| <span data-ttu-id="2720d-132">Требование</span><span class="sxs-lookup"><span data-stu-id="2720d-132">Requirement</span></span> | <span data-ttu-id="2720d-133">Значение</span><span class="sxs-lookup"><span data-stu-id="2720d-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2720d-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2720d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2720d-135">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2720d-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2720d-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2720d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2720d-137">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2720d-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2720d-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2720d-138">Namespace</span></span><br/>                | <span data-ttu-id="2720d-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="2720d-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2720d-140">MOF</span><span class="sxs-lookup"><span data-stu-id="2720d-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2720d-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2720d-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2720d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2720d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2720d-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2720d-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2720d-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2720d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2720d-145">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="2720d-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

