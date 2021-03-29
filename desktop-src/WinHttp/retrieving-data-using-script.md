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
# <a name="retrieving-data-using-script"></a><span data-ttu-id="8a433-103">Извлечение данных с помощью скрипта</span><span class="sxs-lookup"><span data-stu-id="8a433-103">Retrieving Data Using Script</span></span>

<span data-ttu-id="8a433-104">Этот раздел содержит пример того, как написать сценарий, который получает данные через службы Microsoft Windows HTTP (WinHTTP) синхронно или асинхронно.</span><span class="sxs-lookup"><span data-stu-id="8a433-104">This topic includes an example of how to write a script that obtains data through Microsoft Windows HTTP Services (WinHTTP) either synchronously or asynchronously.</span></span> <span data-ttu-id="8a433-105">Концепции, продемонстрированные в этом примере, служат основанием для написания серверных приложений или серверов среднего уровня, которым требуется доступ к данным с помощью протокола HTTP.</span><span class="sxs-lookup"><span data-stu-id="8a433-105">The concepts demonstrated in this example provide the basis for writing client or middle-tier server applications that require access to data using the HTTP protocol.</span></span>

-   [<span data-ttu-id="8a433-106">Необходимые условия и требования</span><span class="sxs-lookup"><span data-stu-id="8a433-106">Prerequisites and Requirements</span></span>](#prerequisites-and-requirements)
-   [<span data-ttu-id="8a433-107">Синхронное получение данных</span><span class="sxs-lookup"><span data-stu-id="8a433-107">Retrieving Data Synchronously</span></span>](#retrieving-data-synchronously)
-   [<span data-ttu-id="8a433-108">Асинхронное получение данных</span><span class="sxs-lookup"><span data-stu-id="8a433-108">Retrieving Data Asynchronously</span></span>](#retrieving-data-asynchronously)
-   [<span data-ttu-id="8a433-109">См. также</span><span class="sxs-lookup"><span data-stu-id="8a433-109">Related topics</span></span>](#related-topics)

## <a name="prerequisites-and-requirements"></a><span data-ttu-id="8a433-110">Необходимые условия и требования</span><span class="sxs-lookup"><span data-stu-id="8a433-110">Prerequisites and Requirements</span></span>

<span data-ttu-id="8a433-111">В дополнение к опыту работы с Microsoft JScript для этого примера требуется следующее:</span><span class="sxs-lookup"><span data-stu-id="8a433-111">In addition to a working knowledge of Microsoft JScript, this example requires the following:</span></span>

-   <span data-ttu-id="8a433-112">Текущая версия пакета средств разработки программного обеспечения (SDK) для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8a433-112">The current version of the Microsoft Windows Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="8a433-113">Средство настройки прокси-сервера для установки параметров прокси-сервера для служб Microsoft Windows HTTP (WinHTTP), если подключение к Интернету осуществляется через прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="8a433-113">The proxy configuration tool to establish the proxy settings for Microsoft Windows HTTP Services (WinHTTP), if your connection to the Internet is through a proxy server.</span></span> <span data-ttu-id="8a433-114">Дополнительные сведения см. [ в разделеProxyCfg.exe, средство настройки прокси-сервера](proxycfg-exe--a-proxy-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="8a433-114">For more information, see [ProxyCfg.exe, a Proxy Configuration Tool](proxycfg-exe--a-proxy-configuration-tool.md).</span></span>
-   <span data-ttu-id="8a433-115">Знакомство с [терминологией](network-terminology.md) и концепциями сети.</span><span class="sxs-lookup"><span data-stu-id="8a433-115">A familiarity with [network terminology](network-terminology.md) and concepts.</span></span>

## <a name="retrieving-data-synchronously"></a><span data-ttu-id="8a433-116">Синхронное получение данных</span><span class="sxs-lookup"><span data-stu-id="8a433-116">Retrieving Data Synchronously</span></span>

<span data-ttu-id="8a433-117">**Чтобы создать скрипт для синхронного получения текста с веб-страницы, выполните следующие действия.**</span><span class="sxs-lookup"><span data-stu-id="8a433-117">**To create a script that obtains the text from a Web page synchronously, do the following:**</span></span>

1.  <span data-ttu-id="8a433-118">Откройте текстовый редактор.</span><span class="sxs-lookup"><span data-stu-id="8a433-118">Open a text editor.</span></span>
2.  <span data-ttu-id="8a433-119">Скопируйте следующий код в текстовый редактор.</span><span class="sxs-lookup"><span data-stu-id="8a433-119">Copy the following code into the text editor.</span></span>

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

    

3.  <span data-ttu-id="8a433-120">Сохраните файл как "Retrieve.js".</span><span class="sxs-lookup"><span data-stu-id="8a433-120">Save the file as "Retrieve.js".</span></span>
4.  <span data-ttu-id="8a433-121">В командной строке введите "cscript Retrieve.js" и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="8a433-121">From a command prompt, type "cscript Retrieve.js" and press ENTER.</span></span>

<span data-ttu-id="8a433-122">Теперь у вас есть скрипт, использующий объект [**WinHttpRequest**](winhttprequest.md) для получения ИСХОДНОГО кода HTML для веб-страницы по адресу https://www.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="8a433-122">You now have a script that uses a [**WinHttpRequest**](winhttprequest.md) object to obtain the HTML source code for the Web page at https://www.microsoft.com.</span></span> <span data-ttu-id="8a433-123">Для отображения кода может потребоваться несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="8a433-123">You might have to wait several seconds for the code to appear.</span></span>

<span data-ttu-id="8a433-124">Приложение содержит только одну функцию "gettext".</span><span class="sxs-lookup"><span data-stu-id="8a433-124">The application contains only one function, "getText".</span></span> <span data-ttu-id="8a433-125">Первая строка скрипта создает объект [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="8a433-125">The first line of the script creates the [**WinHttpRequest**](winhttprequest.md) object.</span></span>


```JScript
    // Create the WinHTTPRequest ActiveX Object.
    var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```



<span data-ttu-id="8a433-126">Когда обработчик JScript обнаруживает эту строку, он создает экземпляр этого объекта.</span><span class="sxs-lookup"><span data-stu-id="8a433-126">When the JScript engine encounters this line, it creates an instance of this object.</span></span> <span data-ttu-id="8a433-127">При получении сообщения об ошибке "компонент ActiveX не может создать объект" в этой строке, скорее всего, WinHttp.dll не был правильно зарегистрирован или отсутствует в системе.</span><span class="sxs-lookup"><span data-stu-id="8a433-127">If you get the error message, "ActiveX component can't create object", on this line, most likely the WinHttp.dll was not properly registered or is not present on the system.</span></span>

<span data-ttu-id="8a433-128">Следующая строка скрипта вызывает метод [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="8a433-128">The next line of the script calls the [**Open**](iwinhttprequest-open.md) method.</span></span>


```JScript
    //  Create an HTTP request.
    WinHttpReq.Open("GET", "https://www.microsoft.com", false);
```



<span data-ttu-id="8a433-129">Три параметра указывают, какую [*HTTP-команду*](glossary.md) использовать, имя ресурса и необходимость использования WinHTTP синхронно или асинхронно.</span><span class="sxs-lookup"><span data-stu-id="8a433-129">Three parameters specify which [*HTTP verb*](glossary.md) to use, the name of the resource, and whether to use WinHTTP synchronously or asynchronously.</span></span> <span data-ttu-id="8a433-130">В этом примере метод использует *команду HTTP*"Get" для получения данных https://www.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="8a433-130">In this example, the method is using the *HTTP verb*"GET" to obtain data from https://www.microsoft.com.</span></span> <span data-ttu-id="8a433-131">Указание значения **false** для последнего параметра определяет, что транзакция выполняется синхронно.</span><span class="sxs-lookup"><span data-stu-id="8a433-131">Specifying **FALSE** for the last parameter determines that the transaction occurs synchronously.</span></span> <span data-ttu-id="8a433-132">Метод [**Open**](iwinhttprequest-open.md) не устанавливает соединение с ресурсом, как это может предположить имя.</span><span class="sxs-lookup"><span data-stu-id="8a433-132">The [**Open**](iwinhttprequest-open.md) method does not establish a connection to the resource as the name might imply.</span></span> <span data-ttu-id="8a433-133">Вместо этого он инициализирует внутренние структуры данных, которые сохраняют сведения о сеансе, соединении и запросе.</span><span class="sxs-lookup"><span data-stu-id="8a433-133">Rather, it initializes the internal data structures that maintain information about the session, connection, and request.</span></span>

<span data-ttu-id="8a433-134">Метод [**Send**](iwinhttprequest-send.md) собирает заголовки запроса и отправляет запрос.</span><span class="sxs-lookup"><span data-stu-id="8a433-134">The [**Send**](iwinhttprequest-send.md) method assembles the request headers and sends the request.</span></span> <span data-ttu-id="8a433-135">При вызове в синхронном режиме метод [**Send**](iwinhttprequest-send.md) также ждет ответа, прежде чем разрешить продолжение работы приложения.</span><span class="sxs-lookup"><span data-stu-id="8a433-135">When called in synchronous mode, the [**Send**](iwinhttprequest-send.md) method also waits for a response before allowing the application to continue.</span></span>


```JScript
    // Send the HTTP request.
    WinHttpReq.Send();
```



<span data-ttu-id="8a433-136">После отправки запроса скрипт возвращает значение свойства [**респонсетекст**](iwinhttprequest-responsetext.md) объекта [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="8a433-136">After sending the request, the script returns the value of the [**ResponseText**](iwinhttprequest-responsetext.md) property of the [**WinHttpRequest**](winhttprequest.md) object.</span></span> <span data-ttu-id="8a433-137">Это свойство содержит текст сущности ответа (в данном случае — источник документа).</span><span class="sxs-lookup"><span data-stu-id="8a433-137">This property contains the entity body of the response, in this case, the source of a document.</span></span>


```JScript
    // Get the response text.
    return WinHttpReq.ResponseText;
```



<span data-ttu-id="8a433-138">Выполнение сценария приостанавливается во время извлечения всего текста ресурса.</span><span class="sxs-lookup"><span data-stu-id="8a433-138">Execution of the script pauses while the entire text of the resource is retrieved.</span></span> <span data-ttu-id="8a433-139">Текст ресурса возвращается из функции и отображается.</span><span class="sxs-lookup"><span data-stu-id="8a433-139">The resource text is returned from the function and displayed.</span></span>

<span data-ttu-id="8a433-140">Объект [**WinHttpRequest**](winhttprequest.md) гарантирует, что все внутренние ресурсы, выделенные для HTTP-транзакции, будут освобождены.</span><span class="sxs-lookup"><span data-stu-id="8a433-140">The [**WinHttpRequest**](winhttprequest.md) object ensures that any internal resources that are allocated for the HTTP transaction are released.</span></span>

## <a name="retrieving-data-asynchronously"></a><span data-ttu-id="8a433-141">Асинхронное получение данных</span><span class="sxs-lookup"><span data-stu-id="8a433-141">Retrieving Data Asynchronously</span></span>

<span data-ttu-id="8a433-142">Асинхронное извлечение данных с помощью WinHTTP очень похоже на получение данных в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="8a433-142">Retrieving data asynchronously using WinHTTP is very similar to retrieving data synchronously.</span></span> <span data-ttu-id="8a433-143">Измените скрипт из предыдущего раздела, сделав два небольших изменения.</span><span class="sxs-lookup"><span data-stu-id="8a433-143">Modify the script from the previous section by making two small changes.</span></span>

1.  <span data-ttu-id="8a433-144">Задайте для третьего параметра метода [**Open**](iwinhttprequest-open.md) значение true вместо false, чтобы указать, что методы WinHTTP должны выполняться асинхронно.</span><span class="sxs-lookup"><span data-stu-id="8a433-144">Set the third parameter of the [**Open**](iwinhttprequest-open.md) method to "true" instead of "false" to specify that WinHTTP methods should be performed asynchronously.</span></span>
    ```JScript
       //  Create a HTTP request.
        var temp = WinHttpReq.Open("GET", strURL, true);
    ```

    

2.  <span data-ttu-id="8a433-145">Вызовите метод [**ваитфорреспонсе**](iwinhttprequest-waitforresponse.md) перед обращением к свойству [**респонсетекст**](iwinhttprequest-responsetext.md) , чтобы убедиться, что получен весь ответ.</span><span class="sxs-lookup"><span data-stu-id="8a433-145">Invoke the [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method before accessing the [**ResponseText**](iwinhttprequest-responsetext.md) property to ensure that the entire response has been received.</span></span>
    ```JScript
        //  Send the HTTP request.
        WinHttpReq.Send();
            
        // Wait for the entire response.
        WinHttpReq.WaitForResponse();
            
        //  Retrieve the response text.
        strResult = WinHttpReq.ResponseText;
    ```

    

<span data-ttu-id="8a433-146">Основным преимуществом асинхронного использования WinHTTP в скрипте является то, что метод [**Send**](iwinhttprequest-send.md) немедленно возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8a433-146">The main advantage to using WinHTTP asynchronously in script is that the [**Send**](iwinhttprequest-send.md) method returns immediately.</span></span> <span data-ttu-id="8a433-147">Запрос подготовлен и отправлен рабочим потоком.</span><span class="sxs-lookup"><span data-stu-id="8a433-147">The request is prepared and sent by a worker thread.</span></span> <span data-ttu-id="8a433-148">Это позволяет приложению выполнять другие действия, пока оно ожидает ответа.</span><span class="sxs-lookup"><span data-stu-id="8a433-148">This enables your application to do other things while it is waiting for the response.</span></span> <span data-ttu-id="8a433-149">Прежде чем пытаться получить доступ к ответу, убедитесь, что получен весь ответ, вызвав метод [**ваитфорреспонсе**](iwinhttprequest-waitforresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="8a433-149">Before attempting to access the response, ensure that the entire response has been received by calling the [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method.</span></span> <span data-ttu-id="8a433-150">В противном случае может возникнуть ошибка.</span><span class="sxs-lookup"><span data-stu-id="8a433-150">Otherwise an error can occur.</span></span>

<span data-ttu-id="8a433-151">Метод [**ваитфорреспонсе**](iwinhttprequest-waitforresponse.md) также можно использовать для указания значения времени ожидания для транзакции.</span><span class="sxs-lookup"><span data-stu-id="8a433-151">The [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method can also be used to specify a time-out value for the transaction.</span></span> <span data-ttu-id="8a433-152">Необязательный параметр позволяет указать значение времени ожидания в секундах.</span><span class="sxs-lookup"><span data-stu-id="8a433-152">An optional parameter enables you to specify the time-out value in seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a433-153">См. также</span><span class="sxs-lookup"><span data-stu-id="8a433-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a433-154">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="8a433-154">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="8a433-155">Запрос HTTP/1.1 для комментариев (RFC 2616)</span><span class="sxs-lookup"><span data-stu-id="8a433-155">HTTP/1.1 Request for Comments (RFC 2616)</span></span>](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



