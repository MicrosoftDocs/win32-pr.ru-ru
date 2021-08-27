---
title: Копирование отдельных кадров из изображения с несколькими кадрами
description: В следующем примере извлекаются отдельные кадры из файла TIFF с несколькими кадрами.
ms.assetid: dfed0b61-2230-4911-a642-0a6e4beb08d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8398df806ad56b65114b0cc9a986ea53061183fa4658872b65b7d08ef7e38a9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115104"
---
# <a name="copy-individual-frames-from-a-multiple-frame-image"></a>Копирование отдельных кадров из изображения с несколькими кадрами

В следующем примере извлекаются отдельные кадры из файла TIFF с несколькими кадрами. При создании TIFF-файла отдельные кадры добавляются в измерение страницы (см. раздел [Создание и сохранение Multiple-Frame образа](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)). Код отображает каждую из четырех страниц и сохраняет каждую страницу в отдельный файл на диске PNG.

Код конструирует объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) из файла TIFF с несколькими кадрами. Чтобы получить отдельные кадры (страницы), код вызывает метод [**Image:: селектактивефраме**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) этого объекта **Image** . Первый аргумент, передаваемый методу **Image:: селектактивефраме** , представляет собой адрес GUID, указывающий измерение, в котором кадры были ранее добавлены в файл TIFF с несколькими кадрами. Идентификатор GUID Фрамедименсионпаже определен в Гдиплусимагинг. h. Другими идентификаторами GUID, определенными в этом файле заголовка, являются Фрамедименсионтиме и Фрамедименсионресолутион. Второй аргумент, передаваемый методу **Image:: селектактивефраме** , — это Отсчитываемый от нуля индекс нужной страницы.

Код полагается на вспомогательную функцию Жетенкодерклсид, которая показана в примере [получения идентификатора класса для кодировщика](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


```
GUID   pageGuid = FrameDimensionPage;
CLSID  encoderClsid;
Image  multi(L"Multiframe.tif");

// Get the CLSID of the PNG encoder.
GetEncoderClsid(L"image/png", &encoderClsid);

// Display and save the first page (index 0).
multi.SelectActiveFrame(&pageGuid, 0);
graphics.DrawImage(&multi, 10, 10);
multi.Save(L"Page0.png", &encoderClsid, NULL);

// Display and save the second page.
multi.SelectActiveFrame(&pageGuid, 1);
graphics.DrawImage(&multi, 200, 10);
multi.Save(L"Page1.png", &encoderClsid, NULL);

// Display and save the third page.
multi.SelectActiveFrame(&pageGuid, 2);
graphics.DrawImage(&multi, 10, 150);
multi.Save(L"Page2.png", &encoderClsid, NULL);

// Display and save the fourth page.
multi.SelectActiveFrame(&pageGuid, 3);
graphics.DrawImage(&multi, 200, 150);
multi.Save(L"Page3.png", &encoderClsid, NULL);
```



На следующем рисунке показаны отдельные страницы, отображаемые в приведенном выше коде.

![Иллюстрация, демонстрирующая геометрическую форму, цветную фотографию, монохромную фотографию и другую геометрическую форму](images/multiframe1.png)

 

 



