---
title: Получение системного времени
description: Получение системного времени
ms.assetid: 33dfcd56-11d9-45b9-b983-8354526101a7
keywords:
- Таймеры мультимедиа, системное время
- таймеры, системное время
- системное время
- Функция Тимежеттиме
- Функция Тимежетсистемтиме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89fdcc905569a500afe689658676137c460d19d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487572"
---
# <a name="obtaining-the-system-time"></a><span data-ttu-id="83286-108">Получение системного времени</span><span class="sxs-lookup"><span data-stu-id="83286-108">Obtaining the System Time</span></span>

<span data-ttu-id="83286-109">Как правило, прежде чем приложение начнет использовать службы таймера мультимедиа, оно получает текущее *системное время*.</span><span class="sxs-lookup"><span data-stu-id="83286-109">Typically, before an application begins using the multimedia timer services, it retrieves the current *system time*.</span></span> <span data-ttu-id="83286-110">Системное время — это время в миллисекундах, с момента запуска операционной системы Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="83286-110">The system time is the time, in milliseconds, since the Microsoft Windows operating system was started.</span></span> <span data-ttu-id="83286-111">Для получения системного времени можно использовать функцию [**тимежеттиме**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) или [**тимежетсистемтиме**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) .</span><span class="sxs-lookup"><span data-stu-id="83286-111">You can use the [**timeGetTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) or [**timeGetSystemTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) function to retrieve the system time.</span></span> <span data-ttu-id="83286-112">Эти две функции очень похожи: **тимежеттиме** возвращает системное время, а **Тимежетсистемтиме** заполняет структуру [**ммтиме**](/previous-versions//dd757347(v=vs.85)) с системным временем.</span><span class="sxs-lookup"><span data-stu-id="83286-112">These two functions are very similar: **timeGetTime** returns the system time, and **timeGetSystemTime** fills an [**MMTIME**](/previous-versions//dd757347(v=vs.85)) structure with the system time.</span></span>

 

 