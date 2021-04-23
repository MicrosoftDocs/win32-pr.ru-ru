---
description: Windows GDI+ группирует шрифты с одинаковым шрифтом, но различными стилями в семейства шрифтов.
ms.assetid: 57428fae-6af4-47a5-a499-717dc378767a
title: Создание семейств шрифтов и шрифтов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2761923847a15be6b1ad51eec0d683129b70b349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997515"
---
# <a name="constructing-font-families-and-fonts"></a><span data-ttu-id="32033-103">Создание семейств шрифтов и шрифтов</span><span class="sxs-lookup"><span data-stu-id="32033-103">Constructing Font Families and Fonts</span></span>

<span data-ttu-id="32033-104">Windows GDI+ группирует шрифты с одинаковым шрифтом, но различными стилями в семейства шрифтов.</span><span class="sxs-lookup"><span data-stu-id="32033-104">Windows GDI+ groups fonts with the same typeface but different styles into font families.</span></span> <span data-ttu-id="32033-105">Например, семейство шрифтов Arial содержит следующие шрифты:</span><span class="sxs-lookup"><span data-stu-id="32033-105">For example, the Arial font family contains the following fonts:</span></span>

-   <span data-ttu-id="32033-106">Arial Regular</span><span class="sxs-lookup"><span data-stu-id="32033-106">Arial Regular</span></span>
-   <span data-ttu-id="32033-107">Arial Bold</span><span class="sxs-lookup"><span data-stu-id="32033-107">Arial Bold</span></span>
-   <span data-ttu-id="32033-108">Arial курсив</span><span class="sxs-lookup"><span data-stu-id="32033-108">Arial Italic</span></span>
-   <span data-ttu-id="32033-109">Arial полужирный курсив</span><span class="sxs-lookup"><span data-stu-id="32033-109">Arial Bold Italic</span></span>

<span data-ttu-id="32033-110">GDI+ использует четыре стиля для формирования семейств: обычный, полужирный, курсив и полужирный курсив.</span><span class="sxs-lookup"><span data-stu-id="32033-110">GDI+ uses four styles to form families: regular, bold, italic, and bold italic.</span></span> <span data-ttu-id="32033-111">Прилагательные, такие как *Narrow* и *Round* , не считаются стилями. скорее, они являются частью имени семейства.</span><span class="sxs-lookup"><span data-stu-id="32033-111">Adjectives such as *narrow* and *rounded* are not considered styles; rather they are part of the family name.</span></span> <span data-ttu-id="32033-112">Например, Arial Narrow — это семейство шрифтов, элементы которого следующие:</span><span class="sxs-lookup"><span data-stu-id="32033-112">For example, Arial Narrow is a font family whose members are the following:</span></span>

-   <span data-ttu-id="32033-113">Arial — узкие обычные</span><span class="sxs-lookup"><span data-stu-id="32033-113">Arial Narrow Regular</span></span>
-   <span data-ttu-id="32033-114">Arial Narrow</span><span class="sxs-lookup"><span data-stu-id="32033-114">Arial Narrow Bold</span></span>
-   <span data-ttu-id="32033-115">Arial — узкий курсив</span><span class="sxs-lookup"><span data-stu-id="32033-115">Arial Narrow Italic</span></span>
-   <span data-ttu-id="32033-116">Arial Narrow полужирный курсив</span><span class="sxs-lookup"><span data-stu-id="32033-116">Arial Narrow Bold Italic</span></span>

<span data-ttu-id="32033-117">Прежде чем можно будет рисовать текст с помощью GDI+, необходимо создать объект [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) и объект [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="32033-117">Before you can draw text with GDI+, you need to construct a [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object and a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span> <span data-ttu-id="32033-118">Объекты **FontFamily** определяют гарнитуру шрифта (например, Arial), а объект **Font** определяет размер, стиль и единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="32033-118">The **FontFamily** objects specifies the typeface (for example, Arial), and the **Font** object specifies the size, style, and units.</span></span>

<span data-ttu-id="32033-119">В следующем примере создается шрифт Arial с обычным начертанием и размером 16 пикселей:</span><span class="sxs-lookup"><span data-stu-id="32033-119">The following example constructs a regular style Arial font with a size of 16 pixels:</span></span>


```
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 16, FontStyleRegular, UnitPixel);
            
```



<span data-ttu-id="32033-120">В приведенном выше коде первый аргумент, передаваемый конструктору [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) , является адресом объекта [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .</span><span class="sxs-lookup"><span data-stu-id="32033-120">In the preceding code, the first argument passed to the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) constructor is the address of the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object.</span></span> <span data-ttu-id="32033-121">Второй аргумент определяет размер шрифта, измеряемого в единицах, определяемых четвертым аргументом.</span><span class="sxs-lookup"><span data-stu-id="32033-121">The second argument specifies the size of the font measured in units identified by the fourth argument.</span></span> <span data-ttu-id="32033-122">Третий аргумент определяет стиль.</span><span class="sxs-lookup"><span data-stu-id="32033-122">The third argument identifies the style.</span></span>

<span data-ttu-id="32033-123">[\* \* \* \* Унитпиксел \* \* \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) является членом перечисления **единиц измерения** , а [\* \* \* \* фонтстилерегулар \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) \* \* \* является членом перечисления **FontStyle** .</span><span class="sxs-lookup"><span data-stu-id="32033-123">[\*\*\*\*UnitPixel\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) is a member of the **Unit** enumeration, and [\*\*\*\*FontStyleRegular\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) is a member of the **FontStyle** enumeration.</span></span> <span data-ttu-id="32033-124">Оба перечисления объявляются в Гдиплусенумс. h.</span><span class="sxs-lookup"><span data-stu-id="32033-124">Both enumerations are declared in Gdiplusenums.h.</span></span>

 

 



