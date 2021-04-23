---
description: Представляет запись в базе данных пересылки, связанную с \_ классом CIM транспарентбридгингсервице.
ms.assetid: 4c3afe7c-f7e5-4a83-8ba1-f0b1909cee52
title: Класс CIM_DynamicForwardingEntry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DynamicForwardingEntry
- CIM_DynamicForwardingEntry.SystemCreationClassName
- CIM_DynamicForwardingEntry.SystemName
- CIM_DynamicForwardingEntry.ServiceCreationClassName
- CIM_DynamicForwardingEntry.ServiceName
- CIM_DynamicForwardingEntry.CreationClassName
- CIM_DynamicForwardingEntry.MACAddress
- CIM_DynamicForwardingEntry.DynamicStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65cf4f1bc5e678089d54dd99a09a6d3b7aeb3dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682941"
---
# <a name="cim_dynamicforwardingentry-class"></a><span data-ttu-id="073d1-103">\_Класс CIM динамикфорвардинжентри</span><span class="sxs-lookup"><span data-stu-id="073d1-103">CIM\_DynamicForwardingEntry class</span></span>

<span data-ttu-id="073d1-104">Представляет запись в базе данных пересылки, связанную с классом [**CIM \_ транспарентбридгингсервице**](cim-transparentbridgingservice.md) .</span><span class="sxs-lookup"><span data-stu-id="073d1-104">Represents an entry in the forwarding database associated with the [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="073d1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="073d1-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_DynamicForwardingEntry : CIM_LogicalElement
{
  string SystemCreationClassName;
  string SystemName;
  string ServiceCreationClassName;
  string ServiceName;
  string CreationClassName;
  string MACAddress;
  uint16 DynamicStatus;
};
```

## <a name="members"></a><span data-ttu-id="073d1-106">Члены</span><span class="sxs-lookup"><span data-stu-id="073d1-106">Members</span></span>

<span data-ttu-id="073d1-107">Класс **CIM \_ динамикфорвардинжентри** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="073d1-107">The **CIM\_DynamicForwardingEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="073d1-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="073d1-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="073d1-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="073d1-109">Properties</span></span>

<span data-ttu-id="073d1-110">Класс **CIM \_ динамикфорвардинжентри** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="073d1-110">The **CIM\_DynamicForwardingEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="073d1-111">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="073d1-111">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d1-112">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="073d1-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="073d1-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="073d1-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d1-114">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="073d1-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="073d1-115">Имя класса или подкласса, используемого для создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="073d1-115">The name of the class or the subclass used to create the instance.</span></span> <span data-ttu-id="073d1-116">При использовании с другими ключевыми свойствами этого класса это свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="073d1-116">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="073d1-117">**динамикстатус**</span><span class="sxs-lookup"><span data-stu-id="073d1-117">**DynamicStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d1-118">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="073d1-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="073d1-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="073d1-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d1-120">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Мост IETF — MIB. dot1dTpFdbStatus ")</span><span class="sxs-lookup"><span data-stu-id="073d1-120">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpFdbStatus")</span></span>
</dt> </dl>

<span data-ttu-id="073d1-121">Состояние записи.</span><span class="sxs-lookup"><span data-stu-id="073d1-121">The status of the entry.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="073d1-122">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="073d1-122">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>

<span data-ttu-id="073d1-123">**Недопустимое** (2)</span><span class="sxs-lookup"><span data-stu-id="073d1-123">**Invalid** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>

<span data-ttu-id="073d1-124">**Узнали** (3)</span><span class="sxs-lookup"><span data-stu-id="073d1-124">**Learned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Self"></span><span id="self"></span><span id="SELF"></span>

<span data-ttu-id="073d1-125">**Self** (4)</span><span class="sxs-lookup"><span data-stu-id="073d1-125">**Self** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>

<span data-ttu-id="073d1-126">Управление **(5** )</span><span class="sxs-lookup"><span data-stu-id="073d1-126">**Mgmt** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="073d1-127">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="073d1-127">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d1-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="073d1-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="073d1-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="073d1-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d1-130">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (12), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Мост IETF — MIB. dot1dTpFdbAddress ")</span><span class="sxs-lookup"><span data-stu-id="073d1-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpFdbAddress")</span></span>
</dt> </dl>

<span data-ttu-id="073d1-131">MAC-адрес одноадресной рассылки, по которому служба моста фильтрует данные.</span><span class="sxs-lookup"><span data-stu-id="073d1-131">The Unicast MAC address for which the bridging service filters information.</span></span> <span data-ttu-id="073d1-132">MAC-адрес имеет формат двенадцати шестнадцатеричных цифр, например 010203040506, с каждой парой, представляющей один из шести октетов MAC-адреса в каноническом порядке в соответствии с RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="073d1-132">The MAC address is formatted as twelve hexadecimal digits, such as 010203040506, with each pair representing one of the six octets of the MAC address in canonical bit order according to RFC 2469.</span></span>

</dd> <dt>

<span data-ttu-id="073d1-133">**сервицекреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="073d1-133">**ServiceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d1-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="073d1-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="073d1-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="073d1-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d1-136">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Служба CIM**](cim-service.md)".**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="073d1-136">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Service**](cim-service.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="073d1-137">Значение **CreationClassName** объекта службы области.</span><span class="sxs-lookup"><span data-stu-id="073d1-137">The **CreationClassName** value of the scoping service object.</span></span>

</dd> <dt>

<span data-ttu-id="073d1-138">**Служба**</span><span class="sxs-lookup"><span data-stu-id="073d1-138">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d1-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="073d1-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="073d1-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="073d1-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d1-141">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Служба CIM**](cim-service.md)".**Name**")</span><span class="sxs-lookup"><span data-stu-id="073d1-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Service**](cim-service.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="073d1-142">Имя службы определения области.</span><span class="sxs-lookup"><span data-stu-id="073d1-142">The name of the scoping service.</span></span>

</dd> <dt>

<span data-ttu-id="073d1-143">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="073d1-143">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d1-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="073d1-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="073d1-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="073d1-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d1-146">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="073d1-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="073d1-147">Значение **CreationClassName** объекта System области.</span><span class="sxs-lookup"><span data-stu-id="073d1-147">The **CreationClassName** value of the scoping system object.</span></span>

</dd> <dt>

<span data-ttu-id="073d1-148">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="073d1-148">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="073d1-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="073d1-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="073d1-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="073d1-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="073d1-151">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="073d1-151">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="073d1-152">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="073d1-152">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="073d1-153">Требования</span><span class="sxs-lookup"><span data-stu-id="073d1-153">Requirements</span></span>



| <span data-ttu-id="073d1-154">Требование</span><span class="sxs-lookup"><span data-stu-id="073d1-154">Requirement</span></span> | <span data-ttu-id="073d1-155">Значение</span><span class="sxs-lookup"><span data-stu-id="073d1-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="073d1-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="073d1-156">Minimum supported client</span></span><br/> | <span data-ttu-id="073d1-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="073d1-157">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="073d1-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="073d1-158">Minimum supported server</span></span><br/> | <span data-ttu-id="073d1-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="073d1-159">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="073d1-160">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="073d1-160">Namespace</span></span><br/>                | <span data-ttu-id="073d1-161">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="073d1-161">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="073d1-162">MOF</span><span class="sxs-lookup"><span data-stu-id="073d1-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="073d1-163"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="073d1-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="073d1-164">DLL</span><span class="sxs-lookup"><span data-stu-id="073d1-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="073d1-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="073d1-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="073d1-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="073d1-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="073d1-167">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="073d1-167">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

