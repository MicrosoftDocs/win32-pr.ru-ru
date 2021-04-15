---
description: Ассоциация, используемая для установления связей между одним экземпляром Мсвм \_ емулатедесернетпортсеттингдата и одним или несколькими экземплярами мсвм \_ есернетсвитчфеатуресеттингдата.
ms.assetid: A2929D81-ED86-4C5A-9280-276204EDE89B
title: Класс Msvm_EthernetPortFailoverSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortFailoverSettingDataComponent
- Msvm_EthernetPortFailoverSettingDataComponent.GroupComponent
- Msvm_EthernetPortFailoverSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 50fff8688beea91495014dd75b1f1c33020869f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545703"
---
# <a name="msvm_ethernetportfailoversettingdatacomponent-class"></a><span data-ttu-id="3ad7e-103">\_Класс мсвм есернетпортфаиловерсеттингдатакомпонент</span><span class="sxs-lookup"><span data-stu-id="3ad7e-103">Msvm\_EthernetPortFailoverSettingDataComponent class</span></span>

<span data-ttu-id="3ad7e-104">Ассоциация, используемая для установления связей между одним экземпляром [**мсвм \_ емулатедесернетпортсеттингдата**](msvm-emulatedethernetportsettingdata.md) и одним или несколькими экземплярами [**мсвм \_ есернетсвитчфеатуресеттингдата**](msvm-ethernetswitchfeaturesettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="3ad7e-104">An association used to establish relationships between one instance of an [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) and one or more instances of an [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="3ad7e-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="3ad7e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ad7e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ad7e-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortFailoverSettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData      REF GroupComponent;
  Msvm_FailoverNetworkAdapterSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="3ad7e-107">Члены</span><span class="sxs-lookup"><span data-stu-id="3ad7e-107">Members</span></span>

<span data-ttu-id="3ad7e-108">Класс **мсвм \_ есернетпортфаиловерсеттингдатакомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3ad7e-108">The **Msvm\_EthernetPortFailoverSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="3ad7e-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="3ad7e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ad7e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="3ad7e-110">Properties</span></span>

<span data-ttu-id="3ad7e-111">Класс **мсвм \_ есернетпортфаиловерсеттингдатакомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3ad7e-111">The **Msvm\_EthernetPortFailoverSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ad7e-112">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="3ad7e-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad7e-113">Тип данных: **[ **CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="3ad7e-113">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="3ad7e-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3ad7e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ad7e-115">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**агрегатная функция**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3ad7e-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3ad7e-116">Ссылка на экземпляр класса [**мсвм \_ Емулатедесернетпортсеттингдата**](msvm-emulatedethernetportsettingdata.md) или [**мсвм \_ синсетицесернетпортсеттингдата**](msvm-syntheticethernetportsettingdata.md) , представляющий порт Ethernet.</span><span class="sxs-lookup"><span data-stu-id="3ad7e-116">A reference to an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class that represents the Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="3ad7e-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="3ad7e-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ad7e-118">Тип данных: **[ **мсвм \_ фаиловернетворкадаптерсеттингдата**](msvm-failovernetworkadaptersettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="3ad7e-118">Data type: **[**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3ad7e-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3ad7e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ad7e-120">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="3ad7e-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="3ad7e-121">Ссылка на экземпляр класса [**мсвм \_ фаиловернетворкадаптерсеттингдата**](msvm-failovernetworkadaptersettingdata.md) , представляющий конфигурацию гостевого сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="3ad7e-121">A reference to an instance of the [**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) class that represents the guest network adapter configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ad7e-122">Требования</span><span class="sxs-lookup"><span data-stu-id="3ad7e-122">Requirements</span></span>



| <span data-ttu-id="3ad7e-123">Требование</span><span class="sxs-lookup"><span data-stu-id="3ad7e-123">Requirement</span></span> | <span data-ttu-id="3ad7e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="3ad7e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ad7e-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ad7e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3ad7e-126">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3ad7e-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3ad7e-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ad7e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3ad7e-128">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3ad7e-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3ad7e-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3ad7e-129">Namespace</span></span><br/>                | <span data-ttu-id="3ad7e-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3ad7e-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3ad7e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3ad7e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ad7e-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ad7e-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ad7e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3ad7e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ad7e-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ad7e-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

