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
# <a name="conversation-management"></a>Управление диалоговыми окнами

Диалог между клиентом и сервером всегда устанавливается по запросу клиента. При установке диалога каждый участник получает маркер, идентифицирующий диалог. Участники используют этот обработчик в других платформа динамических данных функциях библиотеки управления Exchange (ДДЕМЛ) для отправки транзакций и управления диалогом. Клиент может запросить диалог с одним сервером или запросить несколько диалогов с одним или несколькими серверами.

В следующих разделах описывается, как приложение устанавливает новые диалоги и получает сведения о существующих диалогах.

-   [Отдельные беседы](#single-conversations)
-   [Несколько диалогов](#multiple-conversations)

## <a name="single-conversations"></a>Отдельные беседы

Клиентское приложение запрашивает один диалог с сервером, вызывая функцию [**ддеконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) и указывая дескрипторы строк, которые определяют строки, содержащие имя службы серверного приложения и имя раздела диалога. ДДЕМЛ отвечает, отправляя транзакцию [**кстип \_ Connect**](xtyp-connect.md) в функцию обратного вызова платформа динамических данных Exchange (DDE) каждого серверного приложения, которое либо зарегистрировало имя службы, совпадающее с именем, указанным в **ддеконнект** , либо отключило фильтрацию имен служб, вызвав [**дденамесервице**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice). Сервер также может фильтровать транзакции **кстип \_ Connect** , УКАЗЫВАЯ \_ флаг фильтра КБФ Fail \_ Connections в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . Во время транзакции **кстип \_ Connect** ддемл передает имя службы и имя раздела на сервер. Сервер должен проверить имена и вернуть **значение true** , если он поддерживает имя службы и имя раздела, или **false** , если нет.

Если сервер не отвечает на запрос клиента на подключение, клиент получает **значение NULL** из [**ддеконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) , и диалог не устанавливается. Если сервер возвращает **значение true**, то устанавливается диалог и клиент получает маркер диалога — значение **DWORD** , идентифицирующее диалог. Клиент использует этот маркер в последующих вызовах ДДЕМЛ для получения данных с сервера. Сервер получает транзакцию [**кстип \_ Connect \_ Confirm**](xtyp-connect-confirm.md) (если только сервер не указал \_ \_ флаг фильтра Skip Connect КБФ \_ ). Эта транзакция передает обработчик диалога на сервер.

В следующем примере запрашивается диалог в системном разделе с сервером, который распознает имя службы MyServer. Параметры *хсзсервнаме* и *хсзсистопик* ранее создавали дескрипторы строк.


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



В предыдущем примере [**ддеконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) приводит к тому, что функция обратного вызова DDE приложения MyServer Получает транзакцию [**кстип \_ Connect**](xtyp-connect.md) .

В следующем примере сервер отвечает на транзакцию [**кстип \_ Connect**](xtyp-connect.md) , сравнивая строку имени раздела, обменяя ддемл, переданный на сервер, с каждым элементом массива строки имени раздела, который поддерживает сервер. Если сервер находит совпадение, он устанавливает диалог.


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



Если сервер возвращает **значение true** в ответ на транзакцию [**КСТИП \_ Connect**](xtyp-connect.md) , Ддемл отправляет транзакцию [**\_ \_ подтверждения кстип Connect**](xtyp-connect-confirm.md) в функцию обратного вызова DDE сервера. Сервер может получить обработчик для диалога, обрабатывая эту транзакцию.

Клиент может установить диалог с подстановочным знаком, указав **значение NULL** для обработчика строки имени службы, маркера строки имени раздела или и то, и другое в вызове [**ддеконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect). Если хотя бы один из дескрипторов строк имеет **значение NULL**, ддемл отправляет транзакцию [**кстип \_ вилдконнект**](xtyp-wildconnect.md) функциям обратного вызова всех приложений DDE (за исключением тех, кто отфильтрует транзакцию **кстип \_ вилдконнект** ). Каждое серверное приложение должно отвечать, возвращая обработчик данных, который определяет массив структур [**хсзпаир**](/windows/win32/api/ddeml/ns-ddeml-hszpair) , заканчивающийся нулем. Если серверное приложение не вызывало [**дденамесервице**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) для регистрации имен служб и если фильтрация включена, сервер не получает транзакции **кстип \_ вилдконнект** . Дополнительные сведения о дескрипторах данных см. в разделе [Управление данными](data-management.md).

Массив должен содержать одну структуру для каждой пары "имя службы" и "имя раздела", совпадающей с парой, заданной клиентом. ДДЕМЛ выбирает одну из пар для установления диалога и возвращает клиенту маркер, идентифицирующий диалог. ДДЕМЛ отправляет транзакцию [**кстип \_ Connect \_ Confirm**](xtyp-connect-confirm.md) на сервер (если только сервер не фильтрует эту транзакцию). В следующем примере показан типичный ответ сервера на транзакцию [**кстип \_ вилдконнект**](xtyp-wildconnect.md) .


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



Как клиент, так и сервер могут в любой момент завершить диалог, вызвав функцию [**ддедисконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) . Эта функция приводит к тому, что функция обратного вызова участника диалога в диалоге Получает транзакцию [**\_ отключения кстип**](xtyp-disconnect.md) (если только участник не указал \_ \_ флаг фильтра Skip unconnects КБФ). Как правило, приложение реагирует на транзакцию **\_ отключения кстип** , используя функцию [**ддекуериконвинфо**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) для получения сведений о завершенном диалоге. После того как функция обратного вызова возвращает из обработки транзакции **кстип \_ Disconnect** , этот обработчик больше не действителен.

Клиентское приложение, получающее транзакцию [**кстип \_ Disconnect**](xtyp-disconnect.md) в функции обратного вызова DDE, может попытаться восстановить диалог путем вызова функции [**ддереконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) . Клиент должен вызвать **ддереконнект** из функции обратного вызова DDE.

## <a name="multiple-conversations"></a>Несколько диалогов

Клиентское приложение может использовать функцию [**ддеконнектлист**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) , чтобы определить, доступны ли какие-либо серверы в системе. Клиент указывает имя службы и имя раздела при вызове **ддеконнектлист**, что приводит к тому, что ддемл передает транзакцию [**кстип \_ вилдконнект**](xtyp-wildconnect.md) в функции обратного вызова DDE всех серверов, которые соответствуют имени службы (за исключением тех, которые фильтруют транзакцию). Функция обратного вызова сервера должна возвращать маркер данных, который определяет массив структур [**хсзпаир**](/windows/win32/api/ddeml/ns-ddeml-hszpair) , заканчивающийся нулем. Массив должен содержать одну структуру для каждой пары "имя службы" и "имя раздела", совпадающей с парой, заданной клиентом. ДДЕМЛ устанавливает диалог для каждой структуры **хсзпаир** , заполненной сервером, и возвращает клиенту маркер списка диалогов. Сервер получает обработчик диалога посредством транзакции [**кстип \_ Connect**](xtyp-connect.md) (если только сервер не фильтрует эту транзакцию).

Клиент может указать **значение NULL** для имени службы, имени раздела или и того, и другого при вызове [**ддеконнектлист**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist). Если имя службы равно **null**, все серверы в системе, которые поддерживают указанное имя раздела, отвечают. Диалог устанавливается с каждым отвечающим сервером, в том числе с несколькими экземплярами одного и того же сервера. Если имя раздела равно **null**, то для каждого раздела, распознаваемого каждым сервером, который соответствует имени службы, устанавливается диалог.

Клиент может использовать функции [**ддекуеринекстсервер**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) и [**ддекуериконвинфо**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) для обнаружения серверов, которые отвечают на [**ддеконнектлист**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist). **Ддекуеринекстсервер** возвращает следующий обработчик диалога в списке бесед, а **Ддекуериконвинфо** заполняет структуру [**конвинфо**](/windows/win32/api/ddeml/ns-ddeml-convinfo) информацией о диалоге. Клиент может сохранять необходимые дескрипторы диалога и удалять остальные из списка бесед.

В следующем примере [**ддеконнектлист**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) используется для установки диалогов со всеми серверами, которые поддерживают системный раздел, а затем использует функции [**ддекуеринекстсервер**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) и [**ддекуериконвинфо**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) для получения дескрипторов строк имени службы серверов и сохранения их в буфер.


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



Приложение может завершить отдельный диалог в списке бесед, вызвав функцию [**ддедисконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) . Приложение может завершить все диалоги в списке бесед, вызвав функцию [**ддедисконнектлист**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) . Обе функции приводят к тому, что ДДЕМЛ отправляет транзакции [**кстип \_ Disconnect**](xtyp-disconnect.md) в функцию обратного вызова DDE каждого участника. **Ддедисконнектлист** отправляет транзакцию **\_ отключения кстип** для каждого обработчика диалога в списке.

Клиент может получить список дескрипторов диалога в списке бесед, передав существующий дескриптор списка диалогов в [**ддеконнектлист**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist). В процессе перечисления удаляются дескрипторы прерванных диалогов из списка, а также добавляются недублирующиеся диалоги, которые соответствуют указанному имени службы и имени раздела.

Если [**ддеконнектлист**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) указывает существующий дескриптор списка диалогов, функция создает новый список диалогов, содержащий дескрипторы всех новых диалогов и дескрипторов из существующего списка.

Если существуют дублирующиеся беседы, [**ддеконнектлист**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) пытается предотвратить дублирование дескрипторов диалога в списке бесед. Дубликат диалога — это второй диалог с одним и тем же сервером с тем же именем службы и именем раздела. Два таких диалога будут иметь различные дескрипторы, но они будут обозначать один и тот же диалог.

 

 




