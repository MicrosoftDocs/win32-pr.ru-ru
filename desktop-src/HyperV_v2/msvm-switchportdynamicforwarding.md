---
description: Подключает порт коммутатора к динамической записи пересылки (полученный MAC-адрес).
ms.assetid: 70687D56-1282-46C7-AB4E-60E32B9DBA14
title: Класс Msvm_SwitchPortDynamicForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SwitchPortDynamicForwarding
- Msvm_SwitchPortDynamicForwarding.Antecedent
- Msvm_SwitchPortDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e6dda46302e9e8c58710bad1f4221e14e2c3f4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683234"
---
# <a name="msvm_switchportdynamicforwarding-class"></a><span data-ttu-id="c4775-103">\_Класс мсвм свитчпортдинамикфорвардинг</span><span class="sxs-lookup"><span data-stu-id="c4775-103">Msvm\_SwitchPortDynamicForwarding class</span></span>

<span data-ttu-id="c4775-104">Подключает порт коммутатора к динамической записи пересылки (полученный MAC-адрес).</span><span class="sxs-lookup"><span data-stu-id="c4775-104">Connects a switch port to a dynamic forward entry (learned MAC address).</span></span> <span data-ttu-id="c4775-105">Это полезно при поиске всех известных MAC-адресов для указанного порта.</span><span class="sxs-lookup"><span data-stu-id="c4775-105">This is useful in finding all of the learned MAC addresses for a specified port.</span></span>

<span data-ttu-id="c4775-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c4775-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4775-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4775-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SwitchPortDynamicForwarding : CIM_SwitchPortDynamicForwarding
{
  Msvm_EthernetSwitchPort     REF Antecedent;
  Msvm_DynamicForwardingEntry REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c4775-108">Члены</span><span class="sxs-lookup"><span data-stu-id="c4775-108">Members</span></span>

<span data-ttu-id="c4775-109">Класс **мсвм \_ свитчпортдинамикфорвардинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c4775-109">The **Msvm\_SwitchPortDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="c4775-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c4775-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c4775-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="c4775-111">Properties</span></span>

<span data-ttu-id="c4775-112">Класс **мсвм \_ свитчпортдинамикфорвардинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c4775-112">The **Msvm\_SwitchPortDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4775-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="c4775-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4775-114">Тип данных: **[ **мсвм \_ есернетсвитчпорт**](msvm-ethernetswitchport.md)**</span><span class="sxs-lookup"><span data-stu-id="c4775-114">Data type: **[**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c4775-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4775-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4775-116">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="c4775-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c4775-117">Ссылка на экземпляр класса [**мсвм \_ есернетсвитчпорт**](msvm-ethernetswitchport.md) , представляющий порт коммутатора.</span><span class="sxs-lookup"><span data-stu-id="c4775-117">A reference to an instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class that represents the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="c4775-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="c4775-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4775-119">Тип данных: **[ **мсвм \_ динамикфорвардинжентри**](msvm-dynamicforwardingentry.md)**</span><span class="sxs-lookup"><span data-stu-id="c4775-119">Data type: **[**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c4775-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4775-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4775-121">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="c4775-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c4775-122">Ссылка на экземпляр класса [**мсвм \_ динамикфорвардинжентри**](msvm-dynamicforwardingentry.md) , представляющий динамическую запись пересылки базы данных пересылки.</span><span class="sxs-lookup"><span data-stu-id="c4775-122">A reference to an instance of the [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) class that represents the dynamic forwarding entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4775-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c4775-123">Remarks</span></span>

<span data-ttu-id="c4775-124">Доступ к классу **\_ свитчпортдинамикфорвардинг мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="c4775-124">Access to the **Msvm\_SwitchPortDynamicForwarding** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c4775-125">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c4775-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="c4775-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="c4775-126">Examples</span></span>

<span data-ttu-id="c4775-127">См. раздел [запросы к сетевым объектам](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c4775-127">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4775-128">Требования</span><span class="sxs-lookup"><span data-stu-id="c4775-128">Requirements</span></span>



| <span data-ttu-id="c4775-129">Требование</span><span class="sxs-lookup"><span data-stu-id="c4775-129">Requirement</span></span> | <span data-ttu-id="c4775-130">Значение</span><span class="sxs-lookup"><span data-stu-id="c4775-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4775-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4775-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c4775-132">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c4775-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c4775-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4775-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c4775-134">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c4775-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c4775-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c4775-135">Namespace</span></span><br/>                | <span data-ttu-id="c4775-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c4775-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c4775-137">MOF</span><span class="sxs-lookup"><span data-stu-id="c4775-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4775-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4775-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4775-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c4775-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4775-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c4775-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c4775-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4775-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4775-142">**\_СВИТЧПОРТДИНАМИКФОРВАРДИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="c4775-142">**CIM\_SwitchPortDynamicForwarding**</span></span>](cim-switchportdynamicforwarding.md)
</dt> <dt>

<span data-ttu-id="c4775-143">[**\_СВИТЧПОРТДИНАМИКФОРВАРДИНГ CIM**](/previous-versions//cc136921(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c4775-143">[**CIM\_SwitchPortDynamicForwarding**](/previous-versions//cc136921(v=vs.85))</span></span>
</dt> </dl>

 

