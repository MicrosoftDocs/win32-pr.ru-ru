---
description: Макрос типа уведомления содержит следующие элементы.
ms.assetid: b7c6ec2b-640b-4373-a1e3-ff6c130b07d0
ms.tgt_platform: multiple
title: Макрос типа уведомления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2ff7695d7ca36eeaf01115d47df496d52d68ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647219"
---
# <a name="notification-type-macro"></a><span data-ttu-id="c0dd6-103">Макрос типа уведомления</span><span class="sxs-lookup"><span data-stu-id="c0dd6-103">NOTIFICATION-TYPE Macro</span></span>

<span data-ttu-id="c0dd6-104">Макрос типа уведомления содержит следующие элементы.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-104">The NOTIFICATION-TYPE macro contains the following elements.</span></span>

> [!Note]  
> <span data-ttu-id="c0dd6-105">Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="c0dd6-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="components"></a><span data-ttu-id="c0dd6-106">Компоненты</span><span class="sxs-lookup"><span data-stu-id="c0dd6-106">Components</span></span>

<dl> <dt>

<span data-ttu-id="c0dd6-107"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Дескриптор объекта</span><span class="sxs-lookup"><span data-stu-id="c0dd6-107"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Object descriptor</span></span>
</dt> <dd>

<span data-ttu-id="c0dd6-108">Присоединяет имя к событию SNMP в макросе типа уведомления.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-108">Attaches a name to an SNMP event in a NOTIFICATION-TYPE macro.</span></span> <span data-ttu-id="c0dd6-109">В следующем списке перечислены правила сопоставления дескриптора объекта.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-109">The following list lists the rules for mapping the object descriptor.</span></span>



| <span data-ttu-id="c0dd6-110">Тип</span><span class="sxs-lookup"><span data-stu-id="c0dd6-110">Type</span></span>                        | <span data-ttu-id="c0dd6-111">Concatenate</span><span class="sxs-lookup"><span data-stu-id="c0dd6-111">Concatenate</span></span>                                                                                                                                                                                                                                                                                                           |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0dd6-112">Имя инкапсулированного класса CIM</span><span class="sxs-lookup"><span data-stu-id="c0dd6-112">Encapsulated CIM class name</span></span> | <span data-ttu-id="c0dd6-113">"SNMP \_ "</span><span class="sxs-lookup"><span data-stu-id="c0dd6-113">"SNMP\_"</span></span><br/> <span data-ttu-id="c0dd6-114">Имя удостоверения модуля MIB</span><span class="sxs-lookup"><span data-stu-id="c0dd6-114">MIB module identity name</span></span><br/> <span data-ttu-id="c0dd6-115">символ подчеркивания ( \_ )</span><span class="sxs-lookup"><span data-stu-id="c0dd6-115">underscore (\_)</span></span><br/> <span data-ttu-id="c0dd6-116">Дескриптор объекта</span><span class="sxs-lookup"><span data-stu-id="c0dd6-116">object descriptor</span></span><br/> <span data-ttu-id="c0dd6-117">" \_ Уведомление"</span><span class="sxs-lookup"><span data-stu-id="c0dd6-117">"\_Notification"</span></span><br/> <span data-ttu-id="c0dd6-118">Пример. уведомление **втпсервердисаблед** из **Cisco-ВТП-MIB** сопоставляется с **\_ \_ \_ \_ \_ уведомлением SNMP Cisco ВТП MIB втпсервердисаблед**.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-118">Example: The **vtpServerDisabled** notification from the **CISCO-VTP-MIB** maps to **SNMP\_CISCO\_VTP\_MIB\_vtpServerDisabled\_Notification**.</span></span><br/>                 |
| <span data-ttu-id="c0dd6-119">Имя класса CIM референт</span><span class="sxs-lookup"><span data-stu-id="c0dd6-119">Referent CIM class name</span></span>     | <span data-ttu-id="c0dd6-120">"SNMP \_ "</span><span class="sxs-lookup"><span data-stu-id="c0dd6-120">"SNMP\_"</span></span><br/> <span data-ttu-id="c0dd6-121">Имя удостоверения модуля MIB</span><span class="sxs-lookup"><span data-stu-id="c0dd6-121">MIB module identity name</span></span><br/> <span data-ttu-id="c0dd6-122">символ подчеркивания ( \_ )</span><span class="sxs-lookup"><span data-stu-id="c0dd6-122">underscore (\_)</span></span><br/> <span data-ttu-id="c0dd6-123">Дескриптор объекта</span><span class="sxs-lookup"><span data-stu-id="c0dd6-123">object descriptor</span></span><br/> <span data-ttu-id="c0dd6-124">" \_ Екстендеднотификатион"</span><span class="sxs-lookup"><span data-stu-id="c0dd6-124">"\_ExtendedNotification"</span></span><br/> <span data-ttu-id="c0dd6-125">Пример. уведомление **втпсервердисаблед** из **Cisco-ВТП-MIB** сопоставляется с **SNMP \_ Cisco \_ ВТП \_ MIB \_ втпсервердисаблед \_ екстендеднотификатион**.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-125">Example: The **vtpServerDisabled** notification from the **CISCO-VTP-MIB** maps to **SNMP\_CISCO\_VTP\_MIB\_vtpServerDisabled\_ExtendedNotification**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c0dd6-126"><span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>Предложение OBJECTs</span><span class="sxs-lookup"><span data-stu-id="c0dd6-126"><span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>OBJECTS clause</span></span>
</dt> <dd>

<span data-ttu-id="c0dd6-127">Перечисляет набор объектов, связанных с объектом уведомления.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-127">Enumerates the set of objects associated with the notification object.</span></span>

</dd> <dt>

<span data-ttu-id="c0dd6-128"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>Предложение REFERENCE</span><span class="sxs-lookup"><span data-stu-id="c0dd6-128"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>REFERENCE clause</span></span>
</dt> <dd>

<span data-ttu-id="c0dd6-129">Ссылается на другой документ, содержащий дополнительные сведения об объекте.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-129">Refers to another document that contains more information about the object.</span></span> <span data-ttu-id="c0dd6-130">Он сопоставляется со **ссылкой** на КВАЛИФИКАТОР класса CIM, которая имеет тип String.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-130">It maps to the CIM class qualifier **Reference**, which is of type string.</span></span>

</dd> <dt>

<span data-ttu-id="c0dd6-131"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>Предложение DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c0dd6-131"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION clause</span></span>
</dt> <dd>

<span data-ttu-id="c0dd6-132">Описывает рассматриваемый объект.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-132">Describes the object in question.</span></span> <span data-ttu-id="c0dd6-133">Он сопоставляется с **описанием** квалификатора класса CIM, который имеет тип String.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-133">It maps to the CIM class qualifier **Description**, which is of type string</span></span>

</dd> <dt>

<span data-ttu-id="c0dd6-134"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Предложение STATUS</span><span class="sxs-lookup"><span data-stu-id="c0dd6-134"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUS clause</span></span>
</dt> <dd>

<span data-ttu-id="c0dd6-135">Указывает, должен ли быть поддерживаемый объект.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-135">Indicates whether the object must be supported.</span></span> <span data-ttu-id="c0dd6-136">Если состояние **устарело** или **устарело**, уведомление отклоняется из сопоставления.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-136">When the status is either **obsolete** or **deprecated**, the notification is discarded from the mapping.</span></span> <span data-ttu-id="c0dd6-137">В противном случае это предложение сопоставляется с **состоянием** квалификатора класса CIM, который имеет тип **String**.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-137">Otherwise, this clause maps to the CIM class qualifier **Status**, which is of type **string**.</span></span>

<span data-ttu-id="c0dd6-138">Для версии в версии, предпочтительным **является либо** обязательное, либо **необязательное**, но квалификатор может содержать какое **-либо другое** значение.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-138">For SNMPv1, the preferred value of **Status** is either **mandatory** or **optional**, but the qualifier can contain some other value.</span></span> <span data-ttu-id="c0dd6-139">Для SNMPv2C предпочтительным значением **Status** является **Current** или **устарело**, но квалификатор может содержать какое-либо другое значение.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-139">For SNMPv2C, the preferred value of **Status** is either **current** or **deprecated**, but the qualifier can contain some other value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0dd6-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0dd6-140">Remarks</span></span>

<span data-ttu-id="c0dd6-141">Поставщик SNMP сопоставляет макрос **типа уведомления** с определением класса инкапсулированного или референт.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-141">The SNMP provider maps the **NOTIFICATION-TYPE** macro to either an encapsulated or referent class definition.</span></span>

<span data-ttu-id="c0dd6-142">Определение инкапсулированного класса не предоставляет сведения об экземпляре, связанные с объектом MIB.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-142">An encapsulated class definition does not expose the instance information associated with the MIB object.</span></span> <span data-ttu-id="c0dd6-143">Вместо этого определение класса кодирует предложение OBJECTs как ряд свойств класса событий CIM.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-143">Instead, the class definition encodes the OBJECTS clause as a series of properties of the CIM event class.</span></span> <span data-ttu-id="c0dd6-144">Каждое свойство CIM отражает имя, тип и значение соответствующего объекта MIB в предложении OBJECTs.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-144">Each CIM property reflects the name, type, and value of the corresponding MIB object in the OBJECTS clause.</span></span> <span data-ttu-id="c0dd6-145">Если требуются сведения об экземпляре, необходимо соотнести с классом референт.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-145">If you require instance information, you must map to a referent class.</span></span> <span data-ttu-id="c0dd6-146">Определение инкапсулированного класса сопоставляется с классом [снмпнотификатион](snmpnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="c0dd6-146">An encapsulated class definition maps to the [SnmpNotification](snmpnotification.md) class.</span></span>

<span data-ttu-id="c0dd6-147">Класс референт определяет объект MIB и сведения об экземпляре, используемые для получения объекта.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-147">A referent class defines an MIB object and the instance information used to obtain the object.</span></span> <span data-ttu-id="c0dd6-148">Определение класса кодирует предложение OBJECTs как ряд свойств класса событий CIM.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-148">The class definition encodes the OBJECTS clause as a series of properties of the CIM event class.</span></span> <span data-ttu-id="c0dd6-149">Каждое свойство CIM отражает имя соответствующего объекта MIB в предложении OBJECTs и тип как внедренный объект, отражающий экземпляр класса, связанного с этим объектом MIB.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-149">Each CIM property reflects the name of the corresponding MIB object in the OBJECTS clause and the type as an embedded object that reflects an instance of the class associated with that MIB object.</span></span> <span data-ttu-id="c0dd6-150">Затем поставщик создает класс, связанный с объектом MIB.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-150">The provider then generates a class associated with the MIB object.</span></span> <span data-ttu-id="c0dd6-151">Например, **ifIndex** сопоставляется с внедренным классом с именем **SNMP \_ RFC1213 \_ MIB \_ ifIndex**.</span><span class="sxs-lookup"><span data-stu-id="c0dd6-151">For example, **ifIndex** maps to an embedded class named **SNMP\_RFC1213\_MIB\_ifIndex**.</span></span> <span data-ttu-id="c0dd6-152">Дополнительные сведения об этом типе класса см. в разделе [объект-тип макроса](object-type-macro.md).</span><span class="sxs-lookup"><span data-stu-id="c0dd6-152">For more information about this type of class, see [OBJECT-TYPE Macro](object-type-macro.md).</span></span>

 

 




