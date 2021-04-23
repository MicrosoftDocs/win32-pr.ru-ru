---
title: Запуск и остановка локатора Майкрософт
description: Библиотеки времени выполнения RPC автоматически запускают локатор Майкрософт при необходимости. Можно вручную закрыть и запустить локатор, если, например, необходимо очистить базу данных при отладке распределенного приложения.
ms.assetid: 06b50a9f-b640-45b2-86e2-2bcea6c16c5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433ffdb11e86b06ee53d9b01f7f7755758538f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067259"
---
# <a name="starting-and-stopping-microsoft-locator"></a><span data-ttu-id="3a09e-104">Запуск и остановка локатора Майкрософт</span><span class="sxs-lookup"><span data-stu-id="3a09e-104">Starting and Stopping Microsoft Locator</span></span>

<span data-ttu-id="3a09e-105">Библиотеки времени выполнения RPC автоматически запускают локатор Майкрософт при необходимости.</span><span class="sxs-lookup"><span data-stu-id="3a09e-105">The RPC run-time libraries automatically start Microsoft Locator when necessary.</span></span> <span data-ttu-id="3a09e-106">Можно вручную закрыть и запустить локатор, если, например, необходимо очистить базу данных при отладке распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="3a09e-106">You can manually stop and start the Locator if, for example, you need to clear the database while debugging a distributed application.</span></span>

<span data-ttu-id="3a09e-107">**Отключение и запуск локатора Майкрософт**</span><span class="sxs-lookup"><span data-stu-id="3a09e-107">**To stop and start Microsoft Locator**</span></span>

1.  <span data-ttu-id="3a09e-108">В панели управления щелкните значок службы.</span><span class="sxs-lookup"><span data-stu-id="3a09e-108">From Control Panel, click the Services icon.</span></span>

    <span data-ttu-id="3a09e-109">Откроется диалоговое окно **службы** .</span><span class="sxs-lookup"><span data-stu-id="3a09e-109">The **Services** dialog box appears.</span></span>

2.  <span data-ttu-id="3a09e-110">В диалоговом окне **Служба** выберите **Локатор Майкрософт** и нажмите кнопку **запустить** или **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="3a09e-110">In the **Service** dialog box, select **Microsoft Locator** and then click **Start** or **Stop**.</span></span>

<span data-ttu-id="3a09e-111">Кроме того, можно запускать и прекращать работу локатора Майкрософт из командной строки. для этого введите следующее:</span><span class="sxs-lookup"><span data-stu-id="3a09e-111">You can also start and stop Microsoft Locator from the command line by typing:</span></span>

<span data-ttu-id="3a09e-112">**NET \[ Start/ \] рпклокатор завершения**</span><span class="sxs-lookup"><span data-stu-id="3a09e-112">**net \[start/stop\] rpclocator**</span></span>

<span data-ttu-id="3a09e-113">Только администратор может запустить локатор Майкрософт после его остановки.</span><span class="sxs-lookup"><span data-stu-id="3a09e-113">Only an administrator can start Microsoft Locator once it is stopped.</span></span> <span data-ttu-id="3a09e-114">Если она остановлена, она будет перезапущена при необходимости в библиотеках времени выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="3a09e-114">If stopped, it will be restarted as necessary by the RPC run-time libraries.</span></span>

 

 




