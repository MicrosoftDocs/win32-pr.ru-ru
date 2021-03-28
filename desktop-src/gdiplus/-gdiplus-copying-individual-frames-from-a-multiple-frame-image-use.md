---
title: Копирование отдельных кадров из изображения с несколькими кадрами
description: В следующем примере извлекаются отдельные кадры из файла TIFF с несколькими кадрами.
ms.assetid: dfed0b61-2230-4911-a642-0a6e4beb08d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d6bdb5668bcebb9babcbcb7d07839694750aec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264071"
---
# <a name="copy-individual-frames-from-a-multiple-frame-image"></a><span data-ttu-id="d3f9a-103">Копирование отдельных кадров из изображения с несколькими кадрами</span><span class="sxs-lookup"><span data-stu-id="d3f9a-103">Copy individual frames from a multiple-frame image</span></span>

<span data-ttu-id="d3f9a-104">В следующем примере извлекаются отдельные кадры из файла TIFF с несколькими кадрами.</span><span class="sxs-lookup"><span data-stu-id="d3f9a-104">The following example retrieves the individual frames from a multiple-frame TIFF file.</span></span> <span data-ttu-id="d3f9a-105">При создании TIFF-файла отдельные кадры добавляются в измерение страницы (см. раздел [Создание и сохранение Multiple-Frame образа](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)).</span><span class="sxs-lookup"><span data-stu-id="d3f9a-105">When the TIFF file was created, the individual frames were added to the Page dimension (see [Creating and Saving a Multiple-Frame Image](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)).</span></span> <span data-ttu-id="d3f9a-106">Код отображает каждую из четырех страниц и сохраняет каждую страницу в отдельный файл на диске PNG.</span><span class="sxs-lookup"><span data-stu-id="d3f9a-106">The code displays each of the four pages and saves each page to a separate PNG disk file.</span></span>

<span data-ttu-id="d3f9a-107">Код конструирует объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) из файла TIFF с несколькими кадрами.</span><span class="sxs-lookup"><span data-stu-id="d3f9a-107">The code constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the multiple-frame TIFF file.</span></span> <span data-ttu-id="d3f9a-108">Чтобы получить отдельные кадры (страницы), код вызывает метод [**Image:: селектактивефраме**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) этого объекта **Image** .</span><span class="sxs-lookup"><span data-stu-id="d3f9a-108">To retrieve the individual frames (pages), the code calls the [**Image::SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) method of that **Image** object.</span></span> <span data-ttu-id="d3f9a-109">Первый аргумент, передаваемый методу **Image:: селектактивефраме** , представляет собой адрес GUID, указывающий измерение, в котором кадры были ранее добавлены в файл TIFF с несколькими кадрами.</span><span class="sxs-lookup"><span data-stu-id="d3f9a-109">The first argument passed to the **Image::SelectActiveFrame** method is the address of a GUID that specifies the dimension in which the frames were previously added to the multiple-frame TIFF file.</span></span> <span data-ttu-id="d3f9a-110">Идентификатор GUID Фрамедименсионпаже определен в Гдиплусимагинг. h.</span><span class="sxs-lookup"><span data-stu-id="d3f9a-110">The GUID FrameDimensionPage is defined in Gdiplusimaging.h.</span></span> <span data-ttu-id="d3f9a-111">Другими идентификаторами GUID, определенными в этом файле заголовка, являются Фрамедименсионтиме и Фрамедименсионресолутион.</span><span class="sxs-lookup"><span data-stu-id="d3f9a-111">Other GUIDs defined in that header file are FrameDimensionTime and FrameDimensionResolution.</span></span> <span data-ttu-id="d3f9a-112">Второй аргумент, передаваемый методу **Image:: селектактивефраме** , — это Отсчитываемый от нуля индекс нужной страницы.</span><span class="sxs-lookup"><span data-stu-id="d3f9a-112">The second argument passed to the **Image::SelectActiveFrame** method is the zero-based index of the desired page.</span></span>

<span data-ttu-id="d3f9a-113">Код полагается на вспомогательную функцию Жетенкодерклсид, которая показана в примере [получения идентификатора класса для кодировщика](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="d3f9a-113">The code relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



<span data-ttu-id="d3f9a-114">На следующем рисунке показаны отдельные страницы, отображаемые в приведенном выше коде.</span><span class="sxs-lookup"><span data-stu-id="d3f9a-114">The following illustration shows the individual pages as displayed by the preceding code.</span></span>

![Иллюстрация, демонстрирующая геометрическую форму, цветную фотографию, монохромную фотографию и другую геометрическую форму](images/multiframe1.png)

 

 



