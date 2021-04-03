---
description: '\_Класс WMI взаимосвязей Win32 вмиелементсеттинг связывает службу, работающую в системе Windows, и параметры WMI, которые она может использовать.'
ms.assetid: 00e9f882-5f54-4042-a916-2f90ed9a37c0
ms.tgt_platform: multiple
title: Класс Win32_WMIElementSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMIElementSetting
- Win32_WMIElementSetting.Element
- Win32_WMIElementSetting.Setting
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 41f79614fd0931759d502bbd61c7f4143e9e7dc9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895454"
---
# <a name="win32_wmielementsetting-class"></a><span data-ttu-id="47931-103">\_Класс Win32 вмиелементсеттинг</span><span class="sxs-lookup"><span data-stu-id="47931-103">Win32\_WMIElementSetting class</span></span>

<span data-ttu-id="47931-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ вмиелементсеттинг** связывает службу, работающую в системе Windows, и параметры WMI, которые она может использовать.</span><span class="sxs-lookup"><span data-stu-id="47931-104">The **Win32\_WMIElementSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a service running in the Windows system and the WMI settings it can use.</span></span>

<span data-ttu-id="47931-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="47931-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="47931-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="47931-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="47931-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47931-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("WBEMCORE"), UUID("{A83EF167-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMIElementSetting : CIM_ElementSetting
{
  Win32_Service    REF Element;
  Win32_WMISetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="47931-108">Члены</span><span class="sxs-lookup"><span data-stu-id="47931-108">Members</span></span>

<span data-ttu-id="47931-109">Класс **Win32 \_ вмиелементсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="47931-109">The **Win32\_WMIElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="47931-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="47931-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47931-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="47931-111">Properties</span></span>

<span data-ttu-id="47931-112">Класс **Win32 \_ вмиелементсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="47931-112">The **Win32\_WMIElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="47931-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="47931-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47931-114">Тип данных: **\_ служба Win32**</span><span class="sxs-lookup"><span data-stu-id="47931-114">Data type: **Win32\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="47931-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47931-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47931-116">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("элемент"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| Служба WMI Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="47931-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Service")</span></span>
</dt> </dl>

<span data-ttu-id="47931-117">Ссылка на экземпляр, представляющий службу Windows, с помощью или свойств WMI отображая.</span><span class="sxs-lookup"><span data-stu-id="47931-117">Reference to the instance representing the Windows service using or surfacing WMI properties.</span></span>

</dd> <dt>

<span data-ttu-id="47931-118">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="47931-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47931-119">Тип данных: **Win32 \_ вмисеттинг**</span><span class="sxs-lookup"><span data-stu-id="47931-119">Data type: **Win32\_WMISetting**</span></span>
</dt> <dt>

<span data-ttu-id="47931-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47931-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47931-121">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("параметр"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ вмисеттинг")</span><span class="sxs-lookup"><span data-stu-id="47931-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_WMISetting")</span></span>
</dt> </dl>

<span data-ttu-id="47931-122">Ссылка на экземпляр, представляющий параметры WMI, доступные для службы Windows.</span><span class="sxs-lookup"><span data-stu-id="47931-122">Reference to the instance representing the WMI settings available to the Windows service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47931-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47931-123">Remarks</span></span>

<span data-ttu-id="47931-124">Класс **Win32 \_ вмиелементсеттинг** является производным от [**CIM \_ елементсеттинг**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="47931-124">The **Win32\_WMIElementSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="47931-125">Требования</span><span class="sxs-lookup"><span data-stu-id="47931-125">Requirements</span></span>



| <span data-ttu-id="47931-126">Требование</span><span class="sxs-lookup"><span data-stu-id="47931-126">Requirement</span></span> | <span data-ttu-id="47931-127">Значение</span><span class="sxs-lookup"><span data-stu-id="47931-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47931-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47931-128">Minimum supported client</span></span><br/> | <span data-ttu-id="47931-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47931-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="47931-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47931-130">Minimum supported server</span></span><br/> | <span data-ttu-id="47931-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47931-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="47931-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="47931-132">Namespace</span></span><br/>                | <span data-ttu-id="47931-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="47931-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="47931-134">MOF</span><span class="sxs-lookup"><span data-stu-id="47931-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47931-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47931-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="47931-136">DLL</span><span class="sxs-lookup"><span data-stu-id="47931-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47931-137"><dt>Wbemcore.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47931-137"><dt>Wbemcore.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47931-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47931-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47931-139">**\_ЕЛЕМЕНТСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="47931-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="47931-140">Классы управления службами WMI</span><span class="sxs-lookup"><span data-stu-id="47931-140">WMI Service Management Classes</span></span>](./wmi-service-management-classes.md)
</dt> </dl>

 

 
