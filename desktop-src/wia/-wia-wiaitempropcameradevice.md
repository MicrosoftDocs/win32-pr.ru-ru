---
description: Аппаратные устройства для получения образа Windows (WIA) имеют значения свойств, которые хранятся в реестре Windows. Дополнительные сведения см. в разделе Общие константы свойств устройства.
ms.assetid: 7893137b-194c-4ea1-b15c-59d2f41f972a
title: Константы свойств устройства камеры (Виадеф. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPC_PICTURES_TAKEN
- WIA_DPC_PICTURES_REMAINING
- WIA_DPC_EXPOSURE_MODE
- WIA_DPC_EXPOSURE_COMP
- WIA_DPC_EXPOSURE_TIME
- WIA_DPC_FNUMBER
- WIA_DPC_FLASH_MODE
- WIA_DPC_FOCUS_MODE
- WIA_DPC_FOCUS_MANUAL_DIST
- WIA_DPC_ZOOM_POSITION
- WIA_DPC_PAN_POSITION
- WIA_DPC_TILT_POSITION
- WIA_DPC_TIMER_MODE
- WIA_DPC_TIMER_VALUE
- WIA_DPC_POWER_MODE
- WIA_DPC_BATTERY_STATUS
- WIA_DPC_THUMB_WIDTH
- WIA_DPC_THUMB_HEIGHT
- WIA_DPC_PICT_WIDTH
- WIA_DPC_PICT_HEIGHT
- WIA_DPC_DIMENSION
- WIA_DPC_COMPRESSION_SETTING
- WIA_DPC_FOCUS_METERING
- WIA_DPC_TIMELAPSE_INTERVAL
- WIA_DPC_TIMELAPSE_NUMBER
- WIA_DPC_BURST_INTERVAL
- WIA_DPC_BURST_NUMBER
- WIA_DPC_EFFECT_MODE
- WIA_DPC_DIGITAL_ZOOM
- WIA_DPC_SHARPNESS
- WIA_DPC_CONTRAST
- WIA_DPC_CAPTURE_MODE
- WIA_DPC_CAPTURE_DELAY
- WIA_DPC_EXPOSURE_INDEX
- WIA_DPC_EXPOSURE_METERING_MODE
- WIA_DPC_FOCUS_METERING_MODE
- WIA_DPC_FOCUS_DISTANCE
- WIA_DPC_FOCAL_LENGTH
- WIA_DPC_RGB_GAIN
- WIA_DPC_WHITE_BALANCE
- WIA_DPC_UPLOAD_URL
- WIA_DPC_ARTIST
- WIA_DPC_COPYRIGHT_INFO
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 0114fedd7fd4acf811e71db67376afecc2630cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497535"
---
# <a name="camera-device-property-constants"></a><span data-ttu-id="8d7c5-104">Константы свойств устройства камеры</span><span class="sxs-lookup"><span data-stu-id="8d7c5-104">Camera Device Property Constants</span></span>

<span data-ttu-id="8d7c5-105">Аппаратные устройства для получения образа Windows (WIA) имеют значения свойств, которые хранятся в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-105">Windows Image Acquisition (WIA) hardware devices have property values that are stored in the Windows registry.</span></span> <span data-ttu-id="8d7c5-106">Дополнительные сведения см. в разделе [**общие константы свойств устройства**](-wia-wiaitempropcommondevice.md).</span><span class="sxs-lookup"><span data-stu-id="8d7c5-106">For more information, see [**Common Device Property Constants**](-wia-wiaitempropcommondevice.md).</span></span>

<span data-ttu-id="8d7c5-107">Следующие константы свойств устройства со связанными строками относятся к цифровым камерам.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-107">The following device property constants, with their associated strings, are specific to digital cameras.</span></span> <span data-ttu-id="8d7c5-108">Префикс "WIA \_ DPC \_ " указывает свойство устройства для камер и является соглашением об именовании, используемым в C/C++.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-108">The prefix "WIA\_DPC\_" indicates a Device Property for Cameras and is the naming convention used in C/C++.</span></span> <span data-ttu-id="8d7c5-109">Для сценариев эти константы используют префикс "Камерадевице" и являются частью перечислимого типа [виаитемпропертид](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="8d7c5-109">For scripting purposes these constants use the prefix "CameraDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="8d7c5-110">Соответствующее имя элемента из этого перечисления скриптов отображается в круглых скобках рядом с именем константы C/C++ в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-110">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="8d7c5-111">WIA не поддерживает камеры в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-111">WIA does not support cameras in Windows Vista or later.</span></span> <span data-ttu-id="8d7c5-112">Для этих версий Windows используйте API переносных устройств Windows (WPD), описанный в пакете средств разработки драйверов Windows (DDK), для получения изображений из камер.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-112">For those versions of the Windows, use the Windows Portable Device (WPD) API described in the Windows Driver Development Kit (DDK) to acquire images from cameras.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="8d7c5-113">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="8d7c5-113">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="8d7c5-114">Описание</span><span class="sxs-lookup"><span data-stu-id="8d7c5-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_TAKEN"></span><span id="wia_dpc_pictures_taken"></span><dl> <span data-ttu-id="8d7c5-115"><dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>камерадевицепиктурестакен</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-115"><dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>CameraDevicePicturesTaken</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8d7c5-116">Количество изображений, занятых камерой.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-116">The number of pictures that the camera has taken.</span></span> <span data-ttu-id="8d7c5-117">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-117">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="8d7c5-118">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-118">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_REMAINING"></span><span id="wia_dpc_pictures_remaining"></span><dl> <span data-ttu-id="8d7c5-119"><dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>камерадевицепиктуресремаининг</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-119"><dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>CameraDevicePicturesRemaining</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8d7c5-120">Количество снимков, которые могут быть выполнены с учетом текущих настроек свойств.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-120">The number of pictures that can be taken, given the current property settings.</span></span> <span data-ttu-id="8d7c5-121">Если эти параметры изменяются и изменения влияют на размер образов, создаваемых устройством камеры, то WIA минидривер должен обновить количество оставшихся изображений.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-121">If these settings change, and the changes affect the size of the images that the camera device produces, the WIA minidriver should update the number of remaining pictures.</span></span> <span data-ttu-id="8d7c5-122">Минидривер создает и поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-122">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="8d7c5-123">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-123">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_MODE"></span><span id="wia_dpc_exposure_mode"></span><dl> <span data-ttu-id="8d7c5-124"><dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>камерадевицеекспосуремоде</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-124"><dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>CameraDeviceExposureMode</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8d7c5-125">Указывает текущий режим экспозиции камеры.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-125">Indicates the camera's current exposure mode.</span></span> <span data-ttu-id="8d7c5-126">Приложение изменяет это свойство для управления режимом экспозиции устройства камеры.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-126">An application changes this property to control the exposure mode of the camera device.</span></span><br/> <span data-ttu-id="8d7c5-127">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-127">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span><br/> <span data-ttu-id="8d7c5-128">В следующей таблице приведены семь констант, допустимых для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-128">The following table has the seven constants that are valid with this property.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8d7c5-129">Режим экспозиции</span><span class="sxs-lookup"><span data-stu-id="8d7c5-129">Exposure Mode</span></span></th>
<th><span data-ttu-id="8d7c5-130">Описание</span><span class="sxs-lookup"><span data-stu-id="8d7c5-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d7c5-131">EXPOSUREMODE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="8d7c5-131">EXPOSUREMODE_MANUAL</span></span></td>
<td><span data-ttu-id="8d7c5-132">Скорость затвора и Апертура задаются пользователем.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-132">The shutter speed and aperture are set by the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d7c5-133">EXPOSUREMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="8d7c5-133">EXPOSUREMODE_AUTO</span></span></td>
<td><span data-ttu-id="8d7c5-134">Скорость затвора и Апертура автоматически устанавливаются камерой.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-134">The shutter speed and aperture are automatically set by the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d7c5-135">EXPOSUREMODE_APERTURE_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="8d7c5-135">EXPOSUREMODE_APERTURE_PRIORITY</span></span></td>
<td><span data-ttu-id="8d7c5-136">Апертура задается пользователем, а Камера автоматически устанавливает скорость затвора.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-136">The aperture is set by the user, and the camera automatically sets the shutter speed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d7c5-137">EXPOSUREMODE_SHUTTER_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="8d7c5-137">EXPOSUREMODE_SHUTTER_PRIORITY</span></span></td>
<td><span data-ttu-id="8d7c5-138">Скорость затвора задается пользователем, а Камера автоматически устанавливает апертуру.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-138">The shutter speed is set by the user, and the camera automatically sets the aperture.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d7c5-139">EXPOSUREMODE_PROGRAM_CREATIVE</span><span class="sxs-lookup"><span data-stu-id="8d7c5-139">EXPOSUREMODE_PROGRAM_CREATIVE</span></span></td>
<td><span data-ttu-id="8d7c5-140">Скорость затвора и Апертура автоматически устанавливаются камерой, оптимизированы для всех тем.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-140">The shutter speed and aperture are automatically set by the camera, optimized for still subject matter.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d7c5-141">EXPOSUREMODE_PROGRAM_ACTION</span><span class="sxs-lookup"><span data-stu-id="8d7c5-141">EXPOSUREMODE_PROGRAM_ACTION</span></span></td>
<td><span data-ttu-id="8d7c5-142">Скорость затвора и Апертура автоматически устанавливаются камерой, оптимизированы для сцен, содержащих быстрое перемещение.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-142">The shutter speed and aperture are automatically set by the camera, optimized for scenes containing fast motion.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d7c5-143">EXPOSUREMODE_PORTRAIT</span><span class="sxs-lookup"><span data-stu-id="8d7c5-143">EXPOSUREMODE_PORTRAIT</span></span></td>
<td><span data-ttu-id="8d7c5-144">Скорость затвора и Апертура автоматически задаются камерой, оптимизированной для книжной фотографии.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-144">The shutter speed and aperture are automatically set by the camera, optimized for portrait photography.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_COMP"></span><span id="wia_dpc_exposure_comp"></span><dl> <span data-ttu-id="8d7c5-145"><dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>камерадевицеекспосурекомп</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-145"><dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>CameraDeviceExposureComp</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-146">Позволяет корректировать точку установки элемента управления автоматической экспозиции цифровой камеры.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-146">Allows for the adjustment of the set point of the digital camera's auto-exposure control.</span></span> <span data-ttu-id="8d7c5-147">Например, нулевое значение не изменяет уровень автоэкспозиции фабрики.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-147">For example, a setting of zero does not change the factory-set auto-exposure level.</span></span> <span data-ttu-id="8d7c5-148">Единицы находятся в &quot; остановленных единицах &quot; , которые масштабируются с помощью коэффициента 1000, что позволяет использовать дробные значения Stop.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-148">The units are in &quot;stops&quot; that are scaled by a factor of 1000, to allow for fractional stop values.</span></span> <span data-ttu-id="8d7c5-149">Значение 2000 соответствует двум прекращениям (в четыре раза больше энергии на датчике), что дает более яркие образы.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-149">A setting of 2000 corresponds to two stops more exposure (four times more energy on the sensor), yielding brighter images.</span></span> <span data-ttu-id="8d7c5-150">Параметр-1000 соответствует одному снижению экспозиции (половина энергии на датчике), что дает более темные образы.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-150">A setting of -1000 corresponds to one stop less exposure (one-half the energy on the sensor) yielding darker images.</span></span> <span data-ttu-id="8d7c5-151">Значения параметра относятся к дополнительным системам фотографических раскрытия (ВЕРШИНЕ).</span><span class="sxs-lookup"><span data-stu-id="8d7c5-151">The setting values are in Additive System of Photographic Exposure (APEX) units.</span></span> <span data-ttu-id="8d7c5-152">Это свойство может быть выражено либо в виде списка, либо в диапазоне значений.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-152">This property may be expressed as either a list or a range of values.</span></span> <span data-ttu-id="8d7c5-153">Это свойство обычно используется только в том случае, если для устройства свойство <strong>WIA_DPC_EXPOSURE_MODE</strong> имеет значение EXPOSUREMODE_MANUAL.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-153">This property is typically used only when the device has the <strong>WIA_DPC_EXPOSURE_MODE</strong> property set to EXPOSUREMODE_MANUAL.</span></span></p>
<p><span data-ttu-id="8d7c5-154">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> или WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="8d7c5-154">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_TIME"></span><span id="wia_dpc_exposure_time"></span><dl> <span data-ttu-id="8d7c5-155"><dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>камерадевицеекспосуретиме</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-155"><dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>CameraDeviceExposureTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-156">Соответствует скорости затвора в секундах, которая масштабируется на 10 000.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-156">Corresponds to the shutter speed, in seconds that are scaled by 10,000.</span></span> <span data-ttu-id="8d7c5-157">Как правило, устройство использует это свойство только в том случае, если свойство <strong>WIA_DPC_EXPOSURE_MODE</strong> имеет значение EXPOSUREMODE_MANUAL или EXPOSUREMODE_SHUTTER_PRIORITY.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-157">Typically, the device uses this property only when the <strong>WIA_DPC_EXPOSURE_MODE</strong> property is set to EXPOSUREMODE_MANUAL or EXPOSUREMODE_SHUTTER_PRIORITY.</span></span></p>
<p><span data-ttu-id="8d7c5-158">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> или WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="8d7c5-158">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FNUMBER"></span><span id="wia_dpc_fnumber"></span><dl> <span data-ttu-id="8d7c5-159"><dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>камерадевицефнумбер</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-159"><dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>CameraDeviceFNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-160">Соответствует апертуре линзы в единицах числа f-останавливаютй, масштабируемых на 100.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-160">Corresponds to the aperture of the lens, in units of the f-stop number scaled by 100.</span></span> <span data-ttu-id="8d7c5-161">Значение этого свойства обычно допустимо, только если свойство <strong>WIA_DPC_EXPOSURE_MODE</strong> имеет значение EXPOSUREMODE_MANUAL или EXPOSUREMODE_APERTURE_PRIORITY.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-161">The setting of this property is typically valid only when the <strong>WIA_DPC_EXPOSURE_MODE</strong> property is set to EXPOSUREMODE_MANUAL or EXPOSUREMODE_APERTURE_PRIORITY.</span></span></p>
<p><span data-ttu-id="8d7c5-162">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-162">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FLASH_MODE"></span><span id="wia_dpc_flash_mode"></span><dl> <span data-ttu-id="8d7c5-163"><dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>камерадевицефлашмоде</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-163"><dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>CameraDeviceFlashMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-164">Определяет текущую настройку режима вспышки для устройства камеры.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-164">Defines the current flash mode setting for the camera device.</span></span> <span data-ttu-id="8d7c5-165">Драйвер устройства перечисляет поддерживаемые значения этого свойства.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-165">The device driver enumerates the supported values of this property.</span></span> <span data-ttu-id="8d7c5-166">Приложение записывает это свойство, чтобы установить режим вспышки для устройства камеры.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-166">An application writes this property to set the flash mode for the camera device.</span></span></p>
<p><span data-ttu-id="8d7c5-167">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-167">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="8d7c5-168">Следующая таблица содержит шесть констант, допустимых для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-168">The following table has the six constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8d7c5-169">Режим вспышки</span><span class="sxs-lookup"><span data-stu-id="8d7c5-169">Flash Mode</span></span></th>
<th><span data-ttu-id="8d7c5-170">Определение</span><span class="sxs-lookup"><span data-stu-id="8d7c5-170">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d7c5-171">FLASHMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="8d7c5-171">FLASHMODE_AUTO</span></span></td>
<td><span data-ttu-id="8d7c5-172">Устройство камеры определяет правильные параметры Flash.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-172">The camera device determines the proper flash settings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d7c5-173">FLASHMODE_FILL</span><span class="sxs-lookup"><span data-stu-id="8d7c5-173">FLASHMODE_FILL</span></span></td>
<td><span data-ttu-id="8d7c5-174">Устройство камеры настроено на вспышку независимо от текущих условий освещения.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-174">The camera device is configured to flash regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d7c5-175">FLASHMODE_OFF</span><span class="sxs-lookup"><span data-stu-id="8d7c5-175">FLASHMODE_OFF</span></span></td>
<td><span data-ttu-id="8d7c5-176">Устройство <em>камеры настроено</em> на невспышку для любых снимков.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-176">The camera device is configured <em>not</em> to flash for any picture taken.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d7c5-177">FLASHMODE_REDEYE_AUTO</span><span class="sxs-lookup"><span data-stu-id="8d7c5-177">FLASHMODE_REDEYE_AUTO</span></span></td>
<td><span data-ttu-id="8d7c5-178">Устройство камеры определяет правильные параметры Flash, используя сокращение красных глаз, независимо от текущих условий освещения.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-178">The camera device determines the proper flash settings using red-eye reduction, regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d7c5-179">FLASHMODE_REDEYE_FILL</span><span class="sxs-lookup"><span data-stu-id="8d7c5-179">FLASHMODE_REDEYE_FILL</span></span></td>
<td><span data-ttu-id="8d7c5-180">Устройство камеры настроено для использования сокращения красных глаз и флэш-памяти независимо от текущих условий освещения.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-180">The camera device is configured to use red-eye reduction and flash regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d7c5-181">FLASHMODE_EXTERNALSYNC</span><span class="sxs-lookup"><span data-stu-id="8d7c5-181">FLASHMODE_EXTERNALSYNC</span></span></td>
<td><span data-ttu-id="8d7c5-182">Устройство камеры настроено для синхронизации с внешними Flash-устройствами.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-182">The camera device is configured to synchronize with external flash units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MODE"></span><span id="wia_dpc_focus_mode"></span><dl> <span data-ttu-id="8d7c5-183"><dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>камерадевицефокусмоде</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-183"><dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>CameraDeviceFocusMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-184">Определяет текущее значение режима фокусировки для устройства камеры.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-184">Defines the current focus mode setting for the camera device.</span></span> <span data-ttu-id="8d7c5-185">Драйвер устройства перечисляет поддерживаемые значения этого свойства.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-185">The device driver enumerates the supported values of this property.</span></span> <span data-ttu-id="8d7c5-186">Приложение записывает это свойство, чтобы установить режим фокусировки для устройства камеры.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-186">An application writes this property to set the focus mode for the camera device.</span></span></p>
<p><span data-ttu-id="8d7c5-187">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-187">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="8d7c5-188">В следующей таблице приведены три константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-188">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8d7c5-189">Режим фокусировки</span><span class="sxs-lookup"><span data-stu-id="8d7c5-189">Focus Mode</span></span></th>
<th><span data-ttu-id="8d7c5-190">Описание</span><span class="sxs-lookup"><span data-stu-id="8d7c5-190">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d7c5-191">FOCUSMODE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="8d7c5-191">FOCUSMODE_MANUAL</span></span></td>
<td><span data-ttu-id="8d7c5-192">Устройство камеры настроено для разрешения пользователю сосредоточиться вручную.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-192">The camera device is configured to allow the user to focus manually.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d7c5-193">FOCUSMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="8d7c5-193">FOCUSMODE_AUTO</span></span></td>
<td><span data-ttu-id="8d7c5-194">Устройство камеры настроено для автоматического фокуса.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-194">The camera device is configured to focus automatically.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d7c5-195">FOCUSMODE_MACROAUTO</span><span class="sxs-lookup"><span data-stu-id="8d7c5-195">FOCUSMODE_MACROAUTO</span></span></td>
<td><span data-ttu-id="8d7c5-196">Устройство камеры настроено для автоматического фокусирования с использованием параметров макросов с коротким диапазоном.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-196">The camera device is configured to focus automatically using short-range macro settings.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MANUAL_DIST"></span><span id="wia_dpc_focus_manual_dist"></span><dl> <span data-ttu-id="8d7c5-197"><dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-197"><dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-198">Зарезервировано, не используйте.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-198">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="8d7c5-199">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-199">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ZOOM_POSITION"></span><span id="wia_dpc_zoom_position"></span><dl> <span data-ttu-id="8d7c5-200"><dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-200"><dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-201">Зарезервировано, не используйте.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-201">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="8d7c5-202">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-202">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PAN_POSITION"></span><span id="wia_dpc_pan_position"></span><dl> <span data-ttu-id="8d7c5-203"><dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>камерадевицепанпоситион</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-203"><dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>CameraDevicePanPosition</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-204">Зарезервировано, не используйте.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-204">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="8d7c5-205">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-205">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TILT_POSITION"></span><span id="wia_dpc_tilt_position"></span><dl> <span data-ttu-id="8d7c5-206"><dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>камерадевицетилтпоситион</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-206"><dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>CameraDeviceTiltPosition</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-207">Зарезервировано, не используйте.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-207">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="8d7c5-208">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-208">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_MODE"></span><span id="wia_dpc_timer_mode"></span><dl> <span data-ttu-id="8d7c5-209"><dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>камерадевицетимермоде</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-209"><dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>CameraDeviceTimerMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-210">Зарезервировано, не используйте.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-210">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="8d7c5-211">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-211">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_VALUE"></span><span id="wia_dpc_timer_value"></span><dl> <span data-ttu-id="8d7c5-212"><dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>камерадевицетимервалуе</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-212"><dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>CameraDeviceTimerValue</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-213">Зарезервировано, не используйте.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-213">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="8d7c5-214">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-214">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_POWER_MODE"></span><span id="wia_dpc_power_mode"></span><dl> <span data-ttu-id="8d7c5-215"><dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>камерадевицеповермоде</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-215"><dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>CameraDevicePowerMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-216">Определяет текущий источник питания для устройства камеры.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-216">Defines the current power source for the camera device.</span></span> <span data-ttu-id="8d7c5-217">Приложение считывает это свойство, чтобы определить, какой источник питания используется камерой.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-217">An application reads this property to determine what power source the camera is using.</span></span></p>
<p><span data-ttu-id="8d7c5-218">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-218">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="8d7c5-219">В следующей таблице приведены две константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-219">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8d7c5-220">Режим питания</span><span class="sxs-lookup"><span data-stu-id="8d7c5-220">Power Mode</span></span></th>
<th><span data-ttu-id="8d7c5-221">Описание</span><span class="sxs-lookup"><span data-stu-id="8d7c5-221">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d7c5-222">POWERMODE_LINE</span><span class="sxs-lookup"><span data-stu-id="8d7c5-222">POWERMODE_LINE</span></span></td>
<td><span data-ttu-id="8d7c5-223">Устройство камеры работает на адаптере питания.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-223">The camera device is operating on a power adapter.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d7c5-224">POWERMODE_BATTERY</span><span class="sxs-lookup"><span data-stu-id="8d7c5-224">POWERMODE_BATTERY</span></span></td>
<td><span data-ttu-id="8d7c5-225">Устройство камеры работает с питанием от аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-225">The camera device is operating on battery power.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BATTERY_STATUS"></span><span id="wia_dpc_battery_status"></span><dl> <span data-ttu-id="8d7c5-226"><dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>камерадевицебаттеристатус</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-226"><dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>CameraDeviceBatteryStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-227">Процент питания от аккумулятора, который остается в работе устройства камеры.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-227">The percentage of battery power that is left to operate the camera device.</span></span> <span data-ttu-id="8d7c5-228">Это значение должно быть целым числом от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-228">This value should be an integer from 0 through 100.</span></span> <span data-ttu-id="8d7c5-229">Приложение считывает это свойство, чтобы определить оставшийся срок работы аккумулятора устройства камеры.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-229">An application reads this property to determine the remaining battery life of the camera device.</span></span></p>
<p><span data-ttu-id="8d7c5-230">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-230">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_WIDTH"></span><span id="wia_dpc_thumb_width"></span><dl> <span data-ttu-id="8d7c5-231"><dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>камерадевицесумбвидс</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-231"><dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>CameraDeviceThumbWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-232">Ширина (в пикселях) эскиза изображения, используемого для вновь захваченных изображений.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-232">The width, in pixels, of a thumbnail image to use for newly captured images.</span></span> <span data-ttu-id="8d7c5-233">Приложение считывает это значение, чтобы получить приблизительный размер для отображения эскизов в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-233">An application reads this value to get an estimated size for displaying thumbnails in its user interface.</span></span></p>
<p><span data-ttu-id="8d7c5-234">Тип: <strong>VT_I4</strong>, доступ: чтение и запись (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) или только для чтения (WIA_PROP_NONE), допустимые значения: WIA_PROP_LIST или WIA_PROP_NONE</span><span class="sxs-lookup"><span data-stu-id="8d7c5-234">Type: <strong>VT_I4</strong>, Access: Read/Write (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) or Read Only (WIA_PROP_NONE), Valid values: WIA_PROP_LIST or WIA_PROP_NONE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_HEIGHT"></span><span id="wia_dpc_thumb_height"></span><dl> <span data-ttu-id="8d7c5-235"><dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>камерадевицесумбхеигхт</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-235"><dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>CameraDeviceThumbHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-236">Ширина (в пикселях) эскиза изображения, используемого для вновь захваченных изображений.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-236">The width, in pixels, of a thumbnail image to use for newly captured images.</span></span> <span data-ttu-id="8d7c5-237">Приложение считывает это значение, чтобы получить приблизительный размер для отображения эскизов в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-237">An application reads this value to get an estimated size for displaying thumbnails in its user interface.</span></span></p>
<p><span data-ttu-id="8d7c5-238">Тип: <strong>VT_I4</strong>, доступ: чтение и запись (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) или только для чтения (WIA_PROP_NONE), допустимые значения: WIA_PROP_LIST или WIA_PROP_NONE</span><span class="sxs-lookup"><span data-stu-id="8d7c5-238">Type: <strong>VT_I4</strong>, Access: Read/Write (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) or Read Only (WIA_PROP_NONE), Valid values: WIA_PROP_LIST or WIA_PROP_NONE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICT_WIDTH"></span><span id="wia_dpc_pict_width"></span><dl> <span data-ttu-id="8d7c5-239"><dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>камерадевицепиктвидс</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-239"><dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>CameraDevicePictWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-240">Ширина в пикселях, используемая для вновь захваченных изображений.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-240">The width in pixels to use for newly captured images.</span></span> <span data-ttu-id="8d7c5-241">Список допустимых значений для этого свойства имеет соответствие "один к одному" списку допустимых значений для свойства <strong>WIA_DPC_PICT_HEIGHT</strong> .</span><span class="sxs-lookup"><span data-stu-id="8d7c5-241">The list of valid values for this property has a one-to-one correspondence to the list of valid values for the <strong>WIA_DPC_PICT_HEIGHT</strong> property.</span></span> <span data-ttu-id="8d7c5-242">Если отдельные ширина и высота линейно устанавливаются и ортогональны друг к другу, они могут быть выражены в виде диапазона.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-242">If the individual width and height are linearly settable and orthogonal to each other, they may be expressed as a range.</span></span></p>
<p><span data-ttu-id="8d7c5-243">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="8d7c5-243">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICT_HEIGHT"></span><span id="wia_dpc_pict_height"></span><dl> <span data-ttu-id="8d7c5-244"><dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>камерадевицепиксеигхт</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-244"><dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>CameraDevicePictHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-245">Высота в пикселях, используемая для вновь захваченных изображений.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-245">The height in pixels to use for newly captured images.</span></span> <span data-ttu-id="8d7c5-246">Список допустимых значений для этого свойства имеет соответствие "один к одному" со списком допустимых значений для свойства <strong>WIA_DPC_PICT_WIDTH</strong> .</span><span class="sxs-lookup"><span data-stu-id="8d7c5-246">The list of valid values for this property has a one-to-one correspondence with the list of valid values for the <strong>WIA_DPC_PICT_WIDTH</strong> property.</span></span> <span data-ttu-id="8d7c5-247">Если отдельные ширина и высота линейно устанавливаются и ортогональны друг к другу, они могут быть выражены в виде диапазона.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-247">If the individual width and height are linearly settable and orthogonal to each other, they may be expressed as a range.</span></span></p>
<p><span data-ttu-id="8d7c5-248">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="8d7c5-248">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIMENSION"></span><span id="wia_dpc_dimension"></span><dl> <span data-ttu-id="8d7c5-249"><dt><strong>WIA_DPC_DIMENSION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-249"><dt><strong>WIA_DPC_DIMENSION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-250">Зарезервировано, не используйте.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-250">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="8d7c5-251">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-251">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_COMPRESSION_SETTING"></span><span id="wia_dpc_compression_setting"></span><dl> <span data-ttu-id="8d7c5-252"><dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>камерадевицекомпрессионсеттинг</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-252"><dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>CameraDeviceCompressionSetting</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-253">Предназначен для приблизительного линейного использования в отношении воспринимаемого изображения по широкому спектру содержимого сцены и содержит либо диапазон, либо список целых чисел.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-253">Intended to be approximately linear with respect to perceived image quality over a broad range of scene content, and it contains either a range or a list of integers.</span></span> <span data-ttu-id="8d7c5-254">Небольшие целые числа используются для представления низкого качества (то есть максимального сжатия), а большие целые числа используются для представления более высокого качества (то есть минимального сжатия).</span><span class="sxs-lookup"><span data-stu-id="8d7c5-254">Smaller integers are used to represent lower quality (that is, maximum compression), whereas larger integers are used to represent higher quality (that is, minimum compression).</span></span> <span data-ttu-id="8d7c5-255">Все доступные параметры на устройстве относительны только для этого устройства и, следовательно, специфичны для устройства.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-255">Any available settings on a device are relative only to that device and are therefore device specific.</span></span></p>
<p><span data-ttu-id="8d7c5-256">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="8d7c5-256">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING"></span><span id="wia_dpc_focus_metering"></span><dl> <span data-ttu-id="8d7c5-257"><dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-257"><dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-258">Зарезервировано, не используйте.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-258">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="8d7c5-259">Тип: <strong>VT_I4</strong>, доступ: только для чтения, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-259">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_INTERVAL"></span><span id="wia_dpc_timelapse_interval"></span><dl> <span data-ttu-id="8d7c5-260"><dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>камерадевицетимелапсеинтервал</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-260"><dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>CameraDeviceTimelapseInterval</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-261">Время в миллисекундах между записью образа в операции записи промежутка времени.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-261">The time, in milliseconds, between image captures in a time-lapse capture operation.</span></span></p>
<p><span data-ttu-id="8d7c5-262">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST или WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="8d7c5-262">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_NUMBER"></span><span id="wia_dpc_timelapse_number"></span><dl> <span data-ttu-id="8d7c5-263"><dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>камерадевицетимелапсенумбер</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-263"><dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>CameraDeviceTimelapseNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-264">Число образов, которые устройство пытается захватить во время записи промежутка времени.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-264">The number of images the device attempts to capture during a time-lapse capture.</span></span></p>
<p><span data-ttu-id="8d7c5-265">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST или WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="8d7c5-265">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BURST_INTERVAL"></span><span id="wia_dpc_burst_interval"></span><dl> <span data-ttu-id="8d7c5-266"><dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>камерадевицебурстинтервал</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-266"><dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>CameraDeviceBurstInterval</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-267">Время в миллисекундах между записью изображения во время операции пакетной передачи.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-267">The time, in milliseconds, between image captures during a burst operation.</span></span></p>
<p><span data-ttu-id="8d7c5-268">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST или WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="8d7c5-268">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_BURST_NUMBER"></span><span id="wia_dpc_burst_number"></span><dl> <span data-ttu-id="8d7c5-269"><dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>камерадевицебурстнумбер</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-269"><dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>CameraDeviceBurstNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-270">Число образов, которые устройство пытается захватить во время операции пакетной работы.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-270">The number of images the device attempts to capture during a burst operation.</span></span></p>
<p><span data-ttu-id="8d7c5-271">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST или WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="8d7c5-271">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EFFECT_MODE"></span><span id="wia_dpc_effect_mode"></span><dl> <span data-ttu-id="8d7c5-272"><dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>камерадевицееффектмоде</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-272"><dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>CameraDeviceEffectMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-273">Указывает режим получения специального изображения камеры.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-273">Specifies the special image acquisition mode of the camera.</span></span></p>
<p><span data-ttu-id="8d7c5-274">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-274">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="8d7c5-275">В следующей таблице приведены три константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-275">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8d7c5-276">Режим эффектов</span><span class="sxs-lookup"><span data-stu-id="8d7c5-276">Effect Mode</span></span></th>
<th><span data-ttu-id="8d7c5-277">Описание</span><span class="sxs-lookup"><span data-stu-id="8d7c5-277">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d7c5-278">EFFECTMODE_STANDARD</span><span class="sxs-lookup"><span data-stu-id="8d7c5-278">EFFECTMODE_STANDARD</span></span></td>
<td><span data-ttu-id="8d7c5-279">Запись изображения в стандартном режиме для камеры.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-279">Capture an image in the standard mode for the camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d7c5-280">EFFECTMODE_BW</span><span class="sxs-lookup"><span data-stu-id="8d7c5-280">EFFECTMODE_BW</span></span></td>
<td><span data-ttu-id="8d7c5-281">Запись изображения в градациях серого.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-281">Capture a grayscale image.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d7c5-282">EFFECTMODE_SEPIA</span><span class="sxs-lookup"><span data-stu-id="8d7c5-282">EFFECTMODE_SEPIA</span></span></td>
<td><span data-ttu-id="8d7c5-283">Запишите образ выцветшей.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-283">Capture a sepia image.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIGITAL_ZOOM"></span><span id="wia_dpc_digital_zoom"></span><dl> <span data-ttu-id="8d7c5-284"><dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>камерадевицедигиталзум</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-284"><dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>CameraDeviceDigitalZoom</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-285">Эффективное масштабирование полученного образа цифровой камеры с коэффициентом, равным 10.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-285">The effective zoom ratio of the digital camera's acquired image, scaled by a factor of 10.</span></span> <span data-ttu-id="8d7c5-286">Значение 10 соответствует отсутствию цифрового масштаба (1X), то есть стандартного размера сцены, захваченного камерой.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-286">A value of 10 corresponds to the absence of digital zoom (1X), which is the standard scene size captured by the camera.</span></span> <span data-ttu-id="8d7c5-287">Значение 20 соответствует удвоенному масштабу, где камера захватывает один квартал стандартного размера сцены.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-287">A value of 20 corresponds to a 2X zoom, where one-quarter of the standard scene size is captured by the camera.</span></span></p>
<p><span data-ttu-id="8d7c5-288">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="8d7c5-288">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_SHARPNESS"></span><span id="wia_dpc_sharpness"></span><dl> <span data-ttu-id="8d7c5-289"><dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>камерадевицешарпнесс</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-289"><dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>CameraDeviceSharpness</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-290">Воспринимаемая резкость захваченного изображения.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-290">The perceived sharpness of a captured image.</span></span> <span data-ttu-id="8d7c5-291">Это свойство может использовать либо список значений, либо диапазон значений.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-291">This property can use either a list of values or a range of values.</span></span> <span data-ttu-id="8d7c5-292">Минимальное значение представляет собой наименьший уровень резкости, тогда как максимальное значение представляет максимальную резкость.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-292">The minimum value represents the least amount of sharpness, whereas the maximum value represents the maximum sharpness.</span></span> <span data-ttu-id="8d7c5-293">Обычно значение в середине диапазона представляет нормальную, или по умолчанию четкость.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-293">Typically a value in the middle of the range represents normal, or default, sharpness.</span></span></p>
<p><span data-ttu-id="8d7c5-294">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="8d7c5-294">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CONTRAST"></span><span id="wia_dpc_contrast"></span><dl> <span data-ttu-id="8d7c5-295"><dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>камерадевицеконтраст</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-295"><dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>CameraDeviceContrast</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-296">Воспринимаемая контрастность захваченного изображения.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-296">The perceived contrast of a captured image.</span></span> <span data-ttu-id="8d7c5-297">Это свойство может содержать либо список значений, либо диапазон значений.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-297">This property can contain either a list of values or a range of values.</span></span> <span data-ttu-id="8d7c5-298">Минимальное поддерживаемое значение представляет наименьшую степень контрастности, в то время как максимальное значение соответствует наибольшему контрасту.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-298">The minimum supported value represents the least amount of contrast, whereas the maximum value represents the most contrast.</span></span> <span data-ttu-id="8d7c5-299">Как правило, значение в середине диапазона представляет собой нормальную или по умолчанию, контрастность.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-299">Typically, a value in the middle of the range represents normal, or default, contrast.</span></span></p>
<p><span data-ttu-id="8d7c5-300">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="8d7c5-300">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_MODE"></span><span id="wia_dpc_capture_mode"></span><dl> <span data-ttu-id="8d7c5-301"><dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>камерадевицекаптуремоде</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-301"><dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>CameraDeviceCaptureMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-302">Задает режим записи образа.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-302">Sets the image capture mode.</span></span></p>
<p><span data-ttu-id="8d7c5-303">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-303">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="8d7c5-304">В следующей таблице приведены три константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-304">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8d7c5-305">Режим записи</span><span class="sxs-lookup"><span data-stu-id="8d7c5-305">Capture Mode</span></span></th>
<th><span data-ttu-id="8d7c5-306">Описание</span><span class="sxs-lookup"><span data-stu-id="8d7c5-306">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d7c5-307">CAPTUREMODE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="8d7c5-307">CAPTUREMODE_NORMAL</span></span></td>
<td><span data-ttu-id="8d7c5-308">Нормальный режим для камеры.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-308">Normal mode for the camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d7c5-309">CAPTUREMODE_BURST</span><span class="sxs-lookup"><span data-stu-id="8d7c5-309">CAPTUREMODE_BURST</span></span></td>
<td><span data-ttu-id="8d7c5-310">Зафиксируйте более одного образа в быстром выполнении, как определено значениями свойств <strong>WIA_DPC_BURST_NUMBER</strong> и <strong>WIA_DPC_BURST_INTERVAL</strong> .</span><span class="sxs-lookup"><span data-stu-id="8d7c5-310">Capture more than one image in quick succession as defined by the values of the <strong>WIA_DPC_BURST_NUMBER</strong> and <strong>WIA_DPC_BURST_INTERVAL</strong> properties.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d7c5-311">CAPTUREMODE_TIMELAPSE</span><span class="sxs-lookup"><span data-stu-id="8d7c5-311">CAPTUREMODE_TIMELAPSE</span></span></td>
<td><span data-ttu-id="8d7c5-312">Захватите более одного образа в случае успеха, как определено в свойствах <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> и <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> .</span><span class="sxs-lookup"><span data-stu-id="8d7c5-312">Capture more than one image in succession as defined by the <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> and <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> properties.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_DELAY"></span><span id="wia_dpc_capture_delay"></span><dl> <span data-ttu-id="8d7c5-313"><dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>камерадевицекаптуределай</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-313"><dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>CameraDeviceCaptureDelay</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-314">Значение, представляющее количество времени задержки (в миллисекундах), которое должно быть вставлено между триггером записи и фактической инициацией записи данных.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-314">The value representing the amount of time delay, in milliseconds, that should be inserted between the capture trigger and the actual initiation of the data capture.</span></span> <span data-ttu-id="8d7c5-315">Это свойство не предназначено для описания времени между кадрами для одной инициации, нескольких захватов, таких как пакет или промежуток времени, которые имеют отдельные свойства интервала <strong>WIA_DPC_BURST_INTERVAL</strong> и <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-315">This property is not intended to be used to describe the time between frames for single-initiation, multiple captures such as burst or time lapse, which have separate interval properties <strong>WIA_DPC_BURST_INTERVAL</strong> and <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>.</span></span> <span data-ttu-id="8d7c5-316">В таких случаях он по-прежнему выступает в качестве начальной задержки перед записью первого изображения в ряде, независимо от времени между кадрами.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-316">In those cases, it still serves as an initial delay before the first image in the series is captured, independent of the time between frames.</span></span> <span data-ttu-id="8d7c5-317">Для без задержки до записи это свойство должно иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-317">For no precapture delay, this property should be set to zero.</span></span></p>
<p><span data-ttu-id="8d7c5-318">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="8d7c5-318">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_INDEX"></span><span id="wia_dpc_exposure_index"></span><dl> <span data-ttu-id="8d7c5-319"><dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>камерадевицеекспосуреиндекс</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-319"><dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>CameraDeviceExposureIndex</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-320">Разрешает эмуляцию параметров скорости пленки на цифровой камере.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-320">Allows for the emulation of film speed settings on a digital camera.</span></span> <span data-ttu-id="8d7c5-321">Параметры соответствуют стандартам ISO (ASA/DIN).</span><span class="sxs-lookup"><span data-stu-id="8d7c5-321">The settings correspond to the ISO designations (ASA/DIN).</span></span> <span data-ttu-id="8d7c5-322">Как правило, устройство поддерживает дискретные перечислимые значения, но возможно непрерывное управление диапазоном значений.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-322">Typically, a device supports discrete enumerated values, but continuous control over a range of values is possible.</span></span> <span data-ttu-id="8d7c5-323">Значение 0xFFFF соответствует автоматическому параметру ISO.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-323">A value of 0xFFFF corresponds to the Automatic ISO setting.</span></span></p>
<p><span data-ttu-id="8d7c5-324">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="8d7c5-324">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_METERING_MODE"></span><span id="wia_dpc_exposure_metering_mode"></span><dl> <span data-ttu-id="8d7c5-325"><dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>камерадевицеекспосуреметерингмоде</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-325"><dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>CameraDeviceExposureMeteringMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-326">Указывает режим, используемый камерой для автоматической настройки параметра экспозиции.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-326">Specifies the mode the camera uses to automatically adjust the exposure setting.</span></span></p>
<p><span data-ttu-id="8d7c5-327">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-327">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8d7c5-328">Режим измерения экспозиции</span><span class="sxs-lookup"><span data-stu-id="8d7c5-328">Exposure Metering Mode</span></span></th>
<th><span data-ttu-id="8d7c5-329">Описание</span><span class="sxs-lookup"><span data-stu-id="8d7c5-329">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d7c5-330">EXPOSUREMETERING_AVERAGE</span><span class="sxs-lookup"><span data-stu-id="8d7c5-330">EXPOSUREMETERING_AVERAGE</span></span></td>
<td><span data-ttu-id="8d7c5-331">Установите экспозицию на основе среднего значения всей сцены.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-331">Set the exposure based on an average of the entire scene.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d7c5-332">EXPOSUREMETERING_CENTERWEIGHT</span><span class="sxs-lookup"><span data-stu-id="8d7c5-332">EXPOSUREMETERING_CENTERWEIGHT</span></span></td>
<td><span data-ttu-id="8d7c5-333">Установите экспозицию на основе среднего взвешенного значения.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-333">Set the exposure based on a center-weighted average.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d7c5-334">EXPOSUREMETERING_MULTISPOT</span><span class="sxs-lookup"><span data-stu-id="8d7c5-334">EXPOSUREMETERING_MULTISPOT</span></span></td>
<td><span data-ttu-id="8d7c5-335">Установите экспозицию на основе многоточечного шаблона.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-335">Set the exposure based on a multispot pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d7c5-336">EXPOSUREMETERING_CENTERSPOT</span><span class="sxs-lookup"><span data-stu-id="8d7c5-336">EXPOSUREMETERING_CENTERSPOT</span></span></td>
<td><span data-ttu-id="8d7c5-337">Установите экспозицию на основе центральной точки.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-337">Set the exposure based on a center spot.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING_MODE"></span><span id="wia_dpc_focus_metering_mode"></span><dl> <span data-ttu-id="8d7c5-338"><dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>камерадевицефокусметерингмоде</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-338"><dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>CameraDeviceFocusMeteringMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-339">Указывает режим, используемый камерой для автоматического регулирования фокуса.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-339">Specifies the mode the camera uses to automatically adjust the focus.</span></span></p>
<p><span data-ttu-id="8d7c5-340">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-340">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="8d7c5-341">В следующей таблице приведены две константы, допустимые для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-341">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8d7c5-342">Режим измерения фокуса</span><span class="sxs-lookup"><span data-stu-id="8d7c5-342">Focus Metering Mode</span></span></th>
<th><span data-ttu-id="8d7c5-343">Описание</span><span class="sxs-lookup"><span data-stu-id="8d7c5-343">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d7c5-344">FOCUSMETERING_CENTERSPOT</span><span class="sxs-lookup"><span data-stu-id="8d7c5-344">FOCUSMETERING_CENTERSPOT</span></span></td>
<td><span data-ttu-id="8d7c5-345">Регулировка фокуса на основе центральной точки.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-345">Adjust the focus based on a center spot.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d7c5-346">FOCUSMETERING_MULTISPOT</span><span class="sxs-lookup"><span data-stu-id="8d7c5-346">FOCUSMETERING_MULTISPOT</span></span></td>
<td><span data-ttu-id="8d7c5-347">Настройка фокуса на основе многоточечного шаблона.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-347">Adjust the focus based on a multispot pattern.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_DISTANCE"></span><span id="wia_dpc_focus_distance"></span><dl> <span data-ttu-id="8d7c5-348"><dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>камерадевицефокусдистанце</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-348"><dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>CameraDeviceFocusDistance</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-349">Расстояние в миллиметрах между плоскостью захвата изображения цифровой камеры и точкой фокусировки.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-349">The distance, in millimeters, between the image-capturing plane of the digital camera and the point of focus.</span></span> <span data-ttu-id="8d7c5-350">Значение 0xFFFF соответствует параметру, превышающему 655 метров.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-350">A value of 0xFFFF corresponds to a setting greater than 655 meters.</span></span></p>
<p><span data-ttu-id="8d7c5-351">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> или WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="8d7c5-351">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCAL_LENGTH"></span><span id="wia_dpc_focal_length"></span><dl> <span data-ttu-id="8d7c5-352"><dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>камерадевицефокалленгс</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-352"><dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>CameraDeviceFocalLength</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-353">35mm-эквивалентная Длина фокуса.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-353">The 35mm-equivalent focal length.</span></span> <span data-ttu-id="8d7c5-354">Значения этого свойства соответствуют фокусной длине в миллиметрах, умноженной на 100.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-354">The values of this property correspond to the focal length in millimeters multiplied by 100.</span></span> <span data-ttu-id="8d7c5-355">Фокусная длина определяет оптический масштаб.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-355">The focal length determines the optical zoom.</span></span></p>
<p><span data-ttu-id="8d7c5-356">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-356">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_RGB_GAIN"></span><span id="wia_dpc_rgb_gain"></span><dl> <span data-ttu-id="8d7c5-357"><dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>камерадевицергбгаин</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-357"><dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>CameraDeviceRGBGain</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-358">Строка в Юникоде, заканчивающаяся нулем, которая представляет собой усиление красного, зеленого и синего коэффициента, применяемое к данным изображения соответственно.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-358">A null-terminated Unicode string that represents the red, green, and blue gain applied to image data, respectively.</span></span> <span data-ttu-id="8d7c5-359">Например, &quot; 4:25:50 &quot; представляет красную усиление 4, зеленое усиление 25 и синее усиление 50.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-359">For example, &quot;4:25:50&quot; represents a red gain of 4, a green gain of 25, and a blue gain of 50.</span></span></p>
<p><span data-ttu-id="8d7c5-360">Тип: <strong>VT_BSTR</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-360">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_WHITE_BALANCE"></span><span id="wia_dpc_white_balance"></span><dl> <span data-ttu-id="8d7c5-361"><dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>камерадевицевхитебаланце</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-361"><dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>CameraDeviceWhiteBalance</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-362">Указывает, как цветовые каналы плотности цифровых камер.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-362">Specifies how the digital camera weights color channels.</span></span></p>
<p><span data-ttu-id="8d7c5-363">Тип: <strong>VT_I4</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-363">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="8d7c5-364">Ниже приведен список возможных значений для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-364">The following is a list of possible values for this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8d7c5-365">Баланс белого</span><span class="sxs-lookup"><span data-stu-id="8d7c5-365">White Balance</span></span></th>
<th><span data-ttu-id="8d7c5-366">Описание</span><span class="sxs-lookup"><span data-stu-id="8d7c5-366">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d7c5-367">WHITEBALANCE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="8d7c5-367">WHITEBALANCE_MANUAL</span></span></td>
<td><span data-ttu-id="8d7c5-368">Белый баланс задается непосредственно с помощью свойства <strong>WIA_DPC_RGB_GAIN</strong> .</span><span class="sxs-lookup"><span data-stu-id="8d7c5-368">The white balance is set directly using the <strong>WIA_DPC_RGB_GAIN</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d7c5-369">WHITEBALANCE_AUTO</span><span class="sxs-lookup"><span data-stu-id="8d7c5-369">WHITEBALANCE_AUTO</span></span></td>
<td><span data-ttu-id="8d7c5-370">Камера использует автоматический механизм для установки баланса белого.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-370">The camera uses an automatic mechanism to set the white balance.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d7c5-371">WHITEBALANCE_ONEPUSH_AUTO</span><span class="sxs-lookup"><span data-stu-id="8d7c5-371">WHITEBALANCE_ONEPUSH_AUTO</span></span></td>
<td><span data-ttu-id="8d7c5-372">Камера определяет параметр баланс белого, когда пользователь нажимает кнопку захвата, указывая камеру на белой поверхности.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-372">The camera determines the white balance setting when a user presses the capture button while pointing the camera at a white surface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d7c5-373">WHITEBALANCE_DAYLIGHT</span><span class="sxs-lookup"><span data-stu-id="8d7c5-373">WHITEBALANCE_DAYLIGHT</span></span></td>
<td><span data-ttu-id="8d7c5-374">Камера устанавливает баланс белого по значению, подходящему для использования в летних условиях.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-374">The camera sets the white balance to a value appropriate for use in daylight conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d7c5-375">WHITEBALANCE_FLORESCENT</span><span class="sxs-lookup"><span data-stu-id="8d7c5-375">WHITEBALANCE_FLORESCENT</span></span></td>
<td><span data-ttu-id="8d7c5-376">Камера устанавливает баланс белого по значению, подходящему для использования с дневным источником освещения.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-376">The camera sets the white balance to a value appropriate for use with a fluorescent light source.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d7c5-377">WHITEBALANCE_TUNGSTEN</span><span class="sxs-lookup"><span data-stu-id="8d7c5-377">WHITEBALANCE_TUNGSTEN</span></span></td>
<td><span data-ttu-id="8d7c5-378">Камера устанавливает баланс белого на значение, подходящее для использования с источником освещения тунгстен.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-378">The camera sets the white balance to a value appropriate for use with a tungsten light source.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d7c5-379">WHITEBALANCE_FLASH</span><span class="sxs-lookup"><span data-stu-id="8d7c5-379">WHITEBALANCE_FLASH</span></span></td>
<td><span data-ttu-id="8d7c5-380">Камера устанавливает баланс белого на значение, подходящее для использования с электронной Flash.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-380">The camera sets the white balance to a value appropriate for use with an electronic flash.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_UPLOAD_URL"></span><span id="wia_dpc_upload_url"></span><dl> <span data-ttu-id="8d7c5-381"><dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>камерадевицеуплоадурл</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-381"><dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>CameraDeviceUploadURL</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-382">Описывает URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-382">Describes a URL.</span></span> <span data-ttu-id="8d7c5-383">URL-адрес, описываемый этим пророперти, — это один из следующих сценариев, в который можно передать изображения или объекты после их получения с устройства.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-383">The URL described by this proroperty is one that images or objects, after they are acquired from the device, can be uploaded to—according to one of the following scenarios.</span></span></p>
<ul>
<li><span data-ttu-id="8d7c5-384">Приложение WIA считывает это свойство и позволяет пользователю автоматически отправлять изображения по URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-384">A WIA application reads this property and allows the user to automatically upload images to the URL.</span></span></li>
<li><span data-ttu-id="8d7c5-385">Приложение задает URL-адрес, а другие устройства (киоски и т. д.) используют это свойство.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-385">An application sets the URL, and other devices (kiosks and so forth) use this property.</span></span></li>
</ul>
<p><span data-ttu-id="8d7c5-386">Microsoft Windows не передает образы сами по себе.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-386">Microsoft Windows does not upload images by itself.</span></span></p>
<p><span data-ttu-id="8d7c5-387">Тип: <strong>VT_BSTR</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-387">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ARTIST"></span><span id="wia_dpc_artist"></span><dl> <span data-ttu-id="8d7c5-388"><dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>камерадевицеартист</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-388"><dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>CameraDeviceArtist</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-389">Имя владельца (текущего пользователя) устройства.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-389">The name of the owner ( which is the current user) of the device.</span></span> <span data-ttu-id="8d7c5-390">Устройство использует это свойство для заполнения поля исполнителя во всех изображениях EXIF, которые он захватывает.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-390">The device uses this property to populate the Artist field in every EXIF image that it captures.</span></span></p>
<p><span data-ttu-id="8d7c5-391">Тип: <strong>VT_BSTR</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-391">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_COPYRIGHT_INFO"></span><span id="wia_dpc_copyright_info"></span><dl> <span data-ttu-id="8d7c5-392"><dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>камерадевицекопиригхтинфо</dt> </span><span class="sxs-lookup"><span data-stu-id="8d7c5-392"><dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>CameraDeviceCopyrightInfo</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="8d7c5-393">Уведомление об авторских правах.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-393">The copyright notification.</span></span> <span data-ttu-id="8d7c5-394">Устройство использует это свойство для заполнения поля Copyright в каждом образе EXIF, который он захватывает.</span><span class="sxs-lookup"><span data-stu-id="8d7c5-394">The device uses this property to populate the Copyright field in every EXIF image that it captures.</span></span></p>
<p><span data-ttu-id="8d7c5-395">Тип: <strong>VT_BSTR</strong>, доступ: чтение и запись, допустимые значения: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="8d7c5-395">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="8d7c5-396">Требования</span><span class="sxs-lookup"><span data-stu-id="8d7c5-396">Requirements</span></span>



| <span data-ttu-id="8d7c5-397">Требование</span><span class="sxs-lookup"><span data-stu-id="8d7c5-397">Requirement</span></span> | <span data-ttu-id="8d7c5-398">Значение</span><span class="sxs-lookup"><span data-stu-id="8d7c5-398">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8d7c5-399">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d7c5-399">Minimum supported client</span></span><br/> | <span data-ttu-id="8d7c5-400">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8d7c5-400">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="8d7c5-401">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d7c5-401">Minimum supported server</span></span><br/> | <span data-ttu-id="8d7c5-402">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8d7c5-402">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8d7c5-403">Header</span><span class="sxs-lookup"><span data-stu-id="8d7c5-403">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d7c5-404"><dt>Виадеф. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d7c5-404"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




