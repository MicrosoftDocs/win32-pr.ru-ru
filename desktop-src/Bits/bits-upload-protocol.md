---
title: Протокол передачи BITS
description: В этом разделе описывается сетевой протокол для типов заданий отправки и отправки и ответа BITS.
ms.assetid: d0706ab1-1bf4-4b17-9321-ec3e00dd25e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642426decd0bc37390fa9fdd9b1ad2be11a0aa84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773679"
---
# <a name="bits-upload-protocol"></a><span data-ttu-id="b5fda-103">Протокол передачи BITS</span><span class="sxs-lookup"><span data-stu-id="b5fda-103">BITS Upload Protocol</span></span>

<span data-ttu-id="b5fda-104">В этом разделе описывается сетевой протокол для типов заданий отправки и отправки и ответа BITS.</span><span class="sxs-lookup"><span data-stu-id="b5fda-104">This section describes the network protocol for BITS upload and upload-reply job types.</span></span> <span data-ttu-id="b5fda-105">Протокол передачи BITS поверх HTTP 1,1 и использует многие из существующих заголовков HTTP и определяет новые заголовки.</span><span class="sxs-lookup"><span data-stu-id="b5fda-105">The BITS upload protocol is layered on top of HTTP 1.1 and uses many of the existing HTTP headers and defines new headers.</span></span> <span data-ttu-id="b5fda-106">Протокол передачи BITS поддерживает один файл передачи для каждого сеанса.</span><span class="sxs-lookup"><span data-stu-id="b5fda-106">The BITS upload protocol supports a single upload file per session.</span></span>

<span data-ttu-id="b5fda-107">BITS использует пакеты для описания клиентских запросов и ответов сервера.</span><span class="sxs-lookup"><span data-stu-id="b5fda-107">BITS uses packets to describe client requests and server responses.</span></span> <span data-ttu-id="b5fda-108">В заголовке BITS-Packet-Type указывается тип отправляемого пакета.</span><span class="sxs-lookup"><span data-stu-id="b5fda-108">The BITS-Packet-Type header specifies the type of packet being sent.</span></span> <span data-ttu-id="b5fda-109">Каждый пакет содержит определенные заголовки.</span><span class="sxs-lookup"><span data-stu-id="b5fda-109">Each packet contains specific headers.</span></span> <span data-ttu-id="b5fda-110">Служба BITS использует \_ команду BITS POST для обнаружения пакетов загрузки BITS.</span><span class="sxs-lookup"><span data-stu-id="b5fda-110">BITS uses the BITS\_POST verb to identify BITS upload packets.</span></span> <span data-ttu-id="b5fda-111">Пакеты ответов всегда используют тип пакетов ACK, который означает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b5fda-111">Response packets always use the Ack packet type which stands for acknowledge.</span></span> <span data-ttu-id="b5fda-112">Пакет ACK отправляется в контексте предыдущего запроса. в один момент времени может быть только один необработанный запрос.</span><span class="sxs-lookup"><span data-stu-id="b5fda-112">The Ack packet is sent in the context of the previous request; there can be only one outstanding request at one time.</span></span>

<span data-ttu-id="b5fda-113">Для заданий отправки и ответа служба BITS использует этот протокол для отправки файла, но не использует этот протокол для отправки ответа клиенту.</span><span class="sxs-lookup"><span data-stu-id="b5fda-113">For upload-reply jobs, BITS uses this protocol to upload the file but does not use this protocol to send the reply to the client.</span></span> <span data-ttu-id="b5fda-114">Вместо этого сервер BITS отправляет клиенту расположение файла ответов, а клиент создает задание скачивания BITS для скачивания файла ответов.</span><span class="sxs-lookup"><span data-stu-id="b5fda-114">Instead, the BITS server sends the location of the reply file to the client and the client creates a BITS download job to download the reply file.</span></span>

<span data-ttu-id="b5fda-115">Используйте протокол передачи, чтобы заменить клиент или серверное программное обеспечение BITS собственной реализацией.</span><span class="sxs-lookup"><span data-stu-id="b5fda-115">Use the upload protocol to replace the BITS client or server software with your own implementation.</span></span> <span data-ttu-id="b5fda-116">Список пакетов запросов, отправленных клиентом BITS, см. в разделе [BITS Request](bits-request-packets.md)Packets.</span><span class="sxs-lookup"><span data-stu-id="b5fda-116">For a list of request packets sent by the BITS client, see [BITS Request Packets](bits-request-packets.md).</span></span> <span data-ttu-id="b5fda-117">Список пакетов ответов, отправленных сервером BITS, см. в разделе [пакеты ответов BITS](bits-response-packets.md).</span><span class="sxs-lookup"><span data-stu-id="b5fda-117">For a list of response packets sent by the BITS server, see [BITS Response Packets](bits-response-packets.md).</span></span>

<span data-ttu-id="b5fda-118">Клиент определяет реакцию на ошибки или непредвиденные пакеты с сервера BITS.</span><span class="sxs-lookup"><span data-stu-id="b5fda-118">The client determines how it responds to errors or unexpected packets from the BITS server.</span></span> <span data-ttu-id="b5fda-119">Если сервер получает неподдерживаемый пакет, сервер должен отправить ответный пакет с кодом возврата 400 (недопустимый запрос).</span><span class="sxs-lookup"><span data-stu-id="b5fda-119">If the server receives a packet that it does not expect, the server should send an Ack packet with a 400 (Bad Request) return code.</span></span>

 

 




