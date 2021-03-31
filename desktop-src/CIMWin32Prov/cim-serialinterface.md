---
description: Класс CIM \_ сериалинтерфаце представляет \_ отношение CIM контролледби, указывающее, к каким устройствам осуществляется доступ через последовательный контроллер и характеристики доступа.
ms.assetid: bebc304a-c2b7-41c7-b24a-8f450ee3c4bb
ms.tgt_platform: multiple
title: Класс CIM_SerialInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialInterface
- CIM_SerialInterface.NegotiatedDataWidth
- CIM_SerialInterface.NegotiatedSpeed
- CIM_SerialInterface.AccessState
- CIM_SerialInterface.NumberOfHardResets
- CIM_SerialInterface.NumberOfSoftResets
- CIM_SerialInterface.Dependent
- CIM_SerialInterface.Antecedent
- CIM_SerialInterface.FlowControlInfo
- CIM_SerialInterface.NumberOfStopBits
- CIM_SerialInterface.ParityInfo
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1df787ff64798f412035a72e6db6d7b01b4b9b0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895793"
---
# <a name="cim_serialinterface-class"></a><span data-ttu-id="ca4bd-103">\_Класс CIM сериалинтерфаце</span><span class="sxs-lookup"><span data-stu-id="ca4bd-103">CIM\_SerialInterface class</span></span>

<span data-ttu-id="ca4bd-104">Класс **CIM \_ сериалинтерфаце** представляет отношение [**CIM \_ контролледби**](cim-controlledby.md) , указывающее, к каким устройствам осуществляется доступ через последовательный контроллер и характеристики доступа.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-104">The **CIM\_SerialInterface** class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through the serial controller and the characteristics of the access.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ca4bd-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ca4bd-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ca4bd-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ca4bd-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ca4bd-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca4bd-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca4bd-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8B309BDA-E3D4-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SerialInterface : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  CIM_LogicalDevice    REF Dependent;
  CIM_SerialController REF Antecedent;
  uint16                   FlowControlInfo;
  uint16                   NumberOfStopBits;
  uint16                   ParityInfo;
};
```

## <a name="members"></a><span data-ttu-id="ca4bd-110">Члены</span><span class="sxs-lookup"><span data-stu-id="ca4bd-110">Members</span></span>

<span data-ttu-id="ca4bd-111">Класс **CIM \_ сериалинтерфаце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ca4bd-111">The **CIM\_SerialInterface** class has these types of members:</span></span>

-   [<span data-ttu-id="ca4bd-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="ca4bd-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ca4bd-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="ca4bd-113">Properties</span></span>

<span data-ttu-id="ca4bd-114">Класс **CIM \_ сериалинтерфаце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-114">The **CIM\_SerialInterface** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca4bd-115">**акцессстате**</span><span class="sxs-lookup"><span data-stu-id="ca4bd-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca4bd-116">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca4bd-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca4bd-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca4bd-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca4bd-118">Указывает, является ли контроллер активной командой или доступом к устройству.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="ca4bd-119">Эти сведения необходимы в том случае, если логическое устройство может быть командо или доступно через несколько контроллеров.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="ca4bd-120">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="ca4bd-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ca4bd-121">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ca4bd-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="ca4bd-122">**Активно** (1)</span><span class="sxs-lookup"><span data-stu-id="ca4bd-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="ca4bd-123">**Неактивно** (2)</span><span class="sxs-lookup"><span data-stu-id="ca4bd-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ca4bd-124">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="ca4bd-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca4bd-125">Тип данных: **CIM \_ сериалконтроллер**</span><span class="sxs-lookup"><span data-stu-id="ca4bd-125">Data type: **CIM\_SerialController**</span></span>
</dt> <dt>

<span data-ttu-id="ca4bd-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca4bd-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca4bd-127">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="ca4bd-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ca4bd-128">[**\_ Сериалконтроллер CIM**](cim-serialcontroller.md) , описывающий последовательный контроллер.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-128">A [**CIM\_SerialController**](cim-serialcontroller.md) that describes the serial controller.</span></span>

</dd> <dt>

<span data-ttu-id="ca4bd-129">**Него**</span><span class="sxs-lookup"><span data-stu-id="ca4bd-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca4bd-130">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="ca4bd-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="ca4bd-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca4bd-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca4bd-132">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="ca4bd-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ca4bd-133">Логическая [**модель \_ CIM**](cim-logicaldevice.md) , описывающая логическое устройство.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-133">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="ca4bd-134">**фловконтролинфо**</span><span class="sxs-lookup"><span data-stu-id="ca4bd-134">**FlowControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca4bd-135">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca4bd-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca4bd-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca4bd-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca4bd-137">Указывает поток управления для передаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-137">Indicates the flow control for transmitted data.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ca4bd-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ca4bd-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="ca4bd-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="ca4bd-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="ca4bd-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Нет** (2)</span><span class="sxs-lookup"><span data-stu-id="ca4bd-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>

<span data-ttu-id="ca4bd-141"><span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>**Ксонксофф** (3)</span><span class="sxs-lookup"><span data-stu-id="ca4bd-141"><span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>**XonXoff** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="RTS_CTS"></span><span id="rts_cts"></span>

<span data-ttu-id="ca4bd-142"><span id="RTS_CTS"></span><span id="rts_cts"></span>**RTS/CTS** (4)</span><span class="sxs-lookup"><span data-stu-id="ca4bd-142"><span id="RTS_CTS"></span><span id="rts_cts"></span>**RTS/CTS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>

<span data-ttu-id="ca4bd-143"><span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>**Ксонксофф и RTS/CTS** (5)</span><span class="sxs-lookup"><span data-stu-id="ca4bd-143"><span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>**Both XonXoff and RTS/CTS** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ca4bd-144">Ксонксофф и RTS/CTS</span><span class="sxs-lookup"><span data-stu-id="ca4bd-144">XonXoff and RTS/CTS</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ca4bd-145">**неготиатеддатавидс**</span><span class="sxs-lookup"><span data-stu-id="ca4bd-145">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca4bd-146">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca4bd-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca4bd-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca4bd-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca4bd-148">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("биты")</span><span class="sxs-lookup"><span data-stu-id="ca4bd-148">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="ca4bd-149">Если возможно несколько значений ширины данных для шины или соединения, это свойство определяет, какое из них используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-149">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="ca4bd-150">Ширина данных указывается в битах.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-150">Data width is specified in bits.</span></span> <span data-ttu-id="ca4bd-151">Если ширина данных не согласована или если эта информация недоступна или важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="ca4bd-151">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="ca4bd-152">Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="ca4bd-152">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca4bd-153">**неготиатедспид**</span><span class="sxs-lookup"><span data-stu-id="ca4bd-153">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca4bd-154">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ca4bd-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ca4bd-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca4bd-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca4bd-156">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="ca4bd-156">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="ca4bd-157">Если возможны несколько скоростей шины или соединения, это свойство определяет, какое из них используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-157">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="ca4bd-158">Скорость указывается в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-158">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="ca4bd-159">Если скорость подключения или шины не согласована или если эта информация недоступна или не важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="ca4bd-159">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="ca4bd-160">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ca4bd-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="ca4bd-161">Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="ca4bd-161">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca4bd-162">**нумберофхардресетс**</span><span class="sxs-lookup"><span data-stu-id="ca4bd-162">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca4bd-163">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca4bd-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca4bd-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca4bd-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca4bd-165">Число жестких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-165">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="ca4bd-166">При жесткой сбросе устройство возвращается в состояние инициализации или загрузки.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-166">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="ca4bd-167">Все внутренние сведения о состоянии устройства и данные теряются.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-167">All internal device state information and data are lost.</span></span>

<span data-ttu-id="ca4bd-168">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="ca4bd-168">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca4bd-169">**нумберофсофтресетс**</span><span class="sxs-lookup"><span data-stu-id="ca4bd-169">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca4bd-170">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca4bd-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca4bd-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca4bd-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca4bd-172">Количество мягких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-172">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="ca4bd-173">При мягком сбросе текущее состояние и данные устройства не полностью очищаются.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-173">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="ca4bd-174">Точная семантика зависит от устройства и от протоколов и механизмов, используемых для связи с ним.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-174">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="ca4bd-175">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="ca4bd-175">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca4bd-176">**нумберофстопбитс**</span><span class="sxs-lookup"><span data-stu-id="ca4bd-176">**NumberOfStopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca4bd-177">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca4bd-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca4bd-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca4bd-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca4bd-179">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("биты")</span><span class="sxs-lookup"><span data-stu-id="ca4bd-179">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="ca4bd-180">Количество останавливаемых битов для передачи.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-180">Number of stop bits to transmit.</span></span>

</dd> <dt>

<span data-ttu-id="ca4bd-181">**паритинфо**</span><span class="sxs-lookup"><span data-stu-id="ca4bd-181">**ParityInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca4bd-182">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca4bd-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca4bd-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca4bd-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca4bd-184">Сведения о параметре четности для передаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-184">Information about the parity setting for transmitted data.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ca4bd-185">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ca4bd-185">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="ca4bd-186">**Нет** (1)</span><span class="sxs-lookup"><span data-stu-id="ca4bd-186">**None** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span data-ttu-id="ca4bd-187">**Даже** (2)</span><span class="sxs-lookup"><span data-stu-id="ca4bd-187">**Even** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span data-ttu-id="ca4bd-188">**Нечетная** (3)</span><span class="sxs-lookup"><span data-stu-id="ca4bd-188">**Odd** (3)</span></span>


<span data-ttu-id="ca4bd-189"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ca4bd-189"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="ca4bd-190">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca4bd-190">Remarks</span></span>

<span data-ttu-id="ca4bd-191">Класс **CIM \_ сериалинтерфаце** является производным от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="ca4bd-191">The **CIM\_SerialInterface** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="ca4bd-192">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-192">WMI does not implement this class.</span></span>

<span data-ttu-id="ca4bd-193">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-193">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ca4bd-194">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="ca4bd-194">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca4bd-195">Требования</span><span class="sxs-lookup"><span data-stu-id="ca4bd-195">Requirements</span></span>



| <span data-ttu-id="ca4bd-196">Требование</span><span class="sxs-lookup"><span data-stu-id="ca4bd-196">Requirement</span></span> | <span data-ttu-id="ca4bd-197">Значение</span><span class="sxs-lookup"><span data-stu-id="ca4bd-197">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca4bd-198">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca4bd-198">Minimum supported client</span></span><br/> | <span data-ttu-id="ca4bd-199">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca4bd-199">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ca4bd-200">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca4bd-200">Minimum supported server</span></span><br/> | <span data-ttu-id="ca4bd-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca4bd-201">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ca4bd-202">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ca4bd-202">Namespace</span></span><br/>                | <span data-ttu-id="ca4bd-203">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ca4bd-203">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ca4bd-204">MOF</span><span class="sxs-lookup"><span data-stu-id="ca4bd-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca4bd-205"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca4bd-205"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca4bd-206">DLL</span><span class="sxs-lookup"><span data-stu-id="ca4bd-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca4bd-207"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca4bd-207"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca4bd-208">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca4bd-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca4bd-209">**\_КОНТРОЛЛЕДБИ CIM**</span><span class="sxs-lookup"><span data-stu-id="ca4bd-209">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 

