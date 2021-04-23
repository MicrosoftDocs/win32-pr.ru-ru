---
title: Определение состояния оболочки совместимости
description: Определение состояния оболочки совместимости
ms.assetid: 8D0B633F-9117-4F90-BF8C-AC5F57FCD30B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b830cbb4579aa2e523dfe2ec1129ed9cd10f37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331728"
---
# <a name="determining-shim-status"></a><span data-ttu-id="24f44-103">Определение состояния оболочки совместимости</span><span class="sxs-lookup"><span data-stu-id="24f44-103">Determining shim status</span></span>

## <a name="platforms"></a><span data-ttu-id="24f44-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="24f44-104">Platforms</span></span>

<dl> <span data-ttu-id="24f44-105">Клиенты — Windows 8</span><span class="sxs-lookup"><span data-stu-id="24f44-105">Clients - Windows 8</span></span>  
<span data-ttu-id="24f44-106">Серверы — Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="24f44-106">Servers - Windows Server 2012</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="24f44-107">Описание</span><span class="sxs-lookup"><span data-stu-id="24f44-107">Description</span></span>

<span data-ttu-id="24f44-108">Windows 8 регистрирует события, когда приложения оболочкой совместимости по различным причинам.</span><span class="sxs-lookup"><span data-stu-id="24f44-108">Windows 8 logs events when apps are being shimmed for various reasons.</span></span> <span data-ttu-id="24f44-109">Самый простой способ определить, является ли ваше приложение оболочкой совместимости, — проверить средство просмотра событий.</span><span class="sxs-lookup"><span data-stu-id="24f44-109">The easiest way to determine if your app is being shimmed is to check the event viewer.</span></span> <span data-ttu-id="24f44-110">Последовательно выберите приложения и службы журналы \\ телеметрии Microsoft Windows Application-Experience Program \\ .</span><span class="sxs-lookup"><span data-stu-id="24f44-110">Go to Applications and Services Logs\\Microsoft Windows Application-Experience Program\\Telemetry.</span></span>

## <a name="mitigation"></a><span data-ttu-id="24f44-111">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="24f44-111">Mitigation</span></span>

<span data-ttu-id="24f44-112">Лучший способ выйти из оболочек совместимости небольшого — переименовать исполняемый файл или увеличить основной номер версии на 1 (перекомпилировать исполняемый файл).</span><span class="sxs-lookup"><span data-stu-id="24f44-112">The best way to get yourself out of shimming is to rename the executable or to increase the major version by 1 (recompile the executable).</span></span>

 

 




