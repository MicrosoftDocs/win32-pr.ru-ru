---
description: Представляет основные функции отображения монитора компьютера.
ms.assetid: 08405e7f-7824-4e44-9f37-da9bb5619cd6
title: Класс Вмимониторбасикдисплайпарамс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBasicDisplayParams
- WmiMonitorBasicDisplayParams.Active
- WmiMonitorBasicDisplayParams.DisplayTransferCharacteristic
- WmiMonitorBasicDisplayParams.InstanceName
- WmiMonitorBasicDisplayParams.MaxHorizontalImageSize
- WmiMonitorBasicDisplayParams.MaxVerticalImageSize
- WmiMonitorBasicDisplayParams.SupportedDisplayFeatures
- WmiMonitorBasicDisplayParams.VideoInputType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e457757a3542bbfc8ded7536396458ef3e592714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702726"
---
# <a name="wmimonitorbasicdisplayparams-class"></a><span data-ttu-id="ed9b2-103">Класс Вмимониторбасикдисплайпарамс</span><span class="sxs-lookup"><span data-stu-id="ed9b2-103">WmiMonitorBasicDisplayParams class</span></span>

<span data-ttu-id="ed9b2-104">Класс WMI **вмимониторбасикдисплайпарамс** представляет основные функции отображения монитора компьютера.</span><span class="sxs-lookup"><span data-stu-id="ed9b2-104">The **WmiMonitorBasicDisplayParams** WMI class represents the basic display features of a computer monitor.</span></span> <span data-ttu-id="ed9b2-105">Значение свойства **видеоинпуттипе** указывает, является ли монитор аналоговым или цифровым.</span><span class="sxs-lookup"><span data-stu-id="ed9b2-105">The value of the **VideoInputType** property indicates whether the monitor is analog or digital.</span></span> <span data-ttu-id="ed9b2-106">Данные в этом классе соответствуют данным в блоке "основные параметры дисплея" и "функции" расширенного расширенного представления идентификационных данных по стандарту (E-EDID).</span><span class="sxs-lookup"><span data-stu-id="ed9b2-106">Data in this class corresponds to data in the Basic Display Parameters/Features block of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed9b2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed9b2-107">Syntax</span></span>

``` syntax
class WmiMonitorBasicDisplayParams : MSMonitorClass
{
  boolean                            Active;
  uint8                              DisplayTransferCharacteristic;
  string                             InstanceName;
  uint8                              MaxHorizontalImageSize;
  uint8                              MaxVerticalImageSize;
  SupportedDisplayFeaturesDescriptor SupportedDisplayFeatures;
  uint8                              VideoInputType;
};
```

## <a name="members"></a><span data-ttu-id="ed9b2-108">Члены</span><span class="sxs-lookup"><span data-stu-id="ed9b2-108">Members</span></span>

<span data-ttu-id="ed9b2-109">Класс **вмимониторбасикдисплайпарамс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ed9b2-109">The **WmiMonitorBasicDisplayParams** class has these types of members:</span></span>

-   [<span data-ttu-id="ed9b2-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ed9b2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ed9b2-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="ed9b2-111">Properties</span></span>

<span data-ttu-id="ed9b2-112">Класс **вмимониторбасикдисплайпарамс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ed9b2-112">The **WmiMonitorBasicDisplayParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ed9b2-113">**Активен**</span><span class="sxs-lookup"><span data-stu-id="ed9b2-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed9b2-114">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ed9b2-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ed9b2-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed9b2-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed9b2-116">Указывает активный монитор.</span><span class="sxs-lookup"><span data-stu-id="ed9b2-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="ed9b2-117">**дисплайтрансферчарактеристик**</span><span class="sxs-lookup"><span data-stu-id="ed9b2-117">**DisplayTransferCharacteristic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed9b2-118">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="ed9b2-118">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ed9b2-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed9b2-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed9b2-120">Отображение характеристик пересылки ( \* гамма-100 100).</span><span class="sxs-lookup"><span data-stu-id="ed9b2-120">Display transfer characteristic (100\*Gamma-100).</span></span>

</dd> <dt>

<span data-ttu-id="ed9b2-121">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="ed9b2-121">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed9b2-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ed9b2-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed9b2-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed9b2-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed9b2-124">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="ed9b2-124">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ed9b2-125">Имя конкретного экземпляра монитора.</span><span class="sxs-lookup"><span data-stu-id="ed9b2-125">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="ed9b2-126">**максхоризонталимажесизе**</span><span class="sxs-lookup"><span data-stu-id="ed9b2-126">**MaxHorizontalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed9b2-127">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="ed9b2-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ed9b2-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed9b2-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed9b2-129">Максимальный размер изображения по горизонтали в сантиметрах.</span><span class="sxs-lookup"><span data-stu-id="ed9b2-129">Maximum horizontal image size in centimeters.</span></span> <span data-ttu-id="ed9b2-130">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="ed9b2-130">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ed9b2-131">**максвертикалимажесизе**</span><span class="sxs-lookup"><span data-stu-id="ed9b2-131">**MaxVerticalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed9b2-132">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="ed9b2-132">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ed9b2-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed9b2-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed9b2-134">Максимальный размер изображения по вертикали в сантиметрах.</span><span class="sxs-lookup"><span data-stu-id="ed9b2-134">Maximum vertical image size in centimeters.</span></span> <span data-ttu-id="ed9b2-135">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="ed9b2-135">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ed9b2-136">**суппортеддисплайфеатурес**</span><span class="sxs-lookup"><span data-stu-id="ed9b2-136">**SupportedDisplayFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed9b2-137">Тип данных: **[ **суппортеддисплайфеатуресдескриптор**](supporteddisplayfeaturesdescriptor.md)**</span><span class="sxs-lookup"><span data-stu-id="ed9b2-137">Data type: **[**SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)**</span></span>
</dt> <dt>

<span data-ttu-id="ed9b2-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed9b2-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed9b2-139">Отображение функций, поддерживаемых монитором.</span><span class="sxs-lookup"><span data-stu-id="ed9b2-139">Display features supported by the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="ed9b2-140">**видеоинпуттипе**</span><span class="sxs-lookup"><span data-stu-id="ed9b2-140">**VideoInputType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed9b2-141">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="ed9b2-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ed9b2-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed9b2-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed9b2-143">Тип входных данных видео.</span><span class="sxs-lookup"><span data-stu-id="ed9b2-143">Video input type.</span></span>



| <span data-ttu-id="ed9b2-144">Значение</span><span class="sxs-lookup"><span data-stu-id="ed9b2-144">Value</span></span>                                                                              | <span data-ttu-id="ed9b2-145">Значение</span><span class="sxs-lookup"><span data-stu-id="ed9b2-145">Meaning</span></span>            |
|------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="ed9b2-146"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ed9b2-146"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="ed9b2-147">Передача</span><span class="sxs-lookup"><span data-stu-id="ed9b2-147">Analog</span></span><br/>  |
| <dl> <span data-ttu-id="ed9b2-148"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="ed9b2-148"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="ed9b2-149">Цифровой</span><span class="sxs-lookup"><span data-stu-id="ed9b2-149">Digital</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed9b2-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed9b2-150">Remarks</span></span>

<span data-ttu-id="ed9b2-151">**Максхоризонталимажесизе** и **максвертикалимажесизе** представляют собой максимальные размеры изображения, которые монитор может правильно отобразить для всего набора поддерживаемых сочетаний времени и формата.</span><span class="sxs-lookup"><span data-stu-id="ed9b2-151">**MaxHorizontalImageSize** and **MaxVerticalImageSize** represent the maximum image dimensions that the monitor can correctly display for the entire set of supported timing and format combinations.</span></span> <span data-ttu-id="ed9b2-152">Максимальный размер измерения изображения определяется стандартом VESA (ВИАД) для видео в соответствии со значением, округленным до ближайшего сантиметра.</span><span class="sxs-lookup"><span data-stu-id="ed9b2-152">The maximum image dimension is defined by VESA Video Image Area Definition (VIAD) Standard and is rounded to the nearest centimeter.</span></span> <span data-ttu-id="ed9b2-153">Система главного компьютера может использовать эти данные для выбора размера изображения и пропорций, позволяющих правильно масштабировать текст.</span><span class="sxs-lookup"><span data-stu-id="ed9b2-153">The host computer system can use this data to select the image size and aspect ratio that will allow properly scaled text.</span></span> <span data-ttu-id="ed9b2-154">Имейте в виду, что если одно или оба этих поля равны нулю, система не делает никаких предположений о размере отображаемого размера.</span><span class="sxs-lookup"><span data-stu-id="ed9b2-154">Be aware that, if either or both of these fields are zero, then the system makes no assumptions about the display size.</span></span> <span data-ttu-id="ed9b2-155">Например, размер отображения проекции может быть неопределенной.</span><span class="sxs-lookup"><span data-stu-id="ed9b2-155">For example, the size of a projection display may be undetermined.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed9b2-156">Требования</span><span class="sxs-lookup"><span data-stu-id="ed9b2-156">Requirements</span></span>



| <span data-ttu-id="ed9b2-157">Требование</span><span class="sxs-lookup"><span data-stu-id="ed9b2-157">Requirement</span></span> | <span data-ttu-id="ed9b2-158">Значение</span><span class="sxs-lookup"><span data-stu-id="ed9b2-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed9b2-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed9b2-159">Minimum supported client</span></span><br/> | <span data-ttu-id="ed9b2-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed9b2-160">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ed9b2-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed9b2-161">Minimum supported server</span></span><br/> | <span data-ttu-id="ed9b2-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed9b2-162">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ed9b2-163">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ed9b2-163">Namespace</span></span><br/>                | <span data-ttu-id="ed9b2-164">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="ed9b2-164">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="ed9b2-165">MOF</span><span class="sxs-lookup"><span data-stu-id="ed9b2-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed9b2-166"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed9b2-166"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed9b2-167">DLL</span><span class="sxs-lookup"><span data-stu-id="ed9b2-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed9b2-168"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed9b2-168"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed9b2-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed9b2-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed9b2-170">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="ed9b2-170">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




