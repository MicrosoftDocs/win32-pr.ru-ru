---
description: Абстракция порта или точки соединения устройства.
ms.assetid: ee725c64-587b-4e5f-9b1c-7a58902b0631
title: Класс CIM_LogicalPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalPort
- CIM_LogicalPort.Speed
- CIM_LogicalPort.MaxSpeed
- CIM_LogicalPort.RequestedSpeed
- CIM_LogicalPort.UsageRestriction
- CIM_LogicalPort.PortType
- CIM_LogicalPort.OtherPortType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eeed69e9669048377340cb0ca21e7a2e89f4baff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990872"
---
# <a name="cim_logicalport-class"></a><span data-ttu-id="369a3-103">\_Класс CIM логикалпорт</span><span class="sxs-lookup"><span data-stu-id="369a3-103">CIM\_LogicalPort class</span></span>

<span data-ttu-id="369a3-104">Абстракция порта или точки соединения устройства.</span><span class="sxs-lookup"><span data-stu-id="369a3-104">The abstraction of a port or connection point of a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="369a3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="369a3-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_LogicalPort : CIM_LogicalDevice
{
  uint64 Speed;
  uint64 MaxSpeed;
  uint64 RequestedSpeed;
  uint16 UsageRestriction;
  uint16 PortType;
  string OtherPortType;
};
```

## <a name="members"></a><span data-ttu-id="369a3-106">Члены</span><span class="sxs-lookup"><span data-stu-id="369a3-106">Members</span></span>

<span data-ttu-id="369a3-107">Класс **CIM \_ логикалпорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="369a3-107">The **CIM\_LogicalPort** class has these types of members:</span></span>

-   [<span data-ttu-id="369a3-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="369a3-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="369a3-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="369a3-109">Properties</span></span>

<span data-ttu-id="369a3-110">Класс **CIM \_ логикалпорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="369a3-110">The **CIM\_LogicalPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="369a3-111">**максспид**</span><span class="sxs-lookup"><span data-stu-id="369a3-111">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369a3-112">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="369a3-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="369a3-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="369a3-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369a3-114">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("бит в секунду"), **Пунит** ("бит/сек")</span><span class="sxs-lookup"><span data-stu-id="369a3-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="369a3-115">Максимальная пропускная способность порта (в битах в секунду).</span><span class="sxs-lookup"><span data-stu-id="369a3-115">The maximum bandwidth of the port, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="369a3-116">**осерпорттипе**</span><span class="sxs-lookup"><span data-stu-id="369a3-116">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369a3-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="369a3-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="369a3-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="369a3-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369a3-119">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ логикалпорт**.**PortType**")</span><span class="sxs-lookup"><span data-stu-id="369a3-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalPort**.**PortType**")</span></span>
</dt> </dl>

<span data-ttu-id="369a3-120">Описывает тип модуля, когда для **portType** задано значение **other** ("1").</span><span class="sxs-lookup"><span data-stu-id="369a3-120">Describes the type of module, when **PortType** is set to **Other** ("1").</span></span>

</dd> <dt>

<span data-ttu-id="369a3-121">**Порта**</span><span class="sxs-lookup"><span data-stu-id="369a3-121">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369a3-122">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="369a3-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="369a3-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="369a3-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369a3-124">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ нетворкпорт**](cim-networkport.md).**Осернетворкпорттипе**")</span><span class="sxs-lookup"><span data-stu-id="369a3-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_NetworkPort**](cim-networkport.md).**OtherNetworkPortType**")</span></span>
</dt> </dl>

<span data-ttu-id="369a3-125">Тип порта.</span><span class="sxs-lookup"><span data-stu-id="369a3-125">The port type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="369a3-126">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="369a3-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="369a3-127">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="369a3-127">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="369a3-128">**Неприменимо** (2)</span><span class="sxs-lookup"><span data-stu-id="369a3-128">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="369a3-129">**Зарезервировано DMTF** (3.. 15999)</span><span class="sxs-lookup"><span data-stu-id="369a3-129">**DMTF Reserved** (3..15999)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="369a3-130">**Поставщик зарезервирован** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="369a3-130">**Vendor Reserved** (16000..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="369a3-131">**рекуестедспид**</span><span class="sxs-lookup"><span data-stu-id="369a3-131">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369a3-132">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="369a3-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="369a3-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="369a3-133">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="369a3-134">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("бит в секунду"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ логикалпорт**.**Speed**"), **Пунит** (" бит/сек ")</span><span class="sxs-lookup"><span data-stu-id="369a3-134">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalPort**.**Speed**"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="369a3-135">Запрошенная пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="369a3-135">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="369a3-136">Фактическая пропускная способность указывается в свойстве **Speed** .</span><span class="sxs-lookup"><span data-stu-id="369a3-136">The actual bandwidth is reported in the **Speed** property.</span></span>

</dd> <dt>

<span data-ttu-id="369a3-137">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="369a3-137">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369a3-138">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="369a3-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="369a3-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="369a3-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="369a3-140">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("бит в секунду"), **Пунит** ("бит/сек")</span><span class="sxs-lookup"><span data-stu-id="369a3-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="369a3-141">Пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="369a3-141">The bandwidth of the port, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="369a3-142">**усажерестриктион**</span><span class="sxs-lookup"><span data-stu-id="369a3-142">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="369a3-143">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="369a3-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="369a3-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="369a3-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="369a3-145">Указывает, ограничен ли порт внешним интерфейсом или внутренним портом.</span><span class="sxs-lookup"><span data-stu-id="369a3-145">Indicates whether the port is restricted to being a front-end or back-end port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="369a3-146">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="369a3-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>

<span data-ttu-id="369a3-147">**Только внешний** интерфейс (2)</span><span class="sxs-lookup"><span data-stu-id="369a3-147">**Front-end only** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>

<span data-ttu-id="369a3-148">**Только серверная** части (3)</span><span class="sxs-lookup"><span data-stu-id="369a3-148">**Back-end only** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>

<span data-ttu-id="369a3-149">**Не ограничено** (4)</span><span class="sxs-lookup"><span data-stu-id="369a3-149">**Not restricted** (4)</span></span>


<span data-ttu-id="369a3-150"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="369a3-150"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="369a3-151">Требования</span><span class="sxs-lookup"><span data-stu-id="369a3-151">Requirements</span></span>



| <span data-ttu-id="369a3-152">Требование</span><span class="sxs-lookup"><span data-stu-id="369a3-152">Requirement</span></span> | <span data-ttu-id="369a3-153">Значение</span><span class="sxs-lookup"><span data-stu-id="369a3-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="369a3-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="369a3-154">Minimum supported client</span></span><br/> | <span data-ttu-id="369a3-155">Windows 8</span><span class="sxs-lookup"><span data-stu-id="369a3-155">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="369a3-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="369a3-156">Minimum supported server</span></span><br/> | <span data-ttu-id="369a3-157">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="369a3-157">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="369a3-158">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="369a3-158">Namespace</span></span><br/>                | <span data-ttu-id="369a3-159">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="369a3-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="369a3-160">MOF</span><span class="sxs-lookup"><span data-stu-id="369a3-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="369a3-161"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="369a3-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="369a3-162">DLL</span><span class="sxs-lookup"><span data-stu-id="369a3-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="369a3-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="369a3-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="369a3-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="369a3-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="369a3-165">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="369a3-165">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

