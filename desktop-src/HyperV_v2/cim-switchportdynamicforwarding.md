---
description: Представляет ассоциацию, в которой запись пересылаемой базы данных применяется к порту коммутатора.
ms.assetid: e63ac61d-ed0c-49e9-b056-4fcb6d1d5455
title: Класс CIM_SwitchPortDynamicForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchPortDynamicForwarding
- CIM_SwitchPortDynamicForwarding.Antecedent
- CIM_SwitchPortDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0e0d87e2ee5df6a7564d92fd1f8421dfa09abe20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662819"
---
# <a name="cim_switchportdynamicforwarding-class"></a><span data-ttu-id="62b7f-103">\_Класс CIM свитчпортдинамикфорвардинг</span><span class="sxs-lookup"><span data-stu-id="62b7f-103">CIM\_SwitchPortDynamicForwarding class</span></span>

<span data-ttu-id="62b7f-104">Представляет ассоциацию, в которой запись пересылаемой базы данных применяется к порту коммутатора.</span><span class="sxs-lookup"><span data-stu-id="62b7f-104">Represents an association in which an entry of a forwarding database applies to a switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="62b7f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62b7f-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_SwitchPortDynamicForwarding : CIM_Dependency
{
  CIM_SwitchPort             REF Antecedent;
  CIM_DynamicForwardingEntry REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="62b7f-106">Члены</span><span class="sxs-lookup"><span data-stu-id="62b7f-106">Members</span></span>

<span data-ttu-id="62b7f-107">Класс **CIM \_ свитчпортдинамикфорвардинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="62b7f-107">The **CIM\_SwitchPortDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="62b7f-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="62b7f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="62b7f-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="62b7f-109">Properties</span></span>

<span data-ttu-id="62b7f-110">Класс **CIM \_ свитчпортдинамикфорвардинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="62b7f-110">The **CIM\_SwitchPortDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="62b7f-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="62b7f-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62b7f-112">Тип данных: **CIM \_ свитчпорт**</span><span class="sxs-lookup"><span data-stu-id="62b7f-112">Data type: **CIM\_SwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="62b7f-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62b7f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62b7f-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="62b7f-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="62b7f-115">Ссылка [**на \_ свитчпорт CIM**](cim-switchport.md) для порта коммутатора.</span><span class="sxs-lookup"><span data-stu-id="62b7f-115">A [**CIM\_SwitchPort**](cim-switchport.md) reference to the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="62b7f-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="62b7f-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62b7f-117">Тип данных: **CIM \_ динамикфорвардинжентри**</span><span class="sxs-lookup"><span data-stu-id="62b7f-117">Data type: **CIM\_DynamicForwardingEntry**</span></span>
</dt> <dt>

<span data-ttu-id="62b7f-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62b7f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62b7f-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="62b7f-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="62b7f-120">Ссылка [**CIM \_ динамикфорвардинжентри**](cim-dynamicforwardingentry.md) на запись базы данных пересылки.</span><span class="sxs-lookup"><span data-stu-id="62b7f-120">A [**CIM\_DynamicForwardingEntry**](cim-dynamicforwardingentry.md) reference to the entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="62b7f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="62b7f-121">Requirements</span></span>



| <span data-ttu-id="62b7f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="62b7f-122">Requirement</span></span> | <span data-ttu-id="62b7f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="62b7f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62b7f-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62b7f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="62b7f-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="62b7f-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="62b7f-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62b7f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="62b7f-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="62b7f-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="62b7f-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="62b7f-128">Namespace</span></span><br/>                | <span data-ttu-id="62b7f-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="62b7f-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="62b7f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="62b7f-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62b7f-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62b7f-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="62b7f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="62b7f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62b7f-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="62b7f-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="62b7f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62b7f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62b7f-135">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="62b7f-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

