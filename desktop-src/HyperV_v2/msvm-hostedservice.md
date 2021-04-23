---
description: Связывает службу с компьютерной системой, на которой она размещена.
ms.assetid: 888ABA71-6D67-4933-89E6-40F731AA7153
title: Класс Msvm_HostedService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedService
- Msvm_HostedService.Antecedent
- Msvm_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 284254d32e788e374d56b3822f5c00868552e1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682852"
---
# <a name="msvm_hostedservice-class"></a><span data-ttu-id="2894f-103">\_Класс мсвм HostedService</span><span class="sxs-lookup"><span data-stu-id="2894f-103">Msvm\_HostedService class</span></span>

<span data-ttu-id="2894f-104">Связывает службу с компьютерной системой, на которой она размещена.</span><span class="sxs-lookup"><span data-stu-id="2894f-104">Associates a service with its hosting computer system.</span></span> <span data-ttu-id="2894f-105">Экземпляры [**мсвм \_ виртуализатионманажементсервице**](msvm-virtualsystemmanagementservice.md) можно обнаружить с помощью связи с узлом.</span><span class="sxs-lookup"><span data-stu-id="2894f-105">Instances of [**Msvm\_VirtualizationManagementService**](msvm-virtualsystemmanagementservice.md) can be discovered through their association with a host.</span></span>

<span data-ttu-id="2894f-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="2894f-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2894f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2894f-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedService : CIM_HostedService
{
  CIM_ManagedElement REF Antecedent;
  CIM_Service        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2894f-108">Члены</span><span class="sxs-lookup"><span data-stu-id="2894f-108">Members</span></span>

<span data-ttu-id="2894f-109">Класс **мсвм \_ HostedService** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2894f-109">The **Msvm\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="2894f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="2894f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2894f-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="2894f-111">Properties</span></span>

<span data-ttu-id="2894f-112">Класс **мсвм \_ HostedService** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="2894f-112">The **Msvm\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2894f-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="2894f-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2894f-114">Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="2894f-114">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="2894f-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2894f-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2894f-116">Ссылка на систему компьютера размещения.</span><span class="sxs-lookup"><span data-stu-id="2894f-116">A reference to the hosting computer system.</span></span> <span data-ttu-id="2894f-117">Это свойство наследуется от [**CIM \_ HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span><span class="sxs-lookup"><span data-stu-id="2894f-117">This property is inherited from [**CIM\_HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span></span>

</dd> <dt>

<span data-ttu-id="2894f-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="2894f-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2894f-119">Тип данных: **[ **\_ Служба CIM**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="2894f-119">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="2894f-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2894f-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2894f-121">Ссылка на размещенную службу.</span><span class="sxs-lookup"><span data-stu-id="2894f-121">A reference to the service being hosted.</span></span> <span data-ttu-id="2894f-122">Это свойство наследуется от [**CIM \_ HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span><span class="sxs-lookup"><span data-stu-id="2894f-122">This property is inherited from [**CIM\_HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2894f-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2894f-123">Remarks</span></span>

<span data-ttu-id="2894f-124">Доступ к классу **\_ HostedService мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="2894f-124">Access to the **Msvm\_HostedService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2894f-125">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2894f-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="2894f-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="2894f-126">Examples</span></span>

<span data-ttu-id="2894f-127">См. раздел [запросы к сетевым объектам](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2894f-127">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2894f-128">Требования</span><span class="sxs-lookup"><span data-stu-id="2894f-128">Requirements</span></span>



| <span data-ttu-id="2894f-129">Требование</span><span class="sxs-lookup"><span data-stu-id="2894f-129">Requirement</span></span> | <span data-ttu-id="2894f-130">Значение</span><span class="sxs-lookup"><span data-stu-id="2894f-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2894f-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2894f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2894f-132">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2894f-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2894f-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2894f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2894f-134">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2894f-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2894f-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2894f-135">Namespace</span></span><br/>                | <span data-ttu-id="2894f-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="2894f-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2894f-137">MOF</span><span class="sxs-lookup"><span data-stu-id="2894f-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2894f-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2894f-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2894f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2894f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2894f-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2894f-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2894f-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2894f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2894f-142">**CIM \_ HostedService**</span><span class="sxs-lookup"><span data-stu-id="2894f-142">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dt>

[<span data-ttu-id="2894f-143">**CIM \_ HostedService**</span><span class="sxs-lookup"><span data-stu-id="2894f-143">**CIM\_HostedService**</span></span>](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> <dt>

[<span data-ttu-id="2894f-144">Классы управления виртуальной системой</span><span class="sxs-lookup"><span data-stu-id="2894f-144">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

