---
description: Определяет связь между коммутатором Ethernet и ресурсом коммутатора.
ms.assetid: fb29f4cb-50c4-4865-b267-21ff99bb4a8b
title: Класс Msvm_EthernetSwitchInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchInfo
- Msvm_EthernetSwitchInfo.Antecedent
- Msvm_EthernetSwitchInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1106e0930716572b10a95846865d8f90aa991cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999773"
---
# <a name="msvm_ethernetswitchinfo-class"></a><span data-ttu-id="d49c9-103">\_Класс мсвм есернетсвитчинфо</span><span class="sxs-lookup"><span data-stu-id="d49c9-103">Msvm\_EthernetSwitchInfo class</span></span>

<span data-ttu-id="d49c9-104">Определяет связь между коммутатором Ethernet и ресурсом коммутатора.</span><span class="sxs-lookup"><span data-stu-id="d49c9-104">Defines the association between an Ethernet switch and a switch resource.</span></span>

<span data-ttu-id="d49c9-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d49c9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d49c9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d49c9-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchInfo : CIM_Dependency
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  Msvm_EthernetSwitchData    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d49c9-107">Члены</span><span class="sxs-lookup"><span data-stu-id="d49c9-107">Members</span></span>

<span data-ttu-id="d49c9-108">Класс **мсвм \_ есернетсвитчинфо** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d49c9-108">The **Msvm\_EthernetSwitchInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="d49c9-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="d49c9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d49c9-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d49c9-110">Properties</span></span>

<span data-ttu-id="d49c9-111">Класс **мсвм \_ есернетсвитчинфо** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d49c9-111">The **Msvm\_EthernetSwitchInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d49c9-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="d49c9-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49c9-113">Тип данных: **мсвм \_ виртуалесернетсвитч**</span><span class="sxs-lookup"><span data-stu-id="d49c9-113">Data type: **Msvm\_VirtualEthernetSwitch**</span></span>
</dt> <dt>

<span data-ttu-id="d49c9-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d49c9-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d49c9-115">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="d49c9-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d49c9-116">Ссылка на класс [**мсвм \_ виртуалесернетсвитч**](msvm-virtualethernetswitch.md) , представляющий систему размещения.</span><span class="sxs-lookup"><span data-stu-id="d49c9-116">A reference to the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the hosting system.</span></span> <span data-ttu-id="d49c9-117">Это свойство является производным [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="d49c9-117">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="d49c9-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="d49c9-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49c9-119">Тип данных: **мсвм \_ есернетсвитчдата**</span><span class="sxs-lookup"><span data-stu-id="d49c9-119">Data type: **Msvm\_EthernetSwitchData**</span></span>
</dt> <dt>

<span data-ttu-id="d49c9-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d49c9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d49c9-121">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="d49c9-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d49c9-122">Ссылка на класс [**мсвм \_ есернетсвитчдата**](msvm-ethernetswitchdata.md) , представляющий ресурс коммутатора.</span><span class="sxs-lookup"><span data-stu-id="d49c9-122">A reference to the [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md) class that represents the switch resource.</span></span> <span data-ttu-id="d49c9-123">Это свойство является производным [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="d49c9-123">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d49c9-124">Требования</span><span class="sxs-lookup"><span data-stu-id="d49c9-124">Requirements</span></span>



| <span data-ttu-id="d49c9-125">Требование</span><span class="sxs-lookup"><span data-stu-id="d49c9-125">Requirement</span></span> | <span data-ttu-id="d49c9-126">Значение</span><span class="sxs-lookup"><span data-stu-id="d49c9-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d49c9-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d49c9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d49c9-128">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d49c9-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d49c9-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d49c9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d49c9-130">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d49c9-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d49c9-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d49c9-131">Namespace</span></span><br/>                | <span data-ttu-id="d49c9-132">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d49c9-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d49c9-133">MOF</span><span class="sxs-lookup"><span data-stu-id="d49c9-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d49c9-134"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d49c9-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d49c9-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d49c9-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d49c9-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d49c9-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

