---
description: Windows GDI+ предоставляет различные уровни качества для рисования текста. Как правило, отрисовка более высокого качества требует больше времени на обработку, чем более низкое качество визуализации.
ms.assetid: 780d97ec-f446-4d19-837f-517a7d6dd27d
title: Сглаживание текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c7b7c59a436db6c16251aa8e866648eed5cc51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997598"
---
# <a name="antialiasing-with-text"></a><span data-ttu-id="f90d5-104">Сглаживание текста</span><span class="sxs-lookup"><span data-stu-id="f90d5-104">Antialiasing with Text</span></span>

<span data-ttu-id="f90d5-105">Windows GDI+ предоставляет различные уровни качества для рисования текста.</span><span class="sxs-lookup"><span data-stu-id="f90d5-105">Windows GDI+ provides various quality levels for drawing text.</span></span> <span data-ttu-id="f90d5-106">Как правило, отрисовка более высокого качества требует больше времени на обработку, чем более низкое качество визуализации.</span><span class="sxs-lookup"><span data-stu-id="f90d5-106">Typically, higher quality rendering takes more processing time than lower quality rendering.</span></span>

<span data-ttu-id="f90d5-107">Уровень качества является свойством класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="f90d5-107">The quality level is a property of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="f90d5-108">Чтобы задать уровень качества, вызовите метод [**Graphics:: сеттекстрендерингхинт**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) объекта **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="f90d5-108">To set the quality level, call the [**Graphics::SetTextRenderingHint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) method of a **Graphics** object.</span></span> <span data-ttu-id="f90d5-109">Метод **Graphics:: сеттекстрендерингхинт** получает один из элементов перечисления [**текстрендерингхинт**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) , который объявлен в гдиплусенумс. h.</span><span class="sxs-lookup"><span data-stu-id="f90d5-109">The **Graphics::SetTextRenderingHint** method receives one of the elements of the [**TextRenderingHint**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) enumeration, which is declared in Gdiplusenums.h.</span></span>

<span data-ttu-id="f90d5-110">GDI+ обеспечивает традиционную сглаживание и новый тип сглаживания на основе технологии Microsoft ClearType, которая доступна только в Windows XP и Windows Server 2003 и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="f90d5-110">GDI+ provides traditional antialiasing and a new kind of antialiasing based on Microsoft ClearType display technology only available on Windows XP and Windows Server 2003 and later versions of Windows.</span></span> <span data-ttu-id="f90d5-111">Сглаживание ClearType повышает удобочитаемость на цветных ЖК-мониторах с цифровым интерфейсом, например мониторами ноутбуков и высококачественным дисплеем с плоским настольным компьютером.</span><span class="sxs-lookup"><span data-stu-id="f90d5-111">ClearType smoothing improves readability on color LCD monitors that have a digital interface, such as the monitors in laptops and high-quality flat desktop displays.</span></span> <span data-ttu-id="f90d5-112">Удобочитаемость на экранах CRT также немного улучшена.</span><span class="sxs-lookup"><span data-stu-id="f90d5-112">Readability on CRT screens is also somewhat improved.</span></span>

<span data-ttu-id="f90d5-113">Технология ClearType зависит от ориентации и порядка полос LCD.</span><span class="sxs-lookup"><span data-stu-id="f90d5-113">ClearType is dependent on the orientation and ordering of the LCD stripes.</span></span> <span data-ttu-id="f90d5-114">В настоящее время технология ClearType реализована только для вертикальных полос, которые упорядочиваются по RGB.</span><span class="sxs-lookup"><span data-stu-id="f90d5-114">Currently, ClearType is implemented only for vertical stripes that are ordered RGB.</span></span> <span data-ttu-id="f90d5-115">Это может быть проблемой, если вы используете планшетный ПК, где дисплей может быть ориентирован в любом направлении, или если вы используете экран, который может быть включен в альбомную ориентацию.</span><span class="sxs-lookup"><span data-stu-id="f90d5-115">This might be a concern if you are using a tablet PC, where the display can be oriented in any direction, or if you are using a screen that can be turned from landscape to portrait.</span></span>

<span data-ttu-id="f90d5-116">В следующем примере рисуется текст с двумя различными параметрами качества:</span><span class="sxs-lookup"><span data-stu-id="f90d5-116">The following example draws text with two different quality settings:</span></span>


```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 32, FontStyleRegular, UnitPixel);
SolidBrush  solidBrush(Color(255, 0, 0, 255));
WCHAR       string1[] = L"SingleBitPerPixel";
WCHAR       string2[] = L"AntiAlias";

graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);
graphics.DrawString(string1, -1, &font, PointF(10.0f, 10.0f), &solidBrush);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
graphics.DrawString(string2, -1, &font, PointF(10.0f, 60.0f), &solidBrush);
            
```



<span data-ttu-id="f90d5-117">На следующем рисунке показаны выходные данные предыдущего кода.</span><span class="sxs-lookup"><span data-stu-id="f90d5-117">The following illustration shows the output of the preceding code.</span></span>

![снимок экрана со строкой, символы которой имеют зубчатые края, напротив одной с гладкими краями](images/fontstext10.png)

 

 



