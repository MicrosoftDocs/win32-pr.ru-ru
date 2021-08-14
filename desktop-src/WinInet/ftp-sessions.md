---
title: Сеансы FTP
description: WinINet позволяет приложениям перемещаться по каталогам и файлам на FTP-сервере и управлять ими. Так как прокси-серверы CERN не поддерживают FTP, приложения, использующие прокси CERN, должны использовать функцию Интернетопенурл.
ms.assetid: 23763672-765f-4bbc-95c9-c28775e91f3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70942fea5865fa96c9ee81ab996238e3f382471a701ac44969d1ff8797c8780d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113984"
---
# <a name="ftp-sessions"></a>Сеансы FTP

WinINet позволяет приложениям перемещаться по каталогам и файлам на FTP-сервере и управлять ими. Так как прокси-серверы CERN не поддерживают FTP, приложения, использующие прокси CERN, должны использовать функцию [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) . Дополнительные сведения об использовании [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)см. в разделе [доступ к URL-адресам напрямую](handling-uniform-resource-locators.md).

Чтобы начать сеанс FTP, используйте [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) для создания обработчика сеанса.

WinINet позволяет выполнять следующие действия на FTP-сервере.

-   Переход между каталогами.
-   Перечисление, создание, удаление и переименование каталогов.
-   Переименование, передача, скачивание и удаление файлов.

Навигация обеспечивается функциями [**фтпжеткуррентдиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) и [**фтпсеткуррентдиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) . Эти функции используют обработчик сеанса, созданный предыдущим вызовом [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , для определения каталога, в котором в настоящее время находится приложение, или для изменения в другой подкаталог.

Перечисление каталогов выполняется с помощью функций [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) и [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) . [**Фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) использует созданный с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) обработчик сеанса, чтобы найти первый файл, соответствующий заданным условиям поиска, и возвращает маркер, чтобы продолжить перечисление каталогов. [**Интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) использует маркер, возвращенный [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) для возврата следующего файла, соответствующего исходным условиям поиска. Приложение должно продолжать вызывать [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) , пока в каталоге не останется больше файлов.

Используйте функцию [**фтпкреатедиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) для создания новых каталогов. Эта функция использует обработчик сеанса, созданный [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , и создает каталог, указанный в строке, передаваемой функции. Строка может содержать имя каталога относительно текущего каталога или полный путь к каталогу.

Чтобы переименовать файлы или каталоги, приложение может вызвать [**фтпренамефиле**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea). Эта функция заменяет исходное имя новым именем, переданным в функцию. Имя файла или каталога может относиться к текущему каталогу или полному имени.

Для отправки или размещения файлов на FTP-сервере приложение может использовать либо [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) , либо [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (вместе с [**интернетвритефиле**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)). [**Фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) можно использовать, если файл уже существует локально, тогда как [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) и [**интернетвритефиле**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) можно использовать, если данные необходимо записать в файл на FTP-сервере.

Чтобы скачать или получить файлы, приложение может использовать либо [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) , либо [**Фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (с [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)). [**Фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) используется для получения файла с FTP-сервера и локального сохранения, в то время как [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) и [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) можно использовать для управления расположением загруженных данных (например, приложение может отображать информацию в поле ввода).

Удалите файлы на FTP-сервере с помощью функции [**фтпделетефиле**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) . Эта функция удаляет имя файла, которое относится либо к текущему каталогу, либо к полному имени файла с FTP-сервера. [**Фтпделетефиле**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) требует, чтобы в [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)был возвращен обработчик сеанса.

## <a name="ftp-function-handles"></a>Дескрипторы функций FTP

Для правильной работы функции FTP требуются определенные типы дескрипторов [**хинтернет**](appendix-a-hinternet-handles.md) . Эти дескрипторы должны создаваться в определенном порядке, начиная с корневого дескриптора, созданного [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Затем [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) может создать обработчик сеанса FTP.

На следующей диаграмме показаны функции, зависящие от обработчика сеанса FTP, возвращаемого функцией [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Затененные поля представляют функции, которые возвращают дескрипторы [**хинтернет**](appendix-a-hinternet-handles.md) , а обычные поля представляют функции, ИСПОЛЬЗУЮЩИЕ дескриптор хинтернет, созданный функцией, от которой они зависят.

![функции FTP, зависящие от обработчика сеанса FTP, возвращенного интернетконнект](images/ax-wnt06.png)

На следующей диаграмме показаны две функции, которые возвращают дескрипторы [хинтернет](appendix-a-hinternet-handles.md) и зависящие от них функции. Затененные поля представляют функции, которые возвращают дескрипторы **хинтернет** , а обычные поля представляют функции, использующие дескриптор **хинтернет** , созданный функцией, от которой они зависят.

![функции FTP, возвращающие дескрипторы хинтернет](images/ax-wnt03.png)

Дополнительные сведения см. в разделе [Хинтернет Handles](appendix-a-hinternet-handles.md).

## <a name="using-the-wininet-functions-for-ftp-sessions"></a>Использование функций WinINet для сеансов FTP

Во время сеансов FTP используются следующие функции. Эти функции не распознаются прокси-серверами CERN. Приложения, которые должны работать через прокси-серверы CERN, должны использовать [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) и обращаться к ресурсам напрямую. Дополнительные сведения о прямом доступе к ресурсам см. в разделе [доступ к URL-адресам напрямую](handling-uniform-resource-locators.md).



| Функция                                                 | Описание                                                                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**фтпкреатедиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)         | Создает новый каталог на сервере. Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                  |
| [**фтпделетефиле**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)                   | Удаляет файл с сервера. Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                         |
| [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)             | Запускает перечисление файлов или поиск файлов в текущем каталоге. Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).        |
| [**фтпжеткуррентдиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) | Возвращает текущий каталог клиента на сервере. Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                   |
| [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)                         | Извлекает файл с сервера. Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                       |
| [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)                       | Инициирует доступ к файлу на сервере для чтения или записи. Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). |
| [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)                         | Записывает файл на сервер. Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                            |
| [**фтпремоведиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)         | Удаляет каталог на сервере. Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                      |
| [**фтпренамефиле**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)                   | Переименовывает файл на сервере. Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                           |
| [**фтпсеткуррентдиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) | Изменяет текущий каталог клиента на сервере. Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                   |
| [**интернетвритефиле**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)           | Записывает данные в открытый файл на сервере. Эта функция требует создания маркера, созданного с помощью [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).                                      |



 

### <a name="starting-an-ftp-session"></a>Запуск сеанса FTP

Приложение устанавливает сеанс FTP, вызывая [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) для маркера, созданного с помощью [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena). [**Интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) требуется имя сервера, номер порта, имя пользователя, пароль и тип службы (который должен быть установлен на \_ FTP-службу Internet \_ ). Для пассивной семантики FTP приложение также должно установить флаг [ \_ \_ пассивного](api-flags.md) подключения к Интернету.

\_ \_ \_ \_ \_ \_ Для номера порта можно использовать FTP-порт Интернета по умолчанию и значения недопустимых номеров портов в Интернете. \_ \_ FTP-порт по умолчанию в Интернете \_ использует порт FTP по умолчанию, но тип службы по-прежнему должен быть установлен. \_Недопустимый \_ \_ номер порта в Интернете использует значение по умолчанию для указанного типа службы.

Значения имени пользователя и пароля могут быть **равны NULL**. Если оба значения имеют значение **null**, [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) использует "Anonymous" для имени пользователя и адрес электронной почты пользователя для пароля. Если для пароля задано **значение NULL**, имя пользователя, передаваемое в [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , используется для имени пользователя, а для пароля используется пустая строка. Если ни одно из этих значений не равно **null**, используются имя пользователя и пароль, присвоенные [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) .

### <a name="enumerating-directories"></a>Перечисление каталогов

Перечисление каталога на FTP-сервере требует создания обработчика с помощью [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea). Этот обработчик является ветвью обработчика сеанса, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). [**Фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) находит первый файл или каталог на сервере и возвращает его в структуре [**\_ \_ данных Win32 Find**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) . Используйте [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) , пока не вернется [**сообщение об ошибке больше \_ нет \_ \_ файлов**](wininet-errors.md). Этот метод находит все последующие файлы и каталоги на сервере. Дополнительные сведения о [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)см. [в разделе Поиск следующего файла](common-functions.md).

Чтобы определить, является ли файл, полученный с помощью [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) или [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) , каталогом, проверьте, равен ли он каталогу атрибутов файла в **Двфилеаттрибутес** члене структуры [**\_ \_ данных Win32 Find**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) \_ \_ .

Если приложение вносит изменения на FTP-сервере или при частом изменении FTP-сервера, [флаг Internet \_ Flag \_ без \_ \_ записи в кэш](api-flags.md) и флаги [ \_ \_ перезагрузки в Интернете](api-flags.md) должны быть установлены в [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea). Эти флаги гарантируют, что данные каталога, извлекаемые с FTP-сервера, являются актуальными.

После того как приложение завершит перечисление каталогов, приложение должно выполнить вызов [**интернетклосехандле**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) для маркера, созданного [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea). До закрытия этого обработчика приложение не сможет снова вызвать [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) в обработчике сеанса, созданном с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Если вызов [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) выполняется для одного и того же обработчика сеанса до закрытия предыдущего вызова той же функции, происходит сбой функции, возвращающей [ошибку \_ FTP- \_ передачи \_ \_](wininet-errors.md).

В следующем примере выполняется перечисление содержимого FTP-каталога в элемент управления "список". Параметр *хконнектион* — это маркер, возвращаемый функцией [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) после того, как он устанавливает сеанс FTP. Пример исходного кода для функции Интернетеррораут, упоминаемой в этом примере, можно найти в разделе [Обработка ошибок](appendix-c-handling-errors.md).


```C++
#include <windows.h>
#include <strsafe.h>
#include <wininet.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  FTP_FUNCTIONS_BUFFER_SIZE          MAX_PATH+8

BOOL WINAPI DisplayFtpDir(
                           HWND hDlg,
                           HINTERNET hConnection,
                           DWORD dwFindFlags,
                           int nListBoxId )
{
  WIN32_FIND_DATA dirInfo;
  HINTERNET       hFind;
  DWORD           dwError;
  BOOL            retVal = FALSE;
  TCHAR           szMsgBuffer[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR           szFName[FTP_FUNCTIONS_BUFFER_SIZE];
  
  SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
  hFind = FtpFindFirstFile( hConnection, TEXT( "*.*" ), 
                            &dirInfo, dwFindFlags, 0 );
  if ( hFind == NULL )
  {
    dwError = GetLastError( );
    if( dwError == ERROR_NO_MORE_FILES )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "No files found at FTP location specified." ) );
      retVal = TRUE;
      goto DisplayDirError_1;
    }
    StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
      TEXT( "FtpFindFirstFile failed." ) );
    goto DisplayDirError_1;
  }

  do
  {
    if( FAILED( StringCchCopy( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
                  dirInfo.cFileName ) ) ||
        ( ( dirInfo.dwFileAttributes & FILE_ATTRIBUTE_DIRECTORY ) &&
        ( FAILED( StringCchCat( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
         TEXT( " <DIR> " ) ) ) ) ) )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "Failed to copy a file or directory name." ) );
      retVal = FALSE;
      goto DisplayDirError_2;
    }
    SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 
                        0, (LPARAM) szFName );
  } while( InternetFindNextFile( hFind, (LPVOID) &dirInfo ) );

  if( ( dwError = GetLastError( ) ) == ERROR_NO_MORE_FILES )
  {
    InternetCloseHandle(hFind);
    return( TRUE );
  }
  StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
    TEXT( "FtpFindNextFile failed." ) );

DisplayDirError_2:
  InternetCloseHandle( hFind );
DisplayDirError_1:
  MessageBox( hDlg,
    (LPCTSTR) szMsgBuffer,
    TEXT( "DisplayFtpDir( ) Problem" ),
    MB_OK | MB_ICONERROR );
  return( retVal );
}
```



### <a name="navigating-directories"></a>Перемещение по каталогам

Функции [**фтпжеткуррентдиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) и [**фтпсеткуррентдиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) обработают навигацию по каталогам.

[**Фтпжеткуррентдиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) возвращает текущий каталог приложения на FTP-сервере. Путь к каталогу из корневого каталога на FTP-сервере включен.

[**Фтпсеткуррентдиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) изменяет рабочий каталог на сервере. Сведения о каталоге, передаваемые в [**фтпсеткуррентдиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) , могут быть либо частично, либо полным именем пути относительно текущего каталога. Например, если приложение находится в каталоге "общедоступная/информационная", а путь — "FTP/example", [**фтпсеткуррентдиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) изменяет текущий каталог на "общедоступный/информационный/FTP/example".

В следующем примере используется обработчик сеанса FTP Хконнектион, возвращаемый [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Новое имя каталога берется из поля редактирования родительского диалогового окна, IDC которого передается в параметр *ндирнамеид* . Перед изменением каталога функция получает текущий каталог и сохраняет ее в том же поле ввода. Код источник для функции Дисплайфтпдир, вызываемой в конце, приведен выше.


```C++
BOOL WINAPI ChangeFtpDir( HWND hDlg, 
                          HINTERNET hConnection,
                          int nDirNameId, 
                          int nListBoxId )
{
  DWORD dwSize;
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szOldDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR* szFailedFunctionName;

  dwSize = FTP_FUNCTIONS_BUFFER_SIZE;

  if( !GetDlgItemText( hDlg, nDirNameId, szNewDirName, dwSize ) )
  {
    szFailedFunctionName = TEXT( "GetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if ( !FtpGetCurrentDirectory( hConnection, szOldDirName, &dwSize ))
  {
    szFailedFunctionName = TEXT( "FtpGetCurrentDirectory" );
    goto ChangeFtpDirError;
  }

  if( !SetDlgItemText( hDlg, nDirNameId, szOldDirName ) )
  {
    szFailedFunctionName = TEXT( "SetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if( !FtpSetCurrentDirectory( hConnection, szNewDirName ) )
  {
    szFailedFunctionName = TEXT( "FtpSetCurrentDirectory" );
    goto ChangeFtpDirError;
  }
  return( DisplayFtpDir( hDlg, hConnection, 0, nListBoxId ) );

ChangeFtpDirError:
  InternetErrorOut( hDlg, GetLastError( ), szFailedFunctionName );
  DisplayFtpDir( hDlg, hConnection, INTERNET_FLAG_RELOAD, nListBoxId);
  return( FALSE );
}
```



### <a name="manipulating-directories-on-an-ftp-server"></a>Управление каталогами на FTP-сервере

WinINet предоставляет возможность создавать и удалять каталоги на FTP-сервере, к которому приложение имеет необходимые привилегии. Если приложение должно входить на сервер с указанными именем пользователя и паролем, эти значения можно использовать в [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) при создании обработчика сеанса FTP.

Функция [**фтпкреатедиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) принимает допустимый код FTP-сеанса и строку, завершающуюся **нулем**, которая содержит либо полный путь, либо имя относительно текущего каталога, и создает каталог на FTP-сервере.

В следующем примере показаны два отдельных вызова [**фтпкреатедиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya). В обоих примерах Хфтпсессион — это обработчик сеанса, созданный функцией [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , а корневой каталог — текущий каталог.

``` syntax
/* Creates the directory "test" in the current (root) directory. */
FtpCreateDirectory( hFtpSession, "test" );

/* Creates the directory "example" in the test directory. */
FtpCreateDirectory( hFtpSession, "\\test\\example" );
```

Функция [**фтпремоведиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) принимает обработчик сеанса и строку, завершающуюся **нулем**, которая содержит либо полный путь, либо имя относительно текущего каталога, а также удаляет этот каталог с FTP-сервера.

В следующем примере показаны два примера вызовов [**фтпремоведиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya). В обоих вызовах Хфтпсессион — это обработчик сеанса, созданный функцией [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , а корневой каталог — текущий каталог. В корневом каталоге есть каталог с именем Test и каталог «example» в каталоге Test.

``` syntax
/* Removes the "example" directory (plus any files/directories it contains) from the "test" directory. */
FtpRemoveDirectory(hFtpSession,"\\test\\example");

/* Removes the "test" directory (plus any files/directories it contains) from the root directory. */
FtpRemoveDirectory(hFtpSession, "test");
```


```C++
FtpRemoveDirectory(hFtpSession,TEXT("\\test\\example"));
/* Removes the "example" directory and any files or 
directories contained in it from the "test" directory. */

FtpRemoveDirectory(hFtpSession, TEXT("test"));
/* Removes the "test" directory and any files or 
directories contained in it from the root directory. */
```



В следующем примере создается новый каталог на FTP-сервере. Новое имя каталога берется из поля редактирования родительского диалогового окна, IDC которого передается в параметр *ндирнамеид* . Обработчик *хконнектион* был создан [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) после установки сеанса FTP. Исходный код для функции Дисплайфтпдир, вызываемой в конце, приведен выше.


```C++
BOOL WINAPI CreateFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, 
                       szNewDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Create FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpCreateDirectory( hConnection, szNewDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpCreateDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, 
                         nListBoxId ) );
}
```



В следующем примере удаляется каталог с FTP-сервера. Имя удаляемого каталога берется из поля ввода в родительском диалоговом окне, для которого IDC передается в параметр *ндирнамеид* . Обработчик *хконнектион* был создан [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) после установки сеанса FTP. Исходный код для функции Дисплайфтпдир, вызываемой в конце, приведен выше.


```C++
BOOL WINAPI RemoveFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szDelDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, szDelDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Remove FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRemoveDirectory( hConnection, szDelDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpRemoveDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, nListBoxId ) );
}
```



### <a name="getting-files-on-an-ftp-server"></a>Получение файлов на FTP-сервере

Существует три метода извлечения файлов с FTP-сервера.

-   Используйте [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) и [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).
-   Используйте [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) и [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).
-   Используйте [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea).

Дополнительные сведения об использовании функции [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) см. в разделе [чтение файлов](common-functions.md).

Если URL-адрес файла доступен, приложение может вызвать [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) для подключения к этому URL-адресу, а затем использовать [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) для управления загрузкой файла. Это позволяет более строго контролировать загрузку и идеально подходит для ситуаций, когда на FTP-сервере не нужно вносить никаких других операций. Дополнительные сведения о непосредственном доступе к ресурсам см. в разделе [доступ к URL-адресам напрямую](handling-uniform-resource-locators.md).

Если приложение установило для сервера обработчик FTP-сеанса с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), приложение может вызвать [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) с существующим именем файла и с новым именем для локального хранимого файла. Затем приложение может использовать [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) для загрузки файла. Это позволяет более строго контролировать загрузку и поддерживать подключение к FTP-серверу, что позволяет выполнять дополнительные команды.

Если приложению не требуется тщательный контроль над загрузкой, приложение может использовать [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) с обработчиком сеанса FTP, именем удаленного файла и именем локального файла для получения файла. [**Фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) выполняет все операции по регистрации и издержки, связанные с чтением файла с FTP-сервера и сохранением его на локальном компьютере.

Следующий пример извлекает файл с FTP-сервера и сохраняет его локально. Имя файла на FTP-сервере берется из поля ввода в родительском диалоговом окне, в которое передается параметр *нфтпфиленамеид* , а локальное имя, под которым сохраняется файл, берется из поля ввода, которое передается в параметр *нлокалфиленамеид* . Обработчик *хконнектион* был создан [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) после установки сеанса FTP.


```C++
BOOL WINAPI GetFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Download FTP File" );
  TCHAR szAsciiQuery[] =
    TEXT("Do you want to download as ASCII text?(Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Target File or Destination File Missing" ),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType = ( MessageBox( hDlg, 
                                 szAsciiQuery, 
                                 szBoxTitle, 
                                 MB_YESNO ) == IDYES ) ?
                   FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;
  dwTransferType |= INTERNET_FLAG_RELOAD;

  if( !FtpGetFile( hConnection, szFtpFileName, szLocalFileName, FALSE,
                   FILE_ATTRIBUTE_NORMAL, dwTransferType, 0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,( dwTransferType == 
                      (FTP_TRANSFER_TYPE_ASCII | INTERNET_FLAG_RELOAD)) ?
                      szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );
}
```



### <a name="placing-files-on-an-ftp-server"></a>Размещение файлов на FTP-сервере

Существует два способа размещения файла на FTP-сервере.

-   Используйте [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) с [**интернетвритефиле**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile).
-   Используйте [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).

Приложение, которое должно отправить данные на FTP-сервер, но не имеет локального файла, содержащего все данные, должно использовать [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) для создания и открытия файла на FTP-сервере. Затем приложение может использовать [**интернетвритефиле**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) для передачи сведений в файл.

Если файл уже существует локально, приложение может использовать [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) для передачи файла на FTP-сервер. [**Фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) выполняет все издержки, которые передаются при передаче локального файла на удаленный FTP-сервер.

В следующем примере локальный файл копируется на FTP-сервер. Локальное имя файла берется из поля ввода в родительском диалоговом окне, IDC которого передается в параметре *нлокалфиленамеид* , а имя, под которым файл сохраняется на FTP-сервере, берется из поля ввода, которое передается в параметр *нфтпфиленамеид* . Обработчик *хконнектион* был создан [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) после установки сеанса FTP.


```C++
BOOL WINAPI PutFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Upload FTP File" );
  TCHAR szASCIIQuery[] =
    TEXT("Do you want to upload as ASCII text? (Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT("Target File or Destination File Missing"),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType =
    ( MessageBox( hDlg, 
                  szASCIIQuery, 
                  szBoxTitle, 
                  MB_YESNO ) == IDYES ) ?
    FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;

  if( !FtpPutFile( hConnection, 
                   szLocalFileName, 
                   szFtpFileName, 
                   dwTransferType, 
                   0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,
              ( dwTransferType == FTP_TRANSFER_TYPE_ASCII ) ?
                szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="deleting-files-from-an-ftp-server"></a>Удаление файлов с FTP-сервера

Чтобы удалить файл с FTP-сервера, используйте функцию [**фтпделетефиле**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) . Вызывающее приложение должно иметь необходимые привилегии для удаления файла с FTP-сервера.

В следующем примере файл удаляется с FTP-сервера. Имя удаляемого файла берется из поля ввода в родительском диалоговом окне, для которого IDC передается параметр *нфтпфиленамеид* int. Обработчик *хконнектион* был создан [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) после установки сеанса FTP. Так как эта функция не обновляет списки файлов или отображение каталогов, вызывающий процесс должен сделать это после успешного удаления.


```C++
BOOL WINAPI DeleteFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nFtpFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Delete FTP File" );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, TEXT( "File Name Must Be Specified!" ),
                szBoxTitle, MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpDeleteFile( hConnection, szFtpFileName ) )
  {
    InternetErrorOut( hDlg, 
                      GetLastError( ), 
                      TEXT( "FtpDeleteFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg, 
              TEXT( "File has been deleted" ), 
              szBoxTitle, 
              MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="renaming-files-and-directories-on-an-ftp-server"></a>Переименование файлов и каталогов на FTP-сервере

Файлы и каталоги на FTP-сервере можно переименовывать с помощью функции [**фтпренамефиле**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) . [**Фтпренамефиле**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) **принимает две строки**, заканчивающиеся нулем, которые содержат либо частичное, либо полное имя относительно текущего каталога. Функция изменяет имя файла, обозначенного первой строкой, на имя, определяемое второй строкой.

В следующем примере переименовывается файл или каталог на FTP-сервере. Текущее имя файла или каталога берется из поля ввода в родительском диалоговом окне, для которого в качестве параметра *нолдфиленамеид* передается значение IDC, а новое имя берется из поля ввода, которое передается в параметр *нневфиленамеид* . Обработчик *хконнектион* был создан [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) после установки сеанса FTP. Так как эта функция не обновляет списки файлов или отображение каталогов, вызывающий процесс должен сделать это после успешного переименования.


```C++
BOOL WINAPI RenameFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nOldFileNameId, int nNewFileNameId )
{
  TCHAR szOldFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szNewFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Rename FTP File" );

  if( !GetDlgItemText( hDlg, nOldFileNameId, szOldFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nNewFileNameId, szNewFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg,
        TEXT( "Both the current and new file names must be supplied" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRenameFile( hConnection, szOldFileName, szNewFileName ) )
  {
    MessageBox( hDlg,
        TEXT( "FtpRenameFile failed" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }
  return( TRUE );  // Remember to refresh directory listing
}
```



> [!Note]  
> WinINet не поддерживает реализации серверов. Кроме того, его не следует использовать из службы. для серверных реализаций или служб используйте [Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 