---
description: Добавляет параметры гостевой службы в конфигурацию виртуальной системы.
ms.assetid: 2c8c2f2b-332a-470e-af7f-80c82e3e2caf
title: Метод Аддгуестсервицесеттингс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5bcdfd8c159e92efe633c04e22af5bceb9d003e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540303"
---
# <a name="addguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="059bb-103">Метод Аддгуестсервицесеттингс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="059bb-103">AddGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="059bb-104">Добавляет параметры гостевой службы в конфигурацию виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="059bb-104">Adds guest service settings to a virtual system configuration.</span></span>

<span data-ttu-id="059bb-105">При применении к частям "текущей" конфигурации виртуальной системы в качестве побочного действия гостевые службы активной виртуальной системы могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="059bb-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="059bb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="059bb-106">Syntax</span></span>


```mof
uint32 AddGuestServiceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           GuestServiceSettings[],
  [out] CIM_SettingData              REF ResultingGuestServiceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="059bb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="059bb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="059bb-108">*Аффектедконфигуратион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="059bb-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="059bb-109">Ссылка на [**\_ виртуалсистемсеттингдата CIM**](cim-virtualsystemsettingdata.md) , описывающая затронутую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="059bb-109">Reference to a [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that describes the affected configuration.</span></span>

</dd> <dt>

<span data-ttu-id="059bb-110">*Гуестсервицесеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="059bb-110">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="059bb-111">Массив, содержащий параметры гостевой службы.</span><span class="sxs-lookup"><span data-stu-id="059bb-111">An array containing the guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="059bb-112">*Ресултинггуестсервицесеттингс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="059bb-112">*ResultingGuestServiceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="059bb-113">При успешном выполнении содержит ссылку на [**\_ SettingData CIM**](cim-settingdata.md) , описывающий результирующие параметры гостевой службы.</span><span class="sxs-lookup"><span data-stu-id="059bb-113">On success, contains a reference to a [**CIM\_SettingData**](cim-settingdata.md) that describes the resulting guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="059bb-114">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="059bb-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="059bb-115">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="059bb-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="059bb-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="059bb-116">Return value</span></span>

<span data-ttu-id="059bb-117">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="059bb-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="059bb-118">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="059bb-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="059bb-119">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="059bb-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="059bb-120">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="059bb-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="059bb-121">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="059bb-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="059bb-122">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="059bb-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="059bb-123">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="059bb-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="059bb-124">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="059bb-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="059bb-125">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="059bb-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="059bb-126">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="059bb-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="059bb-127">Требования</span><span class="sxs-lookup"><span data-stu-id="059bb-127">Requirements</span></span>



| <span data-ttu-id="059bb-128">Требование</span><span class="sxs-lookup"><span data-stu-id="059bb-128">Requirement</span></span> | <span data-ttu-id="059bb-129">Значение</span><span class="sxs-lookup"><span data-stu-id="059bb-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="059bb-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="059bb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="059bb-131">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="059bb-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="059bb-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="059bb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="059bb-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="059bb-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="059bb-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="059bb-134">Namespace</span></span><br/>                | <span data-ttu-id="059bb-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="059bb-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="059bb-136">MOF</span><span class="sxs-lookup"><span data-stu-id="059bb-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="059bb-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="059bb-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="059bb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="059bb-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="059bb-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="059bb-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="059bb-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="059bb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="059bb-141">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="059bb-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

