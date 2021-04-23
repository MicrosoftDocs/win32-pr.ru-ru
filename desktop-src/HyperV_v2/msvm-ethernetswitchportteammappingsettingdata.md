---
description: Представляет данные настройки функции сопоставления команды порта.
ms.assetid: 7c9a392d-c95e-4b0d-8201-e50adabd21b2
title: Класс Msvm_EthernetSwitchPortTeamMappingSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortTeamMappingSettingData
- Msvm_EthernetSwitchPortTeamMappingSettingData.NetAdapterName
- Msvm_EthernetSwitchPortTeamMappingSettingData.NetAdapterDeviceId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3f0d7385499dcdf6e84c361de03950a4e78be0a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664763"
---
# <a name="msvm_ethernetswitchportteammappingsettingdata-class"></a><span data-ttu-id="772a4-103">\_Класс мсвм есернетсвитчпорттеаммаппингсеттингдата</span><span class="sxs-lookup"><span data-stu-id="772a4-103">Msvm\_EthernetSwitchPortTeamMappingSettingData class</span></span>

<span data-ttu-id="772a4-104">Представляет данные настройки функции сопоставления команды порта.</span><span class="sxs-lookup"><span data-stu-id="772a4-104">Represents the port team mapping feature setting data.</span></span>

<span data-ttu-id="772a4-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="772a4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="772a4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="772a4-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("8D45D4BD-8C18-435C-98A7-D632A7C618FF"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Team Mapping Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortTeamMappingSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string NetAdapterName = "";
  string NetAdapterDeviceId = "";
};
```

## <a name="members"></a><span data-ttu-id="772a4-107">Члены</span><span class="sxs-lookup"><span data-stu-id="772a4-107">Members</span></span>

<span data-ttu-id="772a4-108">Класс **мсвм \_ есернетсвитчпорттеаммаппингсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="772a4-108">The **Msvm\_EthernetSwitchPortTeamMappingSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="772a4-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="772a4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="772a4-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="772a4-110">Properties</span></span>

<span data-ttu-id="772a4-111">Класс **мсвм \_ есернетсвитчпорттеаммаппингсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="772a4-111">The **Msvm\_EthernetSwitchPortTeamMappingSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="772a4-112">**нетадаптердевицеид**</span><span class="sxs-lookup"><span data-stu-id="772a4-112">**NetAdapterDeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="772a4-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="772a4-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="772a4-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="772a4-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="772a4-115">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **вмидатаид** (2), **Интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="772a4-115">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="772a4-116">ИДЕНТИФИКАТОР устройства предпочтительного сопоставленного физического адаптера.</span><span class="sxs-lookup"><span data-stu-id="772a4-116">Device ID of the preferred mapped physical adapter.</span></span>

</dd> <dt>

<span data-ttu-id="772a4-117">**нетадаптернаме**</span><span class="sxs-lookup"><span data-stu-id="772a4-117">**NetAdapterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="772a4-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="772a4-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="772a4-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="772a4-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="772a4-120">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **вмидатаид** (1), **Интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="772a4-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="772a4-121">Имя предпочитаемого сопоставленного физического адаптера.</span><span class="sxs-lookup"><span data-stu-id="772a4-121">Name of the preferred mapped physical adapter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="772a4-122">Требования</span><span class="sxs-lookup"><span data-stu-id="772a4-122">Requirements</span></span>



| <span data-ttu-id="772a4-123">Требование</span><span class="sxs-lookup"><span data-stu-id="772a4-123">Requirement</span></span> | <span data-ttu-id="772a4-124">Значение</span><span class="sxs-lookup"><span data-stu-id="772a4-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="772a4-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="772a4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="772a4-126">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="772a4-126">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="772a4-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="772a4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="772a4-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="772a4-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="772a4-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="772a4-129">Namespace</span></span><br/>                | <span data-ttu-id="772a4-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="772a4-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="772a4-131">MOF</span><span class="sxs-lookup"><span data-stu-id="772a4-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="772a4-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="772a4-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="772a4-133">DLL</span><span class="sxs-lookup"><span data-stu-id="772a4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="772a4-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="772a4-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="772a4-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="772a4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="772a4-136">**Мсвм \_ есернетсвитчпортфеатуресеттингдата**</span><span class="sxs-lookup"><span data-stu-id="772a4-136">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

