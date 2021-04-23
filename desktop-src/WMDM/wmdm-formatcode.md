---
title: Перечисление WMDM_FORMATCODE
description: '\_Тип ПЕРЕЧИСЛЕНИЯ вмдм форматкоде определяет список кодов форматов, описывающих типы содержимого, передаваемые на устройство и с устройства.'
ms.assetid: 203d9bdf-cbbd-4d06-8292-26c8a472e2aa
keywords:
- WMDM_FORMATCODE перечисление Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMDM_FORMATCODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04db31578f36455fdf77bb4044ad45e5ca9f9a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694438"
---
# <a name="wmdm_formatcode-enumeration"></a><span data-ttu-id="6265c-104">\_Перечисление ФОРМАТКОДЕ вмдм</span><span class="sxs-lookup"><span data-stu-id="6265c-104">WMDM\_FORMATCODE enumeration</span></span>

<span data-ttu-id="6265c-105">Тип перечисления **вмдм \_ форматкоде** определяет список кодов форматов, описывающих типы содержимого, передаваемые на устройство и с устройства.</span><span class="sxs-lookup"><span data-stu-id="6265c-105">The **WMDM\_FORMATCODE** enumeration type defines a list of format codes that describe types of content transferred to and from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6265c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6265c-106">Syntax</span></span>


```C++
typedef enum tagWMDM_FORMATCODE { 
  WMDM_FORMATCODE_NOTUSED,
  WMDM_FORMATCODE_ALLIMAGES,
  WMDM_FORMATCODE_UNDEFINED,
  WMDM_FORMATCODE_ASSOCIATION,
  WMDM_FORMATCODE_SCRIPT,
  WMDM_FORMATCODE_EXECUTABLE,
  WMDM_FORMATCODE_TEXT,
  WMDM_FORMATCODE_HTML,
  WMDM_FORMATCODE_DPOF,
  WMDM_FORMATCODE_AIFF,
  WMDM_FORMATCODE_WAVE,
  WMDM_FORMATCODE_MP3,
  WMDM_FORMATCODE_AVI,
  WMDM_FORMATCODE_MPEG,
  WMDM_FORMATCODE_ASF,
  WMDM_FORMATCODE_RESERVED_FIRST,
  WMDM_FORMATCODE_RESERVED_LAST,
  WMDM_FORMATCODE_IMAGE_UNDEFINED,
  WMDM_FORMATCODE_IMAGE_EXIF,
  WMDM_FORMATCODE_IMAGE_TIFFEP,
  WMDM_FORMATCODE_IMAGE_FLASHPIX,
  WMDM_FORMATCODE_IMAGE_BMP,
  WMDM_FORMATCODE_IMAGE_CIFF,
  WMDM_FORMATCODE_IMAGE_GIF,
  WMDM_FORMATCODE_IMAGE_JFIF,
  WMDM_FORMATCODE_IMAGE_PCD,
  WMDM_FORMATCODE_IMAGE_PICT,
  WMDM_FORMATCODE_IMAGE_PNG,
  WMDM_FORMATCODE_IMAGE_TIFF,
  WMDM_FORMATCODE_IMAGE_TIFFIT,
  WMDM_FORMATCODE_IMAGE_JP2,
  WMDM_FORMATCODE_IMAGE_JPX,
  WMDM_FORMATCODE_IMAGE_RESERVED_FIRST,
  WMDM_FORMATCODE_IMAGE_RESERVED_LAST,
  WMDM_FORMATCODE_UNDEFINEDFIRMWARE,
          WMDM_FORMATCODE_WBMP
,
                  WMDM_FORMATCODE_JPEGXR
,
  WMDM_FORMATCODE_WINDOWSIMAGEFORMAT,
  WMDM_FORMATCODE_UNDEFINEDAUDIO,
  WMDM_FORMATCODE_WMA,
  WMDM_FORMATCODE_OGG,
  WMDM_FORMATCODE_AAC,
  WMDM_FORMATCODE_AUDIBLE,
  WMDM_FORMATCODE_FLAC,
          WMDM_FORMATCODE_QCELP
,
          WMDM_FORMATCODE_AMR
,
  WMDM_FORMATCODE_UNDEFINEDVIDEO,
  WMDM_FORMATCODE_WMV,
  WMDM_FORMATCODE_MP4,
  WMDM_FORMATCODE_MP2,
          WMDM_FORMATCODE_3G2
,
                  WMDM_FORMATCODE_AVCHD
,
                  WMDM_FORMATCODE_ATSCTS
,
                          WMDM_FORMATCODE_DVBTS
,
  WMDM_FORMATCODE_UNDEFINEDCOLLECTION,
  WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM,
  WMDM_FORMATCODE_ABSTRACTIMAGEALBUM,
  WMDM_FORMATCODE_ABSTRACTAUDIOALBUM,
  WMDM_FORMATCODE_ABSTRACTVIDEOALBUM,
  WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST,
  WMDM_FORMATCODE_ABSTRACTCONTACTGROUP,
  WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER,
  WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION,
  WMDM_FORMATCODE_WPLPLAYLIST,
  WMDM_FORMATCODE_M3UPLAYLIST,
  WMDM_FORMATCODE_MPLPLAYLIST,
  WMDM_FORMATCODE_ASXPLAYLIST,
  WMDM_FORMATCODE_PLSPLAYLIST,
  WMDM_FORMATCODE_UNDEFINEDDOCUMENT,
  WMDM_FORMATCODE_ABSTRACTDOCUMENT,
  WMDM_FORMATCODE_XMLDOCUMENT,
  WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT,
  WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT,
  WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET,
  WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT,
  WMDM_FORMATCODE_UNDEFINEDMESSAGE,
  WMDM_FORMATCODE_ABSTRACTMESSAGE,
  WMDM_FORMATCODE_UNDEFINEDCONTACT,
  WMDM_FORMATCODE_ABSTRACTCONTACT,
  WMDM_FORMATCODE_VCARD2,
  WMDM_FORMATCODE_VCARD3,
  WMDM_FORMATCODE_UNDEFINEDCALENDARITEM,
  WMDM_FORMATCODE_ABSTRACTCALENDARITEM,
  WMDM_FORMATCODE_VCALENDAR1,
  WMDM_FORMATCODE_VCALENDAR2,
  WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE,
  WMDM_FORMATCODE_MEDIA_CAST,
  WMDM_FORMATCODE_SECTION,
                                  WMDM_FORMATCODE_3G2A

} WMDM_FORMATCODE;
```



## <a name="constants"></a><span data-ttu-id="6265c-107">Константы</span><span class="sxs-lookup"><span data-stu-id="6265c-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6265c-108"><span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**ВМДМ \_ форматкоде \_ нотусед**</span><span class="sxs-lookup"><span data-stu-id="6265c-108"><span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**WMDM\_FORMATCODE\_NOTUSED**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-109">Код формата не используется.</span><span class="sxs-lookup"><span data-stu-id="6265c-109">No format code is used.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-110"><span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**ВМДМ \_ форматкоде \_ аллимажес**</span><span class="sxs-lookup"><span data-stu-id="6265c-110"><span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**WMDM\_FORMATCODE\_ALLIMAGES**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-111">Код формата, который может использоваться для запроса всех изображений.</span><span class="sxs-lookup"><span data-stu-id="6265c-111">Format code that can be used to query for all images.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-112"><span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**ВМДМ \_ форматкоде не \_ определен**</span><span class="sxs-lookup"><span data-stu-id="6265c-112"><span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**WMDM\_FORMATCODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-113">Код формата, используемый для запроса всех неопределенных объектов.</span><span class="sxs-lookup"><span data-stu-id="6265c-113">Format code used to query for all undefined objects.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-114"><span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**\_сопоставление вмдм форматкоде \_**</span><span class="sxs-lookup"><span data-stu-id="6265c-114"><span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**WMDM\_FORMATCODE\_ASSOCIATION**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-115">Код формата, используемый для определения связи между двумя объектами.</span><span class="sxs-lookup"><span data-stu-id="6265c-115">Format code used to define a link between two objects.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-116"><span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**ВМДМ \_ форматкоде \_ сценарий**</span><span class="sxs-lookup"><span data-stu-id="6265c-116"><span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**WMDM\_FORMATCODE\_SCRIPT**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-117">Код формата для файла скрипта.</span><span class="sxs-lookup"><span data-stu-id="6265c-117">Format code for a script file.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-118"><span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**\_ \_ исполняемый файл форматкоде вмдм**</span><span class="sxs-lookup"><span data-stu-id="6265c-118"><span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**WMDM\_FORMATCODE\_EXECUTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-119">Код формата для исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="6265c-119">Format code for an executable file.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-120"><span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**ВМДМ \_ форматкоде \_ текст**</span><span class="sxs-lookup"><span data-stu-id="6265c-120"><span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**WMDM\_FORMATCODE\_TEXT**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-121">Форматирование кода для текстового файла.</span><span class="sxs-lookup"><span data-stu-id="6265c-121">Format code for a text file.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-122"><span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**ВМДМ \_ форматкоде \_ HTML**</span><span class="sxs-lookup"><span data-stu-id="6265c-122"><span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**WMDM\_FORMATCODE\_HTML**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-123">Код формата для HTML-файла.</span><span class="sxs-lookup"><span data-stu-id="6265c-123">Format code for an HTML file.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-124"><span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**ВМДМ \_ форматкоде \_ дпоф**</span><span class="sxs-lookup"><span data-stu-id="6265c-124"><span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**WMDM\_FORMATCODE\_DPOF**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-125">Код формата, используемый для представления формата цифрового порядка печати.</span><span class="sxs-lookup"><span data-stu-id="6265c-125">Format code used to represent the digital print order format.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-126"><span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**ВМДМ \_ форматкоде \_**</span><span class="sxs-lookup"><span data-stu-id="6265c-126"><span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**WMDM\_FORMATCODE\_AIFF**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-127">Код формата, используемый для представления формата файла обмена аудио.</span><span class="sxs-lookup"><span data-stu-id="6265c-127">Format code used to represent the audio interchange file format.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-128"><span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**\_волна вмдм форматкоде \_**</span><span class="sxs-lookup"><span data-stu-id="6265c-128"><span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**WMDM\_FORMATCODE\_WAVE**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-129">Формат кода, используемый для WAV-файла.</span><span class="sxs-lookup"><span data-stu-id="6265c-129">Format code used for a WAV file.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-130"><span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**ВМДМ \_ форматкоде \_ MP3**</span><span class="sxs-lookup"><span data-stu-id="6265c-130"><span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**WMDM\_FORMATCODE\_MP3**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-131">Формат кода, используемый для MP3-файла.</span><span class="sxs-lookup"><span data-stu-id="6265c-131">Format code used for an MP3 file.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-132"><span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**ВМДМ \_ форматкоде \_ AVI**</span><span class="sxs-lookup"><span data-stu-id="6265c-132"><span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**WMDM\_FORMATCODE\_AVI**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-133">Код формата, используемый для файла AVI.</span><span class="sxs-lookup"><span data-stu-id="6265c-133">Format code used for an AVI file.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-134"><span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**ВМДМ \_ форматкоде \_ MPEG**</span><span class="sxs-lookup"><span data-stu-id="6265c-134"><span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**WMDM\_FORMATCODE\_MPEG**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-135">Код формата, используемый для файла MPEG.</span><span class="sxs-lookup"><span data-stu-id="6265c-135">Format code used for an MPEG file.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-136"><span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**ВМДМ \_ форматкоде \_ ASF**</span><span class="sxs-lookup"><span data-stu-id="6265c-136"><span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**WMDM\_FORMATCODE\_ASF**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-137">Код формата, используемый для представления файла расширенных систем формата (ASF).</span><span class="sxs-lookup"><span data-stu-id="6265c-137">Format code used to represent an Advanced Systems Format (ASF) file.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-138"><span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**ВМДМ \_ форматкоде \_ сначала зарезервировано \_**</span><span class="sxs-lookup"><span data-stu-id="6265c-138"><span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**WMDM\_FORMATCODE\_RESERVED\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-139">Код формата, который является первым в диапазоне, зарезервированном для протокола обмена изображениями (PTP).</span><span class="sxs-lookup"><span data-stu-id="6265c-139">Format code that is the first in a range reserved for Picture Transfer Protocol (PTP).</span></span>

</dd> <dt>

<span data-ttu-id="6265c-140"><span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**ВМДМ \_ форматкоде \_ зарезервированный \_ последний**</span><span class="sxs-lookup"><span data-stu-id="6265c-140"><span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**WMDM\_FORMATCODE\_RESERVED\_LAST**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-141">Код формата, который последним в диапазоне, зарезервированном для PTP.</span><span class="sxs-lookup"><span data-stu-id="6265c-141">Format code that is last in a range reserved for PTP.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-142"><span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**\_изображение вмдм форматкоде не \_ \_ определено**</span><span class="sxs-lookup"><span data-stu-id="6265c-142"><span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**WMDM\_FORMATCODE\_IMAGE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-143">Код формата, используемый для представления и изображения неопределенного типа.</span><span class="sxs-lookup"><span data-stu-id="6265c-143">Format code used to represent and image of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-144"><span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**ВМДМ \_ форматкоде \_ image \_ EXIF**</span><span class="sxs-lookup"><span data-stu-id="6265c-144"><span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**WMDM\_FORMATCODE\_IMAGE\_EXIF**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-145">Код формата для файла EXIF.</span><span class="sxs-lookup"><span data-stu-id="6265c-145">Format code for an EXIF file.</span></span> <span data-ttu-id="6265c-146">Также используется для изображений JPEG, не охваченных ВМДМ \_ форматкоде \_ image \_ JP2 или вмдм \_ форматкоде \_ image \_ жпкс.</span><span class="sxs-lookup"><span data-stu-id="6265c-146">Also used for JPEG images not covered by WMDM\_FORMATCODE\_IMAGE\_JP2 or WMDM\_FORMATCODE\_IMAGE\_JPX.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-147"><span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**ВМДМ \_ форматкоде \_ image \_ тиффеп**</span><span class="sxs-lookup"><span data-stu-id="6265c-147"><span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFFEP**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-148">Код формата, используемый для изображений, имеющих формат файла изображения с тегами для электронной фотографии (TIFF/EP)</span><span class="sxs-lookup"><span data-stu-id="6265c-148">Format code used for images that are of type Tagged Image File Format for Electronic Photography (TIFF/EP)</span></span>

</dd> <dt>

<span data-ttu-id="6265c-149"><span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**ВМДМ \_ форматкоде \_ image \_ флашпикс**</span><span class="sxs-lookup"><span data-stu-id="6265c-149"><span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**WMDM\_FORMATCODE\_IMAGE\_FLASHPIX**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-150">Код формата для файла типа ФПКС.</span><span class="sxs-lookup"><span data-stu-id="6265c-150">Format code for a file of type FPX.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-151"><span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**ВМДМ \_ форматкоде \_ image \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="6265c-151"><span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**WMDM\_FORMATCODE\_IMAGE\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-152">Код формата для файла типа BMP.</span><span class="sxs-lookup"><span data-stu-id="6265c-152">Format code for a file of type BMP.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-153"><span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**ВМДМ \_ форматкоде \_ image \_ Цифф**</span><span class="sxs-lookup"><span data-stu-id="6265c-153"><span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**WMDM\_FORMATCODE\_IMAGE\_CIFF**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-154">Формат кода для изображения в формате файла изображения камеры.</span><span class="sxs-lookup"><span data-stu-id="6265c-154">Format code for an image in the camera image file format.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-155"><span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**ВМДМ \_ форматкоде \_ изображение \_ GIF**</span><span class="sxs-lookup"><span data-stu-id="6265c-155"><span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**WMDM\_FORMATCODE\_IMAGE\_GIF**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-156">Форматирование кода для GIF-файла.</span><span class="sxs-lookup"><span data-stu-id="6265c-156">Format code for a GIF file.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-157"><span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**ВМДМ \_ форматкоде \_ image \_ JFIF**</span><span class="sxs-lookup"><span data-stu-id="6265c-157"><span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**WMDM\_FORMATCODE\_IMAGE\_JFIF**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-158">Код формата для файла типа JFIF.</span><span class="sxs-lookup"><span data-stu-id="6265c-158">Format code for a file of type JFIF.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-159"><span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**ВМДМ \_ форматкоде \_ image \_ ПКД**</span><span class="sxs-lookup"><span data-stu-id="6265c-159"><span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**WMDM\_FORMATCODE\_IMAGE\_PCD**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-160">Код формата для изображения типа "Фото CD".</span><span class="sxs-lookup"><span data-stu-id="6265c-160">Format code for an image of type photo cd.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-161"><span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**ВМДМ \_ форматкоде \_ изображение \_ PICT**</span><span class="sxs-lookup"><span data-stu-id="6265c-161"><span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**WMDM\_FORMATCODE\_IMAGE\_PICT**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-162">Код формата для изображения типа PICT.</span><span class="sxs-lookup"><span data-stu-id="6265c-162">Format code for an image of type PICT.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-163"><span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**ВМДМ \_ форматкоде \_ image \_ PNG**</span><span class="sxs-lookup"><span data-stu-id="6265c-163"><span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**WMDM\_FORMATCODE\_IMAGE\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-164">Код формата для изображения типа PNG.</span><span class="sxs-lookup"><span data-stu-id="6265c-164">Format code for an image of type PNG.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-165"><span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**ВМДМ \_ форматкоде \_ image \_ TIFF**</span><span class="sxs-lookup"><span data-stu-id="6265c-165"><span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-166">Код формата для файла типа TIFF.</span><span class="sxs-lookup"><span data-stu-id="6265c-166">Format code for a file of type TIFF.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-167"><span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**ВМДМ \_ форматкоде \_ image \_ тиффит**</span><span class="sxs-lookup"><span data-stu-id="6265c-167"><span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFFIT**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-168">Код формата для изображения типа Tagged Image File Format с помощью технологии Image.</span><span class="sxs-lookup"><span data-stu-id="6265c-168">Format code for an image of type Tagged Image File Format with image technology.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-169"><span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**ВМДМ \_ форматкоде \_ image \_ JP2**</span><span class="sxs-lookup"><span data-stu-id="6265c-169"><span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**WMDM\_FORMATCODE\_IMAGE\_JP2**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-170">Код формата для изображения jpeg200.</span><span class="sxs-lookup"><span data-stu-id="6265c-170">Format code for a jpeg200 image.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-171"><span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**ВМДМ \_ форматкоде \_ image \_ жпкс**</span><span class="sxs-lookup"><span data-stu-id="6265c-171"><span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**WMDM\_FORMATCODE\_IMAGE\_JPX**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-172">Код формата для образа, созданного на основе JPEG200, с использованием расширенной регистрации изображений.</span><span class="sxs-lookup"><span data-stu-id="6265c-172">Format code for an image built on JPEG200, using extended still image registration.</span></span> <span data-ttu-id="6265c-173">Обычно используется расширение имени файла. жпф или. жпкс.</span><span class="sxs-lookup"><span data-stu-id="6265c-173">The file name extension is usually .jpf or .jpx.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-174"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**\_ \_ \_ предварительно зарезервированный образ вмдм форматкоде \_**</span><span class="sxs-lookup"><span data-stu-id="6265c-174"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**WMDM\_FORMATCODE\_IMAGE\_RESERVED\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-175">Код формата, который является первым в диапазоне, зарезервированном для ссылки на изображение в PTP.</span><span class="sxs-lookup"><span data-stu-id="6265c-175">Format code that is the first in a range reserved for an image reference in PTP.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-176"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**снимок ВМДМ \_ форматкоде, \_ \_ зарезервированный \_ последним**</span><span class="sxs-lookup"><span data-stu-id="6265c-176"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**WMDM\_FORMATCODE\_IMAGE\_RESERVED\_LAST**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-177">Форматирование кода, который является последним в диапазоне, зарезервированном для ссылки на изображение в PTP.</span><span class="sxs-lookup"><span data-stu-id="6265c-177">Format code that is the last in a range reserved for an image reference in PTP.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-178"><span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**ВМДМ \_ форматкоде \_ ундефинедфирмваре**</span><span class="sxs-lookup"><span data-stu-id="6265c-178"><span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**WMDM\_FORMATCODE\_UNDEFINEDFIRMWARE**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-179">Форматировать код, если встроенное по не определено.</span><span class="sxs-lookup"><span data-stu-id="6265c-179">Format code when firmware is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-180"><span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span>**Вмдм \_ ФОРМАТКОДЕ \_ WBMP**</span><span class="sxs-lookup"><span data-stu-id="6265c-180"><span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span> **WMDM\_FORMATCODE\_WBMP**</span></span> 
</dt> <dd>

<span data-ttu-id="6265c-181">Код формата для точечного рисунка протокола приложения беспроводной связи (. WBMP).</span><span class="sxs-lookup"><span data-stu-id="6265c-181">Format code for a Wireless Application Protocol Bitmap (.wbmp) image.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-182"><span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span>**Вмдм \_ ФОРМАТКОДЕ \_ жпегкср**</span><span class="sxs-lookup"><span data-stu-id="6265c-182"><span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span> **WMDM\_FORMATCODE\_JPEGXR**</span></span> 
</dt> <dd>

<span data-ttu-id="6265c-183">Формат кода для изображения фотографии HD</span><span class="sxs-lookup"><span data-stu-id="6265c-183">Format code for an HD Photo image</span></span>

</dd> <dt>

<span data-ttu-id="6265c-184"><span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**ВМДМ \_ форматкоде \_ виндовсимажеформат**</span><span class="sxs-lookup"><span data-stu-id="6265c-184"><span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**WMDM\_FORMATCODE\_WINDOWSIMAGEFORMAT**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-185">Код формата для формата образа Windows.</span><span class="sxs-lookup"><span data-stu-id="6265c-185">Format code for Windows image format.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-186"><span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**ВМДМ \_ форматкоде \_ ундефинедаудио**</span><span class="sxs-lookup"><span data-stu-id="6265c-186"><span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**WMDM\_FORMATCODE\_UNDEFINEDAUDIO**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-187">Код формата для звукового файла неопределенного типа.</span><span class="sxs-lookup"><span data-stu-id="6265c-187">Format code for an audio file of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-188"><span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**ВМДМ \_ форматкоде \_ WMA**</span><span class="sxs-lookup"><span data-stu-id="6265c-188"><span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**WMDM\_FORMATCODE\_WMA**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-189">Код формата для WMA-файла Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="6265c-189">Format code for a Windows Media Audio (WMA) file.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-190"><span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**ВМДМ \_ форматкоде \_ OGG**</span><span class="sxs-lookup"><span data-stu-id="6265c-190"><span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**WMDM\_FORMATCODE\_OGG**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-191">Код формата для звукового файла с Vorbis кодировкой в контейнере OGG.</span><span class="sxs-lookup"><span data-stu-id="6265c-191">Format code for a Vorbis-encoded audio file in an Ogg container.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-192"><span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**ВМДМ \_ форматкоде \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="6265c-192"><span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**WMDM\_FORMATCODE\_AAC**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-193">Код формата для расширенного файла аудио-кодирования (AAC).</span><span class="sxs-lookup"><span data-stu-id="6265c-193">Format code for an Advanced Audio Coding (AAC) file.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-194"><span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**ВМДМ \_ форматкоде \_**</span><span class="sxs-lookup"><span data-stu-id="6265c-194"><span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**WMDM\_FORMATCODE\_AUDIBLE**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-195">Код формата для звукового файла.</span><span class="sxs-lookup"><span data-stu-id="6265c-195">Format code for an Audible file.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-196"><span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**ВМДМ \_ форматкоде \_ FLAC**</span><span class="sxs-lookup"><span data-stu-id="6265c-196"><span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**WMDM\_FORMATCODE\_FLAC**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-197">Код формата для бесплатного файла аудиокодека без потерь (FLAC).</span><span class="sxs-lookup"><span data-stu-id="6265c-197">Format code for a Free Lossless Audio Codec (FLAC) file.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-198"><span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span>**Вмдм \_ ФОРМАТКОДЕ \_ кцелп**</span><span class="sxs-lookup"><span data-stu-id="6265c-198"><span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span> **WMDM\_FORMATCODE\_QCELP**</span></span> 
</dt> <dd>

<span data-ttu-id="6265c-199">Код формата для файлового кодека линейного прогноза Qualcomm (КЦЕЛП).</span><span class="sxs-lookup"><span data-stu-id="6265c-199">Format code for a Qualcomm Code Excited Linear Prediction (QCELP) codec file.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-200"><span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span>**Вмдм \_ ФОРМАТКОДЕ \_ AMR**</span><span class="sxs-lookup"><span data-stu-id="6265c-200"><span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span> **WMDM\_FORMATCODE\_AMR**</span></span> 
</dt> <dd>

<span data-ttu-id="6265c-201">Код формата для файла кодека адаптивной многочастотной аудиоподсистемы (AMR).</span><span class="sxs-lookup"><span data-stu-id="6265c-201">Format code for an Adaptive Multi-Rate audio (AMR) codec file.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-202"><span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**ВМДМ \_ форматкоде \_ ундефинедвидео**</span><span class="sxs-lookup"><span data-stu-id="6265c-202"><span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**WMDM\_FORMATCODE\_UNDEFINEDVIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-203">Формат кода для видеофайла с неопределенным типом.</span><span class="sxs-lookup"><span data-stu-id="6265c-203">Format code for a video file with an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-204"><span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**ВМДМ \_ форматкоде \_ WMV**</span><span class="sxs-lookup"><span data-stu-id="6265c-204"><span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**WMDM\_FORMATCODE\_WMV**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-205">Код формата для файла видео Windows Media (WMV).</span><span class="sxs-lookup"><span data-stu-id="6265c-205">Format code for a Windows Media Video (WMV) file.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-206"><span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**ВМДМ \_ форматкоде \_ MP4**</span><span class="sxs-lookup"><span data-stu-id="6265c-206"><span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**WMDM\_FORMATCODE\_MP4**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-207">Код формата для файла MP4.</span><span class="sxs-lookup"><span data-stu-id="6265c-207">Format code for an MP4 file.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-208"><span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**ВМДМ \_ форматкоде \_ MP2**</span><span class="sxs-lookup"><span data-stu-id="6265c-208"><span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**WMDM\_FORMATCODE\_MP2**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-209">Код формата для файла MP2.</span><span class="sxs-lookup"><span data-stu-id="6265c-209">Format code for an MP2 file.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-210"><span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span>**Вмдм \_ ФОРМАТКОДЕ \_ 3G2**</span><span class="sxs-lookup"><span data-stu-id="6265c-210"><span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span> **WMDM\_FORMATCODE\_3G2**</span></span> 
</dt> <dd>

<span data-ttu-id="6265c-211">Код формата для формата контейнера мультимедиа 3G2 (3GPP2).</span><span class="sxs-lookup"><span data-stu-id="6265c-211">Format code for a 3G2 (3GPP2) multimedia container format.</span></span> <span data-ttu-id="6265c-212">Файл этого типа может содержать аудио, видео или текст.</span><span class="sxs-lookup"><span data-stu-id="6265c-212">A file of this type may contain audio, video, or text.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-213"><span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span>**Вмдм \_ ФОРМАТКОДЕ \_ авчд**</span><span class="sxs-lookup"><span data-stu-id="6265c-213"><span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span> **WMDM\_FORMATCODE\_AVCHD**</span></span> 
</dt> <dd>

<span data-ttu-id="6265c-214">Код формата для видео-файла АВЧД (расширенного кодирования видео с высоким определением).</span><span class="sxs-lookup"><span data-stu-id="6265c-214">Format code for an AVCHD (Advanced Video Coding High Definition) video file.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-215"><span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span>**Вмдм \_ ФОРМАТКОДЕ \_ атсктс**</span><span class="sxs-lookup"><span data-stu-id="6265c-215"><span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span> **WMDM\_FORMATCODE\_ATSCTS**</span></span> 
</dt> <dd>

<span data-ttu-id="6265c-216">Код формата для стандарта расширенного формата комитетов телевизионных систем (АТСКТС).</span><span class="sxs-lookup"><span data-stu-id="6265c-216">Format code for the Advanced Television Systems Committee (ATSCTS) format standard.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-217"><span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span>**Вмдм \_ ФОРМАТКОДЕ \_ двбтс**</span><span class="sxs-lookup"><span data-stu-id="6265c-217"><span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span> **WMDM\_FORMATCODE\_DVBTS**</span></span> 
</dt> <dd>

<span data-ttu-id="6265c-218">Код формата для видео MPEG-2 и 2-1 уровня II или AC-3, аудио в соответствующем стандарте канале транспорта MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="6265c-218">Format code for an MPEG-2 video and MPEG-1 Layer II, or AC-3, audio within a DVB-compliant MPEG-2 Transport Stream.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-219"><span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**ВМДМ \_ форматкоде \_ ундефинедколлектион**</span><span class="sxs-lookup"><span data-stu-id="6265c-219"><span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**WMDM\_FORMATCODE\_UNDEFINEDCOLLECTION**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-220">Код формата для коллекции неопределенного типа.</span><span class="sxs-lookup"><span data-stu-id="6265c-220">Format code for a collection of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-221"><span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**ВМДМ \_ форматкоде \_ абстрактмултимедиаалбум**</span><span class="sxs-lookup"><span data-stu-id="6265c-221"><span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTMULTIMEDIAALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-222">Код формата для мультимедийного альбома, где объект содержит свойства мультимедийного альбома и, при необходимости, данные.</span><span class="sxs-lookup"><span data-stu-id="6265c-222">Format code for a multimedia album where the object contains the properties of a multimedia album and, optionally, data.</span></span> <span data-ttu-id="6265c-223">Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.</span><span class="sxs-lookup"><span data-stu-id="6265c-223">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-224"><span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**ВМДМ \_ форматкоде \_ абстрактимажеалбум**</span><span class="sxs-lookup"><span data-stu-id="6265c-224"><span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**WMDM\_FORMATCODE\_ABSTRACTIMAGEALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-225">Код формата для альбома образа, в котором объект содержит свойства альбома изображения и, при необходимости, данные.</span><span class="sxs-lookup"><span data-stu-id="6265c-225">Format code for an image album where the object contains the properties of an image album and, optionally, data.</span></span> <span data-ttu-id="6265c-226">Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.</span><span class="sxs-lookup"><span data-stu-id="6265c-226">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-227"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**ВМДМ \_ форматкоде \_ абстрактаудиоалбум**</span><span class="sxs-lookup"><span data-stu-id="6265c-227"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTAUDIOALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-228">Код формата для альбома аудио, в котором объект содержит свойства фотоальбома и, при необходимости, данные.</span><span class="sxs-lookup"><span data-stu-id="6265c-228">Format code for an audio album where the object contains the properties of an audio album and, optionally, data.</span></span> <span data-ttu-id="6265c-229">Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.</span><span class="sxs-lookup"><span data-stu-id="6265c-229">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-230"><span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**ВМДМ \_ форматкоде \_ абстрактвидеоалбум**</span><span class="sxs-lookup"><span data-stu-id="6265c-230"><span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTVIDEOALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-231">Код формата для видеоальбома, в котором объект содержит свойства видеоальбома и, при необходимости, данные.</span><span class="sxs-lookup"><span data-stu-id="6265c-231">Format code for a video album where the object contains the properties of a video album and, optionally, data.</span></span> <span data-ttu-id="6265c-232">Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.</span><span class="sxs-lookup"><span data-stu-id="6265c-232">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-233"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**ВМДМ \_ форматкоде \_ абстрактаудиовидеоплайлист**</span><span class="sxs-lookup"><span data-stu-id="6265c-233"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**WMDM\_FORMATCODE\_ABSTRACTAUDIOVIDEOPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-234">Код формата для списка воспроизведения аудио/видео, в котором объект содержит свойства списка воспроизведения аудио/видео и, при необходимости, данных.</span><span class="sxs-lookup"><span data-stu-id="6265c-234">Format code for an audio/video playlist where the object contains the properties of an audio/video playlist and, optionally, data.</span></span> <span data-ttu-id="6265c-235">Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.</span><span class="sxs-lookup"><span data-stu-id="6265c-235">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-236"><span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**ВМДМ \_ форматкоде \_ абстрактконтактграуп**</span><span class="sxs-lookup"><span data-stu-id="6265c-236"><span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**WMDM\_FORMATCODE\_ABSTRACTCONTACTGROUP**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-237">Код формата для группы контактов, в которой объект содержит свойства группы контактов и, при необходимости, данные.</span><span class="sxs-lookup"><span data-stu-id="6265c-237">Format code for a contact group where the object contains the properties of a contact group and, optionally, data.</span></span> <span data-ttu-id="6265c-238">Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.</span><span class="sxs-lookup"><span data-stu-id="6265c-238">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-239"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**ВМДМ \_ форматкоде \_ абстрактмессажефолдер**</span><span class="sxs-lookup"><span data-stu-id="6265c-239"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**WMDM\_FORMATCODE\_ABSTRACTMESSAGEFOLDER**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-240">Код формата для папки сообщений, в которой объект содержит свойства папки сообщений и, при необходимости, данные.</span><span class="sxs-lookup"><span data-stu-id="6265c-240">Format code for a message folder where the object contains the properties of a message folder and, optionally, data.</span></span> <span data-ttu-id="6265c-241">Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.</span><span class="sxs-lookup"><span data-stu-id="6265c-241">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-242"><span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**ВМДМ \_ форматкоде \_ абстрактчаптередпродуктион**</span><span class="sxs-lookup"><span data-stu-id="6265c-242"><span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**WMDM\_FORMATCODE\_ABSTRACTCHAPTEREDPRODUCTION**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-243">Код формата для разбитого на разделы производства, в котором объект содержит свойства выглавной рабочей среды и (необязательно) данные.</span><span class="sxs-lookup"><span data-stu-id="6265c-243">Format code for a chaptered production where the object contains the properties of a chaptered production and, optionally, data.</span></span> <span data-ttu-id="6265c-244">Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.</span><span class="sxs-lookup"><span data-stu-id="6265c-244">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-245"><span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**ВМДМ \_ форматкоде \_ вплплайлист**</span><span class="sxs-lookup"><span data-stu-id="6265c-245"><span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**WMDM\_FORMATCODE\_WPLPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-246">Формат кода для списка воспроизведения, отформатированного с помощью формата списка воспроизведения Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6265c-246">Format code for a playlist formatted with Windows Media playlist formatting.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-247"><span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**ВМДМ \_ форматкоде \_ M3UPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="6265c-247"><span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**WMDM\_FORMATCODE\_M3UPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-248">Формат кода для списка воспроизведения с форматированием M3U.</span><span class="sxs-lookup"><span data-stu-id="6265c-248">Format code for a playlist with M3U formatting.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-249"><span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**ВМДМ \_ форматкоде \_ мплплайлист**</span><span class="sxs-lookup"><span data-stu-id="6265c-249"><span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**WMDM\_FORMATCODE\_MPLPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-250">Форматирование кода для списка воспроизведения с форматированием МПЛ.</span><span class="sxs-lookup"><span data-stu-id="6265c-250">Format code for a playlist with MPL formatting.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-251"><span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**ВМДМ \_ форматкоде \_ асксплайлист**</span><span class="sxs-lookup"><span data-stu-id="6265c-251"><span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**WMDM\_FORMATCODE\_ASXPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-252">Формат кода для списка воспроизведения с форматированием ASX.</span><span class="sxs-lookup"><span data-stu-id="6265c-252">Format code for a playlist with ASX formatting.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-253"><span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**ВМДМ \_ форматкоде \_ плсплайлист**</span><span class="sxs-lookup"><span data-stu-id="6265c-253"><span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**WMDM\_FORMATCODE\_PLSPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-254">Форматирование кода для списка воспроизведения с форматированием областей.</span><span class="sxs-lookup"><span data-stu-id="6265c-254">Format code for a playlist with PLS formatting.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-255"><span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**ВМДМ \_ форматкоде \_ ундефинеддокумент**</span><span class="sxs-lookup"><span data-stu-id="6265c-255"><span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**WMDM\_FORMATCODE\_UNDEFINEDDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-256">Код формата для документа неопределенного типа.</span><span class="sxs-lookup"><span data-stu-id="6265c-256">Format code for a document of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-257"><span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**ВМДМ \_ форматкоде \_ абстрактдокумент**</span><span class="sxs-lookup"><span data-stu-id="6265c-257"><span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**WMDM\_FORMATCODE\_ABSTRACTDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-258">Код формата для документа, в котором объект содержит свойства документа и, при необходимости, данные.</span><span class="sxs-lookup"><span data-stu-id="6265c-258">Format code for a document where the object contains the properties of a document and, optionally, data.</span></span> <span data-ttu-id="6265c-259">Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.</span><span class="sxs-lookup"><span data-stu-id="6265c-259">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-260"><span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**ВМДМ \_ форматкоде \_ XMLDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="6265c-260"><span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**WMDM\_FORMATCODE\_XMLDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-261">Код формата для XML-документа.</span><span class="sxs-lookup"><span data-stu-id="6265c-261">Format code for an XML document.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-262"><span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**ВМДМ \_ форматкоде \_ микрософтворддокумент**</span><span class="sxs-lookup"><span data-stu-id="6265c-262"><span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**WMDM\_FORMATCODE\_MICROSOFTWORDDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-263">Код формата для документа Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="6265c-263">Format code for a Microsoft Word document.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-264"><span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**ВМДМ \_ форматкоде \_ мхткомпиледхтмлдокумент**</span><span class="sxs-lookup"><span data-stu-id="6265c-264"><span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**WMDM\_FORMATCODE\_MHTCOMPILEDHTMLDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-265">Формат кода для скомпилированного HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="6265c-265">Format code for a compiled HTML document.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-266"><span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**ВМДМ \_ форматкоде \_ микрософтексцелспреадшит**</span><span class="sxs-lookup"><span data-stu-id="6265c-266"><span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**WMDM\_FORMATCODE\_MICROSOFTEXCELSPREADSHEET**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-267">Форматирование кода для электронной таблицы Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="6265c-267">Format code for a Microsoft Excel spreadsheet.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-268"><span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**ВМДМ \_ форматкоде \_ микрософтповерпоинтдокумент**</span><span class="sxs-lookup"><span data-stu-id="6265c-268"><span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**WMDM\_FORMATCODE\_MICROSOFTPOWERPOINTDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-269">Код формата для документа Microsoft PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="6265c-269">Format code for a Microsoft PowerPoint document.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-270"><span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**ВМДМ \_ форматкоде \_ ундефинедмессаже**</span><span class="sxs-lookup"><span data-stu-id="6265c-270"><span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**WMDM\_FORMATCODE\_UNDEFINEDMESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-271">Код формата для сообщения неопределенного типа.</span><span class="sxs-lookup"><span data-stu-id="6265c-271">Format code for a message of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-272"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**ВМДМ \_ форматкоде \_ абстрактмессаже**</span><span class="sxs-lookup"><span data-stu-id="6265c-272"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**WMDM\_FORMATCODE\_ABSTRACTMESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-273">Код формата для сообщения, в котором объект содержит свойства сообщения и, при необходимости, данные.</span><span class="sxs-lookup"><span data-stu-id="6265c-273">Format code for a message where the object contains the properties of a message and, optionally, data.</span></span> <span data-ttu-id="6265c-274">Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.</span><span class="sxs-lookup"><span data-stu-id="6265c-274">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-275"><span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**ВМДМ \_ форматкоде \_ ундефинедконтакт**</span><span class="sxs-lookup"><span data-stu-id="6265c-275"><span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**WMDM\_FORMATCODE\_UNDEFINEDCONTACT**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-276">Код формата для контакта неопределенного типа.</span><span class="sxs-lookup"><span data-stu-id="6265c-276">Format code for a contact of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-277"><span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**ВМДМ \_ форматкоде \_ абстрактконтакт**</span><span class="sxs-lookup"><span data-stu-id="6265c-277"><span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**WMDM\_FORMATCODE\_ABSTRACTCONTACT**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-278">Код формата для контакта, в котором объект содержит свойства контакта и (необязательно) данные.</span><span class="sxs-lookup"><span data-stu-id="6265c-278">Format code for a contact where the object contains the properties of a contact and, optionally, data.</span></span> <span data-ttu-id="6265c-279">Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.</span><span class="sxs-lookup"><span data-stu-id="6265c-279">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-280"><span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**ВМДМ \_ форматкоде \_ VCARD2**</span><span class="sxs-lookup"><span data-stu-id="6265c-280"><span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**WMDM\_FORMATCODE\_VCARD2**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-281">Код формата для электронной карты с форматом vCard версии 2.</span><span class="sxs-lookup"><span data-stu-id="6265c-281">Format code for an electronic card with vcard version 2 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-282"><span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**ВМДМ \_ форматкоде \_ VCARD3**</span><span class="sxs-lookup"><span data-stu-id="6265c-282"><span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**WMDM\_FORMATCODE\_VCARD3**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-283">Код формата для электронной карты с форматом vCard версии 3.</span><span class="sxs-lookup"><span data-stu-id="6265c-283">Format code for an electronic card with vcard version 3 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-284"><span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**ВМДМ \_ форматкоде \_ ундефинедкалендаритем**</span><span class="sxs-lookup"><span data-stu-id="6265c-284"><span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**WMDM\_FORMATCODE\_UNDEFINEDCALENDARITEM**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-285">Код формата для элемента электронного календаря неопределенного типа.</span><span class="sxs-lookup"><span data-stu-id="6265c-285">Format code for an electronic calendar item of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-286"><span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**ВМДМ \_ форматкоде \_ абстракткалендаритем**</span><span class="sxs-lookup"><span data-stu-id="6265c-286"><span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**WMDM\_FORMATCODE\_ABSTRACTCALENDARITEM**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-287">Код формата для элемента календаря, в котором объект содержит свойства элемента календаря и, при необходимости, данные.</span><span class="sxs-lookup"><span data-stu-id="6265c-287">Format code for a calendar item where the object contains the properties of a calendar item and, optionally, data.</span></span> <span data-ttu-id="6265c-288">Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.</span><span class="sxs-lookup"><span data-stu-id="6265c-288">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-289"><span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**ВМДМ \_ форматкоде \_ VCALENDAR1**</span><span class="sxs-lookup"><span data-stu-id="6265c-289"><span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**WMDM\_FORMATCODE\_VCALENDAR1**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-290">Код формата для элемента электронного календаря с форматированием vCalendar версии 1.</span><span class="sxs-lookup"><span data-stu-id="6265c-290">Format code for an electronic calendar item with vcalendar version 1 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-291"><span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**ВМДМ \_ форматкоде \_ VCALENDAR2**</span><span class="sxs-lookup"><span data-stu-id="6265c-291"><span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**WMDM\_FORMATCODE\_VCALENDAR2**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-292">Код формата для элемента электронного календаря с форматированием vCalendar версии 2.</span><span class="sxs-lookup"><span data-stu-id="6265c-292">Format code for an electronic calendar item with vcalendar version 2 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-293"><span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**ВМДМ \_ форматкоде \_ ундефинедвиндовсексекутабле**</span><span class="sxs-lookup"><span data-stu-id="6265c-293"><span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**WMDM\_FORMATCODE\_UNDEFINEDWINDOWSEXECUTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-294">Код формата для исполняемого файла Windows неопределенного типа.</span><span class="sxs-lookup"><span data-stu-id="6265c-294">Format code for a Windows-based executable of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-295"><span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**ВМДМ \_ форматкоде \_ мультимедиа \_ -приведение**</span><span class="sxs-lookup"><span data-stu-id="6265c-295"><span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**WMDM\_FORMATCODE\_MEDIA\_CAST**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-296">Код формата для объекта приведения к носителю.</span><span class="sxs-lookup"><span data-stu-id="6265c-296">Format code for a media cast object.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-297"><span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**\_раздел вмдм форматкоде \_**</span><span class="sxs-lookup"><span data-stu-id="6265c-297"><span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**WMDM\_FORMATCODE\_SECTION**</span></span>
</dt> <dd>

<span data-ttu-id="6265c-298">Код формата для раздела данных, содержащегося в другом объекте.</span><span class="sxs-lookup"><span data-stu-id="6265c-298">Format code for a section of data that is contained in another object.</span></span>

</dd> <dt>

<span data-ttu-id="6265c-299"><span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span>**Вмдм \_ ФОРМАТКОДЕ \_ 3G2A**</span><span class="sxs-lookup"><span data-stu-id="6265c-299"><span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span> **WMDM\_FORMATCODE\_3G2A**</span></span> 
</dt> <dd>

<span data-ttu-id="6265c-300">Код формата для формата контейнера мультимедиа 3G2A (3GPP2A).</span><span class="sxs-lookup"><span data-stu-id="6265c-300">Format code for a 3G2A (3GPP2A) multimedia container format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6265c-301">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6265c-301">Remarks</span></span>

<span data-ttu-id="6265c-302">Для обнаружения форматов, поддерживаемых устройством, приложение может использовать [**IWMDMDevice3::-Property**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) для запроса свойства **g \_ всзвмдмформатссуппортед** Device.</span><span class="sxs-lookup"><span data-stu-id="6265c-302">To discover the formats supported by a device, an application can use [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) to query the **g\_wszWMDMFormatsSupported** device property.</span></span>

<span data-ttu-id="6265c-303">Чтобы обнаружить возможности устройства для определенного формата, приложение может вызвать [**IWMDMDevice3:: жетформаткапабилити**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span><span class="sxs-lookup"><span data-stu-id="6265c-303">To discover device capabilities for a particular format, an application can call [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span></span>

<span data-ttu-id="6265c-304">Приложение может задать код формата при создании хранилища на устройстве, включив свойство **g \_ всзвмдмформаткоде** в метаданные, переданные в параметре *пметадата* вызова [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).</span><span class="sxs-lookup"><span data-stu-id="6265c-304">An application can set the format code while creating a storage on device by including the **g\_wszWMDMFormatCode** property in metadata passed in the *pMetaData* parameter of a call to [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).</span></span>

<span data-ttu-id="6265c-305">Приложение может запрашивать код формата хранилища, вызывая [**IWMDMStorage3::-Metadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) или [**IWMDMStorage4:: жетспеЦифиедметадата**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) и получая свойство **g \_ всзвмдмформаткоде** .</span><span class="sxs-lookup"><span data-stu-id="6265c-305">An application can query the format code of a storage by calling [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) and retrieving the **g\_wszWMDMFormatCode** property.</span></span>

<span data-ttu-id="6265c-306">Если устройство поддерживает задание кода формата после создания хранилища, приложение может использовать [**IWMDMStorage3:: сетметадата**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) для задания свойства **g \_ всзвмдмформаткоде** .</span><span class="sxs-lookup"><span data-stu-id="6265c-306">If the device supports setting the format code after the creation of storage, an application can use [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) to set the **g\_wszWMDMFormatCode** property.</span></span> <span data-ttu-id="6265c-307">Некоторые устройства могут не допускать изменения кода формата после создания хранилища на устройстве.</span><span class="sxs-lookup"><span data-stu-id="6265c-307">Some devices may not allow changing the format code after the storage is created on the device.</span></span> <span data-ttu-id="6265c-308">Поэтому настоятельно рекомендуется устанавливать это свойство вместе с метаданными, передаваемыми в [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) .</span><span class="sxs-lookup"><span data-stu-id="6265c-308">Therefore, setting this property along with the metadata passed in [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) is strongly recommended.</span></span>

## <a name="requirements"></a><span data-ttu-id="6265c-309">Требования</span><span class="sxs-lookup"><span data-stu-id="6265c-309">Requirements</span></span>



| <span data-ttu-id="6265c-310">Требование</span><span class="sxs-lookup"><span data-stu-id="6265c-310">Requirement</span></span> | <span data-ttu-id="6265c-311">Значение</span><span class="sxs-lookup"><span data-stu-id="6265c-311">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6265c-312">Header</span><span class="sxs-lookup"><span data-stu-id="6265c-312">Header</span></span><br/> | <dl> <span data-ttu-id="6265c-313"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6265c-313"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6265c-314">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6265c-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6265c-315">**Типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="6265c-315">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="6265c-316">**IWMDMDevice3:: Жетформаткапабилити**</span><span class="sxs-lookup"><span data-stu-id="6265c-316">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="6265c-317">**IWMDMDevice3:: Property**</span><span class="sxs-lookup"><span data-stu-id="6265c-317">**IWMDMDevice3::GetProperty**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)
</dt> <dt>

[<span data-ttu-id="6265c-318">**IWMDMStorage3:: Metadata**</span><span class="sxs-lookup"><span data-stu-id="6265c-318">**IWMDMStorage3::GetMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata)
</dt> <dt>

[<span data-ttu-id="6265c-319">**IWMDMStorage3:: Сетметадата**</span><span class="sxs-lookup"><span data-stu-id="6265c-319">**IWMDMStorage3::SetMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)
</dt> <dt>

[<span data-ttu-id="6265c-320">**IWMDMStorage4:: ЖетспеЦифиедметадата**</span><span class="sxs-lookup"><span data-stu-id="6265c-320">**IWMDMStorage4::GetSpecifiedMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)
</dt> <dt>

[<span data-ttu-id="6265c-321">**IWMDMStorageControl3::Insert3**</span><span class="sxs-lookup"><span data-stu-id="6265c-321">**IWMDMStorageControl3::Insert3**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)
</dt> <dt>

[<span data-ttu-id="6265c-322">**Константы метаданных**</span><span class="sxs-lookup"><span data-stu-id="6265c-322">**Metadata Constants**</span></span>](metadata-constants.md)
</dt> </dl>

 

 





