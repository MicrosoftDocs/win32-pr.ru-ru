---
description: Конфигурация
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: Конфигурация (Windows и сообщения)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac66d2ba25e81582734eb13148d2651b276ea01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272086"
---
# <a name="configuration-windows-and-messages"></a><span data-ttu-id="84996-103">Конфигурация (Windows и сообщения)</span><span class="sxs-lookup"><span data-stu-id="84996-103">Configuration (Windows and Messages)</span></span>

<span data-ttu-id="84996-104">*Отображаемые элементы* — это части окна и отображения, отображаемые на экране монитора системы.</span><span class="sxs-lookup"><span data-stu-id="84996-104">*Display elements* are the parts of a window and the display that appear on the system display screen.</span></span> <span data-ttu-id="84996-105">*Системные метрики* — это измерения различных отображаемых элементов.</span><span class="sxs-lookup"><span data-stu-id="84996-105">*System metrics* are the dimensions of various display elements.</span></span> <span data-ttu-id="84996-106">К типичным системным метрикам относятся ширина границы окна, Высота значка и т. д.</span><span class="sxs-lookup"><span data-stu-id="84996-106">Typical system metrics include the window border width, icon height, and so on.</span></span> <span data-ttu-id="84996-107">Системные метрики также описывают другие аспекты системы, например, установлена ли мышь, поддерживаются двухбайтовые символы или установлена отладочная версия операционной системы.</span><span class="sxs-lookup"><span data-stu-id="84996-107">System metrics also describe other aspects of the system, such as whether a mouse is installed, double-byte characters are supported, or a debugging version of the operating system is installed.</span></span> <span data-ttu-id="84996-108">Функция [**жетсистемметрикс**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) извлекает указанную системную метрику.</span><span class="sxs-lookup"><span data-stu-id="84996-108">The [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function retrieves the specified system metric.</span></span>

<span data-ttu-id="84996-109">Приложения также могут извлекать и задавать цвет элементов окна, таких как меню, полосы прокрутки и кнопки, с помощью функций [**жетсисколор**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) и [**сетсисколорс**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) соответственно.</span><span class="sxs-lookup"><span data-stu-id="84996-109">Applications can also retrieve and set the color of window elements such as menus, scroll bars, and buttons by using the [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) and [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) functions, respectively.</span></span>

<span data-ttu-id="84996-110">Функция [**системпараметерсинфо**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) извлекает или устанавливает различные системные атрибуты, такие как время двойного щелчка, время ожидания экранной заставки, ширина границы окна и шаблон рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="84996-110">The [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function retrieves or sets various system attributes, such as double-click time, screen saver time-out, window border width, and desktop pattern.</span></span> <span data-ttu-id="84996-111">Когда приложение использует **системпараметерсинфо** для установки параметра, изменение происходит немедленно.</span><span class="sxs-lookup"><span data-stu-id="84996-111">When an application uses **SystemParametersInfo** to set a parameter, the change takes place immediately.</span></span> <span data-ttu-id="84996-112">Эта функция также позволяет приложениям обновлять профиль пользователя, поэтому изменения в системе будут сохраняться при перезапуске системы.</span><span class="sxs-lookup"><span data-stu-id="84996-112">This function also enables applications to update the user profile, so changes to the system will be preserved when the system is restarted.</span></span>

 

 
