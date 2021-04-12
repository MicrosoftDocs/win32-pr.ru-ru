---
title: Перечисление DRM_LICENSE_STATE_CATEGORY (Дрмекстерналс. h)
description: '\_ \_ \_ Тип перечисления Категория состояния лицензии DRM определяет категории для строк лицензии DRM, которые отображаются для пользователя.'
ms.assetid: f5c5aa78-84f9-4ee4-b551-05bf864243ab
keywords:
- Формат Windows Media DRM_LICENSE_STATE_CATEGORY перечисления
- Формат Windows Media для перечисления
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_CATEGORY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40763ec7f610073784e3bd1516d4c955abcd65b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491835"
---
# <a name="drm_license_state_category-enumeration-drmexternalsh"></a><span data-ttu-id="82957-105">Перечисление DRM_LICENSE_STATE_CATEGORY (Дрмекстерналс. h)</span><span class="sxs-lookup"><span data-stu-id="82957-105">DRM_LICENSE_STATE_CATEGORY enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="82957-106">Тип **перечисления \_ \_ \_ Категория состояния лицензии DRM** определяет категории для строк [*лицензии*](wmformat-glossary.md) DRM, которые отображаются для пользователя.</span><span class="sxs-lookup"><span data-stu-id="82957-106">The **DRM\_LICENSE\_STATE\_CATEGORY** enumeration type defines the categories for DRM [*license*](wmformat-glossary.md) strings that are displayed to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="82957-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82957-107">Syntax</span></span>


```C++
typedef enum DRM_LICENSE_STATE_CATEGORY { 
  WM_DRM_LICENSE_STATE_NORIGHT                    = 0,
  WM_DRM_LICENSE_STATE_UNLIM,
  WM_DRM_LICENSE_STATE_COUNT,
  WM_DRM_LICENSE_STATE_FROM,
  WM_DRM_LICENSE_STATE_UNTIL,
  WM_DRM_LICENSE_STATE_FROM_UNTIL,
  WM_DRM_LICENSE_STATE_COUNT_FROM,
  WM_DRM_LICENSE_STATE_COUNT_UNTIL,
  WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL,
  WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE
} ;
```



## <a name="constants"></a><span data-ttu-id="82957-108">Константы</span><span class="sxs-lookup"><span data-stu-id="82957-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="82957-109"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**\_ \_ \_ неправильное состояние \_ лицензии WM DRM**</span><span class="sxs-lookup"><span data-stu-id="82957-109"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM\_DRM\_LICENSE\_STATE\_NORIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="82957-110">Указывает, что строка примет форму "Воспроизведение запрещено".</span><span class="sxs-lookup"><span data-stu-id="82957-110">Indicates the string will take the form "Playback not permitted."</span></span>

</dd> <dt>

<span data-ttu-id="82957-111"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**\_ \_ \_ УНЛИМ состояния лицензии WM \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="82957-111"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM\_DRM\_LICENSE\_STATE\_UNLIM**</span></span>
</dt> <dd>

<span data-ttu-id="82957-112">Указывает, что строка будет иметь форму "воспроизведение неограниченна".</span><span class="sxs-lookup"><span data-stu-id="82957-112">Indicates the string will take the form "Playback unlimited."</span></span>

</dd> <dt>

<span data-ttu-id="82957-113"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**\_ \_ \_ число состояний лицензий WM \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="82957-113"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT**</span></span>
</dt> <dd>

<span data-ttu-id="82957-114">Указывает, что строка примет форму "воспроизведение допустима 5 раз".</span><span class="sxs-lookup"><span data-stu-id="82957-114">Indicates the string will take the form "Playback valid 5 times."</span></span>

</dd> <dt>

<span data-ttu-id="82957-115"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_ \_ Состояние лицензии WM \_ DRM \_ из**</span><span class="sxs-lookup"><span data-stu-id="82957-115"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**WM\_DRM\_LICENSE\_STATE\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="82957-116">Указывает, что строка примет форму "воспроизведение допустимого из 7/12/00".</span><span class="sxs-lookup"><span data-stu-id="82957-116">Indicates the string will take the form "Playback valid from 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="82957-117"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**\_ \_ Состояние лицензии WM \_ DRM \_ до**</span><span class="sxs-lookup"><span data-stu-id="82957-117"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM\_DRM\_LICENSE\_STATE\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="82957-118">Указывает, что строка примет вид "допустимое воспроизведение до 7/12/00".</span><span class="sxs-lookup"><span data-stu-id="82957-118">Indicates the string will take the form "Playback valid until 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="82957-119"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ Состояние лицензии WM \_ DRM \_ с \_ до**</span><span class="sxs-lookup"><span data-stu-id="82957-119"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="82957-120">Указывает, что строка примет форму "воспроизведение допустимого из 5/12 в 9/12".</span><span class="sxs-lookup"><span data-stu-id="82957-120">Indicates the string will take the form "Playback valid from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="82957-121"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_ \_ \_ число состояний лицензий WM \_ DRM \_ из**</span><span class="sxs-lookup"><span data-stu-id="82957-121"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="82957-122">Указывает, что строка примет форму «воспроизведение допустимого воспроизведения 5 раз с 5/12 по 9/12».</span><span class="sxs-lookup"><span data-stu-id="82957-122">Indicates the string will take the form "Playback valid 5 times from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="82957-123"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**\_ \_ \_ число состояний лицензий WM \_ DRM \_ до**</span><span class="sxs-lookup"><span data-stu-id="82957-123"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="82957-124">Указывает, что строка примет форму «воспроизведение допустимого воспроизведения 5 раз до 7/12/00».</span><span class="sxs-lookup"><span data-stu-id="82957-124">Indicates the string will take the form "Playback valid 5 times until 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="82957-125"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_ \_ число состояний лицензий WM DRM \_ \_ \_ от \_ до**</span><span class="sxs-lookup"><span data-stu-id="82957-125"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="82957-126">Указывает, что строка примет форму «воспроизведение допустимого воспроизведения 5 раз с 5/12 по 9/12».</span><span class="sxs-lookup"><span data-stu-id="82957-126">Indicates the string will take the form "Playback valid 5 times from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="82957-127"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**\_ \_ срок действия лицензии WM DRM \_ \_ \_ после \_ фирстусе**</span><span class="sxs-lookup"><span data-stu-id="82957-127"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**WM\_DRM\_LICENSE\_STATE\_EXPIRATION\_AFTER\_FIRSTUSE**</span></span>
</dt> <dd>

<span data-ttu-id="82957-128">Указывает, что строка примет форму "воспроизведение допустимого в течение 24 часов после первого использования".</span><span class="sxs-lookup"><span data-stu-id="82957-128">Indicates the string will take the form "Playback valid for 24 hours from first use."</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82957-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82957-129">Remarks</span></span>

<span data-ttu-id="82957-130">Это перечисление указывает категорию для каждой возможной отображаемой выходной строки.</span><span class="sxs-lookup"><span data-stu-id="82957-130">This enumeration indicates the category for each possible output string to be displayed.</span></span> <span data-ttu-id="82957-131">Он является членом структуры [**данных о \_ \_ состоянии лицензии \_ DRM**](drm-license-state-data.md) .</span><span class="sxs-lookup"><span data-stu-id="82957-131">It is a member of the [**DRM\_LICENSE\_STATE\_DATA**](drm-license-state-data.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="82957-132">Требования</span><span class="sxs-lookup"><span data-stu-id="82957-132">Requirements</span></span>



| <span data-ttu-id="82957-133">Требование</span><span class="sxs-lookup"><span data-stu-id="82957-133">Requirement</span></span> | <span data-ttu-id="82957-134">Значение</span><span class="sxs-lookup"><span data-stu-id="82957-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="82957-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82957-135">Minimum supported client</span></span><br/> | <span data-ttu-id="82957-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="82957-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="82957-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82957-137">Minimum supported server</span></span><br/> | <span data-ttu-id="82957-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="82957-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="82957-139">Версия</span><span class="sxs-lookup"><span data-stu-id="82957-139">Version</span></span><br/>                  | <span data-ttu-id="82957-140">Пакет SDK для Windows Media Format 7 или более поздние версии пакета SDK</span><span class="sxs-lookup"><span data-stu-id="82957-140">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="82957-141">Header</span><span class="sxs-lookup"><span data-stu-id="82957-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="82957-142"><dt>Дрмекстерналс. h</dt></span><span class="sxs-lookup"><span data-stu-id="82957-142"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82957-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82957-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82957-144">**Типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="82957-144">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





