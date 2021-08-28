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
ms.openlocfilehash: 857f9c018fc34a16a0dc431714aacc1fcdf6a5b1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474800"
---
# <a name="imapi-return-values"></a>Возвращаемые значения IMAPI

Методы IMAPI возвращают неотрицательные значения (обычно S \_ ОК), если метод был успешным. Методы IMAPI возвращают коды успеха или ошибки из Winerror. h, Imapi2error. h или Imapi2fserror. h в случае сбоя.

Определены следующие коды успеха и ошибки.




| Константа/значение | Описание | 
|----------------|-------------|
| <span id="E_IMAPI_BURN_VERIFICATION_FAILED"></span><span id="e_imapi_burn_verification_failed"></span><dl><dt><strong>E_IMAPI_BURN_VERIFICATION_FAILED</strong></dt><dt>(HRESULT) 0xC0AA0007L</dt></dl> | Диск не прошел проверку записи и может содержать поврежденные данные или быть непригодным для использования.<br /> | 
| <span id="E_IMAPI_REQUEST_CANCELLED"></span><span id="e_imapi_request_cancelled"></span><dl><dt><strong>E_IMAPI_REQUEST_CANCELLED</strong></dt><dt>(HRESULT) 0xC0AA0002</dt></dl> | Запрос отменен.<br /> | 
| <span id="E_IMAPI_RECORDER_REQUIRED"></span><span id="e_imapi_recorder_required"></span><dl><dt><strong>E_IMAPI_RECORDER_REQUIRED</strong></dt><dt>(HRESULT) 0xC0AA0003</dt></dl> | Для запроса требуется выбрать текущий записывающий диск.<br /> | 
| <span id="S_IMAPI_WRITE_NOT_IN_PROGRESS"></span><span id="s_imapi_write_not_in_progress"></span><dl><dt><strong>S_IMAPI_WRITE_NOT_IN_PROGRESS</strong></dt><dt>(HRESULT) 0x00AA0302L</dt></dl> | В настоящее время операции записи не выполняются.<br /> | 
| <span id="S_IMAPI_SPEEDADJUSTED"></span><span id="s_imapi_speedadjusted"></span><dl><dt><strong>S_IMAPI_SPEEDADJUSTED</strong></dt><dt>(HRESULT) 0x00AA0004</dt></dl> | Запрошенная скорость записи не поддерживается диском, и была скорректирована скорость.<br /> | 
| <span id="S_IMAPI_ROTATIONADJUSTED"></span><span id="s_imapi_rotationadjusted"></span><dl><dt><strong>S_IMAPI_ROTATIONADJUSTED</strong></dt><dt>(HRESULT) 0x00AA0005</dt></dl> | Запрошенный тип вращения не поддерживается диском, и тип вращения был скорректирован.<br /> | 
| <span id="S_IMAPI_BOTHADJUSTED"></span><span id="s_imapi_bothadjusted"></span><dl><dt><strong>S_IMAPI_BOTHADJUSTED</strong></dt><dt>(HRESULT) 0x00AA0006</dt></dl> | Запрошенная скорость записи и тип вращения не поддерживались диском, и они были скорректированы.<br /> | 
| <span id="S_IMAPI_COMMAND_HAS_SENSE_DATA"></span><span id="s_imapi_command_has_sense_data"></span><dl><dt><strong>S_IMAPI_COMMAND_HAS_SENSE_DATA</strong></dt><dt>(HRESULT) 0x00AA0200</dt></dl> | Устройство приняло команду, но вернуло данные, указывающие на ошибку.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_IS_READ_ONLY"></span><span id="e_imapi_raw_image_is_read_only"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_IS_READ_ONLY</strong></dt><dt>(HRESULT) 0x80AA0A00L</dt></dl> | Образ стал доступен только для чтения из-за вызова <a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-createresultimage"><strong>иравкдимажекреатор:: креатересултимаже</strong></a>. В результате объект больше не может быть изменен.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS"></span><span id="e_imapi_raw_image_too_many_tracks"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS</strong></dt><dt>(HRESULT) 0x80AA0A01L</dt></dl> | Дополнительные записи добавляться не могут. Диск CD ограничен диапазоном 1-99 дорожек.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_NO_TRACKS"></span><span id="e_imapi_raw_image_no_tracks"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_NO_TRACKS</strong></dt><dt>(HRESULT) 0x80AA0A03L</dt></dl> | Перед использованием этой функции необходимо добавить дорожки в образ.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_raw_image_sector_type_not_supported"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0x80AA0A02L</dt></dl> | Запрошенный тип сектора не поддерживается.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED"></span><span id="e_imapi_raw_image_tracks_already_added"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED</strong></dt><dt>(HRESULT) 0x80AA0A04L</dt></dl> | Записи не могут быть добавлены в образ перед использованием этой функции.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE"></span><span id="e_imapi_raw_image_insufficient_space"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE</strong></dt><dt>(HRESULT) 0x80AA0A05L</dt></dl> | Добавление этой записи приведет к превышению ограничений, накладываемых на начало интереса.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES"></span><span id="e_imapi_raw_image_too_many_track_indexes"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES</strong></dt><dt>(HRESULT) 0x80AA0A06L</dt></dl> | Добавление этой записи приведет к превышению предельного числа индексов 99.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND"></span><span id="e_imapi_raw_image_track_index_not_found"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND</strong></dt><dt>(HRESULT) 0x80AA0A07L</dt></dl> | Указанное смещение LBA отсутствует в списке индексов Track.<br /> | 
| <span id="S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS"></span><span id="s_imapi_raw_image_track_index_already_exists"></span><dl><dt><strong>S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS</strong></dt><dt>(HRESULT) 0x00AA0A08L</dt></dl> | Указанное смещение LBA уже находится в списке индексов Track.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED"></span><span id="e_imapi_raw_image_track_index_offset_zero_cannot_be_cleared"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED</strong></dt><dt>(HRESULT) 0x80AA0A09L</dt></dl> | Индекс 1 (Нулевое смещение LBA) не может быть сброшен.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX"></span><span id="e_imapi_raw_image_track_index_too_close_to_other_index"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX</strong></dt><dt>(HRESULT) 0x80AA0A0AL</dt></dl> | Размер каждого индекса должен быть не менее десяти секторов.<br /> | 
| <span id="E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE"></span><span id="e_imapi_recorder_no_such_mode_page"></span><dl><dt><strong>E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE</strong></dt><dt>(HRESULT) 0xC0AA0201</dt></dl> | Устройство сообщило, что запрошенная страница режима (и тип) отсутствует.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_NO_MEDIA"></span><span id="e_imapi_recorder_media_no_media"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_NO_MEDIA</strong></dt><dt>(HRESULT) 0xC0AA0202</dt></dl> | На устройстве нет носителя.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE"></span><span id="e_imapi_recorder_media_incompatible"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE</strong></dt><dt>(HRESULT) 0xC0AA0203</dt></dl> | Носитель несовместим или имеет неизвестный физический формат.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN"></span><span id="e_imapi_recorder_media_upside_down"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN</strong></dt><dt>(HRESULT) 0xC0AA0204</dt></dl> | Носитель вставляется вверх.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_BECOMING_READY"></span><span id="e_imapi_recorder_media_becoming_ready"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_BECOMING_READY</strong></dt><dt>(HRESULT) 0xC0AA0205</dt></dl> | Диск сообщил, что он находится в процессе подготовки. Повторите запрос позже.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS"></span><span id="e_imapi_recorder_media_format_in_progress"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS</strong></dt><dt>(HRESULT) 0xC0AA0206</dt></dl> | Носитель форматируется в данный момент. Дождитесь завершения форматирования, прежде чем пытаться использовать носитель.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_BUSY"></span><span id="e_imapi_recorder_media_busy"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_BUSY</strong></dt><dt>(HRESULT) 0xC0AA0207</dt></dl> | Диск сообщил о выполнении длительной операции, такой как завершение записи. Диск может быть непригоден для длительного периода времени.<br /> | 
| <span id="E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS"></span><span id="e_imapi_recorder_invalid_mode_parameters"></span><dl><dt><strong>E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS</strong></dt><dt>(HRESULT) 0xC0AA0208</dt></dl> | Диск сообщил, что сочетание параметров, указанных на странице режим для команды выбор режима, не поддерживается.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED"></span><span id="e_imapi_recorder_media_write_protected"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED</strong></dt><dt>(HRESULT) 0xC0AA0209</dt></dl> | Диск сообщил, что носитель защищен от записи.<br /> | 
| <span id="E_IMAPI_RECORDER_NO_SUCH_FEATURE"></span><span id="e_imapi_recorder_no_such_feature"></span><dl><dt><strong>E_IMAPI_RECORDER_NO_SUCH_FEATURE</strong></dt><dt>(HRESULT) 0xC0AA020A</dt></dl> | Запрошенная страница функций не поддерживается устройством.<br /> | 
| <span id="E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT"></span><span id="e_imapi_recorder_feature_is_not_current"></span><dl><dt><strong>E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT</strong></dt><dt>(HRESULT) 0xC0AA020B</dt></dl> | Запрошенная страница компонентов поддерживается, но не помечена как текущая.<br /> | 
| <span id="E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED"></span><span id="e_imapi_recorder_get_configuration_not_supported"></span><dl><dt><strong>E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA020C</dt></dl> | Диск не поддерживает команду "получить конфигурацию".<br /> | 
| <span id="E_IMAPI_RECORDER_COMMAND_TIMEOUT"></span><span id="e_imapi_recorder_command_timeout"></span><dl><dt><strong>E_IMAPI_RECORDER_COMMAND_TIMEOUT</strong></dt><dt>(HRESULT) 0xC0AA020D</dt></dl> | Устройству не удалось принять команду в течение периода ожидания. Это может быть вызвано тем, что устройство перешло в непротиворечивое состояние, или может потребоваться увеличить значение времени ожидания для команды.<br /> | 
| <span id="E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT"></span><span id="e_imapi_recorder_dvd_structure_not_present"></span><dl><dt><strong>E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT</strong></dt><dt>(HRESULT) 0xC0AA020E</dt></dl> | Структура DVD отсутствует. Это может быть вызвано тем, что используется несовместимый диск или носитель.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH"></span><span id="e_imapi_recorder_media_speed_mismatch"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH</strong></dt><dt>(HRESULT) 0xC0AA020F</dt></dl> | Скорость носителя несовместима с устройством. Это может быть вызвано использованием носителя с более высокой или низкой скоростью, чем диапазон поддерживаемых устройством частот.<br /> | 
| <span id="E_IMAPI_RECORDER_LOCKED"></span><span id="e_imapi_recorder_locked"></span><dl><dt><strong>E_IMAPI_RECORDER_LOCKED</strong></dt><dt>(HRESULT) 0xC0AA0210</dt></dl> | Устройство, связанное с этим средством записи во время последней операции, заблокировано в монопольном режиме, что привело к сбою этой операции.<br /> | 
| <span id="E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_recorder_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID</strong></dt><dt>(HRESULT) 0xC0AA0211</dt></dl> | Недопустимое имя клиента.<br /> | 
| <span id="E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_recorder_invalid_response_from_device"></span><dl><dt><strong>E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE</strong></dt><dt>(HRESULT) 0xC0AA02FF</dt></dl> | Устройство сообщило о непредвиденных или недопустимых данных для команды.<br /> | 
| <span id="E_IMAPI_LOSS_OF_STREAMING"></span><span id="e_imapi_loss_of_streaming"></span><dl><dt><strong>E_IMAPI_LOSS_OF_STREAMING</strong></dt><dt>(HRESULT) 0xC0AA0300</dt></dl> | Произошел сбой записи, так как диск не получал данные достаточно быстро для продолжения записи. Чтобы устранить эту проблему, можно переместить исходные данные на локальный компьютер, уменьшить скорость записи или включить параметр "Свободная опустошение буфера".<br /> | 
| <span id="E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_unexpected_response_from_device"></span><dl><dt><strong>E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE</strong></dt><dt>(HRESULT) 0xC0AA0301</dt></dl> | Произошел сбой записи, так как диск вернул информацию об ошибке, которую не удалось восстановить из.<br /> | 
| <span id="E_IMAPI_DF2DATA_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2data_write_in_progress"></span><dl><dt><strong>E_IMAPI_DF2DATA_WRITE_IN_PROGRESS</strong></dt><dt>(HRESULT) 0xC0AA0400</dt></dl> | Сейчас выполняется операция записи.<br /> | 
| <span id="E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2data_write_not_in_progress"></span><dl><dt><strong>E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS</strong></dt><dt>(HRESULT) 0xC0AA0401</dt></dl> | Сейчас нет выполняющихся операций записи.<br /> | 
| <span id="E_IMAPI_DF2DATA_INVALID_MEDIA_STATE"></span><span id="e_imapi_df2data_invalid_media_state"></span><dl><dt><strong>E_IMAPI_DF2DATA_INVALID_MEDIA_STATE</strong></dt><dt>(HRESULT) 0xC0AA0402</dt></dl> | Запрошенная операция допустима только для поддерживаемых носителей.<br /> | 
| <span id="E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2data_stream_not_supported"></span><dl><dt><strong>E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA0403</dt></dl> | Указанный поток для записи не поддерживается.<br /> | 
| <span id="E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA"></span><span id="e_imapi_df2data_stream_too_large_for_current_media"></span><dl><dt><strong>E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA</strong></dt><dt>(HRESULT) 0xC0AA0404</dt></dl> | Указанный поток для записи слишком велик для текущего вставленного носителя.<br /> | 
| <span id="E_IMAPI_DF2DATA_MEDIA_NOT_BLANK"></span><span id="e_imapi_df2data_media_not_blank"></span><dl><dt><strong>E_IMAPI_DF2DATA_MEDIA_NOT_BLANK</strong></dt><dt>(HRESULT) 0xC0AA0405</dt></dl> | Перезапись непустого носителя не допускается, если для свойства Форцеоверврите не задано значение VARIANT_TRUE.<br /> | 
| <span id="E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2data_media_is_not_supported"></span><dl><dt><strong>E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA0406</dt></dl> | Текущий тип мультимедиа не поддерживается.<br /> | 
| <span id="E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2data_recorder_not_supported"></span><dl><dt><strong>E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA0407</dt></dl> | Это устройство не поддерживает операции, необходимые для этого формата диска.<br /> | 
| <span id="E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2data_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID</strong></dt><dt>(HRESULT) 0xC0AA0408</dt></dl> | Недопустимое имя клиента.<br /> | 
| <span id="E_IMAPI_DF2TAO_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_in_progress"></span><dl><dt><strong>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</strong></dt><dt>(HRESULT) 0xC0AA0500</dt></dl> | Сейчас выполняется операция записи.<br /> | 
| <span id="E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_not_in_progress"></span><dl><dt><strong>E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS</strong></dt><dt>(HRESULT) 0xC0AA0501</dt></dl> | Сейчас нет выполняющихся операций записи.<br /> | 
| <span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2tao_media_is_not_prepared"></span><dl><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED</strong></dt><dt>(HRESULT) 0xC0AA0502</dt></dl> | Запрошенная операция допустима, только если носитель подготовлен.<br /> | 
| <span id="E_IMAPI_DF2TAO_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2tao_media_is_prepared"></span><dl><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_PREPARED</strong></dt><dt>(HRESULT) 0xC0AA0503</dt></dl> | Запрошенная операция недопустима, если носитель был подготовлен, но не освобожден.<br /> | 
| <span id="E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY"></span><span id="e_imapi_df2tao_property_for_blank_media_only"></span><dl><dt><strong>E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY</strong></dt><dt>(HRESULT) 0xC0AA0504</dt></dl> | Свойство нельзя изменить после того, как носитель будет записан в.<br /> | 
| <span id="E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC"></span><span id="e_imapi_df2tao_table_of_contents_empty_disc"></span><dl><dt><strong>E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC</strong></dt><dt>(HRESULT) 0xC0AA0505</dt></dl> | Не удается получить оглавление с пустого диска.<br /> | 
| <span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2tao_media_is_not_blank"></span><dl><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK</strong></dt><dt>(HRESULT) 0xC0AA0506</dt></dl> | Поддерживается только чистый носитель CD-R/RW.<br /> | 
| <span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_media_is_not_supported"></span><dl><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA0507</dt></dl> | Поддерживается только чистый носитель CD-R/RW.<br /> | 
| <span id="E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED"></span><span id="e_imapi_df2tao_track_limit_reached"></span><dl><dt><strong>E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED</strong></dt><dt>(HRESULT) 0xC0AA0508</dt></dl> | Носители CD-R и CD-RW поддерживают не более 99 звуковых дорожек.<br /> | 
| <span id="E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2tao_not_enough_space"></span><dl><dt><strong>E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE</strong></dt><dt>(HRESULT) 0xC0AA0509</dt></dl> | На носителе недостаточно места для добавления указанной звуковой дорожки.<br /> | 
| <span id="E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2tao_no_recorder_specified"></span><dl><dt><strong>E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED</strong></dt><dt>(HRESULT) 0xC0AA050A</dt></dl> | Вы не можете подготовить носитель, пока не выберите устройство записи.<br /> | 
| <span id="E_IMAPI_DF2TAO_INVALID_ISRC"></span><span id="e_imapi_df2tao_invalid_isrc"></span><dl><dt><strong>E_IMAPI_DF2TAO_INVALID_ISRC</strong></dt><dt>(HRESULT) 0xC0AA050B</dt></dl> | Указан недопустимый ИСРК.<br /> | 
| <span id="E_IMAPI_DF2TAO_INVALID_MCN"></span><span id="e_imapi_df2tao_invalid_mcn"></span><dl><dt><strong>E_IMAPI_DF2TAO_INVALID_MCN</strong></dt><dt>(HRESULT) 0xC0AA050C</dt></dl> | Указан недопустимый номер каталога носителей.<br /> | 
| <span id="E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_stream_not_supported"></span><dl><dt><strong>E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA050D</dt></dl> | Указанный звуковой поток недопустим.<br /> | 
| <span id="E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_recorder_not_supported"></span><dl><dt><strong>E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA050E</dt></dl> | Это устройство не поддерживает операции, необходимые для этого формата диска.<br /> | 
| <span id="E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2tao_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID</strong></dt><dt>(HRESULT) 0xC0AA050F</dt></dl> | Недопустимое имя клиента.<br /> | 
| <span id="E_IMAPI_DF2RAW_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_in_progress"></span><dl><dt><strong>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</strong></dt><dt>(HRESULT) 0xC0AA0600</dt></dl> | Сейчас выполняется операция записи.<br /> | 
| <span id="E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_not_in_progress"></span><dl><dt><strong>E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS</strong></dt><dt>(HRESULT) 0xC0AA0601</dt></dl> | Сейчас нет выполняющихся операций записи.<br /> | 
| <span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2raw_media_is_not_prepared"></span><dl><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</strong></dt><dt>(HRESULT) 0xC0AA0602</dt></dl> | Запрошенная операция допустима, только если носитель подготовлен.<br /> | 
| <span id="E_IMAPI_DF2RAW_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2raw_media_is_prepared"></span><dl><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_PREPARED</strong></dt><dt>(HRESULT) 0xC0AA0603</dt></dl> | Запрошенная операция недопустима, если носитель был подготовлен, но не освобожден.<br /> | 
| <span id="E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2raw_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID</strong></dt><dt>(HRESULT) 0xC0AA0604</dt></dl> | Недопустимое имя клиента.<br /> | 
| <span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2raw_media_is_not_blank"></span><dl><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK</strong></dt><dt>(HRESULT) 0xC0AA0606</dt></dl> | Поддерживается только чистый носитель CD-R/RW.<br /> | 
| <span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_media_is_not_supported"></span><dl><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA0607</dt></dl> | Поддерживается только чистый носитель CD-R/RW.<br /> | 
| <span id="E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2raw_not_enough_space"></span><dl><dt><strong>E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE</strong></dt><dt>(HRESULT) 0xC0AA0609</dt></dl> | Недостаточно места на носителе для добавления указанного сеанса.<br /> | 
| <span id="E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2raw_no_recorder_specified"></span><dl><dt><strong>E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED</strong></dt><dt>(HRESULT) 0xC0AA060A</dt></dl> | Вы не можете подготовить носитель, пока не выберите устройство записи.<br /> | 
| <span id="E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_stream_not_supported"></span><dl><dt><strong>E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA060D</dt></dl> | Указанный звуковой поток недопустим.<br /> | 
| <span id="E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_data_block_type_not_supported"></span><dl><dt><strong>E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA060E</dt></dl> | Запрошенный тип блока данных не поддерживается текущим устройством.<br /> | 
| <span id="E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT"></span><span id="e_imapi_df2raw_stream_leadin_too_short"></span><dl><dt><strong>E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT</strong></dt><dt>(HRESULT) 0xC0AA060F</dt></dl> | Поток не содержит достаточного количества секторов для текущего носителя.<br /> | 
| <span id="E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_recorder_not_supported"></span><dl><dt><strong>E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA0610</dt></dl> | Это устройство не поддерживает операции, необходимые для этого формата диска.<br /> | 
| <span id="E_IMAPI_ERASE_RECORDER_IN_USE"></span><span id="e_imapi_erase_recorder_in_use"></span><dl><dt><strong>E_IMAPI_ERASE_RECORDER_IN_USE</strong></dt><dt>(HRESULT) 0x80AA0900</dt></dl> | В данный момент формат использует устройство записи дисков для операции стирания. Дождитесь завершения стирания, прежде чем пытаться установить или очистить текущий записывающий диск.<br /> | 
| <span id="E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED"></span><span id="e_imapi_erase_only_one_recorder_supported"></span><dl><dt><strong>E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED</strong></dt><dt>(HRESULT) 0x80AA0901</dt></dl> | Формат стирания поддерживает только один инструмент записи. Перед установкой нового параметра необходимо очистить текущее средство записи.<br /> | 
| <span id="E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL"></span><span id="e_imapi_erase_disc_information_too_small"></span><dl><dt><strong>E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL</strong></dt><dt>(HRESULT) 0x80AA0902</dt></dl> | Диск не сообщает о достаточном объеме данных для команды READ CD INFORMATION. Возможно, диск не поддерживается или носитель неправилен.<br /> | 
| <span id="E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL"></span><span id="e_imapi_erase_mode_page_2a_too_small"></span><dl><dt><strong>E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL</strong></dt><dt>(HRESULT) 0x80AA0903</dt></dl> | Диск не сообщает достаточные данные для команды режима MODE (страница 0x2A). Возможно, диск не поддерживается или носитель неправилен.<br /> | 
| <span id="E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE"></span><span id="e_imapi_erase_media_is_not_erasable"></span><dl><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE</strong></dt><dt>(HRESULT) 0x80AA0904</dt></dl> | Диск сообщил, что носитель не может быть поврежден.<br /> | 
| <span id="E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND"></span><span id="e_imapi_erase_drive_failed_erase_command"></span><dl><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND</strong></dt><dt>(HRESULT) 0x80AA0905</dt></dl> | Диск не прошел команду стирания.<br /> | 
| <span id="E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR"></span><span id="e_imapi_erase_took_longer_than_one_hour"></span><dl><dt><strong>E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR</strong></dt><dt>(HRESULT) 0x80AA0906</dt></dl> | Диск не выполнил стирание за один час. Для возобновления работы диска может потребоваться цикл электропитания, удаление носителя или другое вмешательство вручную.<br /><blockquote>[!Note]<br />В настоящее время это значение также будет возвращаться, если попытка выполнить операцию стирания на носителе CD-RW или DVD-RW с помощью интерфейса <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a> завершается неудачей в результате неправильного носителя.</blockquote><br /> | 
| <span id="E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE"></span><span id="e_imapi_erase_unexpected_drive_response_during_erase"></span><dl><dt><strong>E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE</strong></dt><dt>(HRESULT) 0x80AA0907</dt></dl> | Диск вернул непредвиденную ошибку во время стирания. Возможно, носитель непригоден для использования, стирание может быть завершено, или диск по-прежнему находится в процессе стирания диска.<br /> | 
| <span id="E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND"></span><span id="e_imapi_erase_drive_failed_spinup_command"></span><dl><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND</strong></dt><dt>(HRESULT) 0x80AA0908</dt></dl> | Диск возвратил ошибку для команды начального блока (спинуп). Может потребоваться вмешательство вручную.<br /> | 
| <span id="E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_erase_media_is_not_supported"></span><dl><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA0909</dt></dl> | Текущий тип мультимедиа не поддерживается.<br /> | 
| <span id="E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_erase_recorder_not_supported"></span><dl><dt><strong>E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AA090A</dt></dl> | Это устройство не поддерживает операции, необходимые для этого формата диска.<br /> | 
| <span id="E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_erase_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID</strong></dt><dt>(HRESULT) 0xC0AA090B</dt></dl> | Недопустимое имя клиента.<br /> | 




Следующие коды успеха и ошибки определены в Imapi2fserror. h.




| Константа/значение | Описание | 
|----------------|-------------|
| <span id="IMAPI_E_FSI_INTERNAL_ERROR"></span><span id="imapi_e_fsi_internal_error"></span><dl><dt><strong>IMAPI_E_FSI_INTERNAL_ERROR</strong></dt><dt>(HRESULT) 0xC0AAB100</dt></dl> | Произошла внутренняя ошибка: %1! ls!.<br /> | 
| <span id="IMAPI_E_INVALID_PARAM"></span><span id="imapi_e_invalid_param"></span><dl><dt><strong>IMAPI_E_INVALID_PARAM</strong></dt><dt>(HRESULT) 0xC0AAB101</dt></dl> | Значение, указанное для параметра "%1! ls!" , недопустим.<br /> | 
| <span id="IMAPI_E_READONLY"></span><span id="imapi_e_readonly"></span><dl><dt><strong>IMAPI_E_READONLY</strong></dt><dt>(HRESULT) 0xC0AAB102</dt></dl> | Объект Филесистемимаже находится в режиме только для чтения.<br /> | 
| <span id="IMAPI_E_NO_OUTPUT"></span><span id="imapi_e_no_output"></span><dl><dt><strong>IMAPI_E_NO_OUTPUT</strong></dt><dt>(HRESULT) 0xC0AAB103</dt></dl> | Не указана выходная файловая система.<br /> | 
| <span id="IMAPI_E_INVALID_VOLUME_NAME"></span><span id="imapi_e_invalid_volume_name"></span><dl><dt><strong>IMAPI_E_INVALID_VOLUME_NAME</strong></dt><dt>(HRESULT) 0xC0AAB104</dt></dl> | Указанный идентификатор тома либо слишком длинный, либо содержит один или несколько недопустимых символов.<br /> | 
| <span id="IMAPI_E_INVALID_DATE"></span><span id="imapi_e_invalid_date"></span><dl><dt><strong>IMAPI_E_INVALID_DATE</strong></dt><dt>(HRESULT) 0xC0AAB105</dt></dl> | Недопустимые даты файла. %1! Ls! время раньше, чем %2! Ls! времени.<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_NOT_EMPTY"></span><span id="imapi_e_file_system_not_empty"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_EMPTY</strong></dt><dt>(HRESULT) 0xC0AAB106</dt></dl> | Для этой функции файловая система должна быть пустой.<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED"></span><span id="imapi_e_file_system_change_not_allowed"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED</strong></dt><dt>(HRESULT) 0xC0AAB163L</dt></dl> | Невозможно изменить файловую систему, указанную для создания, так как файловая система из импортированного сеанса и файловая система в текущем сеансе не совпадают.<br /> | 
| <span id="IMAPI_E_NOT_FILE"></span><span id="imapi_e_not_file"></span><dl><dt><strong>IMAPI_E_NOT_FILE</strong></dt><dt>(HRESULT) 0xC0AAB108</dt></dl> | Указанный путь "%1! ls!" не определяет файл.<br /> | 
| <span id="IMAPI_E_NOT_DIR"></span><span id="imapi_e_not_dir"></span><dl><dt><strong>IMAPI_E_NOT_DIR</strong></dt><dt>(HRESULT) 0xC0AAB109</dt></dl> | Указанный путь "%1! ls!" не определяет каталог.<br /> | 
| <span id="IMAPI_E_DIR_NOT_EMPTY"></span><span id="imapi_e_dir_not_empty"></span><dl><dt><strong>IMAPI_E_DIR_NOT_EMPTY</strong></dt><dt>(HRESULT) 0xC0AAB10A</dt></dl> | Каталог "%1! s!" не пусто.<br /> | 
| <span id="IMAPI_E_NOT_IN_FILE_SYSTEM"></span><span id="imapi_e_not_in_file_system"></span><dl><dt><strong>IMAPI_E_NOT_IN_FILE_SYSTEM</strong></dt><dt>(HRESULT) 0xC0AAB10B</dt></dl> | ls! ' не является частью файловой системы. Для завершения этой операции необходимо добавить его.<br /> | 
| <span id="IMAPI_E_INVALID_PATH"></span><span id="imapi_e_invalid_path"></span><dl><dt><strong>IMAPI_E_INVALID_PATH</strong></dt><dt>(HRESULT) 0xC0AAB110</dt></dl> | Путь "%1! s!" имеет неправильный формат или содержит недопустимые символы.<br /> | 
| <span id="IMAPI_E_RESTRICTED_NAME_VIOLATION"></span><span id="imapi_e_restricted_name_violation"></span><dl><dt><strong>IMAPI_E_RESTRICTED_NAME_VIOLATION</strong></dt><dt>(HRESULT) 0xC0AAB111</dt></dl> | Имя "%1! ls!" указан недопустимый: имя объекта файла или каталога, созданного при задании свойства Усерестриктедчарактерсет, может содержать только символы ANSI.<br /> | 
| <span id="IMAPI_E_DUP_NAME"></span><span id="imapi_e_dup_name"></span><dl><dt><strong>IMAPI_E_DUP_NAME</strong></dt><dt>(HRESULT) 0xC0AAB112</dt></dl> | ls! ' имя уже существует.<br /> | 
| <span id="IMAPI_E_NO_UNIQUE_NAME"></span><span id="imapi_e_no_unique_name"></span><dl><dt><strong>IMAPI_E_NO_UNIQUE_NAME</strong></dt><dt>(HRESULT) 0xC0AAB113</dt></dl> | Попытка добавить "%1! ls!" Сбой: не удается создать уникальное имя для файловой системы для %2! Ls! .<br /> | 
| <span id="IMAPI_E_ITEM_NOT_FOUND"></span><span id="imapi_e_item_not_found"></span><dl><dt><strong>IMAPI_E_ITEM_NOT_FOUND</strong></dt><dt>(HRESULT) 0xC0AAB118</dt></dl> | Не удается найти элемент "%1! ls!" в иерархии Филесистемимаже.<br /> | 
| <span id="IMAPI_E_FILE_NOT_FOUND"></span><span id="imapi_e_file_not_found"></span><dl><dt><strong>IMAPI_E_FILE_NOT_FOUND</strong></dt><dt>(HRESULT) 0xC0AAB119</dt></dl> | Файл "%1! s!" не найдено в иерархии Филесистемимаже.<br /> | 
| <span id="IMAPI_E_DIR_NOT_FOUND"></span><span id="imapi_e_dir_not_found"></span><dl><dt><strong>IMAPI_E_DIR_NOT_FOUND</strong></dt><dt>(HRESULT) 0xC0AAB11A</dt></dl> | Каталог "%1! s!" не найдено в иерархии Филесистемимаже.<br /> | 
| <span id="IMAPI_E_IMAGE_SIZE_LIMIT"></span><span id="imapi_e_image_size_limit"></span><dl><dt><strong>IMAPI_E_IMAGE_SIZE_LIMIT</strong></dt><dt>(HRESULT) 0xC0AAB120</dt></dl> | Добавление "%1! ls!" приведет к тому, что размер изображения будет больше, чем текущее заданное ограничение.<br /> | 
| <span id="IMAPI_E_IMAGE_TOO_BIG"></span><span id="imapi_e_image_too_big"></span><dl><dt><strong>IMAPI_E_IMAGE_TOO_BIG</strong></dt><dt>(HRESULT) 0xC0AAB121</dt></dl> | Значение, указанное для свойства Фримедиаблоккс, слишком мало для предполагаемого размера изображения на основе текущих данных. <br /> | 
| <span id="IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED"></span><span id="imapi_e_imagemanager_image_not_aligned"></span><dl><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED</strong></dt><dt>(HRESULT) 0xC0AAB200L</dt></dl> | Изображение не согласуется на границе сектора 2 КБ.<br /> | 
| <span id="IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND"></span><span id="imapi_e_imagemanager_no_valid_vd_found"></span><dl><dt><strong>IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND</strong></dt><dt>(HRESULT) 0xC0AAB201L)</dt></dl> | Образ не содержит допустимый дескриптор тома.<br /> | 
| <span id="IMAPI_E_IMAGEMANAGER_NO_IMAGE"></span><span id="imapi_e_imagemanager_no_image"></span><dl><dt><strong>IMAPI_E_IMAGEMANAGER_NO_IMAGE</strong></dt><dt>(HRESULT) 0xC0AAB202L</dt></dl> | Образ не был задан с помощью методов <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath"><strong>иисоимажеманажер:: сетпас</strong></a> или <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream"><strong>Иисоимажеманажер:: сетстреам</strong></a> до вызова метода <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-validate"><strong>иисоимажеманажер:: Validate</strong></a> .<br /> | 
| <span id="IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG"></span><span id="imapi_e_imagemanager_image_too_big"></span><dl><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG</strong></dt><dt>(HRESULT) 0xC0AAB203L</dt></dl> | Указанный образ слишком велик для проверки, так как размер превышает <strong>макслонг</strong>.<br /> | 
| <span id="IMAPI_E_DATA_STREAM_INCONSISTENCY"></span><span id="imapi_e_data_stream_inconsistency"></span><dl><dt><strong>IMAPI_E_DATA_STREAM_INCONSISTENCY</strong></dt><dt>(HRESULT) 0xC0AAB128</dt></dl> | Поток данных, указанный для файла "%1! ls!" не согласуется: ожидается %2! I64d! байт, Найдено %3! I64d!. <br /> | 
| <span id="IMAPI_E_DATA_STREAM_READ_FAILURE"></span><span id="imapi_e_data_stream_read_failure"></span><dl><dt><strong>IMAPI_E_DATA_STREAM_READ_FAILURE</strong></dt><dt>(HRESULT) 0xC0AAB129</dt></dl> | Не удается считать данные из потока, переданного для файла "%1! ls!".<br /> | 
| <span id="IMAPI_E_DATA_STREAM_CREATE_FAILURE"></span><span id="imapi_e_data_stream_create_failure"></span><dl><dt><strong>IMAPI_E_DATA_STREAM_CREATE_FAILURE</strong></dt><dt>(HRESULT) 0xC0AAB12A</dt></dl> | При попытке создать поток данных для файла "%1! ls!" произошла следующая ошибка: <br /> | 
| <span id="IMAPI_E_DIRECTORY_READ_FAILURE"></span><span id="imapi_e_directory_read_failure"></span><dl><dt><strong>IMAPI_E_DIRECTORY_READ_FAILURE</strong></dt><dt>(HRESULT) 0xC0AAB12BL</dt></dl> | Не удалось перечислить файлы в дереве каталогов из-за наличия разрешений.<br /> | 
| <span id="IMAPI_E_TOO_MANY_DIRS"></span><span id="imapi_e_too_many_dirs"></span><dl><dt><strong>IMAPI_E_TOO_MANY_DIRS</strong></dt><dt>(HRESULT) 0xC0AAB130</dt></dl> | Этот образ файловой системы имеет слишком много каталогов для %1! Ls! .<br /> | 
| <span id="IMAPI_E_ISO9660_LEVELS"></span><span id="imapi_e_iso9660_levels"></span><dl><dt><strong>IMAPI_E_ISO9660_LEVELS</strong></dt><dt>(HRESULT) 0xC0AAB131</dt></dl> | ISO9660 ограничено 8 уровнями каталогов.<br /> | 
| <span id="IMAPI_E_DATA_TOO_BIG"></span><span id="imapi_e_data_too_big"></span><dl><dt><strong>IMAPI_E_DATA_TOO_BIG</strong></dt><dt>(HRESULT) 0xC0AAB132</dt></dl> | Слишком большой файл данных для "%1! ls!" .<br /> | 
| <span id="IMAPI_E_STASHFILE_OPEN_FAILURE"></span><span id="imapi_e_stashfile_open_failure"></span><dl><dt><strong>IMAPI_E_STASHFILE_OPEN_FAILURE</strong></dt><dt>(HRESULT) 0xC0AAB138</dt></dl> | Не удается инициализировать %1! Ls! скрытый файл.<br /> | 
| <span id="IMAPI_E_STASHFILE_SEEK_FAILURE"></span><span id="imapi_e_stashfile_seek_failure"></span><dl><dt><strong>IMAPI_E_STASHFILE_SEEK_FAILURE</strong></dt><dt>(HRESULT) 0xC0AAB139</dt></dl> | Поиск ошибок в "%1! ls!" скрытый файл.<br /> | 
| <span id="IMAPI_E_STASHFILE_WRITE_FAILURE"></span><span id="imapi_e_stashfile_write_failure"></span><dl><dt><strong>IMAPI_E_STASHFILE_WRITE_FAILURE</strong></dt><dt>(HRESULT) 0xC0AAB13A</dt></dl> | Произошла ошибка при записи в "%1! ls!" скрытый файл.<br /> | 
| <span id="IMAPI_E_STASHFILE_READ_FAILURE"></span><span id="imapi_e_stashfile_read_failure"></span><dl><dt><strong>IMAPI_E_STASHFILE_READ_FAILURE</strong></dt><dt>(HRESULT) 0xC0AAB13B</dt></dl> | Произошла ошибка при чтении из "%1! ls!" скрытый файл.<br /> | 
| <span id="IMAPI_E_INVALID_WORKING_DIRECTORY"></span><span id="imapi_e_invalid_working_directory"></span><dl><dt><strong>IMAPI_E_INVALID_WORKING_DIRECTORY</strong></dt><dt>(HRESULT) 0xC0AAB140</dt></dl> | Рабочий каталог "%1! ls!" , недопустим.<br /> | 
| <span id="IMAPI_E_WORKING_DIRECTORY_SPACE"></span><span id="imapi_e_working_directory_space"></span><dl><dt><strong>IMAPI_E_WORKING_DIRECTORY_SPACE</strong></dt><dt>(HRESULT) 0xC0AAB141</dt></dl> | Не удается задать для рабочего каталога значение "%1! ls!". Доступное место: %2! I64d! байт, приблизительно %3! I64d! требуемые байты. <br /> | 
| <span id="IMAPI_E_STASHFILE_MOVE"></span><span id="imapi_e_stashfile_move"></span><dl><dt><strong>IMAPI_E_STASHFILE_MOVE</strong></dt><dt>(HRESULT) 0xC0AAB142</dt></dl> | Попытка переместить скрытый файл данных в каталог "%1! ls!" не выполнено.<br /> | 
| <span id="IMAPI_E_BOOT_IMAGE_DATA"></span><span id="imapi_e_boot_image_data"></span><dl><dt><strong>IMAPI_E_BOOT_IMAGE_DATA</strong></dt><dt>(HRESULT) 0xC0AAB148</dt></dl> | Не удалось добавить объект загрузки к образу.<br /> | 
| <span id="IMAPI_E_BOOT_OBJECT_CONFLICT"></span><span id="imapi_e_boot_object_conflict"></span><dl><dt><strong>IMAPI_E_BOOT_OBJECT_CONFLICT</strong></dt><dt>(HRESULT) 0xC0AAB149</dt></dl> | Объект загрузки может быть включен только в исходный образ диска.<br /> | 
| <span id="IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH"></span><span id="imapi_e_boot_emulation_image_size_mismatch"></span><dl><dt><strong>IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH</strong></dt><dt>(HRESULT) 0xC0AAB14A</dt></dl> | Запрошенный тип эмуляции не соответствует размеру загрузочного образа.<br /> | 
| <span id="IMAPI_E_EMPTY_DISC"></span><span id="imapi_e_empty_disc"></span><dl><dt><strong>IMAPI_E_EMPTY_DISC</strong></dt><dt>(HRESULT) 0xC0AAB150</dt></dl> | Оптический носитель пуст.<br /> | 
| <span id="IMAPI_E_NO_SUPPORTED_FILE_SYSTEM"></span><span id="imapi_e_no_supported_file_system"></span><dl><dt><strong>IMAPI_E_NO_SUPPORTED_FILE_SYSTEM</strong></dt><dt>(HRESULT) 0xC0AAB151</dt></dl> | Указанный диск не содержит одну из поддерживаемых файловых систем.<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_NOT_FOUND"></span><span id="imapi_e_file_system_not_found"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_FOUND</strong></dt><dt>(HRESULT) 0xC0AAB152</dt></dl> | Указанный диск не содержит "%1! ls!" .<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR"></span><span id="imapi_e_file_system_read_consistency_error"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR</strong></dt><dt>(HRESULT) 0xC0AAB153</dt></dl> | Произошла ошибка согласованности при импорте "%1! ls!" .<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED"></span><span id="imapi_e_file_system_feature_not_supported"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0xC0AAB154</dt></dl> | "%1! ls!" файловая система на выбранном диске содержит функцию, не поддерживаемую для импорта: %2! Ls!.<br /> | 
| <span id="IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY"></span><span id="imapi_e_import_type_collision_file_exists_as_directory"></span><dl><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY</strong></dt><dt>(HRESULT) 0xC0AAB155</dt></dl> | Не удалось импортировать %2! Ls! файловая система с диска. Файл "%1! ls!" уже существует в иерархии образа в качестве каталога.<br /> | 
| <span id="IMAPI_E_IMPORT_SEEK_FAILURE"></span><span id="imapi_e_import_seek_failure"></span><dl><dt><strong>IMAPI_E_IMPORT_SEEK_FAILURE</strong></dt><dt>(HRESULT) 0xC0AAB156</dt></dl> | Не удается найти блок %1! I64d! на исходном диске. <br /> | 
| <span id="IMAPI_E_IMPORT_READ_FAILURE"></span><span id="imapi_e_import_read_failure"></span><dl><dt><strong>IMAPI_E_IMPORT_READ_FAILURE</strong></dt><dt>(HRESULT) 0xC0AAB157</dt></dl> | Сбой импорта из предыдущего сеанса из-за ошибки при чтении блока на носителе (скорее всего, это блок %1! u!).<br /> | 
| <span id="IMAPI_E_DISC_MISMATCH"></span><span id="imapi_e_disc_mismatch"></span><dl><dt><strong>IMAPI_E_DISC_MISMATCH</strong></dt><dt>(HRESULT) 0xC0AAB158</dt></dl> | Текущий диск не совпадает с тем, с которого была импортирована файловая система.<br /> | 
| <span id="IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED"></span><span id="imapi_e_import_media_not_allowed"></span><dl><dt><strong>IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED</strong></dt><dt>(HRESULT) 0xC0AAB159</dt></dl> | IMAPI не позволяет использовать несколько сеансов с текущим типом носителя.<br /> | 
| <span id="IMAPI_E_UDF_NOT_WRITE_COMPATIBLE"></span><span id="imapi_e_udf_not_write_compatible"></span><dl><dt><strong>IMAPI_E_UDF_NOT_WRITE_COMPATIBLE</strong></dt><dt>(HRESULT) 0xC0AAB15A</dt></dl> | IMAPI не может выполнить несколько сеансов с текущим носителем, так как он не поддерживает совместимую редакцию UDF для записи.<br /> | 
| <span id="IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_incompatible_multisession_type"></span><dl><dt><strong>IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE</strong></dt><dt>(HRESULT) 0xC0AAB15B</dt></dl> | IMAPI не поддерживает запрошенный тип многосеансовой связи.<br /> | 
| <span id="IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION"></span><span id="imapi_e_incompatible_previous_session"></span><dl><dt><strong>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</strong></dt><dt>(HRESULT) 0xC0AAB133</dt></dl> | Сбой операции из-за несовместимого макета предыдущего сеанса, импортированного с носителя.<br /> | 
| <span id="IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_no_compatible_multisession_type"></span><dl><dt><strong>IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE</strong></dt><dt>(HRESULT) 0xC0AAB15C</dt></dl> | IMAPI не поддерживает ни одного типа многосеансовой передачи, предоставленного на текущем носителе.<br /><blockquote>[!Note]<br />Метод [<strong>ифилесистемимаже:: импортфилесистем</strong>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) возвращает эту ошибку, если в записывающем устройстве нет носителя.</blockquote><br /> | 
| <span id="IMAPI_E_MULTISESSION_NOT_SET"></span><span id="imapi_e_multisession_not_set"></span><dl><dt><strong>IMAPI_E_MULTISESSION_NOT_SET</strong></dt><dt>(HRESULT) 0xC0AAB15D</dt></dl> | Перед вызовом этого метода необходимо задать свойство Мултисессионинтерфацес.<br /> | 
| <span id="IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE"></span><span id="imapi_e_import_type_collision_directory_exists_as_file"></span><dl><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE</strong></dt><dt>(HRESULT) 0xC0AAB15E</dt></dl> | Не удалось импортировать %2! Ls! файловая система с диска. Каталог "%1! ls!" уже существует в иерархии изображений в качестве файла.<br /> | 
| <span id="IMAPI_E_BAD_MULTISESSION_PARAMETER"></span><span id="imapi_e_bad_multisession_parameter"></span><dl><dt><strong>IMAPI_E_BAD_MULTISESSION_PARAMETER</strong></dt><dt>(HRESULT) 0xC0AAB162</dt></dl> | Один из многосеансовых параметров не может быть получен или имеет неверное значение.<br /> | 
| <span id="IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED"></span><span id="imapi_s_image_feature_not_supported"></span><dl><dt><strong>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</strong></dt><dt>(HRESULT) 0x00AAB15FL</dt></dl> | Эта функция не поддерживается для текущей редакции файловой системы. Образ будет создан без этой функции.<br /> | 




## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                                                                                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                                                                            |
| Заголовок<br/>                   | <dl> <dt>Imapi2error. h; </dt> <dt>Imapi2fserror. h</dt> </dl> |



 

 





