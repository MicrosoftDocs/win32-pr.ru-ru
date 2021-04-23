---
description: После создания библиотеки DLL для получения уведомлений о подключениях необходимо зарегистрировать ее в системе.
ms.assetid: 1a389de1-367d-4b07-a420-4af431d48b7f
title: Регистрация для получения уведомлений о подключении
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812c47ba43fe13e4908a1812f7c67f38a94bce5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813585"
---
# <a name="registering-to-receive-connection-notifications"></a><span data-ttu-id="1e7bf-103">Регистрация для получения уведомлений о подключении</span><span class="sxs-lookup"><span data-stu-id="1e7bf-103">Registering to Receive Connection Notifications</span></span>

<span data-ttu-id="1e7bf-104">После создания библиотеки DLL для получения уведомлений о подключениях необходимо зарегистрировать ее в системе.</span><span class="sxs-lookup"><span data-stu-id="1e7bf-104">After you have created a DLL to receive connection notifications, you must register it with the system.</span></span> <span data-ttu-id="1e7bf-105">Это можно сделать, добавив значение **reg \_ expand \_ SZ** в поле</span><span class="sxs-lookup"><span data-stu-id="1e7bf-105">You do this by adding a **REG\_EXPAND\_SZ** value under the</span></span>

<span data-ttu-id="1e7bf-106">**HKey \_ Локальный \_ компьютер** \\ **система** \\ **CurrentControlSet** \\ **элемент управления** \\ **нетворкпровидер** \\ **нотифеес**</span><span class="sxs-lookup"><span data-stu-id="1e7bf-106">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**Notifyees**</span></span>

<span data-ttu-id="1e7bf-107">ключ.</span><span class="sxs-lookup"><span data-stu-id="1e7bf-107">key.</span></span> <span data-ttu-id="1e7bf-108">Это значение указывает путь к библиотеке DLL, реализующей [API уведомления о соединении](connection-notification-api.md).</span><span class="sxs-lookup"><span data-stu-id="1e7bf-108">This value specifies the path to the DLL that implements the [Connection Notification API](connection-notification-api.md).</span></span>

<span data-ttu-id="1e7bf-109">Значение может иметь любое имя.</span><span class="sxs-lookup"><span data-stu-id="1e7bf-109">The value can have any name.</span></span> <span data-ttu-id="1e7bf-110">Все значения в ключе **нотифеес** рассматриваются как пути к библиотекам DLL, которые получают уведомления о событиях соединения.</span><span class="sxs-lookup"><span data-stu-id="1e7bf-110">All values under the **Notifyees** key are treated as paths to DLLs that are notified of connection events.</span></span> <span data-ttu-id="1e7bf-111">Рекомендуется использовать имя, идентифицирующее библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="1e7bf-111">It is recommended that you use a name that identifies your DLL.</span></span> <span data-ttu-id="1e7bf-112">Это уменьшает вероятность конфликта имен с другими приложениями уведомлений о соединении.</span><span class="sxs-lookup"><span data-stu-id="1e7bf-112">This lessens the chance of a name conflict with other connection notification applications.</span></span>

<span data-ttu-id="1e7bf-113">Дополнительные сведения о создании приложения, которое получает уведомления о подключении, см. в разделе [Получение уведомлений о подключениях](receiving-connection-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="1e7bf-113">For more information about how to create an application that receives connection notifications, see [Receiving Connection Notifications](receiving-connection-notifications.md).</span></span>

 

 



