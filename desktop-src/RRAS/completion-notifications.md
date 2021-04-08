---
title: Уведомления о завершении
description: Диспетчер подключений удаленного доступа возобновляет уведомления о ходе выполнения до завершения операции подключения.
ms.assetid: 2c3b0d03-1cb7-4fa4-a7fa-bcfe623b791f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b949eb7dcc0f09d05d2fb272f4f3d36da40fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068015"
---
# <a name="completion-notifications"></a><span data-ttu-id="452e7-103">Уведомления о завершении</span><span class="sxs-lookup"><span data-stu-id="452e7-103">Completion Notifications</span></span>

<span data-ttu-id="452e7-104">Диспетчер подключений удаленного доступа возобновляет уведомления о ходе выполнения до завершения операции подключения.</span><span class="sxs-lookup"><span data-stu-id="452e7-104">The Remote Access Connection Manager continues progress notifications until the connection operation has been completed.</span></span> <span data-ttu-id="452e7-105">Это происходит в следующих ситуациях.</span><span class="sxs-lookup"><span data-stu-id="452e7-105">This occurs in the following situations:</span></span>

-   <span data-ttu-id="452e7-106">Обработчик получает \_ уведомление раскс Connected или раскс \_ disconnected.</span><span class="sxs-lookup"><span data-stu-id="452e7-106">The handler receives a RASCS\_Connected, or RASCS\_Disconnected notification.</span></span> <span data-ttu-id="452e7-107">Клиентское приложение RAS может выйти без разрыва установленного подключения.</span><span class="sxs-lookup"><span data-stu-id="452e7-107">The RAS client application can exit without breaking any established connection.</span></span>
-   <span data-ttu-id="452e7-108">Возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="452e7-108">An error occurs.</span></span> <span data-ttu-id="452e7-109">Обработчик получает уведомление, указывающее на ошибку и состояние соединения при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="452e7-109">The handler receives a notification indicating the error and the connection state when the error occurred.</span></span> <span data-ttu-id="452e7-110">Клиентское приложение RAS может выйти из программы.</span><span class="sxs-lookup"><span data-stu-id="452e7-110">The RAS client application can exit.</span></span>

<span data-ttu-id="452e7-111">Клиентское приложение RAS не должно считать, что операция подключения завершена после вызова [**рашангуп**](/windows/desktop/api/Ras/nf-ras-rashangupa).</span><span class="sxs-lookup"><span data-stu-id="452e7-111">The RAS client application should not assume the connection operation is complete after calling [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa).</span></span> <span data-ttu-id="452e7-112">Перед выходом необходимо подождать одно из предыдущих условий.</span><span class="sxs-lookup"><span data-stu-id="452e7-112">It should wait for one of the preceding conditions before exiting.</span></span>

 

 




