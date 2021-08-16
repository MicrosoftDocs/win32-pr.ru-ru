---
title: Обработка указателей универсальных ресурсов
description: Универсальный указатель ресурсов (URL) — это компактное представление расположения и метода доступа для ресурса, расположенного в Интернете.
ms.assetid: bb59ada6-f49f-412c-a32c-4fb9495b1222
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 419433c8a06b6243bf048896664a67da31a3c58d1d79eb6fea65f9fc99dbe63a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121874"
---
# <a name="handling-uniform-resource-locators"></a>Обработка указателей универсальных ресурсов

Универсальный указатель ресурсов (URL) — это компактное представление расположения и метода доступа для ресурса, расположенного в Интернете. Каждый URL-адрес состоит из схемы (HTTP, HTTPS или FTP) и строки, зависящей от схемы. Эта строка может также содержать сочетание пути к каталогу, строки поиска или имени ресурса. Функции WinINet предоставляют возможность создавать, объединять, разбивать и канонизировать URL-адреса. Дополнительные сведения об URL-адресах см. в [документе RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) по универсальным указателям ресурсов (URL).

Функции URL-адреса работают в режиме, ориентированном на задачи. Содержимое и формат URL-адреса, переданного функции, не проверяются. Вызывающее приложение должно следить за использованием этих функций, чтобы убедиться, что данные имеют требуемый формат. Например, функция [**интернетканоникализеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) преобразует символ "%" в escape-последовательность "%25", если не использует флаги. Если в каноническом URL-адресе используется [**интернетканоникализеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) , то управляющая последовательность "%25" будет преобразована в экранированную последовательность "%2525", которая не будет работать должным образом.

-   [Что такое канонический URL-адрес?](#what-is-a-canonicalized-url)
-   [Использование функций WinINet для управления URL-адресами](#using-the-wininet-functions-to-handle-urls)
-   [URL-адреса канонизацию](#what-is-a-canonicalized-url)
-   [Объединение базового и относительного URL-адреса](#combining-base-and-relative-urls)
-   [Взлом URL-адресов](#cracking-urls)
-   [Создание URL-адресов](#creating-urls)
-   [Прямой доступ к URL-адресам](#accessing-urls-directly)

## <a name="what-is-a-canonicalized-url"></a>Что такое канонический URL-адрес?

Формат всех URL-адресов должен соответствовать принятому синтаксису и семантике для доступа к ресурсам через Интернет. Каноническая обработка — это процесс форматирования URL-адреса для соблюдения синтаксиса и семантики.

Символы, которые должны быть закодированы, включают в себя любые символы, не имеющие соответствующих графических символов в кодировке US-ASCII (шестнадцатеричная 80-FF, которые не используются в кодировке US-ASCII, а также шестнадцатеричные 00-1F и 7F, представляющие собой управляющие символы), пробелы, "%" (используемые для кодирования других символов) и ненадежные символы (<, >, ", \# , {,}, \| , \\ , ^, ~,, \[ \] и").

## <a name="using-the-wininet-functions-to-handle-urls"></a>Использование функций WinINet для управления URL-адресами

В следующей таблице перечислены функции URL-адресов.



| Функция                                                   | Описание                                        |
|------------------------------------------------------------|----------------------------------------------------|
| [**интернетканоникализеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) | Каноникализес URL-адрес.                             |
| [**интернеткомбинеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla)           | Объединяет базовый и относительный URL-адрес.                   |
| [**интернеткраккурл**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)               | Выполняет синтаксический анализ строки URL-адреса в компоненты.               |
| [**интернеткреатеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla)             | Создает строку URL-адреса из компонентов.              |
| [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)                 | Начинает получение ресурса FTP, HTTP или HTTPS. |



 

## <a name="canonicalizing-urls"></a>URL-адреса канонизацию

Канонизацию URL-адрес — это процесс, который преобразует URL-адрес, который может содержать ненадежные символы, такие как пробелы, зарезервированные символы и т. д., в допустимый формат.

Функцию [**интернетканоникализеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) можно использовать для канонизировать URL-адресов. Эта функция ориентирована на задачи, поэтому приложение должно внимательно отслеживать его использование. [**Интернетканоникализеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) не проверяет, что переданный в него URL-адрес уже каноническ и что возвращаемый им URL-адрес является допустимым.

Следующие пять флагов управляют тем, как [**интернетканоникализеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) обрабатывает конкретный URL-адрес. Флаги можно использовать в сочетании. Если флаги не используются, функция кодирует URL-адрес по умолчанию.



| Значение                     | Значение                                                                                                                                                                                                 |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_режим браузера \_ ICU        | Не закодировать или декодировать символы после " \# " или "?" и не удалять конечные пробелы после "?". Если это значение не указано, то кодируется весь URL-адрес, а конечные пробелы удаляются. |
| декодирование ICU \_               | Преобразование всех последовательностей% XX в символы, включая escape-последовательности, перед синтаксическим анализом URL.                                                                                                          |
| ICU \_ \_ только символы \_ кодирования | Закодировать только пробелы.                                                                                                                                                                                     |
| ICU \_ без \_ кодирования           | Не преобразуйте ненадежные символы в escape-последовательности.                                                                                                                                                   |
| ICU \_ нет \_ мета             | Не удаляйте в URL-адресе метаданные (например, "." и "..").                                                                                                                                       |



 

\_Флаг декодирования ICU должен использоваться только для канонических URL-адресов, так как предполагается, что все последовательности% XX являются управляющими кодами Escape-кодов и преобразуют их в символы, указанные в коде. Если в URL-адресе есть символ "%", который не является частью Escape-кода, ICU \_ декодирование все еще обрабатывает его как один. Эта характеристика может привести к тому, что [**интернетканоникализеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) создаст недопустимый URL-адрес.

Чтобы использовать [**интернетканоникализеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) для возврата полностью декодированного URL-адреса, \_ \_ \_ необходимо указать флаги декодирования ICU и ICU. Эта программа установки предполагает, что URL-адрес, передаваемый в [**интернетканоникализеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) , был ранее канонический.

## <a name="combining-base-and-relative-urls"></a>Объединение базового и относительного URL-адреса

Относительный URL-адрес — это компактное представление расположения ресурса относительно абсолютного базового URL-адреса. Базовый URL-адрес должен быть известен анализатору и обычно включает схему, сетевое расположение и части пути URL-адреса. Приложение может вызвать [**интернеткомбинеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) , чтобы объединить относительный URL-адрес с его базовым URL-адресом. [**Интернеткомбинеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) также каноникализес результирующий URL-адрес.

## <a name="cracking-urls"></a>Взлом URL-адресов

Функция [**интернеткраккурл**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) разделяет URL-адрес на части его компонентов и возвращает компоненты, указанные в структуре [**\_ компонентов URL-адреса**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , которая передается в функцию.

Компоненты, составляющие структуру [**\_ компонентов URL-адреса**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , — это номер схемы, имя узла, номер порта, имя пользователя, пароль, путь URL-адреса и дополнительные сведения (например, параметры поиска). Каждый компонент, за исключением схемы и номеров портов, имеет строковый элемент, содержащий сведения, и элемент, содержащий длину строкового элемента. В схеме и номерах портов имеется только элемент, в котором хранится соответствующее значение. они оба возвращаются для всех успешных вызовов [**интернеткраккурл**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla).

Чтобы получить значение конкретного компонента в структуре [**\_ компонентов URL-адреса**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , элементу, в котором хранится длина строки этого компонента, должно быть присвоено ненулевое значение. Строковый элемент может быть либо адресом буфера, либо **значением NULL**.

Если элемент указателя содержит адрес буфера, то элемент длины строки должен содержать размер этого буфера. [**Интернеткраккурл**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) возвращает сведения о компоненте в виде строки в буфере и сохраняет длину строки в члене длины строки.

Если элемент указателя имеет **значение NULL**, то элементу длины строки может быть присвоено любое ненулевое значение. [**Интернеткраккурл**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) хранит адрес первого символа строки URL-адреса, содержащей сведения о компоненте, и задает длину строки, равную количеству символов в оставшейся части строки URL-адреса, относящейся к компоненту.

Все члены-указатели имеют **значение NULL** с ненулевой точкой члена, соответствующей отправной точке в строке URL. Длину, хранящуюся в члене length, необходимо использовать для определения конца данных отдельного компонента.

Чтобы правильно инициализировать структуру [**\_ компонентов URL-адресов**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , элементу **двструктсизе** должен быть присвоен размер структуры [**\_ компонентов URL-адреса**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) в байтах.

Следующий пример возвращает компоненты URL-адреса в поле ввода, IDC \_ PreOpen1 и возвращает компоненты в список, IDC \_ преопенлист. Чтобы отобразить только сведения об отдельном компоненте, эта функция копирует символ непосредственно после сведений о компоненте в строке и временно заменяет его **значением NULL**.


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>
#include <wininet.h>
#include <stdlib.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  CRACKER_BUFFER_SIZE           MAX_PATH

// For sample source code implementing the InternetErrorOut( ) 
// function referenced below, see the "Handling Errors" topic  
// under "Using WinInet"
extern BOOL WINAPI InternetErrorOut( HWND hWnd, DWORD dwError,
                                     LPCTSTR szFailingFunctionName );

// Forward declaration of listUrlPart helper functions:
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength );
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, int partValue );

// Static list describing the URL Scheme types 
// enumerated in INTERNET_SCHEME:
TCHAR* schemeType[] =
{
  TEXT( "[Partial URL]" ),                //  0
  TEXT( "[Unknown scheme]" ),             //  1
  TEXT( "[Default scheme]" ),             //  2
  TEXT( "FTP" ),                          //  3
  TEXT( "Gopher" ),                       //  4
  TEXT( "HTTP" ),                         //  5
  TEXT( "HTTPS" ),                        //  6
  TEXT( "File" ),                         //  7
  TEXT( "News" ),                         //  8
  TEXT( "MailTo" ),                       //  9
  TEXT( "Socks" ),                        // 10
  TEXT( "JavaScript" ),                   // 11
  TEXT( "VBScript" )                      // 12
};
#define  CRACKER_SCHEME_TYPE_ARRAY_SIZE      13

BOOL WINAPI Cracker( HWND hDlg, int nURLtextBoxId, int nListBoxId )
{
   int i, j;
   TCHAR* failedFunctionName;
   TCHAR URL_buffer[CRACKER_BUFFER_SIZE];

   URL_COMPONENTS URLparts;

   URLparts.dwStructSize = sizeof( URLparts );

   // The following elements determine which components are displayed
   URLparts.dwSchemeLength    = 1;
   URLparts.dwHostNameLength  = 1;
   URLparts.dwUserNameLength  = 1;
   URLparts.dwPasswordLength  = 1;
   URLparts.dwUrlPathLength   = 1;
   URLparts.dwExtraInfoLength = 1;

   URLparts.lpszScheme     = NULL;
   URLparts.lpszHostName   = NULL;
   URLparts.lpszUserName   = NULL;
   URLparts.lpszPassword   = NULL;
   URLparts.lpszUrlPath    = NULL;
   URLparts.lpszExtraInfo  = NULL;

   SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
   if( !GetDlgItemText( hDlg, nURLtextBoxId, 
                        URL_buffer, CRACKER_BUFFER_SIZE ) )
   {
       failedFunctionName = TEXT( "GetDlgItemText" );
       goto CrackerError_01;
   }

   if( FAILED( StringCchLength( URL_buffer, CRACKER_BUFFER_SIZE, 
                                (size_t*) &i ) ) )
   {
       failedFunctionName = TEXT( "StringCchLength" );
       goto CrackerError_01;
   }

   if( !InternetCrackUrl( URL_buffer, (DWORD)_tcslen( URL_buffer ), 0, 
                          &URLparts ) )
   {
       failedFunctionName = TEXT( "InternetCrackUrl" );
       goto CrackerError_01;
   }

   failedFunctionName = TEXT( "listURLpart" );

   i = URLparts.nScheme + 2;
   if( ( i >= 0 ) && ( i < CRACKER_SCHEME_TYPE_ARRAY_SIZE ) )
   {
       StringCchLength( schemeType[i], 
                        CRACKER_BUFFER_SIZE, 
                        (size_t*) &j );
       if( !listURLpart( hDlg, nListBoxId, 
                         TEXT("Scheme type"), 
                         schemeType[i], j ))
           goto CrackerError_01;
   }

   if( !listURLpart( hDlg, nListBoxId, TEXT( "Scheme text" ), 
                     URLparts.lpszScheme, 
                     URLparts.dwSchemeLength ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Host name" ), 
                     URLparts.lpszHostName, 
                     URLparts.dwHostNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Port number" ), 
                     (int) URLparts.nPort ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "User name" ), 
                     URLparts.lpszUserName, 
                     URLparts.dwUserNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Password" ), 
                     URLparts.lpszPassword, 
                     URLparts.dwPasswordLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Path" ), 
                     URLparts.lpszUrlPath, 
                     URLparts.dwUrlPathLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Extra information"), 
                     URLparts.lpszExtraInfo, 
                     URLparts.dwExtraInfoLength))
           goto CrackerError_01;

   return( TRUE );

CrackerError_01:
// For sample source code of the InternetErrorOut( ) function 
// referenced below, see the "Handling Errors" 
// topic under "Using WinInet"
   InternetErrorOut( hDlg, GetLastError( ), failedFunctionName );
   return FALSE;
}

// listURLpart( ) helper function for string parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];
  LPTSTR nextStart;
  size_t nextSize;

  if( partLength == 0 )  // Just skip empty ones
    return( TRUE );

  if( FAILED( StringCchCopyEx( outputBuffer, 
                              (size_t) CRACKER_BUFFER_SIZE,
                               szPartName, &nextStart, 
                               &nextSize, 0 ) ) ||
      FAILED( StringCchCopyEx( nextStart, nextSize, TEXT( ": " ), 
                               &nextStart, &nextSize, 0 ) ) ||
      FAILED( StringCchCopyNEx( nextStart, nextSize, part, 
                                (size_t) partLength,
                                &nextStart, &nextSize, 0 ) ) )
    return( FALSE );

  *nextStart = 0;
  if( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                          (LPARAM)outputBuffer ) < 0 )
    return( FALSE );
  return( TRUE );
}

// listURLpart( ) helper function for numeric parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, int partValue )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];

  if( FAILED( StringCchPrintf( outputBuffer, 
                               (size_t) CRACKER_BUFFER_SIZE,
                               TEXT( "%s: %d" ), szPartName, 
                               partValue ) ) ||
      ( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                            (LPARAM)outputBuffer ) < 0 ) )
    return( FALSE );
  return( TRUE );
}
```



## <a name="creating-urls"></a>Создание URL-адресов

Функция [**интернеткреатеурл**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) использует сведения в структуре [**\_ компонентов URL-адреса**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) для создания унифицированного указателя ресурса.

Компонентами, которые составляют структуру [**\_ компонентов URL-адреса**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , являются схема, имя узла, номер порта, имя пользователя, пароль, URL-адрес и дополнительные сведения (например, параметры поиска). Каждый компонент, за исключением номера порта, имеет строковый элемент, содержащий сведения, и элемент, содержащий длину строкового элемента.

Для каждого обязательного компонента член указателя должен содержать адрес буфера, содержащего данные. Элемент length должен иметь нулевое значение, если элемент указателя содержит адрес строки, завершающейся нулем; элементу length должна быть присвоена длина строки, если элемент указателя содержит адрес строки, которая не завершается нулем. Элемент указателя всех компонентов, которые не являются обязательными, должен иметь **значение NULL**.

## <a name="accessing-urls-directly"></a>Прямой доступ к URL-адресам

Доступ к ресурсам FTP и HTTP в Интернете Возможен напрямую с помощью функций [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)и [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) . [**Интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) открывает подключение к ресурсу по URL-адресу, переданному в функцию. При установке этого соединения возможны два действия. Во-первых, если ресурс является файлом, [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) может скачать его; Во-вторых, если ресурс является каталогом, [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) может перечислить файлы в каталоге (за исключением случаев использования прокси-серверов CERN). Дополнительные сведения о [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)см. в разделе [чтение файлов](common-functions.md). Дополнительные сведения о [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)см. [в разделе Поиск следующего файла](common-functions.md).

Для приложений, которые должны работать через прокси-сервер CERN, [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) можно использовать для доступа к каталогам и файлам FTP. Запросы FTP упаковываются в виде HTTP-запроса, который будет принимать прокси-сервер CERN.

[**Интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) использует обработчик [**хинтернет**](appendix-a-hinternet-handles.md) , созданный функцией [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena) , и URL-адрес ресурса. URL-адрес должен включать схему (http:, FTP:, файл: \[ для локального файла \] или HTTPS: \[ для безопасного протокола гипертекста \] ) и сетевое расположение (например, `www.microsoft.com` ). URL-адрес может также включать путь (например,/исапи/гомском.АСП? TARGET =/Виндовс/феатуре/) и имя ресурса (например, default.htm). Для запросов HTTP или HTTPS можно включать дополнительные заголовки.

[**Интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), [**Интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)и [**интернетсетфилепоинтер**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (только URL-адреса HTTP или HTTPS) могут использовать для скачивания ресурса маркер, созданный с помощью [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .

На следующей схеме показано, какие дескрипторы используются для каждой функции.

![дескрипторы для использования с функциями](images/ax-wnt02.png)

Корневой обработчик [**хинтернет**](appendix-a-hinternet-handles.md) , созданный [**Интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena) , используется [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla). Обработчик **хинтернет** , созданный [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) , может использоваться [**интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (не показано здесь) и [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (только URL-адреса HTTP или HTTPS).

Дополнительные сведения см. в разделе [**Хинтернет Handles**](appendix-a-hinternet-handles.md).

> [!Note]  
> WinINet не поддерживает реализации серверов. Кроме того, его не следует использовать из службы. для серверных реализаций или служб используйте [Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 