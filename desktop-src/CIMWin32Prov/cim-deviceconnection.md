---
description: '\_Класс СОПОСТАВЛЕНИЯ CIM девицеконнектион представляет два или более подключенных устройства.'
ms.assetid: 82095cd6-1843-4db2-9fe8-3e225611bd3b
ms.tgt_platform: multiple
title: Класс CIM_DeviceConnection (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceConnection
- CIM_DeviceConnection.Dependent
- CIM_DeviceConnection.Antecedent
- CIM_DeviceConnection.NegotiatedDataWidth
- CIM_DeviceConnection.NegotiatedSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b8179287686439ea31c19d700a785de7fff47659
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262673"
---
# <a name="cim_deviceconnection-class-cimwin32-wmi-providers"></a><span data-ttu-id="0797b-103">Класс CIM_DeviceConnection (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="0797b-103">CIM_DeviceConnection class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="0797b-104">Класс сопоставления **CIM \_ девицеконнектион** представляет два или более подключенных устройства.</span><span class="sxs-lookup"><span data-stu-id="0797b-104">The **CIM\_DeviceConnection** association class represents two or more connected devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0797b-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="0797b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0797b-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0797b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0797b-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="0797b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0797b-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="0797b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0797b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0797b-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DeviceConnection : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_LogicalDevice REF Antecedent;
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
};
```

## <a name="members"></a><span data-ttu-id="0797b-110">Члены</span><span class="sxs-lookup"><span data-stu-id="0797b-110">Members</span></span>

<span data-ttu-id="0797b-111">Класс **CIM \_ девицеконнектион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0797b-111">The **CIM\_DeviceConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="0797b-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="0797b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0797b-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="0797b-113">Properties</span></span>

<span data-ttu-id="0797b-114">Класс **CIM \_ девицеконнектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0797b-114">The **CIM\_DeviceConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0797b-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="0797b-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0797b-116">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="0797b-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="0797b-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0797b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0797b-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="0797b-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="0797b-119">Логическая [**модель \_ CIM**](cim-logicaldevice.md) , описывающая логическое устройство.</span><span class="sxs-lookup"><span data-stu-id="0797b-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes a logical device.</span></span>

</dd> <dt>

<span data-ttu-id="0797b-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="0797b-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0797b-121">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="0797b-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="0797b-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0797b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0797b-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="0797b-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="0797b-124">Логическое значение типа [**CIM \_**](cim-logicaldevice.md) , которое описывает второе логическое устройство, подключенное к предшествующему устройству.</span><span class="sxs-lookup"><span data-stu-id="0797b-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes a second logical device connected to the Antecedent device.</span></span>

</dd> <dt>

<span data-ttu-id="0797b-125">**неготиатеддатавидс**</span><span class="sxs-lookup"><span data-stu-id="0797b-125">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0797b-126">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0797b-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0797b-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0797b-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0797b-128">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("биты")</span><span class="sxs-lookup"><span data-stu-id="0797b-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="0797b-129">Если возможно несколько значений ширины данных для шины или соединения, это свойство определяет, какое из них используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="0797b-129">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="0797b-130">Ширина данных указывается в битах.</span><span class="sxs-lookup"><span data-stu-id="0797b-130">Data width is specified in bits.</span></span> <span data-ttu-id="0797b-131">Если ширина данных не согласована или если эта информация недоступна или важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="0797b-131">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="0797b-132">**неготиатедспид**</span><span class="sxs-lookup"><span data-stu-id="0797b-132">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0797b-133">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0797b-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0797b-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0797b-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0797b-135">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="0797b-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="0797b-136">Если возможны несколько скоростей шины или соединения, это свойство определяет, какое из них используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="0797b-136">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="0797b-137">Скорость указывается в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="0797b-137">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="0797b-138">Если скорость подключения или шины не согласована или если эта информация недоступна или не важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="0797b-138">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="0797b-139">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0797b-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0797b-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0797b-140">Remarks</span></span>

<span data-ttu-id="0797b-141">Класс **CIM \_ девицеконнектион** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="0797b-141">The **CIM\_DeviceConnection** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="0797b-142">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="0797b-142">WMI does not implement this class.</span></span> <span data-ttu-id="0797b-143">Дополнительные сведения о классах, производных от **CIM \_ девицеконнектион**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0797b-143">For more information about classes derived from **CIM\_DeviceConnection**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0797b-144">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="0797b-144">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0797b-145">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0797b-145">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0797b-146">Требования</span><span class="sxs-lookup"><span data-stu-id="0797b-146">Requirements</span></span>



| <span data-ttu-id="0797b-147">Требование</span><span class="sxs-lookup"><span data-stu-id="0797b-147">Requirement</span></span> | <span data-ttu-id="0797b-148">Значение</span><span class="sxs-lookup"><span data-stu-id="0797b-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0797b-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0797b-149">Minimum supported client</span></span><br/> | <span data-ttu-id="0797b-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0797b-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0797b-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0797b-151">Minimum supported server</span></span><br/> | <span data-ttu-id="0797b-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0797b-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0797b-153">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0797b-153">Namespace</span></span><br/>                | <span data-ttu-id="0797b-154">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0797b-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0797b-155">MOF</span><span class="sxs-lookup"><span data-stu-id="0797b-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0797b-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0797b-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0797b-157">DLL</span><span class="sxs-lookup"><span data-stu-id="0797b-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0797b-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0797b-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0797b-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0797b-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0797b-160">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="0797b-160">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

