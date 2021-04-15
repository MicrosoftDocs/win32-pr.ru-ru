---
description: Представляет один заголовок \_ объекта CIM дисплайконтроллер.
ms.assetid: 2bb034d9-d1df-4cc8-a6a8-b6ad7289f582
title: Класс CIM_VideoHead
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoHead
- CIM_VideoHead.CurrentBitsPerPixel
- CIM_VideoHead.CurrentHorizontalResolution
- CIM_VideoHead.CurrentVerticalResolution
- CIM_VideoHead.MaxRefreshRate
- CIM_VideoHead.MinRefreshRate
- CIM_VideoHead.CurrentRefreshRate
- CIM_VideoHead.CurrentScanMode
- CIM_VideoHead.OtherCurrentScanMode
- CIM_VideoHead.CurrentNumberOfRows
- CIM_VideoHead.CurrentNumberOfColumns
- CIM_VideoHead.CurrentNumberOfColors
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22f8176c9bdbeae460dfa22ca395e7ed8dd8351e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683251"
---
# <a name="cim_videohead-class"></a><span data-ttu-id="983ef-103">\_Класс CIM видеохеад</span><span class="sxs-lookup"><span data-stu-id="983ef-103">CIM\_VideoHead class</span></span>

<span data-ttu-id="983ef-104">Представляет один заголовок объекта [**CIM \_ дисплайконтроллер**](cim-displaycontroller.md) .</span><span class="sxs-lookup"><span data-stu-id="983ef-104">Represents one head of a [**CIM\_DisplayController**](cim-displaycontroller.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="983ef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="983ef-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_VideoHead : CIM_LogicalDevice
{
  uint32 CurrentBitsPerPixel;
  uint32 CurrentHorizontalResolution;
  uint32 CurrentVerticalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint32 CurrentRefreshRate;
  uint16 CurrentScanMode;
  string OtherCurrentScanMode;
  uint32 CurrentNumberOfRows;
  uint32 CurrentNumberOfColumns;
  uint64 CurrentNumberOfColors;
};
```

## <a name="members"></a><span data-ttu-id="983ef-106">Члены</span><span class="sxs-lookup"><span data-stu-id="983ef-106">Members</span></span>

<span data-ttu-id="983ef-107">Класс **CIM \_ видеохеад** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="983ef-107">The **CIM\_VideoHead** class has these types of members:</span></span>

-   [<span data-ttu-id="983ef-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="983ef-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="983ef-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="983ef-109">Properties</span></span>

<span data-ttu-id="983ef-110">Класс **CIM \_ видеохеад** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="983ef-110">The **CIM\_VideoHead** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="983ef-111">**куррентбитсперпиксел**</span><span class="sxs-lookup"><span data-stu-id="983ef-111">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983ef-112">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="983ef-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="983ef-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983ef-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="983ef-114">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("BITS"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,12 "), **Пунит** (" бит ")</span><span class="sxs-lookup"><span data-stu-id="983ef-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.12"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="983ef-115">Число битов, используемых для вывода каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="983ef-115">The number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="983ef-116">**курренсоризонталресолутион**</span><span class="sxs-lookup"><span data-stu-id="983ef-116">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983ef-117">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="983ef-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="983ef-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983ef-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="983ef-119">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("пикселей"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,11 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ видеохеадресолутион. хоризонталресолутион "), **Пунит** (" пиксель ")</span><span class="sxs-lookup"><span data-stu-id="983ef-119">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixels"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.11"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.HorizontalResolution"), **PUnit** ("pixel")</span></span>
</dt> </dl>

<span data-ttu-id="983ef-120">Текущее число точек по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="983ef-120">The current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="983ef-121">**куррентнумберофколорс**</span><span class="sxs-lookup"><span data-stu-id="983ef-121">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983ef-122">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="983ef-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="983ef-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983ef-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="983ef-124">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ видеохеадресолутион. нумберофколорс")</span><span class="sxs-lookup"><span data-stu-id="983ef-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.NumberOfColors")</span></span>
</dt> </dl>

<span data-ttu-id="983ef-125">Число цветов, поддерживаемое в текущем разрешении.</span><span class="sxs-lookup"><span data-stu-id="983ef-125">The number of colors supported at the current resolution.</span></span>

</dd> <dt>

<span data-ttu-id="983ef-126">**куррентнумберофколумнс**</span><span class="sxs-lookup"><span data-stu-id="983ef-126">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983ef-127">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="983ef-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="983ef-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983ef-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="983ef-129">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 004,14 ")</span><span class="sxs-lookup"><span data-stu-id="983ef-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.14")</span></span>
</dt> </dl>

<span data-ttu-id="983ef-130">Если в символьном режиме, число столбцов для контроллера экрана; в противном случае — "0".</span><span class="sxs-lookup"><span data-stu-id="983ef-130">If in character mode, the number of columns for the display controller; otherwise, "0".</span></span>

</dd> <dt>

<span data-ttu-id="983ef-131">**куррентнумберофровс**</span><span class="sxs-lookup"><span data-stu-id="983ef-131">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983ef-132">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="983ef-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="983ef-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983ef-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="983ef-134">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 004,13 ")</span><span class="sxs-lookup"><span data-stu-id="983ef-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.13")</span></span>
</dt> </dl>

<span data-ttu-id="983ef-135">Если в символьном режиме, число строк для контроллера экрана; в противном случае — "0".</span><span class="sxs-lookup"><span data-stu-id="983ef-135">If in character mode, the number of rows for the display controller; otherwise, "0".</span></span>

</dd> <dt>

<span data-ttu-id="983ef-136">**куррентрефрешрате**</span><span class="sxs-lookup"><span data-stu-id="983ef-136">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983ef-137">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="983ef-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="983ef-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983ef-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="983ef-139">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Герц"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,15 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ видеохеадресолутион. рефрешрате "), **Пунит** (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="983ef-139">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.15"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.RefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="983ef-140">Текущая частота обновления контроллера экрана в герцах.</span><span class="sxs-lookup"><span data-stu-id="983ef-140">The current refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="983ef-141">**куррентсканмоде**</span><span class="sxs-lookup"><span data-stu-id="983ef-141">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983ef-142">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="983ef-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="983ef-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983ef-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="983ef-144">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 004,8 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ видеохеад**.**Осеркуррентсканмоде**, CIM \_ Видеохеадресолутион. сканмоде ")</span><span class="sxs-lookup"><span data-stu-id="983ef-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoHead**.**OtherCurrentScanMode**, CIM\_VideoHeadResolution.ScanMode")</span></span>
</dt> </dl>

<span data-ttu-id="983ef-145">Текущий режим просмотра контроллера экрана.</span><span class="sxs-lookup"><span data-stu-id="983ef-145">The current scan mode of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="983ef-146">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="983ef-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="983ef-147">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="983ef-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="983ef-148">**Не поддерживается** (2)</span><span class="sxs-lookup"><span data-stu-id="983ef-148">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="983ef-149">**Операция без чередования** (3)</span><span class="sxs-lookup"><span data-stu-id="983ef-149">**Non-Interlaced Operation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="983ef-150">**Операция чередования** (4)</span><span class="sxs-lookup"><span data-stu-id="983ef-150">**Interlaced Operation** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="983ef-151">**куррентвертикалресолутион**</span><span class="sxs-lookup"><span data-stu-id="983ef-151">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983ef-152">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="983ef-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="983ef-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983ef-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="983ef-154">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("пикселей"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,10 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ видеохеадресолутион. вертикалресолутион "), **Пунит** (" пиксель ")</span><span class="sxs-lookup"><span data-stu-id="983ef-154">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixels"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.10"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.VerticalResolution"), **PUnit** ("pixel")</span></span>
</dt> </dl>

<span data-ttu-id="983ef-155">Текущее число пикселей по вертикали.</span><span class="sxs-lookup"><span data-stu-id="983ef-155">The current number of vertical pixels.</span></span>

</dd> <dt>

<span data-ttu-id="983ef-156">**максрефрешрате**</span><span class="sxs-lookup"><span data-stu-id="983ef-156">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983ef-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="983ef-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="983ef-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983ef-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="983ef-159">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Герц"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,5 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ видеохеадресолутион. максрефрешрате "), **Пунит** (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="983ef-159">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.MaxRefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="983ef-160">Максимальная частота обновления контроллера экрана в герцах.</span><span class="sxs-lookup"><span data-stu-id="983ef-160">The maximum refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="983ef-161">**минрефрешрате**</span><span class="sxs-lookup"><span data-stu-id="983ef-161">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983ef-162">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="983ef-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="983ef-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983ef-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="983ef-164">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Герц"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,4 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ видеохеадресолутион. минрефрешрате "), **Пунит** (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="983ef-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.MinRefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="983ef-165">Минимальная частота обновления контроллера экрана в герцах.</span><span class="sxs-lookup"><span data-stu-id="983ef-165">The minimum refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="983ef-166">**осеркуррентсканмоде**</span><span class="sxs-lookup"><span data-stu-id="983ef-166">**OtherCurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983ef-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="983ef-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="983ef-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983ef-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="983ef-169">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ видеохеад**.**Куррентсканмоде**, CIM \_ Видеохеадресолутион. осерсканмоде ")</span><span class="sxs-lookup"><span data-stu-id="983ef-169">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoHead**.**CurrentScanMode**, CIM\_VideoHeadResolution.OtherScanMode")</span></span>
</dt> </dl>

<span data-ttu-id="983ef-170">Описание текущего режима сканирования, если свойство **куррентсканмоде** имеет значение "1" (другое).</span><span class="sxs-lookup"><span data-stu-id="983ef-170">A description of current scan mode when the **CurrentScanMode** property is "1" (other).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="983ef-171">Требования</span><span class="sxs-lookup"><span data-stu-id="983ef-171">Requirements</span></span>



| <span data-ttu-id="983ef-172">Требование</span><span class="sxs-lookup"><span data-stu-id="983ef-172">Requirement</span></span> | <span data-ttu-id="983ef-173">Значение</span><span class="sxs-lookup"><span data-stu-id="983ef-173">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="983ef-174">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="983ef-174">Minimum supported client</span></span><br/> | <span data-ttu-id="983ef-175">Windows 8</span><span class="sxs-lookup"><span data-stu-id="983ef-175">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="983ef-176">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="983ef-176">Minimum supported server</span></span><br/> | <span data-ttu-id="983ef-177">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="983ef-177">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="983ef-178">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="983ef-178">Namespace</span></span><br/>                | <span data-ttu-id="983ef-179">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="983ef-179">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="983ef-180">MOF</span><span class="sxs-lookup"><span data-stu-id="983ef-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="983ef-181"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="983ef-181"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="983ef-182">DLL</span><span class="sxs-lookup"><span data-stu-id="983ef-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="983ef-183"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="983ef-183"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="983ef-184">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="983ef-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="983ef-185">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="983ef-185">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

