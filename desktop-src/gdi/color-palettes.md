---
description: Цветовая палитра — это массив, который содержит значения цвета, определяющие цвета, которые в настоящее время можно отображать или рисовать на устройстве вывода.
ms.assetid: 260c5924-d082-4ed2-a8ed-b8a3ad1ca1a9
title: Цветовые палитры (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db6da2aab08d2b482eb678e8541ec166156b78f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155658"
---
# <a name="color-palettes-windows-gdi"></a><span data-ttu-id="7ca71-103">Цветовые палитры (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="7ca71-103">Color Palettes (Windows GDI)</span></span>

<span data-ttu-id="7ca71-104">Цветовая палитра — это массив, который содержит значения цвета, определяющие цвета, которые в настоящее время можно отображать или рисовать на устройстве вывода.</span><span class="sxs-lookup"><span data-stu-id="7ca71-104">A color palette is an array that contains color values identifying the colors that can currently be displayed or drawn on the output device.</span></span> <span data-ttu-id="7ca71-105">Цветовые палитры используются устройствами, которые способны создавать много цветов, но они могут только отображать или нарисовать подмножество из них в любое заданное время.</span><span class="sxs-lookup"><span data-stu-id="7ca71-105">Color palettes are used by devices that are capable of generating many colors but that can only display or draw a subset of these at any given time.</span></span> <span data-ttu-id="7ca71-106">Для таких устройств система поддерживает *системную палитру* для мониторинга текущих цветов устройства и управления ими.</span><span class="sxs-lookup"><span data-stu-id="7ca71-106">For such devices, the system maintains a *system palette* to track and manage the current colors of the device.</span></span> <span data-ttu-id="7ca71-107">Приложения не имеют прямого доступа к системной палитре.</span><span class="sxs-lookup"><span data-stu-id="7ca71-107">Applications do not have direct access to the system palette.</span></span> <span data-ttu-id="7ca71-108">Вместо этого система связывает палитру по умолчанию с каждым контекстом устройства.</span><span class="sxs-lookup"><span data-stu-id="7ca71-108">Instead, the system associates a default palette with each device context.</span></span> <span data-ttu-id="7ca71-109">Приложения могут использовать цвета в палитре по умолчанию или определять собственные цвета, создавая *логические палитры* и связывая их с отдельными контекстами устройств.</span><span class="sxs-lookup"><span data-stu-id="7ca71-109">Applications can use the colors in the default palette or define their own colors by creating *logical palettes* and associating them with individual device contexts.</span></span>

<span data-ttu-id="7ca71-110">Приложение может определить, поддерживает ли устройство цветовые палитры, проверив \_ бит палитры RC в значении растеркапс, возвращаемом функцией [**жетдевицекапс**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) .</span><span class="sxs-lookup"><span data-stu-id="7ca71-110">An application can determine whether a device supports color palettes by checking for the RC\_PALETTE bit in the RASTERCAPS value returned by the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function.</span></span>

 

 



