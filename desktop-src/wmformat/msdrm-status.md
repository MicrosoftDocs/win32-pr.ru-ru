---
title: Перечисление MSDRM_STATUS (Вмдрмсдк. h)
description: '\_Тип перечисления состояния Msdrm определяет условия состояния для подсистемы DRM.'
ms.assetid: b26600ea-2603-4fca-9408-2d5c88091dcc
keywords:
- Формат Windows Media MSDRM_STATUS перечисления
- Формат Windows Media для перечисления
topic_type:
- apiref
api_name:
- MSDRM_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2a73de9e33216e22a01966be8f2ed6a3185fdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721023"
---
# <a name="msdrm_status-enumeration"></a><span data-ttu-id="f0ae6-105">\_Перечисление состояния Msdrm</span><span class="sxs-lookup"><span data-stu-id="f0ae6-105">MSDRM\_STATUS enumeration</span></span>

<span data-ttu-id="f0ae6-106">Тип **перечисления \_ состояния Msdrm** определяет условия состояния для подсистемы DRM.</span><span class="sxs-lookup"><span data-stu-id="f0ae6-106">The **MSDRM\_STATUS** enumeration type defines status conditions for the DRM subsystem.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0ae6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0ae6-107">Syntax</span></span>


```C++
typedef enum MSDRM_STATUS { 
  DRM_ERROR                        = 0,
  DRM_INFORMATION                  = 1,
  DRM_BACKUPRESTORE_BEGIN          = 2,
  DRM_BACKUPRESTORE_END            = 3,
  DRM_BACKUPRESTORE_CONNECTING     = 4,
  DRM_BACKUPRESTORE_DISCONNECTING  = 5,
  DRM_ERROR_WITHURL                = 6,
  DRM_RESTRICTED_LICENSE           = 7,
  DRM_NEEDS_INDIVIDUALIZATION      = 8,
  DRM_PLAY_OPL_NOTIFICATION        = 9,
  DRM_COPY_OPL_NOTIFICATION        = 10,
  DRM_REFRESHCRL_COMPLETE          = 11
} ;
```



## <a name="constants"></a><span data-ttu-id="f0ae6-108">Константы</span><span class="sxs-lookup"><span data-stu-id="f0ae6-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f0ae6-109"><span id="DRM_ERROR"></span><span id="drm_error"></span>**\_Ошибка DRM**</span><span class="sxs-lookup"><span data-stu-id="f0ae6-109"><span id="DRM_ERROR"></span><span id="drm_error"></span>**DRM\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="f0ae6-110">Указывает, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="f0ae6-110">Specifies that an error has occurred.</span></span>

</dd> <dt>

<span data-ttu-id="f0ae6-111"><span id="DRM_INFORMATION"></span><span id="drm_information"></span>**\_сведения об DRM**</span><span class="sxs-lookup"><span data-stu-id="f0ae6-111"><span id="DRM_INFORMATION"></span><span id="drm_information"></span>**DRM\_INFORMATION**</span></span>
</dt> <dd>

<span data-ttu-id="f0ae6-112">Указывает, что имеются дополнительные сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="f0ae6-112">Specifies that there is additional status information.</span></span>

</dd> <dt>

<span data-ttu-id="f0ae6-113"><span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**\_Начало БАККУПРЕСТОРЕ \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="f0ae6-113"><span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**DRM\_BACKUPRESTORE\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="f0ae6-114">Указывает, что началась операция резервного копирования или восстановления лицензий.</span><span class="sxs-lookup"><span data-stu-id="f0ae6-114">Specifies that a license backup or restore operation has begun.</span></span>

</dd> <dt>

<span data-ttu-id="f0ae6-115"><span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**\_конец БАККУПРЕСТОРЕ \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="f0ae6-115"><span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**DRM\_BACKUPRESTORE\_END**</span></span>
</dt> <dd>

<span data-ttu-id="f0ae6-116">Указывает, что операция резервного копирования или восстановления лицензий завершилась.</span><span class="sxs-lookup"><span data-stu-id="f0ae6-116">Specifies that a license backup or restore operation has ended.</span></span>

</dd> <dt>

<span data-ttu-id="f0ae6-117"><span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**\_Подключение БАККУПРЕСТОРЕ \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="f0ae6-117"><span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**DRM\_BACKUPRESTORE\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="f0ae6-118">Указывает, что выполняется операция резервного копирования или восстановления лицензий и что клиентский компьютер подключается к резервному серверу.</span><span class="sxs-lookup"><span data-stu-id="f0ae6-118">Specifies that a license backup or restore operation is in progress and that the client computer is connecting with the backup server.</span></span>

</dd> <dt>

<span data-ttu-id="f0ae6-119"><span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**Отсоединение DRM \_ баккупресторе \_**</span><span class="sxs-lookup"><span data-stu-id="f0ae6-119"><span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**DRM\_BACKUPRESTORE\_DISCONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="f0ae6-120">Указывает, что выполняется операция резервного копирования или восстановления лицензий и что клиентский компьютер отключается от резервного сервера.</span><span class="sxs-lookup"><span data-stu-id="f0ae6-120">Specifies that a license backup or restore operation is in progress and that the client computer is disconnecting from the backup server.</span></span>

</dd> <dt>

<span data-ttu-id="f0ae6-121"><span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**\_Ошибка DRM \_ висурл**</span><span class="sxs-lookup"><span data-stu-id="f0ae6-121"><span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**DRM\_ERROR\_WITHURL**</span></span>
</dt> <dd>

<span data-ttu-id="f0ae6-122">Указывает, что операция DRM обнаружила неверный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="f0ae6-122">Specifies that the DRM operation has encountered a bad URL.</span></span>

</dd> <dt>

<span data-ttu-id="f0ae6-123"><span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**\_Лицензия с ограниченными правами DRM \_**</span><span class="sxs-lookup"><span data-stu-id="f0ae6-123"><span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**DRM\_RESTRICTED\_LICENSE**</span></span>
</dt> <dd>

<span data-ttu-id="f0ae6-124">Указывает, что операция DRM не может быть продолжена, так как на клиентском компьютере нет лицензии, предоставляющей требуемое право.</span><span class="sxs-lookup"><span data-stu-id="f0ae6-124">Specifies that the DRM operation cannot continue because no license granting the required right exists on the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="f0ae6-125"><span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM \_ требуется \_ индивидуальность**</span><span class="sxs-lookup"><span data-stu-id="f0ae6-125"><span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM\_NEEDS\_INDIVIDUALIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="f0ae6-126">Указывает, что операция DRM не может быть продолжена, так как подсистема DRM должна быть индивидуальной.</span><span class="sxs-lookup"><span data-stu-id="f0ae6-126">Specifies that the DRM operation cannot continue because the DRM subsystem needs to be individualized.</span></span>

</dd> <dt>

<span data-ttu-id="f0ae6-127"><span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**\_уведомление DRM Play \_ ОПЛ \_**</span><span class="sxs-lookup"><span data-stu-id="f0ae6-127"><span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**DRM\_PLAY\_OPL\_NOTIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="f0ae6-128">Указывает, что операция воспроизведения не может быть завершена, поскольку не выполнены требования к уровню защиты выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f0ae6-128">Specifies that a playback operation cannot be completed because an output protection level requirement has not been met.</span></span>

</dd> <dt>

<span data-ttu-id="f0ae6-129"><span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**\_ \_ уведомление о копировании ОПЛ DRM \_**</span><span class="sxs-lookup"><span data-stu-id="f0ae6-129"><span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**DRM\_COPY\_OPL\_NOTIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="f0ae6-130">Указывает, что операция копирования не может быть завершена, поскольку не выполнены требования к уровню защиты выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f0ae6-130">Specifies that a copy operation cannot be completed because an output protection level requirement has not been met.</span></span>

</dd> <dt>

<span data-ttu-id="f0ae6-131"><span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**\_РЕФРЕШКРЛ DRM \_ завершена**</span><span class="sxs-lookup"><span data-stu-id="f0ae6-131"><span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**DRM\_REFRESHCRL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="f0ae6-132">Указывает, что вызов [**ивмдрмсекурити::P ерформсекуритюпдате**](iwmdrmsecurity-performsecurityupdate.md) завершил обновление списка отзыва.</span><span class="sxs-lookup"><span data-stu-id="f0ae6-132">Specifies that a call to [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) has completed refreshing a revocation list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0ae6-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f0ae6-133">Remarks</span></span>

<span data-ttu-id="f0ae6-134">Нет.</span><span class="sxs-lookup"><span data-stu-id="f0ae6-134">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0ae6-135">Требования</span><span class="sxs-lookup"><span data-stu-id="f0ae6-135">Requirements</span></span>



| <span data-ttu-id="f0ae6-136">Требование</span><span class="sxs-lookup"><span data-stu-id="f0ae6-136">Requirement</span></span> | <span data-ttu-id="f0ae6-137">Значение</span><span class="sxs-lookup"><span data-stu-id="f0ae6-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ae6-138">Header</span><span class="sxs-lookup"><span data-stu-id="f0ae6-138">Header</span></span><br/> | <dl> <span data-ttu-id="f0ae6-139"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0ae6-139"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0ae6-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0ae6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0ae6-141">**Типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="f0ae6-141">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





