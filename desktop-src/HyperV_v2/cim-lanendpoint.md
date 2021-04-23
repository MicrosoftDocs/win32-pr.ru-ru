---
description: Конечная точка связи, которая может подключаться к локальной сети для отправки и получения кадров данных. К конечным точкам локальной сети относятся интерфейсы Ethernet, Token Ring и FDDI.
ms.assetid: c69464cf-00a9-476d-a494-2d7d65776334
title: Класс CIM_LANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LANEndpoint
- CIM_LANEndpoint.LANID
- CIM_LANEndpoint.LANType
- CIM_LANEndpoint.OtherLANType
- CIM_LANEndpoint.MACAddress
- CIM_LANEndpoint.AliasAddresses
- CIM_LANEndpoint.GroupAddresses
- CIM_LANEndpoint.MaxDataSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c924d175cb48e53346daff59a6317a4a0f241f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664778"
---
# <a name="cim_lanendpoint-class"></a><span data-ttu-id="9a74a-104">\_Класс CIM ланендпоинт</span><span class="sxs-lookup"><span data-stu-id="9a74a-104">CIM\_LANEndpoint class</span></span>

<span data-ttu-id="9a74a-105">Конечная точка связи, которая может подключаться к локальной сети для отправки и получения кадров данных.</span><span class="sxs-lookup"><span data-stu-id="9a74a-105">A communication endpoint that can connect to a LAN to send and receive data frames.</span></span> <span data-ttu-id="9a74a-106">К конечным точкам локальной сети относятся интерфейсы Ethernet, Token Ring и FDDI.</span><span class="sxs-lookup"><span data-stu-id="9a74a-106">LAN endpoints include ethernet, token Ring, and FDDI interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a74a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a74a-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_LANEndpoint : CIM_ProtocolEndpoint
{
  string LANID;
  uint16 LANType;
  string OtherLANType;
  string MACAddress;
  string AliasAddresses[];
  string GroupAddresses[];
  uint32 MaxDataSize;
};
```

## <a name="members"></a><span data-ttu-id="9a74a-108">Члены</span><span class="sxs-lookup"><span data-stu-id="9a74a-108">Members</span></span>

<span data-ttu-id="9a74a-109">Класс **CIM \_ ланендпоинт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9a74a-109">The **CIM\_LANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="9a74a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="9a74a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9a74a-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="9a74a-111">Properties</span></span>

<span data-ttu-id="9a74a-112">Класс **CIM \_ ланендпоинт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9a74a-112">The **CIM\_LANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9a74a-113">**алиасаддрессес**</span><span class="sxs-lookup"><span data-stu-id="9a74a-113">**AliasAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a74a-114">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9a74a-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9a74a-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a74a-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a74a-116">Массив, содержащий другие адреса одноадресной рассылки, которые могут использоваться для связи с конечной точкой локальной сети.</span><span class="sxs-lookup"><span data-stu-id="9a74a-116">An array that contains other unicast addresses that may be used to communicate with the LAN endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="9a74a-117">**граупаддрессес**</span><span class="sxs-lookup"><span data-stu-id="9a74a-117">**GroupAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a74a-118">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9a74a-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9a74a-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a74a-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a74a-120">Массив, содержащий адреса многоадресной рассылки, на которые прослушивается конечная точка локальной сети.</span><span class="sxs-lookup"><span data-stu-id="9a74a-120">An array that contains the multicast addresses to which the LAN endpoint listens.</span></span>

</dd> <dt>

<span data-ttu-id="9a74a-121">**ланид**</span><span class="sxs-lookup"><span data-stu-id="9a74a-121">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a74a-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a74a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a74a-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a74a-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a74a-124">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ланконнективитисегмент. ланид, CIM \_ лансегмент. ланид")</span><span class="sxs-lookup"><span data-stu-id="9a74a-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.LANID, CIM\_LANSegment.LANID")</span></span>
</dt> </dl>

<span data-ttu-id="9a74a-125">Метка или идентификатор сегмента локальной сети, к которой подключена конечная точка.</span><span class="sxs-lookup"><span data-stu-id="9a74a-125">A label or identifier for the LAN segment to which the endpoint is connected.</span></span> <span data-ttu-id="9a74a-126">Если конечная точка в настоящее время не подключена или если эта информация неизвестна, **ланид** имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="9a74a-126">If the endpoint is not currently connected or if this information is unknown, then **LANID** is NULL.</span></span>

</dd> <dt>

<span data-ttu-id="9a74a-127">**лантипе**</span><span class="sxs-lookup"><span data-stu-id="9a74a-127">**LANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a74a-128">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9a74a-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9a74a-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a74a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a74a-130">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ протоколендпоинт**](cim-protocolendpoint.md).**ProtocolType**"), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ ЛАНКОННЕКТИВИТИСЕГМЕНТ. ConnectivityType, CIM \_ лансегмент. лантипе ")</span><span class="sxs-lookup"><span data-stu-id="9a74a-130">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md).**ProtocolType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.ConnectivityType, CIM\_LANSegment.LANType")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="9a74a-131">Нерекомендуемое описание: тип технологии, используемой в локальной сети.</span><span class="sxs-lookup"><span data-stu-id="9a74a-131">Deprecated description: The kind of technology used on the LAN.</span></span>

 

<span data-ttu-id="9a74a-132">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="9a74a-132">This property is deprecated.</span></span> <span data-ttu-id="9a74a-133">Вместо этого рекомендуется использовать свойство **ProtocolType** .</span><span class="sxs-lookup"><span data-stu-id="9a74a-133">Instead we recommend that you use the **ProtocolType** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9a74a-134">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9a74a-134">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9a74a-135">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="9a74a-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="9a74a-136">**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="9a74a-136">**Ethernet** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TokenRing"></span><span id="tokenring"></span><span id="TOKENRING"></span>

<span data-ttu-id="9a74a-137">**Токенринг** (3)</span><span class="sxs-lookup"><span data-stu-id="9a74a-137">**TokenRing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="9a74a-138">**FDDI** (4)</span><span class="sxs-lookup"><span data-stu-id="9a74a-138">**FDDI** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9a74a-139">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="9a74a-139">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a74a-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a74a-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a74a-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a74a-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a74a-142">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)</span><span class="sxs-lookup"><span data-stu-id="9a74a-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)</span></span>
</dt> </dl>

<span data-ttu-id="9a74a-143">Основной адрес одноадресной рассылки, используемый конечной точкой локальной сети.</span><span class="sxs-lookup"><span data-stu-id="9a74a-143">The principal unicast address used by the LAN endpoint.</span></span>

<span data-ttu-id="9a74a-144">MAC-адрес должен быть отформатирован со следующими характеристиками:</span><span class="sxs-lookup"><span data-stu-id="9a74a-144">The MAC address must be formatted with the following characteristics:</span></span>

-   <span data-ttu-id="9a74a-145">Адрес состоит из двенадцати шестнадцатеричных цифр.</span><span class="sxs-lookup"><span data-stu-id="9a74a-145">The address consists of twelve hexadecimal digits.</span></span>
-   <span data-ttu-id="9a74a-146">Каждая пара цифр представляет один из шести октетов MAC-адреса.</span><span class="sxs-lookup"><span data-stu-id="9a74a-146">Each pair of digits represents one of the six octets of the MAC address.</span></span>
-   <span data-ttu-id="9a74a-147">Каждая пара цифр должна быть в каноническом порядке в соответствии с RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="9a74a-147">Each pair of digits must be in canonical bit order according to RFC 2469.</span></span>

</dd> <dt>

<span data-ttu-id="9a74a-148">**максдатасизе**</span><span class="sxs-lookup"><span data-stu-id="9a74a-148">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a74a-149">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a74a-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9a74a-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a74a-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a74a-151">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("биты")</span><span class="sxs-lookup"><span data-stu-id="9a74a-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="9a74a-152">Максимальный размер (в байтах) полей данных, отправленных или полученных конечной точкой локальной сети.</span><span class="sxs-lookup"><span data-stu-id="9a74a-152">The maximum size, in bytes, of data fields sent or received by the LAN endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="9a74a-153">**осерлантипе**</span><span class="sxs-lookup"><span data-stu-id="9a74a-153">**OtherLANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a74a-154">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a74a-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a74a-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a74a-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a74a-156">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ протоколендпоинт**](cim-protocolendpoint.md).**Осертипедескриптион**"), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ ланконнективитисегмент. Осертипедескриптион ","**CIM \_ LANEndpoint**.**Лантипе**")</span><span class="sxs-lookup"><span data-stu-id="9a74a-156">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md).**OtherTypeDescription**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.OtherTypeDescription", "**CIM\_LANEndpoint**.**LANType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="9a74a-157">Нерекомендуемое описание: тип технологии, используемой в локальной сети, если свойство **лантипе** имеет значение "1" (другое).</span><span class="sxs-lookup"><span data-stu-id="9a74a-157">Deprecated description: The type of technology used on the LAN when the **LANType** property is set to "1" (Other).</span></span>

 

<span data-ttu-id="9a74a-158">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="9a74a-158">This property is deprecated.</span></span> <span data-ttu-id="9a74a-159">Вместо этого рекомендуется использовать свойство **осертипедескриптион** .</span><span class="sxs-lookup"><span data-stu-id="9a74a-159">Instead we recommend that you use the **OtherTypeDescription** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9a74a-160">Требования</span><span class="sxs-lookup"><span data-stu-id="9a74a-160">Requirements</span></span>



| <span data-ttu-id="9a74a-161">Требование</span><span class="sxs-lookup"><span data-stu-id="9a74a-161">Requirement</span></span> | <span data-ttu-id="9a74a-162">Значение</span><span class="sxs-lookup"><span data-stu-id="9a74a-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a74a-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9a74a-163">Minimum supported client</span></span><br/> | <span data-ttu-id="9a74a-164">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9a74a-164">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="9a74a-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9a74a-165">Minimum supported server</span></span><br/> | <span data-ttu-id="9a74a-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9a74a-166">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="9a74a-167">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9a74a-167">Namespace</span></span><br/>                | <span data-ttu-id="9a74a-168">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9a74a-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9a74a-169">MOF</span><span class="sxs-lookup"><span data-stu-id="9a74a-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a74a-170"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a74a-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a74a-171">DLL</span><span class="sxs-lookup"><span data-stu-id="9a74a-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a74a-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9a74a-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9a74a-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a74a-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a74a-174">**\_ПРОТОКОЛЕНДПОИНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="9a74a-174">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 

