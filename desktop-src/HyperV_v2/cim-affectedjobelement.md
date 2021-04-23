---
description: Представляет связь между заданием и \_ объектами CIM манажеделемент, на которые может повлиять выполнение.
ms.assetid: 94c5e602-214c-4003-921c-8955c3859738
title: Класс CIM_AffectedJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AffectedJobElement
- CIM_AffectedJobElement.AffectedElement
- CIM_AffectedJobElement.AffectingElement
- CIM_AffectedJobElement.ElementEffects
- CIM_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 830e798ff12dc87c88126375736f116c044de731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156062"
---
# <a name="cim_affectedjobelement-class"></a><span data-ttu-id="f56f6-103">\_Класс CIM аффектеджобелемент</span><span class="sxs-lookup"><span data-stu-id="f56f6-103">CIM\_AffectedJobElement class</span></span>

<span data-ttu-id="f56f6-104">Представляет связь между заданием и объектами **CIM \_ манажеделемент** , на которые может повлиять выполнение.</span><span class="sxs-lookup"><span data-stu-id="f56f6-104">Represents an association between a job and the **CIM\_ManagedElement** objects that may be affected by its execution.</span></span> <span data-ttu-id="f56f6-105">В задании может быть нецелесообразно описать все затронутые элементы.</span><span class="sxs-lookup"><span data-stu-id="f56f6-105">It may not be feasible for the job to describe all of the affected elements.</span></span> <span data-ttu-id="f56f6-106">Основной целью этой ассоциации является предоставление информации, когда заданию требуется эксклюзивное использование затронутых управляемых элементов или описание побочных эффектов, которые могут возникнуть.</span><span class="sxs-lookup"><span data-stu-id="f56f6-106">The main purpose of this association is to provide information when a job requires exclusive use of the affected managed elements or when describing the side effects that may result.</span></span>

## <a name="syntax"></a><span data-ttu-id="f56f6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f56f6-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.15.0"), UMLPackagePath("CIM::System::Processing"), AMENDMENT]
class CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Job            REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="f56f6-108">Члены</span><span class="sxs-lookup"><span data-stu-id="f56f6-108">Members</span></span>

<span data-ttu-id="f56f6-109">Класс **CIM \_ аффектеджобелемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f56f6-109">The **CIM\_AffectedJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="f56f6-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f56f6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f56f6-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="f56f6-111">Properties</span></span>

<span data-ttu-id="f56f6-112">Класс **CIM \_ аффектеджобелемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f56f6-112">The **CIM\_AffectedJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f56f6-113">**аффектеделемент**</span><span class="sxs-lookup"><span data-stu-id="f56f6-113">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56f6-114">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="f56f6-114">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="f56f6-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f56f6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f56f6-116">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f56f6-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f56f6-117">Управляемый элемент, затронутый выполнением задания.</span><span class="sxs-lookup"><span data-stu-id="f56f6-117">The managed element affected by the execution of the job.</span></span>

</dd> <dt>

<span data-ttu-id="f56f6-118">**аффектинжелемент**</span><span class="sxs-lookup"><span data-stu-id="f56f6-118">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56f6-119">Тип данных: **\_ Задание CIM** .</span><span class="sxs-lookup"><span data-stu-id="f56f6-119">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="f56f6-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f56f6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f56f6-121">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f56f6-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f56f6-122">Задание, влияющее на управляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="f56f6-122">The job that is affecting the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="f56f6-123">**елементеффектс**</span><span class="sxs-lookup"><span data-stu-id="f56f6-123">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56f6-124">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="f56f6-124">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f56f6-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f56f6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f56f6-126">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ аффектеджобелемент**.**Осерелементеффектсдескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="f56f6-126">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AffectedJobElement**.**OtherElementEffectsDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="f56f6-127">Воздействие задания на управляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="f56f6-127">The effect the job has on the managed element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f56f6-128">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f56f6-128">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f56f6-129">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f56f6-129">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

<span data-ttu-id="f56f6-130">**Эксклюзивное использование** (2)</span><span class="sxs-lookup"><span data-stu-id="f56f6-130">**Exclusive Use** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

<span data-ttu-id="f56f6-131">**Влияние на производительность** (3)</span><span class="sxs-lookup"><span data-stu-id="f56f6-131">**Performance Impact** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

<span data-ttu-id="f56f6-132">**Целостность элементов** (4)</span><span class="sxs-lookup"><span data-stu-id="f56f6-132">**Element Integrity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="f56f6-133">**CREATE** (5)</span><span class="sxs-lookup"><span data-stu-id="f56f6-133">**Create** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f56f6-134">**осерелементеффектсдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="f56f6-134">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56f6-135">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="f56f6-135">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f56f6-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f56f6-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f56f6-137">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ аффектеджобелемент**.**Елементеффектс**")</span><span class="sxs-lookup"><span data-stu-id="f56f6-137">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AffectedJobElement**.**ElementEffects**")</span></span>
</dt> </dl>

<span data-ttu-id="f56f6-138">Дополнительные сведения для соответствующих значений "1" (другие) в массиве **елементеффектс** .</span><span class="sxs-lookup"><span data-stu-id="f56f6-138">Additional details for corresponding "1" (Other) values in the **ElementEffects** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f56f6-139">Требования</span><span class="sxs-lookup"><span data-stu-id="f56f6-139">Requirements</span></span>



| <span data-ttu-id="f56f6-140">Требование</span><span class="sxs-lookup"><span data-stu-id="f56f6-140">Requirement</span></span> | <span data-ttu-id="f56f6-141">Значение</span><span class="sxs-lookup"><span data-stu-id="f56f6-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f56f6-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f56f6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f56f6-143">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f56f6-143">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f56f6-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f56f6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f56f6-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f56f6-145">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f56f6-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f56f6-146">Namespace</span></span><br/>                | <span data-ttu-id="f56f6-147">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f56f6-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f56f6-148">MOF</span><span class="sxs-lookup"><span data-stu-id="f56f6-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f56f6-149"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f56f6-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f56f6-150">DLL</span><span class="sxs-lookup"><span data-stu-id="f56f6-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f56f6-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f56f6-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

