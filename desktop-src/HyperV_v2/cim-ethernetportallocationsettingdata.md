---
description: Представляет параметры для выделения порта Ethernet в дополнение к параметрам, предоставленным \_ классом ЕСЕРНЕТПОРТ CIM. Эти параметры используются для предоставления сведений, относящихся к самому ресурсу.
ms.assetid: f59ebaf1-60dd-49bd-b48e-d7a6c2650909
title: Класс CIM_EthernetPortAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EthernetPortAllocationSettingData
- CIM_EthernetPortAllocationSettingData.DesiredVLANEndpointMode
- CIM_EthernetPortAllocationSettingData.OtherEndpointMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e77b4387f77e88ceaff273b8be72a354c989e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682422"
---
# <a name="cim_ethernetportallocationsettingdata-class"></a><span data-ttu-id="03105-104">\_Класс CIM есернетпорталлокатионсеттингдата</span><span class="sxs-lookup"><span data-stu-id="03105-104">CIM\_EthernetPortAllocationSettingData class</span></span>

<span data-ttu-id="03105-105">Представляет параметры для выделения порта Ethernet в дополнение к параметрам, предоставленным классом [**\_ есернетпорт CIM**](cim-ethernetport.md) .</span><span class="sxs-lookup"><span data-stu-id="03105-105">Represents settings for the allocation of the ethernet port, in addition to the settings provided by the [**CIM\_EthernetPort**](cim-ethernetport.md) class.</span></span> <span data-ttu-id="03105-106">Эти параметры используются для предоставления сведений, относящихся к самому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="03105-106">These settings are used to provide information specific to the resource itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="03105-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03105-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_EthernetPortAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint16 DesiredVLANEndpointMode;
  string OtherEndpointMode;
};
```

## <a name="members"></a><span data-ttu-id="03105-108">Члены</span><span class="sxs-lookup"><span data-stu-id="03105-108">Members</span></span>

<span data-ttu-id="03105-109">Класс **CIM \_ есернетпорталлокатионсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="03105-109">The **CIM\_EthernetPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="03105-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="03105-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03105-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="03105-111">Properties</span></span>

<span data-ttu-id="03105-112">Класс **CIM \_ есернетпорталлокатионсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="03105-112">The **CIM\_EthernetPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03105-113">**десиредвланендпоинтмоде**</span><span class="sxs-lookup"><span data-stu-id="03105-113">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03105-114">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03105-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03105-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03105-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03105-116">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ вланендпоинт**](cim-vlanendpoint.md).**Оператионалендпоинтмоде**","**CIM \_ вланендпоинт**.**Десиредендпоинтмоде**","**CIM \_ есернетпорталлокатионсеттингдата**.**Осерендпоинтмоде**")</span><span class="sxs-lookup"><span data-stu-id="03105-116">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**", "**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_EthernetPortAllocationSettingData**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="03105-117">Запрошенный режим VLAN.</span><span class="sxs-lookup"><span data-stu-id="03105-117">The requested VLAN mode.</span></span> <span data-ttu-id="03105-118">Это свойство используется для задания значения начального свойства **оператионалендпоинтмоде** в экземпляре **CIM \_ вланендпоинт** , связанного с портом Ethernet.</span><span class="sxs-lookup"><span data-stu-id="03105-118">This property is used to set the initial **OperationalEndpointMode** property value in the instance of **CIM\_VLANEndpoint** associated with the ethernet port.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="03105-119">**Зарезервировано DMTF** (0)</span><span class="sxs-lookup"><span data-stu-id="03105-119">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="03105-120">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="03105-120">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="03105-121">**Доступ** (2)</span><span class="sxs-lookup"><span data-stu-id="03105-121">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="03105-122">**Динамическое автоматическое** (3)</span><span class="sxs-lookup"><span data-stu-id="03105-122">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="03105-123">**Желательно динамически** (4)</span><span class="sxs-lookup"><span data-stu-id="03105-123">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="03105-124">**Магистраль** (5)</span><span class="sxs-lookup"><span data-stu-id="03105-124">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="03105-125">**Туннель Dot1Q** (6)</span><span class="sxs-lookup"><span data-stu-id="03105-125">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="03105-126">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="03105-126">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="03105-127">**Поставщик зарезервирован** (0x8000.. 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="03105-127">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03105-128">**осерендпоинтмоде**</span><span class="sxs-lookup"><span data-stu-id="03105-128">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03105-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03105-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03105-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03105-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03105-131">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ есернетпорталлокатионсеттингдата**.**Десиредвланендпоинтмоде**")</span><span class="sxs-lookup"><span data-stu-id="03105-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPortAllocationSettingData**.**DesiredVLANEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="03105-132">Тип модели конечной точки VLAN, поддерживаемой этой конечной точкой VLAN, если для свойства Mode задано значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="03105-132">The type of VLAN endpoint model that is supported by this VLAN endpoint, when the value of the mode property is set to "1" (Other).</span></span> <span data-ttu-id="03105-133">Этому свойству следует присвоить значение **null** , если свойство Mode имеет любое значение, отличное от "1".</span><span class="sxs-lookup"><span data-stu-id="03105-133">This property should be set to **NULL** when the mode property is any value other than "1".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03105-134">Требования</span><span class="sxs-lookup"><span data-stu-id="03105-134">Requirements</span></span>



| <span data-ttu-id="03105-135">Требование</span><span class="sxs-lookup"><span data-stu-id="03105-135">Requirement</span></span> | <span data-ttu-id="03105-136">Значение</span><span class="sxs-lookup"><span data-stu-id="03105-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03105-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="03105-137">Minimum supported client</span></span><br/> | <span data-ttu-id="03105-138">Windows 8</span><span class="sxs-lookup"><span data-stu-id="03105-138">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="03105-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="03105-139">Minimum supported server</span></span><br/> | <span data-ttu-id="03105-140">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="03105-140">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="03105-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="03105-141">Namespace</span></span><br/>                | <span data-ttu-id="03105-142">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="03105-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="03105-143">MOF</span><span class="sxs-lookup"><span data-stu-id="03105-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03105-144"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03105-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="03105-145">DLL</span><span class="sxs-lookup"><span data-stu-id="03105-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03105-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="03105-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="03105-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03105-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03105-148">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="03105-148">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

