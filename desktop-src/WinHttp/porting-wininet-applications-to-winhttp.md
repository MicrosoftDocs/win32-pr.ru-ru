---
description: службы Microsoft Windows HTTP (WinHTTP) нацелены на приложения среднего уровня и серверной части, которым требуется доступ к стеку клиента HTTP.
ms.assetid: 5b0cf321-8f69-4526-a628-e6ca0f9d4a58
title: Перенос приложений WinINet в WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b111cd79e7ce7edfb09d43993ee2735ce09275f51c58bcfad319fb073dccc5b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052012"
---
# <a name="porting-wininet-applications-to-winhttp"></a>Перенос приложений WinINet в WinHTTP

службы Microsoft Windows HTTP (WinHTTP) нацелены на приложения среднего уровня и серверной части, которым требуется доступ к стеку клиента HTTP. [Microsoft Windows Internet (WinINet)](winhttp-start-page.md) предоставляет стек клиента HTTP для клиентских приложений, а также доступ к протоколам протокол FTP (FTP), SOCKSv4 и Gopher. Этот обзор поможет определить, будет ли использоваться перенос приложений WinINet в службы WinHTTP. Он также описывает конкретные требования к преобразованию.

-   [Вопросы, которые следует учитывать перед переносом приложения WinINet](#things-to-consider-before-porting-your-wininet-application)
-   [Эквиваленты WinHTTP для функций WinINet](#winhttp-equivalents-to-wininet-functions)
-   [Разная Обработка асинхронных запросов](#different-handling-of-asynchronous-requests)
-   [Различия в уведомлениях обратного вызова WinHTTP](#differences-in-winhttp-callback-notifications)
-   [Различия в проверке подлинности](#authentication-differences)
-   [Различия в защищенных транзакциях HTTP](#differences-in-secure-http-transactions)

## <a name="things-to-consider-before-porting-your-wininet-application"></a>Вопросы, которые следует учитывать перед переносом приложения WinINet

Рассмотрите возможность переноса приложения WinINet на WinHTTP, если ваше приложение получит следующие преимущества:

-   Серверный стек HTTP-клиента.
-   Минимальное использование стека.
-   Масштабируемость серверного приложения.
-   Меньше зависимостей от интерфейсов API, связанных с платформой.
-   Поддержка олицетворения потоков.
-   Удобный для службы стек HTTP.
-   Доступ к объекту [**WinHttpRequest**](winhttprequest.md) , поддерживающему скрипт.

Не рекомендуется переносить приложение WinINet на WinHTTP, если оно должно поддерживать одно или несколько из следующих действий:

-   Протокол FTP или gopher из стека HTTP.
-   Поддержка протокола SOCKSv4 для взаимодействия с прокси-серверами SOCKS.
-   Автоматические службы коммутируемого доступа.

Если вы решили перенести приложение на службу WinHTTP, в следующих разделах описывается процесс преобразования.

Чтобы получить пример приложения для WinINet и WinHTTP, Сравните пример Асинкдемо для WinINet с примером Асинкдемо для WinHTTP.

## <a name="winhttp-equivalents-to-wininet-functions"></a>Эквиваленты WinHTTP для функций WinINet

В следующей таблице перечислены функции WinINet, относящиеся к стеку клиента HTTP, а также эквиваленты WinHTTP.

Если приложению требуются функции WinINet, которых нет в списке, не переносите приложение на WinHTTP.



| WinINet, функция                                                       | Эквивалент WinHTTP                                                                                                                                                                                     | Важные изменения                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**хттпаддрекуессеадерс**](/windows/desktop/api/wininet/nf-wininet-httpaddrequestheadersa)             | [**винхттпаддрекуессеадерс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                                                                                                                                           | Отсутствует.                                                                                                                                                                                                                                                                                                                                |
| [**хттпендрекуест**](/windows/desktop/api/wininet/nf-wininet-httpendrequesta)                           | [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)                                                                                                                                               | Значение контекста задается с помощью [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) или [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Параметры запроса задаются с помощью [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) должен вызываться после отправки запроса.                      |
| [**хттпопенрекуест**](/windows/desktop/api/wininet/nf-wininet-httpopenrequesta)                         | [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                                                                                       | Значение контекста задается с помощью [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) или [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).                                                                                                                                                                                                      |
| [**хттпкуеринфо**](/windows/desktop/api/wininet/nf-wininet-httpqueryinfoa)                             | [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)                                                                                                                                                     | Отсутствует.                                                                                                                                                                                                                                                                                                                                |
| [**хттпсендрекуест**](/windows/desktop/api/wininet/nf-wininet-httpsendrequesta)                         | [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                       | Значение контекста можно задать с помощью [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).                                                                                                                                                                                                                                                  |
| [**хттпсендрекуестекс**](/windows/desktop/api/wininet/nf-wininet-httpsendrequestexa)                     | [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                       | Невозможно предоставить буферы.                                                                                                                                                                                                                                                                                                          |
| [**интернетканоникализеурл**](/windows/desktop/api/wininet/nf-wininet-internetcanonicalizeurla)         | Эквивалент отсутствует                                                                                                                                                                                          | URL-адреса теперь помещаются в каноническую форму в [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).                                                                                                                                                                                                                                              |
| [**интернетчеккконнектион**](/windows/desktop/api/wininet/nf-wininet-internetcheckconnectiona)         | Эквивалент отсутствует                                                                                                                                                                                          | Не реализовано в WinHTTP.                                                                                                                                                                                                                                                                                                          |
| [**интернетклосехандле**](/windows/desktop/api/wininet/nf-wininet-internetclosehandle)                 | [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)                                                                                                                                                       | Закрытие родительского дескриптора в WinHTTP не приводит к рекурсивному закрытию дочерних дескрипторов.                                                                                                                                                                                                                                                         |
| [**интернеткомбинеурл**](/windows/desktop/api/wininet/nf-wininet-internetcombineurla)                   | Эквивалент отсутствует                                                                                                                                                                                          | Для сборки URL-адресов можно использовать функцию [**винхттпкреатеурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) .                                                                                                                                                                                                                                                |
| [**интернетконфирмзонекроссинг**](/windows/desktop/api/wininet/nf-wininet-internetconfirmzonecrossing) | Эквивалент отсутствует                                                                                                                                                                                          | Не реализовано в WinHTTP.                                                                                                                                                                                                                                                                                                          |
| [**интернетконнект**](/windows/desktop/api/wininet/nf-wininet-internetconnecta)                         | [**винхттпконнект**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                                                                                               | Значение контекста задается с помощью [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) или [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Параметры запроса задаются с помощью [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). Учетные данные пользователя задаются с помощью [**винхттпсеткредентиалс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).                                 |
| [**интернеткраккурл**](/windows/desktop/api/wininet/nf-wininet-internetcrackurla)                       | [**винхттпкраккурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)                                                                                                                                                             | Противоположное поведение \_ флага escape-последовательности ICU: при использовании [**интернеткраккурл**](/windows/desktop/api/wininet/nf-wininet-internetcrackurla)этот флаг приводит к преобразованию escape-последовательностей (% XX) в символы, но с [**винхттпкраккурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)это приводит к тому, что символы, которые должны быть экранированы из HTTP-запроса, преобразуются в управляющие последовательности. |
| [**интернеткреатеурл**](/windows/desktop/api/wininet/nf-wininet-internetcreateurla)                     | [**винхттпкреатеурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)                                                                                                                                                           | Отсутствует.                                                                                                                                                                                                                                                                                                                                |
| [**интернетеррордлг**](/windows/desktop/api/wininet/nf-wininet-interneterrordlg)                       | Эквивалент отсутствует                                                                                                                                                                                          | Поскольку служба WinHTTP нацелена на приложения на стороне сервера, она не реализует пользовательский интерфейс.                                                                                                                                                                                                                                   |
| [**интернетжеткукие**](/windows/desktop/api/wininet/nf-wininet-internetgetcookiea)                     | Эквивалент отсутствует                                                                                                                                                                                          | Служба WinHTTP не сохраняет данные между сеансами и не может получить доступ к файлам cookie WinINet.                                                                                                                                                                                                                                                    |
| [**интернетопен**](/windows/desktop/api/wininet/nf-wininet-internetopena)                               | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                                                                                     | Отсутствует.                                                                                                                                                                                                                                                                                                                                |
| [**интернетопенурл**](/windows/desktop/api/wininet/nf-wininet-internetopenurla)                         | [**Винхттпконнект**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect), [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) | Эта функция доступна в перечисленных функциях WinHTTP.                                                                                                                                                                                                                                                                     |
| [**интернеткуеридатааваилабле**](/windows/desktop/api/wininet/nf-wininet-internetquerydataavailable)   | [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)                                                                                                                                         | Нет зарезервированных параметров.                                                                                                                                                                                                                                                                                                              |
| [**интернеткуерйоптион**](/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona)                 | [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)                                                                                                                                                       | WinHTTP предлагает другой набор параметров от WinINet. Дополнительные сведения и параметры, предлагаемые WinHTTP, см. в разделе [**флаги параметров**](option-flags.md).                                                                                                                                                                               |
| [**интернетреадфиле**](/windows/desktop/api/wininet/nf-wininet-internetreadfile)                       | [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)                                                                                                                                                             | Отсутствует.                                                                                                                                                                                                                                                                                                                                |
| [**интернетреадфиликс**](/windows/desktop/api/wininet/nf-wininet-internetreadfileexa)                   | [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)                                                                                                                                                             | Вместо структуры буфер является областью памяти, адресованной указателю.                                                                                                                                                                                                                                                  |
| [**интернетсетоптион**](/windows/desktop/api/wininet/nf-wininet-internetsetoptiona)                     | [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)                                                                                                                                                           | Отсутствует.                                                                                                                                                                                                                                                                                                                                |
| [**интернетсетстатускаллбакк**](/windows/desktop/api/wininet/nf-wininet-internetsetstatuscallback)     | [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)                                                                                                                                           | Дополнительные сведения см. в подразделе «различные методы обработки асинхронных запросов» этого раздела.                                                                                                                                                                                                                                               |
| [**интернеттимефромсистемтиме**](/windows/desktop/api/wininet/nf-wininet-internettimefromsystemtime)   | [**винхттптимефромсистемтиме**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)                                                                                                                                         | Отсутствует.                                                                                                                                                                                                                                                                                                                                |
| [**интернеттиметосистемтиме**](/windows/desktop/api/wininet/nf-wininet-internettimetosystemtime)       | [**винхттптиметосистемтиме**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)                                                                                                                                             | Отсутствует.                                                                                                                                                                                                                                                                                                                                |
| [**интернетвритефиле**](/windows/desktop/api/wininet/nf-wininet-internetwritefile)                     | [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)                                                                                                                                                           | Отсутствует.                                                                                                                                                                                                                                                                                                                                |



 

## <a name="different-handling-of-asynchronous-requests"></a>Разная Обработка асинхронных запросов

Имейте в виду, что в WinINet и WinHTTP некоторые функции могут выполнять асинхронные запросы синхронно или асинхронно. Приложение должно работать в любой ситуации. Существуют значительные отличия в том, как WinINet и WinHTTP обрабатывают эти потенциально асинхронные функции.

Операционной

-   Синхронное завершение: Если потенциально асинхронный вызов функции WinINet завершается синхронно, выходные параметры функции возвращают результаты операции. При возникновении ошибки извлеките код ошибки, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) после вызова функции WinInet.

-   Асинхронное завершение: Если потенциально асинхронный вызов функции завершается асинхронно, результаты операции и любые ошибки становятся доступными в функции обратного вызова. Функция обратного вызова выполняется в рабочем потоке, а не в потоке, который выполнил первоначальный вызов функции.

Иными словами, приложение должно дублировать логику для обработки результатов таких операций в двух местах: сразу после вызова функции и в функции обратного вызова.

Служба WinHTTP упрощает эту модель, позволяя реализовать операционную логику только в функции обратного вызова, которая получает уведомление о завершении независимо от того, завершилась ли операция синхронно или асинхронно. Если асинхронная операция включена, параметры OUT функций WinHTTP не возвращают значимые данные и должны иметь значение **null**.

Единственным существенным различием между асинхронным и синхронным завершением в WinHTTP с точки зрения приложения является место, где выполняется функция обратного вызова.

Известен

-   Синхронное завершение: когда операция завершается синхронно, результаты возвращаются в функцию обратного вызова, которая выполняется в том же потоке, что и исходный вызов функции.

-   Асинхронное завершение: когда операция завершается асинхронно, результаты возвращаются в функции обратного вызова, которая выполняется в рабочем потоке.

Несмотря на то, что большинство ошибок может обрабатываться полностью в рамках функции обратного вызова, приложения WinHTTP должны быть готовы к тому, чтобы функция возвращала **значение false** из-за ошибки \_ недопустимого \_ параметра или другой подобной ошибки, полученной при вызове [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

В отличие от WinINet, который может выполнять несколько асинхронных операций одновременно, WinHTTP применяет политику для одной ожидающей асинхронной операции на каждый обработчик запроса. Если одна операция находится в состоянии ожидания и вызывается другая функция WinHTTP, вторая функция завершается ошибкой, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку \_ Недопустимая \_ операция.

Служба WinHTTP упрощает эту модель, позволяя реализовать операционную логику только в функции обратного вызова, которая получает уведомление о завершении независимо от того, завершилась ли операция синхронно или асинхронно. Если асинхронная операция включена, параметры OUT функций WinHTTP не возвращают значимые данные и должны иметь значение **null**.

## <a name="differences-in-winhttp-callback-notifications"></a>Различия в уведомлениях обратного вызова WinHTTP

Функция обратного вызова состояния получает обновления состояния операций с помощью флагов уведомлений. В WinHTTP уведомления выбираются с помощью параметра *двнотификатионфлагс* функции [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) . Используйте флаг **\_ обратного вызова WinHTTP \_ \_ все \_ уведомления** , чтобы получать уведомления обо всех обновлениях состояния.

Уведомления, указывающие на завершение определенной операции, называются уведомлениями о завершении или просто завершением. В WinINet каждый раз, когда функция обратного вызова получает завершение, параметр *лпвстатусинформатион* содержит [**\_ \_ результирующую структуру Internet Async**](/windows/desktop/api/wininet/ns-wininet-internet_async_result) . В WinHTTP эта структура недоступна для всех завершений. Важно ознакомиться со страницей ссылки для [**\_ \_ обратного вызова состояния WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback), который содержит сведения об уведомлениях и о типе данных, которые могут быть ожидаемыми для каждого из них.

В WinHTTP одна операция завершения, **\_ \_ \_ \_ Ошибка запроса состояния обратного вызова WinHTTP**, указывает на сбой операции. Все остальные завершения указывают на успешную операцию.

И WinINet, и WinHTTP используют определяемое пользователем значение контекста для передачи информации из основного потока в функцию обратного вызова состояния, которая может быть выполнена в рабочем потоке. В WinINet значение контекста, используемое функцией обратного вызова состояния, задается путем вызова одной из нескольких функций. В WinHTTP значение контекста задается только с помощью [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) или [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). В связи с этим в WinHTTP может происходить уведомление до установки значения контекста. Если функция обратного вызова получает уведомление до установки значения контекста, приложение должно быть подготовлено к получению значения **null** в параметре *двконтекст* функции обратного вызова.

## <a name="authentication-differences"></a>Различия в проверке подлинности

В WinINet учетные данные пользователя задаются путем вызова функции [**интернетсетоптион**](/windows/desktop/api/wininet/nf-wininet-internetsetoptiona) с использованием кода, аналогичного приведенному в следующем примере кода.

``` syntax
// Use the WinINet InternetSetOption function to set the 
// user credentials to the user name contained in strUsername 
// and the password to the contents of strPassword.
       
InternetSetOption( hRequest, INTERNET_OPTION_PROXY_USERNAME, 
                   strUsername, strlen(strUsername) + 1 );

InternetSetOption( hRequest, INTERNET_OPTION_PROXY_PASSWORD, 
                   strPassword, strlen(strPassword) + 1 );
```

Для совместимости учетные данные пользователя также можно задать в WinHTTP с помощью функции [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , но это не рекомендуется, так как это может привести к уязвимости системы безопасности.

Вместо этого, когда приложение получает код состояния 401 в WinHTTP, рекомендуемый метод настройки учетных данных — сначала определить схему проверки подлинности с помощью [**винхттпкуеряуссчемес**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) и, во-вторых, задать учетные данные с помощью [**винхттпсеткредентиалс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials). В следующем примере кода показано, как это сделать.

``` syntax
DWORD dwSupportedSchemes;
DWORD dwPrefered;
DWORD dwTarget;

// Obtain the supported and first schemes.
WinHttpQueryAuthSchemes( hRequest, &dwSupportedSchemes, &dwPrefered, &dwTarget );

// Set the credentials before resending the request.
WinHttpSetCredentials( hRequest, dwTarget, dwPrefered, strUsername, strPassword, NULL );
```

Так как в WinHTTP нет эквивалента [**интернетеррордлг**](/windows/desktop/api/wininet/nf-wininet-interneterrordlg) , приложения, которые получают учетные данные через пользовательский интерфейс, должны предоставлять собственный интерфейс.

В отличие от WinINet, WinHTTP не кэширует пароли. Для каждого запроса необходимо указать действительные учетные данные пользователя.

Служба WinHTTP не поддерживает схему распределенных паролей с проверкой подлинности (DPA), поддерживаемую WinINet. Однако WinHTTP поддерживает Microsoft Passport 1,4. Дополнительные сведения об использовании проверки подлинности Passport в WinHTTP см. в статье Проверка подлинности [Passport в WinHTTP](passport-authentication-in-winhttp.md).

Служба WinHTTP не использует параметры Internet Explorer для определения политики автоматического входа в систему. Вместо этого для политики автоматического входа задано значение [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Дополнительные сведения о проверке подлинности в WinHTTP, включая политику автоматического входа, см. [в статье Проверка подлинности в WinHTTP](authentication-in-winhttp.md).

## <a name="differences-in-secure-http-transactions"></a>Различия в защищенных транзакциях HTTP

В WinINet запустите безопасный сеанс с помощью [**хттпопенрекуест**](/windows/desktop/api/wininet/nf-wininet-httpopenrequesta) или [**интернетконнект**](/windows/desktop/api/wininet/nf-wininet-internetconnecta), но в WinHTTP необходимо вызвать [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) с помощью флага **\_ \_ Secure** флага WinHTTP.

В безопасной транзакции HTTP сертификаты сервера можно использовать для проверки подлинности сервера для клиента. В WinINet, если сертификат сервера содержит ошибки, [**хттпсендрекуест**](/windows/desktop/api/wininet/nf-wininet-httpsendrequesta) завершается сбоем и предоставляет сведения об ошибках сертификата.

В WinHttp ошибки сертификата сервера обрабатываются в соответствии с версией следующим образом.

-   Начиная с WinHttp 5,1, если сертификат сервера завершается ошибкой или содержит ошибки, вызов [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) сообщает о **\_ состоянии обратного вызова WinHTTP, \_ \_ защищенном \_** в функции обратного вызова. Если ошибка, созданная **WinHttpSendRequest** , игнорируется, последующие вызовы [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) завершаются ошибкой, \_ когда \_ Операция WinHTTP \_ отменила ошибку.
-   В WinHTTP 5,0 ошибки в сертификатах сервера по умолчанию не вызывают ошибку запроса. Вместо этого ошибки выводятся в функции обратного вызова с уведомлением о **\_ \_ \_ \_ сбое обратного вызова WinHTTP** .

на некоторых более ранних платформах WinINet поддерживал протоколы исключительно (PCT) и (или) Fortezza, хотя и не в Windows XP.

Служба WinHTTP не поддерживает протоколы PCT и Fortezza на любой платформе, а использует SSL (SSL) 2,0, SSL 3,0 или TLS 1,0.

 

 
