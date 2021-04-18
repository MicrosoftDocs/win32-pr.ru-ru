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
# <a name="wmdm_formatcode-enumeration"></a>\_Перечисление ФОРМАТКОДЕ вмдм

Тип перечисления **вмдм \_ форматкоде** определяет список кодов форматов, описывающих типы содержимого, передаваемые на устройство и с устройства.

## <a name="syntax"></a>Синтаксис


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



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**ВМДМ \_ форматкоде \_ нотусед**
</dt> <dd>

Код формата не используется.

</dd> <dt>

<span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**ВМДМ \_ форматкоде \_ аллимажес**
</dt> <dd>

Код формата, который может использоваться для запроса всех изображений.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**ВМДМ \_ форматкоде не \_ определен**
</dt> <dd>

Код формата, используемый для запроса всех неопределенных объектов.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**\_сопоставление вмдм форматкоде \_**
</dt> <dd>

Код формата, используемый для определения связи между двумя объектами.

</dd> <dt>

<span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**ВМДМ \_ форматкоде \_ сценарий**
</dt> <dd>

Код формата для файла скрипта.

</dd> <dt>

<span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**\_ \_ исполняемый файл форматкоде вмдм**
</dt> <dd>

Код формата для исполняемого файла.

</dd> <dt>

<span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**ВМДМ \_ форматкоде \_ текст**
</dt> <dd>

Форматирование кода для текстового файла.

</dd> <dt>

<span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**ВМДМ \_ форматкоде \_ HTML**
</dt> <dd>

Код формата для HTML-файла.

</dd> <dt>

<span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**ВМДМ \_ форматкоде \_ дпоф**
</dt> <dd>

Код формата, используемый для представления формата цифрового порядка печати.

</dd> <dt>

<span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**ВМДМ \_ форматкоде \_**
</dt> <dd>

Код формата, используемый для представления формата файла обмена аудио.

</dd> <dt>

<span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**\_волна вмдм форматкоде \_**
</dt> <dd>

Формат кода, используемый для WAV-файла.

</dd> <dt>

<span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**ВМДМ \_ форматкоде \_ MP3**
</dt> <dd>

Формат кода, используемый для MP3-файла.

</dd> <dt>

<span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**ВМДМ \_ форматкоде \_ AVI**
</dt> <dd>

Код формата, используемый для файла AVI.

</dd> <dt>

<span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**ВМДМ \_ форматкоде \_ MPEG**
</dt> <dd>

Код формата, используемый для файла MPEG.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**ВМДМ \_ форматкоде \_ ASF**
</dt> <dd>

Код формата, используемый для представления файла расширенных систем формата (ASF).

</dd> <dt>

<span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**ВМДМ \_ форматкоде \_ сначала зарезервировано \_**
</dt> <dd>

Код формата, который является первым в диапазоне, зарезервированном для протокола обмена изображениями (PTP).

</dd> <dt>

<span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**ВМДМ \_ форматкоде \_ зарезервированный \_ последний**
</dt> <dd>

Код формата, который последним в диапазоне, зарезервированном для PTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**\_изображение вмдм форматкоде не \_ \_ определено**
</dt> <dd>

Код формата, используемый для представления и изображения неопределенного типа.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**ВМДМ \_ форматкоде \_ image \_ EXIF**
</dt> <dd>

Код формата для файла EXIF. Также используется для изображений JPEG, не охваченных ВМДМ \_ форматкоде \_ image \_ JP2 или вмдм \_ форматкоде \_ image \_ жпкс.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**ВМДМ \_ форматкоде \_ image \_ тиффеп**
</dt> <dd>

Код формата, используемый для изображений, имеющих формат файла изображения с тегами для электронной фотографии (TIFF/EP)

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**ВМДМ \_ форматкоде \_ image \_ флашпикс**
</dt> <dd>

Код формата для файла типа ФПКС.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**ВМДМ \_ форматкоде \_ image \_ BMP**
</dt> <dd>

Код формата для файла типа BMP.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**ВМДМ \_ форматкоде \_ image \_ Цифф**
</dt> <dd>

Формат кода для изображения в формате файла изображения камеры.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**ВМДМ \_ форматкоде \_ изображение \_ GIF**
</dt> <dd>

Форматирование кода для GIF-файла.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**ВМДМ \_ форматкоде \_ image \_ JFIF**
</dt> <dd>

Код формата для файла типа JFIF.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**ВМДМ \_ форматкоде \_ image \_ ПКД**
</dt> <dd>

Код формата для изображения типа "Фото CD".

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**ВМДМ \_ форматкоде \_ изображение \_ PICT**
</dt> <dd>

Код формата для изображения типа PICT.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**ВМДМ \_ форматкоде \_ image \_ PNG**
</dt> <dd>

Код формата для изображения типа PNG.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**ВМДМ \_ форматкоде \_ image \_ TIFF**
</dt> <dd>

Код формата для файла типа TIFF.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**ВМДМ \_ форматкоде \_ image \_ тиффит**
</dt> <dd>

Код формата для изображения типа Tagged Image File Format с помощью технологии Image.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**ВМДМ \_ форматкоде \_ image \_ JP2**
</dt> <dd>

Код формата для изображения jpeg200.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**ВМДМ \_ форматкоде \_ image \_ жпкс**
</dt> <dd>

Код формата для образа, созданного на основе JPEG200, с использованием расширенной регистрации изображений. Обычно используется расширение имени файла. жпф или. жпкс.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**\_ \_ \_ предварительно зарезервированный образ вмдм форматкоде \_**
</dt> <dd>

Код формата, который является первым в диапазоне, зарезервированном для ссылки на изображение в PTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**снимок ВМДМ \_ форматкоде, \_ \_ зарезервированный \_ последним**
</dt> <dd>

Форматирование кода, который является последним в диапазоне, зарезервированном для ссылки на изображение в PTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**ВМДМ \_ форматкоде \_ ундефинедфирмваре**
</dt> <dd>

Форматировать код, если встроенное по не определено.

</dd> <dt>

<span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span>**Вмдм \_ ФОРМАТКОДЕ \_ WBMP** 
</dt> <dd>

Код формата для точечного рисунка протокола приложения беспроводной связи (. WBMP).

</dd> <dt>

<span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span>**Вмдм \_ ФОРМАТКОДЕ \_ жпегкср** 
</dt> <dd>

Формат кода для изображения фотографии HD

</dd> <dt>

<span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**ВМДМ \_ форматкоде \_ виндовсимажеформат**
</dt> <dd>

Код формата для формата образа Windows.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**ВМДМ \_ форматкоде \_ ундефинедаудио**
</dt> <dd>

Код формата для звукового файла неопределенного типа.

</dd> <dt>

<span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**ВМДМ \_ форматкоде \_ WMA**
</dt> <dd>

Код формата для WMA-файла Windows Media Audio.

</dd> <dt>

<span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**ВМДМ \_ форматкоде \_ OGG**
</dt> <dd>

Код формата для звукового файла с Vorbis кодировкой в контейнере OGG.

</dd> <dt>

<span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**ВМДМ \_ форматкоде \_ AAC**
</dt> <dd>

Код формата для расширенного файла аудио-кодирования (AAC).

</dd> <dt>

<span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**ВМДМ \_ форматкоде \_**
</dt> <dd>

Код формата для звукового файла.

</dd> <dt>

<span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**ВМДМ \_ форматкоде \_ FLAC**
</dt> <dd>

Код формата для бесплатного файла аудиокодека без потерь (FLAC).

</dd> <dt>

<span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span>**Вмдм \_ ФОРМАТКОДЕ \_ кцелп** 
</dt> <dd>

Код формата для файлового кодека линейного прогноза Qualcomm (КЦЕЛП).

</dd> <dt>

<span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span>**Вмдм \_ ФОРМАТКОДЕ \_ AMR** 
</dt> <dd>

Код формата для файла кодека адаптивной многочастотной аудиоподсистемы (AMR).

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**ВМДМ \_ форматкоде \_ ундефинедвидео**
</dt> <dd>

Формат кода для видеофайла с неопределенным типом.

</dd> <dt>

<span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**ВМДМ \_ форматкоде \_ WMV**
</dt> <dd>

Код формата для файла видео Windows Media (WMV).

</dd> <dt>

<span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**ВМДМ \_ форматкоде \_ MP4**
</dt> <dd>

Код формата для файла MP4.

</dd> <dt>

<span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**ВМДМ \_ форматкоде \_ MP2**
</dt> <dd>

Код формата для файла MP2.

</dd> <dt>

<span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span>**Вмдм \_ ФОРМАТКОДЕ \_ 3G2** 
</dt> <dd>

Код формата для формата контейнера мультимедиа 3G2 (3GPP2). Файл этого типа может содержать аудио, видео или текст.

</dd> <dt>

<span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span>**Вмдм \_ ФОРМАТКОДЕ \_ авчд** 
</dt> <dd>

Код формата для видео-файла АВЧД (расширенного кодирования видео с высоким определением).

</dd> <dt>

<span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span>**Вмдм \_ ФОРМАТКОДЕ \_ атсктс** 
</dt> <dd>

Код формата для стандарта расширенного формата комитетов телевизионных систем (АТСКТС).

</dd> <dt>

<span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span>**Вмдм \_ ФОРМАТКОДЕ \_ двбтс** 
</dt> <dd>

Код формата для видео MPEG-2 и 2-1 уровня II или AC-3, аудио в соответствующем стандарте канале транспорта MPEG-2.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**ВМДМ \_ форматкоде \_ ундефинедколлектион**
</dt> <dd>

Код формата для коллекции неопределенного типа.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**ВМДМ \_ форматкоде \_ абстрактмултимедиаалбум**
</dt> <dd>

Код формата для мультимедийного альбома, где объект содержит свойства мультимедийного альбома и, при необходимости, данные. Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**ВМДМ \_ форматкоде \_ абстрактимажеалбум**
</dt> <dd>

Код формата для альбома образа, в котором объект содержит свойства альбома изображения и, при необходимости, данные. Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**ВМДМ \_ форматкоде \_ абстрактаудиоалбум**
</dt> <dd>

Код формата для альбома аудио, в котором объект содержит свойства фотоальбома и, при необходимости, данные. Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**ВМДМ \_ форматкоде \_ абстрактвидеоалбум**
</dt> <dd>

Код формата для видеоальбома, в котором объект содержит свойства видеоальбома и, при необходимости, данные. Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**ВМДМ \_ форматкоде \_ абстрактаудиовидеоплайлист**
</dt> <dd>

Код формата для списка воспроизведения аудио/видео, в котором объект содержит свойства списка воспроизведения аудио/видео и, при необходимости, данных. Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**ВМДМ \_ форматкоде \_ абстрактконтактграуп**
</dt> <dd>

Код формата для группы контактов, в которой объект содержит свойства группы контактов и, при необходимости, данные. Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**ВМДМ \_ форматкоде \_ абстрактмессажефолдер**
</dt> <dd>

Код формата для папки сообщений, в которой объект содержит свойства папки сообщений и, при необходимости, данные. Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**ВМДМ \_ форматкоде \_ абстрактчаптередпродуктион**
</dt> <dd>

Код формата для разбитого на разделы производства, в котором объект содержит свойства выглавной рабочей среды и (необязательно) данные. Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**ВМДМ \_ форматкоде \_ вплплайлист**
</dt> <dd>

Формат кода для списка воспроизведения, отформатированного с помощью формата списка воспроизведения Windows Media.

</dd> <dt>

<span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**ВМДМ \_ форматкоде \_ M3UPLAYLIST**
</dt> <dd>

Формат кода для списка воспроизведения с форматированием M3U.

</dd> <dt>

<span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**ВМДМ \_ форматкоде \_ мплплайлист**
</dt> <dd>

Форматирование кода для списка воспроизведения с форматированием МПЛ.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**ВМДМ \_ форматкоде \_ асксплайлист**
</dt> <dd>

Формат кода для списка воспроизведения с форматированием ASX.

</dd> <dt>

<span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**ВМДМ \_ форматкоде \_ плсплайлист**
</dt> <dd>

Форматирование кода для списка воспроизведения с форматированием областей.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**ВМДМ \_ форматкоде \_ ундефинеддокумент**
</dt> <dd>

Код формата для документа неопределенного типа.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**ВМДМ \_ форматкоде \_ абстрактдокумент**
</dt> <dd>

Код формата для документа, в котором объект содержит свойства документа и, при необходимости, данные. Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**ВМДМ \_ форматкоде \_ XMLDOCUMENT**
</dt> <dd>

Код формата для XML-документа.

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**ВМДМ \_ форматкоде \_ микрософтворддокумент**
</dt> <dd>

Код формата для документа Microsoft Word.

</dd> <dt>

<span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**ВМДМ \_ форматкоде \_ мхткомпиледхтмлдокумент**
</dt> <dd>

Формат кода для скомпилированного HTML-документа.

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**ВМДМ \_ форматкоде \_ микрософтексцелспреадшит**
</dt> <dd>

Форматирование кода для электронной таблицы Microsoft Excel.

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**ВМДМ \_ форматкоде \_ микрософтповерпоинтдокумент**
</dt> <dd>

Код формата для документа Microsoft PowerPoint.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**ВМДМ \_ форматкоде \_ ундефинедмессаже**
</dt> <dd>

Код формата для сообщения неопределенного типа.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**ВМДМ \_ форматкоде \_ абстрактмессаже**
</dt> <dd>

Код формата для сообщения, в котором объект содержит свойства сообщения и, при необходимости, данные. Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**ВМДМ \_ форматкоде \_ ундефинедконтакт**
</dt> <dd>

Код формата для контакта неопределенного типа.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**ВМДМ \_ форматкоде \_ абстрактконтакт**
</dt> <dd>

Код формата для контакта, в котором объект содержит свойства контакта и (необязательно) данные. Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**ВМДМ \_ форматкоде \_ VCARD2**
</dt> <dd>

Код формата для электронной карты с форматом vCard версии 2.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**ВМДМ \_ форматкоде \_ VCARD3**
</dt> <dd>

Код формата для электронной карты с форматом vCard версии 3.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**ВМДМ \_ форматкоде \_ ундефинедкалендаритем**
</dt> <dd>

Код формата для элемента электронного календаря неопределенного типа.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**ВМДМ \_ форматкоде \_ абстракткалендаритем**
</dt> <dd>

Код формата для элемента календаря, в котором объект содержит свойства элемента календаря и, при необходимости, данные. Все содержащиеся в нем данные имеют неопределенный формат в соответствии со спецификацией MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**ВМДМ \_ форматкоде \_ VCALENDAR1**
</dt> <dd>

Код формата для элемента электронного календаря с форматированием vCalendar версии 1.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**ВМДМ \_ форматкоде \_ VCALENDAR2**
</dt> <dd>

Код формата для элемента электронного календаря с форматированием vCalendar версии 2.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**ВМДМ \_ форматкоде \_ ундефинедвиндовсексекутабле**
</dt> <dd>

Код формата для исполняемого файла Windows неопределенного типа.

</dd> <dt>

<span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**ВМДМ \_ форматкоде \_ мультимедиа \_ -приведение**
</dt> <dd>

Код формата для объекта приведения к носителю.

</dd> <dt>

<span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**\_раздел вмдм форматкоде \_**
</dt> <dd>

Код формата для раздела данных, содержащегося в другом объекте.

</dd> <dt>

<span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span>**Вмдм \_ ФОРМАТКОДЕ \_ 3G2A** 
</dt> <dd>

Код формата для формата контейнера мультимедиа 3G2A (3GPP2A).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Для обнаружения форматов, поддерживаемых устройством, приложение может использовать [**IWMDMDevice3::-Property**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) для запроса свойства **g \_ всзвмдмформатссуппортед** Device.

Чтобы обнаружить возможности устройства для определенного формата, приложение может вызвать [**IWMDMDevice3:: жетформаткапабилити**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).

Приложение может задать код формата при создании хранилища на устройстве, включив свойство **g \_ всзвмдмформаткоде** в метаданные, переданные в параметре *пметадата* вызова [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).

Приложение может запрашивать код формата хранилища, вызывая [**IWMDMStorage3::-Metadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) или [**IWMDMStorage4:: жетспеЦифиедметадата**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) и получая свойство **g \_ всзвмдмформаткоде** .

Если устройство поддерживает задание кода формата после создания хранилища, приложение может использовать [**IWMDMStorage3:: сетметадата**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) для задания свойства **g \_ всзвмдмформаткоде** . Некоторые устройства могут не допускать изменения кода формата после создания хранилища на устройстве. Поэтому настоятельно рекомендуется устанавливать это свойство вместе с метаданными, передаваемыми в [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдм. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Типы перечислений**](enumeration-types.md)
</dt> <dt>

[**IWMDMDevice3:: Жетформаткапабилити**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**IWMDMDevice3:: Property**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)
</dt> <dt>

[**IWMDMStorage3:: Metadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata)
</dt> <dt>

[**IWMDMStorage3:: Сетметадата**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)
</dt> <dt>

[**IWMDMStorage4:: ЖетспеЦифиедметадата**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)
</dt> <dt>

[**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)
</dt> <dt>

[**Константы метаданных**](metadata-constants.md)
</dt> </dl>

 

 





