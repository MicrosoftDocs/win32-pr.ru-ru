---
description: Отношение CIM \_ депенденциконтекст связывает \_ класс зависимостей CIM с одним или несколькими \_ объектами конфигурации CIM. Например, зависимости компьютера могут изменяться в зависимости от сети, к которой подключена система.
ms.assetid: 9f35fc41-1bfa-4018-a54c-64c875c710d4
ms.tgt_platform: multiple
title: Класс CIM_DependencyContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DependencyContext
- CIM_DependencyContext.Context
- CIM_DependencyContext.Dependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 69319a4f4d228d484da62411060ae3fead90bb79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896038"
---
# <a name="cim_dependencycontext-class"></a><span data-ttu-id="184af-104">\_Класс CIM депенденциконтекст</span><span class="sxs-lookup"><span data-stu-id="184af-104">CIM\_DependencyContext class</span></span>

<span data-ttu-id="184af-105">Отношение **CIM \_ депенденциконтекст** связывает класс [**\_ зависимостей CIM**](cim-dependency.md) с одним или несколькими объектами [**\_ конфигурации CIM**](cim-configuration.md) .</span><span class="sxs-lookup"><span data-stu-id="184af-105">The **CIM\_DependencyContext** relationship associates a [**CIM\_Dependency**](cim-dependency.md) class with one or more [**CIM\_Configuration**](cim-configuration.md) objects.</span></span> <span data-ttu-id="184af-106">Например, зависимости компьютера могут изменяться в зависимости от сети, к которой подключена система.</span><span class="sxs-lookup"><span data-stu-id="184af-106">For example, a computer system's dependencies can change based on the network to which the system is attached.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="184af-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="184af-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="184af-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="184af-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="184af-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="184af-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="184af-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="184af-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="184af-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="184af-111">Syntax</span></span>

``` syntax
[Abstract, Aggregation, Association, UUID("{A228E208-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DependencyContext
{
  CIM_Configuration REF Context;
  CIM_Dependency    REF Dependency;
};
```

## <a name="members"></a><span data-ttu-id="184af-112">Члены</span><span class="sxs-lookup"><span data-stu-id="184af-112">Members</span></span>

<span data-ttu-id="184af-113">Класс **CIM \_ депенденциконтекст** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="184af-113">The **CIM\_DependencyContext** class has these types of members:</span></span>

-   [<span data-ttu-id="184af-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="184af-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="184af-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="184af-115">Properties</span></span>

<span data-ttu-id="184af-116">Класс **CIM \_ депенденциконтекст** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="184af-116">The **CIM\_DependencyContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="184af-117">**Контекст**</span><span class="sxs-lookup"><span data-stu-id="184af-117">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="184af-118">Тип данных: **\_ Конфигурация CIM**</span><span class="sxs-lookup"><span data-stu-id="184af-118">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="184af-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="184af-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="184af-120">Квалификаторы: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="184af-120">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="184af-121">Ссылка на объект конфигурации, который выполняет статистическую обработку зависимости.</span><span class="sxs-lookup"><span data-stu-id="184af-121">Reference to the configuration object that aggregates the dependency.</span></span>

</dd> <dt>

<span data-ttu-id="184af-122">**Зависимость**</span><span class="sxs-lookup"><span data-stu-id="184af-122">**Dependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="184af-123">Тип данных: **\_ зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="184af-123">Data type: **CIM\_Dependency**</span></span>
</dt> <dt>

<span data-ttu-id="184af-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="184af-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="184af-125">Ссылка на агрегированную зависимость.</span><span class="sxs-lookup"><span data-stu-id="184af-125">Reference to an aggregated dependency.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="184af-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="184af-126">Remarks</span></span>

<span data-ttu-id="184af-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="184af-127">WMI does not implement this class.</span></span>

<span data-ttu-id="184af-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="184af-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="184af-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="184af-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="184af-130">Требования</span><span class="sxs-lookup"><span data-stu-id="184af-130">Requirements</span></span>



| <span data-ttu-id="184af-131">Требование</span><span class="sxs-lookup"><span data-stu-id="184af-131">Requirement</span></span> | <span data-ttu-id="184af-132">Значение</span><span class="sxs-lookup"><span data-stu-id="184af-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="184af-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="184af-133">Minimum supported client</span></span><br/> | <span data-ttu-id="184af-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="184af-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="184af-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="184af-135">Minimum supported server</span></span><br/> | <span data-ttu-id="184af-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="184af-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="184af-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="184af-137">Namespace</span></span><br/>                | <span data-ttu-id="184af-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="184af-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="184af-139">MOF</span><span class="sxs-lookup"><span data-stu-id="184af-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="184af-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="184af-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="184af-141">DLL</span><span class="sxs-lookup"><span data-stu-id="184af-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="184af-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="184af-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

