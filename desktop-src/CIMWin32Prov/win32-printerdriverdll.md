---
description: '\_Класс WMI взаимосвязей Win32 принтердривердлл связывает локальный принтер и его файл драйвера.'
ms.assetid: decbd1de-8091-47f7-94a1-42862070b920
ms.tgt_platform: multiple
title: Класс Win32_PrinterDriverDll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriverDll
- Win32_PrinterDriverDll.Antecedent
- Win32_PrinterDriverDll.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 41484c39d9e1b59efd79d7aee08719b3a241de97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496524"
---
# <a name="win32_printerdriverdll-class"></a><span data-ttu-id="f2311-103">\_Класс Win32 принтердривердлл</span><span class="sxs-lookup"><span data-stu-id="f2311-103">Win32\_PrinterDriverDll class</span></span>

<span data-ttu-id="f2311-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ принтердривердлл** связывает локальный принтер и его файл драйвера.</span><span class="sxs-lookup"><span data-stu-id="f2311-104">The **Win32\_PrinterDriverDll** association [WMI class](../wmisdk/retrieving-a-class.md) relates a local printer and its driver file.</span></span>

<span data-ttu-id="f2311-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f2311-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f2311-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="f2311-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2311-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2311-107">Syntax</span></span>

``` syntax
class Win32_PrinterDriverDll : CIM_Dependency
{
  CIM_DataFile  REF Antecedent;
  Win32_Printer REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f2311-108">Члены</span><span class="sxs-lookup"><span data-stu-id="f2311-108">Members</span></span>

<span data-ttu-id="f2311-109">Класс **Win32 \_ принтердривердлл** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f2311-109">The **Win32\_PrinterDriverDll** class has these types of members:</span></span>

-   [<span data-ttu-id="f2311-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f2311-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2311-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="f2311-111">Properties</span></span>

<span data-ttu-id="f2311-112">Класс **Win32 \_ принтердривердлл** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f2311-112">The **Win32\_PrinterDriverDll** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f2311-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="f2311-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2311-114">Тип данных: **CIM \_ File**</span><span class="sxs-lookup"><span data-stu-id="f2311-114">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="f2311-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2311-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2311-116">Квалификаторы: [ **ключ**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f2311-116">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f2311-117">Ссылка на экземпляр [**\_ файла данных CIM**](cim-datafile.md) , представляющий файл драйвера для этого принтера на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="f2311-117">Reference to the [**CIM\_DataFile**](cim-datafile.md) instance representing the driver file for this Windows-based printer.</span></span>

<span data-ttu-id="f2311-118">Это свойство наследуется [**от \_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="f2311-118">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2311-119">**Него**</span><span class="sxs-lookup"><span data-stu-id="f2311-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2311-120">Тип данных: **\_ принтер Win32**</span><span class="sxs-lookup"><span data-stu-id="f2311-120">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="f2311-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2311-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2311-122">Квалификаторы: [ **ключ**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f2311-122">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f2311-123">Ссылка на экземпляр [**\_ принтера Win32**](win32-printer.md) .</span><span class="sxs-lookup"><span data-stu-id="f2311-123">Reference to the [**Win32\_Printer**](win32-printer.md) instance.</span></span>

<span data-ttu-id="f2311-124">Это свойство наследуется [**от \_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="f2311-124">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2311-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2311-125">Remarks</span></span>

<span data-ttu-id="f2311-126">Класс **Win32 \_ принтердривердлл** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="f2311-126">The **Win32\_PrinterDriverDll** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2311-127">Требования</span><span class="sxs-lookup"><span data-stu-id="f2311-127">Requirements</span></span>



| <span data-ttu-id="f2311-128">Требование</span><span class="sxs-lookup"><span data-stu-id="f2311-128">Requirement</span></span> | <span data-ttu-id="f2311-129">Значение</span><span class="sxs-lookup"><span data-stu-id="f2311-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2311-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2311-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f2311-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2311-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="f2311-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2311-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f2311-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2311-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="f2311-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f2311-134">Namespace</span></span><br/>                | <span data-ttu-id="f2311-135">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f2311-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="f2311-136">MOF</span><span class="sxs-lookup"><span data-stu-id="f2311-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2311-137"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2311-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2311-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f2311-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2311-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2311-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="f2311-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2311-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2311-141">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="f2311-141">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="f2311-142">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="f2311-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
