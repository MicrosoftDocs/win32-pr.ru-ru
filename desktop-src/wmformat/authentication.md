---
title: Проверка подлинности (пакет SDK для формата Windows Media 11)
description: Аутентификация
ms.assetid: 9c181615-e864-4588-846f-d04d73824f5f
keywords:
- Windows Media Format SDK, проверка подлинности
- Пакет SDK для Windows Media Format, проверка подлинности сети
- Расширенный формат систем (ASF), проверка подлинности
- ASF (Расширенный системный формат), проверка подлинности
- Расширенный системный формат (ASF), проверка подлинности сети
- ASF (Расширенный системный формат), проверка подлинности сети
- проверка подлинности
- Проверка подлинности сети, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf815881ac7beb354fffbfdb9b5475d040e9e83
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105701017"
---
# <a name="authentication-windows-media-format-11-sdk"></a><span data-ttu-id="9d571-111">Проверка подлинности (пакет SDK для формата Windows Media 11)</span><span class="sxs-lookup"><span data-stu-id="9d571-111">Authentication (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="9d571-112">Объект Reader может справляться с проблемами проверки подлинности сети, включая дайджест-аутентификацию и проверку подлинности NTLM.</span><span class="sxs-lookup"><span data-stu-id="9d571-112">The reader object can handle network authentication challenges, including digest authentication and NTLM authentication.</span></span> <span data-ttu-id="9d571-113">В некоторых случаях приложение должно предоставлять учетные данные пользователя через интерфейс обратного вызова:</span><span class="sxs-lookup"><span data-stu-id="9d571-113">In some cases the application must provide the user's credentials through a callback interface:</span></span>

-   <span data-ttu-id="9d571-114">Дайджест-проверка подлинности. приложение должно реализовывать интерфейс **ивмкредентиалкаллбакк** , как описано далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="9d571-114">Digest authentication: The application must implement the **IWMCredentialCallback** interface, as described later in this topic.</span></span>
-   <span data-ttu-id="9d571-115">Проверка подлинности NTLM. модуль чтения автоматически реагирует на учетные данные пользователя для входа.</span><span class="sxs-lookup"><span data-stu-id="9d571-115">NTLM authentication: The reader automatically responds with the user's logon credentials.</span></span> <span data-ttu-id="9d571-116">Если текущий пользователь имеет право на вход на сервер, приложению не нужно ничего делать.</span><span class="sxs-lookup"><span data-stu-id="9d571-116">If the current user is authorized to log on to the server, the application does not have to do anything.</span></span> <span data-ttu-id="9d571-117">Если пользователь не имеет авторизации, приложение должно реализовать интерфейс **ивмкредентиалкаллбакк** .</span><span class="sxs-lookup"><span data-stu-id="9d571-117">If the user does not have authorization, the application must implement the **IWMCredentialCallback** interface.</span></span>

    > [!Note]  
    > <span data-ttu-id="9d571-118">Службы Windows Media версии 4,1 не поддерживают проверку подлинности NTLM через прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="9d571-118">Windows Media Services version 4.1 does not support NTLM authentication through a proxy server.</span></span> <span data-ttu-id="9d571-119">Для проверки подлинности NTLM требуется несколько обменов между клиентом и сервером в одном соединении, а версия 4,1 не сохраняет постоянное подключение к прокси-серверу.</span><span class="sxs-lookup"><span data-stu-id="9d571-119">NTLM authentication requires several client-server exchanges on the same connection, and version 4.1 does not keep a persistent connection with the proxy.</span></span> <span data-ttu-id="9d571-120">Серия Windows Media Services 9 в Microsoft Windows Server 2003 поддерживает проверку подлинности NTLM через прокси-сервер при условии, что прокси поддерживает подключения проверки активности.</span><span class="sxs-lookup"><span data-stu-id="9d571-120">Windows Media Services 9 Series in Microsoft Windows Server 2003 supports NTLM authentication through a proxy server, as long as the proxy supports keep-alive connections.</span></span>

     

<span data-ttu-id="9d571-121">Как уже отмечалось, в некоторых случаях приложение должно предоставить учетные данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="9d571-121">As noted, in some cases the application must provide the user's credentials.</span></span> <span data-ttu-id="9d571-122">Это происходит через интерфейс **ивмкредентиалкаллбакк** , который имеет единственный метод **аккуирекредентиалс**.</span><span class="sxs-lookup"><span data-stu-id="9d571-122">This occurs through the **IWMCredentialCallback** interface, which has a single method, **AcquireCredentials**.</span></span> <span data-ttu-id="9d571-123">Для поддержки проверки подлинности Реализуйте этот интерфейс в приложении.</span><span class="sxs-lookup"><span data-stu-id="9d571-123">To support authentication, implement this interface in your application.</span></span> <span data-ttu-id="9d571-124">Объект модуля чтения запрашивает этот интерфейс путем вызова **QueryInterface** на [**ивмреадеркаллбакк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) указателе, полученном из приложения в методе [**ивмреадер:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) .</span><span class="sxs-lookup"><span data-stu-id="9d571-124">The reader object queries for this interface by calling **QueryInterface** on the [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) pointer that it received from the application in the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method.</span></span> <span data-ttu-id="9d571-125">Если объекту модуля чтения необходимо получить учетные данные пользователя, он вызывает метод **аккуирекредентиалс** приложения.</span><span class="sxs-lookup"><span data-stu-id="9d571-125">If the reader object needs to get the user's credentials, it calls the application's **AcquireCredentials** method.</span></span>

<span data-ttu-id="9d571-126">Если учетные данные будут передаваться по сети без шифрования, средство чтения установит флаг ВМТ для \_ открытого текста учетных данных \_ \_ в параметре *пдвфлагс* .</span><span class="sxs-lookup"><span data-stu-id="9d571-126">If the credentials will be sent over the network without encryption, the reader sets the WMT\_CREDENTIAL\_CLEAR\_TEXT flag in the *pdwFlags* parameter.</span></span> <span data-ttu-id="9d571-127">Это дает приложению возможность предупредить пользователя о том, что его учетные данные будут отправляться в виде обычного текста.</span><span class="sxs-lookup"><span data-stu-id="9d571-127">This gives the application an opportunity to warn the user that his or her credentials will be sent in plain text.</span></span>

<span data-ttu-id="9d571-128">В противном случае объект Reader автоматически шифрует учетные данные перед их отправкой по сети.</span><span class="sxs-lookup"><span data-stu-id="9d571-128">Otherwise, the reader object automatically encrypts the credentials before sending them over the network.</span></span> <span data-ttu-id="9d571-129">Приложение может вернуть их объекту модуля чтения в виде обычного текста.</span><span class="sxs-lookup"><span data-stu-id="9d571-129">The application can return them to the reader object in plain text.</span></span> <span data-ttu-id="9d571-130">Кроме того, если объект модуля чтения задает \_ флаг шифрования учетных данных ВМТ \_ , это означает, что модуль чтения поддерживает получение зашифрованных учетных данных из приложения.</span><span class="sxs-lookup"><span data-stu-id="9d571-130">In addition, if the reader object sets the WMT\_CREDENTIAL\_ENCRYPT flag, it means the reader supports getting encrypted credentials from the application.</span></span> <span data-ttu-id="9d571-131">В этом случае приложение может либо возвращать учетные данные в виде обычного текста, либо шифровать их самостоятельно с помощью функции **CryptProtectData** , которая описана в документации по Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="9d571-131">In that case, the application can either return the credentials in plain text, or else encrypt them itself using the **CryptProtectData** function, which is described in the Platform SDK documentation.</span></span> <span data-ttu-id="9d571-132">Если приложение шифрует учетные данные, необходимо задать \_ флаг шифрования учетных данных ВМТ \_ в параметре *пдвфлагс* перед возвратом метода.</span><span class="sxs-lookup"><span data-stu-id="9d571-132">If the application encrypts the credentials, it must set the WMT\_CREDENTIAL\_ENCRYPT flag in the *pdwFlags* parameter before the method returns.</span></span>

<span data-ttu-id="9d571-133">Как правило, шифрование данных не требуется, так как объект чтения шифрует данные при необходимости.</span><span class="sxs-lookup"><span data-stu-id="9d571-133">Generally, it is not necessary to encrypt the data, because the reader object encrypts the data if necessary.</span></span> <span data-ttu-id="9d571-134">Однако шифрование может быть полезным, если приложение сохраняет имя пользователя и пароль в памяти, так как предотвращает проверку дампа памяти процесса злоумышленником.</span><span class="sxs-lookup"><span data-stu-id="9d571-134">However, encryption might be useful if the application keeps the user name and password in memory, because it prevents an attacker from inspecting a memory dump of the process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d571-135">См. также</span><span class="sxs-lookup"><span data-stu-id="9d571-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d571-136">**Интерфейс Ивмкредентиалкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="9d571-136">**IWMCredentialCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> <dt>

[<span data-ttu-id="9d571-137">**Интерфейс Ивмреадер**</span><span class="sxs-lookup"><span data-stu-id="9d571-137">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> </dl>

 

 




