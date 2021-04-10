---
description: Представляет параметры гостевой службы связи.
ms.assetid: c36d3002-d43e-4284-b765-2795c941f023
title: Класс Msvm_GuestCommunicationServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestCommunicationServiceSettingData
- Msvm_GuestCommunicationServiceSettingData.Name
- Msvm_GuestCommunicationServiceSettingData.EnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c5506689f5b266c428a790774c1fb98a1b0413b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154598"
---
# <a name="msvm_guestcommunicationservicesettingdata-class"></a><span data-ttu-id="d784c-103">\_Класс мсвм гуесткоммуникатионсервицесеттингдата</span><span class="sxs-lookup"><span data-stu-id="d784c-103">Msvm\_GuestCommunicationServiceSettingData class</span></span>

<span data-ttu-id="d784c-104">Представляет параметры гостевой службы связи.</span><span class="sxs-lookup"><span data-stu-id="d784c-104">Represents the settings of the guest communication service.</span></span>

<span data-ttu-id="d784c-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d784c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d784c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d784c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestCommunicationServiceSettingData : CIM_SettingData
{
  string Name;
  uint16 EnabledStatePolicy;
};
```

## <a name="members"></a><span data-ttu-id="d784c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="d784c-107">Members</span></span>

<span data-ttu-id="d784c-108">Класс **мсвм \_ гуесткоммуникатионсервицесеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d784c-108">The **Msvm\_GuestCommunicationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d784c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="d784c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d784c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d784c-110">Properties</span></span>

<span data-ttu-id="d784c-111">Класс **мсвм \_ гуесткоммуникатионсервицесеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d784c-111">The **Msvm\_GuestCommunicationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d784c-112">**енабледстатеполици**</span><span class="sxs-lookup"><span data-stu-id="d784c-112">**EnabledStatePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d784c-113">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d784c-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d784c-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d784c-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d784c-115">Енабледстатеполици — это целочисленное перечисление, которое указывает на включенное, отключенное или по умолчанию состояние **мсвм \_ гуесткоммуникатионсервицесеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="d784c-115">EnabledStatePolicy is an integer enumeration that indicates the enabled, disabled or default state of the **Msvm\_GuestCommunicationServiceSettingData**.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d784c-116"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="d784c-116"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d784c-117">Для службы связи задано состояние Enabled.</span><span class="sxs-lookup"><span data-stu-id="d784c-117">The communication service is set to the enabled state.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d784c-118"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="d784c-118"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d784c-119">Служба связи задается как отключенное состояние.</span><span class="sxs-lookup"><span data-stu-id="d784c-119">The communication service is set to the disabled state.</span></span>

</dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="d784c-120"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Отложено** (8)</span><span class="sxs-lookup"><span data-stu-id="d784c-120"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd>

<span data-ttu-id="d784c-121">Состояние службы связи зависит от **дефаултенабледстатеполици** в **мсвм \_ гуесткоммуникатионсервицесеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="d784c-121">The communication service state depends on **DefaultEnabledStatePolicy** in **Msvm\_GuestCommunicationServiceSettingData**.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d784c-122">**Name**</span><span class="sxs-lookup"><span data-stu-id="d784c-122">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d784c-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d784c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d784c-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d784c-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d784c-125">Идентификатор GUID службы.</span><span class="sxs-lookup"><span data-stu-id="d784c-125">The GUID of the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d784c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="d784c-126">Requirements</span></span>



| <span data-ttu-id="d784c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d784c-127">Requirement</span></span> | <span data-ttu-id="d784c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d784c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d784c-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d784c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d784c-130">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d784c-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d784c-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d784c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d784c-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d784c-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d784c-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d784c-133">Namespace</span></span><br/>                | <span data-ttu-id="d784c-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d784c-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d784c-135">MOF</span><span class="sxs-lookup"><span data-stu-id="d784c-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d784c-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d784c-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d784c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="d784c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d784c-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d784c-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d784c-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d784c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d784c-140">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="d784c-140">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




