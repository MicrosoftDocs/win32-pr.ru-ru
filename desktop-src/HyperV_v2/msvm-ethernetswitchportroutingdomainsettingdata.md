---
description: Представляет данные о параметрах домена маршрутизации.
ms.assetid: 6216cc4e-b2aa-4344-b8fa-489b986c14be
title: Класс Msvm_EthernetSwitchPortRoutingDomainSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRoutingDomainSettingData
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainGuid
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainName
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdList
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdNameList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 40e16a3c952e63ab89c345201742dafe24cdde7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913888"
---
# <a name="msvm_ethernetswitchportroutingdomainsettingdata-class"></a><span data-ttu-id="517d5-103">\_Класс мсвм есернетсвитчпортраутингдомаинсеттингдата</span><span class="sxs-lookup"><span data-stu-id="517d5-103">Msvm\_EthernetSwitchPortRoutingDomainSettingData class</span></span>

<span data-ttu-id="517d5-104">Представляет данные о параметрах домена маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="517d5-104">Represents the routing domain setting data.</span></span>

<span data-ttu-id="517d5-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="517d5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="517d5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="517d5-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("BF874DF0-F729-4312-A0FA-194271B88990"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Routing Domain Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRoutingDomainSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string RoutingDomainGuid = "";
  string RoutingDomainName = "";
  uint32 IsolationIdList[] = {};
  string IsolationIdNameList[] = {};
};
```

## <a name="members"></a><span data-ttu-id="517d5-107">Члены</span><span class="sxs-lookup"><span data-stu-id="517d5-107">Members</span></span>

<span data-ttu-id="517d5-108">Класс **мсвм \_ есернетсвитчпортраутингдомаинсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="517d5-108">The **Msvm\_EthernetSwitchPortRoutingDomainSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="517d5-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="517d5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="517d5-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="517d5-110">Properties</span></span>

<span data-ttu-id="517d5-111">Класс **мсвм \_ есернетсвитчпортраутингдомаинсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="517d5-111">The **Msvm\_EthernetSwitchPortRoutingDomainSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="517d5-112">**исолатионидлист**</span><span class="sxs-lookup"><span data-stu-id="517d5-112">**IsolationIdList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517d5-113">Тип данных: массив **UInt32**</span><span class="sxs-lookup"><span data-stu-id="517d5-113">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="517d5-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="517d5-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="517d5-115">Квалификаторы: **вмидатаид** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Редакция**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="517d5-115">Qualifiers: **WmiDataId** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="517d5-116">Идентификаторы VirtualSubnetId или VLAN для доменов маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="517d5-116">The VirtualSubnetId or VLAN IDs for the routing domains.</span></span>

</dd> <dt>

<span data-ttu-id="517d5-117">**исолатиониднамелист**</span><span class="sxs-lookup"><span data-stu-id="517d5-117">**IsolationIdNameList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517d5-118">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="517d5-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="517d5-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="517d5-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="517d5-120">Квалификаторы: **вмидатаид** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Редакция**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="517d5-120">Qualifiers: **WmiDataId** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="517d5-121">Массив понятных имен VirtualSubnetId или VLAN.</span><span class="sxs-lookup"><span data-stu-id="517d5-121">The VirtualSubnetId or VLAN friendly name array.</span></span>

</dd> <dt>

<span data-ttu-id="517d5-122">**раутингдомаингуид**</span><span class="sxs-lookup"><span data-stu-id="517d5-122">**RoutingDomainGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517d5-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="517d5-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517d5-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="517d5-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="517d5-125">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **вмидатаид** (1), [**версия**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Редакция**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="517d5-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (1), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="517d5-126">GUID домена маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="517d5-126">The routing domain GUID.</span></span>

</dd> <dt>

<span data-ttu-id="517d5-127">**раутингдомаиннаме**</span><span class="sxs-lookup"><span data-stu-id="517d5-127">**RoutingDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="517d5-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="517d5-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="517d5-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="517d5-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="517d5-130">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **вмидатаид** (2), [**версия**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Редакция**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="517d5-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="517d5-131">Понятное имя домена маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="517d5-131">The routing domain friendly name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="517d5-132">Требования</span><span class="sxs-lookup"><span data-stu-id="517d5-132">Requirements</span></span>



| <span data-ttu-id="517d5-133">Требование</span><span class="sxs-lookup"><span data-stu-id="517d5-133">Requirement</span></span> | <span data-ttu-id="517d5-134">Значение</span><span class="sxs-lookup"><span data-stu-id="517d5-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="517d5-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="517d5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="517d5-136">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="517d5-136">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="517d5-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="517d5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="517d5-138">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="517d5-138">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="517d5-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="517d5-139">Namespace</span></span><br/>                | <span data-ttu-id="517d5-140">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="517d5-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="517d5-141">MOF</span><span class="sxs-lookup"><span data-stu-id="517d5-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="517d5-142"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="517d5-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="517d5-143">DLL</span><span class="sxs-lookup"><span data-stu-id="517d5-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="517d5-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="517d5-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="517d5-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="517d5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="517d5-146">**Мсвм \_ есернетсвитчпортфеатуресеттингдата**</span><span class="sxs-lookup"><span data-stu-id="517d5-146">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

