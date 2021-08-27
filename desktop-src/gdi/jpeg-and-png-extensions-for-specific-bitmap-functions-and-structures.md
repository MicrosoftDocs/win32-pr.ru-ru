---
description: в некоторых версиях Microsoft Windows функции стретчдибитс и сетдибитстодевице позволяют передавать изображения JPEG и PNG в качестве исходного изображения на устройства печати.
ms.assetid: a38a807d-44df-40a2-8af7-0ce5e532cba2
title: Расширения JPEG и PNG для конкретных функций и структур точечных рисунков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd7dcd2713b737d86f90ab0d49fdf4eed1216f807a4debdffa1963e43a42a9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115294"
---
# <a name="jpeg-and-png-extensions-for-specific-bitmap-functions-and-structures"></a>Расширения JPEG и PNG для конкретных функций и структур точечных рисунков

в некоторых версиях Microsoft Windows функции [**стретчдибитс**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) и [**сетдибитстодевице**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) позволяют передавать изображения JPEG и PNG в качестве исходного изображения на устройства печати. Это расширение не предназначено для обеспечения общего распаковки JPEG-и PNG-изображений в приложения, а позволяет приложениям передавать изображения JPEG и PNG непосредственно на принтеры, поддерживающие изображения JPEG и PNG.

Структуры [**битмапинфохеадер**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) и [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) расширены для предоставления спецификации значений **бикомпрессион** , указывающих, что точечные рисунки являются изображениями в формате JPEG или PNG. Эти значения сжатия допустимы только для [**сетдибитстодевице**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) и [**стретчдибитс**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) , если параметр *HDC* указывает устройство принтера. Для поддержки буферизации в формате метафайлов для принтера приложение не должно полагаться на возвращаемое значение, чтобы определить, поддерживает ли устройство JPEG-или PNG-файл. Приложение должно выдать КУЕРЕСКСУППОРТ с соответствующим escape-символом перед вызовом **сетдибитстодевице** и **стретчдибитс**. Если escape-последовательность проверки завершается неудачно, приложение должно вернуться на встроенную поддержку JPEG или PNG для распаковки изображения в растровое изображение.

 

 
