---
description: Операция подбора позволяет приложению ответить на сеанс, который оповещает по другому адресу. Приложение определяет цель отправки и возвращает идентификатор сеанса для подобранного вызова.
ms.assetid: 3dfbb5c0-b533-403f-ad6c-b9e1b52ab47a
title: Кладки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e033689ffccf6ba01ad06eb071514c1c37aaca03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816137"
---
# <a name="pickup"></a><span data-ttu-id="cd0f5-104">Кладки</span><span class="sxs-lookup"><span data-stu-id="cd0f5-104">Pickup</span></span>

<span data-ttu-id="cd0f5-105">Операция подбора позволяет приложению ответить на сеанс, который оповещает по другому адресу.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-105">The pickup operation allows an application to answer a session that is alerting at another address.</span></span> <span data-ttu-id="cd0f5-106">Приложение определяет цель отправки и возвращает идентификатор сеанса для подобранного вызова.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-106">The application identifies the target of the pickup and is returned a session identifier for the picked-up call.</span></span>

<span data-ttu-id="cd0f5-107">Существует несколько способов определения цели запроса на расзапрос раскладки.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-107">There are several ways to identify the target of the pickup request.</span></span> <span data-ttu-id="cd0f5-108">Сначала приложение может указать адрес стороны предупреждения.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-108">First, the application may specify the address of the alerting party.</span></span> <span data-ttu-id="cd0f5-109">Во-вторых, если адрес не указан и переключатель разрешает его, приложение может выбрать любой сеанс предупреждений в группе приема.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-109">Second, if no address is specified and the switch allows it, the application can pick up any alerting session in its pickup group.</span></span> <span data-ttu-id="cd0f5-110">В-третьих, некоторые коммутаторы позволяют получать предупреждения сеанса в другой группе отправки, если указан идентификатор группы.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-110">Third, some switches allow pickup of a session alerting in a different pickup group if the group identifier is specified.</span></span>

<span data-ttu-id="cd0f5-111">Некоторые ключевые телефонные системы поддерживают *Перенос через функцию удержания* на внешнем виде вызовов, исключающих мост.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-111">Some key telephone systems support a *transfer through hold* capability on bridged-exclusive call appearances.</span></span> <span data-ttu-id="cd0f5-112">В этой схеме конкретный телефон владеет вызовом только в том случае, если вызов активен, но когда вызов удерживается, любой телефон, имеющий внешний вид строки, может получить вызов.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-112">In this scheme, a particular phone owns a call exclusively when the call is active, but when the call is on hold, any phone that has an appearance of the line can pick up the call.</span></span>

<span data-ttu-id="cd0f5-113">**Интерфейс TAPI 2. x:** Для этой цели приложение может использовать операцию раскладки с конечным адресом **null** , аналогично тому, как функция используется для получения вызова в режиме ожидания в аналоговой строке.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-113">**TAPI 2.x:** An application can use a pickup operation with a **NULL** target address for this purpose, similar to how the function is used to pick up a call waiting call on an analog line.</span></span> <span data-ttu-id="cd0f5-114">ЛИНЕАДДРФЕАТУРЕ \_ пиккуфелд указывает на наличие возможности.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-114">LINEADDRFEATURE\_PICKUPHELD indicates the existence of the capability.</span></span>

<span data-ttu-id="cd0f5-115">Если ЛИНЕАДДРКАПФЛАГС \_ пиккупкаллваит имеет **значение true**, можно выбрать сеанс, для которого пользователь обнаружил, что воспроизвести обнаружил сигнал о ожидании вызова, но для которого поставщик услуг не может выполнить обнаружение.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-115">If LINEADDRCAPFLAGS\_PICKUPCALLWAIT is **TRUE**, a session can be picked up for which the user has audibly detected the call-waiting signal but for which the service provider is unable to perform the detection.</span></span> <span data-ttu-id="cd0f5-116">Это дает пользователю механизм «ответить» на ожидание вызова, даже если поставщик услуг не смог обнаружить сигнал ожидания вызова.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-116">This gives the user a mechanism to "answer" a waiting call even though the service provider was unable to detect the call-waiting signal.</span></span> <span data-ttu-id="cd0f5-117">Адрес назначения и идентификатор группы должны быть **равны NULL** , чтобы получить вызов, ожидающий вызова.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-117">Both the destination address and the group ID must be **NULL** to pick up a call-waiting call.</span></span>

<span data-ttu-id="cd0f5-118">Когда сеанс успешно забирается, приложение получает уведомление об изменении состояния с указанием [причины](reason-ovr.md) линекаллреасонной \_ отправки.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-118">When a session has been picked up successfully, the application receives a state change notification with the [reason](reason-ovr.md) set to LINECALLREASON\_PICKUP.</span></span>

<span data-ttu-id="cd0f5-119">Не все поставщики служб поддерживают использование этой операции.</span><span class="sxs-lookup"><span data-stu-id="cd0f5-119">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="cd0f5-120">**Интерфейс TAPI 2. x:** См. [**линепиккуп**](/windows/win32/api/tapi/nf-tapi-linepickup).</span><span class="sxs-lookup"><span data-stu-id="cd0f5-120">**TAPI 2.x:** See [**linePickup**](/windows/win32/api/tapi/nf-tapi-linepickup).</span></span>

<span data-ttu-id="cd0f5-121">**Интерфейс TAPI 3. x:** См. раздел [**итбасиккаллконтрол::P иккуп**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup).</span><span class="sxs-lookup"><span data-stu-id="cd0f5-121">**TAPI 3.x:** See [**ITBasicCallControl::Pickup**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup).</span></span>

 

 
