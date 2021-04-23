---
description: Класс CIM \_ хостедбутсап определяет размещение единой компьютерной системы для \_ класса CIM бутсап.
ms.assetid: 2113de13-e7af-4a1c-ba80-27e2c57af8a0
ms.tgt_platform: multiple
title: Класс CIM_HostedBootSAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootSAP
- CIM_HostedBootSAP.Dependent
- CIM_HostedBootSAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12e801f420ca2c56cc8960175391cdd9a669a00d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990589"
---
# <a name="cim_hostedbootsap-class"></a><span data-ttu-id="9d179-103">\_Класс CIM хостедбутсап</span><span class="sxs-lookup"><span data-stu-id="9d179-103">CIM\_HostedBootSAP class</span></span>

<span data-ttu-id="9d179-104">Класс **CIM \_ хостедбутсап** определяет размещение единой компьютерной системы для класса [**CIM \_ бутсап**](cim-bootsap.md) .</span><span class="sxs-lookup"><span data-stu-id="9d179-104">The **CIM\_HostedBootSAP** class defines the hosting unitary computer system for a [**CIM\_BootSAP**](cim-bootsap.md) class.</span></span> <span data-ttu-id="9d179-105">Так как эта связь является подклассом из [**CIM \_ хостедакцесспоинт**](cim-hostedaccesspoint.md), она наследует схему определения области и именования, определенную для [**CIM \_ сервицеакцесспоинт**](cim-serviceaccesspoint.md), где точка доступа откладывается на ее систему размещения.</span><span class="sxs-lookup"><span data-stu-id="9d179-105">Since this relationship is subclassed from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md), it inherits the scoping/naming scheme defined for [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md), where an access point defers to its hosting system.</span></span> <span data-ttu-id="9d179-106">В этом случае **CIM \_ бутсап** должен откладываться на класс [**CIM \_ унитарикомпутерсистем**](cim-unitarycomputersystem.md) размещения.</span><span class="sxs-lookup"><span data-stu-id="9d179-106">In this case, **CIM\_BootSAP** must defer to its hosting [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9d179-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="9d179-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9d179-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9d179-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9d179-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="9d179-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9d179-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="9d179-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d179-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d179-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{625B4512-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootSAP : CIM_HostedAccessPoint
{
  CIM_BootSAP               REF Dependent;
  CIM_UnitaryComputerSystem REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="9d179-112">Члены</span><span class="sxs-lookup"><span data-stu-id="9d179-112">Members</span></span>

<span data-ttu-id="9d179-113">Класс **CIM \_ хостедбутсап** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9d179-113">The **CIM\_HostedBootSAP** class has these types of members:</span></span>

-   [<span data-ttu-id="9d179-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="9d179-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d179-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="9d179-115">Properties</span></span>

<span data-ttu-id="9d179-116">Класс **CIM \_ хостедбутсап** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9d179-116">The **CIM\_HostedBootSAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d179-117">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="9d179-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d179-118">Тип данных: **CIM \_ унитарикомпутерсистем**</span><span class="sxs-lookup"><span data-stu-id="9d179-118">Data type: **CIM\_UnitaryComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="9d179-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d179-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d179-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="9d179-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="9d179-121">[**\_ Унитарикомпутерсистем CIM**](cim-unitarycomputersystem.md) , описывающий единую компьютерную систему.</span><span class="sxs-lookup"><span data-stu-id="9d179-121">A [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) that describes the unitary computer system.</span></span>

</dd> <dt>

<span data-ttu-id="9d179-122">**Него**</span><span class="sxs-lookup"><span data-stu-id="9d179-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d179-123">Тип данных: **CIM \_ бутсап**</span><span class="sxs-lookup"><span data-stu-id="9d179-123">Data type: **CIM\_BootSAP**</span></span>
</dt> <dt>

<span data-ttu-id="9d179-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d179-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d179-125">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="9d179-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="9d179-126">[**\_ Бутсап CIM**](cim-bootsap.md) , описывающий загрузочную систему SAP, размещенную на единой компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="9d179-126">A [**CIM\_BootSAP**](cim-bootsap.md) that describes the Boot SAP hosted on the unitary computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d179-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d179-127">Remarks</span></span>

<span data-ttu-id="9d179-128">Класс **CIM \_ хостедбутсап** является производным от [**CIM \_ хостедакцесспоинт**](cim-hostedaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="9d179-128">The **CIM\_HostedBootSAP** class is derived from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md).</span></span>

<span data-ttu-id="9d179-129">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="9d179-129">WMI does not implement this class.</span></span>

<span data-ttu-id="9d179-130">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="9d179-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9d179-131">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="9d179-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d179-132">Требования</span><span class="sxs-lookup"><span data-stu-id="9d179-132">Requirements</span></span>



| <span data-ttu-id="9d179-133">Требование</span><span class="sxs-lookup"><span data-stu-id="9d179-133">Requirement</span></span> | <span data-ttu-id="9d179-134">Значение</span><span class="sxs-lookup"><span data-stu-id="9d179-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d179-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d179-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9d179-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d179-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9d179-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d179-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9d179-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d179-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9d179-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9d179-139">Namespace</span></span><br/>                | <span data-ttu-id="9d179-140">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9d179-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9d179-141">MOF</span><span class="sxs-lookup"><span data-stu-id="9d179-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d179-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d179-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d179-143">DLL</span><span class="sxs-lookup"><span data-stu-id="9d179-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d179-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d179-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d179-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d179-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d179-146">**\_ХОСТЕДАКЦЕССПОИНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="9d179-146">**CIM\_HostedAccessPoint**</span></span>](cim-hostedaccesspoint.md)
</dt> </dl>

 

