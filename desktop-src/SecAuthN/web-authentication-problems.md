---
description: В этом разделе описаны рекомендации по устранению неполадок при использовании API посредника веб-проверки подлинности для веб-страниц.
ms.assetid: 25A024AA-9A70-40A5-BF5E-452FD148D0D2
title: Неполадки при веб-аутентификации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc4611461effd9cbc5546059e71fc8ca3f1f0be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569907"
---
# <a name="web-authentication-problems"></a><span data-ttu-id="e6a35-103">Неполадки при веб-аутентификации</span><span class="sxs-lookup"><span data-stu-id="e6a35-103">Web authentication problems</span></span>

<span data-ttu-id="e6a35-104">В этом разделе описаны рекомендации по устранению неполадок при использовании API посредника веб-проверки подлинности для веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="e6a35-104">This topic describes troubleshooting tips for using the Web Authentication Broker APIs for your web pages.</span></span>

-   [<span data-ttu-id="e6a35-105">Операционные журналы</span><span class="sxs-lookup"><span data-stu-id="e6a35-105">Operational logs</span></span>](#operational-logs)
-   [<span data-ttu-id="e6a35-106">Использование Fiddler с брокером веб-проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="e6a35-106">Using Fiddler with Web Authentication Broker</span></span>](#using-fiddler-with-web-authentication-broker)
-   [<span data-ttu-id="e6a35-107">См. также</span><span class="sxs-lookup"><span data-stu-id="e6a35-107">Related topics</span></span>](#related-topics)

## <a name="operational-logs"></a><span data-ttu-id="e6a35-108">Операционные журналы</span><span class="sxs-lookup"><span data-stu-id="e6a35-108">Operational logs</span></span>

<span data-ttu-id="e6a35-109">Нередко определить, что именно не работает, помогают операционные журналы.</span><span class="sxs-lookup"><span data-stu-id="e6a35-109">Often you can determine what is not working by using the operational logs.</span></span> <span data-ttu-id="e6a35-110">Существует выделенный канал журнала событий Microsoft-Windows- \\ Web AUTH, позволяющий разработчикам веб-сайтов понять, как веб-страницы обрабатываются брокером веб-проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e6a35-110">There is a dedicated event log channel Microsoft-Windows-WebAuth\\Operational that allows website developers to understand how their web pages are being processed by the Web Authentication Broker.</span></span> <span data-ttu-id="e6a35-111">Чтобы включить его, запустите eventvwr.exe и включите операционный журнал в приложении и службах \\ Microsoft \\ Windows веб \\ AUTH.</span><span class="sxs-lookup"><span data-stu-id="e6a35-111">To enable it, launch eventvwr.exe and enable Operational log under the Application and Services\\Microsoft\\Windows\\WebAuth.</span></span> <span data-ttu-id="e6a35-112">Кроме того, брокер веб-проверки подлинности добавляет в строку агента пользователя уникальную строку для идентификации себя на веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="e6a35-112">Also, the Web Authentication Broker appends a unique string to the user agent string to identify itself on the web server.</span></span> <span data-ttu-id="e6a35-113">Это строка "MSAuthHost/1.0".</span><span class="sxs-lookup"><span data-stu-id="e6a35-113">The string is "MSAuthHost/1.0".</span></span> <span data-ttu-id="e6a35-114">Обратите внимание, что номер версии в дальнейшем может меняться, поэтому ваш код не должен зависеть от номера версии.</span><span class="sxs-lookup"><span data-stu-id="e6a35-114">Note that the version number may change in the future, so you should not to depend on that version number in your code.</span></span> <span data-ttu-id="e6a35-115">Ниже приведен пример полной строки агента пользователя.</span><span class="sxs-lookup"><span data-stu-id="e6a35-115">An example of the full user agent string is as follows:</span></span>

`User-Agent: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.2; Win64; x64; Trident/6.0; MSAuthHost/1.0)`

<span data-ttu-id="e6a35-116">Пример использования операционных журналов</span><span class="sxs-lookup"><span data-stu-id="e6a35-116">Example of using operational logs</span></span>

1.  <span data-ttu-id="e6a35-117">Включить Операционные журналы</span><span class="sxs-lookup"><span data-stu-id="e6a35-117">Enable operational logs</span></span>
2.  <span data-ttu-id="e6a35-118">Запуск приложения Contoso Social</span><span class="sxs-lookup"><span data-stu-id="e6a35-118">Run Contoso social application</span></span>![Средство просмотра событий, отображающее операционные журналы WebAuth](images/wab-figure15.png)
3.  <span data-ttu-id="e6a35-120">Созданные записи журналов можно использовать для более подробного понимания поведения брокера веб-проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e6a35-120">The generated logs entries can be used to understand the behavior of Web Authentication Broker in greater detail.</span></span> <span data-ttu-id="e6a35-121">В нашем случае записи могут содержать следующую информацию.</span><span class="sxs-lookup"><span data-stu-id="e6a35-121">In this case, these can include:</span></span>
    -   <span data-ttu-id="e6a35-122">Навигация начата: регистрирует время запуска AuthHost и содержит сведения о URL-адресах начала и окончания навигации.</span><span class="sxs-lookup"><span data-stu-id="e6a35-122">Navigation Start: Logs when the AuthHost is started and contains information about the start and termination URLs.</span></span>
    -   ![Иллюстрация к сведениям о начале навигации](images/wab-figure16.png)
    -   <span data-ttu-id="e6a35-124">Навигация выполнена: регистрирует выполнение загрузки веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="e6a35-124">Navigation Complete: Logs the completion of loading a web page.</span></span>
    -   <span data-ttu-id="e6a35-125">Метатег: регистрирует подробную информацию в случае обнаружения метатега.</span><span class="sxs-lookup"><span data-stu-id="e6a35-125">Meta Tag: Logs when a meta-tag is encountered including the details.</span></span>
    -   <span data-ttu-id="e6a35-126">Завершение навигации: навигация завершена пользователем.</span><span class="sxs-lookup"><span data-stu-id="e6a35-126">Navigation Terminate: Navigation terminated by the user.</span></span>
    -   <span data-ttu-id="e6a35-127">Ошибка навигации: AuthHost обнаруживает ошибку навигации в URL-адресе, включая код состояния HttpStatusCode.</span><span class="sxs-lookup"><span data-stu-id="e6a35-127">Navigation Error: AuthHost encounters a navigation error at a URL including HttpStatusCode.</span></span>
    -   <span data-ttu-id="e6a35-128">Завершение навигации: обнаружен завершающий URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="e6a35-128">Navigation End: Terminating URL is encountered.</span></span>

## <a name="using-fiddler-with-web-authentication-broker"></a><span data-ttu-id="e6a35-129">Использование Fiddler с брокером веб-проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="e6a35-129">Using Fiddler with Web Authentication Broker</span></span>

<span data-ttu-id="e6a35-130">Веб-отладчик Fiddler можно использовать с приложениями Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e6a35-130">The Fiddler web debugger can be used with Windows 8 apps.</span></span>

1.  <span data-ttu-id="e6a35-131">Так как AuthHost работает в собственном контейнере приложения, чтобы предоставить ему возможность частной сети, необходимо настроить раздел реестра: редактор реестра Windows версии 5.00</span><span class="sxs-lookup"><span data-stu-id="e6a35-131">Since the AuthHost runs in its own app container to give it the private network capability, you must set a registry key: Windows Registry Editor Version 5.00</span></span>

    <span data-ttu-id="e6a35-132">**HKey \_ \_** \\  \\  \\  \\  \\ **Параметры выполнения файлов образа** Microsoft Windows NT CurrentVersion по локальному компьютеру \\ **authhost.exe** \\ **енаблеприватенетворк** = 00000001</span><span class="sxs-lookup"><span data-stu-id="e6a35-132">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Image File Execution Options**\\**authhost.exe**\\**EnablePrivateNetwork** = 00000001</span></span><dl> <dt>

                     Data type
</dt> <dd>                     <span data-ttu-id="e6a35-133">DWORD</span><span class="sxs-lookup"><span data-stu-id="e6a35-133">DWORD</span></span></dd> </dl>

2.  <span data-ttu-id="e6a35-134">Добавьте правило для AuthHost, поскольку эта служба создает исходящий трафик.</span><span class="sxs-lookup"><span data-stu-id="e6a35-134">Add a rule for the AuthHost as this is what is generating the outbound traffic.</span></span>
    ```cmd
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.a.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
    D:\Windows\System32>CheckNetIsolation.exe LoopbackExempt -s
    List Loopback Exempted AppContainers
    [1] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
        SID:  S-1-15-2-1973105767-3975693666-32999980-3747492175-1074076486-3102532000-500629349
    [2] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
        SID:  S-1-15-2-166260-4150837609-3669066492-3071230600-3743290616-3683681078-2492089544
    [3] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.a.p_8wekyb3d8bbwe
        SID:  S-1-15-2-3506084497-1208594716-3384433646-2514033508-1838198150-1980605558-3480344935
    ```

    

3.  <span data-ttu-id="e6a35-135">Добавьте правило брандмауэра для входящего трафика в Fiddler.</span><span class="sxs-lookup"><span data-stu-id="e6a35-135">Add a firewall rule for incoming traffic to Fiddler.</span></span>

<span data-ttu-id="e6a35-136">Дополнительные сведения см. [в блоге использование веб-отладчика Fiddler с приложениями для Магазина Windows](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).</span><span class="sxs-lookup"><span data-stu-id="e6a35-136">For more information, see [Blog on using Fiddler web debugger with Windows Store apps](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6a35-137">См. также</span><span class="sxs-lookup"><span data-stu-id="e6a35-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6a35-138">Рекомендации по разработке веб-страниц</span><span class="sxs-lookup"><span data-stu-id="e6a35-138">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="e6a35-139">Вопросы и ответы по брокеру веб-проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="e6a35-139">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.md)
</dt> <dt>

[<span data-ttu-id="e6a35-140">Пример приложения SDK брокера веб-проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="e6a35-140">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="e6a35-141">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="e6a35-141">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041)
</dt> </dl>

 

 
