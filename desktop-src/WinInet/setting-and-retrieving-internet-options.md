---
title: Настройка и получение свойств браузера
description: В этом разделе описано, как задать и получить свойства Интернета с помощью функций Интернетсетоптион и Интернеткуерйоптион.
ms.assetid: b596a4a9-c34a-402a-af76-b930fe5f0901
keywords:
- Настройка и получение свойств браузера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418bf21620cf7b7c4426844c95a39ef1fde04e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890953"
---
# <a name="setting-and-retrieving-internet-options"></a><span data-ttu-id="da98d-104">Настройка и получение свойств браузера</span><span class="sxs-lookup"><span data-stu-id="da98d-104">Setting and Retrieving Internet Options</span></span>

<span data-ttu-id="da98d-105">В этом разделе описано, как задать и получить свойства Интернета с помощью функций [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) и [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) .</span><span class="sxs-lookup"><span data-stu-id="da98d-105">This topic describes how to set and retrieve Internet options using the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) functions.</span></span>

<span data-ttu-id="da98d-106">Свойства Интернета можно задать для или получить с помощью указанного обработчика [**хинтернет**](appendix-a-hinternet-handles.md) или текущих параметров в Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="da98d-106">Internet options can be set on, or retrieved from, a specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle or the current settings in Microsoft Internet Explorer.</span></span>

-   [<span data-ttu-id="da98d-107">Шаги реализации</span><span class="sxs-lookup"><span data-stu-id="da98d-107">Implementation Steps</span></span>](#implementation-steps)
    -   [<span data-ttu-id="da98d-108">Выбор свойств браузера</span><span class="sxs-lookup"><span data-stu-id="da98d-108">Choosing Internet Options</span></span>](#choosing-internet-options)
    -   [<span data-ttu-id="da98d-109">Выбор маркера ХИНТЕРНЕТ</span><span class="sxs-lookup"><span data-stu-id="da98d-109">Choosing the HINTERNET Handle</span></span>](#choosing-the-hinternet-handle)
    -   [<span data-ttu-id="da98d-110">Установка или получение параметров</span><span class="sxs-lookup"><span data-stu-id="da98d-110">Setting or Retrieving the Options</span></span>](#setting-or-retrieving-the-options)
-   [<span data-ttu-id="da98d-111">Область действия маркера ХИНТЕРНЕТ</span><span class="sxs-lookup"><span data-stu-id="da98d-111">Scope of HINTERNET Handle</span></span>](#scope-of-hinternet-handle)
-   [<span data-ttu-id="da98d-112">Настройка отдельных параметров</span><span class="sxs-lookup"><span data-stu-id="da98d-112">Setting Individual Options</span></span>](#setting-individual-options)
-   [<span data-ttu-id="da98d-113">Получение отдельных параметров</span><span class="sxs-lookup"><span data-stu-id="da98d-113">Retrieving Individual Options</span></span>](#retrieving-individual-options)
    -   [<span data-ttu-id="da98d-114">Полный пример</span><span class="sxs-lookup"><span data-stu-id="da98d-114">Complete Sample</span></span>](#complete-sample)
-   [<span data-ttu-id="da98d-115">Настройка параметров соединения</span><span class="sxs-lookup"><span data-stu-id="da98d-115">Setting Connection Options</span></span>](#setting-connection-options)
-   [<span data-ttu-id="da98d-116">Получение параметров соединения</span><span class="sxs-lookup"><span data-stu-id="da98d-116">Retrieving Connection Options</span></span>](#retrieving-connection-options)
-   [<span data-ttu-id="da98d-117">См. также</span><span class="sxs-lookup"><span data-stu-id="da98d-117">Related topics</span></span>](#related-topics)

## <a name="implementation-steps"></a><span data-ttu-id="da98d-118">Шаги реализации</span><span class="sxs-lookup"><span data-stu-id="da98d-118">Implementation Steps</span></span>

<span data-ttu-id="da98d-119">Чтобы задать или получить свойства Интернета, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="da98d-119">To set or retrieve Internet options complete the following:</span></span>

-   [<span data-ttu-id="da98d-120">Выбор свойств браузера</span><span class="sxs-lookup"><span data-stu-id="da98d-120">Choosing Internet Options</span></span>](#choosing-internet-options)
-   [<span data-ttu-id="da98d-121">Выбор маркера ХИНТЕРНЕТ</span><span class="sxs-lookup"><span data-stu-id="da98d-121">Choosing the HINTERNET Handle</span></span>](#choosing-the-hinternet-handle)
-   [<span data-ttu-id="da98d-122">Установка или получение параметров</span><span class="sxs-lookup"><span data-stu-id="da98d-122">Setting or Retrieving the Options</span></span>](#setting-or-retrieving-the-options)

### <a name="choosing-internet-options"></a><span data-ttu-id="da98d-123">Выбор свойств браузера</span><span class="sxs-lookup"><span data-stu-id="da98d-123">Choosing Internet Options</span></span>

<span data-ttu-id="da98d-124">Так как существует много параметров Интернета, важно выбрать правильный вариант.</span><span class="sxs-lookup"><span data-stu-id="da98d-124">Because there are so many Internet options, choosing the right options is important.</span></span> <span data-ttu-id="da98d-125">Многие свойства Интернета влияют на поведение функций WinINet и Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="da98d-125">Many Internet options affect the behavior of the WinINet functions and Internet Explorer:</span></span>

<span data-ttu-id="da98d-126">Например, администратор может сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="da98d-126">For example, you can:</span></span>

-   <span data-ttu-id="da98d-127">Обрабатывайте обычную проверку подлинности сервера и прокси, задав имена пользователей и пароли.</span><span class="sxs-lookup"><span data-stu-id="da98d-127">Handle basic server and proxy authentication by setting user names and passwords.</span></span>
-   <span data-ttu-id="da98d-128">Задайте или получите строку агента пользователя, используемую серверами для определения функций клиентского приложения или браузера.</span><span class="sxs-lookup"><span data-stu-id="da98d-128">Set or retrieve the user agent string used by servers to identify the features of the client application or browser.</span></span>
-   <span data-ttu-id="da98d-129">Получите тип маркера для указанного обработчика [**хинтернет**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="da98d-129">Retrieve the handle type of the specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>

<span data-ttu-id="da98d-130">Дополнительные сведения и список свойств Интернета см. в разделе [**Флаги**](option-flags.md)параметров.</span><span class="sxs-lookup"><span data-stu-id="da98d-130">For more information and a list of the Internet options, see [**Option Flags**](option-flags.md).</span></span>

<span data-ttu-id="da98d-131">В Internet Explorer 5 и более поздних версиях некоторые параметры могут быть заданы или получены из конкретного подключения к Интернету с помощью [**\_ \_ \_ \_ списка параметров «через Интернет на подключение»**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) и « [**\_ в сети \_ \_ » для каждой**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) структуры.</span><span class="sxs-lookup"><span data-stu-id="da98d-131">In Internet Explorer 5 and later, some options can be set or retrieved from a specific Internet connection using the [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) and [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span> <span data-ttu-id="da98d-132">Дополнительные сведения и список параметров, которые можно задать или получить из конкретного подключения к Интернету, см. в разделе **двоптионс** элемента структуры [**Internet \_ per \_ conn \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .</span><span class="sxs-lookup"><span data-stu-id="da98d-132">For more information and a list of options that can be set or retrieved from a specific Internet connection, see the **dwOptions** member of the [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structure.</span></span>

### <a name="choosing-the-hinternet-handle"></a><span data-ttu-id="da98d-133">Выбор маркера ХИНТЕРНЕТ</span><span class="sxs-lookup"><span data-stu-id="da98d-133">Choosing the HINTERNET Handle</span></span>

<span data-ttu-id="da98d-134">Обработчик [**хинтернет**](appendix-a-hinternet-handles.md) , используемый для задания или получения свойств Интернета, определяет область действия операции.</span><span class="sxs-lookup"><span data-stu-id="da98d-134">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle used to set or retrieve Internet options determines the scope of the operation.</span></span> <span data-ttu-id="da98d-135">Все дескрипторы, созданные с помощью этого дескриптора, наследуют параметры, заданные для этого дескриптора.</span><span class="sxs-lookup"><span data-stu-id="da98d-135">All the handles created through this handle will inherit the options set on this handle.</span></span>

<span data-ttu-id="da98d-136">Например, клиентские приложения, которым требуется прокси-сервер с проверкой подлинности, возможно, не занимают имя пользователя и пароль прокси-сервера каждый раз, когда приложение пытается получить доступ к ресурсу в Интернете.</span><span class="sxs-lookup"><span data-stu-id="da98d-136">For example, client applications that require a proxy with authentication, probably do not require setting the proxy user name and password every time the application attempts to access an Internet resource.</span></span> <span data-ttu-id="da98d-137">Если все запросы к определенному соединению обрабатываются одним и тем же прокси-сервером, то задание имени и пароля пользователя прокси-сервера для типа соединения [**хинтернет**](appendix-a-hinternet-handles.md) Handle, то есть маркера, созданного вызовом [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), позволит всем вызовам, производным от этого **хинтернет** , использовать одно и то же имя пользователя и пароль прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="da98d-137">If all requests on a given connection are handled by the same proxy, setting the proxy user name and password on a connection type [**HINTERNET**](appendix-a-hinternet-handles.md) handle, that is, a handle created by a call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), would allow any calls derived from this **HINTERNET** handle to use the same proxy user name and password.</span></span> <span data-ttu-id="da98d-138">Задание имени и пароля пользователя прокси-сервера при каждом создании обработчика **хинтернет** с помощью [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) потребует дополнительных и ненужных затрат.</span><span class="sxs-lookup"><span data-stu-id="da98d-138">Setting the proxy user name and password every time an **HINTERNET** handle is created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) would require extra and unnecessary overhead.</span></span> <span data-ttu-id="da98d-139">Имейте в виду, что если приложение использует прокси-сервер, требующий проверки подлинности, он должен задать учетные данные прокси-сервера для каждого нового соединения.</span><span class="sxs-lookup"><span data-stu-id="da98d-139">Be aware that if the application uses a proxy that requires authentication, it should set the proxy credentials on every new connection.</span></span>

### <a name="setting-or-retrieving-the-options"></a><span data-ttu-id="da98d-140">Установка или получение параметров</span><span class="sxs-lookup"><span data-stu-id="da98d-140">Setting or Retrieving the Options</span></span>

<span data-ttu-id="da98d-141">Когда вы определяете, какие свойства Интернета и [**хинтернет**](appendix-a-hinternet-handles.md) использовать, извлеките эти свойства Интернета.</span><span class="sxs-lookup"><span data-stu-id="da98d-141">When you have determined what Internet options and [**HINTERNET**](appendix-a-hinternet-handles.md) handle to use, retrieve those Internet options.</span></span> <span data-ttu-id="da98d-142">Чтобы задать или получить параметры, вызовите либо [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) , либо [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="da98d-142">To set or retrieve options, call either [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

## <a name="scope-of-hinternet-handle"></a><span data-ttu-id="da98d-143">Область действия маркера ХИНТЕРНЕТ</span><span class="sxs-lookup"><span data-stu-id="da98d-143">Scope of HINTERNET Handle</span></span>

<span data-ttu-id="da98d-144">Обработчик [**хинтернет**](appendix-a-hinternet-handles.md) , используемый для задания или получения свойств Интернета, определяет действия, для которых параметры являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="da98d-144">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle used to set or retrieve Internet options determines the actions for which the options are valid.</span></span>

<span data-ttu-id="da98d-145">Эти маркеры имеют три уровня:</span><span class="sxs-lookup"><span data-stu-id="da98d-145">These handles have three levels:</span></span>

-   <span data-ttu-id="da98d-146">Корневой обработчик [**хинтернет**](appendix-a-hinternet-handles.md) (созданный вызовом [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena)) будет содержать все свойства Интернета, влияющие на этот экземпляр WinInet.</span><span class="sxs-lookup"><span data-stu-id="da98d-146">The root [**HINTERNET**](appendix-a-hinternet-handles.md) handle (created by a call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)) would contain all the Internet options that affect this instance of WinINet.</span></span>
-   <span data-ttu-id="da98d-147">Дескрипторы [**хинтернет**](appendix-a-hinternet-handles.md) , которые подключаются к серверу (созданному путем вызова [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta));</span><span class="sxs-lookup"><span data-stu-id="da98d-147">[**HINTERNET**](appendix-a-hinternet-handles.md) handles that connect to a server (created by a call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta))</span></span>
-   <span data-ttu-id="da98d-148">Дескрипторы [**хинтернет**](appendix-a-hinternet-handles.md) , связанные с ресурсом или перечислением ресурсов на определенном сервере.</span><span class="sxs-lookup"><span data-stu-id="da98d-148">[**HINTERNET**](appendix-a-hinternet-handles.md) handles associated with a resource or enumeration of resources on a particular server.</span></span>

<span data-ttu-id="da98d-149">В дополнение к различным дескрипторам [**хинтернет**](appendix-a-hinternet-handles.md) , приложение может также использовать **null** для установки или получения значений по умолчанию параметров Интернета, используемых Internet Explorer и функциями WinInet.</span><span class="sxs-lookup"><span data-stu-id="da98d-149">In addition to the various [**HINTERNET**](appendix-a-hinternet-handles.md) handles, an application can also use **NULL** to set or retrieve the default values of the Internet options used by Internet Explorer and the WinINet functions.</span></span> <span data-ttu-id="da98d-150">При задании свойств Интернета при использовании значения **null** в качестве маркера изменяются значения параметров по умолчанию, которые в настоящее время хранятся в реестре.</span><span class="sxs-lookup"><span data-stu-id="da98d-150">Setting Internet options when using **NULL** as the handle changes the default values of the options, which are currently stored in the registry.</span></span> <span data-ttu-id="da98d-151">Клиентские приложения не должны использовать функции реестра для изменения значений свойств обозревателя по умолчанию, так как в будущем можно изменить способ хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="da98d-151">Client applications should not use registry functions to change the default values of the Internet options, because the implementation of how the options are stored can be altered in the future.</span></span>

<span data-ttu-id="da98d-152">В следующей таблице перечислены типы дескрипторов [**хинтернет**](appendix-a-hinternet-handles.md) и области связанных с ними параметров Интернета.</span><span class="sxs-lookup"><span data-stu-id="da98d-152">The following table lists the type of [**HINTERNET**](appendix-a-hinternet-handles.md) handles and the scope of the Internet options associated with them.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="da98d-153">Тип обработчика</span><span class="sxs-lookup"><span data-stu-id="da98d-153">Handle Type</span></span></th>
<th><span data-ttu-id="da98d-154">Область</span><span class="sxs-lookup"><span data-stu-id="da98d-154">Scope</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="da98d-155"><strong>NULL</strong></span><span class="sxs-lookup"><span data-stu-id="da98d-155"><strong>NULL</strong></span></span></td>
<td><span data-ttu-id="da98d-156">Параметры по умолчанию для Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="da98d-156">The default option settings for Internet Explorer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da98d-157">INTERNET_HANDLE_TYPE_CONNECT_FTP</span><span class="sxs-lookup"><span data-stu-id="da98d-157">INTERNET_HANDLE_TYPE_CONNECT_FTP</span></span></td>
<td><span data-ttu-id="da98d-158">Параметры для этого соединения с FTP-сервером.</span><span class="sxs-lookup"><span data-stu-id="da98d-158">The option settings for this connection to an FTP server.</span></span> <span data-ttu-id="da98d-159">Эти параметры влияют на любые операции, инициированные этим обработчиком <a href="appendix-a-hinternet-handles.md"><strong>хинтернет</strong></a> , такие как файлы для загрузки.</span><span class="sxs-lookup"><span data-stu-id="da98d-159">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da98d-160">INTERNET_HANDLE_TYPE_CONNECT_GOPHER</span><span class="sxs-lookup"><span data-stu-id="da98d-160">INTERNET_HANDLE_TYPE_CONNECT_GOPHER</span></span></td>
<td><span data-ttu-id="da98d-161">Параметры для этого подключения к серверу Gopher.</span><span class="sxs-lookup"><span data-stu-id="da98d-161">The option settings for this connection to a Gopher server.</span></span> <span data-ttu-id="da98d-162">Эти параметры влияют на любые операции, инициированные этим обработчиком <a href="appendix-a-hinternet-handles.md"><strong>хинтернет</strong></a> , такие как файлы для загрузки.</span><span class="sxs-lookup"><span data-stu-id="da98d-162">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="da98d-163">Windows XP и Windows Server 2003 R2 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="da98d-163">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da98d-164">INTERNET_HANDLE_TYPE_CONNECT_HTTP</span><span class="sxs-lookup"><span data-stu-id="da98d-164">INTERNET_HANDLE_TYPE_CONNECT_HTTP</span></span></td>
<td><span data-ttu-id="da98d-165">Параметры для этого соединения с HTTP-сервером.</span><span class="sxs-lookup"><span data-stu-id="da98d-165">The option settings for this connection to an HTTP server.</span></span> <span data-ttu-id="da98d-166">Эти параметры влияют на любые операции, инициированные этим обработчиком <a href="appendix-a-hinternet-handles.md"><strong>хинтернет</strong></a> , такие как файлы для загрузки.</span><span class="sxs-lookup"><span data-stu-id="da98d-166">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da98d-167">INTERNET_HANDLE_TYPE_FILE_REQUEST</span><span class="sxs-lookup"><span data-stu-id="da98d-167">INTERNET_HANDLE_TYPE_FILE_REQUEST</span></span></td>
<td><span data-ttu-id="da98d-168">Параметры, связанные с этим запросом файла.</span><span class="sxs-lookup"><span data-stu-id="da98d-168">The option settings associated with this file request.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da98d-169">INTERNET_HANDLE_TYPE_FTP_FILE</span><span class="sxs-lookup"><span data-stu-id="da98d-169">INTERNET_HANDLE_TYPE_FTP_FILE</span></span></td>
<td><span data-ttu-id="da98d-170">Параметры, связанные с этим скачиванием FTP-ресурса.</span><span class="sxs-lookup"><span data-stu-id="da98d-170">The option settings associated with this FTP resource download.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da98d-171">INTERNET_HANDLE_TYPE_FTP_FILE_HTML</span><span class="sxs-lookup"><span data-stu-id="da98d-171">INTERNET_HANDLE_TYPE_FTP_FILE_HTML</span></span></td>
<td><span data-ttu-id="da98d-172">Параметры, связанные с этим FTP-ресурсом, загружаются в формате HTML.</span><span class="sxs-lookup"><span data-stu-id="da98d-172">The option settings associated with this FTP resource download formatted in HTML.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da98d-173">INTERNET_HANDLE_TYPE_FTP_FIND</span><span class="sxs-lookup"><span data-stu-id="da98d-173">INTERNET_HANDLE_TYPE_FTP_FIND</span></span></td>
<td><span data-ttu-id="da98d-174">Параметры, связанные с этим поиском файлов на FTP-сервере.</span><span class="sxs-lookup"><span data-stu-id="da98d-174">The option settings associated with this search of files on an FTP server.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da98d-175">INTERNET_HANDLE_TYPE_FTP_FIND_HTML</span><span class="sxs-lookup"><span data-stu-id="da98d-175">INTERNET_HANDLE_TYPE_FTP_FIND_HTML</span></span></td>
<td><span data-ttu-id="da98d-176">Параметры, связанные с этим поиском файлов на FTP-сервере, отформатированном в формате HTML.</span><span class="sxs-lookup"><span data-stu-id="da98d-176">The option settings associated with this search of files on an FTP server formatted in HTML.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da98d-177">INTERNET_HANDLE_TYPE_GOPHER_FILE</span><span class="sxs-lookup"><span data-stu-id="da98d-177">INTERNET_HANDLE_TYPE_GOPHER_FILE</span></span></td>
<td><span data-ttu-id="da98d-178">Параметры, связанные с этим скачиванием ресурса Gopher.</span><span class="sxs-lookup"><span data-stu-id="da98d-178">The option settings associated with this Gopher resource download.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="da98d-179">Windows XP и Windows Server 2003 R2 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="da98d-179">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da98d-180">INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML</span><span class="sxs-lookup"><span data-stu-id="da98d-180">INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML</span></span></td>
<td><span data-ttu-id="da98d-181">Параметры, связанные с этим ресурсом Gopher, загружаются в формате HTML.</span><span class="sxs-lookup"><span data-stu-id="da98d-181">The option settings associated with this Gopher resource download formatted in HTML.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="da98d-182">Windows XP и Windows Server 2003 R2 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="da98d-182">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da98d-183">INTERNET_HANDLE_TYPE_GOPHER_FIND</span><span class="sxs-lookup"><span data-stu-id="da98d-183">INTERNET_HANDLE_TYPE_GOPHER_FIND</span></span></td>
<td><span data-ttu-id="da98d-184">Параметры, связанные с этим поиском файлов на сервере Gopher.</span><span class="sxs-lookup"><span data-stu-id="da98d-184">The option settings associated with this search of files on an Gopher server.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="da98d-185">Windows XP и Windows Server 2003 R2 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="da98d-185">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da98d-186">INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML</span><span class="sxs-lookup"><span data-stu-id="da98d-186">INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML</span></span></td>
<td><span data-ttu-id="da98d-187">Параметры, связанные с этим поиском файлов на сервере Gopher в формате HTML.</span><span class="sxs-lookup"><span data-stu-id="da98d-187">The option settings associated with this search of files on an Gopher server formatted in HTML.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="da98d-188">Windows XP и Windows Server 2003 R2 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="da98d-188">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da98d-189">INTERNET_HANDLE_TYPE_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="da98d-189">INTERNET_HANDLE_TYPE_HTTP_REQUEST</span></span></td>
<td><span data-ttu-id="da98d-190">Параметры, связанные с этим HTTP-запросом.</span><span class="sxs-lookup"><span data-stu-id="da98d-190">The option settings associated with this HTTP request.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da98d-191">INTERNET_HANDLE_TYPE_INTERNET</span><span class="sxs-lookup"><span data-stu-id="da98d-191">INTERNET_HANDLE_TYPE_INTERNET</span></span></td>
<td><span data-ttu-id="da98d-192">Параметры, связанные с этим экземпляром функций WinINet.</span><span class="sxs-lookup"><span data-stu-id="da98d-192">The option settings associated with this instance of the WinINet functions.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="setting-individual-options"></a><span data-ttu-id="da98d-193">Настройка отдельных параметров</span><span class="sxs-lookup"><span data-stu-id="da98d-193">Setting Individual Options</span></span>

<span data-ttu-id="da98d-194">После определения параметров Интернета, которые требуется задать, и области, на которую эти параметры влияют, Настройка параметров Интернета не является сложной.</span><span class="sxs-lookup"><span data-stu-id="da98d-194">After determining the Internet options you want to set and the scope you want affected by these options, setting Internet options is not complicated.</span></span> <span data-ttu-id="da98d-195">Все, что нужно сделать, — это вызвать функцию [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) с требуемым маркером [**хинтернет**](appendix-a-hinternet-handles.md) , флагом параметра Internet и буфером, который содержит нужные сведения.</span><span class="sxs-lookup"><span data-stu-id="da98d-195">All you would need to do is call the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function with desired [**HINTERNET**](appendix-a-hinternet-handles.md) handle, Internet option flag, and a buffer that contains the information you want set.</span></span>

<span data-ttu-id="da98d-196">В следующем примере показано, как задать имя пользователя и пароль учетной записи-посредника для указанного обработчика [**хинтернет**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="da98d-196">The following example shows how to set the proxy user name and password on a specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>


```C++
// strUsername is a string buffer of cchMax characters or less.
// It contains the proxy user name.
size_t cchMax = 80;
size_t cchUserLength, cchPasswordLength;
HRESULT hr = StringCchLength(strUsername, cchMax, &cchUserLength);

if (SUCCEEDED(hr))
{
   // hOpen is the HINTERNET handle created by InternetConnect.
   InternetSetOption(hConnect, INTERNET_OPTION_PROXY_USERNAME,
      strUsername, DWORD(cchUserLength)+1);
}
else
{
   // Insert error handling code here.
}

// strPassword is the string buffer that contains the proxy password.
hr = StringCchLength(strPassword, cchMax, &cchPasswordLength);

InternetSetOption(hOpen, INTERNET_OPTION_PROXY_PASSWORD,
    strPassword, DWORD(cchPasswordLength)+1);
```



## <a name="retrieving-individual-options"></a><span data-ttu-id="da98d-197">Получение отдельных параметров</span><span class="sxs-lookup"><span data-stu-id="da98d-197">Retrieving Individual Options</span></span>

<span data-ttu-id="da98d-198">Свойства браузера можно получить с помощью функции [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) .</span><span class="sxs-lookup"><span data-stu-id="da98d-198">Internet options can be retrieved using the [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) function.</span></span> <span data-ttu-id="da98d-199">Чтобы получить свойства браузера, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="da98d-199">To retrieve Internet options:</span></span>

1.  <span data-ttu-id="da98d-200">Определите размер буфера, необходимый для получения сведений о параметрах Интернета.</span><span class="sxs-lookup"><span data-stu-id="da98d-200">Determine the buffer size necessary to retrieve the Internet option information.</span></span>

    <span data-ttu-id="da98d-201">Размер буфера можно определить с помощью **значения NULL** для адреса буфера и передачи ему нулевого размера буфера.</span><span class="sxs-lookup"><span data-stu-id="da98d-201">The buffer size can be determined by using **NULL** for the address of the buffer and passing it a buffer size of zero.</span></span>

    ```C++
    DWORD dwSize;
    InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);
    ```

    

    <span data-ttu-id="da98d-202">Значение, возвращаемое функцией [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) , — это объем памяти, необходимый для получения сведений в байтах.</span><span class="sxs-lookup"><span data-stu-id="da98d-202">The value returned by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) is the amount of memory required to retrieve the information, in bytes.</span></span>

2.  <span data-ttu-id="da98d-203">Выделение памяти для буфера.</span><span class="sxs-lookup"><span data-stu-id="da98d-203">Allocate a memory for the buffer.</span></span>
    ```C++
    char *lpszData;
    lpszData = new char[dwSize];
    ```

    

3.  <span data-ttu-id="da98d-204">Получение данных.</span><span class="sxs-lookup"><span data-stu-id="da98d-204">Retrieve the data.</span></span>
    ```C++
    InternetQueryOption( NULL, 
                         INTERNET_OPTION_USER_AGENT,
                         lpszData, &dwSize );
    ```

    

4.  <span data-ttu-id="da98d-205">Освободите память.</span><span class="sxs-lookup"><span data-stu-id="da98d-205">Free the memory.</span></span>
    ```C++
    delete [] lpszData;
    ```

    

### <a name="complete-sample"></a><span data-ttu-id="da98d-206">Полный пример</span><span class="sxs-lookup"><span data-stu-id="da98d-206">Complete Sample</span></span>

<span data-ttu-id="da98d-207">Ниже приведен полный пример, используемый в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="da98d-207">The following is the complete sample used in the previous section.</span></span> <span data-ttu-id="da98d-208">В этом примере показано, как получить строку агента пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="da98d-208">This sample shows how to retrieve the default user agent string.</span></span>


```C++
// This call determines the required buffer size.
DWORD dwSize;
InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);

// Allocate the necessary memory.
char *lpszData;
lpszData = new char[dwSize];

// Call InternetQueryOption again with the provided buffer.
InternetQueryOption( NULL, 
                     INTERNET_OPTION_USER_AGENT,
                     lpszData, &dwSize );

// Insert code here to use the user agent string data.

// Free the allocated memory.
delete [] lpszData;
```



## <a name="setting-connection-options"></a><span data-ttu-id="da98d-209">Настройка параметров соединения</span><span class="sxs-lookup"><span data-stu-id="da98d-209">Setting Connection Options</span></span>

<span data-ttu-id="da98d-210">В Internet Explorer 5 и более поздних версиях для конкретного подключения можно задать свойства обозревателя.</span><span class="sxs-lookup"><span data-stu-id="da98d-210">In Internet Explorer 5 and later, Internet options can be set for on a specific connection.</span></span> <span data-ttu-id="da98d-211">Ранее все подключения совместно использовали одни и те же настройки параметров Интернета.</span><span class="sxs-lookup"><span data-stu-id="da98d-211">Previously, all connections shared the same Internet option settings.</span></span> <span data-ttu-id="da98d-212">Чтобы задать параметры для конкретного подключения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="da98d-212">To set options for a particular connection:</span></span>

1.  <span data-ttu-id="da98d-213">Создание структуры [**\_ \_ \_ \_ списка параметров для сети Интернет**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) .</span><span class="sxs-lookup"><span data-stu-id="da98d-213">Create an [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure.</span></span>
2.  <span data-ttu-id="da98d-214">Выделите память для отдельных параметров Интернета, которые необходимо задать для подключения.</span><span class="sxs-lookup"><span data-stu-id="da98d-214">Allocate the memory for the individual Internet options that you want to set for the connection.</span></span>
3.  <span data-ttu-id="da98d-215">Задайте параметры в структурах параметров [**сети Интернет \_ для каждого из \_ \_ них**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .</span><span class="sxs-lookup"><span data-stu-id="da98d-215">Set the options in [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span>
4.  <span data-ttu-id="da98d-216">Задайте параметры с помощью [**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="da98d-216">Set the options using [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="da98d-217">В следующем примере кода показано, как задать данные прокси-сервера для подключения по локальной сети.</span><span class="sxs-lookup"><span data-stu-id="da98d-217">The following code example shows how to set proxy data for a LAN connection.</span></span>


```C++
BOOL SetConnectionOptions()
{
    INTERNET_PER_CONN_OPTION_LIST list;
    BOOL    bReturn;
    DWORD   dwBufSize = sizeof(list);

    // Fill the list structure.
    list.dwSize = sizeof(list);

    // NULL == LAN, otherwise connectoid name.
    list.pszConnection = NULL;

    // Set three options.
    list.dwOptionCount = 3;
    list.pOptions = new INTERNET_PER_CONN_OPTION[3];

    // Ensure that the memory was allocated.
    if(NULL == list.pOptions)
    {
        // Return FALSE if the memory wasn't allocated.
        return FALSE;
    }

    // Set flags.
    list.pOptions[0].dwOption = INTERNET_PER_CONN_FLAGS;
    list.pOptions[0].Value.dwValue = PROXY_TYPE_DIRECT |
        PROXY_TYPE_PROXY;

    // Set proxy name.
    list.pOptions[1].dwOption = INTERNET_PER_CONN_PROXY_SERVER;
    list.pOptions[1].Value.pszValue = TEXT("https://proxy:80");

    // Set proxy override.
    list.pOptions[2].dwOption = INTERNET_PER_CONN_PROXY_BYPASS;
    list.pOptions[2].Value.pszValue = TEXT("local");

    // Set the options on the connection.
    bReturn = InternetSetOption(NULL,
        INTERNET_OPTION_PER_CONNECTION_OPTION, &list, dwBufSize);

    // Free the allocated memory.
    delete [] list.pOptions;

    return bReturn;
}
```



## <a name="retrieving-connection-options"></a><span data-ttu-id="da98d-218">Получение параметров соединения</span><span class="sxs-lookup"><span data-stu-id="da98d-218">Retrieving Connection Options</span></span>

<span data-ttu-id="da98d-219">В Internet Explorer 5 и более поздних версиях свойства браузера можно получить из определенного подключения.</span><span class="sxs-lookup"><span data-stu-id="da98d-219">In Internet Explorer 5 and later, Internet options can be retrieved from a specific connection.</span></span> <span data-ttu-id="da98d-220">Чтобы получить параметры из конкретного подключения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="da98d-220">To retrieve options from a particular connection:</span></span>

1.  <span data-ttu-id="da98d-221">Создание структуры [**\_ \_ \_ \_ списка параметров для сети Интернет**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) .</span><span class="sxs-lookup"><span data-stu-id="da98d-221">Create a [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure.</span></span>
2.  <span data-ttu-id="da98d-222">Выделите память для отдельных параметров Интернета, которые необходимо получить из соединения.</span><span class="sxs-lookup"><span data-stu-id="da98d-222">Allocate the memory for the individual Internet options to retrieve from the connection.</span></span>
3.  <span data-ttu-id="da98d-223">Укажите параметры с использованием [**структур \_ \_ \_ параметров "в сети Интернет"**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .</span><span class="sxs-lookup"><span data-stu-id="da98d-223">Specify the options using [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span>
4.  <span data-ttu-id="da98d-224">Извлеките параметры с помощью [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="da98d-224">Retrieve the options using [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>
5.  <span data-ttu-id="da98d-225">Используйте данные параметров.</span><span class="sxs-lookup"><span data-stu-id="da98d-225">Utilize the option data.</span></span>
6.  <span data-ttu-id="da98d-226">Освободите память, выделенную для хранения данных параметров, с помощью функции [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .</span><span class="sxs-lookup"><span data-stu-id="da98d-226">Free the memory, allocated to hold the option data, using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span>

> [!Note]  
> <span data-ttu-id="da98d-227">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="da98d-227">WinINet does not support server implementations.</span></span> <span data-ttu-id="da98d-228">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="da98d-228">In addition, it should not be used from a service.</span></span> <span data-ttu-id="da98d-229">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="da98d-229">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="da98d-230">См. также</span><span class="sxs-lookup"><span data-stu-id="da98d-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da98d-231">Обработка проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="da98d-231">Handling Authentication</span></span>](handling-authentication.md)
</dt> <dt>

[<span data-ttu-id="da98d-232">Дескрипторы ХИНТЕРНЕТ</span><span class="sxs-lookup"><span data-stu-id="da98d-232">HINTERNET Handles</span></span>](appendix-a-hinternet-handles.md)
</dt> </dl>

 

