---
title: Создание функций обратного вызова состояния
description: В этом учебнике описывается создание функции обратного вызова состояния, используемой для отслеживания состояния Интернет-запроса.
ms.assetid: 518d0800-5ea6-4327-8459-901e6d9a8a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e46040d9b6f93645e2730af287a1955343ec3a
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "105710405"
---
# <a name="creating-status-callback-functions"></a>Создание функций обратного вызова состояния

В этом учебнике описывается создание функции обратного вызова состояния, используемой для отслеживания состояния Интернет-запроса.

Функции обратного вызова состояния получают обратные вызовы состояния для любых Интернет-запросов, которые были переданы из любой функции WinINet, которая передала ненулевое значение контекста.


Для создания функции обратного вызова состояния необходимо выполнить следующие действия.

1.  [Определите значение контекста.](#defining-the-context-value)
2.  [Создайте функцию обратного вызова состояния.](#creating-status-callback-functions)

### <a name="defining-the-context-value"></a>Определение значения контекста

Значением контекста может быть любое длинное целочисленное значение без знака. В идеале значение контекста должно определить, какой запрос был только что выполнен, и расположение связанных ресурсов, если это необходимо.

Одним из наиболее полезных способов использования контекстного значения является передача адреса структуры и его приведение к типу **DWORD \_ ptr**. Структуру можно использовать для хранения сведений о запросе, чтобы он был передан функции обратного вызова состояния.

Следующая структура является примером возможного значения контекста. Элементы структуры выбираются с учетом функции [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .


```C++
typedef struct{
    HWND       hWindow;      // Window handle
    int        nStatusList;  // List box control to hold callbacks
    HINTERNET  hResource;    // HINTERNET handle created by InternetOpenUrl
    char       szMemo[512];  // String to store status memo
} REQUEST_CONTEXT;
```



В этом примере функция обратного вызова состояния будет иметь доступ к маркеру окна, что позволит отобразить пользовательский интерфейс. Созданный [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) обработчик [**хинтернет**](appendix-a-hinternet-handles.md) может быть передан другой функции, которая может загрузить ресурс и массив символов, которые можно использовать для передачи сведений о запросе.

Члены структуры могут быть изменены в соответствии с потребностями конкретного приложения, поэтому в данном примере это не ограничено.

### <a name="creating-the-status-callback-function"></a>Создание функции обратного вызова состояния

Функция обратного вызова состояния должна соответствовать формату [*интернетстатускаллбакк*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback). Для этого выполните следующие действия.

1.  Напишите объявление функции для функции обратного вызова состояния.

    В следующем примере показан пример объявления.

    ```C++
    void CALLBACK CallMaster( HINTERNET,
                              DWORD_PTR,
                              DWORD,
                              LPVOID,
                              DWORD );
    ```

    

2.  Определите, что будет делать функция обратного вызова состояния. Для приложений, выполняющих асинхронные вызовы, функция обратного вызова состояния должна поддерживать \_ \_ значение завершения запроса состояния Интернета \_ , которое указывает на то, что асинхронный запрос завершен. Функцию обратного вызова состояния также можно использовать для отслеживания хода выполнения Интернет запроса.

    Как правило, лучше использовать оператор switch с *двинтернетстатус* в качестве значения переключателя и значений состояния для инструкций CASE. В зависимости от типов функций, которые вызывает приложение, можно игнорировать некоторые значения состояния. Определение различных значений состояния см. в списке под параметром *двинтернетстатус* в [*интернетстатускаллбакк*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).

    Приведенный ниже оператор switch представляет собой пример того, как обрабатывает обратные вызовы состояния.

    ``` syntax
    switch (dwInternetStatus)
    {
        case INTERNET_STATUS_REQUEST_COMPLETE:
            // Add code
            break;
        default:
            // Add code
            break;
    }
    ```

3.  Создайте код для управления значениями состояния.

    Код для управления каждым из значений состояния зависит от предполагаемого использования функции обратного вызова состояния. Для приложений, которые просто отслеживают ход выполнения запроса, запись строки в поле со списком может быть достаточной. Для асинхронных операций код должен поддерживать некоторые данные, возвращаемые в обратном вызове.

    Следующая функция обратного вызова состояния использует функцию Switch для определения значения Status и создает строку, включающую в себя имя значения состояния и предыдущую функцию, которая хранится в элементе Сзмемо \_ структуры контекста запроса.

    ```C++
    void __stdcall CallMaster(
        HINTERNET hInternet,
        DWORD_PTR dwContext,
        DWORD dwInternetStatus,
        LPVOID lpvStatusInformation,
        DWORD dwStatusInformationLength
    )
    {
        UNREFERENCED_PARAMETER(hInternet);
        UNREFERENCED_PARAMETER(lpvStatusInformation);
        UNREFERENCED_PARAMETER(dwStatusInformationLength);

        REQUEST_CONTEXT *cpContext;
        cpContext = (REQUEST_CONTEXT*)dwContext;
        char szStatusText[80];

        switch (dwInternetStatus)
        {
            case INTERNET_STATUS_CLOSING_CONNECTION:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CLOSING_CONNECTION",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_CONNECTED_TO_SERVER:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTED_TO_SERVER",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_CONNECTING_TO_SERVER:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTING_TO_SERVER",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_CONNECTION_CLOSED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTION_CLOSED",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_HANDLE_CLOSING:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s HANDLE_CLOSING",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_HANDLE_CREATED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s HANDLE_CREATED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_INTERMEDIATE_RESPONSE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s INTERMEDIATE_RESPONSE",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_NAME_RESOLVED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s NAME_RESOLVED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RECEIVING_RESPONSE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RECEIVING_RESPONSE",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RESPONSE_RECEIVED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RESPONSE_RECEIVED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_REDIRECT:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REDIRECT",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_REQUEST_COMPLETE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REQUEST_COMPLETE",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_REQUEST_SENT:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REQUEST_SENT",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RESOLVING_NAME:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RESOLVING_NAME",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_SENDING_REQUEST:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s SENDING_REQUEST",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_STATE_CHANGE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s STATE_CHANGE",
                                  cpContext->szMemo );
                break;
            default:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s Unknown Status %d Given",
                                  cpContext->szMemo,
                                  dwInternetStatus);
                break;
        }

        SendDlgItemMessage( cpContext->hWindow,
                          cpContext->nStatusList,
                          LB_ADDSTRING,
                          0, (LPARAM)szStatusText );

    }
    ```

    

4.  Используйте функцию [**интернетсетстатускаллбакк**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) , чтобы задать функцию обратного вызова состояния для маркера [**хинтернет**](appendix-a-hinternet-handles.md) , для которого требуется получить обратные вызовы состояния.

    В следующем примере показано, как задать функцию обратного вызова состояния.

    ```C++
    HINTERNET hOpen;                       // Root HINTERNET handle
    INTERNET_STATUS_CALLBACK iscCallback;  // Holds the callback function

    // Create the root HINTERNET handle.
    hOpen = InternetOpen( TEXT("Test Application"),
                          INTERNET_OPEN_TYPE_PRECONFIG,
                          NULL, NULL, 0);

    // Set the status callback function.
    iscCallback = InternetSetStatusCallback( hOpen, (INTERNET_STATUS_CALLBACK)CallMaster );
    ```

    

> [!Note]  
> WinINet не поддерживает реализации серверов. Кроме того, его не следует использовать из службы. Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание функций обратного вызова состояния](creating-status-callback-functions.md)
</dt> <dt>

[**интернетсетстатускаллбакк**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)
</dt> <dt>

[*интернетстатускаллбакк*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback)
</dt> </dl>

 

 