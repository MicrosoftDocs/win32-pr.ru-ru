---
description: Этот раздел содержит пример того, как написать сценарий, который получает данные через службы Microsoft Windows HTTP (WinHTTP) синхронно или асинхронно.
ms.assetid: 84b847f8-4d9e-4fea-9e87-df4c65b54a02
title: Извлечение данных с помощью скрипта
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 734516cf75f92cc43ab4cb15f22bd97aa803ec33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990856"
---
# <a name="retrieving-data-using-script"></a>Извлечение данных с помощью скрипта

Этот раздел содержит пример того, как написать сценарий, который получает данные через службы Microsoft Windows HTTP (WinHTTP) синхронно или асинхронно. Концепции, продемонстрированные в этом примере, служат основанием для написания серверных приложений или серверов среднего уровня, которым требуется доступ к данным с помощью протокола HTTP.

-   [Необходимые условия и требования](#prerequisites-and-requirements)
-   [Синхронное получение данных](#retrieving-data-synchronously)
-   [Асинхронное получение данных](#retrieving-data-asynchronously)
-   [См. также](#related-topics)

## <a name="prerequisites-and-requirements"></a>Необходимые условия и требования

В дополнение к опыту работы с Microsoft JScript для этого примера требуется следующее:

-   Текущая версия пакета средств разработки программного обеспечения (SDK) для Microsoft Windows.
-   Средство настройки прокси-сервера для установки параметров прокси-сервера для служб Microsoft Windows HTTP (WinHTTP), если подключение к Интернету осуществляется через прокси-сервер. Дополнительные сведения см. [ в разделеProxyCfg.exe, средство настройки прокси-сервера](proxycfg-exe--a-proxy-configuration-tool.md).
-   Знакомство с [терминологией](network-terminology.md) и концепциями сети.

## <a name="retrieving-data-synchronously"></a>Синхронное получение данных

**Чтобы создать скрипт для синхронного получения текста с веб-страницы, выполните следующие действия.**

1.  Откройте текстовый редактор.
2.  Скопируйте следующий код в текстовый редактор.

    ```JScript
    function getText(strURL)
    {
        var strResult;
        
        try
        {
            // Create the WinHTTPRequest ActiveX Object.
            var WinHttpReq = new ActiveXObject(
                                      "WinHttp.WinHttpRequest.5.1");
            
            //  Create an HTTP request.
            var temp = WinHttpReq.Open("GET", strURL, false);

            //  Send the HTTP request.
            WinHttpReq.Send();
            
            //  Retrieve the response text.
            strResult = WinHttpReq.ResponseText;
        }
        catch (objError)
        {
            strResult = objError + "\n"
            strResult += "WinHTTP returned error: " + 
                (objError.number & 0xFFFF).toString() + "\n\n";
            strResult += objError.description;
        }
        
        //  Return the response text.
        return strResult;
    }

    WScript.Echo(getText("https://www.microsoft.com/default.htm"));
    ```

    

3.  Сохраните файл как "Retrieve.js".
4.  В командной строке введите "cscript Retrieve.js" и нажмите клавишу ВВОД.

Теперь у вас есть скрипт, использующий объект [**WinHttpRequest**](winhttprequest.md) для получения ИСХОДНОГО кода HTML для веб-страницы по адресу https://www.microsoft.com . Для отображения кода может потребоваться несколько секунд.

Приложение содержит только одну функцию "gettext". Первая строка скрипта создает объект [**WinHttpRequest**](winhttprequest.md) .


```JScript
    // Create the WinHTTPRequest ActiveX Object.
    var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```



Когда обработчик JScript обнаруживает эту строку, он создает экземпляр этого объекта. При получении сообщения об ошибке "компонент ActiveX не может создать объект" в этой строке, скорее всего, WinHttp.dll не был правильно зарегистрирован или отсутствует в системе.

Следующая строка скрипта вызывает метод [**Open**](iwinhttprequest-open.md) .


```JScript
    //  Create an HTTP request.
    WinHttpReq.Open("GET", "https://www.microsoft.com", false);
```



Три параметра указывают, какую [*HTTP-команду*](glossary.md) использовать, имя ресурса и необходимость использования WinHTTP синхронно или асинхронно. В этом примере метод использует *команду HTTP*"Get" для получения данных https://www.microsoft.com . Указание значения **false** для последнего параметра определяет, что транзакция выполняется синхронно. Метод [**Open**](iwinhttprequest-open.md) не устанавливает соединение с ресурсом, как это может предположить имя. Вместо этого он инициализирует внутренние структуры данных, которые сохраняют сведения о сеансе, соединении и запросе.

Метод [**Send**](iwinhttprequest-send.md) собирает заголовки запроса и отправляет запрос. При вызове в синхронном режиме метод [**Send**](iwinhttprequest-send.md) также ждет ответа, прежде чем разрешить продолжение работы приложения.


```JScript
    // Send the HTTP request.
    WinHttpReq.Send();
```



После отправки запроса скрипт возвращает значение свойства [**респонсетекст**](iwinhttprequest-responsetext.md) объекта [**WinHttpRequest**](winhttprequest.md) . Это свойство содержит текст сущности ответа (в данном случае — источник документа).


```JScript
    // Get the response text.
    return WinHttpReq.ResponseText;
```



Выполнение сценария приостанавливается во время извлечения всего текста ресурса. Текст ресурса возвращается из функции и отображается.

Объект [**WinHttpRequest**](winhttprequest.md) гарантирует, что все внутренние ресурсы, выделенные для HTTP-транзакции, будут освобождены.

## <a name="retrieving-data-asynchronously"></a>Асинхронное получение данных

Асинхронное извлечение данных с помощью WinHTTP очень похоже на получение данных в синхронном режиме. Измените скрипт из предыдущего раздела, сделав два небольших изменения.

1.  Задайте для третьего параметра метода [**Open**](iwinhttprequest-open.md) значение true вместо false, чтобы указать, что методы WinHTTP должны выполняться асинхронно.
    ```JScript
       //  Create a HTTP request.
        var temp = WinHttpReq.Open("GET", strURL, true);
    ```

    

2.  Вызовите метод [**ваитфорреспонсе**](iwinhttprequest-waitforresponse.md) перед обращением к свойству [**респонсетекст**](iwinhttprequest-responsetext.md) , чтобы убедиться, что получен весь ответ.
    ```JScript
        //  Send the HTTP request.
        WinHttpReq.Send();
            
        // Wait for the entire response.
        WinHttpReq.WaitForResponse();
            
        //  Retrieve the response text.
        strResult = WinHttpReq.ResponseText;
    ```

    

Основным преимуществом асинхронного использования WinHTTP в скрипте является то, что метод [**Send**](iwinhttprequest-send.md) немедленно возвращает значение. Запрос подготовлен и отправлен рабочим потоком. Это позволяет приложению выполнять другие действия, пока оно ожидает ответа. Прежде чем пытаться получить доступ к ответу, убедитесь, что получен весь ответ, вызвав метод [**ваитфорреспонсе**](iwinhttprequest-waitforresponse.md) . В противном случае может возникнуть ошибка.

Метод [**ваитфорреспонсе**](iwinhttprequest-waitforresponse.md) также можно использовать для указания значения времени ожидания для транзакции. Необязательный параметр позволяет указать значение времени ожидания в секундах.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Запрос HTTP/1.1 для комментариев (RFC 2616)](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



