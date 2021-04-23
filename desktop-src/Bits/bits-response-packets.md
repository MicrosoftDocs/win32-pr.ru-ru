---
title: Пакеты ответов BITS
description: Пакеты ответов BITS
ms.assetid: 30755476-daa9-42ea-8fb3-5b505fc9dd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755e28b749d201a2c90640ea9e456f012f790453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887720"
---
# <a name="bits-response-packets"></a><span data-ttu-id="936fa-103">Пакеты ответов BITS</span><span class="sxs-lookup"><span data-stu-id="936fa-103">BITS Response Packets</span></span>

<span data-ttu-id="936fa-104">В следующей таблице перечислены пакеты ответа, отправляемые клиенту BITS для заданий отправки и отправки и ответа.</span><span class="sxs-lookup"><span data-stu-id="936fa-104">The following table lists the response packets sent to the BITS client for upload and upload-reply jobs.</span></span> <span data-ttu-id="936fa-105">В таблице перечислены пакеты в типичной последовательности, которые они отправляют клиенту.</span><span class="sxs-lookup"><span data-stu-id="936fa-105">The table lists the packets in the typical sequence they are sent to the client.</span></span>



| <span data-ttu-id="936fa-106">Пакет ответа</span><span class="sxs-lookup"><span data-stu-id="936fa-106">Response packet</span></span>                                      | <span data-ttu-id="936fa-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="936fa-107">Purpose</span></span>                                                                                                                                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="936fa-108">Подтверждение проверки связи</span><span class="sxs-lookup"><span data-stu-id="936fa-108">Ack for Ping</span></span>](ack-for-ping.md)                     | <span data-ttu-id="936fa-109">Подтверждает запрос [проверки связи](ping.md) .</span><span class="sxs-lookup"><span data-stu-id="936fa-109">Acknowledges the [Ping](ping.md) request.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="936fa-110">Подтверждение для создания сеанса</span><span class="sxs-lookup"><span data-stu-id="936fa-110">Ack for Create-Session</span></span>](ack-for-create-session.md) | <span data-ttu-id="936fa-111">Подтверждает запрос на [Создание сеанса](create-session.md) и возвращает идентификатор сеанса, используемый клиентом BITS во всех последующих запросах для идентификации этого сеанса передачи файлов.</span><span class="sxs-lookup"><span data-stu-id="936fa-111">Acknowledges the [Create-Session](create-session.md) request and returns a session identifier that the BITS client uses on all subsequent requests to identify this file transfer session.</span></span> |
| [<span data-ttu-id="936fa-112">Подтверждение для фрагмента</span><span class="sxs-lookup"><span data-stu-id="936fa-112">Ack for Fragment</span></span>](ack-for-fragment.md)             | <span data-ttu-id="936fa-113">Подтверждает запрос [фрагмента](fragment.md) и записывает фрагмент в файл передачи на сервере.</span><span class="sxs-lookup"><span data-stu-id="936fa-113">Acknowledges the [Fragment](fragment.md) request and writes the fragment to the upload file on the server.</span></span>                                                                                 |
| [<span data-ttu-id="936fa-114">Подтверждение для закрытия сеанса</span><span class="sxs-lookup"><span data-stu-id="936fa-114">Ack for Close-Session</span></span>](ack-for-close-session.md)   | <span data-ttu-id="936fa-115">Подтверждает запрос на [закрытие сеанса](close-session.md) и освобождает все ресурсы, связанные с этим сеансом.</span><span class="sxs-lookup"><span data-stu-id="936fa-115">Acknowledges the [Close-Session](close-session.md) request and releases all resources associated with the session.</span></span>                                                                         |
| [<span data-ttu-id="936fa-116">Подтверждение для отмены сеанса</span><span class="sxs-lookup"><span data-stu-id="936fa-116">Ack for Cancel-Session</span></span>](ack-for-cancel-session.md) | <span data-ttu-id="936fa-117">Подтверждает запрос на [отмену сеанса](cancel-session.md) и освобождает все ресурсы, связанные с этим сеансом.</span><span class="sxs-lookup"><span data-stu-id="936fa-117">Acknowledges the [Cancel-Session](cancel-session.md) request and releases all resources associated with the session.</span></span>                                                                       |



 

 

 




