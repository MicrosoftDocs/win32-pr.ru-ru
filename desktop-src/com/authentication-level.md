---
title: Уровень проверки подлинности
description: Уровень проверки подлинности определяет степень безопасности, которую клиент или сервер должен получить от своего поставщика общих служб.
ms.assetid: 0bad2bfd-6930-42fc-beb0-bce32440b0b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c468408a22f1ea0c0fae67d7ce3d5f5b40f8a6342538614c1619acd40574ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311154"
---
# <a name="authentication-level"></a>Уровень проверки подлинности

Уровень проверки подлинности определяет степень безопасности, которую клиент или сервер должен получить от своего поставщика общих служб. Уровень проверки подлинности задается путем передачи \_ соответствующего \_ значения уровня RPC C AUTHN \_ Level \_ xxx в [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) или [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) с помощью параметра *двауснлевел* . Уровни проверки подлинности от клиента и сервера сравниваются во время подтверждения, а для соединения используется параметр защиты более высокого уровня.

Различные уровни проверки подлинности описаны ниже, начиная с нижнего уровня защиты безопасности до самого высокого:

<dl> <dt>

<span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>Нет ( \_ уровень RPC \_ C \_ AUTHN \_ None)
</dt> <dd>

При обмене данными между клиентом и сервером не выполняется проверка подлинности. Все параметры безопасности игнорируются. Этот уровень проверки подлинности можно задать только в том случае, если [уровень службы проверки подлинности](com-authentication-service-constants.md) — RPC \_ C \_ AUTHN \_ None.

</dd> <dt>

<span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Default (RPC \_ C \_ \_ \_ по умолчанию на уровне AUTHN)
</dt> <dd>

COM выбирает уровень проверки подлинности с помощью обычного согласования безопасности. Он никогда не будет выбирать уровень проверки подлинности None.

</dd> <dt>

<span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Подключение (RPC \_ C \_ AUTHN \_ LEVEL \_ Connect)
</dt> <dd>

Обычная проверка подлинности выполняется между клиентом и сервером, а сеансовый ключ устанавливается, но этот ключ никогда не используется для обмена данными между клиентом и сервером. Все связи после подтверждения не являются безопасными.

</dd> <dt>

<span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Call ( \_ \_ вызов уровня RPC C AUTHN \_ \_ )
</dt> <dd>

Подписываются только заголовки начала каждого вызова. Остальные данные, которыми обмениваются клиент и сервер, не являются ни подписанными, ни зашифрованными. Большинство SSP не поддерживают этот уровень проверки подлинности и без уведомления передаются в пакет.

</dd> <dt>

<span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Пакет (RPC \_ C \_ уровня AUTHN на \_ уровне \_ маркера)
</dt> <dd>

Заголовок каждого пакета подписывается, но не шифруется. Сами пакеты не подписываются и не шифруются.

</dd> <dt>

<span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Целостность пакетов ( \_ RPC \_ C \_ AUTHN \_ уровня \_ целостности PKT)
</dt> <dd>

Каждый пакет данных подписывается целиком, но не шифруется. Так как все данные подписаны отправителем, получатель может убедиться, что ни один из данных не был изменен во время передачи.

</dd> <dt>

<span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Конфиденциальность пакетов (RPC \_ C \_ AUTHN \_ уровня \_ \_ "Конфиденциальность")
</dt> <dd>

Каждый пакет данных подписывается и шифруется. Это помогает защитить весь обмен данными между клиентом и сервером.

</dd> </dl>

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[аусентикатионлевел](authenticationlevel.md)
</dt> <dt>

[легациаусентикатионлевел](legacyauthenticationlevel.md)
</dt> </dl>

 

 




