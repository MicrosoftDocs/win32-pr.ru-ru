---
description: Как правило, более старые приложения не требуют изменений для работы в нескольких системах мониторинга.
ms.assetid: 908cf88c-69ed-4855-817d-ba749e14ff85
title: Рекомендации по нескольким мониторам для старых программ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feebb356cb2f9c5480c84f1718b51d6e866ef621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984921"
---
# <a name="multiple-monitor-considerations-for-older-programs"></a><span data-ttu-id="8df15-103">Рекомендации по нескольким мониторам для старых программ</span><span class="sxs-lookup"><span data-stu-id="8df15-103">Multiple Monitor Considerations for Older Programs</span></span>

<span data-ttu-id="8df15-104">Как правило, более старые приложения не требуют изменений для работы в нескольких системах мониторинга.</span><span class="sxs-lookup"><span data-stu-id="8df15-104">Generally, older applications do not need changes to work on multiple monitor systems.</span></span> <span data-ttu-id="8df15-105">В большинстве случаев система выглядит только с одним дисплеем.</span><span class="sxs-lookup"><span data-stu-id="8df15-105">For most, the system will appear to have only one display.</span></span> <span data-ttu-id="8df15-106">Системные метрики соответствуют основным приложениям отображения и полноэкранного режима, отображаемым на основном компьютере.</span><span class="sxs-lookup"><span data-stu-id="8df15-106">System metrics reflect the primary display and fullscreen applications show up on the primary.</span></span> <span data-ttu-id="8df15-107">Система обрабатывает минимизацию, максимизации, меню и диалоговые окна.</span><span class="sxs-lookup"><span data-stu-id="8df15-107">The system handles minimization, maximization, menus, and dialog boxes.</span></span>

<span data-ttu-id="8df15-108">Однако некоторые программы будут иметь проблемы.</span><span class="sxs-lookup"><span data-stu-id="8df15-108">However, some programs will have problems.</span></span> <span data-ttu-id="8df15-109">Некоторые, которые могут иметь проблемы, — это приложения удаленного управления, имеющие прямой доступ к оборудованию, и те, которые установили пакет GDI или видеодрайвер.</span><span class="sxs-lookup"><span data-stu-id="8df15-109">Some that could have problems are remote control applications, those that have direct hardware access, and those that have patched the GDI or DISPLAY driver.</span></span> <span data-ttu-id="8df15-110">В таких случаях пользователю может потребоваться отключить монитор за пределами основного монитора.</span><span class="sxs-lookup"><span data-stu-id="8df15-110">In these cases, the user may be required to disable any monitor beyond the primary monitor.</span></span>

 

 



