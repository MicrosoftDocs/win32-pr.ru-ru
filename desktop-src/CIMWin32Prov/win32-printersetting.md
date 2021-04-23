---
description: '\_Класс WMI взаимосвязей Win32 принтерсеттинг связывает принтер и его параметры конфигурации.'
ms.assetid: 5d0f0724-0583-449b-a6da-336e7c8e526e
ms.tgt_platform: multiple
title: Класс Win32_PrinterSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterSetting
- Win32_PrinterSetting.Setting
- Win32_PrinterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90a77678e61b755550ebb1818c34ccdc3159a88c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262639"
---
# <a name="win32_printersetting-class"></a><span data-ttu-id="ba7ce-103">\_Класс Win32 принтерсеттинг</span><span class="sxs-lookup"><span data-stu-id="ba7ce-103">Win32\_PrinterSetting class</span></span>

<span data-ttu-id="ba7ce-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ принтерсеттинг** связывает принтер и его параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ba7ce-104">The **Win32\_PrinterSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a printer and its configuration settings.</span></span>

<span data-ttu-id="ba7ce-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ba7ce-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ba7ce-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="ba7ce-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba7ce-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba7ce-107">Syntax</span></span>

``` syntax
class Win32_PrinterSetting : Win32_DeviceSettings
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a><span data-ttu-id="ba7ce-108">Члены</span><span class="sxs-lookup"><span data-stu-id="ba7ce-108">Members</span></span>

<span data-ttu-id="ba7ce-109">Класс **Win32 \_ принтерсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ba7ce-109">The **Win32\_PrinterSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="ba7ce-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ba7ce-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba7ce-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="ba7ce-111">Properties</span></span>

<span data-ttu-id="ba7ce-112">Класс **Win32 \_ принтерсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ba7ce-112">The **Win32\_PrinterSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba7ce-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ba7ce-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7ce-114">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="ba7ce-114">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="ba7ce-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ba7ce-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba7ce-116">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="ba7ce-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="ba7ce-117">Логическое значение типа [**CIM \_**](cim-logicaldevice.md) , представляющее свойства логического устройства, к которому можно применить параметры.</span><span class="sxs-lookup"><span data-stu-id="ba7ce-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents properties of the logical device on which the settings can be applied.</span></span>

<span data-ttu-id="ba7ce-118">Это свойство наследуется из [**Win32 \_ девицесеттингс**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="ba7ce-118">This property is inherited from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba7ce-119">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="ba7ce-119">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7ce-120">Тип данных: **\_ параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="ba7ce-120">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="ba7ce-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ba7ce-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba7ce-122">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("параметр CIM CIM \| \_ ")</span><span class="sxs-lookup"><span data-stu-id="ba7ce-122">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="ba7ce-123">[**\_ Параметр CIM**](cim-setting.md) , представляющий параметры, которые могут быть применены к логическому устройству.</span><span class="sxs-lookup"><span data-stu-id="ba7ce-123">A [**CIM\_Setting**](cim-setting.md) that represents settings that can be applied to the logical device.</span></span>

<span data-ttu-id="ba7ce-124">Это свойство наследуется из [**Win32 \_ девицесеттингс**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="ba7ce-124">This property is inherited from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba7ce-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba7ce-125">Remarks</span></span>

<span data-ttu-id="ba7ce-126">Класс **Win32 \_ принтерсеттинг** является производным от [**Win32 \_ девицесеттингс**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="ba7ce-126">The **Win32\_PrinterSetting** class is derived from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba7ce-127">Требования</span><span class="sxs-lookup"><span data-stu-id="ba7ce-127">Requirements</span></span>



| <span data-ttu-id="ba7ce-128">Требование</span><span class="sxs-lookup"><span data-stu-id="ba7ce-128">Requirement</span></span> | <span data-ttu-id="ba7ce-129">Значение</span><span class="sxs-lookup"><span data-stu-id="ba7ce-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba7ce-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba7ce-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ba7ce-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba7ce-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="ba7ce-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba7ce-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ba7ce-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba7ce-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="ba7ce-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ba7ce-134">Namespace</span></span><br/>                | <span data-ttu-id="ba7ce-135">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ba7ce-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="ba7ce-136">MOF</span><span class="sxs-lookup"><span data-stu-id="ba7ce-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba7ce-137"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba7ce-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba7ce-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ba7ce-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba7ce-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba7ce-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="ba7ce-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba7ce-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba7ce-141">**\_Девицесеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="ba7ce-141">**Win32\_DeviceSettings**</span></span>](win32-devicesettings.md)
</dt> <dt>

[<span data-ttu-id="ba7ce-142">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="ba7ce-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
