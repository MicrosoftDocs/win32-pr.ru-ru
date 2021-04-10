---
title: Настройка и получение свойств браузера
description: В этом разделе описано, как задать и получить свойства Интернета с помощью функций Интернетсетоптион и Интернеткуерйоптион.
ms.assetid: b596a4a9-c34a-402a-af76-b930fe5f0901
keywords:
- Настройка и получение свойств браузера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418bf21620cf7b7c4426844c95a39ef1fde04e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890953"
---
# <a name="setting-and-retrieving-internet-options"></a>Настройка и получение свойств браузера

В этом разделе описано, как задать и получить свойства Интернета с помощью функций [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) и [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) .

Свойства Интернета можно задать для или получить с помощью указанного обработчика [**хинтернет**](appendix-a-hinternet-handles.md) или текущих параметров в Microsoft Internet Explorer.

-   [Шаги реализации](#implementation-steps)
    -   [Выбор свойств браузера](#choosing-internet-options)
    -   [Выбор маркера ХИНТЕРНЕТ](#choosing-the-hinternet-handle)
    -   [Установка или получение параметров](#setting-or-retrieving-the-options)
-   [Область действия маркера ХИНТЕРНЕТ](#scope-of-hinternet-handle)
-   [Настройка отдельных параметров](#setting-individual-options)
-   [Получение отдельных параметров](#retrieving-individual-options)
    -   [Полный пример](#complete-sample)
-   [Настройка параметров соединения](#setting-connection-options)
-   [Получение параметров соединения](#retrieving-connection-options)
-   [См. также](#related-topics)

## <a name="implementation-steps"></a>Шаги реализации

Чтобы задать или получить свойства Интернета, выполните следующие действия.

-   [Выбор свойств браузера](#choosing-internet-options)
-   [Выбор маркера ХИНТЕРНЕТ](#choosing-the-hinternet-handle)
-   [Установка или получение параметров](#setting-or-retrieving-the-options)

### <a name="choosing-internet-options"></a>Выбор свойств браузера

Так как существует много параметров Интернета, важно выбрать правильный вариант. Многие свойства Интернета влияют на поведение функций WinINet и Internet Explorer.

Например, администратор может сделать следующее:

-   Обрабатывайте обычную проверку подлинности сервера и прокси, задав имена пользователей и пароли.
-   Задайте или получите строку агента пользователя, используемую серверами для определения функций клиентского приложения или браузера.
-   Получите тип маркера для указанного обработчика [**хинтернет**](appendix-a-hinternet-handles.md) .

Дополнительные сведения и список свойств Интернета см. в разделе [**Флаги**](option-flags.md)параметров.

В Internet Explorer 5 и более поздних версиях некоторые параметры могут быть заданы или получены из конкретного подключения к Интернету с помощью [**\_ \_ \_ \_ списка параметров «через Интернет на подключение»**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) и « [**\_ в сети \_ \_ » для каждой**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) структуры. Дополнительные сведения и список параметров, которые можно задать или получить из конкретного подключения к Интернету, см. в разделе **двоптионс** элемента структуры [**Internet \_ per \_ conn \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .

### <a name="choosing-the-hinternet-handle"></a>Выбор маркера ХИНТЕРНЕТ

Обработчик [**хинтернет**](appendix-a-hinternet-handles.md) , используемый для задания или получения свойств Интернета, определяет область действия операции. Все дескрипторы, созданные с помощью этого дескриптора, наследуют параметры, заданные для этого дескриптора.

Например, клиентские приложения, которым требуется прокси-сервер с проверкой подлинности, возможно, не занимают имя пользователя и пароль прокси-сервера каждый раз, когда приложение пытается получить доступ к ресурсу в Интернете. Если все запросы к определенному соединению обрабатываются одним и тем же прокси-сервером, то задание имени и пароля пользователя прокси-сервера для типа соединения [**хинтернет**](appendix-a-hinternet-handles.md) Handle, то есть маркера, созданного вызовом [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), позволит всем вызовам, производным от этого **хинтернет** , использовать одно и то же имя пользователя и пароль прокси-сервера. Задание имени и пароля пользователя прокси-сервера при каждом создании обработчика **хинтернет** с помощью [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) потребует дополнительных и ненужных затрат. Имейте в виду, что если приложение использует прокси-сервер, требующий проверки подлинности, он должен задать учетные данные прокси-сервера для каждого нового соединения.

### <a name="setting-or-retrieving-the-options"></a>Установка или получение параметров

Когда вы определяете, какие свойства Интернета и [**хинтернет**](appendix-a-hinternet-handles.md) использовать, извлеките эти свойства Интернета. Чтобы задать или получить параметры, вызовите либо [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) , либо [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

## <a name="scope-of-hinternet-handle"></a>Область действия маркера ХИНТЕРНЕТ

Обработчик [**хинтернет**](appendix-a-hinternet-handles.md) , используемый для задания или получения свойств Интернета, определяет действия, для которых параметры являются допустимыми.

Эти маркеры имеют три уровня:

-   Корневой обработчик [**хинтернет**](appendix-a-hinternet-handles.md) (созданный вызовом [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena)) будет содержать все свойства Интернета, влияющие на этот экземпляр WinInet.
-   Дескрипторы [**хинтернет**](appendix-a-hinternet-handles.md) , которые подключаются к серверу (созданному путем вызова [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta));
-   Дескрипторы [**хинтернет**](appendix-a-hinternet-handles.md) , связанные с ресурсом или перечислением ресурсов на определенном сервере.

В дополнение к различным дескрипторам [**хинтернет**](appendix-a-hinternet-handles.md) , приложение может также использовать **null** для установки или получения значений по умолчанию параметров Интернета, используемых Internet Explorer и функциями WinInet. При задании свойств Интернета при использовании значения **null** в качестве маркера изменяются значения параметров по умолчанию, которые в настоящее время хранятся в реестре. Клиентские приложения не должны использовать функции реестра для изменения значений свойств обозревателя по умолчанию, так как в будущем можно изменить способ хранения параметров.

В следующей таблице перечислены типы дескрипторов [**хинтернет**](appendix-a-hinternet-handles.md) и области связанных с ними параметров Интернета.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Тип обработчика</th>
<th>Область</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>NULL</strong></td>
<td>Параметры по умолчанию для Internet Explorer.</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_CONNECT_FTP</td>
<td>Параметры для этого соединения с FTP-сервером. Эти параметры влияют на любые операции, инициированные этим обработчиком <a href="appendix-a-hinternet-handles.md"><strong>хинтернет</strong></a> , такие как файлы для загрузки.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_CONNECT_GOPHER</td>
<td>Параметры для этого подключения к серверу Gopher. Эти параметры влияют на любые операции, инициированные этим обработчиком <a href="appendix-a-hinternet-handles.md"><strong>хинтернет</strong></a> , такие как файлы для загрузки.
<blockquote>
[!Note]<br />
Windows XP и Windows Server 2003 R2 и более ранних версий.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_CONNECT_HTTP</td>
<td>Параметры для этого соединения с HTTP-сервером. Эти параметры влияют на любые операции, инициированные этим обработчиком <a href="appendix-a-hinternet-handles.md"><strong>хинтернет</strong></a> , такие как файлы для загрузки.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_FILE_REQUEST</td>
<td>Параметры, связанные с этим запросом файла.</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_FTP_FILE</td>
<td>Параметры, связанные с этим скачиванием FTP-ресурса.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_FTP_FILE_HTML</td>
<td>Параметры, связанные с этим FTP-ресурсом, загружаются в формате HTML.</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_FTP_FIND</td>
<td>Параметры, связанные с этим поиском файлов на FTP-сервере.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_FTP_FIND_HTML</td>
<td>Параметры, связанные с этим поиском файлов на FTP-сервере, отформатированном в формате HTML.</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_GOPHER_FILE</td>
<td>Параметры, связанные с этим скачиванием ресурса Gopher.
<blockquote>
[!Note]<br />
Windows XP и Windows Server 2003 R2 и более ранних версий.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML</td>
<td>Параметры, связанные с этим ресурсом Gopher, загружаются в формате HTML.
<blockquote>
[!Note]<br />
Windows XP и Windows Server 2003 R2 и более ранних версий.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_GOPHER_FIND</td>
<td>Параметры, связанные с этим поиском файлов на сервере Gopher.
<blockquote>
[!Note]<br />
Windows XP и Windows Server 2003 R2 и более ранних версий.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML</td>
<td>Параметры, связанные с этим поиском файлов на сервере Gopher в формате HTML.
<blockquote>
[!Note]<br />
Windows XP и Windows Server 2003 R2 и более ранних версий.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_HTTP_REQUEST</td>
<td>Параметры, связанные с этим HTTP-запросом.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_INTERNET</td>
<td>Параметры, связанные с этим экземпляром функций WinINet.</td>
</tr>
</tbody>
</table>



 

## <a name="setting-individual-options"></a>Настройка отдельных параметров

После определения параметров Интернета, которые требуется задать, и области, на которую эти параметры влияют, Настройка параметров Интернета не является сложной. Все, что нужно сделать, — это вызвать функцию [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) с требуемым маркером [**хинтернет**](appendix-a-hinternet-handles.md) , флагом параметра Internet и буфером, который содержит нужные сведения.

В следующем примере показано, как задать имя пользователя и пароль учетной записи-посредника для указанного обработчика [**хинтернет**](appendix-a-hinternet-handles.md) .


```C++
// strUsername is a string buffer of cchMax characters or less.
// It contains the proxy user name.
size_t cchMax = 80;
size_t cchUserLength, cchPasswordLength;
HRESULT hr = StringCchLength(strUsername, cchMax, &cchUserLength);

if (SUCCEEDED(hr))
{
   // hOpen is the HINTERNET handle created by InternetConnect.
   InternetSetOption(hConnect, INTERNET_OPTION_PROXY_USERNAME,
      strUsername, DWORD(cchUserLength)+1);
}
else
{
   // Insert error handling code here.
}

// strPassword is the string buffer that contains the proxy password.
hr = StringCchLength(strPassword, cchMax, &cchPasswordLength);

InternetSetOption(hOpen, INTERNET_OPTION_PROXY_PASSWORD,
    strPassword, DWORD(cchPasswordLength)+1);
```



## <a name="retrieving-individual-options"></a>Получение отдельных параметров

Свойства браузера можно получить с помощью функции [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) . Чтобы получить свойства браузера, выполните следующие действия.

1.  Определите размер буфера, необходимый для получения сведений о параметрах Интернета.

    Размер буфера можно определить с помощью **значения NULL** для адреса буфера и передачи ему нулевого размера буфера.

    ```C++
    DWORD dwSize;
    InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);
    ```

    

    Значение, возвращаемое функцией [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) , — это объем памяти, необходимый для получения сведений в байтах.

2.  Выделение памяти для буфера.
    ```C++
    char *lpszData;
    lpszData = new char[dwSize];
    ```

    

3.  Получение данных.
    ```C++
    InternetQueryOption( NULL, 
                         INTERNET_OPTION_USER_AGENT,
                         lpszData, &dwSize );
    ```

    

4.  Освободите память.
    ```C++
    delete [] lpszData;
    ```

    

### <a name="complete-sample"></a>Полный пример

Ниже приведен полный пример, используемый в предыдущем разделе. В этом примере показано, как получить строку агента пользователя по умолчанию.


```C++
// This call determines the required buffer size.
DWORD dwSize;
InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);

// Allocate the necessary memory.
char *lpszData;
lpszData = new char[dwSize];

// Call InternetQueryOption again with the provided buffer.
InternetQueryOption( NULL, 
                     INTERNET_OPTION_USER_AGENT,
                     lpszData, &dwSize );

// Insert code here to use the user agent string data.

// Free the allocated memory.
delete [] lpszData;
```



## <a name="setting-connection-options"></a>Настройка параметров соединения

В Internet Explorer 5 и более поздних версиях для конкретного подключения можно задать свойства обозревателя. Ранее все подключения совместно использовали одни и те же настройки параметров Интернета. Чтобы задать параметры для конкретного подключения, выполните следующие действия.

1.  Создание структуры [**\_ \_ \_ \_ списка параметров для сети Интернет**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) .
2.  Выделите память для отдельных параметров Интернета, которые необходимо задать для подключения.
3.  Задайте параметры в структурах параметров [**сети Интернет \_ для каждого из \_ \_ них**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .
4.  Задайте параметры с помощью [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

В следующем примере кода показано, как задать данные прокси-сервера для подключения по локальной сети.


```C++
BOOL SetConnectionOptions()
{
    INTERNET_PER_CONN_OPTION_LIST list;
    BOOL    bReturn;
    DWORD   dwBufSize = sizeof(list);

    // Fill the list structure.
    list.dwSize = sizeof(list);

    // NULL == LAN, otherwise connectoid name.
    list.pszConnection = NULL;

    // Set three options.
    list.dwOptionCount = 3;
    list.pOptions = new INTERNET_PER_CONN_OPTION[3];

    // Ensure that the memory was allocated.
    if(NULL == list.pOptions)
    {
        // Return FALSE if the memory wasn't allocated.
        return FALSE;
    }

    // Set flags.
    list.pOptions[0].dwOption = INTERNET_PER_CONN_FLAGS;
    list.pOptions[0].Value.dwValue = PROXY_TYPE_DIRECT |
        PROXY_TYPE_PROXY;

    // Set proxy name.
    list.pOptions[1].dwOption = INTERNET_PER_CONN_PROXY_SERVER;
    list.pOptions[1].Value.pszValue = TEXT("https://proxy:80");

    // Set proxy override.
    list.pOptions[2].dwOption = INTERNET_PER_CONN_PROXY_BYPASS;
    list.pOptions[2].Value.pszValue = TEXT("local");

    // Set the options on the connection.
    bReturn = InternetSetOption(NULL,
        INTERNET_OPTION_PER_CONNECTION_OPTION, &list, dwBufSize);

    // Free the allocated memory.
    delete [] list.pOptions;

    return bReturn;
}
```



## <a name="retrieving-connection-options"></a>Получение параметров соединения

В Internet Explorer 5 и более поздних версиях свойства браузера можно получить из определенного подключения. Чтобы получить параметры из конкретного подключения, выполните следующие действия.

1.  Создание структуры [**\_ \_ \_ \_ списка параметров для сети Интернет**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) .
2.  Выделите память для отдельных параметров Интернета, которые необходимо получить из соединения.
3.  Укажите параметры с использованием [**структур \_ \_ \_ параметров "в сети Интернет"**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .
4.  Извлеките параметры с помощью [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).
5.  Используйте данные параметров.
6.  Освободите память, выделенную для хранения данных параметров, с помощью функции [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .

> [!Note]  
> WinINet не поддерживает реализации серверов. Кроме того, его не следует использовать из службы. Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Обработка проверки подлинности](handling-authentication.md)
</dt> <dt>

[Дескрипторы ХИНТЕРНЕТ](appendix-a-hinternet-handles.md)
</dt> </dl>

 

