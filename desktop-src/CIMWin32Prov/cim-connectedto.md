---
description: Класс CIM \_ коннектедто представляет ассоциацию, которая указывает, что подключены два или более физических соединителя.
ms.assetid: fedd9227-8a3b-461a-995b-08cbceb81181
ms.tgt_platform: multiple
title: Класс CIM_ConnectedTo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConnectedTo
- CIM_ConnectedTo.Dependent
- CIM_ConnectedTo.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f1a507cb529f2040607024e1a6167ddcd5dc7c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072478"
---
# <a name="cim_connectedto-class"></a><span data-ttu-id="08534-103">\_Класс CIM коннектедто</span><span class="sxs-lookup"><span data-stu-id="08534-103">CIM\_ConnectedTo class</span></span>

<span data-ttu-id="08534-104">Класс **CIM \_ коннектедто** представляет ассоциацию, которая указывает, что подключены два или более физических соединителя.</span><span class="sxs-lookup"><span data-stu-id="08534-104">The **CIM\_ConnectedTo** class represents an association that indicates that two or more physical connectors are connected.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08534-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="08534-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="08534-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="08534-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="08534-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="08534-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="08534-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="08534-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="08534-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08534-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B85-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ConnectedTo : CIM_Dependency
{
  CIM_PhysicalConnector REF Dependent;
  CIM_PhysicalConnector REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="08534-110">Члены</span><span class="sxs-lookup"><span data-stu-id="08534-110">Members</span></span>

<span data-ttu-id="08534-111">Класс **CIM \_ коннектедто** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="08534-111">The **CIM\_ConnectedTo** class has these types of members:</span></span>

-   [<span data-ttu-id="08534-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="08534-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08534-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="08534-113">Properties</span></span>

<span data-ttu-id="08534-114">Класс **CIM \_ коннектедто** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="08534-114">The **CIM\_ConnectedTo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08534-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="08534-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08534-116">Тип данных: **CIM \_ фисикалконнектор**</span><span class="sxs-lookup"><span data-stu-id="08534-116">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="08534-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08534-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08534-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="08534-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="08534-119">[**\_ Фисикалконнектор CIM**](cim-physicalconnector.md) , представляющий физический соединитель, который выступает в качестве одного конца соединения.</span><span class="sxs-lookup"><span data-stu-id="08534-119">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that represents a physical connector that serves as one end of the connection.</span></span>

</dd> <dt>

<span data-ttu-id="08534-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="08534-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08534-121">Тип данных: **CIM \_ фисикалконнектор**</span><span class="sxs-lookup"><span data-stu-id="08534-121">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="08534-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08534-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08534-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="08534-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="08534-124">[**\_ Фисикалконнектор CIM**](cim-physicalconnector.md) , представляющий другой физический соединитель, который выступает в качестве другого элемента соединения.</span><span class="sxs-lookup"><span data-stu-id="08534-124">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that represents another physical connector that serves as the other end of the connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08534-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08534-125">Remarks</span></span>

<span data-ttu-id="08534-126">Класс **CIM \_ коннектедто** наследуется от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="08534-126">The **CIM\_ConnectedTo** class is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="08534-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="08534-127">WMI does not implement this class.</span></span>

<span data-ttu-id="08534-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="08534-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="08534-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="08534-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="08534-130">Требования</span><span class="sxs-lookup"><span data-stu-id="08534-130">Requirements</span></span>



| <span data-ttu-id="08534-131">Требование</span><span class="sxs-lookup"><span data-stu-id="08534-131">Requirement</span></span> | <span data-ttu-id="08534-132">Значение</span><span class="sxs-lookup"><span data-stu-id="08534-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08534-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="08534-133">Minimum supported client</span></span><br/> | <span data-ttu-id="08534-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08534-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="08534-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="08534-135">Minimum supported server</span></span><br/> | <span data-ttu-id="08534-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08534-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="08534-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="08534-137">Namespace</span></span><br/>                | <span data-ttu-id="08534-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="08534-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="08534-139">MOF</span><span class="sxs-lookup"><span data-stu-id="08534-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08534-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08534-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="08534-141">DLL</span><span class="sxs-lookup"><span data-stu-id="08534-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08534-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08534-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08534-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08534-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08534-144">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="08534-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

