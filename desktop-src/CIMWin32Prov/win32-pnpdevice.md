---
description: '\_Класс WMI взаимосвязей Win32 код устройства PnP связывает устройство (известное как Configuration Manager как пнпентити) и функцию, которую он выполняет.'
ms.assetid: 5163a423-60f2-416d-bf82-89517b499f93
ms.tgt_platform: multiple
title: Класс Win32_PnPDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevice
- Win32_PnPDevice.SameElement
- Win32_PnPDevice.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c17dc6d4169854469d630e2a622eacc85e8a587c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656059"
---
# <a name="win32_pnpdevice-class"></a><span data-ttu-id="22731-103">\_Класс Win32 код устройства PnP</span><span class="sxs-lookup"><span data-stu-id="22731-103">Win32\_PnPDevice class</span></span>

<span data-ttu-id="22731-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ код устройства PnP** связывает устройство (известное как Configuration Manager как пнпентити) и функцию, которую он выполняет.</span><span class="sxs-lookup"><span data-stu-id="22731-104">The **Win32\_PnPDevice** association [WMI class](../wmisdk/retrieving-a-class.md) relates a device (known to Configuration Manager as a PNPEntity) and the function it performs.</span></span> <span data-ttu-id="22731-105">Его функция представлена подклассом логического устройства, описывающего его использование.</span><span class="sxs-lookup"><span data-stu-id="22731-105">Its function is represented by a subclass of the logical device that describes its use.</span></span> <span data-ttu-id="22731-106">Например, [**\_ Клавиатура Win32**](win32-keyboard.md) или экземпляр [**\_ дискдриве Win32**](win32-diskdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="22731-106">For example, a [**Win32\_Keyboard**](win32-keyboard.md) or [**Win32\_DiskDrive**](win32-diskdrive.md) instance.</span></span> <span data-ttu-id="22731-107">Оба упоминаемых объекта представляют одно и то же базовое системное устройство. изменения, связанные с выделением ресурсов на стороне Пнпентити, будут влиять на связанное устройство.</span><span class="sxs-lookup"><span data-stu-id="22731-107">Both referenced objects represent the same underlying system device; changes to resource allocation on the PNPEntity side will effect the associated device.</span></span>

<span data-ttu-id="22731-108">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="22731-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="22731-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="22731-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="22731-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22731-110">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{FE28FD96-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPDevice
{
  CIM_LogicalDevice REF SameElement;
  Win32_PnPEntity   REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="22731-111">Члены</span><span class="sxs-lookup"><span data-stu-id="22731-111">Members</span></span>

<span data-ttu-id="22731-112">Класс **Win32 \_ код устройства PnP** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="22731-112">The **Win32\_PnPDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="22731-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="22731-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="22731-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="22731-114">Properties</span></span>

<span data-ttu-id="22731-115">Класс **Win32 \_ код устройства PnP** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="22731-115">The **Win32\_PnPDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="22731-116">**самилемент**</span><span class="sxs-lookup"><span data-stu-id="22731-116">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22731-117">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="22731-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="22731-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="22731-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22731-119">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="22731-119">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="22731-120">Ссылка на экземпляр [**CIM \_**](cim-logicaldevice.md) , представляющий свойства логического устройства, связанные с устройством Самонастраивающийся.</span><span class="sxs-lookup"><span data-stu-id="22731-120">Reference to the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance representing the logical device properties associated with the Plug and Play device.</span></span>

</dd> <dt>

<span data-ttu-id="22731-121">**системелемент**</span><span class="sxs-lookup"><span data-stu-id="22731-121">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22731-122">Тип данных: **Win32 \_ пнпентити**</span><span class="sxs-lookup"><span data-stu-id="22731-122">Data type: **Win32\_PnPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="22731-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="22731-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22731-124">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ пнпентити")</span><span class="sxs-lookup"><span data-stu-id="22731-124">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PnPEntity")</span></span>
</dt> </dl>

<span data-ttu-id="22731-125">Ссылка на экземпляр [**Win32 \_ пнпентити**](win32-pnpentity.md) , представляющий устройство Самонастраивающийся, связанное с логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="22731-125">Reference to the [**Win32\_PnPEntity**](win32-pnpentity.md) instance representing the Plug and Play device associated with the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="22731-126">Требования</span><span class="sxs-lookup"><span data-stu-id="22731-126">Requirements</span></span>



| <span data-ttu-id="22731-127">Требование</span><span class="sxs-lookup"><span data-stu-id="22731-127">Requirement</span></span> | <span data-ttu-id="22731-128">Значение</span><span class="sxs-lookup"><span data-stu-id="22731-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22731-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22731-129">Minimum supported client</span></span><br/> | <span data-ttu-id="22731-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22731-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="22731-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22731-131">Minimum supported server</span></span><br/> | <span data-ttu-id="22731-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22731-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="22731-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="22731-133">Namespace</span></span><br/>                | <span data-ttu-id="22731-134">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="22731-134">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="22731-135">MOF</span><span class="sxs-lookup"><span data-stu-id="22731-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22731-136"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22731-136"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="22731-137">DLL</span><span class="sxs-lookup"><span data-stu-id="22731-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22731-138"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22731-138"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22731-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22731-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22731-140">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="22731-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
