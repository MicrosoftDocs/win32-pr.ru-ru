---
description: Иногда подписанное сообщение требует другой подписи.
ms.assetid: de83a9ad-4e88-4477-8c9e-6dd7d5ec9e8f
title: Подписи в сообщениях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8dff2920217dd9a79f917f7b625da3919747d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810246"
---
# <a name="message-countersignatures"></a><span data-ttu-id="3e25e-103">Подписи в сообщениях</span><span class="sxs-lookup"><span data-stu-id="3e25e-103">Message Countersignatures</span></span>

<span data-ttu-id="3e25e-104">Иногда подписанное сообщение требует [*другой подписи*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3e25e-104">Sometimes a signed message requires a [*countersignature*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="3e25e-105">Например, пользователь A может отправить сообщение со знакомыми данными пользователю б, ожидая B для подтверждения соглашения с условиями, содержащимися в документе.</span><span class="sxs-lookup"><span data-stu-id="3e25e-105">For example, user A may send a signed-data message to user B, expecting B to confirm agreement with the terms contained in the document.</span></span> <span data-ttu-id="3e25e-106">Пользователь б декодирует сообщение, считывает термины и, если в соглашении, каунтерсигнс сообщение.</span><span class="sxs-lookup"><span data-stu-id="3e25e-106">User B decodes the message, reads the terms and, if in agreement, countersigns the message.</span></span> <span data-ttu-id="3e25e-107">Затем сообщение скрепляющая подпись отправляется обратно пользователю A. пользователь A теперь знает и может доказать, что пользователь б согласен с условиями.</span><span class="sxs-lookup"><span data-stu-id="3e25e-107">The countersigned message is then sent back to user A. User A now knows, and can prove, that user B agreed to the terms.</span></span>

<span data-ttu-id="3e25e-108">В следующей таблице перечислены разделы, в которых содержатся описания процедур или примеры скрепляющая подпись сообщений.</span><span class="sxs-lookup"><span data-stu-id="3e25e-108">The following table lists sections that contain procedure descriptions or C program examples of message countersigning.</span></span>



| <span data-ttu-id="3e25e-109">Section</span><span class="sxs-lookup"><span data-stu-id="3e25e-109">Section</span></span>                                                                                                                                 | <span data-ttu-id="3e25e-110">Содержимое</span><span class="sxs-lookup"><span data-stu-id="3e25e-110">Contents</span></span>                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="3e25e-111">Функции сообщений</span><span class="sxs-lookup"><span data-stu-id="3e25e-111">Message Functions</span></span>](cryptography-functions.md)                                                                       | <span data-ttu-id="3e25e-112">Выводит список функций подписи счетчика.</span><span class="sxs-lookup"><span data-stu-id="3e25e-112">Lists the counter signature functions.</span></span>                             |
| [<span data-ttu-id="3e25e-113">Скрепляющая подпись сообщение</span><span class="sxs-lookup"><span data-stu-id="3e25e-113">Countersigning a Message</span></span>](countersigning-a-message.md)                                                                                | <span data-ttu-id="3e25e-114">Подробное описание процесса подписывания счетчика сообщения.</span><span class="sxs-lookup"><span data-stu-id="3e25e-114">Details the process of counter signing a message.</span></span>                  |
| [<span data-ttu-id="3e25e-115">Проверка подписи другой стороны</span><span class="sxs-lookup"><span data-stu-id="3e25e-115">Verifying a Countersignature</span></span>](verifying-a-countersignature.md)                                                                        | <span data-ttu-id="3e25e-116">Подробно описывается процедура проверки подписи счетчика.</span><span class="sxs-lookup"><span data-stu-id="3e25e-116">Details the procedure for verifying a counter signature.</span></span>           |
| [<span data-ttu-id="3e25e-117">Проверка подписанного сообщения</span><span class="sxs-lookup"><span data-stu-id="3e25e-117">Verifying a Signed Message</span></span>](verifying-a-signed-message.md)                                                                            | <span data-ttu-id="3e25e-118">Подробное описание процесса проверки подписи подписанного сообщения.</span><span class="sxs-lookup"><span data-stu-id="3e25e-118">Details a process for verifying the signature on a signed message.</span></span> |
| [<span data-ttu-id="3e25e-119">Пример программы на языке C: кодирование и декодирование сообщения скрепляющая подпись</span><span class="sxs-lookup"><span data-stu-id="3e25e-119">Example C Program: Encoding and Decoding a CounterSigned Message</span></span>](example-c-program-encoding-and-decoding-a-countersigned-message.md) | <span data-ttu-id="3e25e-120">Образец программы на языке C, который кодирует и декодирует сообщение скрепляющая подпись.</span><span class="sxs-lookup"><span data-stu-id="3e25e-120">Sample C program that encodes and decodes a countersigned message.</span></span> |



 

 

 
