---
description: Перо, кисть, точечный рисунок, палитра, область и путь, связанные с контроллером домена, называются его графическими объектами. С каждым из этих объектов связаны следующие атрибуты.
ms.assetid: 95c82efa-257e-4718-9853-7ef10cdfd76c
title: Графические объекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b80aadcb0988e7bd64910d04ecfbf6ec608845d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997359"
---
# <a name="graphic-objects"></a><span data-ttu-id="4873b-104">Графические объекты</span><span class="sxs-lookup"><span data-stu-id="4873b-104">Graphic Objects</span></span>

<span data-ttu-id="4873b-105">Перо, кисть, точечный рисунок, палитра, область и путь, связанные с контроллером домена, называются его графическими объектами.</span><span class="sxs-lookup"><span data-stu-id="4873b-105">The pen, brush, bitmap, palette, region, and path associated with a DC are referred to as its graphic objects.</span></span> <span data-ttu-id="4873b-106">С каждым из этих объектов связаны следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="4873b-106">The following attributes are associated with each of these objects.</span></span>



| <span data-ttu-id="4873b-107">Графический объект</span><span class="sxs-lookup"><span data-stu-id="4873b-107">Graphic object</span></span> | <span data-ttu-id="4873b-108">Связанные атрибуты</span><span class="sxs-lookup"><span data-stu-id="4873b-108">Associated attributes</span></span>                                                               |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4873b-109">Bitmap</span><span class="sxs-lookup"><span data-stu-id="4873b-109">Bitmap</span></span>         | <span data-ttu-id="4873b-110">Размер в байтах; Размеры в пикселях; цветовой формат; схема сжатия; и т. д.</span><span class="sxs-lookup"><span data-stu-id="4873b-110">Size, in bytes; dimensions, in pixels; color-format; compression scheme; and so on.</span></span> |
| <span data-ttu-id="4873b-111">Brush</span><span class="sxs-lookup"><span data-stu-id="4873b-111">Brush</span></span>          | <span data-ttu-id="4873b-112">Стиль, цвет, шаблон и источник.</span><span class="sxs-lookup"><span data-stu-id="4873b-112">Style, color, pattern, and origin.</span></span>                                                  |
| <span data-ttu-id="4873b-113">Палитра</span><span class="sxs-lookup"><span data-stu-id="4873b-113">Palette</span></span>        | <span data-ttu-id="4873b-114">Цвета и размер (или число цветов).</span><span class="sxs-lookup"><span data-stu-id="4873b-114">Colors and size (or number of colors).</span></span>                                              |
| <span data-ttu-id="4873b-115">Шрифт</span><span class="sxs-lookup"><span data-stu-id="4873b-115">Font</span></span>           | <span data-ttu-id="4873b-116">Имя гарнитуры, ширина, высота, вес, кодировка и т. д.</span><span class="sxs-lookup"><span data-stu-id="4873b-116">Typeface name, width, height, weight, character set, and so on.</span></span>                     |
| <span data-ttu-id="4873b-117">Путь</span><span class="sxs-lookup"><span data-stu-id="4873b-117">Path</span></span>           | <span data-ttu-id="4873b-118">Сектор.</span><span class="sxs-lookup"><span data-stu-id="4873b-118">Shape.</span></span>                                                                              |
| <span data-ttu-id="4873b-119">Перо</span><span class="sxs-lookup"><span data-stu-id="4873b-119">Pen</span></span>            | <span data-ttu-id="4873b-120">Стиль, ширина и цвет.</span><span class="sxs-lookup"><span data-stu-id="4873b-120">Style, width, and color.</span></span>                                                            |
| <span data-ttu-id="4873b-121">Region</span><span class="sxs-lookup"><span data-stu-id="4873b-121">Region</span></span>         | <span data-ttu-id="4873b-122">Расположение и измерения.</span><span class="sxs-lookup"><span data-stu-id="4873b-122">Location and dimensions.</span></span>                                                            |



 

<span data-ttu-id="4873b-123">Когда приложение создает контроллер домена, система автоматически сохраняет в нем набор объектов по умолчанию (отсутствует точечный рисунок или путь по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="4873b-123">When an application creates a DC, the system automatically stores a set of default objects in it (there is no default bitmap or path).</span></span> <span data-ttu-id="4873b-124">Приложение может проверить атрибуты объектов по умолчанию, вызвав функции [**жеткуррентобжект**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) и [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) .</span><span class="sxs-lookup"><span data-stu-id="4873b-124">An application can examine the attributes of the default objects by calling the [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) and [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) functions.</span></span> <span data-ttu-id="4873b-125">Приложение может изменить эти значения по умолчанию, создав новый объект и выбрав его в контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="4873b-125">The application can change these defaults by creating a new object and selecting it into the DC.</span></span> <span data-ttu-id="4873b-126">Объект выбирается в контроллере домена путем вызова функции [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) .</span><span class="sxs-lookup"><span data-stu-id="4873b-126">An object is selected into a DC by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span>

<span data-ttu-id="4873b-127">Приложение может установить для текущего цвета кисти указанное значение цвета с помощью [**сетдкбрушколор**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor).</span><span class="sxs-lookup"><span data-stu-id="4873b-127">An application can set the current brush color to a specified color value with [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor).</span></span>

<span data-ttu-id="4873b-128">Функция [**жетдкбрушколор**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) Возвращает цвет кисти контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="4873b-128">The [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) function returns the DC brush color.</span></span> <span data-ttu-id="4873b-129">Функция [**сетдкпенколор**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) задает цвету пера указанное значение цвета.</span><span class="sxs-lookup"><span data-stu-id="4873b-129">The [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) function sets the pen color to a specified color value.</span></span> <span data-ttu-id="4873b-130">Функция [**жетдкпенколор**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor) Возвращает цвет пера контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="4873b-130">The [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor) function returns the DC pen color.</span></span>

 

 



