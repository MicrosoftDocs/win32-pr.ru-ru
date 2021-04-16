---
description: Сообщения используются для уведомления приложения о асинхронных событиях. Все эти сообщения отправляются в приложение через механизм уведомления о сообщениях, указанный приложением в Линеинитиализикс.
ms.assetid: d302819e-c522-470a-be5e-52625c9223a4
title: Сообщения TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58307a0230b76c6ad98c57f4590098f0dcf6b236
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684040"
---
# <a name="tapi-messages"></a><span data-ttu-id="27c0b-104">Сообщения TAPI</span><span class="sxs-lookup"><span data-stu-id="27c0b-104">TAPI Messages</span></span>

<span data-ttu-id="27c0b-105">Сообщения используются для уведомления приложения о асинхронных событиях.</span><span class="sxs-lookup"><span data-stu-id="27c0b-105">Messages are used to notify the application of asynchronous events.</span></span> <span data-ttu-id="27c0b-106">Все эти сообщения отправляются в приложение через механизм уведомления о сообщениях, указанный приложением в [**линеинитиализикс**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="27c0b-106">All of these messages are sent to the application through the message notification mechanism that the application specified in [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span></span>

<span data-ttu-id="27c0b-107">Сообщение всегда содержит маркер для соответствующего объекта (Телефон, строка или вызов), который приложение может использовать для определения типа сообщений.</span><span class="sxs-lookup"><span data-stu-id="27c0b-107">The message always contains a handle to the relevant object (phone, line, or call), which the application can use to determine the message type.</span></span>

<span data-ttu-id="27c0b-108">Некоторые сообщения используются для уведомления приложения об изменении состояния объекта.</span><span class="sxs-lookup"><span data-stu-id="27c0b-108">Certain messages are used to notify the application about a change in an object's status.</span></span> <span data-ttu-id="27c0b-109">Эти сообщения предоставляют обработчик объекта и дают указание, какой элемент состояния изменился.</span><span class="sxs-lookup"><span data-stu-id="27c0b-109">These messages provide the object handle and give an indication of which status item has changed.</span></span> <span data-ttu-id="27c0b-110">Приложение может вызвать соответствующую функцию "Get Status" объекта, чтобы получить полное состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="27c0b-110">The application can call the appropriate "get status" function of the object to obtain the object's full status.</span></span>

<span data-ttu-id="27c0b-111">При возникновении события сообщения могут быть отправлены в ноль, одно или несколько приложений.</span><span class="sxs-lookup"><span data-stu-id="27c0b-111">When an event occurs, messages can be sent to zero, one, or more applications.</span></span> <span data-ttu-id="27c0b-112">Целевые приложения для сообщения определяются с помощью ряда различных факторов, в том числе от значения сообщения, прав приложения на объект, независимо от того, инициировало ли приложение запрос, для которого это сообщение является прямым результатом, и маскирование сообщений, которое было задано приложением.</span><span class="sxs-lookup"><span data-stu-id="27c0b-112">The target applications for a message are determined by a number of different factors including the meaning of the message, the application's privilege to the object, whether or not the application initiated the request for which the message is a direct result, and the message masking that has been set by the application.</span></span> <span data-ttu-id="27c0b-113">Обратите внимание на следующие моменты, касающиеся сообщений:</span><span class="sxs-lookup"><span data-stu-id="27c0b-113">Note the following points about messages:</span></span>

-   <span data-ttu-id="27c0b-114">Асинхронные сообщения ответов отправляются только в приложение, которое является источником запроса и не могут быть замаскированы.</span><span class="sxs-lookup"><span data-stu-id="27c0b-114">Asynchronous reply messages are only sent to the application that originated the request and cannot be masked.</span></span>
-   <span data-ttu-id="27c0b-115">Сообщения, которые сообщают о завершении создания цифр или тонов или сбор цифр, отправляются только приложению, которое запросило создание цифры или тона.</span><span class="sxs-lookup"><span data-stu-id="27c0b-115">Messages that signal the completion of digit or tone generation or the gathering of digits are only sent to the application that requested the digit or tone generation.</span></span>
-   <span data-ttu-id="27c0b-116">Сообщения, указывающие на изменение состояния строки или адреса, отправляются во все приложения, которые открыли строку, пока сообщение было включено через [**линесетстатусмессажес**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span><span class="sxs-lookup"><span data-stu-id="27c0b-116">Messages that indicate line or address state changes are sent to all applications that have opened the line, so long as the message has been enabled through [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span>
-   <span data-ttu-id="27c0b-117">Сообщения, указывающие на состояние вызова и сведения о вызовах, отправляются всем приложениям, которые имеют маркер вызова.</span><span class="sxs-lookup"><span data-stu-id="27c0b-117">Messages that indicate call state and call information changes are sent to all applications that have a handle to the call.</span></span>
-   <span data-ttu-id="27c0b-118">Сообщения, которые сообщают об обнаружении цифры, обнаружении тона или обнаружении типа носителя, отправляются в приложения, которые запросили наблюдение за этим событием.</span><span class="sxs-lookup"><span data-stu-id="27c0b-118">Messages that signal a digit detection, tone detection, or media type detection are sent to the applications that requested monitoring of that event.</span></span>

<span data-ttu-id="27c0b-119">В этом разделе содержатся справочные сведения о следующих сообщениях TAPI:</span><span class="sxs-lookup"><span data-stu-id="27c0b-119">This section contains the reference information for the following TAPI messages:</span></span>

-   [<span data-ttu-id="27c0b-120">Телефонные сообщения с поддержкой телефонии</span><span class="sxs-lookup"><span data-stu-id="27c0b-120">Assisted Telephony Messages</span></span>](assisted-telephony-messages.md)
-   [<span data-ttu-id="27c0b-121">Сообщения центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="27c0b-121">Call Center Messages</span></span>](call-center-messages.md)
-   [<span data-ttu-id="27c0b-122">Отформатированные сообщения об ошибках</span><span class="sxs-lookup"><span data-stu-id="27c0b-122">Formatted Error Messages</span></span>](formatted-error-messages.md)
-   [<span data-ttu-id="27c0b-123">Сообщения устройства линии</span><span class="sxs-lookup"><span data-stu-id="27c0b-123">Line Device Messages</span></span>](line-device-messages.md)
-   [<span data-ttu-id="27c0b-124">Сообщения телефонного устройства</span><span class="sxs-lookup"><span data-stu-id="27c0b-124">Phone Device Messages</span></span>](phone-device-messages.md)

 

 



