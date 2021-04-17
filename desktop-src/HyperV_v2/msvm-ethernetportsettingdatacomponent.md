---
description: Ассоциация, используемая для установления &\# 0034; часть&\# 0034; связи между одним экземпляром мсвм \_ есернетпорталлокатионсеттингдата и одним или несколькими экземплярами мсвм \_ есернетсвитчфеатуресеттингдата.
ms.assetid: fab15342-a134-4d4a-9668-1272041614b9
title: Класс Msvm_EthernetPortSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortSettingDataComponent
- Msvm_EthernetPortSettingDataComponent.GroupComponent
- Msvm_EthernetPortSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1c00c056bd5095d945af12fde3556d92b9a2d7ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663470"
---
# <a name="msvm_ethernetportsettingdatacomponent-class"></a><span data-ttu-id="b0818-103">\_Класс мсвм есернетпортсеттингдатакомпонент</span><span class="sxs-lookup"><span data-stu-id="b0818-103">Msvm\_EthernetPortSettingDataComponent class</span></span>

<span data-ttu-id="b0818-104">Ассоциация, используемая для установления отношений "часть" между одним экземпляром [**мсвм \_ есернетпорталлокатионсеттингдата**](msvm-ethernetportallocationsettingdata.md) и одним или несколькими экземплярами [**мсвм \_ есернетсвитчфеатуресеттингдата**](msvm-ethernetswitchfeaturesettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="b0818-104">An association used to establish "part of" relationships between one instance of an [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) and one or more instances of an [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="b0818-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="b0818-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0818-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0818-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortSettingDataComponent : CIM_Component
{
  Msvm_EthernetPortAllocationSettingData    REF GroupComponent;
  Msvm_EthernetSwitchPortFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="b0818-107">Члены</span><span class="sxs-lookup"><span data-stu-id="b0818-107">Members</span></span>

<span data-ttu-id="b0818-108">Класс **мсвм \_ есернетпортсеттингдатакомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b0818-108">The **Msvm\_EthernetPortSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="b0818-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="b0818-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b0818-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="b0818-110">Properties</span></span>

<span data-ttu-id="b0818-111">Класс **мсвм \_ есернетпортсеттингдатакомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b0818-111">The **Msvm\_EthernetPortSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b0818-112">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="b0818-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0818-113">Тип данных: **[ **мсвм \_ есернетпорталлокатионсеттингдата**](msvm-ethernetportallocationsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="b0818-113">Data type: **[**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="b0818-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0818-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0818-115">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**агрегатная функция**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b0818-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b0818-116">Ссылка на экземпляр класса [**мсвм \_ есернетпорталлокатионсеттингдата**](msvm-ethernetportallocationsettingdata.md) , представляющий порт Ethernet.</span><span class="sxs-lookup"><span data-stu-id="b0818-116">A reference to an instance of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that represents the Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="b0818-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b0818-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0818-118">Тип данных: **[ **мсвм \_ есернетсвитчпортфеатуресеттингдата**](msvm-ethernetswitchportfeaturesettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="b0818-118">Data type: **[**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="b0818-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0818-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0818-120">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="b0818-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="b0818-121">Ссылка на экземпляр класса [**мсвм \_ есернетсвитчпортфеатуресеттингдата**](msvm-ethernetswitchportfeaturesettingdata.md) , который представляет параметры компонента, применяемые к порту.</span><span class="sxs-lookup"><span data-stu-id="b0818-121">A reference to an instance of the [**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represents the feature settings applied to the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b0818-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b0818-122">Requirements</span></span>



| <span data-ttu-id="b0818-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b0818-123">Requirement</span></span> | <span data-ttu-id="b0818-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b0818-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0818-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0818-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b0818-126">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b0818-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b0818-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0818-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b0818-128">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b0818-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b0818-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b0818-129">Namespace</span></span><br/>                | <span data-ttu-id="b0818-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="b0818-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b0818-131">MOF</span><span class="sxs-lookup"><span data-stu-id="b0818-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0818-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0818-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0818-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b0818-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0818-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b0818-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

