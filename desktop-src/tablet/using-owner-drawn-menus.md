---
description: Использование рисуемых владельцем меню для поддержки функций речи для планшетных ПК.
ms.assetid: fbe2d420-f667-416b-bff3-0fee9ae22203
title: Использование меню Owner-Drawn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f16f9328fadfedccee2c730678fc4cd2d8ab3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809604"
---
# <a name="using-owner-drawn-menus"></a><span data-ttu-id="7251a-103">Использование меню Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="7251a-103">Using Owner-Drawn Menus</span></span>

<span data-ttu-id="7251a-104">При использовании меню, рисуемых владельцем, необходимо сделать имена меню доступными для поддержки речевых функций.</span><span class="sxs-lookup"><span data-stu-id="7251a-104">When using owner-drawn menus, you must make the menu names available to support speech functionality.</span></span> <span data-ttu-id="7251a-105">Это можно сделать двумя способами.</span><span class="sxs-lookup"><span data-stu-id="7251a-105">There are two ways to do this:</span></span>

-   <span data-ttu-id="7251a-106">Предоставьте имя пункта меню с помощью структуры МСААМЕНУИНФО.</span><span class="sxs-lookup"><span data-stu-id="7251a-106">Expose the menu item name by using the MSAAMENUINFO structure.</span></span>
-   <span data-ttu-id="7251a-107">Укажите параметр для замены графических меню стандартными текстовыми меню, если активна вспомогательная функция.</span><span class="sxs-lookup"><span data-stu-id="7251a-107">Provide an option to replace graphic menus with standard text menus when an accessibility aid is active.</span></span> <span data-ttu-id="7251a-108">Если функция [**системпараметерсинфо**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) возвращает **значение true** с параметром *уиактион* , установленным в значение SPI \_ жетскринреадер, используйте стандартные меню. Приложение должно отслеживать \_ сообщение WM сеттингсчанже и реагировать на него, запрашивая состояние этого параметра и соответствующим образом настраивая его отображение.</span><span class="sxs-lookup"><span data-stu-id="7251a-108">If the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function returns **TRUE** with its *uiAction* parameter set to SPI\_GETSCREENREADER, use standard menus.The application should watch for the WM\_SETTINGSCHANGE message and respond by querying the state of this option and adjusting its display appropriately.</span></span> <span data-ttu-id="7251a-109">Например, Microsoft Visual Studio предоставляет возможность использовать стандартные меню вместо пользовательских меню, отображаемых по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7251a-109">For example, Microsoft Visual Studio provides an option to use standard menus instead of the custom menus that are displayed by default.</span></span>

 

 
