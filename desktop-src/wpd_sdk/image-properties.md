---
description: Портативные устройства Windows поддерживают следующие свойства образа.
ms.assetid: fb1707a7-16b0-4073-b21d-2ba2f4fd76f7
title: Свойства изображения (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 959a008d9c30991058226e52db6e45ed417ee6e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669453"
---
# <a name="image-properties"></a><span data-ttu-id="2acec-103">Свойства изображения</span><span class="sxs-lookup"><span data-stu-id="2acec-103">Image Properties</span></span>

<span data-ttu-id="2acec-104">Портативные устройства Windows поддерживают следующие свойства образа.</span><span class="sxs-lookup"><span data-stu-id="2acec-104">Windows Portable Devices supports the following image properties.</span></span>



| <span data-ttu-id="2acec-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="2acec-105">Property</span></span>                                                                                                                                       | <span data-ttu-id="2acec-106">VarType</span><span class="sxs-lookup"><span data-stu-id="2acec-106">VarType</span></span>     | <span data-ttu-id="2acec-107">Описание</span><span class="sxs-lookup"><span data-stu-id="2acec-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2acec-108">**\_битдепс образа \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="2acec-108">**WPD\_IMAGE\_BITDEPTH**</span></span>                                                                                                                       | <span data-ttu-id="2acec-109">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="2acec-109">**VT\_UI4**</span></span> | <span data-ttu-id="2acec-110">Битовая глубина изображения.</span><span class="sxs-lookup"><span data-stu-id="2acec-110">The bit depth of the image.</span></span>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="2acec-111"><span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**\_ \_ \_ Исправлено состояние цвета образа WPD \_**</span><span class="sxs-lookup"><span data-stu-id="2acec-111"><span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**WPD\_IMAGE\_COLOR\_CORRECTED\_STATUS**</span></span> | <span data-ttu-id="2acec-112">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="2acec-112">**VT\_UI4**</span></span> | <span data-ttu-id="2acec-113">Перечисление [**\_ \_ \_ \_ значений состояния WPD Color**](wpd-color-corrected-status-values.md) , указывающее, был ли файл исправлен цветом. Это предотвращает автоматическое выделение цветом изображения во время последующей обработки на нескольких устройствах.</span><span class="sxs-lookup"><span data-stu-id="2acec-113">A [**WPD\_COLOR\_CORRECTED\_STATUS\_VALUES**](wpd-color-corrected-status-values.md) enumeration that specifies whether the file has been color-corrected.This prevents multiple devices from automatically color-correcting the image during post-processing.</span></span><br/>                                                                       |
| <span data-ttu-id="2acec-114">**\_ \_ состояние кадрированного изображения \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="2acec-114">**WPD\_IMAGE\_CROPPED\_STATUS**</span></span>                                                                                                                | <span data-ttu-id="2acec-115">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="2acec-115">**VT\_UI4**</span></span> | <span data-ttu-id="2acec-116">Перечисление [**\_ \_ \_ значений состояния WPD**](wpd-cropped-status-values.md) , которое указывает, обрезан ли файл. Это предотвращает автоматическую обрезку изображения на нескольких устройствах во время последующей обработки.</span><span class="sxs-lookup"><span data-stu-id="2acec-116">A [**WPD\_CROPPED\_STATUS\_VALUES**](wpd-cropped-status-values.md) enumeration that specifies whether the file has been cropped.This prevents multiple devices from automatically cropping the image during post-processing.</span></span><br/>                                                                                                        |
| <span data-ttu-id="2acec-117">**\_ \_ индекс экспозиции образа WPD \_**</span><span class="sxs-lookup"><span data-stu-id="2acec-117">**WPD\_IMAGE\_EXPOSURE\_INDEX**</span></span>                                                                                                                | <span data-ttu-id="2acec-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="2acec-118">**VT\_UI4**</span></span> | <span data-ttu-id="2acec-119">Значение, определяющее настройки скорости пленки при записи этого образа. Параметры соответствуют стандартам ISO для ASA/DIN.</span><span class="sxs-lookup"><span data-stu-id="2acec-119">A value that identifies the film speed settings when this image was captured.The settings correspond to the ISO designations of ASA/DIN.</span></span><br/> <span data-ttu-id="2acec-120">Как правило, устройство поддерживает дискретные перечислимые значения, но возможно непрерывное управление диапазоном.</span><span class="sxs-lookup"><span data-stu-id="2acec-120">Typically, a device supports discrete enumerated values, but continuous control over a range is possible.</span></span><br/> <span data-ttu-id="2acec-121">Значение 0xFFFFFFFF соответствует автоматическому параметру ISO.</span><span class="sxs-lookup"><span data-stu-id="2acec-121">A value of 0xFFFFFFFF corresponds to automatic ISO setting.</span></span><br/> |
| <span data-ttu-id="2acec-122">**\_ \_ время экспозиции образа WPD \_**</span><span class="sxs-lookup"><span data-stu-id="2acec-122">**WPD\_IMAGE\_EXPOSURE\_TIME**</span></span>                                                                                                                 | <span data-ttu-id="2acec-123">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="2acec-123">**VT\_UI4**</span></span> | <span data-ttu-id="2acec-124">Определяет скорость затвора устройства при записи этого образа. Единицы находятся в секундах, масштабируемых на 10000.</span><span class="sxs-lookup"><span data-stu-id="2acec-124">Identifies the shutter speed of the device when this image was captured.Units are in seconds scaled by 10000.</span></span><br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="2acec-125">**\_фнумбер образа \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="2acec-125">**WPD\_IMAGE\_FNUMBER**</span></span>                                                                                                                        | <span data-ttu-id="2acec-126">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="2acec-126">**VT\_UI4**</span></span> | <span data-ttu-id="2acec-127">Определяет параметр апертуры линзы при записи этого изображения. Единицы измерения равны f-номеру, масштабированному на 100.</span><span class="sxs-lookup"><span data-stu-id="2acec-127">Identifies the aperture setting of the lens when this image was captured.Units are equal to the f-number scaled by 100.</span></span><br/>                                                                                                                                                                                                              |
| <span data-ttu-id="2acec-128">**\_разрешение изображения WPD \_ по горизонтали \_**</span><span class="sxs-lookup"><span data-stu-id="2acec-128">**WPD\_IMAGE\_HORIZONTAL\_RESOLUTION**</span></span>                                                                                                         | <span data-ttu-id="2acec-129">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="2acec-129">**VT\_R8**</span></span>  | <span data-ttu-id="2acec-130">Указывает разрешение изображения по горизонтали в точках на дюйм (DPI).</span><span class="sxs-lookup"><span data-stu-id="2acec-130">Indicates the horizontal resolution of an image, in dots per inch (DPI) .</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="2acec-131">**\_разрешение изображения WPD \_ по вертикали \_**</span><span class="sxs-lookup"><span data-stu-id="2acec-131">**WPD\_IMAGE\_VERTICAL\_RESOLUTION**</span></span>                                                                                                           | <span data-ttu-id="2acec-132">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="2acec-132">**VT\_R8**</span></span>  | <span data-ttu-id="2acec-133">Обозначает вертикальное разрешение изображения в точках на дюйм (DPI).</span><span class="sxs-lookup"><span data-stu-id="2acec-133">Indicates the vertical resolution of an image, in dots per inch (DPI) .</span></span>                                                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="2acec-134">Требования</span><span class="sxs-lookup"><span data-stu-id="2acec-134">Requirements</span></span>



| <span data-ttu-id="2acec-135">Требование</span><span class="sxs-lookup"><span data-stu-id="2acec-135">Requirement</span></span> | <span data-ttu-id="2acec-136">Значение</span><span class="sxs-lookup"><span data-stu-id="2acec-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2acec-137">Header</span><span class="sxs-lookup"><span data-stu-id="2acec-137">Header</span></span><br/> | <dl> <span data-ttu-id="2acec-138"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="2acec-138"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2acec-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2acec-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2acec-140">**Свойства и атрибуты WPD**</span><span class="sxs-lookup"><span data-stu-id="2acec-140">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




