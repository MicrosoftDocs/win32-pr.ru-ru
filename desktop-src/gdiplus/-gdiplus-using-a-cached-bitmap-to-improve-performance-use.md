---
description: Изображения и растровые объекты хранят изображения в независимом от устройства формате.
ms.assetid: 42e2b664-197c-4c54-9220-b6231d6439d0
title: Использование кэшированного точечного рисунка для повышения производительности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ffee17a2c8d564a38235cc83d204eacc9b4edf2e8070cb5971d55f1f991169f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036332"
---
# <a name="using-a-cached-bitmap-to-improve-performance"></a>Использование кэшированного точечного рисунка для повышения производительности

[**Изображения**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) и [**растровые**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) объекты хранят изображения в независимом от устройства формате. Объект [**качедбитмап**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) сохраняет изображение в формате текущего устройства вывода. Визуализация изображения, хранящегося в объекте **качедбитмап** , выполняется быстро, так как время обработки не тратится на преобразование изображения в формат, необходимый для устройства отображения.

В следующем примере создается объект [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) и объект [**качедбитмап**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) из файла Texture.jpg. **Точечный рисунок** и **качедбитмап** составляют 30 000 раз. При выполнении кода вы увидите, что изображения **качедбитмап** будут отображаться значительно быстрее, чем **растровые** изображения.


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
> Объект [**качедбитмап**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) соответствует формату устройства дисплея на момент создания объекта **качедбитмап** . Если пользователь программы изменяет параметры экрана, код должен создать новый объект **качедбитмап** . Метод **DrawImage** завершится ошибкой, если передать его объекту **качедбитмап** , созданному до изменения в формате вывода.

 

 

 



