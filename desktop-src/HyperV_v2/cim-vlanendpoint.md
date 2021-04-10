---
description: Конечная точка на коммутаторе или конечной станции, назначенная виртуальной ЛС, или принимает трафик от одной или нескольких виртуальных ЛС.
ms.assetid: 20943be3-35c3-4bf5-8f1a-d4095fa6897e
title: Класс CIM_VLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpoint
- CIM_VLANEndpoint.DesiredEndpointMode
- CIM_VLANEndpoint.OtherEndpointMode
- CIM_VLANEndpoint.OperationalEndpointMode
- CIM_VLANEndpoint.DesiredVLANTrunkEncapsulation
- CIM_VLANEndpoint.OtherTrunkEncapsulation
- CIM_VLANEndpoint.OperationalVLANTrunkEncapsulation
- CIM_VLANEndpoint.GVRPStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f7b0d1318e4c24ab7381032877d16a8ea83868b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143462"
---
# <a name="cim_vlanendpoint-class"></a><span data-ttu-id="e6b05-103">\_Класс CIM вланендпоинт</span><span class="sxs-lookup"><span data-stu-id="e6b05-103">CIM\_VLANEndpoint class</span></span>

<span data-ttu-id="e6b05-104">Конечная точка на коммутаторе или конечной станции, назначенная виртуальной ЛС, или принимает трафик от одной или нескольких виртуальных ЛС.</span><span class="sxs-lookup"><span data-stu-id="e6b05-104">An endpoint on a switch or end station that is assigned to a VLAN, or accepts traffic from one or more VLANs.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6b05-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6b05-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Network::VLAN"), AMENDMENT]
class CIM_VLANEndpoint : CIM_ProtocolEndpoint
{
  uint16 DesiredEndpointMode;
  string OtherEndpointMode;
  uint16 OperationalEndpointMode;
  uint16 DesiredVLANTrunkEncapsulation;
  string OtherTrunkEncapsulation;
  uint16 OperationalVLANTrunkEncapsulation;
  uint16 GVRPStatus;
};
```

## <a name="members"></a><span data-ttu-id="e6b05-106">Члены</span><span class="sxs-lookup"><span data-stu-id="e6b05-106">Members</span></span>

<span data-ttu-id="e6b05-107">Класс **CIM \_ вланендпоинт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e6b05-107">The **CIM\_VLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="e6b05-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="e6b05-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e6b05-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="e6b05-109">Properties</span></span>

<span data-ttu-id="e6b05-110">Класс **CIM \_ вланендпоинт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e6b05-110">The **CIM\_VLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e6b05-111">**десиредендпоинтмоде**</span><span class="sxs-lookup"><span data-stu-id="e6b05-111">**DesiredEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6b05-112">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6b05-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6b05-113">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e6b05-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e6b05-114">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ вланендпоинт**.**Оператионалендпоинтмоде**","**CIM \_ вланендпоинт**.**Осерендпоинтмоде**")</span><span class="sxs-lookup"><span data-stu-id="e6b05-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OperationalEndpointMode**", "**CIM\_VLANEndpoint**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="e6b05-115">Запрошенный режим VLAN для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="e6b05-115">The requested VLAN mode for the endpoint.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e6b05-116">**Зарезервировано DMTF** (0)</span><span class="sxs-lookup"><span data-stu-id="e6b05-116">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e6b05-117">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="e6b05-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="e6b05-118">**Доступ** (2)</span><span class="sxs-lookup"><span data-stu-id="e6b05-118">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="e6b05-119">**Динамическое автоматическое** (3)</span><span class="sxs-lookup"><span data-stu-id="e6b05-119">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="e6b05-120">**Желательно динамически** (4)</span><span class="sxs-lookup"><span data-stu-id="e6b05-120">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="e6b05-121">**Магистраль** (5)</span><span class="sxs-lookup"><span data-stu-id="e6b05-121">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="e6b05-122">**Туннель Dot1Q** (6)</span><span class="sxs-lookup"><span data-stu-id="e6b05-122">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e6b05-123">**Зарезервировано DMTF** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e6b05-123">**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e6b05-124">**Зарезервировано поставщиком** (..)</span><span class="sxs-lookup"><span data-stu-id="e6b05-124">**Vendor Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e6b05-125">**десиредвлантрункенкапсулатион**</span><span class="sxs-lookup"><span data-stu-id="e6b05-125">**DesiredVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6b05-126">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6b05-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6b05-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e6b05-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e6b05-128">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ вланендпоинткапабилитиес. суппортстрункенкапсулатионнеготиатион", "**CIM \_ VLANEndpoint**.**Оператионалвлантрункенкапсулатион**","**CIM \_ вланендпоинт**.**Осертрункенкапсулатион**")</span><span class="sxs-lookup"><span data-stu-id="e6b05-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VLANEndpointCapabilities.SupportsTrunkEncapsulationNegotiation", "**CIM\_VLANEndpoint**.**OperationalVLANTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**OtherTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="e6b05-129">Запрошенный тип инкапсуляции виртуальной ЛС.</span><span class="sxs-lookup"><span data-stu-id="e6b05-129">The requested VLAN encapsulation type.</span></span>

> [!Note]  
> <span data-ttu-id="e6b05-130">Это свойство используется только в том случае, если конечная точка VLAN находится в режиме магистрали.</span><span class="sxs-lookup"><span data-stu-id="e6b05-130">This property is only used when the VLAN endpoint is in trunking mode.</span></span>

 

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e6b05-131">**Зарезервировано DMTF** (0)</span><span class="sxs-lookup"><span data-stu-id="e6b05-131">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e6b05-132">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="e6b05-132">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e6b05-133">**Неприменимо** (2)</span><span class="sxs-lookup"><span data-stu-id="e6b05-133">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

<span data-ttu-id="e6b05-134">**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="e6b05-134">**802.1q** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

<span data-ttu-id="e6b05-135">**Cisco острова** (4)</span><span class="sxs-lookup"><span data-stu-id="e6b05-135">**Cisco ISL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="e6b05-136">**Согласование** (5)</span><span class="sxs-lookup"><span data-stu-id="e6b05-136">**Negotiate** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e6b05-137">**Зарезервировано DMTF** (6.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e6b05-137">**DMTF Reserved** (6..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e6b05-138">**Поставщик зарезервирован** (32768...)</span><span class="sxs-lookup"><span data-stu-id="e6b05-138">**Vendor Reserved** (32768..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e6b05-139">**гврпстатус**</span><span class="sxs-lookup"><span data-stu-id="e6b05-139">**GVRPStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6b05-140">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6b05-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6b05-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e6b05-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6b05-142">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ вланендпоинт**.**Оператионалендпоинтмоде**, CIM \_ Вланендпоинткапабилитиес. Dot1QTagging ")</span><span class="sxs-lookup"><span data-stu-id="e6b05-142">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OperationalEndpointMode**, CIM\_VLANEndpointCapabilities.Dot1QTagging")</span></span>
</dt> </dl>

<span data-ttu-id="e6b05-143">Указывает, включен ли протокол регистрации VLAN Гарп (ГВРП) на конечной точке магистрали.</span><span class="sxs-lookup"><span data-stu-id="e6b05-143">Indicates whether GARP VLAN Registration Protocol (GVRP) is enabled or disabled on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="e6b05-144">Это свойство используется, только если ГВРП поддерживается конечной точкой, а режим магистрали включен.</span><span class="sxs-lookup"><span data-stu-id="e6b05-144">This property is only used when GVRP is supported by the endpoint, and trunking mode is enabled.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e6b05-145">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="e6b05-145">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e6b05-146">**Неприменимо** (2)</span><span class="sxs-lookup"><span data-stu-id="e6b05-146">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e6b05-147">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="e6b05-147">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e6b05-148">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="e6b05-148">**Disabled** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e6b05-149">**оператионалендпоинтмоде**</span><span class="sxs-lookup"><span data-stu-id="e6b05-149">**OperationalEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6b05-150">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6b05-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6b05-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e6b05-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6b05-152">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ вланендпоинт**.**Десиредендпоинтмоде**","**CIM \_ вланендпоинт**.**Осерендпоинтмоде**")</span><span class="sxs-lookup"><span data-stu-id="e6b05-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_VLANEndpoint**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="e6b05-153">Текущий режим VLAN для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="e6b05-153">The current VLAN mode for the endpoint.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e6b05-154">**Зарезервировано DMTF** (0)</span><span class="sxs-lookup"><span data-stu-id="e6b05-154">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e6b05-155">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="e6b05-155">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="e6b05-156">**Доступ** (2)</span><span class="sxs-lookup"><span data-stu-id="e6b05-156">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="e6b05-157">**Динамическое автоматическое** (3)</span><span class="sxs-lookup"><span data-stu-id="e6b05-157">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="e6b05-158">**Желательно динамически** (4)</span><span class="sxs-lookup"><span data-stu-id="e6b05-158">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="e6b05-159">**Магистраль** (5)</span><span class="sxs-lookup"><span data-stu-id="e6b05-159">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="e6b05-160">**Туннель Dot1Q** (6)</span><span class="sxs-lookup"><span data-stu-id="e6b05-160">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e6b05-161">**Зарезервировано DMTF** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e6b05-161">**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e6b05-162">**Зарезервировано поставщиком** (..)</span><span class="sxs-lookup"><span data-stu-id="e6b05-162">**Vendor Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e6b05-163">**оператионалвлантрункенкапсулатион**</span><span class="sxs-lookup"><span data-stu-id="e6b05-163">**OperationalVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6b05-164">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6b05-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6b05-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e6b05-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6b05-166">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ вланендпоинт**.**Осертрункенкапсулатион**","**CIM \_ вланендпоинт**.**Десиредвлантрункенкапсулатион**")</span><span class="sxs-lookup"><span data-stu-id="e6b05-166">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OtherTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**DesiredVLANTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="e6b05-167">Текущий тип инкапсуляции виртуальной ЛС.</span><span class="sxs-lookup"><span data-stu-id="e6b05-167">The current VLAN encapsulation type.</span></span>

> [!Note]  
> <span data-ttu-id="e6b05-168">Это свойство используется только в том случае, если конечная точка VLAN находится в режиме магистрали.</span><span class="sxs-lookup"><span data-stu-id="e6b05-168">This property is only used when the VLAN endpoint is in trunking mode.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e6b05-169">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="e6b05-169">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e6b05-170">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="e6b05-170">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e6b05-171">**Неприменимо** (2)</span><span class="sxs-lookup"><span data-stu-id="e6b05-171">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

<span data-ttu-id="e6b05-172">**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="e6b05-172">**802.1q** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

<span data-ttu-id="e6b05-173">**Cisco острова** (4)</span><span class="sxs-lookup"><span data-stu-id="e6b05-173">**Cisco ISL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>

<span data-ttu-id="e6b05-174">**Согласование** (5)</span><span class="sxs-lookup"><span data-stu-id="e6b05-174">**Negotiating** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e6b05-175">**Зарезервировано DMTF** (6.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e6b05-175">**DMTF Reserved** (6..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e6b05-176">**Поставщик зарезервирован** (32768...)</span><span class="sxs-lookup"><span data-stu-id="e6b05-176">**Vendor Reserved** (32768..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e6b05-177">**осерендпоинтмоде**</span><span class="sxs-lookup"><span data-stu-id="e6b05-177">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6b05-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e6b05-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6b05-179">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e6b05-179">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e6b05-180">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ вланендпоинт**.**Десиредендпоинтмоде**","**CIM \_ вланендпоинт**.**Оператионалендпоинтмоде**")</span><span class="sxs-lookup"><span data-stu-id="e6b05-180">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_VLANEndpoint**.**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="e6b05-181">Тип модели конечной точки VLAN, поддерживаемой Вланендпоинт, если значение **десиредендпоинтмоде** равно "1" (другое); в противном случае **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e6b05-181">The type of VLAN endpoint model that is supported by the VLANEndpoint when the value of **DesiredEndpointMode** is set to "1" (other); otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e6b05-182">**осертрункенкапсулатион**</span><span class="sxs-lookup"><span data-stu-id="e6b05-182">**OtherTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6b05-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e6b05-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6b05-184">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e6b05-184">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e6b05-185">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ вланендпоинт**.**Десиредвлантрункенкапсулатион**","**CIM \_ вланендпоинт**.**Оператионалвлантрункенкапсулатион**")</span><span class="sxs-lookup"><span data-stu-id="e6b05-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredVLANTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**OperationalVLANTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="e6b05-186">Тип инкапсуляции виртуальной ЛС, поддерживаемый конечной точкой VLAN, если значение свойства **десиредвлантрункенкапсулатион** равно 1 (другое); в противном случае **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e6b05-186">The type of VLAN encapsulation that is supported by the VLAN endpoint when the value of the **DesiredVLANTrunkEncapsulation** property is set to 1 (other); otherwise, **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6b05-187">Требования</span><span class="sxs-lookup"><span data-stu-id="e6b05-187">Requirements</span></span>



| <span data-ttu-id="e6b05-188">Требование</span><span class="sxs-lookup"><span data-stu-id="e6b05-188">Requirement</span></span> | <span data-ttu-id="e6b05-189">Значение</span><span class="sxs-lookup"><span data-stu-id="e6b05-189">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6b05-190">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6b05-190">Minimum supported client</span></span><br/> | <span data-ttu-id="e6b05-191">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e6b05-191">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e6b05-192">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6b05-192">Minimum supported server</span></span><br/> | <span data-ttu-id="e6b05-193">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e6b05-193">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e6b05-194">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e6b05-194">Namespace</span></span><br/>                | <span data-ttu-id="e6b05-195">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e6b05-195">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e6b05-196">MOF</span><span class="sxs-lookup"><span data-stu-id="e6b05-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6b05-197"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6b05-197"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6b05-198">DLL</span><span class="sxs-lookup"><span data-stu-id="e6b05-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6b05-199"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e6b05-199"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e6b05-200">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6b05-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6b05-201">**\_ПРОТОКОЛЕНДПОИНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="e6b05-201">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 

