---
description: Приложения могут использовать синхронизации Manager для сохранения кэширования файлов и ресурсов в локальной среде и синхронизации на мобильных и настольных компьютерах.
title: Конфигурации мобильных вычислений
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f7a79dab-5996-4984-968c-beebc22da0af
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 682581f20f70317ea7fae6abdf909c2b7d8fbb41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997762"
---
# <a name="mobile-computing-configurations"></a><span data-ttu-id="5079c-103">Конфигурации мобильных вычислений</span><span class="sxs-lookup"><span data-stu-id="5079c-103">Mobile Computing Configurations</span></span>

<span data-ttu-id="5079c-104">Диспетчер синхронизации полезен для компьютеров, настроенных следующим образом.</span><span class="sxs-lookup"><span data-stu-id="5079c-104">The Synchronization Manager is useful for computers configured as follows:</span></span>

-   <span data-ttu-id="5079c-105">Мобильный компьютер, используемый на стыковочный станции в сети с высокой пропускной способностью, но иногда используемый через коммутируемое соединение.</span><span class="sxs-lookup"><span data-stu-id="5079c-105">Mobile computer used in a docking station on a high bandwidth network but occasionally used via a dial-in connection.</span></span>
-   <span data-ttu-id="5079c-106">Мобильный компьютер используется в основном через коммутируемое подключение.</span><span class="sxs-lookup"><span data-stu-id="5079c-106">Mobile computer used mostly via a dial-in connection.</span></span>
-   <span data-ttu-id="5079c-107">Настольный компьютер используется строго через коммутируемое подключение, например компьютер, используемый удаленным пользователем.</span><span class="sxs-lookup"><span data-stu-id="5079c-107">Desktop computer used strictly via a dial-in connection, such as a computer used by a telecommuter.</span></span>
-   <span data-ttu-id="5079c-108">Настольный компьютер используется строго через сеть с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="5079c-108">Desktop computer used strictly via a high bandwidth network.</span></span>

<span data-ttu-id="5079c-109">Несмотря на то, что последний вариант не является типичным сценарием для мобильных устройств, проблемы с доступом к сети могут быть удобными для локального кэширования ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5079c-109">Although the last case is not a typical mobile scenario, latency issues with network access may make it convenient to cache resources locally.</span></span> <span data-ttu-id="5079c-110">Во всех этих конфигурациях приложение может использовать Синкмгр, чтобы хранить файлы и другие ресурсы в локальном кэше и синхронизировать их между Интернетом и автономным использованием.</span><span class="sxs-lookup"><span data-stu-id="5079c-110">In all these configurations, the application can use the SyncMgr to keep files and other resources cached locally and synchronized between online and offline use.</span></span>

 

 



