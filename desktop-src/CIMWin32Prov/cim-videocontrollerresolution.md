---
description: Класс CIM \_ видеоконтроллерресолутион представляет различные видеорежимы, которые может поддерживать контроллер видео.
ms.assetid: 954ac3fe-9777-460c-8929-853f19379256
ms.tgt_platform: multiple
title: Класс CIM_VideoControllerResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoControllerResolution
- CIM_VideoControllerResolution.Caption
- CIM_VideoControllerResolution.Description
- CIM_VideoControllerResolution.SettingID
- CIM_VideoControllerResolution.HorizontalResolution
- CIM_VideoControllerResolution.MaxRefreshRate
- CIM_VideoControllerResolution.MinRefreshRate
- CIM_VideoControllerResolution.NumberOfColors
- CIM_VideoControllerResolution.RefreshRate
- CIM_VideoControllerResolution.ScanMode
- CIM_VideoControllerResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d448d92d79163bc6a4e1056e88434081c5878159
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896450"
---
# <a name="cim_videocontrollerresolution-class"></a><span data-ttu-id="421c5-103">\_Класс CIM видеоконтроллерресолутион</span><span class="sxs-lookup"><span data-stu-id="421c5-103">CIM\_VideoControllerResolution class</span></span>

<span data-ttu-id="421c5-104">Класс **CIM \_ видеоконтроллерресолутион** представляет различные видеорежимы, которые может поддерживать контроллер видео.</span><span class="sxs-lookup"><span data-stu-id="421c5-104">The **CIM\_VideoControllerResolution** class represents the various video modes that a video controller can support.</span></span> <span data-ttu-id="421c5-105">Видеорежимы определяются с помощью возможных горизонтальных и вертикальных разрешений, частоты обновления, режима сканирования и количества параметров цвета, поддерживаемых контроллером.</span><span class="sxs-lookup"><span data-stu-id="421c5-105">Video modes are defined by the possible horizontal and vertical resolutions, refresh rate, scan mode, and number of color settings supported by a controller.</span></span> <span data-ttu-id="421c5-106">Фактически используемые разрешения — это значения, указанные в объекте [**CIM \_ Видеоконтроллер**](cim-videocontroller.md) .</span><span class="sxs-lookup"><span data-stu-id="421c5-106">The actual resolutions in use are the values specified in the [**CIM\_VideoController**](cim-videocontroller.md) object.</span></span>

<span data-ttu-id="421c5-107">Оборудование, несовместимое с моделью драйвера Windows (WDDM), возвращает неточные значения свойств для экземпляров этого класса.</span><span class="sxs-lookup"><span data-stu-id="421c5-107">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="421c5-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="421c5-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="421c5-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="421c5-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="421c5-110">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="421c5-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="421c5-111">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="421c5-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="421c5-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="421c5-112">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEA-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoControllerResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint64 NumberOfColors;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="421c5-113">Члены</span><span class="sxs-lookup"><span data-stu-id="421c5-113">Members</span></span>

<span data-ttu-id="421c5-114">Класс **CIM \_ видеоконтроллерресолутион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="421c5-114">The **CIM\_VideoControllerResolution** class has these types of members:</span></span>

-   [<span data-ttu-id="421c5-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="421c5-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="421c5-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="421c5-116">Properties</span></span>

<span data-ttu-id="421c5-117">Класс **CIM \_ видеоконтроллерресолутион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="421c5-117">The **CIM\_VideoControllerResolution** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="421c5-118">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="421c5-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="421c5-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="421c5-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="421c5-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="421c5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="421c5-121">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="421c5-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="421c5-122">Краткое текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="421c5-122">Short textual description of the current object.</span></span>

<span data-ttu-id="421c5-123">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="421c5-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="421c5-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="421c5-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="421c5-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="421c5-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="421c5-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="421c5-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="421c5-127">Текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="421c5-127">Textual description of the current object.</span></span>

<span data-ttu-id="421c5-128">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="421c5-128">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="421c5-129">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="421c5-129">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="421c5-130">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="421c5-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="421c5-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="421c5-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="421c5-132">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Курренсоризонталресолутион**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Разрешение монитора DMTF \| 002,2 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" пикселей ")</span><span class="sxs-lookup"><span data-stu-id="421c5-132">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="421c5-133">Разрешение по горизонтали в пикселях.</span><span class="sxs-lookup"><span data-stu-id="421c5-133">Horizontal resolution, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="421c5-134">**максрефрешрате**</span><span class="sxs-lookup"><span data-stu-id="421c5-134">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="421c5-135">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="421c5-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="421c5-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="421c5-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="421c5-137">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Максрефрешрате**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Разрешение монитора DMTF \| 002,7 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="421c5-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="421c5-138">Максимальная частота обновления, если для указанных разрешений поддерживается диапазон частот (в герцах).</span><span class="sxs-lookup"><span data-stu-id="421c5-138">Maximum refresh rate when a range of rates is supported at the specified resolutions, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="421c5-139">**минрефрешрате**</span><span class="sxs-lookup"><span data-stu-id="421c5-139">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="421c5-140">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="421c5-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="421c5-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="421c5-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="421c5-142">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Минрефрешрате**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Разрешение монитора DMTF \| 002,6 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="421c5-142">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="421c5-143">Минимальная частота обновления, если для указанных разрешений поддерживается диапазон частот (в герцах).</span><span class="sxs-lookup"><span data-stu-id="421c5-143">Minimum refresh rate when a range of rates is supported at the specified resolutions, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="421c5-144">**нумберофколорс**</span><span class="sxs-lookup"><span data-stu-id="421c5-144">**NumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="421c5-145">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="421c5-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="421c5-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="421c5-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="421c5-147">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Куррентнумберофколорс**")</span><span class="sxs-lookup"><span data-stu-id="421c5-147">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentNumberOfColors**")</span></span>
</dt> </dl>

<span data-ttu-id="421c5-148">Число цветов, поддерживаемое при текущем разрешении.</span><span class="sxs-lookup"><span data-stu-id="421c5-148">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="421c5-149">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="421c5-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="421c5-150">**рефрешрате**</span><span class="sxs-lookup"><span data-stu-id="421c5-150">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="421c5-151">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="421c5-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="421c5-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="421c5-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="421c5-153">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Куррентрефрешрате**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Разрешение монитора DMTF \| 002,4 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="421c5-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="421c5-154">Частота обновления в герцах.</span><span class="sxs-lookup"><span data-stu-id="421c5-154">Refresh rate, in hertz.</span></span> <span data-ttu-id="421c5-155">Если поддерживается диапазон ставок, используйте свойства **минрефрешрате** и **максрефрешрате** и присвойте этому свойству значение 0.</span><span class="sxs-lookup"><span data-stu-id="421c5-155">If a range of rates is supported, use the **MinRefreshRate** and **MaxRefreshRate** properties, and set this property to 0.</span></span>

</dd> <dt>

<span data-ttu-id="421c5-156">**сканмоде**</span><span class="sxs-lookup"><span data-stu-id="421c5-156">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="421c5-157">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="421c5-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="421c5-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="421c5-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="421c5-159">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Куррентсканмоде**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Разрешение монитора DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="421c5-159">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="421c5-160">Режим сканирования, в котором работает контроллер.</span><span class="sxs-lookup"><span data-stu-id="421c5-160">Scan mode at which the controller operates.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="421c5-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="421c5-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="421c5-162"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="421c5-162"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="421c5-163"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (3)</span><span class="sxs-lookup"><span data-stu-id="421c5-163"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="421c5-164"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Операция без чередования** (4)</span><span class="sxs-lookup"><span data-stu-id="421c5-164"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Non-Interlaced Operation** (4)</span></span>


</dt> <dd>

<span data-ttu-id="421c5-165">Нечересстрочнуюющая операция</span><span class="sxs-lookup"><span data-stu-id="421c5-165">Noninterlaced operation</span></span>

</dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="421c5-166"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Операция чередования** (5)</span><span class="sxs-lookup"><span data-stu-id="421c5-166"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Interlaced Operation** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="421c5-167">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="421c5-167">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="421c5-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="421c5-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="421c5-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="421c5-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="421c5-170">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("свойство settingid"), [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="421c5-170">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="421c5-171">Идентификатор, который служит частью ключа для текущего экземпляра.</span><span class="sxs-lookup"><span data-stu-id="421c5-171">An ID that serves as part of the key for the current instance.</span></span>

</dd> <dt>

<span data-ttu-id="421c5-172">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="421c5-172">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="421c5-173">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="421c5-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="421c5-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="421c5-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="421c5-175">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Куррентвертикалресолутион**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Разрешение монитора DMTF \| 002,3 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" пикселей ")</span><span class="sxs-lookup"><span data-stu-id="421c5-175">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="421c5-176">Разрешение контроллера по вертикали (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="421c5-176">Controller's vertical resolution, in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="421c5-177">Комментарии</span><span class="sxs-lookup"><span data-stu-id="421c5-177">Remarks</span></span>

<span data-ttu-id="421c5-178">WMI реализует класс **CIM \_ видеоконтроллерресолутион** .</span><span class="sxs-lookup"><span data-stu-id="421c5-178">WMI implements the **CIM\_VideoControllerResolution** class.</span></span> <span data-ttu-id="421c5-179">Класс **CIM \_ видеоконтроллерресолутион** является динамическим классом.</span><span class="sxs-lookup"><span data-stu-id="421c5-179">The **CIM\_VideoControllerResolution** class is a dynamic class.</span></span>

<span data-ttu-id="421c5-180">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="421c5-180">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="421c5-181">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="421c5-181">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="421c5-182">Обратите внимание, что этот класс является базовым классом.</span><span class="sxs-lookup"><span data-stu-id="421c5-182">Note that this class is a base class.</span></span> <span data-ttu-id="421c5-183">Если вы пытаетесь получить доступ к видеоконтроллеру с помощью инструментария WMI, вместо этого может потребоваться использовать [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md) .</span><span class="sxs-lookup"><span data-stu-id="421c5-183">If you are attempting to access your video controller through WMI, you may wish to use [**Win32\_VideoController**](win32-videocontroller.md) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="421c5-184">Требования</span><span class="sxs-lookup"><span data-stu-id="421c5-184">Requirements</span></span>



| <span data-ttu-id="421c5-185">Требование</span><span class="sxs-lookup"><span data-stu-id="421c5-185">Requirement</span></span> | <span data-ttu-id="421c5-186">Значение</span><span class="sxs-lookup"><span data-stu-id="421c5-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="421c5-187">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="421c5-187">Minimum supported client</span></span><br/> | <span data-ttu-id="421c5-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="421c5-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="421c5-189">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="421c5-189">Minimum supported server</span></span><br/> | <span data-ttu-id="421c5-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="421c5-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="421c5-191">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="421c5-191">Namespace</span></span><br/>                | <span data-ttu-id="421c5-192">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="421c5-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="421c5-193">MOF</span><span class="sxs-lookup"><span data-stu-id="421c5-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="421c5-194"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="421c5-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="421c5-195">DLL</span><span class="sxs-lookup"><span data-stu-id="421c5-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="421c5-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="421c5-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="421c5-197">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="421c5-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="421c5-198">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="421c5-198">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

