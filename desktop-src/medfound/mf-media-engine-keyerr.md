---
description: Определяет коды ошибок ключа носителя для механизма мультимедиа.
ms.assetid: F6E13260-74A2-40D0-A704-4E1CDB16B8D8
title: Перечисление MF_MEDIA_ENGINE_KEYERR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_KEYERR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 22dd22a7771f5d1e9466709f0b0da9ee936ef2b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351345"
---
# <a name="mf_media_engine_keyerr-enumeration"></a><span data-ttu-id="cf36d-103">\_ \_ Перечисление кэйерр для механизма передачи мультимедиа MF \_</span><span class="sxs-lookup"><span data-stu-id="cf36d-103">MF\_MEDIA\_ENGINE\_KEYERR enumeration</span></span>

<span data-ttu-id="cf36d-104">Определяет коды ошибок ключа носителя для механизма мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cf36d-104">Defines media key error codes for the media engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf36d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf36d-105">Syntax</span></span>


```C++
typedef enum _MF_MEDIA_ENGINE_KEYERR { 
  MF_MEDIAENGINE_KEYERR_UNKNOWN          = 1,
  MF_MEDIAENGINE_KEYERR_CLIENT           = 2,
  MF_MEDIAENGINE_KEYERR_SERVICE          = 3,
  MF_MEDIAENGINE_KEYERR_OUTPUT           = 4,
  MF_MEDIAENGINE_KEYERR_HARDWARECHANGE   = 5,
  MF_MEDIAENGINE_KEYERR_DOMAIN           = 6
} MF_MEDIA_ENGINE_KEYERR;
```



## <a name="constants"></a><span data-ttu-id="cf36d-106">Константы</span><span class="sxs-lookup"><span data-stu-id="cf36d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cf36d-107"><span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF \_ медиаенгине \_ кэйерр \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="cf36d-107"><span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF\_MEDIAENGINE\_KEYERR\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="cf36d-108">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="cf36d-108">Unknown error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="cf36d-109"><span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**\_клиент MF медиаенгине \_ кэйерр \_**</span><span class="sxs-lookup"><span data-stu-id="cf36d-109"><span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**MF\_MEDIAENGINE\_KEYERR\_CLIENT**</span></span>
</dt> <dd>

<span data-ttu-id="cf36d-110">Произошла ошибка клиента.</span><span class="sxs-lookup"><span data-stu-id="cf36d-110">An error with the client occurred.</span></span>

</dd> <dt>

<span data-ttu-id="cf36d-111"><span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**\_Служба MF медиаенгине \_ кэйерр \_**</span><span class="sxs-lookup"><span data-stu-id="cf36d-111"><span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**MF\_MEDIAENGINE\_KEYERR\_SERVICE**</span></span>
</dt> <dd>

<span data-ttu-id="cf36d-112">Произошла ошибка службы.</span><span class="sxs-lookup"><span data-stu-id="cf36d-112">An error with the service occurred.</span></span>

</dd> <dt>

<span data-ttu-id="cf36d-113"><span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**\_ \_ выходные данные MF медиаенгине кэйерр \_**</span><span class="sxs-lookup"><span data-stu-id="cf36d-113"><span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**MF\_MEDIAENGINE\_KEYERR\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="cf36d-114">Произошла ошибка в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cf36d-114">An error with the output occurred.</span></span>

</dd> <dt>

<span data-ttu-id="cf36d-115"><span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF \_ медиаенгине \_ кэйерр \_ хардваречанже**</span><span class="sxs-lookup"><span data-stu-id="cf36d-115"><span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF\_MEDIAENGINE\_KEYERR\_HARDWARECHANGE**</span></span> 
</dt> <dd>

<span data-ttu-id="cf36d-116">Произошла ошибка, связанная с изменением оборудования.</span><span class="sxs-lookup"><span data-stu-id="cf36d-116">An error occurred related to a hardware change.</span></span>

</dd> <dt>

<span data-ttu-id="cf36d-117"><span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**\_медиаенгине \_ кэйерр, \_ домен**</span><span class="sxs-lookup"><span data-stu-id="cf36d-117"><span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**MF\_MEDIAENGINE\_KEYERR\_DOMAIN**</span></span>
</dt> <dd>

<span data-ttu-id="cf36d-118">Произошла ошибка в домене.</span><span class="sxs-lookup"><span data-stu-id="cf36d-118">An error with the domain occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf36d-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf36d-119">Remarks</span></span>

<span data-ttu-id="cf36d-120">**MF \_ MEDIA \_ Engine \_ кэйерр** используется с параметром *Code* [**имфмедиакэйсессионнотифи:: кэйеррор**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) и значением *Code* , возвращенным методом [**имфмедиакэйсессион::-Error**](imfmediakeysession-geterror.md).</span><span class="sxs-lookup"><span data-stu-id="cf36d-120">**MF\_MEDIA\_ENGINE\_KEYERR** is used with the *code* parameter of [**IMFMediaKeySessionNotify::KeyError**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) and the *code* value returned from [**IMFMediaKeySession::GetError**](imfmediakeysession-geterror.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf36d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="cf36d-121">Requirements</span></span>



| <span data-ttu-id="cf36d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="cf36d-122">Requirement</span></span> | <span data-ttu-id="cf36d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="cf36d-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf36d-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf36d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cf36d-125">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cf36d-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cf36d-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf36d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cf36d-127">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cf36d-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="cf36d-128">IDL</span><span class="sxs-lookup"><span data-stu-id="cf36d-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cf36d-129"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cf36d-129"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf36d-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf36d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf36d-131">Перечисления Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cf36d-131">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




