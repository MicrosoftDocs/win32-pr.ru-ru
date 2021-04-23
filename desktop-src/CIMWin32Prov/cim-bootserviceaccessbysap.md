---
description: Класс CIM \_ бутсервицеакцессбисап связывает службу загрузки и ее точки доступа.
ms.assetid: 993469dd-fb9c-4d21-99e0-03c4b19eb7fd
ms.tgt_platform: multiple
title: Класс CIM_BootServiceAccessBySAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootServiceAccessBySAP
- CIM_BootServiceAccessBySAP.Dependent
- CIM_BootServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90548be52defbcf3419d6c7defc21395da5cfbfe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807613"
---
# <a name="cim_bootserviceaccessbysap-class"></a><span data-ttu-id="4fbcc-103">\_Класс CIM бутсервицеакцессбисап</span><span class="sxs-lookup"><span data-stu-id="4fbcc-103">CIM\_BootServiceAccessBySAP class</span></span>

<span data-ttu-id="4fbcc-104">Класс **CIM \_ бутсервицеакцессбисап** связывает службу загрузки и ее точки доступа.</span><span class="sxs-lookup"><span data-stu-id="4fbcc-104">The **CIM\_BootServiceAccessBySAP** class associates a boot service and its access points.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4fbcc-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="4fbcc-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4fbcc-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4fbcc-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4fbcc-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4fbcc-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4fbcc-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="4fbcc-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fbcc-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fbcc-109">Syntax</span></span>

``` syntax
[UUID("{6EDF1DD2-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BootServiceAccessBySAP : CIM_ServiceAccessBySAP
{
  CIM_BootSAP     REF Dependent;
  CIM_BootService REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="4fbcc-110">Члены</span><span class="sxs-lookup"><span data-stu-id="4fbcc-110">Members</span></span>

<span data-ttu-id="4fbcc-111">Класс **CIM \_ бутсервицеакцессбисап** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4fbcc-111">The **CIM\_BootServiceAccessBySAP** class has these types of members:</span></span>

-   [<span data-ttu-id="4fbcc-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="4fbcc-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4fbcc-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="4fbcc-113">Properties</span></span>

<span data-ttu-id="4fbcc-114">Класс **CIM \_ бутсервицеакцессбисап** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4fbcc-114">The **CIM\_BootServiceAccessBySAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4fbcc-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="4fbcc-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fbcc-116">Тип данных: **CIM \_ бутсервице**</span><span class="sxs-lookup"><span data-stu-id="4fbcc-116">Data type: **CIM\_BootService**</span></span>
</dt> <dt>

<span data-ttu-id="4fbcc-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4fbcc-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fbcc-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="4fbcc-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4fbcc-119">[**\_ Бутсервице CIM**](cim-bootservice.md) , описывающий службу загрузки.</span><span class="sxs-lookup"><span data-stu-id="4fbcc-119">A [**CIM\_BootService**](cim-bootservice.md) that describes the boot service.</span></span>

</dd> <dt>

<span data-ttu-id="4fbcc-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="4fbcc-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fbcc-121">Тип данных: **CIM \_ бутсап**</span><span class="sxs-lookup"><span data-stu-id="4fbcc-121">Data type: **CIM\_BootSAP**</span></span>
</dt> <dt>

<span data-ttu-id="4fbcc-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4fbcc-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fbcc-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="4fbcc-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4fbcc-124">[**\_ Бутсап CIM**](cim-bootsap.md) , описывающий точку доступа для службы загрузки.</span><span class="sxs-lookup"><span data-stu-id="4fbcc-124">A [**CIM\_BootSAP**](cim-bootsap.md) that describes an access point for the boot service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4fbcc-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4fbcc-125">Remarks</span></span>

<span data-ttu-id="4fbcc-126">Класс **CIM \_ бутсервицеакцессбисап** является производным от [**CIM \_ сервицеакцессбисап**](cim-serviceaccessbysap.md).</span><span class="sxs-lookup"><span data-stu-id="4fbcc-126">The **CIM\_BootServiceAccessBySAP** class is derived from [**CIM\_ServiceAccessBySAP**](cim-serviceaccessbysap.md).</span></span>

<span data-ttu-id="4fbcc-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="4fbcc-127">WMI does not implement this class.</span></span>

<span data-ttu-id="4fbcc-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="4fbcc-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4fbcc-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="4fbcc-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fbcc-130">Требования</span><span class="sxs-lookup"><span data-stu-id="4fbcc-130">Requirements</span></span>



| <span data-ttu-id="4fbcc-131">Требование</span><span class="sxs-lookup"><span data-stu-id="4fbcc-131">Requirement</span></span> | <span data-ttu-id="4fbcc-132">Значение</span><span class="sxs-lookup"><span data-stu-id="4fbcc-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fbcc-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4fbcc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4fbcc-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4fbcc-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4fbcc-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4fbcc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4fbcc-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4fbcc-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4fbcc-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4fbcc-137">Namespace</span></span><br/>                | <span data-ttu-id="4fbcc-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4fbcc-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4fbcc-139">MOF</span><span class="sxs-lookup"><span data-stu-id="4fbcc-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4fbcc-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4fbcc-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4fbcc-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4fbcc-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fbcc-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fbcc-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fbcc-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4fbcc-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fbcc-144">**\_СЕРВИЦЕАКЦЕССБИСАП CIM**</span><span class="sxs-lookup"><span data-stu-id="4fbcc-144">**CIM\_ServiceAccessBySAP**</span></span>](cim-serviceaccessbysap.md)
</dt> </dl>

 

