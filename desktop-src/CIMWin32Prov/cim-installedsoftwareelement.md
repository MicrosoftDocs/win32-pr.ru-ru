---
description: Класс CIM \_ инсталледсофтварилемент связывает компьютерную систему с установленным программным элементом.
ms.assetid: b9a570ed-b4e0-4f73-82e3-6d2bd1708e16
ms.tgt_platform: multiple
title: Класс CIM_InstalledSoftwareElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InstalledSoftwareElement
- CIM_InstalledSoftwareElement.Software
- CIM_InstalledSoftwareElement.System
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd082477b2e2ba194163784b74883872b1edb6a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141716"
---
# <a name="cim_installedsoftwareelement-class"></a><span data-ttu-id="8c661-103">\_Класс CIM инсталледсофтварилемент</span><span class="sxs-lookup"><span data-stu-id="8c661-103">CIM\_InstalledSoftwareElement class</span></span>

<span data-ttu-id="8c661-104">Класс **CIM \_ инсталледсофтварилемент** связывает компьютерную систему с установленным программным элементом.</span><span class="sxs-lookup"><span data-stu-id="8c661-104">The **CIM\_InstalledSoftwareElement** class associates a computer system with an installed software element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8c661-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="8c661-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8c661-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8c661-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8c661-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="8c661-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8c661-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="8c661-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c661-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c661-109">Syntax</span></span>

``` syntax
[UUID("{A7B05028-DB2A-11d2-85FC-0000F8102E5F}"), Association, Abstract, AMENDMENT]
class CIM_InstalledSoftwareElement
{
  CIM_SoftwareElement REF Software;
  CIM_ComputerSystem  REF System;
};
```

## <a name="members"></a><span data-ttu-id="8c661-110">Члены</span><span class="sxs-lookup"><span data-stu-id="8c661-110">Members</span></span>

<span data-ttu-id="8c661-111">Класс **CIM \_ инсталледсофтварилемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8c661-111">The **CIM\_InstalledSoftwareElement** class has these types of members:</span></span>

-   [<span data-ttu-id="8c661-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="8c661-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c661-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="8c661-113">Properties</span></span>

<span data-ttu-id="8c661-114">Класс **CIM \_ инсталледсофтварилемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8c661-114">The **CIM\_InstalledSoftwareElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8c661-115">**Программное обеспечение**.</span><span class="sxs-lookup"><span data-stu-id="8c661-115">**Software**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c661-116">Тип данных: **CIM \_ софтварилемент**</span><span class="sxs-lookup"><span data-stu-id="8c661-116">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="8c661-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8c661-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c661-118">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false)</span><span class="sxs-lookup"><span data-stu-id="8c661-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE)</span></span>
</dt> </dl>

<span data-ttu-id="8c661-119">Ссылка на программный элемент, установленный в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="8c661-119">Reference to the software element that is installed on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="8c661-120">**Система**</span><span class="sxs-lookup"><span data-stu-id="8c661-120">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c661-121">Тип данных: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="8c661-121">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="8c661-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8c661-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c661-123">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false)</span><span class="sxs-lookup"><span data-stu-id="8c661-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE)</span></span>
</dt> </dl>

<span data-ttu-id="8c661-124">Ссылка на компьютерную систему, на которой размещен определенный программный элемент.</span><span class="sxs-lookup"><span data-stu-id="8c661-124">Reference to the computer system hosting a particular software element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c661-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c661-125">Remarks</span></span>

<span data-ttu-id="8c661-126">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="8c661-126">WMI does not implement this class.</span></span> <span data-ttu-id="8c661-127">Классы, производные от **CIM \_ инсталледсофтварилемент**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8c661-127">For classes derived from **CIM\_InstalledSoftwareElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="8c661-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="8c661-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8c661-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="8c661-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c661-130">Требования</span><span class="sxs-lookup"><span data-stu-id="8c661-130">Requirements</span></span>



| <span data-ttu-id="8c661-131">Требование</span><span class="sxs-lookup"><span data-stu-id="8c661-131">Requirement</span></span> | <span data-ttu-id="8c661-132">Значение</span><span class="sxs-lookup"><span data-stu-id="8c661-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c661-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c661-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8c661-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c661-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8c661-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c661-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8c661-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c661-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8c661-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8c661-137">Namespace</span></span><br/>                | <span data-ttu-id="8c661-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8c661-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8c661-139">MOF</span><span class="sxs-lookup"><span data-stu-id="8c661-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c661-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c661-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c661-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8c661-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c661-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c661-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

