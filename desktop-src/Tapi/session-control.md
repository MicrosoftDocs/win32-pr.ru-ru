---
description: Сеанс или вызов представляет соединение между двумя или более адресами.
ms.assetid: f598c1cd-2b50-4ac6-a05e-4fd8eeb5e3e1
title: Управление сеансом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09250a90f978bde9be4f20aad6ee38f5e9766818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819417"
---
# <a name="session-control"></a><span data-ttu-id="9e0a6-103">Управление сеансом</span><span class="sxs-lookup"><span data-stu-id="9e0a6-103">Session Control</span></span>

<span data-ttu-id="9e0a6-104">Сеанс или вызов представляет соединение между двумя или более адресами.</span><span class="sxs-lookup"><span data-stu-id="9e0a6-104">A session or call represents a connection between two or more addresses.</span></span> <span data-ttu-id="9e0a6-105">Это подключение является динамическим, и связанные программные объекты должны создаваться, обрабатываться и освобождаться по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="9e0a6-105">This connection is dynamic, and the associated programming objects must be created, manipulated, and released as needed.</span></span> <span data-ttu-id="9e0a6-106">В самом простом случае это означает создание и отключение телефонного звонка.</span><span class="sxs-lookup"><span data-stu-id="9e0a6-106">In the simplest case, this means making and disconnecting a phone call.</span></span> <span data-ttu-id="9e0a6-107">Для опытных приложений Управление сеансами может заключаться в управлении Конференцией мультимедиа по IP-сети до уровня отдельных участников.</span><span class="sxs-lookup"><span data-stu-id="9e0a6-107">For advanced applications, session control may involve managing multimedia conferences over an IP network down to the level of individual participants.</span></span>

<span data-ttu-id="9e0a6-108">Управление сеансом состоит из двух основных областей:</span><span class="sxs-lookup"><span data-stu-id="9e0a6-108">Session control involves two basic areas:</span></span>

-   <span data-ttu-id="9e0a6-109">[Операции с сеансами](session-operations-ovr.md) — это элементы управления, которые инициируют, обслуживают и завершают сеанс связи.</span><span class="sxs-lookup"><span data-stu-id="9e0a6-109">[Session Operations](session-operations-ovr.md) are controls that initiate, maintain, and terminate a communications session.</span></span>
-   <span data-ttu-id="9e0a6-110">[Сведения о сеансе](session-information-ovr.md) описывают данные, которые могут быть получены по сеансу связи.</span><span class="sxs-lookup"><span data-stu-id="9e0a6-110">[Session Information](session-information-ovr.md) describes data that can be obtained concerning a communications session.</span></span>

<span data-ttu-id="9e0a6-111">В этом разделе не рассматриваются два специализированных типа управления сеансами.</span><span class="sxs-lookup"><span data-stu-id="9e0a6-111">Two specialized types of session control are not covered in this section.</span></span> <span data-ttu-id="9e0a6-112">Сведения об автоматических центрах распространения вызовов см. в разделе [Управление центром](./call-center-control.md) обработки вызовов (TAPI 2. x) или [сведения об элементах управления центра обработки вызовов](about-call-center-controls.md) (TAPI 3. x).</span><span class="sxs-lookup"><span data-stu-id="9e0a6-112">For information on Automatic Call Distribution Centers, see [Call Center Control](./call-center-control.md) (TAPI 2.x) or [About Call Center Controls](about-call-center-controls.md) (TAPI 3.x).</span></span> <span data-ttu-id="9e0a6-113">Сведения об IP-конференциях см. в статье [о конференц-телефонии для встреч](about-rendezvous-ip-telephony-conferencing.md).</span><span class="sxs-lookup"><span data-stu-id="9e0a6-113">For information on IP conferencing, see [About Rendezvous IP Telephony Conferencing](about-rendezvous-ip-telephony-conferencing.md).</span></span>

 

 
