---
description: '\_Абстрактный Девицесеттингс Win32, класс WMI Association связывает логическое устройство и параметр, который можно применить к нему.'
ms.assetid: 4f6c4c26-8da9-4e2c-8b8c-cec658ac08d4
ms.tgt_platform: multiple
title: Класс Win32_DeviceSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceSettings
- Win32_DeviceSettings.Setting
- Win32_DeviceSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1cd9cae29cfa608c9f3c0c36ebfe3ca7f903c809
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262726"
---
# <a name="win32_devicesettings-class"></a><span data-ttu-id="6123a-103">\_Класс Win32 девицесеттингс</span><span class="sxs-lookup"><span data-stu-id="6123a-103">Win32\_DeviceSettings class</span></span>

<span data-ttu-id="6123a-104">Абстрактный **\_ девицесеттингс Win32** , [класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) Association связывает логическое устройство и параметр, который можно применить к нему.</span><span class="sxs-lookup"><span data-stu-id="6123a-104">The **Win32\_DeviceSettings** abstract, association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical device and a setting that can be applied to it.</span></span>

<span data-ttu-id="6123a-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="6123a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6123a-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="6123a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6123a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6123a-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4FD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceSettings : CIM_ElementSetting
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a><span data-ttu-id="6123a-108">Члены</span><span class="sxs-lookup"><span data-stu-id="6123a-108">Members</span></span>

<span data-ttu-id="6123a-109">Класс **Win32 \_ девицесеттингс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6123a-109">The **Win32\_DeviceSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="6123a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="6123a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6123a-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="6123a-111">Properties</span></span>

<span data-ttu-id="6123a-112">Класс **Win32 \_ девицесеттингс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6123a-112">The **Win32\_DeviceSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6123a-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6123a-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6123a-114">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="6123a-114">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="6123a-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6123a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6123a-116">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("элемент"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="6123a-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="6123a-117">Логическое значение типа [**CIM \_**](cim-logicaldevice.md) , представляющее свойства логического устройства, к которому можно применить параметры.</span><span class="sxs-lookup"><span data-stu-id="6123a-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents properties of the logical device on which the settings can be applied.</span></span>

</dd> <dt>

<span data-ttu-id="6123a-118">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="6123a-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6123a-119">Тип данных: **\_ параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="6123a-119">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="6123a-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6123a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6123a-121">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("параметр"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| параметр CIM CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="6123a-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="6123a-122">[**\_ Параметр CIM**](cim-setting.md) , представляющий параметры, которые могут быть применены к логическому устройству.</span><span class="sxs-lookup"><span data-stu-id="6123a-122">A [**CIM\_Setting**](cim-setting.md) that represents settings that can be applied to the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6123a-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6123a-123">Remarks</span></span>

<span data-ttu-id="6123a-124">Класс **Win32 \_ девицесеттингс** является производным от [**CIM \_ елементсеттинг**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="6123a-124">The **Win32\_DeviceSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6123a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="6123a-125">Requirements</span></span>



| <span data-ttu-id="6123a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="6123a-126">Requirement</span></span> | <span data-ttu-id="6123a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="6123a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6123a-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6123a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6123a-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6123a-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6123a-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6123a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6123a-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6123a-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6123a-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6123a-132">Namespace</span></span><br/>                | <span data-ttu-id="6123a-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6123a-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6123a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6123a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6123a-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6123a-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6123a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6123a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6123a-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6123a-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6123a-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6123a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6123a-139">**\_ЕЛЕМЕНТСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="6123a-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="6123a-140">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="6123a-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

