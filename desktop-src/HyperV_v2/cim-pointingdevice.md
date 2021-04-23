---
description: Представляет устройство, используемое для указания областей экрана.
ms.assetid: ffc675c3-29bd-4c54-8e54-8b6212daf66d
title: Класс CIM_PointingDevice (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PointingDevice
- CIM_PointingDevice.PointingType
- CIM_PointingDevice.NumberOfButtons
- CIM_PointingDevice.Handedness
- CIM_PointingDevice.Resolution
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57cca8c81a2d363e9e31bfc958a75b71e1b910d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156947"
---
# <a name="cim_pointingdevice-class-hyper-v-management"></a><span data-ttu-id="e98f0-103">Класс CIM_PointingDevice (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="e98f0-103">CIM_PointingDevice class (Hyper-V management)</span></span>

<span data-ttu-id="e98f0-104">Представляет устройство, используемое для указания областей экрана.</span><span class="sxs-lookup"><span data-stu-id="e98f0-104">Represents a device used to point to regions of a display.</span></span>

## <a name="syntax"></a><span data-ttu-id="e98f0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e98f0-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_PointingDevice : CIM_UserDevice
{
  uint16 PointingType;
  uint8  NumberOfButtons;
  uint16 Handedness;
  uint32 Resolution;
};
```

## <a name="members"></a><span data-ttu-id="e98f0-106">Члены</span><span class="sxs-lookup"><span data-stu-id="e98f0-106">Members</span></span>

<span data-ttu-id="e98f0-107">Класс **CIM \_ поинтингдевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e98f0-107">The **CIM\_PointingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="e98f0-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="e98f0-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e98f0-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="e98f0-109">Properties</span></span>

<span data-ttu-id="e98f0-110">Класс **CIM \_ поинтингдевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e98f0-110">The **CIM\_PointingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e98f0-111">**Правой или левой**</span><span class="sxs-lookup"><span data-stu-id="e98f0-111">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e98f0-112">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e98f0-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e98f0-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e98f0-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e98f0-114">Указывает, настроено ли указывающее устройство для работы с правой или левой рукой.</span><span class="sxs-lookup"><span data-stu-id="e98f0-114">Indicates whether the pointing device is configured for right or left handed operation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e98f0-115">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="e98f0-115">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e98f0-116">**Неприменимо** (1)</span><span class="sxs-lookup"><span data-stu-id="e98f0-116">**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>

<span data-ttu-id="e98f0-117">**Правая операция** (2)</span><span class="sxs-lookup"><span data-stu-id="e98f0-117">**Right Handed Operation** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>

<span data-ttu-id="e98f0-118">**Левая операция** (3)</span><span class="sxs-lookup"><span data-stu-id="e98f0-118">**Left Handed Operation** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e98f0-119">**нумберофбуттонс**</span><span class="sxs-lookup"><span data-stu-id="e98f0-119">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e98f0-120">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e98f0-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e98f0-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e98f0-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e98f0-122">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Указывающее устройство в DMTF \| 003,4 ")</span><span class="sxs-lookup"><span data-stu-id="e98f0-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Pointing Device\|003.4")</span></span>
</dt> </dl>

<span data-ttu-id="e98f0-123">Число кнопок на устройстве.</span><span class="sxs-lookup"><span data-stu-id="e98f0-123">The number of buttons on the device.</span></span> <span data-ttu-id="e98f0-124">Если указывающее устройство не имеет кнопок, для этого параметра должно быть задано значение "0".</span><span class="sxs-lookup"><span data-stu-id="e98f0-124">If the pointing device has no buttons, this value should be set to "0".</span></span>

</dd> <dt>

<span data-ttu-id="e98f0-125">**поинтингтипе**</span><span class="sxs-lookup"><span data-stu-id="e98f0-125">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e98f0-126">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e98f0-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e98f0-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e98f0-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e98f0-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Указывающее устройство в DMTF \| 003,1 ")</span><span class="sxs-lookup"><span data-stu-id="e98f0-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Pointing Device\|003.1")</span></span>
</dt> </dl>

<span data-ttu-id="e98f0-129">Тип указывающего устройства.</span><span class="sxs-lookup"><span data-stu-id="e98f0-129">The type of the pointing device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e98f0-130">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="e98f0-130">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e98f0-131">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="e98f0-131">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>

<span data-ttu-id="e98f0-132">**Мышь** (3)</span><span class="sxs-lookup"><span data-stu-id="e98f0-132">**Mouse** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>

<span data-ttu-id="e98f0-133">**Отслеживание шарика** (4)</span><span class="sxs-lookup"><span data-stu-id="e98f0-133">**Track Ball** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>

<span data-ttu-id="e98f0-134">**Точка трассировки** (5)</span><span class="sxs-lookup"><span data-stu-id="e98f0-134">**Track Point** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>

<span data-ttu-id="e98f0-135">**Точка глиде** (6)</span><span class="sxs-lookup"><span data-stu-id="e98f0-135">**Glide Point** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>

<span data-ttu-id="e98f0-136">**Сенсорная панель** (7)</span><span class="sxs-lookup"><span data-stu-id="e98f0-136">**Touch Pad** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>

<span data-ttu-id="e98f0-137">**Сенсорный экран** (8)</span><span class="sxs-lookup"><span data-stu-id="e98f0-137">**Touch Screen** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>

<span data-ttu-id="e98f0-138">**Оптический датчик мыши** (9)</span><span class="sxs-lookup"><span data-stu-id="e98f0-138">**Mouse - Optical Sensor** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e98f0-139">**Решение**</span><span class="sxs-lookup"><span data-stu-id="e98f0-139">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e98f0-140">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e98f0-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e98f0-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e98f0-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e98f0-142">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("число счетчиков на дюйм"), **Пунит** ("Счетчик/дюйм")</span><span class="sxs-lookup"><span data-stu-id="e98f0-142">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Counts per Inch"), **PUnit** ("count / inch")</span></span>
</dt> </dl>

<span data-ttu-id="e98f0-143">Разрешение отслежения указывающего устройства в счетчиках на дюйм.</span><span class="sxs-lookup"><span data-stu-id="e98f0-143">The tracking resolution of the pointing device, in counts per inch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e98f0-144">Требования</span><span class="sxs-lookup"><span data-stu-id="e98f0-144">Requirements</span></span>



| <span data-ttu-id="e98f0-145">Требование</span><span class="sxs-lookup"><span data-stu-id="e98f0-145">Requirement</span></span> | <span data-ttu-id="e98f0-146">Значение</span><span class="sxs-lookup"><span data-stu-id="e98f0-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e98f0-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e98f0-147">Minimum supported client</span></span><br/> | <span data-ttu-id="e98f0-148">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e98f0-148">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e98f0-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e98f0-149">Minimum supported server</span></span><br/> | <span data-ttu-id="e98f0-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e98f0-150">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e98f0-151">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e98f0-151">Namespace</span></span><br/>                | <span data-ttu-id="e98f0-152">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e98f0-152">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e98f0-153">MOF</span><span class="sxs-lookup"><span data-stu-id="e98f0-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e98f0-154"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e98f0-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e98f0-155">DLL</span><span class="sxs-lookup"><span data-stu-id="e98f0-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e98f0-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e98f0-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e98f0-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e98f0-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e98f0-158">**\_УСЕРДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="e98f0-158">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

