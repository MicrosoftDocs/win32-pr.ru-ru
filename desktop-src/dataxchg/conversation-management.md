---
title: Управление диалоговыми окнами
description: В этом разделе обсуждаются диалоги между клиентом и сервером.
ms.assetid: 4e5ff1a1-d46a-4e2a-a37c-8df951f2a1ee
keywords:
- Пользовательский интерфейс Windows, платформа динамических данных Exchange (DDE)
- Платформа динамических данных Exchange (DDE), беседы
- DDE (платформа динамических данных Exchange), беседы
- Обмен данными, платформа динамических данных Exchange (DDE)
- Пользовательский интерфейс Windows, Библиотека управления платформа динамических данных Exchange (ДДЕМЛ)
- Библиотека управления платформа динамических данных Exchange (ДДЕМЛ), беседы
- ДДЕМЛ (Библиотека управления Exchange платформа динамических данных), беседы
- Обмен данными, Библиотека управления платформа динамических данных Exchange (ДДЕМЛ)
- Платформа динамических данных Exchange (DDE), несколько диалогов
- DDE (платформа динамических данных Exchange), несколько диалогов
- Библиотека управления платформа динамических данных Exchange (ДДЕМЛ), несколько диалогов
- ДДЕМЛ (Библиотека управления Exchange платформа динамических данных), несколько диалогов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca1a0a8e02bceb6b2f69051d89df289871fdd42
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105719067"
---
# <a name="conversation-management"></a><span data-ttu-id="3aa43-115">Управление диалоговыми окнами</span><span class="sxs-lookup"><span data-stu-id="3aa43-115">Conversation Management</span></span>

<span data-ttu-id="3aa43-116">Диалог между клиентом и сервером всегда устанавливается по запросу клиента.</span><span class="sxs-lookup"><span data-stu-id="3aa43-116">A conversation between a client and a server is always established at the request of the client.</span></span> <span data-ttu-id="3aa43-117">При установке диалога каждый участник получает маркер, идентифицирующий диалог.</span><span class="sxs-lookup"><span data-stu-id="3aa43-117">When a conversation is established, each partner receives a handle that identifies the conversation.</span></span> <span data-ttu-id="3aa43-118">Участники используют этот обработчик в других платформа динамических данных функциях библиотеки управления Exchange (ДДЕМЛ) для отправки транзакций и управления диалогом.</span><span class="sxs-lookup"><span data-stu-id="3aa43-118">The partners use this handle in other Dynamic Data Exchange Management Library (DDEML) functions to send transactions and manage the conversation.</span></span> <span data-ttu-id="3aa43-119">Клиент может запросить диалог с одним сервером или запросить несколько диалогов с одним или несколькими серверами.</span><span class="sxs-lookup"><span data-stu-id="3aa43-119">A client can request a conversation with a single server, or it can request multiple conversations with one or more servers.</span></span>

<span data-ttu-id="3aa43-120">В следующих разделах описывается, как приложение устанавливает новые диалоги и получает сведения о существующих диалогах.</span><span class="sxs-lookup"><span data-stu-id="3aa43-120">The following topics describe how an application establishes new conversations and gets information about existing conversations.</span></span>

-   [<span data-ttu-id="3aa43-121">Отдельные беседы</span><span class="sxs-lookup"><span data-stu-id="3aa43-121">Single Conversations</span></span>](#single-conversations)
-   [<span data-ttu-id="3aa43-122">Несколько диалогов</span><span class="sxs-lookup"><span data-stu-id="3aa43-122">Multiple Conversations</span></span>](#multiple-conversations)

## <a name="single-conversations"></a><span data-ttu-id="3aa43-123">Отдельные беседы</span><span class="sxs-lookup"><span data-stu-id="3aa43-123">Single Conversations</span></span>

<span data-ttu-id="3aa43-124">Клиентское приложение запрашивает один диалог с сервером, вызывая функцию [**ддеконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) и указывая дескрипторы строк, которые определяют строки, содержащие имя службы серверного приложения и имя раздела диалога.</span><span class="sxs-lookup"><span data-stu-id="3aa43-124">A client application requests a single conversation with a server by calling the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function and specifying string handles that identify the strings containing the service name of the server application and the topic name for the conversation.</span></span> <span data-ttu-id="3aa43-125">ДДЕМЛ отвечает, отправляя транзакцию [**кстип \_ Connect**](xtyp-connect.md) в функцию обратного вызова платформа динамических данных Exchange (DDE) каждого серверного приложения, которое либо зарегистрировало имя службы, совпадающее с именем, указанным в **ддеконнект** , либо отключило фильтрацию имен служб, вызвав [**дденамесервице**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice).</span><span class="sxs-lookup"><span data-stu-id="3aa43-125">The DDEML responds by sending the [**XTYP\_CONNECT**](xtyp-connect.md) transaction to the Dynamic Data Exchange (DDE) callback function of each server application that either has registered a service name that matches the one specified in **DdeConnect** or has turned service name filtering off by calling [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice).</span></span> <span data-ttu-id="3aa43-126">Сервер также может фильтровать транзакции **кстип \_ Connect** , УКАЗЫВАЯ \_ флаг фильтра КБФ Fail \_ Connections в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="3aa43-126">A server can also filter **XTYP\_CONNECT** transactions by specifying the CBF\_FAIL\_CONNECTIONS filter flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span> <span data-ttu-id="3aa43-127">Во время транзакции **кстип \_ Connect** ддемл передает имя службы и имя раздела на сервер.</span><span class="sxs-lookup"><span data-stu-id="3aa43-127">During the **XTYP\_CONNECT** transaction, the DDEML passes the service name and the topic name to the server.</span></span> <span data-ttu-id="3aa43-128">Сервер должен проверить имена и вернуть **значение true** , если он поддерживает имя службы и имя раздела, или **false** , если нет.</span><span class="sxs-lookup"><span data-stu-id="3aa43-128">The server must examine the names and return **TRUE** if it supports the service name and topic name pair or **FALSE** if it does not.</span></span>

<span data-ttu-id="3aa43-129">Если сервер не отвечает на запрос клиента на подключение, клиент получает **значение NULL** из [**ддеконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) , и диалог не устанавливается.</span><span class="sxs-lookup"><span data-stu-id="3aa43-129">If no server responds positively to the client's request to connect, the client receives **NULL** from [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) and no conversation is established.</span></span> <span data-ttu-id="3aa43-130">Если сервер возвращает **значение true**, то устанавливается диалог и клиент получает маркер диалога — значение **DWORD** , идентифицирующее диалог.</span><span class="sxs-lookup"><span data-stu-id="3aa43-130">If a server returns **TRUE**, a conversation is established and the client receives a conversation handle — a **DWORD** value that identifies the conversation.</span></span> <span data-ttu-id="3aa43-131">Клиент использует этот маркер в последующих вызовах ДДЕМЛ для получения данных с сервера.</span><span class="sxs-lookup"><span data-stu-id="3aa43-131">The client uses the handle in subsequent DDEML calls to obtain data from the server.</span></span> <span data-ttu-id="3aa43-132">Сервер получает транзакцию [**кстип \_ Connect \_ Confirm**](xtyp-connect-confirm.md) (если только сервер не указал \_ \_ флаг фильтра Skip Connect КБФ \_ ).</span><span class="sxs-lookup"><span data-stu-id="3aa43-132">The server receives the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction (unless the server specified the CBF\_SKIP\_CONNECT\_CONFIRMS filter flag).</span></span> <span data-ttu-id="3aa43-133">Эта транзакция передает обработчик диалога на сервер.</span><span class="sxs-lookup"><span data-stu-id="3aa43-133">This transaction passes the conversation handle to the server.</span></span>

<span data-ttu-id="3aa43-134">В следующем примере запрашивается диалог в системном разделе с сервером, который распознает имя службы MyServer.</span><span class="sxs-lookup"><span data-stu-id="3aa43-134">The following example requests a conversation on the System topic with a server that recognizes the service name MyServer.</span></span> <span data-ttu-id="3aa43-135">Параметры *хсзсервнаме* и *хсзсистопик* ранее создавали дескрипторы строк.</span><span class="sxs-lookup"><span data-stu-id="3aa43-135">The *hszServName* and *hszSysTopic* parameters are previously created string handles.</span></span>


```
HCONV hConv;         // conversation handle 
HWND hwndParent;     // parent window handle 
HSZ hszServName;     // service name string handle 
HSZ hszSysTopic;     // System topic string handle 
 
hConv = DdeConnect( 
    idInst,               // instance identifier 
    hszServName,          // service name string handle 
    hszSysTopic,          // System topic string handle 
    (PCONVCONTEXT) NULL); // use default context 
 
if (hConv == NULL) 
{ 
    MessageBox(hwndParent, "MyServer is unavailable.", 
        (LPSTR) NULL, MB_OK); 
    return FALSE; 
} 
```



<span data-ttu-id="3aa43-136">В предыдущем примере [**ддеконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) приводит к тому, что функция обратного вызова DDE приложения MyServer Получает транзакцию [**кстип \_ Connect**](xtyp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="3aa43-136">In the preceding example, [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) causes the DDE callback function of the MyServer application to receive an [**XTYP\_CONNECT**](xtyp-connect.md) transaction.</span></span>

<span data-ttu-id="3aa43-137">В следующем примере сервер отвечает на транзакцию [**кстип \_ Connect**](xtyp-connect.md) , сравнивая строку имени раздела, обменяя ддемл, переданный на сервер, с каждым элементом массива строки имени раздела, который поддерживает сервер.</span><span class="sxs-lookup"><span data-stu-id="3aa43-137">In the following example, the server responds to the [**XTYP\_CONNECT**](xtyp-connect.md) transaction by comparing the topic name string handle the DDEML passed to the server with each element in the array of topic name string handles the server supports.</span></span> <span data-ttu-id="3aa43-138">Если сервер находит совпадение, он устанавливает диалог.</span><span class="sxs-lookup"><span data-stu-id="3aa43-138">If the server finds a match, it establishes the conversation.</span></span>


```
#define CTOPICS 5 
 
HSZ hsz1;                  // string handle passed by DDEML 
HSZ ahszTopics[CTOPICS];   // array of supported topics 
int i;                     // loop counter 
 
// Use a switch statement to examine transaction types. 
// Here is the connect case.
 
    case XTYP_CONNECT: 
        for (i = 0; i < CTOPICS; i++) 
        { 
            if (hsz1 == ahszTopics[i]) 
                return TRUE;   // establish a conversation 
        } 
 
        return FALSE; // Topic not supported; deny conversation.  
 
// Process other transaction types. 
```



<span data-ttu-id="3aa43-139">Если сервер возвращает **значение true** в ответ на транзакцию [**КСТИП \_ Connect**](xtyp-connect.md) , Ддемл отправляет транзакцию [**\_ \_ подтверждения кстип Connect**](xtyp-connect-confirm.md) в функцию обратного вызова DDE сервера.</span><span class="sxs-lookup"><span data-stu-id="3aa43-139">If the server returns **TRUE** in response to the [**XTYP\_CONNECT**](xtyp-connect.md) transaction, the DDEML sends an [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server's DDE callback function.</span></span> <span data-ttu-id="3aa43-140">Сервер может получить обработчик для диалога, обрабатывая эту транзакцию.</span><span class="sxs-lookup"><span data-stu-id="3aa43-140">The server can obtain the handle to the conversation by processing this transaction.</span></span>

<span data-ttu-id="3aa43-141">Клиент может установить диалог с подстановочным знаком, указав **значение NULL** для обработчика строки имени службы, маркера строки имени раздела или и то, и другое в вызове [**ддеконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect).</span><span class="sxs-lookup"><span data-stu-id="3aa43-141">A client can establish a wildcard conversation by specifying **NULL** for the service name string handle, the topic name string handle, or both in a call to [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect).</span></span> <span data-ttu-id="3aa43-142">Если хотя бы один из дескрипторов строк имеет **значение NULL**, ддемл отправляет транзакцию [**кстип \_ вилдконнект**](xtyp-wildconnect.md) функциям обратного вызова всех приложений DDE (за исключением тех, кто отфильтрует транзакцию **кстип \_ вилдконнект** ).</span><span class="sxs-lookup"><span data-stu-id="3aa43-142">If at least one of the string handles is **NULL**, the DDEML sends the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction to the callback functions of all DDE applications (except those that filter the **XTYP\_WILDCONNECT** transaction).</span></span> <span data-ttu-id="3aa43-143">Каждое серверное приложение должно отвечать, возвращая обработчик данных, который определяет массив структур [**хсзпаир**](/windows/win32/api/ddeml/ns-ddeml-hszpair) , заканчивающийся нулем.</span><span class="sxs-lookup"><span data-stu-id="3aa43-143">Each server application should respond by returning a data handle that identifies a null-terminated array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="3aa43-144">Если серверное приложение не вызывало [**дденамесервице**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) для регистрации имен служб и если фильтрация включена, сервер не получает транзакции **кстип \_ вилдконнект** .</span><span class="sxs-lookup"><span data-stu-id="3aa43-144">If the server application has not called [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) to register its service names and if filtering is on, the server does not receive **XTYP\_WILDCONNECT** transactions.</span></span> <span data-ttu-id="3aa43-145">Дополнительные сведения о дескрипторах данных см. в разделе [Управление данными](data-management.md).</span><span class="sxs-lookup"><span data-stu-id="3aa43-145">For more information about data handles, see [Data Management](data-management.md).</span></span>

<span data-ttu-id="3aa43-146">Массив должен содержать одну структуру для каждой пары "имя службы" и "имя раздела", совпадающей с парой, заданной клиентом.</span><span class="sxs-lookup"><span data-stu-id="3aa43-146">The array must contain one structure for each service name and topic name pair that matches the pair specified by the client.</span></span> <span data-ttu-id="3aa43-147">ДДЕМЛ выбирает одну из пар для установления диалога и возвращает клиенту маркер, идентифицирующий диалог.</span><span class="sxs-lookup"><span data-stu-id="3aa43-147">The DDEML selects one of the pairs to establish a conversation and returns to the client a handle that identifies the conversation.</span></span> <span data-ttu-id="3aa43-148">ДДЕМЛ отправляет транзакцию [**кстип \_ Connect \_ Confirm**](xtyp-connect-confirm.md) на сервер (если только сервер не фильтрует эту транзакцию).</span><span class="sxs-lookup"><span data-stu-id="3aa43-148">The DDEML sends the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server (unless the server filters this transaction).</span></span> <span data-ttu-id="3aa43-149">В следующем примере показан типичный ответ сервера на транзакцию [**кстип \_ вилдконнект**](xtyp-wildconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="3aa43-149">The following example shows a typical server response to the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction.</span></span>


```
#define CTOPICS 2 
 
UINT uType; 
HSZPAIR ahszp[(CTOPICS + 1)]; 
HSZ ahszTopicList[CTOPICS]; 
HSZ hszServ, hszTopic; 
WORD i, j; 
 
if (uType == XTYP_WILDCONNECT) 
{ 
    // Scan the topic list and create an array of HSZPAIR structures. 
 
    j = 0; 
    for (i = 0; i < CTOPICS; i++) 
    { 
        if (hszTopic == (HSZ) NULL || 
                hszTopic == ahszTopicList[i]) 
        { 
            ahszp[j].hszSvc = hszServ; 
            ahszp[j++].hszTopic = ahszTopicList[i]; 
        } 
    } 
 
    // End the list with an HSZPAIR structure that contains NULL 
    // string handles as its members. 
 
    ahszp[j].hszSvc = NULL; 
    ahszp[j++].hszTopic = NULL; 
 
    // Return a handle to a global memory object containing the 
    // HSZPAIR structures. 
 
    return DdeCreateDataHandle( 
        idInst,          // instance identifier 
        (LPBYTE) &ahszp, // pointer to HSZPAIR array 
        sizeof(HSZ) * j, // length of the array 
        0,               // start at the beginning 
        (HSZ) NULL,      // no item name string 
        0,               // return the same format 
        0);              // let the system own it 
} 
```



<span data-ttu-id="3aa43-150">Как клиент, так и сервер могут в любой момент завершить диалог, вызвав функцию [**ддедисконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) .</span><span class="sxs-lookup"><span data-stu-id="3aa43-150">Either the client or the server can terminate a conversation at any time by calling the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function.</span></span> <span data-ttu-id="3aa43-151">Эта функция приводит к тому, что функция обратного вызова участника диалога в диалоге Получает транзакцию [**\_ отключения кстип**](xtyp-disconnect.md) (если только участник не указал \_ \_ флаг фильтра Skip unconnects КБФ).</span><span class="sxs-lookup"><span data-stu-id="3aa43-151">This function causes the callback function of the partner in the conversation to receive the [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transaction (unless the partner specified the CBF\_SKIP\_DISCONNECTS filter flag).</span></span> <span data-ttu-id="3aa43-152">Как правило, приложение реагирует на транзакцию **\_ отключения кстип** , используя функцию [**ддекуериконвинфо**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) для получения сведений о завершенном диалоге.</span><span class="sxs-lookup"><span data-stu-id="3aa43-152">Typically, an application responds to the **XTYP\_DISCONNECT** transaction by using the [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) function to obtain information about the conversation that terminated.</span></span> <span data-ttu-id="3aa43-153">После того как функция обратного вызова возвращает из обработки транзакции **кстип \_ Disconnect** , этот обработчик больше не действителен.</span><span class="sxs-lookup"><span data-stu-id="3aa43-153">After the callback function returns from processing the **XTYP\_DISCONNECT** transaction, the conversation handle is no longer valid.</span></span>

<span data-ttu-id="3aa43-154">Клиентское приложение, получающее транзакцию [**кстип \_ Disconnect**](xtyp-disconnect.md) в функции обратного вызова DDE, может попытаться восстановить диалог путем вызова функции [**ддереконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) .</span><span class="sxs-lookup"><span data-stu-id="3aa43-154">A client application that receives an [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transaction in its DDE callback function can attempt to reestablish the conversation by calling the [**DdeReconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) function.</span></span> <span data-ttu-id="3aa43-155">Клиент должен вызвать **ддереконнект** из функции обратного вызова DDE.</span><span class="sxs-lookup"><span data-stu-id="3aa43-155">The client must call **DdeReconnect** from within its DDE callback function.</span></span>

## <a name="multiple-conversations"></a><span data-ttu-id="3aa43-156">Несколько диалогов</span><span class="sxs-lookup"><span data-stu-id="3aa43-156">Multiple Conversations</span></span>

<span data-ttu-id="3aa43-157">Клиентское приложение может использовать функцию [**ддеконнектлист**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) , чтобы определить, доступны ли какие-либо серверы в системе.</span><span class="sxs-lookup"><span data-stu-id="3aa43-157">A client application can use the [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) function to determine whether any servers of interest are available in the system.</span></span> <span data-ttu-id="3aa43-158">Клиент указывает имя службы и имя раздела при вызове **ддеконнектлист**, что приводит к тому, что ддемл передает транзакцию [**кстип \_ вилдконнект**](xtyp-wildconnect.md) в функции обратного вызова DDE всех серверов, которые соответствуют имени службы (за исключением тех, которые фильтруют транзакцию).</span><span class="sxs-lookup"><span data-stu-id="3aa43-158">A client specifies a service name and topic name when it calls **DdeConnectList**, causing the DDEML to broadcast the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction to the DDE callback functions of all servers that match the service name (except those that filter the transaction).</span></span> <span data-ttu-id="3aa43-159">Функция обратного вызова сервера должна возвращать маркер данных, который определяет массив структур [**хсзпаир**](/windows/win32/api/ddeml/ns-ddeml-hszpair) , заканчивающийся нулем.</span><span class="sxs-lookup"><span data-stu-id="3aa43-159">A server's callback function should return a data handle that identifies a null-terminated array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="3aa43-160">Массив должен содержать одну структуру для каждой пары "имя службы" и "имя раздела", совпадающей с парой, заданной клиентом.</span><span class="sxs-lookup"><span data-stu-id="3aa43-160">The array should contain one structure for each service name and topic name pair that matches the pair specified by the client.</span></span> <span data-ttu-id="3aa43-161">ДДЕМЛ устанавливает диалог для каждой структуры **хсзпаир** , заполненной сервером, и возвращает клиенту маркер списка диалогов.</span><span class="sxs-lookup"><span data-stu-id="3aa43-161">The DDEML establishes a conversation for each **HSZPAIR** structure filled by the server and returns a conversation list handle to the client.</span></span> <span data-ttu-id="3aa43-162">Сервер получает обработчик диалога посредством транзакции [**кстип \_ Connect**](xtyp-connect.md) (если только сервер не фильтрует эту транзакцию).</span><span class="sxs-lookup"><span data-stu-id="3aa43-162">The server receives the conversation handle by way of the [**XTYP\_CONNECT**](xtyp-connect.md) transaction (unless the server filters this transaction).</span></span>

<span data-ttu-id="3aa43-163">Клиент может указать **значение NULL** для имени службы, имени раздела или и того, и другого при вызове [**ддеконнектлист**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span><span class="sxs-lookup"><span data-stu-id="3aa43-163">A client can specify **NULL** for the service name, topic name, or both when it calls [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="3aa43-164">Если имя службы равно **null**, все серверы в системе, которые поддерживают указанное имя раздела, отвечают.</span><span class="sxs-lookup"><span data-stu-id="3aa43-164">If the service name is **NULL**, all servers in the system that support the specified topic name respond.</span></span> <span data-ttu-id="3aa43-165">Диалог устанавливается с каждым отвечающим сервером, в том числе с несколькими экземплярами одного и того же сервера.</span><span class="sxs-lookup"><span data-stu-id="3aa43-165">A conversation is established with each responding server, including multiple instances of the same server.</span></span> <span data-ttu-id="3aa43-166">Если имя раздела равно **null**, то для каждого раздела, распознаваемого каждым сервером, который соответствует имени службы, устанавливается диалог.</span><span class="sxs-lookup"><span data-stu-id="3aa43-166">If the topic name is **NULL**, a conversation is established on each topic recognized by each server that matches the service name.</span></span>

<span data-ttu-id="3aa43-167">Клиент может использовать функции [**ддекуеринекстсервер**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) и [**ддекуериконвинфо**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) для обнаружения серверов, которые отвечают на [**ддеконнектлист**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span><span class="sxs-lookup"><span data-stu-id="3aa43-167">A client can use the [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) and [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) functions to identify the servers that respond to [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="3aa43-168">**Ддекуеринекстсервер** возвращает следующий обработчик диалога в списке бесед, а **Ддекуериконвинфо** заполняет структуру [**конвинфо**](/windows/win32/api/ddeml/ns-ddeml-convinfo) информацией о диалоге.</span><span class="sxs-lookup"><span data-stu-id="3aa43-168">**DdeQueryNextServer** returns the next conversation handle in a conversation list, and **DdeQueryConvInfo** fills a [**CONVINFO**](/windows/win32/api/ddeml/ns-ddeml-convinfo) structure with information about the conversation.</span></span> <span data-ttu-id="3aa43-169">Клиент может сохранять необходимые дескрипторы диалога и удалять остальные из списка бесед.</span><span class="sxs-lookup"><span data-stu-id="3aa43-169">The client can keep the conversation handles that it needs and discard the rest from the conversation list.</span></span>

<span data-ttu-id="3aa43-170">В следующем примере [**ддеконнектлист**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) используется для установки диалогов со всеми серверами, которые поддерживают системный раздел, а затем использует функции [**ддекуеринекстсервер**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) и [**ддекуериконвинфо**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) для получения дескрипторов строк имени службы серверов и сохранения их в буфер.</span><span class="sxs-lookup"><span data-stu-id="3aa43-170">The following example uses [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) to establish conversations with all servers that support the System topic and then uses the [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) and [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) functions to obtain the servers' service name string handles and store them in a buffer.</span></span>


```
HCONVLIST hconvList; // conversation list 
DWORD idInst;        // instance identifier 
HSZ hszSystem;       // System topic 
HCONV hconv = NULL;  // conversation handle 
CONVINFO ci;         // holds conversation data 
UINT cConv = 0;      // count of conv. handles 
HSZ *pHsz, *aHsz;    // point to string handles 
 
// Connect to all servers that support the System topic. 
 
hconvList = DdeConnectList(idInst, NULL, hszSystem, NULL, NULL); 
 
// Count the number of handles in the conversation list. 
 
while ((hconv = DdeQueryNextServer(hconvList, hconv)) != NULL) 
    cConv++; 
 
// Allocate a buffer for the string handles. 
 
hconv = NULL; 
aHsz = (HSZ *) LocalAlloc(LMEM_FIXED, cConv * sizeof(HSZ)); 
 
// Copy the string handles to the buffer. 
 
pHsz = aHsz; 
while ((hconv = DdeQueryNextServer(hconvList, hconv)) != NULL) 
{ 
    DdeQueryConvInfo(hconv, QID_SYNC, (PCONVINFO) &ci); 
    DdeKeepStringHandle(idInst, ci.hszSvcPartner); 
    *pHsz++ = ci.hszSvcPartner; 
} 
 
// Use the handles; converse with the servers. 
 
// Free the memory and terminate the conversations. 
 
LocalFree((HANDLE) aHsz); 
DdeDisconnectList(hconvList); 
```



<span data-ttu-id="3aa43-171">Приложение может завершить отдельный диалог в списке бесед, вызвав функцию [**ддедисконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) .</span><span class="sxs-lookup"><span data-stu-id="3aa43-171">An application can terminate an individual conversation in a conversation list by calling the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function.</span></span> <span data-ttu-id="3aa43-172">Приложение может завершить все диалоги в списке бесед, вызвав функцию [**ддедисконнектлист**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) .</span><span class="sxs-lookup"><span data-stu-id="3aa43-172">An application can terminate all conversations in a conversation list by calling the [**DdeDisconnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) function.</span></span> <span data-ttu-id="3aa43-173">Обе функции приводят к тому, что ДДЕМЛ отправляет транзакции [**кстип \_ Disconnect**](xtyp-disconnect.md) в функцию обратного вызова DDE каждого участника.</span><span class="sxs-lookup"><span data-stu-id="3aa43-173">Both functions cause the DDEML to send [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transactions to each partner's DDE callback function.</span></span> <span data-ttu-id="3aa43-174">**Ддедисконнектлист** отправляет транзакцию **\_ отключения кстип** для каждого обработчика диалога в списке.</span><span class="sxs-lookup"><span data-stu-id="3aa43-174">**DdeDisconnectList** sends an **XTYP\_DISCONNECT** transaction for each conversation handle in the list.</span></span>

<span data-ttu-id="3aa43-175">Клиент может получить список дескрипторов диалога в списке бесед, передав существующий дескриптор списка диалогов в [**ддеконнектлист**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span><span class="sxs-lookup"><span data-stu-id="3aa43-175">A client can retrieve a list of the conversation handles in a conversation list by passing an existing conversation list handle to [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="3aa43-176">В процессе перечисления удаляются дескрипторы прерванных диалогов из списка, а также добавляются недублирующиеся диалоги, которые соответствуют указанному имени службы и имени раздела.</span><span class="sxs-lookup"><span data-stu-id="3aa43-176">The enumeration process removes the handles of terminated conversations from the list, and nonduplicate conversations that fit the specified service name and topic name are added.</span></span>

<span data-ttu-id="3aa43-177">Если [**ддеконнектлист**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) указывает существующий дескриптор списка диалогов, функция создает новый список диалогов, содержащий дескрипторы всех новых диалогов и дескрипторов из существующего списка.</span><span class="sxs-lookup"><span data-stu-id="3aa43-177">If [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) specifies an existing conversation list handle, the function creates a new conversation list that contains the handles of any new conversations and the handles from the existing list.</span></span>

<span data-ttu-id="3aa43-178">Если существуют дублирующиеся беседы, [**ддеконнектлист**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) пытается предотвратить дублирование дескрипторов диалога в списке бесед.</span><span class="sxs-lookup"><span data-stu-id="3aa43-178">If duplicate conversations exist, [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) attempts to prevent duplicate conversation handles in the conversation list.</span></span> <span data-ttu-id="3aa43-179">Дубликат диалога — это второй диалог с одним и тем же сервером с тем же именем службы и именем раздела.</span><span class="sxs-lookup"><span data-stu-id="3aa43-179">A duplicate conversation is a second conversation with the same server on the same service name and topic name.</span></span> <span data-ttu-id="3aa43-180">Два таких диалога будут иметь различные дескрипторы, но они будут обозначать один и тот же диалог.</span><span class="sxs-lookup"><span data-stu-id="3aa43-180">Two such conversations would have different handles, yet they would identify the same conversation.</span></span>

 

 




