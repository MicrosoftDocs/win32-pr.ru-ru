---
title: общие функции (Windows интернет)
description: Различные протоколы Интернета (например, FTP и HTTP) используют несколько функций WinINet для работы с информацией в Интернете.
ms.assetid: c80768cf-c8c0-4bdf-9ea2-f82c92ade05a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7b6a68c2633175eca793f48b2180b7212905762ca0f58290436aa17ae9a728
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132897"
---
# <a name="common-functions-windows-internet"></a>общие функции (Windows интернет)

Различные протоколы Интернета (например, FTP и HTTP) используют несколько функций WinINet для работы с информацией в Интернете. Эти общие функции обрабатывают свои задачи согласованно, независимо от конкретного протокола, к которому они применяются. Приложения могут использовать эти функции для создания функций общего назначения, обрабатывающих задачи в различных протоколах (например, чтение файлов для FTP и HTTP).

Общие функции обрабатывали следующие задачи:

-   Загрузка ресурсов из Интернета ([**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**интернетсетфилепоинтер**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer), [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)и [**интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).
-   Настройка асинхронных операций ([**интернетсетстатускаллбакк**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).
-   Просмотр и изменение параметров ([**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) и [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).
-   Закрытие всех типов дескрипторов [**хинтернет**](appendix-a-hinternet-handles.md) ([**интернетклосехандле**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)).
-   Размещение и удаление блокировок ресурсов ([**интернетлоккрекуестфиле**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) и [**интернетунлоккрекуестфиле**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)).

## <a name="using-common-functions"></a>Использование общих функций

В следующей таблице перечислены общие функции, входящие в функции WinINet. Общие функции могут использоваться для различных типов дескрипторов [**хинтернет**](appendix-a-hinternet-handles.md) или использоваться во время различных типов сеансов.



| Функция                                                         | Описание                                                                                                                                                                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)             | Продолжит перечисление файлов или поиск. Требуется обработчик, созданный функцией [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)или [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .                                                                            |
| [**интернетлоккрекуестфиле**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile)       | Позволяет пользователю поместить блокировку на используемый файл. Для этой функции требуется маркер, возвращенный функцией [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)или [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) . |
| [**интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) | Получает доступный объем данных. Требуется обработчик, созданный функцией [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)или [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .                                                                                    |
| [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)               | Возвращает значение параметра Интернета.                                                                                                                                                                                                            |
| [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)                     | Считывает данные URL-адреса. Требуется обработчик, созданный функцией [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)или [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .                                                                |
| [**интернетсетфилепоинтер**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)         | Задает расположение следующего считывания в файле. Требуется обработчик, созданный [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (только для URL-адреса HTTP) или созданный с помощью [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) токен с помощью команды GET HTTP.                 |
| [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)                   | Задает параметр Интернета.                                                                                                                                                                                                                                |
| [**интернетсетстатускаллбакк**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)   | Задает функцию обратного вызова, которая получает сведения о состоянии. Присваивает функцию обратного вызова назначенному дескриптору [**хинтернет**](appendix-a-hinternet-handles.md) и всем дескрипторам, производным от него.                                                      |
| [**интернетунлоккрекуестфиле**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)   | Разблокирует файл, который был заблокирован с помощью функции [**интернетлоккрекуестфиле**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) .                                                                                                                                           |



 

Чтение файлов, поиск следующего файла, Управление параметрами и настройка асинхронных операций являются общими для функций, поддерживающих различные протоколы и типы обработки [**хинтернет**](appendix-a-hinternet-handles.md) .

### <a name="reading-files"></a>Чтение файлов

Функция [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) используется для загрузки ресурсов из [**хинтернет**](appendix-a-hinternet-handles.md) -маркера, возвращаемого функцией [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)или [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .

[**Интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) принимает переменную указателя void, содержащую адрес буфера, и указатель на переменную, содержащую длину буфера. Функция возвращает данные в буфере и объем данных, загружаемых в буфер.

Функции WinINet предоставляют два метода загрузки всего ресурса:

-   Функция [**интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) .
-   Возвращаемые значения [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).

[**Интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) принимает маркер [**Хинтернет**](appendix-a-hinternet-handles.md) , созданный [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)или [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (после вызова [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) в обработчике), и возвращает количество доступных байтов. Приложение должно выделить буфер, равный количеству доступных байтов, плюс 1 для завершающего **нуль** -символа и использовать этот буфер с [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile). Этот метод не всегда работает, так как [**интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) проверяет размер файла, указанного в заголовке, а не на сам файл. Сведения в файле заголовка могут быть устаревшими, или файл заголовка может отсутствовать, поскольку в настоящее время он не требуется для всех стандартов.

В следующем примере считывается содержимое ресурса, к которому обращается обработчик Хресаурце, и отображается в поле ввода, указанном параметром Интктрлид.


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR    lpszData;           // buffer for the data
    DWORD     dwSize;             // size of the data available
    DWORD     dwDownloaded;       // size of the downloaded data
    DWORD     dwSizeSum=0;        // size of the data in the text box
    LPTSTR    lpszHolding;        // buffer to merge the text box 
                                  // data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.  
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {    
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,(LPVOID)lpszData,
                                 dwSize,&dwDownloaded))
            {
                ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the 
                // data buffer.
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];
                    
                // Check if there has been any data written to 
                // the text box.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the text 
                    // box, if any.
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding, 
                                   dwSizeSum);
                         
                    // Add a null terminator at the end of 
                    // the text box data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string. 
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + 
                                 dwDownloaded + 1;
                LPTSTR pszDestEnd;
                size_t cchRemaining;

                // Add the new data to the holding buffer.
                HRESULT hr = StringCchCatEx(lpszHolding, cchDest, 
                                            lpszData, &pszDestEnd, 
                                            &cchRemaining, 
                                            STRSAFE_NO_TRUNCATION);
                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the text box.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to 
                    // the text box data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.  
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                    {
                        break;
                    }                    
                    else
                    {
                        //  Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    // Return.
    return TRUE;
}
```



[**Интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) возвращает нулевые байты для чтения и завершения после считывания всех доступных данных. Это позволяет приложению использовать [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) в цикле для загрузки данных и выхода, когда оно возвращает нулевые байты, прочитанные и завершенные успешно.

Следующий пример считывает ресурс из Интернета и отображает ресурс в поле ввода, указанном параметром Интктрлид. [**Интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)или [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) вернула [**хинтернет**](appendix-a-hinternet-handles.md) [**-маркер**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), хинтернет.


```C++
int WINAPI Dump(HWND hX, int intCtrlID, HINTERNET hResource)
{
     DWORD dwSize = 0;
     LPTSTR lpszData;
     LPTSTR lpszOutPut;
     LPTSTR lpszHolding = TEXT("");
     int nCounter = 1;
     int nBufferSize = 0;
     DWORD BigSize = 8000;

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Begin the loop that reads the data.
     do
     {
          // Allocate the buffer.
          lpszData =new TCHAR[BigSize+1];

          // Read the data.
          if(!InternetReadFile(hResource,
                              (LPVOID)lpszData,
                              BigSize,&dwSize))
          {
               ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
               delete []lpszData;
               break;
          }
          else
          {
               // Add a null terminator to the end of the buffer.
               lpszData[dwSize]='\0';

               // Check if all of the data has been read.  This should
               // never get called on the first time through the loop.
               if (dwSize == 0)
               {
                    // Write the final data to the text box.
                    SetDlgItemText(hX,intCtrlID,lpszHolding);

                    // Delete the existing buffers.
                    delete [] lpszData;
                    delete [] lpszHolding;
                    break;
               }

               // Determine the buffer size to hold the new data and
               // the data already written to the text box (if any).
               nBufferSize = (nCounter*BigSize)+1;

               // Increment the number of buffers read.
               nCounter++;               

               // Allocate the output buffer.
               lpszOutPut = new TCHAR[nBufferSize];

               // Make sure the buffer is not the initial buffer.
               if(nBufferSize != int(BigSize+1))
               {
                    // Copy the data in the holding buffer.
                    StringCchCopy(lpszOutPut,nBufferSize,lpszHolding);
                    // Add error handling code here.

                    // Concatenate the new buffer with the 
                    // output buffer.
                    StringCchCat(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
     
                    // Delete the holding buffer.
                    delete [] lpszHolding;
               }
               else
               {
                    // Copy the data buffer.
                    StringCchCopy(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
               }

               // Allocate a holding buffer.
               lpszHolding = new TCHAR[nBufferSize]; 

               // Copy the output buffer into the holding buffer.
               memcpy(lpszHolding,lpszOutPut,nBufferSize);

               // Delete the other buffers.
               delete [] lpszData;
               delete [] lpszOutPut;

          }

     }
     while (TRUE);

     // Close the HINTERNET handle.
     InternetCloseHandle(hResource);

     // Set the cursor back to an arrow.
     SetCursor(LoadCursor(NULL,IDC_ARROW));

     // Return.
     return TRUE;
}
```



### <a name="finding-the-next-file"></a>Поиск следующего файла

Функция [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) используется для поиска следующего файла в поиске файла с помощью параметров поиска и [**хинтернетного**](appendix-a-hinternet-handles.md) маркера из [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)или [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

Чтобы завершить поиск файла, продолжайте вызывать [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) с помощью маркера [**хинтернет**](appendix-a-hinternet-handles.md) , возвращенного [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), или [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) до тех пор, пока функция не завершится с ошибкой расширенного сообщения об ошибке, больше [ \_ нет \_ \_ файлов](wininet-errors.md). Чтобы получить расширенные сведения об ошибке, вызовите функцию [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

В следующем примере показано содержимое FTP-каталога в списке, указанном параметром Лстдиректори. Обработчик [**хинтернет**](appendix-a-hinternet-handles.md) , хконнект, возвращается функцией [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) после того, как она устанавливает сеанс FTP.


```C++
bool WINAPI DisplayDir( HWND hX, 
                        int lstDirectory, 
                        HINTERNET hConnect, 
                        DWORD dwFlag )
{
     WIN32_FIND_DATA pDirInfo;
     HINTERNET hDir;
     TCHAR DirList[MAX_PATH];

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Reset the list box.
     SendDlgItemMessage(hX, lstDirectory,LB_RESETCONTENT,0,0);

     // Find the first file.
     hDir = FtpFindFirstFile (hConnect, TEXT ("*.*"), 
                              &pDirInfo, dwFlag, 0);
     if (!hDir)                                     
     {
          // Check if the error was because there were no files.
          if (GetLastError()  == ERROR_NO_MORE_FILES) 
          {
               // Alert user.
               MessageBox(hX, TEXT("There are no files here!!!"), 
                          TEXT("Display Dir"), MB_OK);

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return TRUE;
          }
          else 
          {
               // Call error handler.
               ErrorOut (hX, GetLastError (), TEXT("FindFirst error: "));

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return FALSE;
          }
     }
     else
     {
          // Write the file name to a string.
          StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

          // Check the type of file.
          if (pDirInfo.dwFileAttributes == FILE_ATTRIBUTE_DIRECTORY)
          {
               // Add <DIR> to indicate that this is 
               // a directory to the user.
               StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
               // Add error handling code here.
          }
       
          // Add the file name (or directory) to the list box.
          SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                             0, (LPARAM)DirList);
     }
     do
     {
          // Find the next file.
          if (!InternetFindNextFile (hDir, &pDirInfo))
          {
               // Check if there are no more files left. 
               if ( GetLastError() == ERROR_NO_MORE_FILES ) 
               {
                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return TRUE;
               }
               else
               {   
                    // Handle the error.
                    ErrorOut (hX, GetLastError(), 
                              TEXT("InternetFindNextFile"));

                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return FALSE;
               }
           }
           else
           {
               // Write the file name to a string.
               StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

               // Check the type of file.
               if(pDirInfo.dwFileAttributes==FILE_ATTRIBUTE_DIRECTORY)
               {
                    // Add <DIR> to indicate that this is a 
                    // directory to the user.
                    StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
                    // Add error handling code here.
               }
     
               // Add the file name (or directory) to the list box.
               SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                                  0, (LPARAM)DirList);
           }
     }
     while ( TRUE);
     
}
```



### <a name="manipulating-options"></a>Параметры управления

[**Интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) и [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) используются для работы с параметрами WinInet.

[**Интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) принимает переменную, которая указывает параметр для установки, буфер для хранения параметра параметра и указатель, содержащий адрес переменной, содержащей длину буфера.

[**Интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) принимает переменную, которая указывает возвращаемый параметр, буфер для хранения параметра параметра и указатель, содержащий адрес переменной, содержащей длину буфера.

### <a name="setting-up-asynchronous-operations"></a>Настройка асинхронных операций

По умолчанию функции WinINet работают синхронно. Приложение может запросить асинхронную операцию, установив флаг [Internet \_ Flag \_ Async](api-flags.md) в вызове функции [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena) . Все будущие вызовы дескрипторов, производных от дескрипторов, возвращенных из [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena) , выполняются асинхронно.

Обоснование асинхронной и синхронной операций заключается в том, чтобы позволить однопотоковому приложению максимально увеличить использование ЦП без ожидания завершения сетевых операций ввода-вывода. Таким образом, в зависимости от запроса операция может завершиться синхронно или асинхронно. Приложение должно проверить код возврата. Если функция возвращает **значение false** или **null**, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает сообщение об ошибке \_ ввода-вывода \_ , запрос был выполнен асинхронно и приложение вызывается обратно с \_ запросом состояния в Интернете после завершения \_ \_ функции.

Чтобы начать асинхронную операцию, приложение должно установить флаг [" \_ \_ Async Internet Flag](api-flags.md) " в вызове [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Приложение должно зарегистрировать допустимую функцию обратного вызова с помощью [**интернетсетстатускаллбакк**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback).

После регистрации функции обратного вызова для обработчика все операции с этим обработчиком могут формировать события состояния при условии, что значение контекста, указанное при создании маркера, не равно нулю. Если задать нулевое значение контекста, операция завершится синхронно, даже если в [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena)был указан [ \_ Модификатор Internet Flag \_ Async](api-flags.md) .

События состояния дают отзыв о ходе выполнения сетевых операций, таких как разрешение имени узла, подключение к серверу и получение данных. Для маркера можно создавать три назначения состояния:

-   \_ \_ Закрытие обработчика состояния Интернета \_ — это последняя индикация состояния, сделанная для маркера.
-   \_ \_ Созданный обработчик состояния Интернета \_ указывает, когда был создан этот маркер.
-   \_Запрос состояния Интернета " \_ завершен" \_ означает, что асинхронная операция завершена.

Приложение должно проверить структуру [**\_ асинхронного \_ результата Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) , чтобы определить, завершилась ли операция успешно или неудачно после получения сообщения \_ о состоянии Интернета \_ \_ .

В следующем примере показан пример функции обратного вызова и вызов [**интернетсетстатускаллбакк**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) для регистрации функции в качестве функции обратного вызова.


```C++
void CALLBACK InternetCallback(
    HINTERNET hInternet,
    DWORD_PTR dwcontext,
    DWORD dwInternetStatus,
    LPVOID lpvStatusInformation,
    DWORD dwStatusInformationLength
    )
{
    _tprintf(TEXT("%0xd %0xp %0xd %0xp %0xd\n"),
             hInternet,
             dwcontext,
             dwInternetStatus,
             lpvStatusInformation,
             dwStatusInformationLength);
};

INTERNET_STATUS_CALLBACK dwISC =
    InternetSetStatusCallback(hInternet, InternetCallback); 
```



### <a name="closing-hinternet-handles"></a>Закрытие дескрипторов ХИНТЕРНЕТ

Все дескрипторы [**хинтернет**](appendix-a-hinternet-handles.md) можно закрыть с помощью функции [**интернетклосехандле**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) . Клиентские приложения должны закрыть все дескрипторы **хинтернет** , производные от дескриптора **хинтернет** , которые они пытаются закрыть перед вызовом [**интернетклосехандле**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) для дескриптора.

В следующем примере показана иерархия Handle.


```C++
HINTERNET hRootHandle, hOpenUrlHandle;

hRootHandle = InternetOpen( TEXT("Example"), 
                            INTERNET_OPEN_TYPE_DIRECT, 
                            NULL, 
                            NULL, 0);

hOpenUrlHandle = InternetOpenUrl(hRootHandle, 
    TEXT("https://www.server.com/default.htm"), NULL, 0, 
    INTERNET_FLAG_RAW_DATA,0);

// Close the handle created by InternetOpenUrl so that the
// InternetOpen handle can be closed.
InternetCloseHandle(hOpenUrlHandle); 

// Close the handle created by InternetOpen.
InternetCloseHandle(hRootHandle);
```



### <a name="locking-and-unlocking-resources"></a>Блокировка и разблокировка ресурсов

Функция [**интернетлоккрекуестфиле**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) позволяет приложению гарантировать, что кэшированный ресурс, связанный с переданным в него обработчиком [**хинтернет**](appendix-a-hinternet-handles.md) , не исчезнет из кэша. Если другой файл загрузки пытается зафиксировать ресурс с тем же URL-адресом, что и заблокированный файл, кэш позволяет избежать удаления файла путем выполнения безопасного удаления. После того как приложение вызовет функцию [**интернетунлоккрекуестфиле**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) , кэш получает разрешение на удаление файла.

Если не установлен флаг [Интернета флаг кэширования \_ \_ \_ \_ записи](api-flags.md) или подключения к [Интернету \_ флага \_ \_ кэша не](api-flags.md) , [**интернетлоккрекуестфиле**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) создает временный файл с расширением TMP, если только этот маркер не подключен к ресурсу HTTPS. Если функция обращается к ресурсу HTTPS и \_ флагу Интернета \_ не \_ задано кэширование \_ записи кэша (или \_ кэш не Internet Flag \_ \_ ), [**интернетлоккрекуестфиле**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) завершается с ошибкой.

> [!Note]  
> WinINet не поддерживает реализации серверов. Кроме того, его не следует использовать из службы. для серверных реализаций или служб используйте [Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 
