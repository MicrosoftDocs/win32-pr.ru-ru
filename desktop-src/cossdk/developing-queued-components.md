---
description: Разработка компонентов в очереди
ms.assetid: 867b7512-82ad-4877-8675-aa2d7e62ff8a
title: Разработка компонентов в очереди
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8808ef3e6cba8ff561dd94473fca8f00631081f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807181"
---
# <a name="developing-queued-components"></a><span data-ttu-id="5ec1f-103">Разработка компонентов в очереди</span><span class="sxs-lookup"><span data-stu-id="5ec1f-103">Developing Queued Components</span></span>

<span data-ttu-id="5ec1f-104">Служба COM+ очереди компонентов требует, чтобы все методы приложения содержали \[ только \] Параметры in без возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="5ec1f-104">The COM+ queued components service requires all application methods to contain only \[in\] parameters, with no return values.</span></span> <span data-ttu-id="5ec1f-105">Поскольку объект сервера необязательно доступен, когда клиент выполняет вызов, результаты сервера можно вернуть, отправив сообщение, которое создает другой объект.</span><span class="sxs-lookup"><span data-stu-id="5ec1f-105">Because the server object is not necessarily available when the client makes the call, server results can be returned by sending a message that creates another object.</span></span> <span data-ttu-id="5ec1f-106">Таким образом, двустороннее взаимодействие происходит не в каждом случае, а только тогда, когда это необходимо, с помощью ряда односторонних сообщений между объектами.</span><span class="sxs-lookup"><span data-stu-id="5ec1f-106">In this way, two-way communication occurs not in every case but only when it is required, by a series of one-way messages between objects.</span></span>

<span data-ttu-id="5ec1f-107">Чтобы использовать службу очередей компонентов COM+, необходимо, чтобы служба [очередей сообщений](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) уже была установлена.</span><span class="sxs-lookup"><span data-stu-id="5ec1f-107">To use the COM+ queued components service, you must have the [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) service already installed.</span></span> <span data-ttu-id="5ec1f-108">Служба очередей сообщений не устанавливается автоматически.</span><span class="sxs-lookup"><span data-stu-id="5ec1f-108">Message Queuing is not installed automatically.</span></span> <span data-ttu-id="5ec1f-109">Служба очереди сообщений должна быть выбрана во время установки операционной системы или с помощью компонента " **Установка и удаление программ**".</span><span class="sxs-lookup"><span data-stu-id="5ec1f-109">Message Queuing must be selected during the operating system setup or by using **Add/Remove programs**.</span></span> <span data-ttu-id="5ec1f-110">Внутренний сертификат службы очереди сообщений создается автоматически при входе в систему.</span><span class="sxs-lookup"><span data-stu-id="5ec1f-110">An internal Message Queuing certificate is created automatically at logon.</span></span>

<span data-ttu-id="5ec1f-111">В разделах, приведенных в следующей таблице, приведены дополнительные рекомендации для более специализированных ситуаций.</span><span class="sxs-lookup"><span data-stu-id="5ec1f-111">The topics described in the following table provide additional considerations for more specialized situations.</span></span>



| <span data-ttu-id="5ec1f-112">Раздел</span><span class="sxs-lookup"><span data-stu-id="5ec1f-112">Topic</span></span>                                                                                           | <span data-ttu-id="5ec1f-113">Описание</span><span class="sxs-lookup"><span data-stu-id="5ec1f-113">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec1f-114">[Передача объектов в качестве параметров](passing-objects-as-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="5ec1f-114">[Passing Objects as Parameter](passing-objects-as-parameters.md)s</span></span><br/>                   | <span data-ttu-id="5ec1f-115">Описывает передачу объектов \[ в качестве параметров в \] очереди компонентов.</span><span class="sxs-lookup"><span data-stu-id="5ec1f-115">Describes how to pass objects as \[in\] parameters to queued components.</span></span><br/>                    |
| [<span data-ttu-id="5ec1f-116">Ограничения безопасности в режиме рабочей группы</span><span class="sxs-lookup"><span data-stu-id="5ec1f-116">Security Limitations in Workgroup Mode</span></span>](security-limitations-in-workgroup-mode.md)<br/> | <span data-ttu-id="5ec1f-117">Описывает ограничения использования проверки подлинности очереди сообщений в режиме рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="5ec1f-117">Describes limitations on the use of Message Queuing authentication in workgroup mode.</span></span><br/>       |
| [<span data-ttu-id="5ec1f-118">Особенности работы с потоками</span><span class="sxs-lookup"><span data-stu-id="5ec1f-118">Threading Considerations</span></span>](threading-considerations.md)<br/>                             | <span data-ttu-id="5ec1f-119">Описывает конкретные проблемы, связанные с передачей указателей интерфейса записи между потоками.</span><span class="sxs-lookup"><span data-stu-id="5ec1f-119">Describes specific concerns related to passing recorder interface pointers between threads.</span></span><br/> |
| [<span data-ttu-id="5ec1f-120">Получение ответа</span><span class="sxs-lookup"><span data-stu-id="5ec1f-120">Receiving a Response</span></span>](receiving-a-response.md)<br/>                                     | <span data-ttu-id="5ec1f-121">Описывает, как создать ответ на вызов компонента в очереди.</span><span class="sxs-lookup"><span data-stu-id="5ec1f-121">Describes how to construct a response to a queued component call.</span></span><br/>                           |



 

 

 




