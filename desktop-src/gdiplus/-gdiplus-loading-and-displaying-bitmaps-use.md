---
description: Для отображения растрового изображения (точечного рисунка) на экране необходим объект изображения и графический объект.
ms.assetid: 8c1a26d9-b640-4f38-8276-10c4464525f2
title: Загрузка и отображение растровых изображений
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: db3ec9e1d586a585380123aa01d9553ad1f57f60efb93c28d2d974f54d56b249
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115004"
---
# <a name="loading-and-displaying-bitmaps"></a>Загрузка и отображение растровых изображений

см. также [средство просмотра WIC GDI+ пример приложения](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus).

Для отображения растрового изображения (точечного рисунка) на экране необходим объект [**изображения**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) и [**графический**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект. Передайте имя файла (или указатель на поток) в конструктор **изображений** . После создания объекта **Image** передайте адрес этого объекта **изображения** методу **DrawImage** **графического** объекта.

В следующем примере создается объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) из файла JPEG, а затем изображение рисуется с помощью левого верхнего угла в (60, 10):

```cpp
Image image(L"Grapes.jpg");
graphics.DrawImage(&image, 60, 10);
```

На следующем рисунке показано изображение, отображаемое в указанном месте.

![снимок экрана: окно, содержащее изображение, с выноской точки отсчета ](images/imageposition1.png)

Класс [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) предоставляет базовые методы для загрузки и отображения растровых изображений и векторных изображений. Класс [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) , который наследует от класса **Image** , предоставляет более специализированные методы для загрузки, отображения и манипулирования растровыми изображениями. Например, можно создать **растровый** объект из маркера значка (Хикон).

В следующем примере показано получение маркера для значка, а затем использование этого маркера для создания объекта [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) . Код отображает значок, передавая адрес объекта **Bitmap** методу **DrawImage** [**графического**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта.

```cpp
HICON hIcon = LoadIcon(NULL, IDI_APPLICATION);
Bitmap bitmap(hIcon);
graphics.DrawImage(&bitmap, 10, 10);
```

## <a name="see-also"></a>См. также

[средство просмотра WIC GDI+ пример приложения](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus)
