---
title: Функции обратного вызова состояния
description: Функции обратного вызова состояния
ms.assetid: fe89fb97-0b56-4956-a1a6-f4ad2d06befa
keywords:
- Функции обратного вызова Авикап, состояние
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b4b4bf4cad5f689f1e146986f9d1b55b00f1aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410950"
---
# <a name="status-callback-functions"></a><span data-ttu-id="16c27-104">Функции обратного вызова состояния</span><span class="sxs-lookup"><span data-stu-id="16c27-104">Status Callback Functions</span></span>

<span data-ttu-id="16c27-105">Окно отслеживания может отправлять сообщения функции обратного вызова состояния при записи видео на диск или во время других длительных операций для уведомления приложения о ходе выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="16c27-105">A capture window can send messages to the status callback function while capturing video to disk or during other lengthy operations to notify your application of the progress of an operation.</span></span> <span data-ttu-id="16c27-106">Сведения о состоянии включают идентификатор сообщения и форматированную текстовую строку, готовую для просмотра.</span><span class="sxs-lookup"><span data-stu-id="16c27-106">The status information includes a message identifier and a formatted text string ready for display.</span></span> <span data-ttu-id="16c27-107">Приложение может использовать идентификатор сообщения для фильтрации уведомлений и ограничения сообщений, которые должны быть представлены пользователю.</span><span class="sxs-lookup"><span data-stu-id="16c27-107">Your application can use the message identifier to filter the notifications and limit the messages to present to the user.</span></span> <span data-ttu-id="16c27-108">Во время операций записи первое сообщение, отправленное в функцию обратного вызова, всегда начинается с конца идентификатора \_ \_ , а последняя всегда имеет \_ \_ конечную буквицу.</span><span class="sxs-lookup"><span data-stu-id="16c27-108">During capture operations, the first message sent to the callback function is always IDS\_CAP\_BEGIN and the last is always IDS\_CAP\_END.</span></span> <span data-ttu-id="16c27-109">Нулевой идентификатор сообщения означает, что новая операция запускается, а функция обратного вызова должна очистить текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="16c27-109">A message identifier of zero indicates a new operation is starting and the callback function should clear the current status.</span></span>

 

 




