---
description: Посторонние сообщения шифруют данные для передачи и расшифровки полученных данных. Низкоуровневые функции сообщений также расшифровываются и проверяют подписи полученных сообщений.
ms.assetid: 42c19920-c7f7-4a4d-9de3-3de9a34fbe0c
title: Низкоуровневые функции сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22654f19dfe5178dfb98006c17c2d0536f78cd46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810247"
---
# <a name="low-level-message-functions"></a><span data-ttu-id="937ac-104">Низкоуровневые функции сообщений</span><span class="sxs-lookup"><span data-stu-id="937ac-104">Low-level Message Functions</span></span>

<span data-ttu-id="937ac-105">[*Посторонние сообщения*](../secgloss/l-gly.md) шифруют данные для передачи и расшифровки полученных данных.</span><span class="sxs-lookup"><span data-stu-id="937ac-105">The [*low-level message functions*](../secgloss/l-gly.md) encode data for transmission and decode data that has been received.</span></span> <span data-ttu-id="937ac-106">Низкоуровневые функции сообщений также расшифровываются и проверяют подписи полученных сообщений.</span><span class="sxs-lookup"><span data-stu-id="937ac-106">Low-level message functions also decrypt and verify the signatures of received messages.</span></span>

<span data-ttu-id="937ac-107">Когда сообщение открывается с помощью функции открытого сообщения низкого уровня, оно остается открытым и доступным (сохраняет свое [*состояние*](../secgloss/s-gly.md)) до тех пор, пока оно не будет закрыто.</span><span class="sxs-lookup"><span data-stu-id="937ac-107">When a message is opened using a low-level message open function, it remains open and available (maintains its [*state*](../secgloss/s-gly.md)) until it is closed.</span></span> <span data-ttu-id="937ac-108">Это позволяет формировать поэтапное сообщение с помощью нескольких вызовов функции [**криптмсгупдате**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) .</span><span class="sxs-lookup"><span data-stu-id="937ac-108">This allows a message to be constructed piecemeal using multiple calls to the [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) function.</span></span>

<span data-ttu-id="937ac-109">Использование функций сообщений низкого уровня требует больше вызовов функций, чем использование упрощенных функций сообщений (см. раздел [упрощенные сообщения](simplified-messages.md)).</span><span class="sxs-lookup"><span data-stu-id="937ac-109">Using low-level message functions requires more function calls than using simplified message functions (see [Simplified Messages](simplified-messages.md)).</span></span> <span data-ttu-id="937ac-110">Если используются упрощенные функции сообщений, большую часть работы можно выполнить в функциях API.</span><span class="sxs-lookup"><span data-stu-id="937ac-110">If the simplified message functions are used, more of the work is done inside the functions of the API.</span></span>

<span data-ttu-id="937ac-111">Использование низкоуровневых функций сообщений требует дополнительной работы по выполнению вызовов других сертификатов или криптографических функций.</span><span class="sxs-lookup"><span data-stu-id="937ac-111">Using low-level message functions involves the additional work of making calls to other certificate or cryptographic functions.</span></span> <span data-ttu-id="937ac-112">Например, для инициализации структур, используемых этими функциями сообщений низкого уровня, могут потребоваться данные из вызовов функций сертификатов.</span><span class="sxs-lookup"><span data-stu-id="937ac-112">For example, data from calls to certificate functions may be needed to initialize structures used by these low-level message functions.</span></span> <span data-ttu-id="937ac-113">Упрощенные функции сообщений инициализируют многие из этих структур внутренним образом.</span><span class="sxs-lookup"><span data-stu-id="937ac-113">Simplified message functions initialize many of these structures internally.</span></span>

<span data-ttu-id="937ac-114">В следующей таблице перечислены разделы с описаниями процедур и примеры кода на C, посвященные функциям обработки сообщений низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="937ac-114">The following table lists sections with procedure descriptions and C code examples of using the low-level message functions.</span></span>



| <span data-ttu-id="937ac-115">Section</span><span class="sxs-lookup"><span data-stu-id="937ac-115">Section</span></span>                                                                               | <span data-ttu-id="937ac-116">Содержимое</span><span class="sxs-lookup"><span data-stu-id="937ac-116">Contents</span></span>                                           |
|---------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="937ac-117">Низкоуровневые функции сообщений</span><span class="sxs-lookup"><span data-stu-id="937ac-117">Low-level Message Functions</span></span>](cryptography-functions.md) | <span data-ttu-id="937ac-118">Содержит список функций сообщений низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="937ac-118">Lists the low-level message functions.</span></span>             |
| [<span data-ttu-id="937ac-119">Подписывание данных</span><span class="sxs-lookup"><span data-stu-id="937ac-119">Signing Data</span></span>](signing-data.md)                                                      | <span data-ttu-id="937ac-120">Сведения о задачах, необходимых для подписания данных.</span><span class="sxs-lookup"><span data-stu-id="937ac-120">Details the tasks needed to sign data.</span></span>             |
| [<span data-ttu-id="937ac-121">Кодирование запечатанных данных</span><span class="sxs-lookup"><span data-stu-id="937ac-121">Encoding Enveloped Data</span></span>](encoding-enveloped-data.md)                                | <span data-ttu-id="937ac-122">Сведения о задачах, необходимых для кодирования упакованных данных.</span><span class="sxs-lookup"><span data-stu-id="937ac-122">Details the tasks needed to encode enveloped data.</span></span> |
| [<span data-ttu-id="937ac-123">Декодирование упакованных данных</span><span class="sxs-lookup"><span data-stu-id="937ac-123">Decoding Enveloped Data</span></span>](decoding-enveloped-data.md)                                | <span data-ttu-id="937ac-124">Сведения о задачах, необходимых для декодирования упакованных данных.</span><span class="sxs-lookup"><span data-stu-id="937ac-124">Details the tasks needed to decode enveloped data.</span></span> |



 

 

 
