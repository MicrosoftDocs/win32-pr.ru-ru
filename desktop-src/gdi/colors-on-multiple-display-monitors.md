---
description: Каждый монитор может иметь собственную глубину цвета.
ms.assetid: 8d1ba8d2-b43d-498d-be5a-100fe9fc0f61
title: Цвета на нескольких мониторах монитора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50410631cf0ea3ac0a1b9967f1116809be0a4851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991499"
---
# <a name="colors-on-multiple-display-monitors"></a><span data-ttu-id="7ba6e-103">Цвета на нескольких мониторах монитора</span><span class="sxs-lookup"><span data-stu-id="7ba6e-103">Colors on Multiple Display Monitors</span></span>

<span data-ttu-id="7ba6e-104">Каждый монитор может иметь собственную глубину цвета.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-104">Each monitor can have its own color depth.</span></span> <span data-ttu-id="7ba6e-105">Система автоматически корректирует цвета при перемещении Windows между мониторами с разными глубинами цвета.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-105">The system automatically adjusts colors as windows move across monitors with different color depths.</span></span> <span data-ttu-id="7ba6e-106">В общем случае это дает хорошие результаты.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-106">In general, this produces good results.</span></span> <span data-ttu-id="7ba6e-107">Однако это не всегда оптимально.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-107">However, this is not always optimal.</span></span> <span data-ttu-id="7ba6e-108">Чтобы воспользоваться преимуществами цветовых возможностей различных мониторов, см. следующий раздел [Рисование в нескольких экранных мониторах](painting-on-multiple-display-monitors.md) .</span><span class="sxs-lookup"><span data-stu-id="7ba6e-108">To take advantage of the color capabilities of different monitors, see the [Painting on Multiple Display Monitors](painting-on-multiple-display-monitors.md) section that follows.</span></span>

<span data-ttu-id="7ba6e-109">Чтобы определить, имеют ли все мониторы одинаковый цветовой формат, вызовите [**жетсистемметрикс**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) с SM \_ самедисплайформат.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-109">To determine if all monitors have the same color format, call [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_SAMEDISPLAYFORMAT.</span></span>

<span data-ttu-id="7ba6e-110">Если основным монитором является палеттизед, то [**селектпалетте**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) и [**реализепалетте**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) работают так же, как и раньше, но на всех мониторах.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-110">If the primary monitor is palettized, [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) and [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) work the same as before, but across all monitors.</span></span> <span data-ttu-id="7ba6e-111">Кроме того, синхронизируются палитры всех устройств палеттизед.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-111">In addition, the palettes of all palettized devices are synchronized.</span></span> <span data-ttu-id="7ba6e-112">Если основной монитор не палеттизед, то **селектпалетте** и **реализепалетте** выберет палитру в фоновом режиме, а палеттизед устройства не будут синхронизированы.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-112">If the primary monitor is not palettized, **SelectPalette** and **RealizePalette** will select the palette into the background and palettized devices will not be synchronized.</span></span>

 

 
