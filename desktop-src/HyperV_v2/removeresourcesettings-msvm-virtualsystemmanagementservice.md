---
description: Удаляет параметры виртуального ресурса из конфигурации виртуальной машины.
ms.assetid: 74d9a70a-5258-4e4b-8131-b25513d11a4b
title: Метод Ремовересаурцесеттингс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 20a7c9fb10e4f7a6356e47f8c743266095de2042
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662507"
---
# <a name="removeresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="bae3a-103">Метод Ремовересаурцесеттингс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="bae3a-103">RemoveResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="bae3a-104">Удаляет параметры виртуального ресурса из конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bae3a-104">Removes virtual resource settings from a virtual machine configuration.</span></span> <span data-ttu-id="bae3a-105">При применении к частям текущей конфигурации виртуальной машины активная виртуальная машина может быть удалена.</span><span class="sxs-lookup"><span data-stu-id="bae3a-105">When applied to parts of a current virtual machine configuration, the active virtual machine may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="bae3a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bae3a-106">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bae3a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bae3a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bae3a-108">*Ресаурцесеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bae3a-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bae3a-109">Массив ссылок на экземпляры класса [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) , где каждый экземпляр представляет параметры виртуального ресурса в конфигурации виртуальной машины, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="bae3a-109">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class, where each instance represents the settings of a virtual resource within a virtual machine configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="bae3a-110">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bae3a-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bae3a-111">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bae3a-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bae3a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bae3a-112">Return value</span></span>

<span data-ttu-id="bae3a-113">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="bae3a-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="bae3a-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="bae3a-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bae3a-115">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="bae3a-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bae3a-116">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="bae3a-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bae3a-117">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="bae3a-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bae3a-118">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="bae3a-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bae3a-119">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="bae3a-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bae3a-120">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="bae3a-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bae3a-121">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="bae3a-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bae3a-122">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="bae3a-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="bae3a-123">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="bae3a-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bae3a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="bae3a-124">Requirements</span></span>



| <span data-ttu-id="bae3a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="bae3a-125">Requirement</span></span> | <span data-ttu-id="bae3a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="bae3a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bae3a-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bae3a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bae3a-128">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="bae3a-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bae3a-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bae3a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bae3a-130">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bae3a-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bae3a-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bae3a-131">Namespace</span></span><br/>                | <span data-ttu-id="bae3a-132">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="bae3a-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bae3a-133">MOF</span><span class="sxs-lookup"><span data-stu-id="bae3a-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bae3a-134"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bae3a-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bae3a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="bae3a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bae3a-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bae3a-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bae3a-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bae3a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bae3a-138">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="bae3a-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

