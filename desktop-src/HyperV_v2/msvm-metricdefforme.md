---
description: Определяет связь между \_ Басеметрикдефинитион мсвм и CIM \_ манажеделемент для определения метрик для второго. Определение метрик задается контекстом Манажеделемент, поэтому определение зависит от элемента.
ms.assetid: 528d9b1a-089d-48ae-b5a6-40bc9d09191c
title: Класс Msvm_MetricDefForME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricDefForME
- Msvm_MetricDefForME.Antecedent
- Msvm_MetricDefForME.Dependent
- Msvm_MetricDefForME.MetricCollectionEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: afd5146e3b1222b2b0febbcb098c24d53c22f85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663072"
---
# <a name="msvm_metricdefforme-class"></a><span data-ttu-id="d2921-104">\_Класс мсвм метрикдефформе</span><span class="sxs-lookup"><span data-stu-id="d2921-104">Msvm\_MetricDefForME class</span></span>

<span data-ttu-id="d2921-105">Определяет связь между [**\_ басеметрикдефинитион Мсвм**](msvm-basemetricdefinition.md) и [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) для определения метрик для второго.</span><span class="sxs-lookup"><span data-stu-id="d2921-105">Defines the association between an [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) and a [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) to define metrics for the latter.</span></span> <span data-ttu-id="d2921-106">Определение метрик задается контекстом Манажеделемент, поэтому определение зависит от элемента.</span><span class="sxs-lookup"><span data-stu-id="d2921-106">The metrics definition is given context by the ManagedElement, which is why the definition is dependent on the element.</span></span>

<span data-ttu-id="d2921-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d2921-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2921-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2921-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricDefForME : CIM_MetricDefForME
{
  CIM_ManagedElement       REF Antecedent;
  CIM_BaseMetricDefinition REF Dependent;
  uint16                       MetricCollectionEnabled = 2;
};
```

## <a name="members"></a><span data-ttu-id="d2921-109">Члены</span><span class="sxs-lookup"><span data-stu-id="d2921-109">Members</span></span>

<span data-ttu-id="d2921-110">Класс **мсвм \_ метрикдефформе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d2921-110">The **Msvm\_MetricDefForME** class has these types of members:</span></span>

-   [<span data-ttu-id="d2921-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="d2921-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d2921-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="d2921-112">Properties</span></span>

<span data-ttu-id="d2921-113">Класс **мсвм \_ метрикдефформе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d2921-113">The **Msvm\_MetricDefForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d2921-114">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="d2921-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2921-115">Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="d2921-115">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="d2921-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d2921-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2921-117">Ссылка на экземпляр класса [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) , представляющий управляемый элемент, который может иметь метрики типа, определенные **зависимым от** него.</span><span class="sxs-lookup"><span data-stu-id="d2921-117">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the managed element that can have metrics of the type defined by **Dependent** applied to it.</span></span> <span data-ttu-id="d2921-118">Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="d2921-118">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="d2921-119">**Него**</span><span class="sxs-lookup"><span data-stu-id="d2921-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2921-120">Тип данных: **[ **CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="d2921-120">Data type: **[**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="d2921-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d2921-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2921-122">Ссылка на экземпляр класса [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) , представляющий определение метрики, к которому может быть применена **предшествующая задача** .</span><span class="sxs-lookup"><span data-stu-id="d2921-122">A reference to an instance of the [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the metric definition that the **Antecedent** can have applied to it.</span></span> <span data-ttu-id="d2921-123">Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="d2921-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="d2921-124">**метрикколлектионенаблед**</span><span class="sxs-lookup"><span data-stu-id="d2921-124">**MetricCollectionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2921-125">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2921-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2921-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d2921-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2921-127">Указывает, собираются ли метрики, определенные **зависимыми** , для **предшествующей задачи**.</span><span class="sxs-lookup"><span data-stu-id="d2921-127">Indicates whether the metric defined by **Dependent** is being collected for the **Antecedent**.</span></span> <span data-ttu-id="d2921-128">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d2921-128">This will be one of the following values.</span></span>



| <span data-ttu-id="d2921-129">Значение</span><span class="sxs-lookup"><span data-stu-id="d2921-129">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="d2921-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d2921-130">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="d2921-131"><dt>**Включено**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d2921-131"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                         | <span data-ttu-id="d2921-132">Метрика собирается.</span><span class="sxs-lookup"><span data-stu-id="d2921-132">The metric is being collected.</span></span><br/>                                |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="d2921-133"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d2921-133"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                     | <span data-ttu-id="d2921-134">Метрика не собирается.</span><span class="sxs-lookup"><span data-stu-id="d2921-134">The metric is not being collected.</span></span><br/>                            |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <span data-ttu-id="d2921-135"><dt>**Зарезервировано**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d2921-135"><dt>**Reserved**</dt> <dt>4</dt></span></span> </dl>                                     |                                                                          |
| <span id="PartiallyEnabled"></span><span id="partiallyenabled"></span><span id="PARTIALLYENABLED"></span><dl> <span data-ttu-id="d2921-136"><dt>**Партиалленаблед**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="d2921-136"><dt>**PartiallyEnabled**</dt> <dt>32768</dt></span></span> </dl> | <span data-ttu-id="d2921-137">Метрика собирается для некоторых, но не для всех устройств.</span><span class="sxs-lookup"><span data-stu-id="d2921-137">The metric is being collected for some, but not all, devices.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2921-138">Требования</span><span class="sxs-lookup"><span data-stu-id="d2921-138">Requirements</span></span>



| <span data-ttu-id="d2921-139">Требование</span><span class="sxs-lookup"><span data-stu-id="d2921-139">Requirement</span></span> | <span data-ttu-id="d2921-140">Значение</span><span class="sxs-lookup"><span data-stu-id="d2921-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2921-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d2921-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d2921-142">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d2921-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d2921-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d2921-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d2921-144">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d2921-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d2921-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d2921-145">Namespace</span></span><br/>                | <span data-ttu-id="d2921-146">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d2921-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d2921-147">MOF</span><span class="sxs-lookup"><span data-stu-id="d2921-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2921-148"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2921-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2921-149">DLL</span><span class="sxs-lookup"><span data-stu-id="d2921-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2921-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d2921-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

