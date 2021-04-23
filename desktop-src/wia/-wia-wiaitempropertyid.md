---
description: Большая часть констант свойств для получения образа Windows (WIA) сгруппирована в один перечислимый тип данных, Виаитемпропертид для авторов скриптов.
ms.assetid: d0fd6bd1-c646-4ed8-a6b2-43b424af8288
title: виаитемпропертид
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6ced5d213d68fa3c4386ecf6f05783bd303bad05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809958"
---
# <a name="wiaitempropertyid"></a><span data-ttu-id="ceae0-103">виаитемпропертид</span><span class="sxs-lookup"><span data-stu-id="ceae0-103">WiaItemPropertyId</span></span>

<span data-ttu-id="ceae0-104">Большая часть констант свойств для получения образа Windows (WIA) сгруппирована в один перечислимый тип данных, Виаитемпропертид для авторов скриптов.</span><span class="sxs-lookup"><span data-stu-id="ceae0-104">Most of the Windows Image Acquisition (WIA) property constants are grouped in one enumerated data type, WiaItemPropertyId for scripting authors.</span></span>

<span data-ttu-id="ceae0-105">В следующей таблице представлено сопоставление соглашений об именовании, используемых в сценариях и C++.</span><span class="sxs-lookup"><span data-stu-id="ceae0-105">The following table presents the mapping between the naming conventions used in scripting and C++.</span></span> <span data-ttu-id="ceae0-106">Например, в скрипте префикс "Камерадевице" сопоставляется с \_ префиксом "WIA DPC" для соответствующей константы C++.</span><span class="sxs-lookup"><span data-stu-id="ceae0-106">For example, in script the "CameraDevice" prefix maps to the "WIA\_DPC" prefix for the corresponding C++ constant.</span></span> <span data-ttu-id="ceae0-107">В более конкретном примере свойство "Камерадевицефлашмоде" эквивалентно \_ \_ константе C++ "режим флэш-памяти WIA DPC \_ ".</span><span class="sxs-lookup"><span data-stu-id="ceae0-107">In a more specific example, the "CameraDeviceFlashMode" property is equivalent to the C++ "WIA\_DPC\_FLASH\_MODE" constant.</span></span> <span data-ttu-id="ceae0-108">Описание каждого свойства см. в соответствующих разделах констант свойств.</span><span class="sxs-lookup"><span data-stu-id="ceae0-108">See the corresponding property constant topics for descriptions of each property.</span></span> 

| <span data-ttu-id="ceae0-109">Префикс скрипта</span><span class="sxs-lookup"><span data-stu-id="ceae0-109">Script Prefix</span></span>  | <span data-ttu-id="ceae0-110">Раздел C++ (префикс)</span><span class="sxs-lookup"><span data-stu-id="ceae0-110">C++ Topic (prefix)</span></span>                                                                    |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ceae0-111">Устройство</span><span class="sxs-lookup"><span data-stu-id="ceae0-111">Device</span></span>         | [<span data-ttu-id="ceae0-112">**Общие константы свойств устройства (WIA \_ DPA)**</span><span class="sxs-lookup"><span data-stu-id="ceae0-112">**Common Device Property Constants (WIA\_DPA)**</span></span>](-wia-wiaitempropcommondevice.md)   |
| <span data-ttu-id="ceae0-113">камерадевице</span><span class="sxs-lookup"><span data-stu-id="ceae0-113">CameraDevice</span></span>   | [<span data-ttu-id="ceae0-114">**Константы свойств устройства камеры (WIA \_ DPC)**</span><span class="sxs-lookup"><span data-stu-id="ceae0-114">**Camera Device Property Constants (WIA\_DPC)**</span></span>](-wia-wiaitempropcameradevice.md)   |
| <span data-ttu-id="ceae0-115">сканнердевице</span><span class="sxs-lookup"><span data-stu-id="ceae0-115">ScannerDevice</span></span>  | [<span data-ttu-id="ceae0-116">**Константы свойств устройства сканера (WIA \_ DPS)**</span><span class="sxs-lookup"><span data-stu-id="ceae0-116">**Scanner Device Property Constants (WIA\_DPS)**</span></span>](-wia-wiaitempropscannerdevice.md) |
| <span data-ttu-id="ceae0-117">видеодевице</span><span class="sxs-lookup"><span data-stu-id="ceae0-117">VideoDevice</span></span>    | [<span data-ttu-id="ceae0-118">**Константы свойств видеоустройства WIA (WIA \_ ДПВ)**</span><span class="sxs-lookup"><span data-stu-id="ceae0-118">**Video WIA Device Property Constants (WIA\_DPV)**</span></span>](-wia-wiaitempropvideodevice.md) |
| <span data-ttu-id="ceae0-119">Picture</span><span class="sxs-lookup"><span data-stu-id="ceae0-119">Picture</span></span>        | [<span data-ttu-id="ceae0-120">**Стандартные константы свойств элементов WIA (WIA \_ IPA)**</span><span class="sxs-lookup"><span data-stu-id="ceae0-120">**Common WIA Item Property Constants (WIA\_IPA)**</span></span>](-wia-wiaitempropcommonitem.md)   |
| <span data-ttu-id="ceae0-121">камерапиктуре</span><span class="sxs-lookup"><span data-stu-id="ceae0-121">CameraPicture</span></span>  | [<span data-ttu-id="ceae0-122">**Константы свойства элемента WIA камеры (WIA \_ IPC)**</span><span class="sxs-lookup"><span data-stu-id="ceae0-122">**Camera WIA Item Property Constants (WIA\_IPC)**</span></span>](-wia-wiaitempropcameraitem.md)   |
| <span data-ttu-id="ceae0-123">сканнерпиктуре</span><span class="sxs-lookup"><span data-stu-id="ceae0-123">ScannerPicture</span></span> | [<span data-ttu-id="ceae0-124">**Константы свойства элемента сканера WIA ( \_ IP-адреса WIA)**</span><span class="sxs-lookup"><span data-stu-id="ceae0-124">**Scanner WIA Item Property Constants (WIA\_IPS)**</span></span>](-wia-wiaitempropscanneritem.md) |



 

<span data-ttu-id="ceae0-125">В следующем примере представлен полный перечислимый тип с соответствующими именами.</span><span class="sxs-lookup"><span data-stu-id="ceae0-125">The following example provides the complete enumerated type with the corresponding names.</span></span>


```JScript
typedef enum WiaItemPropertyId {
    CameraDevicePicturesTaken = WIA_DPC_PICTURES_TAKEN,
    CameraDevicePicturesRemaining = WIA_DPC_PICTURES_REMAINING,
    CameraDeviceExposureMode = WIA_DPC_EXPOSURE_MODE,
    CameraDeviceExposureComp = WIA_DPC_EXPOSURE_COMP,
    CameraDeviceExposureTime = WIA_DPC_EXPOSURE_TIME,
    CameraDeviceFNumber = WIA_DPC_FNUMBER,
    CameraDeviceFlashMode = WIA_DPC_FLASH_MODE,
    CameraDeviceFocusMode = WIA_DPC_FOCUS_MODE,
    CameraDevicePanPosition = WIA_DPC_PAN_POSITION,
    CameraDeviceTiltPosition = WIA_DPC_TILT_POSITION,
    CameraDeviceTimerMode = WIA_DPC_TIMER_MODE,
    CameraDeviceTimerValue = WIA_DPC_TIMER_VALUE,
    CameraDevicePowerMode = WIA_DPC_POWER_MODE,
    CameraDeviceBatteryStatus = WIA_DPC_BATTERY_STATUS,
    CameraDeviceThumbWidth = WIA_DPC_THUMB_WIDTH,
    CameraDeviceThumbHeight = WIA_DPC_THUMB_HEIGHT,
    CameraDevicePictWidth = WIA_DPC_PICT_WIDTH,
    CameraDevicePictHeight = WIA_DPC_PICT_HEIGHT,
    CameraDeviceCompressionSetting = WIA_DPC_COMPRESSION_SETTING,
    CameraDeviceTimelapseInterval = WIA_DPC_TIMELAPSE_INTERVAL,
    CameraDeviceTimelapseNumber = WIA_DPC_TIMELAPSE_NUMBER,
    CameraDeviceBurstInterval = WIA_DPC_BURST_INTERVAL,
    CameraDeviceBurstNumber = WIA_DPC_BURST_NUMBER,
    CameraDeviceEffectMode = WIA_DPC_EFFECT_MODE,
    CameraDeviceDigitalZoom = WIA_DPC_DIGITAL_ZOOM,
    CameraDeviceSharpness = WIA_DPC_SHARPNESS,
    CameraDeviceContrast = WIA_DPC_CONTRAST,
    CameraDeviceCaptureMode = WIA_DPC_CAPTURE_MODE,
    CameraDeviceCaptureDelay = WIA_DPC_CAPTURE_DELAY,
    CameraDeviceExposureIndex = WIA_DPC_EXPOSURE_INDEX,
    CameraDeviceExposureMeteringMode = WIA_DPC_EXPOSURE_METERING_MODE,
    CameraDeviceFocusMeteringMode = WIA_DPC_FOCUS_METERING_MODE,
    CameraDeviceFocusDistance = WIA_DPC_FOCUS_DISTANCE,
    CameraDeviceFocalLength = WIA_DPC_FOCAL_LENGTH,
    CameraDeviceRGBGain = WIA_DPC_RGB_GAIN,
    CameraDeviceWhiteBalance = WIA_DPC_WHITE_BALANCE,
    CameraDeviceUploadURL = WIA_DPC_UPLOAD_URL,
    CameraDeviceArtist = WIA_DPC_ARTIST,
    CameraDeviceCopyrightInfo = WIA_DPC_COPYRIGHT_INFO,
    ScannerDeviceHorizontalBedSize = WIA_DPS_HORIZONTAL_BED_SIZE,
    ScannerDeviceVerticalBedSize = WIA_DPS_VERTICAL_BED_SIZE,
    ScannerDeviceHorizontalSheetFeedSize = WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE,
    ScannerDeviceVerticalSheetFeedSize = WIA_DPS_VERTICAL_SHEET_FEED_SIZE,
    ScannerDeviceSheetFeederRegistration = WIA_DPS_SHEET_FEEDER_REGISTRATION,
    ScannerDeviceHorizontalBedRegistration = WIA_DPS_HORIZONTAL_BED_REGISTRATION,
    ScannerDeviceVerticalBedRegistration = WIA_DPS_VERTICAL_BED_REGISTRATION,
    ScannerDevicePlatenColor = WIA_DPS_PLATEN_COLOR,
    ScannerDevicePadColor = WIA_DPS_PAD_COLOR,
    ScannerDeviceDocumentHandlingCapabilities = WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES,
    ScannerDeviceDocumentHandlingStatus = WIA_DPS_DOCUMENT_HANDLING_STATUS,
    ScannerDeviceDocumentHandlingSelect = WIA_DPS_DOCUMENT_HANDLING_SELECT,
    ScannerDeviceDocumentHandlingCapacity = WIA_DPS_DOCUMENT_HANDLING_CAPACITY,
    ScannerDeviceOpticalXres = WIA_DPS_OPTICAL_XRES,
    ScannerDeviceOpticalYres = WIA_DPS_OPTICAL_YRES,
    ScannerDeviceEndorserCharacters = WIA_DPS_ENDORSER_CHARACTERS,
    ScannerDeviceEndorserString = WIA_DPS_ENDORSER_STRING,
    ScannerDeviceScanAheadPages = WIA_DPS_SCAN_AHEAD_PAGES,
    ScannerDeviceMaxScanTime = WIA_DPS_MAX_SCAN_TIME,
    ScannerDevicePages = WIA_DPS_PAGES,
    ScannerDevicePageSize = WIA_DPS_PAGE_SIZE,
    ScannerDevicePageWidth = WIA_DPS_PAGE_WIDTH,
    ScannerDevicePageHeight = WIA_DPS_PAGE_HEIGHT,
    ScannerDevicePreview = WIA_DPS_PREVIEW,
    ScannerDeviceTransparency = WIA_DPS_TRANSPARENCY,
    ScannerDeviceTransparencySelect = WIA_DPS_TRANSPARENCY_SELECT,
    ScannerDeviceShowPreviewControl = WIA_DPS_SHOW_PREVIEW_CONTROL,
    ScannerDeviceMinHorizontalSheetFeedSize = WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE,
    ScannerDeviceMinVerticalSheetFeedSize = WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE,
    FileDeviceMountPoint = WIA_DPF_MOUNT_POINT,
    VideoDeviceLastPictureTaken = WIA_DPV_LAST_PICTURE_TAKEN,
    VideoDeviceImagesDirectory = WIA_DPV_IMAGES_DIRECTORY,
    VideoDeviceDShowDevicePath = WIA_DPV_DSHOW_DEVICE_PATH,
    PictureItemName = WIA_IPA_ITEM_NAME,
    PictureFullItemName = WIA_IPA_FULL_ITEM_NAME,
    PictureItemTime = WIA_IPA_ITEM_TIME,
    PictureItemFlags = WIA_IPA_ITEM_FLAGS,
    PictureAccessRights = WIA_IPA_ACCESS_RIGHTS,
    PictureDatatype = WIA_IPA_DATATYPE,
    PictureDepth = WIA_IPA_DEPTH,
    PicturePreferredFormat = WIA_IPA_PREFERRED_FORMAT,
    PictureFormat = WIA_IPA_FORMAT,
    PictureCompression = WIA_IPA_COMPRESSION,
    PictureTymed = WIA_IPA_TYMED,
    PictureChannelsPerPixel = WIA_IPA_CHANNELS_PER_PIXEL,
    PictureBitsPerChannel = WIA_IPA_BITS_PER_CHANNEL,
    PicturePlanar = WIA_IPA_PLANAR,
    PicturePixelsPerLine = WIA_IPA_PIXELS_PER_LINE,
    PictureBytesPerLine = WIA_IPA_BYTES_PER_LINE,
    PictureNumberOfLines = WIA_IPA_NUMBER_OF_LINES,
    PictureGammaCurves = WIA_IPA_GAMMA_CURVES,
    PictureItemSize = WIA_IPA_ITEM_SIZE,
    PictureColorProfile = WIA_IPA_COLOR_PROFILE,
    PictureMinBufferSize = WIA_IPA_MIN_BUFFER_SIZE,
    PictureBufferSize = WIA_IPA_BUFFER_SIZE,
    PictureRegionType = WIA_IPA_REGION_TYPE,
    PictureIcmProfileName = WIA_IPA_ICM_PROFILE_NAME,
    PictureAppColorMapping = WIA_IPA_APP_COLOR_MAPPING,
    PicturePropStreamCompatId = WIA_IPA_PROP_STREAM_COMPAT_ID,
    PictureFilenameExtension = WIA_IPA_FILENAME_EXTENSION,
    PictureSuppressPropertyPage = WIA_IPA_SUPPRESS_PROPERTY_PAGE,
    CameraPictureThumbnail = WIA_IPC_THUMBNAIL,
    CameraPictureThumbWidth = WIA_IPC_THUMB_WIDTH,
    CameraPictureThumbHeight = WIA_IPC_THUMB_HEIGHT,
    CameraPictureAudioAvailable = WIA_IPC_AUDIO_AVAILABLE,
    CameraPictureAudioDataFormat = WIA_IPC_AUDIO_DATA_FORMAT,
    CameraPictureAudioData = WIA_IPC_AUDIO_DATA,
    CameraPictureNumPictPerRow = WIA_IPC_NUM_PICT_PER_ROW,
    CameraPictureSequence = WIA_IPC_SEQUENCE,
    CameraPictureTimedelay = WIA_IPC_TIMEDELAY,
    ScannerPictureCurIntent = WIA_IPS_CUR_INTENT,
    ScannerPictureXres = WIA_IPS_XRES,
    ScannerPictureYres = WIA_IPS_YRES,
    ScannerPictureXpos = WIA_IPS_XPOS,
    ScannerPictureYpos = WIA_IPS_YPOS,
    ScannerPictureXextent = WIA_IPS_XEXTENT,
    ScannerPictureYextent = WIA_IPS_YEXTENT,
    ScannerPicturePhotometricInterp = WIA_IPS_PHOTOMETRIC_INTERP,
    ScannerPictureBrightness = WIA_IPS_BRIGHTNESS,
    ScannerPictureContrast = WIA_IPS_CONTRAST,
    ScannerPictureOrientation = WIA_IPS_ORIENTATION,
    ScannerPictureRotation = WIA_IPS_ROTATION,
    ScannerPictureMirror = WIA_IPS_MIRROR,
    ScannerPictureThreshold = WIA_IPS_THRESHOLD,
    ScannerPictureInvert = WIA_IPS_INVERT,
    ScannerPictureWarmUpTime = WIA_IPS_WARM_UP_TIME
} WiaItemPropertyId;
```



 

 



