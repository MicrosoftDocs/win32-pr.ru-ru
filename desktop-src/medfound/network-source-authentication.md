---
description: Проверка подлинности источника сети
ms.assetid: bffc33ec-0fb0-4bbe-9bac-583b9d4e1153
title: Проверка подлинности источника сети
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09c38968fccf501f49ac7666a066b88528b237bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080433"
---
# <a name="network-source-authentication"></a><span data-ttu-id="9ccb1-103">Проверка подлинности источника сети</span><span class="sxs-lookup"><span data-stu-id="9ccb1-103">Network Source Authentication</span></span>

<span data-ttu-id="9ccb1-104">Перед предоставлением доступа к носителю некоторым узлам мультимедиа могут потребоваться учетные данные пользователя из клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="9ccb1-104">Certain media hosts may require user credentials from client applications before allowing access to the media.</span></span> <span data-ttu-id="9ccb1-105">Учетные данные пользователя включают идентификацию и подтверждение идентификации, такие как имя пользователя и пароль, которые используются сервером мультимедиа для предоставления доступа к исходному сетевому расположению.</span><span class="sxs-lookup"><span data-stu-id="9ccb1-105">User credentials include identification and proof of identification, such as user name and password, which are used by the media server to grant access to the network source it hosts.</span></span> <span data-ttu-id="9ccb1-106">Сетевой источник может предоставлять NTLM, дайджест или обычную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="9ccb1-106">The network source can provide NTLM, Digest, or Basic authentication.</span></span>

<span data-ttu-id="9ccb1-107">Приложения на основе Media Foundation могут хранить учетные данные пользователя для определенного URL-адреса в объекте *учетных данных* , который предоставляет интерфейс [**имфнеткредентиал**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) .</span><span class="sxs-lookup"><span data-stu-id="9ccb1-107">Applications based on Media Foundation can store user credentials for a specific URL in a *credential* object that exposes the [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) interface.</span></span> <span data-ttu-id="9ccb1-108">Объект учетных данных хранит зашифрованные учетные данные и предоставляет методы для получения таких сведений, как имя пользователя, пароль и домен.</span><span class="sxs-lookup"><span data-stu-id="9ccb1-108">The credential object stores encrypted credentials and provides methods to return information such as user name, password, and domain.</span></span>

<span data-ttu-id="9ccb1-109">Объекты учетных данных создаются и обслуживаются в кэше.</span><span class="sxs-lookup"><span data-stu-id="9ccb1-109">The credential objects are created and maintained in a cache.</span></span> <span data-ttu-id="9ccb1-110">Объект *кэша учетных данных* , предоставляемый интерфейсом [**имфнеткредентиалкаче**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) , предоставляет методы для получения объектов учетных данных из кэша учетных данных.</span><span class="sxs-lookup"><span data-stu-id="9ccb1-110">The *credential cache* object, exposed by the [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) interface provides methods for retrieving the credential objects from the credential cache.</span></span>

<span data-ttu-id="9ccb1-111">Приложение, поддерживающее проверку подлинности, должно реализовывать интерфейс [**имфнеткредентиалманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .</span><span class="sxs-lookup"><span data-stu-id="9ccb1-111">An application that supports authentication must implement the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span> <span data-ttu-id="9ccb1-112">Media Foundation не предоставляет реализацию этого интерфейса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9ccb1-112">Media Foundation does not provide a default implementation of this interface.</span></span> <span data-ttu-id="9ccb1-113">Диспетчер учетных данных отвечает за сбор необходимых учетных данных для URL-адреса из вводимых пользователем данных или считывания из постоянного хранилища.</span><span class="sxs-lookup"><span data-stu-id="9ccb1-113">The credential manager is responsible for gathering the required credentials for a URL from user input or reading from persisted storage.</span></span>

<span data-ttu-id="9ccb1-114">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="9ccb1-114">This section contains the following topics:</span></span>

-   [<span data-ttu-id="9ccb1-115">Настройка диспетчера учетных данных</span><span class="sxs-lookup"><span data-stu-id="9ccb1-115">Setting a Credential Manager</span></span>](setting-a-credential-manager.md)
-   [<span data-ttu-id="9ccb1-116">Использование кэша учетных данных</span><span class="sxs-lookup"><span data-stu-id="9ccb1-116">Using the Credential Cache</span></span>](using-the-credential-cache.md)
-   [<span data-ttu-id="9ccb1-117">Реализация Имфнеткредентиалманажер</span><span class="sxs-lookup"><span data-stu-id="9ccb1-117">Implementing IMFNetCredentialManager</span></span>](implementing-imfnetcredentialmanager.md)

## <a name="related-topics"></a><span data-ttu-id="9ccb1-118">См. также</span><span class="sxs-lookup"><span data-stu-id="9ccb1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ccb1-119">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9ccb1-119">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



