---
title: Параметр настройки клавиатуры
description: Параметр настройки клавиатуры указывает, что пользователь использует клавиатуру вместо мыши, поэтому приложения должны отображать интерфейсы клавиатуры, которые в противном случае были бы скрыты.
ms.assetid: dc3c02d2-a350-4a86-a0b0-9dbb83880029
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802d4ff76efae985cc07b6fe42f9d6b53cdf0b53
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413208"
---
# <a name="keyboard-preference-parameter"></a><span data-ttu-id="c8fe0-103">Параметр настройки клавиатуры</span><span class="sxs-lookup"><span data-stu-id="c8fe0-103">Keyboard preference parameter</span></span>

<span data-ttu-id="c8fe0-104">Параметр настройки клавиатуры указывает, что пользователь использует клавиатуру вместо мыши, поэтому приложения должны отображать интерфейсы клавиатуры, которые в противном случае были бы скрыты.</span><span class="sxs-lookup"><span data-stu-id="c8fe0-104">The keyboard preference parameter indicates that the user relies on the keyboard instead of the mouse, so applications should display keyboard interfaces that would otherwise be hidden.</span></span>

<span data-ttu-id="c8fe0-105">Пользователь управляет параметром настройки клавиатуры с помощью центра специальных возможностей в панели управления или другого приложения для настройки среды.</span><span class="sxs-lookup"><span data-stu-id="c8fe0-105">The user controls the setting of the keyboard preference parameter by using the Ease of Access Center in Control Panel, or another application for customizing the environment.</span></span> <span data-ttu-id="c8fe0-106">Приложения используют флаги **SPI \_ Жеткэйбоардпреф** и **SPI \_ сеткэйбоардпреф** с функцией [**системпараметерсинфо**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) для получения и задания параметра настройки клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="c8fe0-106">Applications use the **SPI\_GETKEYBOARDPREF** and **SPI\_SETKEYBOARDPREF** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to get and set the keyboard preference parameter.</span></span>

<span data-ttu-id="c8fe0-107">Кроме того, в Windows 2000 пользователи могут задать параметр, указывающий, всегда ли подчеркнуты клавиши доступа в меню.</span><span class="sxs-lookup"><span data-stu-id="c8fe0-107">Additionally, on Windows 2000, users can set a parameter that indicates whether menu access keys are always underlined.</span></span> <span data-ttu-id="c8fe0-108">Приложения используют флаги **SPI \_ Жетменуундерлинес** и **SPI \_ сетменуундерлинес** с функцией [**системпараметерсинфо**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) для получения и задания параметра подчеркивания меню.</span><span class="sxs-lookup"><span data-stu-id="c8fe0-108">Applications use the **SPI\_GETMENUUNDERLINES** and **SPI\_SETMENUUNDERLINES** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to get and set the menu underlines parameter.</span></span>

<span data-ttu-id="c8fe0-109">Когда приложение получает сообщение [**WM \_ сеттингчанже**](/windows/desktop/winmsg/wm-settingchange) в качестве параметра клавиатуры или подчеркивания меню, рекомендуется, чтобы приложение вызывало [**системпараметерсинфо**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) для обновления информации для обоих параметров.</span><span class="sxs-lookup"><span data-stu-id="c8fe0-109">When an application receives a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message for either the keyboard preference or menu underline parameter, it is recommended that the application call [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) to update the information for both parameters.</span></span>

<span data-ttu-id="c8fe0-110">Обратите внимание, что **SPI \_ жетменуундерлинес** совпадает с **SPI \_ жеткэйбоардкуес**, а **SPI \_ сетменуундерлинес** совпадает с **SPI \_ сеткэйбоардкуес**.</span><span class="sxs-lookup"><span data-stu-id="c8fe0-110">Note that **SPI\_GETMENUUNDERLINES** is the same as **SPI\_GETKEYBOARDCUES**, and **SPI\_SETMENUUNDERLINES** is the same as **SPI\_SETKEYBOARDCUES**.</span></span>

 

 