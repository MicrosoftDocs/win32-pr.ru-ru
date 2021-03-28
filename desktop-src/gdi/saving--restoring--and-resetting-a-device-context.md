---
description: 'Следующие функции позволяют приложению сохранять, восстанавливать и сбрасывать контекст устройства: Саведк, Ресторедк и Ресетдк.'
ms.assetid: 22837876-2665-49c6-908e-80e107fc09f4
title: Сохранение, восстановление и сброс контекста устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2714360c07f4a4eca354ede5b460864cc897e58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985556"
---
# <a name="saving-restoring-and-resetting-a-device-context"></a><span data-ttu-id="a858d-103">Сохранение, восстановление и сброс контекста устройства</span><span class="sxs-lookup"><span data-stu-id="a858d-103">Saving, Restoring, and Resetting a Device Context</span></span>

<span data-ttu-id="a858d-104">Следующие функции позволяют приложению сохранять, восстанавливать и сбрасывать контекст устройства: [**саведк**](/windows/desktop/api/Wingdi/nf-wingdi-savedc), [**ресторедк**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)и [**ресетдк**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca).</span><span class="sxs-lookup"><span data-stu-id="a858d-104">The following functions enable an application to save, restore, and reset a device context: [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc), [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc), and [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca).</span></span> <span data-ttu-id="a858d-105">Функция Саведк записывает в Специальный стек GDI графические объекты текущего контроллера домена, их атрибуты и графические режимы.</span><span class="sxs-lookup"><span data-stu-id="a858d-105">The SaveDC function records on a special GDI stack the current DC's graphic objects and their attributes, and graphic modes.</span></span> <span data-ttu-id="a858d-106">Приложение-рисунок может вызвать эту функцию, прежде чем пользователь начнет Рисование и сохранить исходное состояние приложения, предоставляя пользователю четкое содержание.</span><span class="sxs-lookup"><span data-stu-id="a858d-106">A drawing application can call this function before a user begins drawing and save the application's original state providing a clean slate for the user.</span></span> <span data-ttu-id="a858d-107">Чтобы вернуться к этому исходному состоянию, приложение вызывает функцию Ресторедк.</span><span class="sxs-lookup"><span data-stu-id="a858d-107">To return to this original state, the application calls the RestoreDC function.</span></span>

<span data-ttu-id="a858d-108">[**Ресетдк**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) предоставляется для сброса данных контроллера домена принтера.</span><span class="sxs-lookup"><span data-stu-id="a858d-108">[**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) is provided to reset printer DC data.</span></span> <span data-ttu-id="a858d-109">Приложение вызывает эту функцию для сброса ориентации бумаги, размера бумаги, коэффициента масштабирования выходных данных, количества печатаемых копий, источника бумаги (bin), дуплексного режима и т. д.</span><span class="sxs-lookup"><span data-stu-id="a858d-109">An application calls this function to reset the paper orientation, paper size, output scaling factor, number of copies to be printed, paper source (or bin), duplex mode, and so on.</span></span> <span data-ttu-id="a858d-110">Как правило, приложение вызывает эту функцию после того, как пользователь изменил один из параметров принтера, и система выдала сообщение [**WM \_ девмодечанже**](wm-devmodechange.md) .</span><span class="sxs-lookup"><span data-stu-id="a858d-110">Typically, an application calls this function after a user has changed one of the printer options and the system has issued a [**WM\_DEVMODECHANGE**](wm-devmodechange.md) message.</span></span>

 

 



