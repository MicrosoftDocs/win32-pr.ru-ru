---
description: Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций, которые реализуются в Gdiplus.dll и объявлены в Гдиплусфлат. h.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: Функции SolidBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7d75e99f46877ce990a985e47bc4b9021faaa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984433"
---
# <a name="solidbrush-functions"></a>Функции SolidBrush

Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций, которые реализуются в Gdiplus.dll и объявлены в Гдиплусфлат. h. Функции в плоском API-интерфейсе GDI+ упаковываются в коллекцию из примерно 40 классов C++. Не рекомендуется вызывать функции непосредственно в неструктурированном API. При каждом вызове GDI+ рекомендуется сделать это, вызвав методы и функции, предоставляемые оболочками C++. Служба технической поддержки Майкрософт не предоставит поддержку для кода, который напрямую вызывает плоский API. Дополнительные сведения об использовании этих методов-оболочек см. в разделе [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Следующие плоские функции API упаковываются классом [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++.

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Функции-кисти и соответствующие методы-оболочки



| Плоская функция                                                                               | Метод-оболочка                                                                                       | Примечания                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Гпстатус ВИНГДИПАПИ Гдипкреатесолидфилл (цвет ARGB, \* \* кисть гпсолидфилл)**<br/>   | [**SolidBrush:: SolidBrush (в цветовой& константы)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_)) | Создает объект [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) на основе цвета |
| **Гпстатус ВИНГДИПАПИ Гдипсетсолидфиллколор ( \* кисть гпсолидфилл, цвет ARGB)**<br/>   | [**SolidBrush:: Сетколор (в цветах констант& Color)**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | Задает цвет сплошной кисти                                                      |
| **Гпстатус ВИНГДИПАПИ Гдипжетсолидфиллколор ( \* кисть гпсолидфилл, \* цвет ARGB)**<br/> | [**SolidBrush::-Color (цвет OUT \* ) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | Возвращает цвет сплошной кисти                                                      |



 

 

 
