---
description: URL-адрес — это компактное представление расположения и метода доступа для ресурса, расположенного в Интернете.
ms.assetid: 940c414d-274f-475c-a50e-7a0853c3c26b
title: Универсальные указатели ресурсов (URL-адреса) в WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486ed3b17e2cf205f6ac815e87617a84e0ccc4cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080592"
---
# <a name="uniform-resource-locators-urls-in-winhttp"></a>Универсальные указатели ресурсов (URL-адреса) в WinHTTP

URL-адрес — это компактное представление расположения и метода доступа для ресурса, расположенного в Интернете. Каждый URL-адрес состоит из схемы (HTTP, HTTPS, FTP или gopher) и строки, зависящей от схемы. Эта строка может также содержать сочетание пути к каталогу, строки поиска или имени ресурса. Функции служб Microsoft Windows HTTP (WinHTTP) обеспечивают возможность создания, объединения, разбиения на себя и канонизировать URL-адресов. Дополнительные сведения см. в статьях [rfc 1738](https://www.ietf.org/rfc/rfc1738.txt), [универсальные указатели ресурсов](https://www.ietf.org/rfc/rfc1738.txt) и [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [универсальные идентификаторы ресурсов (URI): универсальный синтаксис](https://www.ietf.org/rfc/rfc1738.txt).

## <a name="what-is-a-canonicalized-url"></a>Что такое канонический URL-адрес?

Заданный синтаксис и семантика URL-адресов оставляет место для вариации и ошибок. Каноническая обработка — это процесс нормализации фактического URL-адреса в правильную, стандартную, каноническую форму.

Это включает в себя кодирование некоторых символов в виде escape-последовательности. Буквенно-цифровые символы США и ASCII не должны кодироваться (цифры 0-9, прописные буквы A – Z и строчные буквы a – z). Большинство других символов должны быть экранированными, включая управляющие символы, символ пробела, знак процента, "ненадежные символы" (<, >, ", \# , {,},, \| \\ , ^, ~,, \[ \] и") и все символы с кодовой точкой выше 127.

## <a name="using-the-winhttp-functions-to-handle-urls"></a>Использование функций WinHTTP для управления URL-адресами

WinHTTP предоставляет две функции для обработки URL-адресов. [**Винхттпкраккурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) разделяет URL-адрес на части его компонентов, а [**винхттпкреатеурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) создает URL-адрес из компонентов.

### <a name="separating-urls"></a>Отделение URL-адресов

Функция [**винхттпкраккурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) разделяет URL-адрес на части его компонентов и возвращает компоненты, указанные в структуре [**\_ компонентов URL-адреса**](/windows/win32/api/winhttp/ns-winhttp-url_components) , которая передается в функцию.

Компоненты, составляющие структуру [**\_ компонентов URL-адреса**](/windows/win32/api/winhttp/ns-winhttp-url_components) , — это номер схемы, имя узла, номер порта, имя пользователя, пароль, путь URL-адреса и дополнительные сведения, например параметры поиска. Каждый компонент, за исключением схемы и номера портов, имеет строковый элемент, содержащий сведения и элемент, содержащий длину строкового элемента. В схеме и номерах портов имеется только элемент, в котором хранится соответствующее значение. как схема, так и номер порта возвращаются для всех успешных вызовов [**винхттпкраккурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl).

Чтобы получить значение определенного компонента в структуре [**\_ компонентов URL-адреса**](/windows/win32/api/winhttp/ns-winhttp-url_components) , элементу, в котором хранится длина строки этого компонента, должно быть присвоено ненулевое значение. Строковый элемент может быть либо указателем на буфер, либо **значением NULL**.

Если элемент указателя содержит указатель на буфер, элемент длины строки должен содержать размер этого буфера. Функция [**винхттпкраккурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) возвращает сведения о компоненте в виде строки в буфере и сохраняет длину строки в члене длины строки.

Если для элемента указателя задано **значение NULL**, то элементу длины строки может быть присвоено любое ненулевое значение. Функция [**винхттпкраккурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) сохраняет указатель на первый символ строки URL-адреса, который содержит сведения о компоненте, и задает длину строки, равную количеству символов в оставшейся части строки URL-адреса, относящейся к компоненту.

Все члены-указатели имеют **значение NULL** с ненулевой точкой члена, соответствующей отправной точке в строке URL. Длину, хранящуюся в члене length, необходимо использовать для определения конца данных отдельного компонента.

Чтобы правильно инициализировать структуру [**\_ компонентов URL-адресов**](/windows/win32/api/winhttp/ns-winhttp-url_components) , элементу **двструктсизе** должен быть присвоен размер структуры [**\_ компонентов URL-адреса**](/windows/win32/api/winhttp/ns-winhttp-url_components) .

### <a name="creating-urls"></a>Создание URL-адресов

Функция [**винхттпкреатеурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) использует сведения в описанной выше структуре [**\_ компонентов URL-адреса**](/windows/win32/api/winhttp/ns-winhttp-url_components) для создания URL-адреса.

Для каждого обязательного компонента член-указатель должен содержать указатель на буфер, содержащий данные. Элемент length должен иметь нулевое значение, если элемент указателя содержит указатель на строку, завершающуюся нулем; элемент length должен быть установлен в значение длины строки, если элемент указателя содержит указатель на строку, которая не завершается нулем. Элемент указателя всех компонентов, которые не являются обязательными, должен иметь значение **null**.

### <a name="sample-code"></a>Пример кода

В следующем примере кода показано, как использовать [**винхттпкраккурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) и [**винхттпкреатеурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) для РАЗГРУППИРОВАНИЯ существующего URL-адреса, изменения одного из его компонентов и его сборки в новый URL-адрес.


```C++
  URL_COMPONENTS urlComp;
  LPCWSTR pwszUrl1 = 
    L"https://search.msn.com/results.asp?RS=CHECKED&FORM=MSNH&v=1&q=wininet";
  DWORD dwUrlLen = 0;

  // Initialize the URL_COMPONENTS structure.
  ZeroMemory(&urlComp, sizeof(urlComp));
  urlComp.dwStructSize = sizeof(urlComp);

  // Set required component lengths to non-zero so that they are cracked.
  urlComp.dwSchemeLength    = (DWORD)-1;
  urlComp.dwHostNameLength  = (DWORD)-1;
  urlComp.dwUrlPathLength   = (DWORD)-1;
  urlComp.dwExtraInfoLength = (DWORD)-1;

  // Crack the URL.
  if( !WinHttpCrackUrl( pwszUrl1, (DWORD)wcslen(pwszUrl1), 0, &urlComp ) )
      printf( "Error %u in WinHttpCrackUrl.\n", GetLastError( ) );
  else
  {
    // Change the search information.  New info is the same length.
    urlComp.lpszExtraInfo = L"?RS=CHECKED&FORM=MSNH&v=1&q=winhttp";

    // Obtain the size of the new URL and allocate memory.
    WinHttpCreateUrl( &urlComp, 0, NULL, &dwUrlLen );
    LPWSTR pwszUrl2 = new WCHAR[dwUrlLen];

    // Create a new URL.
    if( !WinHttpCreateUrl( &urlComp, 0, pwszUrl2, &dwUrlLen ) )
      printf( "Error %u in WinHttpCreateUrl.\n", GetLastError( ) );
    else
    {
      // Show both URLs.
      printf( "Old URL:  %S\nNew URL:  %S\n", pwszUrl1, pwszUrl2 );
    }

    // Free allocated memory.
    delete [] pwszUrl2;
  }
```



 

 



