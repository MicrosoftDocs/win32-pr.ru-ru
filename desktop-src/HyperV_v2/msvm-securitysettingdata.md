---
description: Представляет настроенное состояние параметров безопасности для.
ms.assetid: c57ab966-591e-4dd9-87be-0d2b81611d5d
title: Класс Msvm_SecuritySettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecuritySettingData
- Msvm_SecuritySettingData.TpmEnabled
- Msvm_SecuritySettingData.KsdEnabled
- Msvm_SecuritySettingData.ShieldingRequested
- Msvm_SecuritySettingData.DataProtectionRequested
- Msvm_SecuritySettingData.EncryptStateAndVmMigrationTraffic
- Msvm_SecuritySettingData.VirtualizationBasedSecurityOptOut
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7125e06ad4ce33e70a8cf84b24933e7390e7a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683535"
---
# <a name="msvm_securitysettingdata-class"></a><span data-ttu-id="60292-103">\_Класс мсвм секуритисеттингдата</span><span class="sxs-lookup"><span data-stu-id="60292-103">Msvm\_SecuritySettingData class</span></span>

<span data-ttu-id="60292-104">Представляет настроенное состояние параметров безопасности для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="60292-104">Represents the configured state of the security settings for a virtual machine.</span></span>

<span data-ttu-id="60292-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="60292-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="60292-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60292-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecuritySettingData : CIM_SettingData
{
  boolean TpmEnabled;
  boolean KsdEnabled;
  boolean ShieldingRequested;
  boolean DataProtectionRequested;
  boolean EncryptStateAndVmMigrationTraffic;
  boolean VirtualizationBasedSecurityOptOut;
};
```

## <a name="members"></a><span data-ttu-id="60292-107">Члены</span><span class="sxs-lookup"><span data-stu-id="60292-107">Members</span></span>

<span data-ttu-id="60292-108">Класс **мсвм \_ секуритисеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="60292-108">The **Msvm\_SecuritySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="60292-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="60292-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="60292-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="60292-110">Properties</span></span>

<span data-ttu-id="60292-111">Класс **мсвм \_ секуритисеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="60292-111">The **Msvm\_SecuritySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60292-112">**датапротектионрекуестед**</span><span class="sxs-lookup"><span data-stu-id="60292-112">**DataProtectionRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60292-113">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="60292-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60292-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="60292-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60292-115">Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="60292-115">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="60292-116">**значение true** , чтобы запросить защиту данных для виртуальной машины. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="60292-116">**true** to request data protection for a VM; otherwise, **false**.</span></span> <span data-ttu-id="60292-117">Значение по умолчанию — **false.**</span><span class="sxs-lookup"><span data-stu-id="60292-117">The default value is **false.**</span></span>

</dd> <dt>

<span data-ttu-id="60292-118">**енкриптстатеандвммигратионтраффик**</span><span class="sxs-lookup"><span data-stu-id="60292-118">**EncryptStateAndVmMigrationTraffic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60292-119">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="60292-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60292-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="60292-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60292-121">Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="60292-121">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="60292-122">**значение true** , чтобы трафик состояния и переноса виртуальной машины был зашифрован; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="60292-122">**true** to have the state and migration traffic of a VM encrypted; otherwise, **false**.</span></span> <span data-ttu-id="60292-123">Значение по умолчанию для вновь созданной виртуальной машины — **false**.</span><span class="sxs-lookup"><span data-stu-id="60292-123">The default value for a newly-created VM is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="60292-124">**ксденаблед**</span><span class="sxs-lookup"><span data-stu-id="60292-124">**KsdEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60292-125">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="60292-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60292-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="60292-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60292-127">Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="60292-127">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="60292-128">**значение true** , чтобы включить устройство хранилища ключей (КСД) для этой виртуальной машины; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="60292-128">**true** to enable a key storage device (KSD) for this virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="60292-129">Недавно созданная виртуальная машина имеет значение Disable КСД.</span><span class="sxs-lookup"><span data-stu-id="60292-129">A newly-created VM has a disable KSD.</span></span>

</dd> <dt>

<span data-ttu-id="60292-130">**шиелдингрекуестед**</span><span class="sxs-lookup"><span data-stu-id="60292-130">**ShieldingRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60292-131">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="60292-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60292-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="60292-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60292-133">Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="60292-133">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="60292-134">**значение true** , чтобы запросить экранирование для виртуальной машины; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="60292-134">**true** to request shielding for a VM; otherwise, **false**.</span></span> <span data-ttu-id="60292-135">Только что созданная виртуальная машина имеет первоначально запрошенное состояние экранирования **false**.</span><span class="sxs-lookup"><span data-stu-id="60292-135">A newly-created VM has an initial shielding requested state of **false**.</span></span>

</dd> <dt>

<span data-ttu-id="60292-136">**тпменаблед**</span><span class="sxs-lookup"><span data-stu-id="60292-136">**TpmEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60292-137">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="60292-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60292-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="60292-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60292-139">Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="60292-139">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="60292-140">**значение true** , чтобы включить доверенную платформенную НОДУЛЕ (TPM) для этой виртуальной машины; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="60292-140">**true** to enable a trusted platform nodule (TPM) for this virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="60292-141">У созданной виртуальной машины отключен доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="60292-141">A newly-created VM has a disable TPM.</span></span>

</dd> <dt>

<span data-ttu-id="60292-142">**виртуализатионбаседсекуритйоптаут**</span><span class="sxs-lookup"><span data-stu-id="60292-142">**VirtualizationBasedSecurityOptOut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60292-143">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="60292-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60292-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="60292-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60292-145">Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="60292-145">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="60292-146">**значение true** , чтобы не предлагать безопасность на основе ВИРТУАЛИЗАЦИИ виртуальной машины. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="60292-146">**true** to not offer a VM virtualization-based security; otherwise, **false**.</span></span> <span data-ttu-id="60292-147">Значение по умолчанию для нового состояния отказа виртуальной машины — **false**.</span><span class="sxs-lookup"><span data-stu-id="60292-147">The default setting for a newly-crated VM's opt-out state is **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="60292-148">Требования</span><span class="sxs-lookup"><span data-stu-id="60292-148">Requirements</span></span>



| <span data-ttu-id="60292-149">Требование</span><span class="sxs-lookup"><span data-stu-id="60292-149">Requirement</span></span> | <span data-ttu-id="60292-150">Значение</span><span class="sxs-lookup"><span data-stu-id="60292-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60292-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60292-151">Minimum supported client</span></span><br/> | <span data-ttu-id="60292-152">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="60292-152">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="60292-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60292-153">Minimum supported server</span></span><br/> | <span data-ttu-id="60292-154">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="60292-154">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="60292-155">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="60292-155">Namespace</span></span><br/>                | <span data-ttu-id="60292-156">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="60292-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="60292-157">MOF</span><span class="sxs-lookup"><span data-stu-id="60292-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60292-158"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60292-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="60292-159">DLL</span><span class="sxs-lookup"><span data-stu-id="60292-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60292-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="60292-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="60292-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60292-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60292-162">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="60292-162">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

