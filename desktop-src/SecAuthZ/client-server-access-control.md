---
description: Серверное приложение предоставляет клиентам службы.
ms.assetid: 8301ed4f-9458-410b-af19-4f055656005a
title: Управление доступом клиента/сервера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b1d349abb2d55f00b9801c9bb493437fa858eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647213"
---
# <a name="clientserver-access-control"></a><span data-ttu-id="172b0-103">Управление доступом клиента/сервера</span><span class="sxs-lookup"><span data-stu-id="172b0-103">Client/Server Access Control</span></span>

<span data-ttu-id="172b0-104">Серверное приложение предоставляет клиентам службы.</span><span class="sxs-lookup"><span data-stu-id="172b0-104">A server application provides services to clients.</span></span> <span data-ttu-id="172b0-105">Например, сервер может выполнять следующие службы от имени клиента:</span><span class="sxs-lookup"><span data-stu-id="172b0-105">For example, a server could perform the following services on behalf of a client:</span></span>

-   <span data-ttu-id="172b0-106">Сохранение и получение сведений из частной базы данных</span><span class="sxs-lookup"><span data-stu-id="172b0-106">Save and retrieve information from a private database</span></span>
-   <span data-ttu-id="172b0-107">Доступ к сетевым ресурсам</span><span class="sxs-lookup"><span data-stu-id="172b0-107">Access network resources</span></span>
-   <span data-ttu-id="172b0-108">Запуск [*процессов*](/windows/desktop/SecGloss/p-gly) в [*контексте безопасности*](/windows/desktop/SecGloss/s-gly) клиента на компьютере сервера</span><span class="sxs-lookup"><span data-stu-id="172b0-108">Start [*processes*](/windows/desktop/SecGloss/p-gly) in the client's [*security context*](/windows/desktop/SecGloss/s-gly) on the server's computer</span></span>

<span data-ttu-id="172b0-109">Защищенный сервер управляет доступом к своим службам.</span><span class="sxs-lookup"><span data-stu-id="172b0-109">A protected server controls access to its services.</span></span> <span data-ttu-id="172b0-110">Windows обеспечивает поддержку безопасности, которая позволяет серверу выполнять следующие действия.</span><span class="sxs-lookup"><span data-stu-id="172b0-110">Windows provides security support that enables a server to do the following:</span></span>

-   <span data-ttu-id="172b0-111">Олицетворяет клиентский [*контекст безопасности*](/windows/desktop/SecGloss/s-gly), что заставляет систему выполнять большинство проверок доступа и [*привилегий*](/windows/desktop/SecGloss/p-gly) для [*маркера доступа*](/windows/desktop/SecGloss/a-gly) клиента, а не сервера</span><span class="sxs-lookup"><span data-stu-id="172b0-111">Impersonate a client's [*security context*](/windows/desktop/SecGloss/s-gly), which causes the system to perform most access and [*privilege*](/windows/desktop/SecGloss/p-gly) checks against the client's [*access token*](/windows/desktop/SecGloss/a-gly) rather than the server's</span></span>
-   <span data-ttu-id="172b0-112">Регистрация клиента на компьютере сервера</span><span class="sxs-lookup"><span data-stu-id="172b0-112">Log a client on to the server's computer</span></span>
-   <span data-ttu-id="172b0-113">Подключение к сетевым ресурсам с помощью контекста безопасности клиента</span><span class="sxs-lookup"><span data-stu-id="172b0-113">Connect to network resources using the client's security context</span></span>
-   <span data-ttu-id="172b0-114">Создание [*дескрипторов безопасности*](/windows/desktop/SecGloss/s-gly) для защиты закрытых объектов</span><span class="sxs-lookup"><span data-stu-id="172b0-114">Create [*security descriptors*](/windows/desktop/SecGloss/s-gly) to protect private objects</span></span>
-   <span data-ttu-id="172b0-115">Определение возможности доступа к клиенту с помощью дескриптора безопасности</span><span class="sxs-lookup"><span data-stu-id="172b0-115">Determine whether a security descriptor allows access to a client</span></span>
-   <span data-ttu-id="172b0-116">Определение того, включен ли набор привилегий в маркере клиента</span><span class="sxs-lookup"><span data-stu-id="172b0-116">Determine whether a set of privileges are enabled in a client's token</span></span>
-   <span data-ttu-id="172b0-117">Создание сообщений аудита в журнале событий безопасности для записи попыток клиента получить доступ к объектам или использовать привилегии</span><span class="sxs-lookup"><span data-stu-id="172b0-117">Generate audit messages in the security event log to record attempts by a client to access objects or use privileges</span></span>

 

 
