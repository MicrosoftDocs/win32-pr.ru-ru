---
description: Цветовые возможности устройств, таких как экраны и принтеры, могут варьироваться от монохромного к тысячам цветов.
ms.assetid: 3d71c24c-77f4-4344-91c3-439052402fae
title: Основные сведения о цвете
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 992953bef75b2bab1f33dbd044a9c80387b5ccd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263690"
---
# <a name="color-basics"></a><span data-ttu-id="fe5ec-103">Основные сведения о цвете</span><span class="sxs-lookup"><span data-stu-id="fe5ec-103">Color Basics</span></span>

<span data-ttu-id="fe5ec-104">Цветовые возможности устройств, таких как экраны и принтеры, могут варьироваться от монохромного к тысячам цветов.</span><span class="sxs-lookup"><span data-stu-id="fe5ec-104">The color capabilities of devices, such as displays and printers, can range from monochrome to thousands of colors.</span></span> <span data-ttu-id="fe5ec-105">Так как приложению может потребоваться создать выходные данные для устройств в этом диапазоне, он должен быть готов к обработке различных возможностей цвета.</span><span class="sxs-lookup"><span data-stu-id="fe5ec-105">Because an application may need to generate output for devices throughout this range, it should be prepared to handle varying color capabilities.</span></span>

<span data-ttu-id="fe5ec-106">Приложение может определить количество цветов, доступных для данного устройства, используя функцию [**жетдевицекапс**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) для получения значения нумколорс.</span><span class="sxs-lookup"><span data-stu-id="fe5ec-106">An application can discover the number of colors available for a given device by using the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function to retrieve the NUMCOLORS value.</span></span> <span data-ttu-id="fe5ec-107">Это значение указывает количество цветов, доступных для использования приложением.</span><span class="sxs-lookup"><span data-stu-id="fe5ec-107">This value specifies the count of colors available for use by the application.</span></span> <span data-ttu-id="fe5ec-108">Обычно это число соответствует физическому свойству выходного устройства, например число красок на принтере или количество различных цветовых сигналов, которые видеоадаптер может передавать монитору.</span><span class="sxs-lookup"><span data-stu-id="fe5ec-108">Usually, this count corresponds to a physical property of the output device, such as the number of inks in the printer or the number of distinct color signals the display adapter can transmit to the monitor.</span></span>

<span data-ttu-id="fe5ec-109">Хотя значение НУМКОЛОРС указывает количество цветов, оно не определяет доступные цвета.</span><span class="sxs-lookup"><span data-stu-id="fe5ec-109">Although the NUMCOLORS value specifies the count of colors, it does not identify what the available colors are.</span></span> <span data-ttu-id="fe5ec-110">Приложение может определить, какие цвета доступны, перечисляя все перья, имеющие \_ сплошной тип PS.</span><span class="sxs-lookup"><span data-stu-id="fe5ec-110">An application can discover what colors are available by enumerating all pens having the PS\_SOLID type.</span></span> <span data-ttu-id="fe5ec-111">Так как драйвер устройства, поддерживающий данное устройство, обычно имеет полный спектр перьев, а система требует, чтобы у твердотельных перьев были только цвета, которые может создать устройство, перечисление этих перьев часто эквивалентно перечислению цветов.</span><span class="sxs-lookup"><span data-stu-id="fe5ec-111">Because the device driver that supports a given device usually has a full range of solid pens and because the system requires that solid pens have only colors that the device can generate, enumerating these pens is often equivalent to enumerating the colors.</span></span> <span data-ttu-id="fe5ec-112">Приложение может перечислить перья с помощью функции [**енумобжектс**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) .</span><span class="sxs-lookup"><span data-stu-id="fe5ec-112">An application can enumerate the pens by using the [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) function.</span></span> <span data-ttu-id="fe5ec-113">Пример кода см. в разделе [перечисление цветов](enumerating-colors.md).</span><span class="sxs-lookup"><span data-stu-id="fe5ec-113">For a code example, see [Enumerating Colors](enumerating-colors.md).</span></span>

<span data-ttu-id="fe5ec-114">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="fe5ec-114">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="fe5ec-115">Значения цвета</span><span class="sxs-lookup"><span data-stu-id="fe5ec-115">Color Values</span></span>](color-values.md)
-   [<span data-ttu-id="fe5ec-116">Приближение цветов и Дизеринг</span><span class="sxs-lookup"><span data-stu-id="fe5ec-116">Color Approximations and Dithering</span></span>](color-approximations-and-dithering.md)
-   [<span data-ttu-id="fe5ec-117">Цвет в точечных рисунках</span><span class="sxs-lookup"><span data-stu-id="fe5ec-117">Color in Bitmaps</span></span>](color-in-bitmaps.md)
-   [<span data-ttu-id="fe5ec-118">Смешение цветов</span><span class="sxs-lookup"><span data-stu-id="fe5ec-118">Color Mixing</span></span>](color-mixing.md)

 

 



