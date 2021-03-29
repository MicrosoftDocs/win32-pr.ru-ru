---
description: Объект CIM \_ коллектионофмсес позволяет группировать \_ объекты CIM манажедсистемелемент с целью связывания параметров и конфигураций. Он является абстрактным, чтобы требовать дальнейшего определения и семантического уточнения в подклассах.
ms.assetid: 9448a7a1-defc-4bac-9ce6-29ec2406d573
ms.tgt_platform: multiple
title: Класс CIM_CollectionOfMSEs (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.Caption
- CIM_CollectionOfMSEs.CollectionID
- CIM_CollectionOfMSEs.Description
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 57942dd6e00d819e4375ddd316e5e15126621b97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141941"
---
# <a name="cim_collectionofmses-class-cimwin32-wmi-providers"></a><span data-ttu-id="54c6e-104">Класс CIM_CollectionOfMSEs (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="54c6e-104">CIM_CollectionOfMSEs class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="54c6e-105">Объект **CIM \_ коллектионофмсес** позволяет группировать объекты [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md) с целью связывания параметров и конфигураций.</span><span class="sxs-lookup"><span data-stu-id="54c6e-105">The **CIM\_CollectionOfMSEs** object allows the grouping of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects for the purpose of associating settings and configurations.</span></span> <span data-ttu-id="54c6e-106">Он является абстрактным, чтобы требовать дальнейшего определения и семантического уточнения в подклассах.</span><span class="sxs-lookup"><span data-stu-id="54c6e-106">It is abstract to require further definition and semantic refinement in subclasses.</span></span>

<span data-ttu-id="54c6e-107">Объект **CIM \_ коллектионофмсес** не содержит сведений о состоянии или состоянии, но представляет только группирование элементов.</span><span class="sxs-lookup"><span data-stu-id="54c6e-107">The **CIM\_CollectionOfMSEs** object does not carry any state or status information, but only represents a grouping of elements.</span></span> <span data-ttu-id="54c6e-108">По этой причине нет нужды в отношении групп-подклассов, имеющих состояние или состояние от **CIM \_ коллектионофмсес**, примером является [**CIM \_ редунданциграуп**](cim-redundancygroup.md) (который правильно подклассировать из [**CIM \_ логикалелемент**](cim-logicalelement.md)).</span><span class="sxs-lookup"><span data-stu-id="54c6e-108">For this reason, it is incorrect to subclass groups that have state/status from **CIM\_CollectionOfMSEs**, An example is [**CIM\_RedundancyGroup**](cim-redundancygroup.md) (which is correctly subclassed from [**CIM\_LogicalElement**](cim-logicalelement.md)).</span></span> <span data-ttu-id="54c6e-109">Коллекции обычно выполняют статистическую обработку "Like" объектов и представляют собой оптимизацию.</span><span class="sxs-lookup"><span data-stu-id="54c6e-109">Collections typically aggregate 'like' objects, and represent an optimization.</span></span> <span data-ttu-id="54c6e-110">Без коллекций один из них вынужден определить отдельные ассоциации [**CIM \_ Елементсеттинг**](cim-elementsetting.md) и [**CIM \_ елементконфигуратион**](cim-elementconfiguration.md) , чтобы связать параметры и объекты конфигурации с отдельными [**CIM \_ манажедсистемелементс**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="54c6e-110">Without collections, one is forced to define individual [**CIM\_ElementSetting**](cim-elementsetting.md) and [**CIM\_ElementConfiguration**](cim-elementconfiguration.md) associations, to tie settings and configuration objects to individual [**CIM\_ManagedSystemElements**](cim-managedsystemelement.md).</span></span> <span data-ttu-id="54c6e-111">Назначение одного и того же параметра нескольким объектам может быть значительно дублирующимся.</span><span class="sxs-lookup"><span data-stu-id="54c6e-111">There may be much duplication in assigning the same setting to multiple objects.</span></span> <span data-ttu-id="54c6e-112">Кроме того, использование объекта Collection позволяет определить, что параметры и ассоциации конфигурации действительно одинаковы для элементов коллекции.</span><span class="sxs-lookup"><span data-stu-id="54c6e-112">In addition, using the collection object allows the determination that the setting and configuration associations are indeed the same for the collection's members.</span></span> <span data-ttu-id="54c6e-113">В противном случае эту информацию можно было бы получить, определив коллекцию особым образом, а затем запросив ассоциации **CIM \_ Елементсеттинг** и **CIM \_ елементконфигуратион** , чтобы определить, полностью ли охвачен набор сбора.</span><span class="sxs-lookup"><span data-stu-id="54c6e-113">This information would otherwise be obtained by defining the collection in a proprietary manner, and then querying the **CIM\_ElementSetting** and **CIM\_ElementConfiguration** associations to determine if the collection set is completely covered.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="54c6e-114">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="54c6e-114">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="54c6e-115">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="54c6e-115">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="54c6e-116">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="54c6e-116">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="54c6e-117">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="54c6e-117">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="54c6e-118">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54c6e-118">Syntax</span></span>

``` syntax
class CIM_CollectionOfMSEs
{
  string Caption;
  string CollectionID;
  string Description;
};
```

## <a name="members"></a><span data-ttu-id="54c6e-119">Члены</span><span class="sxs-lookup"><span data-stu-id="54c6e-119">Members</span></span>

<span data-ttu-id="54c6e-120">Класс **CIM \_ коллектионофмсес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="54c6e-120">The **CIM\_CollectionOfMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="54c6e-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="54c6e-121">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="54c6e-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="54c6e-122">Properties</span></span>

<span data-ttu-id="54c6e-123">Класс **CIM \_ коллектионофмсес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="54c6e-123">The **CIM\_CollectionOfMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="54c6e-124">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="54c6e-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c6e-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="54c6e-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54c6e-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54c6e-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54c6e-127">Краткое текстовое описание объекта Коллектионофмсес.</span><span class="sxs-lookup"><span data-stu-id="54c6e-127">Short textual description of the CollectionOfMSEs object.</span></span>

</dd> <dt>

<span data-ttu-id="54c6e-128">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="54c6e-128">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c6e-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="54c6e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54c6e-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54c6e-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54c6e-131">Идентификация объекта коллекции.</span><span class="sxs-lookup"><span data-stu-id="54c6e-131">Identification of the Collection object.</span></span> <span data-ttu-id="54c6e-132">При создании подкласса свойство CollectionID может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="54c6e-132">When subclassed, the CollectionID property can be overridden to be a Key property.</span></span>

</dd> <dt>

<span data-ttu-id="54c6e-133">**Описание**</span><span class="sxs-lookup"><span data-stu-id="54c6e-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54c6e-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="54c6e-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54c6e-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54c6e-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54c6e-136">Текстовое описание объекта Коллектионофмсес.</span><span class="sxs-lookup"><span data-stu-id="54c6e-136">Textual description of the CollectionOfMSEs object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54c6e-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54c6e-137">Remarks</span></span>

<span data-ttu-id="54c6e-138">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="54c6e-138">WMI does not implement this class.</span></span> <span data-ttu-id="54c6e-139">См. раздел [Классы Win32](win32-provider.md) для классов WMI, производных от **CIM \_ коллектионофмсес**.</span><span class="sxs-lookup"><span data-stu-id="54c6e-139">See [Win32 Classes](win32-provider.md) for WMI classes derived from **CIM\_CollectionOfMSEs**.</span></span>

<span data-ttu-id="54c6e-140">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="54c6e-140">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="54c6e-141">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="54c6e-141">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="54c6e-142">Требования</span><span class="sxs-lookup"><span data-stu-id="54c6e-142">Requirements</span></span>



| <span data-ttu-id="54c6e-143">Требование</span><span class="sxs-lookup"><span data-stu-id="54c6e-143">Requirement</span></span> | <span data-ttu-id="54c6e-144">Значение</span><span class="sxs-lookup"><span data-stu-id="54c6e-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54c6e-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54c6e-145">Minimum supported client</span></span><br/> | <span data-ttu-id="54c6e-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54c6e-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="54c6e-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54c6e-147">Minimum supported server</span></span><br/> | <span data-ttu-id="54c6e-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54c6e-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="54c6e-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="54c6e-149">Namespace</span></span><br/>                | <span data-ttu-id="54c6e-150">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="54c6e-150">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="54c6e-151">MOF</span><span class="sxs-lookup"><span data-stu-id="54c6e-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54c6e-152"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54c6e-152"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="54c6e-153">DLL</span><span class="sxs-lookup"><span data-stu-id="54c6e-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54c6e-154"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54c6e-154"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




