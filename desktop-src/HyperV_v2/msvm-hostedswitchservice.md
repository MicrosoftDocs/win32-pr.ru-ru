---
description: Ассоциация, которая подключает службу виртуального коммутатора к прозрачной службе моста.
ms.assetid: 4DFD73CA-38F0-4C06-BEBE-C684590E50E8
title: Класс Msvm_HostedSwitchService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedSwitchService
- Msvm_HostedSwitchService.Antecedent
- Msvm_HostedSwitchService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f0b7319dbe58649ac7abce2d36201f3984c1b807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662239"
---
# <a name="msvm_hostedswitchservice-class"></a><span data-ttu-id="5caa1-103">\_Класс мсвм хостедсвитчсервице</span><span class="sxs-lookup"><span data-stu-id="5caa1-103">Msvm\_HostedSwitchService class</span></span>

<span data-ttu-id="5caa1-104">Ассоциация, которая подключает службу виртуального коммутатора к прозрачной службе моста.</span><span class="sxs-lookup"><span data-stu-id="5caa1-104">An association that connects a virtual switch service to a transparent bridging service.</span></span>

<span data-ttu-id="5caa1-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="5caa1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5caa1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5caa1-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedSwitchService : CIM_HostedService
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  CIM_Service                REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5caa1-107">Члены</span><span class="sxs-lookup"><span data-stu-id="5caa1-107">Members</span></span>

<span data-ttu-id="5caa1-108">Класс **мсвм \_ хостедсвитчсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5caa1-108">The **Msvm\_HostedSwitchService** class has these types of members:</span></span>

-   [<span data-ttu-id="5caa1-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="5caa1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5caa1-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="5caa1-110">Properties</span></span>

<span data-ttu-id="5caa1-111">Класс **мсвм \_ хостедсвитчсервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5caa1-111">The **Msvm\_HostedSwitchService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5caa1-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="5caa1-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5caa1-113">Тип данных: **[ **мсвм \_ виртуалесернетсвитч**](msvm-virtualethernetswitch.md)**</span><span class="sxs-lookup"><span data-stu-id="5caa1-113">Data type: **[**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span></span>
</dt> <dt>

<span data-ttu-id="5caa1-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5caa1-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5caa1-115">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="5caa1-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="5caa1-116">Ссылка на экземпляр класса [**мсвм \_ виртуалесернетсвитч**](msvm-virtualethernetswitch.md) , представляющий виртуальный коммутатор.</span><span class="sxs-lookup"><span data-stu-id="5caa1-116">A reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="5caa1-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="5caa1-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5caa1-118">Тип данных: **[ **\_ Служба CIM**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="5caa1-118">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="5caa1-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5caa1-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5caa1-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="5caa1-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="5caa1-121">Ссылка на экземпляр класса [**мсвм \_ транспарентбридгингсервице**](msvm-transparentbridgingservice.md) , представляющий службу моста.</span><span class="sxs-lookup"><span data-stu-id="5caa1-121">A reference to an instance of the [**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md) class that represents the bridging service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5caa1-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5caa1-122">Remarks</span></span>

<span data-ttu-id="5caa1-123">Доступ к классу **\_ хостедсвитчсервице мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="5caa1-123">Access to the **Msvm\_HostedSwitchService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5caa1-124">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="5caa1-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="5caa1-125">Требования</span><span class="sxs-lookup"><span data-stu-id="5caa1-125">Requirements</span></span>



| <span data-ttu-id="5caa1-126">Требование</span><span class="sxs-lookup"><span data-stu-id="5caa1-126">Requirement</span></span> | <span data-ttu-id="5caa1-127">Значение</span><span class="sxs-lookup"><span data-stu-id="5caa1-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5caa1-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5caa1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5caa1-129">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5caa1-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5caa1-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5caa1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5caa1-131">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5caa1-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5caa1-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5caa1-132">Namespace</span></span><br/>                | <span data-ttu-id="5caa1-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="5caa1-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5caa1-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5caa1-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5caa1-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5caa1-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5caa1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5caa1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5caa1-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5caa1-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5caa1-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5caa1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5caa1-139">**CIM \_ HostedService**</span><span class="sxs-lookup"><span data-stu-id="5caa1-139">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dt>

[<span data-ttu-id="5caa1-140">**CIM \_ HostedService**</span><span class="sxs-lookup"><span data-stu-id="5caa1-140">**CIM\_HostedService**</span></span>](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> </dl>

 

