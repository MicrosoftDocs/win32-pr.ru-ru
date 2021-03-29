---
title: Create-Session
description: Используйте пакет Create-Session, чтобы запросить сеанс передачи с сервером BITS.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Create-Sessionные БИТЫ
topic_type:
- apiref
api_name:
- Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425ad3bd36305f94547cf2cd8b13c1a420491499
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487092"
---
# <a name="create-session"></a><span data-ttu-id="b3afe-104">Create-Session</span><span class="sxs-lookup"><span data-stu-id="b3afe-104">Create-Session</span></span>

<span data-ttu-id="b3afe-105">Используйте пакет **создания сеанса** , чтобы запросить сеанс передачи с сервером BITS.</span><span class="sxs-lookup"><span data-stu-id="b3afe-105">Use the **Create-Session** packet to request an upload session with the BITS server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Create-Session
BITS-Supported-Protocols: {guid1} ... {guidN}
```

## <a name="headers"></a><span data-ttu-id="b3afe-106">Заголовки</span><span class="sxs-lookup"><span data-stu-id="b3afe-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="b3afe-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_запись BITS</span><span class="sxs-lookup"><span data-stu-id="b3afe-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="b3afe-108">Команда, относящаяся к службе BITS, которая определяет этот пакет серверу BITS.</span><span class="sxs-lookup"><span data-stu-id="b3afe-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="b3afe-109">Замените Remote-URL абсолютным или относительным URI.</span><span class="sxs-lookup"><span data-stu-id="b3afe-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="b3afe-110">Обычно замените Remote-URL именем удаленного файла задания.</span><span class="sxs-lookup"><span data-stu-id="b3afe-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="b3afe-111">Рекомендации по балансировке сетевой нагрузки см. в заголовке BITS-Host-ID.</span><span class="sxs-lookup"><span data-stu-id="b3afe-111">For network load balancing considerations, see the BITS-Host-Id header.</span></span>

</dd> <dt>

<span data-ttu-id="b3afe-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span><span class="sxs-lookup"><span data-stu-id="b3afe-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="b3afe-113">Идентифицирует этот пакет запроса как пакет Create-Session.</span><span class="sxs-lookup"><span data-stu-id="b3afe-113">Identifies this request packet as a Create-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="b3afe-114"><span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>Поддерживаемые BITS — протоколы</span><span class="sxs-lookup"><span data-stu-id="b3afe-114"><span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>BITS-Supported-Protocols</span></span>
</dt> <dd>

<span data-ttu-id="b3afe-115">Разделенный пробелами список протоколов, поддерживаемых клиентом.</span><span class="sxs-lookup"><span data-stu-id="b3afe-115">Space-delimited list of the protocols that the client supports.</span></span> <span data-ttu-id="b3afe-116">Используйте строковые идентификаторы GUID для обнаружения протоколов.</span><span class="sxs-lookup"><span data-stu-id="b3afe-116">Use string GUIDs to identify the protocols.</span></span> <span data-ttu-id="b3afe-117">Укажите список в порядке предпочтения от наиболее предпочтительных.</span><span class="sxs-lookup"><span data-stu-id="b3afe-117">Specify the list in order of preference from most to least preferred.</span></span> <span data-ttu-id="b3afe-118">В следующей таблице перечислены протоколы, поддерживаемые клиентом BITS.</span><span class="sxs-lookup"><span data-stu-id="b3afe-118">The following table lists the protocol that the BITS client supports.</span></span> <span data-ttu-id="b3afe-119">Замените {GUID1}... {Гуидн} с одним или несколькими строковыми идентификаторами GUID из списка.</span><span class="sxs-lookup"><span data-stu-id="b3afe-119">Replace {guid1} ... {guidN} with one or more string GUIDs from the list.</span></span>



| <span data-ttu-id="b3afe-120">Протокол</span><span class="sxs-lookup"><span data-stu-id="b3afe-120">Protocol</span></span>                                          | <span data-ttu-id="b3afe-121">Описание</span><span class="sxs-lookup"><span data-stu-id="b3afe-121">Description</span></span>                         |
|---------------------------------------------------|-------------------------------------|
| <span data-ttu-id="b3afe-122">{7df0354d-249b-430f-820d-3d2a9bef4931}</span><span class="sxs-lookup"><span data-stu-id="b3afe-122">{7df0354d-249b-430f-820d-3d2a9bef4931}</span></span><br/> | <span data-ttu-id="b3afe-123">Протокол отправки BITS 1,5</span><span class="sxs-lookup"><span data-stu-id="b3afe-123">BITS 1.5 Upload Protocol</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3afe-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3afe-124">Remarks</span></span>

<span data-ttu-id="b3afe-125">Перед отправкой пакета Create-Session необходимо отправить пакет [**проверки связи**](ping.md) для установки HTTP-соединения.</span><span class="sxs-lookup"><span data-stu-id="b3afe-125">You should send a [**Ping**](ping.md) packet to establish an HTTP connection before sending the Create-Session packet.</span></span> <span data-ttu-id="b3afe-126">Пакет Create-Session может также установить соединение. Однако Create-Session пакет менее эффективен.</span><span class="sxs-lookup"><span data-stu-id="b3afe-126">The Create-Session packet can also establish the connection; however, the Create-Session packet is less efficient.</span></span>

<span data-ttu-id="b3afe-127">Сервер выбирает нужный протокол из списка, который предоставляется клиентом в заголовке BITS-Supported-protocols.</span><span class="sxs-lookup"><span data-stu-id="b3afe-127">The server selects the protocol it wants to use from the list the client provides in the BITS-Supported-Protocols header.</span></span> <span data-ttu-id="b3afe-128">Сервер возвращает выбранный протокол в заголовке BITS-Protocol [**подтверждения для пакета ответа на создание сеанса**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="b3afe-128">The server returns the selected protocol in the BITS-Protocol header of the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

<span data-ttu-id="b3afe-129">Клиент ожидает, что сервер возвратит подтверждение на ответный пакет [**для создания сеанса**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="b3afe-129">The client expects the server to return an [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span> <span data-ttu-id="b3afe-130">Если серверу удалось установить сеанс, клиент использует пакет запроса [**фрагмента**](fragment.md) для отправки диапазонов файла на сервер.</span><span class="sxs-lookup"><span data-stu-id="b3afe-130">If the server was able to establish a session, the client uses the [**Fragment**](fragment.md) request packet to send ranges of the file to the server.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3afe-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3afe-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3afe-132">**Подтверждение для создания сеанса**</span><span class="sxs-lookup"><span data-stu-id="b3afe-132">**Ack for Create-Session**</span></span>](ack-for-create-session.md)
</dt> <dt>

[<span data-ttu-id="b3afe-133">**Fragment**</span><span class="sxs-lookup"><span data-stu-id="b3afe-133">**Fragment**</span></span>](fragment.md)
</dt> <dt>

[<span data-ttu-id="b3afe-134">**Проверок**</span><span class="sxs-lookup"><span data-stu-id="b3afe-134">**Ping**</span></span>](ping.md)
</dt> </dl>

 

 





