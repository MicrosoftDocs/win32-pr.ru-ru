---
description: '\_Ассоциация компонента CIM представляет части связи между мсес.'
ms.assetid: a074e2f7-b092-4d3c-be5e-2069b643431b
ms.tgt_platform: multiple
title: Класс CIM_Component (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Component
- CIM_Component.GroupComponent
- CIM_Component.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b516118bc0cd6f12285933b1c15e7f2801ad40d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896105"
---
# <a name="cim_component-class-cimwin32-wmi-providers"></a><span data-ttu-id="01e83-103">Класс CIM_Component (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="01e83-103">CIM_Component class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="01e83-104">Ассоциация **\_ компонента CIM** представляет части связи между мсес.</span><span class="sxs-lookup"><span data-stu-id="01e83-104">The **CIM\_Component** association represents the parts of a relationship between MSEs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01e83-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="01e83-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="01e83-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="01e83-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="01e83-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="01e83-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="01e83-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="01e83-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="01e83-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01e83-109">Syntax</span></span>

``` syntax
[Association, Abstract, Aggregation, UUID("{8502C573-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="01e83-110">Члены</span><span class="sxs-lookup"><span data-stu-id="01e83-110">Members</span></span>

<span data-ttu-id="01e83-111">Класс **\_ компонента CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="01e83-111">The **CIM\_Component** class has these types of members:</span></span>

-   [<span data-ttu-id="01e83-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="01e83-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01e83-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="01e83-113">Properties</span></span>

<span data-ttu-id="01e83-114">Класс **\_ компонента CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="01e83-114">The **CIM\_Component** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01e83-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="01e83-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e83-116">Тип данных: **CIM \_ манажедсистемелемент**</span><span class="sxs-lookup"><span data-stu-id="01e83-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="01e83-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="01e83-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e83-118">Квалификаторы: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="01e83-118">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="01e83-119">[**\_ Манажедсистемелемент CIM**](cim-managedsystemelement.md) , описывающий родительский элемент в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="01e83-119">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="01e83-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="01e83-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e83-121">Тип данных: **CIM \_ манажедсистемелемент**</span><span class="sxs-lookup"><span data-stu-id="01e83-121">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="01e83-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="01e83-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01e83-123">[**\_ Манажедсистемелемент CIM**](cim-managedsystemelement.md) , описывающий дочерний элемент в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="01e83-123">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element in the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01e83-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01e83-124">Remarks</span></span>

<span data-ttu-id="01e83-125">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="01e83-125">WMI does not implement this class.</span></span> <span data-ttu-id="01e83-126">Дополнительные сведения о классах, производных от **\_ компонента CIM**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="01e83-126">For more information about classes derived from **CIM\_Component**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="01e83-127">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="01e83-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="01e83-128">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="01e83-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="01e83-129">Требования</span><span class="sxs-lookup"><span data-stu-id="01e83-129">Requirements</span></span>



| <span data-ttu-id="01e83-130">Требование</span><span class="sxs-lookup"><span data-stu-id="01e83-130">Requirement</span></span> | <span data-ttu-id="01e83-131">Значение</span><span class="sxs-lookup"><span data-stu-id="01e83-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01e83-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01e83-132">Minimum supported client</span></span><br/> | <span data-ttu-id="01e83-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01e83-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01e83-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01e83-134">Minimum supported server</span></span><br/> | <span data-ttu-id="01e83-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01e83-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01e83-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="01e83-136">Namespace</span></span><br/>                | <span data-ttu-id="01e83-137">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="01e83-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="01e83-138">MOF</span><span class="sxs-lookup"><span data-stu-id="01e83-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01e83-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01e83-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="01e83-140">DLL</span><span class="sxs-lookup"><span data-stu-id="01e83-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01e83-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01e83-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

