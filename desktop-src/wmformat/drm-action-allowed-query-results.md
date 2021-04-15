---
title: Перечисление DRM_ACTION_ALLOWED_QUERY_RESULTS (Вмдрмсдк. h)
description: '\_ \_ \_ \_ Тип перечисления Results Action Allowed DRM используется интерфейсом ивмдрмлиценсекуери куеряктионалловед для указания причины, по которой действие не разрешено.'
ms.assetid: dc784cdf-6efe-415b-ba72-eb8fc50bef10
keywords:
- Формат Windows Media DRM_ACTION_ALLOWED_QUERY_RESULTS перечисления
- Формат Windows Media для перечисления
topic_type:
- apiref
api_name:
- DRM_ACTION_ALLOWED_QUERY_RESULTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d1e328acb915bd32547f3455e8556e4caba2360
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669219"
---
# <a name="drm_action_allowed_query_results-enumeration"></a><span data-ttu-id="33a79-105">\_ \_ \_ Перечисление результатов запроса действия DRM Allowed \_</span><span class="sxs-lookup"><span data-stu-id="33a79-105">DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS enumeration</span></span>

<span data-ttu-id="33a79-106">Тип **перечисления \_ \_ \_ \_ Results Action Allowed DRM** используется интерфейсом [**ивмдрмлиценсекуери:: куеряктионалловед**](iwmdrmlicensequery-queryactionallowed.md) , чтобы указать причину, по которой действие не разрешено.</span><span class="sxs-lookup"><span data-stu-id="33a79-106">The **DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS** enumeration type is used by the [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) interface to specify the reason an action is not allowed.</span></span>

## <a name="syntax"></a><span data-ttu-id="33a79-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33a79-107">Syntax</span></span>


```C++
typedef enum DRM_ACTION_ALLOWED_QUERY_RESULTS { 
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED                       = 0x00000001,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE            = 0x00000002,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT              = 0x00000004,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED             = 0x00000008,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED               = 0x00000010,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED           = 0x00000020,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW        = 0x00000040,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV             = 0x00000080,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW      = 0x00000100,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED     = 0x00000200,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT      = 0x00000400,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT   = 0x00000800,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH  = 0x00001000
} ;
```



## <a name="constants"></a><span data-ttu-id="33a79-108">Константы</span><span class="sxs-lookup"><span data-stu-id="33a79-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="33a79-109"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**\_запрос на \_ разрешенное действие DRM \_ \_ не \_ включен**</span><span class="sxs-lookup"><span data-stu-id="33a79-109"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED**</span></span>
</dt> <dd>

<span data-ttu-id="33a79-110">Указывает, что действие "запросы" не разрешено.</span><span class="sxs-lookup"><span data-stu-id="33a79-110">Specifies that the queries action is not allowed.</span></span> <span data-ttu-id="33a79-111">Для действий, которые не разрешены, возвращаемое значение представляет это значение в сочетании с помощью побитового или с одним или несколькими другими значениями в этом перечислении.</span><span class="sxs-lookup"><span data-stu-id="33a79-111">For actions that are not allowed, the returned value is this value combined by using a bitwise OR with one or more of the other values in this enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="33a79-112"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**в \_ \_ запросе разрешено действие DRM \_ \_ не \_ включено \_ ни одной \_ лицензии**</span><span class="sxs-lookup"><span data-stu-id="33a79-112"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_LICENSE**</span></span>
</dt> <dd>

<span data-ttu-id="33a79-113">Указывает, что лицензия для запрошенного содержимого не существует.</span><span class="sxs-lookup"><span data-stu-id="33a79-113">Specifies that a license does not exist for the requested content.</span></span>

</dd> <dt>

<span data-ttu-id="33a79-114"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**\_запрос с \_ разрешенным действием DRM \_ \_ не \_ включен \_ без \_ прав**</span><span class="sxs-lookup"><span data-stu-id="33a79-114"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_RIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="33a79-115">Указывает, что для содержимого существует лицензия, но запрошенное право не разрешено.</span><span class="sxs-lookup"><span data-stu-id="33a79-115">Specifies that a license exists for the content, but that the queried right is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="33a79-116"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**\_запрос на \_ разрешенное действие DRM \_ \_ не \_ включен. \_ исчерпано**</span><span class="sxs-lookup"><span data-stu-id="33a79-116"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_EXHAUSTED**</span></span>
</dt> <dd>

<span data-ttu-id="33a79-117">Указывает, что запрашиваемое право ограничено счетчиком и что больше не используется.</span><span class="sxs-lookup"><span data-stu-id="33a79-117">Specifies that the queried right is restricted by a count, and that no more uses remain.</span></span>

</dd> <dt>

<span data-ttu-id="33a79-118"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**\_срок действия \_ запроса с разрешенным действием DRM \_ \_ не \_ включен \_**</span><span class="sxs-lookup"><span data-stu-id="33a79-118"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_EXPIRED**</span></span>
</dt> <dd>

<span data-ttu-id="33a79-119">Указывает, что запрошенное право доступа ограничено датой окончания срока действия, предшествующей текущей дате.</span><span class="sxs-lookup"><span data-stu-id="33a79-119">Specifies that the queried right is restricted with an expiration date that is earlier than the current date.</span></span>

</dd> <dt>

<span data-ttu-id="33a79-120"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**\_запрос с \_ разрешенным действием DRM \_ \_ не \_ включен \_ \_ , не запущен**</span><span class="sxs-lookup"><span data-stu-id="33a79-120"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NOT\_STARTED**</span></span>
</dt> <dd>

<span data-ttu-id="33a79-121">Указывает, что запрошенное право доступа ограничено датой начала, которая позже текущей даты.</span><span class="sxs-lookup"><span data-stu-id="33a79-121">Specifies that the queried right is restricted with a start date that is later than the current date.</span></span>

</dd> <dt>

<span data-ttu-id="33a79-122"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**\_запрос с \_ разрешенным действием DRM \_ \_ не \_ включен \_ аппсек \_ слишком \_ мало**</span><span class="sxs-lookup"><span data-stu-id="33a79-122"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_APPSEC\_TOO\_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="33a79-123">Указывает, что для содержимого существует лицензия, и что лицензия разрешает запрошенное право, но уровень безопасности вызывающего приложения недостаточно высок.</span><span class="sxs-lookup"><span data-stu-id="33a79-123">Specifies that a license exists for the content and that the license allows the queried right, but that the security level of the calling application is not high enough.</span></span>

</dd> <dt>

<span data-ttu-id="33a79-124"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**\_запрос с \_ разрешенным действием DRM \_ \_ не \_ включен \_ \_ индив req**</span><span class="sxs-lookup"><span data-stu-id="33a79-124"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_REQ\_INDIV**</span></span>
</dt> <dd>

<span data-ttu-id="33a79-125">Указывает, что для содержимого существует лицензия, и что лицензия разрешает запрошенное право, но подсистема DRM должна быть индивидуальной.</span><span class="sxs-lookup"><span data-stu-id="33a79-125">Specifies that a license exists for the content and that the license allows the queried right, but that the DRM subsystem must be individualized.</span></span>

</dd> <dt>

<span data-ttu-id="33a79-126"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**в \_ \_ запросе разрешено действие DRM \_ \_ не \_ включено \_ \_ \_ слишком \_ низкое ОПЛ копирования**</span><span class="sxs-lookup"><span data-stu-id="33a79-126"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_COPY\_OPL\_TOO\_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="33a79-127">Указывает, что уровень защиты выходных данных клиента слишком мал.</span><span class="sxs-lookup"><span data-stu-id="33a79-127">Specifies that the output protection level of the client is too low.</span></span>

</dd> <dt>

<span data-ttu-id="33a79-128"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**\_разрешенное действие DRM " \_ \_ запрос \_ не включен" не \_ включено \_ копирование \_ ОПЛ \_ исключено**</span><span class="sxs-lookup"><span data-stu-id="33a79-128"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_COPY\_OPL\_EXCLUDED**</span></span>
</dt> <dd>

<span data-ttu-id="33a79-129">Указывает, что уровень защиты выходных данных клиента находится в списке исключений.</span><span class="sxs-lookup"><span data-stu-id="33a79-129">Specifies that the output protection level of the client is on the exclusion list.</span></span>

</dd> <dt>

<span data-ttu-id="33a79-130"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**в \_ запросе с разрешенным действием DRM \_ \_ \_ не \_ включена \_ \_ \_ Поддержка часов**</span><span class="sxs-lookup"><span data-stu-id="33a79-130"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_CLOCK\_SUPPORT**</span></span>
</dt> <dd>

<span data-ttu-id="33a79-131">Указывает, что для лицензии требуется поддержка безопасных часов, а клиент не предоставил его.</span><span class="sxs-lookup"><span data-stu-id="33a79-131">Specifies that the license requires secure clock support and that the client does not provide it.</span></span>

</dd> <dt>

<span data-ttu-id="33a79-132"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**в \_ \_ запросе разрешенных действий DRM \_ \_ не \_ включена \_ \_ Поддержка отслеживания использования \_**</span><span class="sxs-lookup"><span data-stu-id="33a79-132"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_METERING\_SUPPORT**</span></span>
</dt> <dd>

<span data-ttu-id="33a79-133">Указывает, что запрашиваемое действие разрешено лицензией, но это необходимо, а клиент не поддерживает измерение.</span><span class="sxs-lookup"><span data-stu-id="33a79-133">Specifies that the queried action is allowed by a license, but that metering is required and the client does not support metering.</span></span>

</dd> <dt>

<span data-ttu-id="33a79-134"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**\_ \_ \_ \_ \_ \_ \_ \_ слишком большая глубина цепочки \_ разрешенных запросов для действия DRM**</span><span class="sxs-lookup"><span data-stu-id="33a79-134"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_CHAIN\_DEPTH\_TOO\_HIGH**</span></span>
</dt> <dd>

<span data-ttu-id="33a79-135">Указывает, что права для запрошенного действия не могут быть определены, так как содержимое охватывается связанной лицензией, а конечная лицензия отсутствует.</span><span class="sxs-lookup"><span data-stu-id="33a79-135">Specifies that the rights for the queried action cannot be determined because the content is covered by a chained license and the leaf license is missing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33a79-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33a79-136">Remarks</span></span>

<span data-ttu-id="33a79-137">Значения этого типа перечисления указывают, что действие не разрешено.</span><span class="sxs-lookup"><span data-stu-id="33a79-137">The values of this enumeration type indicate that an action is not allowed.</span></span> <span data-ttu-id="33a79-138">Нулевое значение указывает, что действие разрешено.</span><span class="sxs-lookup"><span data-stu-id="33a79-138">A value of zero indicates that the action is allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="33a79-139">Требования</span><span class="sxs-lookup"><span data-stu-id="33a79-139">Requirements</span></span>



| <span data-ttu-id="33a79-140">Требование</span><span class="sxs-lookup"><span data-stu-id="33a79-140">Requirement</span></span> | <span data-ttu-id="33a79-141">Значение</span><span class="sxs-lookup"><span data-stu-id="33a79-141">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33a79-142">Header</span><span class="sxs-lookup"><span data-stu-id="33a79-142">Header</span></span><br/> | <dl> <span data-ttu-id="33a79-143"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="33a79-143"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33a79-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33a79-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33a79-145">**Типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="33a79-145">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





