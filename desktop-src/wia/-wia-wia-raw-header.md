---
description: '\_ \_ Структура заголовков WIA RAW определяет изображение в формате необработанных данных устройства и позволяет приложениям использовать необработанный формат при передаче изображений в Windows (WIA).'
ms.assetid: c7b50816-d596-4c62-a00e-cd8d6e303e42
title: Структура WIA_RAW_HEADER (Виадеф. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_RAW_HEADER
api_type:
- HeaderDef
api_location:
- Wiadef.h
ms.openlocfilehash: 8da33f0b257168712f1b16fb7f940df5db862d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711080"
---
# <a name="wia_raw_header-structure"></a><span data-ttu-id="8d8c3-103">\_Структура заголовка необработанного WIA \_</span><span class="sxs-lookup"><span data-stu-id="8d8c3-103">WIA\_RAW\_HEADER structure</span></span>

<span data-ttu-id="8d8c3-104">Структура **\_ \_ заголовков WIA RAW** определяет изображение в формате необработанных данных устройства и позволяет приложениям использовать необработанный формат при передаче изображений в Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="8d8c3-104">The **WIA\_RAW\_HEADER** structure defines an image in the RAW data format of a device and enables applications to use RAW format in Windows Image Acquisition (WIA) transfers.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d8c3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d8c3-105">Syntax</span></span>


```C++
typedef struct _WIA_RAW_HEADER {
  DWORD Tag;
  DWORD Version;
  DWORD HeaderSize;
  DWORD XRes;
  DWORD YRes;
  DWORD XExtent;
  DWORD YExtent;
  DWORD BytesPerLine;
  DWORD BitsPerPixel;
  DWORD ChannelsPerPixel;
  DWORD DataType;
  BYTE  BitsPerChannel[8];
  DWORD Compression;
  DWORD PhotometricInterp;
  DWORD LineOrder;
  DWORD RawDataOffset;
  DWORD RawDataSize;
  DWORD PaletteOffset;
  DWORD PaletteSize;
} WIA_RAW_HEADER;
```



## <a name="members"></a><span data-ttu-id="8d8c3-106">Члены</span><span class="sxs-lookup"><span data-stu-id="8d8c3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8d8c3-107">**Тег**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-107">**Tag**</span></span>
</dt> <dd>

<span data-ttu-id="8d8c3-108">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8d8c3-109">Имя формата.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-109">The name of the format.</span></span> <span data-ttu-id="8d8c3-110">Это должен быть литерал "ВРАВ" (четыре символа ASCII с одним байтом).</span><span class="sxs-lookup"><span data-stu-id="8d8c3-110">This must be the literal 'WRAW' (four single byte ASCII characters).</span></span>

</dd> <dt>

<span data-ttu-id="8d8c3-111">**Version**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-111">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="8d8c3-112">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-112">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8d8c3-113">Версия необработанного формата.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-113">The version of the RAW format.</span></span> <span data-ttu-id="8d8c3-114">Всегда используйте 0x00010000.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-114">Always use 0x00010000.</span></span>

</dd> <dt>

<span data-ttu-id="8d8c3-115">**хеадерсизе**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-115">**HeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="8d8c3-116">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8d8c3-117">Общее число допустимых байтов в заголовке.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-117">The total valid bytes in the header.</span></span>

</dd> <dt>

<span data-ttu-id="8d8c3-118">**ксрес**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-118">**XRes**</span></span>
</dt> <dd>

<span data-ttu-id="8d8c3-119">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-119">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8d8c3-120">Разрешение по горизонтали в точках на дюйм.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-120">The horizontal resolution in dots per inch.</span></span>

</dd> <dt>

<span data-ttu-id="8d8c3-121">**ирес**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-121">**YRes**</span></span>
</dt> <dd>

<span data-ttu-id="8d8c3-122">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8d8c3-123">Разрешение по вертикали в точках на дюйм.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-123">The vertical resolution in dots per inch.</span></span>

</dd> <dt>

<span data-ttu-id="8d8c3-124">**ксекстент**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-124">**XExtent**</span></span>
</dt> <dd>

<span data-ttu-id="8d8c3-125">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-125">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8d8c3-126">Ширина изображения в пикселях.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-126">The width of the image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="8d8c3-127">**екстент**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-127">**YExtent**</span></span>
</dt> <dd>

<span data-ttu-id="8d8c3-128">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-128">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8d8c3-129">Высота изображения в пикселях.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-129">The height of the image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="8d8c3-130">**битесперлине**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-130">**BytesPerLine**</span></span>
</dt> <dd>

<span data-ttu-id="8d8c3-131">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-131">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8d8c3-132">Число байтов в строке несжатого изображения.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-132">The number of bytes in a line of an uncompressed image.</span></span> <span data-ttu-id="8d8c3-133">При сжатии данных используйте значение 0, чтобы сообщить о том, что число байтов в строке неизвестно.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-133">Use 0 when the data is compressed to signal that the number of bytes per line is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="8d8c3-134">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-134">**BitsPerPixel**</span></span>
</dt> <dd>

<span data-ttu-id="8d8c3-135">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-135">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8d8c3-136">Общее число бит на пиксель для всех каналов пикселя.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-136">The total number of bits per pixel for all the pixel's channels.</span></span>

</dd> <dt>

<span data-ttu-id="8d8c3-137">**чаннелсперпиксел**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-137">**ChannelsPerPixel**</span></span>
</dt> <dd>

<span data-ttu-id="8d8c3-138">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-138">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8d8c3-139">Число цветовых каналов в пикселе.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-139">The number of color channels in a pixel.</span></span>

</dd> <dt>

<span data-ttu-id="8d8c3-140">**DataType**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-140">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="8d8c3-141">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-141">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8d8c3-142">\_ \_ Тип данных WIA IPA изображения.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-142">The WIA\_IPA\_DATATYPE of the image.</span></span> <span data-ttu-id="8d8c3-143">Так как \_ Формат WIA IPA \_ имеет значение виаимгфмт \_ RAW, это список допустимых значений, из которых приложение выбирается.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-143">Since WIA\_IPA\_FORMAT is set to WiaImgFmt\_RAW, this is a list of allowed values from which the application picks.</span></span>

</dd> <dt>

<span data-ttu-id="8d8c3-144">**Битсперчаннел \[ 8\]**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-144">**BitsPerChannel\[8\]**</span></span>
</dt> <dd>

<span data-ttu-id="8d8c3-145">Тип: **Byte**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-145">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="8d8c3-146">Количество битов в канале, не более 8.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-146">The number of bits in a channel, up to a maximum of 8.</span></span>

</dd> <dt>

<span data-ttu-id="8d8c3-147">**Сжатие**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-147">**Compression**</span></span>
</dt> <dd>

<span data-ttu-id="8d8c3-148">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-148">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8d8c3-149">\_ \_ Значение сжатия WIA IPA, указывающее тип используемого сжатия, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-149">A WIA\_IPA\_COMPRESSION value specifying the type of compression used, if any.</span></span>

</dd> <dt>

<span data-ttu-id="8d8c3-150">**фотометриЦинтерп**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-150">**PhotometricInterp**</span></span>
</dt> <dd>

<span data-ttu-id="8d8c3-151">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-151">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8d8c3-152">Значение WIA \_ IPA \_ интерп, \_ определяющее интерпретацию изображения в виде фотометрики.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-152">A WIA\_IPA\_PHOTOMETRIC\_INTERP value specifying the photometric interpretation of the image.</span></span>

</dd> <dt>

<span data-ttu-id="8d8c3-153">**линеордер**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-153">**LineOrder**</span></span>
</dt> <dd>

<span data-ttu-id="8d8c3-154">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-154">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8d8c3-155">Значение, представляющее порядок линий изображения.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-155">A value representing the image line order.</span></span> <span data-ttu-id="8d8c3-156">Это всегда можно сделать \_ с помощью строки WIA \_ \_ сверху \_ \_ вниз или в \_ порядке строк WIA сверху \_ \_ вниз \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8d8c3-156">This is always either WIA\_LINE\_ORDER\_TOP\_TO\_BOTTOM or WIA\_LINE\_ORDER\_BOTTOM\_TO\_TOP.</span></span>

</dd> <dt>

<span data-ttu-id="8d8c3-157">**равдатаоффсет**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-157">**RawDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="8d8c3-158">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-158">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8d8c3-159">Расположение данных необработанного изображения в байтах, начиная с места, где заканчивается заголовок, или от положения, в котором заканчивается палитра.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-159">The position of the raw image data in bytes, starting from position where the header ends or the position where the palette ends.</span></span>

</dd> <dt>

<span data-ttu-id="8d8c3-160">**равдатасизе**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-160">**RawDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="8d8c3-161">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-161">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8d8c3-162">Размер необработанных данных изображения в байтах.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-162">The size, in bytes, of the raw image data.</span></span>

</dd> <dt>

<span data-ttu-id="8d8c3-163">**палеттеоффсет**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-163">**PaletteOffset**</span></span>
</dt> <dd>

<span data-ttu-id="8d8c3-164">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-164">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8d8c3-165">Расположение палитры в байтах, начиная с места, где заканчивается заголовок, или от места окончания данных.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-165">The position of the palette in bytes, starting from the position where the header ends or the position where the data ends.</span></span> <span data-ttu-id="8d8c3-166">(Это значение равно 0, если палитра отсутствует.)</span><span class="sxs-lookup"><span data-stu-id="8d8c3-166">(This value is 0, if there is no palette.)</span></span>

</dd> <dt>

<span data-ttu-id="8d8c3-167">**палеттесизе**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-167">**PaletteSize**</span></span>
</dt> <dd>

<span data-ttu-id="8d8c3-168">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8d8c3-168">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8d8c3-169">Размер (в байтах) таблицы палитры.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-169">The size, in bytes, of the palette table.</span></span> <span data-ttu-id="8d8c3-170">(Это значение равно 0, если палитра отсутствует.)</span><span class="sxs-lookup"><span data-stu-id="8d8c3-170">(This is 0, if there is no palette.)</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d8c3-171">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d8c3-171">Remarks</span></span>

<span data-ttu-id="8d8c3-172">Так как это не формат файла, используйте пустую строку для \_ \_ Свойства расширения файла WIA IPA \_ .</span><span class="sxs-lookup"><span data-stu-id="8d8c3-172">Because this is not a file format, use an empty string for the WIA\_IPA\_FILE\_EXTENSION property.</span></span>

<span data-ttu-id="8d8c3-173">Палитра и данные могут находиться в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-173">The palette and the data can come in either order.</span></span>

<span data-ttu-id="8d8c3-174">**Равдатасизе** не содержит ни заголовок, ни палитру.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-174">**RawDataSize** does not include either the header or the palette.</span></span> <span data-ttu-id="8d8c3-175">Используйте это поле для проверки успешности перемещения образа.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-175">Use this field to verify that the transfer of the image has been successful.</span></span>

<span data-ttu-id="8d8c3-176">**Палеттесизе** — байт, а не число записей в палитре.</span><span class="sxs-lookup"><span data-stu-id="8d8c3-176">**PaletteSize** is bytes, not the number of entries in the palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d8c3-177">Требования</span><span class="sxs-lookup"><span data-stu-id="8d8c3-177">Requirements</span></span>



| <span data-ttu-id="8d8c3-178">Требование</span><span class="sxs-lookup"><span data-stu-id="8d8c3-178">Requirement</span></span> | <span data-ttu-id="8d8c3-179">Значение</span><span class="sxs-lookup"><span data-stu-id="8d8c3-179">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8d8c3-180">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d8c3-180">Minimum supported client</span></span><br/> | <span data-ttu-id="8d8c3-181">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8d8c3-181">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8d8c3-182">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d8c3-182">Minimum supported server</span></span><br/> | <span data-ttu-id="8d8c3-183">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8d8c3-183">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8d8c3-184">Header</span><span class="sxs-lookup"><span data-stu-id="8d8c3-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d8c3-185"><dt>Виадеф. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d8c3-185"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




