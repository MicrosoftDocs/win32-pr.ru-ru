---
description: API-интерфейсы "Соседние пользователи"
ms.assetid: 3b142d23-a9b2-465c-9bdc-484afbde154e
title: API-интерфейсы "Соседние пользователи"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132d358a7d51a1069f7a4d1dc1ddfe2752dbdd1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998542"
---
# <a name="people-near-me-apis"></a><span data-ttu-id="c4ece-103">API-интерфейсы "Соседние пользователи"</span><span class="sxs-lookup"><span data-stu-id="c4ece-103">People Near Me APIs</span></span>

<span data-ttu-id="c4ece-104">Все приложения, поддерживающие [соседние пользователи](about-people-near-me.md) (PNM), могут использовать следующие API-интерфейсы Win32:</span><span class="sxs-lookup"><span data-stu-id="c4ece-104">Any applications capable of [People Near Me](about-people-near-me.md) (PNM) can use the following Win32 APIs:</span></span>

### <a name="contacts-api"></a><span data-ttu-id="c4ece-105">API контактов</span><span class="sxs-lookup"><span data-stu-id="c4ece-105">Contacts API</span></span>

<span data-ttu-id="c4ece-106">API контактов используется для доступа к контактным данным пользователя, выполнившего вход в систему, получения сведений о ранее сохраненных контактах или для хранения контактной информации и цифрового сертификата нового контакта.</span><span class="sxs-lookup"><span data-stu-id="c4ece-106">The Contacts API is used to access the contact information for the logged on user, retrieve information about previously stored contacts, or store the contact information and digital certificate of a new contact.</span></span>

### <a name="people-near-me-api"></a><span data-ttu-id="c4ece-107">API "Соседние пользователи"</span><span class="sxs-lookup"><span data-stu-id="c4ece-107">People Near Me API</span></span>

<span data-ttu-id="c4ece-108">API PNM используется для поиска ближайших пользователей, их объявленных интересов, любых произвольных объектов, которые они выбирают для публикации, и объявленных приложений.</span><span class="sxs-lookup"><span data-stu-id="c4ece-108">The PNM API is used to find users nearby, their advertised interests, any arbitrary objects they choose to publish, and advertised applications.</span></span>

### <a name="publication-api"></a><span data-ttu-id="c4ece-109">API публикации</span><span class="sxs-lookup"><span data-stu-id="c4ece-109">Publication API</span></span>

<span data-ttu-id="c4ece-110">API публикации используется для взаимодействия с удаленными контактами.</span><span class="sxs-lookup"><span data-stu-id="c4ece-110">The Publication API is used to interact with remote contacts.</span></span> <span data-ttu-id="c4ece-111">Уровень [сигнализации однорангового узла](windows-peer-components-for-people-near-me.md) , используемый диспетчером публикаций, также используется модулем PNM для установления соединений.</span><span class="sxs-lookup"><span data-stu-id="c4ece-111">The [Peer Signaling](windows-peer-components-for-people-near-me.md) layer used by the Publication Manager is also used by the PNM module for establishing connections.</span></span>

### <a name="invitation-api"></a><span data-ttu-id="c4ece-112">API приглашения</span><span class="sxs-lookup"><span data-stu-id="c4ece-112">Invitation API</span></span>

<span data-ttu-id="c4ece-113">API приглашения используется приложением для совместной работы, чтобы пригласить определенные узлы в действие совместной работы.</span><span class="sxs-lookup"><span data-stu-id="c4ece-113">The Invitation API is used by a collaboration application to invite specific peer(s) into a collaboration activity.</span></span>

### <a name="application-registration-api"></a><span data-ttu-id="c4ece-114">API регистрации приложений</span><span class="sxs-lookup"><span data-stu-id="c4ece-114">Application Registration API</span></span>

<span data-ttu-id="c4ece-115">API регистрации приложений используется установщиком приложения для совместной работы для регистрации приложения.</span><span class="sxs-lookup"><span data-stu-id="c4ece-115">The Application Registration API is used by the installer of a collaboration application to register the application.</span></span> <span data-ttu-id="c4ece-116">Приложение, поддерживающее PNM, будет запрашивать пользователя в процессе установки, чтобы определить, должно ли приложение быть доступно пользователям в подсети.</span><span class="sxs-lookup"><span data-stu-id="c4ece-116">A PNM-capable application will prompt the user during the installation process to determine whether the application should be made available to users on the subnet.</span></span>

 

 



