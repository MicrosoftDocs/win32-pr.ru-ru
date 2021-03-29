---
description: '\_Класс WMI взаимосвязей Win32 меморидевицеаррай связывает устройство памяти и массив памяти, в котором он находится.'
ms.assetid: 39ea6333-2352-488b-99e4-97594bea7dcd
ms.tgt_platform: multiple
title: Класс Win32_MemoryDeviceArray
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDeviceArray
- Win32_MemoryDeviceArray.GroupComponent
- Win32_MemoryDeviceArray.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1e527f77183c3bdc09d464f6fed4808e45adefa5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895465"
---
# <a name="win32_memorydevicearray-class"></a><span data-ttu-id="b4607-103">\_Класс Win32 меморидевицеаррай</span><span class="sxs-lookup"><span data-stu-id="b4607-103">Win32\_MemoryDeviceArray class</span></span>

<span data-ttu-id="b4607-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ меморидевицеаррай** связывает устройство памяти и массив памяти, в котором он находится.</span><span class="sxs-lookup"><span data-stu-id="b4607-104">The **Win32\_MemoryDeviceArray** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a memory device and the memory array in which it resides.</span></span>

<span data-ttu-id="b4607-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="b4607-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b4607-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="b4607-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4607-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4607-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF563-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryDeviceArray : CIM_Component
{
  Win32_MemoryArray  REF GroupComponent;
  Win32_MemoryDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="b4607-108">Члены</span><span class="sxs-lookup"><span data-stu-id="b4607-108">Members</span></span>

<span data-ttu-id="b4607-109">Класс **Win32 \_ меморидевицеаррай** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b4607-109">The **Win32\_MemoryDeviceArray** class has these types of members:</span></span>

-   [<span data-ttu-id="b4607-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="b4607-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b4607-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b4607-111">Properties</span></span>

<span data-ttu-id="b4607-112">Класс **Win32 \_ меморидевицеаррай** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b4607-112">The **Win32\_MemoryDeviceArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b4607-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="b4607-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4607-114">Тип данных: **Win32 \_ меморяррай**</span><span class="sxs-lookup"><span data-stu-id="b4607-114">Data type: **Win32\_MemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="b4607-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b4607-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4607-116">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ меморяррай")</span><span class="sxs-lookup"><span data-stu-id="b4607-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="b4607-117">[**\_ Меморяррай Win32**](win32-memoryarray.md) , представляющий часть массива памяти в \_ ассоциации Win32 меморидевицеаррай.</span><span class="sxs-lookup"><span data-stu-id="b4607-117">A [**Win32\_MemoryArray**](win32-memoryarray.md) that represents the memory array part of the Win32\_MemoryDeviceArray association.</span></span>

</dd> <dt>

<span data-ttu-id="b4607-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b4607-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4607-119">Тип данных: **Win32 \_ меморидевице**</span><span class="sxs-lookup"><span data-stu-id="b4607-119">Data type: **Win32\_MemoryDevice**</span></span>
</dt> <dt>

<span data-ttu-id="b4607-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b4607-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4607-121">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ меморидевице")</span><span class="sxs-lookup"><span data-stu-id="b4607-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryDevice")</span></span>
</dt> </dl>

<span data-ttu-id="b4607-122">[**\_ Меморидевице Win32**](win32-memorydevice.md) , который представляет часть устройства памяти в \_ сопоставлении Win32 меморидевицеаррай.</span><span class="sxs-lookup"><span data-stu-id="b4607-122">A [**Win32\_MemoryDevice**](win32-memorydevice.md) that represents a memory device part of the Win32\_MemoryDeviceArray association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4607-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4607-123">Remarks</span></span>

<span data-ttu-id="b4607-124">Класс **Win32 \_ меморидевицеаррай** является производным от [**\_ компонента CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="b4607-124">The **Win32\_MemoryDeviceArray** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4607-125">Требования</span><span class="sxs-lookup"><span data-stu-id="b4607-125">Requirements</span></span>



| <span data-ttu-id="b4607-126">Требование</span><span class="sxs-lookup"><span data-stu-id="b4607-126">Requirement</span></span> | <span data-ttu-id="b4607-127">Значение</span><span class="sxs-lookup"><span data-stu-id="b4607-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4607-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4607-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b4607-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4607-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b4607-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4607-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b4607-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4607-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b4607-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b4607-132">Namespace</span></span><br/>                | <span data-ttu-id="b4607-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b4607-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b4607-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b4607-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4607-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4607-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4607-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b4607-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4607-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4607-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4607-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4607-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4607-139">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="b4607-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="b4607-140">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="b4607-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

