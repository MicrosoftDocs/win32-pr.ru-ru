---
description: Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций. Эти плоские функции API упаковываются классом C++ Качедбитмап.
ms.assetid: 06718603-e001-49d4-ac5e-decdd98df42b
title: Функции Качедбитмап
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1835cd668df90a7703a4aebdd60d37d877fe571f376d440080f5668ec3926a26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888334"
---
# <a name="cachedbitmap-functions"></a>Функции Качедбитмап

Windows GDI+ предоставляет плоский API, который состоит из примерно 600 функций, реализованных в Gdiplus.dll и объявленных в гдиплусфлат. h. функции в GDI+ плоском API упаковываются в коллекцию из примерно 40 классов C++. Не рекомендуется напрямую вызывать функции в плоском API. всякий раз, когда вы вызываете GDI+, это необходимо сделать, вызвав методы и функции, предоставляемые оболочками C++. Служба технической поддержки Майкрософт не предоставит поддержку для кода, который напрямую вызывает плоский API. дополнительные сведения об использовании этих методов-оболочек см. в разделе [GDI+ плоский API](-gdiplus-flatapi-flat.md).

Следующие плоские функции API упаковываются классом C++ [**качедбитмап**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) .

## <a name="cachedbitmap-functions-and-corresponding-wrapper-methods"></a>Функции Качедбитмап и соответствующие методы-оболочки



| Плоская функция                                                                                                             | Метод-оболочка                                                                                  | Описание                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Гпстатус ВИНГДИПАПИ Гдипкреатекачедбитмап (Гпбитмап \* Bitmap, гпграфикс \* Graphics, гпкачедбитмап \* \* качедбитмап)   | [**Качедбитмап:: Качедбитмап**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) | Создает объект [**качедбитмап:: качедбитмап**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) на основе [**растрового**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) объекта и [**графического**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта. Кэшированный точечный рисунок принимает данные пикселя из объекта **Bitmap** и сохраняет его в формате, оптимизированном для устройства вывода, связанного с объектом **Graphics** . |
| Гпстатус ВИНГДИПАПИ Гдипделетекачедбитмап (Гпкачедбитмап \* качедбитмап)<br/>                                      | ~ Качедбитмап ()                                                                                 | Очищает ресурсы, используемые объектом [**качедбитмап**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) .                                                                                                                                                                                                                                                                                                                                |
| Гпстатус ВИНГДИПАПИ Гдипдравкачедбитмап (Гпграфикс \* Graphics, гпкачедбитмап \* КАЧЕДБИТМАП, int x, int y)            | [**Графика::D Равкачедбитмап**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap)          | Метод [**Graphics::D равкачедбитмап**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap) рисует изображение, хранящееся в объекте [**качедбитмап**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) .                                                                                                                                                                                                                                |
| UINT ВИНГДИПАПИ Гдипемфтовмфбитс (ХЕНХМЕТАФИЛЕ хемф, UINT cbData16, LPBYTE pData16, INT Имапмоде, INT Ефлагс)<br/> | [**Метафайл:: Емфтовмфбитс**](/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-metafile-emftowmfbits)                         | преобразует метафайл с расширенным форматом в метафайл формат WMF (WMF) и сохраняет преобразованные записи в указанном буфере.                                                                                                                                                                                                                                                                                       |



 

 

