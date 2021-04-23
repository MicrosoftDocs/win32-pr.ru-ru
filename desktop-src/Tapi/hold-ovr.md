---
description: Операция удержания позволяет одному адресу работать с несколькими сеансами связи.
ms.assetid: 65e22e4e-e346-41c2-929a-ba0d1f7f1732
title: Нажмите
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df54b246c5bde5914a14b53dd56b71688d92a5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897998"
---
# <a name="hold"></a><span data-ttu-id="7c5fa-103">Нажмите</span><span class="sxs-lookup"><span data-stu-id="7c5fa-103">Hold</span></span>

<span data-ttu-id="7c5fa-104">Операция удержания позволяет одному адресу работать с несколькими сеансами связи.</span><span class="sxs-lookup"><span data-stu-id="7c5fa-104">The hold operation allows a single address to handle multiple communications sessions.</span></span> <span data-ttu-id="7c5fa-105">При размещении сеанса на жестком диске освобождается линия или адрес пользователя для выполнения других вызовов.</span><span class="sxs-lookup"><span data-stu-id="7c5fa-105">Placing a session on a hard hold frees the user's line/address to make other calls.</span></span> <span data-ttu-id="7c5fa-106">Вызов на жестком удержании обычно не может быть передан или включен в конференцию, но вызов консультации может.</span><span class="sxs-lookup"><span data-stu-id="7c5fa-106">A call on hard hold typically cannot be transferred or included in a conference call, but a consultation call can.</span></span> <span data-ttu-id="7c5fa-107">Вызовы консультации инициируются с помощью [конференций](conference-ovr.md) или операций [перемещения](transfer-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="7c5fa-107">Consultation calls are initiated using [conference](conference-ovr.md) or [transfer](transfer-ovr.md) operations.</span></span>

<span data-ttu-id="7c5fa-108">После успешного размещения вызова состояние вызова обычно переводится в состояние ожидания.</span><span class="sxs-lookup"><span data-stu-id="7c5fa-108">After a call has been successfully placed on hold, the call state typically transitions to the onhold state.</span></span> <span data-ttu-id="7c5fa-109">Пока вызов удерживается, приложение может получить сообщения об изменениях состояния удерживаемого вызова.</span><span class="sxs-lookup"><span data-stu-id="7c5fa-109">While a call is on hold, the application can receive messages about state changes of the held call.</span></span> <span data-ttu-id="7c5fa-110">Например, если заблокированная сторона зависает, состояние вызова может перейти в режим «отключено».</span><span class="sxs-lookup"><span data-stu-id="7c5fa-110">For example, if the held party hangs up, the call state can transition to disconnected.</span></span>

<span data-ttu-id="7c5fa-111">В ситуации с мостом операция удержания может фактически не полагать на удержание вызова.</span><span class="sxs-lookup"><span data-stu-id="7c5fa-111">In a bridged situation, the hold operation may not actually place the call on hold.</span></span> <span data-ttu-id="7c5fa-112">Состояние других станций в вызове может управлять (например, пытаться "удерживать" вызов, если другие станции не могут быть задействованы); Вместо этого вызов можно просто изменить на неактивное состояние, когда оно останется подключенным к другим станциям.</span><span class="sxs-lookup"><span data-stu-id="7c5fa-112">The status of other stations on the call can govern (for example, attempting to "hold" a call when other stations are participating is not possible); instead, the call can simply be changed to the inactive state while it remains connected at other stations.</span></span>

<span data-ttu-id="7c5fa-113">Не все поставщики служб поддерживают использование этой операции.</span><span class="sxs-lookup"><span data-stu-id="7c5fa-113">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="7c5fa-114">**Интерфейс TAPI 2. x:** См. раздел [**линехолд**](/windows/win32/api/tapi/nf-tapi-linehold), [**линеунхолд**](/windows/win32/api/tapi/nf-tapi-lineunhold).</span><span class="sxs-lookup"><span data-stu-id="7c5fa-114">**TAPI 2.x:** See [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold), [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold).</span></span>

<span data-ttu-id="7c5fa-115">**Интерфейс TAPI 3. x:** См. раздел [**итбасиккаллконтрол:: Hold**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold).</span><span class="sxs-lookup"><span data-stu-id="7c5fa-115">**TAPI 3.x:** See [**ITBasicCallControl::Hold**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold).</span></span>

 

 
