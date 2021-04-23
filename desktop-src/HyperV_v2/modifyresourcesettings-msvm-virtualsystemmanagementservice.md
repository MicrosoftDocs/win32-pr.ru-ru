---
description: Изменяет параметры виртуального ресурса.
ms.assetid: 3fb2a65f-9f40-4eb9-99e8-8fe1451427d9
title: Метод Модифиресаурцесеттингс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 872e81926f717671b741a89c9bf954e452803b36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911680"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="e9307-103">Метод Модифиресаурцесеттингс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="e9307-103">ModifyResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="e9307-104">Изменяет параметры виртуального ресурса.</span><span class="sxs-lookup"><span data-stu-id="e9307-104">Modifies virtual resource settings.</span></span> <span data-ttu-id="e9307-105">При применении к частям текущей конфигурации виртуальной машины в качестве побочного действия ресурсы активной виртуальной машины могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="e9307-105">When applied to parts of a current virtual machine configuration, as a side effect, the resources of the active virtual machine may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9307-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9307-106">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e9307-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9307-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9307-108">*Ресаурцесеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e9307-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9307-109">Массив строк, содержащий внедренный экземпляр класса, производного от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), который содержит измененные аспекты существующих виртуальных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e9307-109">An array of strings that contain an embedded instance of a class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), that contain the modified aspects of existing virtual resources.</span></span> <span data-ttu-id="e9307-110">Свойство **InstanceId** каждого экземпляра определяет изменяемый параметр виртуального ресурса.</span><span class="sxs-lookup"><span data-stu-id="e9307-110">The **InstanceID** property of each instance identifies the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="e9307-111">*Ресултингресаурцесеттингс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e9307-111">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9307-112">Массив ссылок на экземпляры объектов, производных от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) , представляющие виртуальные аспекты измененных виртуальных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e9307-112">An array of references to instances of objects derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="e9307-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e9307-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9307-114">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e9307-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9307-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9307-115">Return value</span></span>

<span data-ttu-id="e9307-116">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e9307-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e9307-117">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="e9307-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e9307-118">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="e9307-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e9307-119">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="e9307-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e9307-120">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="e9307-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e9307-121">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="e9307-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e9307-122">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="e9307-122">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e9307-123">**Несовместимые параметры** (6)</span><span class="sxs-lookup"><span data-stu-id="e9307-123">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e9307-124">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="e9307-124">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e9307-125">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="e9307-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e9307-126">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e9307-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="e9307-127">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="e9307-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e9307-128">Требования</span><span class="sxs-lookup"><span data-stu-id="e9307-128">Requirements</span></span>



| <span data-ttu-id="e9307-129">Требование</span><span class="sxs-lookup"><span data-stu-id="e9307-129">Requirement</span></span> | <span data-ttu-id="e9307-130">Значение</span><span class="sxs-lookup"><span data-stu-id="e9307-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9307-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9307-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e9307-132">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e9307-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e9307-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9307-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e9307-134">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e9307-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e9307-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e9307-135">Namespace</span></span><br/>                | <span data-ttu-id="e9307-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e9307-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e9307-137">MOF</span><span class="sxs-lookup"><span data-stu-id="e9307-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9307-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9307-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9307-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e9307-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9307-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e9307-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e9307-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9307-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9307-142">**Модифивиртуалсистемресаурцес (v1)**</span><span class="sxs-lookup"><span data-stu-id="e9307-142">**ModifyVirtualSystemResources (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="e9307-143">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="e9307-143">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

