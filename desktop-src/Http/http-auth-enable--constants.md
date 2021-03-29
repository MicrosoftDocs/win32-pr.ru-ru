---
title: Константы HTTP_AUTH_ENABLE_ (HTTP. h)
description: Определите схемы проверки подлинности, которые можно включить для группы URL-адресов.
ms.assetid: db22645f-c9e4-427e-b3d5-91d568aec7c5
topic_type:
- apiref
api_name:
- HTTP_AUTH_ENABLE_BASIC
- HTTP_AUTH_ENABLE_DIGEST
- HTTP_AUTH_ENABLE_KERBEROS
- HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING
- HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL
- HTTP_AUTH_ENABLE_NTLM
- HTTP_AUTH_ENABLE_NEGOTIATE
- HTTP_AUTH_ENABLE_ALL
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6462a4f9d884244f460c4bf7714b45d3e17600c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492831"
---
# <a name="http_auth_enable_-constants"></a>\_ \_ Константы включения проверки подлинности HTTP \_

Константы **HTTP \_ AUTH \_ позволяют** определить схемы проверки подлинности, которые можно включить для группы URL-адресов.

Эти константы используются в структуре [**\_ \_ \_ сведений о проверке подлинности HTTP-сервера**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) .

<dl> <dt>

<span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**\_Проверка подлинности HTTP \_ Enable \_ Basic**
</dt> <dd> <dl> <dt>



Основная схема проверки подлинности включена.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**\_дайджест включения проверки подлинности HTTP \_ \_**
</dt> <dd> <dl> <dt>



Схема дайджест-проверки подлинности включена.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**\_Проверка подлинности HTTP \_ Enable \_ Kerberos**
</dt> <dd> <dl> <dt>



Схема проверки подлинности Kerberos включена.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**\_ \_ флаг ex HTTP \_ AUTH \_ Включение \_ \_ кэширования учетных данных Kerberos \_**
</dt> <dd> <dl> <dt>



Кэширование учетных данных Kerberos включено.

**Windows Server 2003 и более того:** Недоступно.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**\_ \_ \_ \_ запись \_ учетных данных с флагом HTTP auth ex**
</dt> <dd> <dl> <dt>



API сервера HTTP захватывает удостоверение вызывающего объекта и использует его для проверки подлинности только для схем Negotiate и Kerberos.

**Windows Server 2003 и более того:** Недоступно.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**\_Проверка подлинности HTTP \_ Enable \_ NTLM**
</dt> <dd> <dl> <dt>



Схема проверки подлинности NTLM включена.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**\_Проверка подлинности HTTP \_ включить \_ согласование**
</dt> <dd> <dl> <dt>



Схема проверки подлинности Negotiate включена.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**\_включить проверку подлинности HTTP \_ \_**
</dt> <dd> <dl> <dt>



Все схемы проверки подлинности включены.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                    |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                              |
| Header<br/>                   | <dl> <dt>HTTP. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы API сервера HTTP версии 2,0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**\_ \_ сведения о проверке подлинности HTTP-сервера \_**](/windows/desktop/api/Http/ns-http-http_server_authentication_info)
</dt> <dt>

[**хттпсетурлграуппроперти**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**хттпсетсерверсессионпроперти**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**хттпкуерюрлграуппроперти**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**хттпкуерисерверсессионпроперти**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





