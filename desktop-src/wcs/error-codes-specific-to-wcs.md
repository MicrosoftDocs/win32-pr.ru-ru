---
title: Коды ошибок, характерные для WCS
description: Ниже приведен список кодов ошибок, особенно связанных с использованием WCS 1,0.
ms.assetid: c6a0cacc-f83e-4f5c-9002-7718bb2ffb6c
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3040f462ce226ebd3018070abc818884cee6ad6
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/02/2021
ms.locfileid: "105719853"
---
# <a name="error-codes-specific-to-wcs"></a>Коды ошибок, характерные для WCS

Ниже приведен список кодов ошибок, особенно связанных с использованием WCS 1,0. Это не означает, что функции WCS будут возвращать только эти коды ошибок. Это означает, что коды, приведенные в таблице ниже, возвращаются только функциями WCS. Они также могут возвращать другие коды ошибок Win32, описанные в другом расположении в API Win32 пакета Platform SDK.

<dl> <dt>

<span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>Ошибка при \_ удалении \_ ICM \_ XForm
</dt> <dd>

Не удалось удалить указанное преобразование цвета.

</dd> <dt>

<span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>Ошибка \_ дублирования \_ тега
</dt> <dd>

Указанный тег элемента профиля цвета уже существует в цветом профиле.

</dd> <dt>

<span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>Ошибка \_ ICM \_ не \_ включена
</dt> <dd>

Управление цветом изображений в настоящее время не включено.

</dd> <dt>

<span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>Ошибка \_ недопустимого модуля \_ CMM
</dt> <dd>

Указанное имя файла не ссылается на допустимый модуль управления цветом.

</dd> <dt>

<span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>Ошибка \_ недопустимого \_ колорспаце
</dt> <dd>

Указано недопустимое цветовое пространство.

</dd> <dt>

<span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>Ошибка при \_ недопустимом \_ профиле
</dt> <dd>

Указанное имя файла не ссылается на допустимый цветовой профиль.

</dd> <dt>

<span id="ERROR_INVALID_TRANSFORM_"></span><span id="error_invalid_transform_"></span>Ошибка \_ недопустимого \_ преобразования 
</dt> <dd>

Указанное преобразование цвета не является допустимым преобразованием цвета.

</dd> <dt>

<span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>\_профиль ошибок \_ не \_ связан \_ с \_ устройством
</dt> <dd>

Указанный цветовой профиль не связан ни с одним устройством.

</dd> <dt>

<span id="ERROR_PROFILE_NOT_FOUND_"></span><span id="error_profile_not_found_"></span>\_профиль ошибок \_ не \_ найден 
</dt> <dd>

Указанное имя файла цветового профиля не найдено. Неверное имя файла или путь.

</dd> <dt>

<span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>\_тег ошибки \_ не \_ найден
</dt> <dd>

Указанный тег элемента цветового профиля не найден в профиле цвета.

</dd> <dt>

<span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>\_тег ошибки \_ отсутствует \_
</dt> <dd>

Тег элемента цветового профиля, необходимый для завершения функции, не был передан функции.

</dd> </dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[Основные понятия управления цветом](basic-color-management-concepts.md)
</dt> <dt>

[Константы WCS](wcs-constants.md)
</dt> </dl>

 

 




