---
description: Установите связь между экземпляром \_ класса мсвм емулатедесернетпортсеттингдата или мсвм \_ синсетицесернетпортсеттингдата с экземпляром \_ класса мсвм GuestNetworkAdapterConfiguration.
ms.assetid: 82262e67-1e72-4bad-974e-f18d00a94c3d
title: Класс Msvm_SettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingDataComponent
- Msvm_SettingDataComponent.GroupComponent
- Msvm_SettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18ed2d4f37b88509a7517861a9b9d842be86bd97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998830"
---
# <a name="msvm_settingdatacomponent-class"></a><span data-ttu-id="dd4a0-103">\_Класс мсвм сеттингдатакомпонент</span><span class="sxs-lookup"><span data-stu-id="dd4a0-103">Msvm\_SettingDataComponent class</span></span>

<span data-ttu-id="dd4a0-104">Установите связь между экземпляром класса [**мсвм \_ Емулатедесернетпортсеттингдата**](msvm-emulatedethernetportsettingdata.md) или [**мсвм \_ Синсетицесернетпортсеттингдата**](msvm-syntheticethernetportsettingdata.md) с экземпляром класса [**мсвм \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="dd4a0-104">Establish a relationship between an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class with an instance of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class.</span></span>

<span data-ttu-id="dd4a0-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="dd4a0-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd4a0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd4a0-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData     REF GroupComponent;
  Msvm_GuestNetworkAdapterConfiguration REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="dd4a0-107">Члены</span><span class="sxs-lookup"><span data-stu-id="dd4a0-107">Members</span></span>

<span data-ttu-id="dd4a0-108">Класс **мсвм \_ сеттингдатакомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dd4a0-108">The **Msvm\_SettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="dd4a0-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="dd4a0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd4a0-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="dd4a0-110">Properties</span></span>

<span data-ttu-id="dd4a0-111">Класс **мсвм \_ сеттингдатакомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dd4a0-111">The **Msvm\_SettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd4a0-112">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="dd4a0-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd4a0-113">Тип данных: **[ **CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="dd4a0-113">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="dd4a0-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd4a0-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd4a0-115">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**агрегатная функция**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dd4a0-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dd4a0-116">Ссылка на экземпляр класса [**мсвм \_ Емулатедесернетпортсеттингдата**](msvm-emulatedethernetportsettingdata.md) или [**мсвм \_ синсетицесернетпортсеттингдата**](msvm-syntheticethernetportsettingdata.md) , представляющий порт Ethernet.</span><span class="sxs-lookup"><span data-stu-id="dd4a0-116">A reference to an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class that represents an Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="dd4a0-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="dd4a0-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd4a0-118">Тип данных: **[ **мсвм \_ гуестнетворкадаптерконфигуратион**](msvm-guestnetworkadapterconfiguration.md)**</span><span class="sxs-lookup"><span data-stu-id="dd4a0-118">Data type: **[**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md)**</span></span>
</dt> <dt>

<span data-ttu-id="dd4a0-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd4a0-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd4a0-120">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="dd4a0-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="dd4a0-121">Ссылка на экземпляр класса [**мсвм \_ гуестнетворкадаптерконфигуратион**](msvm-guestnetworkadapterconfiguration.md) , представляющий конфигурацию гостевого сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="dd4a0-121">A reference to an instance of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class that represents a guest network adapter configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd4a0-122">Требования</span><span class="sxs-lookup"><span data-stu-id="dd4a0-122">Requirements</span></span>



| <span data-ttu-id="dd4a0-123">Требование</span><span class="sxs-lookup"><span data-stu-id="dd4a0-123">Requirement</span></span> | <span data-ttu-id="dd4a0-124">Значение</span><span class="sxs-lookup"><span data-stu-id="dd4a0-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd4a0-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd4a0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dd4a0-126">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dd4a0-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dd4a0-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd4a0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dd4a0-128">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dd4a0-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd4a0-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dd4a0-129">Namespace</span></span><br/>                | <span data-ttu-id="dd4a0-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="dd4a0-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dd4a0-131">MOF</span><span class="sxs-lookup"><span data-stu-id="dd4a0-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd4a0-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd4a0-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd4a0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="dd4a0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd4a0-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dd4a0-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

