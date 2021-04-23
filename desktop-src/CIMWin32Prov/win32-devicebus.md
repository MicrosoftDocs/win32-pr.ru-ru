---
description: '\_Класс WMI взаимосвязей Win32 девицебус связывает системную шину и логическое устройство с помощью шины. Этот класс используется для обнаружения устройств, на которых находится шина.'
ms.assetid: 2d7d83a5-c058-40c0-aab3-7700f4067a16
ms.tgt_platform: multiple
title: Класс Win32_DeviceBus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceBus
- Win32_DeviceBus.Dependent
- Win32_DeviceBus.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2dde01ee6b3f3be026dbc19f8c4b8e2c238f4ff2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142859"
---
# <a name="win32_devicebus-class"></a><span data-ttu-id="74680-104">\_Класс Win32 девицебус</span><span class="sxs-lookup"><span data-stu-id="74680-104">Win32\_DeviceBus class</span></span>

<span data-ttu-id="74680-105">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ девицебус** связывает системную шину и логическое устройство с помощью шины.</span><span class="sxs-lookup"><span data-stu-id="74680-105">The **Win32\_DeviceBus** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a system bus and a logical device using the bus.</span></span> <span data-ttu-id="74680-106">Этот класс используется для обнаружения устройств, на которых находится шина.</span><span class="sxs-lookup"><span data-stu-id="74680-106">This class is used to discover which devices are on which bus.</span></span>

<span data-ttu-id="74680-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="74680-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="74680-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="74680-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="74680-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74680-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceBus : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  Win32_Bus         REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="74680-110">Члены</span><span class="sxs-lookup"><span data-stu-id="74680-110">Members</span></span>

<span data-ttu-id="74680-111">Класс **Win32 \_ девицебус** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="74680-111">The **Win32\_DeviceBus** class has these types of members:</span></span>

-   [<span data-ttu-id="74680-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="74680-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="74680-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="74680-113">Properties</span></span>

<span data-ttu-id="74680-114">Класс **Win32 \_ девицебус** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="74680-114">The **Win32\_DeviceBus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74680-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="74680-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74680-116">Тип данных: **\_ шина Win32**</span><span class="sxs-lookup"><span data-stu-id="74680-116">Data type: **Win32\_Bus**</span></span>
</dt> <dt>

<span data-ttu-id="74680-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74680-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74680-118">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| шина WMI Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="74680-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Bus")</span></span>
</dt> </dl>

<span data-ttu-id="74680-119">[**\_ Шина Win32**](win32-bus.md) , описывающая свойства системной шины, используемой логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="74680-119">A [**Win32\_Bus**](win32-bus.md) that describes the properties of the system bus that is used by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="74680-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="74680-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74680-121">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="74680-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="74680-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74680-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74680-123">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="74680-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="74680-124">Логическое значение типа [**CIM \_**](cim-logicaldevice.md) , описывающее свойства логического устройства, использующего системную шину.</span><span class="sxs-lookup"><span data-stu-id="74680-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the properties of the logical device that is using the system bus.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74680-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74680-125">Remarks</span></span>

<span data-ttu-id="74680-126">Класс **Win32 \_ девицебус** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="74680-126">The **Win32\_DeviceBus** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74680-127">Требования</span><span class="sxs-lookup"><span data-stu-id="74680-127">Requirements</span></span>



| <span data-ttu-id="74680-128">Требование</span><span class="sxs-lookup"><span data-stu-id="74680-128">Requirement</span></span> | <span data-ttu-id="74680-129">Значение</span><span class="sxs-lookup"><span data-stu-id="74680-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74680-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74680-130">Minimum supported client</span></span><br/> | <span data-ttu-id="74680-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74680-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="74680-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74680-132">Minimum supported server</span></span><br/> | <span data-ttu-id="74680-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74680-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="74680-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="74680-134">Namespace</span></span><br/>                | <span data-ttu-id="74680-135">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="74680-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="74680-136">MOF</span><span class="sxs-lookup"><span data-stu-id="74680-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74680-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74680-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="74680-138">DLL</span><span class="sxs-lookup"><span data-stu-id="74680-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74680-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74680-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74680-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74680-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74680-141">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="74680-141">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="74680-142">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="74680-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

