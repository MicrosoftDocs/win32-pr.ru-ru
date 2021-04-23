---
description: Windows GDI+ предоставляет несколько классов, образующих основу для рисования текста.
ms.assetid: 12bc38c3-5fbc-4d7b-902c-92a5f5057473
title: Использование текста и шрифтов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f28ec157888dcf45b309237eb0f7eefff17808c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541434"
---
# <a name="using-text-and-fonts"></a><span data-ttu-id="734aa-103">Использование текста и шрифтов</span><span class="sxs-lookup"><span data-stu-id="734aa-103">Using Text and Fonts</span></span>

<span data-ttu-id="734aa-104">Windows GDI+ предоставляет несколько классов, образующих основу для рисования текста.</span><span class="sxs-lookup"><span data-stu-id="734aa-104">Windows GDI+ provides several classes that form the foundation for drawing text.</span></span> <span data-ttu-id="734aa-105">Класс [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) имеет несколько методов [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) , позволяющих задавать различные функции текста, такие как расположение, ограничивающий прямоугольник, шрифт и формат.</span><span class="sxs-lookup"><span data-stu-id="734aa-105">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class has several [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) methods that allow you to specify various features of text, such as location, bounding rectangle, font, and format.</span></span> <span data-ttu-id="734aa-106">В число других классов, участвующих в отрисовке текста, входят [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), [**инсталледфонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection)и [**приватефонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection).</span><span class="sxs-lookup"><span data-stu-id="734aa-106">Other classes that contribute to text rendering include [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection), and [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection).</span></span>

<span data-ttu-id="734aa-107">В следующих разделах текст и шрифты рассматриваются более подробно:</span><span class="sxs-lookup"><span data-stu-id="734aa-107">The following topics cover text and fonts in more detail:</span></span>

-   [<span data-ttu-id="734aa-108">Создание семейств шрифтов и шрифтов</span><span class="sxs-lookup"><span data-stu-id="734aa-108">Constructing Font Families and Fonts</span></span>](-gdiplus-constructing-font-families-and-fonts-use.md)
-   [<span data-ttu-id="734aa-109">Рисование текста</span><span class="sxs-lookup"><span data-stu-id="734aa-109">Drawing Text</span></span>](-gdiplus-drawing-text-use.md)
-   [<span data-ttu-id="734aa-110">Форматирование текста</span><span class="sxs-lookup"><span data-stu-id="734aa-110">Formatting Text</span></span>](-gdiplus-formatting-text-use.md)
-   [<span data-ttu-id="734aa-111">Перечисление установленных шрифтов</span><span class="sxs-lookup"><span data-stu-id="734aa-111">Enumerating Installed Fonts</span></span>](-gdiplus-enumerating-installed-fonts-use.md)
-   [<span data-ttu-id="734aa-112">Создание частной коллекции шрифтов</span><span class="sxs-lookup"><span data-stu-id="734aa-112">Creating a Private Font Collection</span></span>](-gdiplus-creating-a-private-font-collection-use.md)
-   [<span data-ttu-id="734aa-113">Получение метрик шрифтов</span><span class="sxs-lookup"><span data-stu-id="734aa-113">Obtaining Font Metrics</span></span>](-gdiplus-obtaining-font-metrics-use.md)
-   [<span data-ttu-id="734aa-114">Сглаживание текста</span><span class="sxs-lookup"><span data-stu-id="734aa-114">Antialiasing with Text</span></span>](-gdiplus-antialiasing-with-text-use.md)

 

 



