---
description: Следующие термины полезны для понимания технологии TAPI.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 23331332-38bc-41b9-84c4-281722ddf563
title: C (API телефонии)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c6fade540235ef6c68b42a0aba364038d674e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673525"
---
# <a name="c-telephony-api"></a><span data-ttu-id="2b176-103">C (API телефонии)</span><span class="sxs-lookup"><span data-stu-id="2b176-103">C (Telephony API)</span></span>

<span data-ttu-id="2b176-104">[A](a-tapgloss.md) [B](b-tapgloss.md) C [D](d-tapgloss.md) [E](e-tapgloss.md) F G [р](h-tapgloss.md) [.](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="2b176-104">[A](a-tapgloss.md) [B](b-tapgloss.md) C [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="2b176-105"><span id="tapi2.call_classification_tapgloss"></span><span id="TAPI2.CALL_CLASSIFICATION_TAPGLOSS"></span>**Классификация вызовов**</span><span class="sxs-lookup"><span data-stu-id="2b176-105"><span id="tapi2.call_classification_tapgloss"></span><span id="TAPI2.CALL_CLASSIFICATION_TAPGLOSS"></span>**call classification**</span></span>
</dt> <dd>

<span data-ttu-id="2b176-106">Процесс TAPI, сообщающий об изменениях в типе потока мультимедиа (голоса, факса, модема данных и т. д.) для участвующих приложений.</span><span class="sxs-lookup"><span data-stu-id="2b176-106">TAPI process that reports changes in the type of media stream (voice, fax, data modem, and so on) to participating applications.</span></span>

</dd> <dt>

<span data-ttu-id="2b176-107"><span id="tapi2.call_progress_monitoring_tapgloss"></span><span id="TAPI2.CALL_PROGRESS_MONITORING_TAPGLOSS"></span>**мониторинг хода вызова**</span><span class="sxs-lookup"><span data-stu-id="2b176-107"><span id="tapi2.call_progress_monitoring_tapgloss"></span><span id="TAPI2.CALL_PROGRESS_MONITORING_TAPGLOSS"></span>**call progress monitoring**</span></span>
</dt> <dd>

<span data-ttu-id="2b176-108">Процесс прослушивания звуковых тонов, таких как гудок, специальные информационные тона, сигналы занятости и звонка, для определения состояния звонка (его хода выполнения по сети).</span><span class="sxs-lookup"><span data-stu-id="2b176-108">The process of listening for audible tones such as a dial tone, special information tones, busy signals, and ringback tones to determine the state of a call (its progress through the network).</span></span>

</dd> <dt>

<span data-ttu-id="2b176-109"><span id="tapi2.call_redirection_tapgloss"></span><span id="TAPI2.CALL_REDIRECTION_TAPGLOSS"></span>**Перенаправление вызовов**</span><span class="sxs-lookup"><span data-stu-id="2b176-109"><span id="tapi2.call_redirection_tapgloss"></span><span id="TAPI2.CALL_REDIRECTION_TAPGLOSS"></span>**call redirection**</span></span>
</dt> <dd>

<span data-ttu-id="2b176-110">Функция, которая позволяет приложению отклонения от вызова предложения к другому адресу без предварительного ответа на вызов.</span><span class="sxs-lookup"><span data-stu-id="2b176-110">A function that allows an application to deflect an offering call to another address without first answering the call.</span></span> <span data-ttu-id="2b176-111">Перенаправление вызовов отличается от переадресации вызовов в том, что Пересылка вызовов выполняется с помощью параметра без участия приложения; перенаправление можно выполнить по требованию приложения, например, на основе сведений об ИДЕНТИФИКАТОРе вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="2b176-111">Call redirection differs from call forwarding in that call forwarding is performed by the switch without the involvement of the application; redirection can be done on a call-by-call basis by the application, for example, driven by caller ID information.</span></span> <span data-ttu-id="2b176-112">Он отличается от передачи вызова в том, что для передачи вызова необходимо сначала ответить на вызов.</span><span class="sxs-lookup"><span data-stu-id="2b176-112">It differs from call transfer in that transferring a call requires that the call first be answered.</span></span> <span data-ttu-id="2b176-113">См. раздел *вызванный идентификатор*, *идентификатор звонящего*, [*Перенаправление идентификатора*](r-tapgloss.md), [*идентификатор перенаправления*](r-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="2b176-113">See *called-ID*, *caller-ID*, [*redirecting ID*](r-tapgloss.md), [*redirection ID*](r-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b176-114"><span id="tapi2.called_id_tapgloss"></span><span id="TAPI2.CALLED_ID_TAPGLOSS"></span>**вызванный идентификатор**</span><span class="sxs-lookup"><span data-stu-id="2b176-114"><span id="tapi2.called_id_tapgloss"></span><span id="TAPI2.CALLED_ID_TAPGLOSS"></span>**called-ID**</span></span>
</dt> <dd>

<span data-ttu-id="2b176-115">Определяет исходный адрес назначения вызова.</span><span class="sxs-lookup"><span data-stu-id="2b176-115">Identifies the original destination address of a call.</span></span> <span data-ttu-id="2b176-116">См. раздел *Перенаправление вызова*.</span><span class="sxs-lookup"><span data-stu-id="2b176-116">See *call redirection*.</span></span>

</dd> <dt>

<span data-ttu-id="2b176-117"><span id="tapi2.caller_id_tapgloss"></span><span id="TAPI2.CALLER_ID_TAPGLOSS"></span>**Идентификатор звонящего**</span><span class="sxs-lookup"><span data-stu-id="2b176-117"><span id="tapi2.caller_id_tapgloss"></span><span id="TAPI2.CALLER_ID_TAPGLOSS"></span>**caller-ID**</span></span>
</dt> <dd>

<span data-ttu-id="2b176-118">Определяет исходный адрес вызова.</span><span class="sxs-lookup"><span data-stu-id="2b176-118">Identifies the originating address of a call.</span></span> <span data-ttu-id="2b176-119">См. раздел *Перенаправление вызова*.</span><span class="sxs-lookup"><span data-stu-id="2b176-119">See *call redirection*.</span></span>

</dd> <dt>

<span data-ttu-id="2b176-120"><span id="tapi2.central_office_tapgloss"></span><span id="TAPI2.CENTRAL_OFFICE_TAPGLOSS"></span>**Центральный офис**</span><span class="sxs-lookup"><span data-stu-id="2b176-120"><span id="tapi2.central_office_tapgloss"></span><span id="TAPI2.CENTRAL_OFFICE_TAPGLOSS"></span>**central office**</span></span>
</dt> <dd>

<span data-ttu-id="2b176-121">Локальная компания телефонной компании, которая предоставляет телефонную службу в определенной области.</span><span class="sxs-lookup"><span data-stu-id="2b176-121">Telephone company's local facility that provides telephone service in a specific area.</span></span> <span data-ttu-id="2b176-122">Как правило, линии подписчиков присоединяются к переключаемому оборудованию, соединяющему других подписчиков друг с другом, локально и на длинном расстоянии.</span><span class="sxs-lookup"><span data-stu-id="2b176-122">Typically, subscribers' lines are joined to switching equipment that connects other subscribers to each other, locally and over long distance.</span></span> <span data-ttu-id="2b176-123">Также называется *Co*.</span><span class="sxs-lookup"><span data-stu-id="2b176-123">Also called *CO*.</span></span>

</dd> <dt>

<span data-ttu-id="2b176-124"><span id="tapi2.centrex_tapgloss"></span><span id="TAPI2.CENTREX_TAPGLOSS"></span>**центрекс**</span><span class="sxs-lookup"><span data-stu-id="2b176-124"><span id="tapi2.centrex_tapgloss"></span><span id="TAPI2.CENTREX_TAPGLOSS"></span>**Centrex**</span></span>
</dt> <dd>

<span data-ttu-id="2b176-125">Служба рабочего телефона, предлагаемая местной телефонной компанией из местного центрального офиса.</span><span class="sxs-lookup"><span data-stu-id="2b176-125">A business telephone service offered by a local telephone company from a local, central office.</span></span>

</dd> <dt>

<span data-ttu-id="2b176-126"><span id="tapi2.computer_centric_connection_tapgloss"></span><span id="TAPI2.COMPUTER_CENTRIC_CONNECTION_TAPGLOSS"></span>**ориентированное на компьютер подключение**</span><span class="sxs-lookup"><span data-stu-id="2b176-126"><span id="tapi2.computer_centric_connection_tapgloss"></span><span id="TAPI2.COMPUTER_CENTRIC_CONNECTION_TAPGLOSS"></span>**computer-centric connection**</span></span>
</dt> <dd>

<span data-ttu-id="2b176-127">Подключение, которое использует карту надстройки компьютера или внешний ящик, подключенный к телефонной сети и набору телефонов.</span><span class="sxs-lookup"><span data-stu-id="2b176-127">A connection that uses a computer add-in card or external box that is connected to both the telephone network and the phone set.</span></span> <span data-ttu-id="2b176-128">Сравните [*подключение, ориентированное на телефон*](p-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="2b176-128">Compare [*phone-centric connection*](p-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b176-129"><span id="tapi2.connected_id_tapgloss"></span><span id="TAPI2.CONNECTED_ID_TAPGLOSS"></span>**подключенный ИД**</span><span class="sxs-lookup"><span data-stu-id="2b176-129"><span id="tapi2.connected_id_tapgloss"></span><span id="TAPI2.CONNECTED_ID_TAPGLOSS"></span>**connected-ID**</span></span>
</dt> <dd>

<span data-ttu-id="2b176-130">Идентификатор стороны, к которой вызывается фактический вызов.</span><span class="sxs-lookup"><span data-stu-id="2b176-130">Identifier for the party to which the call was actually connected.</span></span> <span data-ttu-id="2b176-131">Это может отличаться от вызываемой стороны, если вызов был передан.</span><span class="sxs-lookup"><span data-stu-id="2b176-131">This may be different from the called party if the call was diverted.</span></span>

</dd> </dl>

 

 



