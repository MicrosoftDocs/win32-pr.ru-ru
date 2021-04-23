---
description: '\_Класс WMI взаимосвязей Win32 дриверфордевице связывает экземпляр принтера с экземпляром драйвера принтера.'
ms.assetid: 56ff74b2-31ba-4d8e-b389-9f962932aa03
ms.tgt_platform: multiple
title: Класс Win32_DriverForDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DriverForDevice
- Win32_DriverForDevice.Antecedent
- Win32_DriverForDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5fb384eed80c6a614af448477c50be3204d3080
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655987"
---
# <a name="win32_driverfordevice-class"></a><span data-ttu-id="d5376-103">\_Класс Win32 дриверфордевице</span><span class="sxs-lookup"><span data-stu-id="d5376-103">Win32\_DriverForDevice class</span></span>

<span data-ttu-id="d5376-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ дриверфордевице** связывает экземпляр принтера с экземпляром драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="d5376-104">The **Win32\_DriverForDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a printer instance to a printer driver instance.</span></span>

<span data-ttu-id="d5376-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d5376-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d5376-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="d5376-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5376-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5376-107">Syntax</span></span>

``` syntax
class Win32_DriverForDevice : CIM_Dependency
{
  Win32_Printer       REF Antecedent;
  Win32_PrinterDriver REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d5376-108">Члены</span><span class="sxs-lookup"><span data-stu-id="d5376-108">Members</span></span>

<span data-ttu-id="d5376-109">Класс **Win32 \_ дриверфордевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d5376-109">The **Win32\_DriverForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="d5376-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d5376-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d5376-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="d5376-111">Properties</span></span>

<span data-ttu-id="d5376-112">Класс **Win32 \_ дриверфордевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d5376-112">The **Win32\_DriverForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d5376-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="d5376-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5376-114">Тип данных: **\_ принтер Win32**</span><span class="sxs-lookup"><span data-stu-id="d5376-114">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="d5376-115">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d5376-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d5376-116">Ссылка на экземпляр [**\_ принтера Win32**](win32-printer.md) , представляющий принтер.</span><span class="sxs-lookup"><span data-stu-id="d5376-116">Reference to the [**Win32\_Printer**](win32-printer.md) instance that represents the printer.</span></span>

<span data-ttu-id="d5376-117">Это свойство наследуется [**от \_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="d5376-117">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5376-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="d5376-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5376-119">Тип данных: **Win32 \_ принтердривер**</span><span class="sxs-lookup"><span data-stu-id="d5376-119">Data type: **Win32\_PrinterDriver**</span></span>
</dt> <dt>

<span data-ttu-id="d5376-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5376-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5376-121">Ссылка на экземпляр [**Win32 \_ принтердривер**](win32-printerdriver.md) , представляющий драйвер принтера для принтера.</span><span class="sxs-lookup"><span data-stu-id="d5376-121">Reference to the [**Win32\_PrinterDriver**](win32-printerdriver.md) instance that represents the printer driver for the printer.</span></span>

<span data-ttu-id="d5376-122">Это свойство наследуется [**от \_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="d5376-122">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5376-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5376-123">Remarks</span></span>

<span data-ttu-id="d5376-124">Класс **Win32 \_ дриверфордевице** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="d5376-124">The **Win32\_DriverForDevice** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5376-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d5376-125">Requirements</span></span>



| <span data-ttu-id="d5376-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d5376-126">Requirement</span></span> | <span data-ttu-id="d5376-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d5376-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5376-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5376-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d5376-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5376-129">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="d5376-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5376-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d5376-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5376-131">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="d5376-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d5376-132">Namespace</span></span><br/>                | <span data-ttu-id="d5376-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d5376-133">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="d5376-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d5376-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5376-135"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5376-135"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5376-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d5376-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5376-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5376-137"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="d5376-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5376-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5376-139">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="d5376-139">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

