---
description: Добавляет параметры Ethernet-компонентов в конфигурацию подключения Ethernet виртуальной машины.
ms.assetid: f233bf2f-5201-4b02-8384-bb7e2d1e7dee
title: Метод Аддфеатуресеттингс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5e9acbaaf6ff1da6439dcb243869e09133e0031e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345562"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="7acdc-103">Метод Аддфеатуресеттингс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="7acdc-103">AddFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="7acdc-104">Добавляет параметры Ethernet-компонентов в конфигурацию подключения Ethernet виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7acdc-104">Adds Ethernet feature settings to the configuration of a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7acdc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7acdc-105">Syntax</span></span>


```mof
uint32 AddFeatureSettings(
  [in]  Msvm_EthernetPortAllocationSettingData    REF AffectedConfiguration,
  [in]  string                                        FeatureSettings[],
  [out] Msvm_EthernetSwitchPortFeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7acdc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7acdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7acdc-107">*Аффектедконфигуратион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7acdc-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7acdc-108">Ссылка на экземпляр класса [**мсвм \_ есернетпорталлокатионсеттингдата**](msvm-ethernetportallocationsettingdata.md) , представляющий затронутое подключение Ethernet.</span><span class="sxs-lookup"><span data-stu-id="7acdc-108">Reference to an instance of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that represents the affected Ethernet connection.</span></span>

</dd> <dt>

<span data-ttu-id="7acdc-109">*Феатуресеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7acdc-109">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7acdc-110">Массив строк, содержащий один встроенный экземпляр класса [**мсвм \_ есернетсвитчфеатуресеттингдата**](msvm-ethernetswitchfeaturesettingdata.md) , который описывает параметры компонентов, добавляемых в конфигурацию соединения.</span><span class="sxs-lookup"><span data-stu-id="7acdc-110">An array of strings that contain one embedded instance of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class that describes the feature settings to be added to the connection configuration.</span></span>

</dd> <dt>

<span data-ttu-id="7acdc-111">*Ресултингфеатуресеттингс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7acdc-111">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7acdc-112">Массив ссылок на экземпляры класса [**мсвм \_ есернетсвитчфеатуресеттингдата**](msvm-ethernetswitchportfeaturesettingdata.md) , представляющие добавленные параметры функции.</span><span class="sxs-lookup"><span data-stu-id="7acdc-112">An array of references to instances of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represents the added feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="7acdc-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7acdc-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7acdc-114">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7acdc-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7acdc-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7acdc-115">Return value</span></span>

<span data-ttu-id="7acdc-116">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7acdc-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7acdc-117">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="7acdc-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7acdc-118">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="7acdc-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7acdc-119">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="7acdc-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7acdc-120">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="7acdc-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7acdc-121">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="7acdc-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7acdc-122">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="7acdc-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7acdc-123">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="7acdc-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7acdc-124">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="7acdc-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7acdc-125">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="7acdc-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7acdc-126">Требования</span><span class="sxs-lookup"><span data-stu-id="7acdc-126">Requirements</span></span>



| <span data-ttu-id="7acdc-127">Требование</span><span class="sxs-lookup"><span data-stu-id="7acdc-127">Requirement</span></span> | <span data-ttu-id="7acdc-128">Значение</span><span class="sxs-lookup"><span data-stu-id="7acdc-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7acdc-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7acdc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7acdc-130">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7acdc-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7acdc-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7acdc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7acdc-132">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7acdc-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7acdc-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7acdc-133">Namespace</span></span><br/>                | <span data-ttu-id="7acdc-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7acdc-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7acdc-135">MOF</span><span class="sxs-lookup"><span data-stu-id="7acdc-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7acdc-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7acdc-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7acdc-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7acdc-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7acdc-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7acdc-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7acdc-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7acdc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7acdc-140">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="7acdc-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

