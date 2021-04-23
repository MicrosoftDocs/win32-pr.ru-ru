---
description: Функция Декриптмессаже (общая) перехватывает запросы на повторное согласование, поступающие от отправителя сообщения. Он уведомляет ваше приложение, расшифровывать данные сообщения и возвращая \_ значение повторного \_ согласования в секунду.
ms.assetid: 036a93dc-7f52-42f8-945d-7f654289ef63
title: Распознавание запроса на повторное согласование соединения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8ae8083c59485b8b7c917fe03893fa363f5a8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080750"
---
# <a name="recognizing-a-request-to-renegotiate-a-connection"></a><span data-ttu-id="e85c1-104">Распознавание запроса на повторное согласование соединения</span><span class="sxs-lookup"><span data-stu-id="e85c1-104">Recognizing a Request to Renegotiate a Connection</span></span>

<span data-ttu-id="e85c1-105">Функция [**декриптмессаже (общая)**](decryptmessage--general.md) перехватывает запросы на повторное согласование, поступающие от отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="e85c1-105">The [**DecryptMessage (General)**](decryptmessage--general.md) function traps requests for renegotiation coming from the message sender.</span></span> <span data-ttu-id="e85c1-106">Он уведомляет ваше приложение, расшифровывать данные сообщения и возвращая \_ значение повторного \_ согласования в секунду.</span><span class="sxs-lookup"><span data-stu-id="e85c1-106">It notifies your application by decrypting the message data and returning the SEC\_I\_RENEGOTIATE value.</span></span>

<span data-ttu-id="e85c1-107">Приложение должно выполнять такие запросы, вызывая [**AcceptSecurityContext (Общие)**](acceptsecuritycontext--general.md) (серверы) или [**InitializeSecurityContext (Общие)**](initializesecuritycontext--general.md) (клиенты) и передавая содержимое SECBUFFER_EXTRA, возвращенное из декриптмессаже в SECBUFFER_TOKEN.</span><span class="sxs-lookup"><span data-stu-id="e85c1-107">Your application must handle such requests by calling [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) (servers) or [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) (clients) and passing the contents of SECBUFFER_EXTRA returned from DecryptMessage in the SECBUFFER_TOKEN.</span></span> <span data-ttu-id="e85c1-108">После того как этот начальный вызов вернет значение, продолжайте, как будто приложение создает новое соединение.</span><span class="sxs-lookup"><span data-stu-id="e85c1-108">After this initial call returns a value, proceed as though your application were creating a new connection.</span></span>

 

 



