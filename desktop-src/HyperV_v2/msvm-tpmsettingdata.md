---
description: Представляет настроенное состояние устройства TPM.
ms.assetid: 948ccb47-3626-48f1-b18f-ef1d05978b21
title: Класс Msvm_TPMSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TPMSettingData
- Msvm_TPMSettingData.Shielded
- Msvm_TPMSettingData.DataProtected
- Msvm_TPMSettingData.EnabledState
- Msvm_TPMSettingData.KeyProtector
- Msvm_TPMSettingData.LastKnownGoodKeyProtector
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8a14f50f01212129ed34cc7e45ee28facbdb991f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543583"
---
# <a name="msvm_tpmsettingdata-class"></a><span data-ttu-id="e057c-103">\_Класс мсвм тпмсеттингдата</span><span class="sxs-lookup"><span data-stu-id="e057c-103">Msvm\_TPMSettingData class</span></span>

<span data-ttu-id="e057c-104">Представляет настроенное состояние устройства TPM.</span><span class="sxs-lookup"><span data-stu-id="e057c-104">Represents the configured state of the TPM device.</span></span>

<span data-ttu-id="e057c-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e057c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e057c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e057c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TPMSettingData : CIM_ResourceAllocationSettingData
{
  boolean Shielded = FALSE;
  boolean DataProtected = FALSE;
  uint16  EnabledState = 3;
  uint8   KeyProtector[];
  uint8   LastKnownGoodKeyProtector[];
};
```

## <a name="members"></a><span data-ttu-id="e057c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="e057c-107">Members</span></span>

<span data-ttu-id="e057c-108">Класс **мсвм \_ тпмсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e057c-108">The **Msvm\_TPMSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e057c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="e057c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e057c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="e057c-110">Properties</span></span>

<span data-ttu-id="e057c-111">Класс **мсвм \_ тпмсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e057c-111">The **Msvm\_TPMSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e057c-112">**Защищаемые**</span><span class="sxs-lookup"><span data-stu-id="e057c-112">**DataProtected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e057c-113">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e057c-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e057c-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e057c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e057c-115">Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e057c-115">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e057c-116">**значение true** , чтобы задать политику для защиты данных виртуальной машины. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="e057c-116">**true** to set a policy to protect a VM's data; otherwise, **false**.</span></span> <span data-ttu-id="e057c-117">Вновь созданный модуль TPM отключен, поэтому начальное состояние защиты данных — **false**.</span><span class="sxs-lookup"><span data-stu-id="e057c-117">A newly created TPM is disabled, so the initial data protection state is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="e057c-118">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e057c-118">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e057c-119">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e057c-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e057c-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e057c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e057c-121">Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e057c-121">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e057c-122">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="e057c-122">The enabled and disabled states of an element.</span></span> <span data-ttu-id="e057c-123">Значение по умолчанию — **disabled**.</span><span class="sxs-lookup"><span data-stu-id="e057c-123">The default value is **Disabled**.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e057c-124">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="e057c-124">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e057c-125">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="e057c-125">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e057c-126">**кэйпротектор**</span><span class="sxs-lookup"><span data-stu-id="e057c-126">**KeyProtector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e057c-127">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e057c-127">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e057c-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e057c-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e057c-129">Квалификаторы: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), **октетстринг**</span><span class="sxs-lookup"><span data-stu-id="e057c-129">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**</span></span>
</dt> </dl>

<span data-ttu-id="e057c-130">Предохранитель ключа от клиента службы защиты узла.</span><span class="sxs-lookup"><span data-stu-id="e057c-130">The key protector from Host Guardian Service client.</span></span>

</dd> <dt>

<span data-ttu-id="e057c-131">**ласткновнгудкэйпротектор**</span><span class="sxs-lookup"><span data-stu-id="e057c-131">**LastKnownGoodKeyProtector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e057c-132">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e057c-132">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e057c-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e057c-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e057c-134">Квалификаторы: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), **октетстринг**</span><span class="sxs-lookup"><span data-stu-id="e057c-134">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**</span></span>
</dt> </dl>

<span data-ttu-id="e057c-135">Последний известный хороший предохранитель ключа успешно зашифровал состояние устройства TPM во время последней загрузки виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e057c-135">The last known good key protector successfully encrypted TPM device state in the last VM boot.</span></span>

<span data-ttu-id="e057c-136">Это свойство доступно только для чтения для клиента WMI и может быть изменено только устройством TPM виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e057c-136">This property is read-only for the WMI client, and can only be modified by the VM TPM device.</span></span>

</dd> <dt>

<span data-ttu-id="e057c-137">**Экранирование**</span><span class="sxs-lookup"><span data-stu-id="e057c-137">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e057c-138">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e057c-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e057c-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e057c-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e057c-140">Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e057c-140">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e057c-141">**значение true** , чтобы определить политику, которая изолирует виртуальную машину. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="e057c-141">**true** to define a policy that shields a virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="e057c-142">Вновь созданный модуль TPM отключен, поэтому начальное состояние экранирования — **false**.</span><span class="sxs-lookup"><span data-stu-id="e057c-142">A newly created TPM is disabled, so the initial shielding state is **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e057c-143">Требования</span><span class="sxs-lookup"><span data-stu-id="e057c-143">Requirements</span></span>



| <span data-ttu-id="e057c-144">Требование</span><span class="sxs-lookup"><span data-stu-id="e057c-144">Requirement</span></span> | <span data-ttu-id="e057c-145">Значение</span><span class="sxs-lookup"><span data-stu-id="e057c-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e057c-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e057c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e057c-147">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e057c-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e057c-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e057c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e057c-149">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e057c-149">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e057c-150">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e057c-150">End of client support</span></span><br/>    | <span data-ttu-id="e057c-151">Windows 10</span><span class="sxs-lookup"><span data-stu-id="e057c-151">Windows 10</span></span><br/>                                                                                   |
| <span data-ttu-id="e057c-152">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="e057c-152">End of server support</span></span><br/>    | <span data-ttu-id="e057c-153">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e057c-153">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e057c-154">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e057c-154">Namespace</span></span><br/>                | <span data-ttu-id="e057c-155">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e057c-155">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e057c-156">MOF</span><span class="sxs-lookup"><span data-stu-id="e057c-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e057c-157"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e057c-157"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e057c-158">DLL</span><span class="sxs-lookup"><span data-stu-id="e057c-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e057c-159"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e057c-159"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e057c-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e057c-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e057c-161">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="e057c-161">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

