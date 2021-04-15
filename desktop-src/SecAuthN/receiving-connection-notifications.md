---
description: Некоторые приложения должны принимать уведомления о событиях соединения, перед событием, сразу после его возникновения или в обоих случаях. Вы можете создать библиотеку DLL для получения уведомлений о событиях соединения, а не на самом деле.
ms.assetid: 692eb8f2-1c53-4535-b44d-babb30eecd9c
title: Получение уведомлений о подключении
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c054d4f7bb78f610afe6c1cbdf028416de7b5596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539858"
---
# <a name="receiving-connection-notifications"></a><span data-ttu-id="1ba91-104">Получение уведомлений о подключении</span><span class="sxs-lookup"><span data-stu-id="1ba91-104">Receiving Connection Notifications</span></span>

<span data-ttu-id="1ba91-105">Некоторые приложения должны принимать уведомления о событиях соединения, перед событием, сразу после его возникновения или в обоих случаях.</span><span class="sxs-lookup"><span data-stu-id="1ba91-105">Some applications need to receive notification of connection events, either before the event, just after it occurs, or both.</span></span> <span data-ttu-id="1ba91-106">Вы можете создать библиотеку DLL для получения уведомлений о событиях соединения, а не на самом деле.</span><span class="sxs-lookup"><span data-stu-id="1ba91-106">You can create a DLL to receive advance and after-the-fact notification of connection events.</span></span>

<span data-ttu-id="1ba91-107">Примером приложения, которое должно получать предварительное уведомление о событии подключения, является служба удаленного доступа (RAS).</span><span class="sxs-lookup"><span data-stu-id="1ba91-107">An example of an application that needs to receive advance notification of a connection event is the Remote Access Service (RAS).</span></span> <span data-ttu-id="1ba91-108">Служба RAS должна быть уведомлена перед подключением, поскольку перед подключением к сети может потребоваться установить модемное подключение.</span><span class="sxs-lookup"><span data-stu-id="1ba91-108">RAS needs to be informed before a connection is made because it may be necessary to establish a modem connection before making the network connection.</span></span>

<span data-ttu-id="1ba91-109">Аналогичным образом, приложениям может потребоваться очистка ресурсов после подключения, поэтому требуется уведомление после подключения.</span><span class="sxs-lookup"><span data-stu-id="1ba91-109">Similarly, applications may need to clean up resources after the connection is made, therefore requiring a post-connection notification.</span></span>

<span data-ttu-id="1ba91-110">Приложения, заинтересованные в получении аванса и уведомления о событиях соединения по факту, должны предоставить библиотеку DLL, которая экспортирует две функции, [**аддконнектнотифи**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) и [**канцелконнектнотифи**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify).</span><span class="sxs-lookup"><span data-stu-id="1ba91-110">Applications interested in receiving advance and after-the-fact notification of connection events must supply a DLL that exports two functions, [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) and [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify).</span></span>

<span data-ttu-id="1ba91-111">После реализации этих функций необходимо зарегистрировать библиотеку DLL, как описано в статье [Регистрация для получения уведомлений о подключениях](registering-to-receive-connection-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="1ba91-111">After you implement these functions, you must register your DLL as described in [Registering to Receive Connection Notifications](registering-to-receive-connection-notifications.md).</span></span>

 

 



