---
description: Описание возможностей и управления последовательным контроллером.
ms.assetid: ce3e0424-4ab8-435d-a155-1164535b3b0d
title: Класс CIM_SerialController (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialController
- CIM_SerialController.Capabilities
- CIM_SerialController.CapabilityDescriptions
- CIM_SerialController.MaxBaudRate
- CIM_SerialController.Security
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4a2e69bab38bb8b68c15ed93b2bee721c35a7600
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682808"
---
# <a name="cim_serialcontroller-class-hyper-v-management"></a><span data-ttu-id="e7ad4-103">Класс CIM_SerialController (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="e7ad4-103">CIM_SerialController class (Hyper-V management)</span></span>

<span data-ttu-id="e7ad4-104">Описание возможностей и управления последовательным контроллером.</span><span class="sxs-lookup"><span data-stu-id="e7ad4-104">Describes the capabilities and management of a serial controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7ad4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7ad4-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_SerialController : CIM_Controller
{
  uint16 Capabilities[];
  string CapabilityDescriptions[];
  uint32 MaxBaudRate;
  uint16 Security;
};
```

## <a name="members"></a><span data-ttu-id="e7ad4-106">Члены</span><span class="sxs-lookup"><span data-stu-id="e7ad4-106">Members</span></span>

<span data-ttu-id="e7ad4-107">Класс **CIM \_ сериалконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e7ad4-107">The **CIM\_SerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="e7ad4-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="e7ad4-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7ad4-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="e7ad4-109">Properties</span></span>

<span data-ttu-id="e7ad4-110">Класс **CIM \_ сериалконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e7ad4-110">The **CIM\_SerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e7ad4-111">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="e7ad4-111">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7ad4-112">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e7ad4-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e7ad4-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e7ad4-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7ad4-114">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Последовательные порты DMTF \| 004,7 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сериалконтроллер**.**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="e7ad4-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SerialController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="e7ad4-115">Совместимость уровня микросхемы для контроллера последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="e7ad4-115">The chip level compatibility for the serial controller.</span></span> <span data-ttu-id="e7ad4-116">Это свойство описывает буферизацию и другие возможности последовательного контроллера, которые могут быть встроенными в оборудование микросхемы.</span><span class="sxs-lookup"><span data-stu-id="e7ad4-116">This property describes the buffering and other capabilities of the serial controller that might be inherent in the chip hardware.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e7ad4-117">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="e7ad4-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e7ad4-118">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="e7ad4-118">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="e7ad4-119">**XT/AT-совместимый** (3)</span><span class="sxs-lookup"><span data-stu-id="e7ad4-119">**XT/AT Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

<span data-ttu-id="e7ad4-120">**Совместимость с 16450** (4)</span><span class="sxs-lookup"><span data-stu-id="e7ad4-120">**16450 Compatible** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

<span data-ttu-id="e7ad4-121">**Совместимость с 16550** (5)</span><span class="sxs-lookup"><span data-stu-id="e7ad4-121">**16550 Compatible** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

<span data-ttu-id="e7ad4-122">**16550A-совместимый** (6)</span><span class="sxs-lookup"><span data-stu-id="e7ad4-122">**16550A Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="e7ad4-123">**Совместимость с 8251** (160)</span><span class="sxs-lookup"><span data-stu-id="e7ad4-123">**8251 Compatible** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

<span data-ttu-id="e7ad4-124">**8251FIFO-совместимый** (161)</span><span class="sxs-lookup"><span data-stu-id="e7ad4-124">**8251FIFO Compatible** (161)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e7ad4-125">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="e7ad4-125">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7ad4-126">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="e7ad4-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e7ad4-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e7ad4-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7ad4-128">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сериалконтроллер**.**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="e7ad4-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SerialController**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="e7ad4-129">Массив, содержащий более подробные объяснения функций последовательного контроллера в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="e7ad4-129">An array that contains more detailed explanations for serial controller features in the **Capabilities** array.</span></span> <span data-ttu-id="e7ad4-130">Элементы в массиве **капабилитидескриптионс** сопоставляются с элементами в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="e7ad4-130">The items in the **CapabilityDescriptions** array correlate to those in the **Capabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="e7ad4-131">**максбаудрате**</span><span class="sxs-lookup"><span data-stu-id="e7ad4-131">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7ad4-132">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e7ad4-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7ad4-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e7ad4-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7ad4-134">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("бит в секунду"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Последовательные порты DMTF \| 004,6 "), **Пунит** (" бит/сек ")</span><span class="sxs-lookup"><span data-stu-id="e7ad4-134">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.6"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="e7ad4-135">Максимальная скорость в битах в секунду, поддерживаемая последовательным контроллером.</span><span class="sxs-lookup"><span data-stu-id="e7ad4-135">The maximum baud rate in, bits per second, that is supported by the serial controller.</span></span>

</dd> <dt>

<span data-ttu-id="e7ad4-136">**Безопасность**</span><span class="sxs-lookup"><span data-stu-id="e7ad4-136">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7ad4-137">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e7ad4-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e7ad4-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e7ad4-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7ad4-139">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Последовательные порты DMTF \| 004,9 ")</span><span class="sxs-lookup"><span data-stu-id="e7ad4-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="e7ad4-140">Операционная безопасность контроллера.</span><span class="sxs-lookup"><span data-stu-id="e7ad4-140">The operational security for the controller.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e7ad4-141">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="e7ad4-141">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e7ad4-142">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="e7ad4-142">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="e7ad4-143">**Нет** (3)</span><span class="sxs-lookup"><span data-stu-id="e7ad4-143">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="External_Interface_Locked_Out"></span><span id="external_interface_locked_out"></span><span id="EXTERNAL_INTERFACE_LOCKED_OUT"></span>

<span data-ttu-id="e7ad4-144">**Внешний интерфейс заблокирован** (4)</span><span class="sxs-lookup"><span data-stu-id="e7ad4-144">**External Interface Locked Out** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="External_Interface_Enabled"></span><span id="external_interface_enabled"></span><span id="EXTERNAL_INTERFACE_ENABLED"></span>

<span data-ttu-id="e7ad4-145">**Включен внешний интерфейс** (5)</span><span class="sxs-lookup"><span data-stu-id="e7ad4-145">**External Interface Enabled** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

<span data-ttu-id="e7ad4-146">**Обход загрузки** (6)</span><span class="sxs-lookup"><span data-stu-id="e7ad4-146">**Boot Bypass** (6)</span></span>


<span data-ttu-id="e7ad4-147"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e7ad4-147"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e7ad4-148">Требования</span><span class="sxs-lookup"><span data-stu-id="e7ad4-148">Requirements</span></span>



| <span data-ttu-id="e7ad4-149">Требование</span><span class="sxs-lookup"><span data-stu-id="e7ad4-149">Requirement</span></span> | <span data-ttu-id="e7ad4-150">Значение</span><span class="sxs-lookup"><span data-stu-id="e7ad4-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7ad4-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7ad4-151">Minimum supported client</span></span><br/> | <span data-ttu-id="e7ad4-152">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e7ad4-152">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e7ad4-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7ad4-153">Minimum supported server</span></span><br/> | <span data-ttu-id="e7ad4-154">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e7ad4-154">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e7ad4-155">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e7ad4-155">Namespace</span></span><br/>                | <span data-ttu-id="e7ad4-156">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e7ad4-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e7ad4-157">MOF</span><span class="sxs-lookup"><span data-stu-id="e7ad4-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7ad4-158"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7ad4-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7ad4-159">DLL</span><span class="sxs-lookup"><span data-stu-id="e7ad4-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7ad4-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e7ad4-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e7ad4-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7ad4-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7ad4-162">**\_Контроллер CIM**</span><span class="sxs-lookup"><span data-stu-id="e7ad4-162">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

