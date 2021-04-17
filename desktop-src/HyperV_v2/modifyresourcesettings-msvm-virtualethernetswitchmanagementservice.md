---
description: Изменяет параметры ресурсов для виртуального коммутатора.
ms.assetid: 1ae2456f-921c-4ea6-b3fb-7065110063fb
title: Метод Модифиресаурцесеттингс класса Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f40044b20389914281ad4f651019f3e8dc6b6148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683967"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="62dbd-103">Метод Модифиресаурцесеттингс \_ класса Виртуалесернетсвитчманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="62dbd-103">ModifyResourceSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="62dbd-104">Изменяет параметры ресурсов для виртуального коммутатора.</span><span class="sxs-lookup"><span data-stu-id="62dbd-104">Modifies resource settings for a virtual switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="62dbd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62dbd-105">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="62dbd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="62dbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62dbd-107">*Ресаурцесеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="62dbd-107">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62dbd-108">Массив строк, содержащий внедренный экземпляр класса, производного от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), который содержит измененные аспекты существующих виртуальных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62dbd-108">An array of strings that contain an embedded instance of a class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), that contain the modified aspects of existing virtual resources.</span></span> <span data-ttu-id="62dbd-109">Свойство **InstanceId** каждого экземпляра определяет изменяемый параметр виртуального ресурса.</span><span class="sxs-lookup"><span data-stu-id="62dbd-109">The **InstanceID** property of each instance identifies the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="62dbd-110">*Ресултингресаурцесеттингс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="62dbd-110">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62dbd-111">Массив ссылок на экземпляры объектов, производных от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) , представляющие виртуальные аспекты измененных виртуальных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62dbd-111">An array of references to instances of objects derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="62dbd-112">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="62dbd-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62dbd-113">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="62dbd-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62dbd-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62dbd-114">Return value</span></span>

<span data-ttu-id="62dbd-115">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="62dbd-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="62dbd-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="62dbd-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="62dbd-117">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="62dbd-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="62dbd-118">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="62dbd-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="62dbd-119">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="62dbd-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="62dbd-120">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="62dbd-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="62dbd-121">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="62dbd-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="62dbd-122">**Несовместимые параметры** (6)</span><span class="sxs-lookup"><span data-stu-id="62dbd-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="62dbd-123">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="62dbd-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="62dbd-124">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="62dbd-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="62dbd-125">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="62dbd-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="62dbd-126">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="62dbd-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="62dbd-127">Требования</span><span class="sxs-lookup"><span data-stu-id="62dbd-127">Requirements</span></span>



| <span data-ttu-id="62dbd-128">Требование</span><span class="sxs-lookup"><span data-stu-id="62dbd-128">Requirement</span></span> | <span data-ttu-id="62dbd-129">Значение</span><span class="sxs-lookup"><span data-stu-id="62dbd-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62dbd-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62dbd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="62dbd-131">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="62dbd-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="62dbd-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62dbd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="62dbd-133">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="62dbd-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="62dbd-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="62dbd-134">Namespace</span></span><br/>                | <span data-ttu-id="62dbd-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="62dbd-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="62dbd-136">MOF</span><span class="sxs-lookup"><span data-stu-id="62dbd-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62dbd-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62dbd-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="62dbd-138">DLL</span><span class="sxs-lookup"><span data-stu-id="62dbd-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62dbd-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="62dbd-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="62dbd-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62dbd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62dbd-141">**аддресаурцесеттингс**</span><span class="sxs-lookup"><span data-stu-id="62dbd-141">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="62dbd-142">**ремовересаурцесеттингс**</span><span class="sxs-lookup"><span data-stu-id="62dbd-142">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="62dbd-143">**Мсвм \_ виртуалесернетсвитчманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="62dbd-143">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

