---
description: '\_Класс WMI взаимосвязей Win32 сериалпортсеттинг связывает последовательный порт и его параметры конфигурации.'
ms.assetid: 57856207-abe5-4d93-9a34-acfe30ccd80c
ms.tgt_platform: multiple
title: Класс Win32_SerialPortSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortSetting
- Win32_SerialPortSetting.Setting
- Win32_SerialPortSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 713cdb57b5ed7135529959d3c17f7453924ce1dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990386"
---
# <a name="win32_serialportsetting-class"></a><span data-ttu-id="2479f-103">\_Класс Win32 сериалпортсеттинг</span><span class="sxs-lookup"><span data-stu-id="2479f-103">Win32\_SerialPortSetting class</span></span>

<span data-ttu-id="2479f-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ сериалпортсеттинг** связывает последовательный порт и его параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2479f-104">The **Win32\_SerialPortSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a serial port and its configuration settings.</span></span>

<span data-ttu-id="2479f-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="2479f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2479f-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="2479f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2479f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2479f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortSetting : Win32_DeviceSettings
{
  Win32_SerialPortConfiguration REF Setting;
  Win32_SerialPort              REF Element;
};
```

## <a name="members"></a><span data-ttu-id="2479f-108">Члены</span><span class="sxs-lookup"><span data-stu-id="2479f-108">Members</span></span>

<span data-ttu-id="2479f-109">Класс **Win32 \_ сериалпортсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2479f-109">The **Win32\_SerialPortSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="2479f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="2479f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2479f-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="2479f-111">Properties</span></span>

<span data-ttu-id="2479f-112">Класс **Win32 \_ сериалпортсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2479f-112">The **Win32\_SerialPortSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2479f-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="2479f-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2479f-114">Тип данных: **Win32 \_ SerialPort**</span><span class="sxs-lookup"><span data-stu-id="2479f-114">Data type: **Win32\_SerialPort**</span></span>
</dt> <dt>

<span data-ttu-id="2479f-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2479f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2479f-116">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("элемент"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPort")</span><span class="sxs-lookup"><span data-stu-id="2479f-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SerialPort")</span></span>
</dt> </dl>

<span data-ttu-id="2479f-117">[**Win32 \_ SerialPort**](win32-serialport.md) , содержащий свойства последовательного порта в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="2479f-117">A [**Win32\_SerialPort**](win32-serialport.md) that contains the properties of a serial port on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="2479f-118">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="2479f-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2479f-119">Тип данных: **Win32 \_ сериалпортконфигуратион**</span><span class="sxs-lookup"><span data-stu-id="2479f-119">Data type: **Win32\_SerialPortConfiguration**</span></span>
</dt> <dt>

<span data-ttu-id="2479f-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2479f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2479f-121">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("параметр"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ сериалпортконфигуратион")</span><span class="sxs-lookup"><span data-stu-id="2479f-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SerialPortConfiguration")</span></span>
</dt> </dl>

<span data-ttu-id="2479f-122">[**\_ Сериалпортконфигуратион Win32**](win32-serialportconfiguration.md) , который содержит параметр конфигурации для последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="2479f-122">A [**Win32\_SerialPortConfiguration**](win32-serialportconfiguration.md) that contains the configuration setting for the serial port.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2479f-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2479f-123">Remarks</span></span>

<span data-ttu-id="2479f-124">Класс **Win32 \_ сериалпортсеттинг** является производным от [**Win32 \_ девицесеттингс**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="2479f-124">The **Win32\_SerialPortSetting** class is derived from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2479f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="2479f-125">Requirements</span></span>



| <span data-ttu-id="2479f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="2479f-126">Requirement</span></span> | <span data-ttu-id="2479f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="2479f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2479f-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2479f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2479f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2479f-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2479f-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2479f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2479f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2479f-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2479f-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2479f-132">Namespace</span></span><br/>                | <span data-ttu-id="2479f-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2479f-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2479f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="2479f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2479f-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2479f-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2479f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2479f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2479f-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2479f-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2479f-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2479f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2479f-139">**\_Девицесеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="2479f-139">**Win32\_DeviceSettings**</span></span>](win32-devicesettings.md)
</dt> <dt>

[<span data-ttu-id="2479f-140">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="2479f-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
