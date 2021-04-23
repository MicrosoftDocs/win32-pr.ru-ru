---
description: Представляет ЭЛТ-монитор рабочего стола.
ms.assetid: 26a06320-9fd9-434e-87c8-486e9ca4945c
title: Класс CIM_DesktopMonitor (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DesktopMonitor
- CIM_DesktopMonitor.DisplayType
- CIM_DesktopMonitor.Bandwidth
- CIM_DesktopMonitor.ScreenHeight
- CIM_DesktopMonitor.ScreenWidth
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab152fc10f3fd404744c293d2368039ffcfdb291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662603"
---
# <a name="cim_desktopmonitor-class-hyper-v-management"></a><span data-ttu-id="c2036-103">Класс CIM_DesktopMonitor (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="c2036-103">CIM_DesktopMonitor class (Hyper-V management)</span></span>

<span data-ttu-id="c2036-104">Представляет ЭЛТ-монитор рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="c2036-104">Represents a CRT desktop monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2036-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2036-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices")]
class CIM_DesktopMonitor : CIM_Display
{
  uint16 DisplayType;
  uint32 Bandwidth;
  uint32 ScreenHeight;
  uint32 ScreenWidth;
};
```

## <a name="members"></a><span data-ttu-id="c2036-106">Члены</span><span class="sxs-lookup"><span data-stu-id="c2036-106">Members</span></span>

<span data-ttu-id="c2036-107">Класс **CIM \_ десктопмонитор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c2036-107">The **CIM\_DesktopMonitor** class has these types of members:</span></span>

-   [<span data-ttu-id="c2036-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="c2036-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2036-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c2036-109">Properties</span></span>

<span data-ttu-id="c2036-110">Класс **CIM \_ десктопмонитор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c2036-110">The **CIM\_DesktopMonitor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2036-111">**Пропускная способность**</span><span class="sxs-lookup"><span data-stu-id="c2036-111">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2036-112">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2036-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2036-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c2036-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2036-114">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("мегагерц"), **Пунит** ("Герц \* 10 ^ 6")</span><span class="sxs-lookup"><span data-stu-id="c2036-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MegaHertz"), **PUnit** ("hertz \* 10^6")</span></span>
</dt> </dl>

<span data-ttu-id="c2036-115">Пропускная способность дисплея в Мхертз.</span><span class="sxs-lookup"><span data-stu-id="c2036-115">The bandwidth of the display, in MHertz.</span></span> <span data-ttu-id="c2036-116">"0" означает неизвестное значение.</span><span class="sxs-lookup"><span data-stu-id="c2036-116">"0" indicates unknown.</span></span>

</dd> <dt>

<span data-ttu-id="c2036-117">**дисплайтипе**</span><span class="sxs-lookup"><span data-stu-id="c2036-117">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2036-118">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c2036-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c2036-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c2036-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2036-120">Тип типа отображения ЭЛТ-монитора.</span><span class="sxs-lookup"><span data-stu-id="c2036-120">The type of display type of the CRT monitor.</span></span> <span data-ttu-id="c2036-121">Например, многосканирование или монохромный цвет.</span><span class="sxs-lookup"><span data-stu-id="c2036-121">For example, multiscan color, or monochrome.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c2036-122">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="c2036-122">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c2036-123">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="c2036-123">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Color"></span><span id="multiscan_color"></span><span id="MULTISCAN_COLOR"></span>

<span data-ttu-id="c2036-124">**Цвет для многосканирования** (2)</span><span class="sxs-lookup"><span data-stu-id="c2036-124">**Multiscan Color** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Monochrome"></span><span id="multiscan_monochrome"></span><span id="MULTISCAN_MONOCHROME"></span>

<span data-ttu-id="c2036-125">**Многосканерная Монохромная** (3)</span><span class="sxs-lookup"><span data-stu-id="c2036-125">**Multiscan Monochrome** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Color"></span><span id="fixed_frequency_color"></span><span id="FIXED_FREQUENCY_COLOR"></span>

<span data-ttu-id="c2036-126">**Фиксированный цвет частоты** (4)</span><span class="sxs-lookup"><span data-stu-id="c2036-126">**Fixed Frequency Color** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Monochrome"></span><span id="fixed_frequency_monochrome"></span><span id="FIXED_FREQUENCY_MONOCHROME"></span>

<span data-ttu-id="c2036-127">**Фиксированная частота монохромных** (5)</span><span class="sxs-lookup"><span data-stu-id="c2036-127">**Fixed Frequency Monochrome** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c2036-128">**скринхеигхт**</span><span class="sxs-lookup"><span data-stu-id="c2036-128">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2036-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2036-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2036-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c2036-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2036-131">Логическая высота дисплея в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="c2036-131">The logical height of the display, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="c2036-132">**скринвидс**</span><span class="sxs-lookup"><span data-stu-id="c2036-132">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2036-133">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2036-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2036-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c2036-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2036-135">Логическая ширина дисплея в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="c2036-135">The logical width of the display, in screen coordinates.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2036-136">Требования</span><span class="sxs-lookup"><span data-stu-id="c2036-136">Requirements</span></span>



| <span data-ttu-id="c2036-137">Требование</span><span class="sxs-lookup"><span data-stu-id="c2036-137">Requirement</span></span> | <span data-ttu-id="c2036-138">Значение</span><span class="sxs-lookup"><span data-stu-id="c2036-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2036-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2036-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c2036-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c2036-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c2036-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2036-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c2036-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c2036-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c2036-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c2036-143">Namespace</span></span><br/>                | <span data-ttu-id="c2036-144">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c2036-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c2036-145">MOF</span><span class="sxs-lookup"><span data-stu-id="c2036-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2036-146"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2036-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2036-147">DLL</span><span class="sxs-lookup"><span data-stu-id="c2036-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2036-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c2036-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c2036-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2036-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2036-150">**\_Отображение CIM**</span><span class="sxs-lookup"><span data-stu-id="c2036-150">**CIM\_Display**</span></span>](cim-display.md)
</dt> </dl>

 

