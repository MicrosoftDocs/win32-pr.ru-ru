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
ms.openlocfilehash: d66973838bb6d9cf745ae30b885acccf7b4b311834bbe827d96ccbeea501bd17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547814"
---
# <a name="drm_action_allowed_query_results-enumeration"></a>\_ \_ \_ Перечисление результатов запроса действия DRM Allowed \_

Тип **перечисления \_ \_ \_ \_ Results Action Allowed DRM** используется интерфейсом [**ивмдрмлиценсекуери:: куеряктионалловед**](iwmdrmlicensequery-queryactionallowed.md) , чтобы указать причину, по которой действие не разрешено.

## <a name="syntax"></a>Синтаксис


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



## <a name="constants"></a>Константы

<dl> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**\_запрос на \_ разрешенное действие DRM \_ \_ не \_ включен**
</dt> <dd>

Указывает, что действие "запросы" не разрешено. Для действий, которые не разрешены, возвращаемое значение представляет это значение в сочетании с помощью побитового или с одним или несколькими другими значениями в этом перечислении.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**в \_ \_ запросе разрешено действие DRM \_ \_ не \_ включено \_ ни одной \_ лицензии**
</dt> <dd>

Указывает, что лицензия для запрошенного содержимого не существует.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**\_запрос с \_ разрешенным действием DRM \_ \_ не \_ включен \_ без \_ прав**
</dt> <dd>

Указывает, что для содержимого существует лицензия, но запрошенное право не разрешено.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**\_запрос на \_ разрешенное действие DRM \_ \_ не \_ включен. \_ исчерпано**
</dt> <dd>

Указывает, что запрашиваемое право ограничено счетчиком и что больше не используется.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**\_срок действия \_ запроса с разрешенным действием DRM \_ \_ не \_ включен \_**
</dt> <dd>

Указывает, что запрошенное право доступа ограничено датой окончания срока действия, предшествующей текущей дате.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**\_запрос с \_ разрешенным действием DRM \_ \_ не \_ включен \_ \_ , не запущен**
</dt> <dd>

Указывает, что запрошенное право доступа ограничено датой начала, которая позже текущей даты.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**\_запрос с \_ разрешенным действием DRM \_ \_ не \_ включен \_ аппсек \_ слишком \_ мало**
</dt> <dd>

Указывает, что для содержимого существует лицензия, и что лицензия разрешает запрошенное право, но уровень безопасности вызывающего приложения недостаточно высок.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**\_запрос с \_ разрешенным действием DRM \_ \_ не \_ включен \_ \_ индив req**
</dt> <dd>

Указывает, что для содержимого существует лицензия, и что лицензия разрешает запрошенное право, но подсистема DRM должна быть индивидуальной.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**в \_ \_ запросе разрешено действие DRM \_ \_ не \_ включено \_ \_ \_ слишком \_ низкое ОПЛ копирования**
</dt> <dd>

Указывает, что уровень защиты выходных данных клиента слишком мал.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**\_разрешенное действие DRM " \_ \_ запрос \_ не включен" не \_ включено \_ копирование \_ ОПЛ \_ исключено**
</dt> <dd>

Указывает, что уровень защиты выходных данных клиента находится в списке исключений.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**в \_ запросе с разрешенным действием DRM \_ \_ \_ не \_ включена \_ \_ \_ Поддержка часов**
</dt> <dd>

Указывает, что для лицензии требуется поддержка безопасных часов, а клиент не предоставил его.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**в \_ \_ запросе разрешенных действий DRM \_ \_ не \_ включена \_ \_ Поддержка отслеживания использования \_**
</dt> <dd>

Указывает, что запрашиваемое действие разрешено лицензией, но это необходимо, а клиент не поддерживает измерение.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**\_ \_ \_ \_ \_ \_ \_ \_ слишком большая глубина цепочки \_ разрешенных запросов для действия DRM**
</dt> <dd>

Указывает, что права для запрошенного действия не могут быть определены, так как содержимое охватывается связанной лицензией, а конечная лицензия отсутствует.

</dd> </dl>

## <a name="remarks"></a>Remarks

Значения этого типа перечисления указывают, что действие не разрешено. Нулевое значение указывает, что действие разрешено.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Типы перечислений**](drm-enumeration-types.md)
</dt> </dl>

 

 





