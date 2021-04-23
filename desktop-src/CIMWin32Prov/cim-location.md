---
description: '\_Класс расположения CIM представляет позицию и адрес физического элемента.'
ms.assetid: c1ec467c-a338-4beb-a8fe-1ebc5b05c754
ms.tgt_platform: multiple
title: Класс CIM_Location
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Location
- CIM_Location.Address
- CIM_Location.Name
- CIM_Location.PhysicalPosition
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd5a1c1c23d07020b45c1c5979a941f01baff0d0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262662"
---
# <a name="cim_location-class"></a><span data-ttu-id="8e1e9-103">\_Класс расположения CIM</span><span class="sxs-lookup"><span data-stu-id="8e1e9-103">CIM\_Location class</span></span>

<span data-ttu-id="8e1e9-104">Класс **\_ расположения CIM** представляет позицию и адрес физического элемента.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-104">The **CIM\_Location** class represents the position and address of a physical element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8e1e9-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8e1e9-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8e1e9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8e1e9-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8e1e9-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e1e9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e1e9-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B67-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Location
{
  string Address;
  string Name;
  string PhysicalPosition;
};
```

## <a name="members"></a><span data-ttu-id="8e1e9-110">Члены</span><span class="sxs-lookup"><span data-stu-id="8e1e9-110">Members</span></span>

<span data-ttu-id="8e1e9-111">Класс **\_ расположения CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8e1e9-111">The **CIM\_Location** class has these types of members:</span></span>

-   [<span data-ttu-id="8e1e9-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="8e1e9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e1e9-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="8e1e9-113">Properties</span></span>

<span data-ttu-id="8e1e9-114">Класс **\_ расположения CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-114">The **CIM\_Location** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e1e9-115">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="8e1e9-115">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e1e9-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8e1e9-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e1e9-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8e1e9-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e1e9-118">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="8e1e9-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="8e1e9-119">Произвольная строка, указывающая улицу или другой тип адреса для расположения физического элемента.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-119">Free-form string that indicates a street or other type of address for the physical element's location.</span></span>

</dd> <dt>

<span data-ttu-id="8e1e9-120">**Name**</span><span class="sxs-lookup"><span data-stu-id="8e1e9-120">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e1e9-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8e1e9-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e1e9-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8e1e9-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e1e9-123">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8e1e9-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8e1e9-124">Произвольная строка, которая определяет метку для расположения и является частью ключа для объекта.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-124">Free-form string that defines a label for the location and is part of the key for the object.</span></span>

</dd> <dt>

<span data-ttu-id="8e1e9-125">**фисикалпоситион**</span><span class="sxs-lookup"><span data-stu-id="8e1e9-125">**PhysicalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e1e9-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8e1e9-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e1e9-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8e1e9-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e1e9-128">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8e1e9-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8e1e9-129">Произвольная строка, указывающая размещение физического элемента.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-129">Free-form string that indicates the placement of a physical element.</span></span> <span data-ttu-id="8e1e9-130">Он может указывать сведения о слоте на доске размещения, подключать сайт в шкаф, а также информацию широты и долготы.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-130">It can specify slot information on a hosting board, mounting site in a cabinet, or latitude and longitude information.</span></span> <span data-ttu-id="8e1e9-131">Он является частью ключа объекта **\_ расположения CIM** .</span><span class="sxs-lookup"><span data-stu-id="8e1e9-131">It is part of the key of the **CIM\_Location** object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e1e9-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e1e9-132">Remarks</span></span>

<span data-ttu-id="8e1e9-133">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-133">WMI does not implement this class.</span></span> <span data-ttu-id="8e1e9-134">Классы, производные **от \_ расположения CIM**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8e1e9-134">For classes derived from **CIM\_Location**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="8e1e9-135">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8e1e9-136">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e1e9-137">Требования</span><span class="sxs-lookup"><span data-stu-id="8e1e9-137">Requirements</span></span>



| <span data-ttu-id="8e1e9-138">Требование</span><span class="sxs-lookup"><span data-stu-id="8e1e9-138">Requirement</span></span> | <span data-ttu-id="8e1e9-139">Значение</span><span class="sxs-lookup"><span data-stu-id="8e1e9-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e1e9-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e1e9-140">Minimum supported client</span></span><br/> | <span data-ttu-id="8e1e9-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e1e9-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e1e9-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e1e9-142">Minimum supported server</span></span><br/> | <span data-ttu-id="8e1e9-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e1e9-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e1e9-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8e1e9-144">Namespace</span></span><br/>                | <span data-ttu-id="8e1e9-145">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8e1e9-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e1e9-146">MOF</span><span class="sxs-lookup"><span data-stu-id="8e1e9-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e1e9-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e1e9-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e1e9-148">DLL</span><span class="sxs-lookup"><span data-stu-id="8e1e9-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e1e9-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e1e9-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

