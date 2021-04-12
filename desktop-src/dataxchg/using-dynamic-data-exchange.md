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
# <a name="using-dynamic-data-exchange"></a>Использование платформа динамических данных Exchange

В этом разделе приведены примеры кода для следующих задач:

-   [Инициация диалога](#initiating-a-conversation)
-   [Передача одного элемента](#transferring-a-single-item)
    -   [Получение элемента с сервера](#retrieving-an-item-from-the-server)
    -   [Отправка элемента на сервер](#submitting-an-item-to-the-server)
-   [Установка постоянного канала данных](#establishing-a-permanent-data-link)
    -   [Инициация связи с данными](#initiating-a-data-link)
    -   [Запуск связи с данными с помощью команды «вставить ссылку»](#initiating-a-data-link-with-the-paste-link-command)
    -   [Уведомление клиента об изменении данных](#notifying-the-client-that-data-has-changed)
    -   [Завершение связи с данными](#terminating-a-data-link)
-   [Выполнение команд в серверном приложении](#carrying-out-commands-in-a-server-application)
-   [Завершение диалога](#terminating-a-conversation)

## <a name="initiating-a-conversation"></a>Инициация диалога

Чтобы инициировать диалог платформа динамических данных Exchange (DDE), клиент отправляет сообщение об [**\_ \_ инициации DDE WM**](wm-dde-initiate.md) . Как правило, клиент передает это сообщение путем вызова [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)с параметром – 1 в качестве первого параметра. Если приложение уже имеет обработчик окна для серверного приложения, оно может отправить сообщение непосредственно в это окно. Клиент готовит атомы для имени приложения и имени раздела, вызывая [**глобаладдатом**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma). Клиент может запрашивать беседы с любым потенциальным серверным приложением и любым потенциальным разделом, предоставляя для приложения и темы атомы **null** (с подстановочными знаками).

В следующем примере показано, как клиент инициирует диалог, где указаны и приложение, и раздел.


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
> Если приложение использует атомы **null** , не нужно использовать функции [**глобаладдатом**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) и [**глобалделетеатом**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) . В этом примере клиентское приложение создает два глобальных атома, содержащие имя сервера и имя раздела соответственно.

 

Клиентское приложение отправляет сообщение [**о \_ \_ запуске приложения WM DDE**](wm-dde-initiate.md) с этими двумя атомами в параметре *lParam* сообщения. При вызове функции [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) специальный маркер окна – 1 направляет систему на отправку этого сообщения всем остальным активным приложениям. **SendMessage** не возвращает клиентскому приложению, пока все приложения, получающие сообщение, в свою очередь возвращают управление системе. Это означает, что все сообщения с сообщением [**WM \_ \_ DDE**](wm-dde-ack.md) , отправленные в ответе серверными приложениями, гарантированно будут обработаны клиентом на момент возвращения вызова **SendMessage** .

После возврата [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) клиентское приложение удаляет глобальные атомы.

Серверные приложения реагируют в соответствии с логикой, показанной на следующей схеме.

![логика ответа серверного приложения](images/csdde-01.png)

Чтобы подтвердить один или несколько разделов, сервер должен создать атомы для каждого диалога (если существует несколько разделов) и отправить сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) для каждого диалога, как показано в следующем примере.


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



Когда сервер отвечает сообщением [**WM \_ DDE \_ ACK**](wm-dde-ack.md) , клиентское приложение должно сохранить маркер в окне сервера. Клиент, получивший этот маркер в качестве параметра *wParam* сообщения **WM \_ DDE \_ ACK** , отправляет все последующие сообщения DDE в окно сервера, которое идентифицирует этот обработчик.

Если клиентское приложение использует в качестве имени приложения или раздела **значение NULL** Atom, приложение должно получить подтверждения от нескольких серверных приложений. Несколько подтверждений также могут поступать из нескольких экземпляров сервера DDE, даже если клиентское приложение не **имеет значений** , применяющих атомы. Для каждого диалога сервер всегда должен использовать уникальное окно. Процедура окна в клиентском приложении может использовать для наблюдения за несколькими беседами обработчик для окна сервера (предоставленного в качестве параметра *lParam* для [**\_ \_ запуска WM DDE**](wm-dde-initiate.md)). Это позволяет одному клиентскому окну обрабатывать несколько диалогов, не требуя завершения и повторного подключения с новым клиентским окном для каждого диалога.

## <a name="transferring-a-single-item"></a>Передача одного элемента

После установки диалога DDE клиент может либо получить значение элемента данных с сервера, выполнив сообщение [**\_ \_ запроса WM DDE**](wm-dde-request.md) , либо отправить значение элемента данных на сервер, вызвав [**WM \_ DDE \_**](wm-dde-poke.md).

-   [Получение элемента с сервера](#retrieving-an-item-from-the-server)
-   [Отправка элемента на сервер](#submitting-an-item-to-the-server)

### <a name="retrieving-an-item-from-the-server"></a>Получение элемента с сервера

Чтобы получить элемент с сервера, клиент отправляет серверу сообщение [**\_ \_ запроса WM DDE**](wm-dde-request.md) с указанием элемента и формата для извлечения, как показано в следующем примере.


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



В этом примере клиент указывает формат буфера обмена в формате **CF \_** в качестве предпочтительного формата для запрошенного элемента данных.

Получатель (сервер) сообщения [**\_ \_ запроса DDE WM**](wm-dde-request.md) обычно должен удалить элемент Atom, но если вызов [**сообщения**](/windows/desktop/api/winuser/nf-winuser-postmessagea) завершается неудачей, клиент должен удалить Atom.

Если сервер имеет доступ к запрошенному элементу и может визуализировать его в запрошенном формате, сервер копирует значение элемента как объект общей памяти и отправляет клиенту сообщение [**\_ \_ данных WM DDE**](wm-dde-data.md) , как показано в следующем примере.


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



В этом примере серверное приложение выделяет объект памяти для хранения элемента данных. Объект данных инициализируется как структура [**ддедата**](/windows/desktop/api/Dde/ns-dde-ddedata) .

Затем серверное приложение устанавливает в качестве элемента **кфформат** структуры текст CF, \_ чтобы информировать клиентское приложение о том, что данные находятся в текстовом формате. Клиент отвечает, копируя значение запрошенных данных в элемент **value** структуры [**ддедата**](/windows/desktop/api/Dde/ns-dde-ddedata) . После того как сервер заполнит объект данных, сервер разблокирует данные и создаст глобальный объект Atom, содержащий имя элемента данных.

Наконец, сервер выдает сообщение [**\_ \_ данных WM DDE**](wm-dde-data.md) , вызывая [**сообщение**](/windows/desktop/api/winuser/nf-winuser-postmessagea). Маркер объекта данных и объект Atom, содержащий имя элемента, упаковываются в параметр *lParam* сообщения функцией [**паккдделпарам**](/windows/desktop/api/Dde/nf-dde-packddelparam) .

Если [**сообщение**](/windows/desktop/api/winuser/nf-winuser-postmessagea) не выполняется, сервер должен использовать функцию [**фридделпарам**](/windows/desktop/api/Dde/nf-dde-freeddelparam) для высвобождения упакованного параметра *lParam* . Сервер также должен освободить упакованный параметр *lParam* для полученного сообщения о [**\_ \_ запросе DDE WM**](wm-dde-request.md) .

Если сервер не может удовлетворить запрос, он отправляет клиенту негативное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) , как показано в следующем примере.


```
// Negative acknowledgment. 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 0, atomItem));
```



При получении сообщения [**\_ \_ данных DDE WM**](wm-dde-data.md) клиент обрабатывает значение элемента данных соответствующим образом. Затем, если элемент **факкрек** , на который указывает, в сообщении **\_ \_ данных DDE WM** имеет значение 1, клиент должен отправить серверу положительное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) , как показано в следующем примере.


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



В этом примере клиент проверяет формат данных. Если формат не является **\_ текстом CF** (или если клиент не может заблокировать память для данных), клиент отправляет отрицательное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) , чтобы указать, что он не может обработать данные. Если клиент не может заблокировать обработчик данных, так как он содержит элемент **факкрек** , клиент не должен отсылать сообщение о том, что оно не должно содержать отрицательные сообщения **WM \_ DDE \_** . Вместо этого клиент должен завершить диалог.

Если клиент отправляет отрицательное подтверждение в ответ на сообщение [**\_ \_ данных DDE WM**](wm-dde-data.md) , сервер отвечает за освобождение памяти (но не параметра *lParam* ), на который ссылается сообщение **\_ \_ данных WM DDE** , связанное с отрицательным подтверждением.

Если он может обработать данные, клиент проверяет элемент **факкрек** структуры [**ддедата**](/windows/desktop/api/Dde/ns-dde-ddedata) , чтобы определить, запрашивал ли сервер, что он сообщил о том, что клиент получил и обработал данные успешно. Если сервер запрашивал эти сведения, клиент отправляет серверу положительное сообщение [**WM \_ DDE \_**](wm-dde-ack.md) .

Поскольку разблокировка данных делает указатель на данные недействительным, клиент сохраняет значение члена **фрелеасе** перед разблокировкой объекта данных. После сохранения значения клиент проверяет его, чтобы определить, запросил ли клиентское серверное приложение освобождение памяти, содержащей данные. Клиент действует соответствующим образом.

При получении негативного [**сообщения \_ WM \_ DDE**](wm-dde-ack.md) , клиент может запросить еще одно значение элемента, указав другой формат буфера обмена. Как правило, клиент сначала запрашивает наиболее сложный формат, который он может поддерживать, а затем при необходимости выполните шаг с заходом, используя более простые форматы, пока не обнаружит, что сервер может предоставить.

Если сервер поддерживает элемент formats системного раздела, клиент может определить, какой именно формат буфера обмена поддерживает сервер, а не определять их каждый раз, когда клиент запрашивает элемент.

### <a name="submitting-an-item-to-the-server"></a>Отправка элемента на сервер

Клиент может отправить значение элемента на сервер с помощью сообщения [**WM \_ DDE \_**](wm-dde-poke.md) . Клиент визуализирует элемент для отправки и отправляет сообщение **WM \_ DDE \_** , как показано в следующем примере.


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
> Отправка данных с помощью сообщения [**обмена \_ WM \_ DDE**](wm-dde-poke.md) , по сути, аналогична его отправке с помощью [**\_ \_ данных DDE**](wm-dde-data.md)WM, за исключением того, что приложение **WM \_ DDE \_** отправляется с клиента на сервер.

 

Если сервер способен принимать значение элемента данных в формате, подготовленном клиентом, сервер обрабатывает значение элемента соответствующим образом и отправляет клиенту положительное сообщение [**WM \_ DDE \_**](wm-dde-ack.md) . Если не удается обработать значение элемента из-за его формата или по другим причинам, сервер отправляет клиенту отрицательное сообщение **WM \_ DDE \_** .


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



В этом примере сервер вызывает [**глобалжетатомнаме**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) , чтобы получить имя элемента, отправленного клиентом. Затем сервер определяет, поддерживает ли он элемент, и отображается ли он в правильном формате (то есть в \_ тексте CF). Если элемент не поддерживается и не подготавливается к просмотру в правильном формате или если сервер не может заблокировать память для данных, сервер отправляет клиентскому приложению отрицательное подтверждение. Обратите внимание, что в этом случае отправка отрицательного подтверждения является правильной, так как в сообщениях [**WM \_ \_ DDE**](wm-dde-poke.md) , которые всегда имеют набор элементов **факкрек** . Сервер должен игнорировать член.

Если сервер отправляет отрицательное подтверждение в ответ на сообщение о сообщении [**WM \_ DDE \_**](wm-dde-poke.md) , клиент отвечает за освобождение памяти (но не параметра *lParam* ), на который ссылается сообщение **WM \_ \_ DDE** , связанное с отрицательным подтверждением.

## <a name="establishing-a-permanent-data-link"></a>Установка постоянного канала данных

Клиентское приложение может использовать DDE для установки ссылки на элемент в серверном приложении. После того как такая связь установлена, сервер отправляет периодические обновления связанного элемента клиенту, как правило, при каждом изменении значения элемента. Таким словами, между двумя приложениями устанавливается постоянный поток данных; Этот поток данных остается на месте до тех пор, пока он не будет явно отключен.

### <a name="initiating-a-data-link"></a>Инициация связи с данными

Клиент инициирует канал передачи данных, отправляя сообщение [**WM \_ DDE \_ advise**](wm-dde-advise.md) , как показано в следующем примере.


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



В этом примере клиентское приложение устанавливает флаг **фдеферупд** для сообщения [**WM \_ DDE \_ advise**](wm-dde-advise.md) в **значение false**. Это направляет серверное приложение на отправку данных клиенту при каждом изменении данных.

Если серверу не удается выполнить обслуживание запроса [**WM \_ DDE \_**](wm-dde-advise.md) , он отправляет клиенту негативное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) . Но если сервер имеет доступ к элементу и может визуализировать его в запрошенном формате, сервер заносит новую ссылку (повторное обращение к флагам, указанным в параметре *хоптионс* ) и отправляет клиенту положительное сообщение **WM \_ DDE \_ ACK** . После этого, пока клиент не выдаст соответствующее сообщение [**WM \_ DDE \_ unadvise**](wm-dde-unadvise.md) , сервер отправляет клиенту новые данные каждый раз, когда изменяется значение элемента на сервере.

Сообщение [**WM \_ DDE \_ advise**](wm-dde-advise.md) устанавливает формат данных, которые будут передаваться на сервер при связи. Если клиент пытается установить другую связь с тем же элементом, но использует другой формат данных, сервер может отклонить второй формат данных или попытаться его поддерживать. Если для какого-либо элемента данных была установлена горячая связь, сервер может одновременно поддерживать только один формат данных. Это связано с тем, что сообщение [**\_ \_ данных WM DDE**](wm-dde-data.md) для горячего соединения имеет **пустой** обработчик данных, который в противном случае содержит сведения о формате. Таким же, сервер должен отклонять все горячие связи для элемента, который уже связан, и отклонять все ссылки для элемента, для которого имеются горячий ссылки. Другой интерпретацией может быть то, что сервер изменяет формат и горячее или теплое состояние ссылки при запросе второй ссылки на тот же элемент данных.

В общем случае клиентские приложения не должны пытаться одновременно устанавливать несколько ссылок на один элемент данных.

### <a name="initiating-a-data-link-with-the-paste-link-command"></a>Запуск связи с данными с помощью команды «вставить ссылку»

Приложения, поддерживающие каналы "горячий" или "теплый" канал данных, обычно поддерживают зарегистрированный формат буфера обмена с именем Link. При сопоставлении с командами копирования и вставки в приложении этот формат буфера обмена позволяет пользователю устанавливать сеанс DDE между приложениями просто путем копирования элемента данных в серверное приложение и вставки его в клиентское приложение.

Серверное приложение поддерживает формат буфера обмена Link, помещая в буфер обмена строку, содержащую имя приложения, раздела и элемента, когда пользователь выбирает команду **Копировать** в меню **Правка** . Ниже приведен стандартный формат ссылки.

*Приложение ***\\ 0***, раздел ***\\ 0***, элемент * * * \\ 0 \\ 0**

Один символ NULL отделяет имена, а два пустых символа завершают всю строку.

Клиентские и серверные приложения должны зарегистрировать формат буфера обмена ссылок, как показано ниже.


```
cfLink = RegisterClipboardFormat("Link");
```



Клиентское приложение поддерживает формат буфера обмена Link с помощью команды вставить ссылку в его меню Правка. Когда пользователь выбирает эту команду, клиентское приложение анализирует имена приложения, раздела и элемента из данных из буфера обмена формата ссылки. Используя эти имена, клиентское приложение инициирует диалог для приложения и раздела, если такой диалог еще не существует. Затем клиентское приложение отправляет в серверное приложение сообщение с предложением [**WM \_ DDE \_**](wm-dde-advise.md) , указывая имя элемента, которое содержится в данных буфера обмена формата ссылки.

Ниже приведен пример ответа клиентского приложения, когда пользователь выбирает команду Вставить ссылку.


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



В этом примере клиентское приложение открывает буфер обмена и определяет, содержит ли он данные в формате ссылки (т. е. Кфлинк), который был ранее зарегистрирован. Если это не так или не может блокировать данные в буфере обмена, клиент возвращает.

После того как клиентское приложение получит указатель на данные буфера обмена, он анализирует данные для извлечения имен приложения, раздела и элемента.

Клиентское приложение определяет, существует ли связь между этим разделом и серверным приложением. Если диалог существует, клиент проверяет, существует ли уже ссылка для элемента данных. Если такая ссылка существует, клиент отображает окно сообщения пользователю. в противном случае он вызывает собственную функцию *сендадвисе* для отправки на сервер сообщения с сообщением об ошибке [**WM \_ DDE \_**](wm-dde-advise.md) для элемента.

Если между клиентом и сервером не существует диалог, то клиент сначала вызывает собственную функцию *сендинитиате* для отправки сообщения об [**\_ \_ инициировании диалога WM DDE**](wm-dde-initiate.md) и, во-вторых, вызывает собственную функцию *финдсервергивенапптопик* , чтобы установить диалог с окном, отвечающим от имени серверного приложения. После начала диалога клиентское приложение вызывает *сендадвисе* для запроса ссылки.

### <a name="notifying-the-client-that-data-has-changed"></a>Уведомление клиента об изменении данных

Когда клиент устанавливает ссылку с помощью сообщения [**WM \_ DDE \_ advise**](wm-dde-advise.md) , если элемент **фдеферупд** не задан (то есть равен нулю) в структуре [**ддедата**](/windows/desktop/api/Dde/ns-dde-ddedata) , клиент запрашивает сервер отправку элемента данных при каждом изменении значения элемента. В таких случаях сервер отображает новое значение элемента данных в указанном ранее формате и отправляет клиенту сообщение с [**\_ \_ данными DDE WM**](wm-dde-data.md) , как показано в следующем примере.


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



В этом примере клиент обрабатывает значение элемента соответствующим образом. Если установлен флаг **факкрек** для элемента, клиент отправляет серверу положительное сообщение [**WM \_ DDE \_**](wm-dde-ack.md) .

Когда клиент устанавливает связь с набором элементов **фдеферупд** (то есть равным 1), клиент запрашивает, чтобы каждый раз при изменении данных отправлялись только уведомления, а не сами данные. В таких случаях при изменении значения элемента сервер не отображает значение, но просто отправляет клиенту сообщение [**\_ \_ данных WM DDE**](wm-dde-data.md) с нулевым маркером данных, как показано в следующем примере.


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



При необходимости клиент может запросить Последнее значение элемента данных, выполнив нормальное сообщение [**\_ \_ запроса DDE WM**](wm-dde-request.md) , или просто проигнорировать уведомление с сервера об изменении данных. В любом случае, если **факкрек** равен 1, клиент должен отправить на сервер положительное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) .

### <a name="terminating-a-data-link"></a>Завершение связи с данными

Если клиент запрашивает завершение работы определенного канала данных, клиент отправляет серверу сообщение [**WM \_ DDE \_ unadvise**](wm-dde-unadvise.md) , как показано в следующем примере.


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



Сервер проверяет, содержит ли клиент в данный момент ссылку на конкретный элемент в этом диалоге. Если ссылка существует, сервер отправляет клиенту положительное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) ; сервер больше не требуется для отправки обновлений об элементе. Если ссылка не существует, сервер отправляет клиенту негативное сообщение **WM \_ DDE \_ ACK** .

Сообщение [**WM \_ DDE \_ unadvise**](wm-dde-unadvise.md) указывает формат данных. Нулевой формат информирует сервер о необходимости присоединения всех ссылок для указанного элемента, даже если установлено несколько активных ссылок и используется другой формат.

Чтобы завершить все ссылки для диалога, клиентское приложение отправляет серверу сообщение [**WM \_ DDE \_ unadvise**](wm-dde-unadvise.md) с элементом Atom элемента null. Сервер определяет, имеется ли в настоящее время диалога хотя бы один канал. Если ссылка существует, сервер отправляет клиенту положительное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) ; сервер больше не должен отправлять обновления в диалоге. Если ссылка не существует, сервер отправляет клиенту негативное сообщение **WM \_ DDE \_ ACK** .

## <a name="carrying-out-commands-in-a-server-application"></a>Выполнение команд в серверном приложении

Приложения могут использовать сообщение [**\_ \_ выполнения WM DDE**](wm-dde-execute.md) , чтобы вызвать выполнение определенной команды или ряда команд в другом приложении. Для этого клиент отправляет серверу сообщение о **\_ \_ выполнении WM DDE** , содержащее маркер командной строки, как показано в следующем примере.


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



В этом примере сервер пытается выполнить указанную командную строку. В случае успешной работы сервер отправляет клиенту положительное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) ; в противном случае отправляется отрицательное сообщение **WM \_ DDE \_** . Это сообщение **WM \_ DDE \_ ACK** повторно использует маркер *хкомманд* , переданный в исходное [**сообщение \_ \_ выполнения WM DDE**](wm-dde-execute.md) .

Если строка выполнения команды клиента запрашивает завершение работы сервера, сервер должен ответить, отправив положительное сообщение [**WM \_ DDE \_**](wm-dde-ack.md) , а затем опубликовать сообщение о [**\_ \_ прерывании DDE WM**](wm-dde-terminate.md) , прежде чем завершать работу. Все остальные команды, отправляемые с сообщением [**\_ \_ выполнения WM DDE**](wm-dde-execute.md) , должны выполняться синхронно, то есть сервер должен отправить сообщение **WM \_ DDE \_ ACK** только после успешного завершения команды.

## <a name="terminating-a-conversation"></a>Завершение диалога

Как клиент, так и сервер могут выдавать сообщение о [**\_ \_ прерывании WM DDE**](wm-dde-terminate.md) для завершения диалога в любое время. Аналогично, как клиентские, так и серверные приложения должны быть готовы к получению этого сообщения в любое время. Перед завершением работы приложение должно завершить все его диалоги.

В следующем примере приложение, завершающее диалог, отправляет сообщение о [**\_ \_ завершении диалога WM DDE**](wm-dde-terminate.md) .


```
PostMessage(hwndServerDDE, WM_DDE_TERMINATE, 
    (WPARAM) hwndClientDDE, 0);
```



Это информирует другое приложение о том, что отправляющее приложение не будет отправлять дальнейшие сообщения, и получатель может закрыть его окно. Предполагается, что получатель отвечает на запросы немедленно, отправляя сообщение [**о \_ \_ прекращении DDE в WM**](wm-dde-terminate.md) . Получатель не должен отсылать отрицательное, занятое или положительное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) .

После того как приложение отправило сообщение об [**\_ \_ увольнении WM DDE**](wm-dde-terminate.md) участнику в сеансе DDE, оно не должно отвечать на сообщения от этого участника, так как участник мог уничтожить окно, в которое был отправлен ответ.

Если приложение получает сообщение DDE, отличное от [**WM \_ DDE \_**](wm-dde-terminate.md) , после того, как оно отправило **\_ \_ прерывание WM DDE**, оно должно освобождать все объекты, связанные с полученными сообщениями, за исключением дескрипторов данных для [**\_ \_ данных WM DDE**](wm-dde-data.md) или сообщений [**WM \_ DDE \_**](wm-dde-poke.md) , **не** имеющих набора элементов **фрелеасе** .

Когда приложение собирается завершить работу, оно должно завершить все активные сеансы DDE до завершения обработки сообщения [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) . Однако если приложение не заканчивает активные сеансы DDE, система завершит все сеансы DDE, связанные с окном, когда окно будет уничтожено. В следующем примере показано, как серверное приложение завершает все сеансы DDE.


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



 

 