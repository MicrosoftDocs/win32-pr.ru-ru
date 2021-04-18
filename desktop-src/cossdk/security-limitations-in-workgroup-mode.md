---
description: Ограничения безопасности в режиме рабочей группы
ms.assetid: 05c0aba7-b94b-49d4-a0fc-1ff0a23550b3
title: Ограничения безопасности в режиме рабочей группы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eabe38b8d05c49382ae6dd8337b883a6f4a8079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701203"
---
# <a name="security-limitations-in-workgroup-mode"></a><span data-ttu-id="3211d-103">Ограничения безопасности в режиме рабочей группы</span><span class="sxs-lookup"><span data-stu-id="3211d-103">Security Limitations in Workgroup Mode</span></span>

<span data-ttu-id="3211d-104">В конфигурации рабочей группы [очереди сообщений](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) не разрешается поддержка безопасности приложений в службе очередей компонентов COM+.</span><span class="sxs-lookup"><span data-stu-id="3211d-104">The [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) workgroup configuration does not permit the COM+ queued components service to support application security.</span></span> <span data-ttu-id="3211d-105">Если вы установили очередь сообщений с конфигурацией Рабочей группы, необходимо [Отключить параметры безопасности](specifying-the-authentication-protocol.md) для каждого из приложений, помещенных в очередь, которые доступны в этой конфигурации, выбрав параметр не **проверять подлинность сообщений** на вкладке **очередь** диалогового окна **Свойства** приложения COM+ с помощью средства администрирования "службы компонентов".</span><span class="sxs-lookup"><span data-stu-id="3211d-105">If you've installed Message Queuing with the workgroup configuration, you must [disable security](specifying-the-authentication-protocol.md) on each queued application accessed in this configuration by selecting **Do not authenticate messages** on the **Queuing** tab for the COM+ application's **Properties** dialog, using the Component Services administrative tool.</span></span> <span data-ttu-id="3211d-106">Это должно быть выполнено только в доверенной сети и должно выполняться как на клиенте, так и на сервере, если приложение уже было экспортировано.</span><span class="sxs-lookup"><span data-stu-id="3211d-106">This should be done only on a trusted network and must be done at both client and server if the application has already been exported.</span></span>

 

 



