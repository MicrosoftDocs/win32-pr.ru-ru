---
description: Создает новый виртуальный коммутатор.
ms.assetid: de7495e9-48c5-427a-b9bb-0821b53a9b09
title: Метод Дефинесистем класса Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bd6e2dfb7d9cf7e64fb76c35f6f3c3b8457d69d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911695"
---
# <a name="definesystem-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="6ff5d-103">Метод Дефинесистем \_ класса Виртуалесернетсвитчманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="6ff5d-103">DefineSystem method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="6ff5d-104">Создает новый виртуальный коммутатор.</span><span class="sxs-lookup"><span data-stu-id="6ff5d-104">Creates a new virtual switch.</span></span> <span data-ttu-id="6ff5d-105">Свойства, которые не указаны, будут заполнены значениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6ff5d-105">Properties that are not specified will be populated with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ff5d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ff5d-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6ff5d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ff5d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ff5d-108">*SystemSettings* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ff5d-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ff5d-109">Встроенный экземпляр класса [**мсвм \_ виртуалесернетсвитчсеттингдата**](msvm-virtualethernetswitchsettingdata.md) , который используется для определения атрибутов создаваемого виртуального коммутатора.</span><span class="sxs-lookup"><span data-stu-id="6ff5d-109">An embedded instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that is used to define the attributes of the virtual switch to be created.</span></span> <span data-ttu-id="6ff5d-110">Этот параметр обязателен.</span><span class="sxs-lookup"><span data-stu-id="6ff5d-110">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="6ff5d-111">*Ресаурцесеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ff5d-111">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ff5d-112">Массив внедренных экземпляров класса [**мсвм \_ есернетпорталлокатионсеттингдата**](msvm-ethernetportallocationsettingdata.md) , описывающих параметры портов коммутатора, которые будут созданы в области действия нового виртуального коммутатора.</span><span class="sxs-lookup"><span data-stu-id="6ff5d-112">An array of embedded instances of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that describes the settings of the switch ports to be created in the scope of the new virtual switch.</span></span> <span data-ttu-id="6ff5d-113">Если указано **значение NULL** , виртуальный коммутатор будет создан без ресурсов (т. е. нет портов коммутатора).</span><span class="sxs-lookup"><span data-stu-id="6ff5d-113">If **Null** is specified, the virtual switch will be created with no resources (i.e. no switch ports).</span></span>

</dd> <dt>

<span data-ttu-id="6ff5d-114">*Референцеконфигуратион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ff5d-114">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ff5d-115">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="6ff5d-115">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6ff5d-116">*Ресултингсистем* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6ff5d-116">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ff5d-117">Если виртуальный коммутатор успешно создан, ссылка на экземпляр класса [**мсвм \_ виртуалесернетсвитч**](msvm-virtualethernetswitch.md) , представляющий только что определенный виртуальный коммутатор.</span><span class="sxs-lookup"><span data-stu-id="6ff5d-117">If a virtual switch is successfully created, a reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the newly defined virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="6ff5d-118">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6ff5d-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ff5d-119">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6ff5d-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ff5d-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ff5d-120">Return value</span></span>

<span data-ttu-id="6ff5d-121">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6ff5d-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6ff5d-122">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="6ff5d-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6ff5d-123">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="6ff5d-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6ff5d-124">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="6ff5d-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6ff5d-125">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="6ff5d-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6ff5d-126">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="6ff5d-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6ff5d-127">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="6ff5d-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6ff5d-128">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="6ff5d-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6ff5d-129">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="6ff5d-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="6ff5d-130">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="6ff5d-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6ff5d-131">Требования</span><span class="sxs-lookup"><span data-stu-id="6ff5d-131">Requirements</span></span>



| <span data-ttu-id="6ff5d-132">Требование</span><span class="sxs-lookup"><span data-stu-id="6ff5d-132">Requirement</span></span> | <span data-ttu-id="6ff5d-133">Значение</span><span class="sxs-lookup"><span data-stu-id="6ff5d-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ff5d-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ff5d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6ff5d-135">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6ff5d-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6ff5d-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ff5d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6ff5d-137">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6ff5d-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6ff5d-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6ff5d-138">Namespace</span></span><br/>                | <span data-ttu-id="6ff5d-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6ff5d-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6ff5d-140">MOF</span><span class="sxs-lookup"><span data-stu-id="6ff5d-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ff5d-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ff5d-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ff5d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6ff5d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ff5d-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6ff5d-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6ff5d-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ff5d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ff5d-145">**Мсвм \_ виртуалесернетсвитчманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="6ff5d-145">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

