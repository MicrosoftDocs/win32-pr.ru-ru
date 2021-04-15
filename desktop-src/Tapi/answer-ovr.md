---
description: Операция ответа представляет собой типичный ответ на предлагаемый сеанс связи. В случае успеха эта операция приведет к переходу сеанса в состояние подключения.
ms.assetid: 34ac0b34-1d1b-4657-a737-27a4ed9326af
title: Ответ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e08081b32b7ba3a3a24cde3ec37c1a6118582cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545655"
---
# <a name="answer"></a><span data-ttu-id="63127-104">Ответ</span><span class="sxs-lookup"><span data-stu-id="63127-104">Answer</span></span>

<span data-ttu-id="63127-105">Операция ответа представляет собой типичный ответ приложения на предлагаемый сеанс связи.</span><span class="sxs-lookup"><span data-stu-id="63127-105">The answer operation is an application's typical response to an offered communications session.</span></span> <span data-ttu-id="63127-106">В случае успеха эта операция приведет к переходу сеанса в состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="63127-106">If successful, this operation causes a session to transition into the connected state.</span></span>

<span data-ttu-id="63127-107">В некоторых средах телефонии (например, ISDN), где оповещения пользователя отделены от предложения о вызовах, приложение имеет возможность [принять](accept-ovr.md) вызов перед ответом или отклонить ([Удалить](drop-ovr.md)) или [перенаправить](redirect-ovr.md) вызов *предложения* .</span><span class="sxs-lookup"><span data-stu-id="63127-107">In some telephony environments (like ISDN), where user alerting is separate from call offering, the application has the option to [accept](accept-ovr.md) a call prior to answering or to reject ([drop](drop-ovr.md)) or [redirect](redirect-ovr.md) the *offering* call.</span></span>

<span data-ttu-id="63127-108">Если операция ответа выполняется для нового сеанса, когда сеанс уже активен, то воздействие этого на существующий активный сеанс зависит от возможностей поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="63127-108">If an answer operation is performed for a new session when a session is already active, the effect this has on the existing active session depends on the service provider's capabilities.</span></span> <span data-ttu-id="63127-109">Первый вызов может быть нетронут, он может быть автоматически удален или автоматически помещен в удержание.</span><span class="sxs-lookup"><span data-stu-id="63127-109">The first call can be unaffected, it can automatically be dropped, or it can automatically be placed on hold.</span></span> <span data-ttu-id="63127-110">TAPI будет отправлять соответствующие уведомления о событиях, касающиеся обоих вызовов.</span><span class="sxs-lookup"><span data-stu-id="63127-110">TAPI will send the appropriate event notifications concerning both calls.</span></span>

<span data-ttu-id="63127-111">В ситуации с мостом, если вызов подключен, но находится в активном состоянии, его можно объединить с помощью операции ответа.</span><span class="sxs-lookup"><span data-stu-id="63127-111">In a bridged situation, if a call is connected but in the active state, it can be joined using the answer operation.</span></span>

<span data-ttu-id="63127-112">Приложение может отправить сведения о пользователе во время ответа, если поставщик услуг его поддерживает.</span><span class="sxs-lookup"><span data-stu-id="63127-112">The application has the option to send user-user information at the time of the answer, if the service provider supports it.</span></span>

<span data-ttu-id="63127-113">**Интерфейс TAPI 2. x:** См. [**линеансвер**](/windows/win32/api/tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="63127-113">**TAPI 2.x:** See [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).</span></span>

<span data-ttu-id="63127-114">**Интерфейс TAPI 3. x:** См. раздел [**итбасиккаллконтрол:: Answer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).</span><span class="sxs-lookup"><span data-stu-id="63127-114">**TAPI 3.x:** See [**ITBasicCallControl::Answer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).</span></span>

 

 
