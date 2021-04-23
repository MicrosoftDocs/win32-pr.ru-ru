---
description: Добавляет ресурсы в конфигурацию виртуальной машины.
ms.assetid: e2878b60-dc8c-48fb-b163-29457a96d130
title: Метод Аддресаурцесеттингс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4b35379e0fe3925bbf0f7c4d753f77d1d207199b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909843"
---
# <a name="addresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="ac75d-103">Метод Аддресаурцесеттингс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="ac75d-103">AddResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="ac75d-104">Добавляет ресурсы в конфигурацию виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac75d-104">Adds resources to a virtual machine configuration.</span></span> <span data-ttu-id="ac75d-105">При применении к конфигурации виртуальной машины "State" в качестве побочного действия ресурсы добавляются в активную виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ac75d-105">When applied to a "state" virtual machine configuration, as a side effect, resources are added to the active virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac75d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac75d-106">Syntax</span></span>


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ac75d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac75d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac75d-108">*Аффектедконфигуратион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac75d-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac75d-109">Ссылка на объект [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)) , представляющий затронутую конфигурацию виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac75d-109">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) object that represents the affected virtual machine configuration.</span></span>

</dd> <dt>

<span data-ttu-id="ac75d-110">*Ресаурцесеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac75d-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac75d-111">Массив строк, содержащий один внедренный экземпляр класса [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) , который описывает виртуальные аспекты виртуального ресурса, добавляемого в виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ac75d-111">An array of strings that contain one embedded instance of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class that describes the virtual aspects of a virtual resource to be added to the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="ac75d-112">*Ресултингресаурцесеттингс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ac75d-112">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac75d-113">Массив ссылок на экземпляры класса [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) , представляющий виртуальные аспекты добавленных виртуальных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ac75d-113">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class that represents virtual aspects of the added virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="ac75d-114">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ac75d-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac75d-115">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ac75d-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac75d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac75d-116">Return value</span></span>

<span data-ttu-id="ac75d-117">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ac75d-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ac75d-118">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="ac75d-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ac75d-119">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="ac75d-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ac75d-120">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="ac75d-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ac75d-121">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="ac75d-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ac75d-122">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="ac75d-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ac75d-123">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="ac75d-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ac75d-124">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="ac75d-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ac75d-125">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="ac75d-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="ac75d-126">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="ac75d-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ac75d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="ac75d-127">Requirements</span></span>



| <span data-ttu-id="ac75d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="ac75d-128">Requirement</span></span> | <span data-ttu-id="ac75d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="ac75d-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac75d-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac75d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ac75d-131">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ac75d-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ac75d-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac75d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ac75d-133">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ac75d-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ac75d-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ac75d-134">Namespace</span></span><br/>                | <span data-ttu-id="ac75d-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ac75d-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ac75d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="ac75d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac75d-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac75d-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac75d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ac75d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac75d-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ac75d-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ac75d-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac75d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac75d-141">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="ac75d-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

