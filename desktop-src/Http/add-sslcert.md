---
title: add sslcert
description: Добавляет новую привязку сертификата сервера SSL (SSL) и соответствующие политики сертификата клиента для IP-адреса и порта.
ms.assetid: 4ba3d2cb-050f-46e3-81f9-5f7e360b19fb
keywords:
- Добавить sslcert HTTP
topic_type:
- apiref
api_name:
- add sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721931bfa05a96ca47fd69f643a02076201bb5f93eff003afa83714f2d14b519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950953"
---
# <a name="add-sslcert"></a>add sslcert

Добавляет новую привязку сертификата сервера SSL (SSL) и соответствующие политики сертификата клиента для IP-адреса и порта.

``` syntax
add sslcert [ipport=]IP Address:port
            [certhash=]string
            [appid=]GUID
            [certstorename=]string
            [verifyclientcertrevocation={enable|disable}]
            [verifyrevocationwithcachedclientcertonly={enable|disable}]
            [usagecheck={enable|disable}]
            [revocationfreshnesstime=]u-int
            [urlretrievaltimeout=]u-int
            [sslctlidentifier=]string
            [sslctlstorename=]string
            [dsmapperusage={enable|disable}]
            [clientcertnegotiation={enable|disable}]

 
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[иппорт = IP-адрес: порт\]**
</dt> <dd>

Указывает IP-адрес и порт для привязки.

</dd> <dt>

<span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>**\[certhash = строка\]**
</dt> <dd>

Указывает хэш SHA сертификата. Этот хэш имеет длину 20 байт и задается в виде шестнадцатеричной строки.

</dd> <dt>

<span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>**\[AppID = GUID\]**
</dt> <dd>

Указывает GUID для обозначения приложения-владельца.

</dd> <dt>

<span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>**\[цертсторенаме = строка\]**
</dt> <dd>

Указывает имя для хранения сертификата. По умолчанию — MY. Сертификат должен храниться в контексте локального компьютера.

</dd> <dt>

<span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[верификлиентцертревокатион = {включить \| Отключение}\]**
</dt> <dd>

Включает или турнсофф проверку отзыва сертификатов клиента.

</dd> <dt>

<span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[верифиревокатионвискачедклиентцертонли = {включить \| Отключение}\]**
</dt> <dd>

Включает или выключает использование только кэшированного сертификата клиента для проверки отзыва.

</dd> <dt>

<span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[усажечекк = {включить \| Отключение}\]**
</dt> <dd>

Включает или выключает проверку использования. По умолчанию она включена.

</dd> <dt>

<span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>**\[ревокатионфрешнесстиме = u-int\]**
</dt> <dd>

Указывает интервал времени для проверки обновленного списка отзыва сертификатов (CRL). Если это значение равно 0, то новый список отзыва сертификатов обновляется только в том случае, если предыдущий срок истекает (в секундах).

</dd> <dt>

<span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>**\[урлретриевалтимеаут = u-int\]**
</dt> <dd>

Указывает интервал времени ожидания при попытке получить список отзыва сертификатов для удаленного URL-адреса (в миллисекундах).

</dd> <dt>

<span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>**\[сслктлидентифиер = строка\]**
</dt> <dd>

Список издателей сертификатов, которые могут быть доверенными. Этот список может быть подмножеством издателей сертификатов, которые являются доверенными для компьютера.

</dd> <dt>

<span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>**\[сслктлсторенаме = строка\]**
</dt> <dd>

Указывает имя хранилища на локальном \_ компьютере, где хранится сслктлидентифиер.

</dd> <dt>

<span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[дсмапперусаже = {включить \| Отключение}\]**
</dt> <dd>

Включает или выключает модули сопоставления DS. По умолчанию оно отключено.

</dd> <dt>

<span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[клиентцертнеготиатион = {включить \| Отключение}\]**
</dt> <dd>

Включает или отключает согласование сертификата. По умолчанию оно отключено.

</dd> </dl>

## <a name="examples"></a>Примеры

**add sslcert иппорт = 1.1.1.1:443**

**certhash = 0102030405060708090A0B0C0D0E0F1011121314**

**AppID = {00112233-4455-6677-8899-AABBCCDDEEFF}**

 

 




