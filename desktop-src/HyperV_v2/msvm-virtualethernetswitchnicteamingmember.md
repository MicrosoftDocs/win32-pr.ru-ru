---
description: Представляет связь между командой Екстерналесернетпорт и членом Екстерналесернетпорт.
ms.assetid: e21bea94-d6a8-4788-958e-78ce255837aa
title: Класс Msvm_VirtualEthernetSwitchNicTeamingMember
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchNicTeamingMember
- Msvm_VirtualEthernetSwitchNicTeamingMember.Antecedent
- Msvm_VirtualEthernetSwitchNicTeamingMember.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbf83f4605d6ab1b7bc9740b14c493393eb93163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104273120"
---
# <a name="msvm_virtualethernetswitchnicteamingmember-class"></a><span data-ttu-id="ec7fc-103">\_Класс мсвм виртуалесернетсвитчниктеамингмембер</span><span class="sxs-lookup"><span data-stu-id="ec7fc-103">Msvm\_VirtualEthernetSwitchNicTeamingMember class</span></span>

<span data-ttu-id="ec7fc-104">Представляет связь между командой Екстерналесернетпорт и членом Екстерналесернетпорт.</span><span class="sxs-lookup"><span data-stu-id="ec7fc-104">Represents the association between a team ExternalEthernetPort and a member ExternalEthernetPort.</span></span>

<span data-ttu-id="ec7fc-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ec7fc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec7fc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec7fc-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchNicTeamingMember : CIM_Dependency
{
  Msvm_ExternalEthernetPort REF Antecedent;
  Msvm_ExternalEthernetPort REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="ec7fc-107">Члены</span><span class="sxs-lookup"><span data-stu-id="ec7fc-107">Members</span></span>

<span data-ttu-id="ec7fc-108">Класс **мсвм \_ виртуалесернетсвитчниктеамингмембер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ec7fc-108">The **Msvm\_VirtualEthernetSwitchNicTeamingMember** class has these types of members:</span></span>

-   [<span data-ttu-id="ec7fc-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="ec7fc-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ec7fc-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ec7fc-110">Properties</span></span>

<span data-ttu-id="ec7fc-111">Класс **мсвм \_ виртуалесернетсвитчниктеамингмембер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ec7fc-111">The **Msvm\_VirtualEthernetSwitchNicTeamingMember** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ec7fc-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="ec7fc-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec7fc-113">Тип данных: **мсвм \_ екстерналесернетпорт**</span><span class="sxs-lookup"><span data-stu-id="ec7fc-113">Data type: **Msvm\_ExternalEthernetPort**</span></span>
</dt> <dt>

<span data-ttu-id="ec7fc-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ec7fc-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec7fc-115">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="ec7fc-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ec7fc-116">[**Мсвм \_ екстерналесернетпорт**](msvm-externalethernetport.md) , который ссылается на экземпляр внешнего порта Ethernet для команды.</span><span class="sxs-lookup"><span data-stu-id="ec7fc-116">An [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md) that references the team external ethernet port instance.</span></span>

</dd> <dt>

<span data-ttu-id="ec7fc-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="ec7fc-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec7fc-118">Тип данных: **мсвм \_ екстерналесернетпорт**</span><span class="sxs-lookup"><span data-stu-id="ec7fc-118">Data type: **Msvm\_ExternalEthernetPort**</span></span>
</dt> <dt>

<span data-ttu-id="ec7fc-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ec7fc-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec7fc-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="ec7fc-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ec7fc-121">Ссылка на экземпляр [**мсвм \_ екстерналесернетпорт**](msvm-externalethernetport.md) члена.</span><span class="sxs-lookup"><span data-stu-id="ec7fc-121">Reference to the member [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md) instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec7fc-122">Требования</span><span class="sxs-lookup"><span data-stu-id="ec7fc-122">Requirements</span></span>



| <span data-ttu-id="ec7fc-123">Требование</span><span class="sxs-lookup"><span data-stu-id="ec7fc-123">Requirement</span></span> | <span data-ttu-id="ec7fc-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ec7fc-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec7fc-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec7fc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ec7fc-126">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ec7fc-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ec7fc-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec7fc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ec7fc-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ec7fc-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ec7fc-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ec7fc-129">Namespace</span></span><br/>                | <span data-ttu-id="ec7fc-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ec7fc-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ec7fc-131">MOF</span><span class="sxs-lookup"><span data-stu-id="ec7fc-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec7fc-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec7fc-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec7fc-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ec7fc-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec7fc-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ec7fc-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ec7fc-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec7fc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec7fc-136">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="ec7fc-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

