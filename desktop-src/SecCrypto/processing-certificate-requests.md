---
description: Объясняет, как службы сертификации обрабатывают запросы на сертификаты.
ms.assetid: 40641167-12de-4008-80e4-2fb758146421
title: Обработка запросов сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70a25d9ca633247c3995677825dc011b2b38d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104559147"
---
# <a name="processing-certificate-requests"></a><span data-ttu-id="d81da-103">Обработка запросов сертификатов</span><span class="sxs-lookup"><span data-stu-id="d81da-103">Processing Certificate Requests</span></span>

<span data-ttu-id="d81da-104">При обработке [*запроса на сертификат*](../secgloss/c-gly.md)службы сертификации выполняют следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d81da-104">Certificate Services performs the following steps when processing a [*certificate request*](../secgloss/c-gly.md):</span></span>

1.  <span data-ttu-id="d81da-105">Получение запроса.</span><span class="sxs-lookup"><span data-stu-id="d81da-105">Request reception.</span></span>

    <span data-ttu-id="d81da-106">Клиент отправляет [*запрос на сертификат*](../secgloss/c-gly.md) в промежуточное приложение, которое преобразует его в \# запрос формата PKCS 10 и отправляет его в ядро сервера.</span><span class="sxs-lookup"><span data-stu-id="d81da-106">The [*certificate request*](../secgloss/c-gly.md) is sent by the client to an intermediary application, which formats it into a PKCS \#10 format request and submits it to the server engine.</span></span>

2.  <span data-ttu-id="d81da-107">Запрос утверждения.</span><span class="sxs-lookup"><span data-stu-id="d81da-107">Request approval.</span></span>

    <span data-ttu-id="d81da-108">Подсистема сервера вызывает [модуль политики](policy-modules.md), который запрашивает свойства запроса, определяет, является ли запрос полномочным, и устанавливает дополнительные свойства сертификата.</span><span class="sxs-lookup"><span data-stu-id="d81da-108">The server engine calls the [Policy Module](policy-modules.md), which queries request properties, decides whether the request is authorized or not, and sets optional certificate properties.</span></span>

3.  <span data-ttu-id="d81da-109">Формирования сертификата.</span><span class="sxs-lookup"><span data-stu-id="d81da-109">Certificate formation.</span></span>

    <span data-ttu-id="d81da-110">Если запрос утвержден, подсистема сервера принимает запрос и все свойства, запрошенные модулем политики, и создает полный сертификат.</span><span class="sxs-lookup"><span data-stu-id="d81da-110">If the request is approved, the server engine takes the request, and any properties requested by the Policy Module, and builds a complete certificate.</span></span>

4.  <span data-ttu-id="d81da-111">Публикация сертификата.</span><span class="sxs-lookup"><span data-stu-id="d81da-111">Certificate publication.</span></span>

    <span data-ttu-id="d81da-112">Ядро сервера сохраняет завершенный сертификат в базе данных служб сертификации и уведомляет промежуточное приложение о состоянии запроса.</span><span class="sxs-lookup"><span data-stu-id="d81da-112">The server engine stores the completed certificate in the Certificate Services database and notifies the intermediary application of the request status.</span></span> <span data-ttu-id="d81da-113">Если [модуль выхода](exit-modules.md) запрашивается, то ядро сервера сообщит о событии выдачи сертификата.</span><span class="sxs-lookup"><span data-stu-id="d81da-113">If the [exit module](exit-modules.md) has so requested, the server engine will notify it of a certificate issuance event.</span></span> <span data-ttu-id="d81da-114">Это позволяет модулю выхода выполнять дальнейшие операции, такие как публикация сертификата во внешнем репозитории сертификатов (например, Служба каталогов).</span><span class="sxs-lookup"><span data-stu-id="d81da-114">This allows the exit module to perform further operations such as publishing the certificate to an external certificate repository (for example, a directory service).</span></span> <span data-ttu-id="d81da-115">В то же время посредник получает опубликованный сертификат от служб сертификации и передает его обратно клиенту.</span><span class="sxs-lookup"><span data-stu-id="d81da-115">Meanwhile, the intermediary gets the published certificate from Certificate Services and passes it back to the client.</span></span>

<span data-ttu-id="d81da-116">На следующем рисунке показано, как [*запрос сертификата*](../secgloss/c-gly.md) обрабатывается службами сертификации.</span><span class="sxs-lookup"><span data-stu-id="d81da-116">The following illustration shows how a [*certificate request*](../secgloss/c-gly.md) is processed by Certificate Services.</span></span>

![Обработка запроса на сертификат](images/certflow.png)

 

 
