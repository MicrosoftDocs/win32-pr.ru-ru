---
description: 'Приложения Direct3D могут работать в одном из двух режимов: в полноэкранном режиме или в окне.'
ms.assetid: 6ec30c6e-93d1-4b77-9638-86308bbf8f3c
title: Режим с окнами и Full-Screenом (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf51c641446d3f54ceb37c9cc1ac629604f68400
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139551"
---
# <a name="windowed-vs-full-screen-mode-direct3d-9"></a><span data-ttu-id="925eb-103">Режим с окнами и Full-Screenом (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="925eb-103">Windowed vs Full-Screen Mode (Direct3D 9)</span></span>

<span data-ttu-id="925eb-104">Приложения Direct3D могут работать в одном из двух режимов: в полноэкранном режиме или в окне.</span><span class="sxs-lookup"><span data-stu-id="925eb-104">Direct3D applications can run in either of two modes: full-screen or windowed.</span></span>

<span data-ttu-id="925eb-105">Полноэкранный режим означает, что окно, в котором выполняется приложение, охватывает весь рабочий стол, скрывая все работающие приложения (включая среду разработки).</span><span class="sxs-lookup"><span data-stu-id="925eb-105">Full-screen mode means the window that the application runs in covers the entire desktop, hiding all running applications (including your development environment).</span></span> <span data-ttu-id="925eb-106">Игры обычно по умолчанию запускаются в полноэкранном режиме и скрывают все другие работающие приложения, чтобы дать пользователю возможность полностью погрузиться в игру.</span><span class="sxs-lookup"><span data-stu-id="925eb-106">Games typically default to full-screen mode to fully immerse the user in the game by hiding all running applications.</span></span> <span data-ttu-id="925eb-107">Приложение, работающее в режиме с оконным режимом, использует рабочий стол совместно со всеми работающими приложениями.</span><span class="sxs-lookup"><span data-stu-id="925eb-107">An application running in windowed-mode shares the desktop with all running applications.</span></span> <span data-ttu-id="925eb-108">Различия в коде между полноэкранным и оконным режимом минимальны.</span><span class="sxs-lookup"><span data-stu-id="925eb-108">Code differences between full-screen mode and windowed mode are very small.</span></span>

<span data-ttu-id="925eb-109">Поскольку приложение, запущенное в полноэкранном экране, занимает весь экран, для отладки этого приложения требуется отдельный монитор или удаленный отладчик.</span><span class="sxs-lookup"><span data-stu-id="925eb-109">Because an application running in full-screen mode takes over the screen, debugging the application requires either a separate monitor or the use of a remote debugger.</span></span> <span data-ttu-id="925eb-110">Используйте [Панель управления DirectX](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) для включения отладки с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="925eb-110">Use the [DirectX Control Panel Tool](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) to enable multiple-monitor debugging.</span></span> <span data-ttu-id="925eb-111">Одним из преимуществ приложения в оконном режиме является то, что код можно выполнять по шагам в отладчике без дополнительных мониторов или удаленного отладчика.</span><span class="sxs-lookup"><span data-stu-id="925eb-111">One advantage of a windowed-mode application is that you can step through the code in a debugger without multiple monitors or a remote debugger.</span></span>

## <a name="related-topics"></a><span data-ttu-id="925eb-112">См. также</span><span class="sxs-lookup"><span data-stu-id="925eb-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="925eb-113">Устройства Direct3D</span><span class="sxs-lookup"><span data-stu-id="925eb-113">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 



