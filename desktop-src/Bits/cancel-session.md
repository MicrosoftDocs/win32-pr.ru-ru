---
title: Cancel-Session
description: Используйте пакет Cancel-Session, чтобы завершить сеанс передачи с сервером BITS.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- Cancel-Sessionные БИТЫ
topic_type:
- apiref
api_name:
- Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 017097bea656309aabf3d773f34152805fd6a579
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105654251"
---
# <a name="cancel-session"></a><span data-ttu-id="de469-104">Cancel-Session</span><span class="sxs-lookup"><span data-stu-id="de469-104">Cancel-Session</span></span>

<span data-ttu-id="de469-105">Используйте пакет **Cancel-Session** для завершения сеанса передачи с сервером BITS.</span><span class="sxs-lookup"><span data-stu-id="de469-105">Use the **Cancel-Session** packet to terminate the upload session with the BITS server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Cancel-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a><span data-ttu-id="de469-106">Заголовки</span><span class="sxs-lookup"><span data-stu-id="de469-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="de469-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_запись BITS</span><span class="sxs-lookup"><span data-stu-id="de469-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="de469-108">Команда, относящаяся к службе BITS, которая определяет этот пакет серверу BITS.</span><span class="sxs-lookup"><span data-stu-id="de469-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="de469-109">Замените Remote-URL абсолютным или относительным URI.</span><span class="sxs-lookup"><span data-stu-id="de469-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="de469-110">Обычно замените Remote-URL именем удаленного файла задания.</span><span class="sxs-lookup"><span data-stu-id="de469-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="de469-111">Рекомендации по балансировке сетевой нагрузки см. в заголовке BITS-Host-ID в пакете [**создания сеанса**](create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="de469-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="de469-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span><span class="sxs-lookup"><span data-stu-id="de469-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="de469-113">Идентифицирует этот пакет запроса как пакет Cancel-Session.</span><span class="sxs-lookup"><span data-stu-id="de469-113">Identifies this request packet as a Cancel-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="de469-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS — Session-ID</span><span class="sxs-lookup"><span data-stu-id="de469-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="de469-115">Строковый идентификатор GUID, определяющий сеанс на сервере.</span><span class="sxs-lookup"><span data-stu-id="de469-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="de469-116">Замените {GUID} идентификатором сеанса, возвращаемым сервером в ответ на запрос на создание пакета ответа [**для создания сеанса**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="de469-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de469-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de469-117">Remarks</span></span>

<span data-ttu-id="de469-118">Этот пакет отменяет задание отправки, если оно отправляется до отправки последнего фрагмента.</span><span class="sxs-lookup"><span data-stu-id="de469-118">This packet cancels an upload job if it is sent before the last fragment is sent.</span></span> <span data-ttu-id="de469-119">Cancel-Session не влияет на файл, последний фрагмент которого уже был отправлен.</span><span class="sxs-lookup"><span data-stu-id="de469-119">Cancel-Session has no effect on a file whose last fragment has already been sent.</span></span> <span data-ttu-id="de469-120">Когда сервер BITS получает последний фрагмент, он записывает файл в конечное место назначения, а в случае отправки-ответа отправляет файл в серверное приложение.</span><span class="sxs-lookup"><span data-stu-id="de469-120">When the BITS server receives the last fragment, it writes the file to its final destination and, in the case of an upload-reply, posts the file to the server application.</span></span> <span data-ttu-id="de469-121">В случае отправки-ответа пакет Cancel-Session отменяет часть ответа задания отправки и ответа.</span><span class="sxs-lookup"><span data-stu-id="de469-121">In the upload-reply case, the Cancel-Session packet cancels the reply portion of an upload-reply job.</span></span>

<span data-ttu-id="de469-122">Сервер BITS освобождает все ресурсы и удаляет все временные файлы при получении этого пакета.</span><span class="sxs-lookup"><span data-stu-id="de469-122">The BITS server releases all resources and deletes all temporary files when it receives this packet.</span></span>

<span data-ttu-id="de469-123">Клиент BITS отправляет этот пакет, когда пользователь отменяет задание.</span><span class="sxs-lookup"><span data-stu-id="de469-123">The BITS client sends this packet when the user cancels the job.</span></span>

## <a name="see-also"></a><span data-ttu-id="de469-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de469-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de469-125">**Подтверждение для создания сеанса**</span><span class="sxs-lookup"><span data-stu-id="de469-125">**Ack for Create-Session**</span></span>](ack-for-create-session.md)
</dt> <dt>

[<span data-ttu-id="de469-126">**Закрыть — сеанс**</span><span class="sxs-lookup"><span data-stu-id="de469-126">**Close-Session**</span></span>](close-session.md)
</dt> </dl>

 

 




