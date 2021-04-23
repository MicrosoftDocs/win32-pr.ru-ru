---
title: Пакетов запросов BITS
description: Пакетов запросов BITS
ms.assetid: 4d8fd5f3-7621-438f-926f-38ece7a52f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6738f77477342f1329818ae7c2ffb5c010b074c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986225"
---
# <a name="bits-request-packets"></a><span data-ttu-id="d23b2-103">Пакетов запросов BITS</span><span class="sxs-lookup"><span data-stu-id="d23b2-103">BITS Request Packets</span></span>

<span data-ttu-id="d23b2-104">Пакеты запросов описывают запросы клиентов.</span><span class="sxs-lookup"><span data-stu-id="d23b2-104">Request packets describe client requests.</span></span> <span data-ttu-id="d23b2-105">В данный момент времени может быть только один необработанный запрос. перед отправкой другого запроса необходимо получить [Подтверждение](bits-response-packets.md) для текущего запроса от сервера.</span><span class="sxs-lookup"><span data-stu-id="d23b2-105">There can be only one outstanding request at any given time; you must receive an [Ack](bits-response-packets.md) for the current request from the server before sending another request.</span></span>

<span data-ttu-id="d23b2-106">В следующей таблице перечислены пакеты запроса, отправляемые на сервер BITS для заданий отправки и отправки и ответа.</span><span class="sxs-lookup"><span data-stu-id="d23b2-106">The following table lists the request packets sent to the BITS server for upload and upload-reply jobs.</span></span> <span data-ttu-id="d23b2-107">В таблице перечислены пакеты в типичной последовательности, которые они отправляют на сервер.</span><span class="sxs-lookup"><span data-stu-id="d23b2-107">The table lists the packets in the typical sequence they are sent to the server.</span></span>



| <span data-ttu-id="d23b2-108">Пакет запроса</span><span class="sxs-lookup"><span data-stu-id="d23b2-108">Request packet</span></span>                       | <span data-ttu-id="d23b2-109">Назначение</span><span class="sxs-lookup"><span data-stu-id="d23b2-109">Purpose</span></span>                                                                                                                                                        |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d23b2-110">Проверок</span><span class="sxs-lookup"><span data-stu-id="d23b2-110">Ping</span></span>](ping.md)                     | <span data-ttu-id="d23b2-111">Устанавливает соединение и согласовывает безопасность с сервером.</span><span class="sxs-lookup"><span data-stu-id="d23b2-111">Establishes a connection and negotiates security with the server.</span></span>                                                                                              |
| [<span data-ttu-id="d23b2-112">Создание сеанса</span><span class="sxs-lookup"><span data-stu-id="d23b2-112">Create-Session</span></span>](create-session.md) | <span data-ttu-id="d23b2-113">Запрашивает сеанс отправки с сервером BITS.</span><span class="sxs-lookup"><span data-stu-id="d23b2-113">Requests an upload session with the BITS server.</span></span>                                                                                                               |
| [<span data-ttu-id="d23b2-114">Fragment</span><span class="sxs-lookup"><span data-stu-id="d23b2-114">Fragment</span></span>](fragment.md)             | <span data-ttu-id="d23b2-115">Отправляет фрагмент файла на сервер BITS.</span><span class="sxs-lookup"><span data-stu-id="d23b2-115">Sends a fragment of the file to the BITS server.</span></span> <span data-ttu-id="d23b2-116">Число отправленных запросов фрагментов зависит от выбранного размера фрагмента и размера файла отправки.</span><span class="sxs-lookup"><span data-stu-id="d23b2-116">The number of fragment requests sent depends on the fragment size you choose and the size of the upload file.</span></span> |
| [<span data-ttu-id="d23b2-117">Закрыть — сеанс</span><span class="sxs-lookup"><span data-stu-id="d23b2-117">Close-Session</span></span>](close-session.md)   | <span data-ttu-id="d23b2-118">Завершает сеанс передачи файла с сервером BITS.</span><span class="sxs-lookup"><span data-stu-id="d23b2-118">Ends the file upload session with the BITS server.</span></span>                                                                                                             |
| [<span data-ttu-id="d23b2-119">Отмена — сеанс</span><span class="sxs-lookup"><span data-stu-id="d23b2-119">Cancel-Session</span></span>](cancel-session.md) | <span data-ttu-id="d23b2-120">Завершает сеанс передачи файла с сервером BITS.</span><span class="sxs-lookup"><span data-stu-id="d23b2-120">Ends the file upload session with the BITS server.</span></span> <span data-ttu-id="d23b2-121">Как правило, пакет Cancel-Session отправляется, если пользователь отменил задание.</span><span class="sxs-lookup"><span data-stu-id="d23b2-121">Typically, you send the Cancel-Session packet if the user canceled the job.</span></span>                                 |



 

<span data-ttu-id="d23b2-122">Пакет Ping является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d23b2-122">The Ping packet is optional.</span></span> <span data-ttu-id="d23b2-123">Вместо отправки ping-пакета можно использовать пакет Create-Session для установления соединения и согласования безопасности.</span><span class="sxs-lookup"><span data-stu-id="d23b2-123">Instead of sending a Ping packet, you can use the Create-Session packet to establish a connection and negotiate security.</span></span> <span data-ttu-id="d23b2-124">Однако для этой цели более эффективно использовать пакет Ping.</span><span class="sxs-lookup"><span data-stu-id="d23b2-124">However, it is more efficient to use the Ping packet for this purpose.</span></span>

 

 




