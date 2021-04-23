---
description: Система обрабатывает цвета в точечных рисунках иначе, чем цвета в перьях, кистях и тексте.
ms.assetid: c315dd6e-87ee-4905-b193-186ea580ac0a
title: Цвет в точечных рисунках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 834744f35ccc8bd0c8714fa5bbb438b59c8b8db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155663"
---
# <a name="color-in-bitmaps"></a><span data-ttu-id="4a618-103">Цвет в точечных рисунках</span><span class="sxs-lookup"><span data-stu-id="4a618-103">Color in Bitmaps</span></span>

<span data-ttu-id="4a618-104">Система обрабатывает цвета в точечных рисунках иначе, чем цвета в перьях, кистях и тексте.</span><span class="sxs-lookup"><span data-stu-id="4a618-104">The system handles colors in bitmaps differently than colors in pens, brushes, and text.</span></span> <span data-ttu-id="4a618-105">Совместимые точечные рисунки, созданные с помощью функции [**креатебитмап**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) или [**креатекомпатиблебитмап**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , относятся к конкретному устройству и сохраняются в формате, зависящем от устройства.</span><span class="sxs-lookup"><span data-stu-id="4a618-105">Compatible bitmaps, created by using the [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) or [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) function, are device specific and retain color information in a device-dependent format.</span></span> <span data-ttu-id="4a618-106">Значения цвета не используются, а цвета не подчиняются приближениям и Дизеринг.</span><span class="sxs-lookup"><span data-stu-id="4a618-106">No color values are used, and the colors are not subject to approximations and dithering.</span></span>

<span data-ttu-id="4a618-107">Растровые изображения, независимые от устройства (DIB), сомещают сведения о цвете как значения цвета или индексы цветовой палитры.</span><span class="sxs-lookup"><span data-stu-id="4a618-107">Device-independent bitmaps (DIBs) retain color information either as color values or color palette indexes.</span></span> <span data-ttu-id="4a618-108">Если используются значения цвета, то цвета подчиняются приближениям, но не Дизеринг.</span><span class="sxs-lookup"><span data-stu-id="4a618-108">If color values are used, the colors are subject to approximation, but not dithering.</span></span> <span data-ttu-id="4a618-109">Индексы палитры цветов можно использовать только с устройствами, поддерживающими цветовые палитры.</span><span class="sxs-lookup"><span data-stu-id="4a618-109">Color palette indexes can only be used with devices that support color palettes.</span></span> <span data-ttu-id="4a618-110">Несмотря на то, что система не является приблизительным или смешением цветов, определенных индексами, итоговый цвет может отличаться от предполагаемого, поскольку индексы дают действительные результаты только в контексте цветовой палитры, которая была текущей на момент создания точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="4a618-110">Although the system does not approximate or dither colors identified by indexes, the resulting color may be different than that intended, because the indexes yield valid results only in the context of the color palette that was current at the time the bitmap was created.</span></span> <span data-ttu-id="4a618-111">Значение, если палитра изменяется, поэтому цвета в растровом изображении.</span><span class="sxs-lookup"><span data-stu-id="4a618-111">If the palette changes, so do the colors in the bitmap.</span></span> <span data-ttu-id="4a618-112">Дополнительные сведения о индексах палитры см. в разделе [Палитра по умолчанию](default-palette.md) и [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex).</span><span class="sxs-lookup"><span data-stu-id="4a618-112">For more information on palette indexes, see [Default Palette](default-palette.md) and [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex).</span></span>

<span data-ttu-id="4a618-113">Помимо ссылки на логическую палитру, приложение может также ссылаться на значение в таблице цветов DIB.</span><span class="sxs-lookup"><span data-stu-id="4a618-113">In addition to referencing the logical palette, an application can also reference a value in a DIB color table.</span></span> <span data-ttu-id="4a618-114">Чтобы выбрать цвет в таблице цветов DIB, вызовите [**дибиндекс**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex).</span><span class="sxs-lookup"><span data-stu-id="4a618-114">To select a color in a DIB color table, call [**DIBINDEX**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex).</span></span> <span data-ttu-id="4a618-115">Обратите внимание, что это возможно только для контекста устройства, в котором выбран DIB.</span><span class="sxs-lookup"><span data-stu-id="4a618-115">Note that this is only possible for a device context that has a DIB selected into it.</span></span>

 

 



