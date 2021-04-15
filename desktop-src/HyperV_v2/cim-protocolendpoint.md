---
description: Точка обмена данными, используемая для отправки и получения данных между системами, интерфейсами компьютеров и логическими сетями.
ms.assetid: e23ef66b-0bcb-400e-91ff-d6d687d3f0d2
title: Класс CIM_ProtocolEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolEndpoint
- CIM_ProtocolEndpoint.Description
- CIM_ProtocolEndpoint.OperationalStatus
- CIM_ProtocolEndpoint.EnabledState
- CIM_ProtocolEndpoint.TimeOfLastStateChange
- CIM_ProtocolEndpoint.Name
- CIM_ProtocolEndpoint.NameFormat
- CIM_ProtocolEndpoint.ProtocolType
- CIM_ProtocolEndpoint.ProtocolIFType
- CIM_ProtocolEndpoint.OtherTypeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b3d492c140d443d14583a80985820f55ff9bec8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683431"
---
# <a name="cim_protocolendpoint-class"></a><span data-ttu-id="77819-103">\_Класс CIM протоколендпоинт</span><span class="sxs-lookup"><span data-stu-id="77819-103">CIM\_ProtocolEndpoint class</span></span>

<span data-ttu-id="77819-104">Точка обмена данными, используемая для отправки и получения данных между системами, интерфейсами компьютеров и логическими сетями.</span><span class="sxs-lookup"><span data-stu-id="77819-104">A communication point used to send and receive data between systems, computer interfaces, and logical networks.</span></span>

## <a name="syntax"></a><span data-ttu-id="77819-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77819-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ProtocolEndpoint : CIM_ServiceAccessPoint
{
  string   Description;
  uint16   OperationalStatus[];
  uint16   EnabledState;
  datetime TimeOfLastStateChange;
  string   Name;
  string   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType;
  string   OtherTypeDescription;
};
```

## <a name="members"></a><span data-ttu-id="77819-106">Члены</span><span class="sxs-lookup"><span data-stu-id="77819-106">Members</span></span>

<span data-ttu-id="77819-107">Класс **CIM \_ протоколендпоинт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="77819-107">The **CIM\_ProtocolEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="77819-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="77819-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="77819-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="77819-109">Properties</span></span>

<span data-ttu-id="77819-110">Класс **CIM \_ протоколендпоинт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="77819-110">The **CIM\_ProtocolEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="77819-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="77819-111">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77819-112">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="77819-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77819-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77819-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77819-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| If-MIB. ифдескр ")</span><span class="sxs-lookup"><span data-stu-id="77819-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|IF-MIB.ifDescr")</span></span>
</dt> </dl>

<span data-ttu-id="77819-115">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="77819-115">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="77819-116">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="77819-116">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77819-117">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="77819-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="77819-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77819-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77819-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("EnabledState"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| If-MIB. ифадминстатус ")</span><span class="sxs-lookup"><span data-stu-id="77819-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("EnabledState"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|IF-MIB.ifAdminStatus")</span></span>
</dt> </dl>

<span data-ttu-id="77819-120">Включенное состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="77819-120">The enabled state of an element.</span></span>

</dd> <dt>

<span data-ttu-id="77819-121">**Name**</span><span class="sxs-lookup"><span data-stu-id="77819-121">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77819-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="77819-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77819-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77819-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77819-124">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="77819-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="77819-125">Уникальный идентификатор конечной точки протокола, указывающий управляемые функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="77819-125">A unique identifier of the protocol endpoint that indicates the managed functionality.</span></span> <span data-ttu-id="77819-126">Соглашение об именовании для этого свойства определено в свойстве **намеформат** .</span><span class="sxs-lookup"><span data-stu-id="77819-126">The naming convention for this property is defined in the **NameFormat** property.</span></span>

</dd> <dt>

<span data-ttu-id="77819-127">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="77819-127">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77819-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="77819-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77819-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77819-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77819-130">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="77819-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="77819-131">Соглашение об именовании, используемое свойством **Name** для обеспечения уникальности значений **имен** .</span><span class="sxs-lookup"><span data-stu-id="77819-131">The naming convention used by the **Name** property to ensure that **Name** values are unique.</span></span> <span data-ttu-id="77819-132">Например, можно добавить значение свойства **протоколифтипе** в начало имени, за которым следует символ подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="77819-132">For example, you can append the **ProtocolIFType** property value to the beginning of the name followed by an underscore.</span></span>

</dd> <dt>

<span data-ttu-id="77819-133">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="77819-133">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77819-134">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="77819-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="77819-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77819-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77819-136">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| If-MIB. ифоперстатус ")</span><span class="sxs-lookup"><span data-stu-id="77819-136">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|IF-MIB.ifOperStatus")</span></span>
</dt> </dl>

<span data-ttu-id="77819-137">Массив, содержащий текущее состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="77819-137">An array that contains the current status of the element.</span></span> <span data-ttu-id="77819-138">Первое значение массива **OperationalStatus** должно содержать первичное состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="77819-138">The first value of the **OperationalStatus** array should contain the primary status for the element.</span></span>

</dd> <dt>

<span data-ttu-id="77819-139">**осертипедескриптион**</span><span class="sxs-lookup"><span data-stu-id="77819-139">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77819-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="77819-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77819-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77819-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77819-142">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ протоколендпоинт**.**ProtocolType**","**CIM \_ протоколендпоинт**.**Протоколифтипе**")</span><span class="sxs-lookup"><span data-stu-id="77819-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ProtocolEndpoint**.**ProtocolType**", "**CIM\_ProtocolEndpoint**.**ProtocolIFType**")</span></span>
</dt> </dl>

<span data-ttu-id="77819-143">Описание типа сетевого протокола, используемого, если свойство **протоколифтипе** имеет значение 1 (другое); в противном случае это значение должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="77819-143">A description of a network protocol type that is used when the **ProtocolIFType** property is set to "1" (Other); otherwise, this value should be set to null.</span></span>

</dd> <dt>

<span data-ttu-id="77819-144">**протоколифтипе**</span><span class="sxs-lookup"><span data-stu-id="77819-144">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77819-145">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="77819-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="77819-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77819-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77819-147">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| If-MIB. ифтипе "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ протоколендпоинт**.**Осертипедескриптион**")</span><span class="sxs-lookup"><span data-stu-id="77819-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|IF-MIB.ifType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ProtocolEndpoint**.**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="77819-148">Перечисление, используемое для категоризации и классификации различных экземпляров этого класса.</span><span class="sxs-lookup"><span data-stu-id="77819-148">An enumeration used to categorize and classify different instances of this class.</span></span> <span data-ttu-id="77819-149">Возможные значения для этого свойства синхронизируются с Ифтипе MIB-модулем (основной информацией об управлении), который поддерживается в https://www.iana.org/assignments/ianaiftype-mib .</span><span class="sxs-lookup"><span data-stu-id="77819-149">The possible values for this property are synchronized with the Internet Assigned Numbers Authority (IANA) ifType MIB-module (management information base), which is maintained at https://www.iana.org/assignments/ianaiftype-mib.</span></span> <span data-ttu-id="77819-150">Включаются дополнительные значения, определяемые DMTF.</span><span class="sxs-lookup"><span data-stu-id="77819-150">Additional values defined by the DMTF are included.</span></span>

> [!Note]  
> <span data-ttu-id="77819-151">Если для **протоколифтипе** задано значение 1 (другое), то сведения о типе протокола должны быть предоставлены в свойстве **осертипедескриптион** .</span><span class="sxs-lookup"><span data-stu-id="77819-151">If the **ProtocolIFType** is set to 1 (Other), then the protocol type information should be provided in the **OtherTypeDescription** property.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="77819-152">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="77819-152">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="77819-153">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="77819-153">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>

<span data-ttu-id="77819-154">**Регулярное 1822** (2)</span><span class="sxs-lookup"><span data-stu-id="77819-154">**Regular 1822** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="HDH_1822"></span><span id="hdh_1822"></span>

<span data-ttu-id="77819-155">**Хдх 1822** (3)</span><span class="sxs-lookup"><span data-stu-id="77819-155">**HDH 1822** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DDN_X.25"></span><span id="ddn_x.25"></span>

<span data-ttu-id="77819-156">**ДДН X. 25** (4)</span><span class="sxs-lookup"><span data-stu-id="77819-156">**DDN X.25** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>

<span data-ttu-id="77819-157">**RFC877 X. 25** (5)</span><span class="sxs-lookup"><span data-stu-id="77819-157">**RFC877 X.25** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>

<span data-ttu-id="77819-158">**Ethernet КСМа/CD** (6)</span><span class="sxs-lookup"><span data-stu-id="77819-158">**Ethernet CSMA/CD** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>

<span data-ttu-id="77819-159">**ISO 802,3 КСМа/CD** (7)</span><span class="sxs-lookup"><span data-stu-id="77819-159">**ISO 802.3 CSMA/CD** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>

<span data-ttu-id="77819-160">**Шина маркеров ISO 802,4** (8)</span><span class="sxs-lookup"><span data-stu-id="77819-160">**ISO 802.4 Token Bus** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>

<span data-ttu-id="77819-161">**ISO 802,5 Token Ring** (9)</span><span class="sxs-lookup"><span data-stu-id="77819-161">**ISO 802.5 Token Ring** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>

<span data-ttu-id="77819-162">**Человек ISO 802,6 Man** (10)</span><span class="sxs-lookup"><span data-stu-id="77819-162">**ISO 802.6 MAN** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>

<span data-ttu-id="77819-163">**Старлан** (11)</span><span class="sxs-lookup"><span data-stu-id="77819-163">**StarLAN** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>

<span data-ttu-id="77819-164">**Протеон 10Mbit** (12)</span><span class="sxs-lookup"><span data-stu-id="77819-164">**Proteon 10Mbit** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>

<span data-ttu-id="77819-165">**Протеон 80Mbit** (13)</span><span class="sxs-lookup"><span data-stu-id="77819-165">**Proteon 80Mbit** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>

<span data-ttu-id="77819-166">**Канал** связи (14)</span><span class="sxs-lookup"><span data-stu-id="77819-166">**HyperChannel** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="77819-167">**FDDI** (15)</span><span class="sxs-lookup"><span data-stu-id="77819-167">**FDDI** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="LAP-B"></span><span id="lap-b"></span>

<span data-ttu-id="77819-168">**Подлинный-B** (16)</span><span class="sxs-lookup"><span data-stu-id="77819-168">**LAP-B** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDLC"></span><span id="sdlc"></span>

<span data-ttu-id="77819-169">**SDLC** (17)</span><span class="sxs-lookup"><span data-stu-id="77819-169">**SDLC** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="DS1"></span><span id="ds1"></span>

<span data-ttu-id="77819-170">**DS1** (18)</span><span class="sxs-lookup"><span data-stu-id="77819-170">**DS1** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="E1"></span><span id="e1"></span>

<span data-ttu-id="77819-171">**E1** (19)</span><span class="sxs-lookup"><span data-stu-id="77819-171">**E1** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>

<span data-ttu-id="77819-172">**Базовый ISDN** (20)</span><span class="sxs-lookup"><span data-stu-id="77819-172">**Basic ISDN** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>

<span data-ttu-id="77819-173">**Основной ISDN** (21)</span><span class="sxs-lookup"><span data-stu-id="77819-173">**Primary ISDN** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>

<span data-ttu-id="77819-174">**Собственная последовательное подключение "точка — точка** " (22)</span><span class="sxs-lookup"><span data-stu-id="77819-174">**Proprietary Point-to-Point Serial** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="PPP"></span><span id="ppp"></span>

<span data-ttu-id="77819-175">**PPP** (23)</span><span class="sxs-lookup"><span data-stu-id="77819-175">**PPP** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>

<span data-ttu-id="77819-176">**Замыкание программного обеспечения** (24)</span><span class="sxs-lookup"><span data-stu-id="77819-176">**Software Loopback** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="EON"></span><span id="eon"></span>

<span data-ttu-id="77819-177">**ЕОН** (25)</span><span class="sxs-lookup"><span data-stu-id="77819-177">**EON** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>

<span data-ttu-id="77819-178">**Ethernet 3Mbit** (26)</span><span class="sxs-lookup"><span data-stu-id="77819-178">**Ethernet 3Mbit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="NSIP"></span><span id="nsip"></span>

<span data-ttu-id="77819-179">**НСИП** (27)</span><span class="sxs-lookup"><span data-stu-id="77819-179">**NSIP** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="SLIP"></span><span id="slip"></span>

<span data-ttu-id="77819-180">**SLIP** (28)</span><span class="sxs-lookup"><span data-stu-id="77819-180">**SLIP** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>

<span data-ttu-id="77819-181">**Ultra** (29)</span><span class="sxs-lookup"><span data-stu-id="77819-181">**Ultra** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DS3"></span><span id="ds3"></span>

<span data-ttu-id="77819-182">**DS3** (30)</span><span class="sxs-lookup"><span data-stu-id="77819-182">**DS3** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="SIP"></span><span id="sip"></span>

<span data-ttu-id="77819-183">**SIP** (31)</span><span class="sxs-lookup"><span data-stu-id="77819-183">**SIP** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

<span data-ttu-id="77819-184">**Frame Relay** (32)</span><span class="sxs-lookup"><span data-stu-id="77819-184">**Frame Relay** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232"></span><span id="rs-232"></span>

<span data-ttu-id="77819-185">**RS-232** (33)</span><span class="sxs-lookup"><span data-stu-id="77819-185">**RS-232** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>

<span data-ttu-id="77819-186">**Параллельно** (34)</span><span class="sxs-lookup"><span data-stu-id="77819-186">**Parallel** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>

<span data-ttu-id="77819-187">**АркНет** (35)</span><span class="sxs-lookup"><span data-stu-id="77819-187">**ARCNet** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>

<span data-ttu-id="77819-188">**АркНет Plus** (36)</span><span class="sxs-lookup"><span data-stu-id="77819-188">**ARCNet Plus** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="77819-189">**ATM** (37)</span><span class="sxs-lookup"><span data-stu-id="77819-189">**ATM** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="MIO_X.25"></span><span id="mio_x.25"></span>

<span data-ttu-id="77819-190">**МиО X. 25** (38)</span><span class="sxs-lookup"><span data-stu-id="77819-190">**MIO X.25** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="SONET"></span><span id="sonet"></span>

<span data-ttu-id="77819-191">**Сонет** (39)</span><span class="sxs-lookup"><span data-stu-id="77819-191">**SONET** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="X.25_PLE"></span><span id="x.25_ple"></span>

<span data-ttu-id="77819-192">**X. 25 Борки** (40)</span><span class="sxs-lookup"><span data-stu-id="77819-192">**X.25 PLE** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>

<span data-ttu-id="77819-193">**ISO 802.211 c** (41)</span><span class="sxs-lookup"><span data-stu-id="77819-193">**ISO 802.211c** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

<span data-ttu-id="77819-194">**LocalTalk** (42)</span><span class="sxs-lookup"><span data-stu-id="77819-194">**LocalTalk** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="SMDS_DXI"></span><span id="smds_dxi"></span>

<span data-ttu-id="77819-195">**СМДС дкси** (43)</span><span class="sxs-lookup"><span data-stu-id="77819-195">**SMDS DXI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>

<span data-ttu-id="77819-196">**Служба Frame Relay** (44)</span><span class="sxs-lookup"><span data-stu-id="77819-196">**Frame Relay Service** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="77819-197">**V. 35** (45)</span><span class="sxs-lookup"><span data-stu-id="77819-197">**V.35** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSI"></span><span id="hssi"></span>

<span data-ttu-id="77819-198">**Хсси** (46)</span><span class="sxs-lookup"><span data-stu-id="77819-198">**HSSI** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="77819-199">**Хиппи** (47)</span><span class="sxs-lookup"><span data-stu-id="77819-199">**HIPPI** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>

<span data-ttu-id="77819-200">**Модем** (48)</span><span class="sxs-lookup"><span data-stu-id="77819-200">**Modem** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="AAL5"></span><span id="aal5"></span>

<span data-ttu-id="77819-201">**AAL5** (49)</span><span class="sxs-lookup"><span data-stu-id="77819-201">**AAL5** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>

<span data-ttu-id="77819-202">**Путь Сонет** (50)</span><span class="sxs-lookup"><span data-stu-id="77819-202">**SONET Path** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="SONET_VT"></span><span id="sonet_vt"></span>

<span data-ttu-id="77819-203">**Сонет VT** (51)</span><span class="sxs-lookup"><span data-stu-id="77819-203">**SONET VT** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="SMDS_ICIP"></span><span id="smds_icip"></span>

<span data-ttu-id="77819-204">**СМДС иЦип** (52)</span><span class="sxs-lookup"><span data-stu-id="77819-204">**SMDS ICIP** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>

<span data-ttu-id="77819-205">**Собственная виртуальная/внутренняя** (53)</span><span class="sxs-lookup"><span data-stu-id="77819-205">**Proprietary Virtual/Internal** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>

<span data-ttu-id="77819-206">**Собственный мультиплексор** (54)</span><span class="sxs-lookup"><span data-stu-id="77819-206">**Proprietary Multiplexor** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.12"></span><span id="ieee_802.12"></span>

<span data-ttu-id="77819-207">**IEEE 802,12** (55)</span><span class="sxs-lookup"><span data-stu-id="77819-207">**IEEE 802.12** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>

<span data-ttu-id="77819-208">**Fibre Channel** (56)</span><span class="sxs-lookup"><span data-stu-id="77819-208">**Fibre Channel** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>

<span data-ttu-id="77819-209">**Интерфейс хиппи** (57)</span><span class="sxs-lookup"><span data-stu-id="77819-209">**HIPPI Interface** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>

<span data-ttu-id="77819-210">**Соединение Frame Relay** (58)</span><span class="sxs-lookup"><span data-stu-id="77819-210">**Frame Relay Interconnect** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>

<span data-ttu-id="77819-211">**ATM-Эмуляция LAN для 802,3** (59)</span><span class="sxs-lookup"><span data-stu-id="77819-211">**ATM Emulated LAN for 802.3** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>

<span data-ttu-id="77819-212">**ATM-Эмуляция LAN для 802,5** (60)</span><span class="sxs-lookup"><span data-stu-id="77819-212">**ATM Emulated LAN for 802.5** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>

<span data-ttu-id="77819-213">**ATM-Эмуляция** (61)</span><span class="sxs-lookup"><span data-stu-id="77819-213">**ATM Emulated Circuit** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>

<span data-ttu-id="77819-214">**Fast Ethernet (100BASE)** (62)</span><span class="sxs-lookup"><span data-stu-id="77819-214">**Fast Ethernet (100BaseT)** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="77819-215">**ISDN** (63)</span><span class="sxs-lookup"><span data-stu-id="77819-215">**ISDN** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="V.11"></span><span id="v.11"></span>

<span data-ttu-id="77819-216">**V. 11** (64)</span><span class="sxs-lookup"><span data-stu-id="77819-216">**V.11** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="V.36"></span><span id="v.36"></span>

<span data-ttu-id="77819-217">**V. 36** (65)</span><span class="sxs-lookup"><span data-stu-id="77819-217">**V.36** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>

<span data-ttu-id="77819-218">**G703 в 64 КБ** (66)</span><span class="sxs-lookup"><span data-stu-id="77819-218">**G703 at 64K** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>

<span data-ttu-id="77819-219">**G703 в 2 МБ** (67)</span><span class="sxs-lookup"><span data-stu-id="77819-219">**G703 at 2Mb** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="QLLC"></span><span id="qllc"></span>

<span data-ttu-id="77819-220">**Кллк** (68)</span><span class="sxs-lookup"><span data-stu-id="77819-220">**QLLC** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>

<span data-ttu-id="77819-221">**Fast Ethernet 100BaseFX** (69)</span><span class="sxs-lookup"><span data-stu-id="77819-221">**Fast Ethernet 100BaseFX** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>

<span data-ttu-id="77819-222">**Канал** (70)</span><span class="sxs-lookup"><span data-stu-id="77819-222">**Channel** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.11"></span><span id="ieee_802.11"></span>

<span data-ttu-id="77819-223">**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="77819-223">**IEEE 802.11** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>

<span data-ttu-id="77819-224">**Канал IBM 260/370 оеми** (72)</span><span class="sxs-lookup"><span data-stu-id="77819-224">**IBM 260/370 OEMI Channel** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="77819-225">**Ескон** (73)</span><span class="sxs-lookup"><span data-stu-id="77819-225">**ESCON** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>

<span data-ttu-id="77819-226">**Переключение каналов передачи данных** (74)</span><span class="sxs-lookup"><span data-stu-id="77819-226">**Data Link Switching** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>

<span data-ttu-id="77819-227">**Интерфейс ISDN S/T** (75)</span><span class="sxs-lookup"><span data-stu-id="77819-227">**ISDN S/T Interface** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>

<span data-ttu-id="77819-228">**Интерфейс ISDN U** (76)</span><span class="sxs-lookup"><span data-stu-id="77819-228">**ISDN U Interface** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="LAP-D"></span><span id="lap-d"></span>

<span data-ttu-id="77819-229">**Длинный** (77)</span><span class="sxs-lookup"><span data-stu-id="77819-229">**LAP-D** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>

<span data-ttu-id="77819-230">**IP-параметр** (78)</span><span class="sxs-lookup"><span data-stu-id="77819-230">**IP Switch** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>

<span data-ttu-id="77819-231">**Мост удаленных маршрутов удаленного источника** (79)</span><span class="sxs-lookup"><span data-stu-id="77819-231">**Remote Source Route Bridging** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>

<span data-ttu-id="77819-232">**Логический ATM** (80)</span><span class="sxs-lookup"><span data-stu-id="77819-232">**ATM Logical** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="DS0"></span><span id="ds0"></span>

<span data-ttu-id="77819-233">**DS0** (81)</span><span class="sxs-lookup"><span data-stu-id="77819-233">**DS0** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>

<span data-ttu-id="77819-234">**Пакет DS0** (82)</span><span class="sxs-lookup"><span data-stu-id="77819-234">**DS0 Bundle** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="BSC"></span><span id="bsc"></span>

<span data-ttu-id="77819-235">**BSC** (83)</span><span class="sxs-lookup"><span data-stu-id="77819-235">**BSC** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="Async"></span><span id="async"></span><span id="ASYNC"></span>

<span data-ttu-id="77819-236">**Async** (84)</span><span class="sxs-lookup"><span data-stu-id="77819-236">**Async** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>

<span data-ttu-id="77819-237">**Борьбы с сетевым радио** (85)</span><span class="sxs-lookup"><span data-stu-id="77819-237">**Combat Net Radio** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>

<span data-ttu-id="77819-238">**ISO 802.5 r DTR** (86)</span><span class="sxs-lookup"><span data-stu-id="77819-238">**ISO 802.5r DTR** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>

<span data-ttu-id="77819-239">**Система отчетов ext POS Loc** (87)</span><span class="sxs-lookup"><span data-stu-id="77819-239">**Ext Pos Loc Report System** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>

<span data-ttu-id="77819-240">**Протокол удаленного доступа AppleTalk** (88)</span><span class="sxs-lookup"><span data-stu-id="77819-240">**AppleTalk Remote Access Protocol** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>

<span data-ttu-id="77819-241">**Собственная без подключения** (89)</span><span class="sxs-lookup"><span data-stu-id="77819-241">**Proprietary Connectionless** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>

<span data-ttu-id="77819-242">**Хост-приложение ITU X. 29** (90)</span><span class="sxs-lookup"><span data-stu-id="77819-242">**ITU X.29 Host PAD** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>

<span data-ttu-id="77819-243">**Клавиатура терминала ITU X. 3** (91)</span><span class="sxs-lookup"><span data-stu-id="77819-243">**ITU X.3 Terminal PAD** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>

<span data-ttu-id="77819-244">**MPI Frame Relay** (92)</span><span class="sxs-lookup"><span data-stu-id="77819-244">**Frame Relay MPI** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="ITU_X.213"></span><span id="itu_x.213"></span>

<span data-ttu-id="77819-245">**ITU X. 213** (93)</span><span class="sxs-lookup"><span data-stu-id="77819-245">**ITU X.213** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="ADSL"></span><span id="adsl"></span>

<span data-ttu-id="77819-246">**ADSL** (94)</span><span class="sxs-lookup"><span data-stu-id="77819-246">**ADSL** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="RADSL"></span><span id="radsl"></span>

<span data-ttu-id="77819-247">**Радсл** (95)</span><span class="sxs-lookup"><span data-stu-id="77819-247">**RADSL** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="SDSL"></span><span id="sdsl"></span>

<span data-ttu-id="77819-248">**Сдсл** (96)</span><span class="sxs-lookup"><span data-stu-id="77819-248">**SDSL** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="VDSL"></span><span id="vdsl"></span>

<span data-ttu-id="77819-249">**Вдсл** (97)</span><span class="sxs-lookup"><span data-stu-id="77819-249">**VDSL** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>

<span data-ttu-id="77819-250">**ISO 802,5 крфп** (98)</span><span class="sxs-lookup"><span data-stu-id="77819-250">**ISO 802.5 CRFP** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>

<span data-ttu-id="77819-251">**Миринет** (99)</span><span class="sxs-lookup"><span data-stu-id="77819-251">**Myrinet** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>

<span data-ttu-id="77819-252">**Получение и передача голоса** (100)</span><span class="sxs-lookup"><span data-stu-id="77819-252">**Voice Receive and Transmit** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>

<span data-ttu-id="77819-253">**Голосовое внешнее приложение Exchange** (101)</span><span class="sxs-lookup"><span data-stu-id="77819-253">**Voice Foreign Exchange Office** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>

<span data-ttu-id="77819-254">**Служба Voice иностранных валют** (102)</span><span class="sxs-lookup"><span data-stu-id="77819-254">**Voice Foreign Exchange Service** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>

<span data-ttu-id="77819-255">**Инкапсуляция голоса** (103)</span><span class="sxs-lookup"><span data-stu-id="77819-255">**Voice Encapsulation** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>

<span data-ttu-id="77819-256">Передача **голоса по IP** (104)</span><span class="sxs-lookup"><span data-stu-id="77819-256">**Voice over IP** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_DXI"></span><span id="atm_dxi"></span>

<span data-ttu-id="77819-257">**ATM дкси** (105)</span><span class="sxs-lookup"><span data-stu-id="77819-257">**ATM DXI** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_FUNI"></span><span id="atm_funi"></span>

<span data-ttu-id="77819-258">**ATM Фуни** (106)</span><span class="sxs-lookup"><span data-stu-id="77819-258">**ATM FUNI** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_IMA"></span><span id="atm_ima"></span>

<span data-ttu-id="77819-259">**ATM Има** (107)</span><span class="sxs-lookup"><span data-stu-id="77819-259">**ATM IMA** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>

<span data-ttu-id="77819-260">**Многоканальный пакет PPP** (108)</span><span class="sxs-lookup"><span data-stu-id="77819-260">**PPP Multilink Bundle** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>

<span data-ttu-id="77819-261">**IP через кдлк** (109)</span><span class="sxs-lookup"><span data-stu-id="77819-261">**IP over CDLC** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>

<span data-ttu-id="77819-262">**IP через клав** (110)</span><span class="sxs-lookup"><span data-stu-id="77819-262">**IP over CLAW** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>

<span data-ttu-id="77819-263">**Стек в стек** (111)</span><span class="sxs-lookup"><span data-stu-id="77819-263">**Stack to Stack** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>

<span data-ttu-id="77819-264">**Виртуальный IP-адрес** (112)</span><span class="sxs-lookup"><span data-stu-id="77819-264">**Virtual IP Address** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="MPC"></span><span id="mpc"></span>

<span data-ttu-id="77819-265">**MPC** (113)</span><span class="sxs-lookup"><span data-stu-id="77819-265">**MPC** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>

<span data-ttu-id="77819-266">**IP через ATM** (114)</span><span class="sxs-lookup"><span data-stu-id="77819-266">**IP over ATM** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>

<span data-ttu-id="77819-267">**ISO 802.5 j Fibre Token Ring** (115)</span><span class="sxs-lookup"><span data-stu-id="77819-267">**ISO 802.5j Fibre Token Ring** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="TDLC"></span><span id="tdlc"></span>

<span data-ttu-id="77819-268">**Тдлк** (116)</span><span class="sxs-lookup"><span data-stu-id="77819-268">**TDLC** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>

<span data-ttu-id="77819-269">**Гигабитный Ethernet** (117)</span><span class="sxs-lookup"><span data-stu-id="77819-269">**Gigabit Ethernet** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="HDLC"></span><span id="hdlc"></span>

<span data-ttu-id="77819-270">**Хдлк** (118)</span><span class="sxs-lookup"><span data-stu-id="77819-270">**HDLC** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="LAP-F"></span><span id="lap-f"></span>

<span data-ttu-id="77819-271">**Подлинный-F** (119)</span><span class="sxs-lookup"><span data-stu-id="77819-271">**LAP-F** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="V.37"></span><span id="v.37"></span>

<span data-ttu-id="77819-272">**V. 37** (120)</span><span class="sxs-lookup"><span data-stu-id="77819-272">**V.37** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="X.25_MLP"></span><span id="x.25_mlp"></span>

<span data-ttu-id="77819-273">**X. 25 MLP** (121)</span><span class="sxs-lookup"><span data-stu-id="77819-273">**X.25 MLP** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>

<span data-ttu-id="77819-274">**Группа слежения X. 25** (122)</span><span class="sxs-lookup"><span data-stu-id="77819-274">**X.25 Hunt Group** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>

<span data-ttu-id="77819-275">**Трансп хдлк** (123)</span><span class="sxs-lookup"><span data-stu-id="77819-275">**Transp HDLC** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>

<span data-ttu-id="77819-276">**Канал чередования** (124)</span><span class="sxs-lookup"><span data-stu-id="77819-276">**Interleave Channel** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>

<span data-ttu-id="77819-277">**Быстрый канал** (125)</span><span class="sxs-lookup"><span data-stu-id="77819-277">**FAST Channel** (125)</span></span>


</dt> <dd></dd> <dt>

<span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>

<span data-ttu-id="77819-278">**IP-адрес (для АППН ХПР в IP-сетях)** (126)</span><span class="sxs-lookup"><span data-stu-id="77819-278">**IP (for APPN HPR in IP Networks)** (126)</span></span>


</dt> <dd></dd> <dt>

<span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>

<span data-ttu-id="77819-279">**КАТВ Mac Layer** (127)</span><span class="sxs-lookup"><span data-stu-id="77819-279">**CATV MAC Layer** (127)</span></span>


</dt> <dd></dd> <dt>

<span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>

<span data-ttu-id="77819-280">**Нисходящий КАТВ** (128)</span><span class="sxs-lookup"><span data-stu-id="77819-280">**CATV Downstream** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>

<span data-ttu-id="77819-281">**Вышестоящий КАТВ** (129)</span><span class="sxs-lookup"><span data-stu-id="77819-281">**CATV Upstream** (129)</span></span>


</dt> <dd></dd> <dt>

<span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>

<span data-ttu-id="77819-282">**Параметр Avalon 12MPP** (130)</span><span class="sxs-lookup"><span data-stu-id="77819-282">**Avalon 12MPP Switch** (130)</span></span>


</dt> <dd></dd> <dt>

<span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>

<span data-ttu-id="77819-283">**Туннель** (131)</span><span class="sxs-lookup"><span data-stu-id="77819-283">**Tunnel** (131)</span></span>


</dt> <dd></dd> <dt>

<span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>

<span data-ttu-id="77819-284">**Кофе** (132)</span><span class="sxs-lookup"><span data-stu-id="77819-284">**Coffee** (132)</span></span>


</dt> <dd></dd> <dt>

<span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>

<span data-ttu-id="77819-285">**Служба эмуляции канала** (133)</span><span class="sxs-lookup"><span data-stu-id="77819-285">**Circuit Emulation Service** (133)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>

<span data-ttu-id="77819-286">**Подинтерфейс ATM** (134)</span><span class="sxs-lookup"><span data-stu-id="77819-286">**ATM SubInterface** (134)</span></span>


</dt> <dd></dd> <dt>

<span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>

<span data-ttu-id="77819-287">**Виртуальная ЛС уровня 2 с помощью 802.1 q** (135)</span><span class="sxs-lookup"><span data-stu-id="77819-287">**Layer 2 VLAN using 802.1Q** (135)</span></span>


</dt> <dd></dd> <dt>

<span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>

<span data-ttu-id="77819-288">**Виртуальная ЛС уровня 3 с использованием IP-адреса** (136)</span><span class="sxs-lookup"><span data-stu-id="77819-288">**Layer 3 VLAN using IP** (136)</span></span>


</dt> <dd></dd> <dt>

<span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>

<span data-ttu-id="77819-289">**Виртуальная ЛС уровня 3 с использованием IPX** (137)</span><span class="sxs-lookup"><span data-stu-id="77819-289">**Layer 3 VLAN using IPX** (137)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>

<span data-ttu-id="77819-290">**Цифровая линия электропитания** (138)</span><span class="sxs-lookup"><span data-stu-id="77819-290">**Digital Power Line** (138)</span></span>


</dt> <dd></dd> <dt>

<span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>

<span data-ttu-id="77819-291">**Мультимедийная почта через IP-адрес** (139)</span><span class="sxs-lookup"><span data-stu-id="77819-291">**Multimedia Mail over IP** (139)</span></span>


</dt> <dd></dd> <dt>

<span id="DTM"></span><span id="dtm"></span>

<span data-ttu-id="77819-292">**DTM** (140)</span><span class="sxs-lookup"><span data-stu-id="77819-292">**DTM** (140)</span></span>


</dt> <dd></dd> <dt>

<span id="DCN"></span><span id="dcn"></span>

<span data-ttu-id="77819-293">**ДКН** (141)</span><span class="sxs-lookup"><span data-stu-id="77819-293">**DCN** (141)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>

<span data-ttu-id="77819-294">**IP-пересылка** (142)</span><span class="sxs-lookup"><span data-stu-id="77819-294">**IP Forwarding** (142)</span></span>


</dt> <dd></dd> <dt>

<span id="MSDSL"></span><span id="msdsl"></span>

<span data-ttu-id="77819-295">**MsDS** (143)</span><span class="sxs-lookup"><span data-stu-id="77819-295">**MSDSL** (143)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="77819-296">**IEEE 1394** (144)</span><span class="sxs-lookup"><span data-stu-id="77819-296">**IEEE 1394** (144)</span></span>


</dt> <dd></dd> <dt>

<span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>

<span data-ttu-id="77819-297">**If-ГСН/хиппи-6400** (145)</span><span class="sxs-lookup"><span data-stu-id="77819-297">**IF-GSN/HIPPI-6400** (145)</span></span>


</dt> <dd></dd> <dt>

<span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>

<span data-ttu-id="77819-298">**Уровень DVB-RCC Mac** (146)</span><span class="sxs-lookup"><span data-stu-id="77819-298">**DVB-RCC MAC Layer** (146)</span></span>


</dt> <dd></dd> <dt>

<span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>

<span data-ttu-id="77819-299">**Подчиненный DVB-RCC** (147)</span><span class="sxs-lookup"><span data-stu-id="77819-299">**DVB-RCC Downstream** (147)</span></span>


</dt> <dd></dd> <dt>

<span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>

<span data-ttu-id="77819-300">**Вышестоящее телевидение DVB-RCC** (148)</span><span class="sxs-lookup"><span data-stu-id="77819-300">**DVB-RCC Upstream** (148)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>

<span data-ttu-id="77819-301">**Виртуальная Банкомат** (149)</span><span class="sxs-lookup"><span data-stu-id="77819-301">**ATM Virtual** (149)</span></span>


</dt> <dd></dd> <dt>

<span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>

<span data-ttu-id="77819-302">**Туннель MPLS** (150)</span><span class="sxs-lookup"><span data-stu-id="77819-302">**MPLS Tunnel** (150)</span></span>


</dt> <dd></dd> <dt>

<span id="SRP"></span><span id="srp"></span>

<span data-ttu-id="77819-303">**SRP** (151)</span><span class="sxs-lookup"><span data-stu-id="77819-303">**SRP** (151)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>

<span data-ttu-id="77819-304">Передача **голоса по сети ATM** (152)</span><span class="sxs-lookup"><span data-stu-id="77819-304">**Voice over ATM** (152)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>

<span data-ttu-id="77819-305">Передача **голоса через Frame Relay** (153)</span><span class="sxs-lookup"><span data-stu-id="77819-305">**Voice over Frame Relay** (153)</span></span>


</dt> <dd></dd> <dt>

<span id="ISDL"></span><span id="isdl"></span>

<span data-ttu-id="77819-306">**Исдл** (154)</span><span class="sxs-lookup"><span data-stu-id="77819-306">**ISDL** (154)</span></span>


</dt> <dd></dd> <dt>

<span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>

<span data-ttu-id="77819-307">**Составная ссылка** (155)</span><span class="sxs-lookup"><span data-stu-id="77819-307">**Composite Link** (155)</span></span>


</dt> <dd></dd> <dt>

<span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>

<span data-ttu-id="77819-308">**Канал сигнализации SS7** (156)</span><span class="sxs-lookup"><span data-stu-id="77819-308">**SS7 Signaling Link** (156)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>

<span data-ttu-id="77819-309">**Частная сеть P2P** (157)</span><span class="sxs-lookup"><span data-stu-id="77819-309">**Proprietary P2P Wireless** (157)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>

<span data-ttu-id="77819-310">**Кадр вперед** (158)</span><span class="sxs-lookup"><span data-stu-id="77819-310">**Frame Forward** (158)</span></span>


</dt> <dd></dd> <dt>

<span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>

<span data-ttu-id="77819-311">**RFC1483 по протоколу ATM** (159)</span><span class="sxs-lookup"><span data-stu-id="77819-311">**RFC1483 Multiprotocol over ATM** (159)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="77819-312">**USB** (160)</span><span class="sxs-lookup"><span data-stu-id="77819-312">**USB** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>

<span data-ttu-id="77819-313">**Агрегирование ссылок AD IEEE 802.3** (161)</span><span class="sxs-lookup"><span data-stu-id="77819-313">**IEEE 802.3ad Link Aggregate** (161)</span></span>


</dt> <dd></dd> <dt>

<span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>

<span data-ttu-id="77819-314">**Учет политики BGP** (162)</span><span class="sxs-lookup"><span data-stu-id="77819-314">**BGP Policy Accounting** (162)</span></span>


</dt> <dd></dd> <dt>

<span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>

<span data-ttu-id="77819-315">**ФРФ .16 многоканальная связь fr** (163)</span><span class="sxs-lookup"><span data-stu-id="77819-315">**FRF .16 Multilink FR** (163)</span></span>


</dt> <dd></dd> <dt>

<span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>

<span data-ttu-id="77819-316">**Привратник H. 323** (164)</span><span class="sxs-lookup"><span data-stu-id="77819-316">**H.323 Gatekeeper** (164)</span></span>


</dt> <dd></dd> <dt>

<span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>

<span data-ttu-id="77819-317">**H. 323-прокси** (165)</span><span class="sxs-lookup"><span data-stu-id="77819-317">**H.323 Proxy** (165)</span></span>


</dt> <dd></dd> <dt>

<span id="MPLS"></span><span id="mpls"></span>

<span data-ttu-id="77819-318">**MPLS** (166)</span><span class="sxs-lookup"><span data-stu-id="77819-318">**MPLS** (166)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>

<span data-ttu-id="77819-319">**Многочастотная ссылка на сигнал** (167)</span><span class="sxs-lookup"><span data-stu-id="77819-319">**Multi-Frequency Signaling Link** (167)</span></span>


</dt> <dd></dd> <dt>

<span id="HDSL-2"></span><span id="hdsl-2"></span>

<span data-ttu-id="77819-320">**Хдсл-2** (168)</span><span class="sxs-lookup"><span data-stu-id="77819-320">**HDSL-2** (168)</span></span>


</dt> <dd></dd> <dt>

<span id="S-HDSL"></span><span id="s-hdsl"></span>

<span data-ttu-id="77819-321">**S-хдсл** (169)</span><span class="sxs-lookup"><span data-stu-id="77819-321">**S-HDSL** (169)</span></span>


</dt> <dd></dd> <dt>

<span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>

<span data-ttu-id="77819-322">**Ссылка на данные DS1-устройства** (170)</span><span class="sxs-lookup"><span data-stu-id="77819-322">**DS1 Facility Data Link** (170)</span></span>


</dt> <dd></dd> <dt>

<span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>

<span data-ttu-id="77819-323">**Пакет через Сонет/СДХ** (171)</span><span class="sxs-lookup"><span data-stu-id="77819-323">**Packet over SONET/SDH** (171)</span></span>


</dt> <dd></dd> <dt>

<span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>

<span data-ttu-id="77819-324">**Вход DVB-АСИ** (172)</span><span class="sxs-lookup"><span data-stu-id="77819-324">**DVB-ASI Input** (172)</span></span>


</dt> <dd></dd> <dt>

<span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>

<span data-ttu-id="77819-325">**Выходные данные DVB-АСИ** (173)</span><span class="sxs-lookup"><span data-stu-id="77819-325">**DVB-ASI Output** (173)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>

<span data-ttu-id="77819-326">**Линия электропитания** (174)</span><span class="sxs-lookup"><span data-stu-id="77819-326">**Power Line** (174)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>

<span data-ttu-id="77819-327">**Связанные сигналы без устройства** (175)</span><span class="sxs-lookup"><span data-stu-id="77819-327">**Non Facility Associated Signaling** (175)</span></span>


</dt> <dd></dd> <dt>

<span id="TR008"></span><span id="tr008"></span>

<span data-ttu-id="77819-328">**TR008** (176)</span><span class="sxs-lookup"><span data-stu-id="77819-328">**TR008** (176)</span></span>


</dt> <dd></dd> <dt>

<span id="GR303_RDT"></span><span id="gr303_rdt"></span>

<span data-ttu-id="77819-329">**GR303 РДТ** (177)</span><span class="sxs-lookup"><span data-stu-id="77819-329">**GR303 RDT** (177)</span></span>


</dt> <dd></dd> <dt>

<span id="GR303_IDT"></span><span id="gr303_idt"></span>

<span data-ttu-id="77819-330">**GR303 IDT** (178)</span><span class="sxs-lookup"><span data-stu-id="77819-330">**GR303 IDT** (178)</span></span>


</dt> <dd></dd> <dt>

<span id="ISUP"></span><span id="isup"></span>

<span data-ttu-id="77819-331">**ИСУП** (179)</span><span class="sxs-lookup"><span data-stu-id="77819-331">**ISUP** (179)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>

<span data-ttu-id="77819-332">**Частный уровень беспроводной сети Mac** (180)</span><span class="sxs-lookup"><span data-stu-id="77819-332">**Proprietary Wireless MAC Layer** (180)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>

<span data-ttu-id="77819-333">**Собственная беспроводная сеть** (181)</span><span class="sxs-lookup"><span data-stu-id="77819-333">**Proprietary Wireless Downstream** (181)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>

<span data-ttu-id="77819-334">**Частные Беспроводные потоки** (182)</span><span class="sxs-lookup"><span data-stu-id="77819-334">**Proprietary Wireless Upstream** (182)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>

<span data-ttu-id="77819-335">**Тип хиперлан 2** (183)</span><span class="sxs-lookup"><span data-stu-id="77819-335">**HIPERLAN Type 2** (183)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Broadband_Wireless_Access_Point_to_Mulipoint"></span><span id="proprietary_broadband_wireless_access_point_to_mulipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULIPOINT"></span>

<span data-ttu-id="77819-336">**Собственная широкополосная беспроводная точка доступа к мулипоинт** (184)</span><span class="sxs-lookup"><span data-stu-id="77819-336">**Proprietary Broadband Wireless Access Point to Mulipoint** (184)</span></span>


</dt> <dd></dd> <dt>

<span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>

<span data-ttu-id="77819-337">**Канал накладных расходов Сонет** (185)</span><span class="sxs-lookup"><span data-stu-id="77819-337">**SONET Overhead Channel** (185)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>

<span data-ttu-id="77819-338">**Канал накладных расходов цифровых оболочек** (186)</span><span class="sxs-lookup"><span data-stu-id="77819-338">**Digital Wrapper Overhead Channel** (186)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>

<span data-ttu-id="77819-339">**Уровень адаптации ATM 2** (187)</span><span class="sxs-lookup"><span data-stu-id="77819-339">**ATM Adaptation Layer 2** (187)</span></span>


</dt> <dd></dd> <dt>

<span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>

<span data-ttu-id="77819-340">**Радио Mac** (188)</span><span class="sxs-lookup"><span data-stu-id="77819-340">**Radio MAC** (188)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>

<span data-ttu-id="77819-341">**ATM-радио** (189)</span><span class="sxs-lookup"><span data-stu-id="77819-341">**ATM Radio** (189)</span></span>


</dt> <dd></dd> <dt>

<span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>

<span data-ttu-id="77819-342">**Межмашинная магистраль между компьютерами** (190)</span><span class="sxs-lookup"><span data-stu-id="77819-342">**Inter Machine Trunk** (190)</span></span>


</dt> <dd></dd> <dt>

<span id="MVL_DSL"></span><span id="mvl_dsl"></span>

<span data-ttu-id="77819-343">**МВЛ DSL** (191)</span><span class="sxs-lookup"><span data-stu-id="77819-343">**MVL DSL** (191)</span></span>


</dt> <dd></dd> <dt>

<span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>

<span data-ttu-id="77819-344">**Общедоступный для чтения DSL** (192)</span><span class="sxs-lookup"><span data-stu-id="77819-344">**Long Read DSL** (192)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>

<span data-ttu-id="77819-345">**Конечная точка DLCI Frame Relay** (193)</span><span class="sxs-lookup"><span data-stu-id="77819-345">**Frame Relay DLCI Endpoint** (193)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>

<span data-ttu-id="77819-346">**Конечная точка ATM VCI** (194)</span><span class="sxs-lookup"><span data-stu-id="77819-346">**ATM VCI Endpoint** (194)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>

<span data-ttu-id="77819-347">**Оптический канал** (195)</span><span class="sxs-lookup"><span data-stu-id="77819-347">**Optical Channel** (195)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>

<span data-ttu-id="77819-348">**Оптический транспорт** (196)</span><span class="sxs-lookup"><span data-stu-id="77819-348">**Optical Transport** (196)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>

<span data-ttu-id="77819-349">**Собственная ATM** (197)</span><span class="sxs-lookup"><span data-stu-id="77819-349">**Proprietary ATM** (197)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>

<span data-ttu-id="77819-350">**Речь по кабелю** (198)</span><span class="sxs-lookup"><span data-stu-id="77819-350">**Voice over Cable** (198)</span></span>


</dt> <dd></dd> <dt>

<span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

<span data-ttu-id="77819-351">**InfiniBand** (199)</span><span class="sxs-lookup"><span data-stu-id="77819-351">**Infiniband** (199)</span></span>


</dt> <dd></dd> <dt>

<span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>

<span data-ttu-id="77819-352">**Ссылка TE** (200)</span><span class="sxs-lookup"><span data-stu-id="77819-352">**TE Link** (200)</span></span>


</dt> <dd></dd> <dt>

<span id="Q.2931"></span><span id="q.2931"></span>

<span data-ttu-id="77819-353">**Q. 2931** (201)</span><span class="sxs-lookup"><span data-stu-id="77819-353">**Q.2931** (201)</span></span>


</dt> <dd></dd> <dt>

<span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>

<span data-ttu-id="77819-354">**Виртуальная магистральная группа** (202)</span><span class="sxs-lookup"><span data-stu-id="77819-354">**Virtual Trunk Group** (202)</span></span>


</dt> <dd></dd> <dt>

<span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>

<span data-ttu-id="77819-355">**Магистральная группа SIP** (203)</span><span class="sxs-lookup"><span data-stu-id="77819-355">**SIP Trunk Group** (203)</span></span>


</dt> <dd></dd> <dt>

<span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>

<span data-ttu-id="77819-356">**Сигнал SIP** (204)</span><span class="sxs-lookup"><span data-stu-id="77819-356">**SIP Signaling** (204)</span></span>


</dt> <dd></dd> <dt>

<span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>

<span data-ttu-id="77819-357">**Вышестоящий канал КАТВ** (205)</span><span class="sxs-lookup"><span data-stu-id="77819-357">**CATV Upstream Channel** (205)</span></span>


</dt> <dd></dd> <dt>

<span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>

<span data-ttu-id="77819-358">**Еконет** (206)</span><span class="sxs-lookup"><span data-stu-id="77819-358">**Econet** (206)</span></span>


</dt> <dd></dd> <dt>

<span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>

<span data-ttu-id="77819-359">**ФСАН 155MB Пон** (207)</span><span class="sxs-lookup"><span data-stu-id="77819-359">**FSAN 155Mb PON** (207)</span></span>


</dt> <dd></dd> <dt>

<span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>

<span data-ttu-id="77819-360">**ФСАН 622MB Пон** (208)</span><span class="sxs-lookup"><span data-stu-id="77819-360">**FSAN 622Mb PON** (208)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>

<span data-ttu-id="77819-361">**Прозрачный мост** (209)</span><span class="sxs-lookup"><span data-stu-id="77819-361">**Transparent Bridge** (209)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>

<span data-ttu-id="77819-362">**Группа линий** (210)</span><span class="sxs-lookup"><span data-stu-id="77819-362">**Line Group** (210)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_E_M_Feature_Group"></span><span id="voice_e_m_feature_group"></span><span id="VOICE_E_M_FEATURE_GROUP"></span>

<span data-ttu-id="77819-363">**Группа функций Voice E&M** (211)</span><span class="sxs-lookup"><span data-stu-id="77819-363">**Voice E&M Feature Group** (211)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>

<span data-ttu-id="77819-364">**Voice ФГД еана** (212)</span><span class="sxs-lookup"><span data-stu-id="77819-364">**Voice FGD EANA** (212)</span></span>


</dt> <dd></dd> <dt>

<span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>

<span data-ttu-id="77819-365">**Voice** (213)</span><span class="sxs-lookup"><span data-stu-id="77819-365">**Voice DID** (213)</span></span>


</dt> <dd></dd> <dt>

<span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>

<span data-ttu-id="77819-366">**Транспорт MPEG** (214)</span><span class="sxs-lookup"><span data-stu-id="77819-366">**MPEG Transport** (214)</span></span>


</dt> <dd></dd> <dt>

<span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>

<span data-ttu-id="77819-367">**6to4** (215)</span><span class="sxs-lookup"><span data-stu-id="77819-367">**6To4** (215)</span></span>


</dt> <dd></dd> <dt>

<span id="GTP"></span><span id="gtp"></span>

<span data-ttu-id="77819-368">**Гтп** (216)</span><span class="sxs-lookup"><span data-stu-id="77819-368">**GTP** (216)</span></span>


</dt> <dd></dd> <dt>

<span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>

<span data-ttu-id="77819-369">**Парадине есерлуп 1** (217)</span><span class="sxs-lookup"><span data-stu-id="77819-369">**Paradyne EtherLoop 1** (217)</span></span>


</dt> <dd></dd> <dt>

<span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>

<span data-ttu-id="77819-370">**Парадине есерлуп 2** (218)</span><span class="sxs-lookup"><span data-stu-id="77819-370">**Paradyne EtherLoop 2** (218)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>

<span data-ttu-id="77819-371">**Группа оптических каналов** (219)</span><span class="sxs-lookup"><span data-stu-id="77819-371">**Optical Channel Group** (219)</span></span>


</dt> <dd></dd> <dt>

<span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>

<span data-ttu-id="77819-372">**Хомепна** (220)</span><span class="sxs-lookup"><span data-stu-id="77819-372">**HomePNA** (220)</span></span>


</dt> <dd></dd> <dt>

<span id="GFP"></span><span id="gfp"></span>

<span data-ttu-id="77819-373">**ГФП** (221)</span><span class="sxs-lookup"><span data-stu-id="77819-373">**GFP** (221)</span></span>


</dt> <dd></dd> <dt>

<span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>

<span data-ttu-id="77819-374">**Цискоислвлан** (222)</span><span class="sxs-lookup"><span data-stu-id="77819-374">**ciscoISLvlan** (222)</span></span>


</dt> <dd></dd> <dt>

<span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>

<span data-ttu-id="77819-375">**актелисметалуп** (223)</span><span class="sxs-lookup"><span data-stu-id="77819-375">**actelisMetaLOOP** (223)</span></span>


</dt> <dd></dd> <dt>

<span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>

<span data-ttu-id="77819-376">**ФЦип** (224)</span><span class="sxs-lookup"><span data-stu-id="77819-376">**Fcip** (224)</span></span>


</dt> <dd></dd> <dt>

<span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>

<span data-ttu-id="77819-377">**Зарезервирован IANA** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="77819-377">**IANA Reserved** (225..4095)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="77819-378">**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="77819-378">**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="77819-379">**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="77819-379">**IPv6** (4097)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

<span data-ttu-id="77819-380">**IPv4/V6** (4098)</span><span class="sxs-lookup"><span data-stu-id="77819-380">**IPv4/v6** (4098)</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="77819-381">**IPX** (4099)</span><span class="sxs-lookup"><span data-stu-id="77819-381">**IPX** (4099)</span></span>


</dt> <dd></dd> <dt>

<span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>

<span data-ttu-id="77819-382">Протокол **DECnet** (4100)</span><span class="sxs-lookup"><span data-stu-id="77819-382">**DECnet** (4100)</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="77819-383">**SNA** (4101)</span><span class="sxs-lookup"><span data-stu-id="77819-383">**SNA** (4101)</span></span>


</dt> <dd></dd> <dt>

<span id="CONP"></span><span id="conp"></span>

<span data-ttu-id="77819-384">**КОНП** (4102)</span><span class="sxs-lookup"><span data-stu-id="77819-384">**CONP** (4102)</span></span>


</dt> <dd></dd> <dt>

<span id="CLNP"></span><span id="clnp"></span>

<span data-ttu-id="77819-385">**Клнп** (4103)</span><span class="sxs-lookup"><span data-stu-id="77819-385">**CLNP** (4103)</span></span>


</dt> <dd></dd> <dt>

<span id="VINES"></span><span id="vines"></span>

<span data-ttu-id="77819-386">**Vines** (4104)</span><span class="sxs-lookup"><span data-stu-id="77819-386">**VINES** (4104)</span></span>


</dt> <dd></dd> <dt>

<span id="XNS"></span><span id="xns"></span>

<span data-ttu-id="77819-387">**КСНС** (4105)</span><span class="sxs-lookup"><span data-stu-id="77819-387">**XNS** (4105)</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>

<span data-ttu-id="77819-388">**Конечная точка канала ISDN B** (4106)</span><span class="sxs-lookup"><span data-stu-id="77819-388">**ISDN B Channel Endpoint** (4106)</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>

<span data-ttu-id="77819-389">**Конечная точка D канала ISDN** (4107)</span><span class="sxs-lookup"><span data-stu-id="77819-389">**ISDN D Channel Endpoint** (4107)</span></span>


</dt> <dd></dd> <dt>

<span id="BGP"></span><span id="bgp"></span>

<span data-ttu-id="77819-390">**BGP** (4108)</span><span class="sxs-lookup"><span data-stu-id="77819-390">**BGP** (4108)</span></span>


</dt> <dd></dd> <dt>

<span id="OSPF"></span><span id="ospf"></span>

<span data-ttu-id="77819-391">**OSPF** (4109)</span><span class="sxs-lookup"><span data-stu-id="77819-391">**OSPF** (4109)</span></span>


</dt> <dd></dd> <dt>

<span id="UDP"></span><span id="udp"></span>

<span data-ttu-id="77819-392">**UDP** (4110)</span><span class="sxs-lookup"><span data-stu-id="77819-392">**UDP** (4110)</span></span>


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="77819-393">**TCP** (4111)</span><span class="sxs-lookup"><span data-stu-id="77819-393">**TCP** (4111)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11a"></span><span id="802.11A"></span>

<span data-ttu-id="77819-394">**802.11 a** (4112)</span><span class="sxs-lookup"><span data-stu-id="77819-394">**802.11a** (4112)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11b"></span><span id="802.11B"></span>

<span data-ttu-id="77819-395">**802.11 b** (4113)</span><span class="sxs-lookup"><span data-stu-id="77819-395">**802.11b** (4113)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11g"></span><span id="802.11G"></span>

<span data-ttu-id="77819-396">**802.11 g** (4114)</span><span class="sxs-lookup"><span data-stu-id="77819-396">**802.11g** (4114)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11h"></span><span id="802.11H"></span>

<span data-ttu-id="77819-397">**802.11 h** (4115)</span><span class="sxs-lookup"><span data-stu-id="77819-397">**802.11h** (4115)</span></span>


</dt> <dd></dd> <dt>

<span id="NFS"></span><span id="nfs"></span>

<span data-ttu-id="77819-398">**NFS** (4200)</span><span class="sxs-lookup"><span data-stu-id="77819-398">**NFS** (4200)</span></span>


</dt> <dd></dd> <dt>

<span id="CIFS"></span><span id="cifs"></span>

<span data-ttu-id="77819-399">**CIFS** (4201)</span><span class="sxs-lookup"><span data-stu-id="77819-399">**CIFS** (4201)</span></span>


</dt> <dd></dd> <dt>

<span id="DAFS"></span><span id="dafs"></span>

<span data-ttu-id="77819-400">**ДАФС** (4202)</span><span class="sxs-lookup"><span data-stu-id="77819-400">**DAFS** (4202)</span></span>


</dt> <dd></dd> <dt>

<span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>

<span data-ttu-id="77819-401">Протокол **WebDAV** (4203)</span><span class="sxs-lookup"><span data-stu-id="77819-401">**WebDAV** (4203)</span></span>


</dt> <dd></dd> <dt>

<span id="HTTP"></span><span id="http"></span>

<span data-ttu-id="77819-402">**Http** (4204)</span><span class="sxs-lookup"><span data-stu-id="77819-402">**HTTP** (4204)</span></span>


</dt> <dd></dd> <dt>

<span id="FTP"></span><span id="ftp"></span>

<span data-ttu-id="77819-403">**FTP** (4205)</span><span class="sxs-lookup"><span data-stu-id="77819-403">**FTP** (4205)</span></span>


</dt> <dd></dd> <dt>

<span id="NDMP"></span><span id="ndmp"></span>

<span data-ttu-id="77819-404">**Ндмп** (4300)</span><span class="sxs-lookup"><span data-stu-id="77819-404">**NDMP** (4300)</span></span>


</dt> <dd></dd> <dt>

<span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>

<span data-ttu-id="77819-405">**Telnet** (4400)</span><span class="sxs-lookup"><span data-stu-id="77819-405">**Telnet** (4400)</span></span>


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

<span data-ttu-id="77819-406">**SSH** (4401)</span><span class="sxs-lookup"><span data-stu-id="77819-406">**SSH** (4401)</span></span>


</dt> <dd></dd> <dt>

<span id="SM_CLP"></span><span id="sm_clp"></span>

<span data-ttu-id="77819-407">**SM CLP** (4402)</span><span class="sxs-lookup"><span data-stu-id="77819-407">**SM CLP** (4402)</span></span>


</dt> <dd></dd> <dt>

<span id="SMTP"></span><span id="smtp"></span>

<span data-ttu-id="77819-408">**SMTP** (4403)</span><span class="sxs-lookup"><span data-stu-id="77819-408">**SMTP** (4403)</span></span>


</dt> <dd></dd> <dt>

<span id="LDAP"></span><span id="ldap"></span>

<span data-ttu-id="77819-409">**LDAP** (4404)</span><span class="sxs-lookup"><span data-stu-id="77819-409">**LDAP** (4404)</span></span>


</dt> <dd></dd> <dt>

<span id="RDP"></span><span id="rdp"></span>

<span data-ttu-id="77819-410">**RDP** (4405)</span><span class="sxs-lookup"><span data-stu-id="77819-410">**RDP** (4405)</span></span>


</dt> <dd></dd> <dt>

<span id="HTTPS"></span><span id="https"></span>

<span data-ttu-id="77819-411">**HTTPS** (4406)</span><span class="sxs-lookup"><span data-stu-id="77819-411">**HTTPS** (4406)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="77819-412">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="77819-412">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="77819-413">**Поставщик зарезервирован** (32768...)</span><span class="sxs-lookup"><span data-stu-id="77819-413">**Vendor Reserved** (32768..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="77819-414">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="77819-414">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77819-415">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="77819-415">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="77819-416">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77819-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77819-417">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM \_ протоколендпоинт**.**Протоколифтипе**"), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ протоколендпоинт**.**Осертипедескриптион**")</span><span class="sxs-lookup"><span data-stu-id="77819-417">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_ProtocolEndpoint**.**ProtocolIFType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ProtocolEndpoint**.**OtherTypeDescription**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="77819-418">Нерекомендуемое описание: перечисление, используемое для категоризации и классификации различных экземпляров этого класса.</span><span class="sxs-lookup"><span data-stu-id="77819-418">Deprecated description: An enumeration used to categorize and classify different instances of this class.</span></span>

 

<span data-ttu-id="77819-419">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="77819-419">This property is deprecated.</span></span> <span data-ttu-id="77819-420">Вместо этого используйте свойство **протоколифтипе** .</span><span class="sxs-lookup"><span data-stu-id="77819-420">Instead, use the **ProtocolIFType** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="77819-421">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="77819-421">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="77819-422">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="77819-422">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="77819-423">**IPv4** (2)</span><span class="sxs-lookup"><span data-stu-id="77819-423">**IPv4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="77819-424">**IPv6** (3)</span><span class="sxs-lookup"><span data-stu-id="77819-424">**IPv6** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="77819-425">**IPX** (4)</span><span class="sxs-lookup"><span data-stu-id="77819-425">**IPX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AppleTalk"></span><span id="appletalk"></span><span id="APPLETALK"></span>

<span data-ttu-id="77819-426">**AppleTalk** (5)</span><span class="sxs-lookup"><span data-stu-id="77819-426">**AppleTalk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>

<span data-ttu-id="77819-427">Протокол **DECnet** (6)</span><span class="sxs-lookup"><span data-stu-id="77819-427">**DECnet** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="77819-428">**SNA** (7)</span><span class="sxs-lookup"><span data-stu-id="77819-428">**SNA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="CONP"></span><span id="conp"></span>

<span data-ttu-id="77819-429">**КОНП** (8)</span><span class="sxs-lookup"><span data-stu-id="77819-429">**CONP** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="CLNP"></span><span id="clnp"></span>

<span data-ttu-id="77819-430">**Клнп** (9)</span><span class="sxs-lookup"><span data-stu-id="77819-430">**CLNP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="VINES"></span><span id="vines"></span>

<span data-ttu-id="77819-431">**Vines** (10)</span><span class="sxs-lookup"><span data-stu-id="77819-431">**VINES** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="XNS"></span><span id="xns"></span>

<span data-ttu-id="77819-432">**КСНС** (11)</span><span class="sxs-lookup"><span data-stu-id="77819-432">**XNS** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="77819-433">**ATM** (12)</span><span class="sxs-lookup"><span data-stu-id="77819-433">**ATM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

<span data-ttu-id="77819-434">**Frame Relay** (13)</span><span class="sxs-lookup"><span data-stu-id="77819-434">**Frame Relay** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="77819-435">**Ethernet** (14)</span><span class="sxs-lookup"><span data-stu-id="77819-435">**Ethernet** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="TokenRing"></span><span id="tokenring"></span><span id="TOKENRING"></span>

<span data-ttu-id="77819-436">**Токенринг** (15)</span><span class="sxs-lookup"><span data-stu-id="77819-436">**TokenRing** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="77819-437">**FDDI** (16)</span><span class="sxs-lookup"><span data-stu-id="77819-437">**FDDI** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

<span data-ttu-id="77819-438">**InfiniBand** (17)</span><span class="sxs-lookup"><span data-stu-id="77819-438">**Infiniband** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>

<span data-ttu-id="77819-439">**Fibre Channel** (18)</span><span class="sxs-lookup"><span data-stu-id="77819-439">**Fibre Channel** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN_BRI_Endpoint"></span><span id="isdn_bri_endpoint"></span><span id="ISDN_BRI_ENDPOINT"></span>

<span data-ttu-id="77819-440">**Конечная точка ISDN Анд** (19)</span><span class="sxs-lookup"><span data-stu-id="77819-440">**ISDN BRI Endpoint** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>

<span data-ttu-id="77819-441">**Конечная точка канала ISDN B** (20)</span><span class="sxs-lookup"><span data-stu-id="77819-441">**ISDN B Channel Endpoint** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>

<span data-ttu-id="77819-442">**Конечная точка D канала ISDN** (21)</span><span class="sxs-lookup"><span data-stu-id="77819-442">**ISDN D Channel Endpoint** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

<span data-ttu-id="77819-443">**IPv4/V6** (22)</span><span class="sxs-lookup"><span data-stu-id="77819-443">**IPv4/v6** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="BGP"></span><span id="bgp"></span>

<span data-ttu-id="77819-444">**BGP** (23)</span><span class="sxs-lookup"><span data-stu-id="77819-444">**BGP** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="OSPF"></span><span id="ospf"></span>

<span data-ttu-id="77819-445">**OSPF** (24)</span><span class="sxs-lookup"><span data-stu-id="77819-445">**OSPF** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="MPLS"></span><span id="mpls"></span>

<span data-ttu-id="77819-446">**MPLS** (25)</span><span class="sxs-lookup"><span data-stu-id="77819-446">**MPLS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="UDP"></span><span id="udp"></span>

<span data-ttu-id="77819-447">**UDP** (26)</span><span class="sxs-lookup"><span data-stu-id="77819-447">**UDP** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="77819-448">**TCP** (27)</span><span class="sxs-lookup"><span data-stu-id="77819-448">**TCP** (27)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="77819-449">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="77819-449">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77819-450">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="77819-450">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="77819-451">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77819-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77819-452">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("тимеофластстатечанже"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| If-MIB. ифластчанже ")</span><span class="sxs-lookup"><span data-stu-id="77819-452">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("TimeOfLastStateChange"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|IF-MIB.ifLastChange")</span></span>
</dt> </dl>

<span data-ttu-id="77819-453">Дата и время последнего изменения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="77819-453">The date and time when the **EnabledState** property last changed.</span></span> <span data-ttu-id="77819-454">Если параметр **EnabledState** не изменился и это свойство заполнено, то для него должно быть задано нулевое значение интервала.</span><span class="sxs-lookup"><span data-stu-id="77819-454">If **EnabledState** has not changed and this property is populated, then it must be set to a zero interval value.</span></span> <span data-ttu-id="77819-455">Если изменение состояния было запрошено, но отклонено или еще не обработано, свойство не должно обновляться.</span><span class="sxs-lookup"><span data-stu-id="77819-455">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="77819-456">Требования</span><span class="sxs-lookup"><span data-stu-id="77819-456">Requirements</span></span>



| <span data-ttu-id="77819-457">Требование</span><span class="sxs-lookup"><span data-stu-id="77819-457">Requirement</span></span> | <span data-ttu-id="77819-458">Значение</span><span class="sxs-lookup"><span data-stu-id="77819-458">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77819-459">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77819-459">Minimum supported client</span></span><br/> | <span data-ttu-id="77819-460">Windows 8</span><span class="sxs-lookup"><span data-stu-id="77819-460">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="77819-461">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77819-461">Minimum supported server</span></span><br/> | <span data-ttu-id="77819-462">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="77819-462">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="77819-463">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="77819-463">Namespace</span></span><br/>                | <span data-ttu-id="77819-464">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="77819-464">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="77819-465">MOF</span><span class="sxs-lookup"><span data-stu-id="77819-465">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77819-466"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77819-466"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="77819-467">DLL</span><span class="sxs-lookup"><span data-stu-id="77819-467">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77819-468"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="77819-468"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="77819-469">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77819-469">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77819-470">**\_СЕРВИЦЕАКЦЕССПОИНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="77819-470">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> </dl>

 

