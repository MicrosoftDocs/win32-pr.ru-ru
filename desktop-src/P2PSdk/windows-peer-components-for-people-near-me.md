---
description: Одноранговые компоненты Windows для "соседних пользователей"
ms.assetid: aa9e7d4d-4131-4578-8bd1-298f04b826f9
title: Одноранговые компоненты Windows для "соседних пользователей"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c780ccad1abd5ce04c1672f66561285831e5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998534"
---
# <a name="windows-peer-components-for-people-near-me"></a><span data-ttu-id="7b89a-103">Одноранговые компоненты Windows для "соседних пользователей"</span><span class="sxs-lookup"><span data-stu-id="7b89a-103">Windows Peer Components for People Near Me</span></span>

<span data-ttu-id="7b89a-104">В основном исполняемом файле одноранговых сетей Windows (P2phost.exe) [архитектура "Соседние пользователи](people-near-me-architecture.md) " использует следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="7b89a-104">Within the main Windows Peer Networking executable (P2phost.exe), the [People Near Me Architecture](people-near-me-architecture.md) uses the following components:</span></span>

### <a name="people-near-me"></a><span data-ttu-id="7b89a-105">Соседние пользователи</span><span class="sxs-lookup"><span data-stu-id="7b89a-105">People Near Me</span></span>

<span data-ttu-id="7b89a-106">Компонент "Соседние пользователи" (PNM) инициирует обнаружение с помощью обнаружения веб-служб в локальной подсети для имен пользователей компьютеров с поддержкой PNM.</span><span class="sxs-lookup"><span data-stu-id="7b89a-106">The People Near Me (PNM) component initiates discovery using Web Services Discovery on the local subnet for the user names of PNM-capable computers.</span></span>

### <a name="people-near-me-publisher"></a><span data-ttu-id="7b89a-107">Издатель "Соседние пользователи"</span><span class="sxs-lookup"><span data-stu-id="7b89a-107">People Near Me Publisher</span></span>

<span data-ttu-id="7b89a-108">Компонент Publisher "Соседние пользователи" публикует псевдонимы вошедших в систему пользователей, чтобы указать доступность других компьютеров с помощью PNM в локальной подсети.</span><span class="sxs-lookup"><span data-stu-id="7b89a-108">The People Near Me Publisher component publishes the nicknames of logged-on users to indicate availability to other computers using PNM on the local subnet.</span></span> <span data-ttu-id="7b89a-109">Пользователь, выполнивший вход в систему, должен опубликовать свой псевдоним перед объявлением.</span><span class="sxs-lookup"><span data-stu-id="7b89a-109">The logged-on user must elect to publish their nickname before it is advertised.</span></span> <span data-ttu-id="7b89a-110">Псевдоним публикуется в подсети с помощью обнаружения веб-служб.</span><span class="sxs-lookup"><span data-stu-id="7b89a-110">The nickname is published on the subnet using Web Services Discovery.</span></span> <span data-ttu-id="7b89a-111">Кроме того, можно также опубликовать объекты и приложения.</span><span class="sxs-lookup"><span data-stu-id="7b89a-111">Additionally, objects and applications can also be published.</span></span> <span data-ttu-id="7b89a-112">Однако пользователь должен указать публикацию объектов и приложений для областей "**соседние пользователи**" или "**все**".</span><span class="sxs-lookup"><span data-stu-id="7b89a-112">However, the user must specify object and application publication for the '**People Near Me**' or '**All**' scopes.</span></span>

### <a name="people-near-me-enumerator"></a><span data-ttu-id="7b89a-113">Перечислитель "Соседние пользователи"</span><span class="sxs-lookup"><span data-stu-id="7b89a-113">People Near Me Enumerator</span></span>

<span data-ttu-id="7b89a-114">Компонент перечислителя "Соседние пользователи" перечисляет список пользователей в локальной подсети.</span><span class="sxs-lookup"><span data-stu-id="7b89a-114">The People Near Me Enumerator component enumerates the list of users on the local subnet.</span></span> <span data-ttu-id="7b89a-115">С помощью этого списка служба обнаружения веб-служб отправляет многоадресный запрос и получает ответы.</span><span class="sxs-lookup"><span data-stu-id="7b89a-115">Using this list, Web Services Discovery sends a multicast query and receives the responses.</span></span> <span data-ttu-id="7b89a-116">После получения списка псевдонимов приложение может использовать API для получения дополнительных данных, публикуемых пользователем (который шифруется с помощью [канала Schannel](windows-vista-components-for-people-near-me.md)), например списка зарегистрированных приложений и всех публикуемых объектов.</span><span class="sxs-lookup"><span data-stu-id="7b89a-116">After the list of nicknames are obtained, an application can use the API to retrieve more data being published by the user (which is encrypted using [SChannel](windows-vista-components-for-people-near-me.md)), such as the list of applications registered and any objects being published.</span></span>

<span data-ttu-id="7b89a-117">Процесс поиска и перечисления не происходит автоматически, но должен быть явно инициирован пользователем или приложением путем входа в систему PNM.</span><span class="sxs-lookup"><span data-stu-id="7b89a-117">The search and enumeration process does not happen automatically, but must be explicitly initiated by a user or an application by signing-in to PNM.</span></span> <span data-ttu-id="7b89a-118">Результаты поиска представляют собой список псевдонимов других пользователей в той же подсети, в которых объявлены псевдонимы с помощью API PNM.</span><span class="sxs-lookup"><span data-stu-id="7b89a-118">The search results are the list of nicknames of other users on the same subnet that are advertising their nicknames using the PNM API.</span></span>

### <a name="publication-manager"></a><span data-ttu-id="7b89a-119">Диспетчер публикаций</span><span class="sxs-lookup"><span data-stu-id="7b89a-119">Publication Manager</span></span>

<span data-ttu-id="7b89a-120">Компонент диспетчера публикаций отвечает за публикацию обновлений присутствия, приложений или объектов для контактов или соседних пользователей, которые подписались или опрашивают данные.</span><span class="sxs-lookup"><span data-stu-id="7b89a-120">The Publication Manager component is responsible for publishing presence, application, or object updates to contacts or people near me that are subscribed or poll for data.</span></span>

### <a name="peer-signaling"></a><span data-ttu-id="7b89a-121">Сигнал однорангового узла</span><span class="sxs-lookup"><span data-stu-id="7b89a-121">Peer Signaling</span></span>

<span data-ttu-id="7b89a-122">Компонент сигнализации однорангового узла обрабатывает создание подключений между одноранговыми узлами для обмена данными.</span><span class="sxs-lookup"><span data-stu-id="7b89a-122">The Peer Signaling component handles the creation of connections between peers to exchange data.</span></span> <span data-ttu-id="7b89a-123">Для соседних пользователей используется одноранговый сигнал, когда пользователь или приложение отправляет одноадресный запрос на конкретный компьютер для его открытого ключа, приложений и объектов.</span><span class="sxs-lookup"><span data-stu-id="7b89a-123">For People Near Me, Peer Signaling is used when a user or application sends the unicast query to a specific computer for its public key, applications, and objects.</span></span>

### <a name="receive-invitation-handlerux"></a><span data-ttu-id="7b89a-124">Получение обработчика приглашений и UX</span><span class="sxs-lookup"><span data-stu-id="7b89a-124">Receive Invitation Handler/UX</span></span>

<span data-ttu-id="7b89a-125">Компонент обработчика приглашений/UX получает входящее приглашение от другого лица, предлагает пользователю определить, нужно ли запускать приложение, связанное с приглашением, а затем запускает приложение на основе пользователя, получившего приглашение.</span><span class="sxs-lookup"><span data-stu-id="7b89a-125">The Receive Invitation Handler/UX component receives an incoming invitation from another person, prompts the user to determine whether they want to launch the application associated with the invitation, and then launches the application based on the user accepting the invitation.</span></span> <span data-ttu-id="7b89a-126">Приглашение — это сообщение от другого лица для инициации совместной работы с помощью определенного приложения, установленного на обоих компьютерах пользователей и объявленного приглашенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="7b89a-126">An invitation is a message from another person to initiate collaboration activity using a specific application that is installed on both user's computers and is advertised by the user being invited.</span></span>

### <a name="peer-security"></a><span data-ttu-id="7b89a-127">Безопасность узла</span><span class="sxs-lookup"><span data-stu-id="7b89a-127">Peer Security</span></span>

<span data-ttu-id="7b89a-128">При отправке сведений о присутствии, приложении и объекте данные шифруются с[помощью канала SSL](windows-vista-components-for-people-near-me.md).</span><span class="sxs-lookup"><span data-stu-id="7b89a-128">When presence, application, and object are sent, the information is encrypted using an SSL channel ([Schannel](windows-vista-components-for-people-near-me.md)).</span></span> <span data-ttu-id="7b89a-129">Инициирующий компьютер использует открытый ключ приглашаемого компьютера для согласования секретного ключа, который используется для шифрования последующих данных, передаваемых между двумя одноранговыми узлами.</span><span class="sxs-lookup"><span data-stu-id="7b89a-129">The initiating computer uses the public key of the invited computer to negotiate a secret key that is used for encrypting the subsequent data sent between the two peers.</span></span>

 

 



