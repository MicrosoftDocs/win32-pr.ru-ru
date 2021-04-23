---
description: Класс CIM \_ MonitorResolution представляет связь между горизонтальным и вертикальным разрешением, а также частотой обновления и режимом сканирования для настольного монитора. Значения указываются в объекте контроллера видео.
ms.assetid: 064620dd-2d92-42d0-9167-35867830a077
ms.tgt_platform: multiple
title: Класс CIM_MonitorResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MonitorResolution
- CIM_MonitorResolution.Caption
- CIM_MonitorResolution.Description
- CIM_MonitorResolution.SettingID
- CIM_MonitorResolution.HorizontalResolution
- CIM_MonitorResolution.MaxRefreshRate
- CIM_MonitorResolution.MinRefreshRate
- CIM_MonitorResolution.RefreshRate
- CIM_MonitorResolution.ScanMode
- CIM_MonitorResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b359a2e7eccf31b32aced8a2ea9f85fb6dc48b7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990659"
---
# <a name="cim_monitorresolution-class"></a><span data-ttu-id="318f0-104">\_Класс CIM MonitorResolution</span><span class="sxs-lookup"><span data-stu-id="318f0-104">CIM\_MonitorResolution class</span></span>

<span data-ttu-id="318f0-105">Класс **CIM \_ MonitorResolution** представляет связь между горизонтальным и вертикальным разрешением, а также частотой обновления и режимом сканирования для настольного монитора.</span><span class="sxs-lookup"><span data-stu-id="318f0-105">The **CIM\_MonitorResolution** class represents the relationship between horizontal and vertical resolutions and the refresh rate and scan mode for a desktop monitor.</span></span> <span data-ttu-id="318f0-106">Значения указываются в объекте контроллера видео.</span><span class="sxs-lookup"><span data-stu-id="318f0-106">Values are specified in the video controller object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="318f0-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="318f0-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="318f0-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="318f0-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="318f0-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="318f0-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="318f0-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="318f0-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="318f0-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="318f0-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCEC-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_MonitorResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="318f0-112">Члены</span><span class="sxs-lookup"><span data-stu-id="318f0-112">Members</span></span>

<span data-ttu-id="318f0-113">Класс **CIM \_ MonitorResolution** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="318f0-113">The **CIM\_MonitorResolution** class has these types of members:</span></span>

-   [<span data-ttu-id="318f0-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="318f0-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="318f0-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="318f0-115">Properties</span></span>

<span data-ttu-id="318f0-116">Класс **CIM \_ MonitorResolution** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="318f0-116">The **CIM\_MonitorResolution** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="318f0-117">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="318f0-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="318f0-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="318f0-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="318f0-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="318f0-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="318f0-120">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="318f0-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="318f0-121">Краткое текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="318f0-121">Short textual description of the current object.</span></span>

<span data-ttu-id="318f0-122">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="318f0-122">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="318f0-123">**Описание**</span><span class="sxs-lookup"><span data-stu-id="318f0-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="318f0-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="318f0-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="318f0-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="318f0-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="318f0-126">Текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="318f0-126">Textual description of the current object.</span></span>

<span data-ttu-id="318f0-127">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="318f0-127">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="318f0-128">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="318f0-128">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="318f0-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="318f0-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="318f0-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="318f0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="318f0-131">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Курренсоризонталресолутион**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Разрешение монитора DMTF \| 002,2 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" пикселей ")</span><span class="sxs-lookup"><span data-stu-id="318f0-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="318f0-132">Разрешение монитора по горизонтали (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="318f0-132">Monitor's horizontal resolution, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="318f0-133">**максрефрешрате**</span><span class="sxs-lookup"><span data-stu-id="318f0-133">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="318f0-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="318f0-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="318f0-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="318f0-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="318f0-136">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Максрефрешрате**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Разрешение монитора DMTF \| 002,7 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="318f0-136">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="318f0-137">Максимальная частота обновления монитора в герцах, если для указанных разрешений поддерживается диапазон частот.</span><span class="sxs-lookup"><span data-stu-id="318f0-137">Monitor's maximum refresh rate, in hertz, when a range of rates is supported at the specified resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="318f0-138">**минрефрешрате**</span><span class="sxs-lookup"><span data-stu-id="318f0-138">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="318f0-139">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="318f0-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="318f0-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="318f0-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="318f0-141">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Минрефрешрате**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Разрешение монитора DMTF \| 002,6 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="318f0-141">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="318f0-142">Минимальная частота обновления монитора (в герцах), если для указанных разрешений поддерживается диапазон частот.</span><span class="sxs-lookup"><span data-stu-id="318f0-142">Monitor's minimum refresh rate, in hertz, when a range of rates is supported at the specified resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="318f0-143">**рефрешрате**</span><span class="sxs-lookup"><span data-stu-id="318f0-143">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="318f0-144">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="318f0-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="318f0-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="318f0-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="318f0-146">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Куррентрефрешрате**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Разрешение монитора DMTF \| 002,4 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="318f0-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="318f0-147">Частота обновления монитора в герцах.</span><span class="sxs-lookup"><span data-stu-id="318f0-147">Monitor's refresh rate, in hertz.</span></span> <span data-ttu-id="318f0-148">Если поддерживается диапазон ставок, используйте свойства **минрефрешрате** и **максрефрешрате** и присвойте этому свойству значение 0.</span><span class="sxs-lookup"><span data-stu-id="318f0-148">If a range of rates is supported, use the **MinRefreshRate** and **MaxRefreshRate** properties, and set this property to 0.</span></span>

</dd> <dt>

<span data-ttu-id="318f0-149">**сканмоде**</span><span class="sxs-lookup"><span data-stu-id="318f0-149">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="318f0-150">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="318f0-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="318f0-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="318f0-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="318f0-152">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Куррентсканмоде**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Разрешение монитора DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="318f0-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="318f0-153">Режим сканирования, используемый монитором.</span><span class="sxs-lookup"><span data-stu-id="318f0-153">Scan mode that the monitor uses.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="318f0-154">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="318f0-154">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="318f0-155">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="318f0-155">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="318f0-156">**Не поддерживается** (3)</span><span class="sxs-lookup"><span data-stu-id="318f0-156">**Not Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="318f0-157">**Операция без чередования** (4)</span><span class="sxs-lookup"><span data-stu-id="318f0-157">**Non-Interlaced Operation** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="318f0-158">**Операция чередования** (5)</span><span class="sxs-lookup"><span data-stu-id="318f0-158">**Interlaced Operation** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="318f0-159">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="318f0-159">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="318f0-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="318f0-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="318f0-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="318f0-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="318f0-162">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("свойство settingid"), [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="318f0-162">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="318f0-163">Служит частью ключа для текущего экземпляра.</span><span class="sxs-lookup"><span data-stu-id="318f0-163">Serves as part of the key for the current instance.</span></span>

</dd> <dt>

<span data-ttu-id="318f0-164">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="318f0-164">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="318f0-165">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="318f0-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="318f0-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="318f0-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="318f0-167">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Куррентвертикалресолутион**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Разрешение монитора DMTF \| 002,3 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" пикселей ")</span><span class="sxs-lookup"><span data-stu-id="318f0-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="318f0-168">Разрешение монитора по вертикали в пикселях.</span><span class="sxs-lookup"><span data-stu-id="318f0-168">Monitor's vertical resolution in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="318f0-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="318f0-169">Remarks</span></span>

<span data-ttu-id="318f0-170">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="318f0-170">WMI does not implement this class.</span></span>

<span data-ttu-id="318f0-171">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="318f0-171">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="318f0-172">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="318f0-172">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="318f0-173">Требования</span><span class="sxs-lookup"><span data-stu-id="318f0-173">Requirements</span></span>



| <span data-ttu-id="318f0-174">Требование</span><span class="sxs-lookup"><span data-stu-id="318f0-174">Requirement</span></span> | <span data-ttu-id="318f0-175">Значение</span><span class="sxs-lookup"><span data-stu-id="318f0-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="318f0-176">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="318f0-176">Minimum supported client</span></span><br/> | <span data-ttu-id="318f0-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="318f0-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="318f0-178">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="318f0-178">Minimum supported server</span></span><br/> | <span data-ttu-id="318f0-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="318f0-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="318f0-180">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="318f0-180">Namespace</span></span><br/>                | <span data-ttu-id="318f0-181">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="318f0-181">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="318f0-182">MOF</span><span class="sxs-lookup"><span data-stu-id="318f0-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="318f0-183"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="318f0-183"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="318f0-184">DLL</span><span class="sxs-lookup"><span data-stu-id="318f0-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="318f0-185"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="318f0-185"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="318f0-186">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="318f0-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="318f0-187">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="318f0-187">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

