---
description: Объект запроса создается с помощью CoCreateInstance COM и предоставляет один интерфейс Итрекуест.
ms.assetid: 1e4c71ce-6846-4e64-9346-455ed82aa458
title: Объект запроса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51e81cae01f2624ba863b304c0a5f732b221199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673705"
---
# <a name="request-object"></a><span data-ttu-id="fd540-103">Объект запроса</span><span class="sxs-lookup"><span data-stu-id="fd540-103">Request Object</span></span>

<span data-ttu-id="fd540-104">Объект запроса создается с помощью **COCREATEINSTANCE** com и предоставляет один интерфейс [**итрекуест**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest).</span><span class="sxs-lookup"><span data-stu-id="fd540-104">The Request Object is created using COM **CoCreateInstance** and exposes one interface, [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest).</span></span> <span data-ttu-id="fd540-105">Этот интерфейс предоставляет метод [**MAKECALL**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) , позволяющий приложению TAPI 3 использовать телефонные телефония.</span><span class="sxs-lookup"><span data-stu-id="fd540-105">This interface exposes the [**MakeCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) method, which allows a TAPI 3 application to use Assisted Telephony.</span></span> <span data-ttu-id="fd540-106">Служба поддержки телефонии предоставляет приложениям с поддержкой телефонии простой механизм для телефонных звонков, не требуя от разработчика полноценного участия в телефонии.</span><span class="sxs-lookup"><span data-stu-id="fd540-106">Assisted Telephony provides telephony-enabled applications with a simple mechanism for making phone calls without requiring the developer to become fully literate in telephony.</span></span>

<span data-ttu-id="fd540-107">Например, приложение электронной таблицы может добавить кнопку "позвонить" с помощью вспомогательной телефонии, не реализуя более сложные элементы управления, доступные в полном приложении TAPI.</span><span class="sxs-lookup"><span data-stu-id="fd540-107">For example, a spreadsheet application can add a "Make Call" button using Assisted Telephony without implementing the more elaborate controls available in a full TAPI application.</span></span>

<span data-ttu-id="fd540-108">Дополнительные сведения см. в [обзоре службы технической поддержки](assisted-telephony-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="fd540-108">See the [Assisted Telephony Overview](assisted-telephony-overview.md) for additional information.</span></span>

 

 



