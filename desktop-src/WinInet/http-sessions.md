---
title: HTTP-сеансы
description: Доступ к ресурсам WWW осуществляется с помощью протокола HTTP.
ms.assetid: 0f307e28-9c38-41e7-9795-7eef08e99a3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b0b4d30bc86c588495a55ed4867a4084c43a09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134099"
---
# <a name="http-sessions"></a>HTTP-сеансы

WinINet позволяет получать доступ к ресурсам в Интернете (WWW). Доступ к этим ресурсам можно получить напрямую с помощью [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (Дополнительные сведения см. в разделе [доступ к URL-адресам напрямую](handling-uniform-resource-locators.md)).

Доступ к ресурсам WWW осуществляется с помощью протокола HTTP. Функции HTTP обработают базовые протоколы, позволяя приложению получать доступ к информации в Интернете. По мере развития протокола HTTP базовые протоколы обновляются для поддержки поведения функций.

На следующей диаграмме показаны связи функций, используемых с протоколом HTTP. Затененные поля представляют функции, которые возвращают дескрипторы [**хинтернет**](appendix-a-hinternet-handles.md) , а обычные поля представляют функции, использующие дескриптор **хинтернет** , созданный функцией, от которой они зависят.

![функции WinInet, используемые для HTTP](images/ax-wnt05.png)

Дополнительные сведения см. в разделе [Хинтернет Handles](appendix-a-hinternet-handles.md).

## <a name="using-the-wininet-functions-to-access-the-www"></a>Использование функций WinINet для доступа к веб-публикации

-   [Инициализация подключения к WWW](#initiating-a-connection-to-the-www)
-   [Открытие запроса](#opening-a-request)
-   [Добавление заголовков запроса](#adding-request-headers)
-   [Отправка запроса](#sending-a-request)
-   [Отправка данных на сервер](#posting-data-to-the-server)
-   [Получение сведений о запросе](#getting-information-about-a-request)
-   [Загрузка ресурсов из Интернета](#downloading-resources-from-the-www)

Следующие функции используются во время сеансов HTTP для доступа к WWW.



| Функция                                               | Описание                                                                                                                                                                                  |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**хттпаддрекуессеадерс**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) | Добавляет заголовки HTTP-запросов в обработчик HTTP-запросов. Эта функция требует создания маркера, созданного с помощью [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).                                                 |
| [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)             | Открывает обработчик HTTP-запроса. Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                                                         |
| [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)                 | Запрашивает сведения о HTTP-запросе. Эта функция требует создания маркера, созданного функцией [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) или [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) . |
| [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)             | Отправляет заданный HTTP-запрос на HTTP-сервер. Эта функция требует создания маркера, созданного с помощью [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).                                                  |
| [**интернетеррордлг**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)           | Отображает стандартные диалоговые окна для распространенных условий возникновения ошибок Интернета. Для этой функции требуется маркер, используемый в вызове [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).                     |



 

### <a name="initiating-a-connection-to-the-www"></a>Инициализация подключения к WWW

Чтобы запустить подключение к WWW, приложение должно вызвать функцию [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) в корневом [**хинтернет**](appendix-a-hinternet-handles.md) , возвращенном [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena). [**Интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) должен установить сеанс HTTP, объявив \_ тип HTTP службы Интернета \_ . Дополнительные сведения об использовании [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)см. в разделе [Использование интернетконнект](enabling-internet-functionality.md).

### <a name="opening-a-request"></a>Открытие запроса

Функция [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) открывает HTTP-запрос и возвращает маркер [**хинтернет**](appendix-a-hinternet-handles.md) , который может использоваться другими функциями HTTP. В отличие от других открытых функций (таких как [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) и [**Интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)), [**Хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) не отправляет запрос в Интернет при вызове. Функция [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) отправляет запрос и устанавливает подключение по сети.

[**Хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) принимает обработчик сеанса HTTP, созданный [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , и глагол HTTP, имя объекта, строку версии, источник ссылки, типы приема, флаги и значение контекста.

HTTP-команда является строкой, используемой в запросе. Распространенные глаголы HTTP, используемые в запросах, включают GET, WHERE и POST. Если это значение равно **null**, [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) использует значение по умолчанию Get.

Имя объекта — это строка, содержащая имя указанного целевого объекта HTTP-команды. Обычно это имя файла, исполняемый модуль или описатель поиска. Если переданное имя объекта является пустой строкой, [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) ищет страницу по умолчанию.

Строка версии должна содержать версию HTTP. Если этот параметр имеет **значение NULL**, функция использует "HTTP/1.1".

Источник ссылки задает адрес документа, из которого было получено имя объекта. Если этот параметр имеет **значение NULL**, источник ссылки не указывается.

Строка с завершающим **нулем**, которая содержит типы Accept, указывает типы содержимого, принимаемые приложением. Установка этого параметра в **значение NULL** означает, что приложение не принимает типы содержимого. Если указана пустая строка, приложение указывает, что оно принимает только документы типа "" Text/ \* "". Значение "" Text/" \* указывает только текстовые документы, а не рисунки или другие двоичные файлы.

Значения флагов управляют кэшированием, файлами cookie и проблемами безопасности. Для Microsoft Network (MSN), NTLM и других типов проверки подлинности установите флаг [ \_ \_ \_ подключения](api-flags.md) "установить флаг" для Интернета.

Если в вызове [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena)был установлен флаг [ \_ \_ Async Internet](api-flags.md) Flag, то для правильной асинхронной операции должно быть задано ненулевое значение контекста.

Ниже приведен пример вызова [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).

`hHttpRequest = HttpOpenRequest( hHttpSession, "GET", "", NULL, "", NULL, 0, 0);`

### <a name="adding-request-headers"></a>Добавление заголовков запроса

Функция [**хттпаддрекуессеадерс**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) позволяет приложениям добавлять в первоначальный запрос один или несколько заголовков запросов. Эта функция позволяет приложению добавлять в обработчик HTTP-запросов дополнительные заголовки свободного формата. Он предназначен для использования сложными приложениями, требующими точного контроля над запросом, отправленным на HTTP-сервер.

[**Хттпаддрекуессеадерс**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) требуется обработчик HTTP-запроса, созданный [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), строка, содержащая заголовки, длину заголовков и модификаторов.

### <a name="sending-a-request"></a>Отправка запроса

[**Хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) устанавливает подключение к Интернету и отправляет запрос на указанный сайт. Для этой функции требуется обработчик [**хинтернет**](appendix-a-hinternet-handles.md) , созданный [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta). [**Хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) также может передавать дополнительные заголовки или дополнительные сведения. Необязательные сведения обычно используются для операций, которые записывают сведения на сервер, такие как операции размещения и POST.

После того как [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) отправляет запрос, приложение может использовать функции [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)и [**интернетсетфилепоинтер**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) в обработчике [**HINTERNET**](appendix-a-hinternet-handles.md) , созданном [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) , для загрузки ресурсов сервера.

### <a name="posting-data-to-the-server"></a>Отправка данных на сервер

Для отправки данных на сервер HTTP-команда в вызове [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) должна быть либо POST, либо помещается. Адрес буфера, содержащего данные POST, должен передаваться в параметр *лпоптионал* в [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). Для параметра *двоптионалленгс* необходимо задать размер данных.

Можно также использовать функцию [**интернетвритефиле**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) для публикации данных в [**хинтернетном**](appendix-a-hinternet-handles.md) обработчике, отправленном с помощью [**хттпсендрекуестекс**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa).

### <a name="getting-information-about-a-request"></a>Получение сведений о запросе

[**Хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) позволяет приложению получать сведения о HTTP-запросе. Функции требуется обработчик [**хинтернет**](appendix-a-hinternet-handles.md) , созданный [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) или [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), значение информационного уровня и длина буфера. [**Хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) также принимает буфер, в котором хранятся данные, и индекс заголовков, начинающийся с нуля, который перечисляет несколько заголовков с одним и тем же именем.

### <a name="downloading-resources-from-the-www"></a>Загрузка ресурсов из Интернета

После открытия запроса с [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и его отправки на сервер с помощью [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)приложение может использовать функции [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)и [**интернетсетфилепоинтер**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) для загрузки ресурса с HTTP-сервера.

В следующем примере загружается ресурс. Функция принимает маркер в текущее окно, идентификационный номер поля ввода и маркер [**хинтернет**](appendix-a-hinternet-handles.md) , созданный [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) , и отправляется [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). Он использует [**интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) для определения размера ресурса, а затем загружает его с помощью [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile). Затем содержимое отображается в поле ввода.


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR lpszData;    // buffer for the data
    DWORD  dwSize;       // size of the data available
    DWORD  dwDownloaded; // size of the downloaded data
    DWORD  dwSizeSum=0;  // size of the data in the textbox
    LPTSTR lpszHolding;  // buffer to merge the textbox data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            printf("InternetQueryDataAvailable failed (%d)\n", GetLastError());
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,
                                 (LPVOID)lpszData,
                                 dwSize,
                                 &dwDownloaded))
            {
                printf("InternetReadFile failed (%d)\n", GetLastError());
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the data buffer
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];

                // Check if there has been any data written
                // to the textbox.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the textbox if any
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding,
                                   dwSizeSum);

                    // Add a null terminator at the end of the
                    // textbox data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string.
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + dwDownloaded + 1;
                LPTSTR* ppszDestEnd = 0;
                size_t* pcchRemaining = 0;

                // Add the new data to the holding buffer
                HRESULT hr = StringCchCatEx(lpszHolding,
                                            cchDest,
                                            lpszData,
                                            ppszDestEnd,
                                            pcchRemaining,
                                            STRSAFE_NO_TRUNCATION);

                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the textbox.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to the
                    // textbox data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                        break;
                    else
                    {
                    //  TODO: Insert error handling code here.
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

    return TRUE;
}
```



> [!Note]  
> WinINet не поддерживает реализации серверов. Кроме того, его не следует использовать из службы. Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 