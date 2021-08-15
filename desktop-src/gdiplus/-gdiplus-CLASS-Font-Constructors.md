---
description: В этом разделе перечислены конструкторы класса Font. Полный список классов см. в разделе класс Font.
ms.assetid: a0169751-50f6-41d9-bd59-3c85aec1bb78
title: Конструкторы Font. Font
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ff876120655adcf58318a471ed66ddfa4502d625305d9fda37f01c966e19e0cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977904"
---
# <a name="fontfont-constructors"></a>Конструкторы Font. Font

В этом разделе перечислены конструкторы класса [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) . Полный список классов см. в разделе **класс Font**.

### <a name="overload-list"></a>Список перегрузок



| Конструктор                                                                                                                   | Описание                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Шрифт (HDC, ХФОНТ)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont))                                                                | Создает объект [**font:: font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont)) косвенно из логического шрифта GDI с помощью маркера для структуры **LOGFONT** GDI.<br/>                                                                                                                                   |
| [**Шрифт (HDC, ЛОГФОНТА \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta))                                            | Создает объект [**font:: font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta)) непосредственно из логического шрифта GDI. Логический шрифт GDI является структурой **логфонта** , которая является символьной версией логического шрифта в однобайтовой кодировке. Этот конструктор предназначен для совместимости с GDI.<br/> |
| [**Шрифт (HDC, ЛОГФОНТВ \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw))                                            | Создает объект [**font:: font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw)) непосредственно из логического шрифта GDI. Логический шрифт GDI является структурой **логфонтв** , которая является версией логического шрифта в расширенных символах. Этот конструктор предназначен для совместимости с GDI.<br/>     |
| [**Шрифт (FontFamily \* , Real, int, Unit)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit))                                | Создает объект [**font:: font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit)) на основе объекта [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) , размера, стиля шрифта и единицы измерения.<br/>                                                                               |
| [**Font (WCHAR \* , вещественное, int, Unit, фонтколлектион \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) | Создает объект [**font:: font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) на основе семейства шрифтов, размера, стиля шрифта, единицы измерения и объекта [**фонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) .<br/>                                     |
| [**Шрифт (HDC)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc))                                                                            | Создает объект [**font:: font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc)) на основе объекта шрифта GDI, выбранного в данный момент в указанном контексте устройства. Этот конструктор предназначен для совместимости с GDI. <br/>                                                                           |



 

 
