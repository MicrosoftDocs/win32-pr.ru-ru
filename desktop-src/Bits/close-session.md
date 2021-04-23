---
title: Close-Session
description: Используйте пакет Close-Session, чтобы сообщить серверу BITS о завершении передачи файла и завершить сеанс.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- Close-Sessionные БИТЫ
topic_type:
- apiref
api_name:
- Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fe791ba4706689fd23dea8886f5b8f54f135841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889364"
---
# <a name="close-session"></a><span data-ttu-id="2e43f-104">Close-Session</span><span class="sxs-lookup"><span data-stu-id="2e43f-104">Close-Session</span></span>

<span data-ttu-id="2e43f-105">Используйте пакет **закрытия сеанса** , чтобы сообщить серверу BITS о завершении передачи файла и завершить сеанс.</span><span class="sxs-lookup"><span data-stu-id="2e43f-105">Use the **Close-Session** packet to tell the BITS server that file upload is complete and to end the session.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Close-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a><span data-ttu-id="2e43f-106">Заголовки</span><span class="sxs-lookup"><span data-stu-id="2e43f-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="2e43f-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_запись BITS</span><span class="sxs-lookup"><span data-stu-id="2e43f-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="2e43f-108">Команда, относящаяся к службе BITS, которая определяет этот пакет серверу BITS.</span><span class="sxs-lookup"><span data-stu-id="2e43f-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="2e43f-109">Замените Remote-URL абсолютным или относительным URI.</span><span class="sxs-lookup"><span data-stu-id="2e43f-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="2e43f-110">Обычно замените Remote-URL именем удаленного файла задания.</span><span class="sxs-lookup"><span data-stu-id="2e43f-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="2e43f-111">Рекомендации по балансировке сетевой нагрузки см. в заголовке BITS-Host-ID в пакете [**создания сеанса**](create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="2e43f-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="2e43f-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span><span class="sxs-lookup"><span data-stu-id="2e43f-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="2e43f-113">Идентифицирует этот пакет запроса как пакет Close-Session.</span><span class="sxs-lookup"><span data-stu-id="2e43f-113">Identifies this request packet as a Close-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="2e43f-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS — Session-ID</span><span class="sxs-lookup"><span data-stu-id="2e43f-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="2e43f-115">Строковый идентификатор GUID, определяющий сеанс на сервере.</span><span class="sxs-lookup"><span data-stu-id="2e43f-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="2e43f-116">Замените {GUID} идентификатором сеанса, возвращаемым сервером в ответ на запрос на создание пакета ответа [**для создания сеанса**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="2e43f-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e43f-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e43f-117">Remarks</span></span>

<span data-ttu-id="2e43f-118">Сервер BITS освобождает все ресурсы и удаляет все временные файлы при получении этого пакета.</span><span class="sxs-lookup"><span data-stu-id="2e43f-118">The BITS server releases all resources and deletes all temporary files when it receives this packet.</span></span>

<span data-ttu-id="2e43f-119">Для заданий отправки и ответа необходимо загрузить ответ перед отправкой **закрытого сеанса**.</span><span class="sxs-lookup"><span data-stu-id="2e43f-119">For upload-reply jobs, you must download the reply before sending **Close-Session**.</span></span> <span data-ttu-id="2e43f-120">В противном случае ответ будет потерян.</span><span class="sxs-lookup"><span data-stu-id="2e43f-120">Otherwise, the reply is lost.</span></span>

<span data-ttu-id="2e43f-121">Если отправить этот пакет перед отправкой всех фрагментов, файл отправки будет удален; невозможно передать частичный файл.</span><span class="sxs-lookup"><span data-stu-id="2e43f-121">If you send this packet before uploading all fragments, the upload file is deleted; you cannot upload a partial file.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e43f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e43f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e43f-123">**Подтверждение для закрытия сеанса**</span><span class="sxs-lookup"><span data-stu-id="2e43f-123">**Ack for Close-Session**</span></span>](ack-for-close-session.md)
</dt> <dt>

[<span data-ttu-id="2e43f-124">**Отмена — сеанс**</span><span class="sxs-lookup"><span data-stu-id="2e43f-124">**Cancel-Session**</span></span>](cancel-session.md)
</dt> <dt>

[<span data-ttu-id="2e43f-125">**Создание сеанса**</span><span class="sxs-lookup"><span data-stu-id="2e43f-125">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




