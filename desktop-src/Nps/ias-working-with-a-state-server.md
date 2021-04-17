---
title: Работа с сервером состояний
description: Сервер политики сети выполняет проверку подлинности с помощью базы данных, настроенной на сайте сервера политики сети.
ms.assetid: 8313ba91-5ed1-44d0-80db-cfb82c641100
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d79ff46802d53109c7bb8b40fe3a2db2480949e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105681642"
---
# <a name="working-with-a-state-server"></a><span data-ttu-id="872d5-103">Работа с сервером состояний</span><span class="sxs-lookup"><span data-stu-id="872d5-103">Working With a State Server</span></span>

> [!Note]  
> <span data-ttu-id="872d5-104">Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="872d5-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="872d5-105">Содержимое этого раздела относится как к IAS, так и к NPS.</span><span class="sxs-lookup"><span data-stu-id="872d5-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="872d5-106">По всему тексту NPS используется для ссылки на все версии службы, включая версии, изначально называемые IAS.</span><span class="sxs-lookup"><span data-stu-id="872d5-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="872d5-107">Сервер политики сети выполняет проверку подлинности с помощью базы данных, настроенной на сайте сервера политики сети.</span><span class="sxs-lookup"><span data-stu-id="872d5-107">NPS performs authentication using a database that is configured at the NPS server site.</span></span> <span data-ttu-id="872d5-108">Эта база данных проверки подлинности может быть пользовательской базой данных для домена Windows или нарисована на основе сведений о пользователе, полученных из Active Directory Windows.</span><span class="sxs-lookup"><span data-stu-id="872d5-108">This authentication database could be the user database for a Windows Domain or it could draw upon the user information obtained from the Windows Active Directory.</span></span> <span data-ttu-id="872d5-109">На следующей схеме показана типичная конфигурация, которая показывает, как сервер политики сети взаимодействует с базами данных проверки подлинности, например с базой данных пользователя домена Windows или Active Directory.</span><span class="sxs-lookup"><span data-stu-id="872d5-109">The following diagram illustrates a typical configuration that shows how NPS interacts with authentication databases such as a Windows Domain user database or Active Directory.</span></span> <span data-ttu-id="872d5-110">На схеме также показано, как сервер политики сети может взаимодействовать с сервером состояний, предоставляемым третьим лицом.</span><span class="sxs-lookup"><span data-stu-id="872d5-110">The diagram also shows how NPS could interact with a state server that is provided by a third party.</span></span> <span data-ttu-id="872d5-111">Основное назначение сервера состояний заключается в ограничении числа одновременных сеансов входа, которые может выполнять один пользователь.</span><span class="sxs-lookup"><span data-stu-id="872d5-111">The primary purpose of a state server is to limit the number of simultaneous logon sessions a single user can run.</span></span>

![взаимодействие сервера политики сети с сервером состояний и базами данных проверки подлинности](images/ias02.png)

<span data-ttu-id="872d5-113">Существует две точки взаимодействия между сервером политики сети и сервером состояний.</span><span class="sxs-lookup"><span data-stu-id="872d5-113">There are two points of interaction between NPS and the state server.</span></span> <span data-ttu-id="872d5-114">Одно взаимодействие происходит, когда NPS получает запрос на проверку подлинности от NAS.</span><span class="sxs-lookup"><span data-stu-id="872d5-114">One interaction takes place when NPS receives an authentication request from the NAS.</span></span> <span data-ttu-id="872d5-115">Сервер состояний предоставляет сведения из своей базы данных, чтобы определить, следует ли принимать или отклонять запрос.</span><span class="sxs-lookup"><span data-stu-id="872d5-115">The state server provides information from its database to determine whether to accept or deny the request.</span></span> <span data-ttu-id="872d5-116">Другое взаимодействие происходит, когда NPS получает запросы учета от NAS.</span><span class="sxs-lookup"><span data-stu-id="872d5-116">The other interaction takes place when NPS receives accounting requests from the NAS.</span></span> <span data-ttu-id="872d5-117">Сервер состояний использует эти сведения для обновления базы данных запросов на учет.</span><span class="sxs-lookup"><span data-stu-id="872d5-117">The state server uses the information form these accounting requests to update its database.</span></span>

<span data-ttu-id="872d5-118">Дополнительные сведения о серверах состояний см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="872d5-118">For more information on state servers see:</span></span>

-   [<span data-ttu-id="872d5-119">Рекомендации по проектированию сервера состояний</span><span class="sxs-lookup"><span data-stu-id="872d5-119">State Server Design Considerations</span></span>](/windows/desktop/Nps/ias-state-server-design-considerations)

## <a name="related-topics"></a><span data-ttu-id="872d5-120">См. также</span><span class="sxs-lookup"><span data-stu-id="872d5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="872d5-121">Служба проверки подлинности в Интернете и сервер политики сети</span><span class="sxs-lookup"><span data-stu-id="872d5-121">Internet Authentication Service and Network Policy Server</span></span>](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[<span data-ttu-id="872d5-122">Проверка подлинности, авторизация и учет RADIUS</span><span class="sxs-lookup"><span data-stu-id="872d5-122">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="872d5-123">Ведение журнала с помощью сервера политики сети</span><span class="sxs-lookup"><span data-stu-id="872d5-123">Logging With Network Policy Server</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> </dl>

 

 