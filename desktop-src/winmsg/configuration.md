---
description: В этом справочном разделе описывается конфигурация для Windows и сообщений. Сведения о отображаемых элементах и системных метриках.
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: Конфигурация (Windows и сообщения)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa516e87aa7d338d4e2fd46a160fcbd6dadb305
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406347"
---
# <a name="configuration-windows-and-messages"></a><span data-ttu-id="6e82e-104">Конфигурация (Windows и сообщения)</span><span class="sxs-lookup"><span data-stu-id="6e82e-104">Configuration (Windows and Messages)</span></span>

<span data-ttu-id="6e82e-105">*Отображаемые элементы* — это части окна и отображения, отображаемые на экране монитора системы.</span><span class="sxs-lookup"><span data-stu-id="6e82e-105">*Display elements* are the parts of a window and the display that appear on the system display screen.</span></span> <span data-ttu-id="6e82e-106">*Системные метрики* — это измерения различных отображаемых элементов.</span><span class="sxs-lookup"><span data-stu-id="6e82e-106">*System metrics* are the dimensions of various display elements.</span></span> <span data-ttu-id="6e82e-107">К типичным системным метрикам относятся ширина границы окна, Высота значка и т. д.</span><span class="sxs-lookup"><span data-stu-id="6e82e-107">Typical system metrics include the window border width, icon height, and so on.</span></span> <span data-ttu-id="6e82e-108">Системные метрики также описывают другие аспекты системы, например, установлена ли мышь, поддерживаются двухбайтовые символы или установлена отладочная версия операционной системы.</span><span class="sxs-lookup"><span data-stu-id="6e82e-108">System metrics also describe other aspects of the system, such as whether a mouse is installed, double-byte characters are supported, or a debugging version of the operating system is installed.</span></span> <span data-ttu-id="6e82e-109">Функция [**жетсистемметрикс**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) извлекает указанную системную метрику.</span><span class="sxs-lookup"><span data-stu-id="6e82e-109">The [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function retrieves the specified system metric.</span></span>

<span data-ttu-id="6e82e-110">Приложения также могут извлекать и задавать цвет элементов окна, таких как меню, полосы прокрутки и кнопки, с помощью функций [**жетсисколор**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) и [**сетсисколорс**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) соответственно.</span><span class="sxs-lookup"><span data-stu-id="6e82e-110">Applications can also retrieve and set the color of window elements such as menus, scroll bars, and buttons by using the [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) and [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) functions, respectively.</span></span>

<span data-ttu-id="6e82e-111">Функция [**системпараметерсинфо**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) извлекает или устанавливает различные системные атрибуты, такие как время двойного щелчка, время ожидания экранной заставки, ширина границы окна и шаблон рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="6e82e-111">The [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function retrieves or sets various system attributes, such as double-click time, screen saver time-out, window border width, and desktop pattern.</span></span> <span data-ttu-id="6e82e-112">Когда приложение использует **системпараметерсинфо** для установки параметра, изменение происходит немедленно.</span><span class="sxs-lookup"><span data-stu-id="6e82e-112">When an application uses **SystemParametersInfo** to set a parameter, the change takes place immediately.</span></span> <span data-ttu-id="6e82e-113">Эта функция также позволяет приложениям обновлять профиль пользователя, поэтому изменения в системе будут сохраняться при перезапуске системы.</span><span class="sxs-lookup"><span data-stu-id="6e82e-113">This function also enables applications to update the user profile, so changes to the system will be preserved when the system is restarted.</span></span>

 

 
