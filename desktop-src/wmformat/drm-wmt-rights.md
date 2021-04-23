---
title: Перечисление WMT_RIGHTS (Вмдрмсдк. h)
description: Определяет права, которые могут быть указаны в лицензии DRM.
ms.assetid: 9c034ca0-83e9-4a4c-8e98-96e2a95fd97c
keywords:
- Формат Windows Media WMT_RIGHTS перечисления
- Формат Windows Media для перечисления
topic_type:
- apiref
api_name:
- WMT_RIGHTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644cff9c94876fab11bc9fbe181ac0375d9444fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704047"
---
# <a name="wmt_rights-enumeration"></a><span data-ttu-id="48dd0-105">\_Перечисление прав ВМТ</span><span class="sxs-lookup"><span data-stu-id="48dd0-105">WMT\_RIGHTS enumeration</span></span>

<span data-ttu-id="48dd0-106">Тип **перечисления \_ Rights ВМТ** определяет права, которые могут быть указаны в лицензии DRM.</span><span class="sxs-lookup"><span data-stu-id="48dd0-106">The **WMT\_RIGHTS** enumeration type defines the rights that may be specified in a DRM license.</span></span>

## <a name="syntax"></a><span data-ttu-id="48dd0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48dd0-107">Syntax</span></span>


```C++
typedef enum WMT_RIGHTS { 
  WMT_RIGHT_PLAYBACK                 = 0x00000001,
  WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE  = 0x00000002,
  WMT_RIGHT_COPY_TO_CD               = 0x00000008,
  WMT_RIGHT_COPY_TO_SDMI_DEVICE      = 0x00000010,
  WMT_RIGHT_ONE_TIME                 = 0x00000020,
  WMT_RIGHT_SAVE_STREAM_PROTECTED    = 0x00000040,
  WMT_RIGHT_COPY                     = 0x00000080,
  WMT_RIGHT_COLLABORATIVE_PLAY       = 0x00000100,
  WMT_RIGHT_SDMI_TRIGGER             = 0x00010000,
  WMT_RIGHT_SDMI_NOMORECOPIES        = 0x00020000
} ;
```



## <a name="constants"></a><span data-ttu-id="48dd0-108">Константы</span><span class="sxs-lookup"><span data-stu-id="48dd0-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="48dd0-109"><span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**\_Воспроизведение ВМТ вправо \_**</span><span class="sxs-lookup"><span data-stu-id="48dd0-109"><span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**WMT\_RIGHT\_PLAYBACK**</span></span>
</dt> <dd>

<span data-ttu-id="48dd0-110">Указывает право на воспроизведение содержимого без ограничений.</span><span class="sxs-lookup"><span data-stu-id="48dd0-110">Specifies the right to play content without restriction.</span></span>

</dd> <dt>

<span data-ttu-id="48dd0-111"><span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**ВМТ \_ правую \_ копию \_ на \_ устройство, отличное от \_ SDMI \_**</span><span class="sxs-lookup"><span data-stu-id="48dd0-111"><span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="48dd0-112">Указывает право на копирование содержимого на устройство, не соответствующее инициативе защиты цифровой музыки (SDMI).</span><span class="sxs-lookup"><span data-stu-id="48dd0-112">Specifies the right to copy content to a device not compliant with the Secure Digital Music Initiative (SDMI).</span></span>

</dd> <dt>

<span data-ttu-id="48dd0-113"><span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**ВМТ \_ правую \_ копию \_ на \_ компакт-диск**</span><span class="sxs-lookup"><span data-stu-id="48dd0-113"><span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**WMT\_RIGHT\_COPY\_TO\_CD**</span></span>
</dt> <dd>

<span data-ttu-id="48dd0-114">Указывает право на копирование содержимого на компакт-диск.</span><span class="sxs-lookup"><span data-stu-id="48dd0-114">Specifies the right to copy content to a CD.</span></span>

</dd> <dt>

<span data-ttu-id="48dd0-115"><span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**\_Копировать ВМТ \_ вправо \_ на \_ \_ устройство SDMI**</span><span class="sxs-lookup"><span data-stu-id="48dd0-115"><span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**WMT\_RIGHT\_COPY\_TO\_SDMI\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="48dd0-116">Указывает право на копирование содержимого на устройство, совместимое с SDMI.</span><span class="sxs-lookup"><span data-stu-id="48dd0-116">Specifies the right to copy content to a device compliant with the SDMI.</span></span>

</dd> <dt>

<span data-ttu-id="48dd0-117"><span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**ВМТ \_ прямо в \_ один \_ раз**</span><span class="sxs-lookup"><span data-stu-id="48dd0-117"><span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT\_RIGHT\_ONE\_TIME**</span></span>
</dt> <dd>

<span data-ttu-id="48dd0-118">Указывает право на воспроизведение содержимого только один раз.</span><span class="sxs-lookup"><span data-stu-id="48dd0-118">Specifies the right to play content one time only.</span></span>

</dd> <dt>

<span data-ttu-id="48dd0-119"><span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**ВМТ, \_ право на \_ Сохранение \_ \_ защищенного потока**</span><span class="sxs-lookup"><span data-stu-id="48dd0-119"><span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**WMT\_RIGHT\_SAVE\_STREAM\_PROTECTED**</span></span>
</dt> <dd>

<span data-ttu-id="48dd0-120">Указывает право на сохранение содержимого с сервера.</span><span class="sxs-lookup"><span data-stu-id="48dd0-120">Specifies the right to save content from a server.</span></span>

</dd> <dt>

<span data-ttu-id="48dd0-121"><span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**ВМТ \_ правая \_ копия**</span><span class="sxs-lookup"><span data-stu-id="48dd0-121"><span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**WMT\_RIGHT\_COPY**</span></span>
</dt> <dd>

<span data-ttu-id="48dd0-122">Указывает право на копирование содержимого.</span><span class="sxs-lookup"><span data-stu-id="48dd0-122">Specifies the right to copy content.</span></span> <span data-ttu-id="48dd0-123">Windows Media DRM 10 регулирует устройства, на которых можно скопировать содержимое, с помощью уровней защиты выходных данных (Оплс).</span><span class="sxs-lookup"><span data-stu-id="48dd0-123">Windows Media DRM 10 regulates the devices to which the content can be copied by using output protection levels (OPLs).</span></span>

</dd> <dt>

<span data-ttu-id="48dd0-124"><span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**ВМТ в \_ прямом \_ сотрудничестве \_**</span><span class="sxs-lookup"><span data-stu-id="48dd0-124"><span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**WMT\_RIGHT\_COLLABORATIVE\_PLAY**</span></span>
</dt> <dd>

<span data-ttu-id="48dd0-125">Указывает право на воспроизведение содержимого в рамках интерактивного сценария, в котором несколько участников могут добавлять песни из коллекции в общий список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="48dd0-125">Specifies the right to play content as part of an online scenario where multiple participants can contribute songs from their collection to a shared playlist.</span></span>

</dd> <dt>

<span data-ttu-id="48dd0-126"><span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**ВМТ \_ правый \_ SDMI \_**</span><span class="sxs-lookup"><span data-stu-id="48dd0-126"><span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**WMT\_RIGHT\_SDMI\_TRIGGER**</span></span>
</dt> <dd>

<span data-ttu-id="48dd0-127">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="48dd0-127">Reserved for future use.</span></span> <span data-ttu-id="48dd0-128">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="48dd0-128">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="48dd0-129"><span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**ВМТ \_ \_ SDMI \_ номорекопиес**</span><span class="sxs-lookup"><span data-stu-id="48dd0-129"><span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**WMT\_RIGHT\_SDMI\_NOMORECOPIES**</span></span>
</dt> <dd>

<span data-ttu-id="48dd0-130">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="48dd0-130">Reserved for future use.</span></span> <span data-ttu-id="48dd0-131">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="48dd0-131">Do not use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48dd0-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="48dd0-132">Remarks</span></span>

<span data-ttu-id="48dd0-133">Эти значения являются битовыми флагами, поэтому один или несколько можно задать, объединив их с оператором побитового **или** .</span><span class="sxs-lookup"><span data-stu-id="48dd0-133">These values are bit flags, so one or more can be set by combining them with the bitwise **OR** operator.</span></span>

<span data-ttu-id="48dd0-134">При использовании Windows Media DRM 10 **ВМТ \_ \_ Копировать \_ на устройство, \_ не \_ \_** использующее SDMI, **ВМТ \_ правую \_ копию \_ на SDMI- \_ \_ устройство**, а **ВМТ \_ право \_ Копировать \_ на \_ CD** заменяется **ВМТ \_ правой \_ копией**.</span><span class="sxs-lookup"><span data-stu-id="48dd0-134">When using Windows Media DRM 10, **WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE**, **WMT\_RIGHT\_COPY\_TO\_SDMI\_DEVICE**, and **WMT\_RIGHT\_COPY\_TO\_CD** are superseded by **WMT\_RIGHT\_COPY**.</span></span> <span data-ttu-id="48dd0-135">Ограничения на устройства, на которые может копироваться содержимое, указываются с помощью уровней защиты выходных данных (Оплс).</span><span class="sxs-lookup"><span data-stu-id="48dd0-135">Limitations on the devices to which the content may be copied are specified by using output protection levels (OPLs).</span></span>

## <a name="requirements"></a><span data-ttu-id="48dd0-136">Требования</span><span class="sxs-lookup"><span data-stu-id="48dd0-136">Requirements</span></span>



| <span data-ttu-id="48dd0-137">Требование</span><span class="sxs-lookup"><span data-stu-id="48dd0-137">Requirement</span></span> | <span data-ttu-id="48dd0-138">Значение</span><span class="sxs-lookup"><span data-stu-id="48dd0-138">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48dd0-139">Header</span><span class="sxs-lookup"><span data-stu-id="48dd0-139">Header</span></span><br/> | <dl> <span data-ttu-id="48dd0-140"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="48dd0-140"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48dd0-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48dd0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48dd0-142">**Типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="48dd0-142">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





