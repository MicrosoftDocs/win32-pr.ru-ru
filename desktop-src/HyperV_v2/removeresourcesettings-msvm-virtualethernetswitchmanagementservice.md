---
description: Удаляет параметры виртуального ресурса из конфигурации виртуального коммутатора.
ms.assetid: 9992ebcd-8891-42ef-be7e-154f336e37f8
title: Метод Ремовересаурцесеттингс класса Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9e82117b14ab9975b069e5b340ba9ec504ae65ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072823"
---
# <a name="removeresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="f2eab-103">Метод Ремовересаурцесеттингс \_ класса Виртуалесернетсвитчманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="f2eab-103">RemoveResourceSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="f2eab-104">Удаляет параметры виртуального ресурса из конфигурации виртуального коммутатора.</span><span class="sxs-lookup"><span data-stu-id="f2eab-104">Removes virtual resource settings from a virtual switch configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2eab-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2eab-105">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f2eab-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2eab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2eab-107">*Ресаурцесеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2eab-107">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2eab-108">Массив ссылок на экземпляры класса [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) , где каждый экземпляр представляет параметры виртуального ресурса в конфигурации виртуального коммутатора, который необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="f2eab-108">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class, where each instance represents the settings of a virtual resource within a virtual switch configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="f2eab-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f2eab-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2eab-110">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f2eab-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2eab-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2eab-111">Return value</span></span>

<span data-ttu-id="f2eab-112">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f2eab-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f2eab-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="f2eab-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f2eab-114">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="f2eab-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f2eab-115">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="f2eab-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f2eab-116">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="f2eab-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f2eab-117">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="f2eab-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f2eab-118">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="f2eab-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f2eab-119">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="f2eab-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f2eab-120">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="f2eab-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f2eab-121">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f2eab-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f2eab-122">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="f2eab-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f2eab-123">Требования</span><span class="sxs-lookup"><span data-stu-id="f2eab-123">Requirements</span></span>



| <span data-ttu-id="f2eab-124">Требование</span><span class="sxs-lookup"><span data-stu-id="f2eab-124">Requirement</span></span> | <span data-ttu-id="f2eab-125">Значение</span><span class="sxs-lookup"><span data-stu-id="f2eab-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2eab-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2eab-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f2eab-127">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f2eab-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f2eab-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2eab-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f2eab-129">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f2eab-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2eab-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f2eab-130">Namespace</span></span><br/>                | <span data-ttu-id="f2eab-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f2eab-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f2eab-132">MOF</span><span class="sxs-lookup"><span data-stu-id="f2eab-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2eab-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2eab-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2eab-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f2eab-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2eab-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f2eab-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f2eab-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2eab-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2eab-137">**аддресаурцесеттингс**</span><span class="sxs-lookup"><span data-stu-id="f2eab-137">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="f2eab-138">**модифиресаурцесеттингс**</span><span class="sxs-lookup"><span data-stu-id="f2eab-138">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="f2eab-139">**Мсвм \_ виртуалесернетсвитчманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="f2eab-139">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

