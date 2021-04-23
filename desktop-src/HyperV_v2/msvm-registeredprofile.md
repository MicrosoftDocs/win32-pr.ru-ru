---
description: Описывает набор классов с обязательными свойствами и методами, необходимые для управления реальной сущностью или для поддержки сценария использования в среде с возможностью взаимодействия.
ms.assetid: 75644856-3B47-43B8-835C-783A6BEE7251
title: Класс Msvm_RegisteredProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredProfile
- Msvm_RegisteredProfile.InstanceID
- Msvm_RegisteredProfile.Caption
- Msvm_RegisteredProfile.Description
- Msvm_RegisteredProfile.ElementName
- Msvm_RegisteredProfile.RegisteredOrganization
- Msvm_RegisteredProfile.OtherRegisteredOrganization
- Msvm_RegisteredProfile.RegisteredName
- Msvm_RegisteredProfile.RegisteredVersion
- Msvm_RegisteredProfile.AdvertiseTypes
- Msvm_RegisteredProfile.AdvertiseTypeDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a7014687355524fbe10ff01869cac6c3fd35a894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080855"
---
# <a name="msvm_registeredprofile-class"></a><span data-ttu-id="58a8e-103">\_Класс мсвм регистередпрофиле</span><span class="sxs-lookup"><span data-stu-id="58a8e-103">Msvm\_RegisteredProfile class</span></span>

<span data-ttu-id="58a8e-104">Описывает набор классов с обязательными свойствами и методами, необходимые для управления реальной сущностью или для поддержки сценария использования в среде с возможностью взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="58a8e-104">Describes a set of classes with required properties and methods, necessary to manage a real-world entity or to support a usage scenario, in an interoperable fashion.</span></span>

<span data-ttu-id="58a8e-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="58a8e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="58a8e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58a8e-106">Syntax</span></span>

``` syntax
class Msvm_RegisteredProfile : CIM_RegisteredProfile
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 RegisteredOrganization;
  string OtherRegisteredOrganization;
  string RegisteredName;
  string RegisteredVersion;
  uint16 AdvertiseTypes[];
  string AdvertiseTypeDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="58a8e-107">Члены</span><span class="sxs-lookup"><span data-stu-id="58a8e-107">Members</span></span>

<span data-ttu-id="58a8e-108">Класс **мсвм \_ регистередпрофиле** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="58a8e-108">The **Msvm\_RegisteredProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="58a8e-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="58a8e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58a8e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="58a8e-110">Properties</span></span>

<span data-ttu-id="58a8e-111">Класс **мсвм \_ регистередпрофиле** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="58a8e-111">The **Msvm\_RegisteredProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58a8e-112">**адвертисетипедескриптионс**</span><span class="sxs-lookup"><span data-stu-id="58a8e-112">**AdvertiseTypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58a8e-113">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="58a8e-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58a8e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58a8e-115">Массив строк, предоставляющий дополнительные сведения, связанные со свойством **адвертисетипе** .</span><span class="sxs-lookup"><span data-stu-id="58a8e-115">An array of strings that provides additional information related to the **AdvertiseType** property.</span></span> <span data-ttu-id="58a8e-116">Необходимо указать описание, если **адвертисетипе** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="58a8e-116">A description must be provided when the **AdvertiseType** is 1 (Other).</span></span> <span data-ttu-id="58a8e-117">Запись в этом массиве соответствует тому же индексу в массиве **адвертисетипес** .</span><span class="sxs-lookup"><span data-stu-id="58a8e-117">An entry in this array corresponds to the same index in the **AdvertiseTypes** array.</span></span> <span data-ttu-id="58a8e-118">Это свойство наследуется от [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58a8e-118">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="58a8e-119">**адвертисетипес**</span><span class="sxs-lookup"><span data-stu-id="58a8e-119">**AdvertiseTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58a8e-120">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="58a8e-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58a8e-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58a8e-122">Указывает объявление для сведений о профиле.</span><span class="sxs-lookup"><span data-stu-id="58a8e-122">Specifies the advertisement for the profile information.</span></span> <span data-ttu-id="58a8e-123">Он используется службами рекламы инфраструктуры WBEM для определения того, что следует объявить, с помощью каких механизмов.</span><span class="sxs-lookup"><span data-stu-id="58a8e-123">It is used by the advertising services of the WBEM infrastructure to determine what should be advertised, through what mechanisms.</span></span> <span data-ttu-id="58a8e-124">Свойство является массивом, чтобы можно было объявить профиль с помощью нескольких механизмов.</span><span class="sxs-lookup"><span data-stu-id="58a8e-124">The property is an array so that the profile can be advertised using several mechanisms.</span></span> <span data-ttu-id="58a8e-125">Если это свойство имеет **значение NULL**, это эквивалентно указанию значения 2 (не объявлено).</span><span class="sxs-lookup"><span data-stu-id="58a8e-125">If this property is **Null**, this is equivalent to specifying the value 2 (Not Advertised).</span></span> <span data-ttu-id="58a8e-126">Это свойство наследуется от [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58a8e-126">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="58a8e-127"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="58a8e-127"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-128"><span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**Не объявлено** (2)</span><span class="sxs-lookup"><span data-stu-id="58a8e-128"><span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**Not Advertised** (2)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-129"><span id="SLP_"></span><span id="slp_"></span>**SLP** (3)</span><span class="sxs-lookup"><span data-stu-id="58a8e-129"><span id="SLP_"></span><span id="slp_"></span>**SLP** (3 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="58a8e-130">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="58a8e-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58a8e-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58a8e-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58a8e-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58a8e-133">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="58a8e-133">A short description of the object.</span></span> <span data-ttu-id="58a8e-134">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="58a8e-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58a8e-135">**Описание**</span><span class="sxs-lookup"><span data-stu-id="58a8e-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58a8e-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58a8e-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58a8e-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58a8e-138">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="58a8e-138">A description of the object.</span></span> <span data-ttu-id="58a8e-139">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="58a8e-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58a8e-140">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="58a8e-140">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58a8e-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58a8e-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58a8e-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58a8e-143">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="58a8e-143">A display name for the object.</span></span> <span data-ttu-id="58a8e-144">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="58a8e-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58a8e-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="58a8e-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58a8e-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58a8e-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58a8e-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-148">Квалификаторы: **ключ**, **Переопределение**</span><span class="sxs-lookup"><span data-stu-id="58a8e-148">Qualifiers: **Key**, **Override**</span></span>
</dt> </dl>

<span data-ttu-id="58a8e-149">Строка, уникально идентифицирующая экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="58a8e-149">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="58a8e-150">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="58a8e-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58a8e-151">**осеррегистередорганизатион**</span><span class="sxs-lookup"><span data-stu-id="58a8e-151">**OtherRegisteredOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58a8e-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58a8e-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58a8e-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-154">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="58a8e-154">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="58a8e-155">Строка, которая предоставляет описание организации, если **RegisteredOrganization** содержит значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="58a8e-155">A string that provides a description of the organization when **RegisteredOrganization** contains 1 (Other).</span></span> <span data-ttu-id="58a8e-156">Это свойство наследуется от [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58a8e-156">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="58a8e-157">**регистереднаме**</span><span class="sxs-lookup"><span data-stu-id="58a8e-157">**RegisteredName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58a8e-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58a8e-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58a8e-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-160">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="58a8e-160">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="58a8e-161">Имя этого зарегистрированного профиля.</span><span class="sxs-lookup"><span data-stu-id="58a8e-161">The name of this registered profile.</span></span> <span data-ttu-id="58a8e-162">Так как для одного **регистереднаме** могут существовать несколько версий, сочетание **регистереднаме**, **RegisteredOrganization** и **регистередверсион** должно однозначно идентифицировать зарегистрированный профиль в области организации.</span><span class="sxs-lookup"><span data-stu-id="58a8e-162">Since multiple versions can exist for the same **RegisteredName**, the combination of **RegisteredName**, **RegisteredOrganization**, and **RegisteredVersion** must uniquely identify the registered profile within the scope of the organization.</span></span> <span data-ttu-id="58a8e-163">Это свойство наследуется от [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58a8e-163">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="58a8e-164">**RegisteredOrganization**</span><span class="sxs-lookup"><span data-stu-id="58a8e-164">**RegisteredOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58a8e-165">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58a8e-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58a8e-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58a8e-167">Организация, которая определяет этот профиль.</span><span class="sxs-lookup"><span data-stu-id="58a8e-167">The organization that defines this profile.</span></span> <span data-ttu-id="58a8e-168">Это свойство наследуется от [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58a8e-168">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="58a8e-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="58a8e-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-170"><span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2)</span><span class="sxs-lookup"><span data-stu-id="58a8e-170"><span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-171"><span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**КомпТИА** (3)</span><span class="sxs-lookup"><span data-stu-id="58a8e-171"><span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**CompTIA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-172"><span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**Консорциум для инноваций в сфере обслуживания** (4)</span><span class="sxs-lookup"><span data-stu-id="58a8e-172"><span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**Consortium for Service Innovation** (4)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-173"><span id="FAST"></span><span id="fast"></span>**Быстрое** (5)</span><span class="sxs-lookup"><span data-stu-id="58a8e-173"><span id="FAST"></span><span id="fast"></span>**FAST** (5)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-174"><span id="GGF"></span><span id="ggf"></span>**ГГФ** (6)</span><span class="sxs-lookup"><span data-stu-id="58a8e-174"><span id="GGF"></span><span id="ggf"></span>**GGF** (6)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-175"><span id="INTAP"></span><span id="intap"></span>**Интап** (7)</span><span class="sxs-lookup"><span data-stu-id="58a8e-175"><span id="INTAP"></span><span id="intap"></span>**INTAP** (7)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-176"><span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**итсмф** (8)</span><span class="sxs-lookup"><span data-stu-id="58a8e-176"><span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**itSMF** (8)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-177"><span id="NAC"></span><span id="nac"></span>**NAC** (9)</span><span class="sxs-lookup"><span data-stu-id="58a8e-177"><span id="NAC"></span><span id="nac"></span>**NAC** (9)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-178"><span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**10-я экономичный энергетическый союз** (10)</span><span class="sxs-lookup"><span data-stu-id="58a8e-178"><span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**//10 Northwest Energy Efficiency Alliance** (10)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-179"><span id="SNIA"></span><span id="snia"></span>**Сниа** (11)</span><span class="sxs-lookup"><span data-stu-id="58a8e-179"><span id="SNIA"></span><span id="snia"></span>**SNIA** (11)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-180"><span id="TM_Forum"></span><span id="tm_forum"></span><span id="TM_FORUM"></span>**Форум TM** (12)</span><span class="sxs-lookup"><span data-stu-id="58a8e-180"><span id="TM_Forum"></span><span id="tm_forum"></span><span id="TM_FORUM"></span>**TM Forum** (12)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-181"><span id="The_Open_Group"></span><span id="the_open_group"></span><span id="THE_OPEN_GROUP"></span>**Открытая группа** (13)</span><span class="sxs-lookup"><span data-stu-id="58a8e-181"><span id="The_Open_Group"></span><span id="the_open_group"></span><span id="THE_OPEN_GROUP"></span>**The Open Group** (13)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-182"><span id="ANSI"></span><span id="ansi"></span>**ANSI** (14)</span><span class="sxs-lookup"><span data-stu-id="58a8e-182"><span id="ANSI"></span><span id="ansi"></span>**ANSI** (14)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-183"><span id="IEEE"></span><span id="ieee"></span>**IEEE** (15)</span><span class="sxs-lookup"><span data-stu-id="58a8e-183"><span id="IEEE"></span><span id="ieee"></span>**IEEE** (15)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-184"><span id="IETF"></span><span id="ietf"></span>**IETF** (16)</span><span class="sxs-lookup"><span data-stu-id="58a8e-184"><span id="IETF"></span><span id="ietf"></span>**IETF** (16)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-185"><span id="INCITS"></span><span id="incits"></span>**ИнЦитс** (17)</span><span class="sxs-lookup"><span data-stu-id="58a8e-185"><span id="INCITS"></span><span id="incits"></span>**INCITS** (17)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-186"><span id="ISO"></span><span id="iso"></span>**ISO** (18)</span><span class="sxs-lookup"><span data-stu-id="58a8e-186"><span id="ISO"></span><span id="iso"></span>**ISO** (18)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-187"><span id="W3C"></span><span id="w3c"></span>**W3C** (19)</span><span class="sxs-lookup"><span data-stu-id="58a8e-187"><span id="W3C"></span><span id="w3c"></span>**W3C** (19)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-188"><span id="__20___________OGF"></span><span id="__20___________ogf"></span>**20 ОГФ** (20)</span><span class="sxs-lookup"><span data-stu-id="58a8e-188"><span id="__20___________OGF"></span><span id="__20___________ogf"></span>**//20 OGF** (20)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-189"><span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**Зеленая сетка** (21)</span><span class="sxs-lookup"><span data-stu-id="58a8e-189"><span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**The Green Grid** (21)</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-190"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (..</span><span class="sxs-lookup"><span data-stu-id="58a8e-190"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="58a8e-191">)</span><span class="sxs-lookup"><span data-stu-id="58a8e-191">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="58a8e-192">**регистередверсион**</span><span class="sxs-lookup"><span data-stu-id="58a8e-192">**RegisteredVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58a8e-193">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58a8e-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58a8e-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58a8e-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58a8e-195">Версия этого профиля.</span><span class="sxs-lookup"><span data-stu-id="58a8e-195">The version of this profile.</span></span> <span data-ttu-id="58a8e-196">Строка должна иметь вид: "*M*. *N*. *U*"где:</span><span class="sxs-lookup"><span data-stu-id="58a8e-196">The string must be in the form: "*M*.*N*.*U*" Where:</span></span>

-   <span data-ttu-id="58a8e-197">*M* — основной номер версии (в числовом формате), описывающий создание или Последнее изменение профиля.</span><span class="sxs-lookup"><span data-stu-id="58a8e-197">*M* is the major version (in numeric form) describing the profile's creation or last modification.</span></span>
-   <span data-ttu-id="58a8e-198">*N* — это дополнительный номер версии (в числовом формате), описывающий создание или Последнее изменение профиля.</span><span class="sxs-lookup"><span data-stu-id="58a8e-198">*N* is the minor version (in numeric form) describing the profile's creation or last modification.</span></span>
-   <span data-ttu-id="58a8e-199">*U* — это обновление (в числовом формате), описывающее создание или Последнее изменение профиля.</span><span class="sxs-lookup"><span data-stu-id="58a8e-199">*U* is the update (in numeric form) describing the profile's creation or last modification.</span></span>

<span data-ttu-id="58a8e-200">Это свойство наследуется от [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58a8e-200">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="58a8e-201">Требования</span><span class="sxs-lookup"><span data-stu-id="58a8e-201">Requirements</span></span>



| <span data-ttu-id="58a8e-202">Требование</span><span class="sxs-lookup"><span data-stu-id="58a8e-202">Requirement</span></span> | <span data-ttu-id="58a8e-203">Значение</span><span class="sxs-lookup"><span data-stu-id="58a8e-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58a8e-204">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58a8e-204">Minimum supported client</span></span><br/> | <span data-ttu-id="58a8e-205">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="58a8e-205">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="58a8e-206">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58a8e-206">Minimum supported server</span></span><br/> | <span data-ttu-id="58a8e-207">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="58a8e-207">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="58a8e-208">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="58a8e-208">Namespace</span></span><br/>                | <span data-ttu-id="58a8e-209">Корневое \\ взаимодействие</span><span class="sxs-lookup"><span data-stu-id="58a8e-209">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="58a8e-210">MOF</span><span class="sxs-lookup"><span data-stu-id="58a8e-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58a8e-211"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58a8e-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="58a8e-212">DLL</span><span class="sxs-lookup"><span data-stu-id="58a8e-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58a8e-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="58a8e-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

