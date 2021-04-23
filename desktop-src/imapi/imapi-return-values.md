---
title: Возвращаемые значения IMAPI (Imapi2error. h)
description: Методы IMAPI возвращают неотрицательные значения (обычно S \_ ОК), если метод был успешным. Методы IMAPI возвращают коды успеха или ошибки из Winerror. h, Imapi2error. h или Imapi2fserror. h в случае сбоя.
ms.assetid: 0e62ed6c-4810-4d36-a759-9b02b68face6
topic_type:
- apiref
api_name:
- E_IMAPI_BURN_VERIFICATION_FAILED
- E_IMAPI_REQUEST_CANCELLED
- E_IMAPI_RECORDER_REQUIRED
- S_IMAPI_WRITE_NOT_IN_PROGRESS
- S_IMAPI_SPEEDADJUSTED
- S_IMAPI_ROTATIONADJUSTED
- S_IMAPI_BOTHADJUSTED
- S_IMAPI_COMMAND_HAS_SENSE_DATA
- E_IMAPI_RAW_IMAGE_IS_READ_ONLY
- E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS
- E_IMAPI_RAW_IMAGE_NO_TRACKS
- E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED
- E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED
- E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE
- E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES
- E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND
- S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS
- E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED
- E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX
- E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE
- E_IMAPI_RECORDER_MEDIA_NO_MEDIA
- E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE
- E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN
- E_IMAPI_RECORDER_MEDIA_BECOMING_READY
- E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS
- E_IMAPI_RECORDER_MEDIA_BUSY
- E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS
- E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED
- E_IMAPI_RECORDER_NO_SUCH_FEATURE
- E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT
- E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED
- E_IMAPI_RECORDER_COMMAND_TIMEOUT
- E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT
- E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH
- E_IMAPI_RECORDER_LOCKED
- E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE
- E_IMAPI_LOSS_OF_STREAMING
- E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE
- E_IMAPI_DF2DATA_WRITE_IN_PROGRESS
- E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS
- E_IMAPI_DF2DATA_INVALID_MEDIA_STATE
- E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED
- E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA
- E_IMAPI_DF2DATA_MEDIA_NOT_BLANK
- E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED
- E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_DF2TAO_WRITE_IN_PROGRESS
- E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS
- E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED
- E_IMAPI_DF2TAO_MEDIA_IS_PREPARED
- E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY
- E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC
- E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK
- E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED
- E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE
- E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED
- E_IMAPI_DF2TAO_INVALID_ISRC
- E_IMAPI_DF2TAO_INVALID_MCN
- E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED
- E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED
- E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_DF2RAW_WRITE_IN_PROGRESS
- E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS
- E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED
- E_IMAPI_DF2RAW_MEDIA_IS_PREPARED
- E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK
- E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE
- E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED
- E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED
- E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED
- E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT
- E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED
- E_IMAPI_ERASE_RECORDER_IN_USE
- E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED
- E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL
- E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL
- E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE
- E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND
- E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR
- E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE
- E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND
- E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED
- E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID
- IMAPI_E_FSI_INTERNAL_ERROR
- IMAPI_E_INVALID_PARAM
- IMAPI_E_READONLY
- IMAPI_E_NO_OUTPUT
- IMAPI_E_INVALID_VOLUME_NAME
- IMAPI_E_INVALID_DATE
- IMAPI_E_FILE_SYSTEM_NOT_EMPTY
- IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED
- IMAPI_E_NOT_FILE
- IMAPI_E_NOT_DIR
- IMAPI_E_DIR_NOT_EMPTY
- IMAPI_E_NOT_IN_FILE_SYSTEM
- IMAPI_E_INVALID_PATH
- IMAPI_E_RESTRICTED_NAME_VIOLATION
- IMAPI_E_DUP_NAME
- IMAPI_E_NO_UNIQUE_NAME
- IMAPI_E_ITEM_NOT_FOUND
- IMAPI_E_FILE_NOT_FOUND
- IMAPI_E_DIR_NOT_FOUND
- IMAPI_E_IMAGE_SIZE_LIMIT
- IMAPI_E_IMAGE_TOO_BIG
- IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED
- IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND
- IMAPI_E_IMAGEMANAGER_NO_IMAGE
- IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG
- IMAPI_E_DATA_STREAM_INCONSISTENCY
- IMAPI_E_DATA_STREAM_READ_FAILURE
- IMAPI_E_DATA_STREAM_CREATE_FAILURE
- IMAPI_E_DIRECTORY_READ_FAILURE
- IMAPI_E_TOO_MANY_DIRS
- IMAPI_E_ISO9660_LEVELS
- IMAPI_E_DATA_TOO_BIG
- IMAPI_E_STASHFILE_OPEN_FAILURE
- IMAPI_E_STASHFILE_SEEK_FAILURE
- IMAPI_E_STASHFILE_WRITE_FAILURE
- IMAPI_E_STASHFILE_READ_FAILURE
- IMAPI_E_INVALID_WORKING_DIRECTORY
- IMAPI_E_WORKING_DIRECTORY_SPACE
- IMAPI_E_STASHFILE_MOVE
- IMAPI_E_BOOT_IMAGE_DATA
- IMAPI_E_BOOT_OBJECT_CONFLICT
- IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH
- IMAPI_E_EMPTY_DISC
- IMAPI_E_NO_SUPPORTED_FILE_SYSTEM
- IMAPI_E_FILE_SYSTEM_NOT_FOUND
- IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR
- IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED
- IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY
- IMAPI_E_IMPORT_SEEK_FAILURE
- IMAPI_E_IMPORT_READ_FAILURE
- IMAPI_E_DISC_MISMATCH
- IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED
- IMAPI_E_UDF_NOT_WRITE_COMPATIBLE
- IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE
- IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION
- IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE
- IMAPI_E_MULTISESSION_NOT_SET
- IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE
- IMAPI_E_BAD_MULTISESSION_PARAMETER
- IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED
api_location:
- Imapi2error.h
- Imapi2fserror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6bc4b99bb5ac123ea26ca1deb755fa29598811b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491052"
---
# <a name="imapi-return-values"></a><span data-ttu-id="1727f-104">Возвращаемые значения IMAPI</span><span class="sxs-lookup"><span data-stu-id="1727f-104">IMAPI Return Values</span></span>

<span data-ttu-id="1727f-105">Методы IMAPI возвращают неотрицательные значения (обычно S \_ ОК), если метод был успешным.</span><span class="sxs-lookup"><span data-stu-id="1727f-105">The IMAPI methods return non-negative values, (typically S\_OK) if the method was successful.</span></span> <span data-ttu-id="1727f-106">Методы IMAPI возвращают коды успеха или ошибки из Winerror. h, Imapi2error. h или Imapi2fserror. h в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="1727f-106">The IMAPI methods return success or error codes from Winerror.h, Imapi2error.h, or Imapi2fserror.h, on failure.</span></span>

<span data-ttu-id="1727f-107">Определены следующие коды успеха и ошибки.</span><span class="sxs-lookup"><span data-stu-id="1727f-107">The following success and error codes are defined.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="1727f-108">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="1727f-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="1727f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1727f-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_BURN_VERIFICATION_FAILED"></span><span id="e_imapi_burn_verification_failed"></span><dl> <span data-ttu-id="1727f-110"><dt><strong>E_IMAPI_BURN_VERIFICATION_FAILED</strong></dt> <dt>(HRESULT) 0xC0AA0007L</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-110"><dt><strong>E_IMAPI_BURN_VERIFICATION_FAILED</strong></dt> <dt>(HRESULT)0xC0AA0007L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-111">Диск не прошел проверку записи и может содержать поврежденные данные или быть непригодным для использования.</span><span class="sxs-lookup"><span data-stu-id="1727f-111">The disc did not pass burn verification and may contain corrupt data or be unusable.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_REQUEST_CANCELLED"></span><span id="e_imapi_request_cancelled"></span><dl> <span data-ttu-id="1727f-112"><dt><strong>E_IMAPI_REQUEST_CANCELLED</strong></dt> <dt>(HRESULT) 0xC0AA0002</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-112"><dt><strong>E_IMAPI_REQUEST_CANCELLED</strong></dt> <dt>(HRESULT)0xC0AA0002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-113">Запрос отменен.</span><span class="sxs-lookup"><span data-stu-id="1727f-113">The request was canceled.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_REQUIRED"></span><span id="e_imapi_recorder_required"></span><dl> <span data-ttu-id="1727f-114"><dt><strong>E_IMAPI_RECORDER_REQUIRED</strong></dt> <dt>(HRESULT) 0xC0AA0003</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-114"><dt><strong>E_IMAPI_RECORDER_REQUIRED</strong></dt> <dt>(HRESULT)0xC0AA0003</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-115">Для запроса требуется выбрать текущий записывающий диск.</span><span class="sxs-lookup"><span data-stu-id="1727f-115">The request requires a current disc recorder to be selected.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="S_IMAPI_WRITE_NOT_IN_PROGRESS"></span><span id="s_imapi_write_not_in_progress"></span><dl> <span data-ttu-id="1727f-116"><dt><strong>S_IMAPI_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0x00AA0302L</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-116"><dt><strong>S_IMAPI_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0x00AA0302L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-117">В настоящее время операции записи не выполняются.</span><span class="sxs-lookup"><span data-stu-id="1727f-117">No write operation is currently in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="S_IMAPI_SPEEDADJUSTED"></span><span id="s_imapi_speedadjusted"></span><dl> <span data-ttu-id="1727f-118"><dt><strong>S_IMAPI_SPEEDADJUSTED</strong></dt> <dt>(HRESULT) 0x00AA0004</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-118"><dt><strong>S_IMAPI_SPEEDADJUSTED</strong></dt> <dt>(HRESULT)0x00AA0004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-119">Запрошенная скорость записи не поддерживается диском, и была скорректирована скорость.</span><span class="sxs-lookup"><span data-stu-id="1727f-119">The requested write speed was not supported by the drive and the speed was adjusted.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="S_IMAPI_ROTATIONADJUSTED"></span><span id="s_imapi_rotationadjusted"></span><dl> <span data-ttu-id="1727f-120"><dt><strong>S_IMAPI_ROTATIONADJUSTED</strong></dt> <dt>(HRESULT) 0x00AA0005</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-120"><dt><strong>S_IMAPI_ROTATIONADJUSTED</strong></dt> <dt>(HRESULT)0x00AA0005</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-121">Запрошенный тип вращения не поддерживается диском, и тип вращения был скорректирован.</span><span class="sxs-lookup"><span data-stu-id="1727f-121">The requested rotation type was not supported by the drive and the rotation type was adjusted.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="S_IMAPI_BOTHADJUSTED"></span><span id="s_imapi_bothadjusted"></span><dl> <span data-ttu-id="1727f-122"><dt><strong>S_IMAPI_BOTHADJUSTED</strong></dt> <dt>(HRESULT) 0x00AA0006</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-122"><dt><strong>S_IMAPI_BOTHADJUSTED</strong></dt> <dt>(HRESULT)0x00AA0006</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-123">Запрошенная скорость записи и тип вращения не поддерживались диском, и они были скорректированы.</span><span class="sxs-lookup"><span data-stu-id="1727f-123">The requested write speed and rotation type were not supported by the drive and they were both adjusted.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="S_IMAPI_COMMAND_HAS_SENSE_DATA"></span><span id="s_imapi_command_has_sense_data"></span><dl> <span data-ttu-id="1727f-124"><dt><strong>S_IMAPI_COMMAND_HAS_SENSE_DATA</strong></dt> <dt>(HRESULT) 0x00AA0200</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-124"><dt><strong>S_IMAPI_COMMAND_HAS_SENSE_DATA</strong></dt> <dt>(HRESULT)0x00AA0200</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-125">Устройство приняло команду, но вернуло данные, указывающие на ошибку.</span><span class="sxs-lookup"><span data-stu-id="1727f-125">The device accepted the command, but returned sense data, indicating an error.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_IS_READ_ONLY"></span><span id="e_imapi_raw_image_is_read_only"></span><dl> <span data-ttu-id="1727f-126"><dt><strong>E_IMAPI_RAW_IMAGE_IS_READ_ONLY</strong></dt> <dt>(HRESULT) 0x80AA0A00L</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-126"><dt><strong>E_IMAPI_RAW_IMAGE_IS_READ_ONLY</strong></dt> <dt>(HRESULT)0x80AA0A00L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-127">Образ стал доступен только для чтения из-за вызова <a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-createresultimage"><strong>иравкдимажекреатор:: креатересултимаже</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1727f-127">The image has become read-only due to a call to <a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-createresultimage"><strong>IRawCDImageCreator::CreateResultImage</strong></a>.</span></span> <span data-ttu-id="1727f-128">В результате объект больше не может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="1727f-128">As a result the object can no longer be modified.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS"></span><span id="e_imapi_raw_image_too_many_tracks"></span><dl> <span data-ttu-id="1727f-129"><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS</strong></dt> <dt>(HRESULT) 0x80AA0A01L</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-129"><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS</strong></dt> <dt>(HRESULT)0x80AA0A01L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-130">Дополнительные записи добавляться не могут.</span><span class="sxs-lookup"><span data-stu-id="1727f-130">No more tracks may be added.</span></span> <span data-ttu-id="1727f-131">Диск CD ограничен диапазоном 1-99 дорожек.</span><span class="sxs-lookup"><span data-stu-id="1727f-131">CD media is restricted to a range of 1-99 tracks.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_NO_TRACKS"></span><span id="e_imapi_raw_image_no_tracks"></span><dl> <span data-ttu-id="1727f-132"><dt><strong>E_IMAPI_RAW_IMAGE_NO_TRACKS</strong></dt> <dt>(HRESULT) 0x80AA0A03L</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-132"><dt><strong>E_IMAPI_RAW_IMAGE_NO_TRACKS</strong></dt> <dt>(HRESULT)0x80AA0A03L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-133">Перед использованием этой функции необходимо добавить дорожки в образ.</span><span class="sxs-lookup"><span data-stu-id="1727f-133">Tracks must be added to the image before using this function.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_raw_image_sector_type_not_supported"></span><dl> <span data-ttu-id="1727f-134"><dt><strong>E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0x80AA0A02L</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-134"><dt><strong>E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0x80AA0A02L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-135">Запрошенный тип сектора не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1727f-135">The requested sector type is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED"></span><span id="e_imapi_raw_image_tracks_already_added"></span><dl> <span data-ttu-id="1727f-136"><dt><strong>E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED</strong></dt> <dt>(HRESULT) 0x80AA0A04L</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-136"><dt><strong>E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED</strong></dt> <dt>(HRESULT)0x80AA0A04L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-137">Записи не могут быть добавлены в образ перед использованием этой функции.</span><span class="sxs-lookup"><span data-stu-id="1727f-137">Tracks may not be added to the image prior to the use of this function.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE"></span><span id="e_imapi_raw_image_insufficient_space"></span><dl> <span data-ttu-id="1727f-138"><dt><strong>E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE</strong></dt> <dt>(HRESULT) 0x80AA0A05L</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-138"><dt><strong>E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE</strong></dt> <dt>(HRESULT)0x80AA0A05L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-139">Добавление этой записи приведет к превышению ограничений, накладываемых на начало интереса.</span><span class="sxs-lookup"><span data-stu-id="1727f-139">Adding this track would exceed the limitations of the start of the leadout.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES"></span><span id="e_imapi_raw_image_too_many_track_indexes"></span><dl> <span data-ttu-id="1727f-140"><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES</strong></dt> <dt>(HRESULT) 0x80AA0A06L</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-140"><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES</strong></dt> <dt>(HRESULT)0x80AA0A06L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-141">Добавление этой записи приведет к превышению предельного числа индексов 99.</span><span class="sxs-lookup"><span data-stu-id="1727f-141">Adding this track would exceed the 99 index limit.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND"></span><span id="e_imapi_raw_image_track_index_not_found"></span><dl> <span data-ttu-id="1727f-142"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND</strong></dt> <dt>(HRESULT) 0x80AA0A07L</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-142"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND</strong></dt> <dt>(HRESULT)0x80AA0A07L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-143">Указанное смещение LBA отсутствует в списке индексов Track.</span><span class="sxs-lookup"><span data-stu-id="1727f-143">The specified LBA offset is not in the list of track indexes.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS"></span><span id="s_imapi_raw_image_track_index_already_exists"></span><dl> <span data-ttu-id="1727f-144"><dt><strong>S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS</strong></dt> <dt>(HRESULT) 0x00AA0A08L</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-144"><dt><strong>S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS</strong></dt> <dt>(HRESULT)0x00AA0A08L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-145">Указанное смещение LBA уже находится в списке индексов Track.</span><span class="sxs-lookup"><span data-stu-id="1727f-145">The specified LBA offset is already in the list of track indexes.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED"></span><span id="e_imapi_raw_image_track_index_offset_zero_cannot_be_cleared"></span><dl> <span data-ttu-id="1727f-146"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED</strong></dt> <dt>(HRESULT) 0x80AA0A09L</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-146"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED</strong></dt> <dt>(HRESULT)0x80AA0A09L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-147">Индекс 1 (Нулевое смещение LBA) не может быть сброшен.</span><span class="sxs-lookup"><span data-stu-id="1727f-147">Index 1 (LBA offset zero) cannot be cleared.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX"></span><span id="e_imapi_raw_image_track_index_too_close_to_other_index"></span><dl> <span data-ttu-id="1727f-148"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX</strong></dt> <dt>(HRESULT) 0x80AA0A0AL</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-148"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX</strong></dt> <dt>(HRESULT)0x80AA0A0AL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-149">Размер каждого индекса должен быть не менее десяти секторов.</span><span class="sxs-lookup"><span data-stu-id="1727f-149">Each index must have a minimum size of ten sectors.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE"></span><span id="e_imapi_recorder_no_such_mode_page"></span><dl> <span data-ttu-id="1727f-150"><dt><strong>E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE</strong></dt> <dt>(HRESULT) 0xC0AA0201</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-150"><dt><strong>E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE</strong></dt> <dt>(HRESULT)0xC0AA0201</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-151">Устройство сообщило, что запрошенная страница режима (и тип) отсутствует.</span><span class="sxs-lookup"><span data-stu-id="1727f-151">The device reported that the requested mode page (and type) is not present.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_NO_MEDIA"></span><span id="e_imapi_recorder_media_no_media"></span><dl> <span data-ttu-id="1727f-152"><dt><strong>E_IMAPI_RECORDER_MEDIA_NO_MEDIA</strong></dt> <dt>(HRESULT) 0xC0AA0202</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-152"><dt><strong>E_IMAPI_RECORDER_MEDIA_NO_MEDIA</strong></dt> <dt>(HRESULT)0xC0AA0202</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-153">На устройстве нет носителя.</span><span class="sxs-lookup"><span data-stu-id="1727f-153">There is no media in the device.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE"></span><span id="e_imapi_recorder_media_incompatible"></span><dl> <span data-ttu-id="1727f-154"><dt><strong>E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE</strong></dt> <dt>(HRESULT) 0xC0AA0203</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-154"><dt><strong>E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE</strong></dt> <dt>(HRESULT)0xC0AA0203</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-155">Носитель несовместим или имеет неизвестный физический формат.</span><span class="sxs-lookup"><span data-stu-id="1727f-155">The media is not compatible or of unknown physical format.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN"></span><span id="e_imapi_recorder_media_upside_down"></span><dl> <span data-ttu-id="1727f-156"><dt><strong>E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN</strong></dt> <dt>(HRESULT) 0xC0AA0204</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-156"><dt><strong>E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN</strong></dt> <dt>(HRESULT)0xC0AA0204</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-157">Носитель вставляется вверх.</span><span class="sxs-lookup"><span data-stu-id="1727f-157">The media is inserted upside down.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_BECOMING_READY"></span><span id="e_imapi_recorder_media_becoming_ready"></span><dl> <span data-ttu-id="1727f-158"><dt><strong>E_IMAPI_RECORDER_MEDIA_BECOMING_READY</strong></dt> <dt>(HRESULT) 0xC0AA0205</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-158"><dt><strong>E_IMAPI_RECORDER_MEDIA_BECOMING_READY</strong></dt> <dt>(HRESULT)0xC0AA0205</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-159">Диск сообщил, что он находится в процессе подготовки.</span><span class="sxs-lookup"><span data-stu-id="1727f-159">The drive reported that it is in the process of becoming ready.</span></span> <span data-ttu-id="1727f-160">Повторите запрос позже.</span><span class="sxs-lookup"><span data-stu-id="1727f-160">Please try the request again later.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS"></span><span id="e_imapi_recorder_media_format_in_progress"></span><dl> <span data-ttu-id="1727f-161"><dt><strong>E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0206</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-161"><dt><strong>E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0206</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-162">Носитель форматируется в данный момент.</span><span class="sxs-lookup"><span data-stu-id="1727f-162">The media is currently being formatted.</span></span> <span data-ttu-id="1727f-163">Дождитесь завершения форматирования, прежде чем пытаться использовать носитель.</span><span class="sxs-lookup"><span data-stu-id="1727f-163">Please wait for the format to complete before attempting to use the media.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_BUSY"></span><span id="e_imapi_recorder_media_busy"></span><dl> <span data-ttu-id="1727f-164"><dt><strong>E_IMAPI_RECORDER_MEDIA_BUSY</strong></dt> <dt>(HRESULT) 0xC0AA0207</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-164"><dt><strong>E_IMAPI_RECORDER_MEDIA_BUSY</strong></dt> <dt>(HRESULT)0xC0AA0207</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-165">Диск сообщил о выполнении длительной операции, такой как завершение записи.</span><span class="sxs-lookup"><span data-stu-id="1727f-165">The drive reported that it is performing a long-running operation, such as finishing a write.</span></span> <span data-ttu-id="1727f-166">Диск может быть непригоден для длительного периода времени.</span><span class="sxs-lookup"><span data-stu-id="1727f-166">The drive may be unusable for a long period of time.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS"></span><span id="e_imapi_recorder_invalid_mode_parameters"></span><dl> <span data-ttu-id="1727f-167"><dt><strong>E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS</strong></dt> <dt>(HRESULT) 0xC0AA0208</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-167"><dt><strong>E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS</strong></dt> <dt>(HRESULT)0xC0AA0208</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-168">Диск сообщил, что сочетание параметров, указанных на странице режим для команды выбор режима, не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1727f-168">The drive reported that the combination of parameters provided in the mode page for a MODE SELECT command were not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED"></span><span id="e_imapi_recorder_media_write_protected"></span><dl> <span data-ttu-id="1727f-169"><dt><strong>E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED</strong></dt> <dt>(HRESULT) 0xC0AA0209</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-169"><dt><strong>E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED</strong></dt> <dt>(HRESULT)0xC0AA0209</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-170">Диск сообщил, что носитель защищен от записи.</span><span class="sxs-lookup"><span data-stu-id="1727f-170">The drive reported that the media is write protected.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_NO_SUCH_FEATURE"></span><span id="e_imapi_recorder_no_such_feature"></span><dl> <span data-ttu-id="1727f-171"><dt><strong>E_IMAPI_RECORDER_NO_SUCH_FEATURE</strong></dt> <dt>(HRESULT) 0xC0AA020A</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-171"><dt><strong>E_IMAPI_RECORDER_NO_SUCH_FEATURE</strong></dt> <dt>(HRESULT)0xC0AA020A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-172">Запрошенная страница функций не поддерживается устройством.</span><span class="sxs-lookup"><span data-stu-id="1727f-172">The feature page requested is not supported by the device.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT"></span><span id="e_imapi_recorder_feature_is_not_current"></span><dl> <span data-ttu-id="1727f-173"><dt><strong>E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT</strong></dt> <dt>(HRESULT) 0xC0AA020B</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-173"><dt><strong>E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT</strong></dt> <dt>(HRESULT)0xC0AA020B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-174">Запрошенная страница компонентов поддерживается, но не помечена как текущая.</span><span class="sxs-lookup"><span data-stu-id="1727f-174">The feature page requested is supported, but is not marked as current.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED"></span><span id="e_imapi_recorder_get_configuration_not_supported"></span><dl> <span data-ttu-id="1727f-175"><dt><strong>E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA020C</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-175"><dt><strong>E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA020C</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-176">Диск не поддерживает команду "получить конфигурацию".</span><span class="sxs-lookup"><span data-stu-id="1727f-176">The drive does not support the GET CONFIGURATION command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_COMMAND_TIMEOUT"></span><span id="e_imapi_recorder_command_timeout"></span><dl> <span data-ttu-id="1727f-177"><dt><strong>E_IMAPI_RECORDER_COMMAND_TIMEOUT</strong></dt> <dt>(HRESULT) 0xC0AA020D</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-177"><dt><strong>E_IMAPI_RECORDER_COMMAND_TIMEOUT</strong></dt> <dt>(HRESULT)0xC0AA020D</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-178">Устройству не удалось принять команду в течение периода ожидания.</span><span class="sxs-lookup"><span data-stu-id="1727f-178">The device failed to accept the command within the timeout period.</span></span> <span data-ttu-id="1727f-179">Это может быть вызвано тем, что устройство перешло в непротиворечивое состояние, или может потребоваться увеличить значение времени ожидания для команды.</span><span class="sxs-lookup"><span data-stu-id="1727f-179">This may be caused by the device having entered an inconsistent state, or the timeout value for the command may need to be increased.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT"></span><span id="e_imapi_recorder_dvd_structure_not_present"></span><dl> <span data-ttu-id="1727f-180"><dt><strong>E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT</strong></dt> <dt>(HRESULT) 0xC0AA020E</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-180"><dt><strong>E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT</strong></dt> <dt>(HRESULT)0xC0AA020E</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-181">Структура DVD отсутствует.</span><span class="sxs-lookup"><span data-stu-id="1727f-181">The DVD structure is not present.</span></span> <span data-ttu-id="1727f-182">Это может быть вызвано тем, что используется несовместимый диск или носитель.</span><span class="sxs-lookup"><span data-stu-id="1727f-182">This may be caused by incompatible drive/medium used.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH"></span><span id="e_imapi_recorder_media_speed_mismatch"></span><dl> <span data-ttu-id="1727f-183"><dt><strong>E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH</strong></dt> <dt>(HRESULT) 0xC0AA020F</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-183"><dt><strong>E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH</strong></dt> <dt>(HRESULT)0xC0AA020F</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-184">Скорость носителя несовместима с устройством.</span><span class="sxs-lookup"><span data-stu-id="1727f-184">The media's speed is incompatible with the device.</span></span> <span data-ttu-id="1727f-185">Это может быть вызвано использованием носителя с более высокой или низкой скоростью, чем диапазон поддерживаемых устройством частот.</span><span class="sxs-lookup"><span data-stu-id="1727f-185">This may be caused by using higher or lower speed media than the range of speeds supported by the device.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_LOCKED"></span><span id="e_imapi_recorder_locked"></span><dl> <span data-ttu-id="1727f-186"><dt><strong>E_IMAPI_RECORDER_LOCKED</strong></dt> <dt>(HRESULT) 0xC0AA0210</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-186"><dt><strong>E_IMAPI_RECORDER_LOCKED</strong></dt> <dt>(HRESULT)0xC0AA0210</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-187">Устройство, связанное с этим средством записи во время последней операции, заблокировано в монопольном режиме, что привело к сбою этой операции.</span><span class="sxs-lookup"><span data-stu-id="1727f-187">The device associated with this recorder during the last operation has been exclusively locked, causing this operation to fail.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_recorder_client_name_is_not_valid"></span><dl> <span data-ttu-id="1727f-188"><dt><strong>E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xC0AA0211</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-188"><dt><strong>E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA0211</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-189">Недопустимое имя клиента.</span><span class="sxs-lookup"><span data-stu-id="1727f-189">The client name is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_recorder_invalid_response_from_device"></span><dl> <span data-ttu-id="1727f-190"><dt><strong>E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE</strong></dt> <dt>(HRESULT) 0xC0AA02FF</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-190"><dt><strong>E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE</strong></dt> <dt>(HRESULT)0xC0AA02FF</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-191">Устройство сообщило о непредвиденных или недопустимых данных для команды.</span><span class="sxs-lookup"><span data-stu-id="1727f-191">The device reported unexpected or invalid data for a command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_LOSS_OF_STREAMING"></span><span id="e_imapi_loss_of_streaming"></span><dl> <span data-ttu-id="1727f-192"><dt><strong>E_IMAPI_LOSS_OF_STREAMING</strong></dt> <dt>(HRESULT) 0xC0AA0300</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-192"><dt><strong>E_IMAPI_LOSS_OF_STREAMING</strong></dt> <dt>(HRESULT)0xC0AA0300</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-193">Произошел сбой записи, так как диск не получал данные достаточно быстро для продолжения записи.</span><span class="sxs-lookup"><span data-stu-id="1727f-193">The write failed because the drive did not receive data quickly enough to continue writing.</span></span> <span data-ttu-id="1727f-194">Чтобы устранить эту проблему, переместите исходные данные на локальный компьютер, уменьшите скорость записи или включите &quot; параметр Free опустошения буфера &quot; .</span><span class="sxs-lookup"><span data-stu-id="1727f-194">Moving the source data to the local computer, reducing the write speed, or enabling a &quot;buffer underrun free&quot; setting may resolve this issue.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_unexpected_response_from_device"></span><dl> <span data-ttu-id="1727f-195"><dt><strong>E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE</strong></dt> <dt>(HRESULT) 0xC0AA0301</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-195"><dt><strong>E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE</strong></dt> <dt>(HRESULT)0xC0AA0301</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-196">Произошел сбой записи, так как диск вернул информацию об ошибке, которую не удалось восстановить из.</span><span class="sxs-lookup"><span data-stu-id="1727f-196">The write failed because the drive returned error information that could not be recovered from.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2data_write_in_progress"></span><dl> <span data-ttu-id="1727f-197"><dt><strong>E_IMAPI_DF2DATA_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0400</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-197"><dt><strong>E_IMAPI_DF2DATA_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0400</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-198">Сейчас выполняется операция записи.</span><span class="sxs-lookup"><span data-stu-id="1727f-198">There is currently a write operation in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2data_write_not_in_progress"></span><dl> <span data-ttu-id="1727f-199"><dt><strong>E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0401</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-199"><dt><strong>E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0401</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-200">Сейчас нет выполняющихся операций записи.</span><span class="sxs-lookup"><span data-stu-id="1727f-200">There is no write operation currently in progress.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_INVALID_MEDIA_STATE"></span><span id="e_imapi_df2data_invalid_media_state"></span><dl> <span data-ttu-id="1727f-201"><dt><strong>E_IMAPI_DF2DATA_INVALID_MEDIA_STATE</strong></dt> <dt>(HRESULT) 0xC0AA0402</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-201"><dt><strong>E_IMAPI_DF2DATA_INVALID_MEDIA_STATE</strong></dt> <dt>(HRESULT)0xC0AA0402</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-202">Запрошенная операция допустима только для поддерживаемых носителей.</span><span class="sxs-lookup"><span data-stu-id="1727f-202">The requested operation is only valid with supported media.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2data_stream_not_supported"></span><dl> <span data-ttu-id="1727f-203"><dt><strong>E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0403</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-203"><dt><strong>E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0403</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-204">Указанный поток для записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1727f-204">The provided stream to write is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA"></span><span id="e_imapi_df2data_stream_too_large_for_current_media"></span><dl> <span data-ttu-id="1727f-205"><dt><strong>E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA</strong></dt> <dt>(HRESULT) 0xC0AA0404</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-205"><dt><strong>E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA</strong></dt> <dt>(HRESULT)0xC0AA0404</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-206">Указанный поток для записи слишком велик для текущего вставленного носителя.</span><span class="sxs-lookup"><span data-stu-id="1727f-206">The provided stream to write is too large for the currently inserted media.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_MEDIA_NOT_BLANK"></span><span id="e_imapi_df2data_media_not_blank"></span><dl> <span data-ttu-id="1727f-207"><dt><strong>E_IMAPI_DF2DATA_MEDIA_NOT_BLANK</strong></dt> <dt>(HRESULT) 0xC0AA0405</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-207"><dt><strong>E_IMAPI_DF2DATA_MEDIA_NOT_BLANK</strong></dt> <dt>(HRESULT)0xC0AA0405</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-208">Перезапись непустого носителя не допускается, если для свойства Форцеоверврите не задано значение VARIANT_TRUE.</span><span class="sxs-lookup"><span data-stu-id="1727f-208">Overwriting non-blank media is not allowed without the ForceOverwrite property set to VARIANT_TRUE.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2data_media_is_not_supported"></span><dl> <span data-ttu-id="1727f-209"><dt><strong>E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0406</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-209"><dt><strong>E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0406</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-210">Текущий тип мультимедиа не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1727f-210">The current media type is unsupported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2data_recorder_not_supported"></span><dl> <span data-ttu-id="1727f-211"><dt><strong>E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0407</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-211"><dt><strong>E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0407</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-212">Это устройство не поддерживает операции, необходимые для этого формата диска.</span><span class="sxs-lookup"><span data-stu-id="1727f-212">This device does not support the operations required by this disc format.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2data_client_name_is_not_valid"></span><dl> <span data-ttu-id="1727f-213"><dt><strong>E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xC0AA0408</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-213"><dt><strong>E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA0408</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-214">Недопустимое имя клиента.</span><span class="sxs-lookup"><span data-stu-id="1727f-214">The client name is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_in_progress"></span><dl> <span data-ttu-id="1727f-215"><dt><strong>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0500</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-215"><dt><strong>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0500</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-216">Сейчас выполняется операция записи.</span><span class="sxs-lookup"><span data-stu-id="1727f-216">There is currently a write operation in progress.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_not_in_progress"></span><dl> <span data-ttu-id="1727f-217"><dt><strong>E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0501</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-217"><dt><strong>E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0501</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-218">Сейчас нет выполняющихся операций записи.</span><span class="sxs-lookup"><span data-stu-id="1727f-218">There is no write operation currently in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2tao_media_is_not_prepared"></span><dl> <span data-ttu-id="1727f-219"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED</strong></dt> <dt>(HRESULT) 0xC0AA0502</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-219"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED</strong></dt> <dt>(HRESULT)0xC0AA0502</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-220">Запрошенная операция допустима только после &quot; подготовки носителя &quot; .</span><span class="sxs-lookup"><span data-stu-id="1727f-220">The requested operation is only valid when media has been &quot;prepared&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2tao_media_is_prepared"></span><dl> <span data-ttu-id="1727f-221"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_PREPARED</strong></dt> <dt>(HRESULT) 0xC0AA0503</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-221"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_PREPARED</strong></dt> <dt>(HRESULT)0xC0AA0503</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-222">Запрошенная операция недопустима, если носитель &quot; подготовлен &quot; , но не был освобожден.</span><span class="sxs-lookup"><span data-stu-id="1727f-222">The requested operation is not valid when media has been &quot;prepared&quot; but not released.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY"></span><span id="e_imapi_df2tao_property_for_blank_media_only"></span><dl> <span data-ttu-id="1727f-223"><dt><strong>E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY</strong></dt> <dt>(HRESULT) 0xC0AA0504</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-223"><dt><strong>E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY</strong></dt> <dt>(HRESULT)0xC0AA0504</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-224">Свойство нельзя изменить после того, как носитель будет записан в.</span><span class="sxs-lookup"><span data-stu-id="1727f-224">The property cannot be changed once the media has been written to.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC"></span><span id="e_imapi_df2tao_table_of_contents_empty_disc"></span><dl> <span data-ttu-id="1727f-225"><dt><strong>E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC</strong></dt> <dt>(HRESULT) 0xC0AA0505</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-225"><dt><strong>E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC</strong></dt> <dt>(HRESULT)0xC0AA0505</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-226">Не удается получить оглавление с пустого диска.</span><span class="sxs-lookup"><span data-stu-id="1727f-226">The table of contents cannot be retrieved from an empty disc.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2tao_media_is_not_blank"></span><dl> <span data-ttu-id="1727f-227"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK</strong></dt> <dt>(HRESULT) 0xC0AA0506</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-227"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK</strong></dt> <dt>(HRESULT)0xC0AA0506</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-228">Поддерживается только чистый носитель CD-R/RW.</span><span class="sxs-lookup"><span data-stu-id="1727f-228">Only blank CD-R/RW media is supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_media_is_not_supported"></span><dl> <span data-ttu-id="1727f-229"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0507</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-229"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0507</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-230">Поддерживается только чистый носитель CD-R/RW.</span><span class="sxs-lookup"><span data-stu-id="1727f-230">Only blank CD-R/RW media is supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED"></span><span id="e_imapi_df2tao_track_limit_reached"></span><dl> <span data-ttu-id="1727f-231"><dt><strong>E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED</strong></dt> <dt>(HRESULT) 0xC0AA0508</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-231"><dt><strong>E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED</strong></dt> <dt>(HRESULT)0xC0AA0508</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-232">Носители CD-R и CD-RW поддерживают не более 99 звуковых дорожек.</span><span class="sxs-lookup"><span data-stu-id="1727f-232">CD-R and CD-RW media support a maximum of 99 audio tracks.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2tao_not_enough_space"></span><dl> <span data-ttu-id="1727f-233"><dt><strong>E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE</strong></dt> <dt>(HRESULT) 0xC0AA0509</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-233"><dt><strong>E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE</strong></dt> <dt>(HRESULT)0xC0AA0509</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-234">На носителе недостаточно места для добавления указанной звуковой дорожки.</span><span class="sxs-lookup"><span data-stu-id="1727f-234">There is not enough space left on the media to add the provided audio track.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2tao_no_recorder_specified"></span><dl> <span data-ttu-id="1727f-235"><dt><strong>E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED</strong></dt> <dt>(HRESULT) 0xC0AA050A</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-235"><dt><strong>E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED</strong></dt> <dt>(HRESULT)0xC0AA050A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-236">Вы не можете подготовить носитель, пока не выберите устройство записи.</span><span class="sxs-lookup"><span data-stu-id="1727f-236">You cannot prepare the media until you choose a recorder to use.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_INVALID_ISRC"></span><span id="e_imapi_df2tao_invalid_isrc"></span><dl> <span data-ttu-id="1727f-237"><dt><strong>E_IMAPI_DF2TAO_INVALID_ISRC</strong></dt> <dt>(HRESULT) 0xC0AA050B</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-237"><dt><strong>E_IMAPI_DF2TAO_INVALID_ISRC</strong></dt> <dt>(HRESULT)0xC0AA050B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-238">Указан недопустимый ИСРК.</span><span class="sxs-lookup"><span data-stu-id="1727f-238">The ISRC provided is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_INVALID_MCN"></span><span id="e_imapi_df2tao_invalid_mcn"></span><dl> <span data-ttu-id="1727f-239"><dt><strong>E_IMAPI_DF2TAO_INVALID_MCN</strong></dt> <dt>(HRESULT) 0xC0AA050C</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-239"><dt><strong>E_IMAPI_DF2TAO_INVALID_MCN</strong></dt> <dt>(HRESULT)0xC0AA050C</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-240">Указан недопустимый номер каталога носителей.</span><span class="sxs-lookup"><span data-stu-id="1727f-240">The Media Catalog Number provided is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_stream_not_supported"></span><dl> <span data-ttu-id="1727f-241"><dt><strong>E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA050D</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-241"><dt><strong>E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA050D</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-242">Указанный звуковой поток недопустим.</span><span class="sxs-lookup"><span data-stu-id="1727f-242">The provided audio stream is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_recorder_not_supported"></span><dl> <span data-ttu-id="1727f-243"><dt><strong>E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA050E</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-243"><dt><strong>E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA050E</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-244">Это устройство не поддерживает операции, необходимые для этого формата диска.</span><span class="sxs-lookup"><span data-stu-id="1727f-244">This device does not support the operations required by this disc format.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2tao_client_name_is_not_valid"></span><dl> <span data-ttu-id="1727f-245"><dt><strong>E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xC0AA050F</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-245"><dt><strong>E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA050F</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-246">Недопустимое имя клиента.</span><span class="sxs-lookup"><span data-stu-id="1727f-246">The client name is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_in_progress"></span><dl> <span data-ttu-id="1727f-247"><dt><strong>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0600</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-247"><dt><strong>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0600</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-248">Сейчас выполняется операция записи.</span><span class="sxs-lookup"><span data-stu-id="1727f-248">There is currently a write operation in progress.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_not_in_progress"></span><dl> <span data-ttu-id="1727f-249"><dt><strong>E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xC0AA0601</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-249"><dt><strong>E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0601</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-250">Сейчас нет выполняющихся операций записи.</span><span class="sxs-lookup"><span data-stu-id="1727f-250">There is no write operation currently in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2raw_media_is_not_prepared"></span><dl> <span data-ttu-id="1727f-251"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</strong></dt> <dt>(HRESULT) 0xC0AA0602</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-251"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</strong></dt> <dt>(HRESULT)0xC0AA0602</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-252">Запрошенная операция допустима только после &quot; подготовки носителя &quot; .</span><span class="sxs-lookup"><span data-stu-id="1727f-252">The requested operation is only valid when media has been &quot;prepared&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2raw_media_is_prepared"></span><dl> <span data-ttu-id="1727f-253"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_PREPARED</strong></dt> <dt>(HRESULT) 0xC0AA0603</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-253"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_PREPARED</strong></dt> <dt>(HRESULT)0xC0AA0603</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-254">Запрошенная операция недопустима, если носитель &quot; подготовлен &quot; , но не был освобожден.</span><span class="sxs-lookup"><span data-stu-id="1727f-254">The requested operation is not valid when media has been &quot;prepared&quot; but not released.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2raw_client_name_is_not_valid"></span><dl> <span data-ttu-id="1727f-255"><dt><strong>E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xC0AA0604</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-255"><dt><strong>E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA0604</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-256">Недопустимое имя клиента.</span><span class="sxs-lookup"><span data-stu-id="1727f-256">The client name is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2raw_media_is_not_blank"></span><dl> <span data-ttu-id="1727f-257"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK</strong></dt> <dt>(HRESULT) 0xC0AA0606</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-257"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK</strong></dt> <dt>(HRESULT)0xC0AA0606</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-258">Поддерживается только чистый носитель CD-R/RW.</span><span class="sxs-lookup"><span data-stu-id="1727f-258">Only blank CD-R/RW media is supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_media_is_not_supported"></span><dl> <span data-ttu-id="1727f-259"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0607</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-259"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0607</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-260">Поддерживается только чистый носитель CD-R/RW.</span><span class="sxs-lookup"><span data-stu-id="1727f-260">Only blank CD-R/RW media is supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2raw_not_enough_space"></span><dl> <span data-ttu-id="1727f-261"><dt><strong>E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE</strong></dt> <dt>(HRESULT) 0xC0AA0609</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-261"><dt><strong>E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE</strong></dt> <dt>(HRESULT)0xC0AA0609</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-262">Недостаточно места на носителе для добавления указанного сеанса.</span><span class="sxs-lookup"><span data-stu-id="1727f-262">There is not enough space on the media to add the provided session.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2raw_no_recorder_specified"></span><dl> <span data-ttu-id="1727f-263"><dt><strong>E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED</strong></dt> <dt>(HRESULT) 0xC0AA060A</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-263"><dt><strong>E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED</strong></dt> <dt>(HRESULT)0xC0AA060A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-264">Вы не можете подготовить носитель, пока не выберите устройство записи.</span><span class="sxs-lookup"><span data-stu-id="1727f-264">You cannot prepare the media until you choose a recorder to use.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_stream_not_supported"></span><dl> <span data-ttu-id="1727f-265"><dt><strong>E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA060D</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-265"><dt><strong>E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA060D</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-266">Указанный звуковой поток недопустим.</span><span class="sxs-lookup"><span data-stu-id="1727f-266">The provided audio stream is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_data_block_type_not_supported"></span><dl> <span data-ttu-id="1727f-267"><dt><strong>E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA060E</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-267"><dt><strong>E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA060E</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-268">Запрошенный тип блока данных не поддерживается текущим устройством.</span><span class="sxs-lookup"><span data-stu-id="1727f-268">The requested data block type is not supported by the current device.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT"></span><span id="e_imapi_df2raw_stream_leadin_too_short"></span><dl> <span data-ttu-id="1727f-269"><dt><strong>E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT</strong></dt> <dt>(HRESULT) 0xC0AA060F</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-269"><dt><strong>E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT</strong></dt> <dt>(HRESULT)0xC0AA060F</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-270">Поток не содержит достаточного количества секторов для текущего носителя.</span><span class="sxs-lookup"><span data-stu-id="1727f-270">The stream does not contain a sufficient number of sectors in the leadin for the current media.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_recorder_not_supported"></span><dl> <span data-ttu-id="1727f-271"><dt><strong>E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0610</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-271"><dt><strong>E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0610</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-272">Это устройство не поддерживает операции, необходимые для этого формата диска.</span><span class="sxs-lookup"><span data-stu-id="1727f-272">This device does not support the operations required by this disc format.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_RECORDER_IN_USE"></span><span id="e_imapi_erase_recorder_in_use"></span><dl> <span data-ttu-id="1727f-273"><dt><strong>E_IMAPI_ERASE_RECORDER_IN_USE</strong></dt> <dt>(HRESULT) 0x80AA0900</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-273"><dt><strong>E_IMAPI_ERASE_RECORDER_IN_USE</strong></dt> <dt>(HRESULT)0x80AA0900</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-274">В данный момент формат использует устройство записи дисков для операции стирания.</span><span class="sxs-lookup"><span data-stu-id="1727f-274">The format is currently using the disc recorder for an erase operation.</span></span> <span data-ttu-id="1727f-275">Дождитесь завершения стирания, прежде чем пытаться установить или очистить текущий записывающий диск.</span><span class="sxs-lookup"><span data-stu-id="1727f-275">Please wait for the erase to complete before attempting to set or clear the current disc recorder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED"></span><span id="e_imapi_erase_only_one_recorder_supported"></span><dl> <span data-ttu-id="1727f-276"><dt><strong>E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED</strong></dt> <dt>(HRESULT) 0x80AA0901</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-276"><dt><strong>E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED</strong></dt> <dt>(HRESULT)0x80AA0901</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-277">Формат стирания поддерживает только один инструмент записи.</span><span class="sxs-lookup"><span data-stu-id="1727f-277">The erase format only supports one recorder.</span></span> <span data-ttu-id="1727f-278">Перед установкой нового параметра необходимо очистить текущее средство записи.</span><span class="sxs-lookup"><span data-stu-id="1727f-278">You must clear the current recorder before setting a new one.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL"></span><span id="e_imapi_erase_disc_information_too_small"></span><dl> <span data-ttu-id="1727f-279"><dt><strong>E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL</strong></dt> <dt>(HRESULT) 0x80AA0902</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-279"><dt><strong>E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL</strong></dt> <dt>(HRESULT)0x80AA0902</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-280">Диск не сообщает о достаточном объеме данных для команды READ CD INFORMATION.</span><span class="sxs-lookup"><span data-stu-id="1727f-280">The drive did not report sufficient data for a READ DISC INFORMATION command.</span></span> <span data-ttu-id="1727f-281">Возможно, диск не поддерживается или носитель неправилен.</span><span class="sxs-lookup"><span data-stu-id="1727f-281">The drive may not be supported, or the media may not be correct.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL"></span><span id="e_imapi_erase_mode_page_2a_too_small"></span><dl> <span data-ttu-id="1727f-282"><dt><strong>E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL</strong></dt> <dt>(HRESULT) 0x80AA0903</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-282"><dt><strong>E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL</strong></dt> <dt>(HRESULT)0x80AA0903</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-283">Диск не сообщает достаточные данные для команды режима MODE (страница 0x2A).</span><span class="sxs-lookup"><span data-stu-id="1727f-283">The drive did not report sufficient data for a MODE SENSE (page 0x2A) command.</span></span> <span data-ttu-id="1727f-284">Возможно, диск не поддерживается или носитель неправилен.</span><span class="sxs-lookup"><span data-stu-id="1727f-284">The drive may not be supported, or the media may not be correct.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE"></span><span id="e_imapi_erase_media_is_not_erasable"></span><dl> <span data-ttu-id="1727f-285"><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE</strong></dt> <dt>(HRESULT) 0x80AA0904</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-285"><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE</strong></dt> <dt>(HRESULT)0x80AA0904</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-286">Диск сообщил, что носитель не может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="1727f-286">The drive reported that the media is not erasable.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND"></span><span id="e_imapi_erase_drive_failed_erase_command"></span><dl> <span data-ttu-id="1727f-287"><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND</strong></dt> <dt>(HRESULT) 0x80AA0905</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-287"><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND</strong></dt> <dt>(HRESULT)0x80AA0905</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-288">Диск не прошел команду стирания.</span><span class="sxs-lookup"><span data-stu-id="1727f-288">The drive failed the erase command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR"></span><span id="e_imapi_erase_took_longer_than_one_hour"></span><dl> <span data-ttu-id="1727f-289"><dt><strong>E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR</strong></dt> <dt>(HRESULT) 0x80AA0906</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-289"><dt><strong>E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR</strong></dt> <dt>(HRESULT)0x80AA0906</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-290">Диск не выполнил стирание за один час.</span><span class="sxs-lookup"><span data-stu-id="1727f-290">The drive did not complete the erase in one hour.</span></span> <span data-ttu-id="1727f-291">Для возобновления работы диска может потребоваться цикл электропитания, удаление носителя или другое вмешательство вручную.</span><span class="sxs-lookup"><span data-stu-id="1727f-291">The drive may require a power cycle, media removal, or other manual intervention to resume proper operation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1727f-292">В настоящее время это значение также будет возвращаться, если попытка выполнить операцию стирания на носителе CD-RW или DVD-RW с помощью интерфейса <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a> завершается неудачей в результате неправильного носителя.</span><span class="sxs-lookup"><span data-stu-id="1727f-292">Currently, this value will also be returned if an attempt to perform an erase on CD-RW or DVD-RW media via the <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a> interface fails as a result of the media being bad.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE"></span><span id="e_imapi_erase_unexpected_drive_response_during_erase"></span><dl> <span data-ttu-id="1727f-293"><dt><strong>E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE</strong></dt> <dt>(HRESULT) 0x80AA0907</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-293"><dt><strong>E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE</strong></dt> <dt>(HRESULT)0x80AA0907</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-294">Диск вернул непредвиденную ошибку во время стирания.</span><span class="sxs-lookup"><span data-stu-id="1727f-294">The drive returned an unexpected error during the erase.</span></span> <span data-ttu-id="1727f-295">Возможно, носитель непригоден для использования, стирание может быть завершено, или диск по-прежнему находится в процессе стирания диска.</span><span class="sxs-lookup"><span data-stu-id="1727f-295">The media may be unusable, the erase may be complete, or the drive may still be in the process of erasing the disc.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND"></span><span id="e_imapi_erase_drive_failed_spinup_command"></span><dl> <span data-ttu-id="1727f-296"><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND</strong></dt> <dt>(HRESULT) 0x80AA0908</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-296"><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND</strong></dt> <dt>(HRESULT)0x80AA0908</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-297">Диск возвратил ошибку для команды начального блока (спинуп).</span><span class="sxs-lookup"><span data-stu-id="1727f-297">The drive returned an error for a START UNIT (spinup) command.</span></span> <span data-ttu-id="1727f-298">Может потребоваться вмешательство вручную.</span><span class="sxs-lookup"><span data-stu-id="1727f-298">Manual intervention may be required.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_erase_media_is_not_supported"></span><dl> <span data-ttu-id="1727f-299"><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA0909</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-299"><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0909</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-300">Текущий тип мультимедиа не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1727f-300">The current media type is unsupported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_erase_recorder_not_supported"></span><dl> <span data-ttu-id="1727f-301"><dt><strong>E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AA090A</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-301"><dt><strong>E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA090A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-302">Это устройство не поддерживает операции, необходимые для этого формата диска.</span><span class="sxs-lookup"><span data-stu-id="1727f-302">This device does not support the operations required by this disc format.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_erase_client_name_is_not_valid"></span><dl> <span data-ttu-id="1727f-303"><dt><strong>E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xC0AA090B</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-303"><dt><strong>E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA090B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-304">Недопустимое имя клиента.</span><span class="sxs-lookup"><span data-stu-id="1727f-304">The client name is not valid.</span></span><br/></td>
</tr>
</tbody>
</table>



<span data-ttu-id="1727f-305">Следующие коды успеха и ошибки определены в Imapi2fserror. h.</span><span class="sxs-lookup"><span data-stu-id="1727f-305">The following success and error codes are defined in Imapi2fserror.h.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="1727f-306">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="1727f-306">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="1727f-307">Описание</span><span class="sxs-lookup"><span data-stu-id="1727f-307">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FSI_INTERNAL_ERROR"></span><span id="imapi_e_fsi_internal_error"></span><dl> <span data-ttu-id="1727f-308"><dt><strong>IMAPI_E_FSI_INTERNAL_ERROR</strong></dt> <dt>(HRESULT) 0xC0AAB100</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-308"><dt><strong>IMAPI_E_FSI_INTERNAL_ERROR</strong></dt> <dt>(HRESULT)0xC0AAB100</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-309">Произошла внутренняя ошибка: %1! ls!.</span><span class="sxs-lookup"><span data-stu-id="1727f-309">Internal error occurred: %1!ls!.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_PARAM"></span><span id="imapi_e_invalid_param"></span><dl> <span data-ttu-id="1727f-310"><dt><strong>IMAPI_E_INVALID_PARAM</strong></dt> <dt>(HRESULT) 0xC0AAB101</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-310"><dt><strong>IMAPI_E_INVALID_PARAM</strong></dt> <dt>(HRESULT)0xC0AAB101</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-311">Значение, указанное для параметра "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="1727f-311">The value specified for parameter '%1!ls!'</span></span> <span data-ttu-id="1727f-312">, недопустим.</span><span class="sxs-lookup"><span data-stu-id="1727f-312">is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_READONLY"></span><span id="imapi_e_readonly"></span><dl> <span data-ttu-id="1727f-313"><dt><strong>IMAPI_E_READONLY</strong></dt> <dt>(HRESULT) 0xC0AAB102</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-313"><dt><strong>IMAPI_E_READONLY</strong></dt> <dt>(HRESULT)0xC0AAB102</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-314">Объект Филесистемимаже находится в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1727f-314">FileSystemImage object is in read only mode.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_OUTPUT"></span><span id="imapi_e_no_output"></span><dl> <span data-ttu-id="1727f-315"><dt><strong>IMAPI_E_NO_OUTPUT</strong></dt> <dt>(HRESULT) 0xC0AAB103</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-315"><dt><strong>IMAPI_E_NO_OUTPUT</strong></dt> <dt>(HRESULT)0xC0AAB103</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-316">Не указана выходная файловая система.</span><span class="sxs-lookup"><span data-stu-id="1727f-316">No output file system specified.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_VOLUME_NAME"></span><span id="imapi_e_invalid_volume_name"></span><dl> <span data-ttu-id="1727f-317"><dt><strong>IMAPI_E_INVALID_VOLUME_NAME</strong></dt> <dt>(HRESULT) 0xC0AAB104</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-317"><dt><strong>IMAPI_E_INVALID_VOLUME_NAME</strong></dt> <dt>(HRESULT)0xC0AAB104</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-318">Указанный идентификатор тома либо слишком длинный, либо содержит один или несколько недопустимых символов.</span><span class="sxs-lookup"><span data-stu-id="1727f-318">The specified Volume Identifier is either too long or contains one or more invalid characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_DATE"></span><span id="imapi_e_invalid_date"></span><dl> <span data-ttu-id="1727f-319"><dt><strong>IMAPI_E_INVALID_DATE</strong></dt> <dt>(HRESULT) 0xC0AAB105</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-319"><dt><strong>IMAPI_E_INVALID_DATE</strong></dt> <dt>(HRESULT)0xC0AAB105</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-320">Недопустимые даты файла.</span><span class="sxs-lookup"><span data-stu-id="1727f-320">Invalid file dates.</span></span> <span data-ttu-id="1727f-321">%1! Ls!</span><span class="sxs-lookup"><span data-stu-id="1727f-321">%1!ls!</span></span> <span data-ttu-id="1727f-322">время раньше, чем %2! Ls!</span><span class="sxs-lookup"><span data-stu-id="1727f-322">time is earlier than %2!ls!</span></span> <span data-ttu-id="1727f-323">времени.</span><span class="sxs-lookup"><span data-stu-id="1727f-323">time.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_NOT_EMPTY"></span><span id="imapi_e_file_system_not_empty"></span><dl> <span data-ttu-id="1727f-324"><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_EMPTY</strong></dt> <dt>(HRESULT) 0xC0AAB106</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-324"><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_EMPTY</strong></dt> <dt>(HRESULT)0xC0AAB106</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-325">Для этой функции файловая система должна быть пустой.</span><span class="sxs-lookup"><span data-stu-id="1727f-325">The file system must be empty for this function.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED"></span><span id="imapi_e_file_system_change_not_allowed"></span><dl> <span data-ttu-id="1727f-326"><dt><strong>IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED</strong></dt> <dt>(HRESULT) 0xC0AAB163L</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-326"><dt><strong>IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED</strong></dt> <dt>(HRESULT)0xC0AAB163L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-327">Невозможно изменить файловую систему, указанную для создания, так как файловая система из импортированного сеанса и файловая система в текущем сеансе не совпадают.</span><span class="sxs-lookup"><span data-stu-id="1727f-327">You cannot change the file system specified for creation, because the file system from the imported session and the file system in the current session do not match.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_NOT_FILE"></span><span id="imapi_e_not_file"></span><dl> <span data-ttu-id="1727f-328"><dt><strong>IMAPI_E_NOT_FILE</strong></dt> <dt>(HRESULT) 0xC0AAB108</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-328"><dt><strong>IMAPI_E_NOT_FILE</strong></dt> <dt>(HRESULT)0xC0AAB108</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-329">Указанный путь "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="1727f-329">Specified path '%1!ls!'</span></span> <span data-ttu-id="1727f-330">не определяет файл.</span><span class="sxs-lookup"><span data-stu-id="1727f-330">does not identify a file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NOT_DIR"></span><span id="imapi_e_not_dir"></span><dl> <span data-ttu-id="1727f-331"><dt><strong>IMAPI_E_NOT_DIR</strong></dt> <dt>(HRESULT) 0xC0AAB109</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-331"><dt><strong>IMAPI_E_NOT_DIR</strong></dt> <dt>(HRESULT)0xC0AAB109</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-332">Указанный путь "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="1727f-332">Specified path '%1!ls!'</span></span> <span data-ttu-id="1727f-333">не определяет каталог.</span><span class="sxs-lookup"><span data-stu-id="1727f-333">does not identify a directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DIR_NOT_EMPTY"></span><span id="imapi_e_dir_not_empty"></span><dl> <span data-ttu-id="1727f-334"><dt><strong>IMAPI_E_DIR_NOT_EMPTY</strong></dt> <dt>(HRESULT) 0xC0AAB10A</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-334"><dt><strong>IMAPI_E_DIR_NOT_EMPTY</strong></dt> <dt>(HRESULT)0xC0AAB10A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-335">Каталог "%1! s!"</span><span class="sxs-lookup"><span data-stu-id="1727f-335">The directory '%1!s!'</span></span> <span data-ttu-id="1727f-336">не пусто.</span><span class="sxs-lookup"><span data-stu-id="1727f-336">is not empty.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NOT_IN_FILE_SYSTEM"></span><span id="imapi_e_not_in_file_system"></span><dl> <span data-ttu-id="1727f-337"><dt><strong>IMAPI_E_NOT_IN_FILE_SYSTEM</strong></dt> <dt>(HRESULT) 0xC0AAB10B</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-337"><dt><strong>IMAPI_E_NOT_IN_FILE_SYSTEM</strong></dt> <dt>(HRESULT)0xC0AAB10B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-338">ls! '</span><span class="sxs-lookup"><span data-stu-id="1727f-338">ls!'</span></span> <span data-ttu-id="1727f-339">не является частью файловой системы.</span><span class="sxs-lookup"><span data-stu-id="1727f-339">is not part of the file system.</span></span> <span data-ttu-id="1727f-340">Для завершения этой операции необходимо добавить его.</span><span class="sxs-lookup"><span data-stu-id="1727f-340">It must be added to complete this operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_PATH"></span><span id="imapi_e_invalid_path"></span><dl> <span data-ttu-id="1727f-341"><dt><strong>IMAPI_E_INVALID_PATH</strong></dt> <dt>(HRESULT) 0xC0AAB110</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-341"><dt><strong>IMAPI_E_INVALID_PATH</strong></dt> <dt>(HRESULT)0xC0AAB110</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-342">Путь "%1! s!"</span><span class="sxs-lookup"><span data-stu-id="1727f-342">Path '%1!s!'</span></span> <span data-ttu-id="1727f-343">имеет неправильный формат или содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="1727f-343">is badly formed or contains invalid characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_RESTRICTED_NAME_VIOLATION"></span><span id="imapi_e_restricted_name_violation"></span><dl> <span data-ttu-id="1727f-344"><dt><strong>IMAPI_E_RESTRICTED_NAME_VIOLATION</strong></dt> <dt>(HRESULT) 0xC0AAB111</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-344"><dt><strong>IMAPI_E_RESTRICTED_NAME_VIOLATION</strong></dt> <dt>(HRESULT)0xC0AAB111</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-345">Имя "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="1727f-345">The name '%1!ls!'</span></span> <span data-ttu-id="1727f-346">указан недопустимый: имя объекта файла или каталога, созданного при задании свойства Усерестриктедчарактерсет, может содержать только символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="1727f-346">specified is not legal: Name of file or directory object created while the UseRestrictedCharacterSet property is set may only contain ANSI characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DUP_NAME"></span><span id="imapi_e_dup_name"></span><dl> <span data-ttu-id="1727f-347"><dt><strong>IMAPI_E_DUP_NAME</strong></dt> <dt>(HRESULT) 0xC0AAB112</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-347"><dt><strong>IMAPI_E_DUP_NAME</strong></dt> <dt>(HRESULT)0xC0AAB112</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-348">ls! '</span><span class="sxs-lookup"><span data-stu-id="1727f-348">ls!'</span></span> <span data-ttu-id="1727f-349">имя уже существует.</span><span class="sxs-lookup"><span data-stu-id="1727f-349">name already exists.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_UNIQUE_NAME"></span><span id="imapi_e_no_unique_name"></span><dl> <span data-ttu-id="1727f-350"><dt><strong>IMAPI_E_NO_UNIQUE_NAME</strong></dt> <dt>(HRESULT) 0xC0AAB113</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-350"><dt><strong>IMAPI_E_NO_UNIQUE_NAME</strong></dt> <dt>(HRESULT)0xC0AAB113</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-351">Попытка добавить "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="1727f-351">Attempt to add '%1!ls!'</span></span> <span data-ttu-id="1727f-352">Сбой: не удается создать уникальное имя для файловой системы для %2! Ls!</span><span class="sxs-lookup"><span data-stu-id="1727f-352">failed: cannot create a file-system-specific unique name for the %2!ls!</span></span> <span data-ttu-id="1727f-353">.</span><span class="sxs-lookup"><span data-stu-id="1727f-353">file system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_ITEM_NOT_FOUND"></span><span id="imapi_e_item_not_found"></span><dl> <span data-ttu-id="1727f-354"><dt><strong>IMAPI_E_ITEM_NOT_FOUND</strong></dt> <dt>(HRESULT) 0xC0AAB118</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-354"><dt><strong>IMAPI_E_ITEM_NOT_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB118</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-355">Не удается найти элемент "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="1727f-355">Cannot find item '%1!ls!'</span></span> <span data-ttu-id="1727f-356">в иерархии Филесистемимаже.</span><span class="sxs-lookup"><span data-stu-id="1727f-356">in FileSystemImage hierarchy.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_FILE_NOT_FOUND"></span><span id="imapi_e_file_not_found"></span><dl> <span data-ttu-id="1727f-357"><dt><strong>IMAPI_E_FILE_NOT_FOUND</strong></dt> <dt>(HRESULT) 0xC0AAB119</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-357"><dt><strong>IMAPI_E_FILE_NOT_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB119</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-358">Файл "%1! s!"</span><span class="sxs-lookup"><span data-stu-id="1727f-358">The file '%1!s!'</span></span> <span data-ttu-id="1727f-359">не найдено в иерархии Филесистемимаже.</span><span class="sxs-lookup"><span data-stu-id="1727f-359">not found in FileSystemImage hierarchy.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DIR_NOT_FOUND"></span><span id="imapi_e_dir_not_found"></span><dl> <span data-ttu-id="1727f-360"><dt><strong>IMAPI_E_DIR_NOT_FOUND</strong></dt> <dt>(HRESULT) 0xC0AAB11A</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-360"><dt><strong>IMAPI_E_DIR_NOT_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB11A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-361">Каталог "%1! s!"</span><span class="sxs-lookup"><span data-stu-id="1727f-361">The directory '%1!s!'</span></span> <span data-ttu-id="1727f-362">не найдено в иерархии Филесистемимаже.</span><span class="sxs-lookup"><span data-stu-id="1727f-362">not found in FileSystemImage hierarchy.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMAGE_SIZE_LIMIT"></span><span id="imapi_e_image_size_limit"></span><dl> <span data-ttu-id="1727f-363"><dt><strong>IMAPI_E_IMAGE_SIZE_LIMIT</strong></dt> <dt>(HRESULT) 0xC0AAB120</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-363"><dt><strong>IMAPI_E_IMAGE_SIZE_LIMIT</strong></dt> <dt>(HRESULT)0xC0AAB120</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-364">Добавление "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="1727f-364">Adding '%1!ls!'</span></span> <span data-ttu-id="1727f-365">приведет к тому, что размер изображения будет больше, чем текущее заданное ограничение.</span><span class="sxs-lookup"><span data-stu-id="1727f-365">would result in a result image having a size larger than the current configured limit.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMAGE_TOO_BIG"></span><span id="imapi_e_image_too_big"></span><dl> <span data-ttu-id="1727f-366"><dt><strong>IMAPI_E_IMAGE_TOO_BIG</strong></dt> <dt>(HRESULT) 0xC0AAB121</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-366"><dt><strong>IMAPI_E_IMAGE_TOO_BIG</strong></dt> <dt>(HRESULT)0xC0AAB121</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-367">Значение, указанное для свойства Фримедиаблоккс, слишком мало для предполагаемого размера изображения на основе текущих данных.</span><span class="sxs-lookup"><span data-stu-id="1727f-367">Value specified for FreeMediaBlocks property is too small for estimated image size based on current data.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED"></span><span id="imapi_e_imagemanager_image_not_aligned"></span><dl> <span data-ttu-id="1727f-368"><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED</strong></dt> <dt>(HRESULT) 0xC0AAB200L</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-368"><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED</strong></dt> <dt>(HRESULT)0xC0AAB200L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-369">Изображение не согласуется на границе сектора 2 КБ.</span><span class="sxs-lookup"><span data-stu-id="1727f-369">The image is not aligned on a 2kb sector boundary.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND"></span><span id="imapi_e_imagemanager_no_valid_vd_found"></span><dl> <span data-ttu-id="1727f-370"><dt><strong>IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND</strong></dt> <dt>(HRESULT) 0xC0AAB201L)</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-370"><dt><strong>IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB201L)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-371">Образ не содержит допустимый дескриптор тома.</span><span class="sxs-lookup"><span data-stu-id="1727f-371">The image does not contain a valid volume descriptor.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_NO_IMAGE"></span><span id="imapi_e_imagemanager_no_image"></span><dl> <span data-ttu-id="1727f-372"><dt><strong>IMAPI_E_IMAGEMANAGER_NO_IMAGE</strong></dt> <dt>(HRESULT) 0xC0AAB202L</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-372"><dt><strong>IMAPI_E_IMAGEMANAGER_NO_IMAGE</strong></dt> <dt>(HRESULT)0xC0AAB202L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-373">Образ не был задан с помощью методов <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath"><strong>иисоимажеманажер:: сетпас</strong></a> или <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream"><strong>Иисоимажеманажер:: сетстреам</strong></a> до вызова метода <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-validate"><strong>иисоимажеманажер:: Validate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1727f-373">The image has not been set using the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath"><strong>IIsoImageManager::SetPath</strong></a> or <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream"><strong>IIsoImageManager::SetStream</strong></a> methods prior to calling the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-validate"><strong>IIsoImageManager::Validate</strong></a> method.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG"></span><span id="imapi_e_imagemanager_image_too_big"></span><dl> <span data-ttu-id="1727f-374"><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG</strong></dt> <dt>(HRESULT) 0xC0AAB203L</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-374"><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG</strong></dt> <dt>(HRESULT)0xC0AAB203L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-375">Указанный образ слишком велик для проверки, так как размер превышает <strong>макслонг</strong>.</span><span class="sxs-lookup"><span data-stu-id="1727f-375">The provided image is too large to be validated as the size exceeds <strong>MAXLONG</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_DATA_STREAM_INCONSISTENCY"></span><span id="imapi_e_data_stream_inconsistency"></span><dl> <span data-ttu-id="1727f-376"><dt><strong>IMAPI_E_DATA_STREAM_INCONSISTENCY</strong></dt> <dt>(HRESULT) 0xC0AAB128</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-376"><dt><strong>IMAPI_E_DATA_STREAM_INCONSISTENCY</strong></dt> <dt>(HRESULT)0xC0AAB128</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-377">Поток данных, указанный для файла "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="1727f-377">Data stream supplied for file '%1!ls!'</span></span> <span data-ttu-id="1727f-378">не согласуется: ожидается %2! I64d!</span><span class="sxs-lookup"><span data-stu-id="1727f-378">is inconsistent: expected %2!I64d!</span></span> <span data-ttu-id="1727f-379">байт, Найдено %3! I64d!.</span><span class="sxs-lookup"><span data-stu-id="1727f-379">bytes, found %3!I64d!.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DATA_STREAM_READ_FAILURE"></span><span id="imapi_e_data_stream_read_failure"></span><dl> <span data-ttu-id="1727f-380"><dt><strong>IMAPI_E_DATA_STREAM_READ_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB129</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-380"><dt><strong>IMAPI_E_DATA_STREAM_READ_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB129</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-381">Не удается считать данные из потока, переданного для файла "%1! ls!".</span><span class="sxs-lookup"><span data-stu-id="1727f-381">Cannot read data from stream supplied for file '%1!ls!'.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_DATA_STREAM_CREATE_FAILURE"></span><span id="imapi_e_data_stream_create_failure"></span><dl> <span data-ttu-id="1727f-382"><dt><strong>IMAPI_E_DATA_STREAM_CREATE_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB12A</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-382"><dt><strong>IMAPI_E_DATA_STREAM_CREATE_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB12A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-383">При попытке создать поток данных для файла "%1! ls!" произошла следующая ошибка:</span><span class="sxs-lookup"><span data-stu-id="1727f-383">The following error was encountered when trying to create data stream for file '%1!ls!':</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DIRECTORY_READ_FAILURE"></span><span id="imapi_e_directory_read_failure"></span><dl> <span data-ttu-id="1727f-384"><dt><strong>IMAPI_E_DIRECTORY_READ_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB12BL</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-384"><dt><strong>IMAPI_E_DIRECTORY_READ_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB12BL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-385">Не удалось перечислить файлы в дереве каталогов из-за наличия разрешений.</span><span class="sxs-lookup"><span data-stu-id="1727f-385">Failure enumerating files in the directory tree is inaccessible due to permissions.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_TOO_MANY_DIRS"></span><span id="imapi_e_too_many_dirs"></span><dl> <span data-ttu-id="1727f-386"><dt><strong>IMAPI_E_TOO_MANY_DIRS</strong></dt> <dt>(HRESULT) 0xC0AAB130</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-386"><dt><strong>IMAPI_E_TOO_MANY_DIRS</strong></dt> <dt>(HRESULT)0xC0AAB130</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-387">Этот образ файловой системы имеет слишком много каталогов для %1! Ls!</span><span class="sxs-lookup"><span data-stu-id="1727f-387">This file system image has too many directories for the %1!ls!</span></span> <span data-ttu-id="1727f-388">.</span><span class="sxs-lookup"><span data-stu-id="1727f-388">file system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_ISO9660_LEVELS"></span><span id="imapi_e_iso9660_levels"></span><dl> <span data-ttu-id="1727f-389"><dt><strong>IMAPI_E_ISO9660_LEVELS</strong></dt> <dt>(HRESULT) 0xC0AAB131</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-389"><dt><strong>IMAPI_E_ISO9660_LEVELS</strong></dt> <dt>(HRESULT)0xC0AAB131</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-390">ISO9660 ограничено 8 уровнями каталогов.</span><span class="sxs-lookup"><span data-stu-id="1727f-390">ISO9660 is limited to 8 levels of directories.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_DATA_TOO_BIG"></span><span id="imapi_e_data_too_big"></span><dl> <span data-ttu-id="1727f-391"><dt><strong>IMAPI_E_DATA_TOO_BIG</strong></dt> <dt>(HRESULT) 0xC0AAB132</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-391"><dt><strong>IMAPI_E_DATA_TOO_BIG</strong></dt> <dt>(HRESULT)0xC0AAB132</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-392">Слишком большой файл данных для "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="1727f-392">Data file is too large for '%1!ls!'</span></span> <span data-ttu-id="1727f-393">.</span><span class="sxs-lookup"><span data-stu-id="1727f-393">file system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_OPEN_FAILURE"></span><span id="imapi_e_stashfile_open_failure"></span><dl> <span data-ttu-id="1727f-394"><dt><strong>IMAPI_E_STASHFILE_OPEN_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB138</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-394"><dt><strong>IMAPI_E_STASHFILE_OPEN_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB138</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-395">Не удается инициализировать %1! Ls!</span><span class="sxs-lookup"><span data-stu-id="1727f-395">Cannot initialize %1!ls!</span></span> <span data-ttu-id="1727f-396">скрытый файл.</span><span class="sxs-lookup"><span data-stu-id="1727f-396">stash file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_SEEK_FAILURE"></span><span id="imapi_e_stashfile_seek_failure"></span><dl> <span data-ttu-id="1727f-397"><dt><strong>IMAPI_E_STASHFILE_SEEK_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB139</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-397"><dt><strong>IMAPI_E_STASHFILE_SEEK_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB139</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-398">Поиск ошибок в "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="1727f-398">Error seeking in '%1!ls!'</span></span> <span data-ttu-id="1727f-399">скрытый файл.</span><span class="sxs-lookup"><span data-stu-id="1727f-399">stash file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_WRITE_FAILURE"></span><span id="imapi_e_stashfile_write_failure"></span><dl> <span data-ttu-id="1727f-400"><dt><strong>IMAPI_E_STASHFILE_WRITE_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB13A</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-400"><dt><strong>IMAPI_E_STASHFILE_WRITE_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB13A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-401">Произошла ошибка при записи в "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="1727f-401">Error encountered writing to '%1!ls!'</span></span> <span data-ttu-id="1727f-402">скрытый файл.</span><span class="sxs-lookup"><span data-stu-id="1727f-402">stash file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_READ_FAILURE"></span><span id="imapi_e_stashfile_read_failure"></span><dl> <span data-ttu-id="1727f-403"><dt><strong>IMAPI_E_STASHFILE_READ_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB13B</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-403"><dt><strong>IMAPI_E_STASHFILE_READ_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB13B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-404">Произошла ошибка при чтении из "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="1727f-404">Error encountered reading from '%1!ls!'</span></span> <span data-ttu-id="1727f-405">скрытый файл.</span><span class="sxs-lookup"><span data-stu-id="1727f-405">stash file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_WORKING_DIRECTORY"></span><span id="imapi_e_invalid_working_directory"></span><dl> <span data-ttu-id="1727f-406"><dt><strong>IMAPI_E_INVALID_WORKING_DIRECTORY</strong></dt> <dt>(HRESULT) 0xC0AAB140</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-406"><dt><strong>IMAPI_E_INVALID_WORKING_DIRECTORY</strong></dt> <dt>(HRESULT)0xC0AAB140</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-407">Рабочий каталог "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="1727f-407">The working directory '%1!ls!'</span></span> <span data-ttu-id="1727f-408">, недопустим.</span><span class="sxs-lookup"><span data-stu-id="1727f-408">is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_WORKING_DIRECTORY_SPACE"></span><span id="imapi_e_working_directory_space"></span><dl> <span data-ttu-id="1727f-409"><dt><strong>IMAPI_E_WORKING_DIRECTORY_SPACE</strong></dt> <dt>(HRESULT) 0xC0AAB141</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-409"><dt><strong>IMAPI_E_WORKING_DIRECTORY_SPACE</strong></dt> <dt>(HRESULT)0xC0AAB141</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-410">Не удается задать для рабочего каталога значение "%1! ls!".</span><span class="sxs-lookup"><span data-stu-id="1727f-410">Cannot set working directory to '%1!ls!'.</span></span> <span data-ttu-id="1727f-411">Доступное место: %2! I64d!</span><span class="sxs-lookup"><span data-stu-id="1727f-411">Space available is %2!I64d!</span></span> <span data-ttu-id="1727f-412">байт, приблизительно %3! I64d!</span><span class="sxs-lookup"><span data-stu-id="1727f-412">bytes, approximately %3!I64d!</span></span> <span data-ttu-id="1727f-413">требуемые байты.</span><span class="sxs-lookup"><span data-stu-id="1727f-413">bytes required.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_MOVE"></span><span id="imapi_e_stashfile_move"></span><dl> <span data-ttu-id="1727f-414"><dt><strong>IMAPI_E_STASHFILE_MOVE</strong></dt> <dt>(HRESULT) 0xC0AAB142</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-414"><dt><strong>IMAPI_E_STASHFILE_MOVE</strong></dt> <dt>(HRESULT)0xC0AAB142</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-415">Попытка переместить скрытый файл данных в каталог "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="1727f-415">Attempt to move the data stash file to directory '%1!ls!'</span></span> <span data-ttu-id="1727f-416">не выполнено.</span><span class="sxs-lookup"><span data-stu-id="1727f-416">was not successful.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_BOOT_IMAGE_DATA"></span><span id="imapi_e_boot_image_data"></span><dl> <span data-ttu-id="1727f-417"><dt><strong>IMAPI_E_BOOT_IMAGE_DATA</strong></dt> <dt>(HRESULT) 0xC0AAB148</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-417"><dt><strong>IMAPI_E_BOOT_IMAGE_DATA</strong></dt> <dt>(HRESULT)0xC0AAB148</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-418">Не удалось добавить объект загрузки к образу.</span><span class="sxs-lookup"><span data-stu-id="1727f-418">The boot object could not be added to the image.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_BOOT_OBJECT_CONFLICT"></span><span id="imapi_e_boot_object_conflict"></span><dl> <span data-ttu-id="1727f-419"><dt><strong>IMAPI_E_BOOT_OBJECT_CONFLICT</strong></dt> <dt>(HRESULT) 0xC0AAB149</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-419"><dt><strong>IMAPI_E_BOOT_OBJECT_CONFLICT</strong></dt> <dt>(HRESULT)0xC0AAB149</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-420">Объект загрузки может быть включен только в исходный образ диска.</span><span class="sxs-lookup"><span data-stu-id="1727f-420">A boot object can only be included in an initial disc image.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH"></span><span id="imapi_e_boot_emulation_image_size_mismatch"></span><dl> <span data-ttu-id="1727f-421"><dt><strong>IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH</strong></dt> <dt>(HRESULT) 0xC0AAB14A</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-421"><dt><strong>IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH</strong></dt> <dt>(HRESULT)0xC0AAB14A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-422">Запрошенный тип эмуляции не соответствует размеру загрузочного образа.</span><span class="sxs-lookup"><span data-stu-id="1727f-422">The emulation type requested does not match the boot image size.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_EMPTY_DISC"></span><span id="imapi_e_empty_disc"></span><dl> <span data-ttu-id="1727f-423"><dt><strong>IMAPI_E_EMPTY_DISC</strong></dt> <dt>(HRESULT) 0xC0AAB150</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-423"><dt><strong>IMAPI_E_EMPTY_DISC</strong></dt> <dt>(HRESULT)0xC0AAB150</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-424">Оптический носитель пуст.</span><span class="sxs-lookup"><span data-stu-id="1727f-424">Optical media is empty.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_SUPPORTED_FILE_SYSTEM"></span><span id="imapi_e_no_supported_file_system"></span><dl> <span data-ttu-id="1727f-425"><dt><strong>IMAPI_E_NO_SUPPORTED_FILE_SYSTEM</strong></dt> <dt>(HRESULT) 0xC0AAB151</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-425"><dt><strong>IMAPI_E_NO_SUPPORTED_FILE_SYSTEM</strong></dt> <dt>(HRESULT)0xC0AAB151</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-426">Указанный диск не содержит одну из поддерживаемых файловых систем.</span><span class="sxs-lookup"><span data-stu-id="1727f-426">The specified disc does not contain one of the supported file systems.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_NOT_FOUND"></span><span id="imapi_e_file_system_not_found"></span><dl> <span data-ttu-id="1727f-427"><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_FOUND</strong></dt> <dt>(HRESULT) 0xC0AAB152</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-427"><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB152</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-428">Указанный диск не содержит "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="1727f-428">The specified disc does not contain a '%1!ls!'</span></span> <span data-ttu-id="1727f-429">.</span><span class="sxs-lookup"><span data-stu-id="1727f-429">file system.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR"></span><span id="imapi_e_file_system_read_consistency_error"></span><dl> <span data-ttu-id="1727f-430"><dt><strong>IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR</strong></dt> <dt>(HRESULT) 0xC0AAB153</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-430"><dt><strong>IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR</strong></dt> <dt>(HRESULT)0xC0AAB153</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-431">Произошла ошибка согласованности при импорте "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="1727f-431">Consistency error encountered while importing the '%1!ls!'</span></span> <span data-ttu-id="1727f-432">.</span><span class="sxs-lookup"><span data-stu-id="1727f-432">file system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED"></span><span id="imapi_e_file_system_feature_not_supported"></span><dl> <span data-ttu-id="1727f-433"><dt><strong>IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xC0AAB154</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-433"><dt><strong>IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AAB154</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-434">"%1! ls!" файловая система на выбранном диске содержит функцию, не поддерживаемую для импорта: %2! Ls!.</span><span class="sxs-lookup"><span data-stu-id="1727f-434">The '%1!ls!'file system on the selected disc contains a feature not supported for import: %2!ls!.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY"></span><span id="imapi_e_import_type_collision_file_exists_as_directory"></span><dl> <span data-ttu-id="1727f-435"><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY</strong></dt> <dt>(HRESULT) 0xC0AAB155</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-435"><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY</strong></dt> <dt>(HRESULT)0xC0AAB155</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-436">Не удалось импортировать %2! Ls!</span><span class="sxs-lookup"><span data-stu-id="1727f-436">Could not import %2!ls!</span></span> <span data-ttu-id="1727f-437">файловая система с диска. Файл "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="1727f-437">file system from disc. The file '%1!ls!'</span></span> <span data-ttu-id="1727f-438">уже существует в иерархии образа в качестве каталога.</span><span class="sxs-lookup"><span data-stu-id="1727f-438">already exists within the image hierarchy as a directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_SEEK_FAILURE"></span><span id="imapi_e_import_seek_failure"></span><dl> <span data-ttu-id="1727f-439"><dt><strong>IMAPI_E_IMPORT_SEEK_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB156</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-439"><dt><strong>IMAPI_E_IMPORT_SEEK_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB156</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-440">Не удается найти блок %1! I64d!</span><span class="sxs-lookup"><span data-stu-id="1727f-440">Cannot seek to block %1!I64d!</span></span> <span data-ttu-id="1727f-441">на исходном диске.</span><span class="sxs-lookup"><span data-stu-id="1727f-441">on source disc.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_READ_FAILURE"></span><span id="imapi_e_import_read_failure"></span><dl> <span data-ttu-id="1727f-442"><dt><strong>IMAPI_E_IMPORT_READ_FAILURE</strong></dt> <dt>(HRESULT) 0xC0AAB157</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-442"><dt><strong>IMAPI_E_IMPORT_READ_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB157</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-443">Сбой импорта из предыдущего сеанса из-за ошибки при чтении блока на носителе (скорее всего, это блок %1! u!).</span><span class="sxs-lookup"><span data-stu-id="1727f-443">Import from previous session failed due to an error reading a block on the media (most likely block %1!u!).</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DISC_MISMATCH"></span><span id="imapi_e_disc_mismatch"></span><dl> <span data-ttu-id="1727f-444"><dt><strong>IMAPI_E_DISC_MISMATCH</strong></dt> <dt>(HRESULT) 0xC0AAB158</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-444"><dt><strong>IMAPI_E_DISC_MISMATCH</strong></dt> <dt>(HRESULT)0xC0AAB158</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-445">Текущий диск не совпадает с тем, с которого была импортирована файловая система.</span><span class="sxs-lookup"><span data-stu-id="1727f-445">Current disc is not the same one from which file system was imported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED"></span><span id="imapi_e_import_media_not_allowed"></span><dl> <span data-ttu-id="1727f-446"><dt><strong>IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED</strong></dt> <dt>(HRESULT) 0xC0AAB159</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-446"><dt><strong>IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED</strong></dt> <dt>(HRESULT)0xC0AAB159</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-447">IMAPI не позволяет использовать несколько сеансов с текущим типом носителя.</span><span class="sxs-lookup"><span data-stu-id="1727f-447">IMAPI does not allow multi-session with the current media type.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_UDF_NOT_WRITE_COMPATIBLE"></span><span id="imapi_e_udf_not_write_compatible"></span><dl> <span data-ttu-id="1727f-448"><dt><strong>IMAPI_E_UDF_NOT_WRITE_COMPATIBLE</strong></dt> <dt>(HRESULT) 0xC0AAB15A</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-448"><dt><strong>IMAPI_E_UDF_NOT_WRITE_COMPATIBLE</strong></dt> <dt>(HRESULT)0xC0AAB15A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-449">IMAPI не может выполнить несколько сеансов с текущим носителем, так как он не поддерживает совместимую редакцию UDF для записи.</span><span class="sxs-lookup"><span data-stu-id="1727f-449">IMAPI cannot do multi-session with the current media because it does not support a compatible UDF revision for write.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_incompatible_multisession_type"></span><dl> <span data-ttu-id="1727f-450"><dt><strong>IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt>(HRESULT) 0xC0AAB15B</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-450"><dt><strong>IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt>(HRESULT)0xC0AAB15B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-451">IMAPI не поддерживает запрошенный тип многосеансовой связи.</span><span class="sxs-lookup"><span data-stu-id="1727f-451">IMAPI does not support the multisession type requested.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION"></span><span id="imapi_e_incompatible_previous_session"></span><dl> <span data-ttu-id="1727f-452"><dt><strong>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</strong></dt> <dt>(HRESULT) 0xC0AAB133</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-452"><dt><strong>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</strong></dt> <dt>(HRESULT)0xC0AAB133</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-453">Сбой операции из-за несовместимого макета предыдущего сеанса, импортированного с носителя.</span><span class="sxs-lookup"><span data-stu-id="1727f-453">Operation failed due to an incompatible layout of the previous session imported from the medium.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_no_compatible_multisession_type"></span><dl> <span data-ttu-id="1727f-454"><dt><strong>IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt>(HRESULT) 0xC0AAB15C</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-454"><dt><strong>IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt>(HRESULT)0xC0AAB15C</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-455">IMAPI не поддерживает ни одного типа многосеансовой передачи, предоставленного на текущем носителе.</span><span class="sxs-lookup"><span data-stu-id="1727f-455">IMAPI supports none of the multisession type(s) provided on the current media.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1727f-456">[<strong>Ифилесистемимаже:: импортфилесистем</strong>] (/Windows/Desktop/API/IMAPI2FS/NF-IMAPI2FS-ifilesystemimage-importfilesystem) метод возвращает эту ошибку, если в записывающем устройстве нет носителя.</span><span class="sxs-lookup"><span data-stu-id="1727f-456">[<strong>IFileSystemImage::ImportFileSystem</strong>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) method returns this error if there is no media in the recording device.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_MULTISESSION_NOT_SET"></span><span id="imapi_e_multisession_not_set"></span><dl> <span data-ttu-id="1727f-457"><dt><strong>IMAPI_E_MULTISESSION_NOT_SET</strong></dt> <dt>(HRESULT) 0xC0AAB15D</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-457"><dt><strong>IMAPI_E_MULTISESSION_NOT_SET</strong></dt> <dt>(HRESULT)0xC0AAB15D</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-458">Перед вызовом этого метода необходимо задать свойство Мултисессионинтерфацес.</span><span class="sxs-lookup"><span data-stu-id="1727f-458">MultisessionInterfaces property must be set prior calling this method.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE"></span><span id="imapi_e_import_type_collision_directory_exists_as_file"></span><dl> <span data-ttu-id="1727f-459"><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE</strong></dt> <dt>(HRESULT) 0xC0AAB15E</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-459"><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE</strong></dt> <dt>(HRESULT)0xC0AAB15E</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-460">Не удалось импортировать %2! Ls!</span><span class="sxs-lookup"><span data-stu-id="1727f-460">Could not import %2!ls!</span></span> <span data-ttu-id="1727f-461">файловая система с диска. Каталог "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="1727f-461">file system from disc. The directory '%1!ls!'</span></span> <span data-ttu-id="1727f-462">уже существует в иерархии изображений в качестве файла.</span><span class="sxs-lookup"><span data-stu-id="1727f-462">already exists within the image hierarchy as a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_BAD_MULTISESSION_PARAMETER"></span><span id="imapi_e_bad_multisession_parameter"></span><dl> <span data-ttu-id="1727f-463"><dt><strong>IMAPI_E_BAD_MULTISESSION_PARAMETER</strong></dt> <dt>(HRESULT) 0xC0AAB162</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-463"><dt><strong>IMAPI_E_BAD_MULTISESSION_PARAMETER</strong></dt> <dt>(HRESULT)0xC0AAB162</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-464">Один из многосеансовых параметров не может быть получен или имеет неверное значение.</span><span class="sxs-lookup"><span data-stu-id="1727f-464">One of multisession parameters cannot be retrieved or has a wrong value.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED"></span><span id="imapi_s_image_feature_not_supported"></span><dl> <span data-ttu-id="1727f-465"><dt><strong>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0x00AAB15FL</dt> </span><span class="sxs-lookup"><span data-stu-id="1727f-465"><dt><strong>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0x00AAB15FL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="1727f-466">Эта функция не поддерживается для текущей редакции файловой системы.</span><span class="sxs-lookup"><span data-stu-id="1727f-466">This feature is not supported for the current file system revision.</span></span> <span data-ttu-id="1727f-467">Образ будет создан без этой функции.</span><span class="sxs-lookup"><span data-stu-id="1727f-467">The image will be created without this feature.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="1727f-468">Требования</span><span class="sxs-lookup"><span data-stu-id="1727f-468">Requirements</span></span>



| <span data-ttu-id="1727f-469">Требование</span><span class="sxs-lookup"><span data-stu-id="1727f-469">Requirement</span></span> | <span data-ttu-id="1727f-470">Значение</span><span class="sxs-lookup"><span data-stu-id="1727f-470">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1727f-471">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1727f-471">Minimum supported client</span></span><br/> | <span data-ttu-id="1727f-472">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1727f-472">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="1727f-473">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1727f-473">Minimum supported server</span></span><br/> | <span data-ttu-id="1727f-474">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1727f-474">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                            |
| <span data-ttu-id="1727f-475">Header</span><span class="sxs-lookup"><span data-stu-id="1727f-475">Header</span></span><br/>                   | <dl> <span data-ttu-id="1727f-476"><dt>Imapi2error. h; </dt> <dt>Imapi2fserror. h</dt></span><span class="sxs-lookup"><span data-stu-id="1727f-476"><dt>Imapi2error.h; </dt> <dt>Imapi2fserror.h</dt></span></span> </dl> |



 

 





