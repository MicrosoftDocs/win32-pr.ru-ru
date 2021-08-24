---
description: включает параметры, которые можно задать или получить для текущего сеанса служб Microsoft Windows HTTP (WinHTTP).
ms.assetid: 8464d794-b4a8-4c83-9e26-69257000102a
title: Перечисление Винхттпрекуестоптион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestOption
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: ff4112538aff4c76c02e251f45e9dc78e6778633de6a5d93f6892dd87ff70c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051882"
---
# <a name="winhttprequestoption-enumeration"></a>Перечисление Винхттпрекуестоптион

перечисление **винхттпрекуестоптион** включает параметры, которые можно задать или получить для текущего сеанса служб Microsoft Windows HTTP (WinHTTP).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum WinHttpRequestOption { 
  WinHttpRequestOption_UserAgentString,
  WinHttpRequestOption_URL,
  WinHttpRequestOption_URLCodePage,
  WinHttpRequestOption_EscapePercentInURL,
  WinHttpRequestOption_SslErrorIgnoreFlags,
  WinHttpRequestOption_SelectCertificate,
  WinHttpRequestOption_EnableRedirects,
  WinHttpRequestOption_UrlEscapeDisable,
  WinHttpRequestOption_UrlEscapeDisableQuery,
  WinHttpRequestOption_SecureProtocols,
  WinHttpRequestOption_EnableTracing,
  WinHttpRequestOption_RevertImpersonationOverSsl,
  WinHttpRequestOption_EnableHttpsToHttpRedirects,
  WinHttpRequestOption_EnablePassportAuthentication,
  WinHttpRequestOption_MaxAutomaticRedirects,
  WinHttpRequestOption_MaxResponseHeaderSize,
  WinHttpRequestOption_MaxResponseDrainSize,
  WinHttpRequestOption_EnableHttp1_1,
  WinHttpRequestOption_EnableCertificateRevocationCheck
} WinHttpRequestOption;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**Винхттпрекуестоптион \_ усеражентстринг**
</dt> <dd>

Задает или получает **значение типа Variant** , содержащее строку [*агента пользователя*](glossary.md) .

</dd> <dt>

<span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**\_URL-адрес винхттпрекуестоптион**
</dt> <dd>

Извлекает **значение типа Variant** , содержащее URL-адрес ресурса. Это значение доступно только для чтения; задать URL-адрес с помощью этого свойства нельзя. Невозможно прочитать URL-адрес до вызова метода [**Open**](iwinhttprequest-open.md) . Этот параметр полезен для проверки URL-адреса после завершения метода [**Send**](iwinhttprequest-send.md) , чтобы проверить, не произошло ли перенаправление.

</dd> <dt>

<span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**Винхттпрекуестоптион \_ урлкодепаже**
</dt> <dd>

Задает или получает **значение типа Variant** , идентифицирующее [*кодовую страницу*](glossary.md) для строки URL-адреса. Значение по умолчанию — кодовая страница UTF-8. Кодовая страница используется для преобразования строки URL-адреса Юникода, передаваемой в метод [**Open**](iwinhttprequest-open.md) , в однобайтовое строковое представление.

</dd> <dt>

<span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**Винхттпрекуестоптион \_ ескапеперцентинурл**
</dt> <dd>

Задает или получает **значение типа Variant** , которое указывает, преобразуются ли символы процента в строке URL-адреса в управляющую последовательность. По умолчанию этот параметр имеет значение **Variant \_ true** , которое указывает, что все ненадежные символы американский национальный институт стандартов (ANSI) (ANSI), за исключением символа процента, преобразуются в escape-последовательность.

</dd> <dt>

<span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**Винхттпрекуестоптион \_ сслерроригнорефлагс**
</dt> <dd>

Задает или получает **значение типа Variant** , указывающее, какие ошибки сертификата сервера следует игнорировать. Это может быть сочетание одного или нескольких из следующих флагов.



| Error                                                  | Значение  |
|--------------------------------------------------------|--------|
| Неизвестный центр сертификации (ЦС) или недоверенный корень | 0x0100 |
| Неправильное использование                                            | 0x0200 |
| Недопустимое общее имя (CN)                               | 0x1000 |
| Срок действия недействительной даты или сертификата истек                    | 0x2000 |



 

Значение этого параметра по умолчанию в версии 5,1 WinHTTP равно нулю, что не приводит к игнорированию ошибок. В более ранних версиях WinHTTP параметр по умолчанию был 0x3300, что привело к тому, что по умолчанию все ошибки сертификата сервера игнорировались.

</dd> <dt>

<span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**Винхттпрекуестоптион \_ селектцертификате**
</dt> <dd>

Задает **значение типа Variant** , указывающее сертификат клиента, который отправляется на сервер для проверки подлинности. Этот параметр указывает расположение, [*хранилище сертификатов*](glossary.md)и субъект сертификата клиента, разделенные символами обратной косой черты. Дополнительные сведения о выборе сертификата клиента см. в разделе [SSL в WinHTTP](ssl-in-winhttp.md).

</dd> <dt>

<span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**Винхттпрекуестоптион \_ енаблередиректс**
</dt> <dd>

Задает или получает **значение типа Variant** , указывающее, будут ли запросы автоматически перенаправляться, когда сервер указывает новое расположение для ресурса. Значение этого параметра по умолчанию — **Variant \_ true** , указывающее, что запросы перенаправляются автоматически.

</dd> <dt>

<span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**Винхттпрекуестоптион \_ урлескапедисабле**
</dt> <dd>

Задает или получает **значение типа Variant** , указывающее, преобразуются ли незащищенные символы в пути и компонентах запроса URL-адреса в управляющие последовательности. Значение этого параметра по умолчанию — **Variant \_ true**, которое указывает, что символы в пути и запросе преобразованы.

</dd> <dt>

<span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**Винхттпрекуестоптион \_ урлескапедисаблекуери**
</dt> <dd>

Задает или получает **значение типа Variant** , указывающее, преобразуются ли незащищенные символы в компоненте запроса URL-адреса в управляющие последовательности. Значение этого параметра по умолчанию — **Variant \_ true**, которое указывает, что символы в запросе преобразованы.

</dd> <dt>

<span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**Винхттпрекуестоптион \_ секурепротоколс**
</dt> <dd>

Задает или получает **значение типа Variant** , указывающее, какие безопасные протоколы можно использовать. Этот параметр позволяет выбрать протоколы, приемлемые для клиента. Протокол согласовывается во время согласования SSL (SSL). Это может быть сочетание одного или нескольких из следующих флагов.



| Протокол                           | Значение  |
|------------------------------------|--------|
| SSL 2.0                            | 0x0008 |
| SSL 3.0                            | 0x0020 |
| Безопасность транспортного уровня (TLS) 1,0 | 0x0080 |



 

Значение этого параметра по умолчанию — 0x0028, которое указывает, что можно использовать SSL 2,0 или SSL 3,0. Если этот параметр имеет значение 0, клиент и сервер не могут определить приемлемый протокол безопасности, а следующая [**Отправка**](iwinhttprequest-send.md) приведет к ошибке.

</dd> <dt>

<span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**Винхттпрекуестоптион \_ енаблетраЦинг**
</dt> <dd>

Задает или получает **значение типа Variant** , указывающее, включена ли трассировка в данный момент. дополнительные сведения о средстве трассировки в службах Microsoft Windows HTTP (winhttp) см. в разделе служба [трассировки winhttp](winhttptracecfg-exe--a-trace-configuration-tool.md).

</dd> <dt>

<span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**Винхттпрекуестоптион \_ ревертимперсонатионоверссл**
</dt> <dd>

Определяет, будет ли объект [**WinHttpRequest**](winhttprequest.md) временно отменять олицетворение клиента на время операций проверки подлинности SSL-сертификата. Значение по умолчанию для объекта **WinHttpRequest** — **true**. Установите этот параметр в **значение false** , чтобы при выполнении операций проверки подлинности с помощью сертификата сохранение олицетворения выполнялось.

</dd> <dt>

<span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**Винхттпрекуестоптион \_ енаблехттпстохттпредиректс**
</dt> <dd>

Определяет, допускает ли служба WinHTTP перенаправление. По умолчанию все перенаправления выполняются автоматически, за исключением тех, которые передаются с защищенного URL-адреса (HTTPS) на небезопасный (http) URL-адрес. Установите для этого параметра **значение true** , чтобы включить перенаправления по протоколу HTTPS в HTTP.

</dd> <dt>

<span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**Винхттпрекуестоптион \_ енаблепасспортаусентикатион**
</dt> <dd>

Включает или отключает поддержку проверки подлинности Passport. По умолчанию автоматическая поддержка проверки подлинности Passport отключена. Установите для этого параметра **значение true** , чтобы включить поддержку проверки подлинности паспорта.

</dd> <dt>

<span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**Винхттпрекуестоптион \_ максаутоматикредиректс**
</dt> <dd>

Задает или получает максимальное число перенаправлений, которое следует за WinHTTP. значение по умолчанию — 10. Это ограничение не позволяет неавторизованным сайтам сделать клиент WinHTTP остановленным после большого числа перенаправлений.

**Windows XP с пакетом обновления 1 (SP1) и Windows 2000 с SP3:** Это значение перечисления не поддерживается.

</dd> <dt>

<span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**Винхттпрекуестоптион \_ максреспонсехеадерсизе**
</dt> <dd>

Задает или получает связанный набор на максимальный размер заголовка ответа сервера. Эта привязка защищает клиента от вредоносного сервера, пытающегося приостановки работы клиента, отправив ответ с бесконечным объемом данных заголовка. Значение по умолчанию — 64 КБ.

**Windows XP с пакетом обновления 1 (SP1) и Windows 2000 с SP3:** Это значение перечисления не поддерживается.

</dd> <dt>

<span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**Винхттпрекуестоптион \_ максреспонседраинсизе**
</dt> <dd>

Задает или получает ограничение на объем данных, которые будут передаваться из ответов для повторного использования соединения. По умолчанию установлено значение 1 МБ.

**Windows XP с пакетом обновления 1 (SP1) и Windows 2000 с SP3:** Это значение перечисления не поддерживается.

</dd> <dt>

<span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**Винхттпрекуестоптион \_ EnableHttp1 \_ 1**
</dt> <dd>

Задает или получает логическое значение, указывающее, следует ли использовать HTTP/1.1 или HTTP/1.0. Значение по умолчанию — **true**, поэтому по умолчанию используется HTTP/1.1.

**Windows XP с пакетом обновления 1 (SP1) и Windows 2000 с SP3:** Это значение перечисления не поддерживается.

</dd> <dt>

<span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**Винхттпрекуестоптион \_ енаблецертификатеревокатиончекк**
</dt> <dd>

Включает проверку отзыва сертификатов сервера во время согласования SSL. Если сервер представляет сертификат, выполняется проверка, чтобы определить, отозван ли сертификат его издателем. Если сертификат действительно отозван или проверка отзыва не удалась из-за невозможности загрузить список отзыва сертификатов (CRL), запрос завершится ошибкой. такие ошибки отзыва не могут быть подавлены.

**Windows XP с пакетом обновления 1 (SP1) и Windows 2000 с SP3:** Это значение перечисления не поддерживается.

</dd> </dl>

## <a name="remarks"></a>Remarks

Задайте параметр, указав одну из предыдущих констант в качестве параметра свойства [**Option**](iwinhttprequest-option.md) .

> [!Note]  
> сведения о Windows XP и Windows 2000 см. в разделе [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHttp.

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP, Windows 2000 Professional с SP3 \[ только для настольных приложений\]<br/>            |
| Минимальная версия сервера<br/> | Windows сервер 2003, Windows 2000 server с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>         |
| Распространяемые компоненты<br/>          | WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Версии WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




