---
description: Удаляет параметры гостевой службы из конфигурации виртуальной системы.
ms.assetid: 33e55d74-adfd-4174-8f05-14e797a33806
title: Метод Ремовегуестсервицесеттингс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0aee1f8f9d729c093bff2a580e054d93fa7fc033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682492"
---
# <a name="removeguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="f1f08-103">Метод Ремовегуестсервицесеттингс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="f1f08-103">RemoveGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="f1f08-104">Удаляет параметры гостевой службы из конфигурации виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="f1f08-104">Removes guest service settings from a virtual system configuration.</span></span>

<span data-ttu-id="f1f08-105">При применении к частям "текущей" конфигурации виртуальной системы в качестве побочного действия гостевые службы активной виртуальной системы могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="f1f08-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1f08-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1f08-106">Syntax</span></span>


```mof
uint32 RemoveGuestServiceSettings(
  [in]  CIM_SettingData REF GuestServiceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f1f08-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1f08-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1f08-108">*Гуестсервицесеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1f08-108">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f08-109">Ссылка на массив SettingData в [**CIM \_**](cim-settingdata.md) , описывающий удаляемый параметр гостевой службы.</span><span class="sxs-lookup"><span data-stu-id="f1f08-109">Reference to an array of [**CIM\_SettingData**](cim-settingdata.md) that describe the guest service setting to remove.</span></span>

</dd> <dt>

<span data-ttu-id="f1f08-110">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f1f08-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f08-111">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f1f08-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1f08-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1f08-112">Return value</span></span>

<span data-ttu-id="f1f08-113">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="f1f08-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="f1f08-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="f1f08-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f1f08-115">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="f1f08-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f1f08-116">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="f1f08-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f1f08-117">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="f1f08-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f1f08-118">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="f1f08-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f1f08-119">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="f1f08-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f1f08-120">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="f1f08-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f1f08-121">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="f1f08-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f1f08-122">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f1f08-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f1f08-123">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="f1f08-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f1f08-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f1f08-124">Requirements</span></span>



| <span data-ttu-id="f1f08-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f1f08-125">Requirement</span></span> | <span data-ttu-id="f1f08-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f1f08-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1f08-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1f08-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f1f08-128">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f1f08-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f1f08-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1f08-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f1f08-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f1f08-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f1f08-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f1f08-131">Namespace</span></span><br/>                | <span data-ttu-id="f1f08-132">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f1f08-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f1f08-133">MOF</span><span class="sxs-lookup"><span data-stu-id="f1f08-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1f08-134"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1f08-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1f08-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f1f08-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1f08-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f1f08-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f1f08-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1f08-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1f08-138">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="f1f08-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

