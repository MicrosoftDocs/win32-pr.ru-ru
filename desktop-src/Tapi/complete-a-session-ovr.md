---
description: Операции завершения позволяют приложению указать, каким образом будет работать сеанс, когда такие факторы, как занятое назначение, препятствуют нормальному соединению.
ms.assetid: 71e61376-7913-42a9-a8e2-2ea6e4918f30
title: Завершение сеанса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5736b6be452413811f3530f44db280fe4e2a682f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682926"
---
# <a name="complete-a-session"></a><span data-ttu-id="10128-103">Завершение сеанса</span><span class="sxs-lookup"><span data-stu-id="10128-103">Complete a Session</span></span>

<span data-ttu-id="10128-104">Операции завершения позволяют приложению указать, каким образом будет работать сеанс, когда такие факторы, как занятое назначение, препятствуют нормальному соединению.</span><span class="sxs-lookup"><span data-stu-id="10128-104">Completion operations allow an application to specify how it wants to handle a session when factors such as a busy destination prevent normal connection.</span></span>

<span data-ttu-id="10128-105">[ \_ Константы линекаллкомплмоде](./linecallcomplmode--constants.md) определяют возможные параметры, которые может иметь приложение, в зависимости от возможностей поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="10128-105">The [LINECALLCOMPLMODE\_ Constants](./linecallcomplmode--constants.md) define the possible options an application might have, depending on service provider capabilities.</span></span>

<span data-ttu-id="10128-106">Несколько запросов на завершение вызова могут быть недоступными для определенного адреса в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="10128-106">Multiple call completion requests might be outstanding for a given address at any one time.</span></span> <span data-ttu-id="10128-107">Для идентификации отдельных запросов реализация возвращает [идентификатор завершения](completion-id-ovr.md).</span><span class="sxs-lookup"><span data-stu-id="10128-107">To identify individual requests, the implementation returns a [completion identifier](completion-id-ovr.md).</span></span> <span data-ttu-id="10128-108">При отмене запроса на завершение вызова также используется идентификатор завершения вызова.</span><span class="sxs-lookup"><span data-stu-id="10128-108">Canceling a call completion request in progress also uses this call completion identifier.</span></span>

<span data-ttu-id="10128-109">**Интерфейс TAPI 2. x:** См. раздел [**линекомплетекалл**](/windows/win32/api/tapi/nf-tapi-linecompletecall), [**линеункомплетекалл**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall).</span><span class="sxs-lookup"><span data-stu-id="10128-109">**TAPI 2.x:** See [**lineCompleteCall**](/windows/win32/api/tapi/nf-tapi-linecompletecall), [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall).</span></span>

<span data-ttu-id="10128-110">**Интерфейс TAPI 3. x:** См. раздел [**итбасиккаллконтрол:: Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**итбасиккаллконтрол::D соединения**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span><span class="sxs-lookup"><span data-stu-id="10128-110">**TAPI 3.x:** See [**ITBasicCallControl::Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**ITBasicCallControl::Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span></span>

 

 
