---
description: Изменяет параметры гостевой службы.
ms.assetid: a308aa59-bd43-4dd5-a690-c435102e8043
title: Метод Модифигуестсервицесеттингс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bc0af24346c445022ba3f8725ea6102c61dc9c69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896830"
---
# <a name="modifyguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="de6ce-103">Метод Модифигуестсервицесеттингс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="de6ce-103">ModifyGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="de6ce-104">Изменяет параметры гостевой службы.</span><span class="sxs-lookup"><span data-stu-id="de6ce-104">Modifies guest service settings.</span></span>

<span data-ttu-id="de6ce-105">При применении к частям "текущей" конфигурации виртуальной системы в качестве побочного действия гостевые службы активной виртуальной системы могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="de6ce-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="de6ce-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de6ce-106">Syntax</span></span>


```mof
uint32 ModifyGuestServiceSettings(
  [in]  string              GuestServiceSettings[],
  [out] CIM_SettingData REF ResultingGuestServiceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="de6ce-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="de6ce-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de6ce-108">*Гуестсервицесеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de6ce-108">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de6ce-109">Массив, содержащий новые параметры гостевой службы.</span><span class="sxs-lookup"><span data-stu-id="de6ce-109">An array that contains the new guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="de6ce-110">*Ресултинггуестсервицесеттингс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="de6ce-110">*ResultingGuestServiceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de6ce-111">При успешном выполнении контиаинс массив [**\_ SettingData CIM**](cim-settingdata.md) , ссылающийся на результирующие параметры гостевой службы.</span><span class="sxs-lookup"><span data-stu-id="de6ce-111">On success, contiains an array of [**CIM\_SettingData**](cim-settingdata.md) that reference the resulting guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="de6ce-112">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="de6ce-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de6ce-113">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="de6ce-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de6ce-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de6ce-114">Return value</span></span>

<span data-ttu-id="de6ce-115">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="de6ce-115">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="de6ce-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="de6ce-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="de6ce-117">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="de6ce-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="de6ce-118">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="de6ce-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="de6ce-119">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="de6ce-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="de6ce-120">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="de6ce-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="de6ce-121">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="de6ce-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="de6ce-122">**Несовместимые параметры** (6)</span><span class="sxs-lookup"><span data-stu-id="de6ce-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="de6ce-123">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="de6ce-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="de6ce-124">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="de6ce-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="de6ce-125">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="de6ce-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="de6ce-126">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="de6ce-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="de6ce-127">Требования</span><span class="sxs-lookup"><span data-stu-id="de6ce-127">Requirements</span></span>



| <span data-ttu-id="de6ce-128">Требование</span><span class="sxs-lookup"><span data-stu-id="de6ce-128">Requirement</span></span> | <span data-ttu-id="de6ce-129">Значение</span><span class="sxs-lookup"><span data-stu-id="de6ce-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de6ce-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de6ce-130">Minimum supported client</span></span><br/> | <span data-ttu-id="de6ce-131">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="de6ce-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="de6ce-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de6ce-132">Minimum supported server</span></span><br/> | <span data-ttu-id="de6ce-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="de6ce-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="de6ce-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="de6ce-134">Namespace</span></span><br/>                | <span data-ttu-id="de6ce-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="de6ce-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="de6ce-136">MOF</span><span class="sxs-lookup"><span data-stu-id="de6ce-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de6ce-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de6ce-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="de6ce-138">DLL</span><span class="sxs-lookup"><span data-stu-id="de6ce-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de6ce-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="de6ce-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="de6ce-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de6ce-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de6ce-141">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="de6ce-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

