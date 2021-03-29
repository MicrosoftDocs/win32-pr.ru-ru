---
title: Управление файлами cookie
description: В протоколе HTTP сервер или скрипт использует файлы cookie для сохранения сведений о состоянии на клиентской рабочей станции.
ms.assetid: c00279cf-9cdc-4caf-8549-af1851edfa25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0418442e961f6f4d3d2bcddb2c607ac9cf7928
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105654329"
---
# <a name="managing-cookies"></a>Управление файлами cookie

В протоколе HTTP сервер или скрипт использует файлы cookie для сохранения сведений о состоянии на клиентской рабочей станции. Для этой цели функции WinINet реализовали постоянную базу данных cookie. Их можно использовать для задания файлов cookie в и доступа к файлам cookie из базы данных cookie. Дополнительные сведения см. в разделе [файлы cookie HTTP](http-cookies.md).

Для управления файлами cookie можно использовать функции [**интернетсеткукие**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) и [**интернетжеткукие**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) .

## <a name="using-cookie-functions"></a>Использование функций cookie

Следующие функции позволяют приложению создавать или извлекать файлы cookie в базе данных cookie.



| Функция                                       | Описание                                                      |
|------------------------------------------------|------------------------------------------------------------------|
| [**интернетжеткукие**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) | Извлекает файлы cookie для указанного URL-адреса и всех его родительских URL-адресов. |
| [**интернетсеткукие**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) | Задает файл cookie по указанному URL-адресу.                              |



 

Обратите внимание, что эти функции не нуждаются в вызове [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Файлы cookie с датой окончания срока действия хранятся в учетной записи Local Users в \\ каталоге Users "Username" \\ AppData \\ роуминг \\ Microsoft \\ Windows \\ cookies и Users " \\ username" \\ AppData \\ роуминг \\ Microsoft \\ Windows \\ cookies \\ Low Directory для приложений, работающих с низкими привилегиями. Файлы cookie, не имеющие даты окончания срока действия, хранятся в памяти и доступны только процессу, в котором они были созданы.

Как указано в разделе [cookies HTTP](http-cookies.md) , функция [**интернетжеткукие**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) не возвращает файлы cookie, помеченные сервером как несценарии с атрибутом HttpOnly в заголовке Set-Cookie.

### <a name="getting-a-cookie"></a>Получение файла cookie

[**Интернетжеткукие**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) возвращает файлы cookie для указанного URL-адреса и всех его родительских URL-адресов.

В следующем примере демонстрируется вызов [**интернетжеткукие**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea).


```C++
TCHAR szURL[256];         // buffer to hold the URL
LPTSTR lpszData = NULL;   // buffer to hold the cookie data
DWORD dwSize=0;           // variable to get the buffer size needed

// Insert code to retrieve the URL.

retry:

// The first call to InternetGetCookie will get the required
// buffer size needed to download the cookie data.
if (!InternetGetCookie(szURL, NULL, lpszData, &dwSize))
{
    // Check for an insufficient buffer error.
    if (GetLastError()== ERROR_INSUFFICIENT_BUFFER)
    {
        // Allocate the necessary buffer.
        lpszData = new TCHAR[dwSize];

        // Try the call again.
        goto retry;
    }
    else
    {
        // Insert error handling code.
    }
}
else
{
    // Insert code to display the cookie data.

    // Release the memory allocated for the buffer.
    delete[]lpszData;
}
```



### <a name="setting-a-cookie"></a>Настройка файла cookie

[**Интернетсеткукие**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) используется для задания файла cookie по указанному URL-адресу. [**Интернетсеткукие**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) может создавать как постоянные, так и сеансовые файлы cookie.

Постоянные файлы cookie имеют дату окончания срока действия. Эти файлы cookie хранятся в учетной записи Local Users в папке Users " \\ username" \\ AppData \\ роуминг \\ Microsoft \\ Windows \\ cookies, а пользователь \\ "Username" \\ AppData \\ роуминг \\ Microsoft \\ Windows \\ cookies \\ Low каталог для приложений, работающих с низкими привилегиями.

Файлы cookie сеанса хранятся в памяти и доступны только создавшему их процессу.

Данные для файла cookie должны быть в формате:

``` syntax
NAME=VALUE
```

Для даты окончания срока действия формат должен быть следующим:

``` syntax
DAY, DD-MMM-YYYY HH:MM:SS GMT
```

ДЕНЬ — это 3-буквенная аббревиатура дня недели, дд — это день месяца, MMM — это трехзначный аббревиатура месяца, гггг — год, а чч: мм: СС — время суток в воинское время.

В следующем примере показаны два вызова [**интернетсеткукие**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea). Первый вызов создает файл cookie сеанса, а второй создает постоянный файл cookie.


```C++
BOOL bReturn;

// Create a session cookie.
bReturn = InternetSetCookie(TEXT("https://www.adventure_works.com"), NULL,
            TEXT("TestData = Test"));

// Create a persistent cookie.
bReturn = InternetSetCookie(TEXT("https://www.adventure_works.com"), NULL,
           TEXT("TestData = Test; expires = Sat,01-Jan-2000 00:00:00 GMT"));

```



> [!Note]  
> WinINet не поддерживает реализации серверов. Кроме того, его не следует использовать из службы. Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 