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
# <a name="error-codes-specific-to-wcs"></a><span data-ttu-id="5ceae-103">Коды ошибок, характерные для WCS</span><span class="sxs-lookup"><span data-stu-id="5ceae-103">Error Codes Specific To WCS</span></span>

<span data-ttu-id="5ceae-104">Ниже приведен список кодов ошибок, особенно связанных с использованием WCS 1,0.</span><span class="sxs-lookup"><span data-stu-id="5ceae-104">The following is a list of error codes that are specifically related to the use of WCS 1.0.</span></span> <span data-ttu-id="5ceae-105">Это не означает, что функции WCS будут возвращать только эти коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="5ceae-105">This does not mean that WCS functions will return only these error codes.</span></span> <span data-ttu-id="5ceae-106">Это означает, что коды, приведенные в таблице ниже, возвращаются только функциями WCS.</span><span class="sxs-lookup"><span data-stu-id="5ceae-106">It means that the codes in the table below are returned only by WCS functions.</span></span> <span data-ttu-id="5ceae-107">Они также могут возвращать другие коды ошибок Win32, описанные в другом расположении в API Win32 пакета Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="5ceae-107">They may also return other Win32 error codes that are documented elsewhere in the Win32 API of the Platform SDK.</span></span>

<dl> <dt>

<span data-ttu-id="5ceae-108"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>Ошибка при \_ удалении \_ ICM \_ XForm</span><span class="sxs-lookup"><span data-stu-id="5ceae-108"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>ERROR\_DELETING\_ICM\_XFORM</span></span>
</dt> <dd>

<span data-ttu-id="5ceae-109">Не удалось удалить указанное преобразование цвета.</span><span class="sxs-lookup"><span data-stu-id="5ceae-109">The specified color transform could not be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="5ceae-110"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>Ошибка \_ дублирования \_ тега</span><span class="sxs-lookup"><span data-stu-id="5ceae-110"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>ERROR\_DUPLICATE\_TAG</span></span>
</dt> <dd>

<span data-ttu-id="5ceae-111">Указанный тег элемента профиля цвета уже существует в цветом профиле.</span><span class="sxs-lookup"><span data-stu-id="5ceae-111">The specified color profile element tag is already present in the color profile.</span></span>

</dd> <dt>

<span data-ttu-id="5ceae-112"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>Ошибка \_ ICM \_ не \_ включена</span><span class="sxs-lookup"><span data-stu-id="5ceae-112"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>ERROR\_ICM\_NOT\_ENABLED</span></span>
</dt> <dd>

<span data-ttu-id="5ceae-113">Управление цветом изображений в настоящее время не включено.</span><span class="sxs-lookup"><span data-stu-id="5ceae-113">Image Color Management is not currently enabled.</span></span>

</dd> <dt>

<span data-ttu-id="5ceae-114"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>Ошибка \_ недопустимого модуля \_ CMM</span><span class="sxs-lookup"><span data-stu-id="5ceae-114"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>ERROR\_INVALID\_CMM</span></span>
</dt> <dd>

<span data-ttu-id="5ceae-115">Указанное имя файла не ссылается на допустимый модуль управления цветом.</span><span class="sxs-lookup"><span data-stu-id="5ceae-115">The specified file name does not refer to a valid color management module.</span></span>

</dd> <dt>

<span data-ttu-id="5ceae-116"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>Ошибка \_ недопустимого \_ колорспаце</span><span class="sxs-lookup"><span data-stu-id="5ceae-116"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>ERROR\_INVALID\_COLORSPACE</span></span>
</dt> <dd>

<span data-ttu-id="5ceae-117">Указано недопустимое цветовое пространство.</span><span class="sxs-lookup"><span data-stu-id="5ceae-117">The specified color space is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="5ceae-118"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>Ошибка при \_ недопустимом \_ профиле</span><span class="sxs-lookup"><span data-stu-id="5ceae-118"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>ERROR\_INVALID\_PROFILE</span></span>
</dt> <dd>

<span data-ttu-id="5ceae-119">Указанное имя файла не ссылается на допустимый цветовой профиль.</span><span class="sxs-lookup"><span data-stu-id="5ceae-119">The specified file name does not refer to a valid color profile.</span></span>

</dd> <dt>

<span data-ttu-id="5ceae-120"><span id="ERROR_INVALID_TRANSFORM_"></span><span id="error_invalid_transform_"></span>Ошибка \_ недопустимого \_ преобразования</span><span class="sxs-lookup"><span data-stu-id="5ceae-120"><span id="ERROR_INVALID_TRANSFORM_"></span><span id="error_invalid_transform_"></span>ERROR\_INVALID\_TRANSFORM</span></span> 
</dt> <dd>

<span data-ttu-id="5ceae-121">Указанное преобразование цвета не является допустимым преобразованием цвета.</span><span class="sxs-lookup"><span data-stu-id="5ceae-121">The color transform that was specified is not a valid color transform.</span></span>

</dd> <dt>

<span data-ttu-id="5ceae-122"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>\_профиль ошибок \_ не \_ связан \_ с \_ устройством</span><span class="sxs-lookup"><span data-stu-id="5ceae-122"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>ERROR\_PROFILE\_NOT\_ASSOCIATED\_WITH\_DEVICE</span></span>
</dt> <dd>

<span data-ttu-id="5ceae-123">Указанный цветовой профиль не связан ни с одним устройством.</span><span class="sxs-lookup"><span data-stu-id="5ceae-123">The specified color profile is not associated with any device.</span></span>

</dd> <dt>

<span data-ttu-id="5ceae-124"><span id="ERROR_PROFILE_NOT_FOUND_"></span><span id="error_profile_not_found_"></span>\_профиль ошибок \_ не \_ найден</span><span class="sxs-lookup"><span data-stu-id="5ceae-124"><span id="ERROR_PROFILE_NOT_FOUND_"></span><span id="error_profile_not_found_"></span>ERROR\_PROFILE\_NOT\_FOUND</span></span> 
</dt> <dd>

<span data-ttu-id="5ceae-125">Указанное имя файла цветового профиля не найдено.</span><span class="sxs-lookup"><span data-stu-id="5ceae-125">The specified color profile file name was not found.</span></span> <span data-ttu-id="5ceae-126">Неверное имя файла или путь.</span><span class="sxs-lookup"><span data-stu-id="5ceae-126">The file name or path is incorrect.</span></span>

</dd> <dt>

<span data-ttu-id="5ceae-127"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>\_тег ошибки \_ не \_ найден</span><span class="sxs-lookup"><span data-stu-id="5ceae-127"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>ERROR\_TAG\_NOT\_FOUND</span></span>
</dt> <dd>

<span data-ttu-id="5ceae-128">Указанный тег элемента цветового профиля не найден в профиле цвета.</span><span class="sxs-lookup"><span data-stu-id="5ceae-128">The specified color profile element tag was not found in the color profile.</span></span>

</dd> <dt>

<span data-ttu-id="5ceae-129"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>\_тег ошибки \_ отсутствует \_</span><span class="sxs-lookup"><span data-stu-id="5ceae-129"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>ERROR\_TAG\_NOT\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="5ceae-130">Тег элемента цветового профиля, необходимый для завершения функции, не был передан функции.</span><span class="sxs-lookup"><span data-stu-id="5ceae-130">A color profile element tag that is required for the function to succeed was not passed to the function.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="5ceae-131">См. также</span><span class="sxs-lookup"><span data-stu-id="5ceae-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ceae-132">Основные понятия управления цветом</span><span class="sxs-lookup"><span data-stu-id="5ceae-132">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="5ceae-133">Константы WCS</span><span class="sxs-lookup"><span data-stu-id="5ceae-133">WCS Constants</span></span>](wcs-constants.md)
</dt> </dl>

 

 




