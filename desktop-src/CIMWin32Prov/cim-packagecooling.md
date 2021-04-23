---
description: Ассоциация CIM \_ паккажекулинг представляет собой связь, в которой устройство охлаждения устанавливается в пакете, таком как шасси или стойка, для помощи с охлаждением пакета.
ms.assetid: 0aaae8e1-6e70-4b26-8e56-dac5657e58c1
ms.tgt_platform: multiple
title: Класс CIM_PackageCooling
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageCooling
- CIM_PackageCooling.Dependent
- CIM_PackageCooling.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f88cd3f07983870bed8fd2d740f3bf9051019b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538957"
---
# <a name="cim_packagecooling-class"></a><span data-ttu-id="f2a6f-103">\_Класс CIM паккажекулинг</span><span class="sxs-lookup"><span data-stu-id="f2a6f-103">CIM\_PackageCooling class</span></span>

<span data-ttu-id="f2a6f-104">Ассоциация **CIM \_ паккажекулинг** представляет собой связь, в которой устройство охлаждения устанавливается в пакете, таком как шасси или стойка, для помощи с охлаждением пакета.</span><span class="sxs-lookup"><span data-stu-id="f2a6f-104">The **CIM\_PackageCooling** association represents the relationship in which a cooling device is installed in a package, such as a chassis or rack, to assist with the package's cooling.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f2a6f-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="f2a6f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f2a6f-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f2a6f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f2a6f-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f2a6f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f2a6f-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="f2a6f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2a6f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2a6f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageCooling : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_CoolingDevice   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="f2a6f-110">Члены</span><span class="sxs-lookup"><span data-stu-id="f2a6f-110">Members</span></span>

<span data-ttu-id="f2a6f-111">Класс **CIM \_ паккажекулинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f2a6f-111">The **CIM\_PackageCooling** class has these types of members:</span></span>

-   [<span data-ttu-id="f2a6f-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="f2a6f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2a6f-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f2a6f-113">Properties</span></span>

<span data-ttu-id="f2a6f-114">Класс **CIM \_ паккажекулинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f2a6f-114">The **CIM\_PackageCooling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f2a6f-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="f2a6f-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2a6f-116">Тип данных: **CIM \_ кулингдевице**</span><span class="sxs-lookup"><span data-stu-id="f2a6f-116">Data type: **CIM\_CoolingDevice**</span></span>
</dt> <dt>

<span data-ttu-id="f2a6f-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2a6f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2a6f-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="f2a6f-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f2a6f-119">[**\_ Кулингдевице CIM**](cim-coolingdevice.md) , описывающий устройство охлаждения для пакета.</span><span class="sxs-lookup"><span data-stu-id="f2a6f-119">A [**CIM\_CoolingDevice**](cim-coolingdevice.md) that describes the cooling device for the package.</span></span>

</dd> <dt>

<span data-ttu-id="f2a6f-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="f2a6f-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2a6f-121">Тип данных: **CIM \_ фисикалпаккаже**</span><span class="sxs-lookup"><span data-stu-id="f2a6f-121">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="f2a6f-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2a6f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2a6f-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="f2a6f-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f2a6f-124">[**\_ Фисикалпаккаже CIM**](cim-physicalpackage.md) , описывающий физический пакет, окружение которого охлаждения.</span><span class="sxs-lookup"><span data-stu-id="f2a6f-124">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package whose environment is cooled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2a6f-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2a6f-125">Remarks</span></span>

<span data-ttu-id="f2a6f-126">**Модель CIM \_ Паккажекулинг** является производным [**от \_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="f2a6f-126">**CIM\_PackageCooling** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="f2a6f-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="f2a6f-127">WMI does not implement this class.</span></span>

<span data-ttu-id="f2a6f-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="f2a6f-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f2a6f-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="f2a6f-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2a6f-130">Требования</span><span class="sxs-lookup"><span data-stu-id="f2a6f-130">Requirements</span></span>



| <span data-ttu-id="f2a6f-131">Требование</span><span class="sxs-lookup"><span data-stu-id="f2a6f-131">Requirement</span></span> | <span data-ttu-id="f2a6f-132">Значение</span><span class="sxs-lookup"><span data-stu-id="f2a6f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2a6f-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2a6f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f2a6f-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2a6f-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f2a6f-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2a6f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f2a6f-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2a6f-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f2a6f-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f2a6f-137">Namespace</span></span><br/>                | <span data-ttu-id="f2a6f-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f2a6f-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f2a6f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f2a6f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2a6f-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2a6f-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2a6f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f2a6f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2a6f-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2a6f-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2a6f-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2a6f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2a6f-144">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="f2a6f-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

