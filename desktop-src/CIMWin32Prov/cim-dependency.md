---
description: '\_Класс зависимостей CIM представляет ассоциацию, которая устанавливает отношения зависимости между объектами.'
ms.assetid: ff0d6b50-0920-443e-a984-e6a9ab4402b1
ms.tgt_platform: multiple
title: Класс CIM_Dependency (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Dependency
- CIM_Dependency.Antecedent
- CIM_Dependency.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b95d45efff51128b08dc5b6395309f49e85a79e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807523"
---
# <a name="cim_dependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="9bbcf-103">Класс CIM_Dependency (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="9bbcf-103">CIM_Dependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="9bbcf-104">Класс **\_ зависимостей CIM** представляет ассоциацию, которая устанавливает отношения зависимости между объектами.</span><span class="sxs-lookup"><span data-stu-id="9bbcf-104">The **CIM\_Dependency** class represents an association that establishes dependency relationships between objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9bbcf-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="9bbcf-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9bbcf-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9bbcf-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9bbcf-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="9bbcf-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9bbcf-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="9bbcf-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bbcf-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bbcf-109">Syntax</span></span>

``` syntax
[Association, Abstract, UUID("{8502C53A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Dependency
{
  CIM_ManagedSystemElement REF Antecedent;
  CIM_ManagedSystemElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="9bbcf-110">Члены</span><span class="sxs-lookup"><span data-stu-id="9bbcf-110">Members</span></span>

<span data-ttu-id="9bbcf-111">Класс **\_ зависимостей CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9bbcf-111">The **CIM\_Dependency** class has these types of members:</span></span>

-   [<span data-ttu-id="9bbcf-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="9bbcf-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9bbcf-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="9bbcf-113">Properties</span></span>

<span data-ttu-id="9bbcf-114">Класс **\_ зависимости CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="9bbcf-114">The **CIM\_Dependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9bbcf-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="9bbcf-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bbcf-116">Тип данных: **CIM \_ манажедсистемелемент**</span><span class="sxs-lookup"><span data-stu-id="9bbcf-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="9bbcf-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bbcf-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9bbcf-118">Ссылка на независимый объект в этой ассоциации.</span><span class="sxs-lookup"><span data-stu-id="9bbcf-118">Reference to the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="9bbcf-119">**Него**</span><span class="sxs-lookup"><span data-stu-id="9bbcf-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bbcf-120">Тип данных: **CIM \_ манажедсистемелемент**</span><span class="sxs-lookup"><span data-stu-id="9bbcf-120">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="9bbcf-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bbcf-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9bbcf-122">Ссылка на объект, который зависит от свойства **Antecedent** .</span><span class="sxs-lookup"><span data-stu-id="9bbcf-122">Reference to the object that is dependent on the **Antecedent** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9bbcf-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9bbcf-123">Remarks</span></span>

<span data-ttu-id="9bbcf-124">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="9bbcf-124">WMI does not implement this class.</span></span> <span data-ttu-id="9bbcf-125">Дополнительные сведения о классах, производных от **\_ зависимости CIM**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9bbcf-125">For more information about classes derived from **CIM\_Dependency**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9bbcf-126">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="9bbcf-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9bbcf-127">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="9bbcf-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bbcf-128">Требования</span><span class="sxs-lookup"><span data-stu-id="9bbcf-128">Requirements</span></span>



| <span data-ttu-id="9bbcf-129">Требование</span><span class="sxs-lookup"><span data-stu-id="9bbcf-129">Requirement</span></span> | <span data-ttu-id="9bbcf-130">Значение</span><span class="sxs-lookup"><span data-stu-id="9bbcf-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9bbcf-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9bbcf-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9bbcf-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9bbcf-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9bbcf-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9bbcf-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9bbcf-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9bbcf-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9bbcf-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9bbcf-135">Namespace</span></span><br/>                | <span data-ttu-id="9bbcf-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9bbcf-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9bbcf-137">MOF</span><span class="sxs-lookup"><span data-stu-id="9bbcf-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9bbcf-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9bbcf-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9bbcf-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9bbcf-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bbcf-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bbcf-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




