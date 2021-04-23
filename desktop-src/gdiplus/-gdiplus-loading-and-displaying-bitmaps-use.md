---
description: Для отображения растрового изображения (точечного рисунка) на экране необходим объект изображения и графический объект.
ms.assetid: 8c1a26d9-b640-4f38-8276-10c4464525f2
title: Загрузка и отображение растровых изображений
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: ab2405462db5017215893d50d93dc0b228633cfb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104987422"
---
# <a name="loading-and-displaying-bitmaps"></a><span data-ttu-id="375c3-103">Загрузка и отображение растровых изображений</span><span class="sxs-lookup"><span data-stu-id="375c3-103">Loading and displaying bitmaps</span></span>

<span data-ttu-id="375c3-104">См. также [пример приложения GDI+ с средством просмотра WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus).</span><span class="sxs-lookup"><span data-stu-id="375c3-104">Also see the [WIC Viewer GDI+ sample app](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus).</span></span>

<span data-ttu-id="375c3-105">Для отображения растрового изображения (точечного рисунка) на экране необходим объект [**изображения**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) и [**графический**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект.</span><span class="sxs-lookup"><span data-stu-id="375c3-105">To display a raster image (bitmap) on the screen, you need an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="375c3-106">Передайте имя файла (или указатель на поток) в конструктор **изображений** .</span><span class="sxs-lookup"><span data-stu-id="375c3-106">Pass the name of a file (or a pointer to a stream) to an **Image** constructor.</span></span> <span data-ttu-id="375c3-107">После создания объекта **Image** передайте адрес этого объекта **изображения** методу **DrawImage** **графического** объекта.</span><span class="sxs-lookup"><span data-stu-id="375c3-107">After you have created an **Image** object, pass the address of that **Image** object to the **DrawImage** method of a **Graphics** object.</span></span>

<span data-ttu-id="375c3-108">В следующем примере создается объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) из файла JPEG, а затем изображение рисуется с помощью левого верхнего угла в (60, 10):</span><span class="sxs-lookup"><span data-stu-id="375c3-108">The following example creates an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from a JPEG file and then draws the image with its upper-left corner at (60, 10):</span></span>

```cpp
Image image(L"Grapes.jpg");
graphics.DrawImage(&image, 60, 10);
```

<span data-ttu-id="375c3-109">На следующем рисунке показано изображение, отображаемое в указанном месте.</span><span class="sxs-lookup"><span data-stu-id="375c3-109">The following illustration shows the image drawn at the specified location.</span></span>

![<span data-ttu-id="375c3-110">снимок экрана: окно, содержащее изображение, с выноской точки отсчета</span><span class="sxs-lookup"><span data-stu-id="375c3-110">screen shot of a window that contains an image, with a callout for the origin point</span></span> ](images/imageposition1.png)

<span data-ttu-id="375c3-111">Класс [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) предоставляет базовые методы для загрузки и отображения растровых изображений и векторных изображений.</span><span class="sxs-lookup"><span data-stu-id="375c3-111">The [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class provides basic methods for loading and displaying raster images and vector images.</span></span> <span data-ttu-id="375c3-112">Класс [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) , который наследует от класса **Image** , предоставляет более специализированные методы для загрузки, отображения и манипулирования растровыми изображениями.</span><span class="sxs-lookup"><span data-stu-id="375c3-112">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class, which inherits from the **Image** class, provides more specialized methods for loading, displaying, and manipulating raster images.</span></span> <span data-ttu-id="375c3-113">Например, можно создать **растровый** объект из маркера значка (Хикон).</span><span class="sxs-lookup"><span data-stu-id="375c3-113">For example, you can construct a **Bitmap** object from an icon handle (HICON).</span></span>

<span data-ttu-id="375c3-114">В следующем примере показано получение маркера для значка, а затем использование этого маркера для создания объекта [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) .</span><span class="sxs-lookup"><span data-stu-id="375c3-114">The following example obtains a handle to an icon and then uses that handle to construct a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="375c3-115">Код отображает значок, передавая адрес объекта **Bitmap** методу **DrawImage** [**графического**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта.</span><span class="sxs-lookup"><span data-stu-id="375c3-115">The code displays the icon by passing the address of the **Bitmap** object to the **DrawImage** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

```cpp
HICON hIcon = LoadIcon(NULL, IDI_APPLICATION);
Bitmap bitmap(hIcon);
graphics.DrawImage(&bitmap, 10, 10);
```

## <a name="see-also"></a><span data-ttu-id="375c3-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="375c3-116">See also</span></span>

[<span data-ttu-id="375c3-117">Пример приложения GDI+ для средства просмотра WIC</span><span class="sxs-lookup"><span data-stu-id="375c3-117">WIC Viewer GDI+ sample app</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus)
