---
description: Использование компьютера, использующего протокол HTTP, позволяет пользователям использовать веб-браузер для простого доступа к информации на удаленном сервере по сети.
ms.assetid: 44f3ff21-4978-4902-aa74-ddeef60881db
title: Общие сведения о службе COM+ SOAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93ce7d80753f306777d3ac0b77dc46dc4e08d22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662095"
---
# <a name="com-soap-service-overview"></a><span data-ttu-id="79010-103">Общие сведения о службе COM+ SOAP</span><span class="sxs-lookup"><span data-stu-id="79010-103">COM+ SOAP Service Overview</span></span>

<span data-ttu-id="79010-104">Использование компьютера, использующего протокол HTTP, позволяет пользователям использовать веб-браузер для простого доступа к информации на удаленном сервере по сети.</span><span class="sxs-lookup"><span data-stu-id="79010-104">HTTP revolutionized computer use by allowing people to use a Web browser for easy access to information on a remote server over a network.</span></span> <span data-ttu-id="79010-105">Веб-службы XML теперь затронули разработку приложений, позволяя клиентским приложениям легко вызывать удаленные методы по сети.</span><span class="sxs-lookup"><span data-stu-id="79010-105">XML web services have now revolutionized application development by allowing client applications to easily call remote methods over a network.</span></span>

<span data-ttu-id="79010-106">Часто бывает полезно, чтобы клиентское приложение могло вызывать метод, реализованный на удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="79010-106">It is often useful for a client application to be able to call a method implemented on a remote server.</span></span> <span data-ttu-id="79010-107">Иногда метод использует временные данные, хранящиеся на удаленном сервере (например, метод, который возвращает текущую цену акции, соответствующую заданному символу-отметке).</span><span class="sxs-lookup"><span data-stu-id="79010-107">Sometimes the method makes use of volatile information stored on the remote server (for example, a method that returns the current price of the stock corresponding to a given ticker symbol).</span></span> <span data-ttu-id="79010-108">В других случаях разработчику требуется возможность обновления реализации методов без необходимости повторного развертывания всех приложений, которые его используют.</span><span class="sxs-lookup"><span data-stu-id="79010-108">At other times, the developer wants the ability to upgrade the methods implementation without having to redeploy all the applications that use it.</span></span>

<span data-ttu-id="79010-109">Как и веб-страницы, доступ к XML Web Services осуществляется через веб-сервер, например IIS, с использованием протокола HTTP.</span><span class="sxs-lookup"><span data-stu-id="79010-109">Like webpages, XML web services are accessed via a web server, such as IIS, using HTTP.</span></span> <span data-ttu-id="79010-110">Однако вместо веб-страниц, закодированных в HTML, эти пакеты HTTP содержат входные и выходные параметры вызовов к методу, реализованному на сервере, закодированном в SOAP.</span><span class="sxs-lookup"><span data-stu-id="79010-110">However, instead of webpages encoded in HTML, these HTTP packets contain the input and output parameters of calls to a method implemented on the server, encoded in SOAP.</span></span>

<span data-ttu-id="79010-111">Чтобы использовать веб-службу XML, необходимо знать URL-адрес, по которому предоставляется служба, и имя метода, который необходимо вызвать, и указать входные параметры для метода.</span><span class="sxs-lookup"><span data-stu-id="79010-111">To use an XML web service, you need to know the URL where the service is exposed and the name of the method you want to call, and you must provide the input parameters to the method.</span></span> <span data-ttu-id="79010-112">[Стандарт SOAP 1,1](https://www.w3.org/TR/SOAP/) предоставляет следующий пример пакета HTTP, содержащего удаленный вызов веб-службы XML по адресу https://www.stockquoteserver.com/StockQuote , который возвращает текущую цену на акцию, соответствующую данному символу Tick.</span><span class="sxs-lookup"><span data-stu-id="79010-112">[The SOAP 1.1 standard](https://www.w3.org/TR/SOAP/) provides the following example of an HTTP packet containing a remote call to an XML web service at https://www.stockquoteserver.com/StockQuote, which returns the current price of the stock corresponding to a given ticker symbol.</span></span>

``` syntax
POST /StockQuote HTTP/1.1
Host: www.stockquoteserver.com
Content-Type: text/xml; "charset=utf-8"
Content-Length: nnnn
SOAPAction: "Some-URI"

<SOAP-ENV:Envelope
xmlns:SOAP-ENV="https://schemas.xmlsoap.org/soap/envelope/"
SOAP-ENV:encodingStyle="https://schemas.xmlsoap.org/soap/encoding/">
<SOAP-ENV:Body>
<m:GetLastTradePrice xmlns:m="Some-URI">
<symbol>DIS</symbol>
</m:GetLastTradePrice>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

<span data-ttu-id="79010-113">Как показано в предыдущем примере, SOAP — это экземпляр XML, который может быть внедрен в HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="79010-113">As the preceding example illustrates, SOAP is an XML instance that can be embedded in an HTTP request.</span></span> <span data-ttu-id="79010-114">Аналогичным образом результат возвращается как HTTP-пакет с полезной нагрузкой SOAP, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="79010-114">Similarly, the result is returned as an HTTP packet with a SOAP payload, as shown in the following example.</span></span>

``` syntax
HTTP/1.1 200 OK
Content-Type: text/xml; "charset=utf-8"
Content-Length: nnnn

<SOAP-ENV:Envelope
xmlns:SOAP-ENV="https://schemas.xmlsoap.org/soap/envelope/"
SOAP-ENV:encodingStyle="https://schemas.xmlsoap.org/soap/encoding//">
<SOAP-ENV:Body>
<m:GetLastTradePriceResponse xmlns:m="Some-URI">
<Price>34.5</Price>
</m:GetLastTradePriceResponse>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

<span data-ttu-id="79010-115">Хотя полезно иметь представление об инфраструктуре, которая является веб-службами XML, COM+ упрощает создание и использование веб-служб XML, которые часто не приходится углубляться на этот уровень.</span><span class="sxs-lookup"><span data-stu-id="79010-115">While it is helpful to have some understanding of the infrastructure that underlies XML web services, COM+ makes it so easy to create and use XML web services that you won't often have to delve to this level.</span></span>

<span data-ttu-id="79010-116">Вы можете предоставлять методы в интерфейсах по умолчанию настроенных компонентов COM в любом приложении COM+ в качестве веб-службы XML.</span><span class="sxs-lookup"><span data-stu-id="79010-116">You can expose the methods in the default interfaces of the configured COM components in any COM+ application as an XML web service.</span></span> <span data-ttu-id="79010-117">При написании компонентов не требуются специальные рекомендации по программированию, за исключением того, что методы, которые необходимо предоставить, должны быть в интерфейсе по умолчанию, а компонент должен быть настроен (в каталоге COM+ сервера).</span><span class="sxs-lookup"><span data-stu-id="79010-117">No special programming considerations are necessary when writing the components, except that the methods you want to expose must be in the default interface and the component must be configured (in your server's COM+ catalog).</span></span> <span data-ttu-id="79010-118">Не требуется писать код для взаимодействия через сетевой интерфейс или для синтаксического анализа SOAP.</span><span class="sxs-lookup"><span data-stu-id="79010-118">You need not write code to communicate via a network interface or to parse SOAP.</span></span> <span data-ttu-id="79010-119">Подробные инструкции по использованию службы COM+ SOAP для создания веб-службы XML см. в разделе [Создание веб-служб XML](creating-xml-web-services.md).</span><span class="sxs-lookup"><span data-stu-id="79010-119">For detailed instructions about using the COM+ SOAP service to create an XML web service, see [Creating XML Web Services](creating-xml-web-services.md).</span></span>

<span data-ttu-id="79010-120">При предоставлении приложения COM+ в качестве веб-службы XML подробные сведения о синтаксисе всех методов, доступных из веб-службы XML, публикуются автоматически с помощью языка описания веб-служб (WSDL).</span><span class="sxs-lookup"><span data-stu-id="79010-120">When you expose a COM+ application as an XML web service, detailed information about the syntax of all the methods available from an XML web service is published automatically, using the Web Services Description Language (WSDL).</span></span> <span data-ttu-id="79010-121">Эти сведения используются клиентами, которые используют веб-службу XML.</span><span class="sxs-lookup"><span data-stu-id="79010-121">This information is used by clients that use your XML web service.</span></span>

<span data-ttu-id="79010-122">COM+ предоставляет два способа доступа и использования удаленной веб-службы XML, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="79010-122">COM+ provides two ways for you to access and use a remote XML web service, as follows:</span></span>

-   <span data-ttu-id="79010-123">Режим *хорошо известного объекта* (ВКО) можно использовать для доступа к любой веб-службе XML, которая публикует свой синтаксис с помощью WSDL, даже если эта веб-служба XML не была создана с помощью COM+ или даже Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="79010-123">The *well-known object* (WKO) mode can be used to access any XML web service that publishes its syntax using WSDL, even if that XML web service was not created using COM+ or even Microsoft Windows.</span></span>
-   <span data-ttu-id="79010-124">Режим *активируемого клиентом объекта* (Као) можно использовать только для доступа к веб-службам XML, созданным посредством предоставления приложений COM+.</span><span class="sxs-lookup"><span data-stu-id="79010-124">The *client-activated object* (CAO) mode can be used only to access XML web services created by exposing COM+ applications.</span></span> <span data-ttu-id="79010-125">Режим Као повышает производительность с помощью постоянных подключений, функции, которая не поддерживается текущим стандартом SOAP.</span><span class="sxs-lookup"><span data-stu-id="79010-125">CAO mode increases performance by using persistent connections, a feature not supported by the current SOAP standard.</span></span>

<span data-ttu-id="79010-126">Оба метода позволяют клиентским приложениям удаленно вызывать методы веб-служб XML, не требуя написания кода для взаимодействия через сетевой интерфейс или синтаксического анализа SOAP.</span><span class="sxs-lookup"><span data-stu-id="79010-126">Both methods allow client applications to call the methods of XML web services remotely in a straightforward fashion, without having to write code to communicate via a network interface or parse SOAP.</span></span> <span data-ttu-id="79010-127">Дополнительные сведения о доступе к веб-службам XML в любом режиме см. в разделе [доступ к веб-службам XML в режиме Као](accessing-xml-web-services-in-cao-mode.md) и [доступ к веб-службам XML в режиме ВКО](accessing-xml-web-services-in-wko-mode.md).</span><span class="sxs-lookup"><span data-stu-id="79010-127">For details about how to access XML web services in either mode, see [Accessing XML Web Services in CAO Mode](accessing-xml-web-services-in-cao-mode.md) and [Accessing XML Web Services in WKO Mode](accessing-xml-web-services-in-wko-mode.md).</span></span>

> [!Note]  
> <span data-ttu-id="79010-128">COM+ поддерживает только спецификацию SOAP-RPC, а не спецификацию SOAP-Document.</span><span class="sxs-lookup"><span data-stu-id="79010-128">COM+ supports only the SOAP-RPC specification, not the SOAP-Document specification.</span></span>

 

<span data-ttu-id="79010-129">COM+ упрощает использование веб-служб XML, позволяя использовать существующие приложения COM+ в качестве веб-служб XML в режиме Као, полностью прозрачным образом.</span><span class="sxs-lookup"><span data-stu-id="79010-129">COM+ makes using XML web services especially easy by allowing you to use existing COM+ applications as XML web services in CAO mode in a completely transparent fashion.</span></span> <span data-ttu-id="79010-130">При [экспорте](exporting-a-soap-enabled-application.md) приложения COM+, которое было предоставлено в виде веб-службы XML с сервера, любой клиент, выполняющий [Импорт](importing-a-soap-enabled-application.md) приложения, может прозрачно использовать веб-службу сервера XML при каждом использовании импортированного приложения.</span><span class="sxs-lookup"><span data-stu-id="79010-130">If you [export](exporting-a-soap-enabled-application.md) a COM+ application that has been exposed as an XML web service from your server, any client that [imports](importing-a-soap-enabled-application.md) the application can transparently use the server's XML web service whenever the imported application is used.</span></span> <span data-ttu-id="79010-131">Это средство значительно упрощает преобразование существующих приложений COM+ в веб-службы XML и развертывание этих служб в сети.</span><span class="sxs-lookup"><span data-stu-id="79010-131">This facility makes the conversion of existing COM+ applications to XML web services and the deployment of those services over a network very easy.</span></span>

<span data-ttu-id="79010-132">Использование веб-служб XML имеет несколько уникальных преимуществ по сравнению с альтернативными реализациями удаленных вызовов процедур (RPC), включая следующие.</span><span class="sxs-lookup"><span data-stu-id="79010-132">Using XML web services has several unique advantages over alternative implementations of remote procedure calls (RPC), including the following:</span></span>

-   <span data-ttu-id="79010-133">SOAP — это полноценная межплатформенная реализация RPC, которая повышает совместимость.</span><span class="sxs-lookup"><span data-stu-id="79010-133">SOAP is a true cross-platform RPC implementation, which increases interoperability.</span></span>
-   <span data-ttu-id="79010-134">Веб-службы XML поддерживают методы с входными и выходными параметрами.</span><span class="sxs-lookup"><span data-stu-id="79010-134">XML web services support methods with both input and output parameters.</span></span>
-   <span data-ttu-id="79010-135">Веб-службы XML выполняются через HTTP, что обычно может проникнуть брандмауэры, которые могут блокировать другие реализации RPC.</span><span class="sxs-lookup"><span data-stu-id="79010-135">XML web services run over HTTP, which can usually penetrate firewalls that might block other RPC implementations.</span></span>
-   <span data-ttu-id="79010-136">Если веб-служба XML реализована с помощью COM+, разработчику не нужно писать специальный код. Это чрезвычайное преимущество по сравнению с альтернативными механизмами RPC.</span><span class="sxs-lookup"><span data-stu-id="79010-136">When an XML web service is implemented using COM+, the developer does not have to write any specialized code; this is a tremendous advantage over alternative RPC mechanisms.</span></span>

> [!Note]  
> <span data-ttu-id="79010-137">Веб-службы XML не поддерживают асинхронные или прозрачные вызовы транзакций.</span><span class="sxs-lookup"><span data-stu-id="79010-137">XML web services do not support asynchronous or transparently transactional calls.</span></span> <span data-ttu-id="79010-138">Если эта функция необходима, используйте службу [com+ в очереди компонентов](com--queued-components.md) .</span><span class="sxs-lookup"><span data-stu-id="79010-138">Use the [COM+ Queued Components](com--queued-components.md) service when you require this functionality.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="79010-139">См. также</span><span class="sxs-lookup"><span data-stu-id="79010-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79010-140">Вопросы безопасности службы COM+ SOAP</span><span class="sxs-lookup"><span data-stu-id="79010-140">COM+ SOAP Service Security Considerations</span></span>](com--soap-service-security-considerations.md)
</dt> </dl>

 

 



