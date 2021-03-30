---
description: Перенаправление сеанса позволяет приложению отклонения от предлагаемого сеанса к другому адресу без ответа на вызов.
ms.assetid: b52cd5c2-fdd6-4240-b07b-b22733a89d27
title: перенаправление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100ade9315c3b5e8e68c17bf34a0b6d54a9d9663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819433"
---
# <a name="redirect"></a><span data-ttu-id="2bba6-103">перенаправление</span><span class="sxs-lookup"><span data-stu-id="2bba6-103">Redirect</span></span>

<span data-ttu-id="2bba6-104">Перенаправление сеанса позволяет приложению отклонения от предлагаемого сеанса к другому адресу без ответа на вызов.</span><span class="sxs-lookup"><span data-stu-id="2bba6-104">Session redirection allows an application to deflect an offered session to another address without answering the call.</span></span> <span data-ttu-id="2bba6-105">Приложение может выполнять перенаправление на основе вызова по требованию.</span><span class="sxs-lookup"><span data-stu-id="2bba6-105">The application can do redirection on a call-by-call basis.</span></span> <span data-ttu-id="2bba6-106">Например, приложение может разрешить пользователю указывать различные перенаправления на основе сведений об ИДЕНТИФИКАТОРе звонящего.</span><span class="sxs-lookup"><span data-stu-id="2bba6-106">For example, an application might allow a user to specify different redirections based on caller ID information.</span></span> <span data-ttu-id="2bba6-107">После успешного перенаправления вызова состояние обычно переходит в режим бездействия и связанные ресурсы должны быть освобождены.</span><span class="sxs-lookup"><span data-stu-id="2bba6-107">After a call has been successfully redirected, the state typically transitions to idle and associated resources must be released.</span></span>

<span data-ttu-id="2bba6-108">Перенаправление отличается от переадресации. После настройки [пересылки операция](forward-ovr.md) выполняется TAPI, поставщиком услуг или коммутатором без дальнейшего участия в приложении.</span><span class="sxs-lookup"><span data-stu-id="2bba6-108">Redirect differs from [forward](forward-ovr.md) in that once forwarding has been set up, the operation is performed by TAPI, the service provider, or the switch without further involvement of the application.</span></span> <span data-ttu-id="2bba6-109">Перенаправление отличается от [перемещения](transfer-ovr.md) в этом перенаправлении не требует первого ответа на вызов.</span><span class="sxs-lookup"><span data-stu-id="2bba6-109">Redirect differs from [transfer](transfer-ovr.md) in that redirect does not require answering the call first.</span></span>

<span data-ttu-id="2bba6-110">Не все поставщики служб поддерживают использование этой операции.</span><span class="sxs-lookup"><span data-stu-id="2bba6-110">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="2bba6-111">**Интерфейс TAPI 2. x:** См. [**линередирект**](/windows/win32/api/tapi/nf-tapi-lineredirect).</span><span class="sxs-lookup"><span data-stu-id="2bba6-111">**TAPI 2.x:** See [**lineRedirect**](/windows/win32/api/tapi/nf-tapi-lineredirect).</span></span>

 

 
