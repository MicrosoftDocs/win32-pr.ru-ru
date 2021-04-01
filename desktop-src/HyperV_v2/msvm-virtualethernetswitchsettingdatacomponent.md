---
description: Ассоциация, используемая для установления &\# 0034; часть&\# 0034; связи между одним экземпляром мсвм \_ виртуалесернетсвитчсеттингдата и одним или несколькими экземплярами мсвм \_ есернетсвитчфеатуресеттингдата.
ms.assetid: b3adac33-056e-4f39-8022-5d9ef78370e9
title: Класс Msvm_VirtualEthernetSwitchSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingDataComponent
- Msvm_VirtualEthernetSwitchSettingDataComponent.GroupComponent
- Msvm_VirtualEthernetSwitchSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8fa53514c5db3128e13f0504bb883cb802021c20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263847"
---
# <a name="msvm_virtualethernetswitchsettingdatacomponent-class"></a><span data-ttu-id="61c25-103">\_Класс мсвм виртуалесернетсвитчсеттингдатакомпонент</span><span class="sxs-lookup"><span data-stu-id="61c25-103">Msvm\_VirtualEthernetSwitchSettingDataComponent class</span></span>

<span data-ttu-id="61c25-104">Ассоциация, используемая для установления отношений "часть" между одним экземпляром [**мсвм \_ виртуалесернетсвитчсеттингдата**](msvm-virtualethernetswitchsettingdata.md) и одним или несколькими экземплярами [**мсвм \_ есернетсвитчфеатуресеттингдата**](msvm-ethernetswitchfeaturesettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="61c25-104">An association used to establish "part of" relationships between one instance of [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) and one or more instances of [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="61c25-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="61c25-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="61c25-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61c25-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingDataComponent : CIM_Component
{
  Msvm_VirtualEthernetSwitchSettingData REF GroupComponent;
  Msvm_EthernetSwitchFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="61c25-107">Члены</span><span class="sxs-lookup"><span data-stu-id="61c25-107">Members</span></span>

<span data-ttu-id="61c25-108">Класс **мсвм \_ виртуалесернетсвитчсеттингдатакомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="61c25-108">The **Msvm\_VirtualEthernetSwitchSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="61c25-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="61c25-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61c25-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="61c25-110">Properties</span></span>

<span data-ttu-id="61c25-111">Класс **мсвм \_ виртуалесернетсвитчсеттингдатакомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="61c25-111">The **Msvm\_VirtualEthernetSwitchSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61c25-112">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="61c25-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61c25-113">Тип данных: **мсвм \_ виртуалесернетсвитчсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="61c25-113">Data type: **Msvm\_VirtualEthernetSwitchSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="61c25-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61c25-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61c25-115">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**агрегатная функция**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="61c25-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="61c25-116">Ссылка на экземпляр класса [**мсвм \_ виртуалесернетсвитчсеттингдата**](msvm-virtualethernetswitchsettingdata.md) , представляющий порт Ethernet.</span><span class="sxs-lookup"><span data-stu-id="61c25-116">Reference to an instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that represents an Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="61c25-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="61c25-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61c25-118">Тип данных: **мсвм \_ есернетсвитчфеатуресеттингдата**</span><span class="sxs-lookup"><span data-stu-id="61c25-118">Data type: **Msvm\_EthernetSwitchFeatureSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="61c25-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="61c25-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61c25-120">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="61c25-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="61c25-121">Ссылка на экземпляр класса [**мсвм \_ есернетсвитчфеатуресеттингдата**](msvm-ethernetswitchfeaturesettingdata.md) , представляющий параметры, применяемые к коммутатору.</span><span class="sxs-lookup"><span data-stu-id="61c25-121">Reference to an instance of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class that represents the settings applied to the switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61c25-122">Требования</span><span class="sxs-lookup"><span data-stu-id="61c25-122">Requirements</span></span>



| <span data-ttu-id="61c25-123">Требование</span><span class="sxs-lookup"><span data-stu-id="61c25-123">Requirement</span></span> | <span data-ttu-id="61c25-124">Значение</span><span class="sxs-lookup"><span data-stu-id="61c25-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61c25-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61c25-125">Minimum supported client</span></span><br/> | <span data-ttu-id="61c25-126">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="61c25-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="61c25-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61c25-127">Minimum supported server</span></span><br/> | <span data-ttu-id="61c25-128">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="61c25-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="61c25-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="61c25-129">Namespace</span></span><br/>                | <span data-ttu-id="61c25-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="61c25-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="61c25-131">MOF</span><span class="sxs-lookup"><span data-stu-id="61c25-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61c25-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61c25-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61c25-133">DLL</span><span class="sxs-lookup"><span data-stu-id="61c25-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61c25-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61c25-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

