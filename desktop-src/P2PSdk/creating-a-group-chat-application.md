---
description: В этом разделе приводятся соответствующие примеры кода для основных шагов разработки приложения разговора с помощью API одноранговой группировки, предоставляя контекст для каждого вызова API.
ms.assetid: 47bb8606-0b7b-4e71-9d6f-c400d6a82e43
title: Создание приложения группы чата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676d4e9913934024df3131c0f965a5d85477d148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345542"
---
# <a name="creating-a-group-chat-application"></a><span data-ttu-id="06167-103">Создание приложения группы чата</span><span class="sxs-lookup"><span data-stu-id="06167-103">Creating a Group Chat Application</span></span>

<span data-ttu-id="06167-104">В этом разделе приводятся соответствующие примеры кода для основных шагов разработки приложения разговора с помощью API одноранговой группировки, предоставляя контекст для каждого вызова API.</span><span class="sxs-lookup"><span data-stu-id="06167-104">This topic provides relevant code samples for the major steps of developing a chat application with the Peer Grouping API, providing a context for each API call.</span></span> <span data-ttu-id="06167-105">Поведения пользовательского интерфейса и общая структура приложения не включены.</span><span class="sxs-lookup"><span data-stu-id="06167-105">UI behaviors and overall application structure are not included.</span></span>

> [!Note]  
> <span data-ttu-id="06167-106">Пример приложения "полный доступ к одноранговой группе" приведен в пакете SDK для одноранговой группы.</span><span class="sxs-lookup"><span data-stu-id="06167-106">The complete Peer Group Chat sample application is provided in the Peer SDK.</span></span> <span data-ttu-id="06167-107">Этот раздел ссылается на функции, предоставляемые в примере.</span><span class="sxs-lookup"><span data-stu-id="06167-107">This topic references functions provided within the sample.</span></span>

 

## <a name="initializing-a-group"></a><span data-ttu-id="06167-108">Инициализация группы</span><span class="sxs-lookup"><span data-stu-id="06167-108">Initializing a Group</span></span>

<span data-ttu-id="06167-109">Первым шагом при создании приложения для разговора является инициализация инфраструктуры однорангового группирования путем вызова [**пирграупстартуп**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) с самой высокой поддерживаемой версией.</span><span class="sxs-lookup"><span data-stu-id="06167-109">The first step when constructing a chat application is to initialize the Peer Grouping Infrastructure by calling [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) with the highest supported version.</span></span> <span data-ttu-id="06167-110">В этом случае **\_ \_ версия одноранговой группы** будет определена в файле заголовка приложения.</span><span class="sxs-lookup"><span data-stu-id="06167-110">In this case, **PEER\_GROUP\_VERSION** will be defined in the application header file.</span></span> <span data-ttu-id="06167-111">Версия, которая действительно поддерживается инфраструктурой, возвращается в **пирверсион**.</span><span class="sxs-lookup"><span data-stu-id="06167-111">The version actually supported by the infrastructure is returned in **peerVersion**.</span></span>


```C++
    PEER_VERSION_DATA peerVersion;

    hr = PeerGroupStartup(PEER_GROUP_VERSION, &peerVersion);
    if (FAILED(hr))
    {
        return hr;
    }
```



## <a name="creating-a-group"></a><span data-ttu-id="06167-112">Создание группы</span><span class="sxs-lookup"><span data-stu-id="06167-112">Creating a Group</span></span>

<span data-ttu-id="06167-113">Приложение для разговора должно иметь возможность создать одноранговую группу, если она недоступна, или если пользователь приложения хочет создать новое соединение.</span><span class="sxs-lookup"><span data-stu-id="06167-113">A chat application must be able to create a peer group if no group is available to join, or if the application user wants to create a new one.</span></span> <span data-ttu-id="06167-114">Для этого необходимо создать структуру [**свойств одноранговой \_ группы \_**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) и заполнить ее начальными параметрами группы, включая классификатор для одноранговой группы, понятное имя, имя однорангового узла создателя и время существования присутствия.</span><span class="sxs-lookup"><span data-stu-id="06167-114">To do this, you must create a [**PEER\_GROUP\_PROPERTIES**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) structure and populate it with the initial settings for the group, including the classifier for the peer group, the friendly name, the creator's peer name, and the presence lifetime.</span></span> <span data-ttu-id="06167-115">После заполнения этой структуры она передается в [**пирграупкреате**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).</span><span class="sxs-lookup"><span data-stu-id="06167-115">Once this structure has been populated, you pass it to [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).</span></span>


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



## <a name="issuing-invitations"></a><span data-ttu-id="06167-116">Выдача приглашений</span><span class="sxs-lookup"><span data-stu-id="06167-116">Issuing Invitations</span></span>

<span data-ttu-id="06167-117">При выдаче приглашения необходимо получить Гмкс приглашений.</span><span class="sxs-lookup"><span data-stu-id="06167-117">When issuing an invitation, the GMCs of the invitees must be obtained.</span></span> <span data-ttu-id="06167-118">Их можно получить, вызвав [**пиридентитижетксмл**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) в приглашении с именем удостоверения.</span><span class="sxs-lookup"><span data-stu-id="06167-118">These can obtained by calling [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) on the invitee with their identity name.</span></span> <span data-ttu-id="06167-119">В случае успеха сведения об удостоверении (XML-код, содержащий сертификат в кодировке Base-64 с открытым ключом RSA) записываются во внешнее расположение (в этом примере — файл), где он может получить его и использовать для создания приглашения.</span><span class="sxs-lookup"><span data-stu-id="06167-119">If successful, the identity information (the XML that contains the base-64 encoded certificate with the RSA public key) is written to an external location (a file, in this sample) where the inviter can obtain it and use it to create an invitation.</span></span>

<span data-ttu-id="06167-120">На этом этапе необходимо установить механизм доставки приглашения приглашению.</span><span class="sxs-lookup"><span data-stu-id="06167-120">At this point, a mechanism for the delivery of the invitation to the invitee must be established.</span></span> <span data-ttu-id="06167-121">Это может быть электронная почта или другой безопасный метод обмена файлами.</span><span class="sxs-lookup"><span data-stu-id="06167-121">This can be email or another secure method of file exchange.</span></span> <span data-ttu-id="06167-122">В приведенном ниже примере приглашение записывается в файл, который затем можно передать на компьютер приглашения.</span><span class="sxs-lookup"><span data-stu-id="06167-122">In the sample below, the invitation is written to a file which can then be transferred to the invitee's computer.</span></span>


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



<span data-ttu-id="06167-123">Приглашения, как и удостоверения, также выдаются извне.</span><span class="sxs-lookup"><span data-stu-id="06167-123">Invitations, like identities, are also issued externally.</span></span> <span data-ttu-id="06167-124">В этом примере приглашение записывается в файл с **fputws** , где приглашение может получить его и использовать при вызове [**пирграупжоин**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span><span class="sxs-lookup"><span data-stu-id="06167-124">In this example, the invitation is written to a file with **fputws** where the invitee can obtain it and use it when it calls [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span>


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



## <a name="joining-a-peer-group"></a><span data-ttu-id="06167-125">Присоединение к одноранговой группе</span><span class="sxs-lookup"><span data-stu-id="06167-125">Joining a Peer Group</span></span>

<span data-ttu-id="06167-126">Если одноранговая группа пытается присоединиться к одноранговой группе, она потребует приглашения от этого узла.</span><span class="sxs-lookup"><span data-stu-id="06167-126">If the peer is attempting to join a peer group created by another peer, it will need an invitation from that peer.</span></span> <span data-ttu-id="06167-127">Приглашения доставляются внешним процессом или приложением в приглашение и сохраняются в локальном файле, указанном в примере ниже как *пвзфиленаме*.</span><span class="sxs-lookup"><span data-stu-id="06167-127">Invitations are delivered by an external process or application to the invitee and saved to a local file, specified in the sample below as *pwzFileName*.</span></span> <span data-ttu-id="06167-128">Двоичный объект приглашения XML считывается из файла в **взинвитатион** и передается в [**пирграупжоин**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span><span class="sxs-lookup"><span data-stu-id="06167-128">The invitation XML blob is read from the file into **wzInvitation** and passed to [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span>


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



## <a name="register-for-peer-events"></a><span data-ttu-id="06167-129">Регистрация для событий одноранговых узлов</span><span class="sxs-lookup"><span data-stu-id="06167-129">Register for Peer Events</span></span>

<span data-ttu-id="06167-130">Перед подключением необходимо зарегистрироваться для каждого события однорангового узла, относящегося к приложению.</span><span class="sxs-lookup"><span data-stu-id="06167-130">Before connecting, you should register for every peer event pertinent to the application.</span></span> <span data-ttu-id="06167-131">В приведенном ниже примере регистрируются следующие события:</span><span class="sxs-lookup"><span data-stu-id="06167-131">In the example below, you register for the following events:</span></span>

-   <span data-ttu-id="06167-132">запись события одноранговой \_ группы \_ \_ \_ изменена.</span><span class="sxs-lookup"><span data-stu-id="06167-132">PEER\_GROUP\_EVENT\_RECORD\_CHANGED.</span></span> <span data-ttu-id="06167-133">Поскольку записи будут использоваться для хранения общедоступных сообщений разговора, приложение должно получать уведомления при каждом добавлении нового.</span><span class="sxs-lookup"><span data-stu-id="06167-133">Since records will be used to contain public chat messages, the application must be notified every time a new one is added.</span></span> <span data-ttu-id="06167-134">При получении этого однорангового события данные события предоставляют запись с сообщением разговора.</span><span class="sxs-lookup"><span data-stu-id="06167-134">When this peer event is received, the event data exposes the record with the chat message.</span></span> <span data-ttu-id="06167-135">Приложения должны регистрироваться только для тех типов записей, для которых они предназначены для непосредственного управления.</span><span class="sxs-lookup"><span data-stu-id="06167-135">Applications should only register for those record types they intend to handle directly.</span></span>
-   <span data-ttu-id="06167-136">член события одноранговой \_ группы \_ \_ \_ изменен.</span><span class="sxs-lookup"><span data-stu-id="06167-136">PEER\_GROUP\_EVENT\_MEMBER\_CHANGED.</span></span> <span data-ttu-id="06167-137">Приложение должно получать уведомления, когда участники присоединяются к одноранговой группе или оставляют ее, чтобы список участников можно было обновить соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="06167-137">The application must be notified when members join or leave the peer group so the list of participants can be updated accordingly.</span></span>
-   <span data-ttu-id="06167-138">состояние события одноранговой \_ группы \_ \_ \_ изменилось.</span><span class="sxs-lookup"><span data-stu-id="06167-138">PEER\_GROUP\_EVENT\_STATUS\_CHANGED.</span></span> <span data-ttu-id="06167-139">Изменения в состоянии одноранговой группы должны быть переданы в приложение.</span><span class="sxs-lookup"><span data-stu-id="06167-139">Changes to the peer group status must be conveyed to the application.</span></span> <span data-ttu-id="06167-140">Член одноранговой группы считается доступным в одноранговой группе только в том случае, если его состояние указывает на то, что оно подключено к группе, синхронизировано с базой данных записи одноранговой группы и активно ожидает обновления записи.</span><span class="sxs-lookup"><span data-stu-id="06167-140">A peer group member is only considered to be available within the peer group when its status indicates that it is connected to the group, synchronized with the peer group record database, and actively listening to record updates.</span></span>
-   <span data-ttu-id="06167-141">\_ \_ прямое соединение с событием одноранговой группы \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="06167-141">PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION.</span></span> <span data-ttu-id="06167-142">Конфиденциальные сообщения между двумя членами и обменом данными должны осуществляться через прямое соединение, поэтому приложение должно иметь возможность обрабатывать прямые запросы на подключение.</span><span class="sxs-lookup"><span data-stu-id="06167-142">Private messages between two members and exchanges of data must be conducted over a direct connection, so the application must be able to handle direct connection requests.</span></span>
-   <span data-ttu-id="06167-143">\_ \_ входящие данные события одноранговой группы \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="06167-143">PEER\_GROUP\_EVENT\_INCOMING\_DATA.</span></span> <span data-ttu-id="06167-144">После инициирования прямого подключения это событие однорангового узла оповещает приложение о получении частного сообщения.</span><span class="sxs-lookup"><span data-stu-id="06167-144">After a direct connection is initiated, this peer event alerts the application that a private message has been received.</span></span>


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



## <a name="connecting-to-a-peer-group"></a><span data-ttu-id="06167-145">Подключение к одноранговой группе</span><span class="sxs-lookup"><span data-stu-id="06167-145">Connecting to a Peer Group</span></span>

<span data-ttu-id="06167-146">Если вы создали или присоединили группу и зарегистрировались для соответствующих событий, пора перейти в Интернет и начать сеанс разговора.</span><span class="sxs-lookup"><span data-stu-id="06167-146">Having either created or joined the group and registered for the appropriate events, it's time to go online and begin an active chat session.</span></span> <span data-ttu-id="06167-147">Для этого вызовите [**пирграупконнект**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) и передайте маркер группы, полученный из [**пирграупкреате**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) или [**пирграупжоин**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span><span class="sxs-lookup"><span data-stu-id="06167-147">To do this, you call [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) and pass in the group handle obtained from [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) or [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span> <span data-ttu-id="06167-148">После вызова этого сообщения разговора будут получены как \_ \_ \_ события изменения записи событий одноранговой группы \_ .</span><span class="sxs-lookup"><span data-stu-id="06167-148">After calling this, chat messages will be received as PEER\_GROUP\_EVENT\_RECORD\_CHANGED events.</span></span>

## <a name="obtaining-a-list-of-peer-group-members"></a><span data-ttu-id="06167-149">Получение списка членов одноранговой группы</span><span class="sxs-lookup"><span data-stu-id="06167-149">Obtaining a List of Peer Group Members</span></span>

<span data-ttu-id="06167-150">Получение списка членов, подключенных к одноранговой группе, является простым: вызовите [**пирграупенуммемберс**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) , чтобы получить список членов группы, а затем последовательно вызовите [**пиржетнекститем**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) , пока не будут получены все элементы.</span><span class="sxs-lookup"><span data-stu-id="06167-150">Obtaining a list of members connected to the peer group is simple: call [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) to retrieve the list of group members, and then iteratively call [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) until all members are retrieved.</span></span> <span data-ttu-id="06167-151">Необходимо вызвать [**пирфридата**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) после обработки каждой структуры-члена, и необходимо закрыть перечисление, вызвав [**пиренденумератион**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) , когда обработка завершена.</span><span class="sxs-lookup"><span data-stu-id="06167-151">You should call [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) after you process each member structure, and you must close the enumeration by calling [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) when processing is complete.</span></span>


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



## <a name="sending-a-chat-message"></a><span data-ttu-id="06167-152">Отправка сообщения разговора</span><span class="sxs-lookup"><span data-stu-id="06167-152">Sending a Chat Message</span></span>

<span data-ttu-id="06167-153">В этом примере сообщение разговора отправляется путем помещения его в поле **данных** структуры [**одноранговой \_ записи**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="06167-153">In this example, a chat message is sent by placing it in the **data** field of a [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span> <span data-ttu-id="06167-154">Запись добавляется в записи одноранговой группы путем вызова [**пирграупаддрекорд**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord), который будет публиковать ее и вызвать \_ \_ событие изменения записи события одноранговой группы \_ \_ на всех узлах, участвующих в одноранговой группе.</span><span class="sxs-lookup"><span data-stu-id="06167-154">The record is added to the peer group records by calling [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord), which will publish it and raise the PEER\_GROUP\_EVENT\_RECORD\_CHANGED event on all peers participating in the peer group.</span></span>


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



## <a name="receiving-a-chat-message"></a><span data-ttu-id="06167-155">Получение сообщения разговора</span><span class="sxs-lookup"><span data-stu-id="06167-155">Receiving a Chat Message</span></span>

<span data-ttu-id="06167-156">Чтобы получить сообщение разговора, создайте функцию обратного вызова для \_ \_ события изменения записи события одноранговой группы \_ \_ , которое вызывает функцию, аналогичную показанной ниже.</span><span class="sxs-lookup"><span data-stu-id="06167-156">To receive the chat message, create a callback function for the PEER\_GROUP\_EVENT\_RECORD\_CHANGED event that calls a function similar to one below.</span></span> <span data-ttu-id="06167-157">Запись получается путем вызова [**пирграупжетрекорд**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) для данных события, полученных предыдущим вызовом [**пирграупжетевентдата**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) в функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="06167-157">The record is obtained by calling [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) on the event data received by a previous call to [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) in the callback function.</span></span> <span data-ttu-id="06167-158">Сообщение разговора хранится в поле **данных** этой записи.</span><span class="sxs-lookup"><span data-stu-id="06167-158">The chat message is stored in the **data** field of this record.</span></span>


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



 

 



