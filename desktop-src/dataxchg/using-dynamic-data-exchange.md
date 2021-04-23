---
title: Использование платформа динамических данных Exchange
description: В этом разделе приводятся примеры кода, касающиеся динамического обмена данными.
ms.assetid: 6d94403b-64b4-4763-868a-3b94431dab79
keywords:
- Платформа динамических данных Exchange (DDE), беседы
- DDE (платформа динамических данных Exchange), беседы
- Обмен данными, платформа динамических данных Exchange (DDE)
- Платформа динамических данных Exchange (DDE), примеры
- DDE (платформа динамических данных Exchange), примеры
- Платформа динамических данных Exchange (DDE), команды в серверных приложениях
- DDE (платформа динамических данных Exchange), команды в серверных приложениях
- Платформа динамических данных Exchange (DDE), ссылки на данные
- DDE (платформа динамических данных Exchange), ссылки на данные
- Платформа динамических данных Exchange (DDE), элементы
- DDE (платформа динамических данных Exchange), элементы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe20c4dedc38303fe9bcb9c4b0fae42d03ee536
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337913"
---
# <a name="using-dynamic-data-exchange"></a><span data-ttu-id="1ea7f-114">Использование платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="1ea7f-114">Using Dynamic Data Exchange</span></span>

<span data-ttu-id="1ea7f-115">В этом разделе приведены примеры кода для следующих задач:</span><span class="sxs-lookup"><span data-stu-id="1ea7f-115">This section has code samples on the following tasks:</span></span>

-   [<span data-ttu-id="1ea7f-116">Инициация диалога</span><span class="sxs-lookup"><span data-stu-id="1ea7f-116">Initiating a Conversation</span></span>](#initiating-a-conversation)
-   [<span data-ttu-id="1ea7f-117">Передача одного элемента</span><span class="sxs-lookup"><span data-stu-id="1ea7f-117">Transferring a Single Item</span></span>](#transferring-a-single-item)
    -   [<span data-ttu-id="1ea7f-118">Получение элемента с сервера</span><span class="sxs-lookup"><span data-stu-id="1ea7f-118">Retrieving an Item from the Server</span></span>](#retrieving-an-item-from-the-server)
    -   [<span data-ttu-id="1ea7f-119">Отправка элемента на сервер</span><span class="sxs-lookup"><span data-stu-id="1ea7f-119">Submitting an Item to the Server</span></span>](#submitting-an-item-to-the-server)
-   [<span data-ttu-id="1ea7f-120">Установка постоянного канала данных</span><span class="sxs-lookup"><span data-stu-id="1ea7f-120">Establishing a Permanent Data Link</span></span>](#establishing-a-permanent-data-link)
    -   [<span data-ttu-id="1ea7f-121">Инициация связи с данными</span><span class="sxs-lookup"><span data-stu-id="1ea7f-121">Initiating a Data Link</span></span>](#initiating-a-data-link)
    -   [<span data-ttu-id="1ea7f-122">Запуск связи с данными с помощью команды «вставить ссылку»</span><span class="sxs-lookup"><span data-stu-id="1ea7f-122">Initiating a Data Link with the Paste Link Command</span></span>](#initiating-a-data-link-with-the-paste-link-command)
    -   [<span data-ttu-id="1ea7f-123">Уведомление клиента об изменении данных</span><span class="sxs-lookup"><span data-stu-id="1ea7f-123">Notifying the Client that Data Has Changed</span></span>](#notifying-the-client-that-data-has-changed)
    -   [<span data-ttu-id="1ea7f-124">Завершение связи с данными</span><span class="sxs-lookup"><span data-stu-id="1ea7f-124">Terminating a Data Link</span></span>](#terminating-a-data-link)
-   [<span data-ttu-id="1ea7f-125">Выполнение команд в серверном приложении</span><span class="sxs-lookup"><span data-stu-id="1ea7f-125">Carrying Out Commands in a Server Application</span></span>](#carrying-out-commands-in-a-server-application)
-   [<span data-ttu-id="1ea7f-126">Завершение диалога</span><span class="sxs-lookup"><span data-stu-id="1ea7f-126">Terminating a Conversation</span></span>](#terminating-a-conversation)

## <a name="initiating-a-conversation"></a><span data-ttu-id="1ea7f-127">Инициация диалога</span><span class="sxs-lookup"><span data-stu-id="1ea7f-127">Initiating a Conversation</span></span>

<span data-ttu-id="1ea7f-128">Чтобы инициировать диалог платформа динамических данных Exchange (DDE), клиент отправляет сообщение об [**\_ \_ инициации DDE WM**](wm-dde-initiate.md) .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-128">To initiate a Dynamic Data Exchange (DDE) conversation, the client sends a [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message.</span></span> <span data-ttu-id="1ea7f-129">Как правило, клиент передает это сообщение путем вызова [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)с параметром – 1 в качестве первого параметра.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-129">Usually, the client broadcasts this message by calling [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), with –1 as the first parameter.</span></span> <span data-ttu-id="1ea7f-130">Если приложение уже имеет обработчик окна для серверного приложения, оно может отправить сообщение непосредственно в это окно.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-130">If the application already has the window handle to the server application, it can send the message directly to that window.</span></span> <span data-ttu-id="1ea7f-131">Клиент готовит атомы для имени приложения и имени раздела, вызывая [**глобаладдатом**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma).</span><span class="sxs-lookup"><span data-stu-id="1ea7f-131">The client prepares atoms for the application name and topic name by calling [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma).</span></span> <span data-ttu-id="1ea7f-132">Клиент может запрашивать беседы с любым потенциальным серверным приложением и любым потенциальным разделом, предоставляя для приложения и темы атомы **null** (с подстановочными знаками).</span><span class="sxs-lookup"><span data-stu-id="1ea7f-132">The client can request conversations with any potential server application and for any potential topic by supplying **NULL** (wildcard) atoms for the application and topic.</span></span>

<span data-ttu-id="1ea7f-133">В следующем примере показано, как клиент инициирует диалог, где указаны и приложение, и раздел.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-133">The following example illustrates how the client initiates a conversation, where both the application and topic are specified.</span></span>


```
    static BOOL fInInitiate = FALSE; 
    char *szApplication; 
    char *szTopic; 
    atomApplication = *szApplication == 0 ? 
    NULL     : GlobalAddAtom((LPSTR) szApplication); 
    atomTopic = *szTopic == 0 ? 
    NULL     : GlobalAddAtom((LPSTR) szTopic); 
 
    fInInitiate = TRUE; 
    SendMessage((HWND) HWND_BROADCAST, // broadcasts message 
        WM_DDE_INITIATE,               // initiates conversation 
        (WPARAM) hwndClientDDE,        // handle to client DDE window 
        MAKELONG(atomApplication,      // application-name atom 
            atomTopic));               // topic-name atom 
    fInInitiate = FALSE; 
    if (atomApplication != NULL) 
        GlobalDeleteAtom(atomApplication); 
    if (atomTopic != NULL) 
        GlobalDeleteAtom(atomTopic);
```



> [!Note]  
> <span data-ttu-id="1ea7f-134">Если приложение использует атомы **null** , не нужно использовать функции [**глобаладдатом**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) и [**глобалделетеатом**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-134">If your application uses **NULL** atoms, you need not use the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) and [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) functions.</span></span> <span data-ttu-id="1ea7f-135">В этом примере клиентское приложение создает два глобальных атома, содержащие имя сервера и имя раздела соответственно.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-135">In this example, the client application creates two global atoms containing the name of the server and the name of the topic, respectively.</span></span>

 

<span data-ttu-id="1ea7f-136">Клиентское приложение отправляет сообщение [**о \_ \_ запуске приложения WM DDE**](wm-dde-initiate.md) с этими двумя атомами в параметре *lParam* сообщения.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-136">The client application sends a [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message with these two atoms in the *lParam* parameter of the message.</span></span> <span data-ttu-id="1ea7f-137">При вызове функции [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) специальный маркер окна – 1 направляет систему на отправку этого сообщения всем остальным активным приложениям.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-137">In the call to the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function, the special window handle –1 directs the system to send this message to all other active applications.</span></span> <span data-ttu-id="1ea7f-138">**SendMessage** не возвращает клиентскому приложению, пока все приложения, получающие сообщение, в свою очередь возвращают управление системе.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-138">**SendMessage** does not return to the client application until all applications that receive the message have, in turn, returned control to the system.</span></span> <span data-ttu-id="1ea7f-139">Это означает, что все сообщения с сообщением [**WM \_ \_ DDE**](wm-dde-ack.md) , отправленные в ответе серверными приложениями, гарантированно будут обработаны клиентом на момент возвращения вызова **SendMessage** .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-139">This means that all [**WM\_DDE\_ACK**](wm-dde-ack.md) messages sent in reply by the server applications are guaranteed to have been processed by the client by the time the **SendMessage** call has returned.</span></span>

<span data-ttu-id="1ea7f-140">После возврата [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) клиентское приложение удаляет глобальные атомы.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-140">After [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, the client application deletes the global atoms.</span></span>

<span data-ttu-id="1ea7f-141">Серверные приложения реагируют в соответствии с логикой, показанной на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-141">Server applications respond according to the logic illustrated in the following diagram.</span></span>

![логика ответа серверного приложения](images/csdde-01.png)

<span data-ttu-id="1ea7f-143">Чтобы подтвердить один или несколько разделов, сервер должен создать атомы для каждого диалога (если существует несколько разделов) и отправить сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) для каждого диалога, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-143">To acknowledge one or more topics, the server must create atoms for each conversation (requiring duplicate application-name atoms if there are multiple topics) and send a [**WM\_DDE\_ACK**](wm-dde-ack.md) message for each conversation, as illustrated in the following example.</span></span>


```
if ((atomApplication = GlobalAddAtom("Server")) != 0) 
{ 
    if ((atomTopic = GlobalAddAtom(szTopic)) != 0) 
    { 
        SendMessage(hwndClientDDE, 
            WM_DDE_ACK, 
            (WPARAM) hwndServerDDE, 
            MAKELONG(atomApplication, atomTopic)); 
        GlobalDeleteAtom(atomApplication); 
    } 
 
    GlobalDeleteAtom(atomTopic); 
} 
 
if ((atomApplication == 0) || (atomTopic == 0)) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="1ea7f-144">Когда сервер отвечает сообщением [**WM \_ DDE \_ ACK**](wm-dde-ack.md) , клиентское приложение должно сохранить маркер в окне сервера.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-144">When a server responds with a [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the client application should save a handle to the server window.</span></span> <span data-ttu-id="1ea7f-145">Клиент, получивший этот маркер в качестве параметра *wParam* сообщения **WM \_ DDE \_ ACK** , отправляет все последующие сообщения DDE в окно сервера, которое идентифицирует этот обработчик.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-145">The client receiving the handle as the *wParam* parameter of the **WM\_DDE\_ACK** message then sends all subsequent DDE messages to the server window this handle identifies.</span></span>

<span data-ttu-id="1ea7f-146">Если клиентское приложение использует в качестве имени приложения или раздела **значение NULL** Atom, приложение должно получить подтверждения от нескольких серверных приложений.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-146">If your client application uses a **NULL** atom for the application name or topic name, expect the application to receive acknowledgments from more than one server application.</span></span> <span data-ttu-id="1ea7f-147">Несколько подтверждений также могут поступать из нескольких экземпляров сервера DDE, даже если клиентское приложение не **имеет значений** , применяющих атомы.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-147">Multiple acknowledgements can also come from multiple instances of a DDE server, even if your client application does not **NULL** use atoms.</span></span> <span data-ttu-id="1ea7f-148">Для каждого диалога сервер всегда должен использовать уникальное окно.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-148">A server should always use a unique window for each conversation.</span></span> <span data-ttu-id="1ea7f-149">Процедура окна в клиентском приложении может использовать для наблюдения за несколькими беседами обработчик для окна сервера (предоставленного в качестве параметра *lParam* для [**\_ \_ запуска WM DDE**](wm-dde-initiate.md)).</span><span class="sxs-lookup"><span data-stu-id="1ea7f-149">The window procedure in the client application can use a handle to the server window (provided as the *lParam* parameter of [**WM\_DDE\_INITIATE**](wm-dde-initiate.md)) to track multiple conversations.</span></span> <span data-ttu-id="1ea7f-150">Это позволяет одному клиентскому окну обрабатывать несколько диалогов, не требуя завершения и повторного подключения с новым клиентским окном для каждого диалога.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-150">This allows a single client window to process several conversations without needing to terminate and reconnect with a new client window for each conversation.</span></span>

## <a name="transferring-a-single-item"></a><span data-ttu-id="1ea7f-151">Передача одного элемента</span><span class="sxs-lookup"><span data-stu-id="1ea7f-151">Transferring a Single Item</span></span>

<span data-ttu-id="1ea7f-152">После установки диалога DDE клиент может либо получить значение элемента данных с сервера, выполнив сообщение [**\_ \_ запроса WM DDE**](wm-dde-request.md) , либо отправить значение элемента данных на сервер, вызвав [**WM \_ DDE \_**](wm-dde-poke.md).</span><span class="sxs-lookup"><span data-stu-id="1ea7f-152">Once a DDE conversation has been established, the client can either retrieve the value of a data item from the server by issuing the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message, or submit a data-item value to the server by issuing [**WM\_DDE\_POKE**](wm-dde-poke.md).</span></span>

-   [<span data-ttu-id="1ea7f-153">Получение элемента с сервера</span><span class="sxs-lookup"><span data-stu-id="1ea7f-153">Retrieving an Item from the Server</span></span>](#retrieving-an-item-from-the-server)
-   [<span data-ttu-id="1ea7f-154">Отправка элемента на сервер</span><span class="sxs-lookup"><span data-stu-id="1ea7f-154">Submitting an Item to the Server</span></span>](#submitting-an-item-to-the-server)

### <a name="retrieving-an-item-from-the-server"></a><span data-ttu-id="1ea7f-155">Получение элемента с сервера</span><span class="sxs-lookup"><span data-stu-id="1ea7f-155">Retrieving an Item from the Server</span></span>

<span data-ttu-id="1ea7f-156">Чтобы получить элемент с сервера, клиент отправляет серверу сообщение [**\_ \_ запроса WM DDE**](wm-dde-request.md) с указанием элемента и формата для извлечения, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-156">To retrieve an item from the server, the client sends the server a [**WM\_DDE\_REQUEST**](wm-dde-request.md) message specifying the item and format to retrieve, as shown in the following example.</span></span>


```
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndServerDDE, 
            WM_DDE_REQUEST, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_REQUEST, CF_TEXT, atomItem))) 
    {
        GlobalDeleteAtom(atomItem); 
    }
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="1ea7f-157">В этом примере клиент указывает формат буфера обмена в формате **CF \_** в качестве предпочтительного формата для запрошенного элемента данных.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-157">In this example, the client specifies the clipboard format **CF\_TEXT** as the preferred format for the requested data item.</span></span>

<span data-ttu-id="1ea7f-158">Получатель (сервер) сообщения [**\_ \_ запроса DDE WM**](wm-dde-request.md) обычно должен удалить элемент Atom, но если вызов [**сообщения**](/windows/desktop/api/winuser/nf-winuser-postmessagea) завершается неудачей, клиент должен удалить Atom.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-158">The receiver (server) of the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message typically must delete the item atom, but if the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) call fails, the client must delete the atom.</span></span>

<span data-ttu-id="1ea7f-159">Если сервер имеет доступ к запрошенному элементу и может визуализировать его в запрошенном формате, сервер копирует значение элемента как объект общей памяти и отправляет клиенту сообщение [**\_ \_ данных WM DDE**](wm-dde-data.md) , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-159">If the server has access to the requested item and can render it in the requested format, the server copies the item value as a shared memory object and sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message, as illustrated in the following example.</span></span>


```
// Allocate the size of the DDE data header, plus the data: a 
// string,<CR><LF><NULL>. The byte for the string's terminating 
// null character is counted by DDEDATA.Value[1].

size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hData = GlobalAlloc(GMEM_MOVEABLE,
  (LONG) sizeof(DDEDATA) + *pcch + 2)))  
{
    return; 
}
 
if (!(lpData = (DDEDATA FAR*) GlobalLock(hData)))  
{
    GlobalFree(hData); 
    return; 
} 
 
lpData->cfFormat = CF_TEXT;
hResult = StringCchCopy((LPSTR) lpData->Value, *pcch +1, (LPCSTR) szItemValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
 
// Each line of CF_TEXT data is terminated by CR/LF. 
hResult = StringCchCat((LPSTR) lpData->Value, *pcch + 3, (LPCSTR) "\r\n");
if (FAILED(hResult)
{
// TODO: Write error handler.
 return;
} 
GlobalUnlock(hData); 
if ((atomItem = GlobalAddAtom((LPSTR) szItemName)) != 0) 
{ 
    lParam = PackDDElParam(WM_DDE_ACK, (UINT) hData, atomItem); 
    if (!PostMessage(hwndClientDDE, 
            WM_DDE_DATA, 
            (WPARAM) hwndServerDDE, 
            lParam)) 
    { 
        GlobalFree(hData); 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_ACK, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors.  
}
```



<span data-ttu-id="1ea7f-160">В этом примере серверное приложение выделяет объект памяти для хранения элемента данных.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-160">In this example, the server application allocates a memory object to contain the data item.</span></span> <span data-ttu-id="1ea7f-161">Объект данных инициализируется как структура [**ддедата**](/windows/desktop/api/Dde/ns-dde-ddedata) .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-161">The data object is initialized as a [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure.</span></span>

<span data-ttu-id="1ea7f-162">Затем серверное приложение устанавливает в качестве элемента **кфформат** структуры текст CF, \_ чтобы информировать клиентское приложение о том, что данные находятся в текстовом формате.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-162">The server application then sets the **cfFormat** member of the structure to CF\_TEXT to inform the client application that the data is in text format.</span></span> <span data-ttu-id="1ea7f-163">Клиент отвечает, копируя значение запрошенных данных в элемент **value** структуры [**ддедата**](/windows/desktop/api/Dde/ns-dde-ddedata) .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-163">The client responds by copying the value of the requested data into the **Value** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure.</span></span> <span data-ttu-id="1ea7f-164">После того как сервер заполнит объект данных, сервер разблокирует данные и создаст глобальный объект Atom, содержащий имя элемента данных.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-164">After the server has filled the data object, the server unlocks the data and creates a global atom containing the name of the data item.</span></span>

<span data-ttu-id="1ea7f-165">Наконец, сервер выдает сообщение [**\_ \_ данных WM DDE**](wm-dde-data.md) , вызывая [**сообщение**](/windows/desktop/api/winuser/nf-winuser-postmessagea).</span><span class="sxs-lookup"><span data-stu-id="1ea7f-165">Finally, the server issues the [**WM\_DDE\_DATA**](wm-dde-data.md) message by calling [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea).</span></span> <span data-ttu-id="1ea7f-166">Маркер объекта данных и объект Atom, содержащий имя элемента, упаковываются в параметр *lParam* сообщения функцией [**паккдделпарам**](/windows/desktop/api/Dde/nf-dde-packddelparam) .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-166">The handle to the data object and the atom containing the item name are packed into the *lParam* parameter of the message by the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function.</span></span>

<span data-ttu-id="1ea7f-167">Если [**сообщение**](/windows/desktop/api/winuser/nf-winuser-postmessagea) не выполняется, сервер должен использовать функцию [**фридделпарам**](/windows/desktop/api/Dde/nf-dde-freeddelparam) для высвобождения упакованного параметра *lParam* .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-167">If [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) fails, the server must use the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function to free the packed *lParam* parameter.</span></span> <span data-ttu-id="1ea7f-168">Сервер также должен освободить упакованный параметр *lParam* для полученного сообщения о [**\_ \_ запросе DDE WM**](wm-dde-request.md) .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-168">The server must also free the packed *lParam* parameter for the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message it received.</span></span>

<span data-ttu-id="1ea7f-169">Если сервер не может удовлетворить запрос, он отправляет клиенту негативное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-169">If the server cannot satisfy the request, it sends a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message to the client, as shown in the following example.</span></span>


```
// Negative acknowledgment. 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 0, atomItem));
```



<span data-ttu-id="1ea7f-170">При получении сообщения [**\_ \_ данных DDE WM**](wm-dde-data.md) клиент обрабатывает значение элемента данных соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-170">Upon receiving a [**WM\_DDE\_DATA**](wm-dde-data.md) message, the client processes the data-item value as appropriate.</span></span> <span data-ttu-id="1ea7f-171">Затем, если элемент **факкрек** , на который указывает, в сообщении **\_ \_ данных DDE WM** имеет значение 1, клиент должен отправить серверу положительное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-171">Then, if the **fAckReq** member pointed to in the **WM\_DDE\_DATA** message is 1, the client must send the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message, as shown in the following example.</span></span>


```
UnpackDDElParam(WM_DDE_DATA, lParam, (PUINT) &hData, 
    (PUINT) &atomItem); 
if (!(lpDDEData = (DDEDATA FAR*) GlobalLock(hData)) 
        || (lpDDEData->cfFormat != CF_TEXT)) 
{ 
    PostMessage(hwndServerDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_ACK, 0, atomItem)); // Negative ACK. 
} 
 
// Copy data from lpDDEData here. 
 
if (lpDDEData->fAckReq) 
{ 
    PostMessage(hwndServerDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_ACK, 0x8000, 
            atomItem)); // Positive ACK 
} 
 
bRelease = lpDDEData->fRelease; 
GlobalUnlock(hData); 
if (bRelease) 
    GlobalFree(hData);
```



<span data-ttu-id="1ea7f-172">В этом примере клиент проверяет формат данных.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-172">In this example, the client examines the format of the data.</span></span> <span data-ttu-id="1ea7f-173">Если формат не является **\_ текстом CF** (или если клиент не может заблокировать память для данных), клиент отправляет отрицательное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) , чтобы указать, что он не может обработать данные.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-173">If the format is not **CF\_TEXT** (or if the client cannot lock the memory for the data), the client sends a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message to indicate that it cannot process the data.</span></span> <span data-ttu-id="1ea7f-174">Если клиент не может заблокировать обработчик данных, так как он содержит элемент **факкрек** , клиент не должен отсылать сообщение о том, что оно не должно содержать отрицательные сообщения **WM \_ DDE \_** .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-174">If the client cannot lock a data handle because the handle contains the **fAckReq** member, the client should not send a negative **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="1ea7f-175">Вместо этого клиент должен завершить диалог.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-175">Instead, the client should terminate the conversation.</span></span>

<span data-ttu-id="1ea7f-176">Если клиент отправляет отрицательное подтверждение в ответ на сообщение [**\_ \_ данных DDE WM**](wm-dde-data.md) , сервер отвечает за освобождение памяти (но не параметра *lParam* ), на который ссылается сообщение **\_ \_ данных WM DDE** , связанное с отрицательным подтверждением.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-176">If a client sends a negative acknowledgment in response to a [**WM\_DDE\_DATA**](wm-dde-data.md) message, the server is responsible for freeing the memory (but not the *lParam* parameter) referenced by the **WM\_DDE\_DATA** message associated with the negative acknowledgment.</span></span>

<span data-ttu-id="1ea7f-177">Если он может обработать данные, клиент проверяет элемент **факкрек** структуры [**ддедата**](/windows/desktop/api/Dde/ns-dde-ddedata) , чтобы определить, запрашивал ли сервер, что он сообщил о том, что клиент получил и обработал данные успешно.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-177">If it can process the data, the client examines the **fAckReq** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to determine whether the server requested that it be informed that the client received and processed the data successfully.</span></span> <span data-ttu-id="1ea7f-178">Если сервер запрашивал эти сведения, клиент отправляет серверу положительное сообщение [**WM \_ DDE \_**](wm-dde-ack.md) .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-178">If the server did request this information, the client sends the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="1ea7f-179">Поскольку разблокировка данных делает указатель на данные недействительным, клиент сохраняет значение члена **фрелеасе** перед разблокировкой объекта данных.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-179">Because unlocking data invalidates the pointer to the data, the client saves the value of the **fRelease** member before unlocking the data object.</span></span> <span data-ttu-id="1ea7f-180">После сохранения значения клиент проверяет его, чтобы определить, запросил ли клиентское серверное приложение освобождение памяти, содержащей данные. Клиент действует соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-180">After saving the value, the client then examines it to determine whether the server application requested the client to free the memory containing the data; the client acts accordingly.</span></span>

<span data-ttu-id="1ea7f-181">При получении негативного [**сообщения \_ WM \_ DDE**](wm-dde-ack.md) , клиент может запросить еще одно значение элемента, указав другой формат буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-181">Upon receiving a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the client can ask for the same item value again, specifying a different clipboard format.</span></span> <span data-ttu-id="1ea7f-182">Как правило, клиент сначала запрашивает наиболее сложный формат, который он может поддерживать, а затем при необходимости выполните шаг с заходом, используя более простые форматы, пока не обнаружит, что сервер может предоставить.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-182">Typically, a client will first ask for the most complex format it can support, then step down if necessary through progressively simpler formats until it finds one the server can provide.</span></span>

<span data-ttu-id="1ea7f-183">Если сервер поддерживает элемент formats системного раздела, клиент может определить, какой именно формат буфера обмена поддерживает сервер, а не определять их каждый раз, когда клиент запрашивает элемент.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-183">If the server supports the Formats item of the system topic, the client can determine once what clipboard formats the server supports, instead of determining them each time the client requests an item.</span></span>

### <a name="submitting-an-item-to-the-server"></a><span data-ttu-id="1ea7f-184">Отправка элемента на сервер</span><span class="sxs-lookup"><span data-stu-id="1ea7f-184">Submitting an Item to the Server</span></span>

<span data-ttu-id="1ea7f-185">Клиент может отправить значение элемента на сервер с помощью сообщения [**WM \_ DDE \_**](wm-dde-poke.md) .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-185">The client may send an item value to the server by using the [**WM\_DDE\_POKE**](wm-dde-poke.md) message.</span></span> <span data-ttu-id="1ea7f-186">Клиент визуализирует элемент для отправки и отправляет сообщение **WM \_ DDE \_** , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-186">The client renders the item to be sent and sends the **WM\_DDE\_POKE** message, as illustrated in the following example.</span></span>


```
size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hPokeData = GlobalAlloc(GMEM_MOVEABLE,
  (LONG) sizeof(DDEPOKE) + *pcch + 2))) 
{
    return; 
}
 
if (!(lpPokeData = (DDEPOKE *) GlobalLock(hPokeData))) 
{ 
    GlobalFree(hPokeData); 
    return; 
} 
 
lpPokeData->fRelease = TRUE; 
lpPokeData->cfFormat = CF_TEXT;
hResult = StringCchCopy((LPSTR) lpPokeData->Value, *pcch +1, (LPCSTR) szValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}  
 
// Each line of CF_TEXT data is terminated by CR/LF. 
hResult = StringCchCat((LPSTR) lpPokeData->Value, *pcch + 3, (LPCSTR) "\r\n");
if (FAILED(hResult)
{
// TODO: Write error handler.
 return;
}
GlobalUnlock(hPokeData); 
if ((atomItem = GlobalAddAtom((LPSTR) szItem)) != 0) 
{ 
 
        if (!PostMessage(hwndServerDDE, 
                WM_DDE_POKE, 
                (WPARAM) hwndClientDDE, 
                PackDDElParam(WM_DDE_POKE, (UINT) hPokeData, 
                    atomItem))) 
        { 
            GlobalDeleteAtom(atomItem); 
            GlobalFree(hPokeData); 
        } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
} 
```



> [!Note]  
> <span data-ttu-id="1ea7f-187">Отправка данных с помощью сообщения [**обмена \_ WM \_ DDE**](wm-dde-poke.md) , по сути, аналогична его отправке с помощью [**\_ \_ данных DDE**](wm-dde-data.md)WM, за исключением того, что приложение **WM \_ DDE \_** отправляется с клиента на сервер.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-187">Sending data by using a [**WM\_DDE\_POKE**](wm-dde-poke.md) message is essentially the same as sending it by using [**WM\_DDE\_DATA**](wm-dde-data.md), except that **WM\_DDE\_POKE** is sent from the client to the server.</span></span>

 

<span data-ttu-id="1ea7f-188">Если сервер способен принимать значение элемента данных в формате, подготовленном клиентом, сервер обрабатывает значение элемента соответствующим образом и отправляет клиенту положительное сообщение [**WM \_ DDE \_**](wm-dde-ack.md) .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-188">If the server is able to accept the data-item value in the format rendered by the client, the server processes the item value as appropriate and sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span> <span data-ttu-id="1ea7f-189">Если не удается обработать значение элемента из-за его формата или по другим причинам, сервер отправляет клиенту отрицательное сообщение **WM \_ DDE \_** .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-189">If it is unable to process the item value, because of its format or for other reasons, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>


```
UnpackDDElParam(WM_DDE_POKE, lParam, (PUINT) &hPokeData, 
    (PUINT) &atomItem); 
GlobalGetAtomName(atomItem, szItemName, ITEM_NAME_MAX_SIZE); 
if (!(lpPokeData = (DDEPOKE *) GlobalLock(hPokeData)) 
        || lpPokeData->cfFormat != CF_TEXT 
        || !IsItemSupportedByServer(szItemName)) 
{ 
    PostMessage(hwndClientDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndServerDDE, 
        PackDDElParam(WM_DDE_ACK, 0, atomItem)); // negative ACK  
}
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
} 
hResult = StringCchCopy(szItemValue, *pcch +1, lpPokeData->Value); // copies value 
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}  
bRelease = lpPokeData->fRelease; 
GlobalUnlock(hPokeData); 
if (bRelease) 
{ 
    GlobalFree(hPokeData); 
} 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 
         0x8000, atomItem));    // positive ACK.
```



<span data-ttu-id="1ea7f-190">В этом примере сервер вызывает [**глобалжетатомнаме**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) , чтобы получить имя элемента, отправленного клиентом.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-190">In this example, the server calls [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) to retrieve the name of the item the client sent.</span></span> <span data-ttu-id="1ea7f-191">Затем сервер определяет, поддерживает ли он элемент, и отображается ли он в правильном формате (то есть в \_ тексте CF).</span><span class="sxs-lookup"><span data-stu-id="1ea7f-191">The server then determines whether it supports the item and whether the item is rendered in the correct format (that is, CF\_TEXT).</span></span> <span data-ttu-id="1ea7f-192">Если элемент не поддерживается и не подготавливается к просмотру в правильном формате или если сервер не может заблокировать память для данных, сервер отправляет клиентскому приложению отрицательное подтверждение.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-192">If the item is not supported and not rendered in the correct format, or if the server cannot lock the memory for the data, the server sends a negative acknowledgment back to the client application.</span></span> <span data-ttu-id="1ea7f-193">Обратите внимание, что в этом случае отправка отрицательного подтверждения является правильной, так как в сообщениях [**WM \_ \_ DDE**](wm-dde-poke.md) , которые всегда имеют набор элементов **факкрек** .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-193">Note that in this case, sending a negative acknowledgment is correct because [**WM\_DDE\_POKE**](wm-dde-poke.md) messages are always assumed to have the **fAckReq** member set.</span></span> <span data-ttu-id="1ea7f-194">Сервер должен игнорировать член.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-194">The server should ignore the member.</span></span>

<span data-ttu-id="1ea7f-195">Если сервер отправляет отрицательное подтверждение в ответ на сообщение о сообщении [**WM \_ DDE \_**](wm-dde-poke.md) , клиент отвечает за освобождение памяти (но не параметра *lParam* ), на который ссылается сообщение **WM \_ \_ DDE** , связанное с отрицательным подтверждением.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-195">If a server sends a negative acknowledgment in response to a [**WM\_DDE\_POKE**](wm-dde-poke.md) message, the client is responsible for freeing the memory (but not the *lParam* parameter) referenced by the **WM\_DDE\_POKE** message associated with the negative acknowledgment.</span></span>

## <a name="establishing-a-permanent-data-link"></a><span data-ttu-id="1ea7f-196">Установка постоянного канала данных</span><span class="sxs-lookup"><span data-stu-id="1ea7f-196">Establishing a Permanent Data Link</span></span>

<span data-ttu-id="1ea7f-197">Клиентское приложение может использовать DDE для установки ссылки на элемент в серверном приложении.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-197">A client application can use DDE to establish a link to an item in a server application.</span></span> <span data-ttu-id="1ea7f-198">После того как такая связь установлена, сервер отправляет периодические обновления связанного элемента клиенту, как правило, при каждом изменении значения элемента.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-198">After such a link is established, the server sends periodic updates of the linked item to the client, typically, whenever the value of the item changes.</span></span> <span data-ttu-id="1ea7f-199">Таким словами, между двумя приложениями устанавливается постоянный поток данных; Этот поток данных остается на месте до тех пор, пока он не будет явно отключен.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-199">Thus, a permanent data stream is established between the two applications; this data stream remains in place until it is explicitly disconnected.</span></span>

### <a name="initiating-a-data-link"></a><span data-ttu-id="1ea7f-200">Инициация связи с данными</span><span class="sxs-lookup"><span data-stu-id="1ea7f-200">Initiating a Data Link</span></span>

<span data-ttu-id="1ea7f-201">Клиент инициирует канал передачи данных, отправляя сообщение [**WM \_ DDE \_ advise**](wm-dde-advise.md) , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-201">The client initiates a data link by posting a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, as shown in the following example.</span></span>


```
if (!(hOptions = GlobalAlloc(GMEM_MOVEABLE, 
        sizeof(DDEADVISE)))) 
    return; 
if (!(lpOptions = (DDEADVISE FAR*) GlobalLock(hOptions))) 
{ 
    GlobalFree(hOptions); 
    return; 
} 
 
lpOptions->cfFormat = CF_TEXT; 
lpOptions->fAckReq = TRUE; 
lpOptions->fDeferUpd = FALSE; 
GlobalUnlock(hOptions); 
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!(PostMessage(hwndServerDDE, 
            WM_DDE_ADVISE, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_ADVISE, (UINT) hOptions, 
                atomItem)))) 
    { 
        GlobalDeleteAtom(atomItem); 
        GlobalFree(hOptions); 
        FreeDDElParam(WM_DDE_ADVISE, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors 
 
}
```



<span data-ttu-id="1ea7f-202">В этом примере клиентское приложение устанавливает флаг **фдеферупд** для сообщения [**WM \_ DDE \_ advise**](wm-dde-advise.md) в **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-202">In this example, the client application sets the **fDeferUpd** flag of the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to **FALSE**.</span></span> <span data-ttu-id="1ea7f-203">Это направляет серверное приложение на отправку данных клиенту при каждом изменении данных.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-203">This directs the server application to send the data to the client whenever the data changes.</span></span>

<span data-ttu-id="1ea7f-204">Если серверу не удается выполнить обслуживание запроса [**WM \_ DDE \_**](wm-dde-advise.md) , он отправляет клиенту негативное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-204">If the server is unable to service the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) request, it sends the client a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span> <span data-ttu-id="1ea7f-205">Но если сервер имеет доступ к элементу и может визуализировать его в запрошенном формате, сервер заносит новую ссылку (повторное обращение к флагам, указанным в параметре *хоптионс* ) и отправляет клиенту положительное сообщение **WM \_ DDE \_ ACK** .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-205">But if the server has access to the item and can render it in the requested format, the server notes the new link (recalling the flags specified in the *hOptions* parameter) and sends the client a positive **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="1ea7f-206">После этого, пока клиент не выдаст соответствующее сообщение [**WM \_ DDE \_ unadvise**](wm-dde-unadvise.md) , сервер отправляет клиенту новые данные каждый раз, когда изменяется значение элемента на сервере.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-206">From then on, until the client issues a matching [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message, the server sends the new data to the client every time the value of the item changes in the server.</span></span>

<span data-ttu-id="1ea7f-207">Сообщение [**WM \_ DDE \_ advise**](wm-dde-advise.md) устанавливает формат данных, которые будут передаваться на сервер при связи.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-207">The [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message establishes the format of the data to be exchanged during the link.</span></span> <span data-ttu-id="1ea7f-208">Если клиент пытается установить другую связь с тем же элементом, но использует другой формат данных, сервер может отклонить второй формат данных или попытаться его поддерживать.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-208">If the client attempts to establish another link with the same item but is using a different data format, the server can choose to reject the second data format or attempt to support it.</span></span> <span data-ttu-id="1ea7f-209">Если для какого-либо элемента данных была установлена горячая связь, сервер может одновременно поддерживать только один формат данных.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-209">If a warm link has been established for any data item, the server can support only one data format at a time.</span></span> <span data-ttu-id="1ea7f-210">Это связано с тем, что сообщение [**\_ \_ данных WM DDE**](wm-dde-data.md) для горячего соединения имеет **пустой** обработчик данных, который в противном случае содержит сведения о формате.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-210">This is because the [**WM\_DDE\_DATA**](wm-dde-data.md) message for a warm link has a **NULL** data handle, which otherwise contains the format information.</span></span> <span data-ttu-id="1ea7f-211">Таким же, сервер должен отклонять все горячие связи для элемента, который уже связан, и отклонять все ссылки для элемента, для которого имеются горячий ссылки.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-211">Thus, a server must reject all warm links for an item already linked, and must reject all links for an item that has warm links.</span></span> <span data-ttu-id="1ea7f-212">Другой интерпретацией может быть то, что сервер изменяет формат и горячее или теплое состояние ссылки при запросе второй ссылки на тот же элемент данных.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-212">Another interpretation may be that the server changes the format and the hot or warm state of a link when a second link is requested for the same data item.</span></span>

<span data-ttu-id="1ea7f-213">В общем случае клиентские приложения не должны пытаться одновременно устанавливать несколько ссылок на один элемент данных.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-213">In general, client applications should not attempt to establish more than one link at a time for a data item.</span></span>

### <a name="initiating-a-data-link-with-the-paste-link-command"></a><span data-ttu-id="1ea7f-214">Запуск связи с данными с помощью команды «вставить ссылку»</span><span class="sxs-lookup"><span data-stu-id="1ea7f-214">Initiating a Data Link with the Paste Link Command</span></span>

<span data-ttu-id="1ea7f-215">Приложения, поддерживающие каналы "горячий" или "теплый" канал данных, обычно поддерживают зарегистрированный формат буфера обмена с именем Link.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-215">Applications that support hot or warm data links typically support a registered clipboard format named Link.</span></span> <span data-ttu-id="1ea7f-216">При сопоставлении с командами копирования и вставки в приложении этот формат буфера обмена позволяет пользователю устанавливать сеанс DDE между приложениями просто путем копирования элемента данных в серверное приложение и вставки его в клиентское приложение.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-216">When associated with the application's Copy and Paste Link commands, this clipboard format enables the user to establish DDE conversations between applications simply by copying a data item in the server application and pasting it into the client application.</span></span>

<span data-ttu-id="1ea7f-217">Серверное приложение поддерживает формат буфера обмена Link, помещая в буфер обмена строку, содержащую имя приложения, раздела и элемента, когда пользователь выбирает команду **Копировать** в меню **Правка** .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-217">A server application supports the Link clipboard format by placing in the clipboard a string containing the application, topic, and item names when the user chooses the **Copy** command from the **Edit** menu.</span></span> <span data-ttu-id="1ea7f-218">Ниже приведен стандартный формат ссылки.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-218">Following is the standard Link format:</span></span>

<span data-ttu-id="1ea7f-219">*Приложение ***\\ 0***, раздел ***\\ 0***, элемент \* \* \* \\ 0 \\ 0*\*</span><span class="sxs-lookup"><span data-stu-id="1ea7f-219">*application ***\\0*** topic ***\\0*** item\*\*\*\\0\\0*\*</span></span>

<span data-ttu-id="1ea7f-220">Один символ NULL отделяет имена, а два пустых символа завершают всю строку.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-220">A single null character separates the names, and two null characters terminate the entire string.</span></span>

<span data-ttu-id="1ea7f-221">Клиентские и серверные приложения должны зарегистрировать формат буфера обмена ссылок, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-221">Both the client and server applications must register the Link clipboard format, as shown:</span></span>


```
cfLink = RegisterClipboardFormat("Link");
```



<span data-ttu-id="1ea7f-222">Клиентское приложение поддерживает формат буфера обмена Link с помощью команды вставить ссылку в его меню Правка.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-222">A client application supports the Link clipboard format by means of a Paste Link command on its Edit menu.</span></span> <span data-ttu-id="1ea7f-223">Когда пользователь выбирает эту команду, клиентское приложение анализирует имена приложения, раздела и элемента из данных из буфера обмена формата ссылки.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-223">When the user chooses this command, the client application parses the application, topic, and item names from the Link-format clipboard data.</span></span> <span data-ttu-id="1ea7f-224">Используя эти имена, клиентское приложение инициирует диалог для приложения и раздела, если такой диалог еще не существует.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-224">Using these names, the client application initiates a conversation for the application and topic, if such a conversation does not already exist.</span></span> <span data-ttu-id="1ea7f-225">Затем клиентское приложение отправляет в серверное приложение сообщение с предложением [**WM \_ DDE \_**](wm-dde-advise.md) , указывая имя элемента, которое содержится в данных буфера обмена формата ссылки.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-225">The client application then sends a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to the server application, specifying the item name contained in the Link-format clipboard data.</span></span>

<span data-ttu-id="1ea7f-226">Ниже приведен пример ответа клиентского приложения, когда пользователь выбирает команду Вставить ссылку.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-226">Following is an example of a client application's response when the user chooses the Paste Link command.</span></span>


```
void DoPasteLink(hwndClientDDE) 
HWND hwndClientDDE; 
{ 
    HANDLE hData; 
    LPSTR lpData; 
    HWND hwndServerDDE; 
    CHAR szApplication[APP_MAX_SIZE + 1]; 
    CHAR szTopic[TOPIC_MAX_SIZE + 1]; 
    CHAR szItem[ITEM_MAX_SIZE + 1]; 
    size_t * nBufLen; 
 HRESULT hResult;
 
    if (OpenClipboard(hwndClientDDE)) 
    { 
        if (!(hData = GetClipboardData(cfLink)) || 
                !(lpData = GlobalLock(hData))) 
        { 
            CloseClipboard(); 
            return; 
        } 
 
        // Parse the clipboard data.
  hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
// TODO: Write error handler.
  return;
 }
 if (*nBufLen >= APP_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }
 hResult = StringCchCopy(szApplication, APP_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
// TODO: Write error handler.
  return;
 }
        lpData += (*nBufLen + 1); // skips over null
 hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
 // TODO: Write error handler.
  return;
 }
 if (*nBufLen >= TOPIC_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }
 hResult = StringCchCopy(szTopic, TOPIC_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
 // TODO: Write error handler.
  return;
 }
        lpData += (nBufLen + 1); // skips over null
 hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
 // TODO: Write error handler.
  return;
 }
 if (*nBufLen >= ITEM_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }

 hResult = StringCchCopy(szItem, ITEM_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
 // TODO: Write error handler.
  return;
 } 
        GlobalUnlock(hData); 
        CloseClipboard(); 
 
        if (hwndServerDDE = 
                FindServerGivenAppTopic(szApplication, szTopic)) 
        { 
            // App/topic conversation is already started. 
 
            if (DoesAdviseAlreadyExist(hwndServerDDE, szItem)) 
            {
                MessageBox(hwndMain, 
                    "Advisory already established", 
                    "Client", MB_ICONEXCLAMATION | MB_OK); 
            }
            else SendAdvise(hwndClientDDE, hwndServerDDE, szItem); 
        } 
        else 
        { 
            // Client must initiate a new conversation first. 
            SendInitiate(szApplication, szTopic); 
            if (hwndServerDDE = 
                    FindServerGivenAppTopic(szApplication, 
                        szTopic)) 
            {
                SendAdvise(hwndClientDDE, hwndServerDDE, szItem); 
            }
        } 
    } 
    return; 
}
```



<span data-ttu-id="1ea7f-227">В этом примере клиентское приложение открывает буфер обмена и определяет, содержит ли он данные в формате ссылки (т. е. Кфлинк), который был ранее зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-227">In this example, the client application opens the clipboard and determines whether it contains data in the Link format (that is, cfLink) it had previously registered.</span></span> <span data-ttu-id="1ea7f-228">Если это не так или не может блокировать данные в буфере обмена, клиент возвращает.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-228">If not, or if it cannot lock the data in the clipboard, the client returns.</span></span>

<span data-ttu-id="1ea7f-229">После того как клиентское приложение получит указатель на данные буфера обмена, он анализирует данные для извлечения имен приложения, раздела и элемента.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-229">After the client application retrieves a pointer to the clipboard data, it parses the data to extract the application, topic, and item names.</span></span>

<span data-ttu-id="1ea7f-230">Клиентское приложение определяет, существует ли связь между этим разделом и серверным приложением.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-230">The client application determines whether a conversation on the topic already exists between it and the server application.</span></span> <span data-ttu-id="1ea7f-231">Если диалог существует, клиент проверяет, существует ли уже ссылка для элемента данных.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-231">If a conversation does exist, the client checks whether a link already exists for the data item.</span></span> <span data-ttu-id="1ea7f-232">Если такая ссылка существует, клиент отображает окно сообщения пользователю. в противном случае он вызывает собственную функцию *сендадвисе* для отправки на сервер сообщения с сообщением об ошибке [**WM \_ DDE \_**](wm-dde-advise.md) для элемента.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-232">If such a link exists, the client displays a message box to the user; otherwise, it calls its own *SendAdvise* function to send a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to the server for the item.</span></span>

<span data-ttu-id="1ea7f-233">Если между клиентом и сервером не существует диалог, то клиент сначала вызывает собственную функцию *сендинитиате* для отправки сообщения об [**\_ \_ инициировании диалога WM DDE**](wm-dde-initiate.md) и, во-вторых, вызывает собственную функцию *финдсервергивенапптопик* , чтобы установить диалог с окном, отвечающим от имени серверного приложения.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-233">If a conversation on the topic does not already exist between the client and the server, the client first calls its own *SendInitiate* function to broadcast the [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message to request a conversation and, second, calls its own *FindServerGivenAppTopic* function to establish the conversation with the window that responds on behalf of the server application.</span></span> <span data-ttu-id="1ea7f-234">После начала диалога клиентское приложение вызывает *сендадвисе* для запроса ссылки.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-234">After the conversation has begun, the client application calls *SendAdvise* to request the link.</span></span>

### <a name="notifying-the-client-that-data-has-changed"></a><span data-ttu-id="1ea7f-235">Уведомление клиента об изменении данных</span><span class="sxs-lookup"><span data-stu-id="1ea7f-235">Notifying the Client that Data Has Changed</span></span>

<span data-ttu-id="1ea7f-236">Когда клиент устанавливает ссылку с помощью сообщения [**WM \_ DDE \_ advise**](wm-dde-advise.md) , если элемент **фдеферупд** не задан (то есть равен нулю) в структуре [**ддедата**](/windows/desktop/api/Dde/ns-dde-ddedata) , клиент запрашивает сервер отправку элемента данных при каждом изменении значения элемента.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-236">When the client establishes a link by using the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, with the **fDeferUpd** member not set (that is, equal to zero) in the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure, the client has requested the server send the data item each time the item's value changes.</span></span> <span data-ttu-id="1ea7f-237">В таких случаях сервер отображает новое значение элемента данных в указанном ранее формате и отправляет клиенту сообщение с [**\_ \_ данными DDE WM**](wm-dde-data.md) , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-237">In such cases, the server renders the new value of the data item in the previously specified format and sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message, as shown in the following example.</span></span>


```
// Allocate the size of a DDE data header, plus data (a string), 
// plus a <CR><LF><NULL> 

size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hData = GlobalAlloc(GMEM_MOVEABLE,
  sizeof(DDEDATA) + *pcch + 3))) 
{
    return; 
}
if (!(lpData = (DDEDATA FAR*) GlobalLock(hData))) 
{ 
    GlobalFree(hData); 
    return; 
} 
lpData->fAckReq = bAckRequest;       // as in original WM_DDE_ADVISE 
lpData->cfFormat = CF_TEXT;
hResult = StringCchCopy(lpData->Value, *pcch +1, szItemValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
// add CR/LF for CF_TEXT format
hResult = StringCchCat(lpData->Value, *pcch + 3, "\r\n");
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
GlobalUnlock(hData); 
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndClientDDE, 
            WM_DDE_DATA, 
            (WPARAM) hwndServerDDE, 
            PackDDElParam(WM_DDE_DATA, (UINT) hData, atomItem))) 
    { 
        GlobalFree(hData); 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_DATA, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
 
}
```



<span data-ttu-id="1ea7f-238">В этом примере клиент обрабатывает значение элемента соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-238">In this example, the client processes the item value as appropriate.</span></span> <span data-ttu-id="1ea7f-239">Если установлен флаг **факкрек** для элемента, клиент отправляет серверу положительное сообщение [**WM \_ DDE \_**](wm-dde-ack.md) .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-239">If the **fAckReq** flag for the item is set, the client sends the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="1ea7f-240">Когда клиент устанавливает связь с набором элементов **фдеферупд** (то есть равным 1), клиент запрашивает, чтобы каждый раз при изменении данных отправлялись только уведомления, а не сами данные.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-240">When the client establishes the link, with the **fDeferUpd** member set (that is, equal to 1), the client has requested that only a notification, not the data itself, be sent each time the data changes.</span></span> <span data-ttu-id="1ea7f-241">В таких случаях при изменении значения элемента сервер не отображает значение, но просто отправляет клиенту сообщение [**\_ \_ данных WM DDE**](wm-dde-data.md) с нулевым маркером данных, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-241">In such cases, when the item value changes, the server does not render the value but simply sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message with a null data handle, as illustrated in the following example.</span></span>


```
if (bDeferUpd)      // check whether flag was set in WM_DDE_ADVISE
{
    if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
    { 
        if (!PostMessage(hwndClientDDE, 
                WM_DDE_DATA, 
                (WPARAM) hwndServerDDE, 
                PackDDElParam(WM_DDE_DATA, 0, 
                    atomItem)))                  // NULL data
        {
            GlobalDeleteAtom(atomItem); 
            FreeDDElParam(WM_DDE_DATA, lParam); 
        } 
    } 
} 
 
if (atomItem == 0) 
{ 
     // Handle errors. 
} 
```



<span data-ttu-id="1ea7f-242">При необходимости клиент может запросить Последнее значение элемента данных, выполнив нормальное сообщение [**\_ \_ запроса DDE WM**](wm-dde-request.md) , или просто проигнорировать уведомление с сервера об изменении данных.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-242">As necessary, the client can request the latest value of the data item by issuing a normal [**WM\_DDE\_REQUEST**](wm-dde-request.md) message, or it can simply ignore the notice from the server that the data has changed.</span></span> <span data-ttu-id="1ea7f-243">В любом случае, если **факкрек** равен 1, клиент должен отправить на сервер положительное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-243">In either case, if **fAckReq** is equal to 1, the client is expected to send a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message to the server.</span></span>

### <a name="terminating-a-data-link"></a><span data-ttu-id="1ea7f-244">Завершение связи с данными</span><span class="sxs-lookup"><span data-stu-id="1ea7f-244">Terminating a Data Link</span></span>

<span data-ttu-id="1ea7f-245">Если клиент запрашивает завершение работы определенного канала данных, клиент отправляет серверу сообщение [**WM \_ DDE \_ unadvise**](wm-dde-unadvise.md) , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-245">If the client requests that a specific data link be terminated, the client sends the server a [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message, as shown in the following example.</span></span>


```
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndServerDDE, 
            WM_DDE_UNADVISE, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_UNADVISE, 0, atomItem))) 
    { 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_UNADVISE, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="1ea7f-246">Сервер проверяет, содержит ли клиент в данный момент ссылку на конкретный элемент в этом диалоге.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-246">The server checks whether the client currently has a link to the specific item in this conversation.</span></span> <span data-ttu-id="1ea7f-247">Если ссылка существует, сервер отправляет клиенту положительное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) ; сервер больше не требуется для отправки обновлений об элементе.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-247">If a link exists, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; the server is then no longer required to send updates about the item.</span></span> <span data-ttu-id="1ea7f-248">Если ссылка не существует, сервер отправляет клиенту негативное сообщение **WM \_ DDE \_ ACK** .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-248">If no link exists, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>

<span data-ttu-id="1ea7f-249">Сообщение [**WM \_ DDE \_ unadvise**](wm-dde-unadvise.md) указывает формат данных.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-249">The [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message specifies a data format.</span></span> <span data-ttu-id="1ea7f-250">Нулевой формат информирует сервер о необходимости присоединения всех ссылок для указанного элемента, даже если установлено несколько активных ссылок и используется другой формат.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-250">A format of zero informs the server to stop all links for the specified item, even if several hot links are established and each uses a different format.</span></span>

<span data-ttu-id="1ea7f-251">Чтобы завершить все ссылки для диалога, клиентское приложение отправляет серверу сообщение [**WM \_ DDE \_ unadvise**](wm-dde-unadvise.md) с элементом Atom элемента null.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-251">To terminate all links for a conversation, the client application sends the server a [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message with a null item atom.</span></span> <span data-ttu-id="1ea7f-252">Сервер определяет, имеется ли в настоящее время диалога хотя бы один канал.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-252">The server determines whether the conversation has at least one link currently established.</span></span> <span data-ttu-id="1ea7f-253">Если ссылка существует, сервер отправляет клиенту положительное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) ; сервер больше не должен отправлять обновления в диалоге.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-253">If a link exists, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; the server then no longer has to send any updates in the conversation.</span></span> <span data-ttu-id="1ea7f-254">Если ссылка не существует, сервер отправляет клиенту негативное сообщение **WM \_ DDE \_ ACK** .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-254">If no link exists, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>

## <a name="carrying-out-commands-in-a-server-application"></a><span data-ttu-id="1ea7f-255">Выполнение команд в серверном приложении</span><span class="sxs-lookup"><span data-stu-id="1ea7f-255">Carrying Out Commands in a Server Application</span></span>

<span data-ttu-id="1ea7f-256">Приложения могут использовать сообщение [**\_ \_ выполнения WM DDE**](wm-dde-execute.md) , чтобы вызвать выполнение определенной команды или ряда команд в другом приложении.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-256">Applications can use the [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message to cause a certain command or series of commands to be carried out in another application.</span></span> <span data-ttu-id="1ea7f-257">Для этого клиент отправляет серверу сообщение о **\_ \_ выполнении WM DDE** , содержащее маркер командной строки, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-257">To do this, the client sends the server a **WM\_DDE\_EXECUTE** message containing a handle to a command string, as shown in the following example.</span></span>


```
HRESULT hResult;
  
if (!(hCommand = GlobalAlloc(GMEM_MOVEABLE, 
        sizeof(szCommandString) + 1))) 
{
    return; 
}
if (!(lpCommand = GlobalLock(hCommand))) 
{ 
    GlobalFree(hCommand); 
    return; 
} 

hResult = StringCbCopy(lpCommand, sizeof(szCommandString), szCommandString);
if (hResult != S_OK)
{
// TODO: Write error handler.
 return;
}
 
GlobalUnlock(hCommand); 
if (!PostMessage(hwndServerDDE, 
        WM_DDE_EXECUTE, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_EXECUTE, 0, (UINT) hCommand))) 
{ 
    GlobalFree(hCommand); 
    FreeDDElParam(WM_DDE_EXECUTE, lParam); 
}
```



<span data-ttu-id="1ea7f-258">В этом примере сервер пытается выполнить указанную командную строку.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-258">In this example, the server attempts to carry out the specified command string.</span></span> <span data-ttu-id="1ea7f-259">В случае успешной работы сервер отправляет клиенту положительное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) ; в противном случае отправляется отрицательное сообщение **WM \_ DDE \_** .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-259">If it succeeds, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; otherwise, it sends a negative **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="1ea7f-260">Это сообщение **WM \_ DDE \_ ACK** повторно использует маркер *хкомманд* , переданный в исходное [**сообщение \_ \_ выполнения WM DDE**](wm-dde-execute.md) .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-260">This **WM\_DDE\_ACK** message reuses the *hCommand* handle passed in the original [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message.</span></span>

<span data-ttu-id="1ea7f-261">Если строка выполнения команды клиента запрашивает завершение работы сервера, сервер должен ответить, отправив положительное сообщение [**WM \_ DDE \_**](wm-dde-ack.md) , а затем опубликовать сообщение о [**\_ \_ прерывании DDE WM**](wm-dde-terminate.md) , прежде чем завершать работу.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-261">If the client's command execution string requests that the server terminate, the server should respond by sending a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message and then post a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message before terminating.</span></span> <span data-ttu-id="1ea7f-262">Все остальные команды, отправляемые с сообщением [**\_ \_ выполнения WM DDE**](wm-dde-execute.md) , должны выполняться синхронно, то есть сервер должен отправить сообщение **WM \_ DDE \_ ACK** только после успешного завершения команды.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-262">All other commands sent with a [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message should be executed synchronously; that is, the server should send a **WM\_DDE\_ACK** message only after successfully completing the command.</span></span>

## <a name="terminating-a-conversation"></a><span data-ttu-id="1ea7f-263">Завершение диалога</span><span class="sxs-lookup"><span data-stu-id="1ea7f-263">Terminating a Conversation</span></span>

<span data-ttu-id="1ea7f-264">Как клиент, так и сервер могут выдавать сообщение о [**\_ \_ прерывании WM DDE**](wm-dde-terminate.md) для завершения диалога в любое время.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-264">Either the client or the server can issue a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message to terminate a conversation at any time.</span></span> <span data-ttu-id="1ea7f-265">Аналогично, как клиентские, так и серверные приложения должны быть готовы к получению этого сообщения в любое время.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-265">Similarly, both the client and server applications should be prepared to receive this message at any time.</span></span> <span data-ttu-id="1ea7f-266">Перед завершением работы приложение должно завершить все его диалоги.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-266">An application must terminate all of its conversations before shutting down.</span></span>

<span data-ttu-id="1ea7f-267">В следующем примере приложение, завершающее диалог, отправляет сообщение о [**\_ \_ завершении диалога WM DDE**](wm-dde-terminate.md) .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-267">In the following example, the application terminating the conversation posts a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message.</span></span>


```
PostMessage(hwndServerDDE, WM_DDE_TERMINATE, 
    (WPARAM) hwndClientDDE, 0);
```



<span data-ttu-id="1ea7f-268">Это информирует другое приложение о том, что отправляющее приложение не будет отправлять дальнейшие сообщения, и получатель может закрыть его окно.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-268">This informs the other application that the sending application will send no further messages and the recipient can close its window.</span></span> <span data-ttu-id="1ea7f-269">Предполагается, что получатель отвечает на запросы немедленно, отправляя сообщение [**о \_ \_ прекращении DDE в WM**](wm-dde-terminate.md) .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-269">The recipient is expected in all cases to respond promptly by sending a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message.</span></span> <span data-ttu-id="1ea7f-270">Получатель не должен отсылать отрицательное, занятое или положительное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-270">The recipient must not send a negative, busy, or positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="1ea7f-271">После того как приложение отправило сообщение об [**\_ \_ увольнении WM DDE**](wm-dde-terminate.md) участнику в сеансе DDE, оно не должно отвечать на сообщения от этого участника, так как участник мог уничтожить окно, в которое был отправлен ответ.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-271">After an application has sent the [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message to the partner in a DDE conversation, it must not respond to messages from that partner, since the partner might have destroyed the window to which the response would be sent.</span></span>

<span data-ttu-id="1ea7f-272">Если приложение получает сообщение DDE, отличное от [**WM \_ DDE \_**](wm-dde-terminate.md) , после того, как оно отправило **\_ \_ прерывание WM DDE**, оно должно освобождать все объекты, связанные с полученными сообщениями, за исключением дескрипторов данных для [**\_ \_ данных WM DDE**](wm-dde-data.md) или сообщений [**WM \_ DDE \_**](wm-dde-poke.md) , **не** имеющих набора элементов **фрелеасе** .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-272">If an application receives a DDE message other than [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) after it has posted **WM\_DDE\_TERMINATE**, it should free all objects associated with the received messages except the data handles for [**WM\_DDE\_DATA**](wm-dde-data.md) or [**WM\_DDE\_POKE**](wm-dde-poke.md) messages that do **not** have the **fRelease** member set.</span></span>

<span data-ttu-id="1ea7f-273">Когда приложение собирается завершить работу, оно должно завершить все активные сеансы DDE до завершения обработки сообщения [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="1ea7f-273">When an application is about to terminate, it should end all active DDE conversations before completing processing of the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span> <span data-ttu-id="1ea7f-274">Однако если приложение не заканчивает активные сеансы DDE, система завершит все сеансы DDE, связанные с окном, когда окно будет уничтожено.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-274">However, if an application does not end its active DDE conversations, the system will terminate any DDE conversations associated with a window when the window is destroyed.</span></span> <span data-ttu-id="1ea7f-275">В следующем примере показано, как серверное приложение завершает все сеансы DDE.</span><span class="sxs-lookup"><span data-stu-id="1ea7f-275">The following example shows how a server application terminates all DDE conversations.</span></span>


```
void TerminateConversations(hwndServerDDE) 
HWND hwndServerDDE; 
{ 
    HWND hwndClientDDE; 
 
    // Terminate each active conversation. 
 
    while (hwndClientDDE = GetNextLink(hwndClientDDE)) 
    { 
        SendTerminate(hwndServerDDE, hwndClientDDE); 
    } 
    return; 
} 
 
BOOL AtLeastOneLinkActive(VOID) 
{ 
    return TRUE; 
} 
 
HWND GetNextLink(hwndDummy) 
    HWND hwndDummy; 
{ 
    return (HWND) 1; 
} 
 
VOID SendTerminate(HWND hwndServerDDE, HWND hwndClientDDE) 
{ 
    return; 
}
```



 

 