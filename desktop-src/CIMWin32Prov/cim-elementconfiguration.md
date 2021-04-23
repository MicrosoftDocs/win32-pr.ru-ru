---
description: Ассоциация CIM \_ елементконфигуратион связывает \_ объект конфигурации CIM с одним или несколькими управляемыми системными элементами. \_Объект конфигурации CIM представляет определенное поведение или требуемое функциональное состояние для связанного \_ манажедсистемелемент CIM.
ms.assetid: 4d2af009-7466-4394-af42-72c8d96e0786
ms.tgt_platform: multiple
title: Класс CIM_ElementConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConfiguration
- CIM_ElementConfiguration.Configuration
- CIM_ElementConfiguration.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7707338a3c2268cba51146aa8462b3b244b149ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072468"
---
# <a name="cim_elementconfiguration-class"></a><span data-ttu-id="c9478-104">\_Класс CIM елементконфигуратион</span><span class="sxs-lookup"><span data-stu-id="c9478-104">CIM\_ElementConfiguration class</span></span>

<span data-ttu-id="c9478-105">Ассоциация **CIM \_ елементконфигуратион** связывает объект [**\_ конфигурации CIM**](cim-configuration.md) с одним или несколькими управляемыми системными элементами.</span><span class="sxs-lookup"><span data-stu-id="c9478-105">The **CIM\_ElementConfiguration** association relates a [**CIM\_Configuration**](cim-configuration.md) object to one or more managed system elements.</span></span> <span data-ttu-id="c9478-106">Объект **\_ конфигурации CIM** представляет определенное поведение или требуемое функциональное состояние для связанного [**\_ манажедсистемелемент CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c9478-106">The **CIM\_Configuration** object represents a certain behavior, or a desired functional state for the associated [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c9478-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="c9478-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c9478-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c9478-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c9478-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c9478-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c9478-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="c9478-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9478-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9478-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FC049DCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ElementConfiguration
{
  CIM_Configuration        REF Configuration;
  CIM_ManagedSystemElement REF Element;
};
```

## <a name="members"></a><span data-ttu-id="c9478-112">Члены</span><span class="sxs-lookup"><span data-stu-id="c9478-112">Members</span></span>

<span data-ttu-id="c9478-113">Класс **CIM \_ елементконфигуратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c9478-113">The **CIM\_ElementConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="c9478-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="c9478-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9478-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="c9478-115">Properties</span></span>

<span data-ttu-id="c9478-116">Класс **CIM \_ елементконфигуратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c9478-116">The **CIM\_ElementConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9478-117">**Конфигурация**</span><span class="sxs-lookup"><span data-stu-id="c9478-117">**Configuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9478-118">Тип данных: **\_ Конфигурация CIM**</span><span class="sxs-lookup"><span data-stu-id="c9478-118">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="c9478-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c9478-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9478-120">Ссылка на объект [**\_ конфигурации CIM**](cim-configuration.md) , который группирует параметры и зависимости, связанные с управляемым элементом System.</span><span class="sxs-lookup"><span data-stu-id="c9478-120">Reference to the [**CIM\_Configuration**](cim-configuration.md) object that groups the settings and dependencies associated with the managed system element.</span></span>

</dd> <dt>

<span data-ttu-id="c9478-121">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c9478-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9478-122">Тип данных: **CIM \_ манажедсистемелемент**</span><span class="sxs-lookup"><span data-stu-id="c9478-122">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="c9478-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c9478-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9478-124">Ссылка на управляемый системный элемент.</span><span class="sxs-lookup"><span data-stu-id="c9478-124">Reference to the managed system element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9478-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9478-125">Remarks</span></span>

<span data-ttu-id="c9478-126">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="c9478-126">WMI does not implement this class.</span></span>

<span data-ttu-id="c9478-127">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="c9478-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c9478-128">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="c9478-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9478-129">Требования</span><span class="sxs-lookup"><span data-stu-id="c9478-129">Requirements</span></span>



| <span data-ttu-id="c9478-130">Требование</span><span class="sxs-lookup"><span data-stu-id="c9478-130">Requirement</span></span> | <span data-ttu-id="c9478-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c9478-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9478-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9478-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c9478-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9478-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c9478-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9478-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c9478-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9478-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c9478-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c9478-136">Namespace</span></span><br/>                | <span data-ttu-id="c9478-137">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c9478-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c9478-138">MOF</span><span class="sxs-lookup"><span data-stu-id="c9478-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9478-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9478-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9478-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c9478-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9478-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9478-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




