---
description: В интерфейсе графических устройств (GDI) поддерживаются семь стандартных логических стандартных объектов. Существует также 21 стандартный логический запасной кисти, поддерживаемый интерфейсом управления окнами (пользователь).
ms.assetid: ddbc6d54-47f6-4810-9d3a-feede80f2bed
title: Стандартная кисть
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522337752c2d81a92302d4a6a8f025393db1ce15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985924"
---
# <a name="stock-brush"></a><span data-ttu-id="e7b13-104">Стандартная кисть</span><span class="sxs-lookup"><span data-stu-id="e7b13-104">Stock Brush</span></span>

<span data-ttu-id="e7b13-105">В интерфейсе графических устройств (GDI) поддерживаются семь стандартных логических стандартных объектов.</span><span class="sxs-lookup"><span data-stu-id="e7b13-105">There are seven predefined logical stock brushes maintained by the graphics device interface (GDI).</span></span> <span data-ttu-id="e7b13-106">Существует также 21 стандартный логический запасной кисти, поддерживаемый интерфейсом управления окнами (пользователь).</span><span class="sxs-lookup"><span data-stu-id="e7b13-106">There are also 21 predefined logical stock brushes maintained by the window management interface (USER).</span></span>

<span data-ttu-id="e7b13-107">На следующем рисунке показаны прямоугольники, нарисованные с помощью семи предопределенных стандартных кистей.</span><span class="sxs-lookup"><span data-stu-id="e7b13-107">The following illustration shows rectangles painted by using the seven predefined stock brushes.</span></span>

![Иллюстрация, демонстрирующая семь квадратиков: один черный, три оттенка серого и три, которые выглядят пустыми](images/csbru-03.png)

<span data-ttu-id="e7b13-109">Приложение может получить дескриптор, идентифицирующий одну из семи стандартных кистей, вызвав функцию [**жетстоккобжект**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) , указав тип кисти.</span><span class="sxs-lookup"><span data-stu-id="e7b13-109">An application can retrieve a handle identifying one of the seven stock brushes by calling the [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) function, specifying the brush type.</span></span>

<span data-ttu-id="e7b13-110">21 стандартные кисти, поддерживаемые интерфейсом управления окнами, соответствуют цветам элементов окон, таким как меню, полосы прокрутки и кнопки.</span><span class="sxs-lookup"><span data-stu-id="e7b13-110">The 21 stock brushes maintained by the window management interface correspond to the colors of window elements such as menus, scroll bars, and buttons.</span></span> <span data-ttu-id="e7b13-111">Приложение может получить маркер, идентифицирующий одну из этих кистей, вызвав функцию [**жетсисколорбруш**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush) и указав значение системного цвета.</span><span class="sxs-lookup"><span data-stu-id="e7b13-111">An application can obtain a handle identifying one of these brushes by calling the [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush) function and specifying a system-color value.</span></span> <span data-ttu-id="e7b13-112">Приложение может получить цвет, соответствующий определенному элементу окна, вызвав функцию [**жетсисколор**](/windows/win32/api/winuser/nf-winuser-getsyscolor) .</span><span class="sxs-lookup"><span data-stu-id="e7b13-112">An application can retrieve the color corresponding to a particular window element by calling the [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) function.</span></span> <span data-ttu-id="e7b13-113">Приложение может задать цвет, соответствующий элементу окна, вызвав функцию [**сетсисколорс**](/windows/win32/api/winuser/nf-winuser-setsyscolors) .</span><span class="sxs-lookup"><span data-stu-id="e7b13-113">An application can set the color corresponding to a window element by calling the [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) function.</span></span>

 

 
