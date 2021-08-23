---
description: В этом разделе приводятся соответствующие примеры кода для основных шагов разработки приложения разговора с помощью API одноранговой группировки, предоставляя контекст для каждого вызова API.
ms.assetid: 47bb8606-0b7b-4e71-9d6f-c400d6a82e43
title: Создание приложения группы чата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb8f9458f8e01bea86e42f0cd976395e951bda52f13af46952479d5810e46c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011662"
---
# <a name="creating-a-group-chat-application"></a>Создание приложения группы чата

В этом разделе приводятся соответствующие примеры кода для основных шагов разработки приложения разговора с помощью API одноранговой группировки, предоставляя контекст для каждого вызова API. Поведения пользовательского интерфейса и общая структура приложения не включены.

> [!Note]  
> Пример приложения "полный доступ к одноранговой группе" приведен в пакете SDK для одноранговой группы. Этот раздел ссылается на функции, предоставляемые в примере.

 

## <a name="initializing-a-group"></a>Инициализация группы

Первым шагом при создании приложения для разговора является инициализация инфраструктуры однорангового группирования путем вызова [**пирграупстартуп**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) с самой высокой поддерживаемой версией. В этом случае **\_ \_ версия одноранговой группы** будет определена в файле заголовка приложения. Версия, которая действительно поддерживается инфраструктурой, возвращается в **пирверсион**.


```C++
    PEER_VERSION_DATA peerVersion;

    hr = PeerGroupStartup(PEER_GROUP_VERSION, &peerVersion);
    if (FAILED(hr))
    {
        return hr;
    }
```



## <a name="creating-a-group"></a>Создание группы

Приложение для разговора должно иметь возможность создать одноранговую группу, если она недоступна, или если пользователь приложения хочет создать новое соединение. Для этого необходимо создать структуру [**свойств одноранговой \_ группы \_**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) и заполнить ее начальными параметрами группы, включая классификатор для одноранговой группы, понятное имя, имя однорангового узла создателя и время существования присутствия. После заполнения этой структуры она передается в [**пирграупкреате**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).


```C++
//-----------------------------------------------------------------------------
// Function: CreateGroup
//
// Purpose:  Creates a new group with the friendly name.
//
// Returns:  HRESULT
//
HRESULT CreateGroup(PCWSTR pwzName, PCWSTR pwzIdentity)
{
    HRESULT hr = S_OK;
    PEER_GROUP_PROPERTIES props = {0};

    if (SUCCEEDED(hr))
    {
        if ((NULL == pwzName) || (0 == *pwzName))
        {
            hr = E_INVALIDARG;
            DisplayHrError(L"Please enter a group name.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        CleanupGroup( );

        props.dwSize = sizeof(props);
        props.pwzClassifier = L"SampleChatGroup";
        props.pwzFriendlyName = (PWSTR) pwzName;
        props.pwzCreatorPeerName = (PWSTR) pwzIdentity;

        hr = PeerGroupCreate(&props, &g_hGroup);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to create a new group.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = PrepareToChat( );
    }

    return hr;
}
```



## <a name="issuing-invitations"></a>Выдача приглашений

При выдаче приглашения необходимо получить Гмкс приглашений. Их можно получить, вызвав [**пиридентитижетксмл**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) в приглашении с именем удостоверения. В случае успеха сведения об удостоверении (XML-код, содержащий сертификат в кодировке Base-64 с открытым ключом RSA) записываются во внешнее расположение (в этом примере — файл), где он может получить его и использовать для создания приглашения.

На этом этапе необходимо установить механизм доставки приглашения приглашению. Это может быть электронная почта или другой безопасный метод обмена файлами. В приведенном ниже примере приглашение записывается в файл, который затем можно передать на компьютер приглашения.


```C++
//-----------------------------------------------------------------------------
// Function: SaveIdentityInfo
//
// Purpose:  Saves the information for an identity to a file.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT SaveIdentityInfo(PCWSTR pwzIdentity, PCWSTR pwzFile)
{
    PWSTR pwzXML = NULL;
    HRESULT hr = PeerIdentityGetXML(pwzIdentity, &pwzXML);

    if (FAILED(hr))
    {
        DisplayHrError(L"Unable to retrieve the XML data for the identity.", hr);
    }
    else
    {
        FILE *fp = NULL;
        errno_t err = 0;

        err = _wfopen_s(&fp, pwzFile, L"wb");
        if (err != 0)
        {
            hr = E_FAIL;
            DisplayHrError(L"Please choose a valid path", hr);
        }
        else
        {
            if (fputws(pwzXML, fp) == WEOF)
            {
                hr = E_FAIL;
                DisplayHrError(L"End of file error.", hr);
            }
            fclose(fp);
        }

        PeerFreeData(pwzXML);
    }

    return hr;
}
```



Приглашения, как и удостоверения, также выдаются извне. В этом примере приглашение записывается в файл с **fputws** , где приглашение может получить его и использовать при вызове [**пирграупжоин**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).


```C++
//-----------------------------------------------------------------------------
// Function: CreateInvitation
//
// Purpose:  Creates an invitation file for an identity.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT CreateInvitation(PCWSTR wzIdentityInfoPath, PCWSTR wzInvitationPath)
{
    HRESULT hr = S_OK;
    WCHAR wzIdentityInfo[MAX_INVITATION] = {0};
    PWSTR pwzInvitation = NULL;
    errno_t  err  = 0;
    FILE *file = NULL;
        
    err = _wfopen_s(&file, wzIdentityInfoPath, L"rb");
    if (err != 0)
    {
        hr = E_FAIL;
        DisplayHrError(L"Please choose a valid path to the identity information file.", hr);
    }
    else
    {
        fread(wzIdentityInfo, sizeof(WCHAR), MAX_INVITATION, file);
        if (ferror(file))
        {
            hr = E_FAIL;
            DisplayHrError(L"File read error occurred.", hr);
        }
        fclose(file);
    }

    if (SUCCEEDED(hr))
    {
        ULONGLONG ulExpire; // adjust time using this structure
        GetSystemTimeAsFileTime((FILETIME *)&ulExpire);

        // 15days in 100 nanoseconds resolution
        ulExpire += ((ULONGLONG) (60 * 60 * 24 * 15)) * ((ULONGLONG)1000*1000*10);

        hr = PeerGroupCreateInvitation(g_hGroup, wzIdentityInfo, (FILETIME*)&ulExpire, 1, (PEER_ROLE_ID*) &PEER_GROUP_ROLE_MEMBER, &pwzInvitation);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to create the invitation.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        err = _wfopen_s(&file, wzInvitationPath, L"wb");
        if (err != 0)
        {
            hr = E_FAIL;
            DisplayHrError(L"Please choose a valid path to the invitation file.", hr);
        }
        else
        {
            if (fputws(pwzInvitation, file) == WEOF)
            {
                hr = E_FAIL;
                DisplayHrError(L"End of file error.", hr);
            }
            fclose(file);
        }
    }

    PeerFreeData(pwzInvitation);
    return hr;
}
```



## <a name="joining-a-peer-group"></a>Присоединение к одноранговой группе

Если одноранговая группа пытается присоединиться к одноранговой группе, она потребует приглашения от этого узла. Приглашения доставляются внешним процессом или приложением в приглашение и сохраняются в локальном файле, указанном в примере ниже как *пвзфиленаме*. Двоичный объект приглашения XML считывается из файла в **взинвитатион** и передается в [**пирграупжоин**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).


```C++
//-----------------------------------------------------------------------------
// Function: JoinGroup
//
// Purpose:  Uses the invitation to join a group with a specific identity.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT JoinGroup(PCWSTR pwzIdentity, PCWSTR pwzFileName)
{
    HRESULT hr = S_OK;
    WCHAR wzInvitation[MAX_INVITATION] = {0};
    FILE        *file = NULL;
    errno_t     err;

    err = _wfopen_s(&file, pwzFileName, L"rb");
    if (err !=  0)
    {
        hr = E_FAIL;
        DisplayHrError(L"Error opening group invitation file", hr);
        return hr;
    }
    else
    {
        fread(wzInvitation, sizeof(WCHAR), MAX_INVITATION, file);
        if (ferror(file))
        {
            hr = E_FAIL;
            DisplayHrError(L"File read error occurred.", hr);
        }
        fclose(file);

        hr = PeerGroupJoin(pwzIdentity, wzInvitation, NULL, &g_hGroup);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to join group.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = PrepareToChat( );
    }

    return hr;
}
```



## <a name="register-for-peer-events"></a>Регистрация для событий одноранговых узлов

Перед подключением необходимо зарегистрироваться для каждого события однорангового узла, относящегося к приложению. В приведенном ниже примере регистрируются следующие события:

-   запись события одноранговой \_ группы \_ \_ \_ изменена. Поскольку записи будут использоваться для хранения общедоступных сообщений разговора, приложение должно получать уведомления при каждом добавлении нового. При получении этого однорангового события данные события предоставляют запись с сообщением разговора. Приложения должны регистрироваться только для тех типов записей, для которых они предназначены для непосредственного управления.
-   член события одноранговой \_ группы \_ \_ \_ изменен. Приложение должно получать уведомления, когда участники присоединяются к одноранговой группе или оставляют ее, чтобы список участников можно было обновить соответствующим образом.
-   состояние события одноранговой \_ группы \_ \_ \_ изменилось. Изменения в состоянии одноранговой группы должны быть переданы в приложение. Член одноранговой группы считается доступным в одноранговой группе только в том случае, если его состояние указывает на то, что оно подключено к группе, синхронизировано с базой данных записи одноранговой группы и активно ожидает обновления записи.
-   \_ \_ прямое соединение с событием одноранговой группы \_ \_ . Конфиденциальные сообщения между двумя членами и обменом данными должны осуществляться через прямое соединение, поэтому приложение должно иметь возможность обрабатывать прямые запросы на подключение.
-   \_ \_ входящие данные события одноранговой группы \_ \_ . После инициирования прямого подключения это событие однорангового узла оповещает приложение о получении частного сообщения.


```C++
//-----------------------------------------------------------------------------
// Function: RegisterForEvents
//
// Purpose:  Registers the EventCallback function so it will be called for only
//           those events that are specified.
//
// Returns:  HRESULT
//
HRESULT RegisterForEvents(void)
{
    HRESULT hr = S_OK;
    PEER_GROUP_EVENT_REGISTRATION regs[] = {
        { PEER_GROUP_EVENT_RECORD_CHANGED, &RECORD_TYPE_CHAT_MESSAGE },
        { PEER_GROUP_EVENT_MEMBER_CHANGED, 0 },
        { PEER_GROUP_EVENT_STATUS_CHANGED, 0 },
        { PEER_GROUP_EVENT_DIRECT_CONNECTION, &DATA_TYPE_WHISPER_MESSAGE },
        { PEER_GROUP_EVENT_INCOMING_DATA, 0 },
    };

    g_hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (g_hEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    else
    {
        hr = PeerGroupRegisterEvent(g_hGroup, g_hEvent, celems(regs), regs,  &g_hPeerEvent);
    }

    if (SUCCEEDED(hr))
    {
        if (!RegisterWaitForSingleObject(&g_hWait, g_hEvent, EventCallback, NULL, INFINITE, WT_EXECUTEDEFAULT))
        {
            hr = E_UNEXPECTED;
        }
    }

    return hr;
}
```



## <a name="connecting-to-a-peer-group"></a>Подключение к одноранговой группе

Если вы создали или присоединили группу и зарегистрировались для соответствующих событий, пора перейти в Интернет и начать сеанс разговора. Для этого вызовите [**пирграупконнект**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) и передайте маркер группы, полученный из [**пирграупкреате**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) или [**пирграупжоин**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin). После вызова этого сообщения разговора будут получены как \_ \_ \_ события изменения записи событий одноранговой группы \_ .

## <a name="obtaining-a-list-of-peer-group-members"></a>Получение списка членов одноранговой группы

Получение списка членов, подключенных к одноранговой группе, является простым: вызовите [**пирграупенуммемберс**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) , чтобы получить список членов группы, а затем последовательно вызовите [**пиржетнекститем**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) , пока не будут получены все элементы. Необходимо вызвать [**пирфридата**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) после обработки каждой структуры-члена, и необходимо закрыть перечисление, вызвав [**пиренденумератион**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) , когда обработка завершена.


```C++
//-----------------------------------------------------------------------------
// Function: UpdateParticipantList
//
// Purpose:  Update the list of partipants.
//
// Returns:  nothing
//
void UpdateParticipantList(void)
{
    HRESULT          hr = S_OK;
    HPEERENUM        hPeerEnum = NULL;
    PEER_MEMBER   ** ppMember = NULL;

    ClearParticipantList( );
    if (NULL == g_hGroup)
    {
        return;
    }

    // Retrieve only the members currently present in the group.
    hr = PeerGroupEnumMembers(g_hGroup, PEER_MEMBER_PRESENT, NULL, &hPeerEnum);
    if (SUCCEEDED(hr))
    {
        while (SUCCEEDED(hr))
        {
            ULONG cItem = 1;
            hr = PeerGetNextItem(hPeerEnum, &cItem, (PVOID **) &ppMember);
            if (SUCCEEDED(hr))
            {
                if (0 == cItem)
                {
                    PeerFreeData(ppMember);
                    break;
                }
            }

            if (SUCCEEDED(hr))
            {
                if (0 != ((*ppMember)->dwFlags & PEER_MEMBER_PRESENT))
                {
                    AddParticipantName((*ppMember)->pwzIdentity, (*ppMember)->pCredentialInfo->pwzFriendlyName);
                }
                PeerFreeData(ppMember);
            }
        }

        PeerEndEnumeration(hPeerEnum);
    }
}
```



## <a name="sending-a-chat-message"></a>Отправка сообщения разговора

В этом примере сообщение разговора отправляется путем помещения его в поле **данных** структуры [**одноранговой \_ записи**](/windows/desktop/api/P2P/ns-p2p-peer_record) . Запись добавляется в записи одноранговой группы путем вызова [**пирграупаддрекорд**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord), который будет публиковать ее и вызвать \_ \_ событие изменения записи события одноранговой группы \_ \_ на всех узлах, участвующих в одноранговой группе.


```C++
//-----------------------------------------------------------------------------
// Function: AddChatRecord
//
// Purpose:  This adds a new chat message record to the group.
//
// Returns:  HRESULT
//
HRESULT AddChatRecord(PCWSTR pwzMessage)
{
    HRESULT     hr = S_OK;
    PEER_RECORD record = {0};
    GUID        idRecord;
    ULONGLONG   ulExpire;
    ULONG cch = (ULONG) wcslen(pwzMessage);

    GetSystemTimeAsFileTime((FILETIME *) &ulExpire);

    // Calculate a 2 minute expiration time in 100 nanosecond resolution
    ulExpire += ((ULONGLONG) 60 * 2) * ((ULONGLONG)1000*1000*10);

    // Set up the record
    record.dwSize = sizeof(record);
    record.data.cbData = (cch+1) * sizeof(WCHAR);
    record.data.pbData = (PBYTE) pwzMessage;
    memcpy(&record.ftExpiration, &ulExpire, sizeof(ulExpire));

    PeerGroupUniversalTimeToPeerTime(g_hGroup, &record.ftExpiration, &record.ftExpiration);

    // Set the record type GUID
    record.type = RECORD_TYPE_CHAT_MESSAGE;

    // Add the record to the database
    hr = PeerGroupAddRecord(g_hGroup, &record, &idRecord);
    if (FAILED(hr))
    {
        DisplayHrError(L"Failed to add a chat record to the group.", hr);
    }

    return hr;
}
```



## <a name="receiving-a-chat-message"></a>Получение сообщения разговора

Чтобы получить сообщение разговора, создайте функцию обратного вызова для \_ \_ события изменения записи события одноранговой группы \_ \_ , которое вызывает функцию, аналогичную показанной ниже. Запись получается путем вызова [**пирграупжетрекорд**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) для данных события, полученных предыдущим вызовом [**пирграупжетевентдата**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) в функции обратного вызова. Сообщение разговора хранится в поле **данных** этой записи.


```C++
//-----------------------------------------------------------------------------
// Function: ProcessRecordChanged
//
// Purpose:  Processes the PEER_GROUP_EVENT_RECORD_CHANGED event.
//
// Returns:  nothing
//
void ProcessRecordChanged(PEER_EVENT_RECORD_CHANGE_DATA * pData)
{
    switch (pData->changeType)
    {
        case PEER_RECORD_ADDED:
            if (IsEqualGUID(&pData->recordType, &RECORD_TYPE_CHAT_MESSAGE))
            {
                PEER_RECORD * pRecord = {0};
                HRESULT hr = PeerGroupGetRecord(g_hGroup, &pData->recordId, &pRecord);
                if (SUCCEEDED(hr))
                {
                    DisplayChatMessage(pRecord->pwzCreatorId, (PCWSTR) pRecord->data.pbData);
                    PeerFreeData(pRecord);
                }
            }
            break;

        case PEER_RECORD_UPDATED:
        case PEER_RECORD_DELETED:
        case PEER_RECORD_EXPIRED:
            break;

        default:
            break;
    }
}
```



 

 



