---
description: TAPI назначает идентификаторы сеансов, уникальные для каждого сеанса и приложения.
ms.assetid: 711a9bc6-ffc6-499b-8653-ba230028c146
title: Идентификатор сеанса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e135beb439d1c5fb2fdd46d4986cd35dc5ae49b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424070"
---
# <a name="session-identifier"></a><span data-ttu-id="66690-103">Идентификатор сеанса</span><span class="sxs-lookup"><span data-stu-id="66690-103">Session Identifier</span></span>

<span data-ttu-id="66690-104">TAPI назначает идентификаторы сеансов, уникальные для каждого сеанса и приложения.</span><span class="sxs-lookup"><span data-stu-id="66690-104">TAPI assigns session identifiers that are unique for each session and application.</span></span> <span data-ttu-id="66690-105">Приложение использует идентификатор сеанса для взаимодействия с TAPI в отношении определенного сеанса.</span><span class="sxs-lookup"><span data-stu-id="66690-105">An application uses a session identifier to communicate with TAPI concerning a specific session.</span></span> <span data-ttu-id="66690-106">Приложение обычно получает идентификатор, создавая новый сеанс связи или когда TAPI предлагает сеанс.</span><span class="sxs-lookup"><span data-stu-id="66690-106">An application typically obtains an identifier either by creating a new communications session or when TAPI offers a session.</span></span>

<span data-ttu-id="66690-107">Идентификатор сеанса нельзя использовать для передачи информации другому приложению.</span><span class="sxs-lookup"><span data-stu-id="66690-107">A session identifier cannot be used to pass information to another application.</span></span> <span data-ttu-id="66690-108">Для этой цели следует использовать [идентификатор вызова](call-id-ovr.md), который может быть назначен поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="66690-108">For this purpose, use the [Call ID](call-id-ovr.md), which may be assigned by a service provider.</span></span>

<span data-ttu-id="66690-109">Сведения об операциях, которые создают сеансы и возвращают идентификатор сеанса, см. в разделе [Инициация сеанса](initiate-a-session-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="66690-109">See [Initiate a session](initiate-a-session-ovr.md) for information on operations that create sessions and return a session identifier.</span></span> <span data-ttu-id="66690-110">См. раздел [ответ на сеанс, инициированный в других](respond-to-session-initiated-elsewhere-ovr.md) случаях для операций, которые получают идентификаторы сеансов из TAPI.</span><span class="sxs-lookup"><span data-stu-id="66690-110">See [Respond to session initiated elsewhere](respond-to-session-initiated-elsewhere-ovr.md) for operations that acquire session identifiers from TAPI.</span></span> <span data-ttu-id="66690-111">Сведения о освобождении ресурсов сеанса см. в разделе [Завершение сеанса](terminate-a-session-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="66690-111">See [Terminate a Session](terminate-a-session-ovr.md) for information on releasing session resources.</span></span>

<span data-ttu-id="66690-112">Все поставщики служб должны поддерживать некоторую форму идентификации сеанса.</span><span class="sxs-lookup"><span data-stu-id="66690-112">All service providers must support some form of session identification.</span></span>

<span data-ttu-id="66690-113">**Интерфейс TAPI 2. x:** Основным идентификатором сеанса связи является обработчик вызова.</span><span class="sxs-lookup"><span data-stu-id="66690-113">**TAPI 2.x:** The primary identifier of a communications session is the call handle.</span></span>

<span data-ttu-id="66690-114">**Интерфейс TAPI 3. x:** Сеанс представлен [объектом Call](call-object.md) , а первичный идентификатор — указателем на интерфейс [**иткаллинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .</span><span class="sxs-lookup"><span data-stu-id="66690-114">**TAPI 3.x:** A session is represented by a [Call Object](call-object.md) and the primary identifier is a pointer to the [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) interface.</span></span>

 

 



