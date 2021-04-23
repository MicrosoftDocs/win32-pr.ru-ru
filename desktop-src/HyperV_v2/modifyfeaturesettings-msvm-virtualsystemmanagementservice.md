---
description: Изменяет текущие настройки компонентов подключения Ethernet виртуальной машины.
ms.assetid: 3caa810f-0444-45cf-88a4-e93d04accb46
title: Метод Модифифеатуресеттингс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c376158008c5ad0e611d3a05c7e73d2e7d1b44cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346065"
---
# <a name="modifyfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="28047-103">Метод Модифифеатуресеттингс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="28047-103">ModifyFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="28047-104">Изменяет текущие настройки компонентов подключения Ethernet виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="28047-104">Modifies the current feature settings of a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="28047-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28047-105">Syntax</span></span>


```mof
uint32 ModifyFeatureSettings(
  [in]  string                                        FeatureSettings[],
  [out] Msvm_EthernetSwitchPortFeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="28047-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="28047-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28047-107">*Феатуресеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28047-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28047-108">Массив строк, содержащий внедренный экземпляр класса, производного от класса [**мсвм \_ есернетсвитчфеатуресеттингдата**](msvm-ethernetswitchfeaturesettingdata.md) , который описывает изменения текущих параметров существующего подключения Ethernet.</span><span class="sxs-lookup"><span data-stu-id="28047-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class, that describes modifications to the current feature settings of an existing Ethernet connection.</span></span> <span data-ttu-id="28047-109">Свойство **InstanceId** каждого из этих экземпляров определяет изменяемые параметры компонентов.</span><span class="sxs-lookup"><span data-stu-id="28047-109">The **InstanceID** property of each of these instances identifies the feature settings to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="28047-110">*Ресултингфеатуресеттингс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="28047-110">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28047-111">Массив ссылок на экземпляры класса [**мсвм \_ есернетсвитчпортфеатуресеттингдата**](msvm-ethernetswitchportfeaturesettingdata.md) , представляющие измененные параметры функции.</span><span class="sxs-lookup"><span data-stu-id="28047-111">An array of references to instances of the [**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represent the modified feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="28047-112">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="28047-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28047-113">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="28047-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28047-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28047-114">Return value</span></span>

<span data-ttu-id="28047-115">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="28047-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="28047-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="28047-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="28047-117">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="28047-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="28047-118">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="28047-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="28047-119">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="28047-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="28047-120">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="28047-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="28047-121">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="28047-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="28047-122">**Несовместимые параметры** (6)</span><span class="sxs-lookup"><span data-stu-id="28047-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="28047-123">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="28047-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="28047-124">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="28047-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="28047-125">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="28047-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="28047-126">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="28047-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="28047-127">Требования</span><span class="sxs-lookup"><span data-stu-id="28047-127">Requirements</span></span>



| <span data-ttu-id="28047-128">Требование</span><span class="sxs-lookup"><span data-stu-id="28047-128">Requirement</span></span> | <span data-ttu-id="28047-129">Значение</span><span class="sxs-lookup"><span data-stu-id="28047-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28047-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28047-130">Minimum supported client</span></span><br/> | <span data-ttu-id="28047-131">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="28047-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="28047-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28047-132">Minimum supported server</span></span><br/> | <span data-ttu-id="28047-133">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="28047-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="28047-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="28047-134">Namespace</span></span><br/>                | <span data-ttu-id="28047-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="28047-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="28047-136">MOF</span><span class="sxs-lookup"><span data-stu-id="28047-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28047-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="28047-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="28047-138">DLL</span><span class="sxs-lookup"><span data-stu-id="28047-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28047-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="28047-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="28047-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28047-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28047-141">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="28047-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

