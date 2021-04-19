---
title: Обработка проверки подлинности
description: Перед предоставлением доступа к ресурсам в Интернете некоторым учетным записям-посредникам и серверам требуется проверка подлинности.
ms.assetid: f3752031-30d3-4e35-8eae-1d4971b66bc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82d8cd93f1010c71560d856793ad06d8bc5d9d5
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380858"
---
# <a name="handling-authentication"></a>Обработка проверки подлинности

Перед предоставлением доступа к ресурсам в Интернете некоторым учетным записям-посредникам и серверам требуется проверка подлинности. Функции WinINet поддерживают проверку подлинности сервера и прокси для сеансов HTTP. Проверка подлинности FTP-серверов должна обрабатываться функцией [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) . В настоящее время проверка подлинности через FTP-шлюз не поддерживается.

## <a name="about-http-authentication"></a>Об аутентификации HTTP

Если требуется проверка подлинности, клиентское приложение получает код состояния 401, если для сервера требуется проверка подлинности или 407, если прокси-сервер требует проверки подлинности. С кодом состояния прокси или сервер отправляет один или несколько заголовков ответа с проверкой подлинности — прокси-проверка подлинности (для проверки подлинности прокси) или WWW-Authenticate (для проверки подлинности сервера).

Каждый заголовок ответа проверки подлинности содержит доступную схему проверки подлинности и область. Если поддерживаются несколько схем проверки подлинности, сервер возвращает несколько заголовков ответа проверки подлинности. Значение области чувствительно к регистру и определяет пространство защиты на прокси или сервере. Например, заголовок "WWW-Authenticate: Basic realm =", например "" является примером заголовка, возвращаемого при необходимости проверки подлинности сервера.

Клиентское приложение, отправившего запрос, может пройти проверку подлинности, включив поле заголовка авторизации с запросом. Заголовок авторизации будет содержать схему проверки подлинности и соответствующий ответ, необходимый для этой схемы. Например, заголовок "Authorization: Basic \<username:password> " будет добавлен в запрос и повторно отправлен на сервер, если клиент получил заголовок ответа проверки подлинности "WWW-Authenticate: Basic realm =" example "".

Существует два общих типа схем проверки подлинности:

-   Базовая схема проверки подлинности, в которой имя пользователя и пароль отправляются на сервер открытым текстом.
-   Схемы "запрос — ответ", которые позволяют использовать формат "запрос — ответ".

Основная схема проверки подлинности основана на модели, которую клиент должен пройти для проверки подлинности с помощью имени пользователя и пароля для каждой области. Сервер служб отправляет запрос при повторной отправку с помощью заголовка авторизации, включающего допустимые имя пользователя и пароль.

Схемы "запрос — ответ" обеспечивают более безопасную проверку подлинности. Если запрос требует проверки подлинности с помощью схемы запроса и ответа, клиенту возвращается соответствующий код состояния и заголовки проверки подлинности. Клиент должен повторно отправить запрос с помощью Negotiate. Сервер возвратит соответствующий код состояния с запросом, и клиент потребует повторно отправить запрос с правильным ответом, чтобы получить запрошенную службу.

В следующей таблице перечислены схемы проверки подлинности, тип проверки подлинности, Библиотека DLL, которая их поддерживает, и описание схемы.



| Схема                                    | Тип               | DLL                  | Описание                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------|--------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Базовый (открытый текст)                         | basic              | Wininet.dll          | Использует строку в кодировке Base64, содержащую имя пользователя и пароль.                                                                                                                                                                                                                                                                             |
| Digest (дайджест)                                    | запрос-ответ | Digest.dll           | Схема "запрос — ответ", которая дает трудности при использовании nonce (определяемая сервером строка данных). Допустимый ответ содержит контрольную сумму имени пользователя, пароля, заданного значения nonce, метода HTTP и запрошенного универсального кода ресурса (URI). Поддержка дайджест-проверки подлинности появилась в Microsoft Internet Explorer 5. |
| Диспетчер LAN NT (NTLM)                     | запрос-ответ | Winsspi.dll          | Схема запроса и ответа, которая основывается на имени пользователя.                                                                                                                                                                                                                                                                             |
| Сеть Microsoft (MSN)                   | запрос-ответ | Msnsspc.dll          | Схема проверки подлинности сети Майкрософт.                                                                                                                                                                                                                                                                                                     |
| Распределенная проверка пароля (DPA) | запрос-ответ | Msapsspc.dll         | Аналогичен проверке подлинности MSN и также используется сетью Майкрософт.                                                                                                                                                                                                                                                                           |
| Проверка подлинности удаленной парольной фразы (РПА)    | CompuServe         | Rpawinet.dll, da.dll | Схема проверки подлинности CompuServe. Дополнительные сведения см. в [спецификации механизма РПА](https://www.compuserve.com/).                                                                                                                                                                                                    |



 

Для всех, кроме обычной проверки подлинности, необходимо настроить разделы реестра в дополнение к установке соответствующей библиотеки DLL.

Если требуется проверка подлинности, в вызове [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)следует использовать флаг [ \_ \_ \_ подключения к Интернету](api-flags.md) . \_ \_ Флаг подключения к Интернету \_ необходим для проверки подлинности NTLM и других типов аутентификации, чтобы обеспечить подключение при завершении процесса проверки подлинности. Если соединение не сохраняется, процесс проверки подлинности должен быть перезапущен с прокси-сервером или с сервера.

Функции [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) и [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) успешно выполнены, даже если требуется проверка подлинности. Разница заключается в том, что данные, возвращаемые в файлах заголовков и [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) , ПОлучит HTML-страницу с уведомлением пользователя о коде состояния.

### <a name="registering-authentication-keys"></a>Регистрация ключей проверки подлинности

В \_ \_ \_ разделе "Конфигурация открытых типов в Интернете" рассматриваются значения реестра **Проксенабле**, **proxyserver** и **проксйоверриде**. Эти значения находятся в разделе **hKey \_ Current \_ User** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet Settings**.

Для схем проверки подлинности, отличных от Basic, необходимо добавить ключ в реестр в разделе **hKey \_ Local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**. Значение **DWORD** , **flags**, должно быть задано соответствующим значением. В следующем списке приведены возможные значения **флагов** .

-   \_Флаг проверки подлинности подключаемого модуля \_ \_ уникальный \_ контекст \_ на \_ TCP/IP (значение = 0x01)

    Каждый сокет TCP/IP протокола управления передачей содержит другой контекст. В противном случае для каждого шаблона области или URL-адреса блока передается новый контекст.

-   \_Флаги проверки подлинности подключаемого модуля \_ \_ могут \_ управлять \_ пользовательским интерфейсом (значение = 0x02)

    Эта библиотека DLL может работать с собственными данными, введенными пользователем.

-   \_Флаги проверки подлинности подключаемого модуля \_ \_ могут \_ \_ не работать без \_ PASSWD (значение = 0x04)

    Эта библиотека DLL может выполнять проверку подлинности без запроса пароля пользователем.

-   \_Флаги проверки подлинности подключаемого модуля \_ \_ без \_ области (значение = 0x08)

    Эта библиотека DLL не использует стандартную строку области HTTP. Все данные, которые отображаются как область, представляют собой данные, относящиеся к схеме.

-   \_Флаги проверки активности подключаемого модуля \_ \_ \_ \_ не \_ требуются (значение = 0x10)

    Эта библиотека DLL не требует постоянного подключения для своей последовательности "запрос — ответ".

Например, чтобы добавить проверку подлинности NTLM, необходимо добавить ключ NTLM в раздел **hKey \_ Локальное \_ компьютерное** \\ **программное обеспечение** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**. В **разделе \_ hKey локальный \_ компьютер** \\ **программное обеспечение** \\ **Microsoft** \\ **Internet Explorer** \\ **Security** \\ **NTLM** необходимо добавить строковое значение, **дллфиле** и значение **DWORD** , **flags**. Для **дллфиле** необходимо задать значение Winsspi.dll, а для **флагов** должно быть задано значение 0x08.

### <a name="server-authentication"></a>Проверка подлинности сервера

Когда сервер получает запрос, требующий проверки подлинности, сервер возвращает сообщение с кодом состояния 401. В этом сообщении сервер должен содержать один или несколько WWW-Authenticate заголовков ответа. Эти заголовки содержат методы проверки подлинности, доступные для сервера. WinINet выбирает первый распознаваемый метод.

Обычная проверка подлинности обеспечивает слабую безопасность, если канал не зашифрован с помощью SSL или PCT.

Функцию [**интернетеррордлг**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) можно использовать для получения данных имени пользователя и пароля от пользователя, а также для получения данных с помощью настраиваемого пользовательского интерфейса.

Пользовательский интерфейс может использовать функцию [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) , чтобы задать значения параметров [" \_ \_ пароль в Интернете](option-flags.md) " и [ \_ "параметр \_ Интернета](option-flags.md) ", а затем повторно отправить запрос на сервер.

### <a name="proxy-authentication"></a>Проверка подлинности прокси

Когда клиент пытается использовать прокси-сервер, требующий проверки подлинности, прокси-сервер возвращает клиенту сообщение с кодом состояния 407. В этом сообщении прокси-сервер должен содержать один или несколько Proxy-Authenticate заголовков ответа. Эти заголовки включают методы проверки подлинности, доступные из прокси-сервера. WinINet выбирает первый распознаваемый метод.

Функцию [**интернетеррордлг**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) можно использовать для получения данных имени пользователя и пароля от пользователя, а также для разработки настраиваемого пользовательского интерфейса.

Пользовательский интерфейс может использовать функцию [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) для задания [ \_ \_ \_ пароля прокси-сервера](option-flags.md) и параметров Интернета, а затем повторно отправить запрос на прокси-сервер [ \_ \_ \_](option-flags.md) .

Если имя пользователя и пароль прокси-сервера не заданы, WinINet пытается использовать имя пользователя и пароль для сервера. Такое поведение позволяет клиентам реализовать тот же пользовательский интерфейс, который используется для проверки подлинности сервера.

## <a name="handling-http-authentication"></a>Обработка проверки подлинности HTTP

Проверка подлинности HTTP может быть обработана с помощью [**интернетеррордлг**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) или настраиваемой функции, которая использует [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) или добавляет собственные заголовки проверки подлинности. [**Интернетеррордлг**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) может проверить заголовки, связанные с маркером [**хинтернет**](appendix-a-hinternet-handles.md) , чтобы найти скрытые ошибки, такие как коды состояния от прокси-сервера или на сервере. [**Интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) можно использовать для задания имени пользователя и пароля для прокси и сервера. Для проверки подлинности MSN и DPA необходимо использовать [**интернетеррордлг**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) для задания имени пользователя и пароля.

Для любой настраиваемой функции, добавляющей собственные заголовки WWW-Authenticate или Proxy-Authenticate, [флаг \_ Internet \_ флаг \_ проверки подлинности не](api-flags.md) должен быть установлен для отключения проверки подлинности.

В следующем примере показано, как [**интернетеррордлг**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) можно использовать для проверки подлинности HTTP.


```C++
HINTERNET hOpenHandle,  hConnectHandle, hResourceHandle;
DWORD dwError, dwErrorCode;
HWND hwnd = GetConsoleWindow();

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG, 
                           NULL, NULL, 0);

hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"), 
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL, 
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL, 
                                  INTERNET_FLAG_KEEP_CONNECTION, 0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

// dwErrorCode stores the error code associated with the call to
// HttpSendRequest.  

dwErrorCode = hResourceHandle ? ERROR_SUCCESS : GetLastError();

dwError = InternetErrorDlg(hwnd, hResourceHandle, dwErrorCode, 
                           FLAGS_ERROR_UI_FILTER_FOR_ERRORS | 
                           FLAGS_ERROR_UI_FLAGS_CHANGE_OPTIONS |
                           FLAGS_ERROR_UI_FLAGS_GENERATE_DATA,
                           NULL);

if (dwError == ERROR_INTERNET_FORCE_RETRY)
    goto resend;

// Insert code to read the data from the hResourceHandle
// at this point.

```



В этом примере Дверроркоде используется для хранения любых ошибок, связанных с вызовом [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). [**Хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) завершается успешно, даже если прокси или сервер требует проверки подлинности. Если в \_ \_ \_ \_ интернетеррордлг передается флаг "Фильтрация пользовательского интерфейса для ошибок" \_ , функция проверяет заголовки на наличие скрытых ошибок. [](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) Эти скрытые ошибки включают в себя любые запросы на проверку подлинности. [**Интернетеррордлг**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) отображает соответствующее диалоговое окно, в котором пользователю предлагается ввести необходимые данные. Флаги пользовательского интерфейса с флагами \_ ошибок " \_ \_ \_ создать данные" \_ и "флаги \_ \_ пользовательского интерфейса ошибок" \_ \_ \_ также должны передаваться в [**интернетеррордлг**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), чтобы функция создавала соответствующую структуру данных для ошибки и сохраняла результаты диалогового окна в обработчике [**хинтернет**](appendix-a-hinternet-handles.md) .

В следующем примере кода показано, как можно обработать проверку подлинности с помощью [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


```C++
HINTERNET hOpenHandle,  hResourceHandle, hConnectHandle;
DWORD dwStatus;
DWORD dwStatusSize = sizeof(dwStatus);
char strUsername[64], strPassword[64];

// Normally, hOpenHandle, hResourceHandle,
// and hConnectHandle need to be properly assigned.

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG,
                           NULL, NULL, 0);
hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"),
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL,
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL,
                                  INTERNET_FLAG_KEEP_CONNECTION,
                                  0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

HttpQueryInfo(hResourceHandle, HTTP_QUERY_FLAG_NUMBER |
              HTTP_QUERY_STATUS_CODE, &dwStatus, &dwStatusSize, NULL);

switch (dwStatus)
{
    // cchUserLength is the length of strUsername and
    // cchPasswordLength is the length of strPassword.
    DWORD cchUserLength, cchPasswordLength;

    case HTTP_STATUS_PROXY_AUTH_REQ: // Proxy Authentication Required
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert appropriate error handling code.
        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_USERNAME,
                          strUsername,
                          cchUserLength+1);

        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_PASSWORD,
                          strPassword,
                          cchPasswordLength+1);
        goto resend;
        break;

    case HTTP_STATUS_DENIED:     // Server Authentication Required.
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert error handling code as
        // appropriate.
        InternetSetOption(hResourceHandle, INTERNET_OPTION_USERNAME,
                          strUsername, cchUserLength+1);
        InternetSetOption(hResourceHandle, INTERNET_OPTION_PASSWORD,
                          strPassword, cchPasswordLength+1);
        goto resend;
        break;
}

// Insert code to read the data from the hResourceHandle
// at this point.

```



> [!Note]  
> WinINet не поддерживает реализации серверов. Кроме того, его не следует использовать из службы. Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 