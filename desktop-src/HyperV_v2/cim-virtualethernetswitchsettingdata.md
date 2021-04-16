---
description: Описание параметров данных для виртуального коммутатора Ethernet.
ms.assetid: 462cff06-5ba6-410a-b091-5c6abab13f03
title: Класс CIM_VirtualEthernetSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualEthernetSwitchSettingData
- CIM_VirtualEthernetSwitchSettingData.VLANConnection
- CIM_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- CIM_VirtualEthernetSwitchSettingData.MaxNumMACAddress
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64d7053364aebe1fab5739cd75389b1a9343efe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662805"
---
# <a name="cim_virtualethernetswitchsettingdata-class"></a><span data-ttu-id="9d1c0-103">\_Класс CIM виртуалесернетсвитчсеттингдата</span><span class="sxs-lookup"><span data-stu-id="9d1c0-103">CIM\_VirtualEthernetSwitchSettingData class</span></span>

<span data-ttu-id="9d1c0-104">Описание параметров данных для виртуального коммутатора Ethernet.</span><span class="sxs-lookup"><span data-stu-id="9d1c0-104">Describes settings data for a virtual ethernet switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d1c0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d1c0-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualEthernetSwitchSettingData : CIM_VirtualSystemSettingData
{
  string VLANConnection[];
  string AssociatedResourcePool[];
  uint32 MaxNumMACAddress;
};
```

## <a name="members"></a><span data-ttu-id="9d1c0-106">Члены</span><span class="sxs-lookup"><span data-stu-id="9d1c0-106">Members</span></span>

<span data-ttu-id="9d1c0-107">Класс **CIM \_ виртуалесернетсвитчсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9d1c0-107">The **CIM\_VirtualEthernetSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="9d1c0-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="9d1c0-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d1c0-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="9d1c0-109">Properties</span></span>

<span data-ttu-id="9d1c0-110">Класс **CIM \_ виртуалесернетсвитчсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9d1c0-110">The **CIM\_VirtualEthernetSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d1c0-111">**ассоЦиатедресаурцепул**</span><span class="sxs-lookup"><span data-stu-id="9d1c0-111">**AssociatedResourcePool**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1c0-112">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9d1c0-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9d1c0-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d1c0-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1c0-114">Массив, содержащий пулы ресурсов узла, которые в настоящее время связаны или связываются с коммутатором Ethernet для распределения Ethernet-подключений между коммутатором Ethernet и виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="9d1c0-114">An array that contains the host resource pools that are currently associated, or to associate with the ethernet switch, in order to allocate ethernet connections between the ethernet switch and a virtual machine.</span></span> <span data-ttu-id="9d1c0-115">Каждое значение этого свойства, отличное от NULL, должно соответствовать **\_ коду URI WBEM \_ унтипединстанцепас** , как определено в спецификации DMTF "DSP0207".</span><span class="sxs-lookup"><span data-stu-id="9d1c0-115">Each non-Null value of this property must conform to **WBEM\_URI\_UntypedInstancePath** as defined in the DMTF "DSP0207" specification.</span></span>

</dd> <dt>

<span data-ttu-id="9d1c0-116">**макснуммакаддресс**</span><span class="sxs-lookup"><span data-stu-id="9d1c0-116">**MaxNumMACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1c0-117">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d1c0-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d1c0-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d1c0-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1c0-119">Число уникальных MAC-адресов, которые коммутатор может изучить для обучения MAC-адресов, как определено в стандарте IEEE 802,1.</span><span class="sxs-lookup"><span data-stu-id="9d1c0-119">The number of unique MAC addresses that the switch can learn for MAC address learning, as defined in the IEEE 802.1 standard.</span></span>

</dd> <dt>

<span data-ttu-id="9d1c0-120">**вланконнектион**</span><span class="sxs-lookup"><span data-stu-id="9d1c0-120">**VLANConnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1c0-121">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9d1c0-121">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9d1c0-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d1c0-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1c0-123">Массив, содержащий идентификаторы виртуальных ЛС, к которым может получить доступ коммутатор.</span><span class="sxs-lookup"><span data-stu-id="9d1c0-123">An array that contains the VLAN IDs that the switch can access.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d1c0-124">Требования</span><span class="sxs-lookup"><span data-stu-id="9d1c0-124">Requirements</span></span>



| <span data-ttu-id="9d1c0-125">Требование</span><span class="sxs-lookup"><span data-stu-id="9d1c0-125">Requirement</span></span> | <span data-ttu-id="9d1c0-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9d1c0-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d1c0-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d1c0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9d1c0-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9d1c0-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="9d1c0-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d1c0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9d1c0-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9d1c0-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="9d1c0-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9d1c0-131">Namespace</span></span><br/>                | <span data-ttu-id="9d1c0-132">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9d1c0-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9d1c0-133">MOF</span><span class="sxs-lookup"><span data-stu-id="9d1c0-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d1c0-134"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d1c0-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d1c0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9d1c0-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d1c0-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9d1c0-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9d1c0-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d1c0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d1c0-138">**\_ВИРТУАЛСИСТЕМСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="9d1c0-138">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> </dl>

 

 




