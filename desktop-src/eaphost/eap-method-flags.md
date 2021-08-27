---
title: Флаги методов EAP (Еаптипес. h)
description: Флаги методов EAP используются в запрашивающей стороне, средствах проверки подлинности и одноранговых функциях для указания поведения сеанса проверки подлинности EAP.
ms.assetid: b6305349-3418-475e-8a37-2c06b399556e
topic_type:
- apiref
api_name:
- EAP_FLAG_Reserved1
- EAP_FLAG_NON_INTERACTIVE
- EAP_FLAG_LOGON
- EAP_FLAG_PREVIEW
- EAP_FLAG_Reserved2
- EAP_FLAG_MACHINE_AUTH
- EAP_FLAG_GUEST_ACCESS
- EAP_FLAG_Reserved3
- EAP_FLAG_Reserved4
- EAP_FLAG_RESUME_FROM_HIBERNATE
- EAP_FLAG_Reserved5
- EAP_FLAG_Reserved6
- EAP_FLAG_FULL_AUTH
- EAP_FLAG_PREFER_ALT_CREDENTIALS
- EAP_FLAG_Reserved7
- EAP_PEER_FLAG_HEALTH_STATE_CHANGE
- EAP_FLAG_SUPRESS_UI
- EAP_FLAG_PRE_LOGON
- EAP_FLAG_USER_AUTH
- EAP_FLAG_CONFG_READONLY
- EAP_FLAG_Reserved8
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91acce3b3829c947bfb6e705ad7e1f07b938a986bc6f6845a4c10a54b4f1992c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094414"
---
# <a name="eap-method-flags"></a>Флаги методов EAP

Флаги методов EAP используются в запрашивающей стороне, средствах проверки подлинности и одноранговых функциях для указания поведения сеанса проверки подлинности EAP.

<dl> <dt>

<span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**\_Reserved1 флаг \_ EAP**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Не используйте. Зарезервировано для последующего использования.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**Флаг EAP, \_ \_ не \_ Интерактивный**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Не отображать пользовательский интерфейс.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**\_Вход с флагом EAP \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



данные пользователя получены из Windows входа в систему.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**\_ \_ Предварительный просмотр ФЛАГа EAP**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Показать пользовательский интерфейс учетных данных перед проверкой подлинности, даже если имеются кэшированные учетные данные.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span>**Протокол EAP \_ ФЛАГ \_ Reserved2**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Не используйте. Зарезервировано для последующего использования.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**\_ \_ Проверка подлинности компьютера с ФЛАГом EAP \_**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Использовать проверку подлинности на уровне компьютера; Если этот флаг не задан, то используется проверка подлинности на уровне пользователя.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**Флаг EAP, \_ показывающий \_ гостевой \_ доступ**
</dt> <dd> <dl> <dt>

 0x00000040
</dt> <dt>



Указывает запрос на предоставление гостевого доступа.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**\_Reserved3 флаг \_ EAP**
</dt> <dd> <dl> <dt>

0x00000080 
</dt> <dt>



Не используйте. Зарезервировано для последующего использования.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span>**Протокол EAP \_ ФЛАГ \_ Reserved4** 
</dt> <dd> <dl> <dt>

0x00000100 
</dt> <dt>



Не используйте. Зарезервировано для последующего использования.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**\_флаг EAP \_ возобновляется \_ из \_ режима гибернации**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Указывает, что это первый вызов после возобновления активности компьютера с периода гибернации.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span>**Протокол EAP \_ ФЛАГ \_ Reserved5**
</dt> <dd> <dl> <dt>

0x00000400 
</dt> <dt>



Не используйте. Зарезервировано для последующего использования.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**\_Reserved6 флаг \_ EAP** 
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Не используйте. Зарезервировано для последующего использования.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**\_ \_ полная \_ Проверка ПОдлинности EAP**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Указывает, что методы туннеля должны выполнять полную проверку подлинности вместо сокращенной версии, например [защищенное быстрое повторное подключение EAP (PEAP)](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**\_ \_ предпочтительные \_ \_ учетные данные для флага EAP**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Указывает, что учетные данные, передаваемые в [**еаппирбегинсессион**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) , являются предпочтительными для всех других форм получения учетных данных, даже если данные конфигурации, переданные в текущую функцию, запрашивают другой режим получения учетных данных.

> [!Note]  
> Этот флаг используется только [**еаппирбегинсессион**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession).

 


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**\_Reserved7 флаг \_ EAP**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Не используйте. Зарезервировано для последующего использования.


</dt> </dl> </dd> <dt>

<span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**\_ \_ \_ изменение состояния работоспособности однорангового флага EAP \_ \_**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Указывает, что причиной повторной проверки подлинности является обратный вызов [защиты доступа к сети](/windows/desktop/NAP/network-access-protection-start-page) (NAP). NAP инициировала сеанс проверки подлинности, так как изменилось состояние работоспособности. Этот флаг должен отправляться, только если эта функция вызывается обратным вызовом [*нотификатионхандлер*](/previous-versions/windows/desktop/api) , связанным с NAP, предоставленным предыдущим вызовом этой функции.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**\_Пользовательский интерфейс флага EAP \_ скрывать \_**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Продолжайте проверку подлинности с помощью доступной информации. Если проверка подлинности не может быть продолжена, завершится ошибкой.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**\_флаг EAP \_ Предварительный \_ Вход**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Указывает, что EAPHost должен обеспечивать единый вход (SSO). Дополнительные сведения см. в разделе [единый вход и PLAP](understanding-sso-and-plap.md).


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**\_ \_ Проверка подлинности пользователя с ФЛАГом EAP \_**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Указывает проверку подлинности на уровне пользователя для устаревших методов, которые не могут установить **\_ флаг EAP \_ \_ Проверка подлинности компьютера**.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**\_флаг EAP \_ CONFG \_ ReadOnly**
</dt> <dd> <dl> <dt>

 0x00080000
</dt> <dt>



Указывает, что конфигурацию можно просмотреть, но не обновить.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**\_Reserved8 флаг \_ EAP**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Не используйте. Зарезервировано для последующего использования.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Еаптипес. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие константы EAPHost](common-eap-host-error-constants.md)
</dt> </dl>

