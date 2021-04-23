---
description: Правильное завершение сеансов связи и всего приложения требуется для предотвращения того, что ресурсы остаются связанными в вызовах или приложениях, которые больше не нужны.
ms.assetid: 40694b7f-474b-41aa-be3f-48e4ca517a6f
title: Завершение работы TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661273a3d72559d965fa1ea6066f1090f8e6b6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684316"
---
# <a name="tapi-shutdown"></a><span data-ttu-id="f920b-103">Завершение работы TAPI</span><span class="sxs-lookup"><span data-stu-id="f920b-103">TAPI Shutdown</span></span>

<span data-ttu-id="f920b-104">Правильное завершение сеансов связи и всего приложения требуется для предотвращения того, что ресурсы остаются связанными в вызовах или приложениях, которые больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="f920b-104">Proper shutdown of communications sessions and of an entire application is required to prevent resources from remaining tied up in calls or applications that no longer need them.</span></span>

<span data-ttu-id="f920b-105">TAPI предоставляет ряд функций и методов, которые помогут в процессе.</span><span class="sxs-lookup"><span data-stu-id="f920b-105">TAPI provides a series of functions and methods to assist in the process.</span></span> <span data-ttu-id="f920b-106">Очевидно, что приложение должно также принять ответственность за правильное освобождение выделенной памяти, будь то структура данных или ссылки COM.</span><span class="sxs-lookup"><span data-stu-id="f920b-106">Obviously, the application must also take responsibility for properly releasing allocated memory, whether in the form of data structures or COM references.</span></span>



| <span data-ttu-id="f920b-107">Функции TAPI 2. x</span><span class="sxs-lookup"><span data-stu-id="f920b-107">TAPI 2.x functions</span></span>                                                            | <span data-ttu-id="f920b-108">Описание</span><span class="sxs-lookup"><span data-stu-id="f920b-108">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="f920b-109">**линерегистеррекуестреЦипиент**</span><span class="sxs-lookup"><span data-stu-id="f920b-109">**lineRegisterRequestRecipient**</span></span>](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) | <span data-ttu-id="f920b-110">Отменяет регистрацию приложения в качестве обработчика для вызовов телефонной связи.</span><span class="sxs-lookup"><span data-stu-id="f920b-110">Unregisters the application as a handler for assisted telephony calls.</span></span> |
| [<span data-ttu-id="f920b-111">**линеклосе**</span><span class="sxs-lookup"><span data-stu-id="f920b-111">**lineClose**</span></span>](/windows/win32/api/tapi/nf-tapi-lineclose)                                       | <span data-ttu-id="f920b-112">Отключает приложение от имени руководителя для вызовов в данной строке.</span><span class="sxs-lookup"><span data-stu-id="f920b-112">Disconnects the application as a manager for calls on the given line.</span></span>  |
| [<span data-ttu-id="f920b-113">**линешутдовн**</span><span class="sxs-lookup"><span data-stu-id="f920b-113">**lineShutdown**</span></span>](/windows/win32/api/tapi/nf-tapi-lineshutdown)                                 | <span data-ttu-id="f920b-114">Завершает использование абстракции строки приложением.</span><span class="sxs-lookup"><span data-stu-id="f920b-114">Shuts down the application's usage of the line abstraction.</span></span>            |



 



| <span data-ttu-id="f920b-115">Интерфейсы или методы интерфейса TAPI 3. x</span><span class="sxs-lookup"><span data-stu-id="f920b-115">TAPI 3.x interfaces or methods</span></span>                                            | <span data-ttu-id="f920b-116">Описание</span><span class="sxs-lookup"><span data-stu-id="f920b-116">Description</span></span>                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="f920b-117">**ИТТАПИ:: Унрегистернотификатионс**</span><span class="sxs-lookup"><span data-stu-id="f920b-117">**ITTAPI::UnregisterNotifications**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-unregisternotifications) | <span data-ttu-id="f920b-118">Удаляет все регистрации уведомлений о событиях, выполняемые приложением.</span><span class="sxs-lookup"><span data-stu-id="f920b-118">Removes any event notification registrations performed by the application.</span></span> |
| [<span data-ttu-id="f920b-119">**ИТТАПИ:: Shutdown**</span><span class="sxs-lookup"><span data-stu-id="f920b-119">**ITTAPI::Shutdown**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-shutdown)                               | <span data-ttu-id="f920b-120">Отключает приложение как Диспетчер вызовов.</span><span class="sxs-lookup"><span data-stu-id="f920b-120">Disconnects the application as a call manager.</span></span>                             |



 

 

 
