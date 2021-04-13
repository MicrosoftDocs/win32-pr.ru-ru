---
title: Ведение журнала клиента (пакет SDK для формата Windows Media 11)
description: Ведение журнала клиента
ms.assetid: 3e0d0fea-4370-41f8-b461-73a37de8d8bc
keywords:
- Пакет SDK для Windows Media Format, ведение журнала клиента
- Windows Media Format SDK, ведение журнала
- Расширенный формат систем (ASF), ведение журнала клиента
- ASF (Расширенный системный формат), ведение журнала клиента
- Расширенный формат систем (ASF), ведение журнала
- ASF (Расширенный системный формат), ведение журнала
- ведение журнала клиента
- Регистрация клиентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856f2df4c2377b94edc40574c3e2efcced34aa81
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134863"
---
# <a name="client-logging-windows-media-format-11-sdk"></a><span data-ttu-id="e7c46-111">Ведение журнала клиента (пакет SDK для формата Windows Media 11)</span><span class="sxs-lookup"><span data-stu-id="e7c46-111">Client Logging (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="e7c46-112">Когда объект чтения считывает данные с сервера, он отправляет данные журнала на сервер.</span><span class="sxs-lookup"><span data-stu-id="e7c46-112">When the reader object reads data from a server, it sends logging information to the server.</span></span> <span data-ttu-id="e7c46-113">Поставщики содержимого обычно используют эти сведения для измерения качества обслуживания, создания сведений о выставлении счетов или объявления.</span><span class="sxs-lookup"><span data-stu-id="e7c46-113">Content providers typically use this information to measure quality of service, generate billing information, or track advertising.</span></span> <span data-ttu-id="e7c46-114">Данные ведения журнала не содержат персональных данных.</span><span class="sxs-lookup"><span data-stu-id="e7c46-114">The logging information contains no personal data.</span></span>

<span data-ttu-id="e7c46-115">Приложение может указать некоторую информацию, которая заносится в журнал, вызвав метод [**ивмреадерадванцед:: SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) для объекта Reader.</span><span class="sxs-lookup"><span data-stu-id="e7c46-115">The application can specify some of the information that is logged, by calling the [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) method on the reader object.</span></span> <span data-ttu-id="e7c46-116">Например, можно указать строку агента пользователя, имя приложения проигрывателя или веб-страницу, на которой размещен проигрыватель.</span><span class="sxs-lookup"><span data-stu-id="e7c46-116">For example, you can specify the user-agent string, the name of the player application, or the Web page that hosts the player.</span></span>

<span data-ttu-id="e7c46-117">Данные журнала включают идентификатор GUID, который идентифицирует сеанс.</span><span class="sxs-lookup"><span data-stu-id="e7c46-117">The logging information includes a GUID that identifies the session.</span></span> <span data-ttu-id="e7c46-118">По умолчанию средство чтения создает идентификатор анонимного сеанса.</span><span class="sxs-lookup"><span data-stu-id="e7c46-118">By default, the reader generates an anonymous session ID.</span></span> <span data-ttu-id="e7c46-119">При необходимости модуль чтения может вместо этого отправить идентификатор, однозначно определяющий текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="e7c46-119">Optionally, the reader can instead send an ID that uniquely identifies the current user.</span></span> <span data-ttu-id="e7c46-120">Чтобы включить эту функцию, вызовите метод [**IWMReaderAdvanced2:: сетлогклиентид**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="e7c46-120">To enable this feature, call the [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) method with the value **TRUE**.</span></span>

<span data-ttu-id="e7c46-121">Можно настроить объект модуля чтения для отправки сведений о ведении журнала на другой сервер в дополнение к исходному серверу.</span><span class="sxs-lookup"><span data-stu-id="e7c46-121">You can configure the reader object to send the logging information to another server, in addition to the originating server.</span></span> <span data-ttu-id="e7c46-122">Для этого вызовите метод [**ивмреадернетворкконфиг:: аддлоггингурл**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) с URL-адресом сервера.</span><span class="sxs-lookup"><span data-stu-id="e7c46-122">To do so, call the [**IWMReaderNetworkConfig::AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) method with the URL of the server.</span></span> <span data-ttu-id="e7c46-123">Этот URL-адрес должен указывать на скрипт или исполняемый файл, который может выполнять запросы HTTP GET и POST.</span><span class="sxs-lookup"><span data-stu-id="e7c46-123">This URL should point to a script or executable that can handle HTTP GET and POST requests.</span></span> <span data-ttu-id="e7c46-124">Для получения данных журнала можно использовать агент многоадресной рассылки и агента объявления журналов (wmsiislog.dll) или написать пользовательский скрипт ASP или CGI.</span><span class="sxs-lookup"><span data-stu-id="e7c46-124">You can use the Multicast and Logging Advertisement Agent (wmsiislog.dll), or you can write a custom ASP or CGI script to receive the log data.</span></span>

> [!Note]  
> <span data-ttu-id="e7c46-125">Те же функциональные возможности можно получить, создав список воспроизведения на стороне сервера с атрибутом **логурл** .</span><span class="sxs-lookup"><span data-stu-id="e7c46-125">You can get the same functionality by creating a server-side playlist with a **logURL** attribute.</span></span>

 

<span data-ttu-id="e7c46-126">Когда объект модуля чтения отправляет журнал, он выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="e7c46-126">When the reader object sends the log, it does the following:</span></span>

1.  <span data-ttu-id="e7c46-127">Отправляет на сервер пустой запрос GET.</span><span class="sxs-lookup"><span data-stu-id="e7c46-127">Sends an empty GET request to the server.</span></span>
2.  <span data-ttu-id="e7c46-128">Анализирует ответ сервера на наличие одной из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="e7c46-128">Parses the server response for one of the following strings:</span></span>
    -   `<body><h1>NetShow ISAPI Log Dll</h1>`
    -   <span data-ttu-id="e7c46-129">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` где "0.0.0.0" — любой допустимый номер версии.</span><span class="sxs-lookup"><span data-stu-id="e7c46-129">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` where "0.0.0.0" is any valid version number.</span></span>
3.  <span data-ttu-id="e7c46-130">Отправляет запрос POST со сведениями журнала.</span><span class="sxs-lookup"><span data-stu-id="e7c46-130">Sends a POST request with the log information.</span></span>

<span data-ttu-id="e7c46-131">В следующем коде показан пример скрипта ASP, который получает сведения о ведении журнала и записывает их в файл:</span><span class="sxs-lookup"><span data-stu-id="e7c46-131">The following code shows an example ASP script that receives the logging information and writes it to a file:</span></span>


```
<html>
<body>
<h1>WMS ISAPI Log Dll/9.00.00.00.00</h1>
<%@ Language=VBScript %>
<%
  Dim temp, i, post, file, fso

  ' Convert the binary data to a string.
  For i = 1 To Request.TotalBytes
    temp = Request.BinaryRead(1)
    pose = pose & Chr(AscB(temp))
  Next

  Set fso = createobject("Scripting.FileSystemObject")
  Set file = fso.OpenTextFile("C:\log.txt", 8, TRUE)

  file.writeline Now
  file.writeline post
  file.writeBlankLines 2 
%>
</body>
</html>
```



<span data-ttu-id="e7c46-132">Для получения сведений о ведении журнала можно указать несколько серверов. просто вызовите **аддлоггингурл** один раз с каждым URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="e7c46-132">You can specify multiple servers to receive logging information; just call **AddLoggingUrl** once with each URL.</span></span> <span data-ttu-id="e7c46-133">Чтобы очистить список серверов, которые получают журналы, вызовите метод [**ивмреадернетворкконфиг:: ресетлоггингурллист**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) .</span><span class="sxs-lookup"><span data-stu-id="e7c46-133">To clear the list of servers that receive logs, call the [**IWMReaderNetworkConfig::ResetLoggingUrlList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7c46-134">См. также</span><span class="sxs-lookup"><span data-stu-id="e7c46-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7c46-135">**Реализация функций сети**</span><span class="sxs-lookup"><span data-stu-id="e7c46-135">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> <dt>

[<span data-ttu-id="e7c46-136">**Интерфейс Ивмреадерадванцед**</span><span class="sxs-lookup"><span data-stu-id="e7c46-136">**IWMReaderAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)
</dt> <dt>

[<span data-ttu-id="e7c46-137">**Интерфейс IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="e7c46-137">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




