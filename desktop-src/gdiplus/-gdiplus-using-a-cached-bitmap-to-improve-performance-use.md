---
description: Изображения и растровые объекты хранят изображения в независимом от устройства формате.
ms.assetid: 42e2b664-197c-4c54-9220-b6231d6439d0
title: Использование кэшированного точечного рисунка для повышения производительности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8e546460741342bcac8f1633e21d104984af9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997454"
---
# <a name="using-a-cached-bitmap-to-improve-performance"></a><span data-ttu-id="b8a6f-103">Использование кэшированного точечного рисунка для повышения производительности</span><span class="sxs-lookup"><span data-stu-id="b8a6f-103">Using a Cached Bitmap to Improve Performance</span></span>

<span data-ttu-id="b8a6f-104">[**Изображения**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) и [**растровые**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) объекты хранят изображения в независимом от устройства формате.</span><span class="sxs-lookup"><span data-stu-id="b8a6f-104">[**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) and [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) objects store images in a device-independent format.</span></span> <span data-ttu-id="b8a6f-105">Объект [**качедбитмап**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) сохраняет изображение в формате текущего устройства вывода.</span><span class="sxs-lookup"><span data-stu-id="b8a6f-105">A [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) object stores an image in the format of the current display device.</span></span> <span data-ttu-id="b8a6f-106">Визуализация изображения, хранящегося в объекте **качедбитмап** , выполняется быстро, так как время обработки не тратится на преобразование изображения в формат, необходимый для устройства отображения.</span><span class="sxs-lookup"><span data-stu-id="b8a6f-106">Rendering an image stored in a **CachedBitmap** object is fast because no processing time is spent converting the image to the format required by the display device.</span></span>

<span data-ttu-id="b8a6f-107">В следующем примере создается объект [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) и объект [**качедбитмап**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) из файла Texture.jpg.</span><span class="sxs-lookup"><span data-stu-id="b8a6f-107">The following example creates a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object and a [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) object from the file Texture.jpg.</span></span> <span data-ttu-id="b8a6f-108">**Точечный рисунок** и **качедбитмап** составляют 30 000 раз.</span><span class="sxs-lookup"><span data-stu-id="b8a6f-108">The **Bitmap** and the **CachedBitmap** are each drawn 30,000 times.</span></span> <span data-ttu-id="b8a6f-109">При выполнении кода вы увидите, что изображения **качедбитмап** будут отображаться значительно быстрее, чем **растровые** изображения.</span><span class="sxs-lookup"><span data-stu-id="b8a6f-109">If you run the code, you will see that the **CachedBitmap** images are drawn substantially faster than the **Bitmap** images.</span></span>


```
Bitmap        bitmap(L"Texture.jpg");
UINT          width = bitmap.GetWidth();
UINT          height = bitmap.GetHeight();
CachedBitmap  cBitmap(&bitmap, &graphics);
int           j, k;
for(j = 0; j < 300; j += 10)
   for(k = 0; k < 1000; ++k)
     graphics.DrawImage(&bitmap, j, j / 2, width, height);
for(j = 0; j < 300; j += 10)
   for(k = 0; k < 1000; ++k)
      graphics.DrawCachedBitmap(&cBitmap, j, 150 + j / 2 );
```



> [!Note]  
> <span data-ttu-id="b8a6f-110">Объект [**качедбитмап**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) соответствует формату устройства дисплея на момент создания объекта **качедбитмап** .</span><span class="sxs-lookup"><span data-stu-id="b8a6f-110">A [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) object matches the format of the display device at the time the **CachedBitmap** object was constructed.</span></span> <span data-ttu-id="b8a6f-111">Если пользователь программы изменяет параметры экрана, код должен создать новый объект **качедбитмап** .</span><span class="sxs-lookup"><span data-stu-id="b8a6f-111">If the user of your program changes the display settings, your code should construct a new **CachedBitmap** object.</span></span> <span data-ttu-id="b8a6f-112">Метод **DrawImage** завершится ошибкой, если передать его объекту **качедбитмап** , созданному до изменения в формате вывода.</span><span class="sxs-lookup"><span data-stu-id="b8a6f-112">The **DrawImage** method will fail if you pass it a **CachedBitmap** object that was created prior to a change in the display format.</span></span>

 

 

 



